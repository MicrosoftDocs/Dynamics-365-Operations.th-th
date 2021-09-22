---
title: แผนค่าตอบแทนผันแปรในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนผันแปรในบัญชีเงินเดือนใน Dynamics 365 Human Resources
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c30df23debed9e2ab90745e6ea9d0e6b8a05b6d5
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429278"
---
# <a name="payroll-variable-compensation-plan"></a>แผนค่าตอบแทนผันแปรในบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีแผนค่าตอบแทนผันแปรในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะให้แผนค่าตอบแทนผันแปรที่กําหนดให้กับตําแหน่งที่กําหนดของพนักงาน

ชื่อทางกายภาพ: mshr_payrollvariablecompensationawardentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **หมายเลขบุคลากร**</br>mshr_personnelnumber</br>*สตริง* | อ่านอย่างเดียว | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน  |
| **วันที่ให้**</br>mshr_awarddate</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่มอบรางวัล |
| **ชนิดรางวัล**</br>mshr_awardtype</br>*[การกำหนดตัวเลือก mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | อ่านอย่างเดียว | ชนิดรางวัลที่กำหนดสำหรับแผนค่าตอบแทนผันแปร |
| **สกุลเงิน**</br>mshr_unitcurrencycode</br>*สตริง* | อ่านอย่างเดียว |สกุลเงินที่กำหนดสำหรับแผนค่าตอบแทนผันแปร   |
| **รหัสแผนค่าตอบแทนคงที่**</br>mshr_fixedplanid</br>*สตริง* | อ่านอย่างเดียว | แผนค่าตอบแทนคงที่ที่ใช้เป็นพื้นฐานของการคำนวณรางวัล |
| **มูลค่าต่อหน่วย**</br>mshr_awardamount</br>*ทศนิยม* | อ่านอย่างเดียว | หน่วยของสินค้า |
| **ชนิดของกระบวนการ**</br>mshr_processtype</br>*[การกำหนดตัวเลือก mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | อ่านอย่างเดียว | ชนิดของกระบวนการ |
| **ชนิดแผนค่าตอบแทนผันแปร**</br>สตริง</br>*mshr_typeid* | อ่านอย่างเดียว | ชนิดของแผนค่าตอบแทนผันแปร |
| **รหัสแผนค่าตอบแทนผันแปร**</br>สตริง</br>*mshr_planid* | อ่านอย่างเดียว | รหัสของแผนค่าตอบแทนผันแปร |
| **หมายเลขของหน่วย**</br>ทศนิยม</br>*mshr_numberofunits* | อ่านอย่างเดียว | จำนวนหน่วยรางวัล |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*GUID* | อ่านอย่างเดียว</br>ระบบถูกสร้างขึ้น | |
| **เอนทิตีแผนค่าตอบแทนผันแปรในบัญชีเงินเดือน**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตีแผนค่าตอบแทนโดยเฉพาะ |

## <a name="relations"></a>ความสัมพันธ์ 

|ค่าคุณสมบัติ | เอนทิตีที่เกี่ยวข้อง | คุณสมบัติการนําทาง | ชนิดการรวบรวม |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**การตอบสนอง**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
