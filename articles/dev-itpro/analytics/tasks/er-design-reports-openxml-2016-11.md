--- 
title: "ออกแบบการตั้งค่าคอนฟิก ER เพื่อสร้างรายงานในรูปแบบ OpenXML"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ใหม่ (ER) ซึ่งประกอบด้วยเท็มเพลตสำหรับการสร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ OPENXML"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="e34f7-103">ออกแบบการตั้งค่าคอนฟิก ER เพื่อสร้างรายงานในรูปแบบ OpenXML</span><span class="sxs-lookup"><span data-stu-id="e34f7-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e34f7-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ใหม่ (ER) ซึ่งประกอบด้วยเท็มเพลตสำหรับการสร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="e34f7-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="e34f7-105">การตั้งค่าคอนฟิกนี้จะถูกใช้สำหรับการประมวลผลการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e34f7-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="e34f7-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง ซึ่งคือ Litware, Inc. ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัท GBSI </span><span class="sxs-lookup"><span data-stu-id="e34f7-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="e34f7-107">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="e34f7-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="e34f7-108">นอกจากนี้ คุณยังต้องดาวน์โหลดและบันทึกแฟ้ม Microsoft Excel [เท็มเพลตของรายงานการชำระเงิน](https://go.microsoft.com/fwlink/?linkid=862266)</span><span class="sxs-lookup"><span data-stu-id="e34f7-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="e34f7-109">อัพโหลดการตั้งค่าคอนฟิกแบบจำลองข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="e34f7-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e34f7-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e34f7-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e34f7-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e34f7-112">เลือกผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="e34f7-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="e34f7-113">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="e34f7-113">Click Set active.</span></span>
4. <span data-ttu-id="e34f7-114">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="e34f7-114">Click Repositories.</span></span>
    * <span data-ttu-id="e34f7-115">เลือกที่เก็บสำหรับชนิดทรัพยากรการดำเนินงาน ถ้าพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e34f7-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="e34f7-116">ถ้าพร้อมใช้งาน ให้ข้ามขั้นตอนต่อไปนี้เกี่ยวกับการสร้างที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="e34f7-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="e34f7-117">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e34f7-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="e34f7-118">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'ทรัพยากรการดำเนินงาน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="e34f7-119">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="e34f7-119">Click Create repository.</span></span>
8. <span data-ttu-id="e34f7-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e34f7-120">Click OK.</span></span>
9. <span data-ttu-id="e34f7-121">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="e34f7-121">Click Open.</span></span>
10. <span data-ttu-id="e34f7-122">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="e34f7-123">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-123">Click Import.</span></span>
    * <span data-ttu-id="e34f7-124">นำเข้าแบบจำลองข้มูลนี้</span><span class="sxs-lookup"><span data-stu-id="e34f7-124">Import this data model.</span></span> <span data-ttu-id="e34f7-125">ซึ่งจะถูกใช้เป็นแหล่งข้อมูลในการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="e34f7-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="e34f7-126">ให้ข้ามขั้นตอนนี้ถ้าการตั้งค่าคอนฟิกนี้ไดุถูกนำเข้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="e34f7-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="e34f7-127">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="e34f7-127">Click Yes.</span></span>
13. <span data-ttu-id="e34f7-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-128">Close the page.</span></span>
14. <span data-ttu-id="e34f7-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="e34f7-130">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="e34f7-130">Create a new format configuration</span></span>
1. <span data-ttu-id="e34f7-131">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="e34f7-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="e34f7-132">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="e34f7-133">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e34f7-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="e34f7-134">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามข้อมูลแบบจำลอง แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="e34f7-135">สร้างรูปแบบที่เป็นไปตามแบบจำลองข้อมูลของแบบจำลองการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="e34f7-136">ในฟิลด์ชื่อ พิมพ์ 'รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="e34f7-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="e34f7-137">รายงานแผ่นงานตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e34f7-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="e34f7-138">ในฟิลด์คำอธิบาย พิมพ์ 'รายงานแผ่นงานตัวอย่าง สำหรับการชำระเงินของผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="e34f7-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="e34f7-139">รายงานแผ่นงานตัวอย่างสำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e34f7-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="e34f7-140">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e34f7-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="e34f7-141">เลือกข้อกำหนด 'การเริ่มต้นการโอนย้ายเครดิตของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="e34f7-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="e34f7-142">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e34f7-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="e34f7-143">ออกแบบเอกสารใหม่ในรูปแบบแผ่นงาน OPENXML</span><span class="sxs-lookup"><span data-stu-id="e34f7-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="e34f7-144">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน\รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="e34f7-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="e34f7-145">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="e34f7-145">Click Designer.</span></span>
3. <span data-ttu-id="e34f7-146">ในบานหน้าต่างการดำเนินการ คลิกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="e34f7-147">คลิกนำเข้าจาก Excel</span><span class="sxs-lookup"><span data-stu-id="e34f7-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="e34f7-148">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="e34f7-148">Click Attachments.</span></span>
    * <span data-ttu-id="e34f7-149">แนบเอกสาร Excel ที่มีอยู่เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="e34f7-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="e34f7-150">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e34f7-150">Click New.</span></span>
7. <span data-ttu-id="e34f7-151">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="e34f7-151">Click File.</span></span>
    * <span data-ttu-id="e34f7-152">ชี้ไปที่ไฟล์ Excel ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="e34f7-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="e34f7-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-153">Close the page.</span></span>
9. <span data-ttu-id="e34f7-154">ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e34f7-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="e34f7-155">เลือกไฟล์ Excel ที่แนบมาเพื่อใช้เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="e34f7-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="e34f7-156">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e34f7-156">Click OK.</span></span>
    * <span data-ttu-id="e34f7-157">โปรดทราบว่าส่วนประกอบรูปแบบ ER ได้ถูกสร้างขึ้นในรูปแบบการออกแบบตามโครงสร้างของเอกสาร MS Excel อ้างอิง (ช่วงที่มีชื่อ)</span><span class="sxs-lookup"><span data-stu-id="e34f7-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="e34f7-158">สร้างแหล่งข้อมูลใหม่เพื่อคำนวณผลรวมโดยรหัสสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="e34f7-159">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="e34f7-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="e34f7-160">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e34f7-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="e34f7-161">ในแผนภูมิ ให้เลือก 'ฟังก์ชัน\จัดกลุ่มโดย'</span><span class="sxs-lookup"><span data-stu-id="e34f7-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="e34f7-162">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงินในการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="e34f7-163">สกุลเงินในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="e34f7-164">คลิกแก้ไขกลุ่มโดย</span><span class="sxs-lookup"><span data-stu-id="e34f7-164">Click Edit group by.</span></span>
6. <span data-ttu-id="e34f7-165">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="e34f7-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="e34f7-166">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="e34f7-167">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="e34f7-167">Click Add field to.</span></span>
9. <span data-ttu-id="e34f7-168">คลิกสิ่งที่จะจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="e34f7-168">Click What to group.</span></span>
10. <span data-ttu-id="e34f7-169">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="e34f7-170">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="e34f7-171">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="e34f7-171">Click Add field to.</span></span>
13. <span data-ttu-id="e34f7-172">คลิกฟิลด์ที่ถูกจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="e34f7-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="e34f7-173">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ยอดเงินที่แนะนำ(ยอดเงินที่แนะนำ)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="e34f7-174">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="e34f7-174">Click Add field to.</span></span>
16. <span data-ttu-id="e34f7-175">คลิกฟิลด์การรวม</span><span class="sxs-lookup"><span data-stu-id="e34f7-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="e34f7-176">ในฟิลด์วิธีการ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e34f7-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="e34f7-177">เลือกฟังก์ชันการรวม SUM</span><span class="sxs-lookup"><span data-stu-id="e34f7-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="e34f7-178">ในฟิลด์ชือ ให้พิมพ์ 'ยอดเงินที่แนะนำรวม'</span><span class="sxs-lookup"><span data-stu-id="e34f7-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="e34f7-179">ยอดเงินที่แนะนำรวม</span><span class="sxs-lookup"><span data-stu-id="e34f7-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="e34f7-180">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e34f7-180">Click Save.</span></span>
20. <span data-ttu-id="e34f7-181">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-181">Close the page.</span></span>
21. <span data-ttu-id="e34f7-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e34f7-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="e34f7-183">แม็ปส่วนประกอบรูปแบบกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e34f7-183">Map format components to data sources</span></span>
1. <span data-ttu-id="e34f7-184">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="e34f7-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="e34f7-185">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="e34f7-186">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\บัญชีเจ้าหนี้(บัญชีเจ้าหนี้)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="e34f7-187">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ฝ่ายผู้สร้างข้อความ(ฝ่ายผู้สร้างข้อความ)\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="e34f7-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="e34f7-188">ในแผนภูมิ ขยาย 'Excel\ส่วนหัวรายงาน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="e34f7-189">ในแผนภูมิ ให้เลือก 'Excel\ส่วนหัวรายงาน\ชื่อบริษัท'</span><span class="sxs-lookup"><span data-stu-id="e34f7-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="e34f7-190">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-190">Click Bind.</span></span>
8. <span data-ttu-id="e34f7-191">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="e34f7-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="e34f7-192">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\การระบุรหัสประจำตัว'</span><span class="sxs-lookup"><span data-stu-id="e34f7-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="e34f7-193">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\การระบุรหัสประจำตัว\รหัสแหล่งข้อมูล(รหัสแหล่งข้อมูล)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="e34f7-194">ในแผนภูมิ ขยาย 'Excel\รายการการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="e34f7-195">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\ชื่อบัญชีผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="e34f7-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="e34f7-196">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-196">Click Bind.</span></span>
14. <span data-ttu-id="e34f7-197">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระ\เจ้าหนี้\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="e34f7-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="e34f7-198">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\ชื่อผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="e34f7-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="e34f7-199">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-199">Click Bind.</span></span>
17. <span data-ttu-id="e34f7-200">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="e34f7-201">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ตัวแทนเจ้าหนี้(ตัวแทนเจ้าหนี้)\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="e34f7-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="e34f7-202">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="e34f7-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="e34f7-203">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-203">Click Bind.</span></span>
21. <span data-ttu-id="e34f7-204">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ตัวแทนเจ้าหนี้(ตัวแทนเจ้าหนี้)\หมายเลขการกำหนดเส้นทาง(หมายเลขการกำหนดเส้นทาง)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="e34f7-205">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="e34f7-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="e34f7-206">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-206">Click Bind.</span></span>
24. <span data-ttu-id="e34f7-207">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="e34f7-208">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)\Identification'</span><span class="sxs-lookup"><span data-stu-id="e34f7-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="e34f7-209">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\บัญชีเจ้าหนี้(บัญชีเจ้าหนี้)\การระบุรหัสประจำตัว\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="e34f7-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="e34f7-210">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="e34f7-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="e34f7-211">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-211">Click Bind.</span></span>
29. <span data-ttu-id="e34f7-212">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ยอดเงินที่แนะนำ(ยอดเงินที่แนะนำ)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="e34f7-213">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\เดบิต'</span><span class="sxs-lookup"><span data-stu-id="e34f7-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="e34f7-214">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-214">Click Bind.</span></span>
32. <span data-ttu-id="e34f7-215">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="e34f7-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="e34f7-216">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="e34f7-217">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="e34f7-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="e34f7-218">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="e34f7-219">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="e34f7-220">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-220">Click Bind.</span></span>
38. <span data-ttu-id="e34f7-221">ในแผนภูมิ ขยาย 'สกุลเงินในการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="e34f7-222">ในแผนภูมิ ขยาย 'สกุลเงินในการชำระเงิน\จัดกลุ่มแล้ว'</span><span class="sxs-lookup"><span data-stu-id="e34f7-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="e34f7-223">ในแผนภูมิ เลือก 'สกุลเงินในการชำระเงิน\จัดกลุ่มแล้ว\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="e34f7-224">ในแผนภูมิ ขยาย 'Excel\รายการสรุป'</span><span class="sxs-lookup"><span data-stu-id="e34f7-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="e34f7-225">ในแผนภูมิ ให้เลือก 'Excel\รายการสรุป\สกุลเงินสรุป'</span><span class="sxs-lookup"><span data-stu-id="e34f7-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="e34f7-226">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-226">Click Bind.</span></span>
44. <span data-ttu-id="e34f7-227">ในแผนภูมิ ขยาย 'สกุลเงินในการชำระเงิน\รวมแล้ว'</span><span class="sxs-lookup"><span data-stu-id="e34f7-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="e34f7-228">ในแผนภูมิ เลือก 'สกุลเงินในการชำระเงิน\รวมแล้ว\ยอดเงินที่แนะนำรวม'</span><span class="sxs-lookup"><span data-stu-id="e34f7-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="e34f7-229">ในแผนภูมิ ให้เลือก 'Excel\รายการสรุป\จำนวนเงินสรุป'</span><span class="sxs-lookup"><span data-stu-id="e34f7-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="e34f7-230">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-230">Click Bind.</span></span>
48. <span data-ttu-id="e34f7-231">ในแผนภูมิ ให้เลือก 'สกุลเงินในการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="e34f7-232">ในแผนภูมิ ให้เลือก 'Excel\รายการสรุป'</span><span class="sxs-lookup"><span data-stu-id="e34f7-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="e34f7-233">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-233">Click Bind.</span></span>
51. <span data-ttu-id="e34f7-234">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="e34f7-235">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="e34f7-236">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="e34f7-236">Click Bind.</span></span>
54. <span data-ttu-id="e34f7-237">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e34f7-237">Click Save.</span></span>
55. <span data-ttu-id="e34f7-238">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="e34f7-239">ใช้การตั้งค่าคอนฟิกที่สร้างขึ้นสำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="e34f7-240">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="e34f7-240">Click Change status.</span></span>
2. <span data-ttu-id="e34f7-241">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e34f7-241">Click Complete.</span></span>
3. <span data-ttu-id="e34f7-242">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e34f7-242">Click OK.</span></span>
4. <span data-ttu-id="e34f7-243">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-243">Close the page.</span></span>
5. <span data-ttu-id="e34f7-244">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-244">Close the page.</span></span>
6. <span data-ttu-id="e34f7-245">ไปที่บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="e34f7-246">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์วิธีการชำระเงินด้วยค่า 'อิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="e34f7-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="e34f7-247">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e34f7-247">Electronic</span></span>  
8. <span data-ttu-id="e34f7-248">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="e34f7-248">Click Edit.</span></span>
9. <span data-ttu-id="e34f7-249">ขยายส่วนรูปแบบของไฟล์</span><span class="sxs-lookup"><span data-stu-id="e34f7-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="e34f7-250">เลือก ใช่ ในฟิลด์รายงานอิเล็กทรอนิกส์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="e34f7-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="e34f7-251">ในฟิลด์การตั้งค่าคอนฟิกรูปแบบการส่งออก ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e34f7-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="e34f7-252">เลือกการตั้งค่าคอนฟิก 'รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="e34f7-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="e34f7-253">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e34f7-253">Click Save.</span></span>
13. <span data-ttu-id="e34f7-254">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e34f7-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="e34f7-255">ใช้การตั้งค่าคอนฟิกที่สร้างสำหรับการทดสอบการประมวลผลสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="e34f7-256">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="e34f7-257">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e34f7-257">Click New.</span></span>
    * <span data-ttu-id="e34f7-258">สร้างสมุดรายวันการชำระเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="e34f7-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="e34f7-259">ในฟิลด์ชื่อ ให้พิมพ์ 'VendPay'</span><span class="sxs-lookup"><span data-stu-id="e34f7-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="e34f7-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="e34f7-260">VendPay</span></span>  
4. <span data-ttu-id="e34f7-261">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="e34f7-261">Click Lines.</span></span>
5. <span data-ttu-id="e34f7-262">ในฟิลด์บัญชี ให้ระบุค่า 'GB_SI_000001'</span><span class="sxs-lookup"><span data-stu-id="e34f7-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="e34f7-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="e34f7-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="e34f7-264">ตั้งค่าเดบิตเป็น '1000'</span><span class="sxs-lookup"><span data-stu-id="e34f7-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="e34f7-265">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e34f7-265">Click New.</span></span>
8. <span data-ttu-id="e34f7-266">ในฟิลด์บัญชี ให้ระบุค่า 'GB_SI_000005'</span><span class="sxs-lookup"><span data-stu-id="e34f7-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="e34f7-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="e34f7-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="e34f7-268">ตั้งค่าเดบิตเป็น '2000'</span><span class="sxs-lookup"><span data-stu-id="e34f7-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="e34f7-269">ในฟิลด์สกุลเงิน ให้พิมพ์ 'EUR'</span><span class="sxs-lookup"><span data-stu-id="e34f7-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="e34f7-270">EUR</span><span class="sxs-lookup"><span data-stu-id="e34f7-270">EUR</span></span>  
11. <span data-ttu-id="e34f7-271">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่า 'GBSI OPER'</span><span class="sxs-lookup"><span data-stu-id="e34f7-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="e34f7-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="e34f7-272">GBSI OPER</span></span>  
12. <span data-ttu-id="e34f7-273">ในฟิลด์วิธีการชำระเงิน ให้พิมพ์ค่า 'อิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="e34f7-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="e34f7-274">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e34f7-274">Electronic</span></span>  
13. <span data-ttu-id="e34f7-275">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e34f7-275">Click Save.</span></span>
14. <span data-ttu-id="e34f7-276">คลิกสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-276">Click Generate payments.</span></span>
15. <span data-ttu-id="e34f7-277">ในฟิลด์วิธีการชำระเงิน ให้พิมพ์ค่า 'อิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="e34f7-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="e34f7-278">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e34f7-278">Electronic</span></span>  
16. <span data-ttu-id="e34f7-279">ในฟิลด์ชื่อไฟล์ พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="e34f7-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="e34f7-280">ตัวอย่างเช่น พิมพ์ การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e34f7-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="e34f7-281">ในฟิลด์บัญชีธนาคาร ให้พิมพ์ 'GBSI OPER'</span><span class="sxs-lookup"><span data-stu-id="e34f7-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="e34f7-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="e34f7-282">GBSI OPER</span></span>  
18. <span data-ttu-id="e34f7-283">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e34f7-283">Click OK.</span></span>
19. <span data-ttu-id="e34f7-284">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e34f7-284">Click OK.</span></span>
    * <span data-ttu-id="e34f7-285">ตรวจทานแผ่นงานที่สร้าง ซึ่งรวมถึงรายละเอียดของรายการชำระเงิน และยอดรวมสำหรับรหัสสกุลเงินแต่ละรายการที่ใช้ในข้อความการชำระเงินนี้</span><span class="sxs-lookup"><span data-stu-id="e34f7-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


