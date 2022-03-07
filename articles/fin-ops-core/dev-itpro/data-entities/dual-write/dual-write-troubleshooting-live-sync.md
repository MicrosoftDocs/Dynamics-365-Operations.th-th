---
title: แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: df184decdfa900ccb5c2070575e55052b9dfc547
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062374"
---
# <a name="troubleshoot-live-synchronization-issues"></a>แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง

[!include [banner](../../includes/banner.md)]



หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาสำหรับการรวมข้อมูลด้วยการรวมแบบสองทิศทางระหว่างแอปการเงินและการดำเนินงานกับ Microsoft Dataverse กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Azure Active Directory (Azure AD) แต่ละส่วนอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวเฉพาะหรือไม่

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>การซิงโครไนส์ที่เริ่มใช้งานจริงแสดงข้อผิดพลาดเมื่อคุณสร้างแถว

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างแถวในแอปการเงินและการดำเนินงาน:

*\[{\\"ข้อผิดพลาด\\":{\\"รหัส\\":\\"0x80072560\\",\\"ข้อความ\\":\\"ผู้ใช้ไม่ใช่สมาชิกขององค์กร\\"}}\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต"}}"*

เมื่อต้องการแก้ไขปัญหานี้ ให้ทำตามขั้นตอนใน [ข้อกำหนดของระบบและข้อกำหนดเบื้องต้น](requirements-and-prerequisites.md) เมื่อต้องการดำเนินการตามขั้นตอนดังกล่าวให้เสร็จสมบูรณ์ ผู้ใช้แอปพลิเคชันการรวมแบบสองทิศทางที่สร้างขึ้นใน Dataverse ต้องมีบทบาทผู้ดูแลระบบ นอกจากนี้ ทีมงานที่เป็นเจ้าของเริ่มต้นต้องมีบทบาทผู้ดูแลระบบ

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>การซิงโครไนส์ที่เริ่มใช้งานจริงแสดงข้อผิดพลาดเมื่อคุณพยายามบันทึกข้อมูลตาราง

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามบันทึกข้อมูลตารางในแอปการเงินและการดำเนินงาน:

*ไม่สามารถบันทึกการเปลี่ยนแปลงไปยังฐานข้อมูล หน่วยของงานไม่สามารถส่งธุรกรรมได้ ไม่สามารถเขียนข้อมูลไปยังเอนทิตี้ uoms ได้ เขียนไปยัง UnitOfMeasureEntity ล้มเหลว โดยมีข้อความแสดงข้อผิดพลาดว่า ไม่สามารถซิงค์กับเอนทิตี้ uoms ได้*

เมื่อต้องการแก้ไขปัญหานี้ คุณต้องตรวจสอบให้แน่ใจว่ามีข้อมูลอ้างอิงของข้อกำหนดเบื้องต้นอยู่ในทั้งแอปการเงินและการดำเนินงานและ Dataverse ตัวอย่างเช่น ถ้าเรกคอร์ดลูกค้าเป็นของกลุ่มลูกค้าหนึ่งๆ โปรดตรวจสอบให้แน่ใจว่ามีเรกคอร์ดกลุ่มลูกค้าอยู่ใน Dataverse

ถ้ามีข้อมูลอยู่ในทั้งสองที่ และคุณยืนยันว่าปัญหานี้ไม่เกี่ยวข้องกับข้อมูล ให้ทำตามขั้นตอนต่อไปนี้

1. เปิดเอนทิตี **DualWriteProjectConfigurationEntity** โดยใช้ add-in ของ Excel เมื่อต้องการใช้ Add in ให้เปิดใช้งานโหมดการออกแบบใน Add in ของ Excel ของการเงินและการดำเนินงาน และเพิ่ม **DualWriteProjectConfigurationEntity** ลงในเวิร์กชีต สำหรับข้อมูลเพิ่มเติม ให้ดู [ดูและอัปเดตข้อมูลเอนทิตีด้วย Excel](../../office-integration/use-excel-add-in.md)
2. เลือกและลบเรกคอร์ดที่มีปัญหาในแผนผังการรวมแบบสองทิศทางและโครงการ จะมีสองเรกคอร์ดสำหรับทุกแผนผังการรวมแบบสองทิศทาง
3. เผยแพร่การเปลี่ยนแปลงโดยใช้ Add-in ของ Excel ขั้นตอนนี้สําคัญเนื่องจากขั้นตอนนี้จะลบเรกคอร์ดออกจากเอนทิตีและตารางพื้นฐาน

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>จัดการข้อผิดพลาดของสิทธิ์ในการอ่านหรือเขียน เมื่อคุณสร้างข้อมูลในแอปการเงินและการดำเนินงาน

คุณอาจได้รับข้อความแสดงข้อผิดพลาด "คำขอไม่ถูกต้อง" เมื่อคุณสร้างข้อมูลในแอปการเงินและการดำเนินงาน

![ตัวอย่างของข้อความแสดงข้อผิดพลาด คำขอไม่ถูกต้อง](media/error_record_id_source.png)

เมื่อต้องการแก้ไขปัญหานี้ คุณต้องเปิดใช้งานสิทธิ์ที่ขาดหายไปโดยการกำหนดบทบาทความปลอดภัยที่ถูกต้องให้กับทีมงานของหน่วยธุรกิจของ Dynamics 365 Sales หรือ Dynamics 365 Customer Service

1. ในแอปการเงินและการดำเนินงาน ให้ค้นหาหน่วยธุรกิจที่ถูกแมปในชุดการเชื่อมต่อการรวมข้อมูล

    ![การแมปองค์กร](media/mapped_business_unit.png)

2. ในแอปการมีส่วนร่วมของลูกค้า ลงชื่อเข้าใช้ในสภาพแวดล้อม ไปที่ **การตั้งค่า \> การรักษาความปลอดภัย** และค้นหาทีมงานของหน่วยธุรกิจที่ถูกแมป

    ![ทีมงานของหน่วยธุรกิจที่ถูกแมป](media/setting_security_page.png)

3. เปิดหน้าของทีมงานเพื่อแก้ไข แล้วเลือก **จัดการบทบาท**

    ![ปุ่มจัดการบทบาท](media/manage_team_roles.png)

4. ในกล่องโต้ตอบ **จัดการบทบาททีมงาน** ให้กําหนดบทบาทที่มีสิทธิ์อ่าน/เขียนให้กับตารางที่เกี่ยวข้อง แล้วเลือก **ตกลง**

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>แก้ปัญหาการซิงโครไนส์ในสภาพแวดล้อมที่มีสภาพแวดล้อม Dataverse ที่มีการเปลี่ยนแปลงล่าสุด

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างข้อมูลในแอปการเงินและการดำเนินงาน:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**ไม่สามารถสร้างส่วนข้อความสำหรับเอนทิตี้ CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"การสร้างส่วนข้อความล้มเหลวโดยมีข้อผิดพลาด URI ที่ไม่ถูกต้อง: URI ว่างเปล่า"}\],"isErrorCountUpdated":true}*

นี่คือข้อความแสดงข้อผิดพลาดในแอปการมีส่วนร่วมของลูกค้า:

> เกิดข้อผิดพลาดที่ไม่คาดคิดจากรหัส ISV (เกิดข้อผิดพลาดที่ไม่คาดคิดจากรหัส ISV (ErrorType = ClientError) ข้อยกเว้นที่ไม่คาดคิดจากปลั๊กอิน (ดำเนินการ): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: ล้มเหลวในการประมวลผลบัญชีเอนทิตี้ - (ความพยายามในการเชื่อมต่อล้มเหลว เนื่องจากฝ่ายที่เชื่อมต่อไม่ได้ตอบสนองอย่างถูกต้องหลังจากระยะเวลาหนึ่ง หรือการเชื่อมต่อที่สร้างล้มเหลว เนื่องจากโฮสต์ที่เชื่อมต่อล้มเหลวในการตอบสนอง

ข้อผิดพลาดนี้จะเกิดขึ้นหากสภาพแวดล้อม Dataverse ถูกรีเซ็ตอย่างไม่ถูกต้องเมื่อคุณพยายามที่จะสร้างข้อมูลในแอปการเงินและการดำเนินงาน

> [!IMPORTANT]
> ถ้าคุณเชื่อมโยงสภาพแวดล้อมใหม่แล้ว คุณต้องหยุดการแมปเอนทิตีทั้งหมดก่อนที่คุณจะปฏิบัติตามขั้นตอนการลดระดับความเสี่ยงต่อไป

เมื่อต้องการแก้ไขปัญหา คุณต้องปฏิบัติตามขั้นตอนทั้งในแอป Dataverse และการเงินและการดำเนินงานให้เสร็จสมบูรณ์

1. ในแอปการเงินและการดำเนินงาน ให้ปฏิบัติตามขั้นตอนเหล่านี้

    1. เปิดเอนทิตี **DualWriteProjectConfigurationEntity** โดยใช้ add-in ของ Excel เมื่อต้องการใช้ Add in ให้เปิดใช้งานโหมดการออกแบบใน Add in ของ Excel ของการเงินและการดำเนินงาน และเพิ่ม **DualWriteProjectConfigurationEntity** ลงในเวิร์กชีต สำหรับข้อมูลเพิ่มเติม ให้ดู [ดูและอัปเดตข้อมูลเอนทิตีด้วย Excel](../../office-integration/use-excel-add-in.md)
    2. เลือกและลบเรกคอร์ดที่มีปัญหาในแผนผังการรวมแบบสองทิศทางและโครงการ จะมีสองเรกคอร์ดสำหรับทุกแผนผังการรวมแบบสองทิศทาง
    3. เผยแพร่การเปลี่ยนแปลงโดยใช้ Add-in ของ Excel ขั้นตอนนี้สําคัญเนื่องจากขั้นตอนนี้จะลบเรกคอร์ดออกจากเอนทิตีและตารางพื้นฐาน
    4. เพื่อช่วยป้องกันข้อผิดพลาดเมื่อคุณเชื่อมโยงสภาพแวดล้อมการเงินและการดำเนินงานหรือ Dataverse อีกครั้ง ให้ตรวจสอบให้แน่ใจว่าไม่มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางอยู่

2. ใน Dataverse ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ลงชื่อเข้าใช้สภาพแวดล้อม Dataverse ของคุณ (ตัวอย่างเช่น `https://*****.crm.dynamics.com/`)
    2. ไปที่ **การตั้งค่าขั้นสูง** \> **การค้นหาขั้นสูง**
    3. เลือก **การตั้งค่าคอนฟิก DualWrite Runtime**
    4. เลือกคอลัมน์เพื่อดู
    5. เลือก **ผลลัพธ์** เพื่อดูการตั้งค่าคอนฟิก
    6. ลบอินสแตนซ์ทั้งหมด

3. ในแอปการเงินและการดำเนินงาน ให้ปฏิบัติตามขั้นตอนเหล่านี้

    1. เปิดเอนทิตี **DualWriteProjectConfigurationEntity** โดยใช้ add-in ของ Excel เมื่อต้องการใช้ Add in ให้เปิดใช้งานโหมดการออกแบบใน Add in ของ Excel ของการเงินและการดำเนินงาน และเพิ่ม **DualWriteProjectConfigurationEntity** ลงในเวิร์กชีต สำหรับข้อมูลเพิ่มเติม ให้ดู [ดูและอัปเดตข้อมูลเอนทิตีด้วย Excel](../../office-integration/use-excel-add-in.md)
    2. เลือกและลบเรกคอร์ดที่มีปัญหาในแผนผังการรวมแบบสองทิศทางและโครงการ จะมีสองเรกคอร์ดสำหรับทุกแผนผังการรวมแบบสองทิศทาง
    3. เผยแพร่การเปลี่ยนแปลงโดยใช้ Add-in ของ Excel ขั้นตอนนี้สําคัญเนื่องจากขั้นตอนนี้จะลบเรกคอร์ดออกจากเอนทิตีและตารางพื้นฐาน
    4. เพื่อช่วยป้องกันข้อผิดพลาดเมื่อคุณเชื่อมโยงสภาพแวดล้อมการเงินและการดำเนินงานหรือ Dataverse อีกครั้ง ให้ตรวจสอบให้แน่ใจว่าไม่มีการตั้งค่าคอนฟิกการรวมแบบสองทิศทางอยู่

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>ข้อผิดพลาดในการซิงโครไนส์ที่เริ่มใช้งานจริงหลังจากที่คุณคัดลอกฐานข้อมูลแบบเต็มแล้ว

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้หลังจากที่คุณเรียกใช้การคัดลอกฐานข้อมูลแบบเต็มจากระบบหนึ่งไปยังระบบอื่น จากนั้นลองเรียกใช้การดําเนินงานฐานข้อมูล:

*SecureConfig Organization (???) ไม่ตรงกับองค์กร CRM (???) จริง*

ข้อความแสดงข้อผิดพลาดจะแสดงขึ้นจากปลั๊กอินรันไทม์การรวมแบบสองทิศทางเพื่อให้มั่นใจว่าการตั้งค่าคอนฟิกการรวมแบบสองทิศทางที่ตั้งค่าในระบบหนึ่งไม่สามารถใช้ในระบบอื่นได้

เมื่อต้องการแก้ไขปัญหา ให้ลบเรกคอร์ดทั้งหมดในตาราง **msdyn_dualwriteruntimeconfig** หลังจากที่คุณคืนค่าฐานข้อมูล สำหรับข้อมูลเพิ่มเติม ให้ดู [ยกเลิกการเชื่อมโยงและเชื่อมโยงสภาพแวดล้อมการรวมแบบสองทิศทางอีกครั้ง](relink-environments.md)

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>ปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริงที่เกิดจากไวยากรณ์ตัวกรองการสอบถามที่ไม่ถูกต้องในแผนผังการรวมแบบสองทิศทาง

ถึงแม้ว่านิพจน์การสอบถามของตัวกรองข้อมูลแผนผังการรวมแบบสองทิศทางจะถูกต้องตามหลักเดียวกัน แต่ก็อาจไม่ได้ผลตามที่คาดไว้ นิพจน์ตัวกรองอยู่ในเอนทิตี ไม่ใช่บนแหล่งข้อมูลแต่ละแหล่งของออบเจ็กต์การสอบถาม ดังนั้น การสอบถาม SQL ที่สร้างขึ้นจะไม่ส่งคืนผลลัพธ์ที่คาดไว้

นี่คือตัวอย่าง

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

คุณอาจคาดว่าโครงการที่ไม่มีข้อมูลหลักจะถูกกรองออก อย่างไรก็ตาม ตัวกรองข้อมูลไม่ทำงาน เนื่องจากถูกแปลเป็นการสอบถามที่มีลักษณะคล้ายกับตัวอย่างต่อไปนี้

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

ผลลัพธ์จริงคือ ฟิลด์ `parentProject` ถูกประเมินเป็น `null` อย่างไรก็ตาม `null` ไม่เหมือนกับสตริงที่ว่างเปล่า เนื่องจากตัวกรองข้อมูลการสอบถามไม่ตรงกัน การส่งคืนผลลัพธ์จึงไม่ถูกต้อง

เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

1. เพิ่มคอลัมน์ที่คำนวณซึ่งสามารถเพิ่มในแบบจำลองส่วนขยาย และได้รับการสนับสนุนโดยตรรกะที่แปลง `null` เป็นสตริงที่ว่างเปล่า

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. ใช้ตัวกรองในคอลัมน์ที่คำนวณใหม่แทนคอลัมน์ค่าเริ่มต้น

เมื่อต้องการประเมินตัวกรองในสภาพแวดล้อมการพัฒนา คุณสามารถใช้รหัส X++ ต่อไปนี้เพื่อตรวจสอบความถูกต้องของผลลัพธ์ เรัยกใช้รหัสนี้เป็นโปรแกรมที่แยกต่างหาก คุณสามารถใช้ตัวกรองข้อมูลเพื่อประเมินตัวกรองชนิดต่างๆ ที่ใช้ได้กับเอนทิตีก่อนที่คุณจะใช้ตัวกรองข้อมูลเหล่านั้นบนแผนผังการรวมแบบสองทิศทาง คุณสามารถเรียกใช้การสอบถามกับฐานข้อมูลเพื่อประเมินความขัดแย้งได้

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>ข้อมูลจากแอปการเงินและการดําเนินงานไม่ได้ซิงค์กับ Dataverse

ในระหว่างการซิงโครไนส์ที่เริ่มใช้งานจริง คุณอาจพบปัญหาที่มีการซิงค์ข้อมูลจากแอปการเงินและการดําเนินงานไปยัง Dataverse เพียงบางส่วนเท่านั้น หรือข้อมูลไม่ซิงค์เลย

> [!NOTE]
> คุณต้องแก้ไขปัญหานี้ในระหว่างการพัฒนา

ก่อนที่คุณจะเริ่มแก้ไขปัญหา ให้ทบทวนข้อกำหนดเบื้องต้นต่อไปนี้:

+ ตรวจสอบให้แน่ใจว่าการเปลี่ยนแปลงแบบกำหนดเองของคุณเขียนขึ้นในขอบข่ายธุรกรรมเดียว
+ เหตุการณ์ทางธุรกิจและกรอบงานการรวมแบบสองทิศทางจะไม่จัดการการดําเนินงาน `doinsert()`, `doUpdate()` และ `recordset()` หรือเรกคอร์ดที่มีการเลือก `skipBusinessEvents(true)` ถ้ารหัสของคุณอยู่ภายในฟังก์ชันเหล่านี้ การรวมแบบสองทิศทางจะไม่ทริกเกอร์
+ เหตุการณ์ทางธุรกิจต้องลงทะเบียนสำหรับแหล่งข้อมูลที่แมป แหล่งข้อมูลบางแหล่งอาจใช้ตัวเชื่อมภายนอกและอาจถูกเลือกเป็นอ่านอย่างเดียวในแอปการเงินและการดําเนินงาน แหล่งข้อมูลเหล่านี้ไม่มีการติดตาม
+ การเปลี่ยนแปลงจะถูกทริกเกอร์เฉพาะเมื่อการแก้ไขอยู่ในฟิลด์ที่แมปเท่านั้น การแก้ไขฟิลด์ที่ยกเลิกการแมปจะไม่ทริกเกอร์การรวมแบบสองทิศทาง
+ ตรวจสอบให้แน่ใจว่าการประเมินตัวกรองให้ผลลัพธ์ที่ถูกต้อง

### <a name="troubleshooting-steps"></a>ขั้นตอนการแก้ไขปัญหา

1. ตรวจทานการแมปฟิลด์ในหน้าการดูแลระบบการรวมแบบสองทิศทาง หากฟิลด์ไม่ได้แมปจากแอปการเงินและการดําเนินงานไปยัง Dataverse ฟิลด์จะไม่มีการติดตาม ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ ฟิลด์ **คำอธิบาย** จะถูกติดตามจาก Dataverse แต่ไม่ใช่จากแอปการเงินและการดำเนินงาน ไม่มีการติดตามการเปลี่ยนแปลงกับฟิลด์ภายในแอปการเงินและการดำเนินงาน

    ![ฟิลด์ที่มีการติดตาม](media/live-sync-troubleshooting-1.png)

2. ระบุว่าแหล่งข้อมูลมีการติดตามในนิยามเหตุการณ์ทางธุรกิจหรือไม่ ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ จะไม่มีฟิลด์จากตาราง **DefaultDimensionDAVs** และตารางพื้นฐานจะถูกติดตามการเปลี่ยนแปลง แหล่งข้อมูลที่ใช้ตัวเชื่อมภายนอกและที่ทำเครื่องหมายเป็นอ่านอย่างเดียวไม่มีการติดตาม

    ![ฟิลด์ที่ไม่ได้ติดตาม](media/live-sync-troubleshooting-2.png)

3. ระบุว่าฟิลด์ตารางที่แมปจะปรากฏในตาราง **BUSINESSEVENTSDEFINITION** ดังที่แสดงในภาพประกอบต่อไปนี้หรือไม่ ถ้าคุณไม่พบฟิลด์ที่คุณค้นหาในผลลัพธ์ของการสอบถาม ฟิลด์จะไม่ทริกเกอร์ด้วยการรวมแบบสองทิศทาง

    ![ฟิลด์ที่ติดตามในตาราง](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>ตัวอย่างสถานการณ์จำลอง

ในแอปการเงินและการดำเนินงาน จะมีการอัปเดตที่อยู่ของเรกคอร์ดผู้ติดต่อ แต่การเปลี่ยนแปลงที่อยู่ไม่ได้ซิงค์กับ Dataverse สถานการณ์นี้จะเกิดขึ้นเนื่องจากไม่มีเรกคอร์ดในตาราง **BusinessEventsDefinition** ที่มีชุดของตารางที่ได้รับผลกระทบและเอนทิตี โดยเฉพาะ ตาราง **LogisticsPostalAddress** ไม่ใช่แหล่งข้อมูลโดยตรงของเอนทิตี **smmContactpersonCDSV2Entity** เอนทิตี **smmContactpersonCDSV2Entity** มี **smmContactPersonV2Entity** เป็นแหล่งข้อมูล และ **smmContactPersonV2Entity** จึงมี **LogisticsPostalAddressBaseEntity** เป็นแหล่งข้อมูล ตาราง **LogisticsPostalAddress** คือแหล่งข้อมูลของ **LogisticsPostalAddressBaseEntity**

สถานการณ์ที่คล้ายกันอาจเกิดขึ้นในบางรูปแบบที่ไม่ใช่รูปแบบมาตรฐาน เช่น กรณีที่มีการแก้ไขตารางในแอปการเงินและการดำเนินงาน ไม่ได้เชื่อมโยงกับเอนทิตีที่มีสถานการณ์ดังกล่าวอยู่ ตัวอย่างเช่น ข้อมูลที่อยู่หลักจะถูกคำนวณบนเอนทิตี **smmContactPersonCDSV2Entity** กรอบงานการรวมแบบสองทิศทางพยายามระบุว่าการเปลี่ยนแปลงในตารางพื้นฐานถูกแมปกลับไปยังเอนทิตีอย่างไร โดยปกติ วิธีการนี้เพียงพอแล้ว อย่างไรก็ตาม ในบางกรณี ลิงค์จะซับซ้อนมากที่คุณจำเป็นต้องระบุ คุณต้องตรวจสอบให้แน่ใจว่า **RecId** ของตารางที่เกี่ยวข้องมีอยู่ในเอนทิตีโดยตรง แล้วเพิ่มวิธีการแบบคงที่เพื่อตรวจสอบตารางสำหรับการเปลี่ยนแปลง

ตัวอย่างเช่น รีวิววิธีการ **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()** **CustCustomerV3entity** และ **VendVendorV2Entity** มีการแก้ไขเพื่อจัดการสถานการณ์นี้

เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

1. เพิ่มฟิลด์ **PrimaryPostalAddressRecId** ลงในเอนทิตี **smmContactPersonV2Entity** ทำให้เป็นภายใน

    ![ฟิลด์ที่เพิ่มในเอนทิตี smmContactPersonV2Entity](media/Troubleshoot_live_sync_issue_1.png)

2. เพิ่มฟิลด์เดียวกันในเอนทิตี **smmContactPersonCDSV2Entity**

    ![ฟิลด์ที่เพิ่มในเอนทิตี smmContactPersonCDSV2Entity](media/Troubleshoot_live_sync_issue_2.png)

3. เพิ่มวิธีการต่อไปนี้ลงในคลาส **smmContactPersonCDSV2Entity**

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. ซิงค์ฐานข้อมูล และสร้างใบสมัคร
5. หยุดแผนผังการรวมแบบสองทิศทางทั้งหมดที่สร้างขึ้นบนเอนทิตี **smmContactPersonCDSV2Entity**
6. เริ่มต้นการแมป คุณควรเห็นตารางใหม่ (**LogisticsPostalAddress** ในตัวอย่างนี้) ที่คุณเริ่มติดตามโดยใช้คอลัมน์ **RefTableName** ของแถวที่ค่า **refentityname** เท่ากับ **smmContactPersonCDSV2Entity** ในตาราง **BusinessEventsDefinition**

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>เกิดข้อผิดพลาดเมื่อคุณสร้างเรกคอร์ดที่มีการส่งหลายเรกคอร์ดจากแอปการเงินและการดำเนินงานไปยัง Dataverse ในชุดงานเดียวกัน

สำหรับธุรกรรมใดๆ แอปการเงินและการดำเนินงานจะสร้างข้อมูลในชุดงานและส่งข้อมูลเป็นชุดงานไปยัง Dataverse หากมีการสร้างสองเรกคอร์ดเป็นส่วนหนึ่งของธุรกรรมเดียวกัน และทั้งสองเรกคอร์ดอ้างอิงกัน คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่มีลักษณะคล้ายกับตัวอย่างต่อไปนี้ในแอปการเงินและการดำเนินงาน:

*ไม่สามารถเขียนข้อมูลไปยังเอนทิตี aaa_fundingsources ไม่สามารถค้นหา ebecsfs_contracts ด้วยค่า {PC00...} ไม่สามารถค้นหา aaa_fundingsources ด้วยค่า {PC00...} เขียนไปยัง aaa_fundingsources โดยมีข้อความแสดงข้อผิดพลาดเกี่ยวกับข้อยกเว้น: เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (400) คำขอไม่ถูกต้อง*

เมื่อต้องการแก้ไขปัญหา ให้สร้างความสัมพันธ์เอนทิตีในแอปการเงินและการดำเนินงานเพื่อระบุว่าทั้งสองเอนทิตี้เกี่ยวข้องกัน และมีการจัดการ เรกคอร์ดที่เกี่ยวข้องในธุรกรรมเดียวกัน

## <a name="enable-verbose-logging-of-error-messages"></a>เปิดใช้งานการบันทึก verbose ของข้อความแสดงข้อผิดพลาด

ในแอปการเงินและการดำเนินงาน คุณอาจพบข้อผิดพลาดที่เกี่ยวข้องกับสภาพแวดล้อม Dataverse ข้อความแสดงข้อผิดพลาดอาจไม่มีข้อความทั้งหมดของข้อความหรือข้อมูลที่เกี่ยวข้องอื่นๆ หากต้องการได้รับข้อมูลเพิ่มเติม คุณสามารถเปิดใช้งานการบันทึกรายละเอียดโดยการตั้งค่าแฟล็ก **IsDebugMode** ที่มีอยู่ในเอนทิตี้ **DualWriteProjectConfigurationEntity** ในการตั้งค่าคอนฟิกโครงการทั้งหมดในแอปการเงินและการดำเนินงาน

1. เปิดเอนทิตี **DualWriteProjectConfigurationEntity** โดยใช้ add-in ของ Excel เมื่อต้องการใช้ Add in ให้เปิดใช้งานโหมดการออกแบบใน Add in ของ Excel ของการเงินและการดำเนินงาน และเพิ่ม **DualWriteProjectConfigurationEntity** ลงในเวิร์กชีต สำหรับข้อมูลเพิ่มเติม ให้ดู [ดูและอัปเดตข้อมูลเอนทิตีด้วย Excel](../../office-integration/use-excel-add-in.md)
2. ตั้งค่าแฟล็ก **IsDebugMode** เป็น **ใช่** สำหรับโครงการ
3. เรียกใช้สถานการณ์
4. บันทึก verbose พร้อมใช้งานในตาราง **DualWriteErrorLog** เมื่อต้องการค้นหาข้อมูลโดยใช้เบราเซอร์ตาราง ให้ใช้ URL ต่อไปนี้: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`
5. หากต้องการเก็บบันทึกเพิ่มเติมในโหมดดีบัก ให้ติดตั้งการอัปเดตใน [KB 4595434 (แก้ไขค่าว่างเปล่าที่เผยแพร่ในสคริปต์การซิงโครไนส์ที่เริ่มใช้งานจริงของการรวมแบบสองทิศทาง)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9)

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>เกิดข้อผิดพลาดเมื่อคุณเพิ่มที่อยู่ของลูกค้าหรือผู้ติดต่อ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้เมื่อคุณพยายามเพิ่มที่อยู่ของลูกค้าหรือผู้ติดต่อในแอปการเงินและการดำเนินงานหรือ Dataverse:

*ไม่สามารถเขียนข้อมูลไปยังเอนทิตี msdyn_partypostaladdresses เขียนไปยัง DirPartyPostalAddressLocationSEntity ล้มเหลวพร้อมกับข้อความแสดงข้อผิดพลาด คำขอล้มเหลวพร้อมกับรหัสสถานะ BadRequest และรหัสข้อผิดพลาด CDS: ข้อความตอบสนอง 0x80040265: เกิดข้อผิดพลาดขึ้นในปลั๊กอิน เรกคอร์ดที่มีค่าแอททริบิวต์มีรหัสที่ตั้งอยู่แล้ว คีย์รหัสที่ตั้งของคีย์เอนทิตีต้องการให้ชุดแอททริบิวต์นี้มีค่าเฉพาะ เลือกค่าเฉพาะและลองอีกครั้ง*

เมื่อต้องการแก้ไขปัญหา ให้ติดตั้งรุ่นแพคเกจการประสานกันของการรวมแบบสองทิศทาง (2.2.2.60) เพื่อให้คีย์ในตาราง **ที่อยู่** ถูกกําหนดดังที่แสดงในตารางต่อไปนี้

| คุณสมบัติ | มูลค่า |
|---|---|
| ชื่อที่แสดง | **คีย์ที่ตั้ง** |
| ชื่อ | **msdyn_locationkey** |
| ฟิลด์ | **msdyn_locationid**, **parentid** |
| สถานะ | **ใช้งานอยู่** |
| งานระบบ | ว่างเปล่า |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>เกิดข้อผิดพลาดเมื่อคุณเพิ่มลูกค้าใน Dataverse

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามเพิ่มลูกค้าใน Dataverse:

*"RecordError0":"Write ล้มเหลวในเอนทิตีลูกค้า V3 ที่มีข้อยกเว้นที่ไม่รู้จัก - ไม่พบเรกคอร์ดฝ่ายเกี่ยวกับชนิดฝ่าย 'องค์กร'"}*

เมื่อสร้างลูกค้าขึ้นใน Dataverse ระบบจะสร้างหมายเลขฝ่ายใหม่ ข้อความแสดงข้อผิดพลาดจะปรากฏขึ้นเมื่อเรกคอร์ดลูกค้าและฝ่ายถูกซิงค์กับแอปการเงินและการดำเนินงาน แต่มีเรกคอร์ดลูกค้าที่มีหมายเลขฝ่ายแตกต่างกันอยู่แล้ว

เมื่อต้องการแก้ไขปัญหา ให้ค้นหาลูกค้าผ่านการค้นหาฝ่าย ถ้าลูกค้ายังไม่มีอยู่ สร้างเรกคอร์ดลูกค้าใหม่ ถ้ามีลูกค้าอยู่ ให้ใช้ฝ่ายที่มีอยู่เพื่อสร้างเรกคอร์ดลูกค้าใหม่

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>ข้อผิดพลาดเมื่อคุณสร้างลูกค้า ผู้จัดจำหน่าย หรือผู้ติดต่อใหม่ใน Dataverse

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้เมื่อคุณพยายามสร้างลูกค้า ผู้จัดจำหน่าย หรือผู้ติดต่อใน Dataverse:

*ไม่สามารถอัปเดตชนิดของฝ่ายจาก 'DirOrganization' เป็น 'DirPerson' ควรลบฝ่ายที่มีอยู่ตามด้วยการแทรกชนิดใหม่แทน*

ใน Dataverse จะมีลำดับหมายเลขในตาราง **msdyn_party** เมื่อสร้างบัญชีใน Dataverse ฝ่ายใหม่จะถูกสร้างขึ้น (ตัวอย่างเช่น **ฝ่าย-001** ของชนิด **องค์กร**) ข้อมูลนี้จะส่งไปยังแอปการเงินและการดำเนินงาน ถ้ามีการรีเซ็ตสภาพแวดล้อม Dataverse หรือสภาพแวดล้อมการเงินและการดำเนินงานเชื่อมโยงกับสภาพแวดล้อม Dataverse อื่น จากนั้นมีการสร้างเรกคอร์ดผู้ติดต่อใหม่ใน Dataverse ค่าฝ่ายใหม่ที่เริ่มต้นด้วย **ฝ่าย-001** จะถูกสร้างขึ้น เวลานี้ เรกคอร์ดฝ่ายที่สร้างจะเป็น **ฝ่าย-001** ของชนิด **บุคคล** เมื่อซิงค์ข้อมูลนี้แล้ว แอปการเงินและการดำเนินงานจะแสดงข้อความแสดงข้อผิดพลาดก่อนหน้านี้ เนื่องจากมีเรกคอร์ด **ฝ่าย-001** ของชนิด **องค์กร** อยู่แล้ว

เมื่อต้องการแก้ไขปัญหา ให้เปลี่ยนลำดับหมายเลขอัตโนมัติของฟิลด์ **msdyn_partynumber** ของตาราง **msdyn_party** ใน Dataverse เป็นลำดับหมายเลขอัตโนมัติอื่น

## <a name="performance-issue-with-customer-or-contact-mappings"></a>ปัญหาประสิทธิภาพการแมปลูกค้าหรือผู้ติดต่อ

คุณอาจสามารถปรับปรุงประสิทธิภาพของการซิงโครไนส์ที่เริ่มใช้งานจริงของลูกค้าและผู้ติดต่อโดยการกำหนดวิธีการ **getEntityDataSourceToFieldMapping** (ในเอนทิตี **CustCustomerV3Entity**) และวิธีการ **getEntityDataSourceToFieldMapping** (ในเอนทิตี **smmContactPersonPERsonSV2Entity**) การกำหนดเองเหล่านี้จะลดจํานวนเรกคอร์ดในตาราง **BusinessEventsDefinition** การลดจํานวนเรกคอร์ดนี้ลดจํานวนเหตุการณ์ที่เกิดขึ้น

วิธีการ **getEntityDataSourceToFieldMapping** ในเอนทิตี **CustCustomerV3Entity** ทำให้แน่ใจว่าการอัปเดตที่อยู่อิเล็กทรอนิกส์ของลูกค้าหรือที่อยู่ไปรษณีย์จะทริกเกอร์เหตุการณ์ทางธุรกิจ เพื่อให้มีการส่งข้อมูลที่อัปเดตไปยัง Dataverse หากคุณไม่ได้ใช้ฟิลด์ทั้งหมดและไม่ต้องการข้อมูลในการรวมแบบสองทิศทาง ให้แสดงข้อคิดเห็นเกี่ยวกับรายการที่เหมาะสมในวิธีการ ทุกฟิลด์ที่ติดตามและตารางที่เพิ่มในวิธีการนี้จะเพิ่มเรกคอร์ดในตาราง **BusinessEventsDefinition** ให้กับชุดตารางที่ติดตามและเอนทิตีที่มีการติดตาม

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

ในลักษณะที่คล้ายกัน วิธีการ **getEntityDataSourceToFieldMapping** ในเอนทิตี **smmContactPersonCDSV2Entity** ทำให้แน่ใจว่าการอัปเดตที่อยู่อิเล็กทรอนิกส์ของลูกค้าหรือที่อยู่ไปรษณีย์จะทริกเกอร์เหตุการณ์ทางธุรกิจ เพื่อให้มีการส่งข้อมูลที่อัปเดตไปยัง Dataverse ในวิธีการนี้ คุณสามารถให้ข้อคิดเห็นเกี่ยวกับรายการในฟิลด์ใดๆ ที่คุณไม่ได้ใช้

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

หลังจากที่คุณอัปเดตวิธีการ ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ซิงค์ฐานข้อมูล และสร้างใบสมัคร
2. หยุดแผนผังการรวมแบบสองทิศทางทั้งหมดบนเอนทิตี **smmContactPersonCDSV2Entity** และ **CustCustomerV3Entity**
3. เริ่มต้นการแมป คุณควรดูเรกคอร์ดในเอนทิตี **smmContactPersonCDSV2Entity** และ **CustCustomerV3Entity** และตาราง **BusinessEventsDefinition** และประสิทธิภาพอาจปรับปรุงเป็นระยะๆ

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
