---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 กุมภาพันธ์ 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462719"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 กุมภาพันธ์ 2019)

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract
มีการแก้ไขบักรองที่รวมอยู่กับรุ่นนี้

## <a name="changes-in-onboarding"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม
มีการแก้ไขบักรองที่รวมอยู่กับรุ่นนี้
 
## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR 
**สร้าง 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>เอนทิตีค่าตอบแทนคงที่ของพนักงานไม่ส่งออกเรกคอร์ดทั้งหมด
ด้วยการเปลี่ยนแปลงนี้ เอนทิตี **ค่าตอบแทนคงที่ของพนักงาน** จะส่งออกเรกคอร์ดทั้งหมดในขณะนี้ เอนทิตีสามารถถูกใช้เพื่อสร้าง และอัพเดตเรกคอร์ดค่าตอบแทนคงที่ที่มีอยู่สำหรับพนักงาน 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>วันสิ้นสุดการจ้างงานไม่ใช้การตั้งค่าโซนเวลาที่ต้องการของพนักงาน
ตอนนี้วันสิ้นสุดการจ้างงานกำลังใช้โซนเวลาที่ต้องการของผู้ใช้ เมื่อสร้างหรือสิ้นสุดการจ้างงานกับบริษัท
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>ที่อยู่ในสหราชอาณาจักรแสดงผลในการวิเคราะห์เป็นที่อยู่ในสวิตเซอร์แลนด์ตะวันออก
ในรุ่นนี้ มีการทำการเปลี่ยนแปลงเพื่อแก้ไขการไม่ตรงแนวในที่อยู่ในรายงาน **การจัดการบุคลากร** "จำนวนพนักงานตามที่ตั้ง"
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>ไม่มีการเติมข้อมูลรหัสการเลิกจ้างในเรกคอร์ดการมอบหมายตำแหน่งงานของผู้ปฏิบัติงาน เมื่อสิ้นสุดตำแหน่ง
มีการทำการเปลี่ยนแปลงเป็นค่าเริ่มต้นของรหัส "เหตุผลการสิ้นสุดการจ้างงาน" เมื่อสิ้นสุดการมอบหมายตำแหน่งงานของผู้ปฏิบัติงาน

### <a name="new-entity-created-for-job-compensation-levels"></a>เอนทิตีใหม่ที่สร้างขึ้นสำหรับระดับค่าตอบแทนของงาน
เอนทิตีกรอบงานการจัดการข้อมูลใหม่ (DMF) ถูกสร้างขึ้น เอนทิตีแสดงสำหรับการสร้างและการปรับปรุงไปยังระดับค่าตอบแทน มูลค่าตลาด และข้อมูลการสำรวจความคิดเห็น สำหรับงานแต่ละงานที่กำหนดไว้ในระบบ


[!INCLUDE[footer-include](../includes/footer-banner.md)]