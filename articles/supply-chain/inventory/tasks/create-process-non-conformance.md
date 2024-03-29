---
title: สร้างและประมวลผลความไม่สอดคล้องกัน
description: บทความนี้อธิบายวิธีการดำเนินการจัดการความไม่สอดคล้องกัน โดยขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd8a10e88ab4d1be24a11739dddd7619b3fa6bbc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901979"
---
# <a name="create-and-process-nonconformances"></a>สร้างและประมวลผลความไม่สอดคล้องกัน

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการดำเนินการจัดการความไม่สอดคล้องกัน โดยขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่ โดยทั่วไป การจัดการความไม่สอดคล้องกันจะถูกดำเนินการโดยเจ้าหน้าที่ตรวจสอบคุณภาพ คุณต้องมีใบสั่งตรวจสอบคุณภาพที่พร้อมใช้งาน ตามข้อกำหนดเบื้องต้น (สำหรับข้อมูลเกี่ยวกับวิธีการสร้างใบสั่งตรวจสอบคุณภาพ ดูที่ [ตรวจสอบคุณภาพของสินค้า](inspect-quality-goods.md))

ก่อนที่ผู้ใช้จะสามารถประมวลผลการอนุมัติความไม่สอดคล้องกันได้ ต้องมอบหมายผู้ปฏิบัติงานให้กับผู้ปฏิบัติงานในฟิลด์ **บุคคล** ในหน้า **ผู้ใช้** นอกจากนี้ ก่อนที่ผู้ใช้สามารถใช้บันทึกเอกสารได้ ต้องตั้งค่าตัวเลือก **เปิดใช้งานการจัดการเอกสาร** เป็น *ใช่* ในตัวเลือกผู้ใช้

## <a name="create-a-nonconformance"></a>สร้างความไม่สอดคล้องกัน

เมื่อต้องการสร้างความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. บนหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในกล่องโต้ตอบ **สร้างความไม่สอดคล้องกัน** ในฟิลด์ **ชนิดของปัญหา** ให้เลือกชนิดของปัญหาที่พบในระหว่างกระบวนการตรวจสอบ
1. เลือก **ตกลง**

## <a name="approve-or-reject-a-nonconformance"></a>อนุมัติหรือปฏิเสธความไม่สอดคล้องกัน

ในการอนุมัติหรือปฏิเสธความไม่สอดคล้องกัน ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต

    > [!NOTE]
    > คุณสามารถเพิ่มการแก้ไขไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

1. ในบานหน้าต่างการดำเนินการ เลือก **ฟังก์ชัน \> อนุมัติความไม่สอดคล้องกัน** เพื่ออนุมัติความไม่สอดคล้องกันหรือ **ฟังก์ชัน \> ปฏิเสธความไม่สอดคล้องกัน** เพื่อปฏิเสธ คุณสามารถเชื่อมโยงความไม่สอดคล้องกันที่อนุมัติแล้วกับ [การดําเนินงานที่เกี่ยวข้อง](../quality-operations.md) ด้วยวิธีนี้ คุณสามารถบันทึกงานที่ได้เสร็จสิ้นเป็นส่วนหนึ่งของการจัดการความไม่สอดคล้องกันและการประมวลผลการจัดการการแก้ไข
1. คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ เลือก **ใช่** เพื่อดำเนินการต่อ

## <a name="add-operations-and-other-details-to-nonconformances"></a>เพิ่มการดําเนินงานและรายละเอียดอื่นๆ ให้กับความไม่สอดคล้องกัน

หลังจากที่คุณสร้างความไม่สอดคล้องกันแล้ว คุณสามารถเริ่มต้นเพิ่มการดําเนินงานที่เกี่ยวข้องและระบุข้อมูลเพิ่มเติมเกี่ยวกับการดําเนินงานเหล่านั้นได้ คุณสามารถเพิ่มการดําเนินงานที่เกี่ยวข้องไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

นอกจากข้อมูลพื้นฐานแล้ว คุณยังสามารถเพิ่มรายละเอียดต่อไปนี้ลงในการดําเนินงานได้:

- **สินค้า** – คุณสามารถสร้างรายการสินค้าที่จะใช้ในการดำเนินการแก้ไข ตัวอย่างเช่น สินค้าอาจเป็นผลิตภัณฑ์ที่ต้องใช้ในการซ่อมแซมอุปกรณ์ หรือส่วนผสมที่ต้องใช้ในการทำผลิตภัณฑ์สำเร็จรูปใหม่อีกครั้ง
- **ค่าธรรมเนียมคุณภาพ** – คุณสามารถสร้างรายการค่าธรรมเนียมที่เกิดขึ้นหรือถูกเรียกเก็บเงินจากแหล่งที่มาภายนอก
- **แผ่นเวลา** – คุณสามารถสร้างล็อกเวลาที่ผู้ปฏิบัติงานแต่ละคนใช้ในการดําเนินงาน

การตั้งค่าที่เหลือไม่จำเป็นต้องระบุ ต้นทุนสำหรับสินค้า ค่าธรรมเนียมคุณภาพ และแผ่นเวลาแต่ละรายการ จะถูกบวกรวมและแสดงในการดําเนินงาน คุณไม่สามารถแก้ไขฟิลด์ **ต้นทุน** ในการดําเนินงานได้โดยตรง

### <a name="create-an-operation-for-a-nonconformance"></a>สร้างการดำเนินงานสำหรับความไม่สอดคล้องกัน

ในการสร้างการดำเนินงานสำหรับความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต

    > [!NOTE]
    > คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

1. บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**
1. บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **การดําเนินงาน** – เลือกรหัสของการดําเนินงานที่จะดําเนินการสำหรับความไม่สอดคล้องกัน
    - **เหตุผล** – ป้อนคำอธิบายโดยละเอียดที่อธิบายเหตุผลที่ต้องมีการดําเนินงาน
    - **ใบสั่งขาย** – ถ้ารหัสการดําเนินงานที่เลือกเกี่ยวข้องกับชนิดใบสั่งขาย ให้เลือกใบสั่งขายที่คุณเชื่อมโยงการดําเนินงานด้วย
    - **ใบสั่งซื้อ** – ถ้ารหัสการดําเนินงานที่เลือกเกี่ยวข้องกับชนิดใบสั่งซื้อ ให้เลือกใบสั่งซื้อที่คุณเชื่อมโยงการดําเนินงานด้วย

1. ปิดหน้า

### <a name="add-items-to-an-operation"></a>เพิ่มสินค้าในการดําเนินงาน

ในการเพิ่มสินค้าลงในการดําเนินงาน ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต

    > [!NOTE]
    > คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

1. บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**
1. บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ให้เลือกการดําเนินงานที่คุณต้องการเพิ่มสินค้าลงไป
1. บนบานหน้าต่างการดำเนินการ เลือก **สินค้า**
1. บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด จากนั้น ให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **หมายเลขสินค้า** – เลือกผลิตภัณฑ์ที่จะใช้เป็นส่วนหนึ่งของการดําเนินงานที่เลือก
    - **ปริมาณ** – ป้อนจํานวนของสินค้าที่จะใช้

    > [!NOTE]
    > คุณสามารถดูต้นทุนสำหรับสินค้าในฟิลด์ **ต้นทุน** บนแท็บ **ทั่วไป** ต้นทุนที่แสดงที่นั่นจะมาจากต้นทุนที่ตั้งค่าไว้ในหน้า **ผลิตภัณฑ์ที่นำออกใช้** ไม่สามารถอัพเดตต้นทุนโดยตรงในหน้า **รายการของการดําเนินงานที่เกี่ยวข้อง** ต้นทุนของสินค้าทั้งหมดที่เพิ่มในหน้า **รายการของการดําเนินงานที่เกี่ยวข้อง** จะถูกเพิ่มโดยอัตโนมัติในฟิลด์ **ต้นทุน** บนหน้า **การดําเนินงานที่เกี่ยวข้อง**

1. ทําซ้ำขั้นตอนก่อนหน้านี้สำหรับสินค้าเพิ่มเติมแต่ละรายการที่คุณต้องเพิ่ม
1. ปิดหน้า

### <a name="add-quality-charges-to-an-operation"></a>เพิ่มค่าธรรมเนียมคุณภาพในการดําเนินงาน

ในการเพิ่มค่าธรรมเนียมคุณภาพลงในการดําเนินงาน ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต

    > [!NOTE]
    > คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

1. บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**
1. บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ให้เลือกการดําเนินงานที่คุณต้องการเพิ่มค่าธรรมเนียมคุณภาพลงไป
1. บนบานหน้าต่างการดำเนินการ เลือก **ค่าธรรมเนียมคุณภาพ**
1. บนหน้า **ค่าธรรมเนียมของการดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **รหัสค่าธรรมเนียม** – เลือกค่าธรรมเนียมคุณภาพที่คุณต้องการเพิ่ม
    - **คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของค่าธรรมเนียม
    - **มูลค่าของค่าธรรมเนียม** – ป้อนยอดเงินของค่าธรรมเนียม

1. ทําซ้ำขั้นตอนก่อนหน้านี้สำหรับค่าธรรมเนียมเพิ่มเติมแต่ละรายการที่คุณต้องเพิ่ม
1. ปิดหน้า

> [!NOTE]
> จํานวนเงินในฟิลด์ **มูลค่าค่าธรรมเนียม** จะถูกบวกรวมโดยอัตโนมัติสำหรับค่าธรรมเนียมคุณภาพทั้งหมด และถูกเพิ่มในยอดเงินอื่นๆ ในฟิลด์ **ต้นทุน** ในหน้า **การดําเนินงานที่เกี่ยวข้อง**

### <a name="create-a-timesheet-on-an-operation"></a>สร้างแผ่นเวลาในการดําเนินงาน

ในการเพิ่มแผ่นเวลาลงในการดําเนินงาน ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต

    > [!NOTE]
    > คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

1. บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**
1. บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ให้เลือกการดําเนินงานที่คุณต้องการเพิ่มแผ่นเวลาลงไป
1. บนบานหน้าต่างการดำเนินการ เลือก **แผ่นเวลา**
1. บนหน้า **แผ่นเวลาของการดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **วันที่** – ระบุวันที่เมื่องานเสร็จสิ้น โดยค่าเริ่มต้น ฟิลด์นี้ถูกตั้งค่าเป็นวันที่ปัจจุบัน
    - **ผู้ปฏิบัติงาน** – เลือกผู้ปฏิบัติงานที่ทำงาน โดยค่าเริ่มต้น ฟิลด์นี้จะถูกตั้งค่าเป็นผู้ปฏิบัติงานที่ได้รับมอบหมายให้กับผู้ใช้ปัจจุบัน
    - **ชั่วโมงการดําเนินงาน** – ป้อนจํานวนชั่วโมงที่มีการปฏิบัติงานในการดําเนินงานที่เลือก
    - **ออกใบแจ้งหนี้แล้ว** – เลือกกล่องกาเครื่องหมายนี้ ถ้ามีการคิดค่าธรรมเนียมเวลากับลูกค้าหรือผู้จัดจำหน่ายบนใบแจ้งหนี้

    > [!NOTE]
    > คุณสามารถดูต้นทุนในฟิลด์ **ต้นทุน** บนแท็บ **ทั่วไป** ต้นทุนจะถูกคํานวณโดยใช้อัตราที่คุณกําหนดในหน้า **พารามิเตอร์การบริหารสินค้าคงคลัง**

1. ทําซ้ำขั้นตอนก่อนหน้านี้สำหรับรายการแผ่นเวลาเพิ่มเติมแต่ละรายการที่คุณต้องเพิ่ม
1. ปิดหน้า

> [!NOTE]
> จํานวนเงินในฟิลด์ **ต้นทุน** จะถูกบวกรวมสำหรับรายการแผ่นเวลาทั้งหมด และถูกเพิ่มในยอดเงินอื่นๆ ในฟิลด์ **ต้นทุน** ในหน้า **การดําเนินงานที่เกี่ยวข้อง**

## <a name="add-a-correction-to-a-nonconformance"></a>เพิ่มการแก้ไขไปยังความไม่สอดคล้องกัน

ในการเพิ่มการแก้ไขไปยังความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต

    > [!NOTE]
    > คุณสามารถเพิ่มการแก้ไขไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

1. บนบานหน้าต่างการดำเนินการ เลือก **การแก้ไข**
1. บนหน้า **การแก้ไข** ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:

    - **การวินิจฉัย** – เลือกชนิดการวินิจฉัยที่ระบุชนิดของการแก้ไขที่คุณสร้างอยู่
    - **ผู้ปฏิบัติงาน** – เลือกผู้ที่รับผิดชอบการแก้ไข
    - **ระดับความสำคัญของการแก้ไข** – เลือกตัวเลือกเพื่อบ่งชี้ว่าควรจะจัดระดับความสำคัญของการแก้ไขอย่างไร (*ต่ำ* *ปกติ* หรือ *สูง*)
    - **วันที่ร้องขอ** – ป้อนวันที่ที่มีการร้องขอการดำเนินการแก้ไข
    - **วันที่วางแผนไว้** – ป้อนวันที่ที่คาดหวังให้การแก้ไขเสร็จสมบูรณ์
    - **วิธีแก้ไขปัญหาระยะสั้น** – เลือกกล่องกาเครื่องหมายนี้ ถ้าการดำเนินการแก้ไขแก้ไขความไม่สอดคล้องกันในระยะเวลาสั้นๆ เท่านั้น

1. ปิดหน้า

## <a name="mark-a-correction-as-completed"></a>ทำเครื่องหมายการแก้ไขเป็นเสร็จสมบูรณ์แล้ว

ในการทำเครื่องหมายการแก้ไขความไม่สอดคล้องกันเป็นเสร็จสมบูรณ์แล้ว ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต

    > [!NOTE]
    > คุณสามารถเพิ่มการแก้ไขไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น

1. บนบานหน้าต่างการดำเนินการ เลือก **การแก้ไข**
1. บนหน้า **การแก้ไข** ในกริด ให้เลือกการแก้ไขที่คุณต้องการทำเครื่องหมายเป็นเสร็จสมบูรณ์แล้ว
1. ในบานหน้าต่างการดำเนินการ เลือก **ทำเครื่องหมายเป็นเสร็จสมบูรณ์**
1. คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ เลือก **ตกลง** เพื่อดำเนินการต่อ มีการตั้งค่าฟิลด์ **วันที่และเวลาที่เสร็จสมบูรณ์** เป็นวันที่และเวลาปัจจุบัน และมีการเลือกกล่องกาเครื่องหมาย **เสร็จสมบูรณ์แล้ว**
1. ปิดหน้า

## <a name="reopen-a-completed-correction"></a>เปิดการแก้ไขที่เสร็จสมบูรณ์แล้วใหม่

ในการเปิดการแก้ไขที่เสร็จสมบูรณ์แล้วใหม่ ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**
1. ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต
1. บนบานหน้าต่างการดำเนินการ เลือก **การแก้ไข**
1. บนหน้า **การแก้ไข** ในกริด ให้เลือกการแก้ไขที่คุณต้องการเปิดใหม่
1. บนบานหน้าต่างการดำเนินการ เลือก **เปิดใหม่**
1. คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ เลือก **ตกลง** เพื่อดำเนินการต่อ ค่านี้จะถูกล้างข้อมูลจากฟิลด์ **วันที่และเวลาที่เสร็จสมบูรณ์** และมีการยกเลิกการเลือกกล่องกาเครื่องหมาย **เสร็จสมบูรณ์แล้ว**
1. ปิดหน้า

ขณะนี้ คุณสามารถทำการแก้ไขหรืออัพเดตเพิ่มเติมไปยังการแก้ไขได้ เมื่อคุณเสร็จสิ้นแล้ว คุณสามารถทำเครื่องหมายการแก้ไขเป็นเสร็จสมบูรณ์แล้วได้อีกครั้ง

## <a name="close-a-nonconformance"></a>ปิดความไม่สอดคล้องกัน

เมื่อต้องการปิดความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ใบสั่งตรวจสอบคุณภาพ**
1. เลือกใบสั่งตรวจสอบคุณภาพในกริด
1. บนบานหน้าต่างการดำเนินการ เลือก **การสอบถาม \> ความไม่สอดคล้องกัน**
1. บนหน้า **ความไม่สอดคล้องกัน** ให้เลือกความไม่สอดคล้องกันของเป้าหมายในกริด
1. บนบานหน้าต่างการดำเนินการ เลือก **ฟังก์ชัน \> ปิดความไม่สอดคล้องกัน**
1. คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ เลือก **ใช่** เพื่อดำเนินการต่อ
1. ปิดหน้า

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมของการจัดการคุณภาพ](../quality-management-processes.md)
- [เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน](../enable-quality-management.md)
- [ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน](../quality-responsible-workers.md)
- [โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน](../quality-quarantine-zones.md)
- [ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน](../quality-diagnostic-types.md)
- [ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน](../quality-charges.md)
- [การดำเนินงานสำหรับความไม่สอดคล้องกัน](../quality-operations.md)
- [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
