---
title: ใช้การตั้งค่าคอนฟิก ER กับเท็มเพลต Excel มาใช้ใหม่เพื่อสร้างรายงานในรูปแบบ Word
description: หัวข้อนี้จะอธิบายวิธีการออกแบบรูปแบบรายงานที่ออกแบบมาเพื่อสร้างรายงาน เมื่อสามารถตั้งค่าคอนฟิกสมุดงาน Excel ให้สร้างรายงานเป็นเอกสาร Word ได้
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769913fd0344eb276b3b1bd055255272ca5dfffd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092727"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="976d9-103">ใช้การตั้งค่าคอนฟิก ER กับเท็มเพลต Excel มาใช้ใหม่เพื่อสร้างรายงานในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="976d9-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="976d9-104">หากต้องการสร้างรายงานเป็นเอกสาร Microsoft Word คุณสามารถ [ตั้งค่าคอนฟิก](../er-design-configuration-word.md) [การรายงานทางอิเล็กทรอนิกส์ (ER)](../general-electronic-reporting.md) [รูปแบบ](../general-electronic-reporting.md#FormatComponentOutbound) ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="976d9-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="976d9-105">หรือ คุณสามารถใช้รูปแบบ ER ที่ออกแบบไว้ในตอนแรกเพื่อสร้างรายงานเป็นสมุดงาน Excel ได้</span><span class="sxs-lookup"><span data-stu-id="976d9-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="976d9-106">ในกรณีนี้ คุณต้องแทนที่เท็มเพลต Excel ด้วยเท็มเพลต Word</span><span class="sxs-lookup"><span data-stu-id="976d9-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="976d9-107">กระบวนงานต่อไปนี้แสดงวิธีการที่ผู้ใช้ที่มีบทบาทเป็นผู้ดูแลระบบหรือบทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถตั้งค่าคอนฟิกรูปแบบ ER เพื่อสร้างรายงานเป็นไฟล์ Word โดยการใช้รูปแบบ ER ใหม่ ที่ออกแบบมาเพื่อสร้างรายงานเป็นไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="976d9-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="976d9-108">คุณสามารถดำเนินการกระบวนงานเหล่านี้ให้เสร็จสมบูรณ์ได้ในบริษัท GBSI</span><span class="sxs-lookup"><span data-stu-id="976d9-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="976d9-109">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="976d9-109">Prerequisites</span></span>

<span data-ttu-id="976d9-110">เพื่อทำขั้นตอนในกระบวนงานนี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำตามขั้นตอนใน คู่มืองาน [ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML](er-design-reports-openxml-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="976d9-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="976d9-111">คุณยังต้องดาวน์โหลดและบันทึกเท็มเพลตต่อไปนี้ไว้ภายในเครื่อง สำหรับรายงานตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="976d9-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="976d9-112">เท็มเพลตของรายงานการชำระเงิน (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="976d9-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="976d9-113">เท็มเพลตที่กำหนดขอบเขตของรายงานการชำระเงิน (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="976d9-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="976d9-114">กระบวนงานเหล่านี้ใช้เฉพาะกับคุณลักษณะที่ถูกเพิ่มใน Dynamics 365 for Operations เวอร์ชัน 1611 (พฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="976d9-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="976d9-115">เลือกการตั้งค่าคอนฟิกรายงาน ER ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="976d9-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="976d9-116">ใน Dynamics 365 Finance ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="976d9-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="976d9-117">ตรวจสอบให้แน่ใจว่ามีการเลือกให้ผู้ให้บริการการตั้งค่าคอนฟิก **Litware, Inc.** เป็น **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="976d9-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="976d9-118">ถ้าไม่มี ให้ปฏิบัติตามขั้นตอนใน คู่มืองาน [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="976d9-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="976d9-119">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="976d9-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="976d9-120">คุณจะใช้การตั้งค่าคอนฟิก ER ที่มีอยู่ ซึ่งได้รับการออกแบบเพื่อสร้างเอาท์พุทรายงานในรูปแบบ OPENXML อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="976d9-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="976d9-121">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองการชำระเงิน** และเลือก **รายงานเวิร์กชีตตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="976d9-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="976d9-122">เวอร์ชันแบบร่างของรูปแบบ ER ที่เลือก สามารถแก้ไขได้บนแท็บด่วน **เวอร์ชัน**</span><span class="sxs-lookup"><span data-stu-id="976d9-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="976d9-123">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="976d9-123">Select **Designer**.</span></span>
6. <span data-ttu-id="976d9-124">ในหน้า **ตัวออกแบบรูปแบบ** ให้สังเกตว่าชื่อขององค์ประกอบรูปแบบรากบ่งชี้ว่ามีการใช้เท็มเพลต Excel อยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="976d9-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![การเลือกการตั้งค่าคอนฟิกที่มีอยู่](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="976d9-126">ตรวจทานเท็มเพลต Word ที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="976d9-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="976d9-127">ในแอพลิเคชันบนเดสก์ท็อปของ Word ให้เปิดไฟล์เท็มเพลต **SampleVendPaymDocReport.docx** ที่คุณดาวน์โหลดก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="976d9-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="976d9-128">ตรวจสอบว่าเท็มเพลตประกอบด้วยโครงร่างของเอกสารที่คุณต้องการสร้างเป็นเอาท์พุท ER เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="976d9-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![โครงร่างเท็มเพลต Word ในแอพลิเคชันบนเดสก์ทอป](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="976d9-130">แทนที่เท็มเพลต Excel ด้วยเท็มเพลต Word และเพิ่มส่วน XML แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="976d9-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="976d9-131">ปัจจุบัน เอกสาร Excel จะใช้เป็นเท็มเพลตเพื่อสร้างเอาท์พุทในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="976d9-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="976d9-132">คุณจะแทนที่เท็มเพลตนี้ ด้วยไฟล์เท็มเพลต Word ชื่อ SampleVendPaymDocReport.docx ที่คุณดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="976d9-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="976d9-133">คุณยังจะขยายเท็มเพลต Word โดยการเพิ่มส่วน XML แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="976d9-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="976d9-134">ใน Finance บนหน้า **ตัวออกแบบรูปแบบ** บนแท็บ **รูปแบบ** ให้เลือก **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="976d9-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="976d9-135">บนหน้า **เอกสารแนบ** ให้เลือก **ลบ** เพื่อลบเท็มเพลต Excel ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="976d9-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="976d9-136">เลือก **ใช่** เพื่อยืนยันการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="976d9-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="976d9-137">เลือก **ใหม่** \> **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="976d9-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="976d9-138">คุณต้องเลือกชนิดเอกสารที่มีการ [ตั้งค่าคอนฟิก](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ในพารามิเตอร์ ER เพื่อจัดเก็บเท็มเพลตของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="976d9-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="976d9-139">เลือก **เลือกดู** แล้วเลือกดู และเลือกไฟล์ **SampleVendPaymDocReport.docx** ที่คุณดาวน์โหลดก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="976d9-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="976d9-140">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="976d9-140">Select **OK**.</span></span>
6. <span data-ttu-id="976d9-141">ปิดหน้า **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="976d9-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="976d9-142">ในหน้า **โปรแกรมออกแบบรูปแบบ** ในฟิลด์ **เท็มเพลต** ให้ป้อนหรือเลือกไฟล์ **SampleVendPaymDocReport.docx** เพื่อใช้เท็มเพลต Word นั้นแทนเท็มเพลต Excel ที่ใช้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="976d9-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="976d9-143">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="976d9-143">Select **Save**.</span></span>

    <span data-ttu-id="976d9-144">นอกจากจะเก็บข้อมูลการเปลี่ยนแปลงการตั้งค่าคอนฟิก การดำเนินการ **บันทึก** ยังเป็นการอัปเดตเท็มเพลต Word ที่แนบอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="976d9-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="976d9-145">โครงสร้างตามลำดับของรูปแบบที่ได้รับการออกแบบมาถูกเพิ่มไปยังเอกสาร Word ที่แนบ เป็นส่วน XML แบบกำหนดเองใหม่ ที่มีชื่อว่า **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="976d9-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="976d9-146">เท็มเพลต Word ที่แนบมีโครงร่างของเอกสารที่จะสร้างเป็นเอาท์พุท ER และโครงสร้างของข้อมูลที่ ER จะป้อนลงในเท็มเพลตนี้ขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="976d9-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="976d9-147">ให้สังเกตว่าชื่อขององค์ประกอบรูปแบบรากบ่งชี้ว่ามีการใช้เท็มเพลต Word อยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="976d9-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![การแทนที่เท็มเพลต Excel ด้วยเท็มเพลต Word และการเพิ่มส่วน XML แบบกำหนดเอง](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="976d9-149">บนแท็บ **รูปแบบ** ให้เลือก **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="976d9-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="976d9-150">ตอนนี้คุณสามารถแม็ปองค์ประกอบของส่วน XML **รายงาน** แบบกำหนดเองให้กับตัวควบคุมเนื้อหาของเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="976d9-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="976d9-151">ถ้าคุณคุ้นเคยกับกระบวนการของการออกแบบเอกสาร Word ที่เป็นแบบฟอร์มที่มี [ตัวควบคุมเนื้อหา](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) ซึ่งถูกแม็บกับองค์ประกอบของ [ส่วน XML แบบกำหนดเอง](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) ดำเนินการขั้นตอนทั้งหมดในกระบวนงานถัดไปให้เสร็จสิ้น เพื่อสร้างเอกสาร</span><span class="sxs-lookup"><span data-stu-id="976d9-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="976d9-152">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างฟอร์มที่ผู้ใช้ดำเนินการให้เสร็จสิ้นหรือพิมพ์ใน Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b)</span><span class="sxs-lookup"><span data-stu-id="976d9-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="976d9-153">มิฉะนั้น ข้ามกระบวนงานถัดไป</span><span class="sxs-lookup"><span data-stu-id="976d9-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="976d9-154">รับเอกสาร Word ที่มีส่วน XML แบบกำหนดเอง และแม็ปข้อมูล</span><span class="sxs-lookup"><span data-stu-id="976d9-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="976d9-155">ใน Finance บนหน้า **เอกสารแนบ** ให้เลือก **เปิด** เพื่อดาวน์โหลดเท็มเพลตที่เลือกจาก Finance และจัดเก็บเป็นเอกสาร Word ไว้ในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="976d9-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="976d9-156">ในแอพลิเคชันบนเดสก์ท็อปของ Word ให้เปิดเอกสารที่คุณดาวน์โหลดมา</span><span class="sxs-lookup"><span data-stu-id="976d9-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="976d9-157">บนแท็บ **นักพัฒนา** ให้เลือก **บานหน้าต่างการแม็ป XML**</span><span class="sxs-lookup"><span data-stu-id="976d9-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="976d9-158">ถ้าแท็บ **นักพัฒนา** ไม่ปรากฏบน Ribbon ให้เลือกปรับแต่ง Ribbon เพื่อเพิ่มแท็บนั้น</span><span class="sxs-lookup"><span data-stu-id="976d9-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="976d9-159">ในบานหน้าต่าง **การแม็ป XML** ในฟิลด์ **ส่วน XML แบบกำหนดเอง** ให้เลือก ส่วน XML แบบกำหนดเองของ **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="976d9-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="976d9-160">แม็ปองค์ประกอบของส่วน XML แบบกำหนดเองของ **รายงาน** ที่เลือก และตัวควบคุมเนื้อหาของเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="976d9-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="976d9-161">บันทึกเอกสาร Word ที่อัปเดตไว้ในเครื่อง เป็น **SampleVendPaymDocReportBounded.docx**</span><span class="sxs-lookup"><span data-stu-id="976d9-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="976d9-162">ตรวจสอบเท็มเพลต Word ที่มีการแม็ปส่วน XML แบบกำหนดเอง กับตัวควบคุมเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="976d9-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="976d9-163">ในแอพลิเคชันบนเดสก์ท็อปของ Word ให้เปิดไฟล์เท็มเพลต **SampleVendPaymDocReportBounded.docx**</span><span class="sxs-lookup"><span data-stu-id="976d9-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="976d9-164">ตรวจสอบว่าเท็มเพลตประกอบด้วยโครงร่างของเอกสารที่คุณต้องการสร้างเป็นเอาท์พุท ER เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="976d9-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="976d9-165">ตัวควบคุมเนื้อหาที่ใช้เป็นตัวยึดตัวยึดข้อมูลซึ่ง ER จะป้อนในเท็มเพลตนี้เมื่อรันไทม์ จะขึ้นอยู่กับการแม็ปที่มีการตั้งค่าคอนฟิกระหว่างองค์ประกอบของส่วน XML ที่กําหนดเองของ **รายงาน** และตัวควบคุมเนื้อหาของเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="976d9-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![แสดงตัวอย่างเท็มเพลต Word ในแอพลิเคชันบนเดสก์ทอป](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="976d9-167">อัปโหลดเท็มเพลต Word ที่มีการแม็ปส่วน XML แบบกำหนดเองกับตัวควบคุมเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="976d9-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="976d9-168">ใน Finance บนหน้า **เอกสารแนบ** ให้เลือก **ลบ** เพื่อลบเท็มเพลต Word ที่ไม่มีการแม็ประหว่างองค์ประกอบของส่วน XML แบบกำหนดเองของ **รายงาน** และตัวควบคุมเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="976d9-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="976d9-169">เลือก **ใช่** เพื่อยืนยันการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="976d9-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="976d9-170">เลือก **ใหม่** \> **ไฟล์** เพื่อเพิ่มไฟล์เท็มเพลตใหม่ ที่มีการแม็ประหว่างองค์ประกอบของส่วน XML แบบกำหนดเองของ **รายงาน** และตัวควบคุมเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="976d9-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="976d9-171">คุณต้องเลือกชนิดเอกสารที่มีการ [ตั้งค่าคอนฟิก](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ในพารามิเตอร์ ER เพื่อจัดเก็บเท็มเพลตของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="976d9-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="976d9-172">เลือก **เลือกดู** แล้วเลือกดู และเลือกไฟล์ **SampleVendPaymDocReportBounded.docx** ที่คุณดาวน์โหลดหรือจัดเตรียมไว้ โดยการทํากระบวนงานในส่วน [รับ Word ที่มีส่วน XML แบบกำหนดเอง เพื่อแม็บข้อมูล](#get-word-doc)</span><span class="sxs-lookup"><span data-stu-id="976d9-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="976d9-173">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="976d9-173">Select **OK**.</span></span>
5. <span data-ttu-id="976d9-174">ปิดหน้า **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="976d9-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="976d9-175">ในหน้า **โปรแกรมออกแบบรูปแบบ** ในฟิลด์ **เท็มเพลต** ให้เลือกเอกสารที่คุณเพิ่งดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="976d9-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="976d9-176">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="976d9-176">Select **Save**.</span></span>
8. <span data-ttu-id="976d9-177">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="976d9-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="976d9-178">ทำเครื่องหมายรูปแบบที่ตั้งค่าคอนฟิกเป็นรันได้</span><span class="sxs-lookup"><span data-stu-id="976d9-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="976d9-179">เมื่อต้องการรันเวอร์ชันแบบร่างของรูปแบบที่แก้ไขได้ คุณต้องตั้งค่า [ให้รันได้](../er-quick-start2-customize-report.md#MarkFormatRunnable)</span><span class="sxs-lookup"><span data-stu-id="976d9-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="976d9-180">ใน Finance บนหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="976d9-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="976d9-181">ในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ให้ตั้งค่าตัวเลือก **เรียกใช้การตั้งค่า** เป็น **ใช่** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="976d9-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="976d9-182">ให้เลือก **แก้ไข้** เพื่อทำให้หน้าปัจจุบันพร้อมสำหรับการแก้ไข หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="976d9-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="976d9-183">สำหรับการตั้งค่าคอนฟิก **รายงานเวิร์กชีตตัวอย่าง** ที่เลือกในปัจจุบัน ให้ตั้งค่าตัวเลือก **รันแบบร่าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="976d9-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="976d9-184">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="976d9-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="976d9-185">รันรูปแบบเพื่อสร้างผลลัพธ์ในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="976d9-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="976d9-186">ใน Finance ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="976d9-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="976d9-187">ในสมุดรายวันการชำระเงินที่คุณป้อนไว้ก่อนหน้านี้ ให้เลือก **บรรทัด**</span><span class="sxs-lookup"><span data-stu-id="976d9-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="976d9-188">บนหน้า **การชำระเงินให้แก่ผู้จัดจำหน่าย** ให้เลือกแถวทั้งหมดในกริด</span><span class="sxs-lookup"><span data-stu-id="976d9-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="976d9-189">เลือก **สถานะการชำระเงิน** \> **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="976d9-189">Select **Payment status** \> **None**.</span></span>

    ![การชําระเงินสำหรับการดำเนินการ บนหน้าการชําระเงินให้แก่ผู้จัดจําหน่าย](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="976d9-191">ในบานหน้าต่างการดำเนินการ เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="976d9-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="976d9-192">ในกล่องโต้ตอบที่ปรากฎขึ้น ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="976d9-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="976d9-193">เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="976d9-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="976d9-194">ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="976d9-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="976d9-195">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="976d9-195">Select **OK**.</span></span>

7. <span data-ttu-id="976d9-196">ในกล่องโต้ตอบ **พารามิเตอร์ของรายงานทางอิเล็กทรอนิกส์** เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="976d9-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="976d9-197">ผลลัพธ์ที่สร้างขึ้นจะแสดงในรูปแบบ Word และประกอบด้วยรายละเอียดเกี่ยวกับการชำระเงินที่ประมวลผลแล้ว</span><span class="sxs-lookup"><span data-stu-id="976d9-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="976d9-198">วิเคราะห์ผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="976d9-198">Analyze the generated output.</span></span>

    ![ผลลัพธ์ที่สร้างขึ้นในรูปแบบ Word](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="976d9-200">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="976d9-200">Additional resources</span></span>

- [<span data-ttu-id="976d9-201">ออกแบบการตั้งค่าคอนฟิก ER ใหม่ เพื่อสร้างรายงานในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="976d9-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="976d9-202">ฝังข้อมูลและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER</span><span class="sxs-lookup"><span data-stu-id="976d9-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)
