---
title: ปรับเปลี่ยนรูปแบบโดยนำเท็มเพลต Excel มาใช้อีกครั้ง
description: เพื่อทำขั้นตอนในกระบวนงานนี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำดำเนินกระบวนงานให้เสร็จสมบูรณ์ ER - ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "327124"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="a8603-103">ปรับเปลี่ยนรูปแบบโดยนำเท็มเพลต Excel มาใช้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a8603-103">Modify formats by reapplying Excel templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8603-104">เพื่อทำขั้นตอนในกระบวนงานนี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำดำเนินกระบวนงานให้เสร็จสมบูรณ์ ER - ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="a8603-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="a8603-105">กระบวนงานนี้อธิบายวิธีการปรับเปลี่ยนการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) โดยการนำเท็มเพลต Microsoft Excel ที่ได้ถูกปรับเปลี่ยนไปใช้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a8603-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="a8603-106">ในกระบวนงานนี้ คุณจะนำเข้าเท็มเพลต Excel ที่แก้ไขแล้วไปยังการตั้งค่าคอนฟิกรูปแบบ ER ที่สร้างขึ้นสำหรับบริษัทตัวอย่าง Litware, Inc. และจากนั้นสร้างเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a8603-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="a8603-107">กระบวนงานนี้มีไว้สำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a8603-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="a8603-108">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล GBSI</span><span class="sxs-lookup"><span data-stu-id="a8603-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="a8603-109">ก่อนที่คุณจะเริ่มต้น ให้ดาวน์โหลดและบันทึกไฟล์ SampleVendPaymWsReport2.xlsx ซึ่งแสดงรายการอยู่ในหัวข้อวิธีใช้ แก้ไขรูปแบบการรายงานทางอิเล็กทรอนิกส์โดยใช้เท็มเพลต Excel (modify-electronic-reporting-format-reapply-excel-template/)</span><span class="sxs-lookup"><span data-stu-id="a8603-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="a8603-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a8603-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="a8603-111">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="a8603-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="a8603-112">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="a8603-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="a8603-113">เลือกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a8603-113">Select the ER format</span></span>
1. <span data-ttu-id="a8603-114">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="a8603-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="a8603-115">ในแผนภูมิ ขยาย 'รูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="a8603-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="a8603-116">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน\รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="a8603-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="a8603-117">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="a8603-117">Click Attachments.</span></span>
    * <span data-ttu-id="a8603-118">หมายเหตุว่าในขณะนี้ไฟล์ Excel SampleVendPaymWsReport.xlsx ถูกใช้เป็นเท็มเพลตสำหรับการประมวลผลสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a8603-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="a8603-119">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="a8603-119">Click Open.</span></span>
    * <span data-ttu-id="a8603-120">คลิก เปิดเพื่อสำรวจโครงร่างของเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="a8603-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="a8603-121">ตรวจทานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a8603-121">Review the template.</span></span> <span data-ttu-id="a8603-122">หมายเหตุว่าในขณะนี้มีรายละเอียดดังต่อไปนี้สำหรับแต่ละบรรทัดการชำระเงิน: หมายเลขบัญชีผู้จัดจำหน่าย ชื่อผู้จัดจำหน่าย ธนาคาร หมายเลขเส้นทาง หมายเลขบัญชี เดบิต เครดิต และสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="a8603-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="a8603-123">ในตัวอย่างนี้ เราต้องการขยายรายการนี้โดยการเพิ่มรายละเอียดเกี่ยวกับวันที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a8603-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="a8603-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a8603-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="a8603-125">ใช้เท็มเพลต Excel ใหม่กับรูปแบบ ER อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a8603-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="a8603-126">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="a8603-126">Click Designer.</span></span>
    * <span data-ttu-id="a8603-127">เปิดเวอร์ชันแบบร่างของรูปแบบ ER ที่เลือกเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a8603-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="a8603-128">ในบานหน้าต่างการดำเนินการ คลิกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="a8603-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="a8603-129">คลิก อัพเดตจาก Excel</span><span class="sxs-lookup"><span data-stu-id="a8603-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="a8603-130">คลิก 'ปรับปรุงเท็มเพลต' และจากนั้นเลือกไฟล์ SampleVendPaymWsReport2.xlsx</span><span class="sxs-lookup"><span data-stu-id="a8603-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="a8603-131">คลิก อัพเดตเท็มเพลต และเรียกดูเพื่อเรียกใช้ไฟล์ SampleVendPaymWsReport2.xlsx ที่ดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a8603-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="a8603-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a8603-132">Click OK.</span></span>
    * <span data-ttu-id="a8603-133">ใช้เท็มเพลต SampleVendPaymWsReport2.xlsx</span><span class="sxs-lookup"><span data-stu-id="a8603-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="a8603-134">โครงสร้างของรูปแบบ ER จะถูกซิงโครไนส์กับเนื้อหาของเท็มเพลตที่มีการเพิ่มองค์ประกอบไปยังรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="a8603-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="a8603-135">องค์ประกอบใด ๆ ที่มีอยู่ในรูปแบบ ER ที่ไม่รวมอยู่ในเท็มเพลตจะถูกเอาออกจากข้อกำหนดของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="a8603-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="a8603-136">ในแผนภูมิ ให้เลือก 'Excel'</span><span class="sxs-lookup"><span data-stu-id="a8603-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="a8603-137">หมายเหตุว่าในขณะนี้ฟิลเท็มเพลตประกอบด้วยการอ้างอิงไปยังเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="a8603-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="a8603-138">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="a8603-138">Click Attachments.</span></span>
7. <span data-ttu-id="a8603-139">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="a8603-139">Click Open.</span></span>
    * <span data-ttu-id="a8603-140">คลิก เปิดเพื่อสำรวจโครงร่างของเท็มเพลต Excel ที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="a8603-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="a8603-141">ตรวจทานเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a8603-141">Review the template.</span></span> <span data-ttu-id="a8603-142">หมายเหตุว่าในขณะนี้จะประกอบด้วยบรรทัดสำหรับวันที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a8603-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="a8603-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a8603-143">Close the page.</span></span>
9. <span data-ttu-id="a8603-144">ในแผนภูมิ ให้ขยาย 'Excel'</span><span class="sxs-lookup"><span data-stu-id="a8603-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="a8603-145">ในแผนภูมิ ขยาย 'Excel\รายการการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="a8603-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="a8603-146">ในแผนภูมิ ให้เลือก ''Excel\PaymLines\PaymDate'</span><span class="sxs-lookup"><span data-stu-id="a8603-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="a8603-147">หมายเหตุว่าในขณะนี้รูปแบบ ER ประกอบด้วยรายการมากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="a8603-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="a8603-148">มีการเพิ่มเซลล์ PaymDate ไปยังเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="a8603-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="a8603-149">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="a8603-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="a8603-150">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="a8603-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="a8603-151">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="a8603-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="a8603-152">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\วันที่ธุรกรรม(วันที่ธุรกรรม)'</span><span class="sxs-lookup"><span data-stu-id="a8603-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="a8603-153">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="a8603-153">Click Bind.</span></span>
    * <span data-ttu-id="a8603-154">ระบุว่าข้อมูลใดจะถูกเพิ่มไปยังเซลล์ใหม่ขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a8603-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="a8603-155">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="a8603-155">Click Save.</span></span>
18. <span data-ttu-id="a8603-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a8603-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="a8603-157">เปิดใช้งานเวอร์ชันแบบร่างที่แก้ไขแล้วของรูปแบบ ER สำหรับใช้ในการประมวลผลสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a8603-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="a8603-158">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a8603-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="a8603-159">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a8603-159">Click User parameters.</span></span>
3. <span data-ttu-id="a8603-160">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="a8603-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="a8603-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a8603-161">Click OK.</span></span>
5. <span data-ttu-id="a8603-162">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="a8603-162">Click Edit.</span></span>
6. <span data-ttu-id="a8603-163">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="a8603-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="a8603-164">ใช้เวอร์ชันแบบร่างที่แก้ไขแล้วของรูปแบบ ER สำหรับการประมวลผลสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a8603-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="a8603-165">ตรวจทานแผ่นงานที่สร้างขึ้น รวมทั้งรายละเอียดใหม่ของบรรทัดการชำระเงิน – วันที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a8603-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  

