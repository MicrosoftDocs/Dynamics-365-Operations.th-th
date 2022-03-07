---
title: ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882086"
---
# <a name="payroll-worker-address"></a>ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **เมือง**<br>mshr_city<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | เมืองที่ระบุสำหรับที่อยู่   |
| **หมายเลขบุคลากร**<br>mshr_personnelnumber<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน  |
| **ภูมิภาคประเทศ**<br>mshr_countryregionid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | ภูมิภาคประเทศที่ระบุสำหรับที่อยู่  |
| **มีผลใช้ตั้งแต่**<br>mshr_postaladdressvalidfrom<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่ที่ที่อยู่มีผลบังคับใช้ |
| **ที่อยู่ที่ทำงาน**<br>mshr_isworkedinaddressbr>*Int32* | อ่านอย่างเดียว<br>ต้องระบุ | แสดงถ้าที่อยู่เป็นที่อยู่ที่พนักงานทำงาน |
| **เขต**<br>mshr_county<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | ประเทศที่ระบุสำหรับที่อยู่  |
| **รหัสที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน**<br>mshr_payrollworkeraddressentityid<br>*GUID* | ต้องระบุ<br>ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงที่อยู่เฉพาะ  |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |  |
| **ถนน**<br>mshr_street<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | ถนนที่ระบุสำหรับที่อยู่ |
| **มีผลใช้ถึง**<br>mshr_postaladdressvalidto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่ที่ที่อยู่มีผลบังคับใช้ถึง  |
| **รหัสสถานที่**<br>mshr_locationidbr>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ | รหัสของที่อยู่  |
| **รหัสไปรษณีย์**<br>mshr_zipcode<br>*สตริง* | อ่านอย่างเดียว <br>ต้องระบุ |หมายเลขรหัสที่กําหนดไว้ให้กับพนักงาน  |
| **ที่อยู่อาศัย**<br>mshr_islivedinaddressbr>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | แสดงถ้าที่อยู่เป็นที่อยู่ที่พนักงานอาศัย |
| **จังหวัด**<br>mshr_state<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | รัฐที่ระบุสำหรับที่อยู่  |

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
