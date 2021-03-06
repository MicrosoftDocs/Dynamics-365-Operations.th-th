---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (5 มีนาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 115d7cd3d71eaddce2434cb1939c503d36bccdf8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527301"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (5 มีนาคม 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

### <a name="extending-option-sets-in-attract"></a>การขยายชุดตัวเลือกใน Attract

ใน Attract มีฟิลด์หลายฟิลด์ที่เป็นชุดตัวเลือกภายใน Common Data Service ความสามารถใหม่ได้ถูกนำมาใช้ในการขยายชุดตัวเลือก โดยเริ่มต้นด้วยฟิลด์เหตุผล **การปฏิเสธ** ฟิลด์ **ชนิดการจ้างงาน** และฟิลด์ **ชนิดของอายุงาน**

> [!IMPORTANT]
> ฟังก์ชันการโพสต์งานไปยัง LinkedIn จำเป็นต้องมีการใช้ฟิลด์ **ชนิดการจ้างงาน** และฟิลด์ **ชนิดของอายุงาน** ในหน้า **รายละเอียดงาน** ค่าเริ่มต้นในฟิลด์เหล่านี้ได้รับการสนับสนุน โดย LinkedIn และจะแสดงขึ้นเมื่อมีการโพสต์งาน ถ้าคุณกำลังโพสต์งานไปยัง LinkedIn และคุณปรับเปลี่ยนค่าชุดตัวเลือกที่มีอยู่สำหรับฟิลด์เหล่านี้ งานจะยังคงโพสต์ แต่ LinkedIn จะไม่แสดงค่า **ชนิดการจ้างงาน** และ **ชนิดของอายุงาน** แบบกำหนดเอง

## <a name="changes-in-onboarding"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

### <a name="private-preview-for-onboard-teams"></a>การแสดงตัวอย่างแบบส่วนตัวสำหรับทีมงานเตรียมความพร้อม
ขณะนี้ คุณสามารถแบ่งปันและทำงานร่วมกันได้อย่างง่ายดายบนเท็มเพลตทั่วทั้งองค์กรทั้งหมดของคุณ สำหรับข้อมูลเพิ่มเติม ดู [แบ่งปันแนวทางปฏิบัติทั่วทั้งองค์กรของคุณโดยใช้ทีมงานเตรียมความพร้อม](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams)

### <a name="private-preview-for-assignee-placeholders"></a>การแสดงตัวอย่างแบบส่วนตัวสำหรับตัวยึดตำแหน่งผู้รับมอบหมาย
คุณสามารถเพิ่มเท็มเพลตของคุณได้ โดยการกำหนดกิจกรรมให้กับบทบาท แทนที่จะเป็นแต่ละบุคคล จากนั้น บทบาทจะถูกกำหนดให้กับแต่ละบุคคลในขณะที่สร้างคำแนะนำ สำหรับข้อมูลเพิ่มเติม ดู [ลดขั้นตอนซ้ำซ้อนการจัดการคู่มือตามการกำหนดกิจกรรมให้กับบทบาท](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles)

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR
**สร้าง 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>ตั้งค่าคอนฟิกลำดับงานให้อนุมัติอัตโนมัติ หรือทำตามลำดับงานเมื่อผู้จัดการฝ่าย HR หรือสายงาน ส่งหรือปรับปรุงคำขอการลาหยุด
มีการเพิ่มเงื่อนไขลำดับงานใหม่เพื่ออนุญาตให้คำขอลางานได้รับอนุมัติโดยอัตโนมัติ ถ้าถูกส่งโดยผู้จัดการของพนักงาน หรือโดย HR วิธีหนึ่งที่จะได้รับการอนุมัติโดยอัตโนมัตินี้ในลำดับงานคือ การเปิดใช้งานการดำเนินการอัตโนมัติในการอนุมัติลำดับงาน

เงื่อนไขที่ได้ถูกเพิ่มประกอบด้วย:

- ถูกส่งโดย - ใช้เพื่อประเมินรหัสผู้ใช้ระบบของผู้ใช้ที่ส่งคำขอไปยังลำดับงาน
- ถูกส่งในนามของ - ใช้เพื่อประเมิน ถ้ามีการส่งคำขอลางานในนามของผู้ปฏิบัติงานที่เกี่ยวข้องกับคำขอ
- ถูกส่งโดยทรัพยากรบุคคล - ใช้เพื่อประเมิน หากผู้ใช้ระบบที่ส่งคำขอไปยังลำดับงานอยู่ในบทบาทของฝ่ายทรัพยากรบุคคล
- ถูกส่งโดยผู้จัดการ - ใช้เพื่อประเมินว่าผู้ใช้ที่ส่งคำขอลางานไปที่ลำดับงานคือ ผู้จัดการลำดับชั้นของรายการของผู้ปฏิบัติงานที่เกี่ยวข้องกับคำขอหรือไม่

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>เปิดใช้งานค่าตอบแทนคงที่ของพนักงานสำหรับการมอบหมายตำแหน่งในอนาคต
เป็นเรื่องปกติสำหรับพนักงานที่จะเข้าร่วมกับองค์กรที่มีวันที่เริ่มต้นในอนาคต การเปลี่ยนแปลงนี้เปิดใช้งานการกำหนดค่าตอบแทนคงที่สำหรับพนักงานที่มีการมอบหมายตำแหน่งงานในอนาคต

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>ฟิลด์ค่าจ้างของตำแหน่งจะว่างเปล่า เมื่อแก้ไขตำแหน่ง
ด้วยการเปลี่ยนแปลงนี้ เมื่อมีการร้องขอการเปลี่ยนแปลงไปยังตำแหน่งที่มีอยู่ ในขณะนี้ ฟิลด์ค่าจ้างจะตั้งค่าเริ่มต้นจะเป็นค่าปัจจุบัน

### <a name="other-miscellaneous-bug-fixes"></a>การแก้ไขปัญหาบักเบ็ดเตล็ดอื่นๆ
การแก้ไขบักรองอื่นๆ ถูกรวมอยู่กับรุ่นนี้

### <a name="upgrade-to-common-data-service"></a>อัพเกรดเป็น Common Data Service
เวลาสิ้นสุดการอัพเกรดเป็น Common Data Service ใกล้จะมาถึงเร็วๆ นี้ ลงชื่อเข้าใช้ไปยังศูนย์การจัดการ Power Apps เพื่อตรวจสอบว่าฐานข้อมูลของคุณต้องได้รับการอัพเกรดหรือไม่ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกำหนดเวลาสิ้นสุดและขั้นตอนที่จำเป็นในการอัพเกรด ดู [อัพเกรดเป็น Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds)

## <a name="coming-soon"></a>เร็วๆ นี้

###  <a name="advanced-compensation-security-fixed-and-variable"></a>ความปลอดภัยของค่าตอบแทนขั้นสูง (คงที่และผันแปร)
ในหลายองค์กร ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถเข้าถึงได้เฉพาะเรกคอร์ดค่าตอบแทนบางรายการ เช่น เรกคอร์ดสำหรับผู้บริหารหรือพนักงานตามภูมิภาค ด้วยการเปลี่ยนแปลงนี้ คุณสามารถจัดการและรักษาแผนค่าตอบแทนสำหรับกลุ่มพนักงานอื่นๆ ในองค์กรได้ แผนคงที่และผันแปรสามารถถูกกำหนด security role ซึ่งจะกำหนดการเข้าถึงแผนและข้อมูลพนักงานที่เกี่ยวข้องกับแผน เช่น เรกคอร์ดเงินโบนัสหรือเงินเดือน เฉพาะบทบาทที่มีการเข้าถึงที่กำหนด จะสามารถดำเนินการค่าตอบแทนสำหรับพนักงานเหล่านั้นได้

###  <a name="platform-update-24-for-finance-and-operations"></a>การอัพเดตแพลตฟอร์ม 24 สำหรับ Finance and Operations
สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการอัพเดตแพลตฟอร์ม 24 สำหรับ Finance and Operations ดู [มีอะไรใหม่ หรือเปลี่ยนแปลงใน Finance and Operations การอัพเดตแพลตฟอร์ม 24 (มีนาคม 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24)


[!INCLUDE[footer-include](../includes/footer-banner.md)]