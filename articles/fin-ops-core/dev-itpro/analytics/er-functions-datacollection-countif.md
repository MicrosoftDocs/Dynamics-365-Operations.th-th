---
title: ฟังก์ชัน ER COUNTIF
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) COUNTIF
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
ms.openlocfilehash: bebb3d3b810e68fa6a0d3f4deb92b750b7c9a9f3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755311"
---
# <a name="countif-er-function"></a>ฟังก์ชัน ER COUNTIF

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `COUNTIF` ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนขององค์ประกอบรูปแบบที่ถูกรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ เงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์

## <a name="syntax"></a>ไวยากรณ์

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`condition range`: *สตริง*

ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)

`condition value`: *สตริง*

ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)

## <a name="return-values"></a>ค่าที่ส่งคืน

*จำนวนเต็ม*

ค่าตัวเลขที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

คุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** และ **ค่าคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่

ฟังก์ชันนี้ส่งคืนค่า **0** (ศูนย์) เมื่อตัวเลือก **รวบรวมรายละเอียดผลลัพธ์** ของส่วนประกอบของ **Common\\File** ปัจจุบันถูกปิด

ในอาร์กิวเมนต์ `condition range` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว

ในอาร์กิวเมนต์ `condition value` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว

## <a name="example"></a>ตัวอย่าง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันการรวบรวมข้อมูล](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]