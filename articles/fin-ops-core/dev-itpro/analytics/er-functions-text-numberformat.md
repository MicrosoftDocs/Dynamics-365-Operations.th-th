---
title: ฟังก์ชัน NUMBERFORMAT ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMBERFORMAT (ER)
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5519f549c10ba5c02e249592d040582c3f8dc44f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274809"
---
# <a name="numberformat-er-function"></a>ฟังก์ชัน NUMBERFORMAT ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NUMBERFORMAT` ส่งกลับค่า *สตริง* ที่แสดงหมายเลขที่ระบุในรูปแบบที่ระบุและใน [ภาษา](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](/dotnet/standard/base-types/standard-numeric-format-strings) และ [กำหนดเอง](/dotnet/standard/base-types/custom-numeric-format-strings)

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*

ค่าตัวเลขที่ระบุหมายเลขที่ต้องถูกจัดรูปแบบ

`format` : *สตริง*

ค่า *สตริง* ที่แสดงถึงรูปแบบ

`culture`: *สตริง*

ค่า *สตริง* ที่แสดงถึงภาษาที่จะใช้สำหรับการจัดรูปแบบ

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ถ้าภาษาไม่ได้ถูกกำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก บริบทที่มีการเรียกใช้ฟังก์ชันนี้จะกำหนดภาษาที่ใช้ในการจัดรูปแบบตัวเลข

## <a name="example-1"></a>ตัวอย่างที่ 1

สำหรับภาษา **EN-US** `NUMBERFORMAT (0.45, "p")` ส่งกลับค่า **"45.00 %"** และ `NUMBERFORMAT (10.45, "#")` ส่งกลับค่า **"10"**

## <a name="example-2"></a>ตัวอย่างที่ 2

`NUMBERFORMAT (10/3, "F2", "de")` ส่งกลับค่า **3,33** ในขณะที่ `NUMBERFORMAT (10/3, "F2", "en-us")` ส่งกลับค่า **3.33**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
