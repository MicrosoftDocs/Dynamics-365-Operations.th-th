---
title: ประสบการณ์การทำงานของบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้ประสบการณ์การทำงานของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 1defaff8397c41feedbd85893766106338a28941
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798068"
---
# <a name="person-professional-experience"></a>ประสบการณ์การทำงานของบุคคล

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้ประสบการณ์การทำงานของบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะอธิบายถึงประสบการณ์การทำงานหรือประวัติงานของผู้สมัคร

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ประสบการณ์การทำงานของบุคคล**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับบันทึกเอนทิตี้ |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะของเรกคอร์ดบุคคลสำหรับผู้สมัคร |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้บุคคล |
| **ตําแหน่งนายจ้าง**<br>mshr_employerposition<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตําแหน่งที่ค้างอยู่โดนผู้สมัครขณะอยู่ภายใต้การจ้างงาน |
| **ชื่อนายจ้าง**<br>mshr_employername<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ชื่อของนายจ้าง |
| **สถานที่ของนายจ้าง**<br>mshr_employerlocation<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | สถานที่ของนายจ้าง ความยาวสูงสุด: 60 ไม่มีรูปแบบที่กําหนดหรือจำป็น |
| **โทรศัพท์**<br>mshr_phone<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขโทรศัพท์ของนายจ้าง |
| **URL**<br>mshr_url<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | URL ของเว็บไซต์ของนายจ้าง |
| **วันที่เริ่มต้น**<br>mshr_startdate<br>*วันเวลา* | อ่าน/เขียน<br>จำเป็นต้องระบุ | วันที่เริ่มต้นของการจ้างงานของผู้สมัคร |
| **วันที่สิ้นสุด**<br>mshr_enddate<br>*วันเวลา* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่สิ้นสุดของการจ้างงานของผู้สมัครหรือ null ถ้าผู้สมัครยังคงได้รับการว่าจ้างที่นี่ |
| **อนุญาตให้ติดต่อนายจ้าง**<br>mshr_allowcontactemployer<br>*การกำหนดตัวเลือก mshr_hrmblankyesno* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุว่าผู้สมัครอนุญาตให้ติดต่อนายจ้างก่อนหน้านี้หรือไม่ |
| **บันทึกย่อ**<br>mshr_note<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเหตุที่ใช้โดยผู้สรรหาหรือผู้จัดการการจ้างงาน |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่ใช้เป็นตัวระบุหลักของบันทึกเอนทิตี้ ชุดของหมายเลขฝ่าย วันที่เริ่มต้น ตําแหน่งนายจ้าง และชื่อนายจ้าง |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]