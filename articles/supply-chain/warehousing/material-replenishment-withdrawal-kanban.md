---
title: การเติมสินค้าที่มีคัมบังการเบิกถอน
description: บทความนี้อธิบายวิธีใช้คัมบังการเบิกถอนสำหรับการเติมสินค้าวัสดุสำหรับกิจกรรมการผลิต
author: perlynne
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 517b2eeb3b218fe0820ffa4e1d19b20841837b92
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863721"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>การเติมสินค้าที่มีคัมบังการเบิกถอน

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีใช้คัมบังการเบิกถอนสำหรับการเติมสินค้าวัสดุสำหรับกิจกรรมการผลิต

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>ลำดับงานสำหรับการเติมสินค้าวัสดุที่ใช้คัมบังการเบิกถอน

คัมบังการเบิกถอนสามารถถูกใช้เพื่อย้ายคัมบังสินค้าเดี่ยวระหว่างคลังสินค้าและสถานที่ผลิตที่ซึ่งมีการใช้วัสดุ คัมบังการเบิกถอนสนับสนุนโซลูชันที่ทำงานแบบดึงสำหรับการเติมสินค้าวัสดุ ที่ต้องใช้สัญญาณดึงเพื่อทริกเกอร์การจัดหาวัสดุสำหรับความต้องการเฉพาะ 

สถานการณ์จำลองต่อไปนี้แสดงระบบการเติมสินค้าที่ทำงานแบบดึง ซึ่งสัญญาณการดึงทริกเกอร์การสร้างคัมบังเพื่อเติมสินค้าวัสดุสำหรับกระบวนการผลิต 

[![สัญญาณแบบดึงทริกเกอร์การสร้างคัมบังเพื่อเติมสินค้าวัสดุสำหรับกระบวนการผลิต](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  คัมบังการเบิกถอน
2.  สถานที่เก็บ "ต้นทาง" และสถานส่งสินค้าคัมบังสำหรับงานคลังสินค้า
3.  สถานที่ "ปลายทาง" คัมบังและสถานตั้งอินพุทการผลิต
4.  กระบวนการผลิต
5.  งานของคลังสินค้าสำหรับการเบิกสินค้าคัมบัง
6.  ที่ตั้งคลังสินค้าสำหรับวัตถุดิบ
7.  คลังสินค้าวัสดุ
8.  คลังสินค้าสำหรับการผลิต

ในสถานการณ์นี้ กระบวนการผลิต (4) ใช้วัสดุจากสถานที่ตั้งอินพุทการผลิต (3) ในคลังสินค้าสำหรับการผลิต (8) เมื่อมีการใช้หน่วยจัดการวัสดุ (คัมบัง) จะถูกลงทะเบียนเป็นว่างเปล่า มีการสร้างสัญญาณการเติมสินค้าสำหรับจุดเริ่มต้นของสินค้า และมีการสร้างคัมบังใหม่ (1) ในกรณีนี้ จุดเริ่มต้นของสินค้าประกอบด้วยสถานที่ในคลังสินค้าวัสดุ (7) วัสดุสำหรับคัมบังถูกเบิก และย้ายไปยังตำแหน่ง (2) ในคลังสินค้าเดียวกัน เมื่อมีการเบิกวัสดุ จะพร้อมที่จะถูกโอนย้ายจากสถานที่ตั้ง 2 ไปยังสถานที่ตั้งอินพุทการผลิต (3) ในคลังสินค้าสำหรับการผลิต (8)

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>ตั้งค่าคอนฟิกงานคลังสินค้าสำหรับการเบิกสินค้าคัมบังสำหรับคัมบังการเบิกถอน

เมื่อต้องการเปิดใช้งานการเบิกวัตถุดิบสำหรับคัมบังการเบิกถอน ตั้งค่าคอนฟิกเท็มเพลตเวฟ เท็มเพลตงาน และคำสั่งสถานที่สำหรับชนิดใบสั่งงาน **การเบิกคัมบัง** ชนิดใบสั่งงานนี้ไม่เพียงแค่สนับสนุนกระบวนการเบิกสินค้าสำหรับคัมบังการเบิกถอน แต่ยังสนับสนุนกระบวนการเบิกสินค้าสำหรับคัมบังการผลิต อย่างไรก็ตาม คุณสามารถตั้งค่าตอนฟิกกระบวนการเบิกสินค้าแยกต่างหากสำหรับคัมบังแต่ละชนิด โดยแยกเท็มเพลตเวฟ เท็มเพลตงาน และคำสั่งสถานที่ เพื่อแยกเท็มเพลตเวฟ เท็มเพลตงาน และคำสั่งสถานที่ ตั้งค่าเงื่อนไขบนชนิดกิจกรรม (**กระบวนการ** หรือ **การโอนย้าย**) ในการสอบถามสำหรับเอนทิตีเหล่านั้น

## <a name="configure-the-withdrawal-kanban"></a>ตั้งค่าคอนฟิกคัมบังการเบิกถอน

กิจกรรมการโอนย้ายที่ใช้สำหรับการเบิกถอนคัมบัง ถูกตั้งค่าคอนฟิกให้เป็นส่วนหนึ่งของแผนกิจกรรมที่เปิดใช้งานในขั้นตอนการผลิตแบบ Lean ในฐานะที่เป็นส่วนหนึ่งของการตั้งค่าคอนฟิกของกิจกรรมการโอนย้าย คุณระบุสถานที่ "ต้นทาง" และ "ปลายทาง" สำหรับการโอนย้าย หลังจากที่คุณตั้งค่าคอนฟิกกิจกรรมการโอนย้าย คุณสามารถกำหนดให้กฎคัมบังชนิด **เบิกถอน** ได้ กฎคัมบังตั้งค่านโยบายและตั้งค่าคอนฟิกสำหรับคัมบังการเบิกถอน ปริมาณของคัมบังกำหนดจำนวนหน่วยของหน่วยจัดการวัสดุที่คัมบังมีในระหว่างกระบวนการโอนย้าย ปริมาณตามระบบคัมบังคงที่ ถูกใช้เมื่อมีการเลือกกลยุทธ์การเติมสินค้าถาวร ปริมาณนี้กำหนดจำนวนคัมบังที่ต้องใช้เพื่อป้องกันสินค้าคงคลัง หรือสร้างสินค้าคงคลัง จากขาดแหล่งที่มาของความต้องการ ปริมาณคงที่สามารถถูกคำนวณได้ตามความต้องการจริง ความต้องการในอดีต และระดับการบริการ สถานการณ์สมมติสองแบบต่อไปนี้ อธิบายวิธีที่คุณสามารถจัดการการเติมสินค้าวัสดุที่ใช้คัมบังการเบิกถอน

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>สถานการณ์จำลองที่ 1: เติมสินค้าในสถานที่ตั้งอินพุตการผลิต โดยใช้คัมบังการเบิกถอนถาวร

กระบวนการผลิตใช้วัตถุดิยที่ซื้อจากสถานที่ตั้งอินพุทการผลิต ที่อยู่ในคลังสินค้าสำหรับการผลิต เมื่อได้รับวัตถุดิบได้รับจากผู้จัดจำหน่าย จะถูกจัดเก็บอยู่ในสถานที่เก็บในคลังสินค้าวัสดุ เนื่องจากความต้องการสำหรับวัสดุถือว่าคงที่ตลอดรอบระยะเวลา จึงมีการตั้งค่าเพื่อจัดหาวัสดุการผลิตในขั้นตอนคัมบังแบบปริมาณคงที่ เมื่อมีการใช้คัมบังที่สถานที่ตั้งอินพุทการผลิต สัญญาณที่ว่างเปล่าจะถูกลงทะเบียน และมีการเพิ่มคัมบังใหม่ชนิดเดิมลงในขั้นตอน 

สามารถตั้งค่าคอนฟิกสัญญาณว่างเปล่าได้เพื่อให้เกิดโดยอัตโนมัติ เมื่อคัมบังเสร็จสมบูรณ์ อีกทางหนึ่งคือ สัญญาณว่างเปล่าสามารถถูกตั้งค่าเป็นการโต้ตอบที่กำหนดเองที่ได้รับจากบอร์ดการโอนย้ายคัมบัง หรือจากเมนูบนอุปกรณ์มือถือ บอร์ดการโอนย้ายคัมบังเป็นพื้นที่ทำงานที่ใช้ในการจัดการกิจกรรมทั้งหมดในวงจรชีวิตของคัมบัง 

เมื่อมีการสร้างคัมบัง รายการเวฟสำหรับวัตถุดิบจะถูกเพิ่มไปยังเวฟคัมบังสำหรับคลังสินค้าวัสดุ ในส่วนรายการเบิกสินค้าของบอร์ดการโอนย้ายคัมบัง สามารถติดตามสถานะของวัสดุและกระบวนการคลังสินค้าที่เกี่ยวข้องได้จากการสร้างเวฟไปยังการสร้างงาน จนกว่าปริมาณวัสดุจะคงเหลือในสถานที่ตั้ง "การโอนย้ายจาก" และพร้อมที่จะถูกโอนย้ายไปยังสถานที่ตั้งอินพุทการผลิต คัมบังสามารถให้เสร็จสมบูรณ์ได้ จากบอร์ดการโอนย้ายคัมบัง หรือจากเมนูบนอุปกรณ์มือถือ 

ในสถานการณ์จำลองนี้ มีการประมวลผลงานการเบิกสินค้าในคลังสินค้าวัสดุ เช่นเดียวกับกิจกรรมหนึ่ง มีการประมวลผลกิจกรรมการโอนย้ายระหว่างคลังสินค้าวัสดุและคลังสินค้าการผลิต เช่นเดียวกับกิจกรรมที่แยกต่างหาก วิธีการนี้อาจเป็นประโยชน์ เช่น ถ้ามีระยะทางจริงที่ไกลระหว่างคลังสินค้าสองแห่ง ในกรณีนี้ กิจกรรมการโอนย้ายคัมบังสามารถแสดงโหลดรถบรรทุกได้ 

ถ้าระยะห่างระหว่างสถานที่ตั้งคลังสินค้าและสถานที่ตั้งอินพุทการผลิตน้อย อาจจะมีประสิทธิภาพมากขึ้นในการรวมกิจกรรมการโอนย้ายในกระบวนการเบิกสินค้า จากนั้น หลังจากที่มีการเบิกวัสดุ จะสามารถนำไปที่ตั้งอินพุทการผลิตโดยตรง เพื่อสนับสนุนกระบวนการนี้ คุณตั้งค่าคอนฟิกกิจกรรมการโอนย้ายเพื่อให้เสร็จสมบูรณ์โดยอัตโนมัติ เมื่อมีการดำเนินงานเบิกสินค้าของคัมบังการเบิกถอน

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>สถานการณ์จำลองที่ 2: ดำเนินกิจกรรมการโอนย้ายให้เสร็จสมบูรณ์โดยอัตโนมัติ เมื่อมีการประมวลผลการเบิกคัมบัง

ในสถานการณ์จำลองต่อไปนี้ กิจกรรมการโอนย้ายของคัมบังการเบิกถอนจะถูกตั้งค่าคอนฟิกให้โอนย้ายระหว่างสองสถานที่ตั้งในคลังสินค้าเดียวกัน กิจกรรมการโอนย้ายของคัมบังการเบิกถอนถูกตั้งค่า เพื่อให้เสร็จสมบูรณ์โดยอัตโนมัติ 

[![กิจกรรมการโอนย้ายเสร็จสมบูรณ์โดยอัตโนมัติ เมื่อมีการประมวลผลงานการเบิกคัมบัง](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  คลังสินค้าที่ใช้ร่วมกันสำหรับวัตถุดิบและการผลิต
2.  สถานที่ตั้งคลังสินค้าสำหรับวัตถุดิบ
3.  สถานที่เก็บ "ต้นทาง" และสถานส่งสินค้าคัมบังสำหรับงานคลังสินค้า
4.  คัมบังการเบิกถอน
5.  ที่ตั้งอินพุทการผลิต
6.  กระบวนการผลิต

หลังจากมีการใช้คัมบังที่สถานที่ตั้งอินพุทการผลิต คัมบังจะถูกรายงานเป็นว่างเปล่า และมีการเพิ่มคัมบังใหม่ลงในขั้นตอน เมื่อมีการสร้างคัมบัง รายการเวฟถูกเพิ่มไปยังเวฟคัมบัง เมื่อมีการประมวลผลเวฟคัมบัง มีการสร้างงานของคลังสินค้าสำหรับการเบิกสินค้าคัมบัง ผู้ปฏิบัติงานคลังสินค้าประมวลผลงานสำหรับการเบิกสินค้าคัมบัง และถูกนำทางโดยงานเพื่อเบิกวัสดุสำหรับคัมบังในสถานที่ตั้งคลังสินค้า เนื่องจากผู้ปฏิบัติงานคลังสินค้านี้ยืนยันการเบิกของ คัมบังจะเสร็จสมบูรณ์โดยอัตโนมัติ และมีการแนะนำผู้ปฏิบัติงานคลังสินค้าให้วางวัสดุในสถานที่ตั้งอินพุทการผลิต



[!INCLUDE[footer-include](../../includes/footer-banner.md)]