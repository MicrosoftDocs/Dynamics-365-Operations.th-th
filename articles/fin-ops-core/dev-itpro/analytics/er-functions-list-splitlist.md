---
title: ฟังก์ชัน ER SPLITLIST
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLITLIST
author: kfend
ms.date: 03/15/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292540"
---
# <a name="splitlist-er-function"></a>ฟังก์ชัน ER SPLITLIST

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `SPLITLIST` แบ่งรายการที่ระบุเป็นชุดย่อย (หรือชุดงาน) ซึ่งแต่ละชุดประกอบด้วยจำนวนเรกคอร์ดที่ระบุ จากนั้นจะส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่ที่ประกอบด้วยชุดงาน

## <a name="syntax-1"></a>ไวยากรณ์ 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>ไวยากรณ์ 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`list`: *รายการเรกคอร์ด*

พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*

`number`: *เลขจำนวนเต็ม*

จำนวนสูงสุดของเรกคอร์ดต่อชุดงาน

`on-demand reading flag`: *บูลีน*

ค่า *บูลีน* ที่ระบุว่าควรมีการสร้างองค์ประกอบของรายการย่อยตามความต้องการหรือไม่

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

รายการของชุดงานที่ส่งคืนประกอบด้วยองค์ประกอบต่อไปนี้:

 - **ค่า:** *รายการ*

    รายการของเรกคอร์ดที่เป็นของชุดงานปัจจุบัน

- **Batchnumber:** *จำนวนเต็ม*

    หมายเลขของชุดงานปัจจุบันในรายการที่ส่งคืน

เมื่อตั้งค่าแฟล็กการอ่านตามความต้องการเป็น **จริง** รายการย่อยจะถูกสร้างขึ้นตามการร้องขอ ซึ่งอนุญาตให้ลดปริมาณการใช้หน่วยความจํา แต่อาจทําให้ประสิทธิภาพการลดลง ถ้าองค์ประกอบไม่ได้ถูกใช้ตามลำดับ

## <a name="example"></a>ตัวอย่าง

ในภาพประกอบต่อไปนี้ แหล่งข้อมูล **รายการ** ถูกสร้างเป็นรายการเรกคอร์ดที่มีสามเรกคอร์ด รายการนี้จะถูกแบ่งออกเป็นชุดงาน ซึ่งแต่ละชุดงานประกอบด้วยเรกคอร์ดสองรายการ

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

ภาพประกอบต่อไปนี้แสดงโครงร่างรูปแบบที่มีการออกแบบ ในโครงร่างนี้รูปแบบ การผูกกับแหล่งข้อมูล **รายการ** ถูกสร้างเพื่อสร้างเอาท์พุทในรูปแบบ XML เอาท์พุทนี้แสดงโหนดแต่ละโหนดสำหรับแต่ละชุดงานและเรกคอร์ดในนั้น

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการออกแบบ

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
