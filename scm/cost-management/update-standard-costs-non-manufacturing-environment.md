---
title: "อัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต"
description: "บทความนี้ให้คำแนะนำสำหรับวิธีการอัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: be3e5417341094caf0565c1c5ee4f9cbc40f8e76
ms.lasthandoff: 03/31/2017


---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>อัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต

บทความนี้ให้คำแนะนำสำหรับวิธีการอัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต

คำแนะนำต่อไปนี้จะถือว่าคุณใช้วิธีการแบบสองเวอร์ชันเพื่ออัพเดตต้นทุนมาตรฐาน  ในวิธีนี้ การคำนวณต้นทุนในเวอร์ชันหนึ่งประกอบด้วย ต้นทุนมาตรฐานที่กำหนดไว้ตั้งแต่เริ่มแรกสำหรับช่วงเวลาแน่นอนไม่เปลี่ยนแปลง ในขณะที่เวอร์ชันที่สองประกอบด้วยการอัพเดตข้อมูลเพิ่มเติม  การอัพเดตแต่ละครั้งถูกป้อนเป็นเรกคอร์ดต้นทุนซึ่งถูกแนบเวอร์ชันการคิดต้นทุนที่สอง และในท้ายที่สุด จะถูกเปิดใช้งาน  อีกทางหนึ่งคือ วิธีแบบหนึ่งเวอร์ชันใช้ชุดของต้นทุนมาตรฐานที่ถูกกำหนดไว้ตั้งแต่เริ่มต้น  วิธีแบบสองเวอร์ชันต้องการให้คุณกำหนดเวอร์ชันการคิดต้นทุนที่สอง  นี่คือคำแนะนำสำหรับการกำหนดการคิดต้นทุนนี้:

-   กำหนดชนิดการคำนวณต้นทุนของ **ต้นทุนมาตรฐาน**
-   กำหนดรหัสสำคัญที่ระบุเนื้อหาของเวอร์ชันการคำนวณต้นทุน เช่น **2016-UPDATES**
-   ตรวจสอบให้แน่ใจว่าเนื้อหามีเรกคอร์ดต้นทุนรวมอยู่ด้วย
-   อนุญาตให้เรกคอร์ดต้นทุนถูกป้อนสำหรับไซต์ทั้งหมด  ถ้าคุณระบุไซต์ เรกคอร์ดต้นทุนสามารถถูกป้อนสำหรับไซต์ดังกล่าวเท่านั้น
-   Indicate a fallback principle of **None**. หลักการถอยกลับจะใช้เฉพาะกับการคำนวณต้นทุนสำหรับสินค้าที่ผลิตเท่านั้น

ในการแก้ไข เปลี่ยนแปลง หรืออัพเดตต้นทุนมาตรฐานสำหรับสินค้าใหม่ ให้ดำเนินการตามขั้นตอนเหล่านี้

1.  ใช้การ**กำหนดต้นทุนเวอร์ชัน****ตั้งค่า**หน้าเพื่อให้สามารถใช้ข้อมูลต้นทุนจะถูกป้อนลงในเวอร์ชันการคำนวณต้นทุนสอง และอาจป้องกันการเรียกใช้งานของต้นทุนที่เปิดค้างไว้ ดังนั้นการเรียกใช้งานจะได้รับอนุญาตหลังจากที่มีการกำหนดต้นทุนที่เปิดค้างไว้ทั้งหมดอย่างถูกต้องและเสร็จสมบูรณ์แล้ว  You can also optionally enter a date in the **From date** field. ดังเช่นคำแนะนำทั่วไป ให้ใช้วันที่ที่คุณต้องการเปิดใช้งานการอัพเดตที่เพิ่มขึ้น  Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.
2.  ใช้หน้า **ราคาสินค้า** เพื่อป้อนการอัพเดตเป็นเรกคอร์ดต้นทุนสินค้า ที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง
3.  ใช้รายงาน **ราคาสินค้า** เพื่อตรวจสอบความสมบูรณ์และความถูกต้องของเรกคอร์ดต้นทุนสินค้า ที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง
4.  ใช้หน้า **การบำรุงรักษาเวอร์ชันการคิดต้นทุน** เพื่อเปลี่ยนแฟล็กการบล็อค เพื่ออนุญาตการเปิดใช้งานของเรกคอร์ดต้นทุนที่เปิดค้างไว้ที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง
5.  Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version. You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.
6.  To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version. นโยบายการบล็อคจะป้องกันการป้อนรายการของต้นทุนที่เปิดค้างไว้ใหม่และการเรียกใช้งานต้นทุนที่เปิดค้างไว้



