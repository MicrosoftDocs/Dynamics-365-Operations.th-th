---
title: การแบ่งช่วงเวลาของคลังสินค้า
description: หัวข้อนี้มีข้อมูลเกี่ยวกับการแบ่งช่วงเวลาของคลังสินค้า การแบ่งช่วงเวลาของคลังสินค้าช่วยให้คุณสามารถรวมความต้องการตามสินค้าและหน่วยวัดจากใบสั่งที่มีสถานะเป็นสั่งแล้ว จองแล้ว หรือนำออกใช้แล้ว ซึ่งช่วยผู้จัดการคลังสินค้าในการวางแผนสถานที่เบิกสินค้าอย่างชาญฉลาด ก่อนที่พวกเขาจะนำใบสั่งออกใช้ไปยังคลังสินค้าและสร้างงานการเบิกสินค้า
author: mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d9080f192db0c59b4b4bc74468491e86ba0b7471
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530362"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="fedfb-105">การแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fedfb-106">การแบ่งช่วงเวลาของคลังสินค้าช่วยให้คุณสามารถรวมความต้องการตามสินค้าและหน่วยวัดจากใบสั่งที่มีสถานะเป็น *สั่งแล้ว* *จองแล้ว* หรือ *นำออกใช้แล้ว*</span><span class="sxs-lookup"><span data-stu-id="fedfb-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="fedfb-107">จากนั้น ความต้องการที่สร้างขึ้นสามารถนำไปใช้กับสถานที่ที่จะใช้สำหรับการเบิกสินค้าตามปริมาณ หน่วย มิติทางกายภาพ สถานที่คงที่ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="fedfb-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="fedfb-108">หลังจากที่มีการสร้างแผนการแบ่งช่วงเวลาแล้ว คุณสามารถสร้างงานการเติมสินค้าเพื่อนำจำนวนของสินค้าคงคลังที่เหมาะสมไปยังสถานที่แต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="fedfb-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="fedfb-109">ฟังก์ชันนี้ช่วยผู้จัดการคลังสินค้าในการวางแผนสถานที่เบิกสินค้าอย่างชาญฉลาด ก่อนที่พวกเขาจะนำใบสั่งออกใช้ไปยังคลังสินค้าและสร้างงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="fedfb-110">เปิดคุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="fedfb-111">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="fedfb-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="fedfb-112">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="fedfb-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="fedfb-113">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="fedfb-114">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="fedfb-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="fedfb-115">**ชื่อคุณลักษณะ:** *คุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="fedfb-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="fedfb-116">การตั้งค่าการแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-116">Set up warehouse slotting</span></span>

<span data-ttu-id="fedfb-117">เมื่อต้องการใช้การแบ่งช่วงเวลาของคลังสินค้า คุณต้องตั้งค่าองค์ประกอบต่อไปนี้ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="fedfb-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="fedfb-118">สร้างระดับหน่วยวัดสำหรับการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="fedfb-119">ระดับหน่วยวัดทำให้สามารถมีการจัดกลุ่มหน่วยวัดต่างๆ เข้าด้วยกันสำหรับวัตถุประสงค์ของการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="fedfb-120">ตัวอย่างเช่น ถ้ามีการเบิกกล่องหลายขนาดทั้งหมดจากพื้นที่เบิกกล่องเดียวกัน คุณสามารถสร้างระดับเดียวสำหรับทุกขนาดได้</span><span class="sxs-lookup"><span data-stu-id="fedfb-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="fedfb-121">**ต้องสร้างบรรทัดสำหรับแต่ละหน่วยวัดที่ควรจะเป็นส่วนหนึ่งของระดับ**</span><span class="sxs-lookup"><span data-stu-id="fedfb-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="fedfb-122">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> ระดับหน่วยวัดสำหรับการแบ่งช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="fedfb-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="fedfb-123">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="fedfb-123">Select **New**.</span></span>
1. <span data-ttu-id="fedfb-124">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="fedfb-125">**ระดับหน่วยวัด:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="fedfb-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="fedfb-126">**คำอธิบาย:** *แท่นวางสินค้าแต่ละกล่อง*</span><span class="sxs-lookup"><span data-stu-id="fedfb-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="fedfb-127">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fedfb-127">Select **Save**.</span></span>
1. <span data-ttu-id="fedfb-128">บน FastTab **หน่วยวัด:** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="fedfb-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="fedfb-129">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-130">**หน่วย:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="fedfb-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="fedfb-131">**คำอธิบาย:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="fedfb-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="fedfb-132">จะมีการเติมข้อมูลนี้โดยอัตโนมัติ เมื่อคุณบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="fedfb-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="fedfb-133">**คลาสหน่วย:** *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="fedfb-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="fedfb-134">เลือก **สร้าง** เพื่อเพิ่มบรรทัดที่สองลงในกริด</span><span class="sxs-lookup"><span data-stu-id="fedfb-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="fedfb-135">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-136">**หน่วย:** *ea*</span><span class="sxs-lookup"><span data-stu-id="fedfb-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="fedfb-137">**คำอธิบาย:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="fedfb-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="fedfb-138">จะมีการเติมข้อมูลนี้โดยอัตโนมัติ เมื่อคุณบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="fedfb-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="fedfb-139">**คลาสหน่วย:** *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="fedfb-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="fedfb-140">เลือก **สร้าง** เพื่อเพิ่มบรรทัดที่สามลงในกริด</span><span class="sxs-lookup"><span data-stu-id="fedfb-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="fedfb-141">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-142">**หน่วย:** *PL*</span><span class="sxs-lookup"><span data-stu-id="fedfb-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="fedfb-143">**คำอธิบาย:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="fedfb-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="fedfb-144">จะมีการเติมข้อมูลนี้โดยอัตโนมัติ เมื่อคุณบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="fedfb-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="fedfb-145">**คลาสหน่วย:** *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="fedfb-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="fedfb-146">เลือก **บันทึก** เพื่อบันทึกระดับ</span><span class="sxs-lookup"><span data-stu-id="fedfb-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="fedfb-147">สร้างรหัสคำสั่งสำหรับการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-147">Create a directive code for slotting</span></span>

<span data-ttu-id="fedfb-148">คุณต้องเลือกรหัสคำสั่งที่ควรเชื่อมโยงกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fedfb-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="fedfb-149">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> รหัสคำสั่ง**</span><span class="sxs-lookup"><span data-stu-id="fedfb-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="fedfb-150">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="fedfb-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="fedfb-151">ในฟิลด์ **รหัสคำสั่ง** ให้ป้อน *การแบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="fedfb-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="fedfb-152">ในฟิลด์ **คำอธิบายคำสั่ง** ให้ป้อน *การแบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="fedfb-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="fedfb-153">การตั้งค่าเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-153">Set up slotting templates</span></span>

<span data-ttu-id="fedfb-154">เท็มเพลตการแบ่งช่วงเวลาแต่ละรายการจะควบคุมวิธีการกำหนดสินค้าคงคลังให้กับสถานที่สำหรับคลังสินค้าหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="fedfb-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="fedfb-155">เท็มเพลตแต่ละรายการจะต้องรวมบรรทัดสำหรับข้อมูลจำเพาะของการแบ่งช่วงเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="fedfb-156">ใช้กระบวนงานในส่วนนี้เพื่อตั้งค่าเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="fedfb-157">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="fedfb-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="fedfb-158">เลือก **สร้าง** เพื่อสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fedfb-158">Select **New** to create a template.</span></span>

<span data-ttu-id="fedfb-159">ถัดไป คุณต้องตั้งค่าส่วนหัวของเท็มเพลต ข้อมูลจำเพาะของการแบ่งช่วงเวลา และคำสั่งสถานที่ ดังที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="fedfb-160">ตั้งค่าส่วนหัวของเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="fedfb-161">ในส่วนหัวสำหรับเท็มเพลต ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="fedfb-162">**เท็มเพลตการแบ่งช่วงเวลา:** _61_</span><span class="sxs-lookup"><span data-stu-id="fedfb-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="fedfb-163">**คำอธิบาย:** _61_</span><span class="sxs-lookup"><span data-stu-id="fedfb-163">**Description:** _61_</span></span>
    - <span data-ttu-id="fedfb-164">**ชนิดความต้องการ:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="fedfb-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="fedfb-165">ในปัจจุบัน *ใบสั่งขาย* เป็นเพียงความต้องการชนิดเดียวที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="fedfb-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="fedfb-166">**กลยุทธ์ความต้องการ:** _สั่งแล้ว_</span><span class="sxs-lookup"><span data-stu-id="fedfb-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="fedfb-167">ค่าต่อไปนี้จะพร้อมใช้งานในฟิลด์นี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="fedfb-168">**สั่งแล้ว** – ปริมาณที่สั่งทั้งหมดในใบสั่งขายควรมีการพิจารณาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="fedfb-169">**จองแล้ว** – เฉพาะปริมาณของบรรทัดใบสั่งขายที่จองไว้เท่านั้น (มีจริง และสั่งแล้ว) ที่ควรมีการพิจารณาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="fedfb-170">**คลังสินค้า:** _61_</span><span class="sxs-lookup"><span data-stu-id="fedfb-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="fedfb-171">**อนุญาตให้ความต้องการเวฟใช้ปริมาณที่ไม่ได้จอง:** _ใช่_</span><span class="sxs-lookup"><span data-stu-id="fedfb-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="fedfb-172">นอกจากนี้ คุณยังสามารถระบุการสอบถามเพื่อจำกัดขอบเขตของความต้องการที่จะประเมิน</span><span class="sxs-lookup"><span data-stu-id="fedfb-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="fedfb-173">ตั้งค่าข้อมูลจำเพาะของการแบ่งช่วงเวลาสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="fedfb-174">สำหรับเท็มเพลตแต่ละรายการที่คุณสร้าง ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มบรรทัดสำหรับข้อมูลจำเพาะของการแบ่งช่วงเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="fedfb-175">บน FastTab **รายละเอียดเท็มเพลตการแบ่งช่วงเวลา** ให้เลือก **สร้าง** เพื่อสร้างบรรทัดเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fedfb-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="fedfb-176">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-177">**ลำดับ:** _1_</span><span class="sxs-lookup"><span data-stu-id="fedfb-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="fedfb-178">**คำอธิบาย:** _สถานที่คงที่_</span><span class="sxs-lookup"><span data-stu-id="fedfb-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="fedfb-179">**ปริมาณต่ำสุด:** _1_</span><span class="sxs-lookup"><span data-stu-id="fedfb-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="fedfb-180">ฟิลด์นี้จะกำหนดปริมาณต่ำสุดของความต้องการที่จำเป็นสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="fedfb-181">**ปริมาณสูงสุด:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="fedfb-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="fedfb-182">ฟิลด์นี้จะกำหนดปริมาณสูงสุดของความต้องการที่มีผลบังคับใช้สำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="fedfb-183">**หน่วย:** ให้ปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="fedfb-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="fedfb-184">ฟิลด์นี้จะกำหนดหน่วยวัดที่ปริมาณต่ำสุดและสูงสุดอ้างอิงถึง</span><span class="sxs-lookup"><span data-stu-id="fedfb-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="fedfb-185">**ระดับหน่วยวัด:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="fedfb-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="fedfb-186">ฟิลด์นี้จะกำหนดหน่วยวัดของความต้องการที่มีผลบังคับใช้สำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="fedfb-187">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ตั้งค่าระดับหน่วยวัดสำหรับการแบ่งช่วงเวลา](#unit-tiers) ก่อนหน้าในหัวข้อนี้)</span><span class="sxs-lookup"><span data-stu-id="fedfb-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="fedfb-188">**กำหนดเกณฑ์ของช่วงเวลา:** _พิจารณาปริมาณ_</span><span class="sxs-lookup"><span data-stu-id="fedfb-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="fedfb-189">ค่าต่อไปนี้จะพร้อมใช้งานในฟิลด์นี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="fedfb-190">**สมมติว่าว่างเปล่า** – ระบบนี้ควรสันนิษฐานว่าสถานที่ทั้งหมดในพื้นที่เบิกสินค้าว่างเปล่า และไม่ควรตรวจสอบสถานที่เหล่านั้นสำหรับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fedfb-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="fedfb-191">**พิจารณาปริมาณ** – ระบบนี้ควรตรวจสอบสถานที่ทั้งหมดในพื้นที่เบิกสินค้าสำหรับสินค้าคงคลัง และควรข้ามสถานที่ใดๆ ที่ไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="fedfb-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="fedfb-192">**รหัสคำสั่ง:** _การแบ่งช่วงเวลา_</span><span class="sxs-lookup"><span data-stu-id="fedfb-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="fedfb-193">ฟิลด์นี้จะกำหนดคำสั่งสถานที่ที่ใช้ในการค้นหาสถานที่เบิกสินค้าของงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="fedfb-194">**สถานที่ที่มีปริมาณมากเกินไป:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="fedfb-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="fedfb-195">ฟิลด์นี้จะกำหนดสถานที่ที่มีการเก็บสินค้าคงคลัง ถ้าไม่พบสถานที่สำหรับปริมาณ เมื่อมีการประมวลผลรายการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="fedfb-196">**อนุญาตให้หยุด:** _ใช่_</span><span class="sxs-lookup"><span data-stu-id="fedfb-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="fedfb-197">เมื่อมีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ถ้าความต้องการใดๆ ไม่สามารถถูกจัดช่วงเวลาได้ งานการเคลื่อนไหวงานจะถูกสร้างขึ้นเพื่อนำสินค้าคงคลังออกจากสถานที่ที่ซึ่งมีสินค้าคงคลัง แต่ที่ซึ่งไม่มีการจัดช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="fedfb-198">แล้วรันเท็มเพลตอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="fedfb-198">The template is then run again.</span></span> <span data-ttu-id="fedfb-199">ในเวลานี้ จะละเว้นสินค้าคงคลังในสถานที่</span><span class="sxs-lookup"><span data-stu-id="fedfb-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="fedfb-200">ฟังก์ชันนี้จะทำงานได้ดีที่สุด เมื่อฟิลด์ **กำหนดเกณฑ์ของช่วงเวลา** ถูกตั้งค่าเป็น _พิจารณาปริมาณ_</span><span class="sxs-lookup"><span data-stu-id="fedfb-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="fedfb-201">**การใช้สถานที่คงที่:** _เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์_</span><span class="sxs-lookup"><span data-stu-id="fedfb-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="fedfb-202">ค่าต่อไปนี้จะพร้อมใช้งานในฟิลด์นี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="fedfb-203">**สถานที่คงที่และไม่คงที่** – ระบบไม่ควรถูกจำกัดให้ใช้เฉพาะสถานที่คงที่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fedfb-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="fedfb-204">**เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์** – ระบบควรจะใช้เฉพาะกับสถานที่ที่เป็นสถานที่คงที่สำหรับผลิตภัณฑ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fedfb-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="fedfb-205">**เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์ย่อย** – ระบบควรจะใช้เฉพาะกับสถานที่ที่เป็นสถานที่คงที่สำหรับผลิตภัณฑ์ย่อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fedfb-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="fedfb-206">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fedfb-206">Select **Save**.</span></span>
1. <span data-ttu-id="fedfb-207">เลือก **สร้าง** เพื่อเพิ่มบรรทัดเท็มเพลตที่สอง</span><span class="sxs-lookup"><span data-stu-id="fedfb-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="fedfb-208">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-209">**ลำดับ:** _2_</span><span class="sxs-lookup"><span data-stu-id="fedfb-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="fedfb-210">**คำอธิบาย:** _อื่นๆ_</span><span class="sxs-lookup"><span data-stu-id="fedfb-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="fedfb-211">**ปริมาณต่ำสุด:** _1_</span><span class="sxs-lookup"><span data-stu-id="fedfb-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="fedfb-212">**ปริมาณสูงสุด:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="fedfb-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="fedfb-213">**หน่วย:** ให้ปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="fedfb-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="fedfb-214">**ระดับหน่วยวัด:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="fedfb-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="fedfb-215">**กำหนดเกณฑ์ของช่วงเวลา:** _พิจารณาปริมาณ_</span><span class="sxs-lookup"><span data-stu-id="fedfb-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="fedfb-216">**รหัสคำสั่ง:** _การแบ่งช่วงเวลา_</span><span class="sxs-lookup"><span data-stu-id="fedfb-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="fedfb-217">**สถานที่ที่มีปริมาณมากเกินไป:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="fedfb-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="fedfb-218">**อนุญาตให้หยุด:** _ใช่_</span><span class="sxs-lookup"><span data-stu-id="fedfb-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="fedfb-219">**ใช้สถานที่คงที่:** _สถานที่คงที่และไม่คงที่_</span><span class="sxs-lookup"><span data-stu-id="fedfb-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="fedfb-220">ในการสอบถามสำหรับบรรทัดที่สอง คุณจะระบุเกณฑ์ที่จะใช้ในการกำหนดสถานที่ที่ความต้องการสำหรับบรรทัดดังกล่าวถูกจัดช่วงเวลาให้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="fedfb-221">เลือกบรรทัดที่ฟิลด์ **ลำดับ** ถูกตั้งค่าเป็น *2*</span><span class="sxs-lookup"><span data-stu-id="fedfb-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="fedfb-222">เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="fedfb-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="fedfb-223">บนแท็บ **ช่วงระยะ** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="fedfb-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="fedfb-224">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-225">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="fedfb-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="fedfb-226">**ตารางสืบทอด:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="fedfb-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="fedfb-227">**ฟิลด์:** *รหัสโพรไฟล์สถานที่*</span><span class="sxs-lookup"><span data-stu-id="fedfb-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="fedfb-228">**เงื่อนไข:** *เบิกสินค้า-06* (เลือกเครื่องหมายบวกคู่ \[**++**\] ในฟิลด์เพื่อขยายรายการ แล้วจากนั้น เลือก *เบิกสินค้า-06* - *ไซต์เบิกสินค้า 6*)</span><span class="sxs-lookup"><span data-stu-id="fedfb-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="fedfb-229">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fedfb-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="fedfb-230">ตั้งค่าคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="fedfb-230">Set up location directives</span></span>

<span data-ttu-id="fedfb-231">ต้องมีการตั้งค่าคำสั่งสถานที่อย่างน้อยหนึ่งรายการเพื่อสนับสนุนการเบิกสินค้าที่แบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="fedfb-232">ใช้กระบวนงานในส่วนนี้เพื่อตั้งค่า *คำสั่งสถานที่การเติมสินค้า* สำหรับการเบิกสินค้าที่แบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="fedfb-233">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="fedfb-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="fedfb-234">ในบานหน้าต่างด้านซ้าย ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *การเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="fedfb-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="fedfb-235">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="fedfb-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="fedfb-236">ในส่วนหัวของคำสั่งสถานที่ใหม่ ในฟิลด์ **ชื่อ** ให้ป้อน *61 การเบิกสินค้าที่แบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="fedfb-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="fedfb-237">ตั้งค่าคอนฟิก FastTab ของคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="fedfb-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="fedfb-238">บน FastTab **คำสั่งสถานที่** ให้กำหนดค่าดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="fedfb-239">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fedfb-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="fedfb-240">**ชนิดงาน:** _เบิกสินค้า_</span><span class="sxs-lookup"><span data-stu-id="fedfb-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="fedfb-241">**ไซต์:** _6_</span><span class="sxs-lookup"><span data-stu-id="fedfb-241">**Site:** _6_</span></span>
    - <span data-ttu-id="fedfb-242">**คลังสินค้า:** _61_</span><span class="sxs-lookup"><span data-stu-id="fedfb-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="fedfb-243">**รหัสคำสั่ง:** _การแบ่งช่วงเวลา_</span><span class="sxs-lookup"><span data-stu-id="fedfb-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="fedfb-244">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fedfb-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="fedfb-245">ตั้งค่าคอนฟิก FastTab บรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="fedfb-246">บน FastTab **รายการ** เลือก **สร้าง** เพื่อสร้างบรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="fedfb-247">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-247">On the new line, set the following values.</span></span> <span data-ttu-id="fedfb-248">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fedfb-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="fedfb-249">**ปริมาณเริ่มต้น:** _0_</span><span class="sxs-lookup"><span data-stu-id="fedfb-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="fedfb-250">**ปริมาณสิ้นสุด:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="fedfb-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="fedfb-251">เลือก **บันทึก** เพื่อให้แท็บด่วน **การดำเนินคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fedfb-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="fedfb-252">ตั้งค่าคอนฟิก FastTab การดำเนินการของคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="fedfb-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="fedfb-253">บน FastTab **การดำเนินการของคำสั่งสถานที่** เลือก **สร้าง** เพื่อสร้างบรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="fedfb-254">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-254">On the new line, set the following values.</span></span> <span data-ttu-id="fedfb-255">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fedfb-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="fedfb-256">**ชื่อ:** _จำนวนมาก_</span><span class="sxs-lookup"><span data-stu-id="fedfb-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="fedfb-257">**กลยุทธ์:** _ไม่มี_</span><span class="sxs-lookup"><span data-stu-id="fedfb-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="fedfb-258">เลือก **บันทึก** เพื่อทำให้ปุ่ม **แก้ไขแบบสอบถาม** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fedfb-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="fedfb-259">แก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="fedfb-259">Edit the query</span></span>

1. <span data-ttu-id="fedfb-260">บน FastTab **การดำเนินการของคำสั่งสถานที่** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="fedfb-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="fedfb-261">บนแท็บ **ช่วงระยะ** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="fedfb-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="fedfb-262">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-263">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="fedfb-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="fedfb-264">**ตารางสืบทอด:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="fedfb-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="fedfb-265">**ฟิลด์:** *รหัสโซน*</span><span class="sxs-lookup"><span data-stu-id="fedfb-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="fedfb-266">**เงื่อนไข:** *จำนวนมาก* (เลือกเครื่องหมายบวกคู่ \[**++**\] ในฟิลด์เพื่อขยายรายการ แล้วจากนั้น เลือก *จำนวนมาก*)</span><span class="sxs-lookup"><span data-stu-id="fedfb-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="fedfb-267">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fedfb-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="fedfb-268">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="fedfb-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="fedfb-269">ตั้งค่าสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="fedfb-269">Set up the scenario</span></span>

<span data-ttu-id="fedfb-270">สำหรับสถานการณ์จำลองนี้ ให้ใช้ข้อมูลตัวอย่างที่มีอยู่แล้วภายใน และสร้างเรกคอร์ดที่อธิบายไว้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="fedfb-271">ใช้ข้อมูลตัวอย่าง USMF</span><span class="sxs-lookup"><span data-stu-id="fedfb-271">Use the USMF sample data</span></span>

<span data-ttu-id="fedfb-272">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="fedfb-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="fedfb-273">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fedfb-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="fedfb-274">สร้างความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-274">Create demand</span></span>

<span data-ttu-id="fedfb-275">ทำตามขั้นตอนเหล่านี้เพื่อสร้างความต้องการที่คุณจะนำการแบ่งช่วงเวลาไปใช้</span><span class="sxs-lookup"><span data-stu-id="fedfb-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="fedfb-276">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="fedfb-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="fedfb-277">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="fedfb-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="fedfb-278">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ในฟิลด์ **บัญชีลูกค้า** ให้เลือก _US-007_</span><span class="sxs-lookup"><span data-stu-id="fedfb-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="fedfb-279">ในฟิลด์  **คลังสินค้า** เลือก _61_</span><span class="sxs-lookup"><span data-stu-id="fedfb-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="fedfb-280">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fedfb-280">Select **OK**.</span></span>
1. <span data-ttu-id="fedfb-281">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="fedfb-281">The new sales order is opened.</span></span> <span data-ttu-id="fedfb-282">ซึ่งมีบรรทัดว่างบน FastTab **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="fedfb-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="fedfb-283">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-284">**สินค้า:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="fedfb-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="fedfb-285">**ปริมาณ:** _20_</span><span class="sxs-lookup"><span data-stu-id="fedfb-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="fedfb-286">เลือก **สร้างบรรทัด** เพื่อเพิ่มบรรทัดใหม่ และตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="fedfb-287">**สินค้า:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="fedfb-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="fedfb-288">**ปริมาณ:** _8_</span><span class="sxs-lookup"><span data-stu-id="fedfb-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="fedfb-289">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fedfb-289">Select **Save**.</span></span>
1. <span data-ttu-id="fedfb-290">เลือก **สร้าง** เพื่อสร้างใบสั่งขายที่สอง</span><span class="sxs-lookup"><span data-stu-id="fedfb-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="fedfb-291">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ในฟิลด์ **บัญชีลูกค้า** ให้เลือก _US-008_</span><span class="sxs-lookup"><span data-stu-id="fedfb-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="fedfb-292">ในฟิลด์  **คลังสินค้า** เลือก _61_</span><span class="sxs-lookup"><span data-stu-id="fedfb-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="fedfb-293">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="fedfb-293">The new sales order is opened.</span></span> <span data-ttu-id="fedfb-294">ซึ่งมีบรรทัดว่างบน FastTab **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="fedfb-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="fedfb-295">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fedfb-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="fedfb-296">**สินค้า:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="fedfb-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="fedfb-297">**ปริมาณ:** _1_</span><span class="sxs-lookup"><span data-stu-id="fedfb-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="fedfb-298">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fedfb-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="fedfb-299">ศึกษาสถานการณ์จำลองการแบ่งช่วงเวลาทั่วไป</span><span class="sxs-lookup"><span data-stu-id="fedfb-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="fedfb-300">หลังจากที่มีองค์ประกอบของข้อกำหนดเบื้องต้นทั้งหมดแล้ว ตามที่อธิบายไว้ในหัวข้อก่อนหน้านี้ คุณก็พร้อมแล้วที่จะลองใช้คุณลักษณะนี้โดยการศึกษาแบบฝึกหัดแต่ละรายการในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="fedfb-301">สร้างความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-301">Generate demand</span></span>

1. <span data-ttu-id="fedfb-302">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการแบ่งช่วงเวลา** และเลือกเท็มเพลตการแบ่งช่วงเวลาที่คุณสร้างก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="fedfb-303">ในบานหน้าต่างการดำเนินการ เลือก **สร้างความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="fedfb-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="fedfb-304">คำสั่งนี้จะประเมินความต้องการทั้งหมดที่อยู่ในระบบ และที่ตรงกับการสอบถามเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="fedfb-305">จากนั้น จะมีการรวมความต้องการทั้งหมดในใบสั่งทั้งหมดไปยังบรรทัดเดียวต่อปริมาณ/หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="fedfb-306">ข้อความแสดงข้อมูลจะปรากฏขึ้น เมื่อกระบวนการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fedfb-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="fedfb-307">ความต้องการในการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-307">Slotting demand</span></span>

<span data-ttu-id="fedfb-308">*ความต้องการการแบ่งช่วงเวลา* แสดงผลลัพธ์ของการสร้างความต้องการ ตามการตั้งค่าของเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="fedfb-309">ในบานหน้าต่างการดำเนินการ ให้เลือก **ความต้องการการแบ่งช่วงเวลา** เพื่อดูผลลัพธ์จากคำสั่ง **สร้างความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="fedfb-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="fedfb-310">บรรทัดในความต้องการการแบ่งช่วงเวลาสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="fedfb-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="fedfb-311">คุณสามารถลบบรรทัด เพิ่มบรรทัดใหม่ หรือแก้ไขรายละเอียดของบรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="fedfb-312">คุณสามารถแก้ไขความต้องการด้วยตนเอง หรือคุณสามารถนำเข้าจากระบบภายนอกโดยใช้การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fedfb-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="fedfb-313">สิ่งใดก็ตามที่อยู่ในความต้องการการแบ่งช่วงเวลาจะถูกนำมาใช้ในขั้นตอนต่อไป โดยไม่คำนึงถึงสถานที่ที่มา</span><span class="sxs-lookup"><span data-stu-id="fedfb-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="fedfb-314">ค้นหาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-314">Locate demand</span></span>

<span data-ttu-id="fedfb-315">หลังจากที่สร้างความต้องการแล้ว คุณต้องใช้คำสั่ง **ค้นหาความต้องการ** เพื่อสร้าง *แผนการแบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="fedfb-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="fedfb-316">ในบานหน้าต่างการดำเนินการ เลือก **ค้นหาความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="fedfb-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="fedfb-317">กระบวนการแบ่งช่วงเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="fedfb-317">The slotting process runs.</span></span> <span data-ttu-id="fedfb-318">ข้อความแสดงข้อมูลจะปรากฏขึ้น เมื่อกระบวนการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fedfb-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="fedfb-319">แผนการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fedfb-319">Slotting plan</span></span>

<span data-ttu-id="fedfb-320">แผนการแบ่งช่วงเวลาแสดงสถานที่ที่กำหนดให้กับสินค้า/ปริมาณแต่ละรายการ ไม่ว่าจะมีการใช้มากเกินไปหรือไม่ หรือไม่ว่าจะมีการสร้างงานการหยุดหรือไม่ และบรรทัดเท็มเพลตที่ใช้</span><span class="sxs-lookup"><span data-stu-id="fedfb-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="fedfb-321">**ความต้องการใดๆ ที่ไม่สามารถแบ่งช่วงเวลาได้ ถูกเน้นเป็นสีแดง**</span><span class="sxs-lookup"><span data-stu-id="fedfb-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="fedfb-322">ในบานหน้าต่างการดำเนินการ ให้เลือก **แผนการแบ่งช่วงเวลา** เพื่อดูผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="fedfb-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="fedfb-323">สร้างการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-323">Create replenishment</span></span>

<span data-ttu-id="fedfb-324">หลังจากที่สร้างแผนการแบ่งช่วงเวลาแล้ว คุณต้องสร้าง *งานการเติมสินค้า* ตามแผน</span><span class="sxs-lookup"><span data-stu-id="fedfb-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="fedfb-325">บนบานหน้าต่างการดำเนินการ เลือก **รันการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="fedfb-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="fedfb-326">ข้อความแสดงข้อมูลจะปรากฏขึ้น เมื่อกระบวนการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fedfb-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="fedfb-327">ข้อความนี้แสดงจำนวนของส่วนหัวที่สร้างขึ้นสำหรับรหัสการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fedfb-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="fedfb-328">มีการระบุคำสั่งสถานที่ที่จะใช้ตามรหัสคำสั่งที่มีการระบุไว้ในบรรทัดเท็มเพลตแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="fedfb-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="fedfb-329">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="fedfb-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="fedfb-330">ตั้งค่าการแบ่งช่วงเวลาแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fedfb-330">Set up automatic slotting</span></span>

<span data-ttu-id="fedfb-331">หลังจากที่มีองค์ประกอบที่ต้องการทั้งหมด คุณสามารถตั้งค่าการแบ่งช่วงเวลาเพื่อรันโดยอัตโนมัติโดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fedfb-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="fedfb-332">ไปที่ **การจัดการคลังสินค้า \> การเติมสินค้า \> รันการแบ่งช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="fedfb-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="fedfb-333">ระบุขั้นตอนการแบ่งช่วงเวลาที่จะรัน</span><span class="sxs-lookup"><span data-stu-id="fedfb-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="fedfb-334">เลือกขั้นตอนการแบ่งช่วงเวลาต่อไปนี้อย่างน้อยหนึ่งขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="fedfb-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="fedfb-335">สร้างความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-335">Generate demand</span></span>
    - <span data-ttu-id="fedfb-336">ค้นหาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-336">Locate demand</span></span>
    - <span data-ttu-id="fedfb-337">สร้างงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="fedfb-338">ขั้นตอนการแบ่งช่วงเวลามีความก้าวหน้า</span><span class="sxs-lookup"><span data-stu-id="fedfb-338">The slotting steps are progressive.</span></span> <span data-ttu-id="fedfb-339">ถ้าคุณต้องการเลือก *ค้นหาความต้องการ* คุณต้องเลือก *สร้างความต้องการ* ก่อน</span><span class="sxs-lookup"><span data-stu-id="fedfb-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="fedfb-340">ระบุเท็มเพลตการแบ่งช่วงเวลาที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="fedfb-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="fedfb-341">ตั้งค่าการเกิดซ้ำเพื่อรันโดยอัตโนมัติ ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="fedfb-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="fedfb-342">สำหรับแบบฝึกหัดในสถานการณ์สมมติ **อย่า** ตั้งค่าการแบ่งช่วงเวลาแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fedfb-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
