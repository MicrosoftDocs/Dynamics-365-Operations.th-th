---
title: สร้างผลิตภัณฑ์กึ่งสำเร็จรูป (กุมภาพันธ์ 2016 เท่านั้น)
description: งานนี้มุ่งเน้นการสร้างผลิตภัณฑ์กึ่งสำเร็จรูป
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76fcba3732879f85c9bf0faa6d2481b9c5313a17
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "358956"
---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="addbb-103">สร้างผลิตภัณฑ์กึ่งสำเร็จรูป (กุมภาพันธ์ 2016 เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="addbb-103">Create a semi-finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="addbb-104">งานนี้มุ่งเน้นการสร้างผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="addbb-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="addbb-105">นี่คืองานที่สองในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="addbb-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="addbb-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="addbb-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="addbb-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="addbb-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="addbb-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="addbb-108">Click New.</span></span>
3. <span data-ttu-id="addbb-109">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="addbb-110">สำหรับตัวอย่างนี้ ให้พิมพ์ BOM_2</span><span class="sxs-lookup"><span data-stu-id="addbb-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="addbb-111">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-112">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="addbb-112">Select STD.</span></span> <span data-ttu-id="addbb-113">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="addbb-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="addbb-114">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="addbb-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-115">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="addbb-115">For example, select Audio.</span></span> <span data-ttu-id="addbb-116">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="addbb-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="addbb-117">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-118">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="addbb-118">Select SiteWH.</span></span> <span data-ttu-id="addbb-119">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="addbb-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="addbb-120">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-121">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้ เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="addbb-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="addbb-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="addbb-122">Click OK.</span></span>
9. <span data-ttu-id="addbb-123">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="addbb-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="addbb-124">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="addbb-124">Click Default order settings.</span></span>
11. <span data-ttu-id="addbb-125">ในฟิลด์ชนิดใบสั่งเริ่มต้น ให้เลือก 'การผลิต'</span><span class="sxs-lookup"><span data-stu-id="addbb-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="addbb-126">เนื่องจากเป็นผลิตภัณฑ์กึ่งสำเร็จรูปที่จะผลิต เลือก การผลิต</span><span class="sxs-lookup"><span data-stu-id="addbb-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="addbb-127">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-128">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="addbb-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="addbb-129">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-130">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="addbb-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="addbb-131">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-132">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="addbb-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="addbb-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="addbb-133">Close the page.</span></span>
16. <span data-ttu-id="addbb-134">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="addbb-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="addbb-135">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="addbb-135">Click Item price.</span></span>
18. <span data-ttu-id="addbb-136">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="addbb-136">Click New.</span></span>
19. <span data-ttu-id="addbb-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="addbb-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="addbb-138">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="addbb-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-139">สำหรับตัวอย่างนี้ ให้เลือก เวอร์ชัน 10</span><span class="sxs-lookup"><span data-stu-id="addbb-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="addbb-140">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="addbb-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-141">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="addbb-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="addbb-142">กำหนดราคาเป็น '10'</span><span class="sxs-lookup"><span data-stu-id="addbb-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="addbb-143">สำหรับตัวอย่านี้ ให้พิมพ์ราคาต้นทุนเป็น 10</span><span class="sxs-lookup"><span data-stu-id="addbb-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="addbb-144">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="addbb-144">Click Save.</span></span>
24. <span data-ttu-id="addbb-145">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="addbb-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="addbb-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="addbb-146">Close the page.</span></span>
26. <span data-ttu-id="addbb-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="addbb-147">Close the page.</span></span>
27. <span data-ttu-id="addbb-148">คลิก BOM_2 เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="addbb-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="addbb-149">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="addbb-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="addbb-150">ในฟิลด์กลุ่มต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="addbb-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="addbb-151">สำหรับตัวอย่างนี้ ให้เลือก กลุ่มต้นทุน M1</span><span class="sxs-lookup"><span data-stu-id="addbb-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="addbb-152">ใช้ทางลัดนี้สำหรับการบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="addbb-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="addbb-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="addbb-153">Close the page.</span></span>

