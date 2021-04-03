---
title: ฟังก์ชั่น STRINGJOIN ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) STRINGJOIN
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
ms.openlocfilehash: 755e6481abb65dfecc8ddb6bceb032c8110095e2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568181"
---
# <a name="stringjoin-er-function"></a>ฟังก์ชั่น STRINGJOIN ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `STRINGJOIN` ส่งคืนค่า *สตริง* ที่ประกอบด้วยค่าที่ต่อกันของฟิลด์ที่ระบุจากรายการที่ระบุ ค่าสามารถถูกแบ่งด้วยตัวคั่นที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`field`: *ฟิลด์*

เส้นทางที่ถูกต้องของเขตข้อมูลของชนิดข้อมูล *สตริง* ในรายการที่ระบุ

`delimiter`: *สตริง*

ตัวคั่นที่ใช้ในการแยกสตริงย่อย

## <a name="return-values"></a>ค่าที่ส่งคืน

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

ถ้าคุณป้อน `SPLIT("abc" , 1)` เป็นแหล่งข้อมูล **DS** นิพจน์`STRINGJOIN (DS, DS.Value, "-")` จะส่งกลับค่า **"a-b-c"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]