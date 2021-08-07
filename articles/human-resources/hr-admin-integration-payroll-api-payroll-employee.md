---
title: พนักงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีพนักงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 672db002ddf8d12aaab5b97241390c036ad7ab5c
ms.sourcegitcommit: 8fb79920bea14746a71551a4456236a6386bfcea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/12/2021
ms.locfileid: "6538865"
---
# <a name="payroll-employee"></a>พนักงานในบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีพนักงานในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_payrollemployeeentity

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะให้ข้อมูลเกี่ยวกับพนักงาน คุณต้องตั้งค่า [พารามิเตอร์การรวมระบบค่าจ้าง](hr-admin-integration-payroll-api-parameters.md) ก่อนที่จะใช้เอนทิตีนี้

>[!IMPORTANT] 
>**FirstName** **MiddleName** **LastName** **NameValidFrom** และ **NameValidTo** จะไม่สามารถใช้งานได้บนเอนทิตีนี้อีกต่อไป ทั้งนี้เพื่อให้แน่ใจว่ามีแหล่งข้อมูลวันที่มีผลบังคับเพียงหนึ่งเท่านั้นที่สนับสนุนเอนทิตีนี้ ซึ่งเป็น **HcmEmployment** กับฟิลด์ **EmploymentStartDate** และ **EmploymentEndDate**

>ฟิลด์เหล่านี้จะพร้อมใช้งานบน **DirPersonNameHistoricalEntity** ซึ่งถูกนําออกใช้ในการปรับปรุงแพลตฟอร์ม 43 มีความสัมพันธ์ OData จาก **PayrollEmployeeEntity** ถึง **DirPersonNameHistoricalEntity** ในฟิลด์ **บุคคล** อีกทางหนึ่ง เอนทิตี **DirPersonNameHistoricalEntity** สามารถสอบถามโดยตรงผ่าน OData โดยใช้ชื่อสาธารณะ **PersonHistoricalNames**


## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **หมายเลขบุคลากร**<br>mshr_personnelnumber<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | ต้องระบุ<br>ระบบสร้างขึ้น |  |
| **รหัสนิติบุคคล**<br>mshr_legalentityID<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **เพศ**<br>mshr_gender<br>[การกำหนดตัวเลือก mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | อ่านอย่างเดียว<br>ต้องระบุ | เพศของพนักงาน |
| **รหัสเอนทิตีของพนักงานในบัญชีเงินเดือน**<br>mshr_payrollemployeeentityid<br>*GUID* | ต้องระบุ<br>ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงพนักงานเฉพาะ |
| **วันที่เริ่มต้นการจ้างงาน**<br>mshr_employmentstartdate<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว<br>ต้องระบุ | วันที่เริ่มต้นของการจ้างงานของพนักงาน |
| **รหัสชนิดการระบุรหัสประจำตัว**<br>mshr_identificationtypeid<br>*สตริง* |อ่านอย่างเดียว<br>ต้องระบุ | ชนิดรหัสที่กําหนดไว้ให้กับพนักงาน |
| **วันที่สิ้นสุดการจ้างงาน**<br>mshr_employmentenddate<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว<br>ต้องระบุ |วันที่สิ้นสุดของการจ้างงานของพนักงาน  |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid_id<br>*GUID* | ต้องระบุ <br>ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) |
| **มีผลใช้ถึง**<br>mshr_namevalidto<br>*ออฟเซ็ตเวลา วันที่* |  อ่านอย่างเดียว<br>ต้องระบุ | วันที่สิ้นสุดการมีผลบังคับของข้อมูลพนักงาน |
| **วันเกิด**<br>mshr_birthdate<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันเกิดของพนักงาน |
| **หมายเลขรหัส**<br>mshr_identificationnumber<br>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ |หมายเลขรหัสที่กําหนดไว้ให้กับพนักงาน  |

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
## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
