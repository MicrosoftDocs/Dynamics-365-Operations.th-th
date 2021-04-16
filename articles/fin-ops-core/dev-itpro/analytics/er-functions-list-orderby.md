---
title: ฟังก์ชัน ORDERBY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ORDERBY
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753203"
---
# <a name="orderby-er-function"></a>ฟังก์ชัน ORDERBY ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ORDERBY` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* หลังจากที่ถูกเรียงลำดับตามอาร์กิวเมนต์ที่ระบุ อาร์กิวเมนต์เหล่านี้สามารถถูกกำหนดเป็นนิพจน์ได้

## <a name="syntax"></a>ไวยากรณ์

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`expression 1`: *ฟิลด์*

เส้นทางที่ถูกต้องของฟิลด์ของแหล่งข้อมูลที่ถูกอ้างอิงโดยอาร์กิวเมนต์ `list` ของฟังก์ชันที่เรียก ฟิลด์ที่อ้างอิงต้องเป็นฟิลด์ของชนิดข้อมูลดั้งเดิม ต้องระบุอาร์กิวเมนต์นี้

`expression N`: *ฟิลด์*

เส้นทางที่ถูกต้องของฟิลด์ของแหล่งข้อมูลที่ถูกอ้างอิงโดยอาร์กิวเมนต์ `list` ของฟังก์ชันที่เรียก ฟิลด์ที่อ้างอิงต้องเป็นฟิลด์ของชนิดข้อมูลดั้งเดิม อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="example-1"></a>ตัวอย่างที่ 1

ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("C|B|A", "|")` นิพจน์ `FIRST( ORDERBY( DS, DS. Value)).Value` จะส่งกลับค่าข้อความ **A**

## <a name="example-2"></a>ตัวอย่างที่ 2

ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ที่อ้างอิงถึงตาราง VendTable นิพจน์ `ORDERBY (Vendors, Vendors.'name()')` จะส่งกลับรายการของผู้จัดจำหน่ายที่เรียงลำดับตามชื่อในลำดับจากน้อยไปมาก

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]