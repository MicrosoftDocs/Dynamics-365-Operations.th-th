---
title: รายการปริมาณคงคลังคงเหลือ
description: บทความนี้จะอธิบายวิธีการใช้หน้ารายการปริมาณคงคลังคงเหลือ เพื่อตรวจสอบรายละเอียดปริมาณคงคลังคงเหลือ ซึ่งแสดงให้เห็นถึงวิธีการที่ตัวเลือกการกรองข้อมูลและการเรียงลำดับต่างๆ ทำงานร่วมกัน และวิธีที่ตัวเลือกเหล่านี้อาจทำให้เกิดผลลัพธ์ที่ไม่คาดคิดเมื่อรวมกันในบางครั้ง
author: yufeihuang
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 5747ae985e1791de8ddd93b678c2449a4a1802da
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879061"
---
# <a name="inventory-on-hand-list"></a>รายการปริมาณคงคลังคงเหลือ

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการใช้หน้า **รายการปริมาณคงคลังคงเหลือ** เพื่อตรวจสอบรายละเอียดปริมาณคงคลังคงเหลือ ซึ่งแสดงให้เห็นถึงวิธีการที่ตัวเลือกการกรองข้อมูลและการเรียงลำดับต่างๆ ทำงานร่วมกัน และวิธีที่ตัวเลือกเหล่านี้อาจทำให้เกิดผลลัพธ์ที่ไม่คาดคิดเมื่อรวมกันในบางครั้ง

## <a name="query-your-on-hand-inventory"></a>สอบถามปริมาณคงคลังคงเหลือของคุณ

เมื่อต้องการตรวจสอบความพร้อมใช้งานของสินค้าคงคลัง ให้ไปที่ **การจัดการสินค้าคงคลัง \> การสอบถามและรายงาน \> รายการปริมาณคงคลังคงเหลือ**

หน้า **รายการปริมาณคงคลังคงเหลือ** จะถูกอัพเดตโดยอัตโนมัติ เมื่อมีการทำธุรกรรมในสินค้าคงคลัง ธุรกรรมดังกล่าวอาจเป็นธุรกรรมที่คาดการณ์ไว้ ธุรกรรมจริง หรือธุรกรรมทางการเงิน

ใช้เครื่องมือต่อไปนี้เพื่อค้นหาชุดของผลิตภัณฑ์ที่คุณกำลังค้นหา:

- ในบานหน้าต่างการดำเนินการให้เลือก [**มิติ**](#dimensions) เพื่อเปิดกล่องโต้ตอบที่คุณสามารถเพิ่มหรือลบคอลัมน์ที่แสดงอยู่ใน กริด **ปริมาณคงคลังคงเหลือ**
- ใน [บานหน้าต่าง **ตัวกรอง**](#filters-pane) ให้ป้อนค่าสำหรับฟิลด์เฉพาะ เพื่อแสดงเฉพาะเรกคอร์ดที่ตรงกับค่าเหล่านั้น โปรดทราบว่า ตัวกรองที่คุณกำหนดที่นี่จะใช้กับตารางต้นทางที่อาจรวมไว้ในภายหลัง ตามมิติที่คุณเลือกไว้เพื่อแสดง สำหรับข้อมูลเกี่ยวกับลักษณะการทำงานนี้ อาจส่งผลกระทบต่อผลลัพธ์ของคุณ ให้ดู [ตัวอย่าง](#examples) ในตอนท้ายของบทความนี้
- ในบานหน้าต่าง **ตัวกรอง** ให้เลือก **ใช้** เพื่อสร้างรายการของปริมาณคงคลังคงเหลือที่ตรงกัน ในกริด **ปริมาณคงคลังคงเหลือ**
- ในกริด **ปริมาณคงคลังคงเหลือ** ให้เลือกส่วนหัวของคอลัมน์ใดๆ เพื่อเรียงลำดับหรือกรองตามค่าในคอลัมน์นั้น QuickFilter ที่ด้านบนของกริด ให้ตัวเลือกการกรองข้อมูลเพิ่มเติม ตัวกรองข้อมูลเหล่านี้จะนำไปใช้กับผลลัพธ์ ไม่ใช่ตารางต้นทาง สำหรับข้อมูลเกี่ยวกับลักษณะการทำงานนี้ อาจส่งผลกระทบต่อผลลัพธ์ของคุณ ให้ดู [ตัวอย่าง](#examples) ในตอนท้ายของบทความนี้

สำหรับสินค้าแต่ละรายการที่ตรงกัน กริด **ปริมาณคงคลังคงเหลือ** จะมีคอลัมน์ของข้อมูลสินค้าคงคลัง ต่อไปนี้

| คอลัมน์ | คำอธิบาย |
|---|---|
| สินค้าคงคลังที่มีอยู่จริง | ปริมาณตามจริงที่พร้อมใช้งานในสินค้าคงคลัง |
| ที่จองจริง | ปริมาณรวมทั้งหมดที่มีการจองตามจริง |
| ที่มีอยู่จริง | ปริมาณที่พร้อมใช้งาน (ไม่ได้จอง) ที่พร้อมใช้งานในสินค้าคงคลังที่มีอยู่จริง<p>**ปริมาณตามจริงที่พร้อมใช้งาน** เป็นฟิลด์ที่คำนวณได้ ค่า เท่ากับ ค่า **สินค้าคงคลังที่มีอยู่จริง** ลบด้วย ค่า **การจองตามจริง**</p> |
| ที่มีอยู่จริงบนมิติพิเศษ | ปริมาณตามจริงพร้อมใช้งานสำหรับมิติทั้งหมดที่แสดงอยู่ในกริด |
| ผลรวมที่สั่ง | ปริมาณรวมทั้งหมดที่รวมอยู่ในใบสั่งขาเข้า หรือที่มีปริมาณบวกในสมุดรายวันสินค้าคงคลังต่างๆ |
| อยู่ระหว่างการสั่ง | ปริมาณรวมทั้งหมดที่รวมอยู่ในใบสั่งขาออก หรือที่มีปริมาณลบในสมุดรายวันสินค้าคงคลังต่างๆ |
| สำรองตามใบสั่งแล้ว | ปริมาณรวมที่จองไว้ในใบรับสินค้าที่สั่ง ค่าในฟิลด์นี้แสดงถึงปริมาณรวมของสินค้าในธุรกรรมขาออกที่มีสถานะเป็น _สำรองตามใบสั่งแล้ว_ สินค้าที่จองไว้ตามที่สั่งไม่มีอยู่จริงในสินค้าคงคลัง ดังนั้น จึงไม่สามารถเบิกสินค้าและจัดส่งโดยตรงได้ |
| พร้อมสำหรับการจอง | ปริมาณรวมของปริมาณคงคลังคงเหลือที่สามารถจองได้<p>**หมายเหตุ:** ถ้า กล่องกาเครื่องหมาย **สำรองสินค้าที่สั่ง** ถูกเลือกไว้ บนหน้า **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** ค่าในฟิลด์นี้จะรวมถึงการรับสินค้าที่คาดไว้ ถ้ากล่องกาเครื่องหมายไม่ถูกเลือก ค่าจะไม่รวมการรับสินค้าที่คาดไว้</p> |
| รวมปริมาณที่พร้อมใช้งาน | ปริมาณที่พร้อมใช้งานรวม<p>**ปริมาณที่พร้อมใช้งาน** เป็นฟิลด์ที่คำนวณได้ ค่า เท่ากับ ค่า **ค่าที่มีอยู่จริง** บวกกับ ค่า **ผลรวมที่สั่ง** ลบด้วย ค่า **อยู่ระหว่างการสั่ง**</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>ใช้ตัวกรองข้อมูลเพื่อค้นหาเรกคอร์ดที่คุณกำลังค้นหา

ใช้ บานหน้าต่าง **ตัวกรอง** เพื่อกรองข้อมูลรายการปริมาณคงคลังคงเหลือ เพื่อให้รวมเฉพาะเรกคอร์ดที่มีค่าฟิลด์ตรงกันกับเงื่อนไขการกรองข้อมูล การกำหนดตัวกรอง ให้ทำตามขั้นตอนเหล่านี้

1. ใน บานหน้าต่าง **ตัวกรอง** ให้ค้นหาฟิลด์ที่คุณต้องการกรองข้อมูล
2. ในฟิลด์ด้านล่างชื่อของฟิลด์เป้าหมาย ให้เลือกตัวดำเนินการทางตรรกะ (ตัวอย่าง เช่น *เริ่มต้นด้วย* *เท่ากับ* หรือ *มากกว่า*)
3. ป้อนหรือเลือกค่าที่จะค้นหา

> [!IMPORTANT]
> หน้า **รายการปริมาณคงคลังคงเหลือ** ประกอบด้วยตารางปริมาณคงคลังคงเหลือที่มีรายละเอียด ซึ่งรวมมิติที่มีอยู่ทั้งหมด อย่างไรก็ตาม รายการบนหน้านี้เป็นข้อมูลสรุป ดังนั้น จึงอาจรวมแถวจากตารางต้นทางตามค่ารวมตามมิติที่แสดง
>
> ตัวกรองที่คุณกำหนดใน บานหน้าต่าง **ตัวกรอง** จะนำไปใช้กับตารางต้นทาง ไม่ใช่รายการที่รวม ลักษณะการทำงานนี้บางครั้งอาจสร้างผลลัพธ์ที่ไม่คาดคิด สำหรับข้อมูลเกี่ยวกับลักษณะการทำงานนี้ อาจส่งผลกระทบต่อผลลัพธ์ของคุณ ให้ดู [ตัวอย่าง](#examples) ในตอนท้ายของบทความนี้
> 
> อย่างไรก็ตาม [ตัวกรองที่ระบุไว้ในกริด](#grid-filters) *จะถูก* ใช้กับรายการแบบรวม ตัวกรองเหล่านี้รวมทั้ง QuickFilter ที่ด้านบนของกริด และตัวกรองสำหรับแต่ละส่วนหัวของคอลัมน์

คุณสามารถปรับเปลี่ยนชุดของตัวกรองที่มีอยู่ในบานหน้าต่าง **ตัวกรอง** โดยทำตามขั้นตอนต่อไปนี้

- ถ้าต้องการลบตัวกรองจากบานหน้าต่าง ให้เลือกปุ่ม **ปิด** (**X**)
- เมื่อต้องการเพิ่มตัวกรอง ให้เลือก **เพิ่ม** ที่ด้านบนของบานหน้าต่าง **ตัวกรอง** กล่องโต้ตอบ **เพิ่มฟิลด์ตัวกรอง** ที่ปรากฏ จะแสดงรายการของฟิลด์ที่พร้อมใช้งาน นอกจากนี้ยังแสดงข้อมูลเกี่ยวกับชนิดและตารางข้อมูลสำหรับแต่ละฟิลด์ด้วย ใช้ส่วนหัวของคอลัมน์เพื่อกรองข้อมูลและเรียงลำดับรายการตามที่คุณต้องการ แล้วเลือกกล่องกาเครื่องหมายสำหรับแต่ละฟิลด์ที่คุณต้องการเพิ่มลงในบานหน้าต่าง **ตัวกรอง** เมื่อดำเนินการเสร็จสิ้นแล้ว ให้เลือก **แทรก** เพื่อใช้การเปลี่ยนแปลงของคุณ

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>เลือกมิติที่จะแสดง

มิติจะบอกให้คุณทราบถึงสินค้าแต่ละรายการในรายการปริมาณคงคลังคงเหลือ และช่วยให้คุณสามารถเรียงลำดับและกรองข้อมูลรายการได้มากขึ้น มิติที่คุณเลือกเพื่อแสดงจะมีผลต่อวิธีการรวมแถวบนหน้า **รายการปริมาณคงคลังคงเหลือ** การรวมนี้ อาจส่งผลกระทบต่อวิธีการรวมแถวจากตารางต้นทางเข้ากับผลลัพธ์ที่คุณเห็น สำหรับข้อมูลเกี่ยวกับลักษณะการทำงานนี้ อาจส่งผลกระทบต่อผลลัพธ์ของคุณ ให้ดู [ตัวอย่าง](#examples) ในตอนท้ายของบทความนี้

เมื่อต้องการกำหนดการเลือกของมิติสินค้าคงคลังที่จะแสดงขึ้น ให้ทำตามขั้นตอนต่อไปนี้

1. บนบานหน้าต่างการดำเนินการ เลือก **มิติ**

    กล่องโต้ตอบ **แสดงมิติ** ที่ปรากฏขึ้นจะแสดงมิติทั้งหมด

2. เลือกกล่องกาเครื่องหมายของแต่ละมิติที่คุณต้องการใส่ไว้ในกริด
3. ถ้าคุณต้องการให้การเลือกของคุณใช้เป็นค่าเริ่มต้นในครั้งถัดไปที่คุณเปิดหน้า **รายการปริมาณคงคลังคงเหลือ** ให้ตั้งค่าตัวเลือก **บันทึกการตั้งค่า** เป็น **ใช่** ถ้าคุณตั้งค่าตัวเลือกนี้ เป็น **ไม่** การเลือกของคุณจะถูกใช้ในระหว่างรอบเวลาปัจจุบันเท่านั้น ดังน้น ในครั้งถัดไปที่คุณเปิดหน้า การเลือกเริ่มต้นปัจจุบันจะถูกนำมาใช้
4. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ และใช้การเปลี่ยนแปลงของคุณ

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>กรองผลลัพธ์ของรายการปริมาณสินค้าคงคลังคงเหลือ

คุณสามารถเลือกส่วนหัวของคอลัมน์ใดๆ ในกริด **ปริมาณคงคลังคงเหลือ** เพื่อเรียงลำดับหรือกรองตามค่าในคอลัมน์นั้น QuickFilter ที่ด้านบนของกริด ให้ตัวเลือกการกรองข้อมูลเพิ่มเติม ตัวกรองข้อมูลเหล่านี้จะนำไปใช้กับผลลัพธ์ ไม่ใช่ตารางต้นทาง สำหรับข้อมูลเกี่ยวกับลักษณะการทำงานนี้ อาจส่งผลกระทบต่อผลลัพธ์ของคุณ ให้ดู [ตัวอย่าง](#examples) ในตอนท้ายของบทความนี้

> [!NOTE]
> คุณสามารถกรองและเรียงลำดับโดยคอลัมน์ทั้งหมดได้ คอลัมน์ปริมาณส่วนใหญ่ไม่มีตัวควบคุมการเรียงลำดับและการกรอง เนื่องจากเป็นฟิลด์ที่คำนวณได้ คอลัมน์ **อยู่ระหว่างการสั่ง** เป็นข้อยกเว้น

## <a name="examples"></a><a name="examples"></a>ตัวอย่างเช่น

ระบบของคุณรวมตารางสินค้าคงคลังที่มีรายละเอียด (ที่ไม่ใช่) ซึ่งแสดงปริมาณคงคลังคงเหลือต่อไปนี้

| หมายเลขสินค้า | ไซต์ | คลังสินค้า | สินค้าคงคลังที่มีอยู่จริง | ที่มีอยู่จริง |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>สถานการณ์จำลอง 1

หน้า **รายการปริมาณคงคลังคงเหลือ** ถูกตั้งค่าให้แสดงมิติขั้นสุดท้ายต่อไปนี้:

- หมายเลขสินค้า
- ไซต์
- คลังสินค้า

ในบานหน้าต่าง **ตัวกรอง** เงื่อนไขการกรองข้อมูลต่อไปนี้มีการตั้งค่าดังนี้:

- **หมายเลขสินค้า** \| **คือ** \| _IA0001_
- **มีอยู่จริง** \| **น้อยกว่าหรือเท่ากับ** \| _1_

ต่อไปนี้เป็นผลลัพธ์ที่ได้

| หมายเลขสินค้า | ไซต์ | คลังสินค้า | สินค้าคงคลังที่มีอยู่จริง | ที่มีอยู่จริง |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>สถานการณ์จำลอง 2

หน้า **รายการปริมาณคงคลังคงเหลือ** ถูกตั้งค่าให้แสดงมิติขั้นสุดท้ายต่อไปนี้:

- หมายเลขสินค้า
- ไซต์

ในบานหน้าต่าง **ตัวกรอง** เงื่อนไขการกรองข้อมูลต่อไปนี้มีการตั้งค่าดังนี้:

- **หมายเลขสินค้า** \| **คือ** \| _IA0001_
- **มีอยู่จริง** \| **น้อยกว่าหรือเท่ากับ** \| _1_

ต่อไปนี้เป็นผลลัพธ์ที่ได้

| หมายเลขสินค้า | ไซต์ | สินค้าคงคลังที่มีอยู่จริง | ที่มีอยู่จริง |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

โปรดทราบว่าการตั้งค่าในบานหน้าต่าง **ตัวกรอง** จะใช้กับตารางสินค้าคงคลังที่มีรายละเอียด (ที่ไม่รวม) ซึ่งแสดงอยู่ในตอนต้นของส่วนนี้ ดังนั้น เงื่อนไข **มีอยู่จริง** \| **น้อยกว่าหรือเท่ากับ** \| _1_ พบแถวสองแถวจากตารางนั้น (แถวแรกและแถวที่สาม ซึ่งแสดง **ที่มีอยู่จริง** ค่าของ _1_) อย่างไรก็ตาม ในสถานการณ์สมมตินี้ หน้า **รายการปริมาณคงคลังคงเหลือ** ไม่ได้ถูกตั้งค่าให้แสดงมิติ **คลังสินค้า** ดังนั้น จึงรวมแถวดั้งเดิมสองแถวไว้ในแถวผลลัพธ์เดี่ยว เนื่องจากแถวทั้งสองจะมีค่าเหมือนกันในมิติทั้งหมดที่แสดง แถวนี้จะปรากฏขึ้นเพื่อละเมิดเงื่อนไขการกรองข้อมูล เนื่องจากค่า **ที่มีอยู่จริง** แสดงเป็น _2_ อย่างไรก็ตาม ผลลัพธ์มีความถูกต้อง เนื่องจากการตั้งค่าในบานหน้าต่าง **ตัวกรอง** ใช้กับตารางต้นทาง ไม่ใช่ตารางรวมที่แสดงอยู่บนหน้า **ปริมาณคงคลังคงเหลือ**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]