---
title: ฟังก์ชัน ROUND ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUND
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041618"
---
# <a name="ROUND">ฟังก์ชัน ROUND ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ROUND` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษเป็นจำนวนทศนิยมที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จริง*

ค่าตัวเลขที่ต้องถูกปัดเศษ

`decimals`: *จำนวนเต็ม*

ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ถ้าค่าของพารามิเตอร์อาร์กิวเมนต์ `decimals` มากกว่า 0 (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนทศนิยมหลายตำแหน่ง

ถ้าค่าของอาร์กิวเมนต์ `decimals` เป็น **0** (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนเต็มที่ใกล้เคียงที่สุด

ถ้าค่าของอาร์กิวเมนต์ `decimals` น้อยกว่า 0 (ศูนย์) หมายเลขที่ระบุจะถูกปัดเศษเป็นจำนวนทศนิยมปัดขึ้น

## <a name="example-1"></a>ตัวอย่างที่ 1

`ROUND (1200.767, 2)` ปัดเศษเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.77**

## <a name="example-2"></a>ตัวอย่างที่ 2

`ROUND (1200.767, -3)` ปัดเศษเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **1000**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันคณิตศาสตร์](er-functions-category-mathematical.md)
