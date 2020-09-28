---
title: ฟังก์ชัน ER SPLIT
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLIT
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: c171509353fed92b14ca0d7473742e4a9a54bad1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745284"
---
# <a name="split-er-function"></a>ฟังก์ชัน ER SPLIT

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `SPLIT` แบ่งค่าสตริงการป้อนที่ระบุลงในสตริงย่อยและส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
SPLIT (input, length)
```

ไวยากรณ์นี้แบ่งสตริงที่ระบุเป็นสตริงย่อยซึ่งมีความยาวที่ระบุ

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
SPLIT (input, delimiter)
```

ไวยากรณ์นี้ใช้แบ่งสตริงย่อยที่ระบุออกเป็นสตริงย่อยตามตั่วคั่นที่ระบุ

## <a name="arguments"></a>อาร์กิวเมนต์

`input`: *สตริง*

ข้อความที่จะแบ่ง

`length`: *เลขจำนวนเต็ม*

ความยาวสูงสุดของสตริงย่อยเดียว

`delimiter`: *สตริง*

ตัวคั่นที่ใช้ในการแยกสตริงย่อย

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

โครงสร้างเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยฟิลด์ **ค่า** ของชนิด *สตริง* ทุกเรกคอร์ดของรายการที่ถูกส่งกลับประกอบด้วยสตริงย่อยที่สร้างขึ้นในฟิลด์นี้

ถ้าอาร์กิวเมนต์ `delimiter` ว่าง รายการใหม่ที่ถูกส่งกลับที่ประกอบด้วยเรกคอร์ดหนึ่งรายการที่มีฟิลด์ **ค่า** ของชนิด *สตริง* ฟิลด์นี้ประกอบด้วยข้อความป้อนเข้า

ถ้าอาร์กิวเมนต์ `input` ว่างเปล่า จะมีการส่งคืนรายการที่ว่างเปล่าใหม่ ถ้าไม่สามารถระบุอาร์กิวเมนต์ `input` หรือ `delimiter` (null) จะมีข้อยกเว้นแอปพลิเคชันเกิดขึ้น

## <a name="example-1"></a>ตัวอย่างที่ 1

`SPLIT ("abcd", 3)` ส่งคืนรายการใหม่ที่ประกอบด้วยสองเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง* ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"abc"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"d"**

## <a name="example-2"></a>ตัวอย่างที่ 2

`SPLIT ("XAb aBy", "aB")` ส่งคืนรายการใหม่ที่ประกอบด้วยสามเรกคอร์ดที่มีฟิลด์ **ค่า** ของชนิด *สตริง* ฟิลด์ **ค่า** ในเรกคอร์ดแรกประกอบด้วยข้อความ **"X"** ฟิลด์ **ค่า** ในเรกคอร์ดที่สองประกอบด้วยข้อความ **"&nbsp;"** และฟิลด์ **ค่า** ในเรกคอร์ดที่สามประกอบด้วยข้อความ **"y"** 

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
