---
title: การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร
description: บทความนี้อธิบายวิธีแก้ไขปัญหาที่มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151774"
---
# <a name="bank-statement-file-import-troubleshooting"></a>การแก้ไขปัญหาการนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร

[!include [banner](../includes/banner.md)]

>[!NOTE]
>ฟังก์ชันนี้จะไม่ได้รับการสนับสนุนในเดือนกันยายน 2022 ผู้ใช้ใหม่ควรใช้การรายงานทางอิเล็กทรอนิกส์

ถือเป็นสิ่งสำคัญที่ไฟล์ใบแจ้งยอดจากธนาคารต้องตรงกับเค้าโครงที่ Microsoft Dynamics 365 Finance รองรับ เนื่องด้วยมาตรฐานที่เข้มงวดของใบแจ้งยอดจากธนาคาร การรวมส่วนใหญ่จะทำงานอย่างถูกต้อง อย่างไรก็ตาม บางครั้งไม่สามารถนำเข้าไฟล์ใบแจ้งยอดได้ หรือมีผลลัพธ์ที่ไม่ถูกต้อง โดยทั่วไป ปัญหาเหล่านี้มีสาเหตุมาจากความแตกต่างเล็ก ๆ น้อย ๆ ในไฟล์ใบแจ้งยอดจากธนาคาร บทความนี้อธิบายวิธีการแก้ไขความแตกต่างเหล่านี้ และวิธีการแก้ไขปัญหา

## <a name="what-is-the-error"></a>อะไรคือข้อผิดพลาด

หลังจากที่คุณพยายามจะนำเข้าไฟล์ใบแจ้งยอดจากธนาคาร ไปที่ประวัติงานการจัดการข้อมูลและรายละเอียดการดำเนินการเพื่อค้นหาข้อผิดพลาด ข้อผิดพลาดสามารถช่วยได้โดยชี้ไปที่ใบแจ้งยอด ยอดดุล หรือรายการใบแจ้งยอด อย่างไรก็ตาม การให้ข้อมูลที่เพียงพอเพื่อช่วยให้คุณระบุฟิลด์หรือองค์ประกอบที่ทำให้เกิดปัญหาเป็นได้น้อยที่สุด

> [!NOTE]
> ใบแจ้งยอดจากธนาคารที่นําเข้าสามารถทับซ้อนกับใบแจ้งยอดจากธนาคารเดียว ณ เวลาหนึ่งๆ เท่านั้น  ตัวอย่างเช่น ถ้ารายงานสิ้นสุดที่ 12:00 น. ในวันที่ 1 มกราคม 2021 วันที่เริ่มต้นของรายงานถัดไปจะเป็น 12:00 น. ในวันที่ 1 มกราคม 2021 12:00:00 น.

## <a name="what-are-the-differences"></a>อะไรคือความแตกต่าง
เปรียบเทียบคำนิยามโครงร่างไฟล์ธนาคารกับคำนิยามการนำเข้าทางการเงิน และสังเกตความแตกต่างในฟิลด์และองค์ประกอบ เปรียบเทียบไฟล์ใบแจ้งยอดกับไฟล์ตัวอย่างทางการเงินที่เกี่ยวข้อง ในไฟล์ ISO20022 ควรเห็นความแตกต่างได้อย่างชัดเจน

## <a name="time-zone-differences-on-imported-bank-statements"></a>ความแตกต่างของโซนเวลาในใบแจ้งยอดจากธนาคารที่นำเข้า
ค่าวันที่ในไฟล์นำเข้าอาจแตกต่างจากค่าเวลาที่แสดงในการเงินและการดำเนินงาน เพื่อป้องกันไม่ให้เกิดความขัดแย้ง ให้ **ป้อนการตั้ง** ค่าโซนเวลาบนหน้าตั้งค่าคอนฟิกแหล่งข้อมูล สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการป้อนข้อมูลการกำหนดลักษณะโซนเวลา ดู [ตั้งค่ากระบวนการนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูง](set-up-advanced-bank-reconciliation-import-process.md)

## <a name="transformations"></a>การแปลง
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

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  คัดลอกเนื้อหาของไฟล์ใบแจ้งยอดจากธนาคาร และวางลงในไฟล์ XML เพื่อแทนที่ **PASTESTATEMENTFILEHERE**

### <a name="debug-the-xslt"></a>ดีบัก XSLT

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ <https://msdn.microsoft.com/library/ms255605.aspx>

1.  เริ่มต้น Microsoft Visual Studio
2.  สร้างแอปพลิเคชันคอนโซล
3.  เปิด XSLT ที่เหมาะสม
4.  คลิก XLST และหน้าคุณสมบัติ
5.  ตั้งค่าข้อมูลป้อนเข้าไปยังที่ตั้งของไฟล์ใบแจ้งยอดจากธนาคาร
6.  กำหนดที่ตั้งและชื่อไฟล์สำหรับเอาท์พุท
7.  ตั้งค่าจุดหยุดพักที่กำหนด
8.  บนเมนู คลิก **XML** &gt; **เริ่มต้นการดีบัก XSLT**

### <a name="format-the-xslt-output"></a>จัดรูปแบบเอาท์พุท XSLT

เมื่อการแปลงรัน จะสร้างไฟล์เอาต์พุตที่คุณสามารถดูได้ใน Visual Studio ใช้ Ctrl+A, Ctrl+K และ Ctrl+D ในการจัดรูปแบบไฟล์เอาท์พุทอย่างรวดเร็ว

### <a name="adjust-the-transformation"></a>ปรับปรุงการแปลงข้อมูล

ปรับปรุงการแปรงข้อมูลเพื่อรับฟิลด์หรือองค์ประกอบที่เหมาะสมในไฟล์ใบแจ้งยอดจากธนาคาร จากนั้น แม็ปฟิลด์หรือองค์ประกอบนั้นไปยังองค์ประกอบทางการเงินที่เหมาะสม

### <a name="debitcredit-indicator"></a>ตัวบ่งชี้เดบิต/เครดิต

บางครั้ง เดบิตอาจถูกนำเข้าเป็นเครดิต และเครดิตอาจถูกนำเข้าเป็นเดบิต เพื่อแก้ไขปัญหานี้ คุณต้องเปลี่ยน XSLT ที่เหมาะสม ถ้าใบแจ้งยอดจากธนาคารมาจากหลายธนาคาร ตรวจสอบให้แน่ใจว่าใบแจ้งยอดทั้งหมดใช้วิธีการเดบิต/เครดิตเดียวกัน หรือสร้างการแปลงข้อมูลแยกต่างหาก

-   เท็มเพลต BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator
-   เท็มเพลต ISO20022XML-to-Reconcilation.xslt GetCreditDebit
-   เท็มเพลต MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>ตัวอย่างรูปแบบและโครงร่างทางเทคนิคของใบแจ้งยอดจากธนาคาร
ตารางต่อไปนี้เป็นตัวอย่างคำนิยามโครงร่างทางเทคนิคของไฟล์การนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูงและไฟล์ตัวอย่างสามรายการของใบแจ้งยอดจากธนาคารที่เกี่ยวข้อง: คุณสามารถดาวน์โหลดไฟล์ตัวอย่างและโครงร่างทางเทคนิคได้ที่นี่: [นำเข้าไฟล์ตัวอย่าง](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| คำนิยามโครงร่างทางเทคนิค                             | ไฟล์ตัวอย่างใบแจ้งยอดจากธนาคาร          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

