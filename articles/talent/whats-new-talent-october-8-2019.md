---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (8 ตุลาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 159320dcbdf257862378b347172ef71832e293dc
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626073"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (8 ตุลาคม 2019)

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้จะนำไปใช้กับการสร้างหมายเลข 8.1.2542 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>การลบการลงทะเบียนแบบเปิดของผลประโยชน์ออกจากการแสดงตัวอย่างสาธารณะ

ในการเข้าร่วมกับการประกาศของเราในประกาศบล็อก [การลงทุนเชิงกลยุทธ์ในความยอดเยี่ยมในการดำเนินงานของไดรฟ์ Core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) Microsoft จะลบคุณลักษณะการลงทะเบียนแบบเปิดของผลประโยชน์ออกจากการแสดงตัวอย่างสาธารณะในวันที่ 18 ตุลาคม 2019 แต่ฟังก์ชันใหม่จะถูกนำออกใช้ในอนาคตแทน การใช้งานการผลิตของคุณลักษณะการลงทะเบียนแบบเปิดของผลประโยชน์ที่ขณะนี้อยู่ในการแสดงตัวอย่างจะไม่ได้รับการสนับสนุน 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>มีการเปิดการรวม Common Data Service ในขณะนี้โดยค่าเริ่มต้นในส่วนสำรองใหม่ (343675)
 
เมื่อมีการเตรียมใช้งานสภาพแวดล้อมใหม่ การรวม Common Data Service จะถูกปิดใช้งานในขณะนี้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกการรวม Common Data Service](hr-common-data-service-integration.md)

### <a name="streamlined-employee-entry-and-navigation"></a>การป้อนข้อมูลและการนำทางของพนักงานที่มีประสิทธิภาพ

ฟังก์ชันสำหรับการป้อนข้อมูลพนักงานและการนำทางพร้อมใช้งานในสภาพแวดล้อมทั้งหมดในขณะนี้ เมื่อต้องการเปิดใช้งานคุณลักษณะนี้ ไปที่ **การจัดการระบบ \> ลิงค์ \> การตั้งค่า \> พารามิเตอร์ระบบ \> คุณลักษณะตัวอย่าง** และเลือก **ฟอร์มผู้ปฏิบัติงานที่มีการปรับปรุงและการนำทาง** แล้วคุณลักษณะนี้จะถูกเปิดสำหรับผู้ใช้ทั้งหมด คุณสามารถปิดตัวเลือกนี้ได้ตลอดเวลา

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การป้อนข้อมูลพนักงานที่มีประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2

### <a name="issue-attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>ปัญหา: Attract และ Onboard สร้างผู้ปฏิบัติงานที่ไม่ได้ใช้งานใน Core HR (380517)

การนำออกใช้ของสัปดาห์นี้แก้ไขปัญหาที่ Attract และ Onboard สร้างผู้ปฏิบัติงานที่ไม่ได้ใช้งานใน Core HR

### <a name="issue-the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>ปัญหา: ลำดับงานล้มเหลว เมื่อผู้จัดการลงชื่อเข้าใช้ในบริษัทอื่น ในขณะที่เลิกว่าจ้างพนักงาน (346852)

ลำดับงานไม่ล้มเหลวอีกต่อไป ซึ่งขึ้นอยู่กับนิติบุคคลที่ผู้จัดการลงชื่อเข้าใช้

### <a name="issue-missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>ปัญหา: ข้อมูลที่ขาดหายไปใน HcmOnboardingWorkerChecklistTaskEntity (349591)

การนำออกใช้นี้ประกอบด้วยข้อมูลเพิ่มเติมใน **HcmOnboardingWorkerChecklistTaskEntity** ยกตัวอย่างเช่น

- **ชื่อกลุ่ม** เมื่อชนิดที่กำหนดคือ **กลุ่ม**
- **ชื่อพนักงาน** เมื่อชนิดที่กำหนดคือ **พนักงาน**
- **ชื่อผู้จัดการ** เมื่อชนิดที่กำหนดคือ **ผู้จัดการ**

### <a name="issue-entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>ปัญหา: ไม่แสดงรายการเอนทิตีตามลำดับตัวอักษรในการจัดการ Common Data Service (377414)

ขณะนี้มีการแสดงรายการเอนทิตีตามลำดับตัวอักษรในหน้า **การจัดการ CDS**

### <a name="issue-changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>ปัญหา: การเปลี่ยนชนิดการจ้างงานที่มีวันที่ในอนาคตไม่อนุญาตให้มีการกำหนดตำแหน่งงาน (339958)

การเปลี่ยนแปลงนี้จะอนุญาตให้มีการกำหนดตำแหน่ง เมื่อมีการเปลี่ยนแปลงชนิดผู้ปฏิบัติงาน (ตัวอย่างเช่น จากพนักงานเป็นผู้รับเหมา)

### <a name="issue-updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>ปัญหา: การอัพเดต Common Data Service เอนทิตีธุรกรรมการออกจากธนาคารจะสร้างเรกคอร์ดใหม่ใน Talent (352938)

ขณะนี้มีการอัพเดตธุรกรรมการลางาน เมื่อทำการอัพเดตไปยัง Common Data Service สำหรับธุรกรรมการออกจากธนาคาร

### <a name="issue-the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>ปัญหา: ชื่อเรื่องของเอกสารแนบสำหรับรายการความคิดเห็นแสดงคำอธิบายความคิดเห็น (343765)

คำอธิบายความคิดเห็นจะไม่ปรากฏในชื่อไฟล์แนบอีกต่อไป

### <a name="issue-compensation-workflow-comments-field-shows-incorrect-content-339297"></a>ปัญหา: ฟิลด์ข้อคิดเห็นเกี่ยวกับลำดับงานค่าตอบแทนแสดงเนื้อหาที่ไม่ถูกต้อง (339297)

การเปลี่ยนแปลงนี้แสดงเนื้อหาของฟิลด์ **%HcmActionState.HcmWorkerActionComment.Comments%**

### <a name="issue-workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>ปัญหา: WorkCalendarEntity และ WorkCalendarDayEntity ไม่ได้เปิดเผยผ่าน OData (376329)

ในการนำออกใช้นี้ **WorkCalendarEntity** และ **WorkCalendarDayEntity** พร้อมใช้งานในขณะนี้ผ่าน Open Data Protocol (OData)

### <a name="issue-hcmworkerentity-is-slow-when-odata-is-used-375221"></a>ปัญหา: HCMWorkerEntity จะช้า เมื่อมีการใช้ OData (375221)

การเปลี่ยนแปลงจะปรับปรุงประสิทธิภาพการทำงานของ **HCMWorkerEntity** เมื่อมีการใช้ตัวออกแบบสมุดงาน Microsoft Excel

### <a name="issue-manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>ปัญหา: รายการสมุดรายวันประสิทธิภาพการทำงานของผู้จัดการแสดงข้อผิดพลาด หลังจากการลบสมุดรายวันประสิทธิภาพและการสร้างสมุดรายวันใหม่ (336061)

การนำออกใช้นี้แก้ไขปัญหาที่เกิดขึ้นหลังจากที่มีการลบสมุดรายวันประสิทธิภาพหนึ่งรายการ และมีการสร้างสมุดรายวันใหม่ทันทีหลังจากนั้น การแก้ไขนี้จะเปลี่ยนพฤติกรรมในบริการตนเองของผู้จัดการ

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="print-performance-reviews"></a>พิมพ์การตรวจทานประสิทธิภาพ

ให้ดูที่ [พิมพ์การตรวจทานประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2
