---
title: คำขอสรรหาบุคลากร
description: หัวข้อนี้อธิบายเอนทิตีคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd2f2fc74261c6eea3033567fe020c4e03c60637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805189"
---
# <a name="recruiting-request"></a>คำขอสรรหาบุคลากร

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmrecruitingrequestentity

### <a name="description"></a>คำอธิบาย

อธิบายคำขอการสรรหาบุคลากรให้กับงาน

### <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสคำขอสรรหา**<br>mshr_recruitingrequestid<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | รหัสเฉพาะที่ผู้ใช้สามารถอ่านได้ของการร้องขอที่แสดงในแอพลิเคชัน HR ลำดับหมายเลข |
| **รหัสเอนทิตีคำขอการสรรหาบุคลากร**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงคำขอการสรรหาบุคลากรโดยเฉพาะ |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ<br> | ระบุนิติบุคคล (บริษัท) ของคำขอการสรรหาบุคลากร |
| **ค่ารหัสพื้นที่ข้อมูล**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: cdm_companyid ของเอนทิตี cdm_company | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) สำหรับคำขอการสรรหาบุคลากร |
| **หมายเลขบุคลากรของผู้จัดการที่จ้างงาน**<br>mshr_hiringmanagerpersonnelnumber<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขบุคลากรของผู้จัดการฝ่ายการจ้างงานที่เชื่อมโยงกับคำขอการสรรหาบุคลากรนี้ |
| **ค่ารหัสการว่าจ้างผู้จัดการ**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmworkerbaseentityid ของเอนทิตี mshr_hcmworkerbaseentity | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุผู้จัดการที่เชื่อมโยงกับคำขอการสรรหาบุคลากร |
| **หมายเลขฝ่ายของผู้สรรหาบุคลากร**<br>mshr_recruiterpartynumber<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขฝ่าย (บุคคล) ของผู้สรรหาที่เลือกสำหรับคำขอ |
| **ค่ารหัสผู้สรรหา**<br>_mshr_fk_recruiter_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของเอนทิตี้ mshr_direpersonentity | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุผู้สรรหาที่เชื่อมโยงกับคำขอการสรรหาบุคลากร |
| **สถานะ**<br>mshr_status<br>*ชุดตัวเลือก RecruitingRequestStatus* | อ่าน/เขียน<br>จำเป็นต้องระบุ<br> | บ่งชี้สถานะของคำขอสรรหาบุคลากรปัจจุบัน |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | อธิบายคำขแ |
| **รหัสที่ตั้งของคำขอสรรหาบุคลากร**<br>mshr_recruitingrequestlocationid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ตัวระบุเฉพาะที่อ่านได้ของผู้ใช้ของสถานที่งานที่เชื่อมโยงกับคำขอนี้ |
| **ค่ารหัสที่ตั้งของการสรรหาบุคลากร**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmrecruitingrequestlocationentityid ของ mshr_hcmrecruitingrequestlocationentity entity | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระถานที่ร้องขอการสรรหาบุคลากรที่เลือกสำหรับคำขอ |
| **ข้อคิดเห็น**<br>mshr_comments<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ข้อคิดเห็นเกี่ยวกับคำขอใช้โดยการจ้างงานผู้จัดการและผู้สรรหา |
| **รหัสงาน**<br>mshr_jobid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ |   ตัวระบุเฉพาะที่อ่านได้ของผู้ใช้ของงานที่แบ่งปันโดยตำแหน่งทั้งหมดที่เชื่อมโยงกับคำขอนี้ |
| **ค่ารหัสงาน**<br>_mshr_fk_job_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmjobentityid ของ mshr_hcmjobentity entity | ตัวระบุเฉพาะที่สร้างโดยระบบของงานที่แบ่งปันโดยตำแหน่งทั้งหมดที่เชื่อมโยงกับคำขอการสรรหาบุคลากรนี้ |
| **รหัสชื่อ**<br>mshr_titleid<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่อ่านได้ของผู้ใช้ของตำแหน่งงานที่เชื่อมโยงกับคำขอนี้ |
| **ค่ารหัสชื่อ**<br>_mshr_fk_title_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmtitleid ของเอนทิตี mshr_hcmtitleentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับตำแหน่งงานที่เลือกสำหรับคำขอการสรรหาบุคลากร |
| **รหัสฟังก์ชันงาน**<br>mshr_jobfunctionid<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_jobfunctionid ของเอนทิตี mshr_hcmjobfunctionentity | ตัวระบุเฉพาะที่อ่านได้ของผู้ใช้ของฟังก์ชันงานที่เชื่อมโยงกับคำขอนี้ |
| **การเทียบเท่าเต็มเวลาพื้นฐาน**<br>mshr_defaultfulltimeequivalency<br>*สองเท่า* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ค่าเทียบเท่าเต็มเวลาของงาน โดยที่ 1.0 แสดงถึงผู้ปฏิบัติงานเต็มเวลา |
| **ประเภทงานตามระเบียบบังคับ**<br>mshr_regulatoryjobcategory<br>ชุดตัวเลือก *RegulatoryJobCategory* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | ประเภทงาน EEO ของฟังก์ชันงานที่เลือกของงาน ค่าที่ถูกต้องที่รวมอยู่ในชุดตัวเลือก HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) |
| **รหัสชนิดงาน**<br>mshr_jobtypeid<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | ชนิดของงานที่เชื่อมโยงกับตำแหน่ง ชนิดงานเป็นค่าที่กําหนดโดยผู้ใช้ ซึ่งพร้อมใช้งานในเอนทิตี mshr_hcmjobtypeentity |
| **ค่ารหัสชนิดงาน**<br>_mshr_fk_jobtype_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmjobtypeentityid ของเอนทิตี mshr_hcmjobtypenentity | ตัวระบุเฉพาะที่สร้างโดยระบบของชนิดงานที่เชื่อมโยงกับงานสำหรับคำขอการสรรหาบุคลากรนี้ |
| **สถานะยกเว้น**<br>mshr_exemptstatus<br>ชุดตัวเลือก *JobExemptStatus* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | สถานะยกเว้น FLSA ตามชนิดงาน |
| **วันที่เริ่มต้นโดยประมาณ**<br>mshr_estimatedstartdate<br>*วัน เดือน* | อ่าน/เขียน<br>จำเป็นต้องระบุ | วันที่ประเมินที่ผู้สมัครจะเริ่มต้นงาน |
| **คำอธิบายภายนอก**<br>mshr_externaldescription<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายงานที่/ตําแหน่งที่เชื่อมต่อกับผู้สมัคร | 
| **ขีดจำกัดต่ำสุดของค่าตอบแทน**<br>mshr_compensationlowthreshold<br>*สองเท่า* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ขอบเขตล่างของระดับค่าตอบแทน |
| **จุดควบคุมค่าตอบแทน**<br>mshr_compensationcontrolpoint<br>*สองเท่า* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดควบคุมเกี่ยวกับระดับค่าตอบแทน |
| **ขีดจำกัดสูงสุดของค่าตอบแทน**<br>mshr_compensationhighthreshold<br>*สองเท่า* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ขอบเขตบนของระดับค่าตอบแทน |
| **ระดับค่าตอบแทน**<br>mshr_compensationlevelid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระดับค่าตอบแทนของงาน งานสามารถตั้งค่าด้วยระดับค่าตอบแทนหลายระดับได้ แอททริบิวต์นี้จะบ่งชี้ระดับค่าตอบแทนของงานที่เลือกของคำขอนี้ |
| **รหัสค่าตอบแทนงาน**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmjobcompensationentityid ของเอนทิตี mshr_hcmjobcompensationentity | ตัวระบุเฉพาะที่สร้างโดยระบบของค่าตอบแทนที่เชื่อมโยงกับงานสำหรับคำขอการสรรหาบุคลากรนี้ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
