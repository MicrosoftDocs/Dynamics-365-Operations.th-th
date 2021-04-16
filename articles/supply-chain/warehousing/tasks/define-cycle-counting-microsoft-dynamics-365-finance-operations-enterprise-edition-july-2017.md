---
title: 'กำหนดการตรวจนับตามรอบ '
description: 'การตรวจนับตามรอบเป็นกระบวนการคลังสินค้าที่คุณสามารถใช้ตรวจสอบสินค้าคงคลังคงเหลือ '
author: MarkusFogelberg
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 995212dd40f8665da64ca0bf8e1c878002778904
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830965"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="b4e64-103">กำหนดการตรวจนับตามรอบ </span><span class="sxs-lookup"><span data-stu-id="b4e64-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4e64-104">การตรวจนับตามรอบเป็นกระบวนการคลังสินค้าที่คุณสามารถใช้ตรวจสอบสินค้าคงคลังคงเหลือ </span><span class="sxs-lookup"><span data-stu-id="b4e64-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="b4e64-105">การบันทึกงานนี้แสดงวิธีการตั้งค่าระดับความสำคัญของงานการตรวจนับเริ่มต้น เปิดใช้งานรายการเมนูบนอุปกรณ์เคลื่อนที่เพื่อประมวลผลทั้งการเบิกสินค้าและการดำเนินงานการตรวจนับ เปิดใช้งานทริกเกอร์ขีดจำกัดการตรวจนับเมื่อสถานที่ว่างเปล่า และเปิดใช้งานแผนการตรวจนับตามรอบสำหรับสินค้าเฉพาะภายในคลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b4e64-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="b4e64-106">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b4e64-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="b4e64-107">คุณสามารถดำเนินการกระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือในข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="b4e64-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="b4e64-108">ตั้งค่าระดับความสำคัญของงานการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="b4e64-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="b4e64-109">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="b4e64-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="b4e64-110">คลิกแท็บ **การตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="b4e64-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="b4e64-111">ในฟิลด์ **ระดับความสำคัญของงานการตรวจนับตามรอบเริ่มต้น** ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b4e64-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="b4e64-112">ขั้นตอนนี้เปลี่ยนระดับความสำคัญของงานการตรวจนับตามรอบโดยเปรียบเทียบกับชนิดอื่น ๆ ของงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b4e64-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="b4e64-113">คุณสามารถยกระดับความสำคัญของงานการตรวจนับตามรอบได้โดยการป้อนหมายเลขที่ต่ำกว่าหมายเลขของงานชนิดอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b4e64-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="b4e64-114">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4e64-114">Click **Save**.</span></span>
5. <span data-ttu-id="b4e64-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b4e64-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="b4e64-116">เปิดใช้งานอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="b4e64-116">Enable the mobile device</span></span>
1. <span data-ttu-id="b4e64-117">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="b4e64-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="b4e64-118">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-118">Click **New**.</span></span>
3. <span data-ttu-id="b4e64-119">ในฟิลด์ **ชื่อรายการในเมนู** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b4e64-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="b4e64-120">ในฟิลด์ **หัวข้อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="b4e64-121">ในฟิลด์ **โหมด** เลือก 'งาน'</span><span class="sxs-lookup"><span data-stu-id="b4e64-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="b4e64-122">ตั้งค่าตัวเลือก **ใช้งานที่มีอยู่** เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="b4e64-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="b4e64-123">เมื่อคุณตั้งค่าตัวเลือกนี้เป็น ใช่ ระบบจะค้นหางานที่มีอยู่เมื่อรายการเมนูบนอุปกรณ์เคลื่อนที่ถูกใช้ไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="b4e64-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="b4e64-124">ในฟิลด์ **สั่งการโดย** เลือก 'สั่งการโดยระบบ'</span><span class="sxs-lookup"><span data-stu-id="b4e64-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="b4e64-125">เมื่อมีการเลือก "สั่งการโดยระบบ" ผู้ปฏิบัติงานคลังสินค้าจะถูกส่งการให้เปิดงานที่อยู่ในคลาสงานที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="b4e64-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="b4e64-126">(ถัดไปเราจะสร้างคลาสงานเหล่านี้)</span><span class="sxs-lookup"><span data-stu-id="b4e64-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="b4e64-127">ขยาย fastTab **คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="b4e64-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="b4e64-128">ถัดไป เราจะสร้างคลาสงานสองชิ้นที่จะใช้กับรายการเมนูบนอุปกรณ์เคลื่อนที่นี้</span><span class="sxs-lookup"><span data-stu-id="b4e64-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="b4e64-129">เมื่อรายการเมนูถูกใช้ คลาสงานเหล่านี้จะถูกสอบถาม และจะแสดงงานที่มีระดับความสำคัญสูงสุดต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b4e64-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="b4e64-130">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-130">Click **New**.</span></span>
10. <span data-ttu-id="b4e64-131">ในฟิลด์ **รหัสคลาสงาน** เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="b4e64-132">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-132">Click **New**.</span></span>
12. <span data-ttu-id="b4e64-133">ในฟิลด์ **รหัสคลาสงาน** เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="b4e64-134">ใน **บานหน้าต่างการดำเนินการ** คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4e64-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="b4e64-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b4e64-135">Close the page.</span></span>
15. <span data-ttu-id="b4e64-136">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > เมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="b4e64-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="b4e64-137">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b4e64-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b4e64-138">ในแผนภูมิ เลือก 'รายการเมนูที่คุณเพิ่งสร้างขึ้น'</span><span class="sxs-lookup"><span data-stu-id="b4e64-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="b4e64-139">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b4e64-139">Click **Edit**.</span></span>
19. <span data-ttu-id="b4e64-140">คลิก ลูกศรเพื่อเพิ่มรายการเมนูลงในเมนู</span><span class="sxs-lookup"><span data-stu-id="b4e64-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="b4e64-141">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4e64-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="b4e64-142">สร้าง ขีดจำกัดการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="b4e64-142">Create a counting threshold</span></span>
1. <span data-ttu-id="b4e64-143">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > วงจรการตรวจนับตามรอบ > ขีดจำกัดการตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="b4e64-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="b4e64-144">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-144">Click **New**.</span></span>
3. <span data-ttu-id="b4e64-145">ในฟิลด์ **รหัสขีดจำกัดการตรวจนับตามรอบ** พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="b4e64-146">ตั้งค่าตัวเลือก **ดำเนินการตรวจนับตามรอบทันที** เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="b4e64-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="b4e64-147">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="b4e64-148">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4e64-148">Click **Save**.</span></span>
7. <span data-ttu-id="b4e64-149">คลิก **เลือกสถานที่**</span><span class="sxs-lookup"><span data-stu-id="b4e64-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="b4e64-150">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e64-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b4e64-151">ในฟิลด์ **เงื่อนไข** เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="b4e64-152">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-152">Click **OK**.</span></span>
11. <span data-ttu-id="b4e64-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b4e64-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="b4e64-154">สร้าง แผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="b4e64-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="b4e64-155">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > วงจรการตรวจนับตามรอบ > แผนการตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="b4e64-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="b4e64-156">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-156">Click **New**.</span></span>
3. <span data-ttu-id="b4e64-157">ในฟิลด์ **รหัสแผนการตรวจนับตามรอบ** พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="b4e64-158">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b4e64-159">ในฟิลด์ **จำนวนสูงสุดของการตรวจนับตามรอบ** ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b4e64-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="b4e64-160">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4e64-160">Click **Save**.</span></span>
7. <span data-ttu-id="b4e64-161">คลิก **เลือกสถานที่**</span><span class="sxs-lookup"><span data-stu-id="b4e64-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="b4e64-162">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e64-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b4e64-163">ในฟิลด์ **เงื่อนไข** เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="b4e64-164">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-164">Click **OK**.</span></span>
11. <span data-ttu-id="b4e64-165">ในฟิลด์ **จำนวนวันระหว่างการตรวจนับตามรอบ** ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b4e64-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="b4e64-166">ตัวอย่างเช่น ถ้าฟิลด์ **จำนวนวันระหว่างการตรวจนับตามรอบ** ถูกตั้งค่าเป็น 5 งานการตรวจนับตามรอบจะถูกสร้างทุกๆ ห้าวัน</span><span class="sxs-lookup"><span data-stu-id="b4e64-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="b4e64-167">อย่างไรก็ตาม ถ้างานการตรวจนับตามรอบถูกประมวลผลในวันที่สาม งานการตรวจนับครั้งถัดไปจะสร้างขึ้นห้าวันหลังจากการตรวจนับตามรอบครั้งสุดท้ายที่ถูกประมวลผล ก็คือในวันที่แปด</span><span class="sxs-lookup"><span data-stu-id="b4e64-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="b4e64-168">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4e64-168">Click **Save**.</span></span>
13. <span data-ttu-id="b4e64-169">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-169">Click **New**.</span></span>
14. <span data-ttu-id="b4e64-170">ในฟิลด์ **หมายเลขลำดับ** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b4e64-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="b4e64-171">การเรียงคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="b4e64-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="b4e64-172">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="b4e64-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="b4e64-173">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e64-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="b4e64-174">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b4e64-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="b4e64-175">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b4e64-175">Click **Save**.</span></span>
18. <span data-ttu-id="b4e64-176">คลิกการสอบถาม **กำหนดผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="b4e64-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="b4e64-177">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e64-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b4e64-178">ในฟิลด์ **เกณฑ์** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b4e64-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="b4e64-179">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b4e64-179">Click **OK**.</span></span>
22. <span data-ttu-id="b4e64-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b4e64-180">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]