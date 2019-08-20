---
title: สร้างรูปแบบเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์ ER
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดให้กับบทบาทผู้ดูแลระบบหรือบทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสารได้ในผลลัพธ์ ER '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05c0c4a38f34774e7018504c5e3fab834a2ec1b1
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850290"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3-create-format"></a><span data-ttu-id="5a2f3-103">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 3: สร้างรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="5a2f3-103">ER Use Document Management files in format outputs (Part 3: Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a2f3-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="5a2f3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="5a2f3-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="5a2f3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5a2f3-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2: ขยายรูปแบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="5a2f3-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="5a2f3-107">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="5a2f3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="5a2f3-108">สร้างรูปแบบเพื่อเพื่อประมวลผลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="5a2f3-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="5a2f3-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5a2f3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5a2f3-110">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="5a2f3-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5a2f3-111">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="5a2f3-112">ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="5a2f3-113">คุณจะสร้างรูปแบบเพื่อสร้างข้อความทางอิเล็กทรอนิกส์ที่มีข้อมูลเกี่ยวกับไฟล์ใดๆ ที่แนบกับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5a2f3-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="5a2f3-114">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="5a2f3-115">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองใบแจ้งหนี้ของลูกค้า (กำหนดเอง)'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="5a2f3-116">ในฟิลด์ชื่อ ให้พิมพ์ 'ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="5a2f3-117">ข้อความตัวอย่างใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5a2f3-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="5a2f3-118">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="5a2f3-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="5a2f3-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="5a2f3-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="5a2f3-120">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="5a2f3-121">ออกแบบรูปแบบเพื่อเติมข้อมูลเอกสารแนบลงในข้อความที่สร้างในรูปแบบ MIME</span><span class="sxs-lookup"><span data-stu-id="5a2f3-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="5a2f3-122">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="5a2f3-122">Click Designer.</span></span>
2. <span data-ttu-id="5a2f3-123">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="5a2f3-124">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="5a2f3-125">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="5a2f3-126">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="5a2f3-126">Invoice</span></span>  
5. <span data-ttu-id="5a2f3-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-127">Click OK.</span></span>
6. <span data-ttu-id="5a2f3-128">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="5a2f3-129">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="5a2f3-130">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'SalesOrder'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="5a2f3-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="5a2f3-131">SalesOrder</span></span>  
9. <span data-ttu-id="5a2f3-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-132">Click OK.</span></span>
10. <span data-ttu-id="5a2f3-133">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="5a2f3-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="5a2f3-134">ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceNumber'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="5a2f3-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="5a2f3-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="5a2f3-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-136">Click OK.</span></span>
13. <span data-ttu-id="5a2f3-137">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="5a2f3-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="5a2f3-138">ในฟิลด์ชื่อ ให้พิมพ์ 'InvoiceAmount'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="5a2f3-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="5a2f3-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="5a2f3-140">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-140">Click OK.</span></span>
16. <span data-ttu-id="5a2f3-141">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="5a2f3-142">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="5a2f3-143">ในฟิลด์ชื่อ ให้พิมพ์ 'EnclosedDocs'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="5a2f3-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="5a2f3-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="5a2f3-145">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-145">Click OK.</span></span>
20. <span data-ttu-id="5a2f3-146">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="5a2f3-147">คลิก เพิ่มองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="5a2f3-147">Click Add Element.</span></span>
22. <span data-ttu-id="5a2f3-148">ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสาร'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="5a2f3-149">เอกสาร</span><span class="sxs-lookup"><span data-stu-id="5a2f3-149">Document</span></span>  
23. <span data-ttu-id="5a2f3-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-150">Click OK.</span></span>
24. <span data-ttu-id="5a2f3-151">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="5a2f3-152">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="5a2f3-153">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="5a2f3-154">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="5a2f3-155">FileName</span><span class="sxs-lookup"><span data-stu-id="5a2f3-155">FileName</span></span>  
28. <span data-ttu-id="5a2f3-156">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-156">Click OK.</span></span>
29. <span data-ttu-id="5a2f3-157">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="5a2f3-158">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="5a2f3-159">ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="5a2f3-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="5a2f3-160">FileContent</span></span>  
32. <span data-ttu-id="5a2f3-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-161">Click OK.</span></span>
33. <span data-ttu-id="5a2f3-162">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="5a2f3-163">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="5a2f3-164">ในแผนภูมิ ให้เลือก 'Text\Base64'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="5a2f3-165">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5a2f3-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="5a2f3-166">แม็ปองค์ประกอบรูปแบบไปยังแบบจำลองข้อมูลโดยเป็นแหล่งที่มาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5a2f3-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="5a2f3-167">ในแผนภูมิ ให้เลือก 'Invoice\SalesOrder'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="5a2f3-168">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="5a2f3-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="5a2f3-169">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="5a2f3-170">ในแผนภูมิ ให้เลือก 'model\Sales order number(SalesId)'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="5a2f3-171">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-171">Click Bind.</span></span>
6. <span data-ttu-id="5a2f3-172">ในแผนภูมิ ให้เลือก 'Invoice\InvoiceNumber'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="5a2f3-173">ในแผนภูมิ ให้ขยาย 'model\Base invoice(InvoiceBase)'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="5a2f3-174">ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice number(Id)'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="5a2f3-175">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-175">Click Bind.</span></span>
10. <span data-ttu-id="5a2f3-176">ในแผนภูมิ ให้เลือก 'Invoice\InvoiceAmount'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="5a2f3-177">ในแผนภูมิ ให้เลือก 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="5a2f3-178">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-178">Click Bind.</span></span>
13. <span data-ttu-id="5a2f3-179">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="5a2f3-180">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="5a2f3-181">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileContent\Base64'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="5a2f3-182">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-182">Click Bind.</span></span>
17. <span data-ttu-id="5a2f3-183">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="5a2f3-184">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document\FileName'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="5a2f3-185">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-185">Click Bind.</span></span>
20. <span data-ttu-id="5a2f3-186">ในแผนภูมิ ให้เลือก 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="5a2f3-187">ในแผนภูมิ ให้เลือก 'Invoice\EnclosedDocs\Document'</span><span class="sxs-lookup"><span data-stu-id="5a2f3-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="5a2f3-188">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-188">Click Bind.</span></span>
23. <span data-ttu-id="5a2f3-189">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5a2f3-189">Click Save.</span></span>
24. <span data-ttu-id="5a2f3-190">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5a2f3-190">Close the page.</span></span>

