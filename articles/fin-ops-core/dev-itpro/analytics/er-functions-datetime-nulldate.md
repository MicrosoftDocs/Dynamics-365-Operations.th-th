---
title: ฟังก์ชัน NULLDATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NULLDATE
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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744298"
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
