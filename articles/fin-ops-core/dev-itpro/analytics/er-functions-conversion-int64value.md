---
title: ฟังก์ชัน INT64VALUE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ INT64VALUE (ER)
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 37fae9cdc5a833009b0ca1cbeb851e5e6e1b6608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892177"
---
# <a name="int64value-er-function"></a>ฟังก์ชัน INT64VALUE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `INT64VALUE` ส่งกลับค่า *Int64* ที่แสดงถึงสตริงที่ระบุ

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่าข้อความต้องถูกแปลงเป็นหมายเลย *Int64*

`number`: *จำนวนจริง* หรือ *จำนวนเต็ม*

ค่า *จำนวนจริง* or *จำนวนเต็ม* ที่เป็นตัวเลขต้องถูกแปลงเป็นหมายเลย *Int64*

## <a name="return-values"></a>ค่าที่ส่งคืน

*Int64*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ตำแหน่งทศนิยมใดๆ จะถูกตัดออก

## <a name="example-1"></a>ตัวอย่างที่ 1

`INT64VALUE ("22565422744")` ส่งกลับค่า *Int64* **22565422744**

## <a name="example-2"></a>ตัวอย่างที่ 2

`INT64VALUE ( VALUE("22565422744.77"))` ส่งกลับค่า *Int64* **22565422744**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันการแปลงของชนิด](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]