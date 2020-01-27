---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 มีนาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 79bb8c0ed3c3f3bee62a8bc384a9d3a15cfe881a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897614"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-14-2019"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 มีนาคม 2019)

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract
มีการแก้ไขบักรองที่รวมอยู่กับรุ่นนี้

## <a name="changes-in-onboarding"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม
มีการแก้ไขบักรองที่รวมอยู่กับรุ่นนี้

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR
**สร้าง 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>การจัดการประสิทธิภาพการทำงานที่ไม่ได้ทำงานอยู่ในสถานการณ์จำลองทั้งหมด เมื่อใช้บทบาทความปลอดภัยที่ซ้ำกัน
การเปลี่ยนแปลงที่ทำในรุ่นนี้เปิดใช้งานสถานการณ์การจัดการประสิทธิภาพการทำงาน เมื่อใช้บทบาทแบบสำเร็จรูปหรือแบบซ้ำกัน

### <a name="mass-assign-checklists-to-workers"></a>กำหนดรายการตรวจสอบจำนวนมากให้กับผู้ปฏิบัติงาน
ด้วยการเปลี่ยนแปลงนี้ ขณะนี้ คุณสามารถเลือกพนักงานหลายคน และกำหนดรายการตรวจสอบจำนวนมากอย่างน้อยหนึ่งรายการให้กับพนักงานเหล่านั้น 

### <a name="platform-update-24-for-finance-and-operations"></a>การอัพเดตแพลตฟอร์ม 24 สำหรับ Finance and Operations
สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการอัพเดตแพลตฟอร์ม 24 สำหรับ Finance and Operations ให้ดู [มีอะไรใหม่หรือเปลี่ยนแปลงบ้างในการอัพเดตแพลตฟอร์ม 24 สำหรับ Finance and Operations (มีนาคม 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24) การเปลี่ยนแปลงที่สำคัญในแพลตฟอร์ม 24 ประกอบด้วย: 

- ข้อความแจ้งเตือนถูกเปิดใช้งานใน Talent
- ขณะนี้แถบนำทางที่ปรับปรุงแล้วจัดเรียงตามส่วนหัวของ Office

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>การปรับปรุงที่ตั้ง Office สลับบริบทไปด้านบนของรายชื่อผู้ปฏิบัติงาน
ด้วยการนำออกใช้ปัจจุบัน การเปลี่ยนที่ตั้ง office จะไม่สลับบริบทของผู้ปฏิบัติงานที่คุณกำลังดู เมื่อกำหนดตำแหน่งที่ตั้ง office

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>วันที่สิ้นสุดการมอบหมายตำแหน่งไม่ได้แสดงอย่างถูกต้องในการดำเนินการจ้างงานและโอนย้ายผู้ปฏิบัติงาน
ขณะนี้ วันที่สิ้นสุดการมอบหมายตำแหน่งแสดงขึ้นอย่างถูกต้องตามโซนเวลาที่ต้องการของผู้ใช้ เมื่อใช้การดำเนินการ

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>เอนทิตีงาน Common Data Service ไม่อนุญาตให้ปรับปรุงฟิลด์ชนิดงานและฟิลด์ฟังก์ชันงาน
เอนทิตี Common Data Service ในขณะนี้ซิงโครไนส์อย่างถูกต้อง เมื่อปรับปรุงโดยใช้ Common Data Service

## <a name="coming-soon"></a>เร็วๆ นี้

###  <a name="advanced-compensation-security-fixed-and-variable"></a>ความปลอดภัยของค่าตอบแทนขั้นสูง (คงที่และผันแปร)
ในองค์กรหลายองค์กร ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการอาจมีการเข้าถึงเรกคอร์ดค่าตอบแทนบางรายการเท่านั้น รายการเหล่านี้อาจมีไว้สำหรับผู้บริหารหรือพนักงานในภูมิภาค ด้วยการเปลี่ยนแปลงนี้ HR สามารถจัดการและรักษาแผนค่าตอบแทนสำหรับกลุ่มพนักงานอื่นๆ ในองค์กรได้ คุณสามารถมอบหมายบทบาทความปลอดภัยไปยังแผนคงที่และผันแปรที่กำหนดการเข้าถึงแผนและข้อมูลพนักงานที่เกี่ยวข้องกับแผน เช่น เรกคอร์ดเงินโบนัสหรือเงินเดือน เฉพาะบทบาทที่มีการเข้าถึงที่ได้รับ สามารถดำเนินการค่าตอบแทนสำหรับพนักงานเหล่านั้นได้

###  <a name="email-support-for-alerts"></a>การสนับสนุนอีเมลสำหรับข้อความแจ้งเตือน
ด้วยการอัพเดตแพลตฟอร์ม 24 สำหรับ Finance and Operations ผู้ใช้สามารถสร้างกฎการแจ้งเตือนทางอีเมลโดยอัตโนมัติไปยังผู้ติดต่อที่ทริกเกอร์โดยเหตุการณ์

### <a name="duplicate-employee-check-interface-changes"></a>ทำซ้ำการตรวจสอบพนักงาน: เปลี่ยนแปลงอินเทอร์เฟส
ด้วยการเปลี่ยนแปลงนี้ ข้อมูลซ้ำจะถูกตรวจพบขณะที่คุณป้อนฟิลด์ชื่อ และสถานะจะแสดงจำนวนของข้อมูลที่พบ คุณสามารถเลือกการเชื่อมโยงที่ให้มาเพื่อเปิดหน้าใหม่เพื่อประเมินว่าจะใช้การจับคู่ที่ตรวจพบหรือไม่ ฟอร์มข้อมูลซ้ำจะไม่เปิดขึ้นโดยอัตโนมัติ เพื่อหลีกเลี่ยงการรบกวนการป้อนข้อมูล
