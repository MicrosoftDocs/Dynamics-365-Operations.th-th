---
title: ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML ของ ER (พฤศจิกายน 2016)
description: หัวข้อนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ใหม่ (ER) ซึ่งประกอบด้วยเท็มเพลตสำหรับการสร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ OPENXML
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea5b17873dea4508230f39ffb41a50e2f427584f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142143"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="2b510-103">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML ของ ER (พฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="2b510-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b510-104">หัวข้อนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ใหม่ (ER) ซึ่งประกอบด้วยเท็มเพลตสำหรับการสร้างเอกสารทางอิเล็กทรอนิกส์ในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="2b510-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="2b510-105">การตั้งค่าคอนฟิกนี้จะถูกใช้สำหรับการประมวลผลการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2b510-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="2b510-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง ซึ่งคือ Litware, Inc. ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัท GBSI </span><span class="sxs-lookup"><span data-stu-id="2b510-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="2b510-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2b510-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="2b510-108">คุณยังต้องมีไฟล์ Excel ซึ่งจะถูกนำเข้าเมื่อมีการสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="2b510-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="2b510-109">สามารถเข้าถึงไฟล์นี้ได้จาก [เท็มเพลตของรายงานการชำระเงิน](https://go.microsoft.com/fwlink/?linkid=862266)</span><span class="sxs-lookup"><span data-stu-id="2b510-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="2b510-110">อัพโหลดการตั้งค่าคอนฟิกแบบจำลองข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2b510-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="2b510-111">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="2b510-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="2b510-112">ในรายการ ให้ทำเครื่องหมายผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. หากคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ใน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md) ให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="2b510-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don't see this configuration provider, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="2b510-113">เลือก **กำหนดเป็นใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="2b510-113">Select **Set active**.</span></span>
4. <span data-ttu-id="2b510-114">เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="2b510-114">Select **Repositories**.</span></span> <span data-ttu-id="2b510-115">เลือกที่เก็บสำหรับชนิดทรัพยากรการดำเนินงาน ถ้าพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2b510-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="2b510-116">ถ้าพร้อมใช้งาน ให้ข้ามขั้นตอนต่อไปนี้เกี่ยวกับการสร้างที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="2b510-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="2b510-117">เลือก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2b510-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="2b510-118">ในฟิลด์ **ชนิดที่เก็บของการตั้งค่าคอนฟิก** ป้อน `Operations resourcesdd`</span><span class="sxs-lookup"><span data-stu-id="2b510-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="2b510-119">เลือก **สร้างที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="2b510-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="2b510-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b510-120">Select **OK**.</span></span>
9. <span data-ttu-id="2b510-121">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="2b510-121">Select **Open**.</span></span>
10. <span data-ttu-id="2b510-122">ในแผนภูมิ เลือก **แบบจำลองการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2b510-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="2b510-123">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="2b510-123">Select **Import**.</span></span> <span data-ttu-id="2b510-124">นำเข้าแบบจำลองข้มูลนี้</span><span class="sxs-lookup"><span data-stu-id="2b510-124">Import this data model.</span></span> <span data-ttu-id="2b510-125">ซึ่งจะถูกใช้เป็นแหล่งข้อมูลในการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="2b510-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="2b510-126">ให้ข้ามขั้นตอนนี้ถ้าการตั้งค่าคอนฟิกนี้ไดุถูกนำเข้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="2b510-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="2b510-127">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="2b510-127">Select **Yes**.</span></span>
13. <span data-ttu-id="2b510-128">ปิดหน้าที่จนกว่าคุณจะกลับไปที่หน้าการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="2b510-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="2b510-129">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="2b510-129">Create a new format configuration</span></span>
1. <span data-ttu-id="2b510-130">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="2b510-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="2b510-131">ในแผนภูมิ เลือก **แบบจำลองการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2b510-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="2b510-132">เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2b510-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="2b510-133">ในฟิลด์ **ใหม่** ป้อน `Format based on data model PaymentModel`</span><span class="sxs-lookup"><span data-stu-id="2b510-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="2b510-134">สร้างรูปแบบที่เป็นไปตามแบบจำลองข้อมูลของแบบจำลองการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2b510-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="2b510-135">ในฟิลด์ **ชื่อ** ให้พิมพ์ `Sample worksheet report`</span><span class="sxs-lookup"><span data-stu-id="2b510-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="2b510-136">รายงานแผ่นงานตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2b510-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="2b510-137">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ `Sample worksheet report for vendors' payments`.</span><span class="sxs-lookup"><span data-stu-id="2b510-137">In the **Description** field, type `Sample worksheet report for vendors' payments`.</span></span> <span data-ttu-id="2b510-138">รายงานแผ่นงานตัวอย่างสำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2b510-138">Sample worksheet report for vendors' payments.</span></span>  
7. <span data-ttu-id="2b510-139">ในฟิลด์ **คำนิยามแบบจำลองข้อมูล** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2b510-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="2b510-140">เลือกข้อกำหนด **การเริ่มต้นการโอนย้ายเครดิตของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="2b510-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="2b510-141">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="2b510-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="2b510-142">ออกแบบเอกสารใหม่ในรูปแบบแผ่นงาน OPENXML</span><span class="sxs-lookup"><span data-stu-id="2b510-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="2b510-143">ในแผนภูมิ เลือก **แบบจำลองการชำระเงิน\รายงานแผ่นงานตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="2b510-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="2b510-144">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="2b510-144">Select **Designer**.</span></span>
3. <span data-ttu-id="2b510-145">ในบานหน้าต่างการดำเนินการ เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="2b510-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="2b510-146">เลือก **นำเข้าจาก Excel**</span><span class="sxs-lookup"><span data-stu-id="2b510-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="2b510-147">เลือก **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="2b510-147">Select **Attachments**.</span></span> <span data-ttu-id="2b510-148">แนบเอกสาร Excel ที่มีอยู่เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="2b510-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="2b510-149">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2b510-149">Select **New**.</span></span>
7. <span data-ttu-id="2b510-150">เลือก **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="2b510-150">Select **File**.</span></span> <span data-ttu-id="2b510-151">ชี้ไปที่ไฟล์ Excel ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2b510-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="2b510-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2b510-152">Close the page.</span></span>
9. <span data-ttu-id="2b510-153">ในฟิลด์ **เท็มเพลต** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2b510-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="2b510-154">เลือกไฟล์ Excel ที่แนบมาเพื่อใช้เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="2b510-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="2b510-155">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b510-155">Select **OK**.</span></span> <span data-ttu-id="2b510-156">โปรดทราบว่าส่วนประกอบรูปแบบ ER ได้ถูกสร้างขึ้นในรูปแบบการออกแบบตามโครงสร้างของเอกสาร MS Excel อ้างอิง (ช่วงที่มีชื่อ)</span><span class="sxs-lookup"><span data-stu-id="2b510-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="2b510-157">สร้างแหล่งข้อมูลใหม่เพื่อคำนวณผลรวมโดยรหัสสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="2b510-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="2b510-158">เลือกแท็บ **การแมป**  </span><span class="sxs-lookup"><span data-stu-id="2b510-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="2b510-159">เลือก **เพิ่มราก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2b510-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="2b510-160">ในแผนภูมิ ให้เลือก **Functions\Group by**</span><span class="sxs-lookup"><span data-stu-id="2b510-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="2b510-161">ในฟิลด์ **ชื่อ** ให้พิมพ์ `PaymentByCurrency`</span><span class="sxs-lookup"><span data-stu-id="2b510-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="2b510-162">เลือก **แก้ไขกลุ่มโดย**</span><span class="sxs-lookup"><span data-stu-id="2b510-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="2b510-163">ในแผนภูมิ ขยาย **แบบจำลอง** จากนั้น เลือก **model\Payments**</span><span class="sxs-lookup"><span data-stu-id="2b510-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="2b510-164">เลือก **เพิ่มฟิลด์ไปยัง**</span><span class="sxs-lookup"><span data-stu-id="2b510-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="2b510-165">เลือก **สิ่งที่จะจัดกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="2b510-165">Select **What to group**.</span></span>
9. <span data-ttu-id="2b510-166">ในแผนภูมิ ขยาย **model\Payments** จากนั้น เลือก **model\Payments\Currency**</span><span class="sxs-lookup"><span data-stu-id="2b510-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="2b510-167">เลือก **เพิ่มฟิลด์ไปยัง**</span><span class="sxs-lookup"><span data-stu-id="2b510-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="2b510-168">เลือก **ฟิลด์ที่ถูกจัดกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="2b510-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="2b510-169">ในแผนภูมิ เลือก **model\Payments\Instructed Amount(InstructedAmount)**</span><span class="sxs-lookup"><span data-stu-id="2b510-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="2b510-170">เลือก **เพิ่มฟิลด์ไปยัง** แล้วเลือก **ฟิลด์การรวม**</span><span class="sxs-lookup"><span data-stu-id="2b510-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="2b510-171">ในฟิลด์ **วิธีการ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2b510-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="2b510-172">เลือกฟังก์ชัน **การรวม SUM**</span><span class="sxs-lookup"><span data-stu-id="2b510-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="2b510-173">ในฟิลด์ **ชื่อ** ให้พิมพ์ `TotalInstructuredAmount`</span><span class="sxs-lookup"><span data-stu-id="2b510-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="2b510-174">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2b510-174">Select **Save**.</span></span>
17. <span data-ttu-id="2b510-175">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2b510-175">Close the page.</span></span>
18. <span data-ttu-id="2b510-176">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b510-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="2b510-177">แม็ปส่วนประกอบรูปแบบกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b510-177">Map format components to data sources</span></span>
1. <span data-ttu-id="2b510-178">ในแผนภูมิ เลือก **model\Payments\Initiating Party(InitiatingParty)\Name** และ **Excel\ReportHeader\CompanyName**</span><span class="sxs-lookup"><span data-stu-id="2b510-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="2b510-179">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-179">Select **Bind**.</span></span>
3. <span data-ttu-id="2b510-180">ในแผนภูมิ เลือก **model\Payments\Creditor\Identification\Source ID(SourceID)** และ **Excel\PaymLines\VendAccountName**</span><span class="sxs-lookup"><span data-stu-id="2b510-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="2b510-181">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-181">Select **Bind**.</span></span>
5. <span data-ttu-id="2b510-182">ในแผนภูมิ ให้เลือก **model\Payments\Creditor\Name** และ **Excel\PaymLines\VendName**</span><span class="sxs-lookup"><span data-stu-id="2b510-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="2b510-183">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-183">Select **Bind**.</span></span>
7. <span data-ttu-id="2b510-184">ในแผนภูมิ ให้เลือก **model\Payments\Creditor Agent(CreditorAgent)\Name** และ **Excel\PaymLines\Bank**</span><span class="sxs-lookup"><span data-stu-id="2b510-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="2b510-185">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-185">Select **Bind**.</span></span>
9. <span data-ttu-id="2b510-186">ในแผนภูมิ ให้เลือก **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** และ **Excel\PaymLines\RoutingNumber**</span><span class="sxs-lookup"><span data-stu-id="2b510-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="2b510-187">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-187">Select **Bind**.</span></span>
11. <span data-ttu-id="2b510-188">ในแผนภูมิ เลือก **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** และ **Excel\PaymLines\AccountNumber**</span><span class="sxs-lookup"><span data-stu-id="2b510-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="2b510-189">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-189">Select **Bind**.</span></span>
13. <span data-ttu-id="2b510-190">ในแผนภูมิ เลือก **model\Payments\Instructed Amount(InstructedAmount)** และ **Excel\PaymLines\Debit**</span><span class="sxs-lookup"><span data-stu-id="2b510-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="2b510-191">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-191">Select **Bind**.</span></span>
15. <span data-ttu-id="2b510-192">ในแผนภูมิ เลือก **model\Payments\Currency** และ **Excel\PaymLines\Currency**</span><span class="sxs-lookup"><span data-stu-id="2b510-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="2b510-193">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-193">Select **Bind**.</span></span>
17. <span data-ttu-id="2b510-194">ในแผนภูมิ เลือก **PaymentByCurrency\grouped\Currency** และ **Excel\SummaryLines\SummaryCurrency**</span><span class="sxs-lookup"><span data-stu-id="2b510-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="2b510-195">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-195">Select **Bind**.</span></span>
19. <span data-ttu-id="2b510-196">ในแผนภูมิ เลือก **PaymentByCurrency\aggregated\TotalInstructuredAmount** และ **Excel\SummaryLines\SummaryAmount**</span><span class="sxs-lookup"><span data-stu-id="2b510-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="2b510-197">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-197">Select **Bind**.</span></span>
21. <span data-ttu-id="2b510-198">ในแผนภูมิ เลือก **PaymentByCurrency** และ **Excel\SummaryLines**</span><span class="sxs-lookup"><span data-stu-id="2b510-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="2b510-199">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-199">Select **Bind**.</span></span>
23. <span data-ttu-id="2b510-200">ในแผนภูมิ เลือก **model\Payments** และ **Excel\PaymLines**</span><span class="sxs-lookup"><span data-stu-id="2b510-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="2b510-201">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="2b510-201">Select **Bind**.</span></span>
25. <span data-ttu-id="2b510-202">เลือก **บันทึก** จากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2b510-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="2b510-203">ใช้การตั้งค่าคอนฟิกที่สร้างขึ้นสำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2b510-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="2b510-204">เลือก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="2b510-204">Select **Change status**.</span></span>
2. <span data-ttu-id="2b510-205">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="2b510-205">Select **Complete**.</span></span>
3. <span data-ttu-id="2b510-206">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b510-206">Select **OK**.</span></span>
4. <span data-ttu-id="2b510-207">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2b510-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="2b510-208">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์ **วิธีการชำระเงิน** ด้วยค่า **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="2b510-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="2b510-209">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="2b510-209">Select **Edit**.</span></span>
7. <span data-ttu-id="2b510-210">ขยายส่วน **รูปแบบของไฟล์**</span><span class="sxs-lookup"><span data-stu-id="2b510-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="2b510-211">เลือก **ใช่** ในฟิลด์ **รายงานทางอิเล็กทรอนิกส์ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="2b510-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="2b510-212">ในฟิลด์ **การตั้งค่าคอนฟิกรูปแบบการส่งออก** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2b510-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="2b510-213">เลือกการตั้งค่าคอนฟิก **รายงานแผ่นงานตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="2b510-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="2b510-214">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2b510-214">Select **Save**.</span></span>
11. <span data-ttu-id="2b510-215">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2b510-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="2b510-216">ใช้การตั้งค่าคอนฟิกที่สร้างสำหรับการทดสอบการประมวลผลสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2b510-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="2b510-217">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2b510-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="2b510-218">เลือก **ใหม่** เพื่อสร้างสมุดรายวันการชำระเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="2b510-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="2b510-219">ในฟิลด์ **ชื่อ** ให้พิมพ์ **VendPay**</span><span class="sxs-lookup"><span data-stu-id="2b510-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="2b510-220">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="2b510-220">Select **Lines**.</span></span>
5. <span data-ttu-id="2b510-221">ในฟิลด์ **บัญชี** ให้ระบุค่า `GB_SI_000001`</span><span class="sxs-lookup"><span data-stu-id="2b510-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="2b510-222">ตั้งค่า **เดบิต** เป็น `1000`</span><span class="sxs-lookup"><span data-stu-id="2b510-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="2b510-223">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2b510-223">Select **New**.</span></span>
8. <span data-ttu-id="2b510-224">ในฟิลด์ **บัญชี** ให้ระบุค่า `GB_SI_000005`</span><span class="sxs-lookup"><span data-stu-id="2b510-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="2b510-225">ตั้งค่า **เดบิต** เป็น `2000`</span><span class="sxs-lookup"><span data-stu-id="2b510-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="2b510-226">ในฟิลด์ **สกุลเงิน** ให้พิมพ์ `EUR`</span><span class="sxs-lookup"><span data-stu-id="2b510-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="2b510-227">ในฟิลด์ **บัญชีตรงข้าม** ระบุ ค่า `GBSI OPER`</span><span class="sxs-lookup"><span data-stu-id="2b510-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="2b510-228">ในฟิลด์ **วิธีการชำระเงิน** พิมพ์ `Electronic`</span><span class="sxs-lookup"><span data-stu-id="2b510-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="2b510-229">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2b510-229">Select **Save**.</span></span>
14. <span data-ttu-id="2b510-230">เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="2b510-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="2b510-231">ในฟิลด์ **วิธีการชำระเงิน** พิมพ์ `Electronic`</span><span class="sxs-lookup"><span data-stu-id="2b510-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="2b510-232">ในฟิลด์ **ชื่อไฟล์** พิมพ์ `Payments` </span><span class="sxs-lookup"><span data-stu-id="2b510-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="2b510-233">ในฟิลด์ **บัญชีธนาคาร** พิมพ์ `GBSI OPER`</span><span class="sxs-lookup"><span data-stu-id="2b510-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="2b510-234">เลือก **ตกลง** จากนั้น เลือก **ตกลง** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2b510-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="2b510-235">ตรวจทานแผ่นงานที่สร้าง ซึ่งรวมถึงรายละเอียดของรายการชำระเงิน และยอดรวมสำหรับรหัสสกุลเงินแต่ละรายการที่ใช้ในข้อความการชำระเงินนี้</span><span class="sxs-lookup"><span data-stu-id="2b510-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

