---
title: ยกเลิกงานการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438455"
---
# <a name="cancel-a-planning-job"></a>ยกเลิกงานการวางแผน

[!include [banner](../../includes/banner.md)]

ใน Microsoft Dynamics 365 Supply Chain Management คุณสามารถยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน เมื่อคุณเลือก **ยกเลิก** ในกล่องโต้ตอบ เมื่องานการเพิ่มประสิทธิภาพการวางแผนถูกทริกเกอร์โดยตรงจากอินเทอร์เฟสผู้ใช้ (ไม่ได้อยู่ในพื้นหลัง) นี่จะไม่ยกเลิกงานการเพิ่มประสิทธิภาพการวางแผน แม้ว่าคุณจะได้รับคำเตือน เช่น "ยกเลิกการดำเนินงานแล้ว" คุณจะยังคงต้องใช้ขั้นตอนต่อไปนี้เพื่อยกเลิกงานการวางแผนที่มีการเพิ่มประสิทธิภาพการวางแผน


การยกเลิกงานการวางแผนที่ใช้งานอยู่ ให้ทำตามขั้นตอนต่อไปนี้ 

> [!NOTE]
> เฉพาะตำแหน่งงานที่เปิดอยู่เท่านั้น ที่สามารถยกเลิกได้

1. ไปที่ **การวางแผนหลัก \> ตั้งค่า \> แผน**
2. เลือกแผนที่เหมาะสมสำหรับการดำเนินการวางแผน
3. เลือก **ประวัติ**
4. เลือกงานการวางแผนที่จะยกเลิก
5. เลือก **ยกเลิก**

สถานะของงานจะเป็น **กำลังยกเลิก** จนกว่าบริการการเพิ่มประสิทธิภาพของการวางแผนยืนยันว่างานถูกยกเลิกแล้ว สถานะจะเปลี่ยนเป็น **ยกเลิกแล้ว**

> [!NOTE]
> การดูการเปลี่ยนแปลงสถานะ คุณต้องรีเฟรชหน้า โดยเลือกปุ่ม **รีเฟรช**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-overview.md)

[เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน](get-started.md)

[การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน](planning-optimization-fit-analysis.md)

[ดูประวัติการวางแผนและล็อกการวางแผน](plan-history-logs.md)

[ใช้ตัวกรองกับแผน](plan-filters.md)
