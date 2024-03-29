---
title: อัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตขึ้นใหม่
description: บทความนี้ให้คำแนะนำสำหรับการอัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตใหม่
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebc2760777b8f17dc87b06899327d502ac7a0ba7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669809"
---
# <a name="update-standard-costs-for-a-new-manufactured-item"></a>อัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตขึ้นใหม่

[!include [banner](../includes/banner.md)]

บทความนี้ให้คำแนะนำสำหรับการอัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตใหม่ 

คำแนะนำต่อไปนี้จะถือว่าคุณใช้วิธีการแบบสองเวอร์ชันเพื่ออัพเดตต้นทุนมาตรฐาน  ในวิธีนี้ การคำนวณต้นทุนในเวอร์ชันหนึ่งประกอบด้วย ต้นทุนมาตรฐานที่กำหนดไว้ตั้งแต่เริ่มแรกสำหรับช่วงเวลาแน่นอนไม่เปลี่ยนแปลง ในขณะที่เวอร์ชันที่สองประกอบด้วย การอัพเดตข้อมูลเพิ่มเติมในส่วนของวัสดุใหม่ที่ได้จากการผลิต  การอัพเดตเพิ่มเติมนี้จะถูกป้อนเป็นเรกคอร์ดต้นทุนในการคำนวณต้นทุนเวอร์ชันที่สอง และนำไปใช้คำนวณในขั้นตอนสุดท้าย  วิธีแบบสองเวอร์ชันต้องการให้คุณกำหนดเวอร์ชันการคิดต้นทุนที่สอง  นี่คือคำแนะนำสำหรับการกำหนดการคิดต้นทุนนี้:

-   กำหนดชนิดการคำนวณต้นทุนของ **ต้นทุนมาตรฐาน**
-   กำหนดรหัสสำคัญที่ระบุเนื้อหาของเวอร์ชันการคำนวณต้นทุน เช่น **2016-UPDATES**
-   ในกลุ่มฟิลด์ **อนุญาตชนิดราคา** ตรวจสอบให้แน่ใจว่า **ราคาต้นทุน** ถูกตั้งค่าเป็น **ใช่**
-   อนุญาตให้เรกคอร์ดต้นทุนถูกป้อนสำหรับไซต์ทั้งหมด (นั่นคือ ปล่อยให้ฟิลด์ **ไซต์** ว่าง) ถ้าคุณป้อนไซต์ คุณสามารถป้อนเรกคอร์ดต้นทุนสำหรับไซต์ดังกล่าวเท่านั้น
-   ใช้หลักการถอยกลับของ **ใช้งานอยู่**

เมื่อต้องการเพิ่มรายการผลิตตลอดช่วงเวลาที่แน่นอน ให้ทำตามขั้นตอนต่อไปนี้

1.  ใช้หน้า **การตั้งค่าเวอร์ชันการคิดต้นทุน** เพื่อเปิดให้มีการป้อนเรกคอร์ดต้นทุนลงในการคำนวณต้นทุนเวอร์ชันที่สองที่มีข้อมูลอัพเดตเพิ่มเติม ป้องกันการเรียกใช้ต้นทุนที่ค้างอยู่ ที่การเรียกใช้ได้รับอนุญาตหลังจากต้นทุนที่ค้างอยู่ได้ถูกกำหนดอย่างถูกต้องและเสร็จสมบูรณ์ทั้งหมดแล้ว  ต่อมาให้กำหนดนโยบายของการคำนวณต้นทุนเวอร์ชันที่สองว่าไม่มีวันที่เริ่มต้น จากนั้นป้อนวันที่เริ่มต้นเมื่อคุณป้อนเรกคอร์ดต้นทุนแต่ละเรกคอร์ด  จากนั้นป้อนวันที่เริ่มต้นเมื่อคุณป้อนเรกคอร์ดต้นทุนแต่ละเรกคอร์ด วันที่เริ่มต้นควรเป็นวันที่ก่อนที่จะมีการสั่งซื้อหรือผลิตสินค้าใหม่
2.  ใช้หน้า **ราคาสินค้า** เพื่อป้อนเรกคอร์ดต้นทุนสำหรับสินค้าที่สั่งซื้อใหม่ ให้ป้อนเวอร์ชันการคำนวณต้นทุนที่มีข้อมูลอัพเดตเพิ่มเติม สำหรับเรกคอร์ดต้นทุนแต่ละเรกคอร์ด และใช้วันที่เริ่มต้นที่มาก่อนวันที่ผลิตที่คาดไว้ สำหรับสินค้าที่ผลิตใหม่
3.  คำนวณต้นทุนของสินค้าที่ผลิตใหม่ โดยใช้หน้า **การคำนวณ** เปิดหน้า **การคำนวณ** จากหน้า **การบำรุงรักษาเวอร์ชันการคิดต้นทุน** และจากนั้น เลือกเวอร์ชันที่ประกอบด้วยการอัพเดตเพิ่มเติม ใช้เกณฑ์การเลือกเพื่อระบุสินค้าที่ผลิตใหม่ใดๆ ส่วนประกอบที่ผลิตอย่างใดอย่างหนึ่ง  ในโครงสร้างผลิตภัณฑ์แบบหลายระดับ คุณอาจต้องระบุสินค้าหลักใดๆที่ประกอบด้วยสินค้าที่ผลิตใหม่เป็นส่วนประกอบ  ป้อนวันที่เริ่มต้นสำหรับสูตรการผลิต (BOM) ที่สอดคล้องกับจุดเริ่มต้นของการผลิตสำหรับสินค้าที่ผลิตใหม่  วันที่เริ่มต้นควรอยู่ในวันที่มีผลบังคับใช้สำหรับเวอร์ชัน BOM และเวอร์ชันกระบวนการผลิตของสินค้า  **หมายเหตุ:** หากสินค้าใดมีเรกคอร์ดต้นทุนไม่ครบ สินค้านั้นอาจเป็นสินค้าใหม่ที่ผลิต การคำนวณ BOM สามารถถูกจำกัดกับสินค้าที่มีต้นทุนที่ขาดหายไป
4.  ตรวจสอบความสมบูรณ์และความถูกต้องของการคำนวณต้นทุนสำหรับสินค้าที่ผลิตใหม่  ใช้หน้า **เสร็จสมบูรณ์** เพื่อตรวจทานต้นทุนที่คำนวณได้ สำหรับเรกคอร์ดต้นทุนของสินค้าแต่ละเรกคอร์ด และรวมถึงตรวจทานข้อความเตือน Infolog ใดๆ หรือใช้หน้า **การคำนวณ** เพื่อตรวจทานต้นทุนที่คำนวณได้
5.  ใช้หน้า **การตั้งค่าเวอร์ชันการคิดต้นทุน** เพื่อเปลี่ยนแฟล็กการบล็อค เพื่ออนุญาตให้เปิดใช้งานเรกคอร์ดต้นทุนที่เปิดค้างไว้ในเวอร์ชันการคำนวณต้นทุนที่สอง
6.  ใช้หน้า **เรียกใช้งานราคา** (ซึ่งคุณสามารถเปิดได้จากหน้า **การรักษาเวอร์ชันการคิดต้นทุน** ) เพื่อเปิดใช้งานเรกคอร์ดต้นทุนสินค้าที่ค้างอยู่ทั้งหมดภายในเวอร์ชันการคำนวณต้นทุนที่สอง คุณยังสามารถเปิดใช้งานเรกคอร์ดต้นทุนสินค้าที่ค้างอยู่สำหรับสินค้าแต่ละรายการ โดยการคลิกปุ่ม **เรียกใช้งาน** ในหน้า **ราคาสินค้า** ได้
7.  ใช้หน้า **การตั้งค่าเวอร์ชันการคิดต้นทุน** เพื่อเปลี่ยนแฟล็กการบล็อคในเวอร์ชันการคำนวณต้นทุนสอง เพื่อป้องกันการบำรุงรักษาข้อมูลเพิ่มเติม นโยบายการบล็อคป้องกันรายการของต้นทุนใหม่ที่ค้างอยู่และการเรียกใช้ต้นทุนที่ค้างอยู่






[!INCLUDE[footer-include](../../includes/footer-banner.md)]