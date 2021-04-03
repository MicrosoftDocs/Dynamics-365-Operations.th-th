---
title: ฟังก์ชั่น DATETIMEFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DATETIMEFORMAT
author: NickSelin
manager: kfend
ms.date: 01/04/2021
ms.topic: article
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
ms.openlocfilehash: b7516620763e87440c0fb866ce507c744223a229
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563641"
---
# <a name="datetimeformat-er-function"></a>ฟังก์ชั่น DATETIMEFORMAT ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `DATETIMEFORMAT` ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่/เวลาที่ให้เป็นข้อความในรูปแบบที่ระบุและใน [Culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`datetime`: *DateTime*

ค่าวันที่/เวลาที่แสดงถึงวันที่และเวลาในการจัดรูปแบบ

`format`: *สตริง*

รูปแบบของสตริงเอาต์พุต

> [!NOTE]
> สตริงรูปแบบจะคำนึงถึงตัวพิมพ์ เมื่อคุณใช้รูปแบบมาตรฐานหรือรูปแบบที่กำหนดเอง ตัวอย่างเช่น ตัวระบุรูปแบบ "d" [มาตรฐาน](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) จะส่งคืนวันที่โดยใช้รูปแบบวันที่แบบย่อ ในขณะที่ตัวระบุรูปแบบ "D" มาตรฐาน จะส่งคืนวันที่โดยใช้รูปแบบวันที่ที่ยาว นอกจากนี้ ตัวระบุรูปแบบ "M" [แบบกำหนดเอง](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) จะส่งคืนเดือน ตั้งแต่ 1 ถึง 12 ในขณะที่ตัวระบุรูปแบบ "m" แบบกำหนดเอง จะส่งคืนนาที ตั้งแต่ 0 ถึง 59

`culture`: *สตริง*

วัฒนธรรมที่จะใช้สำหรับการจัดรูปแบบ

## <a name="return-values"></a>ค่าที่ส่งคืน

*สตริง*

ค่าสตริงที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

หากวัฒนธรรมไม่ได้กำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก ค่าของ `culture` จะถูกกำหนดโดยบริบทการเรียก ตัวอย่างเช่น ถ้าฟังก์ชัน `DATETIMEFORMAT` ถูกเรียกโดยใช้ไวยากรณ์ 1 ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับส่วนประกอบ **FILE** ที่ถูกกำหนดค่าให้ใช้วัฒนธรรมเยอรมัน การแปลงจะทำโดยใช้วัฒนธรรมเยอรมัน ค่า `culture` เริ่มต้นคือ **EN-US**

เมื่อฟังก์ชัน `DATETIMEFORMAT` แปลงค่าวันที่/เวลาที่กำหนด จะพิจารณาการตั้งค่าโซนเวลาของผู้ใช้แอพลิเคชันที่กำลังเรียกใช้รูปแบบ ER ที่ฟังก์ชันถูกเรียกในบริบท

## <a name="example-1"></a>ตัวอย่างที่ 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้

## <a name="example-2"></a>ตัวอย่างที่ 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ

## <a name="example-3"></a>ตัวอย่างที่ 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` ส่งกลับค่าสตริง **2019-11-12T08:00:00.0000000-08:00** เมื่อฟังก์ชันถูกเรียกในระหว่างกระบวนการที่เริ่มต้นโดยผู้ใช้แอปพลิเคชันที่มีเวลาค่โซนเวลา **(GMT-08:00) เวลาแปซิฟิก (สหรัฐอเมริกา & แคนาดา)** ในส่วน **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]