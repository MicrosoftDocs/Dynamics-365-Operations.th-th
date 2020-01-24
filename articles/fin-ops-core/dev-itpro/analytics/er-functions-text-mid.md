---
title: ฟังก์ชัน MID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ MID (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915613"
---
# <a name="MID">ฟังก์ชัน MID ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `MID` ส่งกลับค่า *สตริง* ที่แสดงจำนวนอักขระที่ระบุจากสตริงที่ระบุซึ่งเริ่มต้นที่ตำแหน่งที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```
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
