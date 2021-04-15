---
title: ฟังก์ชัน EMPTYRECORD ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ EMPTYRECORD (ER)
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746542"
---
# <a name="emptyrecord-er-function"></a>ฟังก์ชัน EMPTYRECORD ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `EMPTYRECORD` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null ซึ่งมีโครงสร้างเดียวกันกับรายการเรกคอร์ดหรือเรกคอร์ดที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*

พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)* อย่างใดอย่างหนึ่ง

## <a name="return-values"></a>ส่งคืนค่า

*คอนเทนเนอร์ (เรกคอร์ด)*

ค่าเรกคอร์ดที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

> [!NOTE] 
> เรกคอร์ด null เป็นเรกคอร์ดที่ฟิลด์ทั้งหมดมีค่าว่างเปล่า ค่าว่างเปล่า **0** (ศูนย์) สำหรับตัวเลข สตริงว่างสำหรับสตริงที่ และอื่นๆ

## <a name="example"></a>ตัวอย่าง

`EMPTYRECORD (SPLIT ("abc", 1))` ส่งคืนเรกคอร์ดที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT` สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [SPLIT](er-functions-list-split.md)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันเรกคอร์ด](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]