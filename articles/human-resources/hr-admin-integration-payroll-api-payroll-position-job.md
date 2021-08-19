---
title: งานของตําแหน่งในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีงานของตําแหน่งในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: d5f84a1a6ff794cdc8b4b81e8518983789a0b33f1708719906f6ad094d9c4285
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722642"
---
# <a name="payroll-position-job"></a>งานของตําแหน่งในบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีงานของตําแหน่งในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะมีความสัมพันธ์ระหว่างตําแหน่งและงานให้กับแผนค่าตอบแทนคงที่ที่กําหนด

ชื่อทางกายภาพ: mshr_payrollpositionjobentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสงาน**<br>mshr_jobid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |รหัสของงาน |
| **มีผลใช้ตั้งแต่**<br>mshr_validto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่เริ่มต้นการมีผลใช้ของความสัมพันธ์ตำแหน่งและงาน |
| **มีผลใช้ถึง**<br>mshr_validto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่สิ้นสุดการมีผลใช้ของความสัมพันธ์ตำแหน่งและงาน  |
| **รหัสตำแหน่ง**<br>mshr_positionid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | รหัสของตำแหน่ง |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | ต้องระบุ<br>ระบบสร้างขึ้น |  |
| **ค่ารหัสตําแหน่งงาน**<br>_mshr_fk_positionjob_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก:mshr_PayrollPositionJobEntity:mshr_payrollpositionjobentity |รหัสของงานที่เชื่อมโยงกับตำแหน่ง|
| **ค่ารหัสแผนค่าตอบแทนคงที่**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | รหัสของแผนค่าตอบแทนคงที่ที่เชื่อมโยงกับตำแหน่ง |
| **รหัสเอนทิตีงานของตําแหน่งในบัญชีเงินเดือน**<br>mshr_payrollpositionjobentityid<br>*Guid* | ต้องระบุ<br>ระบบถูกสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงงานเฉพาะ  |

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
