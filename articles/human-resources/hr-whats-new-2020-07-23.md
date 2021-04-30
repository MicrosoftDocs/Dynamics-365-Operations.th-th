---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (23 กรกฎาคม 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 23 กรกฏาคม 2020
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb4ef2bf335e19d0d890465c851c46f66ef8bd8e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891876"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (23 กรกฎาคม 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3416 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>การลบมิติทางการเงินในตำแหน่งไม่ทำงานตามที่คาดไว้ (445476)

การลบมิติออกจากตำแหน่งลบตำแหน่งเดียวกันเหล่านั้นออกจาก Dataverse ด้วย

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>ตำแหน่งงานที่ไม่ได้อยู่ในลำดับชั้นแสดงตำแหน่งงานที่ไม่ได้ใช้งาน (397257)

ตำแหน่งที่ไม่ได้ใช้งานอยู่ (มีระยะเวลาหมดอายุ) ไม่แสดงลำดับชั้นของตำแหน่งเป็น **ตำแหน่งที่ไม่ได้อยู่ในลำดับชั้น** 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>การตรวจสอบความถูกต้องที่เกิดขึ้นระหว่าง LeaveEnrollmentEntity และ HcmWorkerEntity ในการนำเข้ากรอบงานการจัดการข้อมูล (DMF) ทำให้เกิดการโหลดข้อมูลที่ช้าลง (442324)

การเปลี่ยนแปลงในรุ่นนี้เพิ่มประสิทธิภาพการทำงานของ **LeaveEnrollmentEntity**

## <a name="unable-to-personalize-in-organization-administration-447490"></a>ไม่สามารถตั้งค่าส่วนบุคคลในการบริหารองค์กร (447490)

ด้วยการเปลี่ยนแปลงนี้คุณสามารถกำหนดลิงค์ให้กับการ **การจัดการองค์กร**

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

## <a name="mandatory-fields"></a>ฟิลด์บังคับ 

ขณะนี้คุณสามารถทำให้ฟิลด์บังคับโดยใช้ความสามารถในการตั้งค่าส่วนบุคคลของทรัพยากรบุคคล ลักษณะการทำงานนี้จำเป็นต้องใช้ **มุมมองที่บันทึกไว้**

## <a name="human-resources-application-in-teams"></a>โปรแกรมประบุกต์ Human Resources ใน Teams

พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](./hr-admin-teams-leave-app.md) 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ
 
เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้ เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล

## <a name="buy-and-sell-leave"></a>ซื้อและขายวันลางาน 

บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้ กระบวนการนี้มักจะมีการจัดการด้วยตนเอง คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [จัดการนโยบายซื้อและขายวันลางาน](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [ซื้อและขายวันลางาน](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว

ลูกค้าสามารถประมวลผลการรับรู้สำหรับบริษัทเดียวหรือแผนการลางานและการขาดงานเดียว ความสามารถนี้จะให้ความชัดเจนสำหรับกระบวนการรับรู้สำหรับลูกค้าที่มีปีของการลางานหรือนโยบายการรับรู้การลางานที่แตกต่างกัน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรับรู้การลางานสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน](hr-leave-and-absence-accrue.md)

## <a name="add-attachments-to-time-off-requests"></a>เพิ่มเอกสารแนบไปยังคำขอเวลาหยุดพัก

ความสามารถในการเพิ่มเอกสารแนบไปยังคำขอลางานที่ได้รับการอนุมัติ เป็นสิ่งสำคัญในสภาพแวดล้อม COVID-19 ปัจจุบัน ขณะนี้พนักงานสามารถเพิ่มเอกสารแนบเหล่านี้ได้ นอกจากนี้ ยังมีข้อมูลเชิงลึกเพิ่มเติมเกี่ยวกับวิธีการที่จะทำการปรับปรุงไปยังคำขอลางาน สำหรับข้อมูลเพิ่มเติม ให้ดู [เพิ่มเอกสารแนบไปยังคำขอที่มีอยู่](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)

## <a name="add-reason-code-to-accrual-suspensions"></a>เพิ่มรหัสเหตุผลไปยังการระงับการคงค้าง 

รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง

## <a name="carry-forward-rules"></a>กฎการยกยอดไป 

คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ

คุณสามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ไม่ได้รับชำระเงิน การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้

## <a name="dmf-entity-available-for-accrual-suspensions"></a>เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง 

ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง

## <a name="coming-soon"></a>เร็วๆ นี้

## <a name="checklist-entities-included-in-dataverse"></a>เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Dataverse

เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Dataverse

## <a name="platform-changes"></a>การเปลี่ยนแปลงแพลตฟอร์ม

Platform Update 10.0.12 (36)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]