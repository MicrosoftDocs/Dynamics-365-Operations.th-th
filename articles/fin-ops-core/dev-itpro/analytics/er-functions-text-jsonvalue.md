---
title: ฟังก์ชัน JSONVALUE ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) JSONVALUE
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267994"
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

ตัวระบุของค่าสเกลของข้อมูล JSON ใช้เครื่องหมายทับ (/) เพื่อแยกชื่อของโหนด JSON ที่เกี่ยวข้อง ใช้เครื่องหมายวงเล็บ (\[\]) เพื่อระบุดัชนีของค่าหนึ่งๆ ในอาเรย์ JSON โปรดทราบว่ามีการใช้การหมายเลขตามศูนย์กับดัชนีนี้

## <a name="return-values"></a>ค่าที่ส่งคืน

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example-1"></a>ตัวอย่างที่ 1

แหล่งข้อมูล **JsonField** ประกอบด้วยข้อมูลต่อไปนี้ในรูปแบบ: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}** ในกรณีนี้ นิพจน์ `JSONVALUE (JsonField, "BuildNumber")` ส่งกลับค่าต่อไปนี้ของชนิดข้อมูล *สตริง* : **"7.3.1234.1"**

## <a name="example-2"></a>ตัวอย่างที่ 2

แหล่งข้อมูล **JsonField** ของชนิด *ฟิลด์ที่มีการคำนวณ* ประกอบด้วยนิพจน์ต่อไปนี้ `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

นิพจน์นี้ตั้งค่าคอนฟิกให้ส่งคืนค่า [*สตริง*](er-formula-supported-data-types-primitive.md#string) ที่แสดงถึงข้อมูลต่อไปนี้ในรูปแบบ JSON

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

ในกรณีนี้ นิพจน์ `JSONVALUE(json, "workers/[1]/emails/[0]")` ส่งคืนค่าต่อไปนี้ของชนิดข้อมูล *สตริง*: `JohnS@Contoso.com`

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
