---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (06 สิงหาคม 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 6 สิงหาคม 2020
author: andreabichsel
manager: tfehr
ms.date: 08/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 235af2d4d10687e9d7d7676c29c95428eab99b0a
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467734"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (06 สิงหาคม 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3444 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง

## <a name="platform-update-1001236-is-now-available"></a>Platform update 10.0.12(36) พร้อมใช้งานแล้วในขณะนี้

เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูที่ [Platform update สำหรับรุ่น10.0.12 ของแอป Finance and Operations (สิงหาคม 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ
 
เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้ เอนทิตี DMF อนุญาตให้คุณสามารถนำเข้าและส่งออกข้อมูลเพื่อให้ตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล แม่แบบส่งออกและนำเข้าข้อมูลตามลำดับตามการอ้างอิงข้อมูล สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [การสนับสนุนเอนทิตี้ DMF](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 1
- [ภาพรวมของการจัดการข้อมูล](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire สร้างลำดับงานสำหรับคำขอการซื้อและการขายวันลา (446557)

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [อนุญาตให้พนักงานซื้อและขายวันลา](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2
- [จัดการนโยบายซื้อและขายวันลางาน](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [ซื้อและขายวันลางาน](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>เอนทิตี้ที่อยู่ไปรษณีย์ของผู้ปฏิบัติงาน V2 มีสิทธิ์เข้าถึงในนิติบุคคลที่มีการจำกัดการเข้าถึง (459126)

เมื่อมีการเปลี่ยนแปลงนี้ เอนทิตี้ **ที่อยู่ไปรษณีย์ของผู้ปฏิบัติงาน V2** จะจำกัดตามการเข้าถึงนิติบุคคลที่กำหนดให้กับผู้ใช้

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>ไฮเปอร์ลิงก์อีเมล์ของลำดับงานไม่สามารถเปิดการทบทวนที่เกี่ยวข้อง (437398)

เมื่อคุณใช้ตัวยึดตำแหน่งเพื่อเปิดการทบทวนประสิทธิภาพในลำดับงานการทบทวน ไฮเปอร์ลิงก์ที่สร้างขึ้นในอีเมลจะเปิดเรกคอร์ดที่เลือกในขณะนี้

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>เอนทิตี้ใหม่สำหรับการซื้อและการขายวันลา (473180)

ขณะนี้มีเอนทิตี้กรอบงานการจัดการข้อมูลสามารถใช้งานสำหรับการซื้อและการขายวันลาได้แล้ว สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการข้อมูล](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>เมื่อดูข้อมูลเรกคอร์ดและการใช้ตัวกรองขั้นสูง ผู้ใช้สามารถเข้าถึงเรกคอร์ดของพนักงานรายอื่น (472490)

ด้วยการเปลี่ยนแปลงนี้ ผู้ใช้ระบบบริการตนเองของพนักงานสามารถเข้าถึงได้เฉพาะเรกคอร์ดของตนเท่านั้นในขณะที่ใช้ระบบบริการตนเองของพนักงาน การดูข้อมูลเรกคอร์ดในขณะที่การเปลี่ยนแปลงตัวเลือกการกรองจะไม่แสดงข้อมูลเพิ่มเติมอีกต่อไป

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>การวิเคราะห์การจัดการบุคลากรมีเรกคอร์ดผู้ปฏิบัติงานที่ออกไปแล้ว (382893)

ในรุ่นนี้ การวิเคราะห์การจัดการบุคลากรจะมีเฉพาะผู้ปฏิบัติงานที่ใช้งานอยู่เท่านั้น 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>ไม่สามารถประมวลผลการขึ้นค่าตอบแทนตามผลงานของพนักงาน (473125)

การเปลี่ยนแปลงนี้จะช่วยให้คุณสามารถป้อนการขึ้นค่าตอบแทนตามผลงานเมื่อคุณเปลี่ยนแปลงวันที่มีผลบังคับใช้สำหรับการขึ้นค่าตอบแทนตามผลงานใหม่

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>ลำดับงานการทบทวนสามารถเริ่มต้นได้มากกว่าหนึ่งครั้ง (467541)

เมื่อมีการเปลี่ยนแปลงนี้ คุณจะสามารถเริ่มต้นลำดับงานการทบทวนประสิทธิภาพได้เพียงครั้งเดียว สถานะสำหรับผู้จัดการไม่แสดงตัวเลือกในการเริ่มต้นการทบทวนอีกต่อไป

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>ลำดับงานการขอลางานจบลงด้วยข้อผิดพลาดเมื่อยกเลิกคำขอลางานที่อนุมัติ (472063)

ในรุ่นนี้ เมื่อคุณยกเลิกคำขอลางานที่อนุมัติ สถานะของคำขอจะไม่ยังคงเป็นอนุมัติอีกต่อไป และลำดับงานจะดำเนินการต่อไป

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>ระบบจะแนะนำผู้ปฏิบัติงานที่ออกไปแล้วเมื่อสร้างการทบทวนใหม่จากเท็มเพลต (460624)

เมื่อมีการเปลี่ยนแปลงนี้ ผู้ปฏิบัติงานที่ออกจากงานจะไม่มีอยู่อีกต่อไปเมื่อสร้างการทบทวนใหม่จากเท็มเพลต คุณไม่สามารถสร้างการทบทวนสำหรับพนักงานที่อยู่นอกวันที่ของการจ้างงานได้

## <a name="position-hierarchy-circular-reference-detection-415879"></a>การตรวจสอบการอ้างอิงหมุนเวียนในลำดับชั้นของตำแหน่ง (415879)

ด้วยการเปลี่ยนแปลงนี้ การตรวจสอบการอ้างอิงหมุนเวียนในลำดับชั้นของตำแหน่งถูกจำกัดไว้ที่จุดในเวลาเดียว คุณสามารถดำเนินการตรวจสอบการอ้างอิงแบบหมุนเวียนสำหรับวันที่ต่างๆ เพื่อตรวจสอบว่าโครงสร้างการรายงานไม่มีการอ้างอิงแบบหมุนเวียนใดๆ

## <a name="buy-and-sell-leave"></a>ซื้อและขายวันลางาน 

บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้ กระบวนการนี้มักจะมีการจัดการด้วยตนเอง คุณลักษณะนี้จะทำให้การจัดการนโยบายและการร้องขอสำหรับแผนก HR เป็นอัตโนมัติ ซึ่งช่วยลดขั้นตอนซ้ำซ้อนของกระบวนการการจัดการลางาน และช่วยกำจัดข้อผิดพลาด สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [อนุญาตให้พนักงานซื้อและขายวันลา](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2
- [จัดการนโยบายซื้อและขายวันลางาน](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [ซื้อและขายวันลางาน](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

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

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

### <a name="mandatory-fields"></a>ฟิลด์บังคับ

คุณสามารถทำให้ฟิลด์บังคับโดยใช้ความสามารถในการตั้งค่าส่วนบุคคลของทรัพยากรบุคคล ลักษณะการทำงานนี้จำเป็นต้องใช้ **มุมมองที่บันทึกไว้** สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมุมมองที่บันทึกไว้ ให้ดูที่:

- [มุมมองที่บันทึกไว้ - มีความพร้อมใช้งานทั่วไป](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2
- [สร้างแบบฟอร์มที่ใช้มุมมองที่บันทึกไว้ทั้งหมด](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>โปรแกรมประบุกต์ Human Resources ใน Teams

พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 1
- [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง

ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง

## <a name="coming-soon"></a>เร็วๆ นี้

## <a name="checklist-entities-included-in-dataverse"></a>เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Dataverse

เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Dataverse

## <a name="known-issues"></a>ปัญหาที่ทราบ

พื้นที่ทำงาน **การจัดการคุณลักษณะ** อาจแสดงคุณลักษณะที่ถูกปิดใช้งานจากการเป็นคุณลักษณะรุ่นพรีวิวเมื่อมีความพร้อมใช้งานทั่วไป ด้านล่างนี้เป็นรายการของคุณลักษณะที่พร้อมใช้งานโดยทั่วไปที่แสดงสถานะที่ไม่ถูกต้อง 

1.  การจัดการสวัสดิการ
2.  การจัดการกรณี
3.  การลงบันทึกฐานข้อมูล (การตรวจสอบ)
4.  การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว
5.  การระงับการยกยอดวันลาและขาดงาน
6.  รหัสเหตุผลการปรับปรุงยอดคงเหลือและความคิดเห็น
7.  ซื้อและขายวันลางาน
8.  ปฏิทินการลางานและการขาดงาน
9.  กฎการยกยอดไปของการลางาน
10. การตรวจสอบการลางานคงค้าง
11. การลบการลางานคงค้าง
12. การปัดเศษการลางานคงค้าง
13. ตั้งค่าคอนฟิกชนิดการลางานหลายรายการแผนการลางานเดียว
14. อัพเดตการปรับปรุงเวลาหยุดพัก
15. ใช้ FTE ของพนักงานสำหรับรายการคงค้าง
16. มุมมองค่าตอบแทนข้ามบริษัท
17. พิมพ์การตรวจทานประสิทธิภาพ
18. การแก้ไขวันหยุดคงค้างของการลางาน

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]