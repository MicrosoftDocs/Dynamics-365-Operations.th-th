---
title: ฟังก์ชัน ISOCREDREF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ISOCREDREF (ER)
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
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680697"
---
# <a name="isocredref-er-function"></a>ฟังก์ชัน ISOCREDREF ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ISOCREDREF` ส่งคืนค่า *สตริง* ที่แสดงการอ้างอิงเจ้าหนี้ขององค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) โดยขึ้นอยู่กับตำแหน่งและสัญลักษณ์เรียงตามลำดับอักษรของหมายเลขใบแจ้งหนี้ที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`invoice number digits`: *สตริง*

ค่าของข้อความที่แสดงตัวเลขของหมายเลขใบแจ้งหนี้

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

> [!NOTE] 
> เพื่อขจัดสัญลักษณ์จากอักษรที่ไม่สอดคล้องกับ ISO อาร์กิวเมนต์ `invoice number digits` จะต้องถูกแปลก่อนที่จะมีการส่งผ่านไปยังฟังก์ชันนี้

## <a name="example"></a>ตัวอย่าง

`ISOCredRef ("VEND-200002")` ส่งคืน **"RF23VEND-200002"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]