---
title: รายได้ที่ยังไม่ได้เรียกเก็บเงิน
description: บทความนี้อธิบายวิธีการตั้งค่ารายการและบัญชีที่จะใช้คุณลักษณะรายได้ที่ยังไม่ได้เรียกเก็บเงินในการเรียกเก็บเงินตามการสมัครใช้งาน
author: JodiChristiansen
ms.date: 10/10/2022
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
ms.openlocfilehash: adf6f06ee454f368fa194315a87cfdec9e5e13da
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644180"
---
# <a name="unbilled-revenue"></a>รายได้ที่ยังไม่ได้เรียกเก็บเงิน

บทความนี้อธิบายคุณลักษณะรายได้ที่ยังไม่ได้เรียกเก็บเงินซึ่งจะช่วยคุณรวมยอดเงินของกำหนดการเรียกเก็บเงินทั้งหมดไว้ในงบดุล ยอดเงินเหล่านี้รวมอยู่ในบัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงินและบัญชีตรงข้ามของรายได้ที่ยังไม่ได้เรียกเก็บเงิน และสัญญาดังกล่าวจะเรียกเก็บผ่านการผ่อนชำระ

## <a name="set-up-unbilled-revenue"></a>ตั้งค่ารายได้ที่ยังไม่ได้เรียกเก็บเงิน

หากต้องการตั้งค่ารายได้ที่ยังไม่ได้เรียกเก็บเงิน ให้ดำเนินการตามขั้นตอนเหล่านี้

- ในหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ** ให้ตั้งค่าฟิลด์ในส่วน **รายได้ที่ยังไม่ได้เรียกเก็บเงิน**
- คุณลักษณะรายได้ที่ยังไม่ได้เรียกเก็บเงินสามารถใช้กับรายการที่มีการตั้งค่า **ชนิดรายการ** เป็น **มาตรฐาน** และยังสามารถใช้กับรายการรอการตัดบัญชีได้ด้วย หากต้องการใช้รายได้ที่ยังไม่ได้เรียกเก็บเงินกับฟังก์ชันการทำงานระยะสั้น ให้ตั้งค่าตัวเลือกระยะสั้นในหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ**

หากต้องการตั้งค่าสินค้าที่จะใช้รายได้ที่ยังไม่ได้เรียกเก็บเงิน ให้ดำเนินการตามขั้นตอนเหล่านี้

1. บนหน้า **การตั้งค่ารายได้ที่ยังไม่ได้เรียกเก็บเงิน** บนแท็บ **สินค้า** ให้เลือก **เพิ่ม**
2. บนบรรทัดใหม่ ใน **รหัสสินค้า** ให้เลือกรหัสสินค้า
3. ในฟิลด์ **ความสัมพันธ์ของสินค้า** ให้เลือกความสัมพันธ์ของสินค้า
4. ทำซ้ำขั้นตอนเหล่านี้เพื่อเพิ่มบรรทัดเพิ่มเติม
5. เลือก **บันทึก**

หากต้องการตั้งค่าสินค้าและบัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน ให้ดำเนินการตามขั้นตอนเหล่านี้

1. บนหน้า **การตั้งค่ารายได้ที่ยังไม่ได้เรียกเก็บเงิน** บนแท็บ **บัญชี** ให้เลือก **เพิ่ม**
2. บนบรรทัดใหม่ ใน **รหัสสินค้า** ให้เลือกรหัสสินค้า
3. ในฟิลด์ **ความสัมพันธ์ของสินค้า** ให้เลือกความสัมพันธ์ของสินค้า
4. เลือกบัญชีสำหรับรายได้ที่ยังไม่ได้เรียกเก็บเงิน ส่วนลดที่ยังไม่ได้เรียกเก็บเงิน และการปรับมูลค่ารายได้ที่ยังไม่ได้เรียกเก็บเงิน เมื่อต้องการใช้บัญชีระยะสั้น คุณต้องตั้งค่าฟิลด์ **วิธีการที่ยังไม่ได้เรียกเก้บเงินระยะสั้น** เป็น **รอบระยะเวลาหมุนเวียน** หรือ **ปีคงที่** ในหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ**
5. ทำซ้ำขั้นตอนเหล่านี้เพื่อเพิ่มบรรทัดเพิ่มเติม
6. เลือก **บันทึก**

## <a name="use-unbilled-revenue"></a>ใช้รายได้ที่ยังไม่ได้เรียกเก็บเงิน

1. บนหน้า **กำหนดการเรียกเก็บเงินทั้งหมด** ให้สร้างกำหนดการเรียกเก็บเงิน
2. ถ้าสินค้ายังไม่ได้รับการตั้งค่าให้ใช้รายได้ที่ยังไม่ได้เรียกเก็บเงิน ให้เลือกกล่องกาเครื่องหมาย **รายได้ที่ยังไม่ได้เรียกเก็บเงิน** ในรายการกำหนดการเรียกเก็บเงิน
3. ตั้งค่าตัวเลือก **รายได้ที่ยังไม่ได้เรียกเก็บเงิน** เป็น **ใช่** จากนั้นตรวจสอบและแก้ไขบัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน ส่วนลด บัญชีตรงข้ามของรายได้ที่ยังไม่ได้เรียกเก็บเงินตามที่จำเป็น
4. ในกำหนดการเรียกเก็บเงิน ภายใต้ **การดำเนินการกับรายได้ที่ยังไม่ได้เรียกเก็บเงิน** ให้เลือก **สร้างรายการสมุดรายวัน** เพื่อสร้างรายการสมุดรายวันเริ่มต้นให้กับรายได้ที่ยังไม่ได้เรียกเก็บเงิน คุณต้องกรอกข้อมูลในขั้นตอนนี้ก่อนออกใบแจ้งหนี้ให้กับกำหนดการเรียกเก็บเงิน
5. เมื่อสร้างรายการสมุดรายวันเริ่มต้นแล้ว ให้เลือก **สร้างใบแจ้งหนี้** เพื่อสร้างใบสั่งขายและลงรายการบัญชีใบแจ้งหนี้ให้กับกำหนดการเรียกเก็บเงิน
6. หลังจากลงรายการบัญชีใบแจ้งหนี้แล้ว คุณสามารถตรวจสอบข้อมูลการตรวจสอบบนแท็บ **การต่ออายุ** ของหน้า **กำหนดการเรียกเก็บเงินทั้งหมด**

### <a name="milestone-billing"></a>การเรียกเก็บเงินตามเหตุการณ์สำคัญ

การเรียกเก็บเงินตามเหตุการณ์สำคัญจะใช้ได้กับรายได้ที่ยังไม่ได้เรียกเก็บเงินภายใต้เงื่อนไขต่อไปนี้

- หากสินค้าหลักของเหตุการณ์สำคัญยังไม่ได้เรียกเก็บเงิน (มีการเลือกกล่องกาเครื่องหมาย **รายได้ที่ยังไม่ได้เรียกเก็บเงิน**) และสินค้ารองของเหตุการณ์สำคัญเรียกเก็บเงินแล้ว (มีการล้างกล่องกาเครื่องหมาย **รายได้ที่ยังไม่ได้เรียกเก็บเงิน**) ต้องมีการระบุวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับสินค้าหลัก วันที่เหล่านี้จะใช้เพื่อสร้างรายการสมุดรายวันเริ่มต้น
- หากสินค้าหลักของเหตุการณ์สำคัญยังไม่ได้เรียกเก็บเงิน (มีการล้างกล่องกาเครื่องหมาย **รายได้ที่ยังไม่ได้เรียกเก็บเงิน**) และสินค้ารองของเหตุการณ์สำคัญเรียกเก็บเงินแล้ว (มีการเลือกกล่องกาเครื่องหมาย **รายได้ที่ยังไม่ได้เรียกเก็บเงิน**) ต้องมีการระบุวันที่สิ้นสุดสำหรับสินค้ารองที่คุณต้องการสร้างรายการสมุดรายวันเริ่มต้นเท่านั้น

สินค้ารองของเหตุการณ์สำคัญแต่ละรายการสามารถประมวลผลแยกต่างหากได้ คุณสามารถระบุวันที่สิ้นสุดได้เมื่อคุณพร้อมที่จะสร้างรายการสมุดรายวันเริ่มต้น

> [!NOTE]
> หากสร้างรายการสมุดรายวันเริ่มต้นของสินค้าหลักหรือสินค้ารองของเหตุการณ์สำคัญแล้ว หรือมีการสร้างใบแจ้งหนี้แล้ว คุณจะแก้ไขวันที่เริ่มต้นและวันที่สิ้นสุดดังกล่าวไม่ได้

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>รายได้ที่ยังไม่ได้เรียกเก็บเงินที่มีการรอตัดบัญชีแบบเส้นตรง

เมื่อต้องการใช้รายได้ที่ยังไม่ได้เรียกเก็บเงินที่มีกำหนดการตัดบัญชีแบบเส้นตรง ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. บนหน้า **กำหนดการเรียกเก็บเงินทั้งหมด** ให้สร้างกำหนดการเรียกเก็บเงิน
2. เพิ่มสินค้าในรายการกำหนดการเรียกเก็บเงิน
3. เลือก **การรอตัดบัญชี** สำหรับรายการ
4. บนหน้า **การรอตัดบัญชีธุรกรรม** ให้ปฏิบัติตามขั้นตอนเหล่านี้

    1. ตั้งค่าตัวเลือก **รอตัดบัญชี** เป็น **ใช่**
    2. เปลี่ยนบัญชีตามที่คุณต้องการ
    3. ในส่วน **จัดกำหนดการ** ให้เลือก **แบบเส้นตรง** และแก้ไขค่าอื่นๆ ตามที่คุณต้องการ
    4. เลือก **ตกลง**

5. เลือก **รายได้ที่ยังไม่ได้เรียกเก็บเงิน** สำหรับรายการ แล้วปฏิบัติตามขั้นตอนเหล่านี้

    1. ตั้งค่าตัวเลือก **รายได้ที่ยังไม่ได้เรียกเก็บเงิน** เป็น **ใช่**
    2. เลือกบัญชีที่จะใช้กับรายได้ที่ยังไม่ได้เรียกเก็บเงิน ส่วนลดที่ยังไม่ได้เรียกเก็บเงิน และการปรับมูลค่ารายได้

6. ในกำหนดการเรียกเก็บเงิน ภายใต้ **การดำเนินการกับรายได้ที่ยังไม่ได้เรียกเก็บเงิน** ให้เลือก **สร้างรายการสมุดรายวัน** หรือใช้หน้า **การดำเนินการจำนวนมากของรายได้ที่ยังไม่ได้เรียกเก็บเงิน** เพื่อสร้างรายการสมุดรายวัน
7. ระบบจะสร้างกำหนดการรอตัดบัญชี คุณสามารถตรวจสอบรายละเอียดในหน้า **กำหนดการรอตัดบัญชีทั้งหมด** เมื่อสร้างกำหนดการรอตัดบัญชีแล้ว คุณสามารถแก้ไขค่าต่างๆ ของสินค้าในรายการกำหนดการเรียกเก็บเงินได้ ตัวอย่างเช่น คุณสามารถแก้ไขราคาต่อหน่วย ปริมาณ หรือวันที่

### <a name="unbilled-revenue-with-event-based-deferrals"></a>รายได้ที่ยังไม่ได้เรียกเก็บเงินที่มีการรอตัดบัญชีตามเหตุการณ์

เมื่อต้องการใช้รายได้ที่ยังไม่ได้เรียกเก็บเงินที่มีกำหนดการตัดบัญชีตามเหตุการณ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. บนหน้า **กำหนดการเรียกเก็บเงินทั้งหมด** ให้สร้างกำหนดการเรียกเก็บเงิน
2. เพิ่มสินค้าในรายการกำหนดการเรียกเก็บเงิน
3. เลือก **การรอตัดบัญชี** สำหรับรายการ
4. บนหน้า **การรอตัดบัญชีธุรกรรม** ให้ปฏิบัติตามขั้นตอนเหล่านี้

    1. ตั้งค่าตัวเลือก **รอตัดบัญชี** เป็น **ใช่**
    2. เปลี่ยนบัญชีตามที่คุณต้องการ
    3. ในส่วน **กำหนดการ** ให้เลือก **ตามเหตุการณ์**, **เทมเพลต**, **ชนิดการปันส่วน** และ **บัญชีการหมดอายุ**
    4. เลือก **ตกลง**

5. เลือก **รายได้ที่ยังไม่ได้เรียกเก็บเงิน** สำหรับรายการ แล้วปฏิบัติตามขั้นตอนเหล่านี้

    - ตั้งค่าตัวเลือก **รายได้ที่ยังไม่ได้เรียกเก็บเงิน** เป็น **ใช่**
    - เลือกบัญชีที่จะใช้กับรายได้ที่ยังไม่ได้เรียกเก็บเงิน ส่วนลดที่ยังไม่ได้เรียกเก็บเงิน และการปรับมูลค่ารายได้

6. ในกำหนดการเรียกเก็บเงิน ภายใต้ **การดำเนินการกับรายได้ที่ยังไม่ได้เรียกเก็บเงิน** ให้เลือก **สร้างรายการสมุดรายวัน** หรือใช้หน้า **การดำเนินการจำนวนมากของรายได้ที่ยังไม่ได้เรียกเก็บเงิน** เพื่อสร้างรายการสมุดรายวัน
7. ระบบจะสร้างกำหนดการรอตัดบัญชี คุณสามารถตรวจสอบรายละเอียดในหน้า **กำหนดการรอตัดบัญชีทั้งหมด** เมื่อสร้างกำหนดการรอตัดบัญชีแล้ว คุณสามารถแก้ไขค่าต่างๆ ของสินค้าในรายการกำหนดการเรียกเก็บเงินได้ ตัวอย่างเช่น คุณสามารถแก้ไขราคาต่อหน่วย ปริมาณ หรือวันที่ กำหนดการรอตัดบัญชีจะมีการคำนวณใหม่ตามมูลค่าใหม่

การกระจายจะมีการคำนวณใหม่ตามชนิดการปันส่วนที่เลือก (**เปอร์เซ็นต์**, **เปอร์เซ็นต์ความสมบูรณ์** หรือ **จำนวนเงินที่เท่ากัน**) สำหรับชนิดการปันส่วน **จำนวนเงินผันแปร** การกระจายจะจะมีการคำนวณใหม่ตามเปอร์เซ็นต์ที่เทียบเท่ากับค่าเริ่มต้นของเหตุการณ์ ตัวอย่างเช่น ราคาต่อหน่วยของเดิมคือ $100.00 และเปอร์เซ็นต์ของค่าเริ่มต้นคือ $55.00 (55 เปอร์เซ็นต์) ถ้าราคาต่อหน่วยเปลี่ยนเป็น $200.00 จํานวนเงินผันแปรของเหตุการณ์จะเป็น $110.00 (ยังคงเป็น 55 เปอร์เซ็นต์)

> [!NOTE]
> ถ้ารายการกำหนดการรอตัดบัญชีมีการรับรู้ สินค้าในรายการกำหนดการเรียกเก็บเงินจะไม่สามารถแก้ไขได้ เมื่อต้องการแก้ไขสินค้าในรายการ คุณต้องกลับรายการที่รับรู้นั้นก่อน จากนั้นจึงสามารถอัปเดตรายการกำหนดการเรียกเก็บเงินได้

### <a name="unbilled-revenue-and-top-billing"></a>รายได้ที่ยังไม่ได้เรียกเก็บเงินและการเรียกเก็บเงินบนสุด

โดยจะป้อนกำหนดการเรียกเก็บเงินเป็นเวลาสามปี และใบแจ้งหนี้จะมีการเรียกเก็บเงินเป็นรายปีสําหรับรอบระยะเวลาสามปี จำนวนเงินในสัญญาทั้งหมดจะบันทึกในบัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงินซึ่งสร้างใบแจ้งหนี้ประจําปี บัญชีตรงข้ามคือบัญชีรายได้หรือบัญชีรายได้รอตัดบัญชี

การเรียกเก็บเงินบนสุดและรายได้ที่ยังไม่ได้เรียกเก็บเงินจะไม่ทำงานร่วมกัน เนื่องจากปัญหาการกระทบยอดสามารถเกิดขึ้นในบัญชีแยกประเภททั่วไป ตัวอย่างเช่น ในหน้า **การตั้งค่ากลุ่มสินค้า** กลุ่มสินค้า A มีการตั้งค่าเพื่อให้ฟิลด์ **จำนวนรายการบนสุด** เป็น **2** บนหน้า **กำหนดการเรียกเก็บเงิน** การเพิ่มสินค้าสามรายการ สินค้าทั้งสามรายการเป็นของกลุ่มสินค้า A เมื่อสร้างรายการสมุดรายวันเริ่มต้นให้กับคุณลักษณะรายได้ที่ยังไม่เรียกเก็บเงิน จำนวนเงินของสินค้าทั้งสามรายการจะมีการดำเนินการไปยังบัญชีที่ยังไม่ได้เรียกเก็บเงิน เมื่อมีการสร้างใบแจ้งหนี้สำหรับกำหนดการเรียกเก็บเงิน จะรวมเฉพาะจำนวนเงินของรายการสินค้าสองรายการบนสุดเท่านั้น ดังนั้น จำนวนเงินในใบแจ้งหนี้จะไม่ตรงกับจำนวนเงินที่ดำเนินการไปยังบัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน และจะเกิดปัญหาการกระทบยอดในบัญชีแยกประเภททั่วไป

หากคุณต้องการใช้รายได้ที่ยังไม่ได้เรียกเก็บเงิน ให้ปล่อยหน้า **การตั้งค่ากลุ่มสินค้า** ว่างเปล่าหรือตั้งค่ากลุ่มสินค้าทั้งหมดเพื่อให้มีการตั้งค่าฟิลด์ **จำนวนของรายการบนสุด** เป็น **0** (ศูนย์) หากคุณต้องการใช้การเรียกเก็บเงินบนสุด จะไม่มีการกระทบยอดรายได้ที่ยังไม่ได้เรียกเก็บเงิน

### <a name="examples"></a>ตัวอย่างเช่น

ตั้งแต่เวอร์ชัน 10.0.29 พารามิเตอร์ใหม่จะถูกเพิ่มลงในพารามิเตอร์การเรียกเก็บเงินของสัญญาที่เกิดใหม่ เมื่อตั้งค่าเป็น ใช่ พารามิเตอร์ **ใช้บัญชีตรงข้ามที่ยังไม่ได้เรียกเก็บเงิน** จะเปิดใช้งานบัญชีใหม่สองบัญชีใน **การตั้งค่ารายได้ที่ยังไม่ได้เรียกเก็บเงิน** บัญชีตรงข้ามของรายได้ที่ยังไม่ได้เรียกเก็บเงินและบัญชีตรงข้ามของส่วนลดที่ยังไม่ได้เรียกเก็บ จะพร้อมใช้งานและจะใช้ได้ดีที่สุดเมื่อสร้างกำหนดการการเรียกเก็บเงินในสกุลเงินอื่นที่ไม่ใช่สกุลเงินทางบัญชี การใช้บัญชีตรงข้ามจะช่วยให้มั่นใจว่าบัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงินและบัญชีส่วนลดที่ยังไม่ได้เรียกเก็บเงิน จะถูกกลับรายการโดยใช้อัตราแลกเปลี่ยนเดียวกันกับรายการเริ่มต้น กระบวนการ **สร้างรายการสมุดรายวัน** เริ่มต้น จะเหมือนกับเดบิตเป็นรายได้ที่ยังไม่ได้เรียกเก็บเงิน และเครดิตเป็นงรายได้ หากการใช้ส่วนลด รายการสมุดรายวันเริ่มต้นจะเหมือนกับเดบิตเป็นส่วนลด และเครดิตเป็นส่วนลดที่ยังไม่ได้เรียกเก็บเงิน 

ตัวอย่างนี้แสดงวิธีการใช้รายได้ที่ยังไม่ได้เรียกเก็บเงินเพื่อรับรู้ยอดเงินทั้งหมดของสัญญาในงบดุลเป็นรายได้ที่ยังไม่ได้เรียกเก็บเงิน ส่วนอีกด้านของรายการคือรายได้ หรือรายได้ที่รอการตัดบัญชี เมื่อคุณออกใบแจ้งหนี้ให้ลูกค้า รายได้ที่ยังไม่ได้เรียกเก็บเงินจะถูกกลับรายการ การรับรู้รายได้จะเกิดขึ้นในเวลาที่ออกใบแจ้งหนี้หรือตามเวลาการรับรู้การรอตัดบัญชีที่ตั้งค่าไว้

#### <a name="assumptions"></a>สมมติฐาน

- ในวันที่ 1 มกราคมของปีปัจจุบัน ลูกค้าลงนามในสัญญาสามปีที่มีมูลค่า $390
- สัญญาจะมีสองส่วนคือ สิทธิ์การใช้งานและข้อตกลงการบํารุงรักษา
- ราคาขายของค่าธรรมเนียมสิทธิ์การใช้งานคือ $300 และลูกค้าจะได้รับการออกใบแจ้งหนี้ $100 ในวันที่ 1 มกราคมของปีสัญญาแต่ละปี ค่าธรรมเนียมสิทธิ์การใช้งาน $300 จะถูกเรียกเก็บเป็นรายได้เมื่อมีการลงนามสัญญา
- ราคาขายของค่าธรรมเนียมสิทธิ์การบำรุงรักษาคือ $90 และลูกค้าจะได้รับการออกใบแจ้งหนี้ $30 ในวันที่ 1 มกราคมของปีสัญญาแต่ละปี ค่าธรรมเนียมการรบำรุงรักษา $90 จะรอตัดบัญชี และจะมีการรับรู้ที่ $2.50 ในแต่ละเดือนตลอดอายุของสัญญา
- ลูกค้าจะได้รับการออกใบแจ้งหนี้ $130 ในช่วงเริ่มต้น (1 มกราคม) ของระยะเวลาแต่ละปีในสามปีของสัญญา

#### <a name="steps"></a>ขั้นตอน

1. ตั้งค่าสินค้าที่ปล่อยออกสองรายการเป็นสินค้าที่ยังไม่ได้เรียกเก็บเงิน ใช้หน้า **การตั้งค่ารายได้ที่ยังไม่ได้เรียกเก็บเงิน** เพื่อตั้งค่าสินค้าและบัญชีที่ใช้รายได้ที่ยังไม่ได้เรียกเก็บเงิน
2. ในตัวอย่างนี้ ค่าธรรมเนียมการบํารุงรักษาจะถูกรอตัดบัญชี สินค้านี้ต้องการเทมเพลตการรอตัดบัญชีซึ่งมีการตั้งค่าบนหน้า **เทมเพลตการรอตัดบัญชี** เทมเพลตดังกล่าวมีความถี่ของรอบระยะเวลา **รายเดือน** และรอบระยะเวลาการรับรู้มีระยะเวลา 36 เดือน ดังนั้น รายได้ต่อเดือนจึงเป็น $2.50
3. บนหน้า **สินค้าที่รอตัดบัญชีตามค่าเริ่มต้น** ให้ตั้งค่าฟิลด์ **ค่าธรรมเนียมการบำรุงรักษา** เป็น **สินค้ารอตัดบัญชี** ขั้นตอนนี้และขั้นตอนถัดไปจะทําให้รายการค่าธรรมเนียมการบํารุงรักษาเป็นรอตัดบัญชีเมื่อขายหรือรวมอยู่ในกำหนดการเรียกเก็บเงิน
4. เลือก **ค่าเริ่มต้นการรอตัดบัญชี** \> **เทมเพลต** และเพิ่มสินค้าสำหรับค่าธรรมเนียมการบํารุงรักษาและเทมเพลตแบบเส้นตรงจากขั้นตอนที่ 2 สินค้าสำหรับค่าธรรมเนียมการบํารุงรักษาจะเชื่อมโยงกับกำหนดการรอตัดบัญชี 36 เดือน
5. สร้างกำหนดการเรียกเก็บเงินที่มีสินค้าสองรายการที่ยังไม่ได้เรียกเก็บเงิน ตั้งค่ากำหนดการเรียกเก็บเงินสำหรับสัญญาด้วยรายการต่อไปนี้:

    | สินค้า | วันที่เริ่มต้น | วันที่สิ้นสุด | จำนวนเงิน | ความถี่ในการเรียกเก็บเงิน | สินค้าการรอตัดบัญชี | รายได้ที่ยังไม่ได้เรียกเก็บเงิน | คำอธิบาย |
    |---|---|---|---|---|---|---|---|
    | ใบอนุญาต | 01 มกราคม 2022 | 31 ธันวาคม 2024 | $100.00 | รายปี | หมายเลข | ใช่ | ลูกค้าจะได้รับการออกใบแจ้งหนี้ปีละ $100.00 ยอดรวม $300.00 จะถูกบันทึกล่วงหน้าเป็นรายได้ที่ยังไม่ได้เรียกเก็บเงินในงบดุล และเป็นรายได้ในกําไรขาดทุน ใบแจ้งหนี้แต่ละใบจะลดยอดเงินที่ยังไม่ได้เรียกเก็บเงิน |
    | การบำรุงรักษา | 01 มกราคม 2022 | 31 ธันวาคม 2024 | $30.00 | รายปี | ใช่ | ใช่ | ลูกค้าจะได้รับการออกใบแจ้งหนี้ปีละ $30.00 ยอดรวม $90.00 จะถูกบันทึกล่วงหน้าเป็นรายได้ที่ยังไม่ได้เรียกเก็บเงินและรายได้รอตัดบัญชีในงบดุล ใบแจ้งหนี้แต่ละใบจะลดยอดเงินที่ยังไม่ได้เรียกเก็บเงิน จะมีการรับรู้รายได้ที่รอตัดบัญชีทุกเดือนเป็นเวลา 36 เดือน |

6. บนหน้า **กำหนดการเรียกเก็บเงินทั้งหมด** ให้ใช้กระบวนการ **สร้างรายการสมุดรายวัน** เพื่อลงรายการบัญชีมูลค่าสัญญาไปยังงบดุลเป็นรายได้ที่ยังไม่ได้เรียกเก็บเงิน

จะมีการสร้างรายการสมุดรายวันสองรายการ หนึ่งรายการต่อหนึ่งบรรทัดในกำหนดการเรียกเก็บเงิน

| บัญชี | ยอดเงินเดบิต | ยอดเงินเครดิต |
|---|---|---|
| บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน | $300.00 | |
| บัญชีรายได้ | | $300.00 |

| บัญชี | ยอดเงินเดบิต | ยอดเงินเครดิต |
|---|---|---|
| บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน | $90.00 | |
| รายได้รอตัดบัญชี | | $90.00 |

สัญญานี้ต้องการให้สร้างใบแจ้งหนี้ให้กับลูกค้าเมื่อเริ่มต้นในแต่ละปี ใช้กระบวนการ **สร้างใบแจ้งหนี้** เพื่อสร้างใบแจ้งหนี้ เมื่อมีการสร้างใบแจ้งหนี้ ใบสำคัญใบแจ้งหนี้ต่อไปนี้จะถูกลงรายการบัญชี

| บัญชี| ยอดเงินเดบิต | ยอดเงินเครดิต |
|---|---|---|
| บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน | | $130.00 |
| บัญชีลูกหนี้ | $130.00 | |

รายการสมุดรายวันเดียวกันนี้จะถูกสร้างโดยใบแจ้งหนี้ที่ลงรายการบัญชีในตอนเริ่มต้นของสองปีถัดไป บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงินถูกลดลงในแต่ละปีระหว่างกระบวนการ **สร้างใบแจ้งหนี้** บัญชีตรงข้ามของรายได้ที่ยังไม่ได้เรียกเก็บเงินจะใช้เพื่อปรับยอดดุลบัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน เมื่อใช้อัตราแลกเปลี่ยนที่แตกต่างกัน 

ในขั้นตอนสุดท้าย รายการสมุดรายวันการรับรู้จะถูกสร้างในแต่ละเดือน เพื่อรับรู้รายได้ที่รอการตัดบัญชีจากค่าธรรมเนียมการบํารุงรักษา คุณสามารถสร้างรายการสมุดรายวันได้โดยใช้หน้า **การดำเนินการรับรู้** อีกทางหนึ่งคือสามารถสร้างรายการได้โดยเลือก **รับรู้** สำหรับรายการในหน้า **กำหนดการรอตัดบัญชี**

| บัญชีหลัก | ยอดเงินเดบิต | ยอดเงินเครดิต |
|---|---|---|
| รายได้รอตัดบัญชี | $2.50 | |
| รายได้ | | $2.50 |

ระบบจะถูกสร้างรายการสมุดรายวันนี้ทุกครั้งที่เรียกใช้กระบวนการรับรู้สำหรับสินค้ารอตัดบัญชีนี้ (ทั้งหมด 36 ครั้ง)

#### <a name="short-term-fixed-year"></a>ระยะสั้น: ปีคงที่

คุณสามารถใช้รายได้ที่ยังไม่ได้เรียกเก็บเงินร่วมกับฟังก์ชันการทำงานระยะสั้นได้โดยตั้งค่าฟิลด์ **ยังไม่ได้เรียกเก็บเงินในระยะสั้น** ในหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ** ตัวอย่างต่อไปนี้แสดงการคํานวณที่เสร็จสิ้นเมื่อรายได้ที่ยังไม่ได้เรียกเก็บเงินมีการใช้ร่วมกับวิธีการยังไม่ได้เรียกเก็บเงินในระยะสั้นแบบ **ปีคงที่**

ระบบจะสร้างกำหนดการเรียกเก็บเงินที่มีเงื่อนไขต่อไปนี้

- **วันที่เริ่มต้น:** 1 มิถุนายน 2020
- **วันที่สิ้นสุด:** 31 ธันวาคม 2021
- **ราคาต่อหน่วย:** $100
- **ความถี่:** รายเดือน

ในหน้า **กำหนดการเรียกเก็บเงินทั้งหมด** รายการสมุดรายวันเริ่มต้นจะถูกสร้างโดยกระบวนการ **สร้างรายการสมุดรายวัน** จำนวนเงินระยะสั้นและระยะยาวปัจจุบันมีการคํานวณในลักษณะต่อไปนี้

- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บเงินในระยะสั้นปัจจุบัน:** $700
- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บระยะยาวปัจจุบัน:** $1,200

ระบบจะสร้างใบแจ้งหนี้ตามรอบระยะเวลาการเรียกเก็บเงินตั้งแต่วันที่ 1 มิถุนายน 2020 จนถึงวันที่ 30 พฤศจิกายน 2020 จำนวนเงินระยะสั้นและระยะยาวปัจจุบันมีการคํานวณในลักษณะต่อไปนี้

- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บเงินในระยะสั้นปัจจุบัน:** $100
- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บระยะยาวปัจจุบัน:** $1,200

ระบบจะสร้างใบแจ้งหนี้ตามรอบระยะเวลาการเรียกเก็บเงินตั้งแต่วันที่ 1 ธันวาคม 2020 จนถึงวันที่ 31 ธันวาคม 2020 จำนวนเงินระยะสั้นและระยะยาวปัจจุบันมีการคํานวณในลักษณะต่อไปนี้

- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บเงินในระยะสั้นปัจจุบัน:** $1,200
- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บระยะยาวปัจจุบัน:** $0

#### <a name="short-term-rolling-periods"></a>ระยะสั้น: รอบระยะเวลาหมุนเวียน

คุณสามารถใช้รายได้ที่ยังไม่ได้เรียกเก็บเงินร่วมกับฟังก์ชันการทำงานระยะสั้นได้โดยตั้งค่าวิธีการยังไม่ได้เรียกเก็บเงินในระยะสั้นในหน้า **พารามิเตอร์การเรียกเก็บเงินตามสัญญาที่เกิดซ้ำ** ตัวอย่างต่อไปนี้แสดงการคํานวณที่เสร็จสิ้นเมื่อรายได้ที่ยังไม่ได้เรียกเก็บเงินมีการใช้ร่วมกับวิธีการยังไม่ได้เรียกเก็บเงินในระยะสั้นแบบ **รอบระยะเวลาหมุนเวียน**

ระบบจะสร้างกำหนดการเรียกเก็บเงินที่มีเงื่อนไขต่อไปนี้

- **วันที่เริ่มต้น:** 1 มิถุนายน 2020
- **วันที่สิ้นสุด:** 31 ธันวาคม 2021
- **ราคาต่อหน่วย:** $100
- **ความถี่:** รายเดือน

ในหน้า **กำหนดการเรียกเก็บเงินทั้งหมด** รายการสมุดรายวันเริ่มต้นจะถูกสร้างโดยกระบวนการ **สร้างรายการสมุดรายวัน** จำนวนเงินระยะสั้นและระยะยาวปัจจุบันมีการคํานวณในลักษณะต่อไปนี้

- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บเงินในระยะสั้นปัจจุบัน:** $1,200
- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บระยะยาวปัจจุบัน:** $700

ระบบจะสร้างใบแจ้งหนี้ตามรอบระยะเวลาการเรียกเก็บเงินตั้งแต่วันที่ 1 มิถุนายน 2020 จนถึงวันที่ 30 พฤศจิกายน 2020 จำนวนเงินระยะสั้นและระยะยาวปัจจุบันมีการคํานวณในลักษณะต่อไปนี้

- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บเงินในระยะสั้นปัจจุบัน:** $1,200
- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บระยะยาวปัจจุบัน:** $100

ระบบจะสร้างใบแจ้งหนี้ตามรอบระยะเวลาการเรียกเก็บเงินตั้งแต่วันที่ 1 ธันวาคม 2020 จนถึงวันที่ 31 ธันวาคม 2020 จำนวนเงินระยะสั้นและระยะยาวปัจจุบันมีการคํานวณในลักษณะต่อไปนี้

- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บเงินในระยะสั้นปัจจุบัน:** $1,200
- **จำนวนเงินรายได้ที่ยังไม่ได้เรียกเก็บระยะยาวปัจจุบัน:** $0

### <a name="items-with-revenue-allocation"></a>สินค้าที่มีการปันส่วนรายได้

สินค้าสองรายการที่มีความถี่ในการเรียกเก็บเงินแตกต่างกันจะถูกเพิ่มเข้าในกำหนดการเรียกเก็บเงิน ทั้งคู่ใช้รายได้ที่ยังไม่ได้เรียกเก็บเงินและสินค้าที่รอตัดบัญชีได้

- **หมายเลขสินค้า 1000:** Surface Pro 128GB

    - **ความถี่ในการเรียกเก็บเงิน:** ครั้งเดียว
    - **ราคาต่อหน่วย:** $1,500
    - **ราคาขายแยกต่างหาก:** $1,600
    - **รายได้จากสัญญา:** $1,465.26

- **หมายเลขสินค้า S0021:** การประกันภัยที่ขายพร้อมกับหมายเลขสินค้า 1000

    - **ความถี่ในการเรียกเก็บเงิน:** รายเดือนเป็นเวลา 12 เดือน
    - **ราคาต่อหน่วย:** $20 ต่อเดือน
    - **ราคาขายแยกต่างหาก:** $25
    - **รายได้จากสัญญา:** $264.74

เนื่องจากทั้งสินค้าใช้การปันส่วนรายได้และรายได้ที่ยังไม่ได้เรียกเก็บเงิน ยอดเงินรวมของสัญญาในรายการต่ออายุเป็น 0 (ศูนย์) คอลัมน์ **รายได้ของสัญญา** จะถูกเพิ่มและแสดงยอดรายได้ของสัญญา

ตารางต่อไปนี้จะแสดงรายการสมุดรายวันเริ่มต้นสำหรับสินค้าและใบแจ้งหนี้

| บัญชีหลัก | ยอดเงินเดบิต | ยอดเงินเครดิต |
|---|---|---|
| **รายการสมุดรายวันสินค้า 1000** | | | 
| บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน (401250) | $1,465.26 | |
| บัญชีรายได้ที่รอการตัดบัญชี (250600) | | $1,465.26 |
| **รายการสมุดรายวันสินค้า 0021** | | | 
| บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน (401250) | $274.74 | |
| บัญชีรายได้ที่รอการตัดบัญชี (250600) | | $274.74 |
| **ใบแจ้งหนี้** | | |
| บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน | | $1,465.26 |
| บัญชีรายได้ที่ยังไม่ได้เรียกเก็บเงิน | | $274.74 |
| บัญชี AR (130100) | $1,488.16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>การเปลี่ยนแปลงรายการกำหนดการเรียกเก็บเงิน รายการรายละเอียดการเรียกเก็บเงิน หรือการปันส่วนรายได้

เมื่อมีการเปลี่ยนแปลงราคาต่อหน่วยหรือปริมาณ ต้องอัปเดตยอดเงินรายได้ของสัญญาของสินค้าแต่ละรายการที่เป็นส่วนหนึ่งของการปันส่วนรายได้ ดังนั้น จึงมีการคำนวณรายการสมุดรายวันใหม่

ตัวอย่างเช่น ราคาต่อหน่วยของสินค้า 1000 จะเปลี่ยนจาก $1,500 เป็น $1,600 ในกรณีนี้ ยอดเงินรายได้ของสัญญาจะถูกคำนวณเป็น $1,549.47 โดยอัตโนมัติ รายได้ของสัญญาของสินค้า S0021 จะมีการคำนวณใหม่เป็น $290.53

เมื่อยืนยันและยอมรับการเปลี่ยนแปลง รายการสมุดรายวันเริ่มต้นของสินค้าทั้งสองจะถูกกลับรายการ และมีการสร้างรายการสมุดรายวันใหม่

- **สินค้า 1000:** กลับรายการสมุดรายวันเริ่มต้นของเดิม $1,465.26 มีการสร้างรายการสมุดรายวันใหม่เป็น $1,549.47
- **สินค้า S0021:** กลับรายการสมุดรายวันเริ่มต้นของเดิม $274.74 มีการสร้างรายการสมุดรายวันใหม่เป็น $290.53

#### <a name="termination"></a>การสิ้นสุดการจ้างงาน

สินค้า S0021 มีวันที่เริ่มต้นอยู่ในเดือนมกราคม 2020 และวันที่สิ้นสุดในเดือนธันวาคม 2020 แต่ถูกยกเลิกในเดือนมิถุนายน ยอดเงินรายได้ของสัญญาของสินค้าทั้งสองต้องได้รับการคำนวณใหม่:

- **สินค้า 1000:** รายได้ของสัญญามีการคำนวณใหม่เป็น $1,567.67
- **สินค้า S0021:** รายได้ของสัญญามีการคำนวณใหม่เป็น $124.00

ระบบจะสร้างรายการสมุดรายวันการปรับปรุงขึ้นเนื่องจากรายการที่ถูกยกเลิก รายการสมุดรายวันของรายการที่เป็นของหมายเลขการจัดเตรียมแบบหลายองค์ประกอบ (MEA) เดียวกันจะถูกกลับรายการ และรายการสมุดรายวันใหม่จะถูกสร้างขึ้น

- **สินค้า 1000:** กลับรายการสมุดรายวันเริ่มต้นของเดิม $1,465.26 มีการสร้างรายการสมุดรายวันการปรับปรุงเป็น $1,549.47
- **สินค้า S0021:** กลับรายการสมุดรายวันเริ่มต้นของเดิม $274.74 มีการสร้างรายการสมุดรายวันใหม่เป็น $124.00
