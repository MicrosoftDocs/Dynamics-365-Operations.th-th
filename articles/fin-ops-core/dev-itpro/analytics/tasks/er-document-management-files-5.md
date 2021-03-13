---
title: ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 5 - แก้ไขและรันรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER (ส่วนที่ 5)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092499"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="b581d-104">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 5 - แก้ไขและรันรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="b581d-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b581d-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="b581d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b581d-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="b581d-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="b581d-107">เพื่อดำเนินการขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องดำเนินการขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 4: รันรูปแบบ)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b581d-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="b581d-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="b581d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="b581d-109">แก้ไขรูปแบบเพื่อเติมข้อมูลเอกสารแนบลงในข้อความที่สร้างในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="b581d-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="b581d-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b581d-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b581d-111">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="b581d-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="b581d-112">ในแผนภูมิ ขยาย 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="b581d-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="b581d-113">ในแผนภูมิ เลือกตัวอย่างข้อความใบแจ้งหนี้ 'Customer invoice model\Customer invoice model (custom)\Electronic'</span><span class="sxs-lookup"><span data-stu-id="b581d-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="b581d-114">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b581d-114">Click Designer.</span></span>
    * <span data-ttu-id="b581d-115">คุณจะเติมข้อมูลข้อความใบแจ้งหนี้ในผลลัพธ์ที่สร้างเป็นไฟล์ XML โดยใช้การเข้ารหัส UNICODE</span><span class="sxs-lookup"><span data-stu-id="b581d-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="b581d-116">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b581d-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="b581d-117">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="b581d-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="b581d-118">ในฟิลด์ชื่อ พิมพ์ 'ข้อความ Xml'</span><span class="sxs-lookup"><span data-stu-id="b581d-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="b581d-119">ข้อความ Xml</span><span class="sxs-lookup"><span data-stu-id="b581d-119">Xml message</span></span>  
9. <span data-ttu-id="b581d-120">ในฟิลด์การเข้ารหัส พิมพ์ 'UTF-8'</span><span class="sxs-lookup"><span data-stu-id="b581d-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="b581d-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="b581d-121">UTF-8</span></span>  
10. <span data-ttu-id="b581d-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b581d-122">Click OK.</span></span>
    * <span data-ttu-id="b581d-123">ตั้งค่าคอนฟิกผลลัพธ์ที่สร้างเป็นไฟล์ที่มีการอัด</span><span class="sxs-lookup"><span data-stu-id="b581d-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="b581d-124">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b581d-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="b581d-125">ในแผนภูมิ เลือก 'Common\Folder'</span><span class="sxs-lookup"><span data-stu-id="b581d-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="b581d-126">ในฟิลด์ชื่อ พิมพ์ 'ผลลัพธ์รหัสไปรษณีย์'</span><span class="sxs-lookup"><span data-stu-id="b581d-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="b581d-127">ผลลัพธ์รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="b581d-127">Zip output</span></span>  
14. <span data-ttu-id="b581d-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b581d-128">Click OK.</span></span>
15. <span data-ttu-id="b581d-129">ในแผนภูมิ ให้เลือก 'ผลลัพธ์รหัสไปรษณีย์'</span><span class="sxs-lookup"><span data-stu-id="b581d-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="b581d-130">เพิ่มเอกสารแนบกับไฟล์ที่มีการอัดได้ที่สร้างเป็นไฟล์ที่มีชื่อและนามสกุลเดิม</span><span class="sxs-lookup"><span data-stu-id="b581d-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="b581d-131">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b581d-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="b581d-132">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="b581d-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="b581d-133">ในฟิลด์ชื่อ ให้พิมพ์ 'ไฟล์ที่แนบมา'</span><span class="sxs-lookup"><span data-stu-id="b581d-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="b581d-134">ไฟล์ที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="b581d-134">Attached file</span></span>  
19. <span data-ttu-id="b581d-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b581d-135">Click OK.</span></span>
20. <span data-ttu-id="b581d-136">ในแผนภูมิ ให้เลือก 'Zip output\Attached file'</span><span class="sxs-lookup"><span data-stu-id="b581d-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="b581d-137">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b581d-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="b581d-138">ในแผนภูมิ ให้เลือก 'Text\Base64'</span><span class="sxs-lookup"><span data-stu-id="b581d-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="b581d-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b581d-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="b581d-140">แม็ปองค์ประกอบรูปแบบใหม่ไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b581d-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="b581d-141">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="b581d-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="b581d-142">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="b581d-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="b581d-143">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="b581d-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="b581d-144">ในแผนภูมิ ให้เลือก 'Zip output\Attached file\Base64'</span><span class="sxs-lookup"><span data-stu-id="b581d-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="b581d-145">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="b581d-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="b581d-146">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b581d-146">Click Bind.</span></span>
7. <span data-ttu-id="b581d-147">ในแผนภูมิ ให้เลือก 'Zip output\Attached file'</span><span class="sxs-lookup"><span data-stu-id="b581d-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="b581d-148">คลิก แก้ไขชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="b581d-148">Click Edit filename.</span></span>
9. <span data-ttu-id="b581d-149">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="b581d-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="b581d-150">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="b581d-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="b581d-151">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="b581d-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="b581d-152">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b581d-152">Click Add data source.</span></span>
13. <span data-ttu-id="b581d-153">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="b581d-153">Click Save.</span></span>
14. <span data-ttu-id="b581d-154">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b581d-154">Close the page.</span></span>
15. <span data-ttu-id="b581d-155">ในแผนภูมิ ให้เลือก 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="b581d-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="b581d-156">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b581d-156">Click Bind.</span></span>
17. <span data-ttu-id="b581d-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b581d-157">Click Save.</span></span>
18. <span data-ttu-id="b581d-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b581d-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="b581d-159">รันรายงานที่ออกแบบไว้สำหรับใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b581d-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="b581d-160">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="b581d-160">Click Run.</span></span>
2. <span data-ttu-id="b581d-161">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน ()</span><span class="sxs-lookup"><span data-stu-id="b581d-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="b581d-162">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="b581d-162">Click Filter.</span></span>
4. <span data-ttu-id="b581d-163">เลือกแถวของสมุดรายวันใบแจ้งหนี้ของลูกค้าและฟิลด์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="b581d-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="b581d-164">ในฟิลด์เกณฑ์ ในฟิลด์ "ใบสั่งขาย" ของเกณฑ์ ให้พิมพ์หมายเลขใบสั่ง 000148</span><span class="sxs-lookup"><span data-stu-id="b581d-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="b581d-165">000148</span><span class="sxs-lookup"><span data-stu-id="b581d-165">000148</span></span>  
6. <span data-ttu-id="b581d-166">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="b581d-166">Click OK.</span></span>
7. <span data-ttu-id="b581d-167">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="b581d-167">Click OK.</span></span>
    * <span data-ttu-id="b581d-168">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="b581d-168">Review the generated output.</span></span> <span data-ttu-id="b581d-169">โปรดทราบว่านอกเหนือจากข้อความใบแจ้งหนี้ในรูปแบบ XML จะมีเพียงไฟล์เดียวที่ถูกสร้างสำหรับเอกสารแนบแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="b581d-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="b581d-170">ไฟล์แนบจะถูกเติมข้อมูลด้วยผลลัพธ์ที่มีการอัดในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="b581d-170">The attachment files are populated with the zipped output in binary format.</span></span>  

