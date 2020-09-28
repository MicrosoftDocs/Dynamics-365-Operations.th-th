---
title: ฟังก์ชัน NOW ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NOW (ER)
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e8c411e1ce9656ffa35986f1ceef712c9def1e6b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743530"
---
# <a name="now-er-function"></a>ฟังก์ชัน NOW ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NOW` ส่งคืนค่า *DateTime* ที่แสดงถึงวันที่และเวลาของเซิร์ฟเวอร์แอปลิเคชันปัจจุบัน

## <a name="syntax"></a>ไวยากรณ์

```vb
NOW ()
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่และเวลา*

ค่าวันที่/เวลาที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` ส่งคืนค่าวันที่/เวลาของเซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)
