---
title: ฟังก์ชัน LISTJOIN ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTJOIN
author: kfend
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ec8a5985277de8036ec8ad51b947a8bab098a1c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291218"
---
# <a name="listjoin-er-function"></a>ฟังก์ชัน LISTJOIN ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `LISTJOIN` ส่งกลับค่า *รายการเรกคอร์ด* ที่แสดงรายการเข้าร่วมใหม่ของเรกคอร์ดที่สร้างขึ้นจากอาร์กิวเมนต์ที่ระบุของชนิด

## <a name="syntax"></a>ไวยากรณ์

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list 1`: *รายการเรกคอร์ด*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* อาร์กิวเมนต์นี้เป็นข้อบังคับ

`list N`: *รายการเรกคอร์ด*

การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

โครงสร้างของรายการที่สร้างขึ้นมีเฉพาะฟิลด์ที่แสดงในโครงสร้างของรายการเรกคอร์ดทั้งหมดที่มีการอ้างถึงในอาร์กิวเมนต์

## <a name="example"></a>ตัวอย่าง

คุณป้อนแหล่งข้อมูล **เรกคอร์ด 1** ของชนิดของ `Container` แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:

- **Code**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `String`
- **Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`

จากนั้นคุณป้อนแหล่งข้อมูล **เรกคอร์ด 2** ของชนิดของ `Container` แหล่งข้อมูลนี้ประกอบด้วยฟิลด์ที่ซ้อนกันของชนิดฟิลด์ `Calculated field`:

- **Amount**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Real`
- **IsValid**: ฟิลด์นี้ประกอบด้วยนิพจน์ที่ส่งกลับค่าของชนิด `Boolean`

![หน้าตัวออกแบบการแม็ปแบบจำลอง ER](./media/er-functions-list-listjoin-image1.gif)

ในกรณีนี้นิพจน์ `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` ส่งกลับรายการใหม่ที่ประกอบด้วยสองเรกคอร์ด

![หน้าตัวออกแบบการแม็ปแบบจำลอง ER ที่มีสองเรกคอร์ด](./media/er-functions-list-listjoin-image2.gif)

โครงสร้างของรายการนี้ประกอบด้วยฟิลด์ **ยอดเงิน** เดียวของชนิด `Real` เนื่องจากฟิลด์นี้เป็นฟิลด์เดียวที่จะแสดงในทุกอาร์กิวเมนต์ของฟังก์ชันที่เรียก

![ฟิลด์จำนวนเงินของหน้าตัวออกแบบการแม็ปแบบจำลอง ER](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)

[ดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อวิเคราะห์การแปลงและลำดับของข้อมูล](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
