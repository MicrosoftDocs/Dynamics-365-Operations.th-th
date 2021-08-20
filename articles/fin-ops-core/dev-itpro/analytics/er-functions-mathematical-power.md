---
title: ฟังก์ชัน POWER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) POWER
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
ms.openlocfilehash: 6955d2787b2a9be6d38fe10165a9d5ef8310b108e3a9772709d9d1ff51712424
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767155"
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