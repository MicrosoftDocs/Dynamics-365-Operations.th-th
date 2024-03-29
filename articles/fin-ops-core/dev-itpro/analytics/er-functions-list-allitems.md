---
title: ฟังก์ชัน ALLITEMS ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ALLITEMS
author: kfend
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: bb469955c66baf875eea80dde8199986e69e2e71
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274123"
---
# <a name="allitems-er-function"></a>ฟังก์ชัน ALLITEMS ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ALLITEMS` จะทำงานเป็นตัวเลือกในหน่วยความจำและส่งกลับ *ค่ารายการ* ที่ยุบใหม่ที่เป็นรายการของเรกคอร์ดที่แสดงถึงรายการทั้งหมดที่ตรงกับพาธที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`path`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ต้องกำหนดพาธเป็นพาธแหล่งข้อมูลที่ถูกต้องขององค์ประกอบแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* องค์ประกอบข้อมูล เช่น สตริงพาธ และวันที่ควรรายงานข้อผิดพลาดในตัวสร้างนิพจน์ การรายงานทางอิเล็กทรอนิกส์ (ER) ในขณะที่ออกแบบ

เราไม่แนะนำให้คุณใช้ฟังก์ชันนี้สำหรับแหล่งข้อมูลธุรกรรมที่อาจมีข้อมูลจำนวนมาก ให้พิจารณาใช้ฟังก์ชัน [ALLTEMSQUERY](er-functions-list-allitemsquery.md) แทน

## <a name="example-1"></a>ตัวอย่างที่ 1

ถ้าคุณป้อน `SPLIT("abcdef" , 2)` เป็นแหล่งข้อมูล **DS** นิพจน์ `COUNT( ALLITEMS (DS))` จะส่งกลับค่า **3**

## <a name="example-2"></a>ตัวอย่างที่ 2

ถ้าคุณป้อน **Vend** เป็นแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* ที่อ้างอิงถึงตารางโปรแกรมประยุกต์ นิพจน์ `ALLITEMS (Vend.'<Relations'.ContactPerson)` จะส่งกลับรายการเรกคอร์ดที่ปรับเป็นระนาบที่มีโครงสร้างตาราง **ContactPerson** และประกอบด้วยบุคคลที่ติดต่อทั้งหมดที่สามารถเข้าถึงได้โดยใช้ **ContactPerson.ContactForParty == VendTable.Party** ที่เกี่ยวข้องกันและที่พร้อมใช้งานสำหรับผู้จัดจำหน่ายทั้งหมดจากตารางผู้ขายที่อ้างอิง

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
