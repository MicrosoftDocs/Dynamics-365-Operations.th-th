---
title: ฟังก์ชัน NULLCONTAINER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NULLCONTAINER (ER)
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 13159d9d7c8d1871886beb3cb1938ca8b0097e0efb6f10a9d1b229c49b9ff947
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738587"
---
# <a name="nullcontainer-er-function"></a>ฟังก์ชัน NULLCONTAINER ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NULLCONTAINER` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null ซึ่งมีโครงสร้างเดียวกันกับรายการเรกคอร์ดหรือเรกคอร์ดที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)* อย่างใดอย่างหนึ่ง

## <a name="return-values"></a>ส่งคืนค่า

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

> [!NOTE] 
> ฟังก์ชันนี้ล้าสมัย ใช้ฟังก์ชัน `EMPTYRECORD` แทน สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [EMPTYRECORD](er-functions-record-emptyrecord.md)

## <a name="example"></a>ตัวอย่าง

`NULLCONTAINER (SPLIT ("abc", 1))` ส่งคืนเรกคอร์ดที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT` สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [SPLIT](er-functions-list-split.md)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันเรกคอร์ด](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]