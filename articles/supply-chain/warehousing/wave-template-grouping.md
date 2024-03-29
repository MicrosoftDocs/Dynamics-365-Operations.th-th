---
title: การจัดกลุ่มเท็มเพลตเวฟ
description: การจัดกลุ่มเท็มเพลตเวฟช่วยให้ระบบสามารถใช้การตั้งค่าเท็มเพลตเวฟเพื่อกำหนด โดยยึดตามเงื่อนไขที่คุณกำหนด วิธีการที่ควรแบ่งรายการที่นำออกใช้และกำหนดให้กับเวฟใหม่หรือเวฟที่มีอยู่ คุณลักษณะนี้อาจเป็นประโยชน์ในคลังสินค้าที่มีการสร้างเวฟตามเงื่อนไขที่ระบุ แต่ผู้จัดการต้องการสร้างเวฟโดยอัตโนมัติ แทนที่จะเป็นแบบด้วยตนเอง
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a48e6a81299badf4b811e1cf905beb06099e5a24
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335989"
---
# <a name="wave-template-grouping"></a>การจัดกลุ่มเท็มเพลตเวฟ

[!include [banner](../includes/banner.md)]

การจัดกลุ่มเท็มเพลตเวฟช่วยให้ระบบสามารถใช้การตั้งค่า [เท็มเพลตเวฟ](tasks/configure-wave-processing.md) เพื่อกำหนด โดยยึดตามเงื่อนไขที่คุณกำหนด วิธีการที่ควรแบ่งรายการที่นำออกใช้และกำหนดให้กับเวฟใหม่หรือเวฟที่มีอยู่ คุณลักษณะนี้อาจเป็นประโยชน์ในคลังสินค้าที่มีการสร้างเวฟตามเงื่อนไขที่ระบุ แต่ผู้จัดการต้องการสร้างเวฟโดยอัตโนมัติ แทนที่จะเป็นแบบด้วยตนเอง ซึ่งจะช่วยให้ระบบสามารถเพิ่มการจัดส่งที่นำออกใช้ใหม่แต่ละครั้งไปยังเวฟแรกที่พบว่ามีค่าฟิลด์การจัดกลุ่มที่ตรงกัน ถ้าไม่พบรายการที่ตรงกัน ระบบจะสร้างเวฟใหม่สำหรับการจัดส่งใหม่

> [!IMPORTANT]
> ไม่สนับสนุนการจัดกลุ่มเท็มเพลตเวฟสำหรับชนิดงาน *การเบิกวัตถุดิบในการผลิต* หรือ *การเบิกสินค้าคัมบัง* ทั้งนี้เนื่องจากการจัดกลุ่มเวฟจะขึ้นอยู่กับการจัดส่ง และชนิดงานเหล่านี้ไม่ได้ใช้การจัดส่ง

## <a name="turn-on-the-wave-template-grouping-feature"></a>เปิดคุณลักษณะการจัดกลุ่มเท็มเพลตเวฟ

ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การจัดกลุ่มเท็มเพลตเวฟ* ต้องมีการเปิดใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:

- **โมดูล:** *การจัดการคลังสินค้า*
- **ชื่อคุณลักษณะ:** *การจัดกลุ่มเท็มเพลตเวฟ*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>ตั้งค่าเท็มเพลตเวฟเพื่อใช้การจัดกลุ่มเท็มเพลตเวฟ

เมื่อต้องการทำให้การจัดกลุ่มเท็มเพลตเวฟพร้อมใช้งาน ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่า [เท็มเพลตเวฟ](tasks/configure-wave-processing.md) ของคุณ

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**
1. ในบานหน้าต่างด้านซ้าย ให้เลือกเท็มเพลตเวฟเพื่อตั้งค่า ถ้าคุณกำลังเตรียมทำงานผ่านสถานการณ์จำลองในภายหลังในบทความนี้โดยใช้ข้อมูลสาธิต ให้เลือกเท็มเพลต **62 ค่าเริ่มต้นของการจัดส่ง**
1. ให้เลือก **แก้ไข** เพื่อเปลี่ยนหน้าไปในโหมดแก้ไข
1. บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:

    - **ทำให้การสร้างเวฟเป็นแบบอัตโนมัติ:** *ใช่*
    - **กำหนดให้เปิดเวฟ:** *ใช่*
    - **ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า:** *ไม่*

1. ในบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบการสอบถาม
1. ในกล่องโต้ตอบการสอบถาม บนแท็บ **การเรียงลำดับ** ให้รีวิวเงื่อนไขการเรียงลำดับ และตรวจสอบให้แน่ใจว่ามีกฎที่มีฟิลด์ที่คุณต้องการใช้ในการจัดกลุ่มเวฟของคุณ

    ถ้าคุณกำลังเตรียมทำงานผ่านสถานการณ์จำลองโดยใช้ข้อมูลสาธิต ให้เพิ่มแถวที่มีค่าต่อไปนี้:

    - **ตาราง:** *การจัดส่ง*
    - **ตารางสืบทอด:** *การจัดส่ง*
    - **ฟิลด์:** *บริการขนส่ง*

        > [!NOTE]
        > หลังจากที่คุณเลือกค่านี้ คุณอาจได้รับข้อความต่อไปนี้: "บริการผู้ขนส่งฟิลด์ไม่ใช่ฟิลด์ดัชนี คุณต้องการเพิ่มการเรียงลำดับหรือไม่" เลือก **ใช่** เพื่อเพิ่มการเรียงลำดับ

    - **ทิศทางการค้นหา:** *การเรียงจากน้อยไปมาก*

1. เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ และปิดกล่องโต้ตอบการสอบถาม
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **การจัดกลุ่มเท็มเพลตเวฟ**
1. บนหน้า **การจัดกลุ่มเท็มเพลตเวฟ** ให้เลือกกล่องกาเครื่องหมาย **จัดกลุ่มโดย** สำหรับแถวแต่ละแถวที่คุณต้องการใช้ในการจัดกลุ่มรายการใบสั่งของคุณเป็นเวฟตามต้องการ ถ้าคุณกำลังเตรียมทำงานผ่านสถานการณ์จำลองโดยใช้ข้อมูลสาธิต ให้เลือกกล่องกาเครื่องหมาย **จัดกลุ่มโดย** สำหรับแถว *บริการขนส่ง*
1. เลือก **บันทึก**
1. ปิดหน้า **การจัดกลุ่มเท็มเพลตเวฟ**
1. เลือก **บันทึก** เพื่อบันทึกเท็มเพลตของคุณ

## <a name="scenario"></a>สถานการณ์

ส่วนนี้จะให้สคริปต์ที่คุณสามารถทำงานผ่านการเรียนรู้ว่าคุณลักษณะนี้คืออะไรและทำงานกับคุณลักษณะนี้อย่างไร

### <a name="make-sample-data-available"></a>ทำให้ข้อมูลตัวอย่างพร้อมใช้งาน

เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/fin-ops/get-started/demo-data.md) มาตรฐาน นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น

นอกจากนี้ คุณยังสามารถใช้สถานการณ์จำลองนี้เป็นคำแนะนำสำหรับการใช้คุณลักษณะ เมื่อคุณทำงานในระบบการผลิต อย่างไรก็ตาม ในกรณีดังกล่าว คุณต้องแทนที่ค่าของคุณเอง และคุณอาจขาดเรกคอร์ดที่จำเป็นบางชนิดที่ข้อมูลสาธิตมาตรฐานมีให้

### <a name="scenario-wave-template-grouping"></a>สถานการณ์จำลอง: การจัดกลุ่มเท็มเพลตเวฟ

สถานการณ์นี้แสดงวิธีการใช้การจัดกลุ่มเท็มเพลตเวฟเพื่อสร้างเวฟหลายรายการโดยอัตโนมัติ โดยยึดตามเงื่อนไขการจัดกลุ่มที่กำหนดไว้ในเท็มเพลตเวฟ ในสถานการณ์สมมตินี้ เท็มเพลตเวฟถูกตั้งค่าในระบบเพื่อสร้างหนึ่งเวฟต่อหนึ่งบริการขนส่ง

ก่อนที่คุณจะเริ่มต้น ให้เตรียมเท็มเพลตเวฟตามที่อธิบายไว้ในส่วน [ตั้งค่าเท็มเพลตเวฟเพื่อใช้การจัดกลุ่มเท็มเพลตเวฟ](#set-up-template) ก่อนหน้านี้ในบทความนี้ ถ้าคุณจะทำงานกับข้อมูลสาธิตสำหรับสถานการณ์นี้ โปรดตรวจสอบให้แน่ใจว่าได้ใช้ค่าข้อมูลสาธิตที่แนะนำไว้ในกระบวนงานดังกล่าว การตั้งค่านี้จะจัดกลุ่มเวฟของคุณตามบริการขนส่งที่ตั้งค่าไว้สำหรับใบสั่งขายแต่ละใบ

#### <a name="create-sales-order-1"></a>สร้างใบสั่งขาย 1

1. ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**
1. เลือก **สร้าง** เพื่อสร้างใบสั่งขาย
1. ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:

    - บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-004*
    - บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น *62*

1. เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ **สร้างใบสั่งขาย**
1. ใบสั่งขายใหม่เปิดอยู่ในมุมมอง **รายการ** สร้างบันทึกย่อของหมายเลขใบสั่งขาย
1. สลับไปยังมุมมอง **ส่วนหัว**
1. บน FastTab **การจัดส่ง** ในส่วน **การขนส่ง** ให้ตั้งค่าค่าต่อไปนี้:

    - **ผู้ขนส่งสินค้า:** *สายการบิน*
    - **บริการขนส่ง:** *อากาศ*

1. สลับกลับไปยังมุมมอง **รายการ**
1. ในส่วน **รายกาใบสั่งขาย** ให้เลือก **เพิ่มรายการ** เพื่อเพิ่มรายการไปยังกริด
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **หมายเลขสินค้า:** *A0002*
    - **ปริมาณ:** *2*

1. เลือกรายการใบสั่งใหม่ และจากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**
1. บนหน้า **การจอง** ในบานหน้าต่างการดำเนินการ ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า
1. ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**
1. คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้ จดบันทึกหมายเลขรหัสเวฟและหมายเลขรหัสการจัดส่ง

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>ดูเวฟที่สร้างขึ้นจากใบสั่งขาย 1

1. ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**
1. เลือกรหัสเวฟที่สร้างขึ้นจากใบสั่งขาย
1. เลือกลิงก์รหัสเวฟเพื่อเปิดหน้ารายละเอียดเวฟ
1. โปรดสังเกตว่ามีการเพิ่มการจัดส่งไปยัง FastTab **รายการเวฟ**

#### <a name="create-sales-order-2"></a>สร้างใบสั่งขาย 2

1. ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**
1. เลือก **สร้าง** เพื่อสร้างใบสั่งขาย
1. ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:

    - บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-005*
    - บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น *62*

1. เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ **สร้างใบสั่งขาย**
1. ใบสั่งขายใหม่เปิดอยู่ในมุมมอง **รายการ** สร้างบันทึกย่อของหมายเลขใบสั่งขาย
1. สลับไปยังมุมมอง **ส่วนหัว**
1. บน FastTab **การจัดส่ง** ในส่วน **การขนส่ง** ให้ตั้งค่าค่าต่อไปนี้:

    - **ผู้ขนส่งสินค้า:** *Flower moving*
    - **บริการขนส่ง:** *Std*

1. สลับกลับไปยังมุมมอง **รายการ**
1. ในส่วน **รายกาใบสั่งขาย** ให้เลือก **เพิ่มรายการ** เพื่อเพิ่มรายการไปยังกริด
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **หมายเลขสินค้า:** *A0001*
    - **ปริมาณ:** *1*

1. เลือกรายการใบสั่งใหม่ และจากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**
1. บนหน้า **การจอง** ในบานหน้าต่างการดำเนินการ ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า
1. ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**
1. คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้ จดบันทึกหมายเลขรหัสเวฟและหมายเลขรหัสการจัดส่ง โปรดสังเกตว่ารหัสเวฟแตกต่างจากรหัสเวฟของใบสั่งขายแรก

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>ดูเวฟที่สร้างขึ้นจากใบสั่งขาย 2

1. ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**
1. เลือกรหัสเวฟที่สร้างขึ้นจากใบสั่งขายที่สอง
1. เลือกลิงก์รหัสเวฟเพื่อเปิดหน้ารายละเอียดเวฟ
1. โปรดสังเกตว่ามีการเพิ่มการจัดส่งไปยัง FastTab **รายการเวฟ**

เวฟใหม่ถูกสร้างขึ้นสำหรับการจัดส่งนี้ เนื่องจากมีการใช้บริการขนส่งอื่นที่แตกต่างจากใบสั่งขายแรก

#### <a name="create-sales-order-3"></a>สร้างใบสั่งขาย 3

1. ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**
1. เลือก **สร้าง** เพื่อสร้างใบสั่งขาย
1. ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:

    - บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-006*
    - บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น *62*

1. เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ **สร้างใบสั่งขาย**
1. ใบสั่งขายใหม่เปิดอยู่ในมุมมอง **รายการ** สร้างบันทึกย่อของหมายเลขใบสั่งขาย
1. สลับไปยังมุมมอง **ส่วนหัว**
1. บน FastTab **การจัดส่ง** ในส่วน **การขนส่ง** ให้ตั้งค่าค่าต่อไปนี้:

    - **ผู้ขนส่งสินค้า:** *สายการบิน*
    - **บริการขนส่ง:** *อากาศ*

1. สลับกลับไปยังมุมมอง **รายการ**
1. ในส่วน **รายกาใบสั่งขาย** ให้เลือก **เพิ่มรายการ** เพื่อเพิ่มรายการไปยังกริด
1. บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **หมายเลขสินค้า:** *A0001*
    - **ปริมาณ:** *1*

1. เลือกรายการใบสั่งใหม่ และจากนั้น บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจอง**
1. บนหน้า **การจอง** ในบานหน้าต่างการดำเนินการ ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า
1. ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**
1. คุณได้รับข้อความที่ให้ข้อมูลซึ่งแสดงการจัดส่งและเวฟสำหรับใบสั่งนี้ จดบันทึกหมายเลขรหัสเวฟและหมายเลขรหัสการจัดส่ง การจัดส่งได้รับการกำหนดให้กับเวฟที่มีอยู่จากใบสั่งขายแรก

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>ดูเวฟสำหรับใบสั่งขาย 1 และ 3

1. ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**
1. เลือกรหัสเวฟที่สร้างขึ้นจากใบสั่งขายที่สาม
1. เลือกลิงก์รหัสเวฟเพื่อเปิดหน้ารายละเอียดเวฟ
1. โปรดสังเกตว่ามีการเพิ่มการจัดส่งไปยัง FastTab **รายการเวฟ** พร้อมกับการจัดส่งสำหรับใบสั่งขายแรก


[!INCLUDE[footer-include](../../includes/footer-banner.md)]