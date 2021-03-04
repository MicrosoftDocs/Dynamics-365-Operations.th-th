---
title: ฟังก์ชัน FIRSTORNULL ER
description: หัวข้อนี้อธิบายข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FIRSTORNULL
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 3547eeea3c6fef5cca0699002cc0c35cffd940b3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688054"
---
# <a name="firstornull-er-function"></a>ฟังก์ชัน FIRSTORNULL ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `FIRSTORNULL` ส่งกลับเรกคอร์ดแรกของรายการที่ระบุเป็นค่า *คอนเทนเนอร์ (เรกคอร์ด)* หากเรกคอร์ดไม่ว่าง ถ้าเรกคอร์ดว่าง ฟังก์ชันนี้จะส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null

## <a name="syntax"></a>ไวยากรณ์

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

## <a name="return-values"></a>ค่าที่ส่งคืน

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

นิพจน์ `FIRSTORNULL(SPLIT("",1)).Value` ส่งกลับสตริงที่ว่างเปล่า (**""**)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]