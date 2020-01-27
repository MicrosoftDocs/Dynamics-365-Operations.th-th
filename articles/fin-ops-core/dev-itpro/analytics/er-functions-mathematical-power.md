---
title: ฟังก์ชัน POWER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) POWER
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915912"
---
# <a name="POWER">ฟังก์ชัน POWER ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `POWER` ส่งกลับค่า *จริง* ที่แสดงถึงผลของการเพิ่มจำนวนบวกที่ระบุให้กับพลังงานที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```
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
