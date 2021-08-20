---
title: ฟังก์ชัน NULLDATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NULLDATE
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 657766a838fbcd32c6b8bb0ba1f728e9dbbac92e103c219f3eeeab7ecd8c747d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749763"
---
# <a name="nulldate-er-function"></a>ฟังก์ชัน NULLDATE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NULLDATE` ส่งคืนค่า *Date* ที่แสดงถึงวันที่ **ที่เป็นแบบ null** (1 มกราคม 1900)

## <a name="syntax"></a>ไวยากรณ์

```vb
NULLDATE () as 
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่*

ค่าวันที่ที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` ส่งกลับวันที่ **ที่เป็น null** 1 มกราคม 1900 เป็น **"1900-01-01"** ตามรูปแบบที่กำหนดเองที่ระบุ

## <a name="example-2"></a>ตัวอย่างที่ 2

นิพจน์ `IF( Invoice.DocumentDate = NULLDATE(), true, false)` ส่งคืน **True** เมื่อค่าของฟิลด์ **DocumentDate** เท่ากับวันที่ **ที่เป็น null** ในตัวอย่างนี้ **Invoice** เป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ของชนิด **เรกคอร์ด Finance/Table** และอ้างอิงถึงตาราง CustInvoiceJour

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]