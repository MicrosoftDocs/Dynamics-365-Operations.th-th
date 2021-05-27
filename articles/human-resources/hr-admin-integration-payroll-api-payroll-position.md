---
title: รายละเอียดค่าจ้างสำหรับตำแหน่ง
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019333"
---
# <a name="payroll-position"></a>ตําแหน่งในบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **ชั่วโมงปกติรายปี**<br>annualregularhours<br>*ทศนิยม* | อ่านอย่างเดียว<br>ต้องระบุ | ชั่วโมงปกติรายปีที่กําหนดไว้ในตําแหน่ง  |
| **รหัสเอนทิตีรายละเอียดตำแหน่งค่าจ้าง**<br>payrollpositiondetailsentityid<br>*Guid* | ต้องระบุ<br>ระบบถูกสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตำแหน่งเฉพาะ  |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | ต้องระบุ<br>ระบบสร้างขึ้น |  |
| **ค่ารหัสตําแหน่งงาน**<br>_mshr_fk_positionjob_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก:mshr_PayrollPositionJobEntity:mshr_payrollpositionjobentity |รหัสของงานที่เชื่อมโยงกับตำแหน่ง|
| **ค่ารหัสแผนค่าตอบแทนคงที่**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | รหัสของแผนค่าตอบแทนคงที่ที่เชื่อมโยงกับตำแหน่ง |
| **รหัสรอบการชำระค่าจ้าง**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | วงจรการค่าจ้างที่กําหนดไว้ในตําแหน่ง |
| **ชำระโดยนิติบุคคล**<br>paidbylegalentity<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | นิติบุคคลที่กําหนดตามตําแหน่งที่รับผิดชอบการชำระเงิน |
| **รหัสตำแหน่ง**<br>mshr_positionid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | รหัสของตำแหน่ง |
| **มีผลใช้ถึง**<br>validto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว<br>ต้องระบุ |วันที่เริ่มต้นการมีผลบังคับใช้ของรายละเอียดตําแหน่ง  |
| **มีผลใช้ตั้งแต่**<br>validfrom<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว<br>ต้องระบุ |วันที่สิ้นสุดการมีผลบังคับใช้ของรายละเอียดตําแหน่ง  |

**การสอบถาม**

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
