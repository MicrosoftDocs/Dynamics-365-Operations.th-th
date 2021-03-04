---
title: ฟังก์ชัน ISVALIDCHARACTERISO7064 ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ ISVALIDCHARACTERISO7064 (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680673"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ฟังก์ชัน ISVALIDCHARACTERISO7064 ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ISVALIDCHARACTERISO7064` ส่งกลับค่า *บูลีน* เป็น **จริง** หากสตริงที่ระบุแสดงหมายเลขบัญชีธนาคารระหว่างประเทศที่ถูกต้อง (IBAN) มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**

## <a name="syntax"></a>ไวยากรณ์

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`text`: *สตริง*

ค่าข้อความที่แสดงถึง IBAN

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="example"></a>ตัวอย่าง

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` ส่งกลับค่า **จริง** 

`ISVALIDCHARACTERISO7064 ("AT61")` ส่งกลับค่า **เท็จ**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]