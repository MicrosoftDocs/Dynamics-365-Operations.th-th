---
title: พนักงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีพนักงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: e853a8a5730d397f253c8ce3a330794594dfd907
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068495"
---
# <a name="payroll-employee"></a>พนักงานในบัญชีเงินเดือน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีพนักงานในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_payrollemployeeentity

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะให้ข้อมูลเกี่ยวกับพนักงาน คุณต้องตั้งค่า [พารามิเตอร์การรวมระบบค่าจ้าง](hr-admin-integration-payroll-api-parameters.md) ก่อนที่จะใช้เอนทิตีนี้

>[!IMPORTANT] 
>ฟิลด์ **FirstName** **MiddleName** **LastName** **NameValidFrom** และ **NameValidTo** ไม่สามารถใช้งานได้บนเอนทิตีนี้อีกต่อไป สิ่งนี้ช่วยให้มั่นใจว่ามีแหล่งข้อมูลวันที่มีผลบังคับใช้เพียงแหล่งเดียว ที่กลับไปยังเอนทิตี้นี้
>ฟิลด์เหล่านี้จะพร้อมใช้งานบน **DirPersonNameHistoricalEntity** ซึ่งถูกนําออกใช้ในการปรับปรุงแพลตฟอร์ม 43 มีความสัมพันธ์ OData จาก **PayrollEmployeeEntity** ถึง **DirPersonNameHistoricalEntity** 

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสนิติบุคคล**</br>mshr_legalentityid</br>*สตริง* | อ่านอย่างเดียว | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **หมายเลขบุคลากร**</br>mshr_personnelnumber</br>*สตริง* | อ่านอย่างเดียว | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **วันที่เริ่มต้นการจ้างงาน**</br>mshr_employmentstartdate</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่เริ่มต้นของการจ้างงานของพนักงาน |
| **วันที่สิ้นสุดการจ้างงาน**</br>mshr_employmentenddate</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว |วันที่สิ้นสุดของการจ้างงานของพนักงาน  |
| **วันเกิด**</br>mshr_birthdate</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันเกิดของพนักงาน |
| **เพศ**</br>mshr_gender</br>[การกำหนดตัวเลือก mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | อ่านอย่างเดียว | เพศของพนักงาน |
| **ชนิดการจ้างงาน**</br>mshr_employmenttype</br>[การกำหนดตัวเลือก mshr_hcmemploymenttype](hr-admin-integration-payroll-api-hcmemploymenttype.md) | อ่านอย่างเดียว | ชนิดการจ้างงาน |
| **รหัสชนิดการระบุรหัสประจำตัว**</br>mshr_identificationtypeid</br>*สตริง* |อ่านอย่างเดียว | ชนิดรหัสที่กําหนดไว้ให้กับพนักงาน |
| **หมายเลขรหัส**</br>mshr_identificationnumber</br>*สตริง* | อ่านอย่างเดียว |หมายเลขรหัสที่กําหนดไว้ให้กับพนักงาน |
| **พร้อมที่จะจ่าย**</br>mshr_readytopay</br>[ชุดตัวเลือก mshr_noyes](hr-admin-integration-payroll-api-no-yes.md) | อ่านอย่างเดียว | ระบุว่าพนักงานถูกทำเครื่องหมายเป็นพร้อมที่จะชำระหรือไม่ |
| **รหัสเอนทิตีของพนักงานในบัญชีเงินเดือน**</br>mshr_payrollemployeeentityid</br>*GUID* | ระบบสร้างขึ้น | ค่ารหัสเฉพาะสากล (GUID) ที่ระบบสร้างขึ้นเพื่อระบุพนักงานแต่ละคน |

## <a name="relations"></a>ความสัมพันธ์

|ค่าคุณสมบัติ | เอนทิตีที่เกี่ยวข้อง | คุณสมบัติการนําทาง | ชนิดการรวบรวม |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>ตัวอย่างการสอบถามของพนักงานในบัญชีเงินเดือน

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
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
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
