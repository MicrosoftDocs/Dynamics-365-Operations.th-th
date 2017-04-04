---
title: "อัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตขึ้นใหม่"
description: "บทความนี้ให้คำแนะนำสำหรับการอัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตใหม่"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 84b9f91f49e988244b98aeb7a6a6344548d6a8c0
ms.lasthandoff: 03/31/2017


---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>อัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตขึ้นใหม่

บทความนี้ให้คำแนะนำสำหรับการอัพเดตต้นทุนมาตรฐานสำหรับสินค้าที่ผลิตใหม่ 

คำแนะนำต่อไปนี้จะถือว่าคุณใช้วิธีการแบบสองเวอร์ชันเพื่ออัพเดตต้นทุนมาตรฐาน  ในวิธีนี้ การคำนวณต้นทุนในเวอร์ชันหนึ่งประกอบด้วย ต้นทุนมาตรฐานที่กำหนดไว้ตั้งแต่เริ่มแรกสำหรับช่วงเวลาแน่นอนไม่เปลี่ยนแปลง ในขณะที่เวอร์ชันที่สองประกอบด้วย การอัพเดตข้อมูลเพิ่มเติมในส่วนของวัสดุใหม่ที่ได้จากการผลิต  การอัพเดตเพิ่มเติมนี้จะถูกป้อนเป็นเรกคอร์ดต้นทุนในการคำนวณต้นทุนเวอร์ชันที่สอง และนำไปใช้คำนวณในขั้นตอนสุดท้าย  วิธีแบบสองเวอร์ชันต้องการให้คุณกำหนดเวอร์ชันการคิดต้นทุนที่สอง  นี่คือคำแนะนำสำหรับการกำหนดการคิดต้นทุนนี้:

-   กำหนดชนิดการคำนวณต้นทุนของ **ต้นทุนมาตรฐาน**
-   กำหนดรหัสสำคัญที่ระบุเนื้อหาของเวอร์ชันการคำนวณต้นทุน เช่น **2016-UPDATES**
-   ในกลุ่มฟิลด์ **อนุญาตชนิดราคา** ตรวจสอบให้แน่ใจว่า **ราคาต้นทุน** ถูกตั้งค่าเป็น **ใช่**
-   Allow cost records to be entered for all sites (that is, leave the **Site** field blank). ถ้าคุณป้อนไซต์ คุณสามารถป้อนเรกคอร์ดต้นทุนสำหรับไซต์ดังกล่าวเท่านั้น
-   ใช้หลักการถอยกลับของ **ใช้งานอยู่**

เมื่อต้องการเพิ่มรายการผลิตตลอดช่วงเวลาที่แน่นอน ให้ทำตามขั้นตอนต่อไปนี้

1.  Use the **Costing version setup** page to enable cost records to be entered into the second costing version that contains the incremental updates. ป้องกันการเรียกใช้ต้นทุนที่ค้างอยู่ ที่การเรียกใช้ได้รับอนุญาตหลังจากต้นทุนที่ค้างอยู่ได้ถูกกำหนดอย่างถูกต้องและเสร็จสมบูรณ์ทั้งหมดแล้ว  ต่อมาให้กำหนดนโยบายของการคำนวณต้นทุนเวอร์ชันที่สองว่าไม่มีวันที่เริ่มต้น จากนั้นป้อนวันที่เริ่มต้นเมื่อคุณป้อนเรกคอร์ดต้นทุนแต่ละเรกคอร์ด  จากนั้นป้อนวันที่เริ่มต้นเมื่อคุณป้อนเรกคอร์ดต้นทุนแต่ละเรกคอร์ด วันที่เริ่มต้นควรเป็นวันที่ก่อนที่จะมีการสั่งซื้อหรือผลิตสินค้าใหม่
2.  Use the **Item price** page to enter cost records for new purchased items. สำหรับเรกคอร์ดต้นทุนแต่ละเรกคอร์ด และใช้วันที่เริ่มต้นที่มาก่อนวันที่ผลิตที่คาดไว้ สำหรับสินค้าที่ผลิตใหม่
3.  Calculate the cost of new manufactured items by using the **Calculation** page. Open the **Calculation** page from the **Costing version maintenance** page, and then select the costing version that contains the incremental updates. ใช้เกณฑ์การเลือกเพื่อระบุสินค้าที่ผลิตใหม่ใดๆ ส่วนประกอบที่ผลิตอย่างใดอย่างหนึ่ง  ในโครงสร้างผลิตภัณฑ์แบบหลายระดับ คุณอาจต้องระบุสินค้าหลักใดๆที่ประกอบด้วยสินค้าที่ผลิตใหม่เป็นส่วนประกอบ  ป้อนวันที่เริ่มต้นสำหรับสูตรการผลิต (BOM) ที่สอดคล้องกับจุดเริ่มต้นของการผลิตสำหรับสินค้าที่ผลิตใหม่  วันที่เริ่มต้นควรอยู่ในวันที่มีผลบังคับใช้สำหรับเวอร์ชัน BOM และเวอร์ชันกระบวนการผลิตของสินค้า  **หมายเหตุ:**เป็นเรกคอร์ดต้นทุนที่ขาดหายไปสามารถบ่งชี้สินค้าที่ผลิตใหม่ได้ การคำนวณ BOM สามารถถูกจำกัดกับสินค้าที่มีต้นทุนที่ขาดหายไป
4.  ตรวจสอบความสมบูรณ์และความถูกต้องของการคำนวณต้นทุนสำหรับสินค้าที่ผลิตใหม่  Use the **Complete** page to review the calculated costs for each item cost record, and also review any Infolog warning messages. Alternatively, use the **Calculation** page to review the calculated costs.
5.  ใช้หน้า **การตั้งค่าเวอร์ชันการคิดต้นทุน** เพื่อเปลี่ยนแฟล็กการบล็อค เพื่ออนุญาตให้เปิดใช้งานเรกคอร์ดต้นทุนที่เปิดค้างไว้ในเวอร์ชันการคำนวณต้นทุนที่สอง
6.  Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to enable all pending cost records in the second costing version. You can also enable the pending cost records for individual items by clicking the **Activate** button on the **Item price** page.
7.  Use the **Costing version setup** page to change the blocking flags in the second costing version to prevent additional data maintenance. นโยบายการบล็อคป้องกันรายการของต้นทุนใหม่ที่ค้างอยู่และการเรียกใช้ต้นทุนที่ค้างอยู่



