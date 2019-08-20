---
title: การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร
description: เป็นสิ่งสำคัญที่ไฟล์ใบแจ้งยอดของธนาคารจากธนาคารตรงกับเค้าโครงที่ Microsoft Dynamics 365 for Finance and Operations สนับสนุน เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา
author: ShylaThompson
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
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4275a4d77b03c55decbf161df8f2115183cac3d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842412"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="3d5a1-107">การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d5a1-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d5a1-108">เป็นสิ่งสำคัญที่ไฟล์ใบแจ้งยอดของธนาคารจากธนาคารตรงกับเค้าโครงที่ Microsoft Dynamics 365 for Finance and Operations สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="3d5a1-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="3d5a1-109">เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3d5a1-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="3d5a1-110">อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3d5a1-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="3d5a1-111">โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d5a1-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="3d5a1-112">บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="3d5a1-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="3d5a1-113">อะไรคือข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="3d5a1-113">What is the error?</span></span>
------------------

<span data-ttu-id="3d5a1-114">หลังจากที่คุณพยายามจะนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร ไปที่ประวัติงานการจัดการข้อมูลและรายละเอียดการดำเนินการเพื่อค้นหาข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="3d5a1-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="3d5a1-115">ข้อผิดพลาดสามารถช่วยได้โดยชี้ไปที่ใบแจ้งยอด ยอดดุล หรือรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="3d5a1-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="3d5a1-116">อย่างไรก็ตาม การให้ข้อมูลที่เพียงพอเพื่อช่วยให้คุณระบุฟิลด์หรือองค์ประกอบที่ทำให้เกิดปัญหาเป็นได้น้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="3d5a1-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="3d5a1-117">อะไรคือความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="3d5a1-117">What are the differences?</span></span>
<span data-ttu-id="3d5a1-118">เปรียบเทียบคำนิยามโครงร่างไฟล์ธนาคารกับคำนิยามการนำเข้า Finance and Operations และสังเกตความแตกต่างในฟิลด์และองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="3d5a1-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="3d5a1-119">เปรียบเทียบไฟล์ใบแจ้งยอดจากธนาคารกับไฟล์ตัวอย่าง Finance and Operations ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3d5a1-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="3d5a1-120">ในไฟล์ ISO20022 ควรเห็นความแตกต่างได้อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="3d5a1-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="3d5a1-121">การแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3d5a1-121">Transformations</span></span>
<span data-ttu-id="3d5a1-122">โดยทั่วไป ต้องทำการเปลี่ยนแปลงอย่างใดอย่างหนึ่งจากการแปลงข้อมูลสามอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="3d5a1-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="3d5a1-123">การแปลงข้อมูลแต่ละรายการจะถูกเขียนสำหรับมาตรฐานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3d5a1-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="3d5a1-124">ชื่อทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="3d5a1-124">Resource name</span></span>                                         | <span data-ttu-id="3d5a1-125">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="3d5a1-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="3d5a1-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="3d5a1-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="3d5a1-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="3d5a1-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="3d5a1-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="3d5a1-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="3d5a1-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="3d5a1-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="3d5a1-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="3d5a1-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="3d5a1-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="3d5a1-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="3d5a1-132">การดีบักการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3d5a1-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="3d5a1-133">ปรับปรุงไฟล์ BAI2 และ MT940</span><span class="sxs-lookup"><span data-stu-id="3d5a1-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="3d5a1-134">ไฟล์ BAI2 และ MT940 คือไฟล์ข้อความและจำเป็นต้องมีการปรับปรุงเพื่อเปิดใช้งานการดีบัก Extensible Stylesheet Language Transformations (XSLT)</span><span class="sxs-lookup"><span data-stu-id="3d5a1-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="3d5a1-135">โปรแกรมจะทำการปรับปรุงนี้เมื่อมีการนำเข้าไฟล์</span><span class="sxs-lookup"><span data-stu-id="3d5a1-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="3d5a1-136">สร้างไฟล์ XML และคัดลอกข้อความต่อไปนี้ลงในไฟล์นั้น</span><span class="sxs-lookup"><span data-stu-id="3d5a1-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="3d5a1-137">คัดลอกเนื้อหาของไฟล์ใบแจ้งยอดจากธนาคาร และวางลงในไฟล์ XML เพื่อแทนที่ **PASTESTATEMENTFILEHERE**</span><span class="sxs-lookup"><span data-stu-id="3d5a1-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="3d5a1-138">ดีบัก XSLT</span><span class="sxs-lookup"><span data-stu-id="3d5a1-138">Debug the XSLT</span></span>

<span data-ttu-id="3d5a1-139">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ <https://msdn.microsoft.com/library/ms255605.aspx></span><span class="sxs-lookup"><span data-stu-id="3d5a1-139">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="3d5a1-140">เริ่มต้น Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d5a1-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="3d5a1-141">สร้างแอพลิเคชันคอนโซล</span><span class="sxs-lookup"><span data-stu-id="3d5a1-141">Create a console application.</span></span>
3.  <span data-ttu-id="3d5a1-142">เปิด XSLT ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3d5a1-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="3d5a1-143">คลิก XLST และหน้าคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3d5a1-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="3d5a1-144">ตั้งค่าข้อมูลป้อนเข้าไปยังที่ตั้งของไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d5a1-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="3d5a1-145">กำหนดที่ตั้งและชื่อไฟล์สำหรับเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="3d5a1-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="3d5a1-146">ตั้งค่าจุดหยุดพักที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="3d5a1-146">Set the required break points.</span></span>
8.  <span data-ttu-id="3d5a1-147">บนเมนู คลิก **XML** &gt; **เริ่มต้นการดีบัก XSLT**</span><span class="sxs-lookup"><span data-stu-id="3d5a1-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="3d5a1-148">จัดรูปแบบเอาท์พุท XSLT</span><span class="sxs-lookup"><span data-stu-id="3d5a1-148">Format the XSLT output</span></span>

<span data-ttu-id="3d5a1-149">เมื่อการแปลงรัน จะสร้างไฟล์เอาต์พุตที่คุณสามารถดูได้ใน Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d5a1-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="3d5a1-150">ใช้ Ctrl+A, Ctrl+K และ Ctrl+D ในการจัดรูปแบบไฟล์เอาท์พุทอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="3d5a1-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="3d5a1-151">ปรับปรุงการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3d5a1-151">Adjust the transformation</span></span>

<span data-ttu-id="3d5a1-152">ปรับปรุงการแปรงข้อมูลเพื่อรับฟิลด์หรือองค์ประกอบที่เหมาะสมในไฟล์ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d5a1-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="3d5a1-153">จากนั้น แม็ปฟิลด์หรือองค์ประกอบนั้นไปยังองค์ประกอบ Finance and Operations ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3d5a1-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="3d5a1-154">ตัวบ่งชี้เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="3d5a1-154">Debit/credit indicator</span></span>

<span data-ttu-id="3d5a1-155">บางครั้ง เดบิตอาจถูกนำเข้าเป็นเครดิต และเครดิตอาจถูกนำเข้าเป็นเดบิต</span><span class="sxs-lookup"><span data-stu-id="3d5a1-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="3d5a1-156">เพื่อแก้ไขปัญหานี้ คุณต้องเปลี่ยน XSLT ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3d5a1-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="3d5a1-157">ถ้าใบแจ้งยอดจากธนาคารมาจากหลายธนาคาร ตรวจสอบให้แน่ใจว่าใบแจ้งยอดทั้งหมดใช้วิธีการเดบิต/เครดิตเดียวกัน หรือสร้างการแปลงข้อมูลแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="3d5a1-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="3d5a1-158">เท็มเพลต BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="3d5a1-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="3d5a1-159">เท็มเพลต ISO20022XML-to-Reconcilation.xslt GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="3d5a1-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="3d5a1-160">เท็มเพลต MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="3d5a1-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="3d5a1-161">ตัวอย่างรูปแบบและโครงร่างทางเทคนิคของใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d5a1-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="3d5a1-162">ตารางต่อไปนี้เป็นตัวอย่างคำนิยามโครงร่างทางเทคนิคของไฟล์การนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูงและไฟล์ตัวอย่างสามรายการของใบแจ้งยอดจากธนาคารที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="3d5a1-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="3d5a1-163">คุณสามารถดาวน์โหลดไฟล์ตัวอย่างและโครงร่างทางเทคนิคได้ที่นี่: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="3d5a1-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="3d5a1-164">คำนิยามโครงร่างทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="3d5a1-164">Technical layout definition</span></span>                             | <span data-ttu-id="3d5a1-165">ไฟล์ตัวอย่างใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d5a1-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="3d5a1-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="3d5a1-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="3d5a1-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="3d5a1-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="3d5a1-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="3d5a1-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="3d5a1-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="3d5a1-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="3d5a1-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="3d5a1-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="3d5a1-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="3d5a1-171">BAI2StatementExample</span></span>                 |





