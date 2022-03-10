---
title: ฟังก์ชั่น WHERE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) WHERE
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
ms.openlocfilehash: dd021381e04e8794a5668041dbd71e5c981577a19141581fdde078a9d5801f49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756464"
---
# <a name="where-er-function"></a>ฟังก์ชั่น WHERE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `WHERE` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* หลังจากที่ถูกกรองตามเงื่อนไขที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`condition`: *บูลีน*

นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ใช้ในการกรองเรกคอร์ดของรายการที่ระบุ

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชันนี้แตกต่างจากฟังก์ชัน [FILTER](er-functions-list-filter.md) เนื่องจากเงื่อนไขที่ระบุจะถูกนำไปใช้กับแหล่งข้อมูล การรายงานทางอิเล็กทรอนิกส์ (ER) ใดๆ ของชนิด *รายการเรกคอร์ด* ที่แสดงในหน่วยความจำ

ถ้าอาร์กิวเมนต์ที่ถูกกำหนดค่าสำหรับฟังก์ชันนี้ (`list` และ `condition`) อนุญาตให้มีการแปลการร้องขอนี้ไปยังการเรียก SQL โดยตรงข้อความเตือนจะถูกโยนในเวลาออกแบบ ข้อความนี้จะแจ้งให้ผู้ใช้ที่มีประสิทธิภาพการทำงานอาจถูกปรับปรุงถ้าฟังก์ชัน [FILTER](er-functions-list-filter.md) ถูกใช้แทน `WHERE`

## <a name="example-1"></a>ตัวอย่างที่ 1

ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable นิพจน์ `WHERE (Vendors, Vendors.VendGroup = "40")` จะส่งกลับรายการของเพียงแค่ผู้จัดจำหน่ายที่เป็นของกลุ่มผู้จัดจำหน่าย 40

## <a name="example-2"></a>ตัวอย่างที่ 2

ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิดของ *ฟิลด์ที่มีการคำนวณ* และมีนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `WHERE( DS, DS.Value = "B")` จะส่งคืนรายการเรกคอร์ดที่มีค่าข้อความ **"B"** ในฟิลด์ **ค่า**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]