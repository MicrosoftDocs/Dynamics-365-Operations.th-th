---
title: ฟังก์ชั่น ER TODAY
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) TODAY
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 12c4489751e9e0c06d4b628e7c297eee472054369f7cfacee048622cbc39d074
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755837"
---
# <a name="today-er-function"></a>ฟังก์ชั่น ER TODAY

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `TODAY` ส่งคืนค่า *Date* ที่แสดงถึงวันที่เซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน

## <a name="syntax"></a>ไวยากรณ์

```xpp
TODAY ()
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่*

ค่าวันที่ที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` ส่งคืนค่าวันที่ซิร์ฟเวอร์แอปพลิเคชันปัจจุบัน วันที่ 24 ธันวาคม 2015  เป็นสตริง **"24-12-2015"** ตามรูปแบบเฉพาะที่กำหนดไว้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]