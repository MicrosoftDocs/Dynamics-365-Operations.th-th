---
title: ฟังก์ชัน FA_BALANCE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ FA_BALANCE (ER)
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f9bb52643b60fd1b9423d798c08d731565c70f81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285259"
---
# <a name="fa_balance-er-function"></a>ฟังก์ชัน FA_BALANCE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `FA_BALANCE` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดดุลสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า ปีการรายงาน และวันที่ที่รายงาน

## <a name="syntax"></a>ไวยากรณ์

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`fixed asset code`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสของรายการสินทรัพย์ถาวรที่มีการคำนวณยอดดุล

`value model code`: *สตริง*

ค่า *สตริง* ที่แสดงถึงรหัสของแบบจำลองค่าที่มีการคำนวณยอดดุล

`reporting year`: *ค่าการแจงนับ*

ค่าการแจงนับของการแจงนับแอพลิเคชัน **AssetYear** ที่กำหนดรอบระยะเวลาสำหรับการคำนวณยอดดุล

`reporting date`: *วันที่*

ค่า *วันที่* ที่กำหนดวันที่สำหรับการคำนวณยอดดุล

## <a name="return-values"></a>ส่งคืนค่า

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` ส่งคืนคอนเทนเนอร์ข้อมูลของยอดดุลสำหรับ สินทรัพย์ถาวร **COMP-000001** ที่มีการเตรียมไว้สำหรับแบบจำลองมูลค่า **ปัจจุบัน** ในวันที่รอบเวลาของแอพลิเคชันปัจจุบัน

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
