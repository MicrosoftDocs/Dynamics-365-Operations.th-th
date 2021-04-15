---
title: การโยกย้ายชนิดข้อมูลสกุลเงินสำหรับการรวมแบบสองทิศทาง
description: หัวข้อนี้จะอธิบายวิธีการเปลี่ยนจำนวนตำแหน่งทศนิยมที่รองรับการรวมแบบสองทิศทางสำหรับสกุลเงิน
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: c4f663ae36f7d4ea3db9888e618f2fe3bf8c3256
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748958"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="4d9e8-103">การโยกย้ายชนิดข้อมูลสกุลเงินสำหรับการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4d9e8-104">คุณสามารถเพิ่มจำนวนตำแหน่งทศนิยมที่ได้รับการสนับสนุนสำหรับค่าสกุลเงินได้สูงสุด 10 ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="4d9e8-105">ขีดจำกัดเริ่มต้นคือจุดทศนิยมสี่ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-105">The default limit is four decimal places.</span></span> <span data-ttu-id="4d9e8-106">โดยการเพิ่มจำนวนตำแหน่งทศนิยม คุณจะช่วยป้องกันการสูญเสียข้อมูล เมื่อคุณใช้การรวมแบบสองทิศทางเพื่อซิงค์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d9e8-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="4d9e8-107">การเพิ่มขึ้นในจำนวนตำแหน่งทศนิยมคือการเปลี่ยนแปลงการเข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="4d9e8-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="4d9e8-108">เมื่อต้องการใช้งาน คุณต้องร้องขอความช่วยเหลือจาก Microsoft</span><span class="sxs-lookup"><span data-stu-id="4d9e8-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="4d9e8-109">กระบวนการในการเปลี่ยนจำนวนตำแหน่งทศนิยมมีสองขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="4d9e8-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="4d9e8-110">ร้องขอการโยกย้ายจาก Microsoft</span><span class="sxs-lookup"><span data-stu-id="4d9e8-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="4d9e8-111">เปลี่ยนจำนวนตำแหน่งทศนิยมใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="4d9e8-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="4d9e8-112">แอป Finance and Operations และ Dataverse ต้องสนับสนุนจำนวนตำแหน่งทศนิยมเดียวกันในค่าสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4d9e8-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="4d9e8-113">มิฉะนั้น การสูญเสียข้อมูลอาจเกิดขึ้น เมื่อข้อมูลนี้ถูกซิงค์ระหว่างแอป</span><span class="sxs-lookup"><span data-stu-id="4d9e8-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="4d9e8-114">กระบวนการโยกย้ายตั้งค่าคอนฟิกวิธีการจัดเก็บสกุลเงินและอัตราแลกเปลี่ยนใหม่ แต่จะไม่เปลี่ยนแปลงข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="4d9e8-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="4d9e8-115">หลังจากที่การโยกย้ายเสร็จสมบูรณ์แล้ว คุณสามารถเพิ่มจำนวนตำแหน่งทศนิยมสำหรับรหัสสกุลเงินและการกำหนดราคา และข้อมูลที่ผู้ใช้ป้อนและมุมมองอาจมีจำนวนตำแหน่งทศนิยมมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="4d9e8-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="4d9e8-116">ไม่จำเป็นต้องระบุการโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="4d9e8-116">Migration is optional.</span></span> <span data-ttu-id="4d9e8-117">ถ้าคุณอาจได้รับประโยชน์จากการสนับสนุนสำหรับตำแหน่งทศนิยมที่เพิ่มขึ้น เราขอแนะนำว่าคุณควรพิจารณาการโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="4d9e8-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="4d9e8-118">องค์กรที่ไม่จำเป็นต้องใช้ค่าที่มีตำแหน่งทศนิยมมากกว่าสี่ตำแหน่ง ไม่จำเป็นต้องโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="4d9e8-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="4d9e8-119">การร้องขอการโยกย้ายจาก Microsoft</span><span class="sxs-lookup"><span data-stu-id="4d9e8-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="4d9e8-120">การจัดเก็บสำหรับคอลัมน์สกุลเงินที่มีอยู่ใน Dataverse ไม่สามารถสนับสนุนตำแหน่งทศนิยมที่มากกว่าสี่ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="4d9e8-121">ดังนั้น ในระหว่างกระบวนการโยกย้าย ค่าสกุลเงินจะถูกคัดลอกไปยังคอลัมน์ภายในใหม่ในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d9e8-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="4d9e8-122">กระบวนการนี้จะเกิดขึ้นอย่างต่อเนื่อง จนกว่าจะมีการย้ายข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4d9e8-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="4d9e8-123">เมื่อสิ้นสุดการโยกย้าย ชนิดการจัดเก็บใหม่จะแทนที่ชนิดการจัดเก็บเก่าภายใน แต่ค่าข้อมูลจะไม่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="4d9e8-124">จากนั้น คอลัมน์สกุลเงินสามารถสนับสนุนตำแหน่งทศนิยมได้สูงสุด 10 ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="4d9e8-125">ในระหว่างกระบวนการโยกย้าย Dataverse สามารถใช้งานต่อไปได้โดยไม่มีการขัดจังหวะ</span><span class="sxs-lookup"><span data-stu-id="4d9e8-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="4d9e8-126">ในขณะเดียวกัน อัตราแลกเปลี่ยนจะถูกปรับเปลี่ยนเพื่อให้สนับสนุนตำแหน่งทศนิยมสูงสุด 12 ตำแหน่ง แทนที่จะใช้ขีดจำกัดปัจจุบันเป็น 10</span><span class="sxs-lookup"><span data-stu-id="4d9e8-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="4d9e8-127">ต้องมีการเปลี่ยนแปลงนี้เพื่อให้จำนวนตำแหน่งทศนิยมเหมือนกันในทั้งแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="4d9e8-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="4d9e8-128">การโยกย้ายไม่เปลี่ยนแปลงข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="4d9e8-128">Migration doesn't change any data.</span></span> <span data-ttu-id="4d9e8-129">หลังจากที่มีการแปลงคอลัมน์สกุลเงินและอัตราแลกเปลี่ยนแล้ว ผู้ดูแลระบบสามารถตั้งค่าคอนฟิกระบบให้ใช้ตำแหน่งทศนิยมได้สูงสุด 10 ตำแหน่งสำหรับคอลัมน์สกุลเงิน โดยการระบุจำนวนตำแหน่งทศนิยมสำหรับสกุลเงินของธุรกรรมแต่ละสกุลเงินและสำหรับการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="4d9e8-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="4d9e8-130">ร้องขอการโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="4d9e8-130">Request a migration</span></span>

<span data-ttu-id="4d9e8-131">เมื่อต้องการทำให้คุณลักษณะนี้พร้อมใช้งาน อีเมล **CDSExpandDecimal@microsoft.com** และรวมข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4d9e8-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="4d9e8-132">**เรื่อง:** ร้องขอเพื่อเปิดใช้งานการสนับสนุนทศนิยมแบบขยายสำหรับ \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="4d9e8-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="4d9e8-133">**เนื้อหา:** ฉันต้องการเปิดใช้งานการสนับสนุนทศนิยมแบบขยายสำหรับองค์กรของฉัน \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="4d9e8-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="4d9e8-134">ตัวแทน Microsoft จะติดต่อคุณภายในสองถึงสามวันทำการสำหรับขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4d9e8-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="4d9e8-135">เมื่อคุณร้องขอการโยกย้าย คุณควรตระหนักถึงรายละเอียดต่อไปนี้และวางแผนสำหรับรายละเอียดดังกล่าวให้สอดคล้องกัน:</span><span class="sxs-lookup"><span data-stu-id="4d9e8-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="4d9e8-136">เวลาที่จำเป็นต้องใช้ในการย้ายข้อมูลจะขึ้นอยู่กับจำนวนข้อมูลในระบบ</span><span class="sxs-lookup"><span data-stu-id="4d9e8-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="4d9e8-137">การโยกย้ายฐานข้อมูลที่มีขนาดใหญ่อาจใช้เวลาหลายวัน</span><span class="sxs-lookup"><span data-stu-id="4d9e8-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="4d9e8-138">ขนาดของฐานข้อมูลจะเพิ่มขึ้นชั่วคราว ขณะที่การโยกย้ายกำลังรันอยู่ เนื่องจากจำเป็นต้องมีพื้นที่เพิ่มเติมสำหรับดัชนี</span><span class="sxs-lookup"><span data-stu-id="4d9e8-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="4d9e8-139">พื้นที่เพิ่มเติมส่วนใหญ่จะว่างเปล่า เมื่อการโยกย้ายเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4d9e8-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="4d9e8-140">ในระหว่างกระบวนการโยกย้าย ถ้าเกิดข้อผิดพลาดที่ทำให้ไม่สามารถดำเนินการย้ายข้อมูลให้เสร็จสิ้น ระบบจะเพิ่มการแจ้งเตือนไปยังฝ่ายสนับสนุนของ Microsoft เพื่อให้เจ้าหน้าที่สนับสนุนสามารถแทรกแซง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="4d9e8-141">อย่างไรก็ตาม ถึงแม้ว่าจะเกิดข้อผิดพลาดระหว่างการโยกย้าย Dataverse ยังคงพร้อมใช้งานทั้งหมดสำหรับการใช้งานปกติ</span><span class="sxs-lookup"><span data-stu-id="4d9e8-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="4d9e8-142">กระบวนการโยกย้ายไม่สามารถย้อนกลับได้</span><span class="sxs-lookup"><span data-stu-id="4d9e8-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="4d9e8-143">การเปลี่ยนแปลงจำนวนตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="4d9e8-143">Changing the number of decimal places</span></span>

<span data-ttu-id="4d9e8-144">หลังจากเสร็จสิ้นการโยกย้าย Dataverse สามารถจัดเก็บจำนวนที่มีตำแหน่งทศนิยมมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="4d9e8-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="4d9e8-145">ผู้ดูแลระบบสามารถเลือกจำนวนตำแหน่งทศนิยมที่ใช้สำหรับรหัสสกุลเงินที่ระบุและสำหรับการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="4d9e8-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="4d9e8-146">ผู้ใช้ Microsoft Power Apps, Power BI และ Power Automate สามารถดูและใช้ตัวเลขที่มีตำแหน่งทศนิยมมากขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="4d9e8-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="4d9e8-147">เมื่อต้องการทำการเปลี่ยนแปลงนี้ คุณต้องปรับปรุงการตั้งค่าต่อไปนี้ใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="4d9e8-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="4d9e8-148">**การตั้งค่าระบบ: ความแม่นยำของสกุลเงินสำหรับการกำหนดราคา** – คอลัมน์ **ตั้งค่าความแม่นยำของสกุลเงินที่ใช้สำหรับการกำหนดราคาทั่วทั้งระบบ** กำหนดลักษณะการทำงานของสกุลเงินสำหรับองค์กร เมื่อมีการเลือก **ความแม่นยำของการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="4d9e8-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="4d9e8-149">**การจัดการธุรกิจ: สกุลเงิน** – คอลัมน์ **ความแม่นยำของสกุลเงิน** ช่วยให้คุณสามารถระบุจำนวนตำแหน่งทศนิยมที่กำหนดเองสำหรับสกุลเงินที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4d9e8-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="4d9e8-150">มีการสำรองไปยังการตั้งค่าทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="4d9e8-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="4d9e8-151">มีข้อจำกัดบางรายการ:</span><span class="sxs-lookup"><span data-stu-id="4d9e8-151">There are some limitations:</span></span>

+ <span data-ttu-id="4d9e8-152">คุณไม่สามารถตั้งค่าคอนฟิกคอลัมน์สกุลเงินในตารางได้</span><span class="sxs-lookup"><span data-stu-id="4d9e8-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="4d9e8-153">คุณสามารถระบุตำแหน่งทศนิยมมากกว่าสี่ตำแหน่งได้เฉพาะที่ระดับ **การกำหนดราคา** และ **สกุลเงินและธุรกรรม** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4d9e8-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="4d9e8-154">การตั้งค่าระบบ: ความแม่นยำของสกุลเงินสำหรับการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="4d9e8-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="4d9e8-155">หลังจากการโยกย้ายเสร็จสมบูรณ์ ผู้ดูแลระบบจะสามารถกำหนดความแม่นยำของสกุลเงินได้</span><span class="sxs-lookup"><span data-stu-id="4d9e8-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="4d9e8-156">ไปที่ **การตั้งค่า \> การจัดการ** และเลือก **การตั้งค่าระบบ**</span><span class="sxs-lookup"><span data-stu-id="4d9e8-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="4d9e8-157">จากนั้น บนแท็บ **ทั่วไป** ให้เปลี่ยนค่าของคอลัมน์ **ตั้งค่าความแม่นยำของสกุลเงินที่ใช้สำหรับการกำหนดราคาทั่วทั้งระบบ** ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4d9e8-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![การตั้งค่าระบบสำหรับสกุลเงิน](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="4d9e8-159">การจัดการธุรกิจ: สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4d9e8-159">Business Management: Currencies</span></span>

<span data-ttu-id="4d9e8-160">ถ้าคุณต้องการให้ความแม่นยำของสกุลเงินสำหรับสกุลเงินหนึ่งๆ แตกต่างจากความแม่นยำของสกุลเงินที่ใช้สำหรับการกำหนดราคา คุณสามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="4d9e8-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="4d9e8-161">ไปที่ **การตั้งค่า \> การจัดการธุรกิจ** เลือก **สกุลเงิน** และเลือกสกุลเงินที่จะเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="4d9e8-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="4d9e8-162">จากนั้น ตั้งค่าคอลัมน์ **ความแม่นยำของสกุลเงิน** เป็นจำนวนตำแหน่งทศนิยมที่คุณต้องการ ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4d9e8-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![การตั้งค่าสกุลเงินสำหรับตำแหน่งที่ตั้งที่ระบุ](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="4d9e8-164">ตาราง: คอลัมน์สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4d9e8-164">tables: Currency column</span></span>

<span data-ttu-id="4d9e8-165">จำนวนตำแหน่งทศนิยมที่สามารถตั้งค่าคอนฟิกสำหรับคอลัมน์สกุลเงินเฉพาะ จะถูกจำกัดไว้ที่สี่ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4d9e8-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]