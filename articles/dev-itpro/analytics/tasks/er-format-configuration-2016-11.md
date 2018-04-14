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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ef33fec0162e3b379bc8fe563d37a88fa35dfc85
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="cbec9-103">สร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="cbec9-103">Create a format configuration for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbec9-104">ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="cbec9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="cbec9-105">การตั้งค่าคอนฟิกรูปแบบนี้จะใช้กำหนดรูปแบบของเอกสารทางอิเล็กทรอนิกส์ที่ถูกใช้สำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cbec9-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="cbec9-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ คุณต้องทำขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "แม็ปแบบจำลองไปยังแหล่งข้อมูลที่เลือก" ก่อน </span><span class="sxs-lookup"><span data-stu-id="cbec9-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="cbec9-107">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="cbec9-107">Create a new format configuration</span></span>
1. <span data-ttu-id="cbec9-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cbec9-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cbec9-109">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="cbec9-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="cbec9-110">ในแผนภูมิ เลือก 'การชำระเงิน(แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="cbec9-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="cbec9-111">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="cbec9-112">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามข้อมูลแบบจำลอง แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="cbec9-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="cbec9-113">ในฟิลด์ชื่อ พิมพ์ 'BACS (UK fictitious)'</span><span class="sxs-lookup"><span data-stu-id="cbec9-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="cbec9-114">BACS (แบบสมมติของ UK)</span><span class="sxs-lookup"><span data-stu-id="cbec9-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="cbec9-115">ในฟิลด์คำอธิบาย พิมพ์ 'รูปแบบการชำระเงินของผู้จัดจำหน่าย BACS (UK fictitious)'</span><span class="sxs-lookup"><span data-stu-id="cbec9-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="cbec9-116">รูปแบบการชำระเงินของผู้จัดจำหน่าย BACS (UK fictitious)</span><span class="sxs-lookup"><span data-stu-id="cbec9-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="cbec9-117">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cbec9-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="cbec9-118">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="cbec9-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="cbec9-119">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="cbec9-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="cbec9-120">รูปแบบเฉพาะของเอกสารทางอิเล็กทรอนิกส์สามารถถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="cbec9-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="cbec9-121">ปล่อยฟิลด์นี้ว่างเปล่า ถ้าคุณต้องการเลือกรูปแบบที่ตรงกับเวลาที่ใช้ในการผลิต</span><span class="sxs-lookup"><span data-stu-id="cbec9-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="cbec9-122">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="cbec9-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="cbec9-123">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="cbec9-123">Click Create configuration.</span></span>
    * <span data-ttu-id="cbec9-124">การตั้งค่าคอนฟิกใหม่ถูกสร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="cbec9-124">A new configuration has been created.</span></span> <span data-ttu-id="cbec9-125">รุ่นแบบร่างสามารถใช้เพื่อจัดเก็บรูปแบบการออกแบบสำหรับเอกสารการจัดการทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cbec9-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="cbec9-126">รูปแบบการออกแบบของเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cbec9-126">Design format of electronic document</span></span>
1. <span data-ttu-id="cbec9-127">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-127">Click Designer.</span></span>
2. <span data-ttu-id="cbec9-128">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="cbec9-129">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="cbec9-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="cbec9-130">ในฟิลด์ชื่อ พิมพ์ 'Xml'</span><span class="sxs-lookup"><span data-stu-id="cbec9-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="cbec9-131">Xml</span><span class="sxs-lookup"><span data-stu-id="cbec9-131">Xml</span></span>  
5. <span data-ttu-id="cbec9-132">ในฟิลด์การเข้ารหัส พิมพ์ 'UTF-8'</span><span class="sxs-lookup"><span data-stu-id="cbec9-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="cbec9-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="cbec9-133">UTF-8</span></span>  
6. <span data-ttu-id="cbec9-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-134">Click OK.</span></span>
7. <span data-ttu-id="cbec9-135">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="cbec9-136">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="cbec9-137">ในฟิลด์ชือ พิมพ์ 'ข้อความ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="cbec9-138">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="cbec9-138">Message</span></span>  
10. <span data-ttu-id="cbec9-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-139">Click OK.</span></span>
11. <span data-ttu-id="cbec9-140">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="cbec9-141">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-141">Click Add Element.</span></span>
13. <span data-ttu-id="cbec9-142">ในฟิลด์ชื่อ พิมพ์ 'วันที่ที่ประมวลผล'</span><span class="sxs-lookup"><span data-stu-id="cbec9-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="cbec9-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="cbec9-143">ProcessingDate</span></span>  
14. <span data-ttu-id="cbec9-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-144">Click OK.</span></span>
15. <span data-ttu-id="cbec9-145">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-145">Click Add Element.</span></span>
16. <span data-ttu-id="cbec9-146">ในฟิลด์ชือ พิมพ์ 'รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="cbec9-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="cbec9-147">MessageId</span></span>  
17. <span data-ttu-id="cbec9-148">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-148">Click OK.</span></span>
18. <span data-ttu-id="cbec9-149">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-149">Click Add Element.</span></span>
19. <span data-ttu-id="cbec9-150">ในฟิลด์ชื่อ ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="cbec9-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="cbec9-151">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cbec9-151">Payments</span></span>  
20. <span data-ttu-id="cbec9-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-152">Click OK.</span></span>
21. <span data-ttu-id="cbec9-153">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="cbec9-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="cbec9-154">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-154">Click Add Element.</span></span>
23. <span data-ttu-id="cbec9-155">ในฟิลด์ชื่อ พิมพ์ 'สินค้า'</span><span class="sxs-lookup"><span data-stu-id="cbec9-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="cbec9-156">สินค้า</span><span class="sxs-lookup"><span data-stu-id="cbec9-156">Item</span></span>  
24. <span data-ttu-id="cbec9-157">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-157">Click OK.</span></span>
25. <span data-ttu-id="cbec9-158">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="cbec9-159">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="cbec9-160">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="cbec9-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="cbec9-161">ในฟิลด์ชื่อ พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="cbec9-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="cbec9-162">รหัส</span><span class="sxs-lookup"><span data-stu-id="cbec9-162">Id</span></span>  
29. <span data-ttu-id="cbec9-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-163">Click OK.</span></span>
30. <span data-ttu-id="cbec9-164">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="cbec9-165">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="cbec9-166">ในฟิลด์ชื่อ พิมพ์ 'ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="cbec9-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="cbec9-167">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="cbec9-167">Vendor</span></span>  
33. <span data-ttu-id="cbec9-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-168">Click OK.</span></span>
34. <span data-ttu-id="cbec9-169">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="cbec9-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="cbec9-170">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-170">Click Add Element.</span></span>
36. <span data-ttu-id="cbec9-171">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="cbec9-172">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="cbec9-172">Name</span></span>  
37. <span data-ttu-id="cbec9-173">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-173">Click OK.</span></span>
38. <span data-ttu-id="cbec9-174">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-174">Click Add Element.</span></span>
39. <span data-ttu-id="cbec9-175">ในฟิลด์ชื่อ พิมพ์ 'ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="cbec9-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="cbec9-176">ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="cbec9-176">Bank</span></span>  
40. <span data-ttu-id="cbec9-177">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-177">Click OK.</span></span>
41. <span data-ttu-id="cbec9-178">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="cbec9-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="cbec9-179">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-179">Click Add Element.</span></span>
43. <span data-ttu-id="cbec9-180">ในฟิลด์ชื่อ พิมพ์ 'หมายเลขการกำหนดเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="cbec9-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="cbec9-181">หมายเลขการกำหนดเส้นทาง
 </span><span class="sxs-lookup"><span data-stu-id="cbec9-181">RoutingNumber</span></span>  
44. <span data-ttu-id="cbec9-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-182">Click OK.</span></span>
45. <span data-ttu-id="cbec9-183">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-183">Click Add Element.</span></span>
46. <span data-ttu-id="cbec9-184">ในฟิลด์ชื่อ พิมพ์ 'หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="cbec9-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="cbec9-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="cbec9-185">AccountNumber</span></span>  
47. <span data-ttu-id="cbec9-186">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-186">Click OK.</span></span>
48. <span data-ttu-id="cbec9-187">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="cbec9-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="cbec9-188">คลิก คัดลอก</span><span class="sxs-lookup"><span data-stu-id="cbec9-188">Click Copy.</span></span>
50. <span data-ttu-id="cbec9-189">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="cbec9-190">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-190">Click Paste.</span></span>
52. <span data-ttu-id="cbec9-191">ในฟิลด์ชื่อ พิมพ์ 'ผู้ชำระ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="cbec9-192">ผู้จ่ายเงิน</span><span class="sxs-lookup"><span data-stu-id="cbec9-192">Payer</span></span>  
53. <span data-ttu-id="cbec9-193">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="cbec9-194">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-194">Click Add Element.</span></span>
55. <span data-ttu-id="cbec9-195">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="cbec9-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="cbec9-196">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="cbec9-196">Currency</span></span>  
56. <span data-ttu-id="cbec9-197">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-197">Click OK.</span></span>
57. <span data-ttu-id="cbec9-198">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-198">Click Add Element.</span></span>
58. <span data-ttu-id="cbec9-199">ในฟิลด์ชื่อ ให้พิมพ์ 'คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="cbec9-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="cbec9-200">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cbec9-200">Description</span></span>  
59. <span data-ttu-id="cbec9-201">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-201">Click OK.</span></span>
60. <span data-ttu-id="cbec9-202">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-202">Click Add Element.</span></span>
61. <span data-ttu-id="cbec9-203">ในฟิลด์ชื่อ พิมพ์ 'วันที่ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="cbec9-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="cbec9-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="cbec9-204">TransDate</span></span>  
62. <span data-ttu-id="cbec9-205">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-205">Click OK.</span></span>
63. <span data-ttu-id="cbec9-206">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="cbec9-206">Click Add Element.</span></span>
64. <span data-ttu-id="cbec9-207">ในฟิลด์ชื่อ พิมพ์ 'จำนวน'</span><span class="sxs-lookup"><span data-stu-id="cbec9-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="cbec9-208">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="cbec9-208">Amount</span></span>  
65. <span data-ttu-id="cbec9-209">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="cbec9-210">จัดเตรียมส่วนประกอบรูปแบบสำหรับการแม็ปไปยังองค์ประกอบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cbec9-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="cbec9-211">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\วันที่ประมวลผล'</span><span class="sxs-lookup"><span data-stu-id="cbec9-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="cbec9-212">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="cbec9-213">ในแผนภูมิ ให้เลือก 'ข้อความอักษร\วันที่และเวลา'</span><span class="sxs-lookup"><span data-stu-id="cbec9-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="cbec9-214">ในฟิลด์รูปแบบ พิมพ์ 'yyyy-MM-dd'</span><span class="sxs-lookup"><span data-stu-id="cbec9-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="cbec9-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="cbec9-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="cbec9-216">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-216">Click OK.</span></span>
6. <span data-ttu-id="cbec9-217">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="cbec9-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="cbec9-218">คลิก เพิ่มวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="cbec9-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="cbec9-219">ในฟิลด์รูปแบบ พิมพ์ 'yyyy-MM-dd'</span><span class="sxs-lookup"><span data-stu-id="cbec9-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="cbec9-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="cbec9-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="cbec9-221">ในฟิลด์ชนิดวันที่และเวลา ให้เลือก 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="cbec9-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="cbec9-222">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-222">Click OK.</span></span>
11. <span data-ttu-id="cbec9-223">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="cbec9-224">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cbec9-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="cbec9-225">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="cbec9-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="cbec9-226">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cbec9-226">Click OK.</span></span>
15. <span data-ttu-id="cbec9-227">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="cbec9-228">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-228">Click Add String.</span></span>
17. <span data-ttu-id="cbec9-229">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-229">Click OK.</span></span>
18. <span data-ttu-id="cbec9-230">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="cbec9-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="cbec9-231">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-231">Click Add String.</span></span>
20. <span data-ttu-id="cbec9-232">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-232">Click OK.</span></span>
21. <span data-ttu-id="cbec9-233">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="cbec9-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="cbec9-234">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-234">Click Add String.</span></span>
23. <span data-ttu-id="cbec9-235">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-235">Click OK.</span></span>
24. <span data-ttu-id="cbec9-236">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="cbec9-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="cbec9-237">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-237">Click Add String.</span></span>
26. <span data-ttu-id="cbec9-238">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-238">Click OK.</span></span>
27. <span data-ttu-id="cbec9-239">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="cbec9-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="cbec9-240">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-240">Click Add String.</span></span>
29. <span data-ttu-id="cbec9-241">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-241">Click OK.</span></span>
30. <span data-ttu-id="cbec9-242">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="cbec9-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="cbec9-243">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-243">Click Add String.</span></span>
32. <span data-ttu-id="cbec9-244">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-244">Click OK.</span></span>
33. <span data-ttu-id="cbec9-245">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="cbec9-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="cbec9-246">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-246">Click Add String.</span></span>
35. <span data-ttu-id="cbec9-247">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-247">Click OK.</span></span>
36. <span data-ttu-id="cbec9-248">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="cbec9-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="cbec9-249">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-249">Click Add String.</span></span>
38. <span data-ttu-id="cbec9-250">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-250">Click OK.</span></span>
39. <span data-ttu-id="cbec9-251">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\จำนวนเงิน'</span><span class="sxs-lookup"><span data-stu-id="cbec9-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="cbec9-252">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="cbec9-252">Click Add String.</span></span>
41. <span data-ttu-id="cbec9-253">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cbec9-253">Click OK.</span></span>
42. <span data-ttu-id="cbec9-254">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="cbec9-254">Click Save.</span></span>
43. <span data-ttu-id="cbec9-255">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cbec9-255">Close the page.</span></span>


