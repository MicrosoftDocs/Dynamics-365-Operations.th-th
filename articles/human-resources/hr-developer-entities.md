---
title: ตาราง Dataverse
description: Microsoft Dynamics 365 Human Resources ใช้ Dataverse เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838594"
---
# <a name="dataverse-tables"></a>ตาราง Dataverse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources ใช้ Dataverse เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม

> [!NOTE]
> เอนทิตี Human Resources จะสอดคล้องกับตาราง Dataverse หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดต Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) และการอัปเดตศัพท์ โปรดดูที่ [Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)

ตาราง Dataverse ต่อไปนี้พร้อมใช้งานในเอนทิตี Human Resources

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับปัญหาที่ทราบ ให้ดูที่ [การค้นหาปัญหาใน Lifecycle Services (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs)

## <a name="benefit-tables"></a>ตารางสวัสดิการ

| ชื่อ | ตาราง | ปัญหาที่ทราบ  | สถานะ |
| --- | --- |    --------|----------  |
| ความถี่ในการคำนวณสวัสดิการ | cdm_benefitcalculationfrequency |     |     |
| รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ | cdm_benefitcalculationfrequencypayperiod |     |     |
| อัตราการคำนวณสวัสดิการ | cdm_benefitcalculationrate |    |     |
| รายละเอียดอัตราการคำนวณสวัสดิการ | cdm_benefitcalculationratedetail |753225 | แก้ไขแล้ว  |
| ตัวเลือกสวัสดิการ | cdm_benefitoption |    |     |
| แผนสวัสดิการ | cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง) |    |     |
| ชนิดของสวัสดิการ | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>ตารางงานของกระบวนการทางธุรกิจ

| ชื่อ | ตาราง |ปัญหาที่ทราบ  | สถานะ |
| --- | --- |   --------|----------   |
| ปฏิทินกระบวนการทางธุรกิจ | cdm_businessprocesscalendar | 751867 | แก้ไขแล้ว |
| การกำหนดกลุ่มกระบวนการทางธุรกิจ | cdm_businessprocessgroupassignment | 751869  751863 | ใช้งานอยู่|
| กลุ่มงานไลบรารีกระบวนการทางธุรกิจ | cdm_businessprocesslibrarytaskgroup |751866 | ปิดแล้ว |
| ระยะของกระบวนการทางธุรกิจ | cdm_businessprocessstage |      |     |
| ส่วนหัวเทมเพลตรายการตรวจสอบ | cdm_businessprocesstemplateheader |     |     |
| งานเทมเพลตรายการตรวจสอบ | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>ตารางค่าตอบแทน

| ชื่อ | ตาราง |ปัญหาที่ทราบ  | สถานะ |
| --- | --- | ----------      | -------    |
| แผนค่าตอบแทนคงที่ | cdm_compensationfixedplan |754453 | ปิดแล้ว |
| กริดค่าตอบแทน | cdm_compensationgrid |             |     |
| ระดับค่าตอบแทน | cdm_compensationlevel |           |     |
| ความถี่ในการจ่ายค่าตอบแทน | cdm_compensationpayfrequency |                  |     |
| การตั้งค่าจุดอ้างอิงค่าตอบแทน | cdm_compensationreferencepointsetup |               |     |
| รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน | cdm_compensationreferencepointsetupline |             |     |
| ภูมิภาคของค่าตอบแทน | cdm_compensationregion |                   |     |
| โครงสร้างค่าตอบแทน | cdm_compensationstructure |    754456        | ปิดแล้ว    |
| แผนค่าตอบแทนผันแปร | cdm_compensationvariableplan |               |     |
| ระดับแผนค่าตอบแทนผันแปร | cdm_compensationvariableplanlevel |                |     |
| ชนิดแผนค่าตอบแทนผันแปร | cdm_compensationvariableplantype |               |     |
| เหตุการณ์ค่าตอบแทนคงที่ | cdm_fixedcompensationevent |               |     |
| กฎสิทธิ์พึงได้ | cdm_vestingrule |              |     |
| ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>ตารางองค์กร

| ชื่อ | ตาราง |ปัญหาที่ทราบ  | สถานะ |
| --- | --- | ----------      | -------    |
| แผนก | cdm_department |  752194    | ปิดแล้ว    |
| การจ้างงาน | cdm_employment | 762414  |  ปิดแล้ว  |
| บริษัท | cdm_company |  |     |
| หน้าที่ | cdm_job |  |     |
| ฟังก์ชันงาน | cdm_jobfunction |        |     |
| ตำแหน่งงาน | cdm_jobposition | 752214      | ปิดแล้ว    |
| ชนิดตำแหน่ง | cdm_positiontype |            |     |
| การกำหนดตำแหน่งของผู้ปฏิบัติงาน | cdm_positionworkerassignmentmap | 752224    |  ปิดแล้ว   |
| มิติตำแหน่งงาน | cdm_jobpositiondimension|       |     |
| ชนิดงาน | cdm_jobtype |      |     |
| ภาษา | cdm_language |        |     |
| ชื่อตำแหน่ง | cdm_title |       |     |

> [!NOTE]
> มิติทางการเงินสำหรับ **ชนิดของตำแหน่ง** **การกำหนดผู้ปฏิบัติงานของตำแหน่ง** และ **การจ้างงาน** ให้การรวมทิศทางเดียวแก่ Dataverse ในขณะนี้ การปรับปรุงมิติทางการเงินไม่สามารถซิงโครไนส์จาก Dataverse กับทรัพยากรบุคคลได้ 

## <a name="leave-and-absence-tables"></a>ตารางการลางานและการหยุดงาน

| ชื่อ | ตาราง | ปัญหาที่ทราบ  | สถานะ |
| --- | --- |   ----------      | -------    |
| ธุรกรรมธนาคารวันลา | cdm_leavebanktransaction |  752252    |    แก้ไขแล้ว |
| การลงทะเบียนการลาหยุด | cdm_leaveenrollment |  752934    |ปิดแล้ว     |
| แผนการลาหยุด | cdm_leaveplan |   752232   |   ปิดแล้ว  |
| การขอลา | cdm_leaverequest | 753207     | ปิดแล้ว    |
| รายละเอียดคำขอการลางาน | cdm_leaverequestdetail | 753207     |   ปิดแล้ว  |
| ชนิดการลา | cdm_leavetype |      |     |
| รหัสเหตุผลชนิดการลา | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>การรวมแบบสองทิศทางโดยใช้ตาราง Dataverse สำหรับการลางานและการขาดงานจะพร้อมใช้งานเฉพาะเมื่อคุณลักษณะ **การตั้งค่าคอนฟิกชนิดการลางานหลายชนิดในแผนการลางานเดียว** เปิดใช้งานใน Microsoft Dynamics 365 Finance โดยใช้ **การจัดการคุณลักษณะ** 

## <a name="payroll-tables"></a>ตารางค่าจ้าง

| ชื่อ | ตาราง |ปัญหาที่ทราบ  | สถานะ |
| --- | --- |  ----------      | -------    |
| รอบการชำระค่าจ้าง | cdm_paycycle |    |     |
| รอบระยะเวลาการชำระค่าจ้าง | cdm_payperiod |          |     |
| รหัสรายได้ค่าจ้าง | cdm_payrollearningcode |   754458        |   ปิดแล้ว  |
| การเบิกจ่ายเงินของบัญชีธนาคาร | cdm_bankaccountdisbursement |    751904     |   ปิดแล้ว  |
| ภูมิภาคการเก็บภาษี | cdm_taxregion |          |     |

## <a name="worker-tables"></a>ตารางผู้ปฏิบัติงาน

| ชื่อ | ตาราง |ปัญหาที่ทราบ  | สถานะ |
| --- | --- |----------      | -------    |
| ผู้ปฏิบัติงาน | cdm_worker |    751906    |    ปิดแล้ว |
| ที่อยู่ของผู้ปฏิบัติงาน | cdm_workeraddress |   754465     |ปิดแล้ว     |
| รายละเอียดส่วนตัวของผู้ปฏิบัติงาน | cdm_workerpersonaldetail |   751906     |   ปิดแล้ว  |
| หมายเลขรหัสของผู้ปฏิบัติงาน | cdm_workerpersonidentificationnumber |  766704      |   ปิดแล้ว  |
| ชนิดรหัสของผู้ปฏิบัติงาน | cdm_workerpersonidentificationtype |        |     |
| ปฏิทินการทำงาน | cdm_workcalendar |        |     |
| วันในปฏิทินงาน | cdm_workcalendarday |        |     |
| วันหยุดในปฏิทินการทำงาน |cdm_workcalendarholiday |        |     |
| รายการวันหยุดในปฏิทินงาน | cdm_workcalendarholidayline |        |     |
| ช่วงเวลาในปฏิทินงาน | cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง) |        |     |
| บัญชีธนาคารของผู้ปฏิบัติงาน | cdm_workerbankaccount |        |     |

## <a name="worker-setup-tables"></a>ตารางการตั้งค่าผู้ปฏิบัติงาน

| ชื่อ | ตาราง |
| --- | --- |
| สถานะทหารผ่านศึก | cdm_veteranstatus |
| เชื้อชาติ | cdm_ethnicorigin |
| รหัสเหตุผล | cdm_reasoncode |
| หน่วยงานที่ออกรหัสประจำตัวของบุคคล | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>ตารางความสามารถ

| ชื่อ | ตาราง |
| --- | --- |
| ชนิดทักษะ | cdm_skilltype |

## <a name="table-relationship-models"></a>แบบจำลองความสัมพันธ์ตาราง

### <a name="worker"></a>ผู้ปฏิบัติงาน

![ผู้ปฏิบัติงาน](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>งานและตำแหน่งงาน

![งานและตำแหน่งงาน](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>สวัสดิการ

![สวัสดิการ](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>ค่าตอบแทน

![ค่าตอบแทน](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>การลา

![การลา](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>ปฏิทินการทำงาน

![ปฏิทินการทำงาน](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[เลือกเทคโนโลยีการรวมข้อมูล](hr-admin-integration-choose-technology.md)<br>
[ตั้งค่าคอนฟิกการรวม Dataverse](hr-admin-integration-common-data-service.md)<br>
[ตั้งค่าคอนฟิกตารางเสมือน Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[FAQ เกี่ยวกับตารางเสมือนสำหรับ Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)<br>
[การอัปเดตศัพท์](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
