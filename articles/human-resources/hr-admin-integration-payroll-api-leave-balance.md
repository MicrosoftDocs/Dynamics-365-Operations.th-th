---
title: ยอดดุลการลางาน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตียอดดุลการลางานใน Dynamics 365 Human Resources
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
ms.openlocfilehash: ab136e9b40de280387dc3c5207a08a6bb357941feb3a8c736d9671f7850f2bf8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782694"
---
# <a name="leave-balance"></a>ยอดดุลการลางาน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตียอดดุลการลางานสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้จะให้ยอดดุลการลางานต่อชนิดการลางานของพนักงานที่ที่ระบุ

ชื่อทางกายภาพ: mshr_essleavebalanceentities

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **หมายเลขบุคลากร**</br>mshr_personnelnumber</br>*สตริง* | อ่านอย่างเดียว | หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน |
| **ยอดวันลาคงเหลือปัจจุบัน**</br>mshr_balanceavailable</br>*ทศนิยม* | อ่านอย่างเดียว | ยอดวันลาปัจจุบันของพนักงาน |
| **ชนิด**</br>mshr_balanceavailable</br>*สตริง* | อ่านอย่างเดียว | รหัสของชนิดการลางาน |
| **อัตราตามเกณฑ์คงค้าง**</br>mshr_accrualratedescription</br> | อ่านอย่างเดียว | อัตราคงค้าง |
| **ยอดเงินยกไปล่าสุด**</br>mshr_lastcarryforwardamount</br>*ทศนิยม* | อ่านอย่างเดียว | ยอดยกยอดไปล่าสุด |
| **ใช้ไปในปีนี้**</br>mshr_takenthisyear</br>*ทศนิยม* | อ่านอย่างเดียว | ยอดการลางานที่ใช้ในปีนี้ |
| **ยอดรวมในปีนี้**</br>mshr_totalthisyear</br>*ทศนิยม* | อ่านอย่างเดียว | ยอดรวมสำหรับปีนี้ |
| **รหัสพื้นที่ข้อมูล**</br>mshr_dataareaid_id</br>*สตริง* | อ่านอย่างเดียว | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **ฟิลด์หลัก**</br>mshr_primaryfield</br>*GUID* | อ่านอย่างเดียว</br>ระบบสร้างขึ้น | |
| **รหัสชนิดของการลางาน**</br>_mshr_fk_leavetype_id_value</br>*GUID* | อ่านอย่างเดียว</br>คีย์นอก: เอนทิตี mshr_essleavetypeentityid of mshr_essleavetypeentity  | รหัสชนิดของการลางาน |
| **เอนทิตียอดดุลการลางาน**</br>mshr_essleavebalanceentityid</br>*GUID* | ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงยอดดุลเฉพาะ |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**การตอบสนอง**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
