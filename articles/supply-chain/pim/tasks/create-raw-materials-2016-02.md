--- 
title: "สร้างวัตถุดิบ (กุมภาพันธ์ 2016)"
description: "งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="93578-103">สร้างวัตถุดิบ (กุมภาพันธ์ 2016)</span><span class="sxs-lookup"><span data-stu-id="93578-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93578-104">งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="93578-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="93578-105">นี่คืองานที่สามในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="93578-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="93578-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="93578-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="93578-107">สร้างวัตถุดิบแรก</span><span class="sxs-lookup"><span data-stu-id="93578-107">Create the first material</span></span>
1. <span data-ttu-id="93578-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="93578-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="93578-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93578-109">Click New.</span></span>
3. <span data-ttu-id="93578-110">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="93578-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="93578-111">สำหรับตัวอย่างนี้ ให้ป้อน ITEM_A</span><span class="sxs-lookup"><span data-stu-id="93578-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="93578-112">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-113">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="93578-113">Select STD.</span></span> <span data-ttu-id="93578-114">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="93578-115">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-116">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="93578-116">For example, select Audio.</span></span> <span data-ttu-id="93578-117">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="93578-118">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-119">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="93578-119">Select SiteWH.</span></span> <span data-ttu-id="93578-120">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="93578-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="93578-121">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-122">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="93578-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="93578-123">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="93578-123">Select None.</span></span>  
8. <span data-ttu-id="93578-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="93578-124">Click OK.</span></span>
9. <span data-ttu-id="93578-125">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="93578-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="93578-126">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="93578-126">Click Default order settings.</span></span>
11. <span data-ttu-id="93578-127">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-128">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="93578-129">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-130">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="93578-131">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-132">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="93578-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-133">Close the page.</span></span>
15. <span data-ttu-id="93578-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-134">Close the page.</span></span>
16. <span data-ttu-id="93578-135">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93578-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93578-136">คลิก ITEM_A</span><span class="sxs-lookup"><span data-stu-id="93578-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="93578-137">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="93578-138">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="93578-139">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="93578-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="93578-140">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="93578-141">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="93578-141">Click Item price.</span></span>
21. <span data-ttu-id="93578-142">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93578-142">Click New.</span></span>
22. <span data-ttu-id="93578-143">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-144">สำหรับตัวอย่างนี้ ให้เลือก 10 ซึ่งเป็นชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="93578-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="93578-145">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-146">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="93578-147">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="93578-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="93578-148">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="93578-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="93578-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="93578-149">Click Save.</span></span>
26. <span data-ttu-id="93578-150">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="93578-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="93578-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-151">Close the page.</span></span>
28. <span data-ttu-id="93578-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="93578-153">สร้างวัตถุดิบที่สอง</span><span class="sxs-lookup"><span data-stu-id="93578-153">Create the second material</span></span>
1. <span data-ttu-id="93578-154">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93578-154">Click New.</span></span>
2. <span data-ttu-id="93578-155">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="93578-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="93578-156">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_B</span><span class="sxs-lookup"><span data-stu-id="93578-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="93578-157">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-158">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="93578-158">Select STD.</span></span> <span data-ttu-id="93578-159">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="93578-160">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-161">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="93578-161">For example, select Audio.</span></span> <span data-ttu-id="93578-162">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="93578-163">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-164">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="93578-164">Select SiteWH.</span></span> <span data-ttu-id="93578-165">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="93578-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="93578-166">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-167">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="93578-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="93578-168">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="93578-168">Select None.</span></span>  
7. <span data-ttu-id="93578-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="93578-169">Click OK.</span></span>
8. <span data-ttu-id="93578-170">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="93578-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="93578-171">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="93578-171">Click Default order settings.</span></span>
10. <span data-ttu-id="93578-172">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-173">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="93578-174">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-175">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="93578-176">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-177">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="93578-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-178">Close the page.</span></span>
14. <span data-ttu-id="93578-179">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-179">Close the page.</span></span>
15. <span data-ttu-id="93578-180">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93578-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93578-181">คลิก ITEM_B</span><span class="sxs-lookup"><span data-stu-id="93578-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="93578-182">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="93578-183">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="93578-184">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="93578-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="93578-185">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="93578-186">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="93578-186">Click Item price.</span></span>
20. <span data-ttu-id="93578-187">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93578-187">Click New.</span></span>
21. <span data-ttu-id="93578-188">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-189">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="93578-189">For this example, select 10.</span></span> <span data-ttu-id="93578-190">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="93578-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="93578-191">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-192">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="93578-193">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="93578-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="93578-194">สำหรับการสาธิต ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="93578-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="93578-195">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="93578-195">Click Save.</span></span>
25. <span data-ttu-id="93578-196">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="93578-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="93578-197">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-197">Close the page.</span></span>
27. <span data-ttu-id="93578-198">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="93578-199">สร้างวัตถุดิบที่สาม</span><span class="sxs-lookup"><span data-stu-id="93578-199">Create the third material</span></span>
1. <span data-ttu-id="93578-200">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93578-200">Click New.</span></span>
2. <span data-ttu-id="93578-201">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="93578-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="93578-202">สำหรับการสาธิต ให้พิมพ์ ITEM_C</span><span class="sxs-lookup"><span data-stu-id="93578-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="93578-203">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-204">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="93578-204">Select STD.</span></span> <span data-ttu-id="93578-205">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="93578-206">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-207">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="93578-207">For example, select Audio.</span></span> <span data-ttu-id="93578-208">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="93578-209">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-210">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="93578-210">Select SiteWH.</span></span> <span data-ttu-id="93578-211">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="93578-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="93578-212">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-213">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="93578-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="93578-214">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="93578-214">Select None.</span></span>  
7. <span data-ttu-id="93578-215">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="93578-215">Click OK.</span></span>
8. <span data-ttu-id="93578-216">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="93578-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="93578-217">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="93578-217">Click Default order settings.</span></span>
10. <span data-ttu-id="93578-218">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-219">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="93578-220">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-221">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="93578-222">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93578-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-223">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="93578-224">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-224">Close the page.</span></span>
14. <span data-ttu-id="93578-225">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-225">Close the page.</span></span>
15. <span data-ttu-id="93578-226">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93578-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93578-227">คลิก ITEM_C</span><span class="sxs-lookup"><span data-stu-id="93578-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="93578-228">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="93578-229">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="93578-230">สำหรับตัวอย่างนี้ ให้พิมพ์ M1</span><span class="sxs-lookup"><span data-stu-id="93578-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="93578-231">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="93578-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="93578-232">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="93578-232">Click Item price.</span></span>
20. <span data-ttu-id="93578-233">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93578-233">Click New.</span></span>
21. <span data-ttu-id="93578-234">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-235">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="93578-235">For this example, select 10.</span></span> <span data-ttu-id="93578-236">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="93578-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="93578-237">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93578-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="93578-238">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="93578-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="93578-239">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="93578-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="93578-240">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="93578-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="93578-241">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="93578-241">Click Save.</span></span>
25. <span data-ttu-id="93578-242">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="93578-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="93578-243">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-243">Close the page.</span></span>
27. <span data-ttu-id="93578-244">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93578-244">Close the page.</span></span>


