---
title: ฟังก์ชัน TRANSLATE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRANSLATE (ER)
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278455"
---
# <a name="translate-er-function"></a>ฟังก์ชัน TRANSLATE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `TRANSLATE` ส่งคืนค่า *สตริง* ที่มีผลลัพธ์ของการแทนที่อักขระของข้อความที่ระบุไว้ในอักขระของชุดที่กำหนดไว้อีกชุดหนึ่ง

## <a name="syntax"></a>ไวยากรณ์

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*

`pattern`: *สตริง*

ข้อความที่จะต้องถูกแทนที่

`replacement`: *สตริง*

ข้อความที่จะใช้เป็นการแทนที่

## <a name="return-values"></a>ค่าที่ส่งคืน

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชัน `TRANSLATE` จะแทนที่หนึ่งอักขระพร้อมกัน ฟังก์ชันจะแทนที่อักขระตัวแรกของอาร์กิวเมนต์ `text` โดยใช้อักขระตัวแรกของอาร์กิวเมนต์ `pattern` และอักขระตัวที่สอง และปฏิบัติตามขั้นตอนเดียวกันจนกว่าจะเสร็จสิ้น เมื่ออักขระจากอาร์กิวเมนต์ `text` และ `pattern` ตรงกัน จะถูกแทนที่ด้วยอักขระจากอาร์กิวเมนต์ `replacement` ที่อยู่ในตำแหน่งเดียวกันกับอักขระจากอาร์กิวเมนต์ `pattern` ถ้าอักขระปรากฏหลายครั้งในอาร์กิวเมนต์ `pattern` การแม็ปอาร์กิวเมนต์ `replacement` ที่สอดคล้องกับการเกิดขึ้นครั้งแรกของอักขระนี้จะถูกใช้

## <a name="example-1"></a>ตัวอย่างที่ 1

`TRANSLATE ("abcdef", "cd", "GH")` แทนที่อักขระ **"c"** ของข้อความ **"abcdef"** ที่ระบุที่มีอักขระ **"G"** ของข้อความ `replacement` อันเนื่องมาจากตัวอย่างต่อไปนี้:
-   อักขระ **"c"** จะแสดงอยู่ในข้อความ `pattern` ในตำแหน่งแรก
-   ตำแหน่งแรกของข้อความ `replacement` มีอักขระ **"G"**

## <a name="example-2"></a>ตัวอย่างที่ 2

`TRANSLATE ("abcdef", "ccd", "GH")` ส่งกลับค่า **"abGdef"**

## <a name="example-3"></a>ตัวอย่างที่ 3

`TRANSLATE ("abccba", "abc", "123")` ส่งคืน **"123321"**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
