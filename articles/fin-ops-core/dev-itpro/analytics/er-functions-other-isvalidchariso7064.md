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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f6f3326c9ca5cdcb3cef52f243d6d3da34251ce
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915935"
---
# <a name="ISVALIDCHARACTERISO7064">ฟังก์ชัน ISVALIDCHARACTERISO7064 ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ISVALIDCHARACTERISO7064` ส่งกลับค่า *บูลีน* เป็น **จริง** หากสตริงที่ระบุแสดงหมายเลขบัญชีธนาคารระหว่างประเทศที่ถูกต้อง (IBAN) มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**

## <a name="syntax"></a>ไวยากรณ์

```
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
