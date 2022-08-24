---
title: ฟังก์ชัน POWER ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) POWER
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274010"
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
