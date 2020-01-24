---
title: ฟังก์ชัน OR ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) OR
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917131"
---
# <a name="OR">ฟังก์ชัน OR ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `OR` ส่งกลับค่า *บูลีน* ของ **FALSE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นเท็จ ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง ฟังก์ชันจะส่งกลับค่า *บูลีน* ของ **TRUE**

## <a name="syntax"></a>ไวยากรณ์

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`condition 1`: *บูลีน*

นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ ต้องระบุอาร์กิวเมนต์นี้

`condition N`: *บูลีน*

นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องถูกทดสอบ อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ค่าที่ส่งคืน

*บูลีน*

ค่า *บูลีน* ที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`OR (1=2, "a"="a")` ส่งกลับค่า **TRUE**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันตรรกะ](er-functions-category-logical.md)
