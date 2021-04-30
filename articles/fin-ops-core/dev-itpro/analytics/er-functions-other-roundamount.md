---
title: ฟังก์ชัน ROUNDAMOUNT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ROUNDAMOUNT (ER)
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 7dfc7817eab68e9dd70ce84e68f26d14fd8cf1df
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891220"
---
# <a name="roundamount-er-function"></a>ฟังก์ชัน ROUNDAMOUNT ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ROUNDAMOUNT` ส่งกลับค่า *จำนวนจริง* เป็นผลลัพธ์ของการปัดเศษของหมายเลขที่ระบุเป็นผลคูณที่ใกล้เคียงที่สุดของหมายเลขอื่นตามกฎการปัดเศษที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *เลขจำนวนเต็ม* หรือ *จำนวนจริง*

ค่าตัวเลขที่ต้องถูกปัดเศษ

`decimals`: *เลขจำนวนเต็ม* หรือ *จำนวนจริง*

หมายเลขที่ค่าของพารามิเตอร์ `number` ต้องถูกปัดเศษเป็นผลคูณ

`round rule`: *ค่า Enum*

ค่าการแจงนับของการแจงนับ **RoundOffType** ที่กำหนดกฎการปัดเศษ การแจงนับนี้มีค่าต่อไปนี้:

- ปกติ (ปกติ)
- ลงข้างล่าง (RoundDown)
- การปัดเศษขึ้น (RoundUp)

## <a name="return-values"></a>ส่งคืนค่า

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์คือผลคูณของค่าที่ระบุโดยพารามิเตอร์ `decimals` และใกล้เคียงที่สุดกับค่าที่ระบุโดยพารามิเตอร์ `number`

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

เมื่อพารามิเตอร์ `number` เป็นศูนย์ ฟังก์ชันนี้จะคืนค่าศูนย์เสมอ

เมื่อพารามิเตอร์ `decimals` เป็นศูนย์ ฟังก์ชันนี้จะปัดเศษเป็นค่าการปัดเศษเริ่มต้น เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.Ordinary** ค่าการปัดเศษเริ่มต้นคือ **0.01** มิฉะนั้น ค่าการปัดเศษเริ่มต้นคือ **1.0**

เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.Ordinary** ฟังก์ชันนี้ปัดเศษเป็นจำนวนที่ปัดเศษที่ใกล้ที่สุด

เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.RoundDown** ฟังก์ชันนี้ปัดเศษไปยังศูนย์เป็นจำนวนที่ปัดเศษที่ใกล้ที่สุด

เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.RoundUp** ฟังก์ชันนี้ปัดเศษออกจากศูนย์เป็นจำนวนที่ปัดเศษที่ใกล้ที่สุด

เมื่อพารามิเตอร์ `round rule` ถูกตั้งค่าเป็น **RoundOffType.Ordinary** ฟังก์ชันนี้ทำงานเช่นเดียวกับฟังก์ชัน Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) และฟังก์ชัน X ++ [ROUND](../dev-ref/xpp-math-run-time-functions.md#round)

## <a name="remarks"></a>ข้อสังเกต

หากต้องการปัดเศษค่าตัวเลขให้เป็นตำแหน่งทศนิยมที่ระบุ ให้ใช้ฟังก์ชัน [ROUND](er-functions-mathematical-round.md)

## <a name="example"></a>ตัวอย่าง

ถ้าพารามิเตอร์ **model.RoundOff** ถูกตั้งค่าเป็น **RoundOffType.Ordinary** `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` ส่งกลับค่า 7.35 

ถ้าพารามิเตอร์ **model.RoundOff** ถูกตั้งค่าเป็น **RoundOffType.RoundDown** `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` ส่งกลับค่า 7.35 

ถ้าพารามิเตอร์ **model.RoundOff** ถูกตั้งค่าเป็น **RoundOffType.RoundUp** `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` ส่งกลับค่า 8.4

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)

[ฟังก์ชันคณิตศาสตร์](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]