---
title: ฟังก์ชัน LIST ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LIST
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
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917292"
---
# <a name="LIST">ฟังก์ชัน LIST ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `LIST` ส่งกลับค่า *รายการเรกคอร์ด* ที่ประกอบด้วยรายการใหม่ของเรกคอร์ดที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด

## <a name="syntax"></a>ไวยากรณ์

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`record 1`: *คอนเทนเนอร์ (เรกคอร์ด)*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *เรกคอร์ด* ต้องระบุอาร์กิวเมนต์นี้

`record N`: *คอนเทนเนอร์ (เรกคอร์ด)*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *เรกคอร์ด* อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

โครงสร้างของรายการที่สร้างขึ้นมีเฉพาะฟิลด์ที่ถูกนำเสนอในโครงสร้างของเรกคอร์ดทั้งหมดที่กล่าวถึงในอาร์กิวเมนต์

## <a name="example"></a>ตัวอย่าง

คุณป้อนเรกคอร์ดแหล่งข้อมูล **เรกคอร์ด 1** ของชนิดของ *คอนเทนเนอร์* แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด *ฟิลด์ที่คำนวณได้*

- **รหัส:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *สตริง*
- **จำนวน:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *จำนวนจริง*

จากนั้นให้คุณป้อนแหล่งข้อมูล **เรกคอร์ด 2** ของชนิดของ *คอนเทนเนอร์* แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิด *ฟิลด์ที่คำนวณได้*

- **จำนวน:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *จำนวนจริง*
- **IsValid:** ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด *บูลีน*

ในกรณีนี้นิพจน์ `LIST('Record 1', 'Record 2')` ส่งกลับรายการใหม่ที่ประกอบด้วยสองเรกคอร์ด โครงสร้างของรายการนี้ประกอบด้วยฟิลด์ **ยอดเงิน** ของชนิด *จำนวนจริง* เนื่องจากฟิลด์นี้เป็นฟิลด์เดียวที่จะแสดงในทุกอาร์กิวเมนต์ของฟังก์ชันที่เรียก

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
