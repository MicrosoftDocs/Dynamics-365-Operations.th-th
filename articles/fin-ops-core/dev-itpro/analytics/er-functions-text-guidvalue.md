---
title: ฟังก์ชัน GUIDVALUE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GUIDVALUE (ER)
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: cb706a3607b4443c283a91c42c4dc1c389972e44
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285199"
---
# <a name="guidvalue-er-function"></a>ฟังก์ชัน GUIDVALUE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `GUIDVALUE` แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *GUID*

## <a name="syntax"></a>ไวยากรณ์

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`input`: *สตริง*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*

## <a name="return-values"></a>ส่งคืนค่า

*GUID*

ค่าตัวระบุที่ไม่ซ้ำกันส่วนกลาง (GUID) ที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

เพื่อทำการแปลงในทิศทางตรงกันข้าม (นั่นคือ การแปลงระบุข้อมูลป้อนเข้าที่ระบุของชนิดข้อมูล *GUID* เป็นรายการข้อมูลของชนิดข้อมูล *สตริง*) คุณสามารถใช้ฟังก์ชัน [TEXT](er-functions-text-text.md) ได้

## <a name="example"></a>ตัวอย่าง

คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:

- แหล่งข้อมูล **myID** ของชนิด *ฟิลด์ที่มีการคำนวณ* ที่มีนิพจน์`GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- แหล่งข้อมูล **ผู้ใช้** ของชนิด *เรกคอร์ดของตาราง* ที่อ้างอิงถึงตาราง UserInfo

จากนั้นคุณสามารถใช้นิพจน์ เช่น `FILTER (Users, Users.objectId = myID)` เพื่อกรองตาราง UserInfo โดยฟิลด์ **objectId** ของชนิดข้อมูล *GUID*

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
