---
title: ฟังก์ชัน TRIM ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TRIM (ER)
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c95663f1aacaf93c1c4bfc8d36d9515f495bf61e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040836"
---
# <a name="TRIM">ฟังก์ชัน TRIM ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `TRIM` ส่งคืนสตริงข้อความที่ระบุเป็นค่า *สตริง* หลังจากช่องว่างนำหน้าและต่อท้ายถูกตัดออกแล้ว และหลังจากที่ได้ลบช่องว่างหลายช่องระหว่างคำ

## <a name="syntax"></a>ไวยากรณ์

```vb
TRIM (text )
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` ส่งกลับ **"ข้อความตัวอย่าง"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
