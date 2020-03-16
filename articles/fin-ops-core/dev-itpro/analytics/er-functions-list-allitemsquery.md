---
title: ฟังก์ชัน ALLITEMSQUERY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ALLITEMSQUERY
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99f2aa9863e36a2f2eb1db5d0569d2a82402969a
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070655"
---
# <a name="ALLITEMSQUERY">ฟังก์ชัน ALLITEMSQUERY ER</a>

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `ALLITEMSQUERY` ทำงานเป็นแบบสอบถาม SQL ที่เชื่อมต่อกัน จะส่งกลับค่า *รายการเรกคอร์ด* ที่ทำให้แบนใหม่ที่ประกอบด้วยรายการของเรกคอร์ดที่แสดงถึงรายการทั้งหมดที่ตรงกับพาธที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`path`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* ต้องมีอย่างน้อยหนึ่งความสัมพันธ์

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ต้องกำหนดพาธที่ระบุเป็นพาธแหล่งข้อมูลที่ถูกต้องขององค์ประกอบแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* ต้องมีอย่างน้อยหนึ่งความสัมพันธ์ด้วย องค์ประกอบข้อมูล เช่น *สตริง* พาธ และ *วันที่* ควรรายงานข้อผิดพลาดในตัวสร้างนิพจน์การรายงานทางอิเล็กทรอนิกส์ (ER) ในขณะที่ออกแบบ

เมื่อฟังก์ชันนี้ถูกนำไปใช้กับแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* ที่อ้างถึงออบเจ็กของแอปพลิเคชันต์ที่สามารถเรียกโดยตรงโดยใช้ SQL (ตัวอย่างเช่น ตารางเอนทิตี หรือแบบสอบถาม) จะทำงานเป็นแบบสอบถาม SQL ที่เข้าร่วม มิฉะนั้นจะทำงานในหน่วยความจำเป็นฟังก์ชัน [ALLITEMS](er-functions-list-allitems.md)

## <a name="example"></a>ตัวอย่าง

คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:

- แหล่งข้อมูล **CustInv** ของชนิด *เรกคอร์ดของตาราง* ที่อ้างอิงถึงตาราง CustInvoiceTable
- แหล่งข้อมูล **FilteredInv** ของชนิด *ฟิลด์ที่มีการคำนวณ* ที่ประกอบด้วยนิพจน์ `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- **JourLines** ของชนิด *ฟิลด์ที่มีการคำนวณ* ที่ประกอบด้วยนิพจน์ `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

เมื่อคุณรันการแม็ปแบบจำลองของคุณในการเรียกแหล่งข้อมูล **JourLines** จะมีการรันคำสั่ง SQL ต่อไปนี้:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)
