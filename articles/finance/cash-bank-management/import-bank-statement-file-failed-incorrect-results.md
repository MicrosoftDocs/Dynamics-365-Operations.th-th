---
title: การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร
description: ถือเป็นสิ่งสำคัญที่ไฟล์ใบแจ้งยอดจากธนาคารต้อบตรงกับเค้าโครงที่ Microsoft Dynamics 365 Finance รองรับ เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09b24b88ee5f8104aabd11397d5bd2745e846cb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448291"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="908ea-107">การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="908ea-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="908ea-108">ถือเป็นสิ่งสำคัญที่ไฟล์ใบแจ้งยอดจากธนาคารต้อบตรงกับเค้าโครงที่ Microsoft Dynamics 365 Finance รองรับ</span><span class="sxs-lookup"><span data-stu-id="908ea-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="908ea-109">เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="908ea-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="908ea-110">อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="908ea-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="908ea-111">โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="908ea-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="908ea-112">บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="908ea-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="908ea-113">อะไรคือข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="908ea-113">What is the error?</span></span>
------------------

<span data-ttu-id="908ea-114">หลังจากที่คุณพยายามจะนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร ไปที่ประวัติงานการจัดการข้อมูลและรายละเอียดการดำเนินการเพื่อค้นหาข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="908ea-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="908ea-115">ข้อผิดพลาดสามารถช่วยได้โดยชี้ไปที่ใบแจ้งยอด ยอดดุล หรือรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="908ea-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="908ea-116">อย่างไรก็ตาม การให้ข้อมูลที่เพียงพอเพื่อช่วยให้คุณระบุฟิลด์หรือองค์ประกอบที่ทำให้เกิดปัญหาเป็นได้น้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="908ea-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="908ea-117">อะไรคือความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="908ea-117">What are the differences?</span></span>
<span data-ttu-id="908ea-118">เปรียบเทียบคำนิยามโครงร่างไฟล์ธนาคารกับคำนิยามการนำเข้าทางการเงิน และสังเกตความแตกต่างในฟิลด์และองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="908ea-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="908ea-119">เปรียบเทียบไฟล์ใบแจ้งยอดกับไฟล์ตัวอย่างทางการเงินที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="908ea-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="908ea-120">ในไฟล์ ISO20022 ควรเห็นความแตกต่างได้อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="908ea-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="908ea-121">ความแตกต่างของโซนเวลาในใบแจ้งยอดจากธนาคารที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="908ea-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="908ea-122">ค่าวันที่-เวลาในไฟล์นำเข้าอาจแตกต่างจากค่าวันที่-เวลาที่แสดงใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="908ea-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="908ea-123">เพื่อป้องกันไม่ให้เกิดความขัดแย้ง ให้ **ป้อนการตั้ง** ค่าโซนเวลาบนหน้าตั้งค่าคอนฟิกแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="908ea-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="908ea-124">ดู [การตั้งค่ากระบวนการนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูง](set-up-advanced-bank-reconciliation-import-process.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใส่ข้อมูลการกำหนดลักษณะโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="908ea-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="908ea-125">การแปลง</span><span class="sxs-lookup"><span data-stu-id="908ea-125">Transformations</span></span>
<span data-ttu-id="908ea-126">โดยทั่วไป ต้องทำการเปลี่ยนแปลงอย่างใดอย่างหนึ่งจากการแปลงข้อมูลสามอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="908ea-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="908ea-127">การแปลงข้อมูลแต่ละรายการจะถูกเขียนสำหรับมาตรฐานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="908ea-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="908ea-128">ชื่อทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="908ea-128">Resource name</span></span>                                         | <span data-ttu-id="908ea-129">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="908ea-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="908ea-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="908ea-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="908ea-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="908ea-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="908ea-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="908ea-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="908ea-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="908ea-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="908ea-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="908ea-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="908ea-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="908ea-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="908ea-136">การดีบักการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="908ea-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="908ea-137">ปรับปรุงไฟล์ BAI2 และ MT940</span><span class="sxs-lookup"><span data-stu-id="908ea-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="908ea-138">ไฟล์ BAI2 และ MT940 คือไฟล์ข้อความและจำเป็นต้องมีการปรับปรุงเพื่อเปิดใช้งานการดีบัก Extensible Stylesheet Language Transformations (XSLT)</span><span class="sxs-lookup"><span data-stu-id="908ea-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="908ea-139">โปรแกรมจะทำการปรับปรุงนี้เมื่อมีการนำเข้าไฟล์</span><span class="sxs-lookup"><span data-stu-id="908ea-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="908ea-140">สร้างไฟล์ XML และคัดลอกข้อความต่อไปนี้ลงในไฟล์นั้น</span><span class="sxs-lookup"><span data-stu-id="908ea-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="908ea-141">คัดลอกเนื้อหาของไฟล์ใบแจ้งยอดจากธนาคาร และวางลงในไฟล์ XML เพื่อแทนที่ **PASTESTATEMENTFILEHERE**</span><span class="sxs-lookup"><span data-stu-id="908ea-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="908ea-142">ดีบัก XSLT</span><span class="sxs-lookup"><span data-stu-id="908ea-142">Debug the XSLT</span></span>

<span data-ttu-id="908ea-143">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ <https://msdn.microsoft.com/library/ms255605.aspx></span><span class="sxs-lookup"><span data-stu-id="908ea-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="908ea-144">เริ่มต้น Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="908ea-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="908ea-145">สร้างแอพลิเคชันคอนโซล</span><span class="sxs-lookup"><span data-stu-id="908ea-145">Create a console application.</span></span>
3.  <span data-ttu-id="908ea-146">เปิด XSLT ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="908ea-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="908ea-147">คลิก XLST และหน้าคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="908ea-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="908ea-148">ตั้งค่าข้อมูลป้อนเข้าไปยังที่ตั้งของไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="908ea-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="908ea-149">กำหนดที่ตั้งและชื่อไฟล์สำหรับเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="908ea-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="908ea-150">ตั้งค่าจุดหยุดพักที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="908ea-150">Set the required break points.</span></span>
8.  <span data-ttu-id="908ea-151">บนเมนู คลิก **XML** &gt; **เริ่มต้นการดีบัก XSLT**</span><span class="sxs-lookup"><span data-stu-id="908ea-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="908ea-152">จัดรูปแบบเอาท์พุท XSLT</span><span class="sxs-lookup"><span data-stu-id="908ea-152">Format the XSLT output</span></span>

<span data-ttu-id="908ea-153">เมื่อการแปลงรัน จะสร้างไฟล์เอาต์พุตที่คุณสามารถดูได้ใน Visual Studio</span><span class="sxs-lookup"><span data-stu-id="908ea-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="908ea-154">ใช้ Ctrl+A, Ctrl+K และ Ctrl+D ในการจัดรูปแบบไฟล์เอาท์พุทอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="908ea-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="908ea-155">ปรับปรุงการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="908ea-155">Adjust the transformation</span></span>

<span data-ttu-id="908ea-156">ปรับปรุงการแปรงข้อมูลเพื่อรับฟิลด์หรือองค์ประกอบที่เหมาะสมในไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="908ea-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="908ea-157">จากนั้น แม็ปฟิลด์หรือองค์ประกอบนั้นไปยังองค์ประกอบทางการเงินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="908ea-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="908ea-158">ตัวบ่งชี้เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="908ea-158">Debit/credit indicator</span></span>

<span data-ttu-id="908ea-159">บางครั้ง เดบิตอาจถูกนำเข้าเป็นเครดิต และเครดิตอาจถูกนำเข้าเป็นเดบิต</span><span class="sxs-lookup"><span data-stu-id="908ea-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="908ea-160">เพื่อแก้ไขปัญหานี้ คุณต้องเปลี่ยน XSLT ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="908ea-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="908ea-161">ถ้าใบแจ้งยอดจากธนาคารมาจากหลายธนาคาร ตรวจสอบให้แน่ใจว่าใบแจ้งยอดทั้งหมดใช้วิธีการเดบิต/เครดิตเดียวกัน หรือสร้างการแปลงข้อมูลแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="908ea-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="908ea-162">เท็มเพลต BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="908ea-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="908ea-163">เท็มเพลต ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="908ea-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="908ea-164">เท็มเพลต MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="908ea-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="908ea-165">ตัวอย่างรูปแบบและโครงร่างทางเทคนิคของใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="908ea-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="908ea-166">ตารางต่อไปนี้เป็นตัวอย่างคำนิยามโครงร่างทางเทคนิคของไฟล์การนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูงและไฟล์ตัวอย่างสามรายการของใบแจ้งยอดจากธนาคารที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="908ea-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="908ea-167">คุณสามารถดาวน์โหลดไฟล์ตัวอย่างและโครงร่างทางเทคนิคได้ที่นี่: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="908ea-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="908ea-168">คำนิยามโครงร่างทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="908ea-168">Technical layout definition</span></span>                             | <span data-ttu-id="908ea-169">ไฟล์ตัวอย่างใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="908ea-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="908ea-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="908ea-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="908ea-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="908ea-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="908ea-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="908ea-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="908ea-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="908ea-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="908ea-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="908ea-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="908ea-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="908ea-175">BAI2StatementExample</span></span>                 |





