---
title: ฟังก์ชัน ER SPLITLISTBYLIMIT
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLITLISTBYLIMIT
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
ms.openlocfilehash: eb492560a453ec59bb82d24dd6717f409bd8b257
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745556"
---
# <a name="splitlistbylimit-er-function"></a>ฟังก์ชัน ER SPLITLISTBYLIMIT

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `SPLITLISTBYLIMIT` แยกรายการที่ระบุลงในรายการใหม่ของรายการย่อย (ชุดงาน) จำนวนของเรกคอร์ดในแต่ละชุดงานจะถูกคำนวณแบบไดนามิก จากนั้นฟังก์ชันจะส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่ที่ประกอบด้วยชุดงาน

## <a name="syntax"></a>ไวยากรณ์

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`limit value`: *จำนวนเต็ม* หรือ *จำนวนจริง*

ค่าสูงสุดของขีดจำกัดที่ใช้ในการแบ่งรายการเดิมเป็นชุดงาน

`limit source`: *ฟิลด์*

เส้นทางที่ถูกต้องของเขตข้อมูลของชนิด *จำนวนรวม* หรือ *จำนวนจริง* ในรายการที่ระบุ ค่าของฟิลด์นี้จะกำหนดขั้นตอนที่จะเพิ่มผลรวมทั้งหมด

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

รายการของชุดงานที่ส่งคืนประกอบด้วยองค์ประกอบต่อไปนี้:

- **ค่า**: *รายการ*

    รายการของเรกคอร์ดที่เป็นของชุดงานปัจจุบัน

- **Batchnumber**: *จำนวนเต็ม*

    หมายเลขของชุดงานปัจจุบันในรายการที่ส่งคืน

ขีดจำกัดจะไม่ใช้กับสินค้าเดี่ยวของรายการต้นทาง ถ้าแหล่งที่มาของขีดจำกัดเกินขีดจำกัดที่กำหนดไว้

## <a name="example"></a>ตัวอย่าง

ภาพประกอบต่อไปนี้แสดงรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

ภาพประกอบต่อไปนี้แสดงแหล่งข้อมูลที่ใช้สำหรับรูปแบบ

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบ ในกรณีนี้ ผลลัพธ์เป็นรายการแบบธรรมดาของสินค้าโภคภัณฑ์

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

ในภาพประกอบต่อไปนี้ มีการปรับปรุงรูปแบบเดียวกัน เพื่อให้แสดงรายการของสินค้าโภคภัณฑ์ในชุดงานต่างๆ หากชุดงานเดียวต้องรวมโภคภัณฑ์ และน้ำหนักรวมไม่ควรเกินขีดจำกัดที่ 9

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการปรับเปลี่ยน

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> ขีดจำกัดจะไม่ถูกใช้กับรายการสุดท้ายของรายการต้นทาง เนื่องจากค่า (**11**) ของแหล่งที่มาของขีดจำกัด (**น้ำหนัก**) เกินขีดจำกัดที่กำหนดไว้ (**9**) หากต้องการเพิกเฉยต่อรายการย่อยระหว่างการสร้างรายงาน ใช้ฟังก์ชัน `WHERE` หรือนิพจน์ **Enabled** ขององค์ประกอบรูปแบบที่สอดคล้องกันเพื่อละเว้นตามที่ต้องการ

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]