---
title: ฟังก์ชัน LISTDISTINCT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ LISTDISTINCT (ER)
author: NickSelin
ms.date: 7/30/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 7cc51695d261a63521ae88e2a9362b6f30b9618ed89300bcaeb606b050c81350
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735585"
---
# <a name="listdistinct-er-function"></a>ฟังก์ชัน LISTDISTINCT ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

ฟังก์ชัน `LISTDISTINCT` จะคำนวณนิพจน์ที่ระบุเป็นตัวเลือกสำหรับเรกคอร์ดทั้งหมดของรายการที่ระบุ โดยจะส่งคืน *รายการเรกคอร์ด* ใหม่ที่มีเรกคอร์ดเดียวสำหรับตัวเลือกที่ไม่ซ้ำกันแต่ละรายการ

## <a name="syntax"></a>ไวยากรณ์

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`selector`: *ชนิดข้อมูลพื้นฐาน*

นิพจน์ที่ถูกต้องที่ใช้ในการคำนวณค่าตัวเลือกสำหรับเรกคอร์ดทั้งหมดในรายการที่ระบุ

ชนิดข้อมูลต่อไปนี้ได้รับการสนับสนุนสำหรับพารามิเตอร์นี้:

- บูลีน
- วัน เดือน
- วันที่และเวลา
- GUID
- เลขจำนวนเต็ม
- Int64
- จำนวนจริง
- สตริง

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

โครงสร้างของรายการที่สร้างขึ้นตรงกับโครงสร้างของรายการที่ระบุ

อาจมีการคำนวณค่าตัวเลือกเดียวกันสำหรับหลายเรกคอร์ดในรายการที่ระบุ ในกรณีนี้ ค่าฟิลด์ของเรกคอร์ดที่เกี่ยวข้องในรายการที่สร้างขึ้นจะเท่ากับค่าของเรกคอร์ดแรกจากรายการที่ระบุที่มีการคำนวณค่าตัวเลือก

การดำเนินการของฟังก์ชันนี้เกิดขึ้นในแหล่งข้อมูล [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) ของชนิด *รายการเรกคอร์ด* ที่มีอยู่ในหน่วยความจำ

นอกจากนี้ยังสามารถใช้แหล่งข้อมูล **GROUPBY** เพื่อสร้างรายการเรกคอร์ดที่มีการคำนวณค่าที่แตกต่างกันของตัวเลือกด้วย อย่างไรก็ตาม จากมุมมองด้านประสิทธิภาพและการใช้หน่วยความจำ การใช้ฟังก์ชัน `LISTDISTINCT` ดีกว่าแหล่งข้อมูล **GROUPBY** เนื่องจากมีการดำเนินการของฟังก์ชันในหน่วยความจำ

## <a name="example"></a>ตัวอย่าง

ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถดูรายการของหมายเลขบัญชีลูกค้าที่ไม่ซ้ำกัน ซึ่งมีการออกใบแจ้งหนี้การขายหรือใบแจ้งหนี้โครงการอย่างน้อยหนึ่งรายการในระหว่างรอบระยะเวลาที่ระบุ

1. ป้อนแหล่งข้อมูล **SalesInvoice** ของชนิด `Record list` ที่อ้างถึงตารางแอปพลิเคชัน **CustInvoiceJour** และกรองใบแจ้งหนี้การขายสำหรับรอบระยะเวลาที่ระบุ

    ฟิลด์ `InvoiceAccount` ของแหล่งข้อมูลนี้ส่งคืนหมายเลขบัญชีของลูกค้าที่ออกใบแจ้งหนี้แล้ว

2. ป้อนแหล่งข้อมูล **ProjectInvoice** ของชนิด `Record list` ที่อ้างถึงตารางแอปพลิเคชัน **ProjInvoiceJour** และกรองใบแจ้งหนี้โครงการสำหรับรอบระยะเวลาที่ระบุ

    ฟิลด์ `InvoiceAccount` ของแหล่งข้อมูลนี้ส่งคืนหมายเลขบัญชีของลูกค้าที่ออกใบแจ้งหนี้แล้ว

3. ตั้งค่าคอนฟิกแหล่งข้อมูล **AllInvoices** ของชนิด `Calculated field` ที่มีนิพจน์ `LISTJOIN(SalesInvoice, ProjectInvoice)`

    แหล่งข้อมูลนี้ส่งคืนรายการที่รวมของใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ

4. ตั้งค่าคอนฟิกแหล่งข้อมูล **InvoicedCustomer** ของชนิด `Record list` ที่มีนิพจน์ `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`

    แหล่งข้อมูลนี้ส่งคืนรายการใหม่ที่มีเรกคอร์ดเดียวสำหรับลูกค้าแต่ละรายที่ไม่ซ้ำกันซึ่งมีการออกใบแจ้งหนี้ในระหว่างรอบระยะเวลาที่กำหนด ฟิลด์ `InvoiceAccount` ของรายการนี้มีหมายเลขบัญชีลูกค้า

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]