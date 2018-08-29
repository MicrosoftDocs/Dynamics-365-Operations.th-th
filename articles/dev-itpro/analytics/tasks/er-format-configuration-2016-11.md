--- 
title: "สร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="d8149-103">สร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="d8149-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8149-104">ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="d8149-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="d8149-105">การตั้งค่าคอนฟิกรูปแบบนี้จะใช้กำหนดรูปแบบของเอกสารทางอิเล็กทรอนิกส์ที่ถูกใช้สำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="d8149-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="d8149-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ คุณต้องทำขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "แม็ปแบบจำลองไปยังแหล่งข้อมูลที่เลือก" ก่อน </span><span class="sxs-lookup"><span data-stu-id="d8149-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="d8149-107">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="d8149-107">Create a new format configuration</span></span>
1. <span data-ttu-id="d8149-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d8149-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d8149-109">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="d8149-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d8149-110">ในแผนภูมิ เลือก 'การชำระเงิน(แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="d8149-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="d8149-111">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8149-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="d8149-112">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามข้อมูลแบบจำลอง แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="d8149-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="d8149-113">ในฟิลด์ชื่อ พิมพ์ 'BACS (UK fictitious)'</span><span class="sxs-lookup"><span data-stu-id="d8149-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="d8149-114">BACS (แบบสมมติของ UK)</span><span class="sxs-lookup"><span data-stu-id="d8149-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="d8149-115">ในฟิลด์คำอธิบาย พิมพ์ 'รูปแบบการชำระเงินของผู้จัดจำหน่าย BACS (UK fictitious)'</span><span class="sxs-lookup"><span data-stu-id="d8149-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="d8149-116">รูปแบบการชำระเงินของผู้จัดจำหน่าย BACS (UK fictitious)</span><span class="sxs-lookup"><span data-stu-id="d8149-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="d8149-117">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d8149-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="d8149-118">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="d8149-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="d8149-119">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="d8149-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="d8149-120">รูปแบบเฉพาะของเอกสารทางอิเล็กทรอนิกส์สามารถถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="d8149-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="d8149-121">ปล่อยฟิลด์นี้ว่างเปล่า ถ้าคุณต้องการเลือกรูปแบบที่ตรงกับเวลาที่ใช้ในการผลิต</span><span class="sxs-lookup"><span data-stu-id="d8149-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="d8149-122">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d8149-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="d8149-123">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="d8149-123">Click Create configuration.</span></span>
    * <span data-ttu-id="d8149-124">การตั้งค่าคอนฟิกใหม่ถูกสร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="d8149-124">A new configuration has been created.</span></span> <span data-ttu-id="d8149-125">รุ่นแบบร่างสามารถใช้เพื่อจัดเก็บรูปแบบการออกแบบสำหรับเอกสารการจัดการทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d8149-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="d8149-126">รูปแบบการออกแบบของเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d8149-126">Design format of electronic document</span></span>
1. <span data-ttu-id="d8149-127">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="d8149-127">Click Designer.</span></span>
2. <span data-ttu-id="d8149-128">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8149-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="d8149-129">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="d8149-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="d8149-130">ในฟิลด์ชื่อ พิมพ์ 'Xml'</span><span class="sxs-lookup"><span data-stu-id="d8149-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="d8149-131">Xml</span><span class="sxs-lookup"><span data-stu-id="d8149-131">Xml</span></span>  
5. <span data-ttu-id="d8149-132">ในฟิลด์การเข้ารหัส พิมพ์ 'UTF-8'</span><span class="sxs-lookup"><span data-stu-id="d8149-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="d8149-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="d8149-133">UTF-8</span></span>  
6. <span data-ttu-id="d8149-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-134">Click OK.</span></span>
7. <span data-ttu-id="d8149-135">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8149-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="d8149-136">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="d8149-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="d8149-137">ในฟิลด์ชือ พิมพ์ 'ข้อความ'</span><span class="sxs-lookup"><span data-stu-id="d8149-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="d8149-138">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="d8149-138">Message</span></span>  
10. <span data-ttu-id="d8149-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-139">Click OK.</span></span>
11. <span data-ttu-id="d8149-140">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ'</span><span class="sxs-lookup"><span data-stu-id="d8149-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="d8149-141">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-141">Click Add Element.</span></span>
13. <span data-ttu-id="d8149-142">ในฟิลด์ชื่อ พิมพ์ 'วันที่ที่ประมวลผล'</span><span class="sxs-lookup"><span data-stu-id="d8149-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="d8149-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="d8149-143">ProcessingDate</span></span>  
14. <span data-ttu-id="d8149-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-144">Click OK.</span></span>
15. <span data-ttu-id="d8149-145">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-145">Click Add Element.</span></span>
16. <span data-ttu-id="d8149-146">ในฟิลด์ชือ พิมพ์ 'รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="d8149-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="d8149-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="d8149-147">MessageId</span></span>  
17. <span data-ttu-id="d8149-148">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-148">Click OK.</span></span>
18. <span data-ttu-id="d8149-149">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-149">Click Add Element.</span></span>
19. <span data-ttu-id="d8149-150">ในฟิลด์ชื่อ ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="d8149-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="d8149-151">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="d8149-151">Payments</span></span>  
20. <span data-ttu-id="d8149-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-152">Click OK.</span></span>
21. <span data-ttu-id="d8149-153">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="d8149-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="d8149-154">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-154">Click Add Element.</span></span>
23. <span data-ttu-id="d8149-155">ในฟิลด์ชื่อ พิมพ์ 'สินค้า'</span><span class="sxs-lookup"><span data-stu-id="d8149-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="d8149-156">สินค้า</span><span class="sxs-lookup"><span data-stu-id="d8149-156">Item</span></span>  
24. <span data-ttu-id="d8149-157">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-157">Click OK.</span></span>
25. <span data-ttu-id="d8149-158">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ'</span><span class="sxs-lookup"><span data-stu-id="d8149-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="d8149-159">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8149-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="d8149-160">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="d8149-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="d8149-161">ในฟิลด์ชื่อ พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="d8149-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="d8149-162">รหัส</span><span class="sxs-lookup"><span data-stu-id="d8149-162">Id</span></span>  
29. <span data-ttu-id="d8149-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-163">Click OK.</span></span>
30. <span data-ttu-id="d8149-164">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8149-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="d8149-165">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="d8149-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="d8149-166">ในฟิลด์ชื่อ พิมพ์ 'ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="d8149-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="d8149-167">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="d8149-167">Vendor</span></span>  
33. <span data-ttu-id="d8149-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-168">Click OK.</span></span>
34. <span data-ttu-id="d8149-169">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="d8149-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="d8149-170">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-170">Click Add Element.</span></span>
36. <span data-ttu-id="d8149-171">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="d8149-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="d8149-172">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="d8149-172">Name</span></span>  
37. <span data-ttu-id="d8149-173">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-173">Click OK.</span></span>
38. <span data-ttu-id="d8149-174">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-174">Click Add Element.</span></span>
39. <span data-ttu-id="d8149-175">ในฟิลด์ชื่อ พิมพ์ 'ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="d8149-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="d8149-176">ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="d8149-176">Bank</span></span>  
40. <span data-ttu-id="d8149-177">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-177">Click OK.</span></span>
41. <span data-ttu-id="d8149-178">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="d8149-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="d8149-179">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-179">Click Add Element.</span></span>
43. <span data-ttu-id="d8149-180">ในฟิลด์ชื่อ พิมพ์ 'หมายเลขการกำหนดเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="d8149-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="d8149-181">หมายเลขการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="d8149-181">RoutingNumber</span></span>  
44. <span data-ttu-id="d8149-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-182">Click OK.</span></span>
45. <span data-ttu-id="d8149-183">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-183">Click Add Element.</span></span>
46. <span data-ttu-id="d8149-184">ในฟิลด์ชื่อ พิมพ์ 'หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="d8149-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="d8149-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="d8149-185">AccountNumber</span></span>  
47. <span data-ttu-id="d8149-186">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-186">Click OK.</span></span>
48. <span data-ttu-id="d8149-187">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="d8149-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="d8149-188">คลิก คัดลอก</span><span class="sxs-lookup"><span data-stu-id="d8149-188">Click Copy.</span></span>
50. <span data-ttu-id="d8149-189">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ'</span><span class="sxs-lookup"><span data-stu-id="d8149-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="d8149-190">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="d8149-190">Click Paste.</span></span>
52. <span data-ttu-id="d8149-191">ในฟิลด์ชื่อ พิมพ์ 'ผู้ชำระ'</span><span class="sxs-lookup"><span data-stu-id="d8149-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="d8149-192">ผู้จ่ายเงิน</span><span class="sxs-lookup"><span data-stu-id="d8149-192">Payer</span></span>  
53. <span data-ttu-id="d8149-193">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ'</span><span class="sxs-lookup"><span data-stu-id="d8149-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="d8149-194">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-194">Click Add Element.</span></span>
55. <span data-ttu-id="d8149-195">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="d8149-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="d8149-196">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="d8149-196">Currency</span></span>  
56. <span data-ttu-id="d8149-197">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-197">Click OK.</span></span>
57. <span data-ttu-id="d8149-198">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-198">Click Add Element.</span></span>
58. <span data-ttu-id="d8149-199">ในฟิลด์ชื่อ ให้พิมพ์ 'คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="d8149-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="d8149-200">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d8149-200">Description</span></span>  
59. <span data-ttu-id="d8149-201">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-201">Click OK.</span></span>
60. <span data-ttu-id="d8149-202">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-202">Click Add Element.</span></span>
61. <span data-ttu-id="d8149-203">ในฟิลด์ชื่อ พิมพ์ 'วันที่ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="d8149-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="d8149-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="d8149-204">TransDate</span></span>  
62. <span data-ttu-id="d8149-205">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-205">Click OK.</span></span>
63. <span data-ttu-id="d8149-206">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="d8149-206">Click Add Element.</span></span>
64. <span data-ttu-id="d8149-207">ในฟิลด์ชื่อ พิมพ์ 'จำนวน'</span><span class="sxs-lookup"><span data-stu-id="d8149-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="d8149-208">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="d8149-208">Amount</span></span>  
65. <span data-ttu-id="d8149-209">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="d8149-210">จัดเตรียมส่วนประกอบรูปแบบสำหรับการแม็ปไปยังองค์ประกอบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d8149-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="d8149-211">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\วันที่ประมวลผล'</span><span class="sxs-lookup"><span data-stu-id="d8149-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="d8149-212">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8149-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="d8149-213">ในแผนภูมิ ให้เลือก 'ข้อความอักษร\วันที่และเวลา'</span><span class="sxs-lookup"><span data-stu-id="d8149-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="d8149-214">ในฟิลด์รูปแบบ พิมพ์ 'yyyy-MM-dd'</span><span class="sxs-lookup"><span data-stu-id="d8149-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="d8149-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="d8149-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="d8149-216">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-216">Click OK.</span></span>
6. <span data-ttu-id="d8149-217">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="d8149-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="d8149-218">คลิก เพิ่มวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d8149-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="d8149-219">ในฟิลด์รูปแบบ พิมพ์ 'yyyy-MM-dd'</span><span class="sxs-lookup"><span data-stu-id="d8149-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="d8149-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="d8149-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="d8149-221">ในฟิลด์ชนิดวันที่และเวลา ให้เลือก 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="d8149-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="d8149-222">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-222">Click OK.</span></span>
11. <span data-ttu-id="d8149-223">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="d8149-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="d8149-224">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8149-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="d8149-225">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="d8149-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="d8149-226">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="d8149-226">Click OK.</span></span>
15. <span data-ttu-id="d8149-227">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="d8149-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="d8149-228">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-228">Click Add String.</span></span>
17. <span data-ttu-id="d8149-229">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-229">Click OK.</span></span>
18. <span data-ttu-id="d8149-230">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="d8149-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="d8149-231">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-231">Click Add String.</span></span>
20. <span data-ttu-id="d8149-232">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-232">Click OK.</span></span>
21. <span data-ttu-id="d8149-233">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="d8149-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="d8149-234">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-234">Click Add String.</span></span>
23. <span data-ttu-id="d8149-235">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-235">Click OK.</span></span>
24. <span data-ttu-id="d8149-236">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="d8149-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="d8149-237">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-237">Click Add String.</span></span>
26. <span data-ttu-id="d8149-238">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-238">Click OK.</span></span>
27. <span data-ttu-id="d8149-239">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="d8149-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="d8149-240">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-240">Click Add String.</span></span>
29. <span data-ttu-id="d8149-241">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-241">Click OK.</span></span>
30. <span data-ttu-id="d8149-242">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="d8149-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="d8149-243">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-243">Click Add String.</span></span>
32. <span data-ttu-id="d8149-244">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-244">Click OK.</span></span>
33. <span data-ttu-id="d8149-245">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="d8149-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="d8149-246">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-246">Click Add String.</span></span>
35. <span data-ttu-id="d8149-247">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-247">Click OK.</span></span>
36. <span data-ttu-id="d8149-248">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="d8149-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="d8149-249">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-249">Click Add String.</span></span>
38. <span data-ttu-id="d8149-250">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-250">Click OK.</span></span>
39. <span data-ttu-id="d8149-251">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\จำนวนเงิน'</span><span class="sxs-lookup"><span data-stu-id="d8149-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="d8149-252">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="d8149-252">Click Add String.</span></span>
41. <span data-ttu-id="d8149-253">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8149-253">Click OK.</span></span>
42. <span data-ttu-id="d8149-254">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d8149-254">Click Save.</span></span>
43. <span data-ttu-id="d8149-255">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d8149-255">Close the page.</span></span>


