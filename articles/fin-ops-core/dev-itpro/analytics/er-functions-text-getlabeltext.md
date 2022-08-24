---
title: ฟังก์ชัน GETLABELTEXT ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GETLABELTEXT (ER)
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285953"
---
# <a name="getlabeltext-er-function"></a>ฟังก์ชัน GETLABELTEXT ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `GETLABELTEXT` จะค้นหาป้ายชื่อเฉพาะเพื่อส่งคืนค่า *[สตริง](er-formula-supported-data-types-primitive.md#string)* ที่แสดงถึงคำแปลของป้ายชื่อที่ระบุในภาษาที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>อาร์กิวเมนต์

### <a name="label-id"></a>รหัสป้ายชื่อ

`label id`: *สตริง* หรือ *รหัสป้ายชื่อ*

รหัสที่ถูกต้องของชนิดป้ายชื่อชนิดใดชนิดหนึ่งต่อไปนี้:

- ป้ายชื่อ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)
- ป้ายชื่อ Microsoft Dynamics 365 Finance

#### <a name="usage-notes"></a>บันทึกย่อการใช้งาน

อาร์กิวเมนต์นี้สามารถกําหนดเป็นค่าคงที่เท่านั้น โดยใช้รูปแบบที่รองรับรูปแบบใดรูปแบบหนึ่งต่อไปนี้

- สำหรับป้ายชื่อ ER:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- สำหรับป้ายชื่อการเงิน:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> เมื่อออกแบบ จะมีข้อความแสดงข้อผิดพลาดเกี่ยวกับการตรวจสอบความถูกต้องแสดงบนหน้า **[ตัวออกแบบสูตร](er-advanced-formula-editor.md)** ถ้าไม่พบป้ายชื่อโดยใช้รหัสป้ายชื่อที่ระบุ

### <a name="language"></a>ภาษา

`language`: *สตริง*

สตริงที่แสดงถึงรหัสภาษา

#### <a name="usage-notes"></a>บันทึกย่อการใช้งาน

อาร์กิวเมนต์นี้สามารถกําหนดเป็นค่าคงที่ข้อความหรือเป็นพาธของฟิลด์แหล่งข้อมูลที่ส่งคืนค่า *สตริง*

> [!NOTE]
> เมื่อออกแบบ จะมีข้อความแสดงข้อผิดพลาดเกี่ยวกับการตรวจสอบความถูกต้องแสดงขึ้นหากไม่พบรหัสภาษาที่ใช้อาร์กิวเมนต์ `language` ที่กําหนดไว้เมื่อมีการกําหนดเป็นค่าคงที่ข้อความ
>
> เมื่อรันไทม์ จะส่งคืนคำแปลจากภาษาของระบบ `EN-US` ให้กับป้ายชื่อที่ระบุ ถ้าไม่พบรหัสภาษาที่ใช้อาร์กิวเมนต์ `language` ที่ระบุ

## <a name="return-values"></a>ค่าที่ส่งคืน

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example-1-system-label"></a><a name=example-1></a>ตัวอย่างe 1: ป้ายชื่อของระบบ

นิพจน์ `GETLABELTEXT (@"SYS70894", "en-us")` และ `GETLABELTEXT ("SYS70894", "en-us")` ส่งคืนคำแปลภาษาอังกฤษ "Nothing to print" สำหรับป้ายชื่อแอปพลิเคชัน `@SYS70894`

## <a name="example-2-er-label"></a><a name=example-2></a>ตัวอย่าง 2: ป้ายชื่อ ER

คุณเริ่มต้นแก้ไข [การตั้งค่าคอนฟิก](general-electronic-reporting.md#Configuration) ER ที่ [ได้รับมา](er-quick-start2-customize-report.md#DeriveProvidedFormat) จากการตั้งค่าคอนฟิก **ISO20022 Credit transfer (DE)** ป้อนแหล่งข้อมูลใหม่ของชนิด *[ฟิลด์ที่คำนวณ](er-calculated-field-ds-performance.md)* และตั้งค่าคอนฟิกนิพจน์ `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` ให้กับแหล่งข้อมูลนี้ ในกรณีนี้ เมื่อรันไทม์ แหล่งข้อมูลจะส่งคืนคำแปลภาษาเยอรมัน "Kreditorenname" สำหรับป้ายชื่อ `@GER_LABEL:VendorName` ER ที่เดิมมีการตั้งค่าคอนฟิกในการตั้งค่าคอนฟิก ER ของ **ISO20022 Credit transfer (DE)** ฐาน

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)

[ออกแบบรายงานหลายภาษาในการรายงานทางอิเล็กทรอนิกส์](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
