---
title: ฟังก์ชัน ADDDAYS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ADDDAYS
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 8877bf5a1b6c06e1a25fa9ddaca9c3b039bd2e4d01f39eea9065125977f73e9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740346"
---
# <a name="adddays-er-function"></a>ฟังก์ชัน ADDDAYS ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ADDDAYS` คำนวณค่า *DateTime* ที่เป็นจำนวนวันที่ระบุก่อนหรือหลังวันที่เริ่มต้นที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`datetime`: *DateTime*

ค่าวันที่/เวลาที่แสดงวันที่ที่เริ่มต้น

`days`: *จำนวนเต็ม*

จำนวนวันก่อนหรือหลัง `datetime`

## <a name="return-values"></a>ค่าที่ส่งคืน

*วันที่และเวลา*

ค่าวันที่/เวลาที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ค่าบวกสำหรับการทำให้เกิด `days` ในวันที่ในอนาคต ค่าลบจะให้ผลตอบแทนวันที่ผ่านมา

## <a name="example-1"></a>ตัวอย่างที่ 1

`ADDDAYS (NOW(), 7)` ส่งกลับวันและเวลาเจ็ดวันในอนาคต

## <a name="example-2"></a>ตัวอย่างที่ 2

`ADDDAYS (NOW(), -3)` ส่งกลับวันและเวลาสามวันในอดีต

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันวันที่และเวลา](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]