---
title: ฟังก์ชัน ER SESSIONNOW
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SESSIONNOW
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
ms.openlocfilehash: 586d49a1fbbbcab7b0cd41c31daf0f50598754c2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884212"
---
# <a name="sessionnow-er-function"></a>ฟังก์ชัน ER SESSIONNOW

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `SESSIONNOW` ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซสชันแอปลิเคชันปัจจุบัน

## <a name="syntax"></a>ไวยากรณ์

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่และเวลา*

ค่าวันที่/เวลาที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` ส่งกลับวันที่/เวลาเซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24.12.2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]