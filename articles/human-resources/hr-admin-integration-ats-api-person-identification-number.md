---
title: หมายเลขการระบุรหัสประจำตัวบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้หมายเลขการระบุรหัสประจำตัวบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: a8fa924898472302e67dd4e32251ca0c94da0ea9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798092"
---
# <a name="person-identification-number"></a>หมายเลขการระบุรหัสประจำตัวบุคคล

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้หมายเลขการระบุรหัสประจำตัวบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้อธิบายหมายเลขการระบุรหัสประจำตัวบุคคลสำหรับผู้สมัคร ซึ่งช่วยให้ผู้บริโภคของ API สามารถเขียนหมายเลขการระบุรหัสประจำตัว เช่น หมายเลขประกันสังคมหรือเลขที่หนังสือเดินทางลงในเรกคอร์ดของผู้สมัครได้ หมายเลขการระบุรหัสประจำตัวจะแสดงอยู่ในเรกคอร์ดผู้ปฏิบัติงานแต่ไม่แสดงบนเรกคอร์ดผู้สมัคร ใบสมัครที่รวมสามารถเขียนค่าลงในฐานข้อมูลทรัพยากรบุคคลได้ แต่หมายเลขจะไม่สามารถมองเห็นในทรัพยากรบุคคลได้จนกว่าเรกคอร์ดผู้ปฏิบัติงานของผู้สมัครจะสร้างขึ้น

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้หมายเลขการระบุรหัสประจำตัวบุคคล**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุหลักเฉพาะของเรกคอร์ดหมายเลขการระบุรหัสประจำตัวบุคคล |
| **ชนิดรายการบัญชี**<br>mshr_entrytype<br>*สตริง* | อ่าน-เขียน<br>ไม่จำเป็นต้องระบุ | ค่าอิสระที่จะอ้างอิงชนิดของรายการสำหรับหมายเลขการระบุรหัสประจำตัว |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน-เขียน<br>ไม่จำเป็นต้องระบุ | คำอธิบายของหมายเลขรหัสประจำตัว |
| **วันหมดอายุ**<br>mshr_expirationdate<br>*วันเวลา* | อ่าน-เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่หมายเลขการระบุรหัสประจำตัวหรือเอกสารที่เกี่ยวข้องหมดอายุ |
| **เป็นหลัก**<br>mshr_isprimary<br>*ชุดตัวเลือก mshr_noyes* | อ่าน-เขียน<br>ไม่จำเป็นต้องระบุ | กําหนดว่าหมายเลขการระบุรหัสประจำตัวเป็นเรกคอร์ดหลักหรือไม่สำหรับบุคคลนั้นใช้ชนิดการระบุรหัสประจำตัวนี้ |
| **หมายเลขรหัสประจำตัว**<br>mshr_identificationnumber<br>*สตริง* | อ่าน-เขียน<br>จำเป็นต้องระบุ | หมายเลขรหัสประจำตัว |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน-เขียน<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะของฝ่าย (บุคคล) ที่เป็นเจ้าของหมายเลขการระบุรหัสประจำตัว |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของเอนทิตี้ mshr_direpersonentity | ตัวระบุเฉพาะของฝ่าย (บุคคล) |
| **รหัสชนิดการระบุรหัสประจำตัว**<br>mshr_identificationtypeid<br>*สตริง* | อ่าน-เขียน<br>จำเป็นต้องระบุ | ชนิดของชนิดหมายเลขการระบุรหัสประจำตัว |
| **ค่ารหัสชนิดการระบุรหัสประจำตัว**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmidentificationtypeentityid ของเอนทิตี้ mshr_hcmidentificationtypeentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของชนิดการระบุรหัสประจำตัว |
| **การออกรหัสหน่วยงาน**<br>mshr_issuingagencyid<br>*สตริง* | อ่าน-เขียน<br>ไม่จำเป็นต้องระบุ | หน่วยงานหรือองค์กรที่ออกหมายเลขการระบุรหัสประจำตัว |
| **การออกค่ารหัสหน่วยงาน**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmissuingagencyentityid ของเอนทิตี้ mshr_hcmissuingagencyentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของหน่วยงานการออกหมายเลขการระบุรหัสประจำตัว |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้ ชุดของหมายเลขฝ่าย รหัสชนิดการระบุรหัสประจำตัว และหมายเลขการระบุรหัสประจำตัว |
| **วันที่ออกใช้:**<br>mshr_issuedate<br>*วัน เดือน* | อ่าน-เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่หมายเลขการระบุรหัสประจำตัวได้รับการออก |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]