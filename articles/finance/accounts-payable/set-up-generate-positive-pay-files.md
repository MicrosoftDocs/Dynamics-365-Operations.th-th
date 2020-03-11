---
title: ตั้งค่าและสร้างไฟล์ Positve Pay
description: หัวข้อนี้อธิบายวิธีการตั้งค่า positive pay และสร้างไฟล์ positive pay
author: abruer
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0c44d172e8ed9cdb9c26501b3f4eb9fef4f8cf0b
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059412"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="f33e3-103">ตั้งค่าและสร้างไฟล์ Positve Pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f33e3-104">หัวข้อนี้อธิบายวิธีการตั้งค่า positive pay และสร้างไฟล์ positive pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="f33e3-105">ตั้งค่า Positive Pay เพื่อสร้างรายการอิเล็กทรอนิกส์ของเช็คที่ได้รับไปยังธนาคาร </span><span class="sxs-lookup"><span data-stu-id="f33e3-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="f33e3-106">จากนั้น เมื่อเช็คถูกนำเสนอให้แก่ธนาคารแล้ว ธนาคารจะเปรียบเทียบเช็คกับรายการของเช็ค </span><span class="sxs-lookup"><span data-stu-id="f33e3-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="f33e3-107">ถ้าเช็คตรงกับเช็คในรายการ ธนาคารจะเคลียร์เช็ค </span><span class="sxs-lookup"><span data-stu-id="f33e3-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="f33e3-108">ถ้าเช็คไม่ตรงกัน ธนาคารจะระงับเช็คไว้เพื่อตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="f33e3-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="f33e3-109">ความปลอดภัยสำหรับไฟล์ positive pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-109">Security for positive pay files</span></span>
<span data-ttu-id="f33e3-110">ไฟล์ positive pay สามารถประกอบด้วยข้อมูลที่สำคัญเกี่ยวกับผู้จ่าย และยอดเงินเช็ค </span><span class="sxs-lookup"><span data-stu-id="f33e3-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="f33e3-111">ดังนั้นตรวจสอบให้แน่ใจว่า คุณใช้มาตรการด้านความปลอดภัยที่เหมาะสมจากเวลาที่มีการสร้างไฟล์ จนกระทั่งได้รับโดยธนาคาร </span><span class="sxs-lookup"><span data-stu-id="f33e3-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="f33e3-112">ไฟล์ positive pay ถูกดาวน์โหลดไปยังตำแหน่งที่ระบุโดยเว็บเบราเซอร์ของคุณ </span><span class="sxs-lookup"><span data-stu-id="f33e3-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="f33e3-113">เนื่องจากไฟล์ค่าจ้างเชิงบวกสามารถประกอบด้วยข้อมูลสำคัญ เป็นสิ่งสำคัญที่เฉพาะผู้ใช้ที่ได้รับการรับรองจะมีการเข้าถึงเพื่อสร้างและดูข้อมูลนี้ใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f33e3-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="f33e3-114">ใช้ตารางต่อไปนี้เพื่อช่วยให้คุณกำหนดสิทธิ์ที่จำเป็นได้</span><span class="sxs-lookup"><span data-stu-id="f33e3-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f33e3-115">งาน</span><span class="sxs-lookup"><span data-stu-id="f33e3-115">Task</span></span></th>
<th><span data-ttu-id="f33e3-116">สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="f33e3-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f33e3-117">สร้างไฟล์ positive pay จากหน้ารายการ <strong>บัญชีธนาคาร</strong> หรือหน้า <strong>บัญชีธนาคาร</strong></span><span class="sxs-lookup"><span data-stu-id="f33e3-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="f33e3-118"><strong>รักษาข้อมูล positive pay ของธนาคาร</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="f33e3-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="f33e3-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="f33e3-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33e3-120">สร้างไฟล์ Positive Pay สำหรับนิติบุคคลหลายรายและบัญชีธนาคารจากหน้า <strong>สร้างไฟล์ positive pay</strong></span><span class="sxs-lookup"><span data-stu-id="f33e3-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="f33e3-121"><strong>รักษาข้อมูล positive pay ของธนาคาร</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="f33e3-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="f33e3-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="f33e3-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f33e3-123">ดูไฟล์ positive pay ในหน้า <strong>สรุปไฟล์ positive pay</strong></span><span class="sxs-lookup"><span data-stu-id="f33e3-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="f33e3-124"><strong>ดูข้อมูล Positive Pay ของธนาคารสำหรับนิติบุคคลหลายราย</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="f33e3-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33e3-125">ยืนยันไฟล์ positive pay ของธนาคารในหน้า <strong>สรุปไฟล์ positive pay</strong></span><span class="sxs-lookup"><span data-stu-id="f33e3-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="f33e3-126"><strong>ยืนยันไฟล์ positive pay</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="f33e3-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f33e3-127">เรียกคืนไฟล์ positive pay ของธนาคารในหน้า <strong>สรุปไฟล์ positive pay</strong></span><span class="sxs-lookup"><span data-stu-id="f33e3-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="f33e3-128"><strong>เรียกคืนไฟล์ Positive Pay</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="f33e3-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="f33e3-129">ตั้งค่ารูปแบบของ Positive Pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-129">Set up a positive pay format</span></span>
<span data-ttu-id="f33e3-130">มีสร้างไฟล์ positive pay โดยการใช้เอนทิตีข้อมูล </span><span class="sxs-lookup"><span data-stu-id="f33e3-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="f33e3-131">ก่อนที่คุณสามารถสร้างไฟล์ positive pay คุณต้องตั้งค่ารูปแบบสำหรับการป้อนค่าการแปลง ที่จะใช้ในการแปลข้อมูลเช็คเป็นรูปแบบที่สามารถสื่อสารกับธนาคารได้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="f33e3-132">ในหน้า **รูปแบบ Positive pay** คุณสามารถสร้างตัวบ่งชี้รูปแบบไฟล์และคำอธิบายได้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="f33e3-133">รูปแบบการป้อนข้อมูลการแปลงต้องเป็นชนิด XML </span><span class="sxs-lookup"><span data-stu-id="f33e3-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="f33e3-134">รูปแบบเฉพาะขึ้นอยู่กับไฟล์การแปลงที่คุณกำลังใช้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="f33e3-135">ตัวอย่างเช่น ไฟล์ Extensible Stylesheet Language transformation (XSLT) ที่ได้รับ ใช้รูปแบบ **องค์ประกอบ XML**</span><span class="sxs-lookup"><span data-stu-id="f33e3-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="f33e3-136">ใช้การดำเนินการ **อัพโหลดไฟล์ที่ใช้สำหรับการแปลง** เพื่อระบุที่ตั้งของไฟล์การแปลง สำหรับรูปแบบที่ธนาคารของคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f33e3-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="f33e3-137">ตัวอย่าง: ไฟล์ XSLT สำหรับไฟล์ Positve Pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-137">Example: XSLT file for positive pay file</span></span>

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="f33e3-138">กำหนดรูปแบบ Positve Pay ให้กับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f33e3-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="f33e3-139">สำหรับแต่ละบัญชีธนาคารที่คุณต้องการสร้างข้อมูล positive pay ให้ คุณต้องกำหนดรูปแบบ positive pay ที่คุณระบุไว้ในส่วนก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="f33e3-140">ในหน้า **บัญชีธนาคาร** เลือกรูปแบบ positive pay ที่สอดคล้องกับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f33e3-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="f33e3-141">ในฟิลด์ **วันที่เริ่มต้น Positive pay** ป้อนวันที่แรกในการสร้างไฟล์ Positive pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="f33e3-142">เป็นสิ่งสำคัญที่คุณป้อนวันที่ในฟิลด์นี้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="f33e3-143">มิฉะนั้น ไฟล์ positive pay แรกที่คุณสร้างขึ้นจะรวมเช็คทั้งหมดที่เคยสร้างไว้สำหรับบัญชีธนาคารนี้</span><span class="sxs-lookup"><span data-stu-id="f33e3-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="f33e3-144">มอบหมายลำดับหมายเลขสำหรับไฟล์ Positve Pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="f33e3-145">แต่ละไฟล์ positive pay ต้องมีหมายเลขเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="f33e3-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="f33e3-146">ใช้แท็บ **ลำดับหมายเลข** บนหน้า  **พารามิเตอร์การจัดการเงินสดและธนาคาร** เพื่อสร้างลำดับหมายเลขสำหรับไฟล์ Positive pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="f33e3-147">สร้างไฟล์ positive pay สำหรับบัญชีธนาคารเดี่ยว</span><span class="sxs-lookup"><span data-stu-id="f33e3-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="f33e3-148">คุณสามารถสร้างไฟล์ positive pay สำหรับนิติบุคคลเดียวและบัญชีธนาคารหนึ่งๆ </span><span class="sxs-lookup"><span data-stu-id="f33e3-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="f33e3-149">สำหรับข้อมูลเกี่ยวกับวิธีการสร้างไฟล์ positive pay สำหรับนิติบุคคลและบัญชีธนาคารหลายรายการพร้อมกัน ให้ดูส่วนถัดไป </span><span class="sxs-lookup"><span data-stu-id="f33e3-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="f33e3-150">เพื่อสร้างไฟล์ Positive pay สำหรับนิติบุคคลเดียวและบัญชีธนาคารเดียว ให้เปิดกล่องโต้ตอบ **สร้างไฟล์ Positive pay** จากหน้า **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="f33e3-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="f33e3-151">ในฟิลด์ **วันที่ตัดยอด** ป้อนวันที่ของเช็คล่าสุดเพื่อรวมไว้ในไฟล์ Positive pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="f33e3-152">เช็คทั้งหมดที่ยังไม่ได้ถูกรวมอยู่ในไฟล์ positive pay ภายในวันที่สิ้นสุดของเช็คนี้จะถุกรวมอยู่ในไฟล์</span><span class="sxs-lookup"><span data-stu-id="f33e3-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="f33e3-153">สร้างไฟล์ positive pay สำหรับบัญชีธนาคารหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f33e3-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="f33e3-154">เพื่อสร้างไฟล์ Positive pay สำหรับบัญชีธนาคารหลายรายการ ใช้งานประจำงวด **สร้างไฟล์ Positive pay**</span><span class="sxs-lookup"><span data-stu-id="f33e3-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="f33e3-155">เลือกรูปแบบ positive pay สำหรับไฟล์ และระบุว่าจะสร้างไฟล์สำหรับนิติบุคคลทั้งหมด หรือสำหรับนิติบุคคลที่เลือก </span><span class="sxs-lookup"><span data-stu-id="f33e3-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="f33e3-156">คุณสามารถสร้างไฟล์ positive pay สำหรับบัญชีธนาคารทั้งหมดที่ใช้รูปแบบ positive pay หรือสำหรับบัญชีธนาคารที่เลือก </span><span class="sxs-lookup"><span data-stu-id="f33e3-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="f33e3-157">ในฟิลด์ **วันที่ตัดยอด** ป้อนวันที่ของเช็คล่าสุดเพื่อรวมไว้ในไฟล์ Positive pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="f33e3-158">เช็คทั้งหมดที่ยังไม่ได้ถูกรวมอยู่ในไฟล์ positive pay ภายในวันที่สิ้นสุดของเช็คนี้จะถุกรวมอยู่ในไฟล์</span><span class="sxs-lookup"><span data-stu-id="f33e3-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="f33e3-159">ดูผลลัพธ์ของการสร้างไฟล์ positive pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="f33e3-160">หลังจากที่มีสร้างไฟล์ Positive pay คุณสามารถดูผลลัพธ์ในหน้า  **สรุปไฟล์ Positive pay** ได้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="f33e3-161">เมื่อต้องการดูรายละเอียดของเช็คแต่ละรายการ ใช้หน้ารายละเอียด **ไฟล์ Positive pay**</span><span class="sxs-lookup"><span data-stu-id="f33e3-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="f33e3-162">ยืนยันไฟล์ Positive Pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-162">Confirm a positive pay file</span></span>
<span data-ttu-id="f33e3-163">หลังจากที่เช็คที่ถูกรายการในไฟล์ positive pay ได้ถูกชำระ คุณจะได้รับหมายเลขการยืนยันจากธนาคารของคุณ </span><span class="sxs-lookup"><span data-stu-id="f33e3-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="f33e3-164">จากนั้น คุณสามารถยืนยันไฟล์ positive pay ได้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="f33e3-165">บนหน้า **สรุปไฟล์ Positive pay** ให้เลือกไฟล์ Positive pay ที่มีสถานะเป็น **สร้างแล้ว** และจากนั้นเลือกการดำเนินการ **ป้อนการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="f33e3-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="f33e3-166">เมื่อคุณยืนยันไฟล์ positive pay จะมีการบันทึกหมายเลขใบยืนยันที่คุณได้รับจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f33e3-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="f33e3-167">เรียกคืนไฟล์ Positive Pay</span><span class="sxs-lookup"><span data-stu-id="f33e3-167">Recall a positive pay file</span></span>
<span data-ttu-id="f33e3-168">ถ้าคุณต้องเปลี่ยนไฟล์ positive pay คุณสามารถเรียกคืนได้ </span><span class="sxs-lookup"><span data-stu-id="f33e3-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="f33e3-169">ในหน้า **สรุปไฟล์ Positive pay** เลือกไฟล์ Positive pay ที่มีสถานะเป็น **สร้างแล้ว** และจากนั้นเลือกการดำเนินการ **เรียกคืน**</span><span class="sxs-lookup"><span data-stu-id="f33e3-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="f33e3-170">สำหรับเช็คแต่ละรายการในไฟล์ positive pay ฟิลด์จะบ่งชี้ว่า เช็คที่ได้ถูกรวมในไฟล์ positive pay จะถูกรีเซ็ตหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="f33e3-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="f33e3-171">จากนั้นคุณสามารถสร้างไฟล์ positive pay ใหม่ที่รวมเช็คที่ถูกเรียกคืน</span><span class="sxs-lookup"><span data-stu-id="f33e3-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



