---
title: ฟังก์ชัน JSONVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ JSONVALUE (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 11f9ac680ea00622367ea56106fd22508628d85d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685918"
---
# <a name="jsonvalue-er-function"></a>ฟังก์ชัน JSONVALUE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `JSONVALUE` แยกวิเคราะห์ข้อมูลในรูปแบบ JavaScript Object Notation (JSON) ที่เข้าถึงได้ที่พาธที่ระบุ และจะแยกค่าสเกลที่มีรหัสที่ระบุ จากนั้น จะส่งกลับค่าสเกลที่แยกเป็นค่า *สตริง*

## <a name="syntax"></a>ไวยากรณ์

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`input`: *สตริง*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง* ซึ่งมีข้อมูล JSON

`path`: *สตริง*

ตัวระบุของค่าสเกลของข้อมูล JSON

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

แหล่งข้อมูล **JsonField** ประกอบด้วยข้อมูลต่อไปนี้ในรูปแบบ: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}** ในกรณีนี้ นิพจน์ `JSONVALUE (JsonField, "BuildNumber")` ส่งกลับค่าต่อไปนี้ของชนิดข้อมูล *สตริง* : **"7.3.1234.1"**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]