---
title: ฟังก์ชัน ENUMERATE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ENUMERATE
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
ms.openlocfilehash: adaa2582e6dced428cf1f15a235ecbfd036362e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273262"
---
# <a name="enumerate-er-function"></a>ฟังก์ชัน ENUMERATE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ENUMERATE` ส่งกลับค่า *รายการเรกคอร์ด* ใหม่ที่ประกอบด้วยเฉพาะเรกคอร์ดที่ระบุรายการที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

รายการของเรกคอร์ดที่ระบุที่ถูกส่งกลับแสดงองค์ประกอบเพิ่มเติมต่อไปนี้:

- เรกคอร์ดของฟิลด์ส่วนประกอบ (**ค่า**)
- ดัชนีเรกคอร์ดปัจจุบัน (คอมโพเนนต์ **หมายเลข**)

## <a name="example"></a>ตัวอย่าง

ในแผนภาพต่อไปนี้ แหล่งข้อมูล **ที่ระบุ** ถูกสร้างเป็นรายการที่ระบุของเรกคอร์ดผู้จัดจำหน่ายจากแหล่งข้อมูล **ผู้จัดจำหน่าย** ที่อ้างอิงถึงตาราง VendTable

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

ภาพประกอบต่อไปนี้แสดงรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ในรูปแบบนี้ การผูกข้อมูลถูกสร้างเพื่อสร้างเอาท์พุทในรูปแบบ XML เอาท์พุทนี้แสดงผู้จัดจำหน่ายแต่ละรายเป็นโหนดที่ระบุ

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการออกแบบ

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
