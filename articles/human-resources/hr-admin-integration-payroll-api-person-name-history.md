---
title: ประวัติชื่อบุคคล
description: หัวข้อนี้แสดงรายละเอียดและการสอบถามตัวอย่างสำหรับเอนทิตีประวัติของชื่อบุคคลใน Dynamics 365 Human Resources
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 418047a0643ee29b89763dbe2b030753f405b575
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559684"
---
# <a name="person-name-history"></a>ประวัติชื่อบุคคล

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีประวัติของชื่อบุคคลใน Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_dirpersonnamehistoricalentity

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะให้ข้อมูลเกี่ยวกับประวัติของชื่อสำหรับบุคคลที่กำหนด

> [!IMPORTANT] 
> ฟิลด์ **FirstName**, **MiddleName**, **LastName**, **NameValidFrom**, และ **NameValidTo** ไม่สามารถใช้งานได้อีกต่อไปบนเอนทิตีพนักงานในบัญชีเงินเดือน รายการเหล่านี้ได้ถูกลบออกเพื่อช่วยให้มั่นใจว่า แหล่งข้อมูลวันที่มีผลบังคับใช้เพียงแหล่งเดียวเท่านั้นจะกลับไปยังเอนทิตีนี้

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **ชื่อ**</br>mshr_firstname</br>*สตริง* | อ่านอย่างเดียว | ชื่อ |
| **คำนำหน้านามสกุล**</br>mshr_lastnameprefix</br>*สตริง*) | อ่านอย่างเดียว | คำนำหน้านามสกุล |
| **นามสกุล**</br>mshr_lastname</br>*สตริง*) | อ่านอย่างเดียว | นามสกุล |
| **ชื่อกลาง**</br>mshr_middlename</br>*สตริง*) | อ่านอย่างเดียว | ชื่อกลาง |
| **มีผลใช้ถึง**</br>mshr_validto</br>*สตริง*) | อ่านอย่างเดียว | วันที่ซึ่งชื่อสิ้นสุดการมีผลบังคับใช้ |
| **หมายเลขฝ่าย**</br>mshr_partynumber</br>*สตริง* | อ่านอย่างเดียว | ตัวระบุเฉพาะที่ระบบสร้างขึ้นและผู้ใช้สามารถอ่านได้สำหรับบุคคล |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*สตริง* | อ่านอย่างเดียว | ตัวระบุเฉพาะของเรกคอร์ด |
| **รหัสเอนทิตีประวัติของชื่อบุคคล**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | ระบบสร้างขึ้น | ค่ารหัสเฉพาะสากล (GUID) ที่ระบบสร้างขึ้นเพื่อระบุเรกคอร์ดโดยไม่ซ้ำกัน |

## <a name="relations"></a>ความสัมพันธ์

| ค่าคุณสมบัติ | เอนทิตีที่เกี่ยวข้อง | คุณสมบัติการนําทาง | ชนิดการรวบรวม |
| --- | --- | --- | --- |
| ใช้ไม่ได้ | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | ใช้ไม่ได้ | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>ตัวอย่างการสอบถามของพนักงานในบัญชีเงินเดือน

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**การตอบสนอง**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
