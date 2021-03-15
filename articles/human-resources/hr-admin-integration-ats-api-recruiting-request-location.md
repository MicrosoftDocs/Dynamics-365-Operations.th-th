---
title: ที่ตั้งของคำขอสรรหาบุคลากร
description: หัวข้อนี้อธิบายเอนทิตีที่ตั้งของคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa153b1cfcbb70294ed6da3618c83396df04f8db
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125244"
---
# <a name="recruiting-request-location"></a>ที่ตั้งของคำขอสรรหาบุคลากร

หัวข้อนี้อธิบายเอนทิตีที่ตั้งของคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>คำอธิบาย

รายการของสถานที่ซึ่งกําหนดเป็นที่ตั้งที่พนักงานสรรหาบุคลากรจะว่าจ้าง ซึ่งเป็นที่ตั้งที่สร้างระหว่างนิติบุคคล

### <a name="json-representation"></a>การแสดง JSON

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสสถานที่**<br>mshr_locationid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ผู้ใช้สามารถอ่านได้ที่ระบบสร้างขึ้นสำหรับที่ตั้งของการสรรหาบุคลากร |
| **ที่ตั้งของคำขอสรรหาบุคลากร**<br>mshr_recruitingrequestlocationid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่กำหนดโดยผู้ใช้ของที่ตั้งของการสรรหาบุคลากร |
| **รหัสเอนทิตีการสรรหาบุคลากรที่มีคำขอที่ตั้ง**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดที่ตั้งของคำขอสรรหาบุคลากร |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | คำอธิบายเกี่ยวกับที่ตั้ง |
| **รหัสภูมิภาค/ประเทศ**<br>mshr_countryregionid<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | ระบุประเทศหรือภูมิภาคที่ผู้สมัครมีสัญชาติ |
| **ค่ารหัสภูมิภาค/ประเทศ**<br>_mshr_fk_countriregion_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_logisticaddresscountryregionentityid ของ mshr_logisticsaddresscountryregionentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของประเทศ/ภูมิภาคของที่อยู่ |
| **รหัสไปรษณีย์**<br>mshr_zipcode<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | รหัสไปรษณีย์ |
| **ถนน**<br>mshr_street<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | ที่อยู่ถนน |
| **เมือง**<br>mshr_city<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | เมือง |
| **จังหวัด**<br>mshr_state<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | รัฐหรือจังหวัด |
| **เขต**<br>mshr_county<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | เขต |
| **โทรศัพท์**<br>mshr_telephone<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขโทรศัพท์ของที่ตั้ง |
| **อีเมล**<br>mshr_email<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ที่อยู่อีเมล |
| **InternetAddress**<br>mshr_internetaddress<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | URL ของเว็บไซต์ที่ตั้ง |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **ค่ารหัสพื้นที่ข้อมูล**<br>_mshr_dataareaid_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: cdm_companyid ของเอนทิตี cdm_company | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]