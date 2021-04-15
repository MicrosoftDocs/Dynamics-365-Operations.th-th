---
title: ฟังก์ชัน NULLDATETIME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NULLDATETIME
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: f7282b7c161b6e183186ba81e6bcf7b34ce6e612
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746830"
---
# <a name="nulldatetime-er-function"></a>ฟังก์ชัน NULLDATETIME ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NULLDATETIME` ส่งกลับค่า *DateTime* ที่แสดงค่าวัน/เวลา **ที่เป็น null** (1 มกราคม 1900) ในเวลาสากลที่สอดคล้องกัน (เวลามาตรฐานกรีนิช \[GMT\])

## <a name="syntax"></a>ไวยากรณ์

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่และเวลา*

ค่าวันที่/เวลาที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`DATETIMEFORMAT( NULLDATETIME(), "O")` ส่งกลับค่าสตริง **1900-01-01T00:00:00.0000000+00:00** ที่ถูกเรียกในระหว่างกระบวนการที่เริ่มต้นโดยผู้ใช้แอปพลิเคชันที่มีเวลาโซนเวลา **เวลามาตรฐานสากล (GMT)** ในส่วน **การกำหนดลักษณะภาษาและประเทศ/ภูมิภาค**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]