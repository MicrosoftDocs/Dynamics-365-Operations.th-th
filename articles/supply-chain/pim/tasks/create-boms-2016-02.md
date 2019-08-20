---
title: สร้าง BOM (กุมภาพันธ์ 2016)
description: งานนี้มุ่งเน้นการสร้างโครงสร้างสูตรการผลิตสำหรับผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0087c53d9cdc3bb65e6fa446c193c752d0f9b4fc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845100"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="f6cc1-103">สร้าง BOM (กุมภาพันธ์ 2016)</span><span class="sxs-lookup"><span data-stu-id="f6cc1-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6cc1-104">งานนี้มุ่งเน้นการสร้างโครงสร้างสูตรการผลิตสำหรับผลิตภัณฑ์สำเร็จรูปและผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="f6cc1-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="f6cc1-105">นี่คืองานที่สี่ในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="f6cc1-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="f6cc1-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="f6cc1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="f6cc1-107">สร้าง BOM สำหรับผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="f6cc1-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="f6cc1-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="f6cc1-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f6cc1-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f6cc1-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f6cc1-110">เลือกหมายเลขสินค้า BOM_2</span><span class="sxs-lookup"><span data-stu-id="f6cc1-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="f6cc1-111">ในบานหน้าต่างการดำเนินการ คลิกวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="f6cc1-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="f6cc1-112">คลิกเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="f6cc1-112">Click BOM versions.</span></span>
5. <span data-ttu-id="f6cc1-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-113">Click New.</span></span>
6. <span data-ttu-id="f6cc1-114">คลิก BOM และเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="f6cc1-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="f6cc1-115">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f6cc1-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f6cc1-116">ตัวอย่างเช่น พิมพ์ BOM_2</span><span class="sxs-lookup"><span data-stu-id="f6cc1-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="f6cc1-117">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f6cc1-118">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก Site 1</span><span class="sxs-lookup"><span data-stu-id="f6cc1-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="f6cc1-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-119">Click OK.</span></span>
10. <span data-ttu-id="f6cc1-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-120">Click New.</span></span>
11. <span data-ttu-id="f6cc1-121">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6cc1-122">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_C</span><span class="sxs-lookup"><span data-stu-id="f6cc1-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="f6cc1-123">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6cc1-124">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก 11</span><span class="sxs-lookup"><span data-stu-id="f6cc1-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="f6cc1-125">คลิกหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="f6cc1-125">Click Header.</span></span>
14. <span data-ttu-id="f6cc1-126">คลิกการอนุมัติเพื่ออนุมัติสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="f6cc1-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="f6cc1-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-127">Click OK.</span></span>
16. <span data-ttu-id="f6cc1-128">คลิกอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f6cc1-128">Click Approve.</span></span>
    * <span data-ttu-id="f6cc1-129">ปุ่ม อนุมัติ อยู่บนแถบเครื่องมือในส่วนเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="f6cc1-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="f6cc1-130">ถ้ามองไม่เห็น ให้คลิก ส่วนหัว ที่ด้านขวาบนของหน้าสูตรการผลิตเพื่อแสดง อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f6cc1-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="f6cc1-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-131">Click OK.</span></span>
18. <span data-ttu-id="f6cc1-132">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="f6cc1-132">Click Activate.</span></span>
19. <span data-ttu-id="f6cc1-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-133">Close the page.</span></span>
20. <span data-ttu-id="f6cc1-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-134">Close the page.</span></span>
21. <span data-ttu-id="f6cc1-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="f6cc1-136">สร้าง BOM สำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="f6cc1-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="f6cc1-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f6cc1-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f6cc1-138">เลือกหมายเลขสินค้า BOM_1</span><span class="sxs-lookup"><span data-stu-id="f6cc1-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="f6cc1-139">ในบานหน้าต่างการดำเนินการ คลิกวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="f6cc1-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="f6cc1-140">คลิกเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="f6cc1-140">Click BOM versions.</span></span>
4. <span data-ttu-id="f6cc1-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-141">Click New.</span></span>
5. <span data-ttu-id="f6cc1-142">คลิก BOM และเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="f6cc1-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="f6cc1-143">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f6cc1-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f6cc1-144">ตัวอย่างเช่น พิมพ์ BOM_1</span><span class="sxs-lookup"><span data-stu-id="f6cc1-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="f6cc1-145">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f6cc1-146">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก Site 1</span><span class="sxs-lookup"><span data-stu-id="f6cc1-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="f6cc1-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-147">Click OK.</span></span>
9. <span data-ttu-id="f6cc1-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-148">Click New.</span></span>
10. <span data-ttu-id="f6cc1-149">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6cc1-150">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_A</span><span class="sxs-lookup"><span data-stu-id="f6cc1-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="f6cc1-151">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6cc1-152">สำหรับตัวอย่างนี้ ให้เลือก 11</span><span class="sxs-lookup"><span data-stu-id="f6cc1-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="f6cc1-153">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-153">Click New.</span></span>
13. <span data-ttu-id="f6cc1-154">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6cc1-155">สำหรับตัวอย่างนี้ ให้พิมพ์ ITEM_B</span><span class="sxs-lookup"><span data-stu-id="f6cc1-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="f6cc1-156">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6cc1-157">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก 11</span><span class="sxs-lookup"><span data-stu-id="f6cc1-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="f6cc1-158">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-158">Click New.</span></span>
16. <span data-ttu-id="f6cc1-159">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6cc1-160">สำหรับตัวอย่างนี้ ให้พิมพ์ BOM_2</span><span class="sxs-lookup"><span data-stu-id="f6cc1-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="f6cc1-161">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f6cc1-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="f6cc1-162">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6cc1-163">สำหรับตัวอย่างนี้ ให้ป้อนหรือเลือก คลังสินค้า 11</span><span class="sxs-lookup"><span data-stu-id="f6cc1-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="f6cc1-164">คลิกหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="f6cc1-164">Click Header.</span></span>
20. <span data-ttu-id="f6cc1-165">คลิกการอนุมัติเพื่ออนุมัติสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="f6cc1-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="f6cc1-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-166">Click OK.</span></span>
22. <span data-ttu-id="f6cc1-167">คลิกอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f6cc1-167">Click Approve.</span></span>
    * <span data-ttu-id="f6cc1-168">ปุ่ม อนุมัติ อยู่บนแถบเครื่องมือในส่วนเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="f6cc1-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="f6cc1-169">ถ้ามองไม่เห็น ให้คลิก ส่วนหัว ที่ด้านขวาบนของหน้าสูตรการผลิตเพื่อแสดง อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f6cc1-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="f6cc1-170">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f6cc1-170">Click OK.</span></span>
24. <span data-ttu-id="f6cc1-171">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="f6cc1-171">Click Activate.</span></span>
25. <span data-ttu-id="f6cc1-172">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-172">Close the page.</span></span>
26. <span data-ttu-id="f6cc1-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-173">Close the page.</span></span>
27. <span data-ttu-id="f6cc1-174">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f6cc1-174">Close the page.</span></span>

