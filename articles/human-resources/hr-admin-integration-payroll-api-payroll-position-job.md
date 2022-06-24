---
title: งานของตําแหน่งในบัญชีเงินเดือน
description: บทความนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีงานของตําแหน่งในบัญชีเงินเดือนใน Dynamics 365 Human Resources
author: jcart
ms.date: 04/07/2021
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
ms.openlocfilehash: fa347f4b99adc7c29d69daf62ad2bbfc14726a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864096"
---
# <a name="payroll-position-job"></a>งานของตําแหน่งในบัญชีเงินเดือน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายเอนทิตีงานของตําแหน่งในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะมีความสัมพันธ์ระหว่างตําแหน่งและงานให้กับแผนค่าตอบแทนคงที่ที่กําหนด

ชื่อทางกายภาพ: mshr_payrollpositionjobentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสตำแหน่ง**</br>mshr_positionid</br>*สตริง* | อ่านอย่างเดียว | รหัสของตำแหน่ง |
| **มีผลใช้ตั้งแต่**</br>mshr_validto</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่นั้นซึ่งความสัมพันธ์ตำแหน่งและงานเริ่มมีผลบังคับใช้ |
| **มีผลใช้ถึง**</br>mshr_validto</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่นั้นซึ่งความสัมพันธ์ตำแหน่งและงานสิ้นสุดการมีผลบังคับใช้ |
| **รหัสงาน**</br>mshr_jobid</br>*สตริง* | อ่านอย่างเดียว | รหัสของงาน |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*สตริง* | ระบบสร้างขึ้น | ฟิลด์หลัก |
| **รหัสเอนทิตีงานของตําแหน่งในบัญชีเงินเดือน**</br>mshr_payrollpositionjobentityid</br>*Guid* | ระบบถูกสร้างขึ้น | ค่ารหัสเฉพาะสากล (GUID) ที่ระบบสร้างขึ้นเพื่อระบุงานโดยไม่ซ้ำกัน |

## <a name="relations"></a>ความสัมพันธ์

| ค่าคุณสมบัติ | เอนทิตีที่เกี่ยวข้อง | คุณสมบัติการนําทาง | ชนิดการรวบรวม |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | ใช้ไม่ได้ |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**การตอบสนอง**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
