---
title: "การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร"
description: "ไฟล์ใบแจ้งยอดจากธนาคารจำเป็นต้องตรงกับโครงร่างที่ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition รองรับ เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา"
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4feb77bf0031494dfd456c23c632a264c96f0e43
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a>การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร

[!include[banner](../includes/banner.md)]


ไฟล์ใบแจ้งยอดจากธนาคารจำเป็นต้องตรงกับโครงร่างที่ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition รองรับ เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา

<a name="what-is-the-error"></a>อะไรคือข้อผิดพลาด
------------------

หลังจากที่คุณพยายามจะนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร ไปที่ประวัติงานการจัดการข้อมูลและรายละเอียดการดำเนินการเพื่อค้นหาข้อผิดพลาด ข้อผิดพลาดสามารถช่วยได้โดยชี้ไปที่ใบแจ้งยอด ยอดดุล หรือรายการใบแจ้งยอด อย่างไรก็ตาม การให้ข้อมูลที่เพียงพอเพื่อช่วยให้คุณระบุฟิลด์หรือองค์ประกอบที่ทำให้เกิดปัญหาเป็นได้น้อยที่สุด

## <a name="what-are-the-differences"></a>อะไรคือความแตกต่าง
เปรียบเทียบคำนิยามโครงร่างไฟล์ธนาคารกับคำนิยามการนำเข้า Finance and Operations และสังเกตความแตกต่างในฟิลด์และองค์ประกอบ เปรียบเทียบไฟล์ใบแจ้งยอดจากธนาคารกับไฟล์ตัวอย่าง Finance and Operations ที่เกี่ยวข้อง ในไฟล์ ISO20022 ควรเห็นความแตกต่างได้อย่างชัดเจน

## <a name="transformations"></a>การแปลงข้อมูล
โดยทั่วไป ต้องทำการเปลี่ยนแปลงอย่างใดอย่างหนึ่งจากการแปลงข้อมูลสามอย่างนี้ การแปลงข้อมูลแต่ละรายการจะถูกเขียนสำหรับมาตรฐานเฉพาะ

| ชื่อทรัพยากร                                         | ชื่อไฟล์                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>การดีบักการแปลงข้อมูล
### <a name="adjust-the-bai2-and-mt940-files"></a>ปรับปรุงไฟล์ BAI2 และ MT940

ไฟล์ BAI2 และ MT940 คือไฟล์ข้อความและจำเป็นต้องมีการปรับปรุงเพื่อเปิดใช้งานการดีบัก Extensible Stylesheet Language Transformations (XSLT) โปรแกรมจะทำการปรับปรุงนี้เมื่อมีการนำเข้าไฟล์

1.  สร้างไฟล์ XML และคัดลอกข้อความต่อไปนี้ลงในไฟล์นั้น

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  คัดลอกเนื้อหาของไฟล์ใบแจ้งยอดจากธนาคาร และวางลงในไฟล์ XML เพื่อแทนที่ **PASTESTATEMENTFILEHERE**

### <a name="debug-the-xslt"></a>ดีบัก XSLT

สำหรับข้อมูลเพิ่มเติม ให้ดู <https://msdn.microsoft.com/en-us/library/ms255605.aspx>

1.  เริ่มต้น Microsoft Visual Studio
2.  สร้างแอพลิเคชันคอนโซล
3.  เปิด XSLT ที่เหมาะสม
4.  คลิก XLST และหน้าคุณสมบัติ
5.  ตั้งค่าข้อมูลป้อนเข้าไปยังที่ตั้งของไฟล์ใบแจ้งยอดจากธนาคาร
6.  กำหนดที่ตั้งและชื่อไฟล์สำหรับเอาท์พุท
7.  ตั้งค่าจุดหยุดพักที่กำหนด
8.  บนเมนู คลิก **XML** &gt; **เริ่มต้นการดีบัก XSLT**

### <a name="format-the-xslt-output"></a>จัดรูปแบบเอาท์พุท XSLT

เมื่อรันการแปลงข้อมูล ระบบจะสร้างไฟล์เอาท์พุทที่คุณสามารถดูใน Visual Studio ได้ ใช้ Ctrl+A, Ctrl+K และ Ctrl+D ในการจัดรูปแบบไฟล์เอาท์พุทอย่างรวดเร็ว

### <a name="adjust-the-transformation"></a>ปรับปรุงการแปลงข้อมูล

ปรับปรุงการแปรงข้อมูลเพื่อรับฟิลด์หรือองค์ประกอบที่เหมาะสมในไฟล์ใบแจ้งยอดจากธนาคาร จากนั้น แม็ปฟิลด์หรือองค์ประกอบนั้นไปยังองค์ประกอบ Finance and Operations ที่เหมาะสม

### <a name="debitcredit-indicator"></a>ตัวบ่งชี้เดบิต/เครดิต

บางครั้ง เดบิตอาจถูกนำเข้าเป็นเครดิต และเครดิตอาจถูกนำเข้าเป็นเดบิต เพื่อแก้ไขปัญหานี้ คุณต้องเปลี่ยน XSLT ที่เหมาะสม ถ้าใบแจ้งยอดจากธนาคารมาจากหลายธนาคาร ตรวจสอบให้แน่ใจว่าใบแจ้งยอดทั้งหมดใช้วิธีการเดบิต/เครดิตเดียวกัน หรือสร้างการแปลงข้อมูลแยกต่างหาก

-   เท็มเพลต BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator
-   เท็มเพลต ISO20022XML-to-Reconcilation.xslt GetCreditDebit
-   เท็มเพลต MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>ตัวอย่างรูปแบบและโครงร่างทางเทคนิคของใบแจ้งยอดจากธนาคาร
ตารางต่อไปนี้เป็นตัวอย่างคำนิยามโครงร่างทางเทคนิคของไฟล์การนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูงและไฟล์ตัวอย่างสามรายการของใบแจ้งยอดจากธนาคารที่เกี่ยวข้อง: คุณสามารถดาวน์โหลดไฟล์ตัวอย่างและโครงร่างทางเทคนิคที่นี่: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| คำนิยามโครงร่างทางเทคนิค                             | ไฟล์ตัวอย่างใบแจ้งยอดจากธนาคาร          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |






