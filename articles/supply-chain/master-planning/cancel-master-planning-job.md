---
title: ยกเลิกงานการวางแผนหลัก
description: หัวข้อนี้จะอธิบายถึงวิธีการยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการวางแผนในตัว
author: ChristianRytt
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08dd612d9fb01ba2db6d4fcc7db9507a41a4b29f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203928"
---
# <a name="cancel-a-master-planning-job"></a>ยกเลิกงานการวางแผนหลัก

[!include [banner](../includes/banner.md)]

ใน Microsoft Dynamics 365 Supply Chain Management มีหลายตัวเลือกสำหรับการยกเลิกงานการวางแผนหลัก ตัวอย่างเช่น คุณอาจต้องการยกเลิกงานการวางแผนหลัก ถ้ามีการเริ่มต้นโดยไม่ได้ตั้งใจหรือทำงานนานกว่าที่คาดไว้และคุณต้องการที่จะสิ้นสุด วิธีที่ดีที่สุดในการยกเลิกงานการวางแผนคือจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น** ตัวเลือกอื่นจากหน้า **ชุดงาน** และ **ชุดงานที่ปรับปรุง** ควรจะใช้เฉพาะเมื่อยกเลิกงานการวางแผนหลักจาหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสมบูรณ์** ไม่เสร็จภายในไม่กี่นาที

## <a name="preferred-cancel-option"></a>ตัวเลือกการยกเลิกที่ต้องการ
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>ยกเลิกงานการวางแผนหลักจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**
1. ไปยัง **การวางแผนหลัก > การสอบถามและรายงาน > การวางแผนหลัก > กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**
2. เลือกบรรทัดที่กระบวนการวางแผนที่คุณต้องการยกเลิก
3. คลิก **ยกเลิก**

## <a name="additional-cancel-options"></a>ตัวเลือกยกเลิกเพิ่มเติม
รายการเหล่านี้ควรถูกใช้ เมื่อยกเลิกงานการวางแผนหลักจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น** ไม่เสร็จสมบูรณ์ภายในสองสามนาที

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>ลบงานการวางแผนหลักออกจากหน้า **ชุดงาน**
1. ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**
2. เลือกบรรทัดที่กระบวนการวางแผนงานที่คุณต้องการลบ
3. คลิก **ลบ**

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>ยกเลิกงานการวางแผนหลักออกจากหน้า **ชุดงานที่ปรับปรุง**
1. ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**
2. ถ้าไม่มีการแสดงรหัสงานในรายการให้คลิก **สลับไปยังแบบฟอร์มที่ปรับปรุงแล้ว** มิฉะนั้นดำเนินการขั้นตอนต่อไป
3. เปิดชุดงาน คลิก **รหัสงาน** สำหรับชุดงานที่มีงานที่คุณต้องการสิ้นสุด
4. ใน **ชุดงาน** เลือกงานที่จะสิ้นสุด
5. บนแท็บ **ชุดงาน** ให้คลิก **ยกเลิก**
