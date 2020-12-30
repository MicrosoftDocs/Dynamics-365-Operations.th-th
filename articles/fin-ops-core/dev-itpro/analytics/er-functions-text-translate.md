---
title: ฟังก์ชัน TRANSLATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRANSLATE (ER)
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
ms.openlocfilehash: c5d192b8679d6df2c44a0038fe4ffc181a6a54df
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685314"
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
