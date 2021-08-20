---
title: ฟังก์ชัน FA_SUM ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ FA_SUM (ER)
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 96b579cff1a61b8e1131317917ededb3b26963677e99da0e294501817cda26d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740322"
---
# <a name="fa_sum-er-function"></a>ฟังก์ชัน FA_SUM ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `FA_SUM` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดเงินสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า และรอบระยะเวลาของวันที่

## <a name="syntax"></a>ไวยากรณ์

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`fixed asset code`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสของรายการสินทรัพย์ถาวรที่มีการคำนวณยอดดุล

`value model code`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสของแบบจำลองค่าที่มีการคำนวณยอดดุล

`start date`: *วันที่*

ค่า *วันที่* แสดงถึงวันที่เริ่มต้นของรอบระยะเวลาที่มีการคำนวณยอดเงินสินทรัพย์ถาวร

`end date`: *วันที่*

ค่า *วันที่* แสดงถึงวันที่สิ้นสุดของรอบระยะเวลาที่มีการคำนวณยอดเงินสินทรัพย์ถาวร

## <a name="return-values"></a>ส่งคืนค่า

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` ส่งกลับค่าคอนเทนเนอร์ข้อมูลสำหรับสินทรัพย์ถาวร **COMP-000001** ที่เตรียมไว้สำหรับแบบจำลองค่า **ปัจจุบัน** และสำหรับรอบระยะเวลาตั้งแต่ **Date1** ถึง **Date2**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]