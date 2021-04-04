---
title: ฟังก์ชัน DAYS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) DAYS
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0252a68aebaa9af95de561b88ceb0666b3460d79
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563497"
---
# <a name="days-er-function"></a>ฟังก์ชัน DAYS ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `DAYS` ส่งคืนค่าที่แสดง *จำนวนเต็ม* ที่แสดงจำนวนของวันระหว่างวันที่ที่ระบุที่หนึ่งกับวันที่ที่ระบุที่สอง

## <a name="syntax"></a>ไวยากรณ์

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>อาร์กิวเมนต์

`date 1`: *วันที่*

ค่าวันที่ที่แสดงถึงวันที่ที่จะใช้สำหรับการคำนวณจำนวนวัน

`date 2`: *วันที่*

ค่าวันที่ที่แสดงถึงวันที่สิ้นสุดที่จะใช้สำหรับการคำนวณจำนวนวัน

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนเต็ม*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชัน `DAYS` ส่งคืนค่าบวกเมื่อวันที่วันแรกเป็นวันที่หลังจากวันที่ที่สอง ส่งคืน **0** (ศูนย์) เมื่อวันที่วันแรกเท่ากับวันที่ที่สอง หรือส่งคืนค่าลบ เมื่อวันที่วันแรกเป็นวันที่ก่อนวันที่ที่สอง

## <a name="example"></a>ตัวอย่าง

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` ส่งคืน **-1**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]