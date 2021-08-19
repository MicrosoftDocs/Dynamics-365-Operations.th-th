---
title: การสรรหาบุคลากรที่มีคำขอทักษะ
description: หัวข้อนี้อธิบายเอนทิตีทักษะคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9347b6f2e18c7ec12c18137846507532fc9fcc3149a3638d12c070dc848a1fc7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712132"
---
# <a name="recruiting-request-skill"></a>การสรรหาบุคลากรที่มีคำขอทักษะ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีทักษะคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>คำอธิบาย

อธิบายความต้องการทักษะของ RecruitingRequest

### <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตีการสรรหาบุคลากรที่มีคำขอทักษะ**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ด **การสรรหาบุคลากรที่มีคำขอทักษะ** |
| **รหัสคำขอสรรหา**<br>mshr_recruitingrequestid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | รหัสเฉพาะที่ผู้ใช้สามารถอ่านได้ของคำขอการสรรหาบุคลากรที่เกี่ยวข้อง |
| **ค่ารหัสคำขอสรรหา**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br> คีย์นอก: mshr_hcmrecruitingrequestentityid ของเอนทิตี mshr_hcmrecruitingrequestentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของคำขอการสรรหาบุคลากรที่เกี่ยวข้อง |
| **รหัสทักษะ**<br>mshr_skillid<br>*สตริง*<br> | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | รหัสเฉพาะที่ผู้ใช้สามารถอ่านได้ของทักษะจำเป็น |
| **ค่ารหัสทักษะ**<br>_mshr_fk_skill_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmskillentityid ของเอนทิตี mshr_hcmskillentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของทักษะจำเป็น |
| **รหัสระดับของการจัดอันดับ**<br>mshr_ratinglevelid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>ไม่จำเป็นต้องระบุ | ค่าระดับทักษะที่ต้องการซึ่งเลือกไว้ให้กับงาน ตามรูปแบบการประเมินที่มอบหมายให้กับทักษะ |
| **ค่ารหัสระดับการจัดอันดับ**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmratinglevelentityid ของเอนทิตี mshr_hcmratinglevelentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับระดับ |
| **คำอธิบายทักษะ**<br>mshr_skilldescription<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | คำอธิบายทักษะ |
| **คำอธิบายระดับการจัดอันดับ**<br>mshr_ratingleveldescription<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | คำอธิบายของระดับทักษะที่เลือก |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **ค่ารหัสพื้นที่ข้อมูล**<br>_mshr_dataareaid_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: cdm_companyid ของเอนทิตี cdm_company | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | การเชื่อมต่อของค่าคำขอการสรรหาบุคลากรและรหัสทักษะเป็นวิธีการอื่นเพื่อระบุเรกคอร์ดเฉพาะ |
| **รหัสแบบจำลองการจัดอันดับ**<br>mshr_ratingmodelid<br>*สตริง* | อ่าน-เขียน<br>จำเป็นต้องระบุ | แบบจำลองการประเมินที่ใช้เพื่อจัดอันดับทักษะ |
| **ค่ารหัสแบบจำลองการจัดอันดับ**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmratingmodelentityid ของเอนทิตี mshr_hcmratingmodelentity | ตัวระบุที่เฉพาะที่ระบบสร้างขึ้นของแบบจำลองการประเมินที่ใช้ในการจัดอันดับทักษะ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]