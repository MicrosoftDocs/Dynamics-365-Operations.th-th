---
title: รายการของฟังก์ชั่น ER ในประเภทการแปลงข้อมูล
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการแปลงที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686086"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>รายการของฟังก์ชั่น ER ในประเภทการแปลงข้อมูล

[!include [banner](../includes/banner.md)]

ฟังก์ชันการแปลงชนิดของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อแปลงค่าระหว่างชนิด หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="type-conversion-functions"></a>ฟังก์ชันการแปลงของชนิด

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | ฟังก์ชันนี้ส่งกลับค่า *Int64* ที่แสดงถึงสตริงที่ระบุ |
| [IntValue](er-functions-conversion-intvalue.md)       | ฟังก์ชันนี้ส่งกลับค่า *Int* ที่แสดงถึงสตริงที่ระบุ |
| [NumberValue](er-functions-conversion-numbervalue.md) | ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่ถูกแปลงจากค่า *สตริง* ที่ระบุ ในระหว่างการแปลงจะมีการพิจารณาตัวแบ่งการจัดกลุ่มทศนิยมและเลขฐานที่ระบุ |
| [มูลค่า](er-functions-conversion-value.md)             | ฟังก์ชันนี้ส่งกลับค่า *จำนวนจริง* ที่ถูกแปลงจากค่า *สตริง* ที่ระบุ |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>ฟังก์ชันการแปลงชนิดในประเภทวันที่และเวลา

ตารางต่อไปนี้อธิบายฟังก์ชันการแปลงชนิดใน [ประเภทวันที่และเวลา](er-functions-category-datetime.md)

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่แปลงจากค่า *สตริง* ที่ให้ในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือกเป็นค่าวันที่/เวลา |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่า *วันที่* ที่กำหนดให้เป็นค่าวันที่/เวลาในเวลาสากล (เวลามาตรฐานกรีนิช \[GMT\]) |
| [DateValue](er-functions-datetime-datevalue.md)           | ฟังก์ชันนี้ส่งกลับค่า *Date* ที่แปลงจากค่า *สตริง* ที่ให้ในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือกเป็นค่าวันที่/เวลา |

## <a name="type-conversion-functions-in-the-list-category"></a>ฟังก์ชั่นการสนทนาของชนิดในประเภทการ

ตารางต่อไปนี้อธิบายฟังก์ชันการแปลงชนิดใน [รายการประเภท](er-functions-category-list.md)

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [รายการ](er-functions-list-list.md)                 | ฟังก์ชันนี้ส่งกลับค่า *รายการเรกคอร์ด* เป็นรายการใหม่ที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด *คอนเทนเนอร์ (เรกคอร์ด)* |
| [ListOfFields](er-functions-list-listoffields.md) | ฟังก์ชันนี้ส่งกลับค่า *รายการเรกคอร์ด* ที่สร้างขึ้นตามโครงสร้างของอาร์กิวเมนต์ที่ให้ชนิดของ *การแจงนับ* หรือ *คอนเทนเนอร์ (เรกคอร์ด)* |
| [การแบ่ง](er-functions-list-split.md)               | ฟังก์ชันนี้แบ่งค่า *สตริง* ที่ระบุลงในสตริงย่อยและส่งกลับผลลัพธ์เป็นค่า *ค่ารายการเรกคอร์ด* ใหม่ |
| [StringJoin](er-functions-list-stringjoin.md)     | ฟังก์ชันนี้ส่งคืนค่า *สตริง* ที่ประกอบด้วยค่าที่ต่อกันของฟิลด์ที่ระบุจากค่า *รายการเรกคอร์ด* ที่ระบุ ค่าสามารถถูกแบ่งด้วยตัวคั่นที่ระบุ |

## <a name="type-conversion-functions-in-the-text-category"></a>ฟังก์ชั่นการสนทนาของชนิดในประเภทข้อความ

ตารางต่อไปนี้อธิบายฟังก์ชันการแปลงชนิดใน [ประเภทข้อความ](er-functions-category-text.md)

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงอักขระเดี่ยวที่ถูกอ้างอิงโดยหมายเลข Unicode ที่ระบุ |
| [GuidValue](er-functions-text-guidvalue.md)       | ฟังก์ชันนี้แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *GUID* |
| [NumberFormat](er-functions-text-numberformat.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงถึงหมายเลขที่ระบุในรูปแบบที่ระบุและในวัฒนธรรมที่ระบุเป็นทางเลือก |
| [QrCode](er-functions-text-qrcode.md)             | ฟังก์ชันนี้ส่งกลับค่า *คอนเทนเนอร์* ที่แสดงรูป Quick Response code (QR code) สำหรับสตริงที่ระบุในรูปแบบไบนารี |
| [ข้อความ](er-functions-text-text.md)                 | ฟังก์ชันนี้ส่งคืนตัวเลขที่ระบุเป็นค่า *สตริง* ที่แสดงถึงตัวเลขที่ระบุ หลังจากที่ได้ถูกแปลงเป็นข้อความแบบสตริงที่ถูกจัดรูปแบบตามการตั้งค่าตำแหน่งที่ตั้งของเซิร์ฟเวอร์ของอินสแตนซ์ของแอปพลิเคชันปัจจุบัน |

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)
