---
title: ฟังก์ชัน VALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) VALUE
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 56b32a802674725347ab496d3a09b99c8f04446d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681219"
---
# <a name="value-er-function"></a>ฟังก์ชัน VALUE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `VALUE` ส่งกลับค่า *จริง* ที่ถูกแปลงจากสตริงที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
VALUE (text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ไม่สามารถแปลงค่าสตริงเป็นค่าตัวเลข

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

เครื่องหมายจุลภาคและอักขระจุด (.) ถือเป็นตัวแบ่งทศนิยม และยุติภังค์นำหน้า (-) จะถูกใช้เป็นเครื่องหมายลบ มีข้อยกเว้นเกิดขึ้นในขณะรันไทม์ ถ้าสตริงที่ระบุประกอบด้วยอักขระที่ไม่ใช่ตัวเลขอื่นๆ

## <a name="example-1"></a>ตัวอย่างที่ 1

`VALUE ("1 234,56")` เกิดข้อยกเว้น

## <a name="example-2"></a>ตัวอย่างที่ 2

`VALUE ("1234,56")` ส่งกลับค่า **1234.56**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันการแปลงของชนิด](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]