---
title: ฟังก์ชัน VALUE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) VALUE
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 0a47637c47ca6c947451efa1230191779401b4e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277676"
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
