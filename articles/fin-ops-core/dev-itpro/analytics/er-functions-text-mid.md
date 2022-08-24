---
title: ฟังก์ชัน MID ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ MID (ER)
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c53963876db92bb07ed5ac49f009ed4f9bc5e8c4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285923"
---
# <a name="mid-er-function"></a>ฟังก์ชัน MID ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `MID` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากสตริงที่ระบุซึ่งเริ่มต้นที่ตำแหน่งที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่า *สตริง* ที่ระบุข้อความที่จะส่งกลับอักขระ

`starting position`: *เลขจำนวนเต็ม*

ค่า *เลขจำนวนเต็ม* ที่ระบุตำแหน่งของอักขระตัวแรกที่ต้องถูกส่งกลับจากข้อความที่ระบุ

`number of characters`: *เลขจำนวนเต็ม*

ค่า *เลขจำนวนเต็ม* ที่ระบุจำนวนของอักขระที่ต้องถูกส่งกลับ ซึ่งเริ่มต้นที่ตำแหน่งเริ่มต้นที่ระบุ

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ถ้าค่าของอาร์กิวเมนต์ `starting position` น้อยกว่า 0 (ศูนย์) อักขระที่ถูกส่งกลับจะถูกนับจากตำแหน่งแรกในสตริงที่ระบุ

ถ้าค่าของอาร์กิวเมนต์ `starting position` เกินความยาวของสตริงที่ระบุ สตริงที่ว่างจะถูกส่งกลับ

## <a name="example"></a>ตัวอย่าง

`MID ("Sample", 2, 3)`ส่งกลับค่า **"amp"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
