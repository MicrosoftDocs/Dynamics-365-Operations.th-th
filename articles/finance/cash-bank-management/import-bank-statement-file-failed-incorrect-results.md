---
title: การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร
description: ถือเป็นสิ่งสำคัญที่ไฟล์ใบแจ้งยอดจากธนาคารต้องตรงกับเค้าโครงที่ Microsoft Dynamics 365 Finance รองรับ เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188571"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="9f3fe-107">การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f3fe-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f3fe-108">ถือเป็นสิ่งสำคัญที่ไฟล์ใบแจ้งยอดจากธนาคารต้องตรงกับเค้าโครงที่ Microsoft Dynamics 365 Finance รองรับ</span><span class="sxs-lookup"><span data-stu-id="9f3fe-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="9f3fe-109">เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9f3fe-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="9f3fe-110">อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9f3fe-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="9f3fe-111">โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f3fe-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="9f3fe-112">บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="9f3fe-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="9f3fe-113">อะไรคือข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9f3fe-113">What is the error?</span></span>

<span data-ttu-id="9f3fe-114">หลังจากที่คุณพยายามจะนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร ไปที่ประวัติงานการจัดการข้อมูลและรายละเอียดการดำเนินการเพื่อค้นหาข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9f3fe-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="9f3fe-115">ข้อผิดพลาดสามารถช่วยได้โดยชี้ไปที่ใบแจ้งยอด ยอดดุล หรือรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="9f3fe-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="9f3fe-116">อย่างไรก็ตาม การให้ข้อมูลที่เพียงพอเพื่อช่วยให้คุณระบุฟิลด์หรือองค์ประกอบที่ทำให้เกิดปัญหาเป็นได้น้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="9f3fe-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="9f3fe-117">ใบแจ้งยอดจากธนาคารที่นําเข้าสามารถทับซ้อนกับใบแจ้งยอดจากธนาคารเดียว ณ เวลาหนึ่งๆ เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9f3fe-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="9f3fe-118">ตัวอย่างเช่น ถ้ารายงานสิ้นสุดที่ 12:00 น. ในวันที่ 1 มกราคม 2021 วันที่เริ่มต้นของรายงานถัดไปจะเป็น 12:00 น. ในวันที่ 1 มกราคม 2021 12:00:00 น.</span><span class="sxs-lookup"><span data-stu-id="9f3fe-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="9f3fe-119">อะไรคือความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="9f3fe-119">What are the differences?</span></span>
<span data-ttu-id="9f3fe-120">เปรียบเทียบคำนิยามโครงร่างไฟล์ธนาคารกับคำนิยามการนำเข้าทางการเงิน และสังเกตความแตกต่างในฟิลด์และองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="9f3fe-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="9f3fe-121">เปรียบเทียบไฟล์ใบแจ้งยอดกับไฟล์ตัวอย่างทางการเงินที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="9f3fe-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="9f3fe-122">ในไฟล์ ISO20022 ควรเห็นความแตกต่างได้อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="9f3fe-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="9f3fe-123">ความแตกต่างของโซนเวลาในใบแจ้งยอดจากธนาคารที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="9f3fe-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="9f3fe-124">ค่าวันที่-เวลาในไฟล์นำเข้าอาจแตกต่างจากค่าวันที่-เวลาที่แสดงใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9f3fe-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="9f3fe-125">เพื่อป้องกันไม่ให้เกิดความขัดแย้ง ให้ **ป้อนการตั้ง** ค่าโซนเวลาบนหน้าตั้งค่าคอนฟิกแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9f3fe-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="9f3fe-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการป้อนข้อมูลการกำหนดลักษณะโซนเวลา ดู [ตั้งค่ากระบวนการนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูง](set-up-advanced-bank-reconciliation-import-process.md)</span><span class="sxs-lookup"><span data-stu-id="9f3fe-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="9f3fe-127">การแปลง</span><span class="sxs-lookup"><span data-stu-id="9f3fe-127">Transformations</span></span>
<span data-ttu-id="9f3fe-128">โดยทั่วไป ต้องทำการเปลี่ยนแปลงอย่างใดอย่างหนึ่งจากการแปลงข้อมูลสามอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="9f3fe-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="9f3fe-129">การแปลงข้อมูลแต่ละรายการจะถูกเขียนสำหรับมาตรฐานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="9f3fe-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="9f3fe-130">ชื่อทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="9f3fe-130">Resource name</span></span>                                         | <span data-ttu-id="9f3fe-131">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="9f3fe-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="9f3fe-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="9f3fe-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="9f3fe-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="9f3fe-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="9f3fe-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="9f3fe-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="9f3fe-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="9f3fe-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="9f3fe-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="9f3fe-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="9f3fe-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="9f3fe-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="9f3fe-138">การดีบักการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9f3fe-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="9f3fe-139">ปรับปรุงไฟล์ BAI2 และ MT940</span><span class="sxs-lookup"><span data-stu-id="9f3fe-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="9f3fe-140">ไฟล์ BAI2 และ MT940 คือไฟล์ข้อความและจำเป็นต้องมีการปรับปรุงเพื่อเปิดใช้งานการดีบัก Extensible Stylesheet Language Transformations (XSLT)</span><span class="sxs-lookup"><span data-stu-id="9f3fe-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="9f3fe-141">โปรแกรมจะทำการปรับปรุงนี้เมื่อมีการนำเข้าไฟล์</span><span class="sxs-lookup"><span data-stu-id="9f3fe-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="9f3fe-142">สร้างไฟล์ XML และคัดลอกข้อความต่อไปนี้ลงในไฟล์นั้น</span><span class="sxs-lookup"><span data-stu-id="9f3fe-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="9f3fe-143">คัดลอกเนื้อหาของไฟล์ใบแจ้งยอดจากธนาคาร และวางลงในไฟล์ XML เพื่อแทนที่ **PASTESTATEMENTFILEHERE**</span><span class="sxs-lookup"><span data-stu-id="9f3fe-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="9f3fe-144">ดีบัก XSLT</span><span class="sxs-lookup"><span data-stu-id="9f3fe-144">Debug the XSLT</span></span>

<span data-ttu-id="9f3fe-145">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ <https://msdn.microsoft.com/library/ms255605.aspx></span><span class="sxs-lookup"><span data-stu-id="9f3fe-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="9f3fe-146">เริ่มต้น Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9f3fe-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="9f3fe-147">สร้างแอพลิเคชันคอนโซล</span><span class="sxs-lookup"><span data-stu-id="9f3fe-147">Create a console application.</span></span>
3.  <span data-ttu-id="9f3fe-148">เปิด XSLT ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9f3fe-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="9f3fe-149">คลิก XLST และหน้าคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="9f3fe-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="9f3fe-150">ตั้งค่าข้อมูลป้อนเข้าไปยังที่ตั้งของไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f3fe-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="9f3fe-151">กำหนดที่ตั้งและชื่อไฟล์สำหรับเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="9f3fe-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="9f3fe-152">ตั้งค่าจุดหยุดพักที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="9f3fe-152">Set the required break points.</span></span>
8.  <span data-ttu-id="9f3fe-153">บนเมนู คลิก **XML** &gt; **เริ่มต้นการดีบัก XSLT**</span><span class="sxs-lookup"><span data-stu-id="9f3fe-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="9f3fe-154">จัดรูปแบบเอาท์พุท XSLT</span><span class="sxs-lookup"><span data-stu-id="9f3fe-154">Format the XSLT output</span></span>

<span data-ttu-id="9f3fe-155">เมื่อการแปลงรัน จะสร้างไฟล์เอาต์พุตที่คุณสามารถดูได้ใน Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9f3fe-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="9f3fe-156">ใช้ Ctrl+A, Ctrl+K และ Ctrl+D ในการจัดรูปแบบไฟล์เอาท์พุทอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="9f3fe-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="9f3fe-157">ปรับปรุงการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9f3fe-157">Adjust the transformation</span></span>

<span data-ttu-id="9f3fe-158">ปรับปรุงการแปรงข้อมูลเพื่อรับฟิลด์หรือองค์ประกอบที่เหมาะสมในไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f3fe-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="9f3fe-159">จากนั้น แม็ปฟิลด์หรือองค์ประกอบนั้นไปยังองค์ประกอบทางการเงินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9f3fe-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="9f3fe-160">ตัวบ่งชี้เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="9f3fe-160">Debit/credit indicator</span></span>

<span data-ttu-id="9f3fe-161">บางครั้ง เดบิตอาจถูกนำเข้าเป็นเครดิต และเครดิตอาจถูกนำเข้าเป็นเดบิต</span><span class="sxs-lookup"><span data-stu-id="9f3fe-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="9f3fe-162">เพื่อแก้ไขปัญหานี้ คุณต้องเปลี่ยน XSLT ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9f3fe-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="9f3fe-163">ถ้าใบแจ้งยอดจากธนาคารมาจากหลายธนาคาร ตรวจสอบให้แน่ใจว่าใบแจ้งยอดทั้งหมดใช้วิธีการเดบิต/เครดิตเดียวกัน หรือสร้างการแปลงข้อมูลแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="9f3fe-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="9f3fe-164">เท็มเพลต BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="9f3fe-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="9f3fe-165">เท็มเพลต ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="9f3fe-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="9f3fe-166">เท็มเพลต MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="9f3fe-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="9f3fe-167">ตัวอย่างรูปแบบและโครงร่างทางเทคนิคของใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f3fe-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="9f3fe-168">ตารางต่อไปนี้เป็นตัวอย่างคำนิยามโครงร่างทางเทคนิคของไฟล์การนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูงและไฟล์ตัวอย่างสามรายการของใบแจ้งยอดจากธนาคารที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="9f3fe-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="9f3fe-169">คุณสามารถดาวน์โหลดไฟล์ตัวอย่างและโครงร่างทางเทคนิคได้ที่นี่: [นำเข้าไฟล์ตัวอย่าง](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="9f3fe-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="9f3fe-170">คำนิยามโครงร่างทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="9f3fe-170">Technical layout definition</span></span>                             | <span data-ttu-id="9f3fe-171">ไฟล์ตัวอย่างใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f3fe-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="9f3fe-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="9f3fe-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="9f3fe-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="9f3fe-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="9f3fe-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="9f3fe-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="9f3fe-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="9f3fe-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="9f3fe-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="9f3fe-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="9f3fe-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="9f3fe-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
