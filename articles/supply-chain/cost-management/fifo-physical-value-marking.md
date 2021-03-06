---
title: FIFO ที่มีมูลค่าจริงและมีการทำเครื่องหมาย
description: เข้าก่อนออกก่อน (FIFO) เป็นแบบจำลองสินค้าคงคลังที่สินค้าที่ได้รับเข้ามาแรกสุดจะถูกนำออกใช้ก่อน  ในทางการเงิน ปัญหาที่อัพเดตจากสินค้าคงคลังจะถูกจับคู่กับการรับสินค้าเข้าในคลังสินค้ารายการแรกที่ได้รับการอัพเดต ตามวันที่ทางการเงินของรายการความเคลื่อนไหวของสินค้าคงคลัง
author: AndersGirke
manager: tfehr
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b6b5e7b654b5732290489c0dbcb13d1cc441e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002059"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO ที่มีมูลค่าจริงและมีการทำเครื่องหมาย

[!include [banner](../includes/banner.md)]

เข้าก่อนออกก่อน (FIFO) เป็นแบบจำลองสินค้าคงคลังที่สินค้าที่ได้รับเข้ามาแรกสุดจะถูกนำออกใช้ก่อน  ในทางการเงิน ปัญหาที่อัพเดตจากสินค้าคงคลังจะถูกจับคู่กับการรับสินค้าเข้าในคลังสินค้ารายการแรกที่ได้รับการอัพเดต ตามวันที่ทางการเงินของรายการความเคลื่อนไหวของสินค้าคงคลัง 

เมื่อคุณใช้ FIFO คุณไม่จำเป็นต้องใช้กฎ FIFO  คุณสามารถทำเครื่องหมายธุรกรรมสินค้าคงคลังแทน เพื่อให้ใบรับสินค้าเฉพาะถูกจับคู่กับการนำสินค้าออกใช้ที่ระบุ  ขอแนะนำให้ปิดบัญชีสินค้าคงคลังประจำงวด เมื่อคุณใช้แบบจำลองสินค้าคงคลัง FIFO ตัวอย่างต่อไปนี้จะแสดงผลกระทบของการใช้ FIFO ในการตั้งค่าคอนฟิก 3 ชุด:

-   FIFO ที่ไม่มีตัวเลือก **รวมมูลค่าทางกายภาพ**
-   FIFO ที่มีตัวเลือก **รวมมูลค่าทางกายภาพ**
-   FIFO ที่มีการทำเครื่องหมาย

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO ที่ไม่มีตัวเลือกรวมค่าทางกายภาพ
ในตัวอย่างนี้ ไม่มีการทำเครื่องหมายกลุ่มรูปแบบจำลองสินค้าเพื่อรวมมูลค่าทางกายภาพ ภาพประกอบต่อไปนี้แสดงธุรกรรมเหล่านี้:

-   1a. การรับสินค้าจริงของสินค้าคงคลังสำหรับปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   1b. การรับสินค้าทางการเงินของสินค้าคงคลังสำหรับปริมาณเท่ากับ 1 หน่วย ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   2a. การรับสินค้าจริงของสินค้าคงคลังสำหรับปริมาณเท่ากับ 2 หน่วย ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   2b. การรับสินค้าทางการเงินของสินค้าคงคลังสำหรับริมาณเท่ากับ 2 หน่วย ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   3a. การรับสินค้าจริงของสินค้าคงคลังสำหรับปริมาณเท่ากับ 1 หน่วย ที่ต้นทุนหน่วยละ 25.00 เหรียญสหรัฐ
-   4a. การรับสินค้าจริงของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 30.00 เหรียญสหรัฐ
-   4b. การรับสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 30.00 เหรียญสหรัฐ
-   5a. ธุรกรรมการรับทางกายภาพของสินค้าคงคลังสำหรับปริมาณ 1 หน่วยที่ต้นทุน USD 20.00 (ค่าเฉลี่ยสืบเนื่องของธุรกรรมที่มีการอัพเดตทางการเงิน)
-   5b. ธุรกรรมการรับทางการเงินของสินค้าคงคลังสำหรับปริมาณ 1 หน่วยที่ต้นทุน USD 15.00 (ค่าเฉลี่ยสืบเนื่องของธุรกรรมที่มีการอัพเดตทางการเงิน)
-   6. ดำเนินการปิดสินค้าคงคลัง  โดยยึดตามวิธี FIFO การตัดสินค้าที่มีการอัพเดตทางการเงินรายการแรกจะถูกจับคู่กับการรับสินค้าที่มีการอัพเดตรายการแรก  จะมีการดำเนินการปรับปรุง –5.00 เหรียญสหรัฐในธุรกรรมการตัดสินค้า

ราคาต้นทุนเฉลี่ยสืบเนื่องใหม่จะสอดคล้องกับค่าเฉลี่ยของธุรกรรมที่มีการอัพเดตทางการเงิน ภาพประกอบต่อไปนี้แสดงผลของแบบจำลองสินค้าคงคลังวันที่ FIFO เมื่อตัวเลือก **รวมค่าทางกายภาพ** ไม่ได้ถูกใช้ 

![FIFO โดยไม่รวมค่าทางกายภาพ](./media/fifowithoutincludephysicalvalue.gif) 

**สัญลักษณ์แผนภาพ**

- รายการความเคลื่อนไหวของสินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้ง
- การรับสินค้าเข้าสู่สินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้งเหนือเส้นเวลา
- การตัดสินค้าออกจากสินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้งใต้เส้นเวลา
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่อยู่เหนือ (หรือใต้) ลูกศรแนวตั้งต่างๆ จะแสดงในรูปแบบ Quantity@Unitprice
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่อยู่ในวงเล็บจะแสดงว่ามีการลงรายการบัญชีรายการความเคลื่อนไหวของสินค้าคงคลังตามจริงในสินค้าคงคลังแล้ว
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่ไม่อยู่ในวงเล็บจะแสดงว่ามีการลงรายการบัญชีรายการความเคลื่อนไหวของสินค้าคงคลังทางการเงินในสินค้าคงคลังแล้ว
- รายการธุรกรรมการรับสินค้าใหม่และการตัดสินค้าออกจากคลังแต่ละรายการจะถูกกำหนดด้วยป้ายชื่อใหม่
- แต่ละลูกศรในแนวตั้งจะมีป้ายชื่อกำกับพร้อมตัวบ่งชี้ลำดับ เช่น *1a* ตัวระบุบ่งชี้ถึงลำดับของการลงรายการบัญชีธุรกรรมของสินค้าคงคลังในเส้นเวลา
- การปิดสินค้าคงคลังจะแสดงโดยใช้เส้นประสีแดงแนวตั้งและป้ายชื่อ *การปิดสินค้าคงคลัง*
- การจับคู่ที่ดำเนินการโดยการปิดสินค้าคงคลังจะถูกแสดงโดยใช้ลูกศรสีแดงเป็นเส้นประ ในลักษณะทแยงมุมจากการรับสินค้าไปยังการตัดสินค้าออกจากคลัง

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO ที่มีตัวเลือกรวมค่าทางกายภาพ
หากมีการเลือกกล่อง **รวมมูลค่าทางกายภาพ** สำหรับสินค้าในหน้า **กลุ่มแบบจำลองสินค้า** ระบบจะใช้ธุรกรรมการรับสินค้าทั้งทางกายภาพและทางการเงิน เพื่อคำนวณราคาต้นทุนถัวเฉลี่ย และหากสามารถทำได้ ระบบจะทำการปรับค่าของธุรกรรมการออกที่มีการอัพเดตทางกายภาพด้วย  เมื่อยกเลิกการเลือกกล่อง **รวมมูลค่าทางกายภาพ** การปิดสินค้าคงคลังด้วยแบบจำลองสินค้าคงคลัง FIFO จะจับคู่เฉพาะกับธุรกรรมที่มีการอัพเดตทางการเงินเท่านั้น ภาพประกอบต่อไปนี้แสดงธุรกรรมเหล่านี้:

-   1a. การรับสินค้าจริงของสินค้าคงคลังสำหรับปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   1b. การรับสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   2a. การรับสินค้าจริงของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 20.00 เหรียญสหรัฐ
-   2b. การรับสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 20.00 เหรียญสหรัฐ
-   3a. การรับสินค้าจริงของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 25.00 เหรียญสหรัฐ
-   4a. การรับสินค้าจริงของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 30.00 เหรียญสหรัฐ
-   4b. การรับสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 30.00 เหรียญสหรัฐ
-   5a. การตัดสินค้าจากคลังของสินค้าคงคลังทางกายภาพสำหรับปริมาณของสินค้า 1 รายการ ที่ราคาต้นทุนหน่วยละ 21.25 เหรียญสหรัฐ (ค่าเฉลี่ยสืบเนื่องของธุรกรรมที่อัพเดตทางการเงินและทางกายภาพ)
-   5b. ธุรกรรมการออกทางการเงินของสินค้าคงคลังสำหรับปริมาณ 1 หน่วยที่ต้นทุน USD 21.25 (ค่าเฉลี่ยสืบเนื่องของธุรกรรมที่มีการอัพเดตทางกายภาพและทางการเงิน)
-   6a. การตัดสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ราคาต้นทุนหน่วยละ 21.25 เหรียญสหรัฐ
-   7. ดำเนินการปิดสินค้าคงคลัง  ตามวิธี FIFO ธุรกรรมการตัดสินค้าจากคลังทางการเงินรายการแรก จะถูกปรับปรุงหรือจับคู่กับการรับสินค้ารายการแรกที่มีการอัพเดต ไม่ว่าจะเป็นทางการเงินหรือทางกายภาพ

ธุรกรรม 5b จะถูกจับคู่กับธุรกรรมที่รับสินค้า 1b จะมีการดำเนินการปรับปรุง –11.25 เหรียญสหรัฐ ในธุรกรรมการตัดสินค้านี้ ราคาต้นทุนค่าเฉลี่ยของการดำเนินการใหม่จะแสดงค่าเฉลี่ยของธุรกรรมที่อัพเดตทางการเงินและที่อัพเดตจริงที่ 27.50 เหรียญสหรัฐ ภาพประกอบต่อไปนี้แสดงผลกระทบของแบบจำลองสินค้าคงคลัง FIFO บนชุดของธุรกรรมเมื่อตัวเลือก **รวมมูลค่าทางกายภาพ** ได้ถูกใช้ 

![FIFO โดยรวมค่าทางกายภาพ](./media/fifowithincludephysicalvalue.gif) 

**สัญลักษณ์แผนภาพ**

- รายการความเคลื่อนไหวของสินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้ง
- การรับสินค้าเข้าสู่สินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้งเหนือเส้นเวลา
- การตัดสินค้าออกจากสินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้งใต้เส้นเวลา
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่อยู่เหนือ (หรือใต้) ลูกศรแนวตั้งต่างๆ จะแสดงในรูปแบบ Quantity@Unitprice
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่อยู่ในวงเล็บจะแสดงว่ามีการลงรายการบัญชีรายการความเคลื่อนไหวของสินค้าคงคลังตามจริงในสินค้าคงคลังแล้ว
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่ไม่อยู่ในวงเล็บจะแสดงว่ามีการลงรายการบัญชีรายการความเคลื่อนไหวของสินค้าคงคลังทางการเงินในสินค้าคงคลังแล้ว
- รายการธุรกรรมการรับสินค้าใหม่และการตัดสินค้าออกจากคลังแต่ละรายการจะถูกกำหนดด้วยป้ายชื่อใหม่
- แต่ละลูกศรในแนวตั้งจะมีป้ายชื่อกำกับพร้อมตัวบ่งชี้ลำดับ เช่น *1a* ตัวระบุบ่งชี้ถึงลำดับของการลงรายการบัญชีธุรกรรมของสินค้าคงคลังในเส้นเวลา
- การปิดสินค้าคงคลังจะแสดงโดยใช้เส้นประสีแดงแนวตั้งและป้ายชื่อ *การปิดสินค้าคงคลัง*
- การจับคู่ที่ดำเนินการโดยการปิดสินค้าคงคลังจะถูกแสดงโดยใช้ลูกศรสีแดงเป็นเส้นประ ในลักษณะทแยงมุมจากการรับสินค้าไปยังการตัดสินค้าออกจากคลัง

## <a name="fifo-with-marking"></a>FIFO ที่มีการทำเครื่องหมาย
การทำเครื่องหมายเป็นกระบวนการที่ช่วยให้คุณสามารถลิงค์ หรือทำเครื่องหมายธุรกรรมการตัดสินค้าจากคลังไปยังธุรกรรมการรับสินค้า การทำเครื่องหมายอาจเกิดขึ้นก่อนหน้าหรือหลังจากที่ลงรายบัญชีธุรกรรมก็ได้ คุณสามารถใช้การทำเครื่องหมายเมื่อคุณต้องการตรวจสอบต้นทุนที่แน่นอนของสินค้าคงคลัง เมื่อมีการลงรายบัญชีธุรกรรมหรือเมื่อมีการดำเนินการปิดสินค้าคงคลัง ตัวอย่างเช่น ฝ่ายบริการลูกค้าของคุณยอมรับการสั่งที่เร่งด่วนจากลูกค้าคนสำคัญ เนื่องจากการสั่งนี้เป็นการสั่งที่เร่งด่วน คุณจะต้องชำระค่าสินค้านี้เพิ่มเติมสำหรับสินค้านี้เพื่อตอบสนองคำขอของลูกค้า คุณต้องทำให้แน่ใจว่าต้นทุนของสินค้าในสินค้าคงคลังนี้สะท้อนให้เห็นในกำไรเบื้องต้น หรือต้นทุนขาย (COGS) สำหรับใบแจ้งหนี้ใบสั่งขายนี้ เมื่อลงรายการบัญชีใบสั่งซื้อ สินค้าคงคลังได้รับ โดยมีต้นทุน 120.00 เหรียญสหรัฐ หากเอกสารใบสั่งขายนี้มีการทำเครื่องหมายไปยังใบสั่งซื้อก่อนมีการลงรายการบัญชีบันทึกการจัดส่งหรือใบแจ้งหนี้ COGS จะเป็น USD 120.00 แทนที่จะเป็นต้นทุนค่าเฉลี่ยเคลื่อนที่ปัจจุบันของสินค้า ถ้าใบสั่งขายที่บันทึกการจัดส่งหรือใบแจ้งหนี้ถูกลงรายการบัญชีก่อนการทำเครื่องหมาย COGS จะถูกลงรายการบัญชีราคาต้นทุนเฉลี่ยสืบเนื่อง ก่อนดำเนินการปิดสินค้าคงคลัง รายการความเคลื่อนไหวสองรายการดังกล่าวจะถูกทำเครื่องหมายไว้ เมื่อธุรกรรมการรับสินค้าตรงกับธุรกรรมการออกใช้ วิธีการประเมินค่าที่ถูกกำหนดในกลุ่มแบบจำลองสินค้าของสินค้าจะถูกละเว้น และระบบจะจับคู่กับธุรกรรมเหล่านี้ คุณสามารถทำเครื่องหมายธุรกรรมการตัดสินค้าจากคลังไปยังการรับสินค้า ก่อนที่จะลงรายบัญชีธุรกรรม  คุณสามารถทำได้จากรายการใบสั่งขายในหน้า **รายละเอียดของใบสั่งขาย** คุณสามารถดูธุรกรรมการรับสินค้าที่เปิดค้างไว้ในหน้า **การทำเครื่องหมาย** ได้ คุณสามารถทำเครื่องหมายธุรกรรมการตัดสินค้าจากคลังเป็นการรับสินค้าหลังที่จะลงรายบัญชีธุรกรรมได้ด้วย คุณสามารถจับคู่หรือทำเครื่องหมายธุรกรรมการตัดสินค้าจากคลัง สำหรับธุรกรรมการรับสินค้าที่เปิดค้างไว้สำหรับสินค้าในสินค้าคงคลังจากสมุดรายวันการปรับปรุงสินค้าคงคลังที่ลงรายการบัญชีไว้ ภาพประกอบต่อไปนี้แสดงธุรกรรมเหล่านี้:

-   1a. การรับสินค้าจริงของสินค้าคงคลังสำหรับปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   1b. การรับสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 10.00 เหรียญสหรัฐ
-   2a. การรับสินค้าจริงของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 20.00 เหรียญสหรัฐ
-   2b. การรับสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 20.00 เหรียญสหรัฐ
-   3a. การรับสินค้าจริงของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 25.00 เหรียญสหรัฐ
-   4a. การรับสินค้าจริงของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 30.00 เหรียญสหรัฐ
-   4b. การรับสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ต้นทุนหน่วยละ 30.00 เหรียญสหรัฐ
-   5a. การตัดสินค้าจากคลังของสินค้าคงคลังทางกายภาพสำหรับปริมาณของสินค้า 1 รายการ ที่ราคาต้นทุนหน่วยละ 21.25 เหรียญสหรัฐ (ค่าเฉลี่ยสืบเนื่องของธุรกรรมที่อัพเดตทางการเงินและทางกายภาพ)
-   5b. การตัดสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 หน่วย มีการทำเครื่องหมายไปยังการรับสินค้าของสินค้าคงคลัง 2b ก่อนการลงรายการบัญชีธุรกรรม ธุรกรรมนี้จะมีการลงรายการบัญชีที่ราคาต้นทุนที่หน่วยละ 20.00 เหรียญสหรัฐ
-   6a. การตัดสินค้าทางการเงินของสินค้าคงคลังในปริมาณเท่ากับ 1 ที่ราคาต้นทุนหน่วยละ 21.25 เหรียญสหรัฐ
-   7. ดำเนินการปิดสินค้าคงคลัง  เนื่องจากธุรกรรม FIFO ที่มีการอัพเดตทางการเงินถูกทำเครื่องหมายไปยังการรับสินค้าที่มีอยู่ รายการธุรกรรมเหล่านี้จะมีการหักลบซึ่งกันและกันและไม่มีการปรับปรุงใดๆ

ราคาต้นทุนค่าเฉลี่ยของการดำเนินการใหม่จะแสดงค่าเฉลี่ยของธุรกรรมที่อัพเดตทางการเงินและที่อัพเดตจริงที่ 27.50 เหรียญสหรัฐ แผนภาพต่อไปนี้จะแสดงผลกระทบของแบบจำลองสินค้าคงคลัง FIFO บนชุดของธุรกรรมเมื่อการทำเครื่องหมายระหว่างธุรกรรมการออกและธุรกรรมการรับถูกใช้อยู่ 

![FIFO กับการตลาด](./media/fifowithmarking.gif) 

**สัญลักษณ์แผนภาพ**

- รายการความเคลื่อนไหวของสินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้ง
- การรับสินค้าเข้าสู่สินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้งเหนือเส้นเวลา
- การตัดสินค้าออกจากสินค้าคงคลังจะแสดงโดยใช้ลูกศรแนวตั้งใต้เส้นเวลา
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่อยู่เหนือ (หรือใต้) ลูกศรแนวตั้งต่างๆ จะแสดงในรูปแบบ Quantity@Unitprice
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่อยู่ในวงเล็บจะแสดงว่ามีการลงรายการบัญชีรายการความเคลื่อนไหวของสินค้าคงคลังตามจริงในสินค้าคงคลังแล้ว
- ค่าของรายการความเคลื่อนไหวของสินค้าคงคลังที่ไม่อยู่ในวงเล็บจะแสดงว่ามีการลงรายการบัญชีรายการความเคลื่อนไหวของสินค้าคงคลังทางการเงินในสินค้าคงคลังแล้ว
- รายการธุรกรรมการรับสินค้าใหม่และการตัดสินค้าออกจากคลังแต่ละรายการจะถูกกำหนดด้วยป้ายชื่อใหม่
- แต่ละลูกศรในแนวตั้งจะมีป้ายชื่อกำกับพร้อมตัวบ่งชี้ลำดับ เช่น *1a* ตัวระบุบ่งชี้ถึงลำดับของการลงรายการบัญชีธุรกรรมของสินค้าคงคลังในเส้นเวลา
- การปิดสินค้าคงคลังจะแสดงโดยใช้เส้นประสีแดงแนวตั้งและป้ายชื่อ *การปิดสินค้าคงคลัง*
- การจับคู่ที่ดำเนินการโดยการปิดสินค้าคงคลังจะถูกแสดงโดยใช้ลูกศรสีแดงเป็นเส้นประ ในลักษณะทแยงมุมจากการรับสินค้าไปยังการตัดสินค้าออกจากคลัง




