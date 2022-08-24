---
title: ฟังก์ชัน MOD_97 ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) MOD_97
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
ms.openlocfilehash: 55d2bce660186f10fc48e29f5cf03385a778a57a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285229"
---
# <a name="mod_97-er-function"></a>ฟังก์ชัน MOD_97 ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `MOD_97` ส่งกลับค่า *สตริง* ที่แสดงถึงการอ้างอิงของเจ้าหนี้เป็นนิพจน์ MOD97 ตามตัวเลขของหมายเลขใบแจ้งหนี้ที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`invoice number digits`: *สตริง*

ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`MOD_97 ("VEND-200002")` ส่งคืน **"20000285"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
