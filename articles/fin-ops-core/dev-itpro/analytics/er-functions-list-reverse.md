---
title: ฟังก์ชัน REVERSE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) REVERSE
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 895d5f13f065b2188f245d081fa69e7e63555dde
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686451"
---
# <a name="reverse-er-function"></a>ฟังก์ชัน REVERSE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `REVERSE` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* ในลำดับการจัดเรียงแบบย้อนกลับ

## <a name="syntax"></a>ไวยากรณ์

```vb
REVERSE (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="example-1"></a>ตัวอย่างที่ 1

ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("C|B|A", "|")` นิพจน์ `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` จะส่งกลับค่าข้อความ **C**

## <a name="example-2"></a>ตัวอย่างที่ 2

ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ที่อ้างอิงถึงตาราง VendTable นิพจน์ `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` จะส่งกลับรายการของผู้จัดจำหน่ายที่เรียงลำดับตามชื่อในลำดับจากมากไปน้อย

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
