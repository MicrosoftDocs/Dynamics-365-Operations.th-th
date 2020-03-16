---
title: ฟังก์ชัน NUMBERFORMAT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMBERFORMAT (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070563"
---
# <a name="NUMBERFORMAT">ฟังก์ชัน NUMBERFORMAT ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NUMBERFORMAT` ส่งกลับค่า *สตริง* ที่แสดงหมายเลขที่ระบุในรูปแบบที่ระบุและใน [ภาษา](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) ที่ระบุเป็นทางเลือก สำหรับข้อมูลเกี่ยวกับรูปแบบที่สนับสนุน ดู [มาตรฐาน](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) และ [กำหนดเอง](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx)

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*

ค่าตัวเลขที่ระบุหมายเลขที่ต้องถูกจัดรูปแบบ

`format` : *สตริง*

ค่า *สตริง* ที่แสดงถึงรูปแบบ

`culture`: *สตริง*

ค่า *สตริง* ที่แสดงถึงภาษาที่จะใช้สำหรับการจัดรูปแบบ

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ถ้าภาษาไม่ได้ถูกกำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันที่ถูกเรียก บริบทที่มีการเรียกใช้ฟังก์ชันนี้จะกำหนดภาษาที่ใช้ในการจัดรูปแบบตัวเลข

## <a name="example-1"></a>ตัวอย่างที่ 1

สำหรับภาษา **EN-US** `NUMBERFORMAT (0.45, "p")` ส่งกลับค่า **"45.00 %"** และ `NUMBERFORMAT (10.45, "#")` ส่งกลับค่า **"10"**

## <a name="example-2"></a>ตัวอย่างที่ 2

`NUMBERFORMAT (10/3, "F2", "de")` ส่งกลับค่า **3,33** ในขณะที่ `NUMBERFORMAT (10/3, "F2", "en-us")` ส่งกลับค่า **3.33**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)
