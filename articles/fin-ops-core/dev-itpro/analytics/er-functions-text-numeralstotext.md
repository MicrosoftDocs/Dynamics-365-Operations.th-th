---
title: ฟังก์ชัน NUMERALSTOTEXT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMERALSTOTEXT (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31fd4076d04ce7d849555bc8301c4d23ad8e1a7e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041029"
---
# <a name="NUMERALSTOTEXT">ฟังก์ชัน NUMERALSTOTEXT ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NUMERALSTOTEXT` ส่งกลับหมายเลขที่ระบุเป็นค่า *สตริง* หลังจากที่ถูกสะกด (นั่นคือ ถูกแปลงเป็นสตริงข้อความ) ในภาษาที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*

ค่าตัวเลขที่ระบุหมายเลขที่ต้องถูกสะกด

`language`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสภาษา

`currency`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสสกุลเงิน

`print currency name flag`: *บูลีน*

ค่า *บูลีน* ที่บ่งชี้ว่าต้องเพิ่มชื่อสกุลเงินในข้อความที่สะกดหรือไม่

`decimal points`: *เลขจำนวนเต็ม*

ค่า *เลขจำนวนเต็ม* ที่ระบุจำนวนของตำแหน่งทศนิยมที่ข้อความที่สะกดควรมี

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ไม่จำเป็นต้องระบุรหัสภาษา หากมีการกำหนดเป็นสตริงว่าง รหัสภาษาสำหรับบริบทที่รันจะถูกนำมาใช้ รหัสภาษาเริ่มต้นคือ **EN-US** รหัสภาษาสำหรับบริบทที่กำลังทำงานอยู่ถูกกำหนดในองค์ประกอบ **โฟลเดอร์** หรือ **ไฟล์** ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่กำลังทำงานอยู่

ไม่จำเป็นต้องระบุรหัสสกุลเงิน หากมีการกำหนดเป็นสตริงว่าง สกุลเงินของบริษัทสำหรับบริบทที่รันจะถูกนำมาใช้

> [!NOTE] 
> อาร์กิวเมนต์ `print currency name flag` และ `decimal points` ถูกวิเคราะห์สำหรับรหัสภาษาต่อไปนี้เท่านั้น: **CS** **ET** **HU** **LT** **LV** **PL** และ **RU** นอกจากนี้ อาร์กิวเมนต์ `print currency name flag` จะถูกวิเคราะห์สำหรับบริษัทที่บริบทของประเทศหรือของภูมิภาคสนับสนุนการกระจายของชื่อสกุลเงิน

## <a name="example-1"></a>ตัวอย่างที่ 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` ส่งกลับค่า **"หนึ่งพันสองร้อยสามสิบสี่และ 56"**

## <a name="example-2"></a>ตัวอย่างที่ 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` ส่งกลับค่า **"Sto dwadzieścia"** 

## <a name="example-3"></a>ตัวอย่างที่ 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` ส่งกลับค่า **"Сто двадцать евро 21 евроцент"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
