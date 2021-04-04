---
title: ฟังก์ชัน ER FORMATELEMENTNAME
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FORMATELEMENTNAME
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561313"
---
# <a name="formatelementname-er-function"></a>ฟังก์ชัน ER FORMATELEMENTNAME

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME` ฟังก์ชันส่งกลับค่า *สตริง* ที่แสดงถึงชื่อขององค์ประกอบรูปแบบการรายงานอิเล็กทรอนิกส์ปัจจุบัน (ER)

## <a name="syntax"></a>ไวยากรณ์

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>ค่าที่ส่งคืน

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ฟังก์ชันนี้สามารถถูกเรียกในนิพจน์ ER ที่ถูกกำหนดค่าสำหรับ **ชื่อคีย์ข้อมูลที่เก็บรวบรวม** และคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวมไว้** ของส่วนประกอบรูปแบบ ER จากกลุ่ม **ข้อความ** ที่อยู่ภายใต้ส่วนประกอบ **ทั่วไป\\ไฟล์** ซึ่งมีเปิดตัวเลือก **รายละเอียดของผลลัพธ์การรวบรวม**

## <a name="example"></a>ตัวอย่าง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันการรวบรวมข้อมูล](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]