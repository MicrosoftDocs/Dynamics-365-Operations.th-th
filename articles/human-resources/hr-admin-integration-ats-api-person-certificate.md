---
title: ใบรับรองของบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้ใบรับรองของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466531"
---
# <a name="person-certificate"></a>ใบรับรองของบุคคล

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้ใบรับรองของบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpersoncertificateentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะอธิบายถึงใบรับรองวิชาชีพของผู้สมัคร

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ใบรับรองของบุคคล**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้ใบรับรองของบุคคล |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | รหัสฝ่าย (บุคคล) ของผู้สมัคร |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล) |
| **รหัสชนิดใบรับรอง**<br>mshr_certificatetypeid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ |  ตัวระบุของชนิดใบรับรองที่กําหนดในทรัพยากรบุคคล |
| **ค่ารหัสชนิดใบรับรอง**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmcertificatetypeentityid ของ mshr_hcmcertificatetypeentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของชนิดใบรับรองในเอนทิตี้ที่เกี่ยวข้อง |
| **วันที่เริ่มต้น**<br>mshr_startdate<br>*วันเวลา* | อ่าน/เขียน<br>จำเป็นต้องระบุ | วันที่ที่ใบรับรองได้รับการออก |
| **วันที่สิ้นสุด**<br>mshr_enddate<br>*วันเวลา* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่ใบรับรองจะหมดอายุ |
| **บันทึกย่อ**<br>mshr_notes<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเหตุที่ใช้โดยผู้จัดการการจ้างงานหรือผู้จัดหาบุคลากร |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ |  ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้ ชุดของหมายเลขฝ่าย รหัสชนิดใบรับรองและวันที่เริ่มต้น |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]