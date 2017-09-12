--- 
title: "สร้างกระบวนการผลิต (กุมภาพันธ์ 2016 เท่านั้น)"
description: "งานนี้มุ่งเน้นการสร้างกระบวนการผลิตสำหรับผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป"
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df913543d89a502aecfe7e2fe61265a8a1a121c
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="90536-103">สร้างกระบวนการผลิต (กุมภาพันธ์ 2016 เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="90536-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90536-104">งานนี้มุ่งเน้นการสร้างกระบวนการผลิตสำหรับผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="90536-104">This task focuses on creating the production routes for a finished product and and a semi-finished product.</span></span> <span data-ttu-id="90536-105">นี่คืองานที่ห้าในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="90536-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="90536-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="90536-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="90536-107">สร้างกระบวนการผลิตสำหรับผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="90536-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="90536-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="90536-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="90536-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="90536-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90536-110">เลือกหมายเลขสินค้า BOM_2</span><span class="sxs-lookup"><span data-stu-id="90536-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="90536-111">ในบานหน้าต่างการดำเนินการ คลิกวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="90536-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="90536-112">คลิกกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-112">Click Route.</span></span>
5. <span data-ttu-id="90536-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="90536-113">Click New.</span></span>
6. <span data-ttu-id="90536-114">คลิก กระบวนการผลิตและเวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-114">Click Route and route version.</span></span>
7. <span data-ttu-id="90536-115">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="90536-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="90536-116">ตัวอย่างเช่น พิมพ์ ROUTE_2</span><span class="sxs-lookup"><span data-stu-id="90536-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="90536-117">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90536-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-118">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก Site 1</span><span class="sxs-lookup"><span data-stu-id="90536-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="90536-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="90536-119">Click OK.</span></span>
10. <span data-ttu-id="90536-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="90536-120">Click New.</span></span>
11. <span data-ttu-id="90536-121">ในฟิลด์การดำเนินงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90536-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-122">สำหรับตัวอย่างนี้ ให้เลือก ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="90536-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="90536-123">ในฟิลด์เวลาที่ใช้ในการผลิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="90536-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="90536-124">ตัวอย่างเช่น พิมพ์ 1</span><span class="sxs-lookup"><span data-stu-id="90536-124">For example, type 1.</span></span> <span data-ttu-id="90536-125">โดยทั่วไปเวลาที่ใช้ในการผลิตจะเป็นส่วนหนึ่งของราคาที่คำนวณสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="90536-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="90536-126">ในฟิลด์กลุ่มกระบวนการผลิต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="90536-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-127">สำหรับตัวอย่างนี้ ให้เลือก Std</span><span class="sxs-lookup"><span data-stu-id="90536-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="90536-128">คลิกแท็บ การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="90536-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="90536-129">ในฟิลด์ประเภทการตั้งค่า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90536-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-130">สำหรับตัวอย่างนี้ ให้เลือก ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="90536-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="90536-131">คลิกแท็บเวลา</span><span class="sxs-lookup"><span data-stu-id="90536-131">Click the Times tab.</span></span>
17. <span data-ttu-id="90536-132">ในฟิลด์เวลาเซ็ตอัพ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="90536-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="90536-133">สำหรับตัวอย่างนี้ ให้พิมพ์ 1</span><span class="sxs-lookup"><span data-stu-id="90536-133">For this example, type 1.</span></span> <span data-ttu-id="90536-134">โดยทั่วไปเวลาเซ็ตอัพจะเป็นส่วนหนึ่งของราคาที่คำนวณสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="90536-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="90536-135">ในบานหน้าต่างการดำเนินการ คลิกเวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="90536-136">คลิกอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="90536-136">Click Approve.</span></span>
20. <span data-ttu-id="90536-137">เลือก ใช่ ในฟิลด์คุณยังต้องการอนุมัติกระบวนการผลิตหรือไม่ ?</span><span class="sxs-lookup"><span data-stu-id="90536-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="90536-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="90536-138">Click OK.</span></span>
22. <span data-ttu-id="90536-139">ในบานหน้าต่างการดำเนินการ คลิกเวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="90536-140">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="90536-140">Click Activate.</span></span>
24. <span data-ttu-id="90536-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="90536-141">Close the page.</span></span>
25. <span data-ttu-id="90536-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="90536-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="90536-143">สร้างกระบวนการผลิตสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="90536-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="90536-144">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="90536-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90536-145">เลือกหมายเลขสินค้า BOM_1</span><span class="sxs-lookup"><span data-stu-id="90536-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="90536-146">ในบานหน้าต่างการดำเนินการ คลิกวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="90536-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="90536-147">คลิกกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-147">Click Route.</span></span>
4. <span data-ttu-id="90536-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="90536-148">Click New.</span></span>
5. <span data-ttu-id="90536-149">คลิก กระบวนการผลิตและเวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-149">Click Route and route version.</span></span>
6. <span data-ttu-id="90536-150">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="90536-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="90536-151">สำหรับตัวอย่างนี้ ให้พิมพ์ ROUTE_1</span><span class="sxs-lookup"><span data-stu-id="90536-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="90536-152">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90536-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-153">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก Site 1</span><span class="sxs-lookup"><span data-stu-id="90536-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="90536-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="90536-154">Click OK.</span></span>
9. <span data-ttu-id="90536-155">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="90536-155">Click New.</span></span>
10. <span data-ttu-id="90536-156">ในฟิลด์การดำเนินงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90536-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-157">สำหรับตัวอย่างนี้ ให้เลือก การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="90536-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="90536-158">ในฟิลด์เวลาที่ใช้ในการผลิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="90536-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="90536-159">สำหรับตัวอย่างนี้ ให้พิมพ์ 1</span><span class="sxs-lookup"><span data-stu-id="90536-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="90536-160">ในฟิลด์กลุ่มกระบวนการผลิต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="90536-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-161">สำหรับตัวอย่างนี้ ให้เลือก Std</span><span class="sxs-lookup"><span data-stu-id="90536-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="90536-162">คลิกแท็บ การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="90536-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="90536-163">ในฟิลด์ประเภทการตั้งค่า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90536-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="90536-164">สำหรับตัวอย่างนี้ ให้เลือก การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="90536-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="90536-165">คลิกแท็บเวลา</span><span class="sxs-lookup"><span data-stu-id="90536-165">Click the Times tab.</span></span>
16. <span data-ttu-id="90536-166">ในฟิลด์เวลาเซ็ตอัพ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="90536-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="90536-167">สำหรับตัวอย่างนี้ ให้พิมพ์ 1</span><span class="sxs-lookup"><span data-stu-id="90536-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="90536-168">ในบานหน้าต่างการดำเนินการ คลิกเวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="90536-169">คลิกอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="90536-169">Click Approve.</span></span>
19. <span data-ttu-id="90536-170">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="90536-170">Click OK.</span></span>
20. <span data-ttu-id="90536-171">ในบานหน้าต่างการดำเนินการ คลิกเวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="90536-172">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="90536-172">Click Activate.</span></span>
22. <span data-ttu-id="90536-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="90536-173">Close the page.</span></span>
23. <span data-ttu-id="90536-174">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="90536-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="90536-175">เปิดใช้งานปริมาณการใช้เวลาเซ็ตอัพอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="90536-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="90536-176">ไปที่ การควบคุมการผลิต > การตั้งค่า > กระบวนการผลิต > กลุ่มกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="90536-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="90536-177">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="90536-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="90536-178">เลือก Std ในรายการ</span><span class="sxs-lookup"><span data-stu-id="90536-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="90536-179">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="90536-179">Click Edit.</span></span>
4. <span data-ttu-id="90536-180">เลือก ใช่ ในฟิลด์เวลาเซ็ตอัพ</span><span class="sxs-lookup"><span data-stu-id="90536-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="90536-181">โดยทั่วไปเวลาเซ็ตอัพจะเป็นส่วนหนึ่งของราคาที่คำนวณสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="90536-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="90536-182">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="90536-182">Click Save.</span></span>
6. <span data-ttu-id="90536-183">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="90536-183">Close the page.</span></span>


