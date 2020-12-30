---
title: ฟังก์ชัน CN_GBT_ADDITIONALDIMENSIONID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CN_GBT_ADDITIONALDIMENSIONID (ER)
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686821"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>ฟังก์ชัน CN_GBT_ADDITIONALDIMENSIONID ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `CN_GBT_ADDITIONALDIMENSIONID` ส่งกลับค่า *สตริง* ที่แสดงถึงรหัสมิติทางการเงินเดียวที่ถูกนำมาจากสตริงที่ระบุ สตริงที่ระบุแสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค

## <a name="syntax"></a>ไวยากรณ์

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่า *สตริง* ที่แสดงมิติทั้งหมดเป็นรายการของรหัสที่คั่นด้วยเครื่องหมายจุลภาค

`number`: เลขจำนวนเต็ม

ค่า *เลขจำนวนเต็ม* จะกำหนดรหัสลำดับของมิติที่ร้องขอในสตริงที่ระบุ

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`  ส่งคืน **"CC"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)
