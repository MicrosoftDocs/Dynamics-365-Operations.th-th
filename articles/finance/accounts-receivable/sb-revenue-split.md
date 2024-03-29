---
title: เทมเพลตการแบ่งส่วนรายได้ในการเรียกเก็บเงินตามการสมัครใช้งาน
description: บทความนี้อธิบายวิธีการตั้งค่าเทมเพลตการแบ่งส่วนรายได้สำหรับสินค้าที่ขายเป็นชุดรวม
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904772"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>เทมเพลตการแบ่งส่วนรายได้ในการเรียกเก็บเงินตามการสมัครใช้งาน

ใช้หน้า **เทมเพลตการแบ่งส่วนรายได้** เพื่อตั้งค่าเทมเพลตสำหรับการแบ่งส่วนรายได้ การแบ่งรายได้ประกอบด้วยสินค้าหลักที่มีสินค้ารอง สินค้าชนิดนี้มักขายให้ลูกค้าเป็นสินค้าชิ้นเดียวหรือชุดรวม

ตัวอย่างเช่น คุณสามารถสร้างรายการสินค้าคอมพิวเตอร์ในลักษณะต่อไปนี้

- **สินค้าหลัก:** การสมัครใช้งานระดับ Silver
- **สินค้าในรายการ (รอง):**

    - การสนับสนุน
    - การบำรุงรักษา
    - ใบอนุญาต

เมื่อคุณสร้างสินค้าหลัก ควรระลึกข้อจํากัดต่อไปนี้

- สามารถระบุสินค้าเป็นสินค้าหลักได้ในเวลาเดียวกัน
- คุณสามารถเลือกสินค้าหลักเป็นสินค้ารองในเทมเพลตเดียวกันได้
- เทมเพลตที่ถูกต้องต้องมีสินค้ารองอย่างน้อยหนึ่งรายการ
- สามารถระบุสินค้าเป็นสินค้ารองของสินค้าชุดรวมมากกว่าหนึ่งรายการ
- ความสัมพันธ์หลัก-รองแต่ละรายการต้องไม่ซ้ำกัน

## <a name="create-a-parent-item-that-has-child-items"></a>สร้างสินค้าหลักที่มีสินค้ารอง

ทำตามขั้นตอนเหล่านี้เพื่อสร้างสินค้าหลักที่มีสินค้ารอง

1. บนหน้า **เทมเพลตการแบ่งส่วนรายได้** ให้เลือก **ใหม่**
1. ในฟิลด์ **สินค้าหลัก** ให้เลือกสินค้าหลัก ฟิลด์ **หมายเลขตัวแปร** มีการอัปเดตโดยอัตโนมัติ คุณสามารถเปลี่ยนค่าได้ตามที่คุณต้องการ
1. ในฟิลด์ **วิธีการปันส่วน** ให้เลือกวิธีการปันส่วน
1. ในรายการ **สินค้าส่วนประกอบ** ให้เลือก **เพิ่ม** เพื่อเพิ่มสินค้ารอง
1. หากคุณเลือก **เปอร์เซ็นต์** ในฟิลด์ **วิธีการปันส่วน** ให้ระบุเปอร์เซ็นต์ในฟิลด์ **เปอร์เซ็นต์**

    - ถ้าคุณเลือก **จำนวนเงินที่เท่ากัน** ในฟิลด์ **วิธีการปันส่วน** ฟิลด์ **เปอร์เซ็นต์** จะมีการอัปเดตโดยอัตโนมัติเพื่อให้สินค้าทุกรายการมีเปอร์เซ็นต์ที่เท่ากัน
    - หากคุณเลือก **จำนวนเงินผันแปร**, **จำนวนเงินหลักเป็นศูนย์** หรือ **จำนวนเงินเป็นศูนย์** ในฟิลด์ **วิธีการปันส่วน** ค่าของฟิลด์ **เปอร์เซ็นต์** จะยังคงเป็น **0** (ศูนย์) และไม่สามารถเปลี่ยนได้

1. เลือก **บันทึก**

## <a name="fields"></a>ฟิลด์

หน้า **เทมเพลตการแบ่งส่วนรายได้** ประกอบด้วยฟิลด์ต่อไปนี้

| ฟิลด์ | คำอธิบาย |
|-------|-------------|
| รายการหลัก | เลือกหมายเลขสินค้า สินค้านี้จะกลายเป็นสินค้าหลักของสินค้าชุดรวมที่คุณสร้าง |
| ชื่อผลิตภัณฑ์ | ชื่อผลิตภัณฑ์ |
| วิธีการปันส่วน | <p>เลือกวิธีการปันส่วน</p><ul><li>**จํานวนเงินที่เท่ากัน** – เปอร์เซ็นต์การปันส่วนจะถูกคํานวณโดยอัตโนมัติและแบ่งเท่าๆ กันระหว่างสินค้าทั้งหมดในเทมเพลต</li><li>**เปอร์เซ็นต์** – คุณสามารถระบุจํานวนเปอร์เซ็นต์สำหรับการปันส่วนได้ ผลรวมของเปอร์เซ็นต์ทั้งหมดต้องเท่ากับ 100</li><li>**จำนวนเงินผันแปร** – สินค้ารองที่เพิ่มมียอดเงินสุทธิเป็น 0 (ศูนย์) ต้องระบุราคาของสินค้ารองในระดับธุรกรรม</li><li>**จำนวนเงินเป็นศูนย์** – สินค้าหลักคงราคาต่อหน่วยและยอดเงินสุทธิของสินค้านั้น สินค้ารองทั้งหมดมียอดเงินสุทธิเป็น 0 (ศูนย์)</li><li>**จำนวนเงินหลักเป็นศูนย์** – สินค้าหลักมียอดเงินสุทธิคงที่เป็น 0 (ศูนย์) สินค้ารองทั้งหมดจะถือว่าเป็นสินค้ามาตรฐาน ไม่มีการตรวจสอบความถูกต้องเพื่อตรวจสอบว่าผลรวมของจำนวนเงินของสินค้ารองเท่ากับจำนวนเงินของสินค้าหลักหรือไม่</li></ul> |
| **รายการข้อมูลที่เป็นส่วนประกอบ** | |
| รายการข้อมูลที่เป็นส่วนประกอบ | เลือกหมายเลขสินค้า สินค้านี้เป็นรายการสินค้ารอง |
| หมายเลขตัวแปร | เลือกหมายเลขตัวแปรสำหรับสินค้า |
| ชื่อผลิตภัณฑ์ | ชื่อผลิตภัณฑ์ |
| เปอร์เซ็นต์ | <p>เปอร์เซ็นต์การปันส่วนสำหรับหลักเป้าหมาย:</p><ul><li>ถ้าฟิลด์ **วิธีการปันส่วน** ตั้งค่าเป็น **เปอร์เซ็นต์** คุณสามารถระบุเปอร์เซ็นต์ได้</li><li>หากฟิลด์ **วิธีการปันส่วน** ตั้งค่าเป็น **จำนวนเงินเท่ากัน** เปอร์เซ็นต์จะถูกคำนวณโดยอัตโนมัติเพื่อให้สินค้าทุกรายการในเทมเพลตมีเปอร์เซ็นต์ที่เท่ากัน</li><li>ถ้าฟิลด์ **วิธีการปันส่วน** ตั้งค่าเป็น **จำนวนเงินผันแปร**, **จํานวนเงินหลักเป็นศูนย์** หรือ **จำนวนเงินเป็นศูนย์** เปอร์เซ็นต์จะเป็น 0 (ศูนย์) และแก้ไขไม่ได้</li></ul><p>ค่าของฟิลด์นี้สามารถเป็นตัวเลขค่าบวกใดๆ ระหว่าง 0 (ศูนย์) ถึง 100 ผลรวมของเปอร์เซ็นต์ทั้งหมดต้องเท่ากับ 100</p> |
| เปอร์เซ็นต์รวม | <p>ผลรวมของค่าในคอลัมน์ **เปอร์เซ็นต์**</p><ul><li>ถ้าฟิลด์ **วิธีการปันส่วน** ตั้งค่าเป็น **จำนวนเงินที่เท่ากัน** หรือ **เปอร์เซ็นต์** ผลรวมของเปอร์เซ็นต์ต้องเท่ากับ 100</li><li>ถ้าฟิลด์ **วิธีการปันส่วน** ตั้งค่าเป็น **จำนวนเงินผันแปร**, **จํานวนเงินหลักเป็นศูนย์** หรือ **จำนวนเงินเป็นศูนย์** เปอร์เซ็นต์รวมจะเป็น 0 (ศูนย์)</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>การแบ่งส่วนรายได้ในใบสั่งขาย

เมื่อต้องการสร้างใบสั่งขายที่มีสินค้าซึ่งตั้งค่าให้แบ่งส่วนรายได้ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. บนหน้า **ใบสั่งขาย** ให้สร้างใบสั่งขาย
2. ในรายการของสินค้าแต่ละรายการที่ตั้งค่าให้แบ่งส่วนรายได้ ให้เลือกกล่องกาเครื่องหมาย **การแบ่งส่วนรายได้** สินค้านั้นจะกลายเป็นสินค้าหลัก ถ้ามีการตั้งค่าเทมเพลตไว้แล้ว สินค้ารายการรองจะปรากฏในรายการโดยอัตโนมัติ
3. เมื่อต้องการเพิ่มสินค้ารายการรองเพิ่มเติม ให้เลือก **เพิ่มรายการรองการแบ่งส่วนรายได้** และเลือกสินค้ารายการรองที่คุณต้องการเพิ่ม
4. บันทึกใบสั่ง

## <a name="revenue-split-with-billing-schedules"></a>การแบ่งส่วนรายได้ที่มีกำหนดการเรียกเก็บเงิน

เมื่อต้องการสร้างกำหนดการเรียกเก็บเงินที่มีสินค้าซึ่งตั้งค่าให้แบ่งส่วนรายได้ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. บนหน้า **กำหนดการเรียกเก็บเงินทั้งหมด/ที่ใช้งานอยู่** ให้สร้างกำหนดการเรียกเก็บเงิน
2. ในรายการของสินค้าแต่ละรายการที่ตั้งค่าให้แบ่งส่วนรายได้ ให้เลือกกล่องกาเครื่องหมาย **การแบ่งส่วนรายได้** สินค้านั้นจะกลายเป็นสินค้าหลัก ถ้ามีการตั้งค่าเทมเพลตไว้แล้ว สินค้ารายการรองจะปรากฏในรายการโดยอัตโนมัติ
3. เมื่อต้องการเพิ่มสินค้ารายการรองเพิ่มเติม ให้เลือก **เพิ่มรายการรองการแบ่งส่วนรายได้** และเลือกสินค้ารายการรองที่คุณต้องการเพิ่ม
4. ปฏิบัติตามขั้นตอนต่างๆ ต่อไปเพื่อใช้งานกำหนดการเรียกเก็บเงิน

> [!NOTE]
> หากตัวเลือก **สร้างการแบ่งส่วนรายได้โดยอัตโนมัติ** ตั้งค่าเป็น **ใช่** ในหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ** จะมีการดำเนินการต่อไปนี้:
>
> - หากสินค้าในรายการตั้งค่าเป็นสินค้าหลักในเทมเพลตการแบ่งส่วนรายได้ กล่องกาเครื่องหมาย **การแบ่งส่วนรายได้** จะมีการเลือกโดยอัตโนมัติ
> - สินค้ารองจะถูกป้อนโดยอัตโนมัติในรายการใบสั่งขายหรือกำหนดการเรียกเก็บเงิน
>
> หากตัวเลือก **สร้างการแบ่งส่วนรายได้โดยอัตโนมัติ** ตั้งค่าเป็น **ไม่** ลักษณะการทำงานจะเป็นตามที่อธิบายไว้ก่อนหน้านี้

## <a name="additional-revenue-split-information"></a>ข้อมูลการแบ่งส่วนรายได้เพิ่มเติม

เมื่อคุณเพิ่มสินค้าที่เป็นส่วนหนึ่งของการแบ่งรายได้ ให้จดบันทึกข้อมูลต่อไปนี้ 

- จำนวนเงินหลักไม่สามารถรอการตัดบัญชี
- วันที่เริ่มต้น วันที่สิ้นสุด ปริมาณ หน่วย ไซต์ และค่าคลังสินค้าของสินค้ารองยึดตามสินค้าหลัก ไม่สามารถเปลี่ยนค่าเหล่านี้ให้กับสินค้ารอง การเปลี่ยนแปลงต้องทำกับสินค้าหลักทั้งหมด 
- วิธีการกําหนดราคาจะเป็น **แบบคงที่** ซึ่งไม่สามารถเปลี่ยนแปลงได้
- สินค้ารองสามารถเพิ่มหรือลบได้
- สินค้าหลักและสินค้ารองต้องใช้กลุ่มสินค้าเดียวกัน 
- สินค้ารองอาจมีการตั้งค่าอย่างใดอย่างหนึ่งดังนี้

    - ฟิลด์ **ความถี่ในการเรียกเก็บเงิน** และ **ช่วงเวลาการเรียกเก็บเงิน** จะถูกตั้งค่าเป็นค่าเดียวกันกับสินค้าหลัก 
    - ฟิลด์ **ความถี่ในการเรียกเก็บเงิน** ตั้งค่าเป็น **ครั้งเดียว** ในกรณีนี้ จะมีการตั้งค่าในฟิลด์ **ช่วงเวลาการเรียกเก็บเงิน** โดยอัตโนมัติเท่ากับ **1** 

- ผลรวมของยอดเงินสุทธิของสินค้ารองเท่ากับยอดเงินหลัก หากวิธีการปันส่วนเป็น **ยอดเงินศูนย์** ทั้งยอดเงินของสินค้ารองและยอดเงินสินค้าหลักจะเป็น 0 (ศูนย์) 

    > [!NOTE]
    > หากวิธีการปันส่วนเป็น **จำนวนเงินหลักเป็นศูนย์** ผลรวม (ไม่ใช่ศูนย์) ของสินค้ารองไม่เท่ากับจำนวนเงินหลัก ซึ่งเป็น 0 (ศูนย์) วิธีการปันส่วนนี้จะใช้เพื่อวัตถุประสงค์ภายใน เพื่อให้พนักงานสามารถดูสินค้ารองได้ แต่ลูกค้าสามารถดูได้เฉพาะสินค้าหลักเท่านั้น

- ถ้าชนิดการจัดเตรียมแบบหลายองค์ประกอบ (MEA) ของใบสั่งขายเป็น **รายการเดียว** รายการธุรกรรมการปันส่วนรายได้หลายองค์ประกอบที่สอดคล้องกันจะถูกสร้างขึ้นเมื่อมีการเพิ่มสินค้าหลักและสินค้ารอง 
- ถ้าวิธีการปันส่วนการแบ่งรายได้เป็น **จำนวนเงินที่เท่ากัน** และจำนวนเงินหลักมีการเปลี่ยนแปลง จํานวนเงินจะถูกคำนวณใหม่ให้กับรายการรองทั้งหมด 
- สำรับการแบ่งรายได้โดยวิธีการปันส่วนเป็น **จํานวนเงินผันแปร** ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น

    - ยอดเงินสุทธิของสินค้าหลักจะปรากฏในคอลัมน์ **จำนวนเงินหลัก** ค่านี้สามารถแก้ไขได้ อย่างไรก็ตาม ราคาต่อหน่วย ยอดเงินสุทธิ และส่วนลดคือ 0 (ศูนย์) และแก้ไขไม่ได้
    - ราคาต่อหน่วยของสินค้ารองคือ 0 (ศูนย์) คุณสามารถแก้ไขราคาต่อหน่วยหรือยอดเงินสุทธิได้ เมื่อคุณแก้ไขค่าหนึ่ง ค่าอื่นๆ จะถูกอัปเดตโดยอัตโนมัติ

- สำรับการแบ่งรายได้โดยวิธีการปันส่วนเป็น **เปอร์เซ็นต์** ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น

    - ยอดเงินสุทธิของสินค้าหลักจะปรากฏในคอลัมน์ **จำนวนเงินหลัก** ค่านี้สามารถแก้ไขได้ อย่างไรก็ตาม ราคาต่อหน่วย ยอดเงินสุทธิ และส่วนลดคือ 0 (ศูนย์) และแก้ไขไม่ได้ 
    - ยอดเงินสุทธิของสินค้ารองถูกคํานวณเป็น *เปอร์เซ็นต์* &times; *จำนวนเงินหลัก*

- สำรับการแบ่งรายได้โดยวิธีการปันส่วนเป็น **จํานวนเงินที่เท่ากัน** ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น

    - ยอดเงินสุทธิของสินค้าหลักจะปรากฏในคอลัมน์ **จำนวนเงินหลัก** ค่านี้สามารถแก้ไขได้ อย่างไรก็ตาม ราคาต่อหน่วย ยอดเงินสุทธิ และส่วนลดคือ 0 (ศูนย์) และแก้ไขไม่ได้ 
    - ยอดเงินสุทธิของสินค้ารองคํานวณโดยการหารยอดเงินหลักเท่าๆ กันระหว่างสินค้ารองทั้งหมด 
    - ถ้ามีลบหรือเพิ่มสินค้ารอง ยอดเงินสุทธิและราคาต่อหน่วยจะถูกคำนวณใหม่เพื่อให้สินค้ารองทั้งหมดมีจํานวนเงินที่เท่ากัน 
    - ถ้าไม่สามารถแบ่งจํานวนเงินหลักเท่าๆ กัน ได้ ยอดเงินสุทธิและราคาต่อหน่วยของสินค้ารองล่าสุดอาจน้อยกว่ายอดเงินสุทธิและราคาต่อหน่วยของสินค้ารองอื่นๆ เล็กน้อย 

- สำรับการแบ่งรายได้โดยวิธีการปันส่วนเป็น **จำนวนเงินเป็นศูนย์** ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น

    - ราคาต่อหน่วย ยอดเงินสุทธิ และส่วนลดสามารถแก้ไขได้ จำนวนเงินหลักคือ 0 (ศูนย์) และแก้ไขไม่ได้ 
    - ปริมาณ หน่วย ไซต์ และค่าคลังสินค้าของสินค้ารองยึดตามสินค้าหลัก คุณไม่สามารถเปลี่ยนค่าเหล่านี้ให้กับสินค้ารอง การเปลี่ยนแปลงต้องทำกับสินค้าหลักทั้งหมด 
    - ราคาต่อหน่วยและราคาสุทธิของสินค้ารองคือ 0 (ศูนย์) และแก้ไขไม่ได้ 

- สำรับการแบ่งรายได้โดยวิธีการปันส่วนเป็น **จำนวนเงินหลักเป็นศูนย์** ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น

    - ราคาต่อหน่วย สินค้าหลัก และยอดเงินสุทธิของสินค้าหลักนั้นเป็น 0 (ศูนย์)
    - ในกำหนดการเรียกเก็บเงิน รายการรองจะปรากฏเหมือนกับว่ารายการเหล่านั้นถูกเพิ่มด้วยตนเอง และมีการอัปเดตค่าทั้งหมดตามกลุ่มกำหนดการเรียกเก็บเงินที่เลือก ค่าเหล่านี้สามารถแก้ไขได้ สำหรับสินค้ารอง คุณสามารถเข้าถึงตัวเลือก **การเลื่อนระดับและส่วนลด** และ **การกำหนดราคาขั้นสูง** โดยใช้ฟิลด์ **ปริมาณที่ป้อน** **ราคาต่อหน่วย** **ส่วนลด** และ **ยอดเงินสุทธิ** ใน **ดูรายละเอียดการเรียกเก็บเงิน** 
    - ในใบสั่งขาย รายการรองจะมีเปอร์เซ็นต์ส่วนลดและส่วนลดเป็น 0 (ศูนย์) 
    - ความถี่ในการเรียกเก็บเงินของสินค้าหลักและสินค้ารองสามารถเปลี่ยนแปลงได้ และแต่ละบรรทัดอาจมีความถี่แตกต่างกัน อย่างไรก็ตาม สินค้าหลักจะถูกอัปเดตโดยอัตโนมัติ เพื่อให้ใช้ความถี่ที่สั้นที่สุดจากรรายการรองของสินค้านั้น ตัวอย่างเช่น การแบ่งรายได้มีรายการรองสองรายการ ซึ่งรายการหนึ่งใช้ความถี่ในการเรียกเก็บเงิน **รายเดือน** และรายการอื่นๆ ที่ใช้ความถี่ในการเรียกเก็บเงิน **รายปี** ในกรณีนี้ ความถี่ในการเรียกเก็บเงินของสินค้าหลักจะถูกอัปเดตเป็น **รายเดือน**
