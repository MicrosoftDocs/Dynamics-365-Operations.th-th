--- 
title: "สร้าง BOM (กุมภาพันธ์ 2016 เท่านั้น)"
description: "งานนี้มุ่งเน้นการสร้างโครงสร้างสูตรการผลิตสำหรับผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป"
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
ms.openlocfilehash: f8ad4b0e230fb0f018355e486e3b898895a61f28
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="d07c6-103">สร้าง BOM (กุมภาพันธ์ 2016 เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="d07c6-103">Create BOMs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d07c6-104">งานนี้มุ่งเน้นการสร้างโครงสร้างสูตรการผลิตสำหรับผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="d07c6-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="d07c6-105">นี่คืองานที่สี่ในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="d07c6-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="d07c6-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="d07c6-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="d07c6-107">สร้าง BOM สำหรับผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="d07c6-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="d07c6-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="d07c6-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="d07c6-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d07c6-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d07c6-110">เลือกหมายเลขสินค้า BOM_2</span><span class="sxs-lookup"><span data-stu-id="d07c6-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="d07c6-111">ในบานหน้าต่างการดำเนินการ คลิกวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="d07c6-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="d07c6-112">คลิกเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="d07c6-112">Click BOM versions.</span></span>
5. <span data-ttu-id="d07c6-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d07c6-113">Click New.</span></span>
6. <span data-ttu-id="d07c6-114">คลิก BOM และเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="d07c6-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="d07c6-115">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d07c6-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d07c6-116">ตัวอย่างเช่น พิมพ์ BOM_2</span><span class="sxs-lookup"><span data-stu-id="d07c6-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="d07c6-117">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d07c6-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="d07c6-118">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก Site 1</span><span class="sxs-lookup"><span data-stu-id="d07c6-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="d07c6-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d07c6-119">Click OK.</span></span>
10. <span data-ttu-id="d07c6-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d07c6-120">Click New.</span></span>
11. <span data-ttu-id="d07c6-121">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d07c6-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d07c6-122">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_C</span><span class="sxs-lookup"><span data-stu-id="d07c6-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="d07c6-123">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d07c6-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d07c6-124">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก 11</span><span class="sxs-lookup"><span data-stu-id="d07c6-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="d07c6-125">คลิกหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="d07c6-125">Click Header.</span></span>
14. <span data-ttu-id="d07c6-126">คลิกการอนุมัติเพื่ออนุมัติสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="d07c6-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="d07c6-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d07c6-127">Click OK.</span></span>
16. <span data-ttu-id="d07c6-128">คลิกอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d07c6-128">Click Approve.</span></span>
    * <span data-ttu-id="d07c6-129">ปุ่ม อนุมัติ อยู่บนแถบเครื่องมือในส่วนเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="d07c6-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="d07c6-130">ถ้ามองไม่เห็น ให้คลิก ส่วนหัว ที่ด้านขวาบนของหน้าสูตรการผลิตเพื่อแสดง อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d07c6-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="d07c6-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d07c6-131">Click OK.</span></span>
18. <span data-ttu-id="d07c6-132">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="d07c6-132">Click Activate.</span></span>
19. <span data-ttu-id="d07c6-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d07c6-133">Close the page.</span></span>
20. <span data-ttu-id="d07c6-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d07c6-134">Close the page.</span></span>
21. <span data-ttu-id="d07c6-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d07c6-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="d07c6-136">สร้าง BOM สำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="d07c6-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="d07c6-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d07c6-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d07c6-138">เลือกหมายเลขสินค้า BOM_1</span><span class="sxs-lookup"><span data-stu-id="d07c6-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="d07c6-139">ในบานหน้าต่างการดำเนินการ คลิกวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="d07c6-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="d07c6-140">คลิกเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="d07c6-140">Click BOM versions.</span></span>
4. <span data-ttu-id="d07c6-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d07c6-141">Click New.</span></span>
5. <span data-ttu-id="d07c6-142">คลิก BOM และเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="d07c6-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="d07c6-143">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d07c6-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d07c6-144">ตัวอย่างเช่น พิมพ์ BOM_1</span><span class="sxs-lookup"><span data-stu-id="d07c6-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="d07c6-145">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d07c6-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="d07c6-146">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก Site 1</span><span class="sxs-lookup"><span data-stu-id="d07c6-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="d07c6-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d07c6-147">Click OK.</span></span>
9. <span data-ttu-id="d07c6-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d07c6-148">Click New.</span></span>
10. <span data-ttu-id="d07c6-149">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d07c6-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d07c6-150">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_A</span><span class="sxs-lookup"><span data-stu-id="d07c6-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="d07c6-151">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d07c6-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d07c6-152">สำหรับตัวอย่างนี้ ให้เลือก 11</span><span class="sxs-lookup"><span data-stu-id="d07c6-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="d07c6-153">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d07c6-153">Click New.</span></span>
13. <span data-ttu-id="d07c6-154">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d07c6-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d07c6-155">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_B</span><span class="sxs-lookup"><span data-stu-id="d07c6-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="d07c6-156">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d07c6-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d07c6-157">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก 11</span><span class="sxs-lookup"><span data-stu-id="d07c6-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="d07c6-158">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d07c6-158">Click New.</span></span>
16. <span data-ttu-id="d07c6-159">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d07c6-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d07c6-160">สำหรับตัวอย่างนี้ ให้พิมพ์ BOM_2</span><span class="sxs-lookup"><span data-stu-id="d07c6-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="d07c6-161">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d07c6-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="d07c6-162">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d07c6-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d07c6-163">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก คลังสินค้า 11</span><span class="sxs-lookup"><span data-stu-id="d07c6-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="d07c6-164">คลิกหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="d07c6-164">Click Header.</span></span>
20. <span data-ttu-id="d07c6-165">คลิกการอนุมัติเพื่ออนุมัติสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="d07c6-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="d07c6-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d07c6-166">Click OK.</span></span>
22. <span data-ttu-id="d07c6-167">คลิกอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d07c6-167">Click Approve.</span></span>
    * <span data-ttu-id="d07c6-168">ปุ่ม อนุมัติ อยู่บนแถบเครื่องมือในส่วนเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="d07c6-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="d07c6-169">ถ้ามองไม่เห็น ให้คลิก ส่วนหัว ที่ด้านขวาบนของหน้าสูตรการผลิตเพื่อแสดง อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d07c6-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="d07c6-170">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d07c6-170">Click OK.</span></span>
24. <span data-ttu-id="d07c6-171">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="d07c6-171">Click Activate.</span></span>
25. <span data-ttu-id="d07c6-172">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d07c6-172">Close the page.</span></span>
26. <span data-ttu-id="d07c6-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d07c6-173">Close the page.</span></span>
27. <span data-ttu-id="d07c6-174">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d07c6-174">Close the page.</span></span>


