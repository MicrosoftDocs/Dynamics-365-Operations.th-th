---
title: ผู้สมัครที่จะจ้างงาน
description: บทความนี้อธิบายเอนทิตี้ผู้สมัครที่จะจ้างงานสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 12/05/2021
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
ms.openlocfilehash: 7c243bdf81beabe9e1ee429227a6edf4d4864bfb
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832010"
---
# <a name="candidate-to-hire"></a>ผู้สมัครที่จะจ้างงาน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายเอนทิตี้ผู้สมัครที่จะจ้างงานสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmcandidatetohireentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะให้รายละเอียดผู้สมัครที่ใช้ในการสร้างผู้ปฏิบัติงานใน Dynamics 365 Human Resources ใช้ในการอ่านเรกคอร์ดผู้สมัครทั้งหมดและสร้างเรกคอร์ดผู้สมัครภายในและภายนอก ซึ่งช่วยให้คุณสามารถสร้างรายละเอียดส่วนตัวสำหรับผู้สมัครใหม่ได้

เมื่อคุณสร้างเรกคอร์ดผู้สมัครภายนอกที่จะเป็นเรกคอร์ดบุคคลใหม่ในระบบ คุณต้องไม่กําหนดหมายเลขฝ่าย (บุคคล) ที่คุณลงรายการบัญชีเรกคอร์ดผู้สมัครใหม่ เรกคอร์ดเอนทิตี้บุคคลใหม่จะถูกสร้างขึ้นด้วยเรกคอร์ดผู้สมัครใหม่

เมื่อคุณสร้างเรกคอร์ดผู้สมัครภายใน (ผู้สมัครสำหรับตำแหน่งที่มีเรกคอร์ดพนักงานอยู่กับบริษัทอยู่แล้ว) กําหนดหมายเลขฝ่าย (บุคคล) ของเรกคอร์ดที่มีอยู่แล้วสำหรับบุคคลในคุณสมบัติ mshr_partynumber ในเรกคอร์ดผู้สมัครแทนที่จะกําหนดข้อมูลส่วนบุคคล (เช่น ชื่อ เพศ หรือวันเกิด) ที่จะใช้เพื่อสร้างเรกคอร์ดบุคคลใหม่

## <a name="json-representation"></a>การแสดง JSON

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
            "mshr_militaryserviceenddate": "Date",
            "mshr_militaryservicestartdate": "Date"
        }
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ผู้สมัครที่จะจ้างงาน**<br>mshr_hcmcandidatetohireentityid<br>GUID | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้ |
| **รหัสผู้สมัคร**<br>mshr_candidateid<br>สตริง | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุเฉพาะสำหรับเอนทิตี้ |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>สตริง | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | หมายเลขฝ่าย (บุคคล) ของเรกคอร์ดบุคคลของผู้สมัคร |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>GUID | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_direpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดฝ่าย (บุคคล) ของผู้สมัคร |
| **ชนิดฝ่าย**<br>mshr_partytype<br>ตัวเลือกการตั้งค่า mshr_dirpartytype | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ชนิดฝ่ายของเรกคอร์ดตามที่กําหนดในตัวเลือกการตั้งค่า mshr_dirpartytype สำหรับเอนทิตี้นี้นี้ ชนิดจะเป็น "บุคคล" เสมอ |
| **รหัสคำขอสรรหา**<br>mshr_recruitingrequestid<br>สตริง | เขียนเพียงครั้งเดียว<br>ไม่จำเป็นต้องระบุ | อ้างอิงคำขอการสรรหาที่ผู้สมัครนี้ตอบสนอง |
| **ค่ารหัสคำขอสรรหา**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmrecruitingrequestentityid ของ mshr_hcmrecruitingrequestentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับคำขอการสรรหาที่ผู้สมัครนี้ตอบสนอง |
| **รหัสตำแหน่ง**<br>mshr_positionid<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสของตําแหน่งที่ผู้สมัครได้รับการพิจารณา |
| **ค่ารหัสตําแหน่ง**<br>_mshr_fk_position_if_value<br>GUID | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmpositionv2entityid ของ mshr_hcmpositionv2entity | ตัวระบุที่ระบบสร้างขึ้นของตําแหน่งสำหรับผู้สมัครได้รับการพิจารณา |
| **ชื่อ**<br>mshr_firstname<br>สตริง | อ่าน/เขียน<br>จำเป็นต้องระบุ | ชื่อของผู้สมัคร |
| **ชื่อกลาง**<br>mshr_middlename<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ชื่อกลางของผู้สมัคร |
| **คำนำหน้านามสกุล**<br>mshr_lastnameprefix<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | คำนำหน้านามสกุลของผู้สมัคร |
| **นามสกุล**<br>mshr_lastname<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | นามสกุลของผู้สมัคร |
| **เพศ**<br>mshr_gender<br>การกำหนดตัวเลือก mshr_hcmpersongender | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เพศของผู้สมัคร |
| **วันเกิด**<br>mshr_birthdate<br>วันที่และเวลา | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันเกิดของผู้สมัคร |
| **รหัสประเทศของสัญชาติ**<br>mshr_citizenshipcountrycode<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุประเทศที่ผู้สมัครมีสัญชาติ รหัสประเทศที่ถูกต้องอยู่ใน mshr_logisticaddresscountryregionentity |
| **รหัสสถานะทหารผ่านศึก**<br>mshr_veteranstatusid<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุว่าสถานะทหารผ่านศึกของผู้สมัคร |
| **ค่ารหัสสถานะทหารผ่านศึก**<br>_mshr_fk_veteranstatus_id_value<br>GUID | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmveteranstatusentityid ของ mshr_hcmveteranstatusentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้สถานะทหารผ่านศึก |
| **วันที่เริ่มต้นการรับราชการทหาร**<br>mshr_militaryservicestartdate<br>วันที่และเวลา | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่เริ่มต้นของการรับราชการทหารของผู้สมัคร |
| **วันที่สิ้นสุดการรับราชการทหาร**<br>mshr_militaryserviceenddate<br>วันที่และเวลา | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่สิ้นสุดของการรับราชการทหารของผู้สมัคร |
| **เป็นทหารผ่านศึกที่เป็นผู้ทุพพลภาพ**<br>mshr_isdisabledveteran<br>ตัวเลือกการตั้งค่า mshr_noyes | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุถ้าผู้สมัครปิดใช้งานสถานะทหารผ่านศึก |
| **วันที่พร้อมใช้งาน**<br>mshr_availabilitydate<br>วันที่และเวลา | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่แรกสุดที่ผู้สมัครพร้อมจะเข้างาน |
| **ยินดีที่จะย้ายที่อยู่หรือไม่**<br>mshr_iswillingtorelocate<br>ตัวเลือกการตั้งค่า mshr_noyes | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | บ่งชี้ว่าผู้สมัครสมัครยินดีที่จะย้ายตําแหน่งหรือไม่ |
| **ข้อคิดเห็น**<br>mshr_comments<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ข้อคิดเห็นที่ให้ผู้สรรหาหรือว่าจ้างผู้จัดการนำไปใช้ |
| **ผลลัพธ์การรวมแอปพลิเคชัน**<br>mshr_applcantintegrationresult<br>ตัวเลือกการตั้งค่า mshr_applicantintegrationresult | อ่าน/เขียน<br>จำเป็นต้องระบุ | สถานะของผู้สมัครในกระบวนการว่าจ้างที่เกี่ยวข้องกับการรวม |
| **อย่าจ้างรหัสโค้ดเหตุผล**<br>mshr_donothirereasoncodeid<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสเหตุผลอาจระบุได้เมื่อสถานะ (ผลลัพธ์การรวมแอปพลิเคชัน) ถูกตั้งค่าเป็น "ไม่จ้างงาน" |
| **ค่ารหัสโค้ดเหตุผล**<br>_mshr_fk_reasoncode_id_value<br>GUID | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmreasoncodeentityid ของเอนทิตี้ mshr_hcmreasoncodeentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับรหัสเหตุผล **ไม่ต้องจ้างงาน** |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid<br>สตริง | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ |  ระบุเอนทิตี้นิติบุคคล (บริษัท) |
| **ค่ารหัสพื้นที่ข้อมูล**<br>_mshr_dataareaid_id_value<br>GUID | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: cdm_companyid ของเอนทิตี cdm_company | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
