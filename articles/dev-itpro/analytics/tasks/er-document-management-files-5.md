---
title: ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 5 - แก้ไขและรันรูปแบบ)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba9cc4dcdfcfbc1bdb933336e85da9b4b6d97a40
ms.sourcegitcommit: f5556189a80ad9f23f1af3333837eae034ddb247
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/29/2019
ms.locfileid: "1791867"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="ce4db-103">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 5: แก้ไขและรันรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="ce4db-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce4db-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="ce4db-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ce4db-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="ce4db-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ce4db-106">เพื่อดำเนินการขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องดำเนินการขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 4: รันรูปแบบ)"</span><span class="sxs-lookup"><span data-stu-id="ce4db-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="ce4db-107">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="ce4db-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="ce4db-108">แก้ไขรูปแบบเพื่อเติมข้อมูลเอกสารแนบลงในข้อความที่สร้างในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="ce4db-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="ce4db-109">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ce4db-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ce4db-110">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="ce4db-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ce4db-111">ในแผนภูมิ ขยาย 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="ce4db-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ce4db-112">ในแผนภูมิ เลือกตัวอย่างข้อความใบแจ้งหนี้ 'Customer invoice model\Customer invoice model (custom)\Electronic'</span><span class="sxs-lookup"><span data-stu-id="ce4db-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ce4db-113">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="ce4db-113">Click Designer.</span></span>
    * <span data-ttu-id="ce4db-114">คุณจะเติมข้อมูลข้อความใบแจ้งหนี้ในผลลัพธ์ที่สร้างเป็นไฟล์ XML โดยใช้การเข้ารหัส UNICODE</span><span class="sxs-lookup"><span data-stu-id="ce4db-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="ce4db-115">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="ce4db-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="ce4db-116">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="ce4db-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="ce4db-117">ในฟิลด์ชื่อ พิมพ์ 'ข้อความ Xml'</span><span class="sxs-lookup"><span data-stu-id="ce4db-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="ce4db-118">ข้อความ Xml</span><span class="sxs-lookup"><span data-stu-id="ce4db-118">Xml message</span></span>  
9. <span data-ttu-id="ce4db-119">ในฟิลด์การเข้ารหัส พิมพ์ 'UTF-8'</span><span class="sxs-lookup"><span data-stu-id="ce4db-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="ce4db-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="ce4db-120">UTF-8</span></span>  
10. <span data-ttu-id="ce4db-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ce4db-121">Click OK.</span></span>
    * <span data-ttu-id="ce4db-122">ตั้งค่าคอนฟิกผลลัพธ์ที่สร้างเป็นไฟล์ที่มีการอัด</span><span class="sxs-lookup"><span data-stu-id="ce4db-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="ce4db-123">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="ce4db-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="ce4db-124">ในแผนภูมิ เลือก 'Common\Folder'</span><span class="sxs-lookup"><span data-stu-id="ce4db-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="ce4db-125">ในฟิลด์ชื่อ พิมพ์ 'ผลลัพธ์รหัสไปรษณีย์'</span><span class="sxs-lookup"><span data-stu-id="ce4db-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="ce4db-126">ผลลัพธ์รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="ce4db-126">Zip output</span></span>  
14. <span data-ttu-id="ce4db-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ce4db-127">Click OK.</span></span>
15. <span data-ttu-id="ce4db-128">ในแผนภูมิ ให้เลือก 'ผลลัพธ์รหัสไปรษณีย์'</span><span class="sxs-lookup"><span data-stu-id="ce4db-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="ce4db-129">เพิ่มเอกสารแนบกับไฟล์ที่มีการอัดได้ที่สร้างเป็นไฟล์ที่มีชื่อและนามสกุลเดิม</span><span class="sxs-lookup"><span data-stu-id="ce4db-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="ce4db-130">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="ce4db-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="ce4db-131">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="ce4db-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="ce4db-132">ในฟิลด์ชื่อ ให้พิมพ์ 'ไฟล์ที่แนบมา'</span><span class="sxs-lookup"><span data-stu-id="ce4db-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="ce4db-133">ไฟล์ที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="ce4db-133">Attached file</span></span>  
19. <span data-ttu-id="ce4db-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ce4db-134">Click OK.</span></span>
20. <span data-ttu-id="ce4db-135">ในแผนภูมิ ให้เลือก 'Zip output\Attached file'</span><span class="sxs-lookup"><span data-stu-id="ce4db-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="ce4db-136">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="ce4db-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="ce4db-137">ในแผนภูมิ ให้เลือก 'Text\Base64'</span><span class="sxs-lookup"><span data-stu-id="ce4db-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="ce4db-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ce4db-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="ce4db-139">แม็ปองค์ประกอบรูปแบบใหม่ไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ce4db-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="ce4db-140">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="ce4db-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="ce4db-141">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="ce4db-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="ce4db-142">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="ce4db-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="ce4db-143">ในแผนภูมิ ให้เลือก 'Zip output\Attached file\Base64'</span><span class="sxs-lookup"><span data-stu-id="ce4db-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="ce4db-144">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="ce4db-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="ce4db-145">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="ce4db-145">Click Bind.</span></span>
7. <span data-ttu-id="ce4db-146">ในแผนภูมิ ให้เลือก 'Zip output\Attached file'</span><span class="sxs-lookup"><span data-stu-id="ce4db-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="ce4db-147">คลิก แก้ไขชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="ce4db-147">Click Edit filename.</span></span>
9. <span data-ttu-id="ce4db-148">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="ce4db-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="ce4db-149">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="ce4db-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="ce4db-150">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="ce4db-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="ce4db-151">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ce4db-151">Click Add data source.</span></span>
13. <span data-ttu-id="ce4db-152">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="ce4db-152">Click Save.</span></span>
14. <span data-ttu-id="ce4db-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ce4db-153">Close the page.</span></span>
15. <span data-ttu-id="ce4db-154">ในแผนภูมิ ให้เลือก 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="ce4db-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="ce4db-155">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="ce4db-155">Click Bind.</span></span>
17. <span data-ttu-id="ce4db-156">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ce4db-156">Click Save.</span></span>
18. <span data-ttu-id="ce4db-157">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ce4db-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ce4db-158">รันรายงานที่ออกแบบไว้สำหรับใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ce4db-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ce4db-159">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ce4db-159">Click Run.</span></span>
2. <span data-ttu-id="ce4db-160">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน ()</span><span class="sxs-lookup"><span data-stu-id="ce4db-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="ce4db-161">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="ce4db-161">Click Filter.</span></span>
4. <span data-ttu-id="ce4db-162">เลือกแถวของสมุดรายวันใบแจ้งหนี้ของลูกค้าและฟิลด์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="ce4db-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="ce4db-163">ในฟิลด์เกณฑ์ ในฟิลด์ "ใบสั่งขาย" เกณฑ์ ให้พิมพ์หมายเลขใบสั่ง 000148</span><span class="sxs-lookup"><span data-stu-id="ce4db-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="ce4db-164">000148</span><span class="sxs-lookup"><span data-stu-id="ce4db-164">000148</span></span>  
6. <span data-ttu-id="ce4db-165">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ce4db-165">Click OK.</span></span>
7. <span data-ttu-id="ce4db-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ce4db-166">Click OK.</span></span>
    * <span data-ttu-id="ce4db-167">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="ce4db-167">Review the generated output.</span></span> <span data-ttu-id="ce4db-168">โปรดทราบว่านอกเหนือจากข้อความใบแจ้งหนี้ในรูปแบบ XML จะมีเพียงไฟล์เดียวที่ถูกสร้างสำหรับเอกสารแนบแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="ce4db-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="ce4db-169">ไฟล์แนบจะถูกเติมข้อมูลด้วยผลลัพธ์ที่มีการอัดในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="ce4db-169">The attachment files are populated with the zipped output in binary format.</span></span>  

