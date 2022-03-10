---
title: ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 70e42cbf657a28327699d927731edd36de7c4a64
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069768"
---
# <a name="payroll-worker-address"></a>ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีที่อยู่ของผู้ปฏิบัติงานในบัญชีเงินเดือนสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_payrollworkeraddressentity

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้เสนอที่ตั้งถิ่นที่อยู่ในบัญชีเงินเดือนและสถานที่งานในบัญชีเงินเดือนของพนักงานที่กำหนด

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **หมายเลขบุคลากร**</br>mshr_personnelnumber</br>*สตริง* | อ่านอย่างเดียว | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **รหัสสถานที่**</br>mshr_locationidbr>*สตริง* | อ่านอย่างเดียว | รหัสของที่อยู่ |
| **ที่อยู่อาศัย**</br>mshr_islivedinaddressbr </br> *[ตัวเลือกการตั้งค่า mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | อ่านอย่างเดียว | ค่าที่ระบุว่าที่อยู่คือที่ซึ่งพนักงานอาศัยอยู่หรือไม่ |
| **ที่อยู่ที่ทำงาน** </br> mshr_isworkedinaddressbr </br>*[ตัวเลือกการตั้งค่า mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | อ่านอย่างเดียว | ค่าที่ระบุว่าที่อยู่คือที่ซึ่งพนักงานทำงานอยู่หรือไม่ |
| **ภูมิภาคประเทศ**</br>mshr_countryregionid</br>*สตริง* | อ่านอย่างเดียว</br>ต้องระบุ | ประเทศหรือภูมิภาคที่ถูกระบุสำหรับที่อยู่ |
| **รหัสไปรษณีย์**</br>mshr_zipcode<br>*สตริง* | อ่านอย่างเดียว | หมายเลขการระบุรหัสประจำตัวที่ถูกกําหนดสำหรับพนักงาน |
| **ถนน**</br>mshr_street</br>*สตริง* | อ่านอย่างเดียว | ถนนที่ถูกระบุสำหรับที่อยู่ |
| **เมือง**</br>mshr_city</br>*สตริง* | อ่านอย่างเดียว | เมืองที่ถูกระบุสำหรับที่อยู่ |
| **จังหวัด**</br>mshr_state</br>*สตริง* | อ่านอย่างเดียว | รัฐหรือจังหวัดที่ถูกระบุสำหรับที่อยู่ |
| **เขต**</br>mshr_county</br>*สตริง* | อ่านอย่างเดียว | ประเทศที่ถูกระบุสำหรับที่อยู่ |
| **มีผลใช้ตั้งแต่**</br>mshr_postaladdressvalidfrom</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่ซึ่งที่อยู่เริ่มมีผลบังคับใช้ |
| **มีผลใช้ถึง**</br>mshr_postaladdressvalidto</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่ซึ่งที่อยู่สิ้นสุดการมีผลบังคับใช้ |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*สตริง* | อ่านอย่างเดียว | ฟิลด์หลัก |
| **รหัสที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน**</br>mshr_payrollworkeraddressentityid</br>*GUID* | ระบบสร้างขึ้น | ค่ารหัสเฉพาะสากล (GUID) ที่ระบบสร้างขึ้นเพื่อระบุที่อยู่โดยไม่ซ้ำกัน |

## <a name="relations"></a>ความสัมพันธ์

| ค่าคุณสมบัติ | เอนทิตีที่เกี่ยวข้อง | คุณสมบัติการนําทาง | ชนิดการรวบรวม |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**การตอบสนอง**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
