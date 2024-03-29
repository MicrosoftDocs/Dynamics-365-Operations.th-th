---
title: โครงร่างป้ายชื่อการกำหนดเส้นทางเอกสาร
description: บทความนี้จะอธิบายวิธีการใช้วิธีการจัดรูปแบบเพื่อพิมพ์ค่าบนป้ายชื่อ
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708657"
---
# <a name="document-routing-label-layout"></a>โครงร่างป้ายชื่อการกำหนดเส้นทางเอกสาร

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการสร้างโครงร่างสำหรับป้ายชื่อของป้ายทะเบียน คอนเทนเนอร์ และป้ายชื่อเวฟ และยังให้แนวทางเกี่ยวกับการใช้ Zebra Programming Language (ZPL) ที่ใช้ในการสร้างโครงร่างด้วย

โครงร่างป้ายชื่อการกำหนดเส้นทางเอกสารจะกำหนดวิธีจัดวางป้ายชื่อและข้อมูลที่จะพิมพ์บนป้ายชื่อ คุณตั้งค่าคอนฟิกจุดทริกเกอร์การพิมพ์เมื่อคุณตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่และเทมเพลตการทำงาน

ข้อมูลในบทความนี้จะใช้กับโครงร่างป้ายชื่อการกำหนดเส้นทางเอกสารทั้งหมด รวมถึงโครงร่างของ [ป้ายชื่อป้ายทะเบียน](tasks/license-plate-label-printing.md), [ป้ายชื่อคอนเทนเนอร์](print-container-labels.md) และ [ป้ายชื่อเวฟ](configure-wave-label-printing.md)

คุณสามารถพิมพ์ป้ายชื่อที่ซับซ้อนสูงได้ ซึ่งอุปกรณ์การพิมพ์สามารถแปลข้อความที่ส่งไปได้ ตัวอย่างเช่น โครงร่าง ZPL ซึ่งมีบาร์โค้ด อาจคล้ายกับตัวอย่างต่อไปนี้

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

โดยเป็นส่วนหนึ่งของกระบวนการพิมพ์ป้ายชื่อ ข้อความ `$LicensePlateId$` ในตัวอย่างนี้จะถูกแทนที่ด้วยค่าข้อมูล เครื่องมือการสร้างป้ายชื่อที่มีอยู่หลายตัวสามารถช่วยคุณจัดรูปแบบข้อความสำหรับโครงร่างป้ายชื่อ หลายๆ เครื่องมือเหล่านี้สนับสนุนรูปแบบ `$FieldName$` นอกจากนี้ Microsoft Dynamics 365 Supply Chain Management ยังใช้ตรรกะการจัดรูปแบบพิเศษ โดยเป็นส่วนหนึ่งของการแมปฟิลด์สำหรับโครงร่างการกำหนดเส้นทางเอกสาร

เมื่อต้องการดูค่าที่จะพิมพ์ ให้ไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> ป้ายชื่อทะเบียน**

## <a name="turn-on-this-feature-for-your-system"></a>เปิดใช้งานคุณลักษณะนี้สำหรับระบบของคุณ

ถ้าระบบของคุณยังไม่ได้รวมคุณลักษณะที่อธิบายไว้ในบทความนี้ ให้ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และ เปิดคุณลักษณะ *โครงร่างป้ายชื่อป้ายทะเบียนขั้นสูง* (เริ่มจาก Supply Chain Management รุ่น 10.0.21 คุณลักษณะนี้จะเปิดตามค่าเริ่มต้น) (เริ่มจาก Supply Chain Management รุ่น 10.0.25 คุณลักษณะนี้เป็นแบบบังคับและไม่สามารถปิดได้)

## <a name="custom-number-formats"></a>รูปแบบตัวเลขที่กำหนดเอง

คุณสามารถเลือกกำหนดการจัดรูปแบบของค่าฟิลด์ตัวเลขที่พิมพ์โดยใช้รหัสที่มีรูปแบบต่อไปนี้

```dos
$FieldName:FormatString$
```

ต่อไปนี้เป็นคำอธิบายของรูปแบบนี้:

- `FieldName` คือชื่อของฟิลด์ข้อมูล (เช่น **ปริมาณ**)
- `FormatString` กำหนดว่าต้องพิมพ์ข้อมูลอย่างไร

ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถกำหนดฟิลด์ปริมาณงาน (**ปริมาณ**):

- เมื่อต้องการแสดงตัวเลขสี่หลักเสมอ (โดยใช้เลขศูนย์เป็นตัวยึดตำแหน่ง) ให้ใช้ `$Qty:0000$` ตัวอย่างเช่น ถ้าปริมาณคือ 10 ป้ายชื่อจะแสดง "0010"
- เมื่อต้องการแสดงตำแหน่งทศนิยมสองตำแหน่งเสมอ ให้ใช้ `$Qty:0.00$` ตัวอย่างเช่น ถ้าปริมาณคือ 10 ป้ายชื่อจะแสดง "10.00"

สำหรับรายการทั้งหมดของสตริงรูปแบบตัวเลขที่พร้อมใช้งาน ให้ดูที่ [สตริงรูปแบบตัวเลขที่กำหนดเอง](/dotnet/standard/base-types/custom-numeric-format-strings)

## <a name="custom-string-formats"></a>รูปแบบสตริงที่กำหนดเอง

คุณสามารถลบอักขระตัวแรกของสตริงโดยการใช้ฟิลด์และรหัสรูปแบบต่อไปนี้

```dos
$FieldName:#..$
```

ที่นี่ `#` ระบุจำนวนของอักขระที่จะข้าม ตัวอย่างเช่น ถ้าต้องการพิมพ์หมายเลขป้ายทะเบียนรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) ที่ไม่มีอักขระสองตัวแรก ให้ใช้ `$LicensePlateId:2..$` ในกรณีนี้ หมายเลขป้ายทะเบียน 0011111111111222221 จะถูกพิมพ์เป็น "11111111111222221"

## <a name="custom-datetime-formats"></a>รูปแบบวันที่/เวลาแบบกำหนดเอง

ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถควบคุมรูปแบบที่ใช้ในการพิมพ์วันที่

```dos
$PrintedDate:dd-MM-yyyy$
```

ในตัวอย่างนี้ วันที่ 30 เมษายน 2020 จะถูกพิมพ์เป็น "30-04-2020"

สำหรับรายการทั้งหมดของรูปแบบวันที่/เวลาที่พร้อมใช้งาน ให้ดูที่ [สตริงรูปแบบเวลาและวันที่ที่กำหนดเอง](/dotnet/standard/base-types/custom-date-and-time-format-strings)

## <a name="print-individual-lines-from-multiline-data"></a>พิมพ์แต่ละบรรทัดจากข้อมูลหลายบรรทัด

ถ้าฟิลด์ข้อมูลมีหลายบรรทัด (นั่นคือบรรทัดที่คั่นด้วยตัวแบ่งบรรทัด) คุณสามารถพิมพ์แต่ละบรรทัดได้โดยใช้รูปแบบต่อไปนี้

```dos
$FieldName[#]$
```

ที่นี่ `#` คือหมายเลขรายการที่คุณต้องการพิมพ์ (ใช้ 1 สำหรับบรรทัดแรก)

ตัวอย่างเช่น ระบบของคุณมีฟิลด์ `AdditionalAddress` ที่จัดเก็บที่อยู่หลายบรรทัดต่อไปนี้:

Contoso Inc  
ชื่อถนน 123  
บางเมือง บางรัฐ

คุณสามารถพิมพ์ที่อยู่นี้ หนึ่งบรรทัดในแต่ละครั้ง โดยใช้รหัสดังต่อไปนี้

| รหัส | ข้อความที่พิมพ์ |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc |
| `$AdditionalAddress[2]$` | ชื่อถนน 123 |
| `$AdditionalAddress[3]$` | บางเมือง บางรัฐ |

## <a name="print-and-format-from-a-display-method"></a>พิมพ์และจัดรูปแบบจากวิธีการแสดง

คุณสามารถพิมพ์จากวิธีการแสดงโดยใช้รูปแบบต่อไปนี้

```dos
$DisplayMethod()$
```

คุณสามารถรวมรูปแบบนี้กับชนิดอื่นๆ ที่อธิบายไว้ก่อนหน้านี้ในบทความนี้ ตัวอย่างเช่น คุณมีวิธีการแสดงที่มีการระบุชื่อ `DisplayListOfItemsNumbers()` และคุณต้องการพิมพ์หมายเลขสินค้าแรกของวิธีการนี้ ในกรณีนี้ คุณสามารถใช้รหัสต่อไปนี้

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>ข้อมูลเพิ่มเติมเกี่ยวกับวิธีการพิมพ์ป้ายชื่อ

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าและพิมพ์ป้ายชื่อ ให้ดูที่บทความต่อไปนี้:

- [การพิมพ์ป้ายชื่อป้ายทะเบียน](tasks/license-plate-label-printing.md)
- [พิมพ์ป้ายชื่อคอนเทนเนอร์](print-container-labels.md)
- [การพิมพ์ป้ายชื่อของเวฟ](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
