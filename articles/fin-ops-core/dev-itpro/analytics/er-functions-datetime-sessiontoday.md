---
title: ฟังก์ชัน SESSIONTODAY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SESSIONTODAY
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042285"
---
# <a name="SESSIONTODAY">ฟังก์ชัน SESSIONTODAY ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `SESSIONTODAY` ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซสชันแอปพลิเคชันปัจจุบัน

## <a name="syntax"></a>ไวยากรณ์

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่*

ค่าวันที่ที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` ส่งกลับวันที่เซสชันของแอปพลิเคชันปัจจุบัน 24 ธันวาคม 2015 เป็นสตริง **"24-12-2015"** ตามวัฒนธรรมเยอรมันที่เลือกและรูปแบบที่ระบุ

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)
