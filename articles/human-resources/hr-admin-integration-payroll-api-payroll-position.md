---
title: รายละเอียดค่าจ้างสำหรับตำแหน่ง
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 2bbb234d2f51391ea65e3d6153d6cee250f3c6dc
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069818"
---
# <a name="payroll-position"></a>ตําแหน่งในบัญชีเงินเดือน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีตําแหน่งในบัญชีเงินเดือนใน Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_payrollpositionentity

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้แสดงข้อมูลที่เกี่ยวข้องกับตำแหน่งของพนักงานที่ระบุ

ชื่อทางกายภาพ: mshr_payrollpositionentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสตำแหน่ง**</br>mshr_positionid</br>*สตริง* | อ่านอย่างเดียว | รหัสของตำแหน่ง |
| **รหัสรอบการชำระค่าจ้าง**</br>mshr_paycycleid</br>*สตริง* | อ่านอย่างเดียว | รอบการชำระค่าจ้างที่ถูกกําหนดไว้ในตําแหน่ง |
| **ชั่วโมงปกติรายปี**</br>annualregularhours</br>*ทศนิยม* | อ่านอย่างเดียว | ชั่วโมงปกติรายปีที่ถูกกําหนดไว้ในตําแหน่ง |
| **ชำระโดยนิติบุคคล**</br>paidbylegalentity</br>*สตริง* | อ่านอย่างเดียว | นิติบุคคลที่ถูกกําหนดในตําแหน่งและรับผิดชอบการออกการชำระเงิน |
| **มีผลใช้ถึง**</br>validto</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่ซึ่งสิ้นสุดการมีผลบังคับใช้ของรายละเอียดตําแหน่ง |
| **มีผลใช้ตั้งแต่**</br>validfrom</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่ซึ่งเริ่มมีผลบังคับใช้ของรายละเอียดตําแหน่ง |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*สตริง* | ระบบสร้างขึ้น | ฟิลด์หลัก |
| **รหัสเอนทิตีรายละเอียดตำแหน่งค่าจ้าง**</br>payrollpositiondetailsentityid</br>*Guid* | ต้องระบุ</br>ระบบถูกสร้างขึ้น | ค่ารหัสเฉพาะสากล (GUID) ที่ระบบสร้างขึ้นเพื่อระบุตำแหน่งโดยไม่ซ้ำกัน |

## <a name="relations"></a>ความสัมพันธ์

| ค่าคุณสมบัติ | เอนทิตีที่เกี่ยวข้อง | คุณสมบัติการนําทาง | ชนิดการรวบรวม |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | ใช้ไม่ได้ |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | ใช้ไม่ได้ |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**การตอบสนอง**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
