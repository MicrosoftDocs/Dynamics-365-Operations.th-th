---
title: สร้างรายงานในรูปแบบ Office ที่ได้ฝังรูปภาพ
description: ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ที่มีบทบาท ‘ผู้ดูแลระบบ‘ หรือ ‘นักพัฒนาการรายงานทางอิเล็กทรอนิกส์’ สามารถออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ MS office (Excel และ Word) ที่มีรูปภาพที่ฝัง
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 78dcdbd83dc717104d437662f7f451c9ecb714cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684391"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="f070e-103">สร้างรายงานในรูปแบบ Office ที่ได้ฝังรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="f070e-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f070e-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ที่มีบทบาท ‘ผู้ดูแลระบบ‘ หรือ ‘นักพัฒนาการรายงานทางอิเล็กทรอนิกส์’ สามารถออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ MS office (Excel และ Word) ที่มีรูปภาพที่ฝัง</span><span class="sxs-lookup"><span data-stu-id="f070e-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="f070e-105">ในตัวอย่างนี้ คุณจะใช้การตั้งค่าคอนฟิก ER ที่สร้างขึ้นสำหรับบริษัทตัวอย่าง 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="f070e-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="f070e-106">เมื่อต้องการทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำตามขั้นตอนในคู่มืองาน "ER ทำรายงานในรูปแบบ MS Office ที่มีรูปภาพที่ฝัง (ส่วนที่ 2: ตรวจทานการตั้งค่าคอนฟิก)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f070e-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="f070e-107">ขั้นตอนเหล่านี้สามารถดำเนินการได้ในบริษัท ‘USMF‘</span><span class="sxs-lookup"><span data-stu-id="f070e-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="f070e-108">เรียกใช้รูปแบบที่มีการแม็ปแบบจำลองเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f070e-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="f070e-109">ไปที่ การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f070e-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="f070e-110">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'USMF OPER'</span><span class="sxs-lookup"><span data-stu-id="f070e-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="f070e-111">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="f070e-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="f070e-112">คลิกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-112">Click Check.</span></span>
5. <span data-ttu-id="f070e-113">คลิก พิมพ์การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-113">Click Print test.</span></span>
    * <span data-ttu-id="f070e-114">เรียกใช้รูปแบบสำหรับวัตถุประสงค์ในการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="f070e-115">เลือก ใช่ ในฟิลด์รูปแบบเช็คที่เปลี่ยนมือได้</span><span class="sxs-lookup"><span data-stu-id="f070e-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="f070e-116">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="f070e-116">Click OK.</span></span>
    * <span data-ttu-id="f070e-117">ตรวจทานผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f070e-117">Review the created output.</span></span> <span data-ttu-id="f070e-118">โลโก้บริษัทจะแสดงขึ้นในรายงาน เช่นเดียวกับลายเซ็นของบุคคลที่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="f070e-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="f070e-119">รูปภาพลายเซ็นจะได้มาจากฟิลด์ของชนิดข้อมูล 'คอนเทนเนอร์' ของเรกคอร์ดโครงร่างเช็คที่เชื่อมโยงกับบัญชีธนาคารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f070e-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="f070e-120">ขยายส่วนสำเนา</span><span class="sxs-lookup"><span data-stu-id="f070e-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="f070e-121">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f070e-121">Click Edit.</span></span>
10. <span data-ttu-id="f070e-122">ในฟิลด์ลายน้ำ ป้อน 'พิมพ์ลายน้ำเป็นโมฆะ'</span><span class="sxs-lookup"><span data-stu-id="f070e-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="f070e-123">เปลี่ยนการตั้งค่าโครงร่างลายน้ำเพื่อแสดงข้อความลายน้ำในการสร้างเอกสารในองค์ประกอบรูปร่าง Excel</span><span class="sxs-lookup"><span data-stu-id="f070e-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="f070e-124">คลิก พิมพ์การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-124">Click Print test.</span></span>
12. <span data-ttu-id="f070e-125">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="f070e-125">Click OK.</span></span>
    * <span data-ttu-id="f070e-126">ตรวจทานผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f070e-126">Review the created output.</span></span> <span data-ttu-id="f070e-127">ลายน้ำจะแสดงขึ้นในรายงานที่สร้างขึ้นตามตัวเลือกการเลือก</span><span class="sxs-lookup"><span data-stu-id="f070e-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="f070e-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-128">Close the page.</span></span>
14. <span data-ttu-id="f070e-129">ในบานหน้าต่างการดำเนินการ คลิกจัดการการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f070e-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="f070e-130">คลิก เช็ค</span><span class="sxs-lookup"><span data-stu-id="f070e-130">Click Checks.</span></span>
16. <span data-ttu-id="f070e-131">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="f070e-131">Click Show filters.</span></span>
17. <span data-ttu-id="f070e-132">ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรอง "381","385","389" ในฟิลด์ "หมายเลขเช็ค" โดยใช้ตัวดำเนินการตัวกรอง "เป็นหนึ่งใน"</span><span class="sxs-lookup"><span data-stu-id="f070e-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="f070e-133">ในรายการนี้ ให้สลับไปใช้ 'ทำเครื่องหมายทุกแถว'</span><span class="sxs-lookup"><span data-stu-id="f070e-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="f070e-134">คลิก พิมพ์สำเนาเช็ค</span><span class="sxs-lookup"><span data-stu-id="f070e-134">Click Print check copy.</span></span>
    * <span data-ttu-id="f070e-135">เรียกใช้รูปแบบเพื่อพิมพ์เช็คที่เลือกใหม่</span><span class="sxs-lookup"><span data-stu-id="f070e-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="f070e-136">ตรวจทานผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f070e-136">Review the created output.</span></span> <span data-ttu-id="f070e-137">เช็คที่เลือกได้ถูกพิมพ์ใหม่แล้ว</span><span class="sxs-lookup"><span data-stu-id="f070e-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="f070e-138">โลโก้บริษัทและป้ายชื่อจะไม่ถูกพิมพ์ออกมาเนื่องจากจะถูกแสดงบนแบบฟอร์มที่พิมพ์ไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="f070e-139">ปรับเปลี่ยนการแม็ปของแบบจำลองข้อมูลที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="f070e-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="f070e-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-140">Close the page.</span></span>
2. <span data-ttu-id="f070e-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-141">Close the page.</span></span>
3. <span data-ttu-id="f070e-142">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f070e-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="f070e-143">ในแผนภูมิ ให้เลือก 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="f070e-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="f070e-144">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f070e-144">Click Designer.</span></span>
6. <span data-ttu-id="f070e-145">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f070e-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="f070e-146">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f070e-146">Click Designer.</span></span>
    * <span data-ttu-id="f070e-147">เราจะเปลี่ยนแปลงการผูกข้อมูลของรายการลายเซ็นของแบบจำลองข้อมูล เพื่อรับรูปภาพลายเซ็นจากไฟล์ที่แนบกับเรกคอร์ดโครงร่างเช็คที่เชื่อมโยงกับบัญชีธนาคารที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="f070e-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="f070e-148">ปิดการแสดงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="f070e-148">Turn off Show details.</span></span>
9. <span data-ttu-id="f070e-149">ในแผนภูมิ ขยาย 'โครงร่าง'</span><span class="sxs-lookup"><span data-stu-id="f070e-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="f070e-150">ในแผนภูมิ ขยาย 'โครงร่าง\ลายเซ็น'</span><span class="sxs-lookup"><span data-stu-id="f070e-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="f070e-151">ในแผนภูมิ เลือก 'โครงร่าง\ลายเซ็น\รูปภาพ = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'</span><span class="sxs-lookup"><span data-stu-id="f070e-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="f070e-152">ในแผนภูมิ ขยาย 'chequesaccount'</span><span class="sxs-lookup"><span data-stu-id="f070e-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="f070e-153">ในแผนภูมิ ขยาย 'chequesaccount\<Relations'</span><span class="sxs-lookup"><span data-stu-id="f070e-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="f070e-154">ในแผนภูมิ ขยาย 'chequesaccount\<Relations\BankChequeLayout'</span><span class="sxs-lookup"><span data-stu-id="f070e-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="f070e-155">ในแผนภูมิ ขยาย 'chequesaccount\<Relations\BankChequeLayout\<Relations'</span><span class="sxs-lookup"><span data-stu-id="f070e-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="f070e-156">ในแผนภูมิ ขยาย 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'</span><span class="sxs-lookup"><span data-stu-id="f070e-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="f070e-157">ในแผนภูมิ เลือก 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="f070e-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="f070e-158">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f070e-158">Click Bind.</span></span>
19. <span data-ttu-id="f070e-159">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f070e-159">Click Save.</span></span>
20. <span data-ttu-id="f070e-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-160">Close the page.</span></span>
21. <span data-ttu-id="f070e-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-161">Close the page.</span></span>
22. <span data-ttu-id="f070e-162">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-162">Close the page.</span></span>
23. <span data-ttu-id="f070e-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="f070e-164">รันรูปแบบโดยใช้การแม็ปแบบจำลองที่ปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="f070e-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="f070e-165">ไปที่ การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f070e-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="f070e-166">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="f070e-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f070e-167">เช่น กรองข้อมูลในฟิลด์บัญชีธนาคาร ด้วยค่า 'USMF OPER'</span><span class="sxs-lookup"><span data-stu-id="f070e-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="f070e-168">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="f070e-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="f070e-169">คลิกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-169">Click Check.</span></span>
5. <span data-ttu-id="f070e-170">คลิก พิมพ์การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-170">Click Print test.</span></span>
6. <span data-ttu-id="f070e-171">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="f070e-171">Click OK.</span></span>
    * <span data-ttu-id="f070e-172">ตรวจทานผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f070e-172">Review the created output.</span></span> <span data-ttu-id="f070e-173">รูปภาพจากเอกสารแนบการจัดการจะแสดงเป็นลายเซ็นของบุคคลที่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="f070e-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="f070e-174">ใช้เอกสาร MS Word เป็นเท็มเพลตในรูปแบบที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="f070e-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="f070e-175">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-175">Close the page.</span></span>
2. <span data-ttu-id="f070e-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-176">Close the page.</span></span>
3. <span data-ttu-id="f070e-177">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f070e-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="f070e-178">ในแผนภูมิ ขยาย 'แบบจำลองสำหรับเช็ค'</span><span class="sxs-lookup"><span data-stu-id="f070e-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="f070e-179">ในแผนภูมิ เลือก 'แบบจำลองสำหรับเช็ค\รูปแบบการพิมพ์เช็ค'</span><span class="sxs-lookup"><span data-stu-id="f070e-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="f070e-180">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f070e-180">Click Designer.</span></span>
7. <span data-ttu-id="f070e-181">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="f070e-181">Click Attachments.</span></span>
8. <span data-ttu-id="f070e-182">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="f070e-182">Click Delete.</span></span>
9. <span data-ttu-id="f070e-183">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="f070e-183">Click Yes.</span></span>
10. <span data-ttu-id="f070e-184">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f070e-184">Click New.</span></span>
11. <span data-ttu-id="f070e-185">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="f070e-185">Click File.</span></span>
    * <span data-ttu-id="f070e-186">คลิกเรียกดู และเลือกรายการที่ดาวน์โหลดไว้ในไฟล์ 'Cheque template Word.docx' ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="f070e-187">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-187">Close the page.</span></span>
13. <span data-ttu-id="f070e-188">ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f070e-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="f070e-189">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f070e-189">Click Save.</span></span>
15. <span data-ttu-id="f070e-190">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-190">Close the page.</span></span>
16. <span data-ttu-id="f070e-191">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f070e-191">Click Edit.</span></span>
17. <span data-ttu-id="f070e-192">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="f070e-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="f070e-193">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f070e-193">Close the page.</span></span>
19. <span data-ttu-id="f070e-194">ไปที่ การจัดการเงินสดและธนาคาร > บัญชีธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f070e-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="f070e-195">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'USMF OPER'</span><span class="sxs-lookup"><span data-stu-id="f070e-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="f070e-196">คลิกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-196">Click Check.</span></span>
22. <span data-ttu-id="f070e-197">คลิก พิมพ์การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f070e-197">Click Print test.</span></span>
23. <span data-ttu-id="f070e-198">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="f070e-198">Click OK.</span></span>
    * <span data-ttu-id="f070e-199">ตรวจทานผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f070e-199">Review the created output.</span></span> <span data-ttu-id="f070e-200">ผลลัพธ์ได้ถูกสร้างขึ้นโดยเป็นเอกสาร Word ด้วยรูปภาพแบบฝังที่นำเสนอโลโก้บริษัท ลายเซ็นของบุคคลที่ได้รับอนุญาตและข้อความลายน้ำที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f070e-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

