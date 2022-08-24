---
title: ฟังก์ชัน NULLDATE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NULLDATE
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 276ad99303a4e88ecb1c83e9518e06bfd7afaa45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272666"
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
