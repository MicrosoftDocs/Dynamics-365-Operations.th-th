---
title: แผนสวัสดิการของผู้ปฏิบัติงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนสวัสดิการของผู้ปฏิบัติงานในบัญชีเงินเดือน ใน Dynamics 365 Human Resources
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1805f7efaf2efc48d5996776f3aa27d75606886f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068445"
---
# <a name="payroll-worker-benefit-plan"></a>แผนสวัสดิการของผู้ปฏิบัติงานในบัญชีเงินเดือน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีแผนสวัสดิการของผู้ปฏิบัติงานในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_payrollworkerbenefitplanentities

### <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะให้ข้อมูลเกี่ยวกับแผนสวัสดิการของผู้ปฏิบัติงานที่มอบหมาย

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **หมายเลขบุคลากร**</br>mshr_personnelnumber</br>*สตริง* | อ่านอย่างเดียว</br>ต้องระบุ | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **รหัสนิติบุคคล**</br>mshr_legalentityID</br>*สตริง* | อ่านอย่างเดียว | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **รหัสรอบระยะเวลา**</br>mshr_periodid</br>*สตริง* | อ่านอย่างเดียว | ตัวระบุของรอบระยะเวลา |
| **รหัสแผน**</br>mshr_planid</br>*สตริง* | อ่านอย่างเดียว | ตัวระบุของแผน |
| **ตัวเลือกความคุ้มครอง**</br>mshr_coverageoptionid</br>*สตริง* | อ่านอย่างเดียว | ตัวระบุของตัวเลือกความครอบคลุม |
| **วันที่เริ่มต้นของรายการหัก**</br>mshr_deductionstartdatetime</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่เริ่มต้นของรายการหัก |
| **วันที่สิ้นสุดการหักเงิน**</br>mshr_deductionenddatetime</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่สิ้นสุดของรายการหัก |
| **สถานะ**</br>mshr_status</br>*[ตัวเลือกการตั้งค่าสถานะของแผนพนักงานในสวัสดิการ](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | อ่านอย่างเดียว | สถานะของแผนสวัสดิการ |
| **มีผลใช้ตั้งแต่**</br>mshr_validfrom</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | เวลาเริ่มต้นที่เรกคอร์ดนี้มีผลบังคับใช้ |
| **มีผลใช้ถึง**</br>mshr_validto</br>*ออฟเซ็ตเวลา วันที่* |  อ่านอย่างเดียว | เวลาสิ้นสุดที่เรกคอร์ดนี้มีผลบังคับใช้ |
| **รหัสชนิดแผน**</br>mshr_plantypeid</br>*สตริง* | อ่านอย่างเดียว | ตัวระบุของชนิดแผน |
| **รหัสชนิดแผน**</br>mshr_plantypecode</br>*[ตัวเลือกการตั้งค่าใบปะหน้าชนิดแผนสวัสดิการ](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | อ่านอย่างเดียว | ข้อมูลจำเพาะของชนิดแผน |
| **จำนวนของรอบระยะเวลาการชำระค่าจ้าง**</br>mshr_payperiod</br>*เลขจำนวนเต็ม* | อ่านอย่างเดียว | จำนวนของรอบระยะเวลาการชำระเงินที่แสดงถึงความถี่ในการชำระเงินของผู้ให้บริการสิทธิประโยชน์หรือพนักงาน จำนวนนี้จะถูกนำไปใช้ในการคำนวณจำนวนรายได้สวัสดิการประจำปีของพนักงาน |
| **จำนวนเงินของพนักงาน**</br>mshr_amountemployee</br>*ทศนิยม* | อ่านอย่างเดียว | จำนวนพนักงานหรือเปอร์เซ็นต์ |
| **จำนวนเงินของนายจ้าง**</br>mshr_amountemployer</br>*ทศนิยม* | อ่านอย่างเดียว | จำนวนนายจ้างหรือเปอร์เซ็นต์ |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*สตริง* | ระบบสร้างขึ้น | ฟิลด์หลัก |
| **ค่ารหัสผู้ปฏิบัติงาน** </br>_mshr_fk_worker_id_value</br>*GUID* | คีย์นอก: mshr_hcmworkerbaseentityid ของเอนทิตี mshr_hcmworkerbaseentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับผู้ปฏิบัติงาน |
| **ค่ารหัสของรอบระยะเวลา**</br> _mshr_fk_period_id_value</br>*GUID* | คีย์นอก: mshr_benefitperiodentityid ของเอนทิตี mshr_benefitperiodentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับรอบระยะเวลา |
| **ค่ารหัสแผน**</br> _mshr_fk_plan_id_value</br>*GUID* | คีย์นอก: mshr_benefitplanentityid ของเอนทิตี mshr_benefitplanentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับแผน |
| **ค่ารหัสชนิดแผน**</br> _mshr_fk_plantype_id_value</br>*GUID* | คีย์นอก: mshr_benefitplantypeentityid ของเอนทิตี mshr_benefitplantypeentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับแผน |
| **ค่ารหัสตัวเลือกความครอบคลุม**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | คีย์นอก: mshr_benefitcoverageoptionentityid ของเอนทิตี mshr_benefitcoverageoptionentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับแผน |
| **ค่ารหัสเอนทิตีของแผนสวัสดิการของผู้ปฏิบัติงานในบัญชีเงินเดือน**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | อ่านอย่างเดียว </br> ระบบสร้างขึ้น | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ด |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>ตัวอย่างการสอบถามเกี่ยวกับแผนสวัสดิการของผู้ปฏิบัติงานในบัญชีเงินเดือน

**คำขอ**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**การตอบสนอง**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
