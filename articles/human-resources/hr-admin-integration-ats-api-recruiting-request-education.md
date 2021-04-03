---
title: การสรรหาบุคลากรที่มีคำขอการศึกษา
description: หัวข้อนี้อธิบายเอนทิตีการศึกษาของคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: efc5c4813f8abd869e8137052c4aeb356a930d0b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465977"
---
# <a name="recruiting-request-education"></a>การสรรหาบุคลากรที่มีคำขอการศึกษา

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีการศึกษาของคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>คำอธิบาย

อธิบายความต้องการด้านการศึกษาของ RecruitingRequest

### <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตีการสรรหาบุคลากรที่มีคำขอการศึกษา**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดการศึกษาของคำขอสรรหาบุคลากร |
| **รหัสคำขอสรรหา**<br>mshr_recruitingrequestid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | รหัสเฉพาะที่ผู้ใช้สามารถอ่านได้ของคำขอการสรรหาบุคลากรที่เกี่ยวข้อง |
| **ค่ารหัสคำขอสรรหา**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmrecruitingrequestentityid ของ mshr_hcmrecruitingrequestentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของคำขอการสรรหาบุคลากรที่เกี่ยวข้อง |
| **รหัสระดับการศึกษา**<br>mshr_educationlevelid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | ระดับการศึกษาที่จำเป็น |
| **ค่ารหัสระดับการศึกษา**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmeducationlevelentityid ของ mshr_hcmeducationlevelentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับระดับการศึกษาที่จำเป็น |
| **คำอธิบายของระดับการศึกษา**<br>mshr_educationleveldescription<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | คำอธิบายของระดับที่จำเป็นสำหรับทักษะ |
| **รหัสสาขาวิชาการศึกษา**<br>mshr_educationdisciplinedescription<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | พื้นที่ของสาขาวิชาการศึกษา |
| **ค่ารหัสสาขาวิชาการศึกษา**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmeducationdisciplineentityid ของ mshr_hcmeducationdisciplineentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับพื้นที่ของสาขาวิชาการศึกษา |
| **คำอธิบายสาขาวิชาการศึกษา**<br>mshr_educationdisciplinedescription<br>สตริง | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | อธิบายของพื้นที่ของสาขาวิชาการศึกษา |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุเอนทิตี้นิติบุคคล (บริษัท)|
| **ค่ารหัสพื้นที่ข้อมูล**<br>_mshr_dataareaid_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: cdm_companyid ของเอนทิตี cdm_company | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | การเชื่อมต่อของค่าคำขอการสรรหาบุคลากร รหัสระดับการศึกษา และรหัสสาขาวิชาการศึกษาเป็นวิธีการอื่นเพื่อระบุเรกคอร์ดเฉพาะ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]