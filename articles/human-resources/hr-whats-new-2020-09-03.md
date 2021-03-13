---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (03 กันยายน 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 3 กันยายน 2020
author: andreabichsel
manager: tfehr
ms.date: 09/03/2020
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
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41763a8817d0c39b14284a247cf3e46678e7811b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130868"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (3 กันยายน 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3504 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุน Lifecycle Services (LCS) สำหรับการอ้างอิง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะที่กำลังจะเกิดขึ้นใน Human Resources ดูที่ [ภาพรวมของ Dynamics 365 Human Resources 2019 เวฟการนำออกใช้ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการอัปเดตสำหรับ Human Resources ให้ดูที่ [กระบวนการอัปเดต](hr-admin-setup-update-process.md)

## <a name="in-this-release"></a>ในการเผยแพร่นี้

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>ตารางมิติทางการเงินเริ่มต้นและรูปแบบกล่องโต้ตอบใหม่ใน Human Resources (469495)

ขณะนี้รูปแบบใหม่สำหรับมิติทางการเงินจะพร้อมใช้งานในส่วนต่อไปนี้:

- กำหนดตำแหน่งการดำเนินการ (แบบฟอร์ม: **HcmPositionActionDetail**)
- รหัสรายได้ค่าจ้าง (แบบฟอร์ม: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>รายการไม่ปรากฏในปฏิทินการลางานของบริษัทถ้าไม่ได้เปิดใช้งานการปรับปรุงปฏิทินการลางานและการขาดงาน (484406)

การเผยแพร่นี้แก้ไขปัญหาที่ไม่มีการแสดงรายการลางานในปฏิทินการลางานของบริษัท ปัญหานี้จะเกิดขึ้นเฉพาะเมื่อไม่ได้เปิดใช้งานตัวเลือก **การปรับปรุงปฏิทินการลางงานและการขาดงาน** ของการจัดการคุณลักษณะ

### <a name="benefitplanemployeeentity-issue-467597"></a>ปัญหา BenefitPlanEmployeeEntity (467597)

การเผยแพร่นี้จะแก้ไขปัญหาที่เกิดขึ้นกับเอนทิตี้ **BenefitsPlanEmployee** เมื่อมีการนำเข้าการลงทะเบียนของผู้ปฏิบัติงาน **รหัสความคุ้มครอง** และ **รหัสชนิดของแผน** มีการตั้งค่าอย่างถูกต้อง ปัญหานี้ทำให้แผนสวัสดิการของพนักงานแสดงอย่างไม่ถูกต้องในแบบฟอร์ม **แผนสวัสดิการของผู้ปฏิบัติงาน** และแบบฟอร์ม **การลงทะเบียนที่เปิด** ในระบบบริการตนเองของพนักงาน

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>ผลลัพธ์ของไฟล์อิเล็กทรอนิกส์ 1094-C ไม่มีตัวอักษรใน XML (435190)

การเปลี่ยนแปลงนี้แก้ไขปัญหาที่เกิดขึ้นกับไฟล์เอาต์พุต1094-C ไม่มีอักขระที่จำเป็นเมื่อส่งไปที่ IRS

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>ตารางค่าตอบแทนผันแปรของพนักงานที่แม็ปกับแบบฟอร์มค่าตอบแทนคงที่ (476117)

การเปลี่ยนแปลงนี้จัดตำแหน่งฟิลด์ค่าตอบแทนคงที่ให้สอดคล้องกับแบบฟอร์มค่าตอบแทนคงที่ ขณะนี้ฟิลด์ค่าตอบแทนผันแปรสามารถใช้งานกับแบบฟอร์มค่าตอบแทนผันแปรเท่านั้น

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>อนุญาตให้มีการร้องขอการลางานก่อนการลงทะเบียนถ้าชนิดการลางานนั้นมียอดคงเหลือต่ำสุดเป็นค่าลบ (469917)

การเปลี่ยนแปลงนี้ไม่อนุญาตให้ป้อนการร้องขอการลางานก่อนที่จะลงทะเบียนในแผน ถึงแม้ว่าการลงทะเบียนจะมียอดคงเหลือต่ำสุดที่เป็นค่าลบ คุณสามารถป้อนหรือส่งคำขอได้เฉพาะเมื่อแผนเปิดใช้งานอยู่เท่านั้น

### <a name="document-templates-dont-download-457279"></a>เท็มเพลตเอกสารไม่ดาวน์โหลด (457279)

เมื่อคุณทำการเปลี่ยนแปลงนี้ คุณสามารถดาวน์โหลดเท็มเพลตเอกสารทั้งหมดได้แล้ว 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>ข้อมูลจะแสดงเป็นส่วนหัวของคอลัมน์แทนแถวสำหรับฟิลด์อัตราการชำระค่าจ้างในรายงานแผนค่าตอบแทน (476077)

รายงานการวิเคราะห์จะแสดงข้อมูลที่ถูกต้องสำหรับ **อัตราการชำระค่าจ้าง**

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

### <a name="human-resources-application-in-teams"></a>โปรแกรมประบุกต์ Human Resources ใน Teams

พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 

- [การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 1
- [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841) ในคู่มือ Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>คุณลักษณะรุ่นพรีวิวของแอป Human Resources ใน Teams
 
-  **การแจ้งเตือน**: ผู้ส่งและผู้อนุมัติที่ส่งคำขอการลาหยุดจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams ผู้อนุมัติจะสามารถอนุมัติหรือปฏิเสธคำขอการลาหยุดได้ ผู้ส่งจะได้รับการแจ้งเตือนถ้าคำขอได้รับการอนุมัติหรือถูกปฏิเสธ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 
   - [การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2
   - [เปิดใช้งานการแจ้งเตือนสำหรับแอป Human Resources ใน Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) ในคู่มือ Human Resources
   - [เปิดหรือปิดการแจ้งเตือนของ Teams สำหรับผู้ใช้แต่ละราย](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) ในคู่มือ Human Resources
   - [การแจ้งเตือนของ Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) ในคู่มือ Human Resources
   - [ดูปฏิทินการลางานของทีมของคุณ](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) ในคู่มือ Human Resources
 
- **ปฏิทินการลาหยุดของผู้จัดการ**: ผู้จัดการจะสามารถดูการลาหยุดที่อนุมัติและที่ค้างอยู่สำหรับผู้ใต้บังคับบัญชาโดยตรงของตนในมุมมองปฏิทิน มุมมองนี้จะทำให้เข้าใจง่ายเมื่อสมาชิกในทีมของตนไม่มาทำงาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ 
   - [การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2
   - [ดูปฏิทินการลางานของทีมของคุณ](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) ในคู่มือ Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>ตัวเลือกการตั้งค่าคอนฟิกเพื่อกำหนดตำแหน่งรายการงานที่กำหนดให้กับฉัน (477004)

ขณะนี้ตัวเลือกใหม่จะพร้อมใช้งานในการกำหนดตำแหน่งรายการของ **รายการงานที่กำหนดให้กับฉัน** ในคอลัมน์ทางด้านขวาของแดชบอร์ด เมื่อมีการเปลี่ยนแปลงนี้ รายการงานและรายการสิ่งที่ต้องทำทั้งหมดแสดงในพื้นที่เดียวกัน เปิดใช้งานฟังก์ชันนี้โดยการเปิด **พรีวิว - การปรับปรุงประสบการณ์ของลำดับงาน** ในการจัดการคุณลักษณะ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดคุณลักษณะพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)

คุณลักษณะนี้จะส่งเสริมตัวเลือกลำดับงานที่จะปรากฏในแบบฟอร์มการดำเนินการด้านบุคลากร ตัวเลือกลำดับงานจะปรากฎในแท็บด่วนการดำเนินการเพื่อให้สามารถเข้าถึงได้อย่างรวดเร็ว สำหรับข้อมูลเพิ่มเติม ให้ดูที่  

- [การปรับปรุงประสบการณ์การใช้งานลำดับงานการจัดการองค์กรและบุคลากร](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) ในแผน Dynamics 365 2020 การนำออกใช้เวฟ 2

![รายการงานที่กำหนดให้กับฉัน](./media/hr-workflow-work-items-assigned-to-me.png)

![การเข้าถึงด่วนของรายการลำดับงาน](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="checklist-entities-included-in-dataverse"></a>เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Dataverse

เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Dataverse

### <a name="benefits-management-reason-codes"></a>รหัสเหตุผลของการจัดการสวัสดิการ

รหัสเหตุผลของการจัดการสวัสดิการจะมีการรวมเข้ากับรหัสเหตุผลที่มีอยู่ใน Human Resources ในเร็วๆ นี้ ถ้าคุณสร้างรหัสเหตุผลไว้ในการจัดการสวัสดิการที่มีอักขระเกินกว่า 15 ตัว คุณต้องเปลี่ยนชื่อของรหัสเหตุผลในแบบฟอร์ม **รหัสเหตุผล** ของการจัดการสวัสดิการเป็นอักขระ15 ตัวหรือน้อยกว่า หลังจากที่คุณอัปเดตชื่อ รหัสเหตุผลจะปรากฏขึ้นภายใต้แบบฟอร์มรหัสเหตุผลที่มีอยู่ในการจัดการบุคลากร การเปลี่ยนแปลงนี้จะพร้อมใช้งานในอนาคตและจะไม่มีผลกระทบต่อฟังก์ชันการทำงานที่มีอยู่

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)
