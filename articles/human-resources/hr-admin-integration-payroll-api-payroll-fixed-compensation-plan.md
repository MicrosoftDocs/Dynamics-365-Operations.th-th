---
title: แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: f1e5345d9f27106bdf3a3a60cb0480a9b072e340c01236e4d48c5e2ae592ddbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738402"
---
# <a name="payroll-fixed-compensation-plan"></a>แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะให้แผนค่าตอบแทนคงที่ที่กําหนดให้กับตําแหน่งที่กําหนดของพนักงาน

ชื่อทางกายภาพ: mshr_payrollfixedcompensationplanentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสพนักงาน**<br>mshr_fk_employee_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก: เอนทิตี mshr_Employee_idของmshr_payrollemployeeentity  | รหัสพนักงาน |
| **อัตราการชำระค่าจ้าง**<br>mshr_payrate<br>*ทศนิยม* | อ่านอย่างเดียว<br>ต้องระบุ | อัตราการค่าจ้างที่กําหนดในแผนค่าตอบแทนคงที่ |
| **รหัสแผน**<br>mshr_planid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |ระบุแผนค่าตอบแทน  |
| **มีผลใช้ตั้งแต่**<br>mshr_validfrom<br>*ออฟเซ็ตเวลา วันที่* |  อ่านอย่างเดียว<br>ต้องระบุ |วันที่เริ่มต้นการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน  |
| **เอนทิตีแผนค่าตอบแทนคงที่ของบัญชีเงินเดือน**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | ต้องระบุ<br>ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตีแผนค่าตอบแทนโดยเฉพาะ |
| **ความถี่ในการชำระค่าจ้าง**<br>mshr_payfrequency<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |ความถี่ในการชําระค่าจ้างของพนักงาน  |
| **มีผลใช้ถึง**<br>mshr_validto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่สิ้นสุดการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน |
| **รหัสตำแหน่ง**<br>mshr_positionid<br>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ | รหัสไปรษณีย์ที่เชื่อมโยงกับพนักงานและการลงทะเบียนแผนค่าตอบแทนคงที่ |
| **สกุลเงิน**<br>mshr_currency<br>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ |สกุลเงินที่กำหนดสำหรับแผนค่าตอบแทนคงที่   |
| **หมายเลขบุคลากร**<br>mshr_personnelnumber<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน  |

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
