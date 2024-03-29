---
title: การตั้งค่าพารามิเตอร์การจัดการเครดิต
description: บทความนี้จะอธิบายถึงตัวเลือกที่คุณสามารถใช้เพื่อตั้งค่าคอนฟิกการจัดการเครดิต เพื่อให้ตรงกับความต้องการของธุรกิจของคุณได้
author: JodiChristiansen
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8955518e7b5c0200d3827c1c22b7d150a09be244
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799557"
---
# <a name="credit-management-parameters-setup"></a>การตั้งค่าพารามิเตอร์การจัดการเครดิต

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายถึงตัวเลือกที่คุณสามารถใช้เพื่อตั้งค่าคอนฟิกการจัดการเครดิต เพื่อให้ตรงกับความต้องการของธุรกิจของคุณได้ เมื่อต้องการใช้คุณลักษณะการจัดการสินเชื่อ ให้ตั้งค่าพารามิเตอร์บนหน้า **พารามิเตอร์สินเชื่อและการเรียกเก็บเงิน** (**สินเชื่อและการเรียกเก็บเงิน \> การตั้งค่า \> พารามิเตอร์สินเชื่อและการเรียกเก็บเงิน**)

## <a name="credit-parameters"></a>พารามิเตอร์เครดิต

มี FastTabs สี่แท็บในส่วน **สินเชื่อ** ที่ซึ่งคุณสามารถเปลี่ยนพารามิเตอร์ที่ควบคุมการจัดการสินเชื่อ: **การระงับสินเชื่อ** **จุดตรวจสอบการจัดการสินเชื่อ** **สถิติการจัดการสินเชื่อ** และ **วงเงินสินเชื่อ** ส่วนต่อไปนี้จะอธิบายถึงการตั้งค่าที่มีอยู่บนแท็บด่วนแต่ละแท็บ

### <a name="credit-holds"></a>การระงับสินเชื่อ

- ตั้งค่าตัวเลือก **การอนุญาตให้แก้ไขมูลค่าของใบสั่งขายหลังจากการระงับใบสั่งถูกนำออกใช้** เป็น **ไม่** เพื่อให้มีการตรวจกฎการลงรายการบัญชีอีกครั้ง หากมูลค่าใบสั่งขาย (ราคารวม) เพิ่มขึ้นเนื่องจากมีการนำใบสั่งขายออกใช้จากรายการที่ถูกระงับ
- ในฟิลด์ **เหตุผลสำหรับใบสั่งที่ถูกยกเลิก** ให้เลือกเหตุผลการนำออกใช้ ซึ่งจะใช้โดยค่าเริ่มต้น เมื่อยกเลิกใบสั่งขายที่มีการระงับการจัดการเครดิต
- ตั้งค่าตัวเลือก **ตรวจสอบวงเงินสินเชื่อของกลุ่มเครดิตลูกค้า** เป็น **ใช่** เพื่อตรวจสอบวงเงินสินเชื่อของกลุ่มเครดิตของลูกค้า เมื่อลูกค้าในใบสั่งขายเป็นสมาชิกของกลุ่มเครดิตของลูกค้า วงเงินสินเชื่อสำหรับกลุ่มจะมีการตรวจสอบ หลังจากนั้น ถ้าเพียงพอ เงินสินเชื่อของลูกค้าจะถูกตรวจสอบ
- ตั้งค่าตัวเลือก **ตรวจสอบวงเงินสินเชื่อเมื่อมีการเพิ่มเงื่อนไขการชำระ** เป็น **ใช่** เพื่อตรวจสอบการจัดอันดับเงื่อนไขการชำระเงิน เพื่อกำหนดว่าเงื่อนไขการชำระเงินในใบสั่งขายแตกต่างจากเงื่อนไขการชำระเงินเริ่มต้นสำหรับลูกค้าหรือไม่ ถ้าเงื่อนไขการชำระเงินใหม่มีอันดับสูงกว่าเงื่อนไขการชำระเงินดั้งเดิม ใบสั่งจะถูกระงับไว้ในการจัดการเครดิต
- ตั้งค่าตัวเลือก **ตรวจสอบวงเงินสินเชื่อเมื่อมีการเพิ่มส่วนลดการชำระเงิน** เป็น **ใช่** เพื่อตรวจสอบการจัดอันดับส่วนลดการชำระเงิน เพื่อกำหนดว่าส่วนลดเงินสดในใบสั่งขายแตกต่างจากส่วนลดเงินสดเริ่มต้นสำหรับลูกค้าหรือไม่ ถ้าส่วนลดเงินสดใหม่มีอันดับสูงกว่าส่วนลดเงินสดดั้งเดิม ใบสั่งจะถูกระงับไว้ในการจัดการเครดิต
- ในฟิลด์ **เหตุผลสำหรับการนำออกใช้ที่แก้ไขสำหรับใบสั่ง** ให้เลือกเหตุผลการนำออกใช้ซึ่งจะใช้โดยค่าเริ่มต้น เมื่อใบสั่งที่มีการปรับเปลี่ยนถูกนำออกใช้โดยอัตโนมัติจากการระงับการจัดการเครดิต
- ตั้งค่าตัวเลือก **ยกเลิกกฎการบล็อคที่หมดอายุเมื่อวันหมดอายุว่างเปล่า** เป็น **ใช่** เพื่อควบคุมลักษณะการทำงานของกฎ **วงเงินสินเชื่อหมดอายุ** ตั้งค่าตัวเลือกเป็น **ไม่ใช่** เพื่อบล็อคใบสั่งเมื่อวันหมดอายุว่างเปล่า
- ในการบริหารคลังสินค้า จำนวนงานในศูนย์การผลิตสามารถสร้างได้เมื่อมีการป้อนข้อมูลใบสั่งขาย ตั้งค่าตัวเลือก **ลบรายการจำนวนงานในศูนย์การผลิตที่ถูกบล็อค** เป็น **ไม่ใช่** เพื่อออกจากบรรทัดใบสั่งขายบนจำนวนงานในศูนย์การผลิต เมื่อใบสั่งขายอยู่ระหว่างการระงับเครดิต จำนวนงานในศูนย์การผลิตไม่สามารถประมวลผลได้ในขณะที่ใบสั่งขายถูกระงับ ตั้งค่าตัวเลือกเป็น **ใช่** เพื่อเอาบรรทัดใบสั่งขายออกจากจำนวนงานในศูนย์การผลิต เมื่อใบสั่งขายอยู่ระหว่างการระงับเครดิต หลังจากนั้นจำนวนงานในศูนย์การผลิตสามารถประมวลผลได้
- ใบสั่งขายจะถูกนำออกใช้โดยอัตโนมัติจากการตรวจทานการจัดการเครดิต ในฟิลด์ **เหตุผลที่จะนำออกใช้โดยอัตโนมัติ** ให้เลือกเหตุผลการนำออกใช้ซึ่งจะใช้โดยค่าเริ่มต้น เมื่อมีการนำใบสั่งขายออกใช้โดยอัตโนมัติ
- ใบสั่งขายจะถูกนำออกใช้โดยอัตโนมัติจากการตรวจทานการจัดการเครดิต ในฟิลด์ **นำออกใช้โดยอัตโนมัติ** ให้เลือก **ไม่มีการลงรายการบัญชี** เพื่อปล่อยการระงับของใบสั่ง คุณต้องรันกระบวนการที่มีการระงับใบสั่งด้วยตนเอง เลือก **พร้อมกับการลงรายการบัญชี** เพื่อลงรายการบัญชีใบสั่งโดยใช้กระบวนการลงรายการบัญชีเดียวกันกับที่รันเมื่อใบสั่งขายมีการระงับไว้

### <a name="credit-management-checkpoint"></a>จุดตรวจสอบของการจัดการสินเชื่อ

คุณสามารถตั้งค่าเวลาที่ใช้ในการตรวจสอบใบสั่งขายสำหรับการตัดสินค้าจากคลัง แท็บด่วน **จุดตรวจสอบการบริหารเครดิต** ระบุกระบวนการลงรายการบัญชีเอกสารที่มีการประมวลผลกฎการจัดการเครดิต นอกจากนี้ คุณยังสามารถตรวจสอบกฎเครดิตในขณะที่คุณทำการลงรายการบัญชีชั่วคราวหรือการลงรายการบัญชีใบสั่งขายทั้งหมด เลือกกล่องกาเครื่องหมายนี้เพื่อกำหนดกระบวนการลงรายการบัญชีที่ควรระงับใบสั่ง ถ้าพบการตัดสินค้าจากคลังหลังจากที่มีการประมวลผลกฎการบล็อคการจัดการเครดิต

นอกจากนี้ คุณยังสามารถกำหนดจำนวนวันปลอดหนี้ก่อนที่จะมีการตรวจสอบกฎเครดิตอีกครั้ง ถึงแม้ว่าคุณจะสามารถระบุว่ากฎการจัดการเครดิตมีการตรวจสอบเมื่อลงรายการบัญชี กฎจะไม่มีการตรวจสอบความถูกต้องของจำนวนวันปลอดหนี้ที่ระบุ ตัวอย่างเช่น คุณยืนยันใบสั่งขายในวันที่หนึ่ง และคุณระบุวันปลอดหนี้สองวันสำหรับขั้นตอนการยืนยัน ในกรณีนี้ กฎเครดิตจะไม่มีการตรวจสอบในขั้นตอนการลงรายการบัญชีถัดไป (ตัวอย่างเช่น การสร้างบันทึกการจัดส่ง หรือการออกใบแจ้งหนี้ของใบสั่ง) จนถึงวันที่สี่ ในวันที่หรือหลังจากวันที่สี่ กฎจะมีการตรวจสอบอีกครั้งเมื่อมีการลงรายการบัญชีเกิดขึ้น และจำนวนวันปลอดหนี้จะถูกเปลี่ยนเป็นค่าที่ระบุไว้สำหรับจุดตรวจสอบการลงรายการบัญชีถัดไป

ถ้าคุณไม่ได้ระบุจำนวนวันปลอดหนี้ กฎเครดิตจะมีการตรวจสอบในขั้นตอนการลงรายการบัญชีทุกรายการที่ตั้งค่าไว้เพื่อรันกฎการจัดการเครดิต ถ้าคุณนำใบสั่งขายออกใช้โดยไม่มีการลงรายการบัญชีแล้วรันขั้นตอนการประมวลผลใบสั่งเดียวกันอีกครั้ง กฎเครดิตจะถูกตรวจสอบอีกครั้ง ตัวอย่างเช่น ใบสั่งจะถูกระงับหลังจากการยืนยัน และคุณนำใบสั่งออกใช้โดยมีหรือไม่มีการลงรายการบัญชี ในกรณีนี้ ใบสั่งจะถูกระงับไว้อีกครั้ง ถ้าคุณยืนยันอีกครั้ง ใช้จำนวนวันปลอดหนี้ ถ้าใบสั่งควรเลื่อนไปยังขั้นตอนการประมวลผลถัดไปโดยไม่มีการระงับอีกครั้ง

> [!Note]
> หากจุดตรวจสอบการลงรายการบัญชีหนึ่งมีการป้อนวันปลอดหนี้ไว้ จุดตรวจสอบทั้งหมดที่ทําเครื่องหมายไว้เพื่อให้การลงรายการบัญชีต้องมีวันปลอดหนี้

- เลือกกล่องกาเครื่องหมาย **การลงรายการบัญชี** เพื่อรันกฎการจัดการเครดิตเมื่อมีการรันจุดตรวจสอบการลงรายการบัญชีที่แสดงอยู่บนบรรทัด ถ้าคุณไม่เลือกกล่องกาเครื่องหมาย กฎจะถูกตรวจสอบเพียงครั้งเดียวในระหว่างกระบวนการลงรายการบัญชีทั้งหมด
- ถ้าคุณเลือกกล่องกาเครื่องหมาย **การลงรายการบัญชี** ให้ระบุจำนวนวันปลอดหนี้ที่ควรผ่านไปก่อนที่จะมีการตรวจสอบกฎการบล็อคอีกครั้ง คุณไม่สามารถเพิ่มวันปลอดหนี้ได้ ถ้ากล่องกาเครื่องหมาย **การลงรายการบัญชี** ไม่ได้ถูกเลือก
- เลือกกล่องกาเครื่องหมาย **ใบชั่วคราว** เพื่อรันกฎการจัดการเครดิตเมื่อมีการรันจุดตรวจสอบการลงรายการบัญชีใบชั่วคราวที่แสดงอยู่บนบรรทัด ในกรณีส่วนใหญ่ ฟิลด์ **การลงรายการบัญชี** ถูกตั้งค่าเป็น **ไม่ใช่** ในกล่องโต้ตอบที่ปรากฏขึ้นเมื่อใบสั่งขายลงรายการบัญชี
- ถ้าคุณเลือกกล่องกาเครื่องหมาย **การลงรายการบัญชี** ให้ระบุจำนวนวันปลอดหนี้ที่ควรผ่านไปก่อนที่จะมีการตรวจสอบกฎการบล็อคอีกครั้ง คุณไม่สามารถเพิ่มวันปลอดหนี้ได้ ถ้ากล่องกาเครื่องหมาย **การลงรายการบัญชี** ไม่ได้ถูกเลือก

### <a name="credit-management-statistics"></a>สถิติการจัดการสินเชื่อ

สถิติการจัดการเครดิตต่าง ๆ จะรวมอยู่ในกล่องแสดงข้อมูลย่อ **สถิติการจัดการเครดิตของลูฏค้า** ในเพจ **ลูกค้า** คุณต้องระบุค่าหลายค่าที่จำเป็นต้องใช้ในการคำนวณสถิติเหล่านั้น ป้อนจำนวนเดือนที่ใช้ในการคำนวณค่าต่อไปนี้ในกล่องแสดงข้อมูลย่อ **สถิติการจัดการเครดิตของลูกค้า**:

1. ระยะเวลาการเก็บหนี้ถัวเฉลี่ย 1
2. ระยะเวลาการเก็บหนี้ถัวเฉลี่ย 2
3. ยอดดุลเฉลี่ย 1
4. ยอดดุลเฉลี่ย 2
5. เปอร์เซนต์วงเงินสินเชื่อเฉลี่ย
6. เปอร์เซนต์ปริมาณแสงโดยเฉลี่ย

### <a name="credit-limits"></a>วงเงินสินเชื่อ

- ในการจัดการเครดิต วงเงินสินเชื่อของลูกค้าจะแสดงอยู่ในสกุลเงินของลูกค้า คุณต้องกำหนดชนิดอัตราแลกเปลี่ยนสำหรับวงเงินสินเชื่อในสกุลเงินของลูกค้า ในฟิลด์ **ชนิดอัตราแลกเปลี่ยนวงเงินสินเชื่อ** ให้เลือกชนิดของอัตราแลกเปลี่ยนที่ควรใช้ในการแปลงวงเงินสินเชื่อหลักให้กับวงเงินสินเชื่อของลูกค้า
- ตั้งค่าตัวเลือก **อนุญาตให้มีการแก้ไขวงเงินสินเชื่อด้วยตนเอง** เป็น **ไม่ใช่** เพื่อไม่ให้ผู้ใช้แก้ไขวงเงินสินเชื่อในเพจ **ลูกค้า** ถ้ามีการตั้งค่าตัวเลือกเป็น **ไม่ใช่** การเปลี่ยนแปลงวงเงินสินเชื่อของลูกค้าสามารถทำได้โดยการลงรายการบัญชีธุรกรรมการปรับปรุงวงเงินสินเชื่อเท่านั้น
- ตั้งค่าตัวเลือก **ข้ามการจองสินค้าคงคลัง** เป็น **ใช่** เพื่อละเว้นการจองสินค้าคงคลังเมื่อตรวจสอบกฎการบล็อคการจัดการเครดิต ในกรณีนี้ ปริมาณจะถูกตรวจสอบและระยะเวลาผ่อนผันของจุดตรวจสอบจะถูกเปิดใช้งาน โดยไม่พิจารณาถึงปริมาณการจองสินค้าคงคลัง
- เมื่อการจัดการเครดิตเปิดใช้งาน การตั้งค่าของฟิลด์ **ข้อความเมื่อมีการใช้เกินวงเงินสินเชื่อ** เพื่อประมวลผลเฉพาะใบแจ้งหนี้ข้อความอิสระเท่านั้น แม้ว่าข้อความจะยังคงถูกเพิ่มไปยังใบสั่งขายเมื่อลูกค้าเกินวงเงินสินเชื่อแล้ว การมีอยู่ของข้อความเหล่านั้นจะไม่บล็อคการยืนยัน การพิมพ์รายการเบิกสินค้าและบันทึกการจัดส่ง หรือการลงรายการบัญชีใบแจ้งหนี้

    การจัดการสินเชื่อมีการเปิดใช้งานโดยค่าเริ่มต้น แต่คุณสามารถปิดใช้งานได้ ถ้าเปิดใช้งาน คุณจะใช้กฎการบล็อคการจัดการสินเชื่อและจุดตรวจสอบ เพื่อระบุว่าลูกค้าเกินวงเงินสินเชื่อเมื่อใด ถ้าปิดใช้งานฟิลด์นี้ ข้อความที่เพิ่มไปยังใบสั่งขายตามการตั้งค่าของฟิลด์ **ข้อความเมื่อเกินวงเงินสินเชื่อ** สามารถช่วยคุณระบุได้ เมื่อลูกค้าเกินวงเงินสินเชื่อ

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>ลำดับหมายเลขและพารามิเตอร์ลำดับหมายเลขที่ใช้ร่วมกัน

รหัสสมุดรายวันต้องใช้เพื่อประมวลผลการปรับปรุงวงเงินสินเชื่อ คุณต้องเพิ่มหมายเลขการปรับปรุงวงเงินสินเชื่อที่ควรใช้ในการสร้างรหัสสมุดรายวัน


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
