---
title: ฟังก์ชัน INTVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) INTVALUE
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743650"
---
# <a name="intvalue-er-function"></a>ฟังก์ชัน INTVALUE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `INTVALUE` ส่งกลับค่า *Int* ที่แสดงถึงสตริงที่ระบุ

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่าข้อความต้องถูกแปลงเป็นหมายเลย *Int*

`number`: *จำนวนจริง* หรือ *จำนวนเต็ม*

ค่า *จำนวนจริง* or *จำนวนเต็ม* ที่เป็นตัวเลขต้องถูกแปลงเป็นหมายเลย *Int*

## <a name="return-values"></a>ค่าที่ส่งคืน

*Int*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ตำแหน่งทศนิยมใดๆ จะถูกตัดออก

## <a name="example-1"></a>ตัวอย่างที่ 1

`INTVALUE ("100.77")` ส่งกลับค่า *Int* **100**

## <a name="example-2"></a>ตัวอย่างที่ 2

`INTVALUE (-100.77)` ส่งกลับค่า *Int* **-100**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันการแปลงของชนิด](er-functions-category-type-conversion.md)
