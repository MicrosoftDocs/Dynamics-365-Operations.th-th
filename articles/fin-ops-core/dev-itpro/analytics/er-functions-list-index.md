---
title: ฟังก์ชัน INDEX ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) INDEX
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
ms.openlocfilehash: a7fe2cbb5421da3c6dd1d044316b276836c5e5c1
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917315"
---
# <a name="INDEX">ฟังก์ชัน INDEX ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `INDEX` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เลือกโดยใช้ดัชนีตัวเลขที่ระบุในรายการที่ระบุ ถ้าดัชนีอยู่นอกช่วสำหรับเรกคอร์ดในรายการที่ระบุ จะมีข้อยกเว้นเกิดขึ้น

## <a name="syntax"></a>ไวยากรณ์

```
INDEX (list, index)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`index`: *เลขจำนวนเต็ม*

ดัชนีตัวเลขที่ระบุตำแหน่งของเรกคอร์ดที่ต้องการในรายการที่ระบุ

## <a name="return-values"></a>ค่าที่ส่งคืน

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิดของ *ฟิลด์ที่คำนวณได้* และมีนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `DS.Value` นิพจน์จะส่งคืนค่าข้อความ **B** สำหรับเรกคอร์ดที่สองของรายการเรกคอร์ดนี้ นิพจน์ `INDEX (SPLIT ("A|B|C", "|"), 2).Value` ยังส่งกลับค่าข้อความ **B** ด้วย

## <a name="example-2"></a>ตัวอย่างที่ 2

ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่คำนวณได้* และประกอบด้วยนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `INDEX (SPLIT ("A|B|C", "|"), 4).Value` จะมีข้อยกเว้นเกิดขึ้นขณะรันไทม์

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
