---
title: ทักษะของบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้ทักษะของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: d2721e3eace401537e85e57b5895d508317e6c4b71d481d15ff176b786a937e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756207"
---
# <a name="person-skill"></a>ทักษะของบุคคล

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้ทักษะของบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpersonskillentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้อธิบายถึงทักษะของผู้สมัคร

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ทักษะของบุคคล**<br>mshr_hcmpersonskillentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับบันทึกเอนทิตี้ |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ |   รหัสของบันทึกฝ่าย (บุคคล) ที่เกี่ยวข้อง |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล) |
| **ผู้รับรอง**<br>mshr_certifier<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขบุคลากรของผู้ปฏิบัติงานที่ได้รับการรับรองทักษะนี้ |
| **ค่ารหัสผู้รับรอง**<br>_mshr_fk_certifier_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmworkerentityid ของ mshr_hcmworkerentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดผู้ปฏิบัติงานสำหรับผู้ปฏิบัติงานที่ได้รับการรับรองทักษะ |
| **รหัสทักษะ**<br>mshr_skillid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตัวระบุของทักษะที่กําหนดในทรัพยากรบุคคล |
| **ค่ารหัสทักษะ**<br>_mshr_fk_skill_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmskillentityid ของ mshr_hcmskillentity | ตัวระบุที่ระบบสร้างขึ้นของทักษะที่เลือก |
| **ปีของประสบการณ์ทำงาน**<br>mshr_yearsofexperience<br>*ทศนิยม* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ปีประสบการณ์ที่ผู้สมัครมีในทักษะนี้ |
| **รหัสการจัดอันดับ**<br>mshr_ratingid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ชนิดระดับการจัดอันดับ สำหรับเอนทิตี้นี้ ค่าเป็น **ทักษะ** |
| **ชนิดระดับ**<br>mshr_leveltype<br>*การกำหนดตัวเลือก mshr_hrmskillleveltype* | อ่าน/เขียน<br>จำเป็นต้องระบุ | การจัดประเภทชนิดให้กับระดับที่มอบหมายให้กับทักษะ |
| **รหัสระดับ**<br>mshr_levelid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | รหัสของระดับการจัดอันดับที่ผู้สมัครมีสำหรับทักษะนี้ |
| **ค่ารหัสระดับการจัดอันดับ**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmratinglevelentityid ของ mshr_hcmratinglevelentity | ตัวระบุที่ระบบสร้างขึ้นของระดับการจัดอันดับ |
| **วันที่ระดับ**<br>mshr_leveldate<br>*วันเวลา* | อ่าน/เขียน<br>จำเป็นต้องระบุ | วันที่ที่ผู้สมัครถูดจัดอันดับในทักษะ |
| **ผู้ตรวจสอบระดับการจัดอันดับ**<br>mshr_ratinglevelexaminer<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขบุคลากรของผู้ปฏิบัติงานที่จัดอันดับผู้สมัคร |
| **ค่ารหัสผู้ตรวจสอบระดับการจัดอันดับ**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmworkerentityid ของ mshr_hcmworkerentity | ตัวระบุที่ระบบสร้างขึ้นของผู้ปฏิบัติงานที่ตรวจสอบระดับทักษะของผู้สมัคร |
| **ตรวจสอบแล้ว**<br>mshr_verified<br>*ตัวเลือกการตั้งค่า mshr_noyes* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ระบุว่าระดับทักษะที่ประเมินได้ตรวจสอบแล้วหรือไม่ |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้ ชุดของหมายเลขฝ่าย ชนิดระดับ รหัสทักษะ และวันที่ระดับ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]