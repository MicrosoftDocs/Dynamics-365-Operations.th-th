---
title: ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าขั้นสูงโดยใช้สมุดรายวันการมาถึงของสินค้า
description: หัวข้อนี้นำเสนอสถานการณ์ที่แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้กระบวนการจัดการคลังสินค้าขั้นสูง
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830845"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="cb54c-103">ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าขั้นสูงโดยใช้สมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb54c-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb54c-104">หัวข้อนี้นำเสนอสถานการณ์ที่แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้กระบวนการจัดการคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="cb54c-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="cb54c-105">ซึ่งโดยปกติแล้ว เจ้าหน้าที่ส่วนรับสินค้าจะเป็นผู้ดำเนินการในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="cb54c-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="cb54c-106">เปิดใช้งานข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cb54c-106">Enable sample data</span></span>

<span data-ttu-id="cb54c-107">หากต้องการสถานการณ์นี้โดยใช้เรกคอร์ดตัวอย่างและค่าที่ระบุในหัวข้อนี้ คุณต้องใช้ระบบที่ติดตั้งข้อมูลสาธิตมาตรฐานไว้ และคุณต้องเลือกนิติบุคคล *USMF* ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cb54c-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="cb54c-108">คุณสามารถใช้งานสถานการณ์ดังกล่าวแทนได้ ด้วยการแทนที่ค่าจากข้อมูลของคุณเองที่คุณมีข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb54c-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="cb54c-109">คุณต้องมีใบสั่งซื้อที่ยืนยันที่มีบรรทัดใบสั่งซื้อที่เปิด</span><span class="sxs-lookup"><span data-stu-id="cb54c-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="cb54c-110">ต้องเก็บสินค้าในรายการในคลัง</span><span class="sxs-lookup"><span data-stu-id="cb54c-110">The item on the line must be stocked.</span></span> <span data-ttu-id="cb54c-111">ต้องใช้ผลิตภัณฑ์ย่อย และต้องไม่มีมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="cb54c-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="cb54c-112">สินค้าจะต้องเชื่อมโยงกับกลุ่มมิติคลังสินค้าที่จะเปิดใช้งานกระบวนการการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb54c-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="cb54c-113">ต้องเปิดใช้คลังสินค้าที่จะใช้สำหรับกระบวนการจัดการคลังสินค้า และสถานที่ที่คุณใช้สำหรับการรับสินค้าต้องมีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cb54c-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="cb54c-114">สร้างส่วนหัวของสมุดรายวันการมาถึงของสินค้าที่ใช้การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb54c-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="cb54c-115">สถานการณ์ต่อไปนี้แสดงวิธีการสร้างส่วนหัวของสมุดรายวันการมาถึงของสินค้าที่ใช้การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb54c-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="cb54c-116">ตรวจสอบให้แน่ใจว่าระบบของคุณมีใบสั่งซื้อที่ยืนยันซึ่งเป็นไปตามข้อความต้องการที่อธิบายไว้ในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="cb54c-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="cb54c-117">สถานการณ์นี้ใช้ใบสั่งซื้อกับของบริษัท *USMF* บัญชีผู้จัดจำหน่าย *1001* คลังสินค้า *51* ที่มีบรรทัดใบสั่งจํานวน *10 PL* (10 แท่นวางสินค้า) ของหมายเลขสินค้า *M9200*</span><span class="sxs-lookup"><span data-stu-id="cb54c-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="cb54c-118">สร้างบันทึกย่อของหมายเลขใบสั่งซื้อที่คุณจะใช้</span><span class="sxs-lookup"><span data-stu-id="cb54c-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="cb54c-119">ไปยัง **การบริหารสินค้าคงคลัง \> รายการสมุดรายวัน \> การมาถึงของสินค้า \> การมาถึงของสินค้า**</span><span class="sxs-lookup"><span data-stu-id="cb54c-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="cb54c-120">เลือก **สร้าง** บนหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="cb54c-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="cb54c-121">กล่องโต้ตอบ **สร้างสมุดรายวันการจัดการคลังสินค้า** เปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="cb54c-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="cb54c-122">ให้เลือกชื่อสมุดรายวัน ในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="cb54c-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="cb54c-123">ถ้าคุณกำลังใช้ข้อมูลสาธิต *USMF* เลือก *WHS*</span><span class="sxs-lookup"><span data-stu-id="cb54c-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="cb54c-124">ถ้าคุณใช้ข้อมูลของคุณเอง สมุดรายวันที่คุณเลือกต้องมีการตั้งค่า **สถานที่เบิกสินค้า** เป็น *ไม่* และ **การบริหารการตรวจสอบสินค้า** จะถูกตั้งค่าเป็น *ไม่*</span><span class="sxs-lookup"><span data-stu-id="cb54c-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="cb54c-125">ตั้งค่า **อ้างอิง** เป็น *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="cb54c-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="cb54c-126">ตั้งค่า **หมายเลขบัญชี** เป็น *1001*</span><span class="sxs-lookup"><span data-stu-id="cb54c-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="cb54c-127">ตั้งค่า **หมายเลข** เป็นหมายเลขของใบสั่งซื้อที่คุณระบุไว้เพื่อการออกใช้นี้</span><span class="sxs-lookup"><span data-stu-id="cb54c-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="cb54c-128">![สมุดรายวันการมาถึงของสินค้า](../media/item-arrival-journal-header.png "สมุดรายวันการมาถึงของสินค้า")</span><span class="sxs-lookup"><span data-stu-id="cb54c-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="cb54c-129">เลือก **ตกลง** เพื่อสร้างหัวข้อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="cb54c-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="cb54c-130">ในส่วน **รายการสมุดรายวัน** ให้เลือก **เพิ่มรายการ** และป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb54c-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="cb54c-131">**หมายเลขสินค้า** ตั้งค่าเป็น *M9200*</span><span class="sxs-lookup"><span data-stu-id="cb54c-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="cb54c-132">**ไซต์** **คลังสินค้า** และ **ปริมาณ** จะได้รับการตั้งค่าตามข้อมูลธุรกรรมสินค้าคงคลัง 10 แท่นวางสินค้า (1000 ชิ้น)</span><span class="sxs-lookup"><span data-stu-id="cb54c-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="cb54c-133">**สถานที่** – ตั้งค่าเป็น *001*</span><span class="sxs-lookup"><span data-stu-id="cb54c-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="cb54c-134">สถานที่เฉพาะนี้ไม่ติดตามป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cb54c-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="cb54c-135">![รายการสมุดรายวันการมาถึงของสินค้า](../media/item-arrival-journal-line.png "รายการสมุดรายวันการมาถึงของสินค้า")</span><span class="sxs-lookup"><span data-stu-id="cb54c-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb54c-136">ฟิลด์ **วันที่** จะกำหนดวันที่ที่ปริมาณคงเหลือของสินค้านี้จะถูกลงทะเบียนในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cb54c-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="cb54c-137">**รหัสล็อต** จะถูกเติมโดยระบบ ถ้ามีการระบุเฉพาะจากข้อมูลที่ให้ไว้</span><span class="sxs-lookup"><span data-stu-id="cb54c-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="cb54c-138">มิฉะนั้น คุณจะต้องป้อนรายการนี้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="cb54c-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="cb54c-139">นี่เป็นฟิลด์บังคับที่ลิงค์การลงทะเบียนนี้กับรายการเอกสารต้นทางเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="cb54c-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="cb54c-140">เลือก **ตรวจสอบความถูกต้อง** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="cb54c-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="cb54c-141">มีการตรวจสอบว่า สมุดรายวันพร้อมที่จะถูกลงรายการบัญชีหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="cb54c-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="cb54c-142">หากการตรวจสอบจะล้มเหลวคุณ คุณจำเป็นต้องแก้ไขข้อผิดพลาดก่อนที่คุณจะสามารถลงรายการบัญชีสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="cb54c-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="cb54c-143">กล่องโต้ตอบ **ตรวจสอบสมุดรายวัน** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="cb54c-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="cb54c-144">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb54c-144">Select **OK**.</span></span>
1. <span data-ttu-id="cb54c-145">ตรวจทานแถบข้อความ</span><span class="sxs-lookup"><span data-stu-id="cb54c-145">Review the message bar.</span></span> <span data-ttu-id="cb54c-146">ควรมีข้อความแจ้งว่า การดำเนินงานสำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="cb54c-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="cb54c-147">เลือก **ลงรายการบัญชี** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="cb54c-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="cb54c-148">กล่องโต้ตอบ **ลงรายการบัญชีสมุดรายวัน** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="cb54c-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="cb54c-149">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb54c-149">Select **OK**.</span></span>
1. <span data-ttu-id="cb54c-150">ตรวจทานแถบข้อความ</span><span class="sxs-lookup"><span data-stu-id="cb54c-150">Review the message bar.</span></span> <span data-ttu-id="cb54c-151">ควรมีข้อความแจ้งว่า การดำเนินงานสำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="cb54c-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="cb54c-152">เลือก **ฟังก์ชัน > ใบรับสินค้า** ในบานหน้าต่างการด้านล่างเพื่ออัพเดตรายการใบสั่งซื้อและลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb54c-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
