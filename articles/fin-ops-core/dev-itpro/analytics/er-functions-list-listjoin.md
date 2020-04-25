---
title: ฟังก์ชัน LISTJOIN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTJOIN
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249046"
---
# <a name=""></a><a name="LISTJOIN">ฟังก์ชัน LISTJOIN ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `LISTJOIN` ส่งกลับค่า *รายการเรกคอร์ด* ที่แสดงรายการเข้าร่วมใหม่ของเรกคอร์ดที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด

## <a name="syntax"></a>ไวยากรณ์

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list 1`: *รายการเรกคอร์ด*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* อาร์กิวเมนต์นี้เป็นข้อบังคับ

`list N`: *รายการเรกคอร์ด*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

โครงสร้างของรายการที่สร้างขึ้นมีเฉพาะฟิลด์ที่แสดงในโครงสร้างของรายการเรกคอร์ดทั้งหมดที่มีการอ้างถึงในอาร์กิวเมนต์

## <a name="example"></a>ตัวอย่าง

คุณป้อนแหล่งข้อมูล **เรกคอร์ด 1** ของชนิดของ `Container` แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:

- **Code**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `String`
- **Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`

จากนั้นคุณป้อนแหล่งข้อมูล **เรกคอร์ด 2** ของชนิดของ `Container` แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:

- **Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`
- **IsValid**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Boolean`

ในกรณีนี้นิพจน์ `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` ส่งกลับรายการใหม่ที่ประกอบด้วยสองเรกคอร์ด โครงสร้างของรายการนี้ประกอบด้วยฟิลด์ **ยอดเงิน** เดียวของชนิด `Real` เนื่องจากฟิลด์นี้เป็นฟิลด์เดียวที่จะแสดงในทุกอาร์กิวเมนต์ของฟังก์ชันที่เรียก

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
