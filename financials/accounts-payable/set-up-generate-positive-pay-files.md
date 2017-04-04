---
title: "ตั้งค่าและสร้างไฟล์ Positve Pay"
description: "บทความนี้อธิบายวิธีการตั้งค่า positive pay และสร้างไฟล์ positive pay"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e23a341565d7c97484646e32161815253ae69ceb
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-generate-positive-pay-files"></a>ตั้งค่าและสร้างไฟล์ Positve Pay

บทความนี้อธิบายวิธีการตั้งค่า positive pay และสร้างไฟล์ positive pay 

ตั้งค่า Positive Pay เพื่อสร้างรายการอิเล็กทรอนิกส์ของเช็คที่ได้รับไปยังธนาคาร  จากนั้น เมื่อเช็คถูกนำเสนอให้แก่ธนาคารแล้ว ธนาคารจะเปรียบเทียบเช็คกับรายการของเช็ค  ถ้าเช็คตรงกับเช็คในรายการ ธนาคารจะเคลียร์เช็ค  ถ้าเช็คไม่ตรงกัน ธนาคารจะระงับเช็คไว้เพื่อตรวจสอบ

## <a name="security-for-positive-pay-files"></a>ความปลอดภัยสำหรับไฟล์ positive pay
ไฟล์ positive pay สามารถประกอบด้วยข้อมูลที่สำคัญเกี่ยวกับผู้จ่าย และยอดเงินเช็ค  ดังนั้นตรวจสอบให้แน่ใจว่า คุณใช้มาตรการด้านความปลอดภัยที่เหมาะสมจากเวลาที่มีการสร้างไฟล์ จนกระทั่งได้รับโดยธนาคาร  ไฟล์ positive pay ถูกดาวน์โหลดไปยังตำแหน่งที่ระบุโดยเว็บเบราเซอร์ของคุณ  เนื่องจากแฟ้มบวกค่าจ้างสามารถประกอบด้วยข้อมูลที่สำคัญ สิ่งสำคัญคือว่า เฉพาะผู้ใช้ที่ได้รับอนุญาตสามารถเข้าถึงสร้าง และดูข้อมูลนี้ใน 365 Dynamics Microsoft สำหรับการดำเนินงาน ใช้ตารางต่อไปนี้เพื่อช่วยให้คุณกำหนดสิทธิ์ที่จำเป็นได้

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>งาน</th>
<th>สิทธิ์</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>สร้างไฟล์ positive pay จากหน้ารายการ <strong>บัญชีธนาคาร</strong> หรือหน้า <strong>บัญชีธนาคาร</strong></td>
<td><ul>
<li><strong>รักษาข้อมูล positive pay ของธนาคาร</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>สร้างไฟล์ Positive Pay สำหรับนิติบุคคลหลายรายและบัญชีธนาคารจากหน้า <strong>สร้างไฟล์ positive pay</strong></td>
<td><ul>
<li><strong>รักษาข้อมูล positive pay ของธนาคาร</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>ดูไฟล์ positive pay ในหน้า <strong>สรุปไฟล์ positive pay</strong></td>
<td><strong>ดูข้อมูล Positive Pay ของธนาคารสำหรับนิติบุคคลหลายราย</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>ยืนยันไฟล์ positive pay ของธนาคารในหน้า <strong>สรุปไฟล์ positive pay</strong></td>
<td><strong>ยืนยันไฟล์ positive pay</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>เรียกคืนไฟล์ positive pay ของธนาคารในหน้า <strong>สรุปไฟล์ positive pay</strong></td>
<td><strong>เรียกคืนไฟล์ Positive Pay</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>ตั้งค่ารูปแบบของ Positive Pay
มีสร้างไฟล์ positive pay โดยการใช้เอนทิตีข้อมูล  ก่อนที่คุณสามารถสร้างไฟล์ positive pay คุณต้องตั้งค่ารูปแบบสำหรับการป้อนค่าการแปลง ที่จะใช้ในการแปลข้อมูลเช็คเป็นรูปแบบที่สามารถสื่อสารกับธนาคารได้  On the **Positive pay format** page, you can create a file format identifier and a description. รูปแบบการป้อนข้อมูลการแปลงต้องเป็นชนิด XML  รูปแบบเฉพาะขึ้นอยู่กับไฟล์การแปลงที่คุณกำลังใช้  แฟ้ม Extensible สไตล์ชีภาษาแปลง (XSLT) ตัวอย่างที่มีให้ใช้งานตัวอย่างเช่น การ**องค์ประกอบ XML**รูปแบบ Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.

## <a name="example-xslt-file-for-positive-pay-file"></a>ตัวอย่าง: ไฟล์ XSLT สำหรับไฟล์ Positve Pay
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
          <xsl:for-each select="Document/BankPositivePayExportEntity">
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>กำหนดรูปแบบ Positve Pay ให้กับบัญชีธนาคาร
สำหรับแต่ละบัญชีธนาคารที่คุณต้องการสร้างข้อมูล positive pay ให้ คุณต้องกำหนดรูปแบบ positive pay ที่คุณระบุไว้ในส่วนก่อนหน้านี้  On the **Bank accounts** page, select the positive pay format that corresponds to the bank account. In the **Positive pay start date** field, enter the first date to generate positive pay files. เป็นสิ่งสำคัญที่คุณป้อนวันที่ในฟิลด์นี้  มิฉะนั้น ไฟล์ positive pay แรกที่คุณสร้างขึ้นจะรวมเช็คทั้งหมดที่เคยสร้างไว้สำหรับบัญชีธนาคารนี้

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>มอบหมายลำดับหมายเลขสำหรับไฟล์ Positve Pay
แต่ละไฟล์ positive pay ต้องมีหมายเลขเฉพาะ  Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>สร้างไฟล์ positive pay สำหรับบัญชีธนาคารเดี่ยว
คุณสามารถสร้างไฟล์ positive pay สำหรับนิติบุคคลเดียวและบัญชีธนาคารหนึ่งๆ  สำหรับข้อมูลเกี่ยวกับวิธีการสร้างไฟล์ positive pay สำหรับนิติบุคคลและบัญชีธนาคารหลายรายการพร้อมกัน ให้ดูส่วนถัดไป  To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page. In the **Cut-off date** field, enter the last check date to include in the positive pay file. เช็คทั้งหมดที่ยังไม่ได้ถูกรวมอยู่ในไฟล์ positive pay ภายในวันที่สิ้นสุดของเช็คนี้จะถุกรวมอยู่ในไฟล์

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>สร้างไฟล์ positive pay สำหรับบัญชีธนาคารหลายรายการ
To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task. เลือกรูปแบบ positive pay สำหรับไฟล์ และระบุว่าจะสร้างไฟล์สำหรับนิติบุคคลทั้งหมด หรือสำหรับนิติบุคคลที่เลือก  คุณสามารถสร้างไฟล์ positive pay สำหรับบัญชีธนาคารทั้งหมดที่ใช้รูปแบบ positive pay หรือสำหรับบัญชีธนาคารที่เลือก  In the **Cut-off date** field, enter the last check date to include in the positive pay file. เช็คทั้งหมดที่ยังไม่ได้ถูกรวมอยู่ในไฟล์ positive pay ภายในวันที่สิ้นสุดของเช็คนี้จะถุกรวมอยู่ในไฟล์

## <a name="view-the-results-of-positive-pay-file-generation"></a>ดูผลลัพธ์ของการสร้างไฟล์ positive pay
After the positive pay file is generated, you can view the results on the **Positive pay file summary** page. To view the details of the individual checks, use the **Positive pay file** details page.

## <a name="confirm-a-positive-pay-file"></a>ยืนยันไฟล์ Positive Pay
หลังจากที่เช็คที่ถูกรายการในไฟล์ positive pay ได้ถูกชำระ คุณจะได้รับหมายเลขการยืนยันจากธนาคารของคุณ  จากนั้น คุณสามารถยืนยันไฟล์ positive pay ได้  On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action. เมื่อคุณยืนยันไฟล์ positive pay จะมีการบันทึกหมายเลขใบยืนยันที่คุณได้รับจากธนาคาร

## <a name="recall-a-positive-pay-file"></a>เรียกคืนไฟล์ Positive Pay
ถ้าคุณต้องเปลี่ยนไฟล์ positive pay คุณสามารถเรียกคืนได้  On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action. สำหรับเช็คแต่ละรายการในไฟล์ positive pay ฟิลด์จะบ่งชี้ว่า เช็คที่ได้ถูกรวมในไฟล์ positive pay จะถูกรีเซ็ตหรือไม่  จากนั้นคุณสามารถสร้างไฟล์ positive pay ใหม่ที่รวมเช็คที่ถูกเรียกคืน


