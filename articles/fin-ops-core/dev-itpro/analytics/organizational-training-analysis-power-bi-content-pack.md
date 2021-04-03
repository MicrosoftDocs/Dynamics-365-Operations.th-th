---
title: เนื้อหา Power BI การฝึกเชิงองค์กร
description: หัวข้อนี้อธิบายเนื้อหา Finance and Operations - การฝึกอบรมขององค์กร Power BI
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: de81c0268b0eb726ff3119bfef53a64d372df6d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564578"
---
# <a name="organizational-training-power-bi-content"></a>เนื้อหา Power BI การฝึกเชิงองค์กร

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายเนื้อหา Finance and Operations - การฝึกอบรมขององค์กร Power BI

## <a name="reports-that-are-included-in-the-content-pack"></a>รายงานที่รวมอยู่ในชุดเนื้อหา
หลังจากที่คุณได้เชื่อมต่อชุดเนื้อหากับข้อมูลของคุณแล้ว รายงานจะแสดงข้อมูลขององค์กรของคุณ ถ้าคุณไม่เคยใช้ Microsoft Power BI มาก่อน คุณสามารถเรียนรู้เพิ่มเติมได้ใน [หน้าแนวทางการเรียนรู้สำหรับ Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData) รายงานที่รวมอยู่ในชุดเนื้อหามีทั้งแผนภูมิและตารางที่ประกอบด้วยข้อมูลเพิ่มเติม ตารางต่อไปนี้ให้คำอธิบายเกี่ยวกับรายงาน

| รายงาน          | เนื้อหา                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| การวิเคราะห์หลักสูตร | การลงทะเบียนตามสถานที่ ผู้เข้าร่วมหลักสูตรตามสถานะ และรายการลงทะเบียน |
| ชนิดของหลักสูตร    | ชนิดของหลักสูตรตามทักษะ                                                       |

คุณสามารถกรองข้อมูลแผนภูมิและไทล์ในรายงานเหล่านี้ และตรึงแผนภูมิและไทล์ไปยังแดชบอร์ด สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกรองและปักหมุดใน Power BI ดู [สร้างและตั้งค่าคอนฟิกแดชบอร์ด](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards)

## <a name="understanding-the-data-model-and-entities"></a>การทำความเข้าใจเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้
ข้อมูลใบสมัครถูกใช้เพื่อรวบรวมรายงานในชุดเนื้อหาการฝึกอบรมขององค์กร ตารางต่อไปนี้แสดงเอนทิตีที่ชุดเนื้อหายึดตาม

| เอนทิตี้                    | เนื้อหา                                                         | ความสัมพันธ์กับเอนทิตีอื่น |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| การฝึกอบรม\_CalendarOffset  | ปฏิทินออฟเซ็ตเพื่อแบ่งส่วนรายงาน                                | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees |
| การฝึกอบรม\_บริษัท         | บริษัทสามารถกรองข้อมูลรายงานโดย                                   | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees |
| หลักสูตร\_การฝึกอบรม          | หลักสูตร คำอธิบาย ชื่อผู้สอน สถานที่ ห้อง และสถานะ | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees การฝึกอบรม\_CourseSkill |
| การฝึกอบรม\_CourseAgenda    | วาระการประชุม หลักสูตร และเวลาเริ่มต้นและสิ้นสุด                          | การฝึกอบรม\_บริษัท การฝึกอบรม\_CalendarOffset การฝึกอบรม\_วันที่ การฝึกอบรม\_หลักสูตร |
| การฝึกอบรม\_CourseAttendees | ชื่อ สถานะ งาน และวันที่ลงทะเบียน                         | การฝึกอบรม\_บริษัท การฝึกอบรม\_CalendarOffset การฝึกอบรม\_วันที่ การฝึกอบรม\_ข้อมูลประชากร การฝึกอบรม\_การจ้างงาน การฝึกอบรม\_หลักสูตร การฝึกอบรม\_WorkerName การฝึกอบรม\_WorkerTitle การฝึกอบรม\_งาน การฝึกอบรม\_ตำแหน่ง |
| การฝึกอบรม\_CourseSkill     | ทักษะ ชนิดของทักษะ และระดับ                                     | หลักสูตร\_การฝึกอบรม |
| วันที่\_ฝึกอบรม            | จำนวนวัน, จำนวนสัปดาห์, จำนวนเดือน และจำนวนปี                                   | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees |
| ข้อมูลประชากร\_การฝึกอบรม    | วันเกิด เพศ เชื้อชาติ และสถานภาพการสมรส         | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees |
| การฝึกอบรม\_การจ้างงาน      | วันที่เริ่มต้น วันที่สิ้นสุด และวันที่เปลี่ยน                        | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees |
| การฝึกอบรม\_งาน             | ฟังก์ชัน ชนิด และตำแหน่งงาน                                        | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees |
| การฝึกอบรม\_ตำแหน่ง        | ตำแหน่งงาน ชื่อ และเทียบเท่าเต็มเวลา (FTE)                  | การฝึกอบรม\_CourseAgenda การฝึกอบรม\_CourseAttendees |
| การฝึกอบรม\_WorkerName      | ชื่อจริง นามสกุล และชื่อเต็ม                             | การฝึกอบรม\_CourseAttendees |
| การฝึกอบรม\_WorkerTitle     | ตำแหน่งงานและวันที่อายุงาน                                         | การฝึกอบรม\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]