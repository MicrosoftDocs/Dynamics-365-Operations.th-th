---
title: ฟังก์ชัน POWER ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) POWER
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da3ae988b57cb5588de1e2fd8ee962b77b5534ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864701"
---
# <a name="power-er-function"></a>ฟังก์ชัน POWER ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `POWER` ส่งกลับค่า *จริง* ที่แสดงถึงผลของการเพิ่มจำนวนบวกที่ระบุให้กับพลังงานที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
POWER (number, power)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จำนวนจริง* หรือ *จำนวนเต็ม*

ค่าตัวเลขที่ต้องถูกยกขึ้นกับพลังงานที่ระบุ

`power`: *จำนวนจริง* หรือ *จำนวนเต็ม*

ค่าตัวเลขที่แสดงถึงพลังงานเฉพาะ

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

`POWER (10, 2)` ส่งกลับค่า **100**

## <a name="example-2"></a>ตัวอย่างที่ 2

`POWER (4, 0.5)` ส่งกลับค่า **2**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันคณิตศาสตร์](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]