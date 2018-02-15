--- 
title: "ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Microsoft Office ที่มีรูปภาพที่ฝังสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER) (ส่วนที่ 1)"
description: "ขั้นตอนในหัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ในรูปแบบ Microsoft Office (Excel และ Word) ที่ประกอบด้วยรูปภาพที่ฝังอยู่"
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.sourcegitcommit: 9cb9343028acacc387370e1cdd2202b84919185e
ms.openlocfilehash: 844d8de1d5a1958457eaab1d434bef015f92e33c
ms.contentlocale: th-th
ms.lasthandoff: 01/23/2018

---
# <a name="design-configurations-to-generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er-part-1"></a><span data-ttu-id="420e0-103">ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Microsoft Office ที่มีรูปภาพที่ฝังสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER) (ส่วนที่ 1)</span><span class="sxs-lookup"><span data-stu-id="420e0-103">Design configurations to generate reports in Microsoft Office formats with embedded images for electronic reporting (ER) (Part 1)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="420e0-104">เพื่อทำตามขั้นตอนในกระบวนงานนี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำกระบวนงาน “ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งาน”</span><span class="sxs-lookup"><span data-stu-id="420e0-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="420e0-105">กระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสาร Microsoft Excel หรือ Word ที่ประกอบด้วยรูปภาพที่ฝังอยู่</span><span class="sxs-lookup"><span data-stu-id="420e0-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="420e0-106">ในกระบวนงานนี้ คุณจะสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นสำหรับบริษัทตัวอย่าง Litware, inc สามารถดำเนินขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล USMF</span><span class="sxs-lookup"><span data-stu-id="420e0-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="420e0-107">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="420e0-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="420e0-108">ก่อนที่คุณจะเริ่มต้น ดาวน์โหลดและบันทึกแฟ้มที่แสดงรายการอยู่ในหัวข้อวิธีใช้ [รูปและรูปร่างที่ฝังอยู่ในเอกสารทางธุรกิจที่ถูกสร้างขึ้นโดยใช้เครื่องมือการรายงานทางอิเล็กทรอนิกส์](../electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="420e0-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="420e0-109">แฟ้มคือ: แบบจำลองสำหรับเช็ค.xml รูปแบบการพิมพ์เช็ค.xml โลโก้.png โลโก้บริษัท.png รูปภาพลายเซ็น.png รูปภาพลายเซ็น 2.png และ Word เท็มเพลตของเช็ค.docx</span><span class="sxs-lookup"><span data-stu-id="420e0-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="420e0-110">ตรวจสอบข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="420e0-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="420e0-111">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="420e0-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="420e0-112">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="420e0-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="420e0-113">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน “สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่”</span><span class="sxs-lookup"><span data-stu-id="420e0-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="420e0-114">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="420e0-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="420e0-115">เพิ่มการตั้งค่าคอนฟิกแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="420e0-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="420e0-116">แทนที่จะสร้างแบบจำลองใหม่ คุณสามารถโหลดไฟล์โครงแบบแบบจำลอง ER ได้ (แบบจำลองสำหรับเช็ค.xml) ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="420e0-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="420e0-117">แฟ้มนี้ประกอบด้วย รูปแบบข้อมูลตัวอย่างสำหรับเช็คการชำระเงิน และการแม็ปของแบบจำลองข้อมูลกับส่วนประกอบข้อมูลของแอพลิเคชัน Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="420e0-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="420e0-118">บน FastTab ของเวอร์ชัน คลิก แลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="420e0-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="420e0-119">คลิก โหลดจากไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="420e0-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="420e0-120">คลิก เรียกดู และจากนั้นเลือกแบบจำลองสำหรับ cheques.xml</span><span class="sxs-lookup"><span data-stu-id="420e0-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="420e0-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="420e0-121">Click OK.</span></span>  
 6. <span data-ttu-id="420e0-122">แบบจำลองที่โหลดจะใช้เป็นแหล่งข้อมูลของข้อมูลในการสร้างเอกสารที่ประกอบด้วยรูปภาพใน Excel และ Word</span><span class="sxs-lookup"><span data-stu-id="420e0-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="420e0-123">เพิ่มการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="420e0-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="420e0-124">แทนที่จะสร้างรูปแบบใหม่ คุณสามารถโหลดไฟล์โครงแบบรูปแบบ ER ได้ (รูปแบบการพิมพ์เช็ค.xml) ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="420e0-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="420e0-125">แฟ้มนี้ประกอบด้วยโครงร่างตัวอย่างของรูปแบบที่จะพิมพ์เช็ค โดยใช้แบบฟอร์มที่พิมพ์ล่วงหน้าและการแม็ปรูปแบบนี้ไปยังแบบจำลองข้อมูล 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="420e0-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="420e0-126">คลิก แลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="420e0-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="420e0-127">คลิก โหลดจากไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="420e0-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="420e0-128">คลิก เรียกดู และเลือก ไฟล์รูปแบบการพิมพ์เช็ค.xml</span><span class="sxs-lookup"><span data-stu-id="420e0-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="420e0-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="420e0-129">Click OK.</span></span>  
 6. <span data-ttu-id="420e0-130">ในแผนภูมิ ขยาย 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="420e0-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="420e0-131">ในแผนภูมิ เลือก 'แบบจำลองสำหรับเช็ค\รูปแบบการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="420e0-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="420e0-132">รูปแบบที่โหลดจะใช้เพื่อสร้างเอกสารที่ประกอบด้วยรูปภาพใน Excel และ Word</span><span class="sxs-lookup"><span data-stu-id="420e0-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="420e0-133">ตั้งค่าคอนฟิกพารามิเตอร์ผู้ใช้ ER</span><span class="sxs-lookup"><span data-stu-id="420e0-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="420e0-134">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="420e0-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="420e0-135">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="420e0-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="420e0-136">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="420e0-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="420e0-137">เปิดใช้งานแฟล็ก 'รันฉบับร่าง' เพื่อเริ่มต้นเวอร์ชันแบบร่างของรูปแบบที่เลือก แทนที่เวอร์ชันที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="420e0-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="420e0-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="420e0-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="420e0-139">ตั้งค่าคอนฟิกเงินสด & พารามิเตอร์การจัดการธนาคาร</span><span class="sxs-lookup"><span data-stu-id="420e0-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="420e0-140">ไปที่ การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="420e0-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="420e0-141">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'USMF OPER'</span><span class="sxs-lookup"><span data-stu-id="420e0-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="420e0-142">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="420e0-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="420e0-143">คลิกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="420e0-143">Click Check.</span></span>  
 5. <span data-ttu-id="420e0-144">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="420e0-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="420e0-145">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="420e0-145">Click Edit.</span></span>  
 7. <span data-ttu-id="420e0-146">เลือก ใช่ ในฟิลด์โลโก้ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="420e0-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="420e0-147">คลิกโลโก้ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="420e0-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="420e0-148">คลิกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="420e0-148">Click Change.</span></span>  
 10. <span data-ttu-id="420e0-149">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ โลโก้บริษัท.png</span><span class="sxs-lookup"><span data-stu-id="420e0-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="420e0-150">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="420e0-150">Click Save.</span></span>  
 12. <span data-ttu-id="420e0-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="420e0-151">Close the page.</span></span>  
 13. <span data-ttu-id="420e0-152">ขยายส่วนลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="420e0-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="420e0-153">เลือก ใช่ ในฟิลด์พิมพ์ลายเซ็นแรก</span><span class="sxs-lookup"><span data-stu-id="420e0-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="420e0-154">คลิกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="420e0-154">Click Change.</span></span>  
 16. <span data-ttu-id="420e0-155">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ รูปภาพลายเซ็น.png</span><span class="sxs-lookup"><span data-stu-id="420e0-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="420e0-156">ขยายส่วนสำเนา</span><span class="sxs-lookup"><span data-stu-id="420e0-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="420e0-157">ในฟิลด์ลายน้ำ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="420e0-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="420e0-158">เลือก ใช่ ในรูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="420e0-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="420e0-159">เลือกการตั้งค่าคอนฟิก 'แบบฟอร์มในการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="420e0-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="420e0-160">ขณะนี้ รูปแบบ ER ที่เลือกจะใช้สำหรับการพิมพ์เช็ค</span><span class="sxs-lookup"><span data-stu-id="420e0-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="420e0-161">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="420e0-161">Click Attach.</span></span>  
 23. <span data-ttu-id="420e0-162">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="420e0-162">Click New.</span></span>  
 24. <span data-ttu-id="420e0-163">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="420e0-163">Click File.</span></span>  
 25. <span data-ttu-id="420e0-164">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ รูปภาพลายเซ็น 2.png</span><span class="sxs-lookup"><span data-stu-id="420e0-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="420e0-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="420e0-165">Close the page.</span></span>  
 27. <span data-ttu-id="420e0-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="420e0-166">Close the page.</span></span>  
 28. <span data-ttu-id="420e0-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="420e0-167">Close the page.</span></span>  
 29. <span data-ttu-id="420e0-168">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > พารามิเตอร์การจัดการเงินสดและธนาคาร</span><span class="sxs-lookup"><span data-stu-id="420e0-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="420e0-169">เลือก ใช่ ในฟิลด์ อนุญาตให้สร้างบันทึกย่อในบัญชีธนาคารที่ไม่ได้ใช้งานอยู่:</span><span class="sxs-lookup"><span data-stu-id="420e0-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="420e0-170">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="420e0-170">Click Save.</span></span>  
 32. <span data-ttu-id="420e0-171">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="420e0-171">Close the page.</span></span>  

