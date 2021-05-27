---
title: พนักงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีพนักงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 0cd37a7323c0dd0dc6e60ff0495f827e9a8582c1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019381"
---
# <a name="payroll-employee"></a>พนักงานในบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีพนักงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **หมายเลขบุคลากร**<br>mshr_personnelnumber<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | ต้องระบุ<br>ระบบสร้างขึ้น |  |
| **นามสกุล**<br>mshr_lastname<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | นามสกุลพนักงาน |
| **รหัสนิติบุคคล**<br>mshr_legalentityID<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **มีผลใช้ตั้งแต่**<br>mshr_namevalidfrom<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่เริ่มต้นการมีผลบังคับของข้อมูลพนักงาน  |
| **เพศ**<br>mshr_gender<br>*Int32* | อ่านอย่างเดียว<br>ต้องระบุ | เพศของพนักงาน |
| **รหัสเอนทิตีของพนักงานในบัญชีเงินเดือน**<br>mshr_payrollemployeeentityid<br>*GUID* | ต้องระบุ<br>ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงพนักงานเฉพาะ |
| **วันที่เริ่มต้นการจ้างงาน**<br>mshr_employmentstartdate<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว<br>ต้องระบุ | วันที่เริ่มต้นของการจ้างงานของพนักงาน |
| **รหัสชนิดการระบุรหัสประจำตัว**<br>mshr_identificationtypeid<br>*สตริง* |อ่านอย่างเดียว<br>ต้องระบุ | ชนิดรหัสที่กําหนดไว้ให้กับพนักงาน |
| **วันที่สิ้นสุดการจ้างงาน**<br>mshr_employmentenddate<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว<br>ต้องระบุ |วันที่สิ้นสุดของการจ้างงานของพนักงาน  |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid_id<br>*GUID* | ต้องระบุ <br>ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) |
| **มีผลใช้ถึง**<br>mshr_namevalidto<br>*ออฟเซ็ตเวลา วันที่* |  อ่านอย่างเดียว<br>ต้องระบุ | วันที่สิ้นสุดการมีผลบังคับของข้อมูลพนักงาน |
| **วันเกิด**<br>mshr_birthdate<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันเกิดของพนักงาน |
| **หมายเลขรหัส**<br>mshr_identificationnumber<br>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ |หมายเลขรหัสที่กําหนดไว้ให้กับพนักงาน  |
| **ชื่อ**<br>mshr_firstname<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | ชื่อพนักงาน |
| **ชื่อกลาง**<br>mshr_middlename<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |ชื่อกลางของพนักงาน  |

## <a name="example-query-for-payroll-employee"></a>ตัวอย่างการสอบถามของพนักงานในบัญชีเงินเดือน

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**การตอบสนอง**

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
