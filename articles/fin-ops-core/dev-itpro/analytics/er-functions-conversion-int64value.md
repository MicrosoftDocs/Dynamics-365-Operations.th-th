---
title: ฟังก์ชัน INT64VALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) INT64VALUE
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916556"
---
# <a name="INT64VALUE">ฟังก์ชัน INT64VALUE ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `INT64VALUE` ส่งกลับค่า *Int64* ที่แสดงถึงสตริงที่ระบุ

## <a name="syntax-1"></a>ไวยากรณ์ 1

```
INT64VALUE (text)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```
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
