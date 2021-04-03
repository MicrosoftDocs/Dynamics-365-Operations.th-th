---
title: ฟังก์ชัน MID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ MID (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e0520bc54465f00d36e88787933b291847dee852
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562744"
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