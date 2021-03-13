---
title: ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Office ที่มีรูปภาพที่ฝัง
description: หัวข้อนี้อธิบายเกี่ยวกับวิธีการออกแบบการตั้งค่าคอนฟิกที่สร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ Excel และ Word ที่ประกอบด้วยภาพที่ฝัง
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b60ed6b07851c44ceb4b8f313bc65f04b802e646
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093681"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="1211b-103">ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Office ที่มีรูปภาพที่ฝัง</span><span class="sxs-lookup"><span data-stu-id="1211b-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1211b-104">เพื่อทำตามขั้นตอนในกระบวนงานนี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำกระบวนงาน “ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่”</span><span class="sxs-lookup"><span data-stu-id="1211b-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="1211b-105">กระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสาร Microsoft Excel หรือ Word ที่ประกอบด้วยภาพที่ฝัง</span><span class="sxs-lookup"><span data-stu-id="1211b-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="1211b-106">ในกระบวนงานนี้ คุณจะสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นสำหรับบริษัทตัวอย่าง Litware, inc สามารถดำเนินขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล USMF</span><span class="sxs-lookup"><span data-stu-id="1211b-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="1211b-107">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1211b-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="1211b-108">ก่อนที่คุณจะเริ่มต้น ดาวน์โหลดและบันทึกแฟ้มที่แสดงรายการอยู่ในหัวข้อวิธีใช้ [รูปและรูปร่างที่ฝังอยู่ในเอกสารที่คุณสร้างขึ้นโดยใช้ ER ](../electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="1211b-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="1211b-109">แฟ้มคือ: แบบจำลองสำหรับเช็ค.xml รูปแบบการพิมพ์เช็ค.xml โลโก้.png โลโก้บริษัท.png รูปภาพลายเซ็น.png รูปภาพลายเซ็น 2.png และ Word เท็มเพลตของเช็ค.docx</span><span class="sxs-lookup"><span data-stu-id="1211b-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="1211b-110">ตรวจสอบข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="1211b-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="1211b-111">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1211b-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="1211b-112">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1211b-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="1211b-113">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1211b-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="1211b-114">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="1211b-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="1211b-115">เพิ่มการตั้งค่าคอนฟิกแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="1211b-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="1211b-116">แทนที่จะสร้างแบบจำลองใหม่ คุณสามารถโหลดไฟล์โครงแบบแบบจำลอง ER ได้ (แบบจำลองสำหรับเช็ค.xml) ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="1211b-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="1211b-117">ไฟล์นี้ประกอบด้วยแบบจำลองข้อมูลตัวอย่างสำหรับเช็คการชำระเงิน และการแม็ปของข้อมูลไปยังองค์ประกอบข้อมูลของแอพลิเคชัน Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="1211b-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="1211b-118">บน FastTab ของเวอร์ชัน คลิก แลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="1211b-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="1211b-119">คลิก โหลดจากไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="1211b-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="1211b-120">คลิก เรียกดู และจากนั้นเลือกแบบจำลองสำหรับ cheques.xml</span><span class="sxs-lookup"><span data-stu-id="1211b-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="1211b-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="1211b-121">Click OK.</span></span>  
 6. <span data-ttu-id="1211b-122">แบบจำลองที่โหลดจะใช้เป็นแหล่งข้อมูลของข้อมูลในการสร้างเอกสารที่ประกอบด้วยรูปภาพใน Excel และ Word</span><span class="sxs-lookup"><span data-stu-id="1211b-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="1211b-123">เพิ่มการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="1211b-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="1211b-124">แทนที่จะสร้างรูปแบบใหม่ คุณสามารถโหลดไฟล์โครงแบบรูปแบบ ER ได้ (รูปแบบการพิมพ์เช็ค.xml) ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="1211b-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="1211b-125">ไฟล์นี้ประกอบด้วยโครงร่างตัวอย่างของรูปแบบที่จะพิมพ์เช็ค โดยใช้ฟอร์มที่พิมพ์ล่วงหน้าและการแม็ปรูปแบบนี้ไปยังแบบจำลองข้อมูล 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="1211b-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="1211b-126">คลิก แลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="1211b-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="1211b-127">คลิก โหลดจากไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="1211b-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="1211b-128">คลิก เรียกดู และเลือก ไฟล์รูปแบบการพิมพ์เช็ค.xml</span><span class="sxs-lookup"><span data-stu-id="1211b-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="1211b-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="1211b-129">Click OK.</span></span>  
 6. <span data-ttu-id="1211b-130">ในแผนภูมิ ขยาย 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="1211b-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="1211b-131">ในแผนภูมิ เลือก 'แบบจำลองสำหรับเช็ค\รูปแบบการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="1211b-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="1211b-132">รูปแบบที่โหลดจะใช้เพื่อสร้างเอกสารที่ประกอบด้วยรูปภาพใน Excel และ Word</span><span class="sxs-lookup"><span data-stu-id="1211b-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="1211b-133">ตั้งค่าคอนฟิกพารามิเตอร์ผู้ใช้ ER</span><span class="sxs-lookup"><span data-stu-id="1211b-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="1211b-134">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="1211b-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="1211b-135">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="1211b-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="1211b-136">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="1211b-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="1211b-137">เปิดใช้งานแฟล็ก 'รันฉบับร่าง' เพื่อเริ่มต้นรุ่นแบบร่างของรูปแบบที่เลือก แทนที่รุ่นที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1211b-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="1211b-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="1211b-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="1211b-139">ตั้งค่าคอนฟิกเงินสด & พารามิเตอร์การจัดการธนาคาร</span><span class="sxs-lookup"><span data-stu-id="1211b-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="1211b-140">ไปที่ การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="1211b-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="1211b-141">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'USMF OPER'</span><span class="sxs-lookup"><span data-stu-id="1211b-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="1211b-142">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="1211b-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="1211b-143">คลิกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="1211b-143">Click Check.</span></span>  
 5. <span data-ttu-id="1211b-144">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="1211b-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="1211b-145">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="1211b-145">Click Edit.</span></span>  
 7. <span data-ttu-id="1211b-146">เลือก ใช่ ในฟิลด์โลโก้ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="1211b-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="1211b-147">คลิกโลโก้ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="1211b-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="1211b-148">คลิกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1211b-148">Click Change.</span></span>  
 10. <span data-ttu-id="1211b-149">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ โลโก้บริษัท.png</span><span class="sxs-lookup"><span data-stu-id="1211b-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="1211b-150">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="1211b-150">Click Save.</span></span>  
 12. <span data-ttu-id="1211b-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1211b-151">Close the page.</span></span>  
 13. <span data-ttu-id="1211b-152">ขยายส่วนลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="1211b-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="1211b-153">เลือก ใช่ ในฟิลด์พิมพ์ลายเซ็นแรก</span><span class="sxs-lookup"><span data-stu-id="1211b-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="1211b-154">คลิกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1211b-154">Click Change.</span></span>  
 16. <span data-ttu-id="1211b-155">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ รูปภาพลายเซ็น.png</span><span class="sxs-lookup"><span data-stu-id="1211b-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="1211b-156">ขยายส่วนสำเนา</span><span class="sxs-lookup"><span data-stu-id="1211b-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="1211b-157">ในฟิลด์ลายน้ำ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1211b-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="1211b-158">เลือก ใช่ ในรูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="1211b-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="1211b-159">เลือกการตั้งค่าคอนฟิก 'แบบฟอร์มในการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="1211b-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="1211b-160">ขณะนี้ รูปแบบ ER ที่เลือกจะใช้สำหรับการพิมพ์เช็ค</span><span class="sxs-lookup"><span data-stu-id="1211b-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="1211b-161">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="1211b-161">Click Attach.</span></span>  
 23. <span data-ttu-id="1211b-162">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1211b-162">Click New.</span></span>  
 24. <span data-ttu-id="1211b-163">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="1211b-163">Click File.</span></span>  
 25. <span data-ttu-id="1211b-164">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ รูปภาพลายเซ็น 2.png</span><span class="sxs-lookup"><span data-stu-id="1211b-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="1211b-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1211b-165">Close the page.</span></span>  
 27. <span data-ttu-id="1211b-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1211b-166">Close the page.</span></span>  
 28. <span data-ttu-id="1211b-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1211b-167">Close the page.</span></span>  
 29. <span data-ttu-id="1211b-168">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > พารามิเตอร์การจัดการเงินสดและธนาคาร</span><span class="sxs-lookup"><span data-stu-id="1211b-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="1211b-169">เลือก ใช่ ในฟิลด์ อนุญาตให้สร้างบันทึกย่อในบัญชีธนาคารที่ไม่ได้ใช้งานอยู่:</span><span class="sxs-lookup"><span data-stu-id="1211b-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="1211b-170">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="1211b-170">Click Save.</span></span>  
 32. <span data-ttu-id="1211b-171">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1211b-171">Close the page.</span></span>  
