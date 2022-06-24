---
title: ฟังก์ชัน NEWGUID ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NEWGUID
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861829"
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
