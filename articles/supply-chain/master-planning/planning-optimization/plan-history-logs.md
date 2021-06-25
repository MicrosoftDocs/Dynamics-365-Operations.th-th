---
title: ดูประวัติการวางแผนและล็อกการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการดูประวัติของงานการวางแผน ซึ่งทริกเกอร์โดยฟังก์ชันการเพิ่มประสิทธิภาพของการวางแผน
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187258"
---
# <a name="view-plan-history-and-planning-logs"></a>ดูประวัติการวางแผนและล็อกการวางแผน

[!include [banner](../../includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการดูประวัติของงานการวางแผน ซึ่งทริกเกอร์โดยฟังก์ชันการเพิ่มประสิทธิภาพของการวางแผนใน Microsoft Dynamics 365 Supply Chain Management

เมื่อต้องการดูประวัติสำหรับแผนให้เปิดแผนโดยไปที่ **การวางแผนหลัก** \> **การตั้งค่าแผน** \> **แผน** \> **แผนหลัก** และเลือก **ประวัติ** ประวัติแสดงรายการงานทั้งหมดสำหรับแผนที่เลือก รายการรวมงานที่เสร็จสมบูรณ์และงานที่ใช้งานอยู่

ประวัติของงานเกี่ยวกับการวางแผนหลักในการเพิ่มประสิทธิภาพการวางแผนจะรักษาไว้เพียง 60 เรกคอร์ดต่อแผนหลัก เมื่อใดก็ตามที่คุณรันการคํานวณการวางแผนหลักใหม่ เรกคอร์ดประวัติแรกสุดของแผนนั้นจะถูกลบออก

นอกจากการดูเวลาเริ่มต้นและสถานะของงานแล้วคุณยังสามารถดูล็อกของงานที่ระบุได้ ล็อกรวมถึงข้อมูลเพิ่มเติมและคำเตือน ไม่ใช่ทุกงานที่จะมีล็อก เมื่อต้องการดูล็อกของงานให้เลือก **ล็อก** รายการบันทึกจะจัดเก็บไว้เฉพาะเมื่อ 30 วันหลังจากวันที่งานเสร็จสิ้น หลังจากนั้นจะถูกลบโดยอัตโนมัติ

## <a name="related-resources"></a>ทรัพยากรที่เกี่ยวข้อง

- [ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-overview.md)
- [เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน](get-started.md)
- [การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน](planning-optimization-fit-analysis.md)
- [ใช้ตัวกรองกับแผน](plan-filters.md)
- [ยกเลิกงานการวางแผน](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]