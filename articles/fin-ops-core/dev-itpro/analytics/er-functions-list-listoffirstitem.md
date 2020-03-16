---
title: ฟังก์ชัน ER LISTOFFIRSTITEM
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTOFFIRSTITEM
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041986"
---
# <a name="LISTOFFIRSTITEM">ฟังก์ชัน ER LISTOFFIRSTITEM</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `LISTOFFIRSTITEM` ส่งกลับค่า *รายการเรกคอร์ด* ที่ประกอบด้วยเฉพาะเรกคอร์ดแรกของรายการที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="example"></a>ตัวอย่าง

นิพจน์ `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` ส่งกลับค่าข้อความ **"A"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
