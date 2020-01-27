---
title: ฟังก์ชัน REPLACE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ REPLACE (ER)
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916878"
---
# <a name="REPLACE">ฟังก์ชัน REPLACE ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `REPLACE` ส่งกลับสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากทั้งหมดหรือบางส่วนถูกแทนที่ด้วยสตริงอื่น

## <a name="syntax"></a>ไวยากรณ์

```
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

หากอาร์กิวเมนต์ `regular expression flag` เป็น **เท็จ** ฟังก์ชันนี้จะทำงานเช่นเดียวกับ [TRANSLATE](er-functions-text-translate.md) อักขระที่ถูกที่ระบุโดยอาร์กิวเมนต์ `replacement` ถูกใช้ในการแทนที่อักขระที่พบ 

## <a name="example-1"></a>ตัวอย่างที่ 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` ใช้นิพจน์ทั่วไปที่ลบสัญลักษณ์ที่ไม่ใช่ตัวเลขทั้งหมด และส่งกลับ **"19234564971"** 

## <a name="example-2"></a>ตัวอย่างที่ 2

`REPLACE ("abcdef", "cd", "GH", false)` แทนที่รูปแบบ **"cd"** ด้วยสตริง **"GH"** และส่งกลับค่า **"abGHef"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
