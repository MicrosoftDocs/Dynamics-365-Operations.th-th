--- 
title: "ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OpenXML สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 51208cbc5118e95fd402cca3cbc228ef1b87a47f
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="61f97-103">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OpenXML สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="61f97-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61f97-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ใหม่ (ER) ซึ่งประกอบด้วยเท็มเพลตสำหรับการสร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="61f97-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="61f97-105">การตั้งค่าคอนฟิกนี้จะถูกใช้สำหรับการประมวลผลการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="61f97-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="61f97-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง ซึ่งคือ Litware, Inc. ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัท GBSI </span><span class="sxs-lookup"><span data-stu-id="61f97-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="61f97-107">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="61f97-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="61f97-108">คุณยังต้องมีไฟล์ Excel ซึ่งจะถูกนำเข้าเมื่อมีการสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="61f97-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="61f97-109">ไฟล์นี้สามารถเข้าถึงได้จาก: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="61f97-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="61f97-110">อัพโหลดการตั้งค่าคอนฟิกแบบจำลองข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="61f97-111">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="61f97-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="61f97-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="61f97-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="61f97-113">เลือกผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="61f97-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="61f97-114">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="61f97-114">Click Set active.</span></span>
4. <span data-ttu-id="61f97-115">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="61f97-115">Click Repositories.</span></span>
    * <span data-ttu-id="61f97-116">เลือกที่เก็บสำหรับชนิดทรัพยากรการดำเนินงาน ถ้าพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="61f97-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="61f97-117">ถ้าพร้อมใช้งาน ให้ข้ามขั้นตอนต่อไปนี้เกี่ยวกับการสร้างที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="61f97-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="61f97-118">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="61f97-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="61f97-119">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'ทรัพยากรการดำเนินงาน'</span><span class="sxs-lookup"><span data-stu-id="61f97-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="61f97-120">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="61f97-120">Click Create repository.</span></span>
8. <span data-ttu-id="61f97-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="61f97-121">Click OK.</span></span>
9. <span data-ttu-id="61f97-122">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="61f97-122">Click Open.</span></span>
10. <span data-ttu-id="61f97-123">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="61f97-124">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="61f97-124">Click Import.</span></span>
    * <span data-ttu-id="61f97-125">นำเข้าแบบจำลองข้มูลนี้</span><span class="sxs-lookup"><span data-stu-id="61f97-125">Import this data model.</span></span> <span data-ttu-id="61f97-126">ซึ่งจะถูกใช้เป็นแหล่งข้อมูลในการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="61f97-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="61f97-127">ให้ข้ามขั้นตอนนี้ถ้าการตั้งค่าคอนฟิกนี้ไดุถูกนำเข้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="61f97-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="61f97-128">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="61f97-128">Click Yes.</span></span>
13. <span data-ttu-id="61f97-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-129">Close the page.</span></span>
14. <span data-ttu-id="61f97-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="61f97-131">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="61f97-131">Create a new format configuration</span></span>
1. <span data-ttu-id="61f97-132">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="61f97-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="61f97-133">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="61f97-134">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="61f97-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="61f97-135">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามข้อมูลแบบจำลอง แบบจำลองการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="61f97-136">สร้างรูปแบบที่เป็นไปตามแบบจำลองข้อมูลของแบบจำลองการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="61f97-137">ในฟิลด์ชื่อ พิมพ์ 'รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="61f97-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="61f97-138">รายงานแผ่นงานตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="61f97-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="61f97-139">ในฟิลด์คำอธิบาย พิมพ์ 'รายงานแผ่นงานตัวอย่าง สำหรับการชำระเงินของผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="61f97-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="61f97-140">รายงานแผ่นงานตัวอย่างสำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="61f97-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="61f97-141">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="61f97-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="61f97-142">เลือกข้อกำหนด 'การเริ่มต้นการโอนย้ายเครดิตของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="61f97-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="61f97-143">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="61f97-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="61f97-144">ออกแบบเอกสารใหม่ในรูปแบบแผ่นงาน OPENXML</span><span class="sxs-lookup"><span data-stu-id="61f97-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="61f97-145">ในแผนภูมิ เลือก 'แบบจำลองการชำระเงิน\รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="61f97-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="61f97-146">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="61f97-146">Click Designer.</span></span>
3. <span data-ttu-id="61f97-147">ในบานหน้าต่างการดำเนินการ คลิกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="61f97-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="61f97-148">คลิกนำเข้าจาก Excel</span><span class="sxs-lookup"><span data-stu-id="61f97-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="61f97-149">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="61f97-149">Click Attachments.</span></span>
    * <span data-ttu-id="61f97-150">แนบเอกสาร Excel ที่มีอยู่เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="61f97-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="61f97-151">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="61f97-151">Click New.</span></span>
7. <span data-ttu-id="61f97-152">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="61f97-152">Click File.</span></span>
    * <span data-ttu-id="61f97-153">ชี้ไปที่ไฟล์ Excel ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="61f97-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="61f97-154">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-154">Close the page.</span></span>
9. <span data-ttu-id="61f97-155">ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="61f97-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="61f97-156">เลือกไฟล์ Excel ที่แนบมาเพื่อใช้เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="61f97-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="61f97-157">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="61f97-157">Click OK.</span></span>
    * <span data-ttu-id="61f97-158">โปรดทราบว่าส่วนประกอบรูปแบบ ER ได้ถูกสร้างขึ้นในรูปแบบการออกแบบตามโครงสร้างของเอกสาร MS Excel อ้างอิง (ช่วงที่มีชื่อ)</span><span class="sxs-lookup"><span data-stu-id="61f97-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="61f97-159">สร้างแหล่งข้อมูลใหม่เพื่อคำนวณผลรวมโดยรหัสสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="61f97-160">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="61f97-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="61f97-161">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="61f97-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="61f97-162">ในแผนภูมิ ให้เลือก 'ฟังก์ชัน\จัดกลุ่มโดย'</span><span class="sxs-lookup"><span data-stu-id="61f97-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="61f97-163">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงินในการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="61f97-164">สกุลเงินในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="61f97-165">คลิกแก้ไขกลุ่มโดย</span><span class="sxs-lookup"><span data-stu-id="61f97-165">Click Edit group by.</span></span>
6. <span data-ttu-id="61f97-166">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="61f97-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="61f97-167">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="61f97-168">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="61f97-168">Click Add field to.</span></span>
9. <span data-ttu-id="61f97-169">คลิกสิ่งที่จะจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="61f97-169">Click What to group.</span></span>
10. <span data-ttu-id="61f97-170">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="61f97-171">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="61f97-172">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="61f97-172">Click Add field to.</span></span>
13. <span data-ttu-id="61f97-173">คลิกฟิลด์ที่ถูกจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="61f97-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="61f97-174">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ยอดเงินที่แนะนำ(ยอดเงินที่แนะนำ)'</span><span class="sxs-lookup"><span data-stu-id="61f97-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="61f97-175">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="61f97-175">Click Add field to.</span></span>
16. <span data-ttu-id="61f97-176">คลิกฟิลด์การรวม</span><span class="sxs-lookup"><span data-stu-id="61f97-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="61f97-177">ในฟิลด์วิธีการ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="61f97-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="61f97-178">เลือกฟังก์ชันการรวม SUM</span><span class="sxs-lookup"><span data-stu-id="61f97-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="61f97-179">ในฟิลด์ชือ ให้พิมพ์ 'ยอดเงินที่แนะนำรวม'</span><span class="sxs-lookup"><span data-stu-id="61f97-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="61f97-180">ยอดเงินที่แนะนำรวม</span><span class="sxs-lookup"><span data-stu-id="61f97-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="61f97-181">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="61f97-181">Click Save.</span></span>
20. <span data-ttu-id="61f97-182">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-182">Close the page.</span></span>
21. <span data-ttu-id="61f97-183">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="61f97-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="61f97-184">แม็ปส่วนประกอบรูปแบบกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61f97-184">Map format components to data sources</span></span>
1. <span data-ttu-id="61f97-185">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="61f97-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="61f97-186">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="61f97-187">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\บัญชีเจ้าหนี้(บัญชีเจ้าหนี้)'</span><span class="sxs-lookup"><span data-stu-id="61f97-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="61f97-188">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ฝ่ายผู้สร้างข้อความ(ฝ่ายผู้สร้างข้อความ)\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="61f97-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="61f97-189">ในแผนภูมิ ขยาย 'Excel\ส่วนหัวรายงาน'</span><span class="sxs-lookup"><span data-stu-id="61f97-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="61f97-190">ในแผนภูมิ ให้เลือก 'Excel\ส่วนหัวรายงาน\ชื่อบริษัท'</span><span class="sxs-lookup"><span data-stu-id="61f97-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="61f97-191">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-191">Click Bind.</span></span>
8. <span data-ttu-id="61f97-192">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="61f97-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="61f97-193">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\การระบุรหัสประจำตัว'</span><span class="sxs-lookup"><span data-stu-id="61f97-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="61f97-194">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\การระบุรหัสประจำตัว\รหัสแหล่งข้อมูล(รหัสแหล่งข้อมูล)'</span><span class="sxs-lookup"><span data-stu-id="61f97-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="61f97-195">ในแผนภูมิ ขยาย 'Excel\รายการการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="61f97-196">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\ชื่อบัญชีผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="61f97-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="61f97-197">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-197">Click Bind.</span></span>
14. <span data-ttu-id="61f97-198">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระ\เจ้าหนี้\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="61f97-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="61f97-199">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\ชื่อผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="61f97-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="61f97-200">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-200">Click Bind.</span></span>
17. <span data-ttu-id="61f97-201">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="61f97-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="61f97-202">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ตัวแทนเจ้าหนี้(ตัวแทนเจ้าหนี้)\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="61f97-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="61f97-203">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="61f97-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="61f97-204">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-204">Click Bind.</span></span>
21. <span data-ttu-id="61f97-205">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ตัวแทนเจ้าหนี้(ตัวแทนเจ้าหนี้)\หมายเลขการกำหนดเส้นทาง(หมายเลขการกำหนดเส้นทาง)'</span><span class="sxs-lookup"><span data-stu-id="61f97-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="61f97-206">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="61f97-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="61f97-207">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-207">Click Bind.</span></span>
24. <span data-ttu-id="61f97-208">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="61f97-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="61f97-209">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)\Identification'</span><span class="sxs-lookup"><span data-stu-id="61f97-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="61f97-210">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\บัญชีเจ้าหนี้(บัญชีเจ้าหนี้)\การระบุรหัสประจำตัว\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="61f97-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="61f97-211">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\หมายเลขบัญชี'</span><span class="sxs-lookup"><span data-stu-id="61f97-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="61f97-212">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-212">Click Bind.</span></span>
29. <span data-ttu-id="61f97-213">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ยอดเงินที่แนะนำ(ยอดเงินที่แนะนำ)'</span><span class="sxs-lookup"><span data-stu-id="61f97-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="61f97-214">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\เดบิต'</span><span class="sxs-lookup"><span data-stu-id="61f97-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="61f97-215">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-215">Click Bind.</span></span>
32. <span data-ttu-id="61f97-216">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="61f97-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="61f97-217">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="61f97-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="61f97-218">ในแผนภูมิ ขยาย 'model\Payments\Creditor Account(CreditorAccount)'</span><span class="sxs-lookup"><span data-stu-id="61f97-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="61f97-219">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="61f97-220">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="61f97-221">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-221">Click Bind.</span></span>
38. <span data-ttu-id="61f97-222">ในแผนภูมิ ขยาย 'สกุลเงินในการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="61f97-223">ในแผนภูมิ ขยาย 'สกุลเงินในการชำระเงิน\จัดกลุ่มแล้ว'</span><span class="sxs-lookup"><span data-stu-id="61f97-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="61f97-224">ในแผนภูมิ เลือก 'สกุลเงินในการชำระเงิน\จัดกลุ่มแล้ว\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="61f97-225">ในแผนภูมิ ขยาย 'Excel\รายการสรุป'</span><span class="sxs-lookup"><span data-stu-id="61f97-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="61f97-226">ในแผนภูมิ ให้เลือก 'Excel\รายการสรุป\สกุลเงินสรุป'</span><span class="sxs-lookup"><span data-stu-id="61f97-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="61f97-227">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-227">Click Bind.</span></span>
44. <span data-ttu-id="61f97-228">ในแผนภูมิ ขยาย 'สกุลเงินในการชำระเงิน\รวมแล้ว'</span><span class="sxs-lookup"><span data-stu-id="61f97-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="61f97-229">ในแผนภูมิ เลือก 'สกุลเงินในการชำระเงิน\รวมแล้ว\ยอดเงินที่แนะนำรวม'</span><span class="sxs-lookup"><span data-stu-id="61f97-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="61f97-230">ในแผนภูมิ ให้เลือก 'Excel\รายการสรุป\จำนวนเงินสรุป'</span><span class="sxs-lookup"><span data-stu-id="61f97-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="61f97-231">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-231">Click Bind.</span></span>
48. <span data-ttu-id="61f97-232">ในแผนภูมิ ให้เลือก 'สกุลเงินในการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="61f97-233">ในแผนภูมิ ให้เลือก 'Excel\รายการสรุป'</span><span class="sxs-lookup"><span data-stu-id="61f97-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="61f97-234">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-234">Click Bind.</span></span>
51. <span data-ttu-id="61f97-235">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="61f97-236">ในแผนภูมิ ให้เลือก 'Excel\รายการการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="61f97-237">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="61f97-237">Click Bind.</span></span>
54. <span data-ttu-id="61f97-238">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="61f97-238">Click Save.</span></span>
55. <span data-ttu-id="61f97-239">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="61f97-240">ใช้การตั้งค่าคอนฟิกที่สร้างขึ้นสำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="61f97-241">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="61f97-241">Click Change status.</span></span>
2. <span data-ttu-id="61f97-242">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="61f97-242">Click Complete.</span></span>
3. <span data-ttu-id="61f97-243">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="61f97-243">Click OK.</span></span>
4. <span data-ttu-id="61f97-244">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-244">Close the page.</span></span>
5. <span data-ttu-id="61f97-245">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-245">Close the page.</span></span>
6. <span data-ttu-id="61f97-246">ไปที่บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="61f97-247">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์วิธีการชำระเงินด้วยค่า 'อิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="61f97-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="61f97-248">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="61f97-248">Electronic</span></span>  
8. <span data-ttu-id="61f97-249">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="61f97-249">Click Edit.</span></span>
9. <span data-ttu-id="61f97-250">ขยายส่วนรูปแบบของไฟล์</span><span class="sxs-lookup"><span data-stu-id="61f97-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="61f97-251">เลือก ใช่ ในฟิลด์รายงานอิเล็กทรอนิกส์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="61f97-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="61f97-252">ในฟิลด์การตั้งค่าคอนฟิกรูปแบบการส่งออก ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="61f97-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="61f97-253">เลือกการตั้งค่าคอนฟิก 'รายงานแผ่นงานตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="61f97-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="61f97-254">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="61f97-254">Click Save.</span></span>
13. <span data-ttu-id="61f97-255">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="61f97-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="61f97-256">ใช้การตั้งค่าคอนฟิกที่สร้างสำหรับการทดสอบการประมวลผลสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="61f97-257">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="61f97-258">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="61f97-258">Click New.</span></span>
    * <span data-ttu-id="61f97-259">สร้างสมุดรายวันการชำระเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="61f97-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="61f97-260">ในฟิลด์ชื่อ ให้พิมพ์ 'VendPay'</span><span class="sxs-lookup"><span data-stu-id="61f97-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="61f97-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="61f97-261">VendPay</span></span>  
4. <span data-ttu-id="61f97-262">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="61f97-262">Click Lines.</span></span>
5. <span data-ttu-id="61f97-263">ในฟิลด์บัญชี ให้ระบุค่า 'GB_SI_000001'</span><span class="sxs-lookup"><span data-stu-id="61f97-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="61f97-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="61f97-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="61f97-265">ตั้งค่าเดบิตเป็น '1000'</span><span class="sxs-lookup"><span data-stu-id="61f97-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="61f97-266">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="61f97-266">Click New.</span></span>
8. <span data-ttu-id="61f97-267">ในฟิลด์บัญชี ให้ระบุค่า 'GB_SI_000005'</span><span class="sxs-lookup"><span data-stu-id="61f97-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="61f97-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="61f97-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="61f97-269">ตั้งค่าเดบิตเป็น '2000'</span><span class="sxs-lookup"><span data-stu-id="61f97-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="61f97-270">ในฟิลด์สกุลเงิน ให้พิมพ์ 'EUR'</span><span class="sxs-lookup"><span data-stu-id="61f97-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="61f97-271">EUR</span><span class="sxs-lookup"><span data-stu-id="61f97-271">EUR</span></span>  
11. <span data-ttu-id="61f97-272">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่า 'GBSI OPER'</span><span class="sxs-lookup"><span data-stu-id="61f97-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="61f97-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="61f97-273">GBSI OPER</span></span>  
12. <span data-ttu-id="61f97-274">ในฟิลด์วิธีการชำระเงิน ให้พิมพ์ค่า 'อิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="61f97-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="61f97-275">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="61f97-275">Electronic</span></span>  
13. <span data-ttu-id="61f97-276">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="61f97-276">Click Save.</span></span>
14. <span data-ttu-id="61f97-277">คลิกสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-277">Click Generate payments.</span></span>
15. <span data-ttu-id="61f97-278">ในฟิลด์วิธีการชำระเงิน ให้พิมพ์ค่า 'อิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="61f97-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="61f97-279">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="61f97-279">Electronic</span></span>  
16. <span data-ttu-id="61f97-280">ในฟิลด์ชื่อไฟล์ พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="61f97-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="61f97-281">ตัวอย่างเช่น พิมพ์ การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="61f97-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="61f97-282">ในฟิลด์บัญชีธนาคาร ให้พิมพ์ 'GBSI OPER'</span><span class="sxs-lookup"><span data-stu-id="61f97-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="61f97-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="61f97-283">GBSI OPER</span></span>  
18. <span data-ttu-id="61f97-284">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="61f97-284">Click OK.</span></span>
19. <span data-ttu-id="61f97-285">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="61f97-285">Click OK.</span></span>
    * <span data-ttu-id="61f97-286">ตรวจทานแผ่นงานที่สร้าง ซึ่งรวมถึงรายละเอียดของรายการชำระเงิน และยอดรวมสำหรับรหัสสกุลเงินแต่ละรายการที่ใช้ในข้อความการชำระเงินนี้</span><span class="sxs-lookup"><span data-stu-id="61f97-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


