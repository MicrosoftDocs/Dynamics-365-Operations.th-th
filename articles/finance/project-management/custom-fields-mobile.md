---
title: ใช้ฟิลด์ที่กำหนดเองสำหรับแอปมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android
description: หัวข้อนี้จะให้รูปแบบทั่วไปสำหรับการใช้ส่วนขยายในการใช้ฟิลด์ที่กำหนดเอง
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080783"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>ใช้ฟิลด์ที่กำหนดเองสำหรับแอปมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะให้รูปแบบทั่วไปสำหรับการใช้ส่วนขยายในการใช้ฟิลด์ที่กำหนดเอง จะครอบคลุมหัวข้อต่อไปนี้:

- ชนิดข้อมูลต่างๆ ที่โครงสร้างของฟิลด์ที่กำหนดเองสนับสนุน
- วิธีการแสดงฟิลด์แบบอ่านอย่างเดียวหรือที่สามารถแก้ไขได้ในรายการแผ่นเวลา และบันทึกค่าที่ผู้ใช้ระบุกลับไปยังฐานข้อมูล
- วิธีการแสดงฟิลด์แบบอ่านอย่างเดียวบนส่วนหัวของแผ่นเวลา
- วิธีการรวมตรรกะทางธุรกิจแบบกำหนดเองอื่นๆ เพื่อป้อนค่าเริ่มต้นในฟิลด์ และทำการตรวจสอบความถูกต้องเพิ่มเติม

## <a name="audience"></a>ผู้ชม

หัวข้อนี้มีไว้สำหรับนักพัฒนาที่กำลังรวมฟิลด์ที่กำหนดเองของพวกเขาเข้ากับแอพลิเคชันบนมือถือ Microsoft Dynamics 365 Project Timesheet ที่พร้อมใช้งานสำหรับ Apple iOS และ Google Android สมมติฐานคือ ผู้อ่านมีความคุ้นเคยกับการพัฒนา X++ และฟังก์ชันของแผ่นเวลาโครงการ

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>สัญญาข้อมูล – คลาส TSTimesheetCustomField X++

คลาส **TSTimesheetCustomField** เป็นคลาสของสัญญาข้อมูล X++ ซึ่งแสดงข้อมูลเกี่ยวกับฟิลด์ที่กำหนดเองสำหรับฟังก์ชันของแผ่นเวลา รายการของออบเจ็กต์ของฟิลด์ที่กำหนดเองจะถูกส่งผ่านไปยังทั้งสัญญาข้อมูล TSTimesheetDetails และสัญญาข้อมูล TSTimesheetEntry เพื่อแสดงฟิลด์ที่กำหนดเองในแอปบนมือถือ

- **TSTimesheetDetails** - สัญญาส่วนหัวของแผ่นเวลา
- **TSTimesheetEntry** - สัญญาของธุรกรรมแผ่นเวลา กลุ่มของออบเจ็กต์เหล่านี้ที่มีข้อมูลโครงการเดียวกัน และค่า **timesheetLineRecId** ประกอบด้วยหนึ่งรายการ

### <a name="fieldbasetype-types"></a>fieldBaseType (ชนิด)

คุณสมบัติ **FieldBaseType** บนออบเจ็กต์ **TsTimesheetCustom** กำหนดชนิดของฟิลด์ที่จะปรากฏขึ้นในแอป ค่า **ชนิด** ต่อไปนี้ที่ได้รับการสนับสนุน

| มูลค่าชนิด | ชนิดข้อมูล              | บันทึกย่อ |
|-------------|-------------------|-------|
| 0           | สตริง (และ Enum) | ฟิลด์นี้จะปรากฏเป็นฟิลด์ข้อความ |
| 1           | จำนวนเต็ม           | ค่าจะแสดงเป็นตัวเลขโดยไม่มีตำแหน่งทศนิยม |
| 2           | จำนวนจริง              | ค่าจะแสดงเป็นตัวเลขที่มีตำแหน่งทศนิยม<p>ถ้าต้องการแสดงมูลค่าจริงเป็นสกุลเงินในแอป ให้ใช้คุณสมบัติ **fieldExtenededType** คุณสามารถใช้คุณสมบัติ **numberOfDecimals** เพื่อตั้งค่าจำนวนของตำแหน่งทศนิยมที่จะแสดง</p> |
| 3           | วัน เดือน              | รูปแบบวันที่ถูกกำหนดโดยการตั้งค่า **วันที่ เวลา และรูปแบบหมายเลข** ของผู้ใช้ ซึ่งระบุไว้ภายใต้ **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค** ใน **ตัวเลือกผู้ใช้** |
| 4           | บูลีน           | |
| วันที่ 15 ก.ย.          | GUID              | |
| 16          | Int64             | |

- ถ้าไม่มีคุณสมบัติ **stringOptions** บนออบเจ็กต์ **TSTimesheetCustomField** จะให้ฟิลด์ข้อความอิสระกับผู้ใช้

    คุณสมบัติ **stringLength** สามารถใช้ในการตั้งค่าความยาวของสตริงสูงสุดที่ผู้ใช้สามารถป้อนได้

- ถ้าให้คุณสมบัติ **stringOptions** บนออบเจ็กต์ **TSTimesheetCustomField** องค์ประกอบรายการเหล่านั้นเป็นค่าเฉพาะที่ผู้ใช้สามารถเลือกได้โดยใช้ปุ่มตัวเลือก (ปุ่ม radio)

    ในกรณีนี้ ฟิลด์สตริงสามารถทำหน้าที่เป็นค่า enum สำหรับวัตถุประสงค์ของรายการผู้ใช้ เมื่อต้องการบันทึกค่าลงในฐานข้อมูลเป็น enum ให้แม็ปค่าสตริงกลับไปยังค่า enum ด้วยตนเอง ก่อนที่คุณจะบันทึกลงในฐานข้อมูลโดยใช้ห่วงโซ่ของคำสั่ง (โปรดดูที่ส่วน "ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปยังฐานข้อมูล" ในหัวข้อนี้สำหรับตัวอย่าง)

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

คุณสามารถใช้คุณสมบัตินี้ในการจัดรูปแบบค่าจริงเป็นสกุลเงิน วิธีการนี้สามารถใช้ได้เฉพาะเมื่อค่า **fieldBaseType** เป็น **จริง**

- **TSCustomFieldExtendedType:ไม่มี** – ไม่มีการนำการจัดรูปแบบไปใช้
- **TSCustomFieldExtendedType::สกุลเงิน** – จัดรูปแบบค่าเป็นสกุลเงิน

    เมื่อการจัดรูปแบบสกุลเงินเปิดใช้งานอยู่ ฟิลด์ **stringValue** จะสามารถใช้ส่งรหัสสกุลเงินที่ควรจะแสดงในแอป ค่าเป็นค่าแบบอ่านอย่างเดียว

    ฟิลด์ **realValue** มีจำนวนเงินที่ควรจะถูกบันทึกไปยังฐานข้อมูล

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

คุณสามารถใช้คุณสมบัตินี้เพื่อระบุตำแหน่งฟิลด์ที่กำหนดเองจะปรากฏในแอป

- **TSCustomFieldSection::ส่วนหัว** – ฟิลด์จะปรากฏในส่วน **ดูรายละเอียดเพิ่มเติม** ในแอป ฟิลด์เหล่านี้เป็นแบบอ่านอย่างเดียวเสมอ
- **TSCustomFieldSection::รายการ** – ฟิลด์จะปรากฏขึ้นหลังจากฟิลด์รายการแบบสำเร็จรูปทั้งหมดในรายการแผ่นเวลา ฟิลด์เหล่านี้สามารถแก้ไขได้ หรือเป็นแบบอ่านอย่างเดียว อย่างใดอย่างหนึ่ง

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

คุณสมบัตินี้จะระบุฟิลด์ เมื่อค่าที่แอปให้ถูกบันทึกกลับไปยังฐานข้อมูล

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

คุณสมบัตินี้จะระบุฟิลด์ เมื่อค่าที่แอปให้ถูกบันทึกกลับไปยังฐานข้อมูล

### <a name="iseditable-noyes"></a>isEditable (NoYes)

ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าฟิลด์ในส่วนรายการแผ่นเวลาควรจะสามารถแก้ไขได้โดยผู้ใช้ ตั้งค่าคุณสมบัติเป็น **ไม่** เพื่อทำให้ฟิลด์นี้เป็นแบบอ่านอย่างเดียว

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าฟิลด์ในส่วนรายการแผ่นเวลาควรจะเป็นแบบบังคับ

### <a name="label-str"></a>ป้ายชื่อ (str)

คุณสมบัตินี้จะระบุป้ายชื่อที่แสดงถัดจากฟิลด์ในแอป

### <a name="stringoptions-list-of-strings"></a>stringOptions (รายการของสตริง)

คุณสมบัตินี้สามารถใช้ได้เฉพาะเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **สตริง** ถ้ามีการตั้งค่า **stringOptions** ค่าสตริงที่พร้อมใช้งานสำหรับการเลือกผ่านปุ่มตัวเลือก (ปุ่ม radio) จะถูกระบุโดยสตริงในรายการ ถ้าไม่มีการระบุสตริง การให้ป้อนข้อความอิสระในฟิลด์สตริงจะได้รับอนุญาต (โปรดดูที่ส่วน "ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปยังฐานข้อมูล" ในหัวข้อนี้สำหรับตัวอย่าง)

### <a name="stringlength-int"></a>stringLength (int)

คุณสมบัตินี้ระบุความยาวสูงสุดสำหรับฟิลด์สตริง สามารถใช้ได้เฉพาะเมื่อ **fieldBaseTyp** ถูกตั้งค่าเป็น **สตริง**

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

คุณสมบัตินี้จะระบุจำนวนของตำแหน่งทศนิยมที่แสดงสำหรับฟิลด์จริง สามารถใช้ได้เฉพาะเมื่อ **fieldBaseTyp** ถูกตั้งค่าเป็น **จำนวนจริง**

### <a name="ordersequence-int"></a>orderSequence (int)

คุณสมบัตินี้ควบคุมใบสั่งที่จะแสดงฟิลด์ที่กำหนดเองในแอป เมื่อมีการระบุฟิลด์ที่กำหนดเองมากกว่าหนึ่งฟิลด์ ฟิลด์ที่มีตัวเลขที่ต่ำกว่าจะแสดงขึ้นก่อน

### <a name="booleanvalue-boolean"></a>booleanValue (บูลีน)

สำหรับฟิลด์ของชนิด **บูลีน** คุณสมบัตินี้จะส่งค่าบูลีนของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="guidvalue-guid"></a>guidValue (guid)

สำหรับฟิลด์ของชนิด **GUID** คุณสมบัตินี้จะส่งค่า Global Unique Identifier (GUID) ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="int64value-int64"></a>int64Value (int64)

สำหรับฟิลด์ของชนิด **Int64** คุณสมบัตินี้จะส่งค่า Int64 ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="intvalue-int"></a>intValue (int)

สำหรับฟิลด์ของชนิด **Int** คุณสมบัตินี้จะส่งค่า Int ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="realvalue-real"></a>realValue (real)

สำหรับฟิลด์ของชนิด **จำนวนจริง** คุณสมบัตินี้จะส่งค่าจำนวนจริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="stringvalue-str"></a>stringValue (str)

สำหรับฟิลด์ของชนิด **สตริง** คุณสมบัตินี้จะส่งค่าสตริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป นอกจากนี้ ยังใช้สำหรับฟิลด์ของชนิด **จำนวนจริง** ที่มีการจัดรูปแบบเป็นสกุลเงินด้วย สำหรับฟิลด์เหล่านั้น คุณสมบัตินี้จะถูกใช้ในการส่งรหัสสกุลเงินไปยังแอป

### <a name="datevalue-date"></a>dateValue (วันที่)

สำหรับฟิลด์ของชนิด **วันที่** คุณสมบัตินี้จะส่งค่าวันที่ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>แสดงและบันทึกฟิลด์ที่กำหนดเองในส่วนของส่วนรายการแผ่นเวลา

ด้านล่างเป็นภาพหน้าจอจากแอปบนมือถือของการสร้างรายการแผ่นเวลา ซึ่งแสดงฟิลด์สำเร็จรูปและฟิลด์ที่กำหนดเองในส่วน "รายการเวลา" ที่เรียกว่า "สตริงการทดสอบ" ด้วยค่า enum ของ "ตัวเลือกที่สอง" ที่กำหนดไว้แล้ว

![ทดสอบฟิลด์ที่กำหนดเองของสตริงในแอป](media/timesheet-entry.jpg)



ด้านล่างเป็นภาพหน้าจอจากแอปบนมือถือของผู้ใช้ที่เลือกหนึ่งในตัวเลือก enum ที่พร้อมใช้งานสำหรับฟิลด์แบบกำหนดเองของ "สตริงการทดสอบ"  ตัวเลือกสองรายการคือ "ตัวเลือกแรก" และ "ตัวเลือกที่สอง" ซึ่งแสดงเป็นปุ่ม radio มีการเลือกตัวเลือกที่สองอยู่ในขณะนี้

![ปุ่มตัวเลือก (ปุ่ม radio) สำหรับฟิลด์ที่กำหนดเองของสตริงการทดสอบ](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>ขยายตาราง TSTimesheetLine เพื่อให้มีฟิลด์ที่กำหนดเอง

ในสถานการณ์ปกติ อาจเป็นไปได้ว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนของการป้อนข้อมูลแผ่นเวลาจะถูกบันทึกไปยังตาราง TSTimesheetLine อย่างไรก็ตาม คุณสามารถใช้ตารางอื่นๆ ได้ ถ้าสามารถดึงข้อมูลได้โดยขึ้นอยู่กับเรกคอร์ด TSTimesheetTrans ที่ระบุ หรือถ้าไม่มีบริบทของเรกคอร์ดเฉพาะ (ตัวอย่างเช่น ถ้ามีการตั้งค่าฟิลด์เป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)

โปรดสังเกตว่าฟิลด์ที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรองใดๆ สามารถสร้างขึ้นโดยยึดตามตรรกะ X++ แบบไดนามิก วิธีการนี้อาจเป็นประโยชน์ในสถานการณ์แบบอ่านอย่างเดียว (โปรดดูที่ส่วน "ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetDetails วิธีการ buildCustomFieldListForHeader ในการกรอกข้อมูลในรายละเอียดแผ่นเวลา" สำหรับตัวอย่างของค่าฟิลด์แบบกำหนดเองที่สร้างขึ้นแบบไดนามิก)

ด้านล่างเป็นภาพหน้าจอจาก Visual Studio ของ Application Object Tree ซึ่งแสดงส่วนขยายของตาราง TSTimesheetLine ที่มีฟิลด์ TestLineString ที่เพิ่มเป็นฟิลด์ที่กำหนดเอง

![สตริงรายการ](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนของการป้อนข้อมูลแผ่นเวลา

รหัสนี้จะควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป ตัวอย่างเช่น จะควบคุมชนิดของฟิลด์ ป้ายชื่อ ไม่ว่าฟิลด์เป็นฟิลด์บังคับหรือไม่ และส่วนใดของฟิลด์ที่จะปรากฏด้านใน

ตัวอย่างต่อไปนี้แสดงฟิลด์สตริงบนรายการเวลา ฟิลด์นี้มีสองตัวเลือก **ตัวเลือกแรก** และ **ตัวเลือกที่สอง** ซึ่งพร้อมใช้งานผ่านปุ่มตัวเลือก (ปุ่ม radio) ฟิลด์ในแอปเชื่อมโยงกับฟิลด์ **TestLineString** ซึ่งถูกเพิ่มลงในตาราง TSTimesheetLine

หมายเหตุ การใช้ของวิธีการ **TSTimesheetCustomField::newFromMetatdata()** เพื่อทำให้การเริ่มต้นคุณสมบัติฟิลด์แบบกำหนดเองเป็นไปได้ง่ายขึ้น: **fieldBaseType** **tableName** **fieldname** **label** **isEditable** **isMandatory** **stringLength** และ **numberOfDecimals** นอกจากนี้ คุณยังสามารถตั้งค่าพารามิเตอร์เหล่านี้ด้วยตนเองได้ตามที่คุณต้องการ

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldListForEntry ของคลาส TSTimesheetEntry เพื่อป้อนค่าในการป้อนข้อมูลแผ่นเวลา

วิธีการ **buildCustomFieldListForEntry** ถูกใช้ในการป้อนค่าในรายการแผ่นเวลาที่บันทึกไว้ในแอปบนมือถือ ใช้เรกคอร์ด TSTimesheetTrans เป็นพารามิเตอร์ สามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>ใช้ห่วงโซ่ของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปยังฐานข้อมูล

เมื่อต้องการบันทึกฟิลด์ที่กำหนดเองกลับไปยังฐานข้อมูลที่ใช้งานโดยทั่วไป คุณต้องขยายวิธีหลายวิธีดังนี้:

- วิธีการ **timesheetLineNeedsUpdating** ถูกใช้ในการกำหนดว่ามีการเปลี่ยนแปลงเรกคอร์ดรายการโดยผู้ใช้ในแอป และต้องถูกบันทึกไปยังฐานข้อมูลหรือไม่ ถ้าประสิทธิภาพไม่เกี่ยวข้อง วิธีการนี้สามารถถูกทำให้ได้ง่ายขึ้นได้เพื่อให้ส่งคืน **จริง** เสมอ
- วิธีการ **populateTimesheetLineFromEntryDuringCreate** และ **populateTimesheetLineFromEntryDuringUpdate** สามารถขยายเพื่อให้ป้อนค่าในเรกคอร์ดฐานข้อมูล TSTimesheetLine จากเรกคอร์ดสัญญาข้อมูล TSTimesheetEntry ที่ให้ ในตัวอย่างต่อไปนี้ โปรดสังเกตวิธีการที่การแม็ประหว่างฟิลด์ฐานข้อมูลและฟิลด์รายการถูกดำเนินการด้วยตนเองโดยใช้รหัส X++
- นอกจากนี้ ยังสามารถขยายวิธีการ **populateTimesheetWeekFromEntry** ได้ ถ้าฟิลด์แบบกำหนดเองที่ถูกแม็ปไปยังออบเจ็กต์ **TSTimesheetEntry** ต้องเขียนกลับไปยังตารางฐานข้อมูล TSTimesheetLineweek

> [!NOTE]
> ตัวอย่างต่อไปนี้จะบันทึกค่า **firstOption** หรือ **secondOption** ที่ผู้ใช้เลือกไปยังฐานข้อมูลเป็นค่าสตริงดิบ ถ้าฟิลด์ฐานข้อมูลเป็นฟิลด์ของชนิด **Enum** ค่าเหล่านั้นอาจถูกแม็ปด้วยตนเองไปยังค่า Enum แล้วถูกบันทึกไปยังฟิลด์ Enum บนตารางฐานข้อมูล

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>แสดงฟิลด์ที่กำหนดเองในส่วนของส่วนหัวรายการแผ่นเวลา

ด้านล่างเป็นภาพหน้าจอจากแอปมือถือของผู้ใช้ที่ดูแผ่นเวลา มีการเลือกปุ่ม "ข้อมูลเพิ่มเติม" ในมุมขวาด้านบนเพื่อแสดงตัวเลือก "ดูรายละเอียดเพิ่มเติม"  

![ดูคำสั่งในรายละเอียดเพิ่มเติม](media/show-more.png)

ด้านล่างเป็นภาพหน้าจอจากแอปมือถือที่แสดงส่วน "เพิ่มเติม" ของแผ่นเวลา ฟิลด์แบบกำหนดเองที่เรียกว่า "อัตราการใช้ประโยชน์ของแผ่นเวลานี้ (ฟิลด์แบบกำหนดเองที่คำนวณได้)" ถูกเพิ่มลงในส่วนของส่วนหัวของแผ่นเวลา มีการตั้งค่าแบบอ่านอย่างเดียวของ "0.667" บนฟิลด์ที่กำหนดเอง

![ส่วนเพิ่มเติม](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>ขยายตาราง TSTimesheetTable เพื่อให้มีฟิลด์ที่กำหนดเอง

ในสถานการณ์ปกติ อาจเป็นไปได้ว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนของส่วนหัวจะถูกดึงข้อมูลจากตาราง TSTimesheetHeader อย่างไรก็ตาม คุณสามารถใช้ตารางอื่นๆ ได้ ถ้าสามารถดึงข้อมูลได้โดยขึ้นอยู่กับเรกคอร์ด TSTimesheetTable ที่ระบุ หรือถ้าไม่มีบริบทของเรกคอร์ดเฉพาะ (ตัวอย่างเช่น ถ้ามีการตั้งค่าฟิลด์เป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)

โปรดสังเกตว่าฟิลด์ที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรองใดๆ สามารถสร้างขึ้นโดยยึดตามตรรกะ X++ แบบไดนามิก ตัวอย่างต่อจากนี้จะแสดงวิธีการนี้

ฟิลด์ในส่วนในส่วนหัวจะเป็นแบบอ่านอย่างเดียวในแอปเสมอ

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนของส่วนหัว

รหัสนี้จะควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป ตัวอย่างเช่น จะควบคุมชนิดของฟิลด์ ป้ายชื่อ ไม่ว่าฟิลด์เป็นฟิลด์บังคับหรือไม่ และส่วนใดของฟิลด์ที่จะปรากฏด้านใน

ตัวอย่างต่อไปนี้จะแสดงค่าที่คำนวณได้ในส่วนของส่วนหัวในแอป

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>ใช้ห่วงโซ่ของคำสั่งในวิธีการ buildCustomFieldListForHeader ของคลาส TSTimesheetDetails เพื่อกรอกข้อมูลในรายละเอียดแผ่นเวลา

วิธีการ **buildCustomFieldListForHeader** ถูกใช้ในการกรอกข้อมูลรายละเอียดส่วนหัวของแผ่นเวลาในแอปบนมือถือ ซึ่งใช้เรกคอร์ด TSTimesheetTable เป็นพารามิเตอร์ สามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป ตัวอย่างต่อไปนี้ไม่ได้อ่านค่าใดๆ จากฐานข้อมูล แต่จะใช้ตรรกะ X++ เพื่อสร้างค่าที่มีการคำนวณซึ่งจะแสดงในแอปแทน


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>โอกาสของความสามารถในการตั้งค่าคอนฟิก/ความสามารถในการขยายอื่นๆ

### <a name="adding-additional-validation-for-the-app"></a>การเพิ่มการตรวจสอบความถูกต้องเพิ่มเติมสำหรับแอป

ตรรกะที่มีอยู่สำหรับฟังก์ชันแผ่นเวลาที่ระดับฐานข้อมูลจะยังคงทำงานตามที่คาดไว้ เมื่อต้องการขัดจังหวะความสมบูรณ์ของการบันทึกหรือส่งการดำเนินงาน และแสดงข้อความแสดงข้อผิดพลาดที่ระบุ คุณสามารถเพิ่ม **ส่งข้อผิดพลาด ("ส่งข้อความไปยังผู้ใช้")** ไปยังรหัสผ่านห่วงโซ่ของส่วนขยายคำสั่ง ต่อไปนี้เป็นตัวอย่างสามรายการของวิธีการที่สามารถขยายได้ซึ่งมีประโยชน์:

- ถ้า **validateWrite** บนตาราง TSTimesheetLine ส่งคืน **เท็จ** ระหว่างการดำเนินงานบันทึกสำหรับรายการแผ่นเวลา ข้อความแสดงข้อผิดพลาดจะถูกแสดงในแอปบนมือถือ
- ถ้า **validateSubmit** บนตาราง TSTimesheetTable ส่งคืน **เท็จ** ระหว่างการส่งแผ่นเวลาในแอป ข้อความแสดงข้อผิดพลาดจะถูกแสดงไปยังผู้ใช้
- ตรรกะที่กรอกข้อมูลในฟิลด์ (ตัวอย่างเช่น **คุณสมบัติของรายการ**) ในระหว่างวิธีการ **แทรก** บนตาราง TSTimesheetLine จะยังคงรันอยู่

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>การซ่อนและการทำเครื่องหมายฟิลด์สำเร็จรูปเป็นแบบอ่านอย่างเดียวผ่านทางการตั้งค่าคอนฟิก

จากพารามิเตอร์โครงการ คุณสามารถทำให้ฟิลด์สำเร็จรูปเป็นแบบอ่านอย่างเดียว หรือถูกซ่อนอยู่ในแอปบนมือถือ ตั้งค่าตัวเลือกในส่วน **แผ่นเวลาสำหรับมือถือ** บนแท็บ **แผ่นเวลา** ของหน้า **พารามิเตอร์การจัดการและการบัญชีโครงการ**

![พารามิเตอร์โครงการ](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>การเปลี่ยนกิจกรรมที่พร้อมใช้งานสำหรับการเลือกผ่านส่วนขยาย

กิจกรรมที่พร้อมใช้งานสำหรับการเลือกสำหรับโครงการจะถูกกรอกข้อมูลโดยผ่านวิธีการ **getActivitiesForProject()** และ **getActivityQuery()** ในคลาส **TsTimesheetProjectService** คุณสามารถใช้ห่วงโซ่ของคำสั่งเพื่อเปลี่ยนลักษณะการทำงานนี้ให้ตรงกับสถานการณ์จำลองทางธุรกิจของคุณ สำหรับกิจกรรมที่พร้อมใช้งานสำหรับการเลือกสำหรับโครงการที่ระบุ

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>การป้อนประเภทโครงการเริ่มต้นในรายการแผ่นเวลา

รายการของประเภทโครงการเริ่มต้นในรายการแผ่นเวลาจะเกิดขึ้นในสามระดับ คุณสามารถใช้ห่วงโซ่ของคำสั่งเพื่อขยายลักษณะการทำงานที่ระดับใดๆ เหล่านี้หรือทั้งหมด เพื่อให้เกิดลักษณะการทำงานที่ต้องการ มีการใช้ลำดับชั้นต่อไปนี้:

1. แอปพยายามที่จะใส่ประเภทเริ่มต้นจากทรัพยากรโครงการ ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธีการ **getCurrentUserResource** และ **getDelegatedResourcesForCurrentUser** ในคลาส **TSTimesheetSettingsService**
2. ถ้าไม่ได้ระบุประเภทเริ่มต้นที่ระดับทรัพยากรโครงการ แอปจะพยายามดึงข้อมูลจากกิจกรรมโครงการ ประเภทเริ่มต้นนี้ถูกตั้งค่าวิธีการ **getActivitiesForProject** ในคลาส **TSTimesheetProjectService**
3. ถ้าไม่ได้ระบุประเภทเริ่มต้นที่ระดับกิจกรรมโครงการ ประเภทเริ่มต้นจะมาจากพารามิเตอร์โครงการ ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธีการ **getProjectDetailsbyRule** ในคลาส **TSTimesheetProjectService**
