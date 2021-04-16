---
title: ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 3 - สร้างรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ เพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์ ER (ส่วนที่ 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755021"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="567f1-104">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 3 - สร้างรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="567f1-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="567f1-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="567f1-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="567f1-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="567f1-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="567f1-107">เพื่อทำให้ขั้นตอนเหล่านี้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำให้ขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2: ขยายรูปแบบจำลองข้อมูล)" เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="567f1-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="567f1-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="567f1-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="567f1-109">สร้างรูปแบบเพื่อเพื่อประมวลผลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="567f1-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="567f1-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="567f1-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="567f1-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="567f1-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="567f1-112">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="567f1-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="567f1-113">ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="567f1-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="567f1-114">คุณจะสร้างรูปแบบเพื่อสร้างข้อความทางอิเล็กทรอนิกส์ที่มีข้อมูลเกี่ยวกับไฟล์ใดๆ ที่แนบกับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="567f1-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="567f1-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="567f1-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="567f1-116">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองใบแจ้งหนี้ของลูกค้า (กำหนดเอง)'</span><span class="sxs-lookup"><span data-stu-id="567f1-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="567f1-117">ในฟิลด์ชื่อ ให้พิมพ์ 'ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="567f1-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="567f1-118">ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="567f1-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="567f1-119">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="567f1-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="567f1-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="567f1-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="567f1-121">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="567f1-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="567f1-122">ออกแบบรูปแบบเพื่อเติมข้อมูลเอกสารแนบลงในข้อความที่สร้างในรูปแบบ MIME</span><span class="sxs-lookup"><span data-stu-id="567f1-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="567f1-123">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="567f1-123">Click Designer.</span></span>
2. <span data-ttu-id="567f1-124">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="567f1-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="567f1-125">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="567f1-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="567f1-126">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="567f1-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="567f1-127">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="567f1-127">Invoice</span></span>  
5. <span data-ttu-id="567f1-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-128">Click OK.</span></span>
6. <span data-ttu-id="567f1-129">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="567f1-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="567f1-130">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="567f1-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="567f1-131">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'SalesOrder'</span><span class="sxs-lookup"><span data-stu-id="567f1-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="567f1-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="567f1-132">SalesOrder</span></span>  
9. <span data-ttu-id="567f1-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-133">Click OK.</span></span>
10. <span data-ttu-id="567f1-134">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="567f1-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="567f1-135">ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceNumber'</span><span class="sxs-lookup"><span data-stu-id="567f1-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="567f1-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="567f1-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="567f1-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-137">Click OK.</span></span>
13. <span data-ttu-id="567f1-138">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="567f1-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="567f1-139">ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceAmount'</span><span class="sxs-lookup"><span data-stu-id="567f1-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="567f1-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="567f1-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="567f1-141">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-141">Click OK.</span></span>
16. <span data-ttu-id="567f1-142">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="567f1-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="567f1-143">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="567f1-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="567f1-144">ในฟิลด์ชื่อ ให้พิมพ์ 'EnclosedDocs'</span><span class="sxs-lookup"><span data-stu-id="567f1-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="567f1-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="567f1-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="567f1-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-146">Click OK.</span></span>
20. <span data-ttu-id="567f1-147">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs'</span><span class="sxs-lookup"><span data-stu-id="567f1-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="567f1-148">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="567f1-148">Click Add Element.</span></span>
22. <span data-ttu-id="567f1-149">ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสาร'</span><span class="sxs-lookup"><span data-stu-id="567f1-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="567f1-150">เอกสาร</span><span class="sxs-lookup"><span data-stu-id="567f1-150">Document</span></span>  
23. <span data-ttu-id="567f1-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-151">Click OK.</span></span>
24. <span data-ttu-id="567f1-152">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'</span><span class="sxs-lookup"><span data-stu-id="567f1-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="567f1-153">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="567f1-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="567f1-154">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="567f1-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="567f1-155">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="567f1-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="567f1-156">FileName</span><span class="sxs-lookup"><span data-stu-id="567f1-156">FileName</span></span>  
28. <span data-ttu-id="567f1-157">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-157">Click OK.</span></span>
29. <span data-ttu-id="567f1-158">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="567f1-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="567f1-159">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="567f1-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="567f1-160">ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'</span><span class="sxs-lookup"><span data-stu-id="567f1-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="567f1-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="567f1-161">FileContent</span></span>  
32. <span data-ttu-id="567f1-162">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-162">Click OK.</span></span>
33. <span data-ttu-id="567f1-163">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent'</span><span class="sxs-lookup"><span data-stu-id="567f1-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="567f1-164">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="567f1-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="567f1-165">ในแผนภูมิ ให้เลือก 'Text\Base64'</span><span class="sxs-lookup"><span data-stu-id="567f1-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="567f1-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="567f1-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="567f1-167">แม็ปองค์ประกอบรูปแบบไปยังแบบจำลองข้อมูลโดยเป็นแหล่งที่มาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="567f1-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="567f1-168">ในแผนภูมิ ให้เลือก 'Invoice\SalesOrder'</span><span class="sxs-lookup"><span data-stu-id="567f1-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="567f1-169">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="567f1-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="567f1-170">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="567f1-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="567f1-171">ในแผนภูมิ ให้เลือก 'model\Sales order number(SalesId)'</span><span class="sxs-lookup"><span data-stu-id="567f1-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="567f1-172">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="567f1-172">Click Bind.</span></span>
6. <span data-ttu-id="567f1-173">ในแผนภูมิ ให้เลือก 'Invoice\InvoiceNumber'</span><span class="sxs-lookup"><span data-stu-id="567f1-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="567f1-174">ในแผนภูมิ ให้ขยาย 'model\Base invoice(InvoiceBase)'</span><span class="sxs-lookup"><span data-stu-id="567f1-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="567f1-175">ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice number(Id)'</span><span class="sxs-lookup"><span data-stu-id="567f1-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="567f1-176">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="567f1-176">Click Bind.</span></span>
10. <span data-ttu-id="567f1-177">ในแผนภูมิ ให้เลือก 'Invoice\InvoiceAmount'</span><span class="sxs-lookup"><span data-stu-id="567f1-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="567f1-178">ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'</span><span class="sxs-lookup"><span data-stu-id="567f1-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="567f1-179">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="567f1-179">Click Bind.</span></span>
13. <span data-ttu-id="567f1-180">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="567f1-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="567f1-181">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="567f1-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="567f1-182">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent\Base64'</span><span class="sxs-lookup"><span data-stu-id="567f1-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="567f1-183">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="567f1-183">Click Bind.</span></span>
17. <span data-ttu-id="567f1-184">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="567f1-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="567f1-185">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileName'</span><span class="sxs-lookup"><span data-stu-id="567f1-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="567f1-186">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="567f1-186">Click Bind.</span></span>
20. <span data-ttu-id="567f1-187">ในแผนภูมิ ให้เลือก 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="567f1-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="567f1-188">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'</span><span class="sxs-lookup"><span data-stu-id="567f1-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="567f1-189">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="567f1-189">Click Bind.</span></span>
23. <span data-ttu-id="567f1-190">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="567f1-190">Click Save.</span></span>
24. <span data-ttu-id="567f1-191">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="567f1-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]