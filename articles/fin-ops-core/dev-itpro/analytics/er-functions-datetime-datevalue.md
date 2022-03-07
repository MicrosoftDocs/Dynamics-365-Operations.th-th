---
title: ฟังก์ชัน ER DATEVALUE
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATEVALUE
author: NickSelin
ms.date: 09/08/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446f1357e54342073e73f86ef36e6467e029ebc4
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485585"
---
# <a name="datevalue-er-function"></a>ฟังก์ชัน ER DATEVALUE

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `DATEVALUE` ส่งกลับค่า *[วันที่](er-formula-supported-data-types-primitive.md#date)* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและใน [วัฒนธรรม](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือกไปยังค่าวันที่ สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](/dotnet/standard/base-types/standard-date-and-time-format-strings) และ [กำหนดเอง](/dotnet/standard/base-types/custom-date-and-time-format-strings)

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *[สตริง](er-formula-supported-data-types-primitive.md#string)*

ข้อความที่แสดงถึงค่าไปยังรูปแบบ

`format`: *สตริง*

รูปแบบของข้อความที่ให้ สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](/dotnet/standard/base-types/standard-date-and-time-format-strings) และ [กำหนดเอง](/dotnet/standard/base-types/custom-date-and-time-format-strings)

`culture`: *สตริง*

วัฒนธรรมที่ใช้สำหรับการจัดรูปแบบของข้อความที่กำหนด สำหรับข้อมูลเกี่ยวกับวัฒนธรรมที่ได้รับการสนับสนุน โปรดดูที่ [วัฒนธรรม](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)

## <a name="return-values"></a>ค่าที่ส่งคืน

*วัน เดือน*

ค่าวันที่ที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

เมื่อวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก ตัวอย่างเช่น ถ้าฟังก์ชัน `DATEVALUE` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน ค่า `culture` เริ่มต้นคือ **EN-US**

## <a name="example-1"></a>ตัวอย่างที่ 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` ส่งกลับค่าวันที่ **21 ธันวาคม 2016** ขึ้นอยู่กับรูปแบบที่กำหนดเองที่ระบุและวัฒนธรรม **EN-US** ของแอปพลิเคชันเริ่มต้น

## <a name="example-2"></a>ตัวอย่างที่ 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` ส่งกลับค่า **วันที่ 21 มกราคม 2016** ตามรูปแบบและวัฒนธรรมที่กำหนดเองที่ระบุ

อย่างไรก็ตาม `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` จะส่งข้อยกเว้นเพื่อแจ้งผู้ใช้ว่าไม่รับรู้สตริงที่ระบุว่าเป็นค่าวันที่สำหรับวัฒนธรรมที่ระบุที่ถูกต้อง

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
