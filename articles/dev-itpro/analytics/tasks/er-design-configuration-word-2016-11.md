--- 
title: "ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ Microsoft Word สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์ Microsoft Word"
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d602e07548d22bcdee3f375c3c327c0e8963c3b4
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a><span data-ttu-id="0d8fb-103">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ Microsoft Word สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="0d8fb-103">Design a configuration for generating reports in Microsoft Word format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d8fb-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์ Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="0d8fb-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="0d8fb-105">ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัท GBSI</span><span class="sxs-lookup"><span data-stu-id="0d8fb-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="0d8fb-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ คุณต้องทำขั้นตอนอย่างแรกให้เสร็จสมบูรณ์ในคู่มืองาน "สร้างการตั้งค่าคอนฟิก ER สำหรับการสร้างรายงานในรูปแบบ OPENXML" ก่อน</span><span class="sxs-lookup"><span data-stu-id="0d8fb-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="0d8fb-107">นอกจากนี้คุณยังต้องดาวน์โหลดและบันทึกเท็มเพลตต่อไปนี้ล่วงหน้าไว้ภายในเครื่องสำหรับรายงานตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="0d8fb-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

<span data-ttu-id="0d8fb-108">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx</span><span class="sxs-lookup"><span data-stu-id="0d8fb-108">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx</span></span>

<span data-ttu-id="0d8fb-109">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx</span><span class="sxs-lookup"><span data-stu-id="0d8fb-109">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx</span></span>

<span data-ttu-id="0d8fb-110">กระบวนงานนี้ใช้สำหรับคุณลักษณะที่ถูกเพิ่มเข้ามาใน Microsoft Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="0d8fb-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="0d8fb-111">เลือกการตั้งค่าคอนฟิกรายงาน ER ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0d8fb-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="0d8fb-112">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0d8fb-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0d8fb-113">ตรวจสอบให้แน่ใจว่ามีการเลือกให้ผู้ให้บริการการตั้งค่าคอนฟิก 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="0d8fb-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="0d8fb-114">เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0d8fb-114">is selected as active.</span></span>  
2. <span data-ttu-id="0d8fb-115">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="0d8fb-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="0d8fb-116">เราจะใช้การตั้งค่าคอนฟิก ER ที่มีอยู่ ซึ่งแต่เดิมได้รับการออกแบบเพื่อสร้างเอาท์พุทรายงานในรูปแบบ OPENXML อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="0d8fb-117">ในแผนภูมิ ขยาย 'รูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="0d8fb-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="0d8fb-118">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน\รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="0d8fb-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="0d8fb-119">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="0d8fb-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="0d8fb-120">แทนที่เท็มเพลต Excel ด้วยเท็มเพลต Word</span><span class="sxs-lookup"><span data-stu-id="0d8fb-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="0d8fb-121">ปัจจุบัน เอกสาร Excel จะใช้เป็นเท็มเพลตเพื่อสร้างเอาท์พุทในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="0d8fb-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="0d8fb-122">เราจะนำเข้าเท็มเพลตของรายงานในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="0d8fb-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="0d8fb-123">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="0d8fb-123">Click Attachments.</span></span>
    * <span data-ttu-id="0d8fb-124">แทนที่เท็มเพลต Excel ที่มีอยู่ด้วยเท็มเพลต Word ที่คุณดาวน์โหลดมาก่อนหน้านี้ SampleVendPaymDocReport.docx</span><span class="sxs-lookup"><span data-stu-id="0d8fb-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="0d8fb-125">หมายเหตุ เท็มเพลตนี้ประกอบด้วยโครงร่างของเอกสารที่เราต้องการสร้างเป็นเอาท์พุท ER เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0d8fb-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="0d8fb-126">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="0d8fb-126">Click Delete.</span></span>
3. <span data-ttu-id="0d8fb-127">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="0d8fb-127">Click Yes.</span></span>
4. <span data-ttu-id="0d8fb-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-128">Click New.</span></span>
5. <span data-ttu-id="0d8fb-129">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="0d8fb-129">Click File.</span></span>
6. <span data-ttu-id="0d8fb-130">คลิกเรียกดู</span><span class="sxs-lookup"><span data-stu-id="0d8fb-130">Click Browse.</span></span> <span data-ttu-id="0d8fb-131">นำทางไปยังและเลือก SampleVendPaymDocReport.docx ที่คุณดาวน์โหลดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="0d8fb-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="0d8fb-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-132">Click OK.</span></span>
    * <span data-ttu-id="0d8fb-133">เลือกเท็มเพลตที่คุณดาวน์โหลดไว้แล้วในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="0d8fb-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="0d8fb-134">ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0d8fb-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="0d8fb-135">ขยายเท็มเพลต Word โดยการเพิ่มส่วน XML แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="0d8fb-136">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d8fb-136">Click Save.</span></span>
    * <span data-ttu-id="0d8fb-137">นอกจากจะเก็บข้อมูลการเปลี่ยนแปลงการตั้งค่าคอนฟิก การดำเนินการบันทึกยังเป็นการอัพเดตเท็มเพลต Word ที่แนบอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="0d8fb-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="0d8fb-138">โครงสร้างของรูปแบบที่ได้รับการออกแบบมาถูกนำไปยังเอกสาร Word ที่แนบเป็นส่วน XML แบบกำหนดเองใหม่ด้วยชื่อ 'รายงาน'</span><span class="sxs-lookup"><span data-stu-id="0d8fb-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="0d8fb-139">โปรดทราบว่า เท็มเพลต Word ที่แนบไม่ได้มีเฉพาะโครงร่างของเอกสารที่เราต้องการสร้างเป็นเอาท์พุท ER แต่ยังประกอบด้วยโครงสร้างของข้อมูลที่ ER จะเติมลงในเท็มเพลตนี้ขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="0d8fb-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="0d8fb-140">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="0d8fb-140">Click Attachments.</span></span>
    * <span data-ttu-id="0d8fb-141">ขณะนี้ คุณจำเป็นต้องเชื่อมโยงองค์ประกอบของส่วน XML แบบกำหนดเอง 'รายงาน' กับส่วนเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="0d8fb-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="0d8fb-142">ถ้าคุณคุ้นเคยกับเอกสาร Word ที่สามารถออกแบบให้เป็นแบบฟอร์มที่มีตัวควบคุมเนื้อหา ซึ่งถูกกำหนดขอบเขตด้วยองค์ประกอบของส่วน XML แบบกำหนดเอง – เล่นขั้นตอนทั้งหมดของงานย่อยถัดไปเพื่อสร้างเอกสารดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="0d8fb-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="0d8fb-143">สำหรับรายละเอียดเพิ่มเติม ให้ดูลิงก์นี้ https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US</span><span class="sxs-lookup"><span data-stu-id="0d8fb-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="0d8fb-144">หรือข้ามขั้นตอนทั้งหมดในงานย่อยถัดไป</span><span class="sxs-lookup"><span data-stu-id="0d8fb-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="0d8fb-145">เรียกดู Word ด้วยส่วน XML แบบกำหนดเองเพื่อดำเนินการเชื่อมโยงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0d8fb-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="0d8fb-146">เปิดเอกสารนี้ใน Word และดำเนินการต่อไปนี้:  - เปิดแท็บนักพัฒนา Word (เลือกกำหนด Ribbon ถ้ายังไม่ได้เปิดใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="0d8fb-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="0d8fb-147">- เลือกบานหน้าต่างการแม็ป XML</span><span class="sxs-lookup"><span data-stu-id="0d8fb-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="0d8fb-148">- เลือกส่วน XML แบบกำหนดเอง 'รายงาน' ในการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0d8fb-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="0d8fb-149">- ทำการแม็ปองค์ประกอบของส่วน XML แบบกำหนดเองที่เลือกและตัวควบคุมเนื้อหาของเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="0d8fb-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="0d8fb-150">- บันทึกเอกสาร Word ที่อัพเดตแล้วบนไดรฟ์ในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="0d8fb-151">อัพโหลดเท็มเพลต Word ด้วยส่วน XML แบบกำหนดเองที่ถูกกำหนดขอบเขตไปยังตัวควบคุมเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="0d8fb-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="0d8fb-152">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="0d8fb-152">Click Delete.</span></span>
2. <span data-ttu-id="0d8fb-153">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="0d8fb-153">Click Yes.</span></span>
    * <span data-ttu-id="0d8fb-154">เพิ่มเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="0d8fb-154">Add a new template.</span></span> <span data-ttu-id="0d8fb-155">ถ้าคุณทำขั้นตอนต่างๆ ในงานย่อยก่อนหน้านี้เสร็จสมบูรณ์แล้ว ให้เลือกเอกสาร Word ที่คุณจัดเตรียม และบันทึกภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="0d8fb-156">หรือเลือกเท็มเพลต MS Word SampleVendPaymDocReportBounded.docx ที่ดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="0d8fb-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="0d8fb-157">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-157">Click New.</span></span>
4. <span data-ttu-id="0d8fb-158">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="0d8fb-158">Click File.</span></span>
5. <span data-ttu-id="0d8fb-159">คลิกเรียกดู</span><span class="sxs-lookup"><span data-stu-id="0d8fb-159">Click Browse.</span></span> <span data-ttu-id="0d8fb-160">นำทางไปยังและเลือก SampleVendPaymDocReportBounded.docx ที่คุณดาวน์โหลดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="0d8fb-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="0d8fb-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-161">Click OK.</span></span>
6. <span data-ttu-id="0d8fb-162">ในฟิลด์เท็มเพลต ให้เลือกเอกสารที่คุณดาวน์โหลดไว้แล้วในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="0d8fb-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="0d8fb-163">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d8fb-163">Click Save.</span></span>
8. <span data-ttu-id="0d8fb-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0d8fb-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="0d8fb-165">ดำเนินการรูปแบบเพื่อสร้างเอาท์พุทของ Word</span><span class="sxs-lookup"><span data-stu-id="0d8fb-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="0d8fb-166">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="0d8fb-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="0d8fb-167">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0d8fb-167">Click User parameters.</span></span>
3. <span data-ttu-id="0d8fb-168">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="0d8fb-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="0d8fb-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-169">Click OK.</span></span>
5. <span data-ttu-id="0d8fb-170">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="0d8fb-170">Click Edit.</span></span>
6. <span data-ttu-id="0d8fb-171">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="0d8fb-172">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d8fb-172">Click Save.</span></span>
8. <span data-ttu-id="0d8fb-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0d8fb-173">Close the page.</span></span>
9. <span data-ttu-id="0d8fb-174">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0d8fb-174">Close the page.</span></span>
10. <span data-ttu-id="0d8fb-175">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0d8fb-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="0d8fb-176">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="0d8fb-176">Click Lines.</span></span>
12. <span data-ttu-id="0d8fb-177">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="0d8fb-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="0d8fb-178">คลิกสถานะการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0d8fb-178">Click Payment status.</span></span>
14. <span data-ttu-id="0d8fb-179">คลิก ไม่มี</span><span class="sxs-lookup"><span data-stu-id="0d8fb-179">Click None.</span></span>
15. <span data-ttu-id="0d8fb-180">คลิกสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0d8fb-180">Click Generate payments.</span></span>
16. <span data-ttu-id="0d8fb-181">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-181">Click OK.</span></span>
17. <span data-ttu-id="0d8fb-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0d8fb-182">Click OK.</span></span>
    * <span data-ttu-id="0d8fb-183">วิเคราะห์ผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0d8fb-183">Analyze the generated output.</span></span> <span data-ttu-id="0d8fb-184">โปรดทราบว่าผลลัพธ์ที่สร้างขึ้นจะแสดงในรูปแบบ Word และประกอบด้วยรายละเอียดเกี่ยวกับการชำระเงินที่ประมวลผลแล้ว</span><span class="sxs-lookup"><span data-stu-id="0d8fb-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


