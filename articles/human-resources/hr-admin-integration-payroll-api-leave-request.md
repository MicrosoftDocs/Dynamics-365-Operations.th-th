---
title: คำขอการลางาน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีคำขอการลางานใน Dynamics 365 Human Resources
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7f5744265dd106f11e6ffe7334873e697a7ea13
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314498"
---
# <a name="leave-request"></a>คำขอการลางาน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีคำขอการลางานสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้แสดงข้อมูลของคำขอการลางาน

ชื่อทางกายภาพ: mshr_essleaverequestentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสคำขอ**</br>mshr_requestid</br>*สตริง* | อ่านอย่างเดียว | รหัสคำขอ |
| **รหัสชนิดของการลางาน**</br>mshr_leavetypeid</br>*สตริง* | อ่านอย่างเดียว | รหัสของชนิดการลางาน |
| **วัน เดือน**</br>mshr_leavedate</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่ของคำขอลางาน |
| **จำนวนเงิน**</br>mshr_amount</br>*ทศนิยม* | อ่านอย่างเดียว | จำนวนคำขอลางาน |
| **ชนิดครึ่งวัน**</br>mshr_halfdaydefinition</br>*ตัวเลือกการตั้งค่า mshr_LeaveHalfDayDefinition* | อ่านอย่างเดียว | ชนิดของการลางานครึ่งวัน |
| **ข้อคิดเห็น**</br>mshr_comment</br>*สตริง* | อ่านอย่างเดียว | ข้อคิดเห็นของคำขอ |
| **สถานะ**</br>mshr_status</br>*ชุดตัวเลือก mshr_status* | อ่านอย่างเดียว | สถานะของคำขอ |
| **วัน เดือน**</br>mshr_requestdate</br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว | วันที่คำขอ |
| **หมายเลขบุคลากร**</br>mshr_personnelnumber</br>*สตริง* | อ่านอย่างเดียว | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **รหัสเหตุผล**</br>mshr_reasoncodeid</br>*สตริง* | อ่านอย่างเดียว | รหัสเหตุผล |
| **รหัสพื้นที่ข้อมูล**</br>mshr_dataareaid</br>*สตริง* | อ่านอย่างเดียว | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*GUID* | อ่านอย่างเดียว</br>ระบบสร้างขึ้น | |
| **เอนทิตีชนิดของการลางาน**</br>mshr_essleaverequestentityid</br>*GUID* | ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงคำขอลางานโดยเฉพาะ |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**การตอบสนอง**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
