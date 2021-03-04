---
title: รายการของฟังก์ชั่น ER ในประเภทข้อความ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันข้อความที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 228620afc81e154eced572f3b6024d6836d00d66
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686038"
---
# <a name="list-of-er-functions-of-the-text-category"></a>รายการของฟังก์ชั่น ER ในประเภทข้อความ

[!include [banner](../includes/banner.md)]

ฟังก์ชันข้อความการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อดำเนินการกับแหล่งข้อมูลของชนิดข้อมูล *สตริง* หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้

## <a name="list-of-supported-functions"></a>รายการฟังก์ชันที่ได้รับการสนับสนุน

| ฟังก์ชัน | คำอธิบาย |
|----------|-------------|
| [Char](er-functions-text-char.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่นำเสนออักขระเดี่ยวที่ถูกอ้างอิงโดยหมายเลข Unicode ที่ระบุ |
| [เชื่อมเข้าด้วยกัน](er-functions-text-concatenate.md) | ฟังก์ชันนี้ส่งกลับสตริงข้อความที่ระบุทั้งหมดเป็นค่า *สตริง* หลังจากที่ได้เข้าร่วมเป็นหนึ่งสตริง |
| [รูปแบบ](er-functions-text-format.md) | ฟังก์ชันนี้ส่งคืนสตริงที่ระบุเป็นค่า *สตริง* หลังจากที่ได้ถูกจัดรูปแบบโดยการแทนที่การเกิดเหตุการณ์ใดๆ ของ **%N** ด้วยอาร์กิวเมนต์ลำดับที่ *N* |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | ฟังก์ชันนี้ค้นหาค่า *Enum* ที่ระบุในแหล่งข้อมูลการแจงนับที่ระบุ โดยใช้ชื่อการแจงนับที่ระบุเป็นค่า *สตริง* ถ้าพบค่า *Enum* ฟังก์ชันจะส่งคืน |
| [GuidValue](er-functions-text-guidvalue.md) | ฟังก์ชันนี้แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *GUID* |
| [JsonValue](er-functions-text-jsonvalue.md) | ฟังก์ชันนี้แยกวิเคราะห์ข้อมูลในรูปแบบ JavaScript Object Notation (JSON) ที่เข้าถึงได้ที่พาธที่ระบุ และจะแยกค่าสเกลตามรหัสที่ระบุ จากนั้น จะส่งกลับค่าสเกลที่แยกเป็นค่า *สตริง* |
| [ซ้าย](er-functions-text-left.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากจุดเริ่มต้นของสตริงที่ระบุ |
| [Len](er-functions-text-len.md) | ฟังก์ชันนี้ส่งกลับค่า *จำนวนเต็ม* ที่แสดงตัวเลขหรืออักขระในสตริงที่ระบุ |
| [Lower](er-functions-text-lower.md) | ฟังก์ชันนี้ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์เล็ก |
| [Mid](er-functions-text-mid.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากสตริงที่ระบุ ซึ่งเริ่มต้นที่ตำแหน่งที่ระบุ |
| [NumberFormat](er-functions-text-numberformat.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงหมายเลขที่ระบุในรูปแบบที่ระบุและในวัฒนธรรมที่ระบุเป็นทางเลือก |
| [NumeralsToText](er-functions-text-numeralstotext.md) | ฟังก์ชันนี้ส่งกลับหมายเลขที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกสะกด (นั่นคือ ถูกแปลงเป็นสตริงข้อความ) ในภาษาที่ระบุ |
| [PadLeft](er-functions-text-padleft.md) | ฟังก์ชันนี้ส่งคืนค่า *สตริง* ของความยาวที่ระบุ ซึ่งมีการเริ่มต้นสตริงที่ระบุด้วยอักขระที่ระบุด้วยหนึ่งอินสแตนช์หรือมากกว่านั้นของอักขระที่ระบุ |
| [QrCode](er-functions-text-qrcode.md) | ฟังก์ชันนี้ส่งกลับค่า *คอนเทนเนอร์* ที่แสดงรูป Quick Response code (QR code) สำหรับสตริงที่ระบุในรูปแบบไบนารี |
| [แทนที่](er-functions-text-replace.md) | ฟังก์ชันนี้ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากทั้งหมดหรือบางส่วนถูกแทนที่ด้วยสตริงอื่น |
| [สิทธิ์](er-functions-text-right.md) | ฟังก์ชันนี้ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากจุดสิ้นสุดของสตริงที่ระบุ |
| [ข้อความ](er-functions-text-text.md) | ฟังก์ชันนี้ส่งคืนตัวเลขที่ระบุเป็นค่า *สตริง* หลังจากที่ได้ถูกแปลงเป็นข้อความแบบสตริงที่ถูกจัดรูปแบบตามการตั้งค่าตำแหน่งที่ตั้งของเซิร์ฟเวอร์ของอินสแตนซ์ของแอปพลิเคชันปัจจุบัน |
| [แปล](er-functions-text-translate.md) | ฟังก์ชันนี้ส่งคืนค่า *สตริง* ที่มีผลลัพธ์ของการแทนที่อักขระของข้อความที่ระบุไว้สำหรับอักขระของชุดอักขระที่กำหนดไว้อีกชุดหนึ่ง |
| [Trim](er-functions-text-trim.md) | ฟังก์ชันนี้ส่งคืนสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากช่องว่างนำหน้าและต่อท้ายถูกตัดออกแล้ว และหลังจากที่ได้ลบช่องว่างหลายช่องระหว่างคำ |
| [Upper](er-functions-text-upper.md) | ฟังก์ชันนี้ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกแปลงเป็นตัวพิมพ์ใหญ่ |

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting-formula-designer.md)

[ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]