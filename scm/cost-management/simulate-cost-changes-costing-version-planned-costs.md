---
title: "จำลองการเปลี่ยนแปลงของต้นทุน โดยการใช้เวอร์ชันการคำนวณต้นทุนสำหรับต้นทุนที่วางแผนไว้"
description: "บทความนี้อธิบายวิธีที่คุณสามารถจำลองผลกระทบของการเปลี่ยนแปลงต้นทุน ในต้นทุนที่คำนวณแล้วของสินค้าที่ผลิต โดยการใช้เวอร์ชันการคำนวณต้นทุนที่แยกต่างหากสำหรับต้นทุนที่วางแผนไว้"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8bdea0ae201ffbf805707cdfda2489c316779e5f
ms.lasthandoff: 03/31/2017


---

# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>จำลองการเปลี่ยนแปลงของต้นทุน โดยการใช้เวอร์ชันการคำนวณต้นทุนสำหรับต้นทุนที่วางแผนไว้

บทความนี้อธิบายวิธีที่คุณสามารถจำลองผลกระทบของการเปลี่ยนแปลงต้นทุน ในต้นทุนที่คำนวณแล้วของสินค้าที่ผลิต โดยการใช้เวอร์ชันการคำนวณต้นทุนที่แยกต่างหากสำหรับต้นทุนที่วางแผนไว้

คุณสามารถจำลองผลกระทบของการเปลี่ยนแปลงต้นทุนในต้นทุนที่คำนวณแล้วของสินค้าที่ผลิต  โดยการใช้เวอร์ชันการคำนวณต้นทุนแยกต่างหากสำหรับต้นทุนที่วางแผนไว้ ใช้เวอร์ชันการคำนวนต้นทุนแยกต่างหากนี้เพื่อป้อนเรกคอร์ดต้นทุนที่ค้างอยู่ ซึ่งสะท้อนการเปลี่ยนแปลงของต้นทุนส่วนเพิ่มและคำนวณต้นทุนที่มีผลต่อสินค้าที่ผลิต เนื่องจากหลักการถอยกลับสำหรับต้นทุนที่คำนวณอยู่จะถูกใช้ในการคำนวณสูตรการผลิต BOM เฉพาะต้นทุนส่วนเพิ่มเท่านั้นที่ต้องถูกป้อน

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>คำแนะนำสำหรับการกำหนดเวอร์ชันการจำลองการคำนวณต้นทุน
ใช้คำแนะนำต่อไปนี้เมื่อคุณกำหนดเวอร์ชันการคำนวณต้นทุนสำหรับการจำลอง

-   กำหนดชนิดการคำนวณต้นทุนของ **ต้นทุนที่วางแผนไว้**
-   กำหนดตัวระบุที่มีความหมายสำหรับเวอร์ชันการคำนวณต้นทุน เช่น **การจำลอง**
-   ตรวจสอบให้แน่ใจว่าเนื้อหามีเรกคอร์ดต้นทุนรวมอยู่ด้วย
-   อนุญาตให้มีรายการของเรกคอร์ดต้นทุน อย่าบล็อครายการของต้นทุนคงค้าง
-   อนุญาตให้มีรายการของเรกคอร์ดต้นทุนสำหรับไซต์ทั้งหมด ถ้าคุณระบุไซต์ คุณจะจำกัดรายการของเรกคอร์ดต้นทุนกับไซต์นั้น
-   ป้องกันการเรียกใช้ต้นทุนที่รอดำเนินการ  ต้องมีการป้อนเฉพาะต้นทุนที่ค้างอยู่สำหรับเรกคอร์ดต้นทุนในเวอร์ชันการคำนวณต้นทุนจำลอง
-   ห้ามป้อนวันที่ "จาก"  วันที่คำนวณจะถูกป้อนสำหรับการคำนวณ BOM แต่ละรายการที่ใช้เวอร์ชันการคำนวณต้นทุนจำลอง
-   Specify a fallback principle of **Current active**. หลักการถอยกลับอนุญาตให้มีการเปลี่ยนแปลงต้นทุนที่เพิ่มขึ้นที่จะถูกป้อนสำหรับวัตถุประสงค์เพื่อการจำลอง แต่ใช้ต้นทุนการใช้งานในปัจจุบันให้เป็นแหล่งที่มาสำหรับเรกคอร์ดต้นทุนอื่นๆ  ระบบจะถือว่ามีต้นทุนการใช้งานในปัจจุบันอยู่สำหรับเรกคอร์ดต้นทุนอื่นๆทั้งหมด
-   Specify a cost price model of **Version cost price**, but don't restrict calculations. For example, the simulations can also use the **BOM calculation group** cost price model to indicate the source of cost contribution data for purchased items.
-   Specify an explosion mode of **Multilevel**, but don't restrict calculations. แบบจำลองสามารถใช้โหมดการกระจายอื่นได้

## <a name="costing-versions"></a>เวอร์ชันการคิดต้นทุน
สถานการณ์ต่อไปนี้แสดงวิธีการใช้เวอร์ชันการคำนวณต้นทุนจำลอง ที่ถูกใช้เพื่อจำลองผลกระทบของการเปลี่ยนแปลงต้นทุน  ก่อนที่จะป้อนการเปลี่ยนแปลงต้นทุนที่มีการจำลอง ให้ลบเรกคอร์ดต้นทุนที่ค้างอยู่ในเวอร์ชันการคำนวณต้นทุนจำลองเพื่อให้คุณมีจุดเริ่มต้นที่ล้างข้อมูลแล้ว  Use the **Item price** page to view and delete the pending cost records that are related to item prices and cost category prices.

-   จำลองการเปลี่ยนแปลงต้นทุนสำหรับสินค้าที่ซื้อ  ตัวอย่างเช่น การเปลี่ยนแปลงต้นทุนอาจสะท้อนการเพิ่มขึ้นหรือลดลงที่คาดไว้ในต้นทุนของวัสดุซื้อที่สำคัญ  To define the different cost for a purchased item, use the **Item price** page to enter a pending cost record in the simulation costing version.
-   จำลองการเปลี่ยนแปลงต้นทุนสำหรับประเภทต้นทุน  ตัวอย่างเช่น การเปลี่ยนแปลงต้นทุนอาจสะท้อนการเพิ่มหรือการลดที่คาดไว้ของอัตราแรงงาน หรือในอัตราต่อชั่วโมงสำหรับทรัพยากรการดำเนินงาน  To define the different cost for a cost category, use the **Cost category price** page to enter a pending cost record in the simulation costing version.
-   จำลองการเปลี่ยนแปลงต้นทุนในสูตรการคำนวณต้นทุนทางอ้อม  ตัวอย่างเช่น การเปลี่ยนแปลงต้นทุนอาจสะท้อนการเพิ่มหรือการลดที่คาดไว้ในค่าโสหุ้ยการผลิต  To define the change in an indirect cost calculation formula, use the **Costing sheet setup** page to enter a pending cost record in the simulation of costing version, and to validate and save the change.

หลังจากที่คุณป้อนการเปลี่ยนแปลงต้นทุนที่มีการจำลอง ให้คำนวณต้นทุนสำหรับสินค้าที่ผลิตที่ได้รับผลกระทบจากการเปลี่ยนแปลงต้นทุน  Use the **Calculation** page for the simulation costing version, and identify the selected manufactured items that will be affected by the cost changes. การคำนวณ BOM ใช้กับสินค้าที่ผลิตทั้งหมดยกเว้นว่าคุณได้เลือกสินค้าเฉพาะ  อีกทางหนึ่งคือ คุณสามารถใช้ตัวเลือกการคำนวณ BOM สำหรับการอัพเดตตำแหน่งที่จะใช้  ดูเรกคอร์ดต้นทุนสินค้าในเวอร์ชันการคำนวณต้นทุนจำลองเพื่อวิเคราะห์วิธีเปลี่ยนแปลงต้นทุนที่มีการจำลอง ซึ่งส่งผลกระทบต่อต้นทุนของสินค้าที่ผลิตที่เลือก  Use the **Item price** page and the **Calculate item cost** page to view and analyze the costs.


