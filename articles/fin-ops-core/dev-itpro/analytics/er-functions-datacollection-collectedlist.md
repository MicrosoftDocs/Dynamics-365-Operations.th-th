---
title: ฟังก์ชัน COLLECTEDLIST ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) COLLECTEDLIST
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 494fb0fa1000abe8d0234d512e41926103c56f05
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755335"
---
# <a name="collectedlist-er-function"></a>ฟังก์ชัน COLLECTEDLIST ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `COLLECTEDLIST` เป็น *ค่ารายการ* ที่ประกอบด้วยรายการของค่าที่ถูกส่งกลับโดยคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ขององค์ประกอบรูปแบบ และเก็บรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์

## <a name="syntax"></a>ไวยากรณ์

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`condition 1 range`: *สตริง*

ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) อาร์กิวเมนต์นี้เป็นข้อบังคับ

`condition 1 value`: *สตริง*

ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) อาร์กิวเมนต์นี้เป็นข้อบังคับ

`condition N range`: *สตริง*

ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

`condition N value`: *สตริง*

ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

คุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** และ **ค่าคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่

ส่งคืนรายการที่ว่างเมื่อตัวเลือก **รวบรวมรายละเอียดผลลัพธ์** ของส่งนประกอบของ **Common\\File** ปัจจุบันถูกปิด

ในอาร์กิวเมนต์ `condition range` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว

ในอาร์กิวเมนต์ `condition value` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว

## <a name="example"></a>ตัวอย่าง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันการรวบรวมข้อมูล](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]