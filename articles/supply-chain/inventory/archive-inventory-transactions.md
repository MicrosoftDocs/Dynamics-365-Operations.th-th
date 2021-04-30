---
title: เก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง
description: หัวข้อนี้อธิบายวิธีการเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง เพื่อช่วยปรับปรุงประสิทธิภาพของระบบ
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b740da1a8a349f4a1a80b41bf717c388fd3db0c0
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881843"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="283ee-103">เก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="283ee-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="283ee-104">เมื่อเวลาผ่านไป ตารางธุรกรรมของสินค้าคงคลัง (`InventTrans`) จะยังคงเพิ่มขึ้นและใช้พื้นที่ฐานข้อมูลมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="283ee-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="283ee-105">ดังนั้น การสอบถามที่ถูกสร้างขึ้นเทียบกับตารางจะช้าลงทีละน้อย</span><span class="sxs-lookup"><span data-stu-id="283ee-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="283ee-106">หัวข้อนี้อธิบายวิธีการที่คุณสามารถใช้คุณลักษณะ *การเก็บถาวรของธุรกรรมสินค้าคงคลัง* เพื่อเก็บถาวรข้อมูลเกี่ยวกับธุรกรรมของสินค้าคงคลัง เพื่อช่วยปรับปรุงประสิทธิภาพของระบบ</span><span class="sxs-lookup"><span data-stu-id="283ee-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="283ee-107">สามารถเก็บถาวรได้เฉพาะธุรกรรมของสินค้าคงคลังที่อัพเดตทางการเงินในรอบระยะเวลาบัญชีแยกประเภทที่ปิดแล้วที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="283ee-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="283ee-108">หากต้องการเก็บถาวร ธุรกรรมของสินค้าคงคลังขาออกที่อัพเดตทางการเงิน ต้องมีสถานะการตัดสินค้าจากคลังเป็น *ขายแล้ว* และธุรกรรมของสินค้าคงคลังขาเข้าต้องมีสถานะการรับสินค้าเป็น *ซื้อแล้ว*</span><span class="sxs-lookup"><span data-stu-id="283ee-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="283ee-109">เมื่อคุณเก็บถาวรธุรกรรมของสินค้าคงคลัง ธุรกรรมที่เกี่ยวข้องทั้งหมดจะถูกย้ายไปยังตาราง `InventTransArchive`</span><span class="sxs-lookup"><span data-stu-id="283ee-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="283ee-110">ธุรกรรมการออกสินค้าคงคลังและธุรกรรมการรับสต็อกจะถูกเก็บถาวรโดยแยกต่างหาก ตามชุดข้อมูลของรหัสสินค้า (`itemId`) และรหัสมิติสินค้าคงคลัง (`inventDimId`) และธุรกรรมเหล่านั้นจะถูกจัดวางลงในสรุปการตัดสินค้าจากคลังและสรุปธุรกรรมการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="283ee-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="283ee-111">ถ้าชุดของ `itemId` และ `inventDimId` มีธุรกรรมการรับสินค้าหรือการตัดสินค้าจากคลังเพียงธุรกรรมเดียว ธุรกรรมจะไม่ถูกเก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="283ee-112">เปิดใช้งานคุณลักษณะการทำงานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="283ee-112">Turn on the feature in your system</span></span>

<span data-ttu-id="283ee-113">ถ้าระบบของคุณยังไม่ได้รวมคุณลักษณะที่อธิบายไว้ในหัวข้อนี้ ให้ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดคุณลักษณะ *การเก็บถาวรของธุรกรรมสินค้าคงคลัง*</span><span class="sxs-lookup"><span data-stu-id="283ee-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span> <span data-ttu-id="283ee-114">โปรดทราบว่าคุณลักษณะนี้ไม่สามารถปิดใช้งานได้หลังจากที่เปิดใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="283ee-114">Note that this feature cannot be disabled once it has been enabled.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="283ee-115">สิ่งที่ต้องพิจารณาก่อนที่คุณจะเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="283ee-115">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="283ee-116">ก่อนที่คุณจะเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง คุณควรพิจารณาสถานการณ์ทางธุรกิจต่อไปนี้ เนื่องจากจะได้รับผลกระทบจากการดําเนินงาน:</span><span class="sxs-lookup"><span data-stu-id="283ee-116">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="283ee-117">เมื่อคุณตรวจสอบธุรกรรมของสินค้าคงคลังจากเอกสารที่เกี่ยวข้อง เช่น รายการใบสั่งซื้อ รายการเหล่านั้นจะถูกแสดงเป็นเก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-117">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="283ee-118">หากต้องการทบทวนธุรกรรมที่เก็บถาวร คุณต้องไปที่งานล้างข้อมูลธุรกรรม **การบริหารสินค้าคงคลัง \> งานประจำงวด \> การล้างข้อมูล \> การเก็บถาวรของธุรกรรมสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="283ee-118">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="283ee-119">ไม่สามารถยกเลิกการปิดบัญชีสินค้าคงคลังสำหรับรอบระยะเวลาที่เก็บถาวรไว้ได้</span><span class="sxs-lookup"><span data-stu-id="283ee-119">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="283ee-120">ก่อนที่คุณจะสามารถยกเลิกการปิดบัญชีสินค้าคงคลังได้ คุณต้องกลับรายการการเก็บถาวรของธุรกรรมสินค้าคงคลังสำหรับรอบระยะเวลาที่เกี่ยวข้องก่อน</span><span class="sxs-lookup"><span data-stu-id="283ee-120">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="283ee-121">ไม่สามารถทำการแปลงต้นทุนมาตรฐานสำหรับรอบระยะเวลาที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-121">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="283ee-122">ก่อนที่คุณจะสามารถทำการแปลงต้นทุนมาตรฐานได้ คุณต้องกลับรายการการเก็บถาวรของธุรกรรมสินค้าคงคลังสำหรับรอบระยะเวลาที่เกี่ยวข้องก่อน</span><span class="sxs-lookup"><span data-stu-id="283ee-122">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="283ee-123">รายงานสินค้าคงคลังที่มีต้นทางมาจากธุรกรรมสินค้าคงคลังจะได้รับผลกระทบ เมื่อคุณเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="283ee-123">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="283ee-124">รายงานเหล่านี้รวมรายงานอายุหนี้ของสินค้าคงคลังและรายงานมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="283ee-124">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="283ee-125">การคาดการณ์สินค้าคงคลังอาจได้รับผลกระทบ หากมีการรันในระหว่างระยะเวลาในการลงทุนของระยะเวลาที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-125">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="283ee-126">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="283ee-126">Prerequisites</span></span>

<span data-ttu-id="283ee-127">สามารถเก็บถาวรธุรกรรมสินค้าคงคลังได้เฉพาะในระหว่างรอบระยะเวลาที่เป็นไปตามเงื่อนไขต่อไปนี้เท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="283ee-127">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="283ee-128">ต้องปิดรอบระยะเวลาบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="283ee-128">The ledger period must be closed.</span></span>
- <span data-ttu-id="283ee-129">ต้องรันการปิดบัญชีสินค้าคงคลังในวันที่หรือหลังจากวันที่ถึงรอบระยะเวลาของที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-129">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="283ee-130">รอบระยะเวลาต้องเป็นอย่างน้อยหนึ่งปี ก่อนหน้าวันที่เริ่มต้นรอบระยะเวลาของที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-130">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="283ee-131">ต้องไม่มีการคำนวณซ้ำสินค้าคงคลังที่มีอยู่ใดๆ</span><span class="sxs-lookup"><span data-stu-id="283ee-131">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="283ee-132">เก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="283ee-132">Archive inventory transactions</span></span>

<span data-ttu-id="283ee-133">หากต้องการเก็บถาวรธุรกรรมสินค้าคงคลัง ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="283ee-133">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="283ee-134">ไปที่ **การบริหารสินค้าคงคลัง** \> **งานประจำงวด** \> **ล้างข้อมูล** \> **การเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="283ee-134">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="283ee-135">หน้า **การเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง** จะปรากฏขึ้นและแสดงรายการของเรกคอร์ดกระบวนการที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-135">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="283ee-136">![หน้าการเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง](media/archive-inventory-empty.png "หน้าการเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง")</span><span class="sxs-lookup"><span data-stu-id="283ee-136">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="283ee-137">บนบานหน้าต่างการดำเนินการ เลือก **การเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง** เพื่อสร้างการเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="283ee-137">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="283ee-138">ในกล่องโต้ตอบ **การเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง** บน FastTab **พารามิเตอร์** ให้ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="283ee-138">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="283ee-139">**วันที่เริ่มต้นในรอบระยะเวลาบัญชีแยกประเภทที่ปิด** – เลือกวันที่ธุรกรรมแรกสุดที่จะรวมไว้ในที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-139">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="283ee-140">**วันที่สิ้นสุดในรอบระยะเวลาบัญชีแยกประเภทที่ปิด** – เลือกวันที่ธุรกรรมสุดท้ายที่จะรวมไว้ในที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-140">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="283ee-141">![กล่องโต้ตอบการเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง](media/archive-inventory-dates.png "กล่องโต้ตอบการเก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง")</span><span class="sxs-lookup"><span data-stu-id="283ee-141">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="283ee-142">เฉพาะรอบระยะเวลาที่ตรงตาม [เงื่อนไขเบื้องต้น](#prerequisites) เท่านั้นที่จะพร้อมใช้งานในการเลือก</span><span class="sxs-lookup"><span data-stu-id="283ee-142">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="283ee-143">บน FastTab **รันในแบบเบื้องหลัง** ให้ตั้งค่ารายละเอียดการประมวลผลชุดงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="283ee-143">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="283ee-144">ปฏิบัติตามขั้นตอนปกติสำหรับงานของชุดงานใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="283ee-144">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="283ee-145">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="283ee-145">Select **OK**.</span></span>
1. <span data-ttu-id="283ee-146">คุณจะได้รับข้อความเตือนให้คุณยืนยันว่าคุณต้องการดำเนินการต่อหรือไม่</span><span class="sxs-lookup"><span data-stu-id="283ee-146">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="283ee-147">อ่านข้อความอย่างรอบคอบ แล้วจากนั้น เลือก **ใช่** ถ้าคุณต้องการดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="283ee-147">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="283ee-148">คุณจะได้รับข้อความที่ระบุว่างานในการเก็บถาวรของธุรกรรมสินค้าคงคลังของคุณ ได้ถูกเพิ่มเข้าในคิวชุดงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="283ee-148">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="283ee-149">ขณะนี้งานจะเริ่มต้นเก็บถาวรรายการธุรกรรมของสินค้าคงคลังจากรอบระยะเวลาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="283ee-149">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="283ee-150">ดูธุรกรรมสินค้าคงคลังที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-150">View archived inventory transactions</span></span>

<span data-ttu-id="283ee-151">หน้า **การเก็บถาวรข้อมูลของธุรกรรมสินค้าคงคลัง** แสดงประวัติการเก็บถาวรทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="283ee-151">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="283ee-152">แถวแต่ละแถวในกริดแสดงข้อมูล เช่น วันที่ที่มีการสร้างที่เก็บถาวร ผู้ใช้ที่สร้าง และสถานะ</span><span class="sxs-lookup"><span data-stu-id="283ee-152">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="283ee-153">![ประวัติการเก็บถาวรในหน้าการเก็บถาวรข้อมูลของธุรกรรมสินค้าคงคลัง](media/archive-inventory-full.png "ประวัติการเก็บถาวรในหน้าการเก็บถาวรข้อมูลของธุรกรรมสินค้าคงคลัง")</span><span class="sxs-lookup"><span data-stu-id="283ee-153">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="283ee-154">ในรายการแบบหล่นลงที่ด้านบนของหน้า เลือกค่าใดค่าหนึ่งต่อไปนี้เพื่อกรองข้อมูลที่เก็บถาวรซึ่งแสดงในกริด:</span><span class="sxs-lookup"><span data-stu-id="283ee-154">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="283ee-155">**ใช้งานอยู่** – แสดงเฉพาะที่เก็บถาวรที่ใช้งานอยู่ ไม่ใช่ที่เก็บถาวรที่กลับรายการ</span><span class="sxs-lookup"><span data-stu-id="283ee-155">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="283ee-156">**ทั้งหมด** – แสดงที่เก็บถาวรทั้งหมด ทั้งแบบที่ใช้งานอยู่และกลับรายการแล้ว</span><span class="sxs-lookup"><span data-stu-id="283ee-156">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="283ee-157">สำหรับการเก็บถาวรแต่ละรายการในกริด มีการระบุข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="283ee-157">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="283ee-158">**ใช้งานอยู่** – เครื่องหมายถูกบ่งชี้ว่าที่เก็บถาวรใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="283ee-158">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="283ee-159">**วันที่เริ่มต้น** – วันที่ของธุรกรรมที่เก่าที่สุดที่สามารถรวมไว้ในที่เก็บถาวรได้</span><span class="sxs-lookup"><span data-stu-id="283ee-159">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="283ee-160">**วันที่สิ้นสุด** – วันที่ของธุรกรรมล่าสุดที่สามารถรวมไว้ในที่เก็บถาวรได้</span><span class="sxs-lookup"><span data-stu-id="283ee-160">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="283ee-161">**จัดกำหนดการตาม** – บัญชีผู้ใช้ที่สร้างที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-161">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="283ee-162">**ดำเนินการแล้ว** – วันที่ที่สร้างที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-162">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="283ee-163">**กลับรายการ** – เครื่องหมายถูกระบุว่ามีการกลับรายการที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-163">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="283ee-164">**หยุดการอัพเดตปัจจุบัน** – เครื่องหมายถูกบ่งชี้ว่าที่เก็บถาวรอยู่ระหว่างกระบวนการ แต่ถูกหยุดไว้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="283ee-164">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="283ee-165">**สถานะ** – สถานะการประมวลผลของที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-165">**State** – The processing status of the archive.</span></span> <span data-ttu-id="283ee-166">ค่าที่เป็นไปได้คือ *กำลังรอ* *อยู่ระหว่างดำเนินการ* และ *เสร็จสิ้นแล้ว*</span><span class="sxs-lookup"><span data-stu-id="283ee-166">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="283ee-167">แถบเครื่องมือเหนือกริดจะมีปุ่มต่อไปนี้ที่คุณสามารถใช้เพื่อทำงานกับที่เก็บถาวรที่เลือก:</span><span class="sxs-lookup"><span data-stu-id="283ee-167">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="283ee-168">**ธุรกรรมที่เก็บถาวร** – ดูรายละเอียดทั้งหมดเกี่ยวกับที่เก็บถาวรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="283ee-168">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="283ee-169">หน้า **ธุรกรรมที่เก็บถาวร** ซึ่งปรากฏขึ้น แสดงธุรกรรมทั้งหมดในที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="283ee-169">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="283ee-170">![หน้าธุรกรรมที่เก็บถาวร](media/archive-inventory-transactions.png "หน้าธุรกรรมที่เก็บถาวร")</span><span class="sxs-lookup"><span data-stu-id="283ee-170">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="283ee-171">เมื่อต้องการดูข้อมูลเพิ่มเติมเกี่ยวกับธุรกรรมเฉพาะบนหน้า **ธุรกรรมที่เก็บถาวร** ให้เลือกธุรกรรมนั้นในกริด แล้วจากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **รายละเอียดธุรกรรมที่เก็บถาวร**</span><span class="sxs-lookup"><span data-stu-id="283ee-171">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="283ee-172">หน้า **รายละเอียดธุรกรรมที่เก็บถาวร** ซึ่งปรากฏขึ้น จะแสดงข้อมูล เช่น การลงรายการบัญชีแยกประเภท ข้อมูลอ้างอิงของบัญชีแยกประเภทย่อยที่เกี่ยวข้อง และมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="283ee-172">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="283ee-173">**หยุดการเก็บถาวรชั่วคราว** – หยุดที่เก็บถาวรที่เลือกที่กำลังถูกประมวลผลอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="283ee-173">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="283ee-174">การหยุดชั่วคราวจะมีผลเฉพาะหลังจากที่มีการสร้างงานการเก็บถาวรแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="283ee-174">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="283ee-175">ดังนั้น อาจมีความล่าช้าสั้นๆ ก่อนที่การหยุดชั่วคราวจะมีผล</span><span class="sxs-lookup"><span data-stu-id="283ee-175">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="283ee-176">ถ้าที่เก็บถาวรถูกหยุดชั่วคราว เครื่องหมายถูกจะปรากฏขึ้นในฟิลด์ **หยุดการอัพเดตปัจจุบัน**</span><span class="sxs-lookup"><span data-stu-id="283ee-176">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="283ee-177">**ดำเนินการเก็บถาวรต่อ** – ดำเนินการประมวลผลต่อสำหรับที่เก็บถาวรที่เลือกที่ถูกหยุดชั่วคราวอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="283ee-177">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="283ee-178">**กลับรายการ** – กลับรายการที่เก็บถาวรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="283ee-178">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="283ee-179">คุณสามารถกลับรายการที่เก็บถาวรได้เฉพาะเมื่อฟิลด์ **สถานะ** ถูกตั้งค่าเป็น *เสร็จสิ้นแล้ว* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="283ee-179">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="283ee-180">ถ้าที่เก็บถาวรถูกกลับรายการ เครื่องหมายถูกจะปรากฏขึ้นในฟิลด์ **กลับรายการ**</span><span class="sxs-lookup"><span data-stu-id="283ee-180">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
