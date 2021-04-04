---
title: ระงับการควบคุมเนื้อหา Word ในรายงานที่สร้างขึ้น
description: หัวข้อนี้อธิบายวิธีการกำหนดค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์ Microsoft Word ที่ถูกระงับตัวควบคุมเนื้อหา
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562129"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="a793d-103">ระงับการควบคุมเนื้อหา Word ในรายงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a793d-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a793d-104">เพื่อสร้างรายงานเป็นเอกสาร Microsoft Word คุณต้องออกแบบเท็มเพลตให้กับรายงานเป็นเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="a793d-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="a793d-105">เท็มเพลตนี้ต้องมีตัวควบคุมเนื้อหา Word เป็นตัวยึดข้อมูลซึ่งจะถูกเติมขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="a793d-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="a793d-106">ในการใช้เอกสาร Word ที่สร้างเป็นเท็มเพลตของรายงานของคุณ คุณจะสามารถ [กำหนดค่าคอนฟิก](er-design-configuration-word.md) [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) [โซลูชัน](er-quick-start1-new-solution.md) ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="a793d-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="a793d-107">โซลูชันี้ต้องมี [การกำหนดค่าคอนฟิก](general-electronic-reporting.md#Configuration) ที่มีส่วนประกอบ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) ของ ER</span><span class="sxs-lookup"><span data-stu-id="a793d-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="a793d-108">ต้องกำหนดค่าคอนฟิกรูปแบบ ER นี้เพื่อใช้เท็มเพลตที่ออกแบบไว้ในการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="a793d-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="a793d-109">ในเวอร์ชัน 10.0.6 และเวอร์ชันต่อมาของ Dynamics 365 Finance คุณสามารถกำหนดค่าคอนฟิกสูตรในรูปแบบ ER ของคุณเพื่อระงับการควบคุมเนื้อหา Word บางรายการในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a793d-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="a793d-110">ขั้นตอนต่อไปนี้จะอธิบายว่าผู้ใช้ที่ได้รับมอบหมายให้เป็นผู้ดูแลระบบหรือบทบาทที่ปรึกษาด้านฟังก์ชันการรายงานทางอิเล็กทรอนิกส์จะสามารถกำหนดค่ารูปแบบ ER ที่สร้างรายงานเป็นไฟล์ Word และยับยั้งการควบคุมเนื้อหาบางส่วนในรายงานที่สร้างขึ้นซึ่งได้รับการกำหนดค่าโดยใช้เท็มเพลต Word ได้</span><span class="sxs-lookup"><span data-stu-id="a793d-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="a793d-111">คุณสามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท GBSI</span><span class="sxs-lookup"><span data-stu-id="a793d-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a793d-112">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a793d-112">Prerequisites</span></span>

<span data-ttu-id="a793d-113">เพื่อทำตามขั้นตอนเหล่านี้ คุณต้องดำเนินการตามคำแนะนำงานสามรายการนี้ก่อน</span><span class="sxs-lookup"><span data-stu-id="a793d-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="a793d-114">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="a793d-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="a793d-115">นำการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ที่มีเท็มเพลต Excel มาใช้ใหม่เพื่อสร้างรายงานในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="a793d-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="a793d-116">เมื่อคุณทําขั้นตอนของคู่มืองานนี้แล้ว รายการต่อไปนี้จะถูกจัดเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="a793d-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="a793d-117">รูปแบบ ER ของ **รายงานแผ่นงานตัวอย่าง** ที่ถูกกำหนดค่าคอนฟิกให้สร้างเอกสารในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="a793d-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="a793d-118">เวอร์ชัน [แบบร่าง](general-electronic-reporting.md#component-versioning) ของรูปแบบ ER **รายงานแผ่นงานตัวอย่าง** ที่ทำเครื่องหมายเป็น **รันได้**</span><span class="sxs-lookup"><span data-stu-id="a793d-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="a793d-119">วิธีการจ่ายเงินแบบ **อิเล็กทรอนิกส์** ที่ถูกกำหนดค่าคอนฟิกให้ใช้รูปแบบ ER ของ **รายงานแผ่นงานตัวอย่าง** เพื่อการดำเนินการจ่ายเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a793d-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="a793d-120">คุณยังต้องดาวน์โหลดและบันทึกเท็มเพลตต่อไปนี้สำหรับรายงานตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a793d-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="a793d-121">เท็มเพลตถูกผูกไว้ 2 ของรายงานการชำระเงิน (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="a793d-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="a793d-122">ตรวจทานเท็มเพลต Word ที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="a793d-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="a793d-123">ในแอพลิเคชันบนเดสก์ท็อปของ Word ให้เปิดไฟล์เท็มเพลต **SampleVendPaymDocReportBounded2.docx** ที่คุณได้ดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a793d-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="a793d-124">ตรวจสอบว่าไฟล์เท็มเพลตมีส่วนสรุปที่แสดงยอดการชำระเงินรวมของทุกรหัสสกุลเงินซึ่งตรงตามการชำระเงินที่ดำเนินการแล้ว</span><span class="sxs-lookup"><span data-stu-id="a793d-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="a793d-125">ส่วนสรุปจะอยู่ในตารางแยกต่างหากของเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="a793d-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="a793d-126">แถวแรกของตารางนี้จะถือส่วนหัวคอลัมน์ของตารางเป็นส่วนหัวของส่วน</span><span class="sxs-lookup"><span data-stu-id="a793d-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="a793d-127">แถวที่สองของตารางนี้จะถือตัวควบคุมเนื้อหาที่ทําซ้ำเป็นรายละเอียดของส่วน</span><span class="sxs-lookup"><span data-stu-id="a793d-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="a793d-128">ตัวควบคุมเนื้อหานี้จะถูกแม็ปกับเขตข้อมูล **SummaryLines** ของส่วน **รายงาน** XML ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a793d-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="a793d-129">ตามการแม็ปนี้ ตัวควบคุมเนื้อหาจะเชื่อมโยงกับองค์ประกอบ **SummaryLines** ของรูปแบบ ER ที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a793d-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a793d-130">ตัวควบคุมเนื้อหาการทําซ้ำจะถูกแท็กโดยคีย์ **SummaryLines** ที่ตรงกับเขตข้อมูลของส่วน XML ที่ศุลกากรซึ่งได้รับการแม็ป</span><span class="sxs-lookup"><span data-stu-id="a793d-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![เค้าโครงเทมเพลต Word ](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="a793d-132">เลือกการตั้งค่าคอนฟิกรายงาน ER ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a793d-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="a793d-133">สำหรับขั้นตอนต่อไปนี้ คุณจะสามารถนำการกำหนดค่าคอนฟิกของ ER ที่คุณกำหนดไว้กลับมาใช้ใหม่เมื่อคุณทำตามขั้นตอนในคู่มืองานที่กล่าวถึงก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="a793d-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="a793d-134">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a793d-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="a793d-135">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="a793d-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a793d-136">บนหน้า **การกำหนดค่าคอนฟิก** ในแผนภูมิการกำหนดค่าคอนฟิก ให้ขยาย **แบบจำลองการชำระเงิน** และเลือก **รายงานแผ่นงานตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="a793d-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="a793d-137">เลือก **ตัวออกแบบ** เพื่อแก้ไขเวอร์ชันแบบร่างของรูปแบบ ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a793d-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="a793d-138">แทนที่เท็มเพลตปัจจุบันด้วยเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="a793d-138">Replace the current template with the new template</span></span>

<span data-ttu-id="a793d-139">ปัจจุบัน ไฟล์ SampleVendPaymDocReportBounded.docx จะถูกนำไปใช้เป็นเท็มเพลตเพื่อสร้างชิ้นงานในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="a793d-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="a793d-140">ในขั้นตอนต่อไปนี้ คุณจะสามารถแทนที่เทมเพลต Word นี้ด้วยเทมเพลต Word ใหม่ SampleVendPaymDocReportBounded2.docx ที่คุณดาวน์โหลดไว้ก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="a793d-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="a793d-141">บหน้า **ตัวออกแบบรูปแบบ** เลือก **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="a793d-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="a793d-142">บนหน้า **เอกสารแนบ** ให้เลือก **ลบ** เพื่อลบเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a793d-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="a793d-143">เลือก **ใช่** เพื่อยืนยันการลบ</span><span class="sxs-lookup"><span data-stu-id="a793d-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="a793d-144">เลือก **ใหม่** \> **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="a793d-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="a793d-145">เลือก **เรียกดู** แล้วเรียกดูและเลือกไฟล์ **SampleVendPaymDocReportBounded2.docx** ที่คุณดาวน์โหลดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a793d-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="a793d-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a793d-146">Select **OK**.</span></span>
7. <span data-ttu-id="a793d-147">ปิดหน้า **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="a793d-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="a793d-148">บหน้า **ตัวออกแบบรูปแบบ** ในเขตข้อมูล **เทมเพลต** ให้ป้อนหรือเลือกไฟล์ **SampleVendPaymDocReportBounded2.docx**</span><span class="sxs-lookup"><span data-stu-id="a793d-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="a793d-149">ดำเนินการรูปแบบเพื่อสร้างชิ้นงานของ Word</span><span class="sxs-lookup"><span data-stu-id="a793d-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="a793d-150">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="a793d-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="a793d-151">บนหน้า **การจ่ายเงินของผู้จัดจำหน่าย** บนแท็บ **รายการ** ให้เลือกการจ่ายเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a793d-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="a793d-152">เลือก **สถานะการชำระเงิน** \> **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="a793d-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="a793d-153">เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="a793d-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="a793d-154">เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a793d-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="a793d-155">ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="a793d-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="a793d-156">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a793d-156">Select **OK**.</span></span>
8. <span data-ttu-id="a793d-157">ในกล่องโต้ตอบ **พารามิเตอร์รายงานอิเล็กทรอนิกส์** ให้เลือก **ตกลง** และวิเคราะห์ผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a793d-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![การชําระเงินสำหรับการดำเนินการ บนหน้าการชําระเงินให้แก่ผู้จัดจําหน่าย](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="a793d-159">ผลลัพธ์จะแสดงในรูปแบบ Word และมีส่วนสรุปด้วย</span><span class="sxs-lookup"><span data-stu-id="a793d-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="a793d-160">กำหนดค่าคอนฟิกรูปแบบที่แก้ไขได้เพื่อระงับส่วนสรุป</span><span class="sxs-lookup"><span data-stu-id="a793d-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="a793d-161">ถ้าคุณต้องการระงับส่วนสรุปในเอกสารที่สร้างขึ้น ตามการร้องขอของผู้ใช้ที่รันรูปแบบ ER นี้ คุณต้องแก้ไขรูปแบบ ER ที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a793d-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="a793d-162">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์** และเปิดเวอร์ชันแบบร่างของรูปแบบ ER เพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a793d-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="a793d-163">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="a793d-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="a793d-164">บนหน้า **การกำหนดค่าคอนฟิก** ในแผนภูมิการกำหนดค่าคอนฟิก ให้ขยาย **แบบจำลองการชำระเงิน** \> **รายงานแผ่นงานตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="a793d-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="a793d-165">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="a793d-165">Select **Designer**.</span></span>
5. <span data-ttu-id="a793d-166">บนหน้า **ตัวออกแบบรูปแบบ** ให้ขยาย **Word** และเลือก **SummaryLines**</span><span class="sxs-lookup"><span data-stu-id="a793d-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="a793d-167">บนแท็บ **การแม็ป** ให้เพิ่มแหล่งข้อมูลใหม่เพื่อถามผู้ใช้ขณะรันไทม์ว่าควรระงับส่วนสรุปหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a793d-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="a793d-168">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="a793d-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="a793d-169">ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ให้เลือก **อินพุทพารามิเตอร์ทั่วไป\ผู้ใช้** เพื่อเปิดกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'ผู้ใช้อินพุทพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a793d-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="a793d-170">ในเขตข้อมูล **ชื่อ** ให้ป้อน **uipSuppress**</span><span class="sxs-lookup"><span data-stu-id="a793d-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="a793d-171">ในเขตข้อมูล **ป้ายชื่อ** ให้ป้อน **ส่วนระงับการสรุป**</span><span class="sxs-lookup"><span data-stu-id="a793d-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="a793d-172">ในเขตข้อมูล **ชื่อชนิดข้อมูลการดําเนินงาน** ให้เลือกหรือป้อน **NoYes**</span><span class="sxs-lookup"><span data-stu-id="a793d-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="a793d-173">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a793d-173">Select **OK**.</span></span>

7. <span data-ttu-id="a793d-174">เพิ่มแหล่งข้อมูลใหม่ของชนิดประเภทการแจงนับแอปพลิเคชัน **NoYes**</span><span class="sxs-lookup"><span data-stu-id="a793d-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="a793d-175">เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="a793d-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="a793d-176">ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ให้เลือก **Dynamics 365 for Operations\การแจงนับ** เพื่อเปิดกล่องโต้ตอบ **คุณสมบัติการแจงนับแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a793d-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="a793d-177">ในเขตข้อมูล **ชื่อ** ให้ป้อน **enumNoYes**</span><span class="sxs-lookup"><span data-stu-id="a793d-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="a793d-178">ในเขตข้อมูล **ป้ายชื่อ** ให้ป้อน **ตัวเลือกการระงับ**</span><span class="sxs-lookup"><span data-stu-id="a793d-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="a793d-179">ในเขตข้อมูล **ชื่อชนิดข้อมูลการดําเนินงาน** ให้เลือกหรือป้อน **NoYes**</span><span class="sxs-lookup"><span data-stu-id="a793d-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="a793d-180">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a793d-180">Select **OK**.</span></span>

8. <span data-ttu-id="a793d-181">สำหรับส่วนประกอบรูปแบบที่ถูกเลือก **SummaryLines** กำหนดค่าสูตรเพื่อระบุว่าเมื่อใดควรระงับการควบคุมเนื้อหา Word ที่เชื่อมโยงกับองค์ประกอบรูปแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a793d-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="a793d-182">บนแท็บ **การแม็ป** ในส่วน **ลบ** ให้เลือก **แก้ไข** เพื่อเปิดหน้า **[ผู้ออกแบบสูตร](general-electronic-reporting-formula-designer.md)**</span><span class="sxs-lookup"><span data-stu-id="a793d-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="a793d-183">ในเขตข้อมูล **สูตร** ให้ป้อนสูตร `uipSuppress = enumNoYes.Yes`</span><span class="sxs-lookup"><span data-stu-id="a793d-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="a793d-184">เลือก **บันทึก** และปิดหน้า **ตัวออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="a793d-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a793d-185">สูตรนี้จะถูกนำไปใช้กับเอกสารที่สร้างขึ้น **หลังจากที่รันองค์ประกอบรูปแบบอื่นทั้งหมดแล้ว**</span><span class="sxs-lookup"><span data-stu-id="a793d-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="a793d-186">เมื่อต้องการใช้สูตรนี้ ตัวควบคุมเนื้อหา Word ที่มีถูกแท็กเป็นองค์ประกอบรูปแบบที่มีการกำหนดค่าคอนฟิกสูตรไว้สำหรับ (**SummaryLines** ในกรณีนี้) จะพบไดในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a793d-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="a793d-187">ตัวควบคุมเนื้อหานั้นจะถูกลบออกโดยสมบูรณ์ พร้อมกับแถวในตาราง Word ที่ระงับการควบคุมเนื้อหานั้น</span><span class="sxs-lookup"><span data-stu-id="a793d-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="a793d-188">แถวรายละเอียดของส่วนสรุปจะถูกลบออกจากเอกสารที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="a793d-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="a793d-189">ในขณะที่ออกแบบ คุณอาจกำหนดค่าคอนฟิกสูตร **ลบ** ให้กับองค์ประกอบรูปแบบ ถึงแม้ว่าจะไม่มีการควบคุมเนื้อหาในเท็มเพลต Word ที่คุณใช้อยู่จะมีแท็กที่ตรงกับชื่อขององค์ประกอบรูปแบบที่มีการกำหนดค่าคอนฟิกคุณสมบัติเป็น **ลบ** ไว้</span><span class="sxs-lookup"><span data-stu-id="a793d-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="a793d-190">เมื่อคุณตรวจสอบความถูกต้องของรูปแบบ ณ เวลาการออกแบบ คุณจะได้รับ [คำเตือน](er-components-inspections.md#i14) เกี่ยวกับความไม่สอดคล้องกันนี้</span><span class="sxs-lookup"><span data-stu-id="a793d-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="a793d-191">ขณะรันไทม์ จะมีข้อยกเว้นเกิดขึ้น ถ้าไม่มีการควบคุมเนื้อหาในเท็มเพลต Word ที่คุณใช้อยู่มีแท็กที่ตรงกับชื่อขององค์ประกอบรูปแบบที่มีการตั้งค่าคอนฟิกคุณสมบัติเป็น **ลบ** ไว้</span><span class="sxs-lookup"><span data-stu-id="a793d-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="a793d-192">บนแท็บ **การแม็ป** ในส่วน **ลบ** ให้ตั้งค่าตัวเลือก **กับข้อมูลหลัก** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a793d-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a793d-193">คุณต้องตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อลบตาราง Word ทั้งหมดเป็นออบเจ็กต์หลักของแถวที่มีรายละเอียดส่วนสรุป</span><span class="sxs-lookup"><span data-stu-id="a793d-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="a793d-194">ถ้าคุณตั้งค่าตัวเลือกนี้เป็น **ไม่** แถวส่วนหัวจะยังคงอยู่ในเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a793d-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="a793d-195">เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณไปรูปแบบที่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="a793d-195">Select **Save** to save your changes to the editable format.</span></span>

    ![ผลลัพธ์ที่สร้างขึ้นในรูปแบบ Word](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="a793d-197">ดำเนินการรูปแบบที่แก้ไขแล้วเพื่อสร้างชิ้นงานของ Word</span><span class="sxs-lookup"><span data-stu-id="a793d-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="a793d-198">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="a793d-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="a793d-199">เลือกสมุดรายวันการชำระเงินที่คุณสร้างขึ้น แล้วเลือก **Lines**</span><span class="sxs-lookup"><span data-stu-id="a793d-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="a793d-200">บนหน้า **การชำระเงินของผู้จัดจำหน่าย** ให้เลือกแถวทั้งหมด แล้วเลือก **สถานะการชำระเงิน** \> **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="a793d-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="a793d-201">เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="a793d-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="a793d-202">เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a793d-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="a793d-203">ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="a793d-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="a793d-204">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a793d-204">Select **OK**.</span></span>
8. <span data-ttu-id="a793d-205">ในกล่องโต้ตอบ **พารามิเตอร์รายงานอิเล็กทรอนิกส์** ในเขตข้อมูล **ระงับส่วนสรุป** ให้เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a793d-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="a793d-206">เลือก **ตกลง** และวิเคราะห์ผลลัพธ์ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="a793d-206">Select **OK**, and analyze the generated output.</span></span>

    ![ผลลัพธ์ที่สร้างขึ้นในรูปแบบ Word](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="a793d-208">โปรดสังเกตว่าผลลัพธ์จะไม่มีส่วนสรุป เนื่องจากถูกระงับไว้</span><span class="sxs-lookup"><span data-stu-id="a793d-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a793d-209">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a793d-209">Additional resources</span></span>

- [<span data-ttu-id="a793d-210">ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML</span><span class="sxs-lookup"><span data-stu-id="a793d-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="a793d-211">ออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์เพื่อสร้างรายงานในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="a793d-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="a793d-212">นำการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ที่มีเท็มเพลต Excel มาใช้ใหม่เพื่อสร้างรายงานในรูปแบบ Word</span><span class="sxs-lookup"><span data-stu-id="a793d-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="a793d-213">ตรวจสอบส่วนประกอบ ER ที่ตั้งค่าคอนฟิกเพื่อป้องกันปัญหารันไทม์</span><span class="sxs-lookup"><span data-stu-id="a793d-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]