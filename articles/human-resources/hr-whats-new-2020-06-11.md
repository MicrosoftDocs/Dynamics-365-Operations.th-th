---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (11 มิถุนายน 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 11 มิถุนายน 2020
author: andreabichsel
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ff359f65afc03a1b5691fddc078f73682e99e44
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127812"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 Human Resources (11 มิถุนายน 2020)

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3316 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>บางครั้งฟอร์มพนักงานที่มีประสิทธิภาพทำให้ปุ่มปิด (X) ของฟอร์มรองหยุดทำงาน (442369)

เมื่อมีการเปิดใช้งานฟอร์ม **ผู้ปฏิบัติงาน** ใหม่ ปุ่มปิด (**X**) บางครั้งไม่ทำงานบนฟอร์มรอง ปัญหานี้ไม่ต่อเนื่อง คุณสามารถปิดฟอร์มได้ หลังจากที่ปล่อยและกลับมา ตัวอย่างเช่น คุณสามารถเลือกรายการเมนูทางด้านซ้าย และนำทางกลับไปยังฟอร์ม **ผู้ปฏิบัติงาน** และจากนั้นปิด การนำออกใช้ของสัปดาห์นี้แก้ไขปัญหานี้ 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>เอนทิตีผู้ติดต่อส่วนบุคคลของผู้ปฏิบัติงานไม่ส่งออกผู้ติดต่อส่วนบุคคลที่มีชนิดความสัมพันธ์หลัก

ด้วยการนำออกใช้นี้ เอนทิตี **ผู้ติดต่อส่วนบุคคลของผู้ปฏิบัติงาน** จะส่งออกชนิดความสัมพันธ์ทั้งหมด

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity ควรเป็นส่วนหนึ่งของแพคเกจการรวมค่าจ้าง Ceridian ตามค่าเริ่มต้น (448506)

ด้วยการเปลี่ยนแปลงนี้ **HcmPositionWorkerAssignmentV2Entity** จะรวมอยู่ในแพคเกจการรวมค่าจ้าง Ceridian

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

## <a name="database-logging"></a>การล็อกฐานข้อมูล

คุณลักษณะการบันทึกฐานข้อมูลจะช่วยให้คุณสามารถกำหนดตารางและฟิลด์ที่จะตรวจสอบได้ นอกจากนี้ยังช่วยให้คุณสามารถกำหนดเหตุการณ์ที่ควรทริกเกอร์การติดตามการเปลี่ยนแปลง คุณสามารถใช้ความสามารถในการบันทึกฐานข้อมูลเพื่อดูการเปลี่ยนแปลงเหล่านี้เมื่อเวลาผ่านไป สำหรับข้อมูลเพิ่มเติมให้ ดูที่ [ตั้งค่าคอนฟิกและจัดการการบันทึกฐานข้อมูล](hr-admin-database-logging.md)

## <a name="human-resources-application-in-teams"></a>โปรแกรมประบุกต์ Human Resources ใน Teams

พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841) 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ
 
เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้ เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล

## <a name="buy-and-sell-leave"></a>ซื้อและขายวันลางาน 

บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้ กระบวนการนี้มักจะมีการจัดการด้วยตนเอง คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [จัดการนโยบายซื้อและขายวันลางาน](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [ซื้อและขายวันลางาน](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว

ลูกค้าสามารถประมวลผลการรับรู้สำหรับบริษัทเดียวหรือแผนการลางานและการขาดงานเดียว ความสามารถนี้จะให้ความชัดเจนแก่กระบวนการรับรู้สำหรับลูกค้าที่มีปีของการลางานหรือนโยบายการรับรู้การลางานที่แตกต่างกัน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรับรู้การลางานสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน](hr-leave-and-absence-accrue.md)

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

## <a name="new-platform-capabilities"></a>ความสามารถของแพลตฟอร์มใหม่ 

คุณจะสามารถทำให้ฟิลด์เป็นแบบบังคับโดยใช้การตั้งค่าส่วนบุคคลได้ คุณลักษณะนี้จะกำหนดให้คุณเปิดใช้งาน **มุมมองที่บันทึกไว้**

## <a name="configure-the-name-of-employee-self-service"></a>ตั้งค่าคอนฟิกชื่อของระบบบริการตนเองของพนักงาน

ตัวเลือกใหม่จะพร้อมใช้งานในพารามิเตอร์ทรัพยากรบุคคลเพื่อปรับปรุงชื่อของพื้นที่ทำงานแบบบริการตนเองของพนักงานเป็นบริการตนเอง 

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)