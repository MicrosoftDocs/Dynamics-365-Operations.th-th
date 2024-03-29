---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (28 พฤษภาคม 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 28 พฤษภาคม 2020
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42cb9e595c2997f17f487c31f674d1c099a3c80d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902974"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (28 พฤษภาคม 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3287 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>เอนทิตี LeaveRequest ไม่ทำงาน เมื่อคุณเปิดใช้งานหลายชนิดต่อแผนการลางาน (447498)

เมื่อมีการเปลี่ยนแปลงนี้ ขณะนี้ **LeaveEnrollmentV2Entity** พร้อมใช้งานเมื่อต้องการแก้ไขข้อผิดพลาดที่เกิดขึ้น เมื่อคุณเปิดใช้งานชนิดการลางานหลายรายการ

## <a name="batch-contention-reduction-feature-preview-446619"></a>ลักษณะการทำงานของการลดการขัดแย้งของชุดงาน (ตัวอย่าง) (446619)

เมื่อคุณเปิดใช้งานลักษณะการทำงานนี้ คุณสามารถคาดการณ์การลดในการบล็อคในตารางกรอบงานชุดงานได้ ในขณะที่เลือกงานและทำงานให้เสร็จสิ้น

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict ขณะบันทึก ผู้ปฏิบัติงานป้องกันการแก้ไขเรกคอร์ดในบุคคล (427915)

การเปลี่ยนแปลงนี้จะแก้ไขข้อผิดพลา เมื่อเพิ่มผู้ปฏิบัติงานใหม่ การอัปเดตข้อมูลที่อยู่ และการเปลี่ยนแปลงการตั้งค่าภาษา ในสถานการณ์จำลองที่ไม่ซ้ำกันนี้ ข้อผิดพลาดที่แสดงบ่งชี้ว่าเรกคอร์ดไม่สามารถอัปเดตได้ 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>ไม่สามารถเพิ่มเอกสารแนบให้คำขอการลางานที่ได้รับอนุมัติส่งได้อีกครั้ง (425407)

การเปลี่ยนแปลงนี้จะอนุญาตให้มีเอกสารแนบเพื่ออนุมัติคำขอลางานแล้ว

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>ผู้ใช้สามารถป้อนค่าตอบแทนสำหรับพนักงานในฟอร์มนิติบุคคลอื่น (409529)

การเปลี่ยนแปลงนี้ปิดใช้งานตัวเลือกค่าตอบแทน เพื่อป้องกันไม่ให้มีการป้อนข้อมูลค่าตอบแทนโดยไม่ได้ตั้งใจสำหรับนิติบุคคลที่ไม่ถูกต้อง

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>เกิดข้อผิดพลาดเมื่อคุณโอนย้ายพนักงาน และวันที่กำหนดตำแหน่งของผู้ปฏิบัติงานอยู่ก่อนช่วงเวลาของตำแหน่งงาน (429402)

ข้อความแสดงข้อผิดพลาด เมื่อการโอนย้ายพนักงานในสถานการณ์นี้ได้รับการอัปเดตเพื่ออธิบายถึงการเปลี่ยนแปลงที่จำเป็นในการแก้ไขปัญหาให้ดีขึ้น

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>ความสามารถของเอกสารแนบในการลงทะเบียนสวัสดิการการบริการตนเองของพนักงาน
 
ขณะนี้คุณสามารถเพิ่มเอกสารแนบระหว่างกระบวนการลงทะเบียนสวัสดิการ สำหรับแต่ละแผนงานที่มีการลงทะเบียนของพนักงาน คุณสามารถดูเอกสารแนบภายในฟอร์ม **สวัสดิการของผู้ปฏิบัติงานลงทะเบียนไว้**

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

## <a name="human-resources-application-in-teams"></a>โปรแกรมประบุกต์ Human Resources ใน Teams

พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](./hr-admin-teams-leave-app.md) 

## <a name="leave-suspension"></a>การระงับการลางาน

คุณสามารถระงับการลางานและการขาดงานในทรัพยากรบุคคลสำหรับพนักงาน การระงับการลางานจะหยุดการรับรู้การลางานสำหรับชนิดการลางานที่เลือก ถ้าการระงับเกิดขึ้นหลังจากที่มีการประมวลผลการรับรู้ การระงับการลางานจะสร้างการปรับปรุงตามสัดส่วนให้กับยอดดุลการลางานของพนักงาน สำหรับข้อมูลเพิ่มเติม โปรดดู [ระงับการลางาน](hr-leave-and-absence-suspend-leave.md)

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>อัปเดตประสบการณ์ผู้ใช้เพื่อบ่งชี้ว่ารายการคงค้างถูกระงับแล้ว (429550)

ประสบการณ์ผู้ใช้บ่งชี้ว่าการคงค้างถูกระงับสำหรับแผนแล้ว

## <a name="coming-soon"></a>เร็วๆ นี้

## <a name="database-logging-in-preview-in-june"></a>การบันทึกฐานข้อมูล (ในการแสดงตัวอย่างในเดือนมิถุนายน)

ลักษณะการทำงานการบันทึกฐานข้อมูลจะช่วยให้คุณสามารถกำหนดตารางและฟิลด์ที่ควรตรวจสอบได้ นอกจากนี้ยังช่วยให้คุณสามารถกำหนดเหตุการณ์ที่ควรทริกเกอร์การติดตามการเปลี่ยนแปลง ความสามารถในการสอบถามจะพร้อมใช้งานเพื่อดูการเปลี่ยนแปลงเหล่านี้เมื่อเวลาผ่านไป

## <a name="buy-and-sell-leave-in-preview-june-1"></a>การซื้อและการขายการลางาน (ในการแสดงตัวอย่างวันที่ 1มิถุนายน)

บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้ กระบวนการนี้มักจะมีการจัดการด้วยตนเอง ลักษณะการทำงานนี้จะช่วยให้คุณสามารถจัดการนโยบายและคำร้องขอแผนก HR โดยอัตโนมัติได้มากขึ้น และจะช่วยลดข้อผิดพลาด ขณะดำเนินการจัดการลางาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [จัดการนโยบายซื้อและขายวันลางาน](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [ซื้อและขายวันลางาน](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ
 
เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้ เอนทิตี DMF อนุญาตการนำเข้าและส่งออกข้อมูล เพื่อตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล แม่แบบส่งออกและนำเข้าข้อมูลในลักษณะตามลำดับตามการอ้างอิงข้อมูล

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>เพิ่มรหัสเหตุผลให้กับการระงับการคงค้าง (วันที่ 1 มิถุนายน)

รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง

## <a name="carry-forward-rules-june-1"></a>กฎการยกยอดดุล (วันที่ 1 มิถุนายน)

คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ (วันที่ 1 มิถุนายน)

ในรุ่นนี้ HR สามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ยังไม่ได้ชำระเงิน การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง (วันที่ 1 มิถุนายน)

ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]