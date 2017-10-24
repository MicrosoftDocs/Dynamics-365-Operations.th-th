--- 
title: "กำหนดการตรวจนับตามรอบ "
description: "การตรวจนับตามรอบเป็นกระบวนการคลังสินค้าที่คุณสามารถใช้ตรวจสอบสินค้าคงคลังคงเหลือ "
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f9cdb0a7de0199363279c53e817c98085b31fe6b
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="define-cycle-counting"></a><span data-ttu-id="f5cad-103">กำหนดการตรวจนับตามรอบ </span><span class="sxs-lookup"><span data-stu-id="f5cad-103">Define cycle counting</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5cad-104">การตรวจนับตามรอบเป็นกระบวนการคลังสินค้าที่คุณสามารถใช้ตรวจสอบสินค้าคงคลังคงเหลือ </span><span class="sxs-lookup"><span data-stu-id="f5cad-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="f5cad-105">การบันทึกงานนี้แสดงวิธีการตั้งค่าระดับความสำคัญของงานการตรวจนับเริ่มต้น เปิดใช้งานรายการเมนูบนอุปกรณ์เคลื่อนที่เพื่อประมวลผลทั้งการเบิกสินค้าและการดำเนินงานการตรวจนับ เปิดใช้งานทริกเกอร์ขีดจำกัดการตรวจนับเมื่อสถานที่ว่างเปล่า และเปิดใช้งานแผนการตรวจนับตามรอบสำหรับสินค้าเฉพาะภายในคลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="f5cad-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="f5cad-106">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f5cad-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="f5cad-107">คุณสามารถดำเนินการกระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือในข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="f5cad-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="f5cad-108">ตั้งค่าระดับความสำคัญของงานการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="f5cad-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="f5cad-109">ไปที่การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f5cad-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="f5cad-110">คลิก แท็บการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="f5cad-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="f5cad-111">ในฟิลด์ระดับความสำคัญของงานการตรวจนับตามรอบเริ่มต้น ป้อน หมายเลข</span><span class="sxs-lookup"><span data-stu-id="f5cad-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="f5cad-112">ขั้นตอนนี้เปลี่ยนระดับความสำคัญของงานการตรวจนับตามรอบโดยเปรียบเทียบกับชนิดอื่น ๆ ของงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f5cad-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="f5cad-113">คุณสามารถยกระดับความสำคัญของงานการตรวจนับตามรอบได้โดยการป้อนหมายเลขที่ต่ำกว่าหมายเลขของงานชนิดอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f5cad-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="f5cad-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f5cad-114">Click Save.</span></span>
5. <span data-ttu-id="f5cad-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f5cad-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="f5cad-116">เปิดใช้งานอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f5cad-116">Enable the mobile device</span></span>
1. <span data-ttu-id="f5cad-117">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f5cad-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="f5cad-118">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f5cad-118">Click New.</span></span>
3. <span data-ttu-id="f5cad-119">ในฟิลด์ชื่อเมนูสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f5cad-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="f5cad-120">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="f5cad-121">ในฟิลด์โหมด เลือก 'งาน'</span><span class="sxs-lookup"><span data-stu-id="f5cad-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="f5cad-122">ตั้งค่าตัวเลือกใช้งานที่มีอยู่เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="f5cad-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="f5cad-123">เมื่อคุณตั้งค่าตัวเลือกนี้เป็น ใช่ ระบบจะค้นหางานที่มีอยู่เมื่อรายการเมนูบนอุปกรณ์เคลื่อนที่ถูกใช้ไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="f5cad-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="f5cad-124">ในฟิลด์สั่งการโดย เลือก 'สั่งการโดยระบบ'</span><span class="sxs-lookup"><span data-stu-id="f5cad-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="f5cad-125">เมื่อมีการเลือก "สั่งการโดยระบบ" ผู้ปฏิบัติงานคลังสินค้าจะถูกส่งการให้เปิดงานที่อยู่ในคลาสงานที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="f5cad-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="f5cad-126">(ถัดไปเราจะสร้างคลาสงานเหล่านี้)</span><span class="sxs-lookup"><span data-stu-id="f5cad-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="f5cad-127">ขยายหรือยุบส่วนคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="f5cad-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="f5cad-128">ถัดไป เราจะสร้างคลาสงานสองชิ้นที่จะใช้กับรายการเมนูบนอุปกรณ์เคลื่อนที่นี้</span><span class="sxs-lookup"><span data-stu-id="f5cad-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="f5cad-129">เมื่อรายการเมนูถูกใช้ คลาสงานเหล่านี้จะถูกสอบถาม และจะแสดงงานที่มีระดับความสำคัญสูงสุดต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f5cad-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="f5cad-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f5cad-130">Click New.</span></span>
10. <span data-ttu-id="f5cad-131">ในฟิลด์รหัสคลาสงาน เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="f5cad-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f5cad-132">Click New.</span></span>
12. <span data-ttu-id="f5cad-133">ในฟิลด์รหัสคลาสงาน เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="f5cad-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f5cad-134">Click Save.</span></span>
14. <span data-ttu-id="f5cad-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f5cad-135">Close the page.</span></span>
15. <span data-ttu-id="f5cad-136">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > เมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f5cad-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="f5cad-137">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f5cad-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="f5cad-138">ในแผนภูมิ เลือก 'รายการเมนูที่คุณเพิ่งสร้างขึ้น'</span><span class="sxs-lookup"><span data-stu-id="f5cad-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="f5cad-139">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f5cad-139">Click Edit.</span></span>
19. <span data-ttu-id="f5cad-140">คลิก ลูกศรเพื่อเพิ่มรายการเมนูลงในเมนู</span><span class="sxs-lookup"><span data-stu-id="f5cad-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="f5cad-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f5cad-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="f5cad-142">สร้าง ขีดจำกัดการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="f5cad-142">Create a counting threshold</span></span>
1. <span data-ttu-id="f5cad-143">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การตรวจนับตามรอบ > ขีดจำกัดการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="f5cad-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="f5cad-144">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f5cad-144">Click New.</span></span>
3. <span data-ttu-id="f5cad-145">ในฟิลด์รหัสขีดจำกัดการตรวจนับตามรอบ พิมพ์ ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="f5cad-146">ตั้งค่า กระบวนการตัวเลือกการตรวจนับตามรอบทันทีเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="f5cad-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="f5cad-147">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f5cad-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f5cad-148">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="f5cad-148">Click Save.</span></span>
7. <span data-ttu-id="f5cad-149">คลิก เลือก ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-149">Click Select locations.</span></span>
8. <span data-ttu-id="f5cad-150">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f5cad-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f5cad-151">ในฟิลด์เงื่อนไข เลือก ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="f5cad-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f5cad-152">Click OK.</span></span>
11. <span data-ttu-id="f5cad-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f5cad-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="f5cad-154">สร้าง แผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="f5cad-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="f5cad-155">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การตรวจนับตามรอบ > แผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="f5cad-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="f5cad-156">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f5cad-156">Click New.</span></span>
3. <span data-ttu-id="f5cad-157">ในฟิลด์รหัสแผนการตรวจนับตามรอบ พิมพ์ ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="f5cad-158">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f5cad-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f5cad-159">ในฟิลด์จำนวนสูงสุดของการตรวจนับตามรอบ ป้อน หมายเลข</span><span class="sxs-lookup"><span data-stu-id="f5cad-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="f5cad-160">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f5cad-160">Click Save.</span></span>
7. <span data-ttu-id="f5cad-161">คลิก เลือก ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-161">Click Select locations.</span></span>
8. <span data-ttu-id="f5cad-162">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f5cad-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f5cad-163">ในฟิลด์เงื่อนไข เลือก ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="f5cad-164">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f5cad-164">Click OK.</span></span>
11. <span data-ttu-id="f5cad-165">ในฟิลด์จำนวนวันระหว่างการตรวจนับตามรอบ ป้อน หมายเลข</span><span class="sxs-lookup"><span data-stu-id="f5cad-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="f5cad-166">ตัวอย่างเช่น ถ้าฟิลด์จำนวนวันระหว่างการตรวจนับตามรอบถูกตั้งค่าเป็น 5 งานการตรวจนับตามรอบจะสร้างทุกห้าวัน</span><span class="sxs-lookup"><span data-stu-id="f5cad-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="f5cad-167">อย่างไรก็ตาม ถ้างานการตรวจนับตามรอบถูกประมวลผลในวันที่สาม งานการตรวจนับครั้งถัดไปจะสร้างขึ้นห้าวันหลังจากการตรวจนับตามรอบครั้งสุดท้ายที่ถูกประมวลผล ก็คือในวันที่แปด</span><span class="sxs-lookup"><span data-stu-id="f5cad-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="f5cad-168">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f5cad-168">Click Save.</span></span>
13. <span data-ttu-id="f5cad-169">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f5cad-169">Click New.</span></span>
14. <span data-ttu-id="f5cad-170">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="f5cad-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="f5cad-171">การเรียงคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="f5cad-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="f5cad-172">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="f5cad-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="f5cad-173">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f5cad-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="f5cad-174">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f5cad-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="f5cad-175">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f5cad-175">Click Save.</span></span>
18. <span data-ttu-id="f5cad-176">คลิก กำหนดการสอบถามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f5cad-176">Click Define product query.</span></span>
19. <span data-ttu-id="f5cad-177">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f5cad-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="f5cad-178">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5cad-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="f5cad-179">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f5cad-179">Click OK.</span></span>
22. <span data-ttu-id="f5cad-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f5cad-180">Close the page.</span></span>


