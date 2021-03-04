---
title: เอนทิตี้ Common Data Service
description: Microsoft Dynamics 365 Human Resources ใช้ Common Data Service เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530017"
---
# <a name="common-data-service-entities"></a>เอนทิตี้ Common Data Service

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources ใช้ Common Data Service เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Common Data Service ให้ดูที่ [อะไรคือ Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

เอนทิตีทรัพยากรต่อไปนี้พร้อมใช้งานใน Common Data Service

## <a name="benefit-entities"></a>เอนทิตี้สวัสดิการ

| ชื่อ | เอนทิตี้ |
| --- | --- |
| ความถี่ในการคำนวณสวัสดิการ | cdm_benefitcalculationfrequency |
| รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ | cdm_benefitcalculationfrequencypayperiod |
| อัตราการคำนวณสวัสดิการ | cdm_benefitcalculationrate |
| รายละเอียดอัตราการคำนวณสวัสดิการ | cdm_benefitcalculationratedetail |
| ตัวเลือกสวัสดิการ | cdm_benefitoption |
| แผนสวัสดิการ | cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง) |
| ชนิดของสวัสดิการ | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>เอนทิตีงานของกระบวนการทางธุรกิจ

| ชื่อ | เอนทิตี้ |
| --- | --- |
| ปฏิทินกระบวนการทางธุรกิจ | cdm_businessprocesscalendar |
| การกำหนดกลุ่มกระบวนการทางธุรกิจ | cdm_businessprocessgroupassignment |
| กลุ่มงานไลบรารีกระบวนการทางธุรกิจ | cdm_businessprocesslibrarytaskgroup |
| ระยะของกระบวนการทางธุรกิจ | cdm_businessprocessstage |
| ส่วนหัวเท็มเพลตรายการตรวจสอบ | cdm_businessprocesstemplateheader |
| งานเท็มเพลตรายการตรวจสอบ | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>เอนทิตีค่าตอบแทน

| ชื่อ | เอนทิตี้ |
| --- | --- |
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
| เหตุการณ์ค่าตอบแทนคงที่ | cdm_fixedcompensationevent |
| กฎสิทธิ์พึงได้ | cdm_vestingrule |
| ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>เอนทิตี้องค์กร

| ชื่อ | เอนทิตี้ |
| --- | --- |
| แผนก | cdm_department |
| การจ้างงาน | cdm_employment |
| บริษัท | cdm_company |
| หน้าที่ | cdm_job |
| ฟังก์ชันงาน | cdm_jobfunction |
| ตำแหน่งงาน | cdm_jobposition |
| ชนิดตำแหน่ง | cdm_positiontype |
| การกำหนดตำแหน่งของผู้ปฏิบัติงาน | cdm_positionworkerassignmentmap |
| มิติตำแหน่งงาน | cdm_jobpositiondimension|
| ชนิดงาน | cdm_jobtype |
| ภาษา | cdm_language |
| ชื่อตำแหน่ง | cdm_title |

> [!NOTE]
> มิติทางการเงินสำหรับ **ชนิดของตำแหน่ง** **การกำหนดผู้ปฏิบัติงานของตำแหน่ง** และ **การจ้างงาน** ให้การรวมทิศทางเดียวแก่ Common Data Service ในขณะนี้ การปรับปรุงมิติทางการเงินไม่สามารถซิงโครไนส์จาก Common Data Service กับทรัพยากรบุคคลได้ 

## <a name="leave-and-absence-entities"></a>เอนทิตี้การลางานและการขาดงาน

| ชื่อ | เอนทิตี้ |
| --- | --- |
| ธุรกรรมธนาคารวันลา | cdm_leavebanktransaction |
| การลงทะเบียนการลางาน | cdm_leaveenrollment |
| แผนการลาหยุด | cdm_leaveplan |
| การขอลา | cdm_leaverequest |
| รายละเอียดคำขอการลางาน | cdm_leaverequestdetail |
| ชนิดการลา | cdm_leavetype |
| รหัสเหตุผลชนิดการลา | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>เอนทิตี้ค่าจ้าง

| ชื่อ | เอนทิตี้ |
| --- | --- |
| รอบการชำระค่าจ้าง | cdm_paycycle |
| รอบระยะเวลาการชำระค่าจ้าง | cdm_payperiod |
| รหัสรายได้ค่าจ้าง | cdm_payrollearningcode |
| การเบิกจ่ายเงินของบัญชีธนาคาร | cdm_bankaccountdisbursement |
| ภูมิภาคการเก็บภาษี | cdm_taxregion |

## <a name="worker-entities"></a>เอนทิตี้ของผู้ปฏิบัติงาน

| ชื่อ | เอนทิตี้ |
| --- | --- |
| ผู้ปฏิบัติงาน | cdm_worker |
| ที่อยู่ผู้ปฏิบัติงาน | cdm_workeraddress |
| รายละเอียดส่วนตัวของผู้ปฏิบัติงาน | cdm_workerpersonaldetail |
| หมายเลขรหัสของผู้ปฏิบัติงาน | cdm_workerpersonidentificationnumber |
| ชนิดรหัสของผู้ปฏิบัติงาน | cdm_workerpersonidentificationtype |
| ปฏิทินการทำงาน | cdm_workcalendar |
| วันในปฏิทินงาน | cdm_workcalendarday |
| วันหยุดในปฏิทินการทำงาน |cdm_workcalendarholiday |
| รายการวันหยุดในปฏิทินงาน | cdm_workcalendarholidayline |
| ช่วงเวลาในปฏิทินงาน | cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง) |
| บัญชีธนาคารของผู้ปฏิบัติงาน | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>เอนทิตีการตั้งค่าของผู้ปฏิบัติงาน

| ชื่อ | เอนทิตี้ |
| --- | --- |
| สถานะทหารผ่านศึก | cdm_veteranstatus |
| เชื้อชาติ | cdm_ethnicorigin |
| รหัสเหตุผล | cdm_reasoncode |
| หน่วยงานที่ออกรหัสประจำตัวของบุคคล | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>เอนทิตีความสามารถ

| ชื่อ | เอนทิตี้ |
| --- | --- |
| ชนิดของทักษะ | cdm_skilltype |

## <a name="entity-relationship-models"></a>รูปแบบความสัมพันธ์เอนทีตี้

### <a name="worker"></a>ผู้ปฏิบัติงาน

![ผู้ปฏิบัติงาน](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>งานและตำแหน่งงาน

![งานและตำแหน่งงาน](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>สวัสดิการ

![สวัสดิการ](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>ค่าตอบแทน

![ค่าตอบแทน](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>ออก

![ออก](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>ปฏิทินการทำงาน

![ปฏิทินการทำงาน](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[เลือกเทคโนโลยีการรวมข้อมูล](hr-admin-integration-choose-technology.md)</br>
[ตั้งค่าคอนฟิกการรวม Common Data Service](hr-admin-integration-common-data-service.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]