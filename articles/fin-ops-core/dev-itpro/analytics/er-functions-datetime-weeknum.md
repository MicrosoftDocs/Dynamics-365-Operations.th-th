---
title: ฟังก์ชัน WEEKNUM ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) WEEKNUM
author: NickSelin
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 37e62b32896e2030b3322a89ac4acdd6c18d5e3c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982188"
---
# <a name="weeknum-er-function"></a>ฟังก์ชัน WEEKNUM ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `WEEKNUM` ส่งคืนค่า *[จำนวนเต็ม](er-formula-supported-data-types-primitive.md#integer)* ที่หมายถึงสัปดาห์ของปีที่มีค่า *[วันที่](er-formula-supported-data-types-primitive.md#date)* ที่ระบุ การคํานวณดังกล่าวจะขึ้นอยู่กับกฎตามวัฒนธรรมที่กําหนดสัปดาห์ในปฏิทินและวันแรกของสัปดาห์

## <a name="syntax"></a>ไวยากรณ์

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">อาร์กิวเมนต์</a>

`date`: *วันที่*

ค่าวันที่ที่แสดงถึงวันที่ที่จะใช้สำหรับการคำนวณจำนวนสัปดาห์ของปี

`culture`: *[สตริง](er-formula-supported-data-types-primitive.md#string)*

วัฒนธรรมที่จะใช้สำหรับการคำนวณ คุณสามารถใช้รหัสวัฒนธรรมที่ได้รับการสนับสนุนตาม [มาตรฐาน](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0) .NET

## <a name="return-values"></a>ค่าที่ส่งคืน

*เลขจำนวนเต็ม*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

สัปดาห์ของปีมีการคํานวณตามมาตรฐาน [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) ถ้ามาตรฐานนี้นํามาใช้โดยประเทศหรือภูมิภาคที่มีการกำหนดตำแหน่ทงี่ตั้งสำหรับขณะรันไทม์ ไม่เช่นนั้น การคํานวณจะเป็นไปตามมาตรฐานประจำชาติเฉพาะประเทศ/ภูมิภาค

หากมีการระบุรหัส [วัฒนธรรม](#arguments) ที่ไม่รองรับเป็นอาร์กิวเมนต์ของฟังก์ชัน `WEEKNUM` ขณะรันไทม์ จะเกิดข้อยกเว้นขึ้น ถ้ามีการระบุสตริงเปล่าเป็นรหัสวัฒนธรรม จะมีการใช้ปฏิทินภาษาอังกฤษที่เป็นกลางเพื่อคํานวณหมายเลขสัปดาห์

## <a name="examples"></a>ตัวอย่างเช่น

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` ส่งคืน **1**

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` ส่งคืน **53**

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` ส่งคืน **52**

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` ส่งคืน **21**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
