--- 
title: "สร้างรูปแบบเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์ ER"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดให้กับบทบาทผู้ดูแลระบบหรือบทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสารได้ในผลลัพธ์ ER "
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1815a0004eee6734b3c7d2c2f9e75ce5fe16af1c
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---

# <a name="create-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="4ce8b-103">สร้างรูปแบบเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์ ER</span><span class="sxs-lookup"><span data-stu-id="4ce8b-103">Create formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ce8b-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="4ce8b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="4ce8b-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="4ce8b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4ce8b-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2: ขยายรูปแบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="4ce8b-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="4ce8b-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="4ce8b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="4ce8b-108">สร้างรูปแบบเพื่อเพื่อประมวลผลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4ce8b-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="4ce8b-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4ce8b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4ce8b-110">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="4ce8b-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4ce8b-111">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="4ce8b-112">ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="4ce8b-113">คุณจะสร้างรูปแบบเพื่อสร้างข้อความทางอิเล็กทรอนิกส์ที่มีข้อมูลเกี่ยวกับไฟล์ใดๆ ที่แนบกับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4ce8b-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="4ce8b-114">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="4ce8b-115">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองใบแจ้งหนี้ของลูกค้า (กำหนดเอง)'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="4ce8b-116">ในฟิลด์ชื่อ ให้พิมพ์ 'ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="4ce8b-117">ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4ce8b-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="4ce8b-118">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="4ce8b-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="4ce8b-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="4ce8b-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="4ce8b-120">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="4ce8b-121">ออกแบบรูปแบบเพื่อเติมข้อมูลเอกสารแนบลงในข้อความที่สร้างในรูปแบบ MIME</span><span class="sxs-lookup"><span data-stu-id="4ce8b-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="4ce8b-122">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="4ce8b-122">Click Designer.</span></span>
2. <span data-ttu-id="4ce8b-123">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="4ce8b-124">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="4ce8b-125">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="4ce8b-126">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4ce8b-126">Invoice</span></span>  
5. <span data-ttu-id="4ce8b-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-127">Click OK.</span></span>
6. <span data-ttu-id="4ce8b-128">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="4ce8b-129">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="4ce8b-130">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'SalesOrder'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="4ce8b-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="4ce8b-131">SalesOrder</span></span>  
9. <span data-ttu-id="4ce8b-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-132">Click OK.</span></span>
10. <span data-ttu-id="4ce8b-133">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="4ce8b-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="4ce8b-134">ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceNumber'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="4ce8b-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="4ce8b-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="4ce8b-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-136">Click OK.</span></span>
13. <span data-ttu-id="4ce8b-137">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="4ce8b-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="4ce8b-138">ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceAmount'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="4ce8b-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="4ce8b-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="4ce8b-140">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-140">Click OK.</span></span>
16. <span data-ttu-id="4ce8b-141">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="4ce8b-142">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="4ce8b-143">ในฟิลด์ชื่อ ให้พิมพ์ 'EnclosedDocs'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="4ce8b-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="4ce8b-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="4ce8b-145">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-145">Click OK.</span></span>
20. <span data-ttu-id="4ce8b-146">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="4ce8b-147">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="4ce8b-147">Click Add Element.</span></span>
22. <span data-ttu-id="4ce8b-148">ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสาร'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="4ce8b-149">เอกสาร</span><span class="sxs-lookup"><span data-stu-id="4ce8b-149">Document</span></span>  
23. <span data-ttu-id="4ce8b-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-150">Click OK.</span></span>
24. <span data-ttu-id="4ce8b-151">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="4ce8b-152">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="4ce8b-153">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="4ce8b-154">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="4ce8b-155">FileName</span><span class="sxs-lookup"><span data-stu-id="4ce8b-155">FileName</span></span>  
28. <span data-ttu-id="4ce8b-156">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-156">Click OK.</span></span>
29. <span data-ttu-id="4ce8b-157">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="4ce8b-158">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="4ce8b-159">ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="4ce8b-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="4ce8b-160">FileContent</span></span>  
32. <span data-ttu-id="4ce8b-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-161">Click OK.</span></span>
33. <span data-ttu-id="4ce8b-162">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="4ce8b-163">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="4ce8b-164">ในแผนภูมิ ให้เลือก 'Text\Base64'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="4ce8b-165">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ce8b-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="4ce8b-166">แม็ปองค์ประกอบรูปแบบไปยังแบบจำลองข้อมูลโดยเป็นแหล่งที่มาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4ce8b-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="4ce8b-167">ในแผนภูมิ ให้เลือก 'Invoice\SalesOrder'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="4ce8b-168">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="4ce8b-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="4ce8b-169">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="4ce8b-170">ในแผนภูมิ ให้เลือก 'model\Sales order number(SalesId)'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="4ce8b-171">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-171">Click Bind.</span></span>
6. <span data-ttu-id="4ce8b-172">ในแผนภูมิ ให้เลือก 'Invoice\InvoiceNumber'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="4ce8b-173">ในแผนภูมิ ให้ขยาย 'model\Base invoice(InvoiceBase)'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="4ce8b-174">ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice number(Id)'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="4ce8b-175">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-175">Click Bind.</span></span>
10. <span data-ttu-id="4ce8b-176">ในแผนภูมิ ให้เลือก 'Invoice\InvoiceAmount'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="4ce8b-177">ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="4ce8b-178">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-178">Click Bind.</span></span>
13. <span data-ttu-id="4ce8b-179">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="4ce8b-180">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="4ce8b-181">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent\Base64'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="4ce8b-182">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-182">Click Bind.</span></span>
17. <span data-ttu-id="4ce8b-183">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="4ce8b-184">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileName'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="4ce8b-185">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-185">Click Bind.</span></span>
20. <span data-ttu-id="4ce8b-186">ในแผนภูมิ ให้เลือก 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="4ce8b-187">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'</span><span class="sxs-lookup"><span data-stu-id="4ce8b-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="4ce8b-188">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-188">Click Bind.</span></span>
23. <span data-ttu-id="4ce8b-189">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4ce8b-189">Click Save.</span></span>
24. <span data-ttu-id="4ce8b-190">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ce8b-190">Close the page.</span></span>


