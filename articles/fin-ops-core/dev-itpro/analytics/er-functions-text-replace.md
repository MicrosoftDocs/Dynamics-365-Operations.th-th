---
title: ฟังก์ชัน REPLACE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ REPLACE (ER)
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: c9f1abe397e05f816fcf226df76362d872819f57
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570275"
---
# <a name="replace-er-function"></a>ฟังก์ชัน REPLACE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `REPLACE` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากทั้งหมดหรือบางส่วนถูกแทนที่ด้วยสตริงอื่น

## <a name="syntax"></a>ไวยากรณ์

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*

`pattern`: *สตริง*

ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** อาร์กิวเมนต์นี้ประกอบด้วยข้อความที่ต้องถูกแทนที่

ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** อาร์กิวเมนต์นี้ประกอบด้วยนิพจน์ทั่วไปที่กำหนดทั้งรูปแบบการค้นหาและข้อความการแทนที่

`replacement`: *สตริง*

ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** อาร์กิวเมนต์นี้ประกอบด้วยข้อความเพื่อใช้เป็นการแทนที่

ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** อาร์กิวเมนต์นี้จะไม่ถูกใช้

`regular expression flag`: *บูลีน*

ค่า *บูลีน* ที่บ่งชี้ว่ามีการใช้นิพจน์ทั่วไปเพื่อทำการแทนที่หรือไม่

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **จริง** ฟังก์ชันนี้จะส่งกลับสตริงที่ระบุ หลังจากที่มีการเปลี่ยนแปลงโดยใช้นิพจน์ทั่วไปที่ระบุโดยอาร์กิวเมนต์ `pattern` นิพจน์ทั่วไปจะถูกใช้ในการค้นหาอักขระซึ่งต้องถูกแทนที่

ถ้าอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** ฟังก์ชันนี้ส่งคืนสตริงที่ระบุหลังจากชุดของอักขระที่กำหนดไว้ในอาร์กิวเมนต์ `pattern` ถูกแทนที่โดยอักขระของอาร์กิวเมนต์ `replacement` 

## <a name="example-1"></a>ตัวอย่างที่ 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` ใช้นิพจน์ทั่วไปที่ลบสัญลักษณ์ที่ไม่ใช่ตัวเลขทั้งหมด และส่งกลับ **"19234564971"** 

## <a name="example-2"></a>ตัวอย่างที่ 2

`REPLACE ("abcdef", "cd", "GH", false)` แทนที่รูปแบบ **"cd"** ด้วยสตริง **"GH"** และส่งกลับค่า **"abGHef"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]