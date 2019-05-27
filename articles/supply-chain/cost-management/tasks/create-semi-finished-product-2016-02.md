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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563192"
---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="75904-103">สร้างผลิตภัณฑ์กึ่งสำเร็จรูป (กุมภาพันธ์ 2016 เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="75904-103">Create a semi-finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75904-104">งานนี้มุ่งเน้นการสร้างผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="75904-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="75904-105">นี่คืองานที่สองในลำดับการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="75904-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="75904-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="75904-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="75904-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="75904-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="75904-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="75904-108">Click New.</span></span>
3. <span data-ttu-id="75904-109">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="75904-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="75904-110">สำหรับตัวอย่างนี้ ให้พิมพ์ BOM_2</span><span class="sxs-lookup"><span data-stu-id="75904-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="75904-111">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="75904-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-112">เลือก STD</span><span class="sxs-lookup"><span data-stu-id="75904-112">Select STD.</span></span> <span data-ttu-id="75904-113">STD ย่อมาจาก ต้นทุนมาตรฐาน และเป็นแบบจำลองที่ถูกนำมาใช้มากที่สุดเมื่อทำงานกับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="75904-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="75904-114">ในฟิลด์กลุ่มสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="75904-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-115">ตัวอย่างเช่น เลือก เสียง</span><span class="sxs-lookup"><span data-stu-id="75904-115">For example, select Audio.</span></span> <span data-ttu-id="75904-116">ซึ่งไม่มีผลกระทบต่อการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="75904-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="75904-117">ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="75904-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-118">เลือก SiteWH</span><span class="sxs-lookup"><span data-stu-id="75904-118">Select SiteWH.</span></span> <span data-ttu-id="75904-119">เฉพาะไซต์และคลังสินค้าที่จะถูกใช้สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="75904-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="75904-120">ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="75904-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-121">จะไม่ใช้มิติการติดตามสำหรับตัวอย่างนี้ เลือก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="75904-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="75904-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="75904-122">Click OK.</span></span>
9. <span data-ttu-id="75904-123">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="75904-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="75904-124">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="75904-124">Click Default order settings.</span></span>
11. <span data-ttu-id="75904-125">ในฟิลด์ชนิดใบสั่งเริ่มต้น ให้เลือก 'การผลิต'</span><span class="sxs-lookup"><span data-stu-id="75904-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="75904-126">เนื่องจากเป็นผลิตภัณฑ์กึ่งสำเร็จรูปที่จะผลิต เลือก การผลิต</span><span class="sxs-lookup"><span data-stu-id="75904-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="75904-127">ในฟิลด์ ไซต์การซื้อ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="75904-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-128">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="75904-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="75904-129">ในฟิลด์ ไซต์สินค้าคงคลัง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="75904-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-130">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="75904-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="75904-131">ในฟิลด์ ไซต์การขาย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="75904-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-132">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="75904-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="75904-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="75904-133">Close the page.</span></span>
16. <span data-ttu-id="75904-134">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="75904-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="75904-135">คลิก ราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="75904-135">Click Item price.</span></span>
18. <span data-ttu-id="75904-136">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="75904-136">Click New.</span></span>
19. <span data-ttu-id="75904-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="75904-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="75904-138">ในฟิลด์เวอร์ชัน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="75904-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-139">สำหรับตัวอย่างนี้ ให้เลือก เวอร์ชัน 10</span><span class="sxs-lookup"><span data-stu-id="75904-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="75904-140">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="75904-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-141">สำหรับตัวอย่างนี้ ให้เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="75904-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="75904-142">กำหนดราคาเป็น '10'</span><span class="sxs-lookup"><span data-stu-id="75904-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="75904-143">สำหรับตัวอย่านี้ ให้พิมพ์ราคาต้นทุนเป็น 10</span><span class="sxs-lookup"><span data-stu-id="75904-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="75904-144">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="75904-144">Click Save.</span></span>
24. <span data-ttu-id="75904-145">คลิก เปิดใช้งานราคาที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="75904-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="75904-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="75904-146">Close the page.</span></span>
26. <span data-ttu-id="75904-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="75904-147">Close the page.</span></span>
27. <span data-ttu-id="75904-148">คลิก BOM_2 เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="75904-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="75904-149">ขยายส่วน จัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="75904-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="75904-150">ในฟิลด์กลุ่มต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="75904-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="75904-151">สำหรับตัวอย่างนี้ ให้เลือก กลุ่มต้นทุน M1</span><span class="sxs-lookup"><span data-stu-id="75904-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="75904-152">ใช้ทางลัดนี้สำหรับการบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="75904-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="75904-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="75904-153">Close the page.</span></span>

