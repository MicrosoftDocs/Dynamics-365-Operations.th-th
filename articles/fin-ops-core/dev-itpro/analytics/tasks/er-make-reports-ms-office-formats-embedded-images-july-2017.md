---
title: ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Office ที่มีรูปภาพที่ฝัง
description: หัวข้อนี้อธิบายเกี่ยวกับวิธีการออกแบบการตั้งค่าคอนฟิกที่สร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ Excel และ Word ที่ประกอบด้วยภาพที่ฝัง
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944568"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="9ce82-103">ออกแบบการตั้งค่าคอนฟิกเพื่อสร้างรายงานในรูปแบบ Office ที่มีรูปภาพที่ฝัง</span><span class="sxs-lookup"><span data-stu-id="9ce82-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ce82-104">เพื่อทำตามขั้นตอนในกระบวนงานนี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำกระบวนงาน “ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่”</span><span class="sxs-lookup"><span data-stu-id="9ce82-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="9ce82-105">กระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสาร Microsoft Excel หรือ Word ที่ประกอบด้วยภาพที่ฝัง</span><span class="sxs-lookup"><span data-stu-id="9ce82-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="9ce82-106">ในกระบวนงานนี้ คุณจะสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นสำหรับบริษัทตัวอย่าง Litware, inc สามารถดำเนินขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล USMF</span><span class="sxs-lookup"><span data-stu-id="9ce82-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="9ce82-107">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="9ce82-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="9ce82-108">ก่อนที่คุณจะเริ่มต้น ต้องดาวน์โหลดและบันทึกไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9ce82-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="9ce82-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9ce82-109">Description</span></span>                                          | <span data-ttu-id="9ce82-110">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="9ce82-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="9ce82-111">การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER</span><span class="sxs-lookup"><span data-stu-id="9ce82-111">ER data model configuration</span></span>                          | [<span data-ttu-id="9ce82-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="9ce82-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="9ce82-113">การตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="9ce82-113">ER format configuration</span></span>                              | [<span data-ttu-id="9ce82-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="9ce82-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="9ce82-115">รูปโลโก้บริษัท</span><span class="sxs-lookup"><span data-stu-id="9ce82-115">Company logo image</span></span>                                   | [<span data-ttu-id="9ce82-116">Company logo.png</span><span class="sxs-lookup"><span data-stu-id="9ce82-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="9ce82-117">รูปภาพลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="9ce82-117">Signature image</span></span>                                      | [<span data-ttu-id="9ce82-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="9ce82-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="9ce82-119">รูปภาพลายเซ็นอื่น</span><span class="sxs-lookup"><span data-stu-id="9ce82-119">Alternative signature image</span></span>                          | [<span data-ttu-id="9ce82-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="9ce82-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="9ce82-121">เท็มเพลต Microsoft Word สำหรับการพิมพ์เช็คการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9ce82-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="9ce82-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="9ce82-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="9ce82-123">ตรวจสอบข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9ce82-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="9ce82-124">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="9ce82-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="9ce82-125">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="9ce82-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="9ce82-126">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9ce82-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="9ce82-127">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="9ce82-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="9ce82-128">เพิ่มการตั้งค่าคอนฟิกแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="9ce82-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="9ce82-129">แทนที่จะสร้างแบบจำลองใหม่ คุณสามารถโหลดไฟล์โครงแบบแบบจำลอง ER ได้ (แบบจำลองสำหรับเช็ค.xml) ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9ce82-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="9ce82-130">ไฟล์นี้ประกอบด้วยแบบจำลองข้อมูลตัวอย่างสำหรับเช็คการชำระเงิน และการแม็ปของข้อมูลไปยังองค์ประกอบข้อมูลของแอพลิเคชัน Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="9ce82-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="9ce82-131">บน FastTab ของเวอร์ชัน คลิก แลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="9ce82-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="9ce82-132">คลิก โหลดจากไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="9ce82-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="9ce82-133">คลิก เรียกดู และจากนั้นเลือกแบบจำลองสำหรับ cheques.xml</span><span class="sxs-lookup"><span data-stu-id="9ce82-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="9ce82-134">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9ce82-134">Click OK.</span></span>  
 6. <span data-ttu-id="9ce82-135">แบบจำลองที่โหลดจะใช้เป็นแหล่งข้อมูลของข้อมูลในการสร้างเอกสารที่ประกอบด้วยรูปภาพใน Excel และ Word</span><span class="sxs-lookup"><span data-stu-id="9ce82-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="9ce82-136">เพิ่มการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="9ce82-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="9ce82-137">แทนที่จะสร้างรูปแบบใหม่ คุณสามารถโหลดไฟล์โครงแบบรูปแบบ ER ได้ (รูปแบบการพิมพ์เช็ค.xml) ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9ce82-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="9ce82-138">ไฟล์นี้ประกอบด้วยโครงร่างตัวอย่างของรูปแบบที่จะพิมพ์เช็ค โดยใช้ฟอร์มที่พิมพ์ล่วงหน้าและการแม็ปรูปแบบนี้ไปยังแบบจำลองข้อมูล 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="9ce82-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="9ce82-139">คลิก แลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="9ce82-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="9ce82-140">คลิก โหลดจากไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="9ce82-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="9ce82-141">คลิก เรียกดู และเลือก ไฟล์รูปแบบการพิมพ์เช็ค.xml</span><span class="sxs-lookup"><span data-stu-id="9ce82-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="9ce82-142">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9ce82-142">Click OK.</span></span>  
 6. <span data-ttu-id="9ce82-143">ในแผนภูมิ ขยาย 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="9ce82-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="9ce82-144">ในแผนภูมิ เลือก 'แบบจำลองสำหรับเช็ค\รูปแบบการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="9ce82-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="9ce82-145">รูปแบบที่โหลดจะใช้เพื่อสร้างเอกสารที่ประกอบด้วยรูปภาพใน Excel และ Word</span><span class="sxs-lookup"><span data-stu-id="9ce82-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="9ce82-146">ตั้งค่าคอนฟิกพารามิเตอร์ผู้ใช้ ER</span><span class="sxs-lookup"><span data-stu-id="9ce82-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="9ce82-147">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="9ce82-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="9ce82-148">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9ce82-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="9ce82-149">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9ce82-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="9ce82-150">เปิดใช้งานแฟล็ก 'รันฉบับร่าง' เพื่อเริ่มต้นรุ่นแบบร่างของรูปแบบที่เลือก แทนที่รุ่นที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9ce82-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="9ce82-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9ce82-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="9ce82-152">ตั้งค่าคอนฟิกเงินสด & พารามิเตอร์การจัดการธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9ce82-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="9ce82-153">ไปที่ การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9ce82-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="9ce82-154">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'USMF OPER'</span><span class="sxs-lookup"><span data-stu-id="9ce82-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="9ce82-155">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9ce82-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="9ce82-156">คลิกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9ce82-156">Click Check.</span></span>  
 5. <span data-ttu-id="9ce82-157">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9ce82-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="9ce82-158">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="9ce82-158">Click Edit.</span></span>  
 7. <span data-ttu-id="9ce82-159">เลือก ใช่ ในฟิลด์โลโก้ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="9ce82-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="9ce82-160">คลิกโลโก้ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="9ce82-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="9ce82-161">คลิกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="9ce82-161">Click Change.</span></span>  
 10. <span data-ttu-id="9ce82-162">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ โลโก้บริษัท.png</span><span class="sxs-lookup"><span data-stu-id="9ce82-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="9ce82-163">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9ce82-163">Click Save.</span></span>  
 12. <span data-ttu-id="9ce82-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9ce82-164">Close the page.</span></span>  
 13. <span data-ttu-id="9ce82-165">ขยายส่วนลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="9ce82-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="9ce82-166">เลือก ใช่ ในฟิลด์พิมพ์ลายเซ็นแรก</span><span class="sxs-lookup"><span data-stu-id="9ce82-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="9ce82-167">คลิกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="9ce82-167">Click Change.</span></span>  
 16. <span data-ttu-id="9ce82-168">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ รูปภาพลายเซ็น.png</span><span class="sxs-lookup"><span data-stu-id="9ce82-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="9ce82-169">ขยายส่วนสำเนา</span><span class="sxs-lookup"><span data-stu-id="9ce82-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="9ce82-170">ในฟิลด์ลายน้ำ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="9ce82-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="9ce82-171">เลือก ใช่ ในรูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="9ce82-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="9ce82-172">เลือกการตั้งค่าคอนฟิก 'แบบฟอร์มในการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="9ce82-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="9ce82-173">ขณะนี้ รูปแบบ ER ที่เลือกจะใช้สำหรับการพิมพ์เช็ค</span><span class="sxs-lookup"><span data-stu-id="9ce82-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="9ce82-174">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="9ce82-174">Click Attach.</span></span>  
 23. <span data-ttu-id="9ce82-175">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9ce82-175">Click New.</span></span>  
 24. <span data-ttu-id="9ce82-176">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="9ce82-176">Click File.</span></span>  
 25. <span data-ttu-id="9ce82-177">คลิกเรียกดู และเลือกไฟล์ที่คุณดาวน์โหลดมาก่อนหน้านี้ ซึ่งคือ รูปภาพลายเซ็น 2.png</span><span class="sxs-lookup"><span data-stu-id="9ce82-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="9ce82-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9ce82-178">Close the page.</span></span>  
 27. <span data-ttu-id="9ce82-179">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9ce82-179">Close the page.</span></span>  
 28. <span data-ttu-id="9ce82-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9ce82-180">Close the page.</span></span>  
 29. <span data-ttu-id="9ce82-181">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > พารามิเตอร์การจัดการเงินสดและธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9ce82-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="9ce82-182">เลือก ใช่ ในฟิลด์ อนุญาตให้สร้างบันทึกย่อในบัญชีธนาคารที่ไม่ได้ใช้งานอยู่:</span><span class="sxs-lookup"><span data-stu-id="9ce82-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="9ce82-183">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9ce82-183">Click Save.</span></span>  
 32. <span data-ttu-id="9ce82-184">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9ce82-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
