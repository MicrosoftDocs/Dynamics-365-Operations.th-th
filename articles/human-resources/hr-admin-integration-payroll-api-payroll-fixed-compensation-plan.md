---
title: แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources
author: jcart
manager: tfehr
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882089"
---
# <a name="payroll-fixed-compensation-plan"></a>แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสพนักงาน**<br>mshr_fk_employee_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก: เอนทิตี mshr_Employee_idของmshr_payrollemployeeentity  | รหัสพนักงาน |
| **อัตราการชำระค่าจ้าง**<br>mshr_payrate<br>*ทศนิยม* | อ่านอย่างเดียว<br>ต้องระบุ | อัตราการค่าจ้างที่กําหนดในแผนค่าตอบแทนคงที่ |
| **รหัสแผน**<br>mshr_planid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |ระบุแผนค่าตอบแทน  |
| **มีผลใช้ตั้งแต่**<br>mshr_validfrom<br>*ออฟเซ็ตเวลา วันที่* |  อ่านอย่างเดียว<br>ต้องระบุ |วันที่เริ่มต้นการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน  |
| **เอนทิตีแผนค่าตอบแทนคงที่ของบัญชีเงินเดือน**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | ต้องระบุ<br>ระบบถูกสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตีแผนค่าตอบแทนโดยเฉพาะ |
| **ความถี่ในการชำระค่าจ้าง**<br>mshr_payfrequency<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |ความถี่ในการชําระค่าจ้างของพนักงาน  |
| **มีผลใช้ถึง**<br>mshr_validto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่สิ้นสุดการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน |
| **รหัสตำแหน่ง**<br>mshr_positionid<br>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ | รหัสไปรษณีย์ที่เชื่อมโยงกับพนักงานและการลงทะเบียนแผนค่าตอบแทนคงที่ |
| **สกุลเงิน**<br>mshr_currency<br>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ |สกุลเงินที่กำหนดสำหรับแผนค่าตอบแทนคงที่   |
| **หมายเลขบุคลากร**<br>mshr_personnelnumber<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน  |

**การสอบถาม**

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
