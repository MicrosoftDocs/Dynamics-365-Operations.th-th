---
title: การสนับสนุนและการต่ออายุ
description: บทความนี้อธิบายวิธีการตั้งค่าและใช้กระบวนการสนับสนุนและต่ออายุในใบสั่งขายเพื่อสร้างกำหนดการเรียกเก็บเงินสำหรับสินค้าการต่ออายุ
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b40e0136883d909755480a3ce101627297bd9ffb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896534"
---
# <a name="support-and-renewals"></a>การสนับสนุนและการต่ออายุ 

บทความนี้อธิบายวิธีการป้อนสินค้าการสนับสนุนหรือการต่ออายุเมื่อคุณป้อนใบสั่งขาย สินค้าเหล่านี้ใช้ในการคํานวณจำนวนเงินค่าธรรมเนียมของสัญญาการสนับสนุนเดิมและ/หรือจํานวนเงินการต่ออายุที่ใช้เมื่อสร้างกำหนดการเรียกเก็บเงินในการเรียกเก็บเงินตามการสมัครใช้งาน ตัวอย่างเช่น บริษัทของคุณขายเซิร์ฟเวอร์ให้กับลูกค้า และเสนอการสมัครใช้งานการสํารองข้อมูลในปีแรกและตัวเลือกที่จะต่ออายุการสั่งซื้อโดยการสมัครใช้งานนั้นทุกปี *สินค้าการสนับสนุน* คือการสมัครใช้งานในปีแรก และ *สินค้าการต่ออายุ* คือการต่ออายุในแต่ละปีต่อๆ มา

คุณสามารถป้อนข้อมูลเกี่ยวกับสัญญาการสนับสนุน สัญญาการต่ออายุ หรือทั้งสองอย่าง เมื่อคุณป้อนข้อมูลสัญญาการสนับสนุน เฉพาะสินค้าการสนับสนุนเท่านั้นที่จะเพิ่มเข้าในใบสั่งขาย เมื่อคุณป้อนข้อมูลสัญญาการต่ออายุ สินค้าการต่ออายุจะใช้เพื่อสร้างกำหนดการเรียกเก็บเงิน

## <a name="support-and-renewal-setup"></a>การตั้งค่าการสนับสนุนและการต่ออายุ

บนหน้า **ระดับการสนับสนุนและการต่ออายุ** คุณสามารถตั้งค่าระดับการสนับสนุนต่างๆ สำหรับสินค้าการสนับสนุนและการต่ออายุได้ การสนับสนุนหรือการต่ออายุอาจเป็นเปอร์เซ็นต์ของจํานวนเงินสินค้าเดิม หรือเป็นจํานวนเงินมาตรฐาน

คุณสามารถเลือกระดับการสนับสนุนเริ่มต้นในหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ**

ตัวอย่างเช่น บริษัทอาจมีระดับการสนับสนุนและการต่ออายุต่อไปนี้

| ระดับการสนับสนุน | เปอร์เซ็นต์การสนับสนุน | เปอร์เซ็นต์การต่ออายุ |
|---|---|---|
| ไม่จำกัด | 40% | 30% |
| สีทอง | 25% | 18% |
| เงิน | 20% | 14% |
| Bronze | 15% | 10% |

เมื่อต้องการสร้างระดับการสนับสนุนหรือการต่ออายุ ให้ทำตามขั้นตอนเหล่านี้

1. บนหน้า **ระดับการสนับสนุนหรือการต่ออายุ** ให้เลือก **ใหม่**
2. ในฟิลด์ **ระดับการสนับสนุน** ให้ป้อนชื่อเฉพาะ
3. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
4. ในฟิลด์ **วิธีการคํานวณการสนับสนุน** ให้เลือกวิธีการคํานวณการสนับสนุน ถ้าคุณเลือก **เปอร์เซ็นต์** ให้ป้อนเปอร์เซ็นต์การสนับสนุนในฟิลด์ **เปอร์เซ็นต์การสนับสนุน**
5. ในฟิลด์ **วิธีการคํานวณการต่ออายุ** ให้เลือกวิธีการคํานวณการต่ออายุ ถ้าคุณเลือก **เปอร์เซ็นต์** ให้ป้อนเปอร์เซ็นต์การต่ออายุในฟิลด์ **เปอร์เซ็นต์การต่ออายุ**
6. เลือก **บันทึก**

### <a name="fields"></a>ฟิลด์

หน้า **ระดับการสนับสนุนหรือการต่ออายุ** จะมีฟิลด์ต่อไปนี้

| ฟิลด์ | คำอธิบาย |
|---|---|
| ระดับการสนับสนุน | รหัสเฉพาะของระดับการสนับสนุนหรือการต่ออายุ (ตัวอย่างเช่น **Gold** หรือ **Silver**) |
| คำอธิบาย | อธิบายของระดับการสนับสนุนหรือการต่ออายุ |
| วิธีการคำนวณการสนับสนุน | เลือกวิธีการคํานวณการสนับสนุนของระดับ: **เปอร์เซ็นต์** หรือ **จำนวนเงินมาตรฐาน** |
| เปอร์เซ็นต์การสนับสนุน | ถ้าคุณเลือก **เปอร์เซ็นต์** เป็นวิธีการคํานวณการสนับสนุน ให้ระบุเปอร์เซ็นต์ที่ใช้ในการคํานวณราคาของสินค้าการสนับสนุน ถ้าคุณเลือก **จำนวนเงินมาตรฐาน** เป็นวิธีการคํานวณ จํานวนเงินจะถูกระบุเมื่อสร้างธุรกรรม |
| วิธีการคำนวณการต่ออายุ | เลือกวิธีการคํานวณการต่ออายุของระดับ: **เปอร์เซ็นต์** หรือ **จำนวนเงินมาตรฐาน** |
| เปอร์เซ็นต์การต่ออายุ | ถ้าคุณเลือก **เปอร์เซ็นต์** เป็นวิธีการคํานวณการต่ออายุ ให้ระบุเปอร์เซ็นต์ที่ใช้ในการคํานวณราคาของสินค้าการต่ออายุ ถ้าคุณเลือก **จำนวนเงินมาตรฐาน** เป็นวิธีการคํานวณ จํานวนเงินจะถูกระบุเมื่อสร้างธุรกรรม |

## <a name="support-and-renewal-process"></a>กระบวนการของการสนับสนุนและการต่ออายุ

ฟังก์ชันการสนับสนุนและการต่ออายุสามารถใช้ระดับการสนับสนุนต่างๆ กับสินค้าและอัปเดตข้อมูลการต่ออายุในการเรียกเก็บเงินตามการสมัครใช้งาน

ก่อนที่คุณจะใช้ฟังก์ชันการสนับสนุนและการต่ออายุ งานต่อไปนี้ต้องเสร็จสมบูรณ์

1. บนหน้า **ระดับการสนับสนุนและการต่ออายุ** ให้สร้างระดับการสนับสนุนหรือการต่ออายุอย่างน้อยหนึ่งระดับ
2. บนหน้า **การตั้งค่าสินค้า** ให้เชื่อมโยงสินค้ากับสินค้าการสนับสนุนและการต่ออายุ งานนี้จะต้องใช้เฉพาะเมื่อคุณต้องการตั้งค่าเริ่มต้นสำหรับสินค้าการสนับสนุนและ/หรือการต่ออายุ
3. บนหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ** ให้ระบุการตั้งค่าการสนับสนุนและการต่ออายุเริ่มต้นสำหรับกำหนดการใหม่

เมื่อต้องการใช้ระดับการสนับสนุนต่างๆ กับรายการและอัพเดตข้อมูลการต่ออายุ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. บนหน้า **ใบสั่งขายทั้งหมด** ให้สร้างใบสั่งขาย
2. บนแท็บด่วน **รายการใบสั่งขาย** ให้สินค้า
3. บนแท็บ **ใบแจ้งหนี้** ให้เลือก **การสนับสนุนและการต่ออายุ \>เพิ่มการสนับสนุนและการต่ออายุ**
4. บนหน้า **กระบวนการสนับสนุนและการต่ออายุ** ส่วนหัวจะถูกอัปเดตด้วยการตั้งค่าจากหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ** ค่าเหล่านี้จะใช้กับสินค้าการสนับสนุนและการต่ออายุทั้งหมด (ตัวอย่างเช่น ถ้าความถี่ในการเรียกเก็บเงินถูกตั้งค่าเป็น **ทุกปี** รายการขายทั้งหมดที่สร้างขึ้นที่มีสินค้าการต่ออายุจะมีความถี่แบบรายปี) เมื่อต้องการเชื่อมโยงใบสั่งขายกับกำหนดการเรียกเก็บเงินที่มีอยู่ ให้เลือกค่าในฟิลด์ **หมายเลขกำหนดการเรียกเก็บเงิน**
5. เมื่อต้องการเปลี่ยนวันที่เริ่มต้นการสนับสนุนหรือการต่ออายุ ให้ตั้งค่าตัวเลือก **แทนที่วันที่เริ่มต้น** เป็น **ใช่**
6. เมื่อต้องการเพิ่มหรือแก้ไขสินค้าการสนับสนุน ให้เลือกกล่องกาเครื่องหมาย **การสนับสนุน** แล้วป้อนสินค้าการสนับสนุนในฟิลด์ **สินค้าการสนับสนุน** สินค้าจะมีการเพิ่มลงในใบสั่งขาย
7. เมื่อต้องการเพิ่มหรือแก้ไขสินค้าการต่ออายุ ให้เลือกกล่องกาเครื่องหมาย **การต่ออายุ** แล้วป้อนสินค้าการต่ออายุในฟิลด์ **สินค้าการต่ออายุ** เมื่อมีการออกใบแจ้งหนี้ใบสั่งขาย จะมีการสร้างกำหนดการเรียกเก็บเงินที่รวมสินค้านั้น
8. เลือก **ตกลง**
9. ในแท็บ **ทั่วไป** ให้เลือก **ใบแจ้งหนี้** เมื่อมีการลงรายการบัญชีใบสั่งขาย กำหนดการเรียกเก็บเงินจะถูกสร้างขึ้น การแจ้งเตือนที่รวมข้อมูลกำหนดการเรียกเก็บเงินจะปรากฏในรายละเอียดข้อความ
10. ในหน้ารายการ **กำหนดการเรียกเก็บเงินทั้งหมด/ที่ใช้งานอยู่** เลือกหมายเลขกำหนดการเรียกเก็บเงินเพื่อตรวจสอบรายละเอียดของกำหนดการเรียกเก็บเงินในหน้า **กำหนดการเรียกเก็บเงิน**
11. บนแท็บด่วน **รายการกำหนดการเรียกเก็บเงิน** ให้เลือก **การสนับสนุนและการต่ออายุ** เพื่อตรวจสอบรายละเอียดของรายการที่สร้างขึ้น

> [!NOTE]
> ถ้าต้องเปลี่ยนวันที่เริ่มต้นการต่ออายุสำหรับรายการกำหนดการเรียกเก็บเงิน คุณสามารถแก้ไขค่า **วันที่เริ่มต้น** ของรายการนั้นในหน้า **กำหนดการเรียกเก็บเงิน** เมื่อคุณเปิดหน้า **ดูรายละเอียดการเรียกเก็บเงิน** ของรายการ ฟิลด์ **วันที่เริ่มต้นของการเรียกเก็บเงิน** จะมีการอัปเดตด้วยวันที่ใหม่ ค่า **วันที่สิ้นสุดของการเรียกเก็บเงิน** จะถูกคำนวณใหม่ตามความถี่ในการเรียกเก็บเงิน วันที่เริ่มต้นการต่ออายุสามารถอัปเดตได้ก็ต่อเมื่อไม่มีการสร้างและลงรายการบัญชีใบแจ้งหนี้ใบแรกสำหรับกำหนดการเรียกเก็บเงินการต่ออายุ หลังจากสร้างและลงรายการบัญชีใบแจ้งหนี้ในแรกแล้ว จะแก้ไขวันที่เริ่มต้นไม่ได้

กระบวนการสนับสนุนและการต่ออายุสามารถใช้งานได้กับใบสั่งขายเท่านั้น เมื่อคุณเพิ่มสินค้าการสนับสนุนและการต่ออายุลงในใบสั่งขาย คุณสามารถสร้างกำหนดการเรียกเก็บเงินใหม่หรือเพิ่มสินค้าการต่ออายุในกำหนดการเรียกเก็บเงินที่มีอยู่

## <a name="support-and-renewal-audit"></a>การตรวจสอบการสนับสนุนและการต่ออายุ

บนหน้า **การตรวจสอบการสนับสนุนและการต่ออายุ** คุณสามารถตรวจสอบรายละเอียดของรายการกำหนดการเรียกเก็บเงินที่สร้างขึ้นจากสินค้าการต่ออายุในใบสั่งขาย ตัวเลือกนี้จะสามารถใช้งานเฉพาะเมื่อสินค้าในรายการกำหนดการเรียกเก็บเงินเป็นสินค้าการต่ออายุ

หากต้องการแก้ไขข้อมูลการสนับสนุนและการต่ออายุสำหรับรายการกำหนดการเรียกเก็บเงิน ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. บนหน้า **กำหนดการเรียกเก็บเงินทั้งหมด** ให้เลือกหมายเลขกำหนดการเรียกเก็บเงิน
2. ในส่วน **รายการกำหนดการเรียกเก็บเงิน** เลือกรายการ แล้วเลือก **การสนับสนุนและการต่ออายุ**
3. ตรวจสอบข้อมูลทั้งหมดสำหรับสินค้าการสนับสนุนหรือการต่ออายุ
4. ทำการเปลี่ยนแปลงที่จำเป็นในระดับการสนับสนุนหรือเปอร์เซ็นต์การต่ออายุหรือจำนวนเงินแล้วป้อนค่าในฟิลด์ **เหตุผลของการเปลี่ยนแปลง**
5. เลือก **กระบวนการ**

### <a name="fields"></a>ฟิลด์

หน้า **การตรวจสอบการสนับสนุนหรือการต่ออายุ** จะมีฟิลด์ต่อไปนี้

| ฟิลด์ | คำอธิบาย |
|-------|-------------|
| หมายเลขสินค้า | หมายเลขสินค้าสำหรับกำหนดการเรียกเก็บเงิน |
| ชื่อผลิตภัณฑ์ | ชื่อผลิตภัณฑ์ |
| ระดับแผนการสนับสนุน | ดูหรือเปลี่ยนแปลงระดับการสนับสนุนสำหรับสินค้าการต่ออายุ |
| เปอร์เซ็นต์การต่ออายุ | ป้อนเปอร์เซ็นต์การต่ออายุที่จะใช้เมื่อคํานวณราคาต่อหน่วยสำหรับสินค้าการต่ออายุในกำหนดการเรียกเก็บเงิน |
| จำนวนเงินในการต่ออายุ | ป้อนจำนวนเงินการต่ออายุที่จะใช้เมื่อคํานวณราคาต่อหน่วยสำหรับสินค้าการต่ออายุในกำหนดการเรียกเก็บเงิน |
| เหตุผลในการเปลี่ยนแปลง | ป้อนเหตุผลของการเปลี่ยนข้อมูลการสนับสนุนและการต่ออายุ คุณต้องป้อนเหตุผลเมื่อคุณเปลี่ยนค่า **เปอร์เซ็นต์การต่ออายุ**, **จํานวนเงินการต่ออายุ** หรือ **ระดับแผนการสนับสนุน** |
| สินค้าขายเดิม | หมายเลขสินค้าขายเริ่มต้นจากใบสั่งขาย |
| ยอดเงินสุทธิเดิม | ยอดเงินสุทธิเริ่มต้นสำหรับสินค้า |
| ระดับการสนับสนุนเดิม | ระดับการสนับสนุนเดิมสำหรับสินค้า |
| เปอร์เซ็นต์ในการต่ออายุเดิม | เปอร์เซ็นต์การต่ออายุเดิมสำหรับสินค้า |
| จำนวนเงินในการต่ออายุเดิม | จำนวนเงินในการต่ออายุเดิมสำหรับสินค้า |
| **เส้นกริด** | |
| ระดับการสนับสนุนเดิม | ระดับการสนับสนุนก่อนหน้า |
| เปอร์เซ็นต์ในการต่ออายุเดิม | เปอร์เซ็นต์การต่ออายุก่อนหน้า |
| จำนวนเงินในการต่ออายุเดิม | จำนวนเงินในการต่ออายุก่อนหน้า |
| ปรับเปลี่ยนโดย | ชื่อผู้ใช้ของผู้ใช้ที่ทำการเปลี่ยนแปลง |
| วันที่และเวลาที่แก้ไข | วันที่ที่เกิดการเปลี่ยนแปลง |
| เหตุผล | เหตุผลสำหรับการเปลี่ยนแปลง |
