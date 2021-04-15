---
title: ฟังก์ชัน NUMBERVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NUMBERVALUE
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755359"
---
# <a name="numbervalue-er-function"></a>ฟังก์ชัน NUMBERVALUE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NUMBERVALUE` ส่งกลับค่า *จำนวนจริง* ที่ถูกแปลงจากค่า *สตริง* ที่ระบุ ในระหว่างการแปลงจะมีการพิจารณาตัวแบ่งการจัดกลุ่มทศนิยมและเลขฐานที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่าข้อความต้องถูกแปลงเป็นหมายเลย *จำนวนจริง*

`decimal separator`: สตริง

ตัวแบ่งทศนิยม ใช้ในการแยกจำนวนเต็มและเศษส่วนของตัวเลขทศนิยม

`digit grouping separator`: *สตริง*

ตัวแบ่งการจัดกลุ่มตัวเลข ใช้เป็นตัวแบ่งหลักพัน

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`NUMBERVALUE( "1 234,56", ",", " ")` ส่งกลับค่า **1234.56**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันการแปลงของชนิด](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]