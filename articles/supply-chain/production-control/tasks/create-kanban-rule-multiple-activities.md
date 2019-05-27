---
title: สร้างกฎคัมบังสำหรับหลายกิจกรรม
description: 'กระบวนงานนี้แสดงวิธีการสร้างกฎคัมบังที่ประกอบด้วยกิจกรรมหลายรายการจากขั้นตอนการผลิต '
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe7e1c67161bd77e6ddc5d7c9f1607fe895ce21
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558482"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>สร้างกฎคัมบังสำหรับหลายกิจกรรม

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างกฎคัมบังที่ประกอบด้วยกิจกรรมหลายรายการจากขั้นตอนการผลิต  ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF งานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เนื่องจากเป็นผู้จัดเตรียมการผลิตผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยนในสภาพแวดล้อมแบบลีน


## <a name="create-a-new-kanban-rule"></a>สร้างกฎคัมบังใหม่
1. ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง
2. คลิก สร้าง
3. ในฟิลด์กลยุทธ์การเติมสินค้า ให้เลือก 'จัดกำหนดการแล้ว'
4. ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือก SpeakerAssemblyAndPolish  
5. เลือกกล่องกาเครื่องหมายกิจกรรมหลายอย่าง
    * วัตถุประสงค์คือเพื่อรวมกิจกรรมหนึ่งรายการขึ้นไปในกฎคัมบัง  คุณสามารถเลือกเส้นทางในขั้นตอนการผลิตเมื่อคุณเลือกกิจกรรมแผนล่าสุด  
6. ในฟิลด์กิจกรรมการวางแผนสุดท้าย ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือก SpeakerTestAndPackaging  หลังจากที่คุณเลือกค่า หน้าจะเปิดโดยอัตโนมัติ  เลือกขั้นตอนคัมบัง SpeakerAssemblyAndPolish > SpeakerTestAndPackaging คลิก ตกลง  
7. ขยายส่วนรายละเอียด 
8. ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือก สินค้า L0006  

## <a name="create-kanban-and-view-jobs"></a>สร้างคัมบังและดูงาน
1. ขยายส่วนคัมบัง
2. คลิก เพิ่ม
3. ในฟิลด์จำนวนคัมบังใหม่ ให้ป้อน '1'
    * นี่จะสร้างหนึ่งคัมบัง  
4. ตั้งค่าปริมาณผลิตภัณฑ์เป็น 3
    * คัมบังจะประมวลผลผลิตภัณฑ์ 3 รายการ  
5. ในฟิลด์วันที่/เวลาที่ครบกำหนด ให้ป้อนวันที่และเวลา
    * คุณสามารถป้อน วันนี้  
6. คลิก สร้าง
7. คลิก รายละเอียด
    * โปรดสังเกตว่าคัมบังมีงานกระบวนการสองรายการจากขั้นตอนการผลิต  รายการแรกคือ SpeakerAssemblyAndPolish และรายการที่สองเป็คือ SpeakerTestAndPackaging  
    * นี่เป็นขั้นตอนสุดท้าย!  

