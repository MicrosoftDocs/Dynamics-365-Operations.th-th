--- 
title: "สร้างวัตถุดิบ (กุมภาพันธ์ 2016 เท่านั้น)"
description: "งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5a31ceacb7037164d35e38fb70a013b33d670d94
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="3ef52-103">สร้างวัตถุดิบ (กุมภาพันธ์ 2016 เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="3ef52-103">Create raw materials (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ef52-104">งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="3ef52-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="3ef52-105">นี่คืองานที่สามในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="3ef52-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="3ef52-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="3ef52-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="3ef52-107">สร้างวัตถุดิบแรก</span><span class="sxs-lookup"><span data-stu-id="3ef52-107">Create the first material</span></span>
1. <span data-ttu-id="3ef52-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="3ef52-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="3ef52-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3ef52-109">Click New.</span></span>
3. <span data-ttu-id="3ef52-110">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="3ef52-111">สำหรับตัวอย่างนี้ ให้ป้อน ITEM_A</span><span class="sxs-lookup"><span data-stu-id="3ef52-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="3ef52-112">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-113">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="3ef52-113">Select STD.</span></span> <span data-ttu-id="3ef52-114">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="3ef52-115">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-116">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="3ef52-116">For example, select Audio.</span></span> <span data-ttu-id="3ef52-117">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="3ef52-118">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-119">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="3ef52-119">Select SiteWH.</span></span> <span data-ttu-id="3ef52-120">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="3ef52-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="3ef52-121">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-122">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="3ef52-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="3ef52-123">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="3ef52-123">Select None.</span></span>  
8. <span data-ttu-id="3ef52-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3ef52-124">Click OK.</span></span>
9. <span data-ttu-id="3ef52-125">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3ef52-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="3ef52-126">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3ef52-126">Click Default order settings.</span></span>
11. <span data-ttu-id="3ef52-127">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-128">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="3ef52-129">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-130">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="3ef52-131">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-132">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="3ef52-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-133">Close the page.</span></span>
15. <span data-ttu-id="3ef52-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-134">Close the page.</span></span>
16. <span data-ttu-id="3ef52-135">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3ef52-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3ef52-136">คลิก ITEM_A</span><span class="sxs-lookup"><span data-stu-id="3ef52-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="3ef52-137">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="3ef52-138">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="3ef52-139">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="3ef52-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="3ef52-140">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="3ef52-141">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-141">Click Item price.</span></span>
21. <span data-ttu-id="3ef52-142">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3ef52-142">Click New.</span></span>
22. <span data-ttu-id="3ef52-143">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-144">สำหรับตัวอย่างนี้ ให้เลือก 10 ซึ่งเป็นชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="3ef52-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="3ef52-145">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-146">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="3ef52-147">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3ef52-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="3ef52-148">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="3ef52-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="3ef52-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3ef52-149">Click Save.</span></span>
26. <span data-ttu-id="3ef52-150">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="3ef52-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="3ef52-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-151">Close the page.</span></span>
28. <span data-ttu-id="3ef52-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="3ef52-153">สร้างวัตถุดิบที่สอง</span><span class="sxs-lookup"><span data-stu-id="3ef52-153">Create the second material</span></span>
1. <span data-ttu-id="3ef52-154">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3ef52-154">Click New.</span></span>
2. <span data-ttu-id="3ef52-155">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="3ef52-156">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_B</span><span class="sxs-lookup"><span data-stu-id="3ef52-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="3ef52-157">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-158">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="3ef52-158">Select STD.</span></span> <span data-ttu-id="3ef52-159">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="3ef52-160">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-161">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="3ef52-161">For example, select Audio.</span></span> <span data-ttu-id="3ef52-162">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="3ef52-163">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-164">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="3ef52-164">Select SiteWH.</span></span> <span data-ttu-id="3ef52-165">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="3ef52-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="3ef52-166">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-167">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="3ef52-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="3ef52-168">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="3ef52-168">Select None.</span></span>  
7. <span data-ttu-id="3ef52-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3ef52-169">Click OK.</span></span>
8. <span data-ttu-id="3ef52-170">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3ef52-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="3ef52-171">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3ef52-171">Click Default order settings.</span></span>
10. <span data-ttu-id="3ef52-172">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-173">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="3ef52-174">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-175">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="3ef52-176">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-177">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="3ef52-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-178">Close the page.</span></span>
14. <span data-ttu-id="3ef52-179">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-179">Close the page.</span></span>
15. <span data-ttu-id="3ef52-180">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3ef52-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3ef52-181">คลิก ITEM_B</span><span class="sxs-lookup"><span data-stu-id="3ef52-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="3ef52-182">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="3ef52-183">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="3ef52-184">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="3ef52-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="3ef52-185">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="3ef52-186">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-186">Click Item price.</span></span>
20. <span data-ttu-id="3ef52-187">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3ef52-187">Click New.</span></span>
21. <span data-ttu-id="3ef52-188">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-189">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="3ef52-189">For this example, select 10.</span></span> <span data-ttu-id="3ef52-190">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="3ef52-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="3ef52-191">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-192">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="3ef52-193">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3ef52-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="3ef52-194">สำหรับการสาธิต ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="3ef52-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="3ef52-195">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3ef52-195">Click Save.</span></span>
25. <span data-ttu-id="3ef52-196">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="3ef52-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="3ef52-197">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-197">Close the page.</span></span>
27. <span data-ttu-id="3ef52-198">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="3ef52-199">สร้างวัตถุดิบที่สาม</span><span class="sxs-lookup"><span data-stu-id="3ef52-199">Create the third material</span></span>
1. <span data-ttu-id="3ef52-200">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3ef52-200">Click New.</span></span>
2. <span data-ttu-id="3ef52-201">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="3ef52-202">สำหรับการสาธิต ให้พิมพ์ ITEM_C</span><span class="sxs-lookup"><span data-stu-id="3ef52-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="3ef52-203">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-204">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="3ef52-204">Select STD.</span></span> <span data-ttu-id="3ef52-205">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="3ef52-206">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-207">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="3ef52-207">For example, select Audio.</span></span> <span data-ttu-id="3ef52-208">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="3ef52-209">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-210">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="3ef52-210">Select SiteWH.</span></span> <span data-ttu-id="3ef52-211">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="3ef52-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="3ef52-212">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-213">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="3ef52-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="3ef52-214">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="3ef52-214">Select None.</span></span>  
7. <span data-ttu-id="3ef52-215">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3ef52-215">Click OK.</span></span>
8. <span data-ttu-id="3ef52-216">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3ef52-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="3ef52-217">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3ef52-217">Click Default order settings.</span></span>
10. <span data-ttu-id="3ef52-218">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-219">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="3ef52-220">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-221">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="3ef52-222">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ef52-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-223">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="3ef52-224">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-224">Close the page.</span></span>
14. <span data-ttu-id="3ef52-225">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-225">Close the page.</span></span>
15. <span data-ttu-id="3ef52-226">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3ef52-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3ef52-227">คลิก ITEM_C</span><span class="sxs-lookup"><span data-stu-id="3ef52-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="3ef52-228">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="3ef52-229">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="3ef52-230">สำหรับตัวอย่างนี้ ให้พิมพ์ M1</span><span class="sxs-lookup"><span data-stu-id="3ef52-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="3ef52-231">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3ef52-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="3ef52-232">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-232">Click Item price.</span></span>
20. <span data-ttu-id="3ef52-233">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3ef52-233">Click New.</span></span>
21. <span data-ttu-id="3ef52-234">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-235">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="3ef52-235">For this example, select 10.</span></span> <span data-ttu-id="3ef52-236">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="3ef52-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="3ef52-237">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ef52-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="3ef52-238">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="3ef52-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="3ef52-239">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3ef52-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="3ef52-240">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="3ef52-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="3ef52-241">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3ef52-241">Click Save.</span></span>
25. <span data-ttu-id="3ef52-242">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="3ef52-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="3ef52-243">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-243">Close the page.</span></span>
27. <span data-ttu-id="3ef52-244">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ef52-244">Close the page.</span></span>


