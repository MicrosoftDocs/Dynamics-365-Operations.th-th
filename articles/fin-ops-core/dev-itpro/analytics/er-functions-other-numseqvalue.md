---
title: ฟังก์ชัน NUMSEQVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NUMSEQVALUE (ER)
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
ms.openlocfilehash: b513d04bfeb3a37aa0b1703d0fdde040885a5159
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680601"
---
# <a name="numseqvalue-er-function"></a>ฟังก์ชัน NUMSEQVALUE ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `NUMSEQVALUE` ส่งกลับค่า *สตริง* ที่แสดงถึงค่าที่สร้างขึ้นใหม่ของลำดับหมายเลข ตามลำดับหมายเลข ขอบเขต และรหัสขอบเขตที่ระบุ รหัสขอบเขตจะเท่ากับรหัสบริษัทที่จัดหาโดยบริบทที่เรียกใช้รูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>ไวยากรณ์ 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`number sequence code`: *สตริง*

ค่าข้อความที่แสดงรหัสของลำดับหมายเลขที่จำเป็นต้องใช้ค่าใหม่

`number sequence record ID`: *Int64*

ค่า *Int64* ที่แสดงถึงรหัสเรกคอร์ดของเรกคอร์ดในตาราง NumberSequenceTable ที่มีคำนิยามของลำดับหมายเลขที่จำเป็นต้องใช้ค่าใหม่

`scope type`: *ค่า Enum*

ค่าการแจงนับของการแจงนับ **ERExpressionNumberSequenceScopeType** ที่กำหนดขอบเขตของลำดับหมายเลขที่จำเป็นต้องใช้ค่าใหม่ ชนิดขอบเขตที่พร้อมใช้งานจะ **ถูกใช้ร่วมกัน** **นิติบุคคล** และ **บริษัท**

`scope ID`: *สตริง*

ค่า *สตริง* ที่ระบุขอบเขต ตามชนิดขอบเขตที่ระบุ

## <a name="return-values"></a>ส่งคืนค่า

*สตริง*

ค่าข้อความที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

สำหรับชนิดขอบข่าย **ที่ใช้ร่วมกัน** ระบุสตริงที่ว่างเป็นรหัสขอบเขต

สำหรับชนิดขอบเขต **บริษัท** และ **นิติบุคคล** ระบุรหัสบริษัทเป็นรหัสขอบเขต ถ้าคุณระบุสตริงที่ว่างเป็นรหัสขอบเขตสำหรับชนิดขอบเขตนี้ จะมีการใช้รหัสบริษัทปัจจุบัน

เมื่อมีการใช้ไวยากรณ์ 1 ลำดับหมายเลขจะถูกร้องขอสำหรับชนิดขอบเขตของ **บริษัท** และรหัสบริษัทจะถูกจัดหาโดยบริบทที่มีการรันรูปแบบ ER

## <a name="example-1"></a>ตัวอย่างที่ 1

ในรูปแบบ ER ของคุณ คุณสามารถกำหนดแหล่งข้อมูล **AskNumSeq** ของชนิด *พารามิเตอร์ป้อนเข้าของผู้ใช้* แหล่งข้อมูลนี้อ้างอิงถึงชนิดข้อมูลแบบขยาย (EDT) ของ **คำอธิบาย** ถัดไป คุณกำหนดแหล่งข้อมูล **NumSeq** ของชนิดของ *ฟิลด์ที่มีการคำนวณ* แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `NUMSEQVALUE (AskNumSeq)` เมื่อแหล่งข้อมูล **NumSeq** ถูกเรียก จะส่งกลับค่าที่สร้างขึ้นใหม่ของลำดับหมายเลขที่ระบุไว้ในขณะทำงานโดยการป้อนรหัสในกล่องโต้ตอบ มีการร้องขอลำดับหมายเลขสำหรับชนิดขอบเขตของ **บริษัท** รหัสบริษัทจะถูกจัดหาโดยบริบทที่มีการรันรูปแบบ ER

## <a name="example-2"></a>ตัวอย่างที่ 2

มีการกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:

- แหล่งข้อมูล **LedgerParms** ของชนิด *ตาราง* แหล่งข้อมูลนี้อ้างถึงตาราง LedgerParameters
- แหล่งข้อมูล **NumSeq** ของชนิดของ *ฟิลด์ที่มีการคำนวณ* แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`

เมื่อมีการเรียกแหล่งข้อมูล **NumSeq** จะส่งกลับค่าที่สร้างขึ้นใหม่ของลำดับหมายเลขที่ถูกตั้งค่าคอนฟิกในพารามิเตอร์บัญชีแยกประเภททั่วไป สำหรับบริษัทที่ให้บริบทที่รันเหนือรูปแบบ ER ลำดับหมายเลขนี้ระบุสมุดรายวันโดยไม่ซ้ำกัน และทำหน้าที่เป็นหมายเลขชุดงานที่เชื่อมโยงธุรกรรมร่วมกัน

## <a name="example-3"></a>ตัวอย่างที่ 3

มีการกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:

- แหล่งข้อมูล **enumScope** ของชนิด *การแจงนับ* ของ Microsoft Dynamics 365 Finance แหล่งข้อมูลนี้อ้างอิงถึงการแจงนับ **ERExpressionNumberSequenceScopeType**
- แหล่งข้อมูล **NumSeq** ของชนิดของ *ฟิลด์ที่มีการคำนวณ* แหล่งข้อมูลนี้ประกอบด้วยนิพจน์ `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`

เมื่อมีการเรียกแหล่งข้อมูล **NumSeq** จะส่งกลับค่าที่สร้างขึ้นใหม่ของลำดับหมายเลข **Gene\_1** ที่ถูกตั้งค่าคอนฟิกสำหรับบริษัทที่ให้บริบทที่รันเหนือรูปแบบ ER

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)](er-functions-category-other.md)
