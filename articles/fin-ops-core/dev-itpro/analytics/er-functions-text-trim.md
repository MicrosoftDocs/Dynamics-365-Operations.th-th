---
title: ฟังก์ชัน TRIM ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRIM (ER)
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273112"
---
# <a name="trim-er-function"></a>ฟังก์ชัน TRIM ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `TRIM` จะส่งคืนสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังแท็บ อักขระขึ้นบรรทัดใหม่ การป้อนบรรทัด และอัขระการป้อนแบบฟอร์มจะถูกแทนที่ด้วยอักขระช่องว่างเดียว หลังช่องว่างนำหน้าและช่องว่างต่อท้ายถูกตัดให้สั้นลง และหลังจากที่ลบช่องว่างหลายช่องระหว่างอักขระ

## <a name="syntax"></a>ไวยากรณ์

```vb
TRIM (text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*

## <a name="return-values"></a>ค่าที่ส่งคืน

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ในบางกรณี คุณอาจต้องการตัดช่องว่างนำหน้าและช่องว่างต่อท้ายให้สั้นลง แต่ยังคงรักษาการจัดรูปแบบของข้อความที่ระบุไว้ ตัวอย่างเช่น เมื่อข้อความนี้แสดงถึงที่อยู่ที่สามารถป้อนในกล่องข้อความหลายบรรทัด ซึ่งอาจประกอบด้วยเนื้อหาป้อนบรรทัดและการจัดรูปแบบอักขระขึ้นบรรทัดใหม่ ในกรณีนี้ ให้ใช้นิพจน์ต่อไปนี้: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` โดยที่ `text` เป็นอาร์กิวเมนต์ที่อ้างอิงถึงสตริงข้อความที่ระบุ

## <a name="example-1"></a>ตัวอย่างที่ 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` ส่งกลับ **"ข้อความตัวอย่าง"**

## <a name="example-2"></a>ตัวอย่างที่ 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` ส่งคืน **"ข้อความตัวอย่าง"**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)

[ฟังก์ชัน REPLACE ER](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
