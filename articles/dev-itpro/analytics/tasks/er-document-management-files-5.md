--- 
title: "แก้ไขและเรียกใช้รูปแบบที่จะใช้ไฟล์การจัดการเอกสารในผลลัพธ์ ER"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER "
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 5effbecf98e633d07f9e5eb22d3df1a12967c1e4
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="modify-and-run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="d8171-103">แก้ไขและเรียกใช้รูปแบบที่จะใช้ไฟล์การจัดการเอกสารในผลลัพธ์ ER</span><span class="sxs-lookup"><span data-stu-id="d8171-103">Modify and run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8171-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="d8171-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d8171-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="d8171-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d8171-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 4: รันรูปแบบ)"</span><span class="sxs-lookup"><span data-stu-id="d8171-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="d8171-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="d8171-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="d8171-108">แก้ไขรูปแบบเพื่อเติมข้อมูลเอกสารแนบลงในข้อความที่สร้างในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="d8171-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="d8171-109">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="d8171-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d8171-110">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="d8171-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="d8171-111">ในแผนภูมิ ขยาย 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="d8171-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="d8171-112">ในแผนภูมิ เลือกตัวอย่างข้อความใบแจ้งหนี้ 'Customer invoice model\Customer invoice model (custom)\Electronic'</span><span class="sxs-lookup"><span data-stu-id="d8171-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="d8171-113">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="d8171-113">Click Designer.</span></span>
    * <span data-ttu-id="d8171-114">คุณจะเติมข้อมูลข้อความใบแจ้งหนี้ในผลลัพธ์ที่สร้างเป็นไฟล์ XML โดยใช้การเข้ารหัส UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8171-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="d8171-115">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8171-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="d8171-116">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="d8171-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="d8171-117">ในฟิลด์ชื่อ พิมพ์ 'ข้อความ Xml'</span><span class="sxs-lookup"><span data-stu-id="d8171-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="d8171-118">ข้อความ Xml</span><span class="sxs-lookup"><span data-stu-id="d8171-118">Xml message</span></span>  
9. <span data-ttu-id="d8171-119">ในฟิลด์การเข้ารหัส พิมพ์ 'UTF-8'</span><span class="sxs-lookup"><span data-stu-id="d8171-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="d8171-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="d8171-120">UTF-8</span></span>  
10. <span data-ttu-id="d8171-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8171-121">Click OK.</span></span>
    * <span data-ttu-id="d8171-122">ตั้งค่าคอนฟิกผลลัพธ์ที่สร้างเป็นไฟล์ที่มีการอัด</span><span class="sxs-lookup"><span data-stu-id="d8171-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="d8171-123">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8171-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="d8171-124">ในแผนภูมิ เลือก 'Common\Folder'</span><span class="sxs-lookup"><span data-stu-id="d8171-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="d8171-125">ในฟิลด์ชื่อ พิมพ์ 'ผลลัพธ์รหัสไปรษณีย์'</span><span class="sxs-lookup"><span data-stu-id="d8171-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="d8171-126">ผลลัพธ์รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="d8171-126">Zip output</span></span>  
14. <span data-ttu-id="d8171-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8171-127">Click OK.</span></span>
15. <span data-ttu-id="d8171-128">ในแผนภูมิ ให้เลือก 'ผลลัพธ์รหัสไปรษณีย์'</span><span class="sxs-lookup"><span data-stu-id="d8171-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="d8171-129">เพิ่มเอกสารแนบกับไฟล์ที่มีการอัดได้ที่สร้างเป็นไฟล์ที่มีชื่อและนามสกุลเดิม</span><span class="sxs-lookup"><span data-stu-id="d8171-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="d8171-130">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8171-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="d8171-131">ในแผนภูมิ เลือก 'Common\File'</span><span class="sxs-lookup"><span data-stu-id="d8171-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="d8171-132">ในฟิลด์ชื่อ ให้พิมพ์ 'ไฟล์ที่แนบมา'</span><span class="sxs-lookup"><span data-stu-id="d8171-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="d8171-133">ไฟล์ที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="d8171-133">Attached file</span></span>  
19. <span data-ttu-id="d8171-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8171-134">Click OK.</span></span>
20. <span data-ttu-id="d8171-135">ในแผนภูมิ ให้เลือก 'Zip output\Attached file'</span><span class="sxs-lookup"><span data-stu-id="d8171-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="d8171-136">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d8171-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="d8171-137">ในแผนภูมิ ให้เลือก 'Text\Base64'</span><span class="sxs-lookup"><span data-stu-id="d8171-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="d8171-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8171-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="d8171-139">แม็ปองค์ประกอบรูปแบบใหม่ไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d8171-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="d8171-140">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="d8171-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="d8171-141">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="d8171-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="d8171-142">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="d8171-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="d8171-143">ในแผนภูมิ ให้เลือก 'Zip output\Attached file\Base64'</span><span class="sxs-lookup"><span data-stu-id="d8171-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="d8171-144">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="d8171-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="d8171-145">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="d8171-145">Click Bind.</span></span>
7. <span data-ttu-id="d8171-146">ในแผนภูมิ ให้เลือก 'Zip output\Attached file'</span><span class="sxs-lookup"><span data-stu-id="d8171-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="d8171-147">คลิก แก้ไขชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="d8171-147">Click Edit filename.</span></span>
9. <span data-ttu-id="d8171-148">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="d8171-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="d8171-149">ในแผนภูมิ ให้ขยาย 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="d8171-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="d8171-150">ในแผนภูมิ ให้เลือก 'model\Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="d8171-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="d8171-151">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d8171-151">Click Add data source.</span></span>
13. <span data-ttu-id="d8171-152">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="d8171-152">Click Save.</span></span>
14. <span data-ttu-id="d8171-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d8171-153">Close the page.</span></span>
15. <span data-ttu-id="d8171-154">ในแผนภูมิ ให้เลือก 'model\Invoice attachments'</span><span class="sxs-lookup"><span data-stu-id="d8171-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="d8171-155">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="d8171-155">Click Bind.</span></span>
17. <span data-ttu-id="d8171-156">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d8171-156">Click Save.</span></span>
18. <span data-ttu-id="d8171-157">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d8171-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="d8171-158">รันรายงานที่ออกแบบไว้สำหรับใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d8171-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="d8171-159">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="d8171-159">Click Run.</span></span>
2. <span data-ttu-id="d8171-160">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน ()</span><span class="sxs-lookup"><span data-stu-id="d8171-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="d8171-161">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="d8171-161">Click Filter.</span></span>
4. <span data-ttu-id="d8171-162">เลือกแถวของสมุดรายวันใบแจ้งหนี้ของลูกค้าและฟิลด์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d8171-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="d8171-163">ในฟิลด์เกณฑ์ ในฟิลด์ "ใบสั่งขาย" เกณฑ์ ให้พิมพ์หมายเลขใบสั่ง 000148</span><span class="sxs-lookup"><span data-stu-id="d8171-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="d8171-164">000148</span><span class="sxs-lookup"><span data-stu-id="d8171-164">000148</span></span>  
6. <span data-ttu-id="d8171-165">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8171-165">Click OK.</span></span>
7. <span data-ttu-id="d8171-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d8171-166">Click OK.</span></span>
    * <span data-ttu-id="d8171-167">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="d8171-167">Review the generated output.</span></span> <span data-ttu-id="d8171-168">โปรดทราบว่า นอกเหนือจากข้อความใบแจ้งหนี้ในรูปแบบ XML มีการสร้างไฟล์เดี่ยวสำหรับเอกสารแนบแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="d8171-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="d8171-169">ไฟล์แนบจะถูกเติมข้อมูลด้วยผลลัพธ์ที่มีการอัดในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="d8171-169">The attachment files are populated with the zipped output in binary format.</span></span>  


