---
title: ฟังก์ชัน ABS ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ABS (ER)
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 90fbff223be5c195feb66b9ea72ee0688e60697b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886891"
---
# <a name="abs-er-function"></a>ฟังก์ชัน ABS ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ABS` ส่งกลับค่าเงินเต็ม (โมดูล) ของจำนวนที่ระบุเป็นค่า *จริง* กล่าวคือ ส่งคืนหมายเลขโดยไม่มีเครื่องหมาย

## <a name="syntax"></a>ไวยากรณ์

```vb
ABS (number)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number`: *จริง*

ค่าตัวเลขที่คุณต้องการโมดูลัส

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนจริง*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`ABS (-1)` ส่งกลับค่า **1**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันคณิตศาสตร์](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]