---
title: ชนิดของการลางาน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีชนิดการลางานใน Dynamics 365 Human Resources
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
ms.openlocfilehash: a99d53805efd7ee2001217ea3154d46b5d5e66cd
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314502"
---
# <a name="leave-type"></a>ชนิดของการลางาน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีชนิดการลางานสำหรับ Dynamics 365 Human Resources

### <a name="description"></a>คำอธิบาย

เอนทิตีนี้แสดงข้อมูลของชนิดการลางานที่ระบุ

ชื่อทางกายภาพ: mshr_essleavetypeentity

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ</br>**ชื่อทางกายภาพ**</br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสชนิดของการลางาน**</br>mshr_leavetypeid</br>*สตริง* | อ่านอย่างเดียว | รหัสของชนิดการลางาน |
| **คำอธิบาย**</br>msdyn_description</br>*สตริง* | อ่านอย่างเดียว | คำอธิบายเกี่ยวกับชนิดการลางาน |
| **ประเภท**</br>mshr_category</br>*การกำหนดตัวเลือก mshr_LeaveTypeCategory* | อ่านอย่างเดียว | ประเภทของชนิดการลางาน |
| **ต้องการรหัสเหตุผล**</br>mshr_isreasoncoderequired</br>*ชุดตัวเลือก mshr_NoYes* | อ่านอย่างเดียว | กําหนดว่าต้องใช้รหัสเหตุผลในชนิดการลางานหรือไม่ |
| **หน่วยการลางาน**</br>mshr_leaveamountunit</br>*การกำหนดตัวเลือก mshr_LeaveAmountUnit* | อ่านอย่างเดียว | หน่วยของชนิดการลางานนี้ |
| **เปิดใช้งานครึ่งวัน**</br>mshr_enablehalfdaydefinition</br>*ชุดตัวเลือก mshr_NoYes* | กําหนดว่าเปิดใช้งานครึ่งวันของชนิดการลางานหรือไม่ |
| **รหัสพื้นที่ข้อมูล**</br>mshr_dataareaid_id</br>*สตริง* | อ่านอย่างเดียว | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **เอนทิตีชนิดของการลางาน**</br>mshr_essleavetypeentityid</br>*GUID* | ระบบสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงชนิดการลางานโดยเฉพาะ |

## <a name="example-query"></a>ตัวอย่างการสอบถาม

**คำขอ**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**การตอบสนอง**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
