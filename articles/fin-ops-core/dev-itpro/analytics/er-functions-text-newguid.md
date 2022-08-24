---
title: ฟังก์ชัน NEWGUID ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NEWGUID
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274786"
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
