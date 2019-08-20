---
title: สร้างวัตถุดิบ (กุมภาพันธ์ 2016)
description: งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844596"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="67cd5-103">สร้างวัตถุดิบ (กุมภาพันธ์ 2016)</span><span class="sxs-lookup"><span data-stu-id="67cd5-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67cd5-104">งานนี้มุ่งเน้นการสร้างส่วนประกอบของผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="67cd5-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="67cd5-105">นี่คืองานที่สามในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="67cd5-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="67cd5-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="67cd5-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="67cd5-107">สร้างวัตถุดิบแรก</span><span class="sxs-lookup"><span data-stu-id="67cd5-107">Create the first material</span></span>
1. <span data-ttu-id="67cd5-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="67cd5-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="67cd5-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="67cd5-109">Click New.</span></span>
3. <span data-ttu-id="67cd5-110">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="67cd5-111">สำหรับตัวอย่างนี้ ให้ป้อน ITEM_A</span><span class="sxs-lookup"><span data-stu-id="67cd5-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="67cd5-112">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-113">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="67cd5-113">Select STD.</span></span> <span data-ttu-id="67cd5-114">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="67cd5-115">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-116">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="67cd5-116">For example, select Audio.</span></span> <span data-ttu-id="67cd5-117">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="67cd5-118">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-119">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="67cd5-119">Select SiteWH.</span></span> <span data-ttu-id="67cd5-120">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="67cd5-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="67cd5-121">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-122">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="67cd5-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="67cd5-123">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="67cd5-123">Select None.</span></span>  
8. <span data-ttu-id="67cd5-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="67cd5-124">Click OK.</span></span>
9. <span data-ttu-id="67cd5-125">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="67cd5-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="67cd5-126">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="67cd5-126">Click Default order settings.</span></span>
11. <span data-ttu-id="67cd5-127">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-128">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="67cd5-129">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-130">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="67cd5-131">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-132">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="67cd5-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-133">Close the page.</span></span>
15. <span data-ttu-id="67cd5-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-134">Close the page.</span></span>
16. <span data-ttu-id="67cd5-135">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="67cd5-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="67cd5-136">คลิก ITEM_A</span><span class="sxs-lookup"><span data-stu-id="67cd5-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="67cd5-137">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="67cd5-138">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="67cd5-139">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="67cd5-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="67cd5-140">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="67cd5-141">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-141">Click Item price.</span></span>
21. <span data-ttu-id="67cd5-142">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="67cd5-142">Click New.</span></span>
22. <span data-ttu-id="67cd5-143">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-144">สำหรับตัวอย่างนี้ ให้เลือก 10 ซึ่งเป็นชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="67cd5-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="67cd5-145">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-146">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="67cd5-147">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="67cd5-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="67cd5-148">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="67cd5-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="67cd5-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="67cd5-149">Click Save.</span></span>
26. <span data-ttu-id="67cd5-150">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="67cd5-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="67cd5-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-151">Close the page.</span></span>
28. <span data-ttu-id="67cd5-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="67cd5-153">สร้างวัตถุดิบที่สอง</span><span class="sxs-lookup"><span data-stu-id="67cd5-153">Create the second material</span></span>
1. <span data-ttu-id="67cd5-154">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="67cd5-154">Click New.</span></span>
2. <span data-ttu-id="67cd5-155">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="67cd5-156">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_B</span><span class="sxs-lookup"><span data-stu-id="67cd5-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="67cd5-157">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-158">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="67cd5-158">Select STD.</span></span> <span data-ttu-id="67cd5-159">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="67cd5-160">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-161">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="67cd5-161">For example, select Audio.</span></span> <span data-ttu-id="67cd5-162">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="67cd5-163">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-164">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="67cd5-164">Select SiteWH.</span></span> <span data-ttu-id="67cd5-165">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="67cd5-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="67cd5-166">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-167">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="67cd5-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="67cd5-168">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="67cd5-168">Select None.</span></span>  
7. <span data-ttu-id="67cd5-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="67cd5-169">Click OK.</span></span>
8. <span data-ttu-id="67cd5-170">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="67cd5-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="67cd5-171">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="67cd5-171">Click Default order settings.</span></span>
10. <span data-ttu-id="67cd5-172">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-173">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="67cd5-174">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-175">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="67cd5-176">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-177">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="67cd5-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-178">Close the page.</span></span>
14. <span data-ttu-id="67cd5-179">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-179">Close the page.</span></span>
15. <span data-ttu-id="67cd5-180">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="67cd5-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="67cd5-181">คลิก ITEM_B</span><span class="sxs-lookup"><span data-stu-id="67cd5-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="67cd5-182">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="67cd5-183">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="67cd5-184">สำหรับตัวอย่างนี้ ให้พิมพ์ M2</span><span class="sxs-lookup"><span data-stu-id="67cd5-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="67cd5-185">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="67cd5-186">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-186">Click Item price.</span></span>
20. <span data-ttu-id="67cd5-187">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="67cd5-187">Click New.</span></span>
21. <span data-ttu-id="67cd5-188">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-189">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="67cd5-189">For this example, select 10.</span></span> <span data-ttu-id="67cd5-190">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="67cd5-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="67cd5-191">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-192">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="67cd5-193">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="67cd5-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="67cd5-194">สำหรับการสาธิต ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="67cd5-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="67cd5-195">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="67cd5-195">Click Save.</span></span>
25. <span data-ttu-id="67cd5-196">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="67cd5-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="67cd5-197">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-197">Close the page.</span></span>
27. <span data-ttu-id="67cd5-198">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="67cd5-199">สร้างวัตถุดิบที่สาม</span><span class="sxs-lookup"><span data-stu-id="67cd5-199">Create the third material</span></span>
1. <span data-ttu-id="67cd5-200">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="67cd5-200">Click New.</span></span>
2. <span data-ttu-id="67cd5-201">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="67cd5-202">สำหรับการสาธิต ให้พิมพ์ ITEM_C</span><span class="sxs-lookup"><span data-stu-id="67cd5-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="67cd5-203">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-204">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="67cd5-204">Select STD.</span></span> <span data-ttu-id="67cd5-205">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="67cd5-206">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-207">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="67cd5-207">For example, select Audio.</span></span> <span data-ttu-id="67cd5-208">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="67cd5-209">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-210">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="67cd5-210">Select SiteWH.</span></span> <span data-ttu-id="67cd5-211">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับการสาธิต</span><span class="sxs-lookup"><span data-stu-id="67cd5-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="67cd5-212">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-213">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="67cd5-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="67cd5-214">เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="67cd5-214">Select None.</span></span>  
7. <span data-ttu-id="67cd5-215">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="67cd5-215">Click OK.</span></span>
8. <span data-ttu-id="67cd5-216">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="67cd5-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="67cd5-217">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="67cd5-217">Click Default order settings.</span></span>
10. <span data-ttu-id="67cd5-218">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-219">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="67cd5-220">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-221">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="67cd5-222">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67cd5-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-223">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="67cd5-224">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-224">Close the page.</span></span>
14. <span data-ttu-id="67cd5-225">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-225">Close the page.</span></span>
15. <span data-ttu-id="67cd5-226">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="67cd5-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="67cd5-227">คลิก ITEM_C</span><span class="sxs-lookup"><span data-stu-id="67cd5-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="67cd5-228">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="67cd5-229">ในฟิลด์กลุ่มต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="67cd5-230">สำหรับตัวอย่างนี้ ให้พิมพ์ M1</span><span class="sxs-lookup"><span data-stu-id="67cd5-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="67cd5-231">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="67cd5-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="67cd5-232">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-232">Click Item price.</span></span>
20. <span data-ttu-id="67cd5-233">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="67cd5-233">Click New.</span></span>
21. <span data-ttu-id="67cd5-234">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-235">สำหรับตัวอย่างนี้ ให้เลือก 10</span><span class="sxs-lookup"><span data-stu-id="67cd5-235">For this example, select 10.</span></span> <span data-ttu-id="67cd5-236">นี่คือชนิดการคิดต้นทุนของต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="67cd5-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="67cd5-237">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="67cd5-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="67cd5-238">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="67cd5-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="67cd5-239">ในฟิลด์ราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="67cd5-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="67cd5-240">สำหรับตัวอย่างนี้ ให้พิมพ์ 10</span><span class="sxs-lookup"><span data-stu-id="67cd5-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="67cd5-241">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="67cd5-241">Click Save.</span></span>
25. <span data-ttu-id="67cd5-242">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="67cd5-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="67cd5-243">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-243">Close the page.</span></span>
27. <span data-ttu-id="67cd5-244">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67cd5-244">Close the page.</span></span>

