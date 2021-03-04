---
title: ฟังก์ชัน IF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) IF
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687013"
---
# <a name="if-er-function"></a>ฟังก์ชัน IF ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `IF` ส่งคืนค่าที่ระบุค่าแรก หากตรงตามเงื่อนไขที่ที่ระบุ มิฉะนั้นจะส่งคืนค่าที่สองที่ระบุ ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน

## <a name="syntax"></a>ไวยากรณ์

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>อาร์กิวเมนต์

`condition`: *บูลีน*

นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ

`first value`: *ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*

ผลลัพธ์ที่ถูกส่งกลับถ้าเป็นไปตามเงื่อนไข

`second value`: *ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*

ผลลัพธ์ที่ถูกส่งกลับถ้าไม่เป็นไปตามเงื่อนไข

## <a name="return-values"></a>ค่าที่ส่งคืน

*ชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน*

ค่าผลลัพธ์ของชนิดข้อมูลใดๆ ที่ได้รับการสนับสนุน

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

อาร์กิวเมนต์ `first value` และ `second value` ต้องถูกระบุและโดยใช้ชนิดข้อมูลเดียวกัน มีข้อยกเว้นเกิดขึ้นในเวลาออกแบบถ้าชนิดข้อมูลของค่าที่ถูกกำหนดค่าไม่ตรงกัน

ถ้าค่าแรกและค่าที่สองคือค่าของชนิดข้อมูลของ *คอนเทนเนอร์ (เรกคอร์ด)* หรือชนิดข้อมูล *รายการเรกคอร์ด* ผลลัพธ์จะมีเฉพาะฟิลด์ที่มีอยู่ในค่าทั้งสองเท่านั้น

## <a name="example"></a>ตัวอย่าง

`IF (1=2, "condition is met", "condition is not met")` จะส่งกลับสตริง **"ไม่เป็นไปตามเงื่อนไข"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันตรรกะ](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]