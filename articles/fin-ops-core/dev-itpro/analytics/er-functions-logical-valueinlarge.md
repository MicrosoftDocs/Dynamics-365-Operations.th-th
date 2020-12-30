---
title: ฟังก์ชัน VALUEINLARGE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) VALUEINLARGE
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 26a7148a4caa80a191688145bac625bdf0bf83b2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686917"
---
# <a name="valueinlarge-er-function"></a>ฟังก์ชัน VALUEINLARGE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `VALUEINLARGE` กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่า *Int64* หรือ *Integer* ใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่ ฟังก์ชันนี้จะส่งกลับค่า *แบบบูลีน* ของ **TRUE** ถ้าข้อมูลที่ป้อนที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ** เพื่อทำความเข้าใจความแตกต่างของฟังก์ชัน `VALUEIN` ดูที่ส่วน [หมายเหตุการใช้งาน](#usage_note) ที่อยู่ต่อไปในหัวข้อนี้

## <a name="syntax"></a>ไวยากรณ์

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`input`: *ฟิลด์*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิด *รายการเรกคอร์ด* ค่าของรายการนี้จะถูกจับคู่กัน

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`list item expression`: *นิพจน์*

นิพจน์ที่มีเงื่อนไขที่ถูกต้องที่ชี้ไป หรือประกอบด้วยฟิลด์เดียวของรายการที่ระบุที่ควรจะใช้สำหรับการจับคู่กัน

## <a name="return-values"></a>ค่าที่ส่งคืน

*บูลีน*

ค่า *บูลีน* ที่เป็นผลลัพธ์

## <a name=""></a><a name="usage_note">บันทึกย่อการใช้งาน</a>

เมื่อข้อมูลที่ป้อนที่ระบุแสดงชนิด *Int64* หรือ *Integer* ของรายการแหล่งข้อมูล จะมีการเรียกไปยังรายการที่แปลได้กับคำสั่ง SQL โดยตรง รายการที่ระบุจะถูกแปลงเป็นตาราง SQL ชั่วคราวและมีการดำเนินการจับคู่ในฐานข้อมูลโดยดำเนินการสอบถาม `EXISTS JOIN` เดียว หรือไม่ฟังก์ชันนี้จะทำงานเป็นฟังก์ชัน [`VALUEIN`](er-functions-logical-valuein.md)

เมื่อข้อมูลที่ป้อนที่ระบุแสดงรายการแหล่งข้อมูลที่ได้รับการออกแบบเป็นรายการอื่นที่ไม่ใช่ชนิด *Int64* และ *Integer* จะเกิดข้อผิดพลาดในเวลาที่ออกแบบเพื่อแจ้งให้คุณทราบว่าฟังก์ชัน `VALUEINLARGE` ไม่สามารถใช้ได้กับนิพจน์ ER ที่ตั้งค่าคอนฟิกไว้

เมื่อนิพจน์ฟังก์ชัน `VALUEINLARGE` ดำเนินการและมีการใช้ตารางชั่วคราวมากกว่าหนึ่งตารางในขอบเขตของการดำเนินการนี้ จะเกิดข้อผิดพลาดรันไทม์ขึ้น

## <a name="example"></a>ตัวอย่าง

คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:

- แหล่งข้อมูล **In** ของชนิด *เรกคอร์ดตาราง*
    - แหล่งข้อมูลนี้อ้างถึงตาราง **อินทราสแทต**
    - ตัวเลือก **ข้ามบริษัท** ตั้งค่าเป็น **ไม่**
- แหล่งข้อมูล **InMemory** ของชนิดของ *ฟิลด์ที่คำนวณได้*
    - แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `WHERE (In, In.Port <> "")`
- แหล่งข้อมูล **InFiltered** ของชนิดของ *ฟิลด์ที่คำนวณได้*
    - แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`

เมื่อมีการเรียกแหล่งข้อมูล **InFiltered** ภายใต้บริบทของบริษัท **DEMF** จะมีการสร้างตารางชั่วคราวใหม่ในฐานข้อมูลแอปพลิเคชัน รายการที่รวบรวมไว้ในรายการหน่วยความจำของรหัสการระบุเรกคอร์ดจะถูกแทรกลงในตารางนี้ และมีการสร้างคำสั่ง SQL ต่อไปนี้เพื่อส่งกลับเรกคอร์ดที่กรองของตาราง **อินทราสแทต**

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันตรรกะ](er-functions-category-logical.md)

[ฟังก์ชัน VALUEIN](er-functions-logical-valuein.md)
