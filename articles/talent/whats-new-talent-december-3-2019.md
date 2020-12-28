---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (3 ธันวาคม 2019)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
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
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528704"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (3 ธันวาคม 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2646 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

### <a name="feature-management-workspace"></a>พื้นที่ทำงานการจัดการคุณลักษณะ

พื้นที่ **การจัดการลักษณะการทำงาน** แสดงรายการของลักษณะการทำงานที่จัดส่งในแต่ละรุ่น ตามค่าเริ่มต้น คุณลักษณะใหม่จะถูกปิด คุณสามารถใช้พื้นที่ทำงานเพื่อเปิดและดูเอกสารประกอบได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการคุณลักษณะ ดูที่ [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)

ลักษณะการทำงานใหม่ทั้งหมดยังคงอยู่ในการแสดงตัวอย่างอย่างน้อย 30 วัน และโดยปกติจะคงอยู่ 30-60 วัน ลักษณะการทำงานที่สำคัญโดยทั่วไปจะมีอยู่ในเดือนตุลาคมและเดือนเมษายนของแต่ละปีตามรอบระยะเวลาการแสดงตัวอย่าง ทันทีที่คุณเห็นความสามารถใหม่ในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** คุณสามารถเปิดใช้งานได้ ลักษณะการทำงานบางอย่างอาจเปิดใช้งานตามค่าเริ่มต้น
 
เมื่อเวลาผ่านไป ลักษณะการทำงานที่สำคัญจะเปิดใช้งานโดยค่าเริ่มต้นและไม่สามารถปิดได้ (ตัวอย่างเช่น พื้นที่ทำงาน **การจัดการลักษณะการทำงาน**)
 
เมื่อมีลักษณะการทำงานที่พร้อมใช้งาน โดยทั่วไปจะสามารถเปิดหรือปิดใช้งานได้ในสภาพแวดล้อมการผลิต พื้นที่ทำงาน **การจัดการลักษณะการทำงาน** บ่งชี้ว่าลักษณะการทำงานในการแสดงตัวอย่างจะกลายเป็นข้อบังคับ โดยปกติแล้ววันที่นี้จะเป็นวันที่ 1 ตุลาคม หรือ 1 เมษายน เพื่อให้สอดคล้องกับแผนการวางจำหน่ายรายย่อย คุณไม่สามารถเปิดหรือปิดคุณลักษณะบังคับได้ คุณไม่สามารถเปิดและปิดลักษณะการทำงานในสภาพแวดล้อมทั้งหมดได้จนกว่าจะเป็นข้อบังคับ

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>เพิ่มการจัดกำหนดการอัตโนมัติของการล้างข้อมูลประวัติชุดงาน (332528)

ด้วยการเปลี่ยนแปลงนี้ **ประวัติชุดงาน** เรียกใช้แต่ละคืน และลบรายการประวัติชุดงานที่เก่ากว่า 30 วัน

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent ไม่ตอบสนองในการดำเนินการของผู้ปฏิบัติงาน เมื่อความยาวของหมายเลขรหัสไม่ตรงกับชนิดของรหัส (390971)

รุ่นนี้แก้ไขปัญหาที่แสดง เมื่อความยาวของหมายเลขรหัสไม่ตรงกับข้อกำหนดภายในชนิดของรหัส 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>ค่าตอบแทนคงที่ไม่ปรับปรุงระดับด้วยการเปลี่ยนแปลงไปยังรายละเอียดตำแหน่ง (348085)

ในการนำออกใช้ของสัปดาห์นี้ **วันที่เริ่มต้นการชดเชย** กำหนดงานที่เกี่ยวข้องกับตำแหน่ง ณ เวลานั้น เมื่อสร้างเรกคอร์ดค่าตอบแทนคงที่ใหม่สำหรับพนักงาน

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>รายการของผู้ปฏิบัติงาน พนักงาน และผู้รับเหมา จะแสดงชนิดของผู้ปฏิบัติงานเป็นทั้งสองแบบ เมื่อพวกเขาควรเป็นผู้ปฏิบัติงานหรือผู้รับเหมาเท่านั้น (384473)

การเปลี่ยนแปลงนี้จะสะท้อนถึงชนิดของผู้ปฏิบัติงานที่ป้อน (ผู้รับเหมา หรือพนักงาน) อย่างถูกต้อง

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>การแจ้งเตือนทางอีเมลสำหรับการดำเนินการจ้างงานใหม่ไม่มีข้อมูลชื่อ เนื่องจากนโยบายความปลอดภัย (383402)

การเปลี่ยนแปลงนี้แก้ไขข้อมูลที่แสดงในฟิลด์ชื่อหรือนามสกุลภายในตัวยึดตำแหน่งสำหรับลำดับงาน เมื่อมีการเปิดใช้งานความปลอดภัยขั้นสูง

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>ระบบจะอนุญาตให้มีการร้องขอการลาแบบเต็มวันสองวันในวันเดียวกันได้ (379284)

ด้วยการเปลี่ยนแปลงนี้ คุณจะไม่สามารถออกการร้องขอการลางานสองรายการในวันเดียวกันได้ 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>รายการการเปลี่ยนแปลงที่อยู่ควรถูกเรียงลำดับตามวันที่มีผลบังคับใช้ (352798)

ด้วยการเปลี่ยนแปลงนี้ ในขณะนี้รายการการเปลี่ยนแปลงที่อยู่จะถูกเรียงลำดับตาม **วันที่มีผลบังคับใช้**

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>การร้องขอการลาควรอนุญาตให้ลบออกจาก Common Data Service ไปยัง Talent (376999)

ด้วยการเปลี่ยนแปลงนี้ สามารถลบการร้องขอการลางานแบบร่างและที่ยกเลิกออกจาก Common Data Service และจากนั้นจึงถูกลบออกจาก Talent

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>ลบรหัสรายได้ที่ได้รับอนุญาต เมื่อมีการกำหนดรหัสรายได้เดียวกันให้กับพนักงาน (371792)

ในรุ่นนี้ ก่อนอื่นคุณต้องลบรหัสรายได้จากพนักงาน ก่อนที่จะลบรหัสรายได้จากระบบ

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>ลำดับงานการลางานและการขาดงานที่มีขั้นตอนการอนุมัติสองขั้นตอนล้มเหลวในการทำให้เสร็จสมบูรณ์ (391116)

ด้วยการเปลี่ยนแปลงนี้ ลำดับงานการลางานและการขาดงานดำเนินการต่อผ่านขั้นตอนทั้งหมด เมื่อมีการตั้งค่าคอนฟิกระยะการอนุมัติมากกว่าหนึ่งระยะสำหรับคำขอ

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>วันที่ออกไม่ซิงค์กับ Common Data Service เมื่อมีการปรับปรุงหรือมีการป้อนใน Talent (397361)

การเปลี่ยนแปลงนี้แก้ไขปัญหาที่ซึ่งวันที่ออกสำหรับเรกคอร์ด **รหัสประจำตัวของบุคคล** ไม่ซิงค์กับ Common Data Service จาก Talent

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>มีการออกข้อผิดพลาดการอ้างอิงแบบวนของลำดับชั้น เมื่อกำหนดผู้จัดการให้กับตำแหน่ง (386659)

การเปลี่ยนแปลงนี้แก้ไขสถานการณ์เฉพาะที่มีข้อผิดพลาดในการอ้างอิงแบบวนปรากฏขึ้น เมื่อมีการกำหนดผู้จัดการใหม่ให้กับตำแหน่ง

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>เอนทิตี Common Data Service ที่สนับสนุนฟิลด์ที่กำหนดเองในขณะนี้

เอนทิตี Common Data Service ต่อไปนี้สนับสนุนฟิลด์ที่กำหนดเองในขณะนี้

| ชื่อ | เอนทิตี้ |
| --- | --- |
| การเบิกจ่ายเงินของบัญชีธนาคาร | cdm_bankaccountdisbursement |
| ความถี่ในการคำนวณสวัสดิการ | cdm_benefitcalculationfrequency |
| รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ | cdm_benefitcalculationfrequencypayperiod |
| อัตราการคำนวณสวัสดิการ | cdm_benefitcalculationrate |
| รายละเอียดอัตราการคำนวณสวัสดิการ | cdm_benefitcalculationratedetail |
| ตัวเลือกสวัสดิการ | cdm_benefitoption |
| แผนสวัสดิการ | cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง) |
| ชนิดของสวัสดิการ | cdm_benefittype |
| ปฏิทินกระบวนการทางธุรกิจ | cdm_businessprocesscalendar |
| การกำหนดกลุ่มกระบวนการทางธุรกิจ | cdm_businessprocessgroupassignment |
| กลุ่มงานไลบรารีกระบวนการทางธุรกิจ | cdm_businessprocesslibrarytaskgroup |
| ระยะของกระบวนการทางธุรกิจ | cdm_businessprocessstage |
| ส่วนหัวเท็มเพลตรายการตรวจสอบ | cdm_businessprocesstemplateheader |
| งานเท็มเพลตรายการตรวจสอบ | cdm_businessprocesstemplatetask |
| บริษัท | cdm_company |
| แผนค่าตอบแทนคงที่ | cdm_compensationfixedplan |
| กริดค่าตอบแทน | cdm_compensationgrid |
| ระดับค่าตอบแทน | cdm_compensationlevel |
| ความถี่ในการจ่ายค่าตอบแทน | cdm_compensationpayfrequency |
| การตั้งค่าจุดอ้างอิงค่าตอบแทน | cdm_compensationreferencepointsetup |
| รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน | cdm_compensationreferencepointsetupline |
| ภูมิภาคของค่าตอบแทน | cdm_compensationregion |
| โครงสร้างค่าตอบแทน | cdm_compensationstructure |
| แผนค่าตอบแทนผันแปร | cdm_compensationvariableplan |
| ระดับแผนค่าตอบแทนผันแปร | cdm_compensationvariableplanlevel |
| ชนิดแผนค่าตอบแทนผันแปร | cdm_compensationvariableplantype |
| แผนก | cdm_department |
| การจ้างงาน | cdm_employment |
| เชื้อชาติ | cdm_ethnicorigin |
| เหตุการณ์ค่าตอบแทนคงที่ | cdm_fixedcompensationevent |
| หน้าที่ | cdm_job |
| ฟังก์ชันงาน | cdm_jobfunction |
| ตำแหน่งงาน | cdm_jobposition |
| ชนิดงาน | cdm_jobtype |
| ภาษา | cdm_language |
| ธุรกรรมการออกจากธนาคาร | cdm_leavebanktransaction |
| การลงทะเบียนการลางาน | cdm_leaveenrollment |
| แผนการลาหยุด | cdm_leaveplan |
| การขอลา | cdm_leaverequest |
| รายละเอียดคำขอการลางาน | cdm_leaverequestdetail |
| ชนิดการลา | cdm_leavetype |
| รหัสเหตุผลชนิดการลา | cdm_leavetypereasoncode |
| รอบการชำระค่าจ้าง | cdm_paycycle |
| รอบระยะเวลาการชำระค่าจ้าง | cdm_payperiod |
| รหัสรายได้ค่าจ้าง | cdm_payrollearningcode |
| หน่วยงานที่ออกรหัสประจำตัวของบุคคล | cdm_personidentificationissuingagency |
| ชนิดตำแหน่ง | cdm_positiontype |
| การกำหนดผู้ปฏิบัติงานของตำแหน่ง | cdm_positionworkerassignmentmap |
| รหัสเหตุผล | cdm_reasoncode |
| ชนิดของทักษะ | cdm_skilltype |
| ภูมิภาคการเก็บภาษี | cdm_taxregion |
| กฎสิทธิ์พึงได้ | cdm_vestingrule |
| สถานะทหารผ่านศึก | cdm_veteranstatus |
| ปฏิทินการทำงาน | cdm_workcalendar |
| วันในปฏิทินงาน | cdm_workcalendarday |
| วันหยุดในปฏิทินการทำงาน |cdm_workcalendarholiday |
| รายการวันหยุดในปฏิทินงาน | cdm_workcalendarholidayline |
| ช่วงเวลาในปฏิทินงาน | cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง) |
| ผู้ปฏิบัติงาน | cdm_worker |
| ที่อยู่ผู้ปฏิบัติงาน | cdm_workeraddress |
| บัญชีธนาคารของผู้ปฏิบัติงาน | cdm_workerbankaccount |
| ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน | cdm_workerfixedcompensation |
| รายละเอียดส่วนตัวของผู้ปฏิบัติงาน | cdm_workerpersonaldetail |
| หมายเลขรหัสของผู้ปฏิบัติงาน | cdm_workerpersonidentificationnumber |
| ชนิดรหัสของผู้ปฏิบัติงาน | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

คุณลักษณะการแสดงตัวอย่างจะพร้อมใช้งานเฉพาะในสภาพแวดล้อม **Sandbox** เท่านั้น

### <a name="print-performance-reviews"></a>พิมพ์การตรวจทานประสิทธิภาพ

ให้ดูที่ [พิมพ์การตรวจทานประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2
