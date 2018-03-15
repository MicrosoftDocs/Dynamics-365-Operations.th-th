--- 
title: "ออกแบบนิพจน์เพื่อเรียกวิธีการคลาสแอพลิเคชัน (ER)"
description: "คู่มือนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ซ้ำตรรกะแอพลิเคชันที่มีอยู่ในการตั้งค่าคอนฟิกการรายงานอิเล็กทรอนิกส์ (ER) โดยการเรียกใช้วิธีที่ต้องการของคลาสแอพลิเคชันในนิพจน์ ER"
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: b0a1dba5afbd7beba45149340f637223f6ecedcf
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---
# <a name="design-expressions-to-call-application-class-methods-er"></a><span data-ttu-id="c68e4-103">ออกแบบนิพจน์เพื่อเรียกวิธีการคลาสแอพลิเคชัน (ER)</span><span class="sxs-lookup"><span data-stu-id="c68e4-103">Design expressions to call application class methods (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c68e4-104">คู่มือนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ซ้ำตรรกะแอพลิเคชันที่มีอยู่ในการตั้งค่าคอนฟิกการรายงานอิเล็กทรอนิกส์ (ER) โดยการเรียกใช้วิธีที่ต้องการของคลาสแอพลิเคชันในนิพจน์ ER</span><span class="sxs-lookup"><span data-stu-id="c68e4-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="c68e4-105">ค่าของอาร์กิวเมนต์สำหรับการเรียกคลาสที่สามารถถูกกำหนดแบบไดนามิกได้ในขณะทำงาน: ตัวอย่างเช่น ตามข้อมูลในเอกสารแยกวิเคราะห์เพื่อให้มั่นใจถึงความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c68e4-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="c68e4-106">ในคู่มือนี้ คุณจะสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นสำหรับบริษัทตัวอย่าง Litware, inc กระบวนงานนี้จะถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทของผู้ดูแลระบบหรือนักพัฒนารายงานทางอิเล็กทรอนิกส์ที่ได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="c68e4-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="c68e4-107">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="c68e4-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="c68e4-108">นอกจากนี้ คุณต้องดาวน์โหลดและบันทึกไฟล์ต่อไปนี้ไว้ภายในเครื่อง: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt</span><span class="sxs-lookup"><span data-stu-id="c68e4-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="c68e4-109">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงานให้เสร็จสมบูรณ์ "ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="c68e4-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="c68e4-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="c68e4-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c68e4-111">ตรวจสอบว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง 'Litware, Inc.' พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="c68e4-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="c68e4-112">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ในกระบวนงานให้สำเร็จ "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="c68e4-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="c68e4-113">สมมติว่า คุณกำลังออกแบบกระบวนการสำหรับการแยกวิเคราะห์ใบแจ้งยอดจากธนาคารขาเข้าสำหรับการปรับปรุงข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c68e4-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="c68e4-114">คุณจะได้รับใบแจ้งยอดจากธนาคารขาเข้าเป็นไฟล์ TXT ที่ประกอบด้วยรหัส IBAN</span><span class="sxs-lookup"><span data-stu-id="c68e4-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="c68e4-115">เนื่องจากเป็นส่วนหนึ่งของกระบวนการนำเข้าใบแจ้งยอดจากธนาคาร คุณต้องตรวจสอบความถูกต้องของรหัส IBAN นี้โดยใช้ตรรกะที่พร้อมใช้งานอยู่แล้วใน Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="c68e4-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="c68e4-116">นำเข้าการตั้งค่าคอนฟิกแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="c68e4-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="c68e4-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c68e4-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c68e4-118">เลือกไทล์ผู้ให้บริการของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="c68e4-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="c68e4-119">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="c68e4-119">Click Repositories.</span></span>
3. <span data-ttu-id="c68e4-120">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="c68e4-120">Click Show filters.</span></span>
4. <span data-ttu-id="c68e4-121">เพิ่มฟิลด์ตัวกรอง 'พิมพ์ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="c68e4-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="c68e4-122">ในฟิลด์ชื่อ ป้อนค่า "ทรัพยากร" เลือกตัวดำเนินการตัวกรอง "ประกอบด้วย" และจากนั้นคลิก ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c68e4-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="c68e4-123">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="c68e4-123">Click Open.</span></span>
6. <span data-ttu-id="c68e4-124">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="c68e4-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="c68e4-125">ถ้าไม่ได้เปิดใช้งานปุ่มนำเข้าบน FastTab รุ่น คุณได้นำเข้ารุ่น 1 หนึ่งในการตั้งค่าคอนฟิก ER 'แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="c68e4-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="c68e4-126">คุณสามารถข้ามขั้นตอนที่เหลือในงานย่อยนี้ได้</span><span class="sxs-lookup"><span data-stu-id="c68e4-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="c68e4-127">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="c68e4-127">Click Import.</span></span>
8. <span data-ttu-id="c68e4-128">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="c68e4-128">Click Yes.</span></span>
9. <span data-ttu-id="c68e4-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c68e4-129">Close the page.</span></span>
10. <span data-ttu-id="c68e4-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c68e4-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c68e4-131">เพิ่มการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="c68e4-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="c68e4-132">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="c68e4-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="c68e4-133">เพิ่มรูปแบบ ER ใหม่เพื่อแยกวิเคราะห์ใบแจ้งยอดจากธนาคารขาเข้าในรูปแบบ TXT</span><span class="sxs-lookup"><span data-stu-id="c68e4-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="c68e4-134">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="c68e4-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="c68e4-135">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดเมนูกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="c68e4-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="c68e4-136">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามข้อมูลแบบจำลอง แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="c68e4-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="c68e4-137">ในฟิลด์ชื่อ ชนิด 'รูปแบบการนำเข้าใบแจ้งยอดจากธนาคาร (ตัวอย่าง)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="c68e4-138">รูปแบบการนำเข้าสำหรับใบแจ้งยอดจากธนาคาร (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="c68e4-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="c68e4-139">เลือก ใช่ ในฟิลด์สนับสนุนการนำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c68e4-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="c68e4-140">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="c68e4-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="c68e4-141">ออกแบบการตั้งค่าคอนฟิกรูปแบบ ER - รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="c68e4-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="c68e4-142">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="c68e4-142">Click Designer.</span></span>
    * <span data-ttu-id="c68e4-143">รูปแบบที่ได้รับการออกแบบแสดงถึงโครงสร้างของไฟล์ภายนอกที่คาดไว้ในรูปแบบ TXT</span><span class="sxs-lookup"><span data-stu-id="c68e4-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="c68e4-144">คลิกเพิ่มรากเพื่อเปิดเมนูกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="c68e4-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="c68e4-145">ในแผนภูมิ ให้เลือก 'ข้อความ\ลำดับ'</span><span class="sxs-lookup"><span data-stu-id="c68e4-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="c68e4-146">ในฟิลด์ ชื่อ ให้พิมพ์ 'Root'</span><span class="sxs-lookup"><span data-stu-id="c68e4-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="c68e4-147">ราก</span><span class="sxs-lookup"><span data-stu-id="c68e4-147">Root</span></span>  
5. <span data-ttu-id="c68e4-148">ในฟิลด์อักขระพิเศษ ให้เลือก 'รายการใหม่ - Windows (CR LF)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="c68e4-149">ตัวเลือก 'รายการใหม่ - Windows (CR LF)' ได้ถูกเลือกในฟิลด์ ‘อักขระพิเศษ’</span><span class="sxs-lookup"><span data-stu-id="c68e4-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="c68e4-150">โดยขึ้นอยู่กับการตั้งค่านี้ แต่ละรายการในไฟล์แยกวิเคราะห์จะถือว่าเป็นเรกคอร์ดแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="c68e4-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="c68e4-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c68e4-151">Click OK.</span></span>
7. <span data-ttu-id="c68e4-152">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c68e4-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="c68e4-153">ในแผนภูมิ ให้เลือก 'ข้อความ\ลำดับ'</span><span class="sxs-lookup"><span data-stu-id="c68e4-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="c68e4-154">ในฟิลด์ชื่อ ให้พิมพ์ชื่อ 'แถว'</span><span class="sxs-lookup"><span data-stu-id="c68e4-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="c68e4-155">แถว</span><span class="sxs-lookup"><span data-stu-id="c68e4-155">Rows</span></span>  
10. <span data-ttu-id="c68e4-156">ในฟิลด์ความหลากหลาย ให้เลือก 'หนึ่งต่อหลายรายการ'</span><span class="sxs-lookup"><span data-stu-id="c68e4-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="c68e4-157">มีการเลือกตัวเลือก 'หนึ่งต่อหลายรายการ' ในฟิลด์ 'ความหลากหลาย'</span><span class="sxs-lookup"><span data-stu-id="c68e4-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="c68e4-158">โดยขึ้นอยู่กับการตั้งค่านี้ มีการคาดหวังว่า รายการอย่างน้อยหนึ่งรายการจะปรากฏในไฟล์แยกวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="c68e4-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="c68e4-159">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c68e4-159">Click OK.</span></span>
12. <span data-ttu-id="c68e4-160">ในแผนภูมิ ให้เลือก 'ราก\แถว'</span><span class="sxs-lookup"><span data-stu-id="c68e4-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="c68e4-161">คลิก เพิ่มลำดับ</span><span class="sxs-lookup"><span data-stu-id="c68e4-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="c68e4-162">ในฟิลด์ชื่อ ให้พิมพ์ 'ฟิลด์'</span><span class="sxs-lookup"><span data-stu-id="c68e4-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="c68e4-163">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c68e4-163">Fields</span></span>  
15. <span data-ttu-id="c68e4-164">ในฟิลด์ความหลากหลาย ให้เลือก 'เพียงรายการเดียว'</span><span class="sxs-lookup"><span data-stu-id="c68e4-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="c68e4-165">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c68e4-165">Click OK.</span></span>
17. <span data-ttu-id="c68e4-166">ในแผนภูมิ ให้เลือก 'ราก\แถว\ฟิลด์'</span><span class="sxs-lookup"><span data-stu-id="c68e4-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="c68e4-167">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c68e4-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="c68e4-168">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="c68e4-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="c68e4-169">ในฟิลด์ชื่อ ให้พิมพ์ 'IBAN'</span><span class="sxs-lookup"><span data-stu-id="c68e4-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="c68e4-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="c68e4-170">IBAN</span></span>  
21. <span data-ttu-id="c68e4-171">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c68e4-171">Click OK.</span></span>
    * <span data-ttu-id="c68e4-172">มีการตั้งค่าคอนฟิกที่แต่ละรายการในไฟล์แยกวิเคราะห์ประกอบด้วยรหัส IBAN เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c68e4-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="c68e4-173">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c68e4-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="c68e4-174">ออกแบบการตั้งค่าคอนฟิกรูปแบบของ ER – การแม็ปไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c68e4-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="c68e4-175">คลิก แม็ปรูปแบบไปยังแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="c68e4-175">Click Map format to model.</span></span>
2. <span data-ttu-id="c68e4-176">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c68e4-176">Click New.</span></span>
3. <span data-ttu-id="c68e4-177">ในฟิลด์คำนิยาม พิมพ์ 'BankToCustomerDebitCreditNotificationInitiation'</span><span class="sxs-lookup"><span data-stu-id="c68e4-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="c68e4-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="c68e4-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="c68e4-179">แก้ไขการเปลี่ยนแปลงของคำนิยาม</span><span class="sxs-lookup"><span data-stu-id="c68e4-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="c68e4-180">ในฟิลด์ชื่อ ให้พิมพ์ 'การแม็ปไปยังแบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="c68e4-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="c68e4-181">การแม็ปไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c68e4-181">Mapping to data model</span></span>  
6. <span data-ttu-id="c68e4-182">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c68e4-182">Click Save.</span></span>
7. <span data-ttu-id="c68e4-183">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="c68e4-183">Click Designer.</span></span>
8. <span data-ttu-id="c68e4-184">ในแผนภูมิ เลือก 'Dynamics 365 for Operations\คลาส'</span><span class="sxs-lookup"><span data-stu-id="c68e4-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="c68e4-185">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="c68e4-185">Click Add root.</span></span>
    * <span data-ttu-id="c68e4-186">เพิ่มแหล่งข้อมูลใหม่เพื่อเรียกตรรกะแอพลิเคชันที่มีอยู่สำหรับการตรวจสอบรหัส IBAN</span><span class="sxs-lookup"><span data-stu-id="c68e4-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="c68e4-187">ในฟิลด์ชื่อ พิมพ์ 'ตรวจสอบรหัส'</span><span class="sxs-lookup"><span data-stu-id="c68e4-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="c68e4-188">ตรวจสอบรหัส</span><span class="sxs-lookup"><span data-stu-id="c68e4-188">check_codes</span></span>  
11. <span data-ttu-id="c68e4-189">ในฟิลด์คลาส ให้พิมพ์ 'ISO7064'</span><span class="sxs-lookup"><span data-stu-id="c68e4-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="c68e4-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="c68e4-190">ISO7064</span></span>  
12. <span data-ttu-id="c68e4-191">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c68e4-191">Click OK.</span></span>
13. <span data-ttu-id="c68e4-192">ในแผนภูมิ ให้ขยาย 'รูปแบบ'</span><span class="sxs-lookup"><span data-stu-id="c68e4-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="c68e4-193">ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="c68e4-194">ในแผนภูมิ เลือก 'รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..\* (แถว)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="c68e4-195">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c68e4-195">Click Bind.</span></span>
17. <span data-ttu-id="c68e4-196">ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..\* (แถว)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="c68e4-197">ในแผนภูมิ ขยาย ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..\* (แถว)\ฟิลด์: 1..1 ลำดับ (ฟิลด์)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="c68e4-198">ในแผนภูมิ เลือก ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..\* (แถว)\ฟิลด์: ลำดับ 1..1 (ฟิลด์)\IBAN: สตริง(IBAN)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="c68e4-199">ในแผนภูมิ ขยาย 'การชำระเงิน: รูปแบบ.ราก.แถว'</span><span class="sxs-lookup"><span data-stu-id="c68e4-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="c68e4-200">ในแผนภูมิ ขยาย 'การชำระเงิน = รูปแบบ.ราก.แถว\บัญชีเจ้าหนี้(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="c68e4-201">ในแผนภูมิ ขยาย 'การชำระเงิน = รูปแบบ.ราก.แถว\บัญชีเจ้าหนี้(CreditorAccount)\การระบุรหัสประจำตัว'</span><span class="sxs-lookup"><span data-stu-id="c68e4-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="c68e4-202">ในแผนภูมิ เลือก 'การชำระเงิน = รูปแบบ.ราก.แถว\บัญชีเจ้าหนี้(CreditorAccount)\การระบุรหัสประจำตัว\IBAN'</span><span class="sxs-lookup"><span data-stu-id="c68e4-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="c68e4-203">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c68e4-203">Click Bind.</span></span>
25. <span data-ttu-id="c68e4-204">คลิกแท็บ การตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c68e4-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="c68e4-205">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c68e4-205">Click New.</span></span>
    * <span data-ttu-id="c68e4-206">เพิ่มกฎการตรวจสอบใหม่ที่แสดงข้อผิดพลาดสำหรับรายการใดๆ ในไฟล์แยกวิเคราะห์ที่ประกอบด้วยรหัส IBAN ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c68e4-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="c68e4-207">คลิก แก้ไขเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="c68e4-207">Click Edit condition.</span></span>
28. <span data-ttu-id="c68e4-208">ในแผนภูมิ ขยาย 'ตรวจสอบรหัส'</span><span class="sxs-lookup"><span data-stu-id="c68e4-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="c68e4-209">ในแผนภูมิ เลือก 'check_codes\verifyMOD1271_36'</span><span class="sxs-lookup"><span data-stu-id="c68e4-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="c68e4-210">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c68e4-210">Click Add data source.</span></span>
31. <span data-ttu-id="c68e4-211">ในฟิลด์สูตร ป้อน 'check_codes.verifyMOD1271_36('</span><span class="sxs-lookup"><span data-stu-id="c68e4-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="c68e4-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="c68e4-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="c68e4-213">ในแผนภูมิ ให้ขยาย 'รูปแบบ'</span><span class="sxs-lookup"><span data-stu-id="c68e4-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="c68e4-214">ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="c68e4-215">ในแผนภูมิ ขยาย 'รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..\* (แถว)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="c68e4-216">ในแผนภูมิ ขยาย ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..\* (แถว)\ฟิลด์: 1..1 ลำดับ (ฟิลด์)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="c68e4-217">ในแผนภูมิ เลือก ' รูปแบบ\ราก: ลำดับ(ราก)\แถว: ลำดับ 1..\* (แถว)\ฟิลด์: ลำดับ 1..1 (ฟิลด์)\IBAN: สตริง(IBAN)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="c68e4-218">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c68e4-218">Click Add data source.</span></span>
38. <span data-ttu-id="c68e4-219">ในฟิลด์สูตร ป้อน 'check_codes.verifyMOD1271_36 (รูปแบบ.ราก.แถว.ฟิลด์.IBAN)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="c68e4-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="c68e4-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="c68e4-221">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c68e4-221">Click Save.</span></span>
40. <span data-ttu-id="c68e4-222">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c68e4-222">Close the page.</span></span>
    * <span data-ttu-id="c68e4-223">เงื่อนไขในการตรวจสอบได้ถูกตั้งค่าคอนฟิกเพื่อส่งคืนค่า เท็จ สำหรับรหัส IBAN ที่ไม่ถูกต้องใดๆ โดยการเรียกวิธีการที่มีอยู่ 'verifyMOD1271_36' ของคลาสแอพลิเคชัน 'ISO7064'</span><span class="sxs-lookup"><span data-stu-id="c68e4-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="c68e4-224">หมายเหตุว่า ค่าของรหัส IBAN ถูกกำหนดแบบไดนามิกขณะรันไทม์เป็นอาร์กิวเมนต์ของวิธีการเรียก โดยยึดตามเนื้อหาของไฟล์ TXT ที่แยกวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="c68e4-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="c68e4-225">คลิกแก้ไขข้อความ</span><span class="sxs-lookup"><span data-stu-id="c68e4-225">Click Edit message.</span></span>
42. <span data-ttu-id="c68e4-226">ในฟิลด์สูตร ป้อน ' CONCATENATE ("พบรหัส IBAN ที่ไม่ถูกต้อง: ", รูปแบบ.ราก.แถว.ฟิลด์.IBAN)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="c68e4-227">CONCATENATE("พบรหัส IBAN ที่ไม่ถูกต้อง: ", รูปแบบ.ราก.แถว.ฟิลด์.IBAN)'</span><span class="sxs-lookup"><span data-stu-id="c68e4-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="c68e4-228">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c68e4-228">Click Save.</span></span>
44. <span data-ttu-id="c68e4-229">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c68e4-229">Close the page.</span></span>
45. <span data-ttu-id="c68e4-230">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c68e4-230">Click Save.</span></span>
46. <span data-ttu-id="c68e4-231">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c68e4-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="c68e4-232">รันการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="c68e4-232">Run the format mapping</span></span>
<span data-ttu-id="c68e4-233">เพื่อวัตถุประสงค์ในการทดสอบ ดำเนินการแม็ปรูปแบบโดยใช้แฟ้ม SampleIncomingMessage.txt ซึ่งคุณดาวน์โหลดไว้</span><span class="sxs-lookup"><span data-stu-id="c68e4-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="c68e4-234">เอาท์พุทที่สร้างขึ้นรวมข้อมูลที่จะถูกนำเข้าจากไฟล์ TXT ที่เลือก และจะถูกเติมข้อมูลไปยังแบบจำลองข้อมูลที่กำหนดเองในระหว่างการนำเข้าจริง</span><span class="sxs-lookup"><span data-stu-id="c68e4-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="c68e4-235">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="c68e4-235">Click Run.</span></span>
    * <span data-ttu-id="c68e4-236">คลิก เรียกดู และนำทางไปยังไฟล์ SampleIncomingMessage.txt ที่คุณดาวน์โหลดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c68e4-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="c68e4-237">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c68e4-237">Click OK.</span></span>
    * <span data-ttu-id="c68e4-238">ตรวจสอบเอาท์พุทในรูปแบบ XML ซึ่งแสดงข้อมูลที่ได้ถูกนำเข้าจากไฟล์ที่เลือก และถูกนำไปยังแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c68e4-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="c68e4-239">โปรดทราบว่า มีการประมวลผลรายการของไฟล์ TXT ที่นำเข้า 3 รายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c68e4-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="c68e4-240">รหัส IBAN บนรายการที่ 4 ที่ไม่ถูกต้อง ถูกข้าม และมีการระบุข้อความแสดงข้อผิดพลาดใน Infolog</span><span class="sxs-lookup"><span data-stu-id="c68e4-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  


