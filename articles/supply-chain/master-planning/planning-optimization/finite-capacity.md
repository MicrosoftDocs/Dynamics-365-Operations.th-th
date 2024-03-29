---
title: การวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัด
description: การวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัดช่วยให้คุณเข้าใจปริมาณงานที่สามารถผลิตได้ในระหว่างรอบระยะเวลาเฉพาะ เมื่อมีการพิจารณาข้อจํากัดเกี่ยวกับทรัพยากรต่างๆ
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 5f02ec58c88cfd0d663a97de4e3e4dff1cdd5e90
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740098"
---
# <a name="finite-capacity-planning-and-scheduling"></a>การวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัด

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

กำลังการผลิตมีจำกัดช่วยให้คุณเข้าใจปริมาณงานที่สามารถผลิตได้ในระหว่างรอบระยะเวลาเฉพาะ เมื่อมีการพิจารณาข้อจํากัดเกี่ยวกับทรัพยากรต่างๆ วัตถุประสงค์ของการจัดกำหนดการกำลังการผลิตมีจำกัดคือเพื่อให้แน่ใจว่างานจะดําเนินการต่อไปในระดับที่ราบรื่นและมีประสิทธิภาพทั่วทั้งโรงงาน

การวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัดสร้างกำหนดการที่สมจริงมากขึ้นสำหรับกระบวนการผลิตมากกว่าวิธีการใช้กำลังการผลิตไม่จำกัด ถ้ามีกำลังการผลิตของทรัพยากรไม่เพียงพอ วันที่จัดส่งจะถูกเลื่อนออกไปและงานจะมีการจัดกำหนดการเมื่อมีกำลังการผลิตเพียงพอ

> [!NOTE]
> การวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัดทำงานเกือบเหมือนกัน ไม่ว่าคุณจะใช้การเพิ่มประสิทธิภาพการวางแผนหรือกลไกจัดการการวางแผนหลักที่ไม่สนับสนุน อย่างไรก็ตาม การเพิ่มประสิทธิภาพการวางแผนไม่ได้ใช้พารามิเตอร์ **กรอบเวลาสภาวะคอขวด** เมื่อคุณใช้การเพิ่มประสิทธิภาพการวางแผน ทรัพยากรที่ติดขัดจะถูกจัดกำหนดการโดยใช้กรอบเวลาเดียวกันกับทรัพยากรที่ไม่ติดขัดเสมอ (ตามที่ระบุโดยกรอบเวลากำลังการผลิตมีจำกัด)

## <a name="set-up-finite-capacity-functionality"></a>ตั้งค่าฟังก์ชันกำลังการผลิตมีจำกัด

หากต้องการใช้ฟังก์ชันกำลังการผลิตมีจำกัด คุณต้องเปิดใช้งานการวางแผนการผลิตแบบส่วนรวม และคุณต้องเปิดใช้งานการวางแผนกำลังการผลิตกับทั้งแผนหลักที่คุณต้องการใช้และทรัพยากรแต่ละรายการที่จะใช้ สำหรับแผนและทรัพยากรที่มีการเปิดใช้งานกำลังการผลิตมีจำกัด การจัดกำหนดการแผนการใบสั่งผลิตจะถือว่ากำลังการผลิตมีการสำรองไว้อยู่แล้ว แผนการใบสั่งผลิตจะมีการจัดกำหนดการแบบย้อนหลังจากวันที่ความต้องการ ถ้าไม่มีกำลังการผลิตที่ตรงกับกำหนดการที่มีประสิทธิภาพสูงสุด ระบบจะพยายามใช้สินค้าที่เป็นส่วนประกอบในวันที่ก่อนหน้านั้น ถ้ากำลังการผลิตของคุณสามารถเปลี่ยนได้ตามความต้องการที่เปลี่ยนไป (เช่น เมื่อคุณกำลังทำงานเป็นกะ) คุณไม่ควรใช้ฟังก์ชันกำลังการผลิตมีจำกัด เนื่องจากเวลาในการประมวลผลที่คำนวณจะไม่ถูกต้อง การจัดกำหนดการจะพิจารณาเฉพาะกำลังการผลิตที่สำรองไว้แล้วของทรัพยากรที่มีการเปิดใช้งานกำลังการผลิตมีจำกัด ด้วยการเปิดใช้งานกำลังการผลิตมีจำกัดสำหรับทรัพยากรหนึ่งๆ คุณสามารถปรับเปลี่ยนกรอบเวลากำลังการผลิตมีจำกัดได้

### <a name="activate-master-planning-parameters"></a>เปิดใช้งานพารามิเตอร์การวางแผนหลัก

หากต้องการใช้ฟังก์ชันกำลังการผลิตมีจำกัด คุณต้องเปิดใช้งานการวางแผนกำลังการผลิตในหน้า **พารามิเตอร์การวางแผนหลัก**

1. ไปที่ **การวางแผนหลัก \> การตั้งค่า \> พารามิเตอร์การวางแผนหลัก**
1. บนแท็บ **แผนการใบสั่ง** ในส่วน **การวางแผนกำลังการผลิต** ให้ตั้งค่าตัวเลือก **การผลิต** เป็น *ใช่*

### <a name="activate-a-master-plan"></a>เปิดใช้งานแผนหลัก

คุณต้องเปิดใช้งานการวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัดสำหรับแผนหลักแต่ละแผนที่คุณต้องการใช้งาน

1. ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก**
1. ในบานหน้าต่างรายการ ให้เลือกแผนหลักที่คุณต้องการตั้งค่าให้ใช้การวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัด
1. บนแท็บด่วน **ทั่วไป** ในส่วน **แผนการใบสั่งผลิต** ให้ตั้งค่าตัวเลือก **กำลังการผลิตมีจำกัด** เป็น *ใช่*
1. ทําซ้ำขั้นตอนที่ 2 และ 3 กับแผนหลักเพิ่มเติมที่คุณต้องการตั้งค่า

### <a name="activate-resources"></a>เปิดใช้งานทรัพยากร

คุณต้องเปิดใช้งานการวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัดสำหรับทรัพยากรแต่ละอย่างที่คุณต้องการใช้งาน

1. ไปที่ **การควบคุมการผลิต \> การตั้งค่า \> ทรัพยากร \> ทรัพยากร**
1. ในบานหน้าต่างรายการ ให้เลือกทรัพยากรที่คุณต้องการตั้งค่าให้ใช้การวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัด
1. บนแท็บด่วน **การดำเนินงาน** ในส่วน **ปุ่มกำลังการผลิต** ให้ตั้งค่าตัวเลือก **กำลังการผลิตมีจำกัด** เป็น *ใช่*
1. ทําซ้ำขั้นตอนที่ 2 และ 3 กับทรัพยากรเพิ่มเติมแต่ละอย่างที่คุณต้องการตั้งค่า

## <a name="examples"></a>ตัวอย่างเช่น

ส่วนนี้มีตัวอย่างต่อไปนี้ซึ่งแสดงวิธีการทำงานกับทั้งการวางแผนและการจัดกำหนดการกำลังการผลิตมีจำกัดและไม่จำกัด:

- ตัวอย่างที่ 1 – การวางแผนกำลังการผลิตไม่จำกัด
- ตัวอย่างที่ 2 – การวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาหนึ่งวัน
- ตัวอย่างที่ 3 – การวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาสองวัน

### <a name="preconditions"></a>เงื่อนไขเบื้องต้น

ตัวอย่างทั้งสามจะถือเป็นเงื่อนไขเบื้องต้นที่อธิบายไว้ในส่วนนี้

ผลิตภัณฑ์ *ผลิตภัณฑ์1* มีกระบวนการผลิตที่ประกอบด้วยการดําเนินงานต่อไปนี้

| หมายเลขการดำเนินงาน | ชื่อการดำเนินงาน | ทรัพยากร        | เวลาที่ใช้ในการผลิต | ปริมาณกระบวนการ | ถัดไป |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | การเชื่อม        | สายการเชื่อม    | 1        | 2            | 20   |
| 20            | การประกอบ     | สายการประกอบ | 1        | 4            |      |

ผู้ปฏิบัติงานที่บริษัทของคุณลางานหนึ่งกะเป็นเวลาแปดชั่วโมง (8:00–16:00)

มีใบสั่งผลิตตามกำหนดการจำนวน *24 ชิ้น* ของ *ผลิตภัณฑ์1* มีวันที่ส่งเป็น *วันนี้ + 3 วัน*

ตามการวางแผน ระบบจะใช้ทรัพยากรในลักษณะต่อไปนี้:

- **สายการเชื่อม:** มีการใช้ทรัพยากรนี้ตั้งแต่ *วันนี้เวลา 8:00* จนถึง *วันนี้ + 1 เวลา 12:00*
- **สายการประกอบ:** มีการใช้ทรัพยากรนี้ตั้งแต่ *วันนี้ + 1 เวลา 12:00* จนถึง *วันนี้ + 2 เวลา 10:00*

รูปภาพประกอบต่อไปนี้จะแสดงแผนภูมิแกนต์ที่ได้ (เลือกแผนภูมิเพื่อดูในมุมมองที่ใหญ่ขึ้น)

[![แผนภูมิแกนต์แสดงเงื่อนไขที่กำหนดล่วงหน้า](media/finite-examples-conditions-small.png "แผนภูมิแกนต์แสดงเงื่อนไขเบื้องต้น")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>ตัวอย่างที่ 1 – การวางแผนกำลังการผลิตไม่จำกัด

ตัวอย่างนี้แสดงผลลัพธ์การวางแผนเมื่อคุณใช้การวางแผนกำลังการผลิตไม่จำกัดแทนที่จะเป็นการวางแผนกำลังการผลิตมีจำกัด

แผนหลักมีการตั้งค่าที่เกี่ยวข้องต่อไปนี้ ซึ่งปิดใช้งานการวางแผนกำลังการผลิตมีจำกัดสำหรับแผน:

- **กำลังการผลิตมีจำกัด:** *ไม่ใช่*

นอกจากนี้ตัวเลือก **กำลังการผลิตมีจำกัด** ยังตั้งค่าเป็น *ไม่ใช่* สำหรับทั้งทรัพยากรที่เกี่ยวข้องเพื่อปิดใช้งานการวางแผนกำลังการผลิตมีจำกัดสำหรับทั้งคู่ด้วย:

- สายการเชื่อม
- สายการประกอบ

ขณะนี้คุณเพิ่มใบสั่งขายใหม่สำหรับจำนวน *8 ชิ้น* ของ *ผลิตภัณฑ์1* และเรียกใช้แผน ดังนั้น ระบบจะใช้สายการเชื่อมตั้งแต่ *วันนี้เวลา 8:00* จนถึง *วันนี้เวลา 12:00* หลังจากดําเนินงานในสายการเชื่อมเสร็จสมบูรณ์ ระบบจะใช้สายการประกอบตั้งแต่ *วันนี้เวลา 12:00* จนถึง *วันนี้เวลา 14:00*

รูปภาพประกอบต่อไปนี้จะแสดงแผนภูมิแกนต์ที่ได้ (เลือกแผนภูมิเพื่อดูในมุมมองที่ใหญ่ขึ้น)

[![แผนภูมิแกนต์แสดงตัวอย่างการวางแผนกำลังการผลิตไม่จำกัด](media/finite-examples-example1-small.png "แผนภูมิแกนต์แสดงตัวอย่างการวางแผนกำลังการผลิตไม่จำกัด")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>ตัวอย่างที่ 2 – การวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาหนึ่งวัน

ตัวอย่างนี้แสดงผลลัพธ์การวางแผนเมื่อคุณใช้การวางแผนกำลังการผลิตมีจำกัดและกรอบเวลาหนึ่งวัน

แผนหลักมีการตั้งค่าที่เกี่ยวข้องต่อไปนี้ ซึ่งเปิดใช้งานการวางแผนกำลังการผลิตมีจำกัดและตั้งค่ากรอบเวลาสำหรับแผน:

- **กำลังการผลิตมีจำกัด:** *ใช่*
- **กรอบเวลากำลังการผลิตมีจำกัด:** *1*

นอกจากนี้ตัวเลือก **กำลังการผลิตมีจำกัด** ยังตั้งค่าเป็น *ใช่* สำหรับทั้งทรัพยากรที่เกี่ยวข้องเพื่อเปิดใช้งานการวางแผนกำลังการผลิตมีจำกัดสำหรับทั้งคู่ด้วย:

- สายการเชื่อม
- สายการประกอบ

ขณะนี้คุณเพิ่มใบสั่งขายใหม่สำหรับจำนวน *8 ชิ้น* ของ *ผลิตภัณฑ์1* และเรียกใช้แผน ดังนั้น ระบบจะใช้สายการเชื่อมตั้งแต่ *วันนี้ + 1 เวลา 8:00* จนถึง *วันนี้ + 1 เวลา 12:00* หลังจากดําเนินงานในสายการเชื่อมเสร็จสมบูรณ์ ระบบจะใช้สายการประกอบตั้งแต่ *วันนี้ + 1 เวลา 12:00* จนถึง *วันนี้ + 1 เวลา 14:00* ระบบจะพิจารณากำลังการผลิตมีจำกัดสำหรับหนึ่งวันเท่านั้น

รูปภาพประกอบต่อไปนี้จะแสดงแผนภูมิแกนต์ที่ได้ (เลือกแผนภูมิเพื่อดูในมุมมองที่ใหญ่ขึ้น)

[![แผนภูมิแกนต์แสดงการวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาหนึ่งวัน](media/finite-examples-example2-small.png "แผนภูมิแกนต์แสดงการวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาหนึ่งวัน")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>ตัวอย่างที่ 3 – การวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาสองวัน

ตัวอย่างนี้แสดงผลลัพธ์การวางแผนเมื่อคุณใช้การวางแผนกำลังการผลิตมีจำกัดและกรอบเวลาสองวัน

แผนหลักมีการตั้งค่าที่เกี่ยวข้องต่อไปนี้ ซึ่งเปิดใช้งานการวางแผนกำลังการผลิตมีจำกัดและตั้งค่ากรอบเวลาสำหรับแผน:

- **กำลังการผลิตมีจำกัด:** *ใช่*
- **กรอบเวลากำลังการผลิตมีจำกัด:** *2*

นอกจากนี้ตัวเลือก **กำลังการผลิตมีจำกัด** ยังตั้งค่าเป็น *ใช่* สำหรับทั้งทรัพยากรที่เกี่ยวข้องเพื่อเปิดใช้งานการวางแผนกำลังการผลิตมีจำกัดสำหรับทั้งคู่ด้วย:

- สายการเชื่อม
- สายการประกอบ

ขณะนี้คุณเพิ่มใบสั่งขายใหม่สำหรับจำนวน *8 ชิ้น* ของ *ผลิตภัณฑ์1* และเรียกใช้แผน ดังนั้น ระบบจะใช้สายการเชื่อมตั้งแต่ *วันนี้ + 1 เวลา 12:00* จนถึง *วันนี้ + 1 เวลา 16:00* หลังจากดําเนินงานในสายการเชื่อมเสร็จสมบูรณ์ ระบบจะใช้สายการประกอบตั้งแต่ *วันนี้ + 2 เวลา 8:00* จนถึง *วันนี้ + 2 เวลา 10:00* ระบบจะพิจารณากำลังการผลิตมีจำกัดสำหรับสองวันเท่านั้น

รูปภาพประกอบต่อไปนี้จะแสดงแผนภูมิแกนต์ที่ได้ (เลือกแผนภูมิเพื่อดูในมุมมองที่ใหญ่ขึ้น)

[![แผนภูมิแกนต์แสดงการวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาสองวัน](media/finite-examples-example3-small.png "แผนภูมิแกนต์แสดงการวางแผนกำลังการผลิตมีจำกัดที่มีกรอบเวลาสองวัน")](media/finite-examples-example3.png)

> [!IMPORTANT]
> คุณควรตั้งค่ากรอบเวลากำลังการผลิตมีจำกัดตามความต้องการทางธุรกิจของคุณเสมอ ตัวอย่างที่ให้ไว้ในบทความนี้เพียงแต่แสดงฟังก์ชันเท่านั้น ในความเป็นจริง กรอบเวลาแบบวันเดียวอาจต่ำเกินไปสำหรับผู้ผลิตส่วนใหญ่ที่ใช้การวางแผนกำลังการผลิตมีจำกัด
