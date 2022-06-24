---
title: ฟังก์ชัน DAYOFYEAR ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DAYOFYEAR
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: fc4d1d3293c31b1b89a7390c8ac313e1407d433e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848793"
---
# <a name="dayofyear-er-function"></a>ฟังก์ชัน DAYOFYEAR ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `DAYOFYEAR` ส่งคืนค่าที่แสดง *จำนวนเต็ม* ของวันระหว่างวันที่ 1 มกราคมและวันที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>อาร์กิวเมนต์

`date`: *วันที่*

ค่าวันที่ที่แสดงถึงวันที่ที่จะใช้สำหรับการคำนวณจำนวนวัน

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนเต็ม*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` ส่งกลับค่า **61**

## <a name="example-2"></a>ตัวอย่างที่ 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` ส่งกลับค่า **1**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]