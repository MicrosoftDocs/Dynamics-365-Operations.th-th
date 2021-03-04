---
title: ฟังก์ชัน ROUNDDOWN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ROUNDDOWN
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686893"
---
# <a name="rounddown-er-function"></a>ฟังก์ชัน ROUNDDOWN ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ROUNDDOWN` ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษลงเป็นจำนวนทศนิยมที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จริง*

ค่าตัวเลขที่ต้องถูกปัดเศษลง

`decimals`: *จำนวนเต็ม*

ค่าของข้อความที่แสดงจำนวนของตำแหน่งทศนิยม

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชันนี้ทำหน้าที่เหมือนกับ [ปัดเศษ](er-functions-mathematical-round.md) แต่จะปัดเศษจำนวนที่ระบุลงเสมอ (ไปยังศูนย์)

## <a name="example-1"></a>ตัวอย่างที่ 1

`ROUNDDOWN (1200.767, 2)` ปัดเศษลงเป็นทศนิยมสองตำแหน่ง และส่งกลับ **1200.76** 

## <a name="example-2"></a>ตัวอย่างที่ 2

`ROUNDDOWN (1700.767, -3)` ปัดเศษลงเป็นผลคูณที่ใกล้ที่สุดของ 1,000 และส่งกลับ **1000**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันคณิตศาสตร์](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]