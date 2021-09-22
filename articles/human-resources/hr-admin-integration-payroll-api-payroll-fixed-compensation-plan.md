---
title: แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources
author: jcart
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dcb253fabbb183003048119c7a627bf0ab960050
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429251"
---
# <a name="payroll-fixed-compensation-plan"></a>แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะให้แผนค่าตอบแทนคงที่ที่กําหนดให้กับตําแหน่งที่กําหนดของพนักงาน

ชื่อทางกายภาพ: mshr_payrollfixedcompensationplanentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสแผน**</br>mshr_planid</br>*สตริง* | อ่านอย่างเดียว | ระบุแผนค่าตอบแทน  |
| **หมายเลขบุคลากร**</br>mshr_personnelnumber</br>*สตริง* | อ่านอย่างเดียว | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **อัตราการชำระค่าจ้าง**</br>mshr_payrate</br>*ทศนิยม* | อ่านอย่างเดียว | อัตราการค่าจ้างที่กําหนดในแผนค่าตอบแทนคงที่ |
| **รหัสตำแหน่ง**</br>mshr_positionid</br>*สตริง* | อ่านอย่างเดียว | รหัสไปรษณีย์ที่เชื่อมโยงกับพนักงานและการลงทะเบียนแผนค่าตอบแทนคงที่ |
| **มีผลใช้ตั้งแต่**</br>mshr_validfrom</br>*ออฟเซ็ตเวลา วันที่* |  อ่านอย่างเดียว | วันที่เริ่มต้นการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน  |
| **มีผลใช้ถึง**</br>mshr_validto</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่สิ้นสุดการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน |
| **ความถี่ในการชำระค่าจ้าง**</br>mshr_payfrequency</br>*สตริง* | อ่านอย่างเดียว | ความถี่ในการชําระค่าจ้างของพนักงาน  |
| **สกุลเงิน**</br>mshr_currency</br>*สตริง* | อ่านอย่างเดียว | สกุลเงินที่กำหนดสำหรับแผนค่าตอบแทนคงที่ |
| **เอนทิตีแผนค่าตอบแทนคงที่ของบัญชีเงินเดือน**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตีแผนค่าตอบแทนโดยเฉพาะ |

## <a name="relations"></a>ความสัมพันธ์

|ค่าคุณสมบัติ | เอนทิตีที่เกี่ยวข้อง | คุณสมบัติการนําทาง | ชนิดการรวบรวม |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**การตอบสนอง**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
