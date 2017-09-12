--- 
title: "สร้างวัตถุดิบ (กุมภาพันธ์ 2016 เท่านั้น)"
description: "งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป"
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
ms.openlocfilehash: f1c10e0f8275d928c1455cd99105aece8780e7f0
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="c9552-103">สร้างวัตถุดิบ (กุมภาพันธ์ 2016 เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="c9552-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9552-104">งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="c9552-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="c9552-105">นี่คืองานที่สามในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="c9552-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="c9552-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c9552-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="c9552-107">สร้างวัตถุดิบแรก</span><span class="sxs-lookup"><span data-stu-id="c9552-107">Create the first material</span></span>
1. <span data-ttu-id="c9552-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="c9552-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c9552-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c9552-109">Click New.</span></span>
3. <span data-ttu-id="c9552-110">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c9552-111">สำหรับตัวอย่างนี้ ให้ป้อน ITEM_A</span><span class="sxs-lookup"><span data-stu-id="c9552-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="c9552-112">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-113">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="c9552-113">Select STD.</span></span> <span data-ttu-id="c9552-114">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="c9552-115">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-116">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="c9552-116">For example, select Audio.</span></span> <span data-ttu-id="c9552-117">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="c9552-118">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-119">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="c9552-119">Select SiteWH.</span></span> <span data-ttu-id="c9552-120">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="c9552-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="c9552-121">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-122">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="c9552-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c9552-123">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="c9552-123">Select None.</span></span>  
8. <span data-ttu-id="c9552-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c9552-124">Click OK.</span></span>
9. <span data-ttu-id="c9552-125">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="c9552-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="c9552-126">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c9552-126">Click Default order settings.</span></span>
11. <span data-ttu-id="c9552-127">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-128">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c9552-129">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-130">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c9552-131">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-132">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="c9552-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-133">Close the page.</span></span>
15. <span data-ttu-id="c9552-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-134">Close the page.</span></span>
16. <span data-ttu-id="c9552-135">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c9552-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c9552-136">คลิก ITEM_A</span><span class="sxs-lookup"><span data-stu-id="c9552-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="c9552-137">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="c9552-138">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c9552-139">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="c9552-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="c9552-140">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="c9552-141">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9552-141">Click Item price.</span></span>
21. <span data-ttu-id="c9552-142">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c9552-142">Click New.</span></span>
22. <span data-ttu-id="c9552-143">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-144">สำหรับตัวอย่างนี้ ให้เลือก 10 ซึ่งเป็นชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="c9552-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="c9552-145">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-146">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="c9552-147">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c9552-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c9552-148">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="c9552-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="c9552-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c9552-149">Click Save.</span></span>
26. <span data-ttu-id="c9552-150">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="c9552-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="c9552-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-151">Close the page.</span></span>
28. <span data-ttu-id="c9552-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="c9552-153">สร้างวัตถุดิบที่สอง</span><span class="sxs-lookup"><span data-stu-id="c9552-153">Create the second material</span></span>
1. <span data-ttu-id="c9552-154">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c9552-154">Click New.</span></span>
2. <span data-ttu-id="c9552-155">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c9552-156">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_B</span><span class="sxs-lookup"><span data-stu-id="c9552-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="c9552-157">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-158">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="c9552-158">Select STD.</span></span> <span data-ttu-id="c9552-159">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="c9552-160">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-161">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="c9552-161">For example, select Audio.</span></span> <span data-ttu-id="c9552-162">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="c9552-163">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-164">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="c9552-164">Select SiteWH.</span></span> <span data-ttu-id="c9552-165">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="c9552-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="c9552-166">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-167">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="c9552-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c9552-168">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="c9552-168">Select None.</span></span>  
7. <span data-ttu-id="c9552-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c9552-169">Click OK.</span></span>
8. <span data-ttu-id="c9552-170">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="c9552-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="c9552-171">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c9552-171">Click Default order settings.</span></span>
10. <span data-ttu-id="c9552-172">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-173">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="c9552-174">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-175">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c9552-176">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-177">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c9552-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-178">Close the page.</span></span>
14. <span data-ttu-id="c9552-179">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-179">Close the page.</span></span>
15. <span data-ttu-id="c9552-180">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c9552-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c9552-181">คลิก ITEM_B</span><span class="sxs-lookup"><span data-stu-id="c9552-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="c9552-182">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="c9552-183">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c9552-184">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="c9552-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="c9552-185">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="c9552-186">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9552-186">Click Item price.</span></span>
20. <span data-ttu-id="c9552-187">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c9552-187">Click New.</span></span>
21. <span data-ttu-id="c9552-188">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-189">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="c9552-189">For this example, select 10.</span></span> <span data-ttu-id="c9552-190">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="c9552-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="c9552-191">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-192">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="c9552-193">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c9552-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c9552-194">สำหรับการสาธิต ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="c9552-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="c9552-195">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c9552-195">Click Save.</span></span>
25. <span data-ttu-id="c9552-196">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="c9552-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="c9552-197">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-197">Close the page.</span></span>
27. <span data-ttu-id="c9552-198">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="c9552-199">สร้างวัตถุดิบที่สาม</span><span class="sxs-lookup"><span data-stu-id="c9552-199">Create the third material</span></span>
1. <span data-ttu-id="c9552-200">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c9552-200">Click New.</span></span>
2. <span data-ttu-id="c9552-201">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c9552-202">สำหรับการสาธิต ให้พิมพ์ ITEM_C</span><span class="sxs-lookup"><span data-stu-id="c9552-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="c9552-203">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-204">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="c9552-204">Select STD.</span></span> <span data-ttu-id="c9552-205">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="c9552-206">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-207">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="c9552-207">For example, select Audio.</span></span> <span data-ttu-id="c9552-208">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="c9552-209">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-210">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="c9552-210">Select SiteWH.</span></span> <span data-ttu-id="c9552-211">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="c9552-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="c9552-212">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-213">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="c9552-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c9552-214">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="c9552-214">Select None.</span></span>  
7. <span data-ttu-id="c9552-215">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c9552-215">Click OK.</span></span>
8. <span data-ttu-id="c9552-216">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="c9552-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="c9552-217">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c9552-217">Click Default order settings.</span></span>
10. <span data-ttu-id="c9552-218">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-219">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="c9552-220">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-221">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c9552-222">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c9552-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-223">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c9552-224">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-224">Close the page.</span></span>
14. <span data-ttu-id="c9552-225">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-225">Close the page.</span></span>
15. <span data-ttu-id="c9552-226">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c9552-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c9552-227">คลิก ITEM_C</span><span class="sxs-lookup"><span data-stu-id="c9552-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="c9552-228">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="c9552-229">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c9552-230">สำหรับตัวอย่างนี้ ให้พิมพ์ M1</span><span class="sxs-lookup"><span data-stu-id="c9552-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="c9552-231">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c9552-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="c9552-232">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9552-232">Click Item price.</span></span>
20. <span data-ttu-id="c9552-233">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c9552-233">Click New.</span></span>
21. <span data-ttu-id="c9552-234">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-235">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="c9552-235">For this example, select 10.</span></span> <span data-ttu-id="c9552-236">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="c9552-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="c9552-237">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c9552-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c9552-238">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="c9552-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="c9552-239">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c9552-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c9552-240">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="c9552-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="c9552-241">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c9552-241">Click Save.</span></span>
25. <span data-ttu-id="c9552-242">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="c9552-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="c9552-243">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-243">Close the page.</span></span>
27. <span data-ttu-id="c9552-244">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9552-244">Close the page.</span></span>


