---
title: การศึกษาของบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้การศึกษาของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: c04a9c973e5a93b716889bdc0bb5f59ff5bbdd7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053766"
---
# <a name="person-education"></a>การศึกษาของบุคคล

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้การศึกษาของบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpersoneducationentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้ประกอบด้วยประวัติการศึกษาของบุคคลที่เป็นผู้สมัคร การศึกษาถูกเชื่อมโยงกับเรกคอร์ดบุคคลซึ่งเปิดใช้งานการศึกษาที่จะเชื่อมโยงกับบทบาทอื่นๆที่สร้างไว้ให้กับบุคคลนอกเหนือจากเรกคอร์ดผู้สมัคร (ผู้ปฏิบัติงาน ผู้รับเหมา และอื่นๆ)

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้การศึกษาของบุคคล**<br>mshr_hcmpersoneducationentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้การศึกษาของบุคคล |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดฝ่าย (บุคคล) สำหรับผู้สมัคร |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดบุคคลของผู้สมัคร |
| **พื้นฐานเครดิต**<br>mshr_creditbasis<br>*การกำหนดตัวเลือก mshr_hcmeducationcreditbasis* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | พื้นฐานเครดิตของระดับการศึกษา |
| **เครดิตที่เสร็จสมบูรณ์**<br>mshr_creditscompleted<br>*ทศนิยม* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จํานวนเครดิตที่เสร็จสมบูรณ์สำหรับการศึกษา |
| **เครดิตสะสม**<br>mshr_creditsearned<br>*ทศนิยม* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จํานวนของเครดิตสะสมสำหรับเรกคอร์ดการศึกษาสำหรับระดับหนึ่งในระหว่างดำเนินการ |
| **เครดิตที่ต้องใช้**<br>mshr_creditsneeded<br>*ทศนิยม* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จํานวนเครดิตที่ต้องใช้สำหรับระดับหนึ่งในระหว่างดำเนินการ |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายของระดับผู้สมัคร |
| **รหัสระดับการศึกษา**<br>mshr_educationlevelid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสของระดับการศึกษา | 
| **ค่ารหัสระดับการศึกษา**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmeducationdegreeentityid ของ เอนทิตี้ mshr_hcmeducationdegreeentity | ตัวระบุที่ระบบสร้างขึ้นสำหรับเรกคอร์ดระดับการศึกษา ตัวระบุนี้จะให้องศาและระดับการศึกษาที่กําหนดไว้สำหรับองค์กร |
| **รหัสสาขาวิชาการศึกษา**<br>mshr_educationdisciplineid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ<br>คีย์นอก: EducationDiscipline | รหัสของสาขาวิชาการศึกษา |
| **ค่ารหัสสาขาวิชาการศึกษา**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmeducationdisciplineentityid ของ mshr_hcmeducationdisciplineentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของสาขาวิชาการศึกษาของเรกคอร์ดการศึกษา |
| **การมุ่งเน้นวิชารอง**<br>mshr_secondaryemphasis<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | การมุ่งเน้นวิชารองของระดับที่ได้สะสม |
| **รหัสสถาบันการศึกษา**<br>mshr_educationinstitutionid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสของสถาบันการศึกษาที่เข้าร่วม |
| **ค่ารหัสสถาบันการศึกษา**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmeducationinstitutionentityid ของ mshr_hcmeducationinstitutionentity | ตัวระบุที่ระบบสร้างขึ้นของสถาบันการศึกษา |
| **วันที่เริ่มต้น**<br>mshr_startdate<br>*วันเวลา* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่เริ่มต้นของการศึกษาสำหรับระดับที่ได้เรียน |
| **วันที่สิ้นสุด**<br>mshr_enddate<br>*วันเวลา* | อ่าน/เขียน<br>จำเป็นต้องระบุ | วันที่ที่หนังสือรับรองได้รับการออก |
| **ระยะเวลา**<br>mshr_duration<br>*ทศนิยม* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ช่วงเวลาของเวลาของเรกคอร์ดการศึกษา |
| **หน่วยระยะเวลา**<br>mshr_durationunit<br>*ตัวเลือกการตั้งค่า mshr_periodunit* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หน่วยของเวลาที่เชื่อมโยงกับช่วงเวลาของเรกคอร์ดการศึกษา |
| **คะแนนเฉลี่ย**<br>mshr_gradepointaverage<br>*ทศนิยม* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คะแนนเฉลี่ยสะสมสำหรับปริญญา |
| **ระดับคะแนน**<br>mshr_gradescale<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระดับที่ถูกใช้สะหรับคะแนนเฉลี่ย |
| **บันทึกย่อ**<br>mshr_notes<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเหตุที่ใช้โดยผู้สรรหาหรือผู้จัดการการจ้างงาน |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่ใช้เป็นตัวระบุหลักอื่นของเรกคอร์ดเอนทิตี้ ชุดของหมายเลขฝ่าย รหัสสาขาวิชาการศึกษา รหัสสถาบันการศึกษา และรหัสระดับการศึกษา |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]