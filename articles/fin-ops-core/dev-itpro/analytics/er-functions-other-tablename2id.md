---
title: ฟังก์ชัน TABLENAME2ID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TABLENAME2ID (ER)
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563281"
---
# <a name="tablename2id-er-function"></a>ฟังก์ชัน TABLENAME2ID ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `TABLENAME2ID` ส่งกลับการแสดงตัวเลขของรหัสตารางสำหรับชื่อตารางที่ระบุเป็นค่า *จำนวนเต็ม*

## <a name="syntax"></a>ไวยากรณ์

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่าข้อความที่แสดงชื่อตารางที่ถูกต้อง

## <a name="return-values"></a>ส่งคืนค่า

*จำนวนเต็ม*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

การดำเนินการของฟังก์ชันนี้สามารถมีผลลัพธ์ที่แตกต่างกันในอินสแตนซ์ต่างๆ ของ Microsoft Dynamics 365 Finance แม้ว่าจะมีการใช้ชื่อบริษัทเดียวกัน

## <a name="example"></a>ตัวอย่าง

`TABLENAME2ID ("Intrastat")` ส่งกลับค่า **1510**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]