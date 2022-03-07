---
title: ฟังก์ชัน FIRST ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FIRST
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564746"
---
# <a name="first-er-function"></a>ฟังก์ชัน FIRST ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `FIRST` ส่งกลับเรกคอร์ดแรกของรายการที่ระบุเป็นค่า *คอนเทนเนอร์ (เรกคอร์ด)* หากรายการนั้นไม่ว่าง ถ้ารายการว่าง ฟังก์ชันนี้จะแสดงข้อยกเว้น

## <a name="syntax"></a>ไวยากรณ์

```vb
FIRST (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

## <a name="return-values"></a>ค่าที่ส่งคืน

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

นิพจน์ `FIRST(SPLIT("ABC",1)).Value` ส่งกลับค่าข้อความ **"A"**

## <a name="example-2"></a>ตัวอย่างที่ 2

นิพจน์ `FIRST(SPLIT("",1)).Value`แสดงข้อยกเว้นขณะรันไทม์

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]