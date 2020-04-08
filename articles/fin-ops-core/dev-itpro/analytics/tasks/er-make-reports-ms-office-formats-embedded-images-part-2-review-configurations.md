---
title: ตรวจทานการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Office ที่มีรูปภาพที่ฝัง
description: เมื่อต้องการทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำตามขั้นตอนในคู่มืองาน "ER ทำรายงานในรูปแบบ MS Office ที่มีรูปภาพที่ฝัง (ส่วนที่ 1 - ตั้งค่าพารามิเตอร์)"
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f81f0f86c255d048393047965c0aa29cbef09d0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143088"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="fe039-103">ตรวจทานการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Office ที่มีรูปภาพที่ฝัง</span><span class="sxs-lookup"><span data-stu-id="fe039-103">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe039-104">เมื่อต้องการทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำตามขั้นตอนในคู่มืองาน "ER ทำรายงานในรูปแบบ MS Office ที่มีรูปภาพที่ฝัง (ส่วนที่ 1: ตั้งค่าพารามิเตอร์)"</span><span class="sxs-lookup"><span data-stu-id="fe039-104">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="fe039-105">กระบวนงานนี้แสดงวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารทางอิเล็กทรอนิกส์ที่ประกอบด้วยภาพที่ฝังใน Microsoft Excel และ Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="fe039-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="fe039-106">ในตัวอย่างนี้ คุณจะตรวจทานการตั้งค่าคอนฟิก ER สำหรับบริษัทตัวอย่าง Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fe039-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="fe039-107">กระบวนงานนี้มีไว้สำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="fe039-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="fe039-108">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล USMF</span><span class="sxs-lookup"><span data-stu-id="fe039-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="fe039-109">ตรวจทานแบบจำลองข้อมูลที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="fe039-109">Review the imported data model</span></span>
1. <span data-ttu-id="fe039-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="fe039-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fe039-111">ในแผนภูมิ ให้เลือก 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="fe039-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="fe039-112">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fe039-112">Click Designer.</span></span>
    * <span data-ttu-id="fe039-113">แบบจำลองนี้ได้รับการออกแบบมาเพื่อแสดงถึงเช็คการชำระเงินจากจุดยืนทางธุรกิจและการแม็ปแบบจำลองนี้กับแหล่งข้อมูลของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fe039-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="fe039-114">ตรวจทานแบบจำลองนี้โดยผู้ออกแบบการดำเนินงาน ER</span><span class="sxs-lookup"><span data-stu-id="fe039-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="fe039-115">หมายเหตุว่าแอททริบิวต์ขององค์ประกอบแบบจำลองที่จะนำเสนอ: โครงสร้าง ชื่อ คำอธิบาย ชนิดข้อมูล และอื่น ๆ </span><span class="sxs-lookup"><span data-stu-id="fe039-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="fe039-116">ในแผนภูมิ ให้ขยาย 'ราก'</span><span class="sxs-lookup"><span data-stu-id="fe039-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="fe039-117">ในแผนภูมิ ให้เลือก 'ราก\เช็ค'</span><span class="sxs-lookup"><span data-stu-id="fe039-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="fe039-118">ในแผนภูมิ ขยายหรือยุบ 'ราก\เช็ค'</span><span class="sxs-lookup"><span data-stu-id="fe039-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="fe039-119">ในแผนภูมิ ขยาย 'ราก\เช็ค\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="fe039-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="fe039-120">ในแผนภูมิ ให้ขยาย 'ราก\ผู้ชำระ'</span><span class="sxs-lookup"><span data-stu-id="fe039-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="fe039-121">ในแผนภูมิ ให้เลือก 'ราก\istestrun'</span><span class="sxs-lookup"><span data-stu-id="fe039-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="fe039-122">ในแผนภูมิ ให้เลือก 'ราก\โครงร่าง'</span><span class="sxs-lookup"><span data-stu-id="fe039-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="fe039-123">องค์ประกอบเค้าโครงของแบบจำลองนี้แสดงรายละเอียดของโครงร่างแบบฟอร์มการพิมพ์เช็คสำหรับบัญชีธนาคารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fe039-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="fe039-124">และยังประกอบด้วยโหนดสองรายการของชนิดข้อมูลคอนเทนเนอร์เพื่อจัดเก็บรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="fe039-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="fe039-125">ในแผนภูมิ ให้ขยาย 'ราก\โครงร่าง'</span><span class="sxs-lookup"><span data-stu-id="fe039-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="fe039-126">ในแผนภูมิ เลือก 'ราก\โครงร่าง\โลโก้บริษัท'</span><span class="sxs-lookup"><span data-stu-id="fe039-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="fe039-127">ในแผนภูมิ ขยาย 'ราก\โครงร่าง\โลโก้บริษัท'</span><span class="sxs-lookup"><span data-stu-id="fe039-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="fe039-128">ในแผนภูมิ เลือก 'ราก\โครงร่าง\โลโก้บริษัท\รูปภาพ'</span><span class="sxs-lookup"><span data-stu-id="fe039-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="fe039-129">ในแผนภูมิ เลือก 'ราก\โครงร่าง\โลโก้บริษัท\isprinted'</span><span class="sxs-lookup"><span data-stu-id="fe039-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="fe039-130">ในแผนภูมิ ให้เลือก 'ราก\โครงร่าง\ลายเซ็น'</span><span class="sxs-lookup"><span data-stu-id="fe039-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="fe039-131">ในแผนภูมิ ขยาย 'ราก\โครงร่าง\ลายเซ็น'</span><span class="sxs-lookup"><span data-stu-id="fe039-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="fe039-132">ในแผนภูมิ ให้เลือก 'ราก\โครงร่าง\ลายเซ็น\รูปภาพ'</span><span class="sxs-lookup"><span data-stu-id="fe039-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="fe039-133">ในแผนภูมิ ให้เลือก 'ราก\โครงร่าง\ลายเซ็น\isprinted'</span><span class="sxs-lookup"><span data-stu-id="fe039-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="fe039-134">หมายเหตุว่าองค์ประกอบแบบจำลองข้อมูลรูปภาพทั้งสองจะผูกอยู่กับฟิลด์ของตารางที่ประกอบด้วยรูปภาพของโลโก้บริษัทและลายเซ็นของบุคคลที่ได้รับอนุญาตในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="fe039-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="fe039-135">ในแผนภูมิ ขยาย 'ราก\โครงร่าง\ลายน้ำ'</span><span class="sxs-lookup"><span data-stu-id="fe039-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="fe039-136">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fe039-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="fe039-137">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fe039-137">Click Designer.</span></span>
23. <span data-ttu-id="fe039-138">ในแผนภูมิ ขยาย 'chequesselected'</span><span class="sxs-lookup"><span data-stu-id="fe039-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="fe039-139">ในแผนภูมิ ขยาย 'โครงร่าง'</span><span class="sxs-lookup"><span data-stu-id="fe039-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="fe039-140">ในแผนภูมิ ขยาย 'โครงร่าง\โลโก้บริษัท'</span><span class="sxs-lookup"><span data-stu-id="fe039-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="fe039-141">ในแผนภูมิ ขยาย 'โครงร่าง\ลายเซ็น'</span><span class="sxs-lookup"><span data-stu-id="fe039-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="fe039-142">ในแผนภูมิ ขยาย 'โครงร่าง\ลายน้ำ'</span><span class="sxs-lookup"><span data-stu-id="fe039-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="fe039-143">เปิด 'แสดงรายละเอียด'</span><span class="sxs-lookup"><span data-stu-id="fe039-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="fe039-144">หมายเหตุว่าองค์ประกอบแบบจำลองข้อมูลเช็คถูกผูกไว้กับตาราง TmpChequePrintout ซึ่งในขณะรันไทม์ จะประกอบด้วยเรกคอร์ดสำหรับเช็คที่ผู้ใช้เลือกไว้สำหรับการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="fe039-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="fe039-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe039-145">Close the page.</span></span>
30. <span data-ttu-id="fe039-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe039-146">Close the page.</span></span>
31. <span data-ttu-id="fe039-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe039-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="fe039-148">ตรวจทานรูปแบบที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="fe039-148">Review the imported format</span></span>
1. <span data-ttu-id="fe039-149">ในแผนภูมิ ขยาย 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="fe039-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="fe039-150">ในแผนภูมิ เลือก 'แบบจำลองสำหรับเช็ค\รูปแบบการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="fe039-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="fe039-151">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fe039-151">Click Designer.</span></span>
4. <span data-ttu-id="fe039-152">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="fe039-152">Click Attachments.</span></span>
5. <span data-ttu-id="fe039-153">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="fe039-153">Click Open.</span></span>
    * <span data-ttu-id="fe039-154">เปิดเท็มเพลตของรายงานที่แนบมาใน Excel</span><span class="sxs-lookup"><span data-stu-id="fe039-154">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="fe039-155">ตรวจทานเท็มเพลต Excel ของรายงานที่แนบมาที่จะใช้ในการพิมพ์เช็ค</span><span class="sxs-lookup"><span data-stu-id="fe039-155">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="fe039-156">เท็มเพลตที่ประกอบด้วยเช็คสองรายการต่อหนึ่งหน้าและมีวัตถุประสงค์เพื่อพิมพ์เช็คไปยังแบบฟอร์มที่พิมพ์ไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="fe039-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="fe039-157">หมายเหตุว่ารูปภาพที่ว่างสองรายการจะถูกฝังอยู่</span><span class="sxs-lookup"><span data-stu-id="fe039-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="fe039-158">รูปภาพที่ว่างเหล่านี้มีไว้สำหรับโลโก้บริษัทและลายเซ็นของบุคคลที่ได้รับการอนุมัติสำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="fe039-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="fe039-159">ตรวจสอบว่ารูปภาพมีชื่อว่า CompLogo และ SignatureImage ตามลำดับใน Excel</span><span class="sxs-lookup"><span data-stu-id="fe039-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="fe039-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe039-160">Close the page.</span></span>
7. <span data-ttu-id="fe039-161">ในแผนภูมิ ขยาย 'รายงาน'</span><span class="sxs-lookup"><span data-stu-id="fe039-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="fe039-162">ในแผนภูมิ ขยาย 'รายงาน\ChequeLines'</span><span class="sxs-lookup"><span data-stu-id="fe039-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="fe039-163">ในแผนภูมิ เลือก 'รายงาน\ChequeLines\CompLogo'</span><span class="sxs-lookup"><span data-stu-id="fe039-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="fe039-164">เปิด 'แสดงรายละเอียด'</span><span class="sxs-lookup"><span data-stu-id="fe039-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="fe039-165">หมายเหตุว่าองค์ประกอบเซลล์ของรูปแบบ 'CompLogo' แสดงรายการ Excel ที่ใช้เพื่อเติมข้อมูลรูปภาพโลโก้ของบริษัทในรายงาน</span><span class="sxs-lookup"><span data-stu-id="fe039-165">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="fe039-166">องค์ประกอบรูปแบบนี้ถูกผูกเข้ากับองค์ประกอบแบบจำลองข้อมูลรูปภาพนั้นซึ่งในช่วงรันไทม์จะประกอบด้วยรูปภาพโลโก้บริษัทในรูปแบบฐานสอง</span><span class="sxs-lookup"><span data-stu-id="fe039-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="fe039-167">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="fe039-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="fe039-168">คลิก แก้ไขการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fe039-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="fe039-169">หมายเหตุว่าคุณสามารถสร้างองค์ประกอบเซลล์ของรูปแบบ 'CompLogo' เพื่อให้ไม่มีการเปิดใช้งานอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="fe039-169">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="fe039-170">ในกรณีนี้ องค์ประกอบรูปภาพ Excel ที่เชื่อมโยงกันจะซ่อนโลโก้บริษัทในรายงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fe039-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="fe039-171">ถ้านิพจน์ที่เปิดใช้งานส่งคืน TRUE และการผูกข้อมูลที่กำหนดไม่มีรูปภาพ องค์ประกอบรูปภาพ Excel ที่เชื่อมโยงกันจะแสดงรูปภาพที่บันทึกไว้ในเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="fe039-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="fe039-172">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe039-172">Close the page.</span></span>
14. <span data-ttu-id="fe039-173">ในแผนภูมิ ขยาย 'ป้ายชื่อ: คอนเทนเนอร์'</span><span class="sxs-lookup"><span data-stu-id="fe039-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="fe039-174">ป้ายชื่อบางรายการที่แสดงอยู่ในฟอร์มเช็คที่พิมพ์ไว้ล่วงหน้าจะถูกรวมในรายงาน เมื่อมีการสร้างขึ้นเพื่อวัตถุประสงค์ในการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fe039-174">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="fe039-175">อย่างไรก็ตาม จะไม่สามารถพิมพ์ป้ายชื่อเหล่านั้นในระหว่างการพิมพ์จริงได้ เนื่องจากฟอร์มที่พิมพ์ไว้ล่วงหน้าได้รวมรายการเหล่านั้นไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="fe039-175">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="fe039-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe039-176">Close the page.</span></span>

