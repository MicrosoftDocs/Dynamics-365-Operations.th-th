---
title: ฟังก์ชัน ER EMPTYLIST
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) EMPTYLIST
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
ms.openlocfilehash: ccb52d7d88f292720360ae913ead5be239165193
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687681"
---
# <a name="emptylist-er-function"></a>ฟังก์ชัน ER EMPTYLIST

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `EMPTYLIST` ส่งคืนค่า *รายการเรกคอร์ด* ที่ว่างเปล่าโดยใช้รายการที่ระบุเป็นแหล่งข้อมูลสำหรับโครงสร้างรายการ

## <a name="syntax"></a>ไวยากรณ์

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="example"></a>ตัวอย่าง

`EMPTYLIST (SPLIT ("abc", 1))` ส่งคืนรายการที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT` ที่ใช้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]