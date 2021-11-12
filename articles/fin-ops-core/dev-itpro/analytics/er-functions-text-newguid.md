---
title: ฟังก์ชัน NEWGUID ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NEWGUID
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647960"
---
# <a name="newguid-er-function"></a>ฟังก์ชัน NEWGUID ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NEWGUID` จะสร้างรหัสเฉพาะสากลใหม่ (GUID) และส่งคืนเป็นค่า *[GUID](er-formula-supported-data-types-primitive.md#guid)*

## <a name="syntax"></a>ไวยากรณ์

```vb
NEWGUID ()
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*GUID*

ค่า GUID ที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`NEWGUID()` จะส่งคืนค่า *GUID* ใหม่เสมอ เช่น **3afcf7ff-af10-ec11-b6e6-000d3a13209e**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
