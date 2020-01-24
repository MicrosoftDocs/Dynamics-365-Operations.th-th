---
title: ฟังก์ชัน PADLEFT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ PADLEFT (ER)
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
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916786"
---
# <a name="PADLEFT">ฟังก์ชัน PADLEFT ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `PADLEFT` ส่งคืนค่า *สตริง* ของความยาวที่ระบุ ซึ่งมีการเริ่มต้นสตริงที่ระบุด้วยอักขระที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่า *สตริง* ที่แสดงถึงข้อความต้นฉบับ

`length`: *เลขจำนวนเต็ม*

ค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนสุดท้ายของอักขระในสตริงที่ระบุ

`padding chars`: *สตริง*

อักขระที่จะใช้สำหรับการระบุ

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`PADLEFT ("1234", 10, "`&nbsp;`")` ส่งคืนสตริงข้อความ **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
