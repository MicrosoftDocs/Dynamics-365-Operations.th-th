---
title: รายการของฟังก์ชั่น ER ในประเภทวันที่และเวลา
description: บทความนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันวันที่และเวลาที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: d77f41e10d927a9aae06b9ba0fc58ca237c071cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291338"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>รายการของฟังก์ชั่น ER ในประเภทวันที่และเวลา

[!include [banner](../includes/banner.md)]

ฟังก์ชันวันและเวลาของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อดึงข้อมูลจากค่าวันที่และเวลาและเพื่อมาดำเนินการ บทความนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="list-of-supported-functions"></a>รายการฟังก์ชันที่ได้รับการสนับสนุน

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | ฟังก์ชันนี้ส่งคืนค่า *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* ที่เป็นจำนวนวันที่ระบุก่อนหรือหลังวันที่เริ่มต้นที่ระบุ |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่าวันที่/เวลาที่กำหนดในโซนเวลาใดๆ ให้เป็นค่าวันที่/เวลาในอีกโซนเวลา |
| [DateFormat](er-functions-datetime-dateformat.md) | ฟังก์ชันนี้ส่งกลับค่า *[สตริง](er-formula-supported-data-types-primitive.md#string)* ที่แสดงค่าวันที่ที่ให้เป็นข้อความในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือก |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงค่าวันที่/เวลาที่ให้เป็นข้อความในรูปแบบที่ระบุและใน Culture ที่ระบุเป็นทางเลือก |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและใน Culture ไปยังค่าวันที่/เวลาที่ระบุเป็นทางเลือก |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่ถูกแปลงจากค่าวันที่ที่กำหนดให้เป็นค่าวันที่/เวลาในเวลาสากล (เวลามาตรฐานกรีนิช \[GMT\]) |
| [DateValue](er-functions-datetime-datevalue.md) | ฟังก์ชันนี้ส่งคืนค่า *[วันที่](er-formula-supported-data-types-primitive.md#date)* ที่แปลงจากค่าข้อความที่ให้ในรูปแบบที่ระบุและในวัฒนธรรมไปยังค่าวันที่ที่ระบุเป็นทางเลือก |
| [DayOfYear](er-functions-datetime-dayofyear.md) | ฟังก์ชันนี้ส่งคืนค่าที่แสดง *[จำนวนเต็ม](er-formula-supported-data-types-primitive.md#integer)* ของวันระหว่างวันที่ 1 มกราคมและวันที่ระบุ |
| [วัน](er-functions-datetime-days.md) | ฟังก์ชันนี้ส่งคืนค่าที่แสดง *จำนวนเต็ม* ที่แสดงจำนวนของวันระหว่างวันที่ที่ระบุที่หนึ่งกับวันที่ที่ระบุที่สอง |
| [Now](er-functions-datetime-now.md) | ฟังก์ชันนี้ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน |
| [NullDate](er-functions-datetime-nulldate.md) | ฟังก์ชันนี้ส่งคืนค่า *Date* ที่แสดงถึงวันที่ **ที่เป็นแบบ null** (1 มกราคม 1900) |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | ฟังก์ชันนี้ส่งกลับค่า *DateTime* ที่แสดงค่าวัน/เวลา **ที่เป็น null** (1 มกราคม 1900) ในเวลาสากลที่สอดคล้องกัน |
| [SessionNow](er-functions-datetime-sessionnow.md) | ฟังก์ชันนี้ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซสชันแอปพลิเคชันปัจจุบัน |
| [SessionToday](er-functions-datetime-sessiontoday.md) | ฟังก์ชันนี้ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซสชันแอปพลิเคชันปัจจุบัน |
| [วันนี้](er-functions-datetime-today.md) | ฟังก์ชันนี้ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน |
| [WeekNum](er-functions-datetime-weeknum.md) | ฟังก์ชันนี้ส่งคืนค่า *จำนวนเต็ม* ที่แสดงถึงสัปดาห์ของปี |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
