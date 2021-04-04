---
title: การคัดเลือกบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้การสรรหาบุคลากรของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467252"
---
# <a name="person-screening"></a>การคัดเลือกบุคคล

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้การสรรหาบุคลากรของบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpersonscreeningentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะอธิบายถึงการสรรหาผู้สมัครที่ผ่านหรือต้องผ่านสำหรับการจ้างงาน

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้การสรรหาของบุคคล**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุหลักเฉพาะของเรกคอร์ดการสรรหาของบุคคล |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | หมายเลขฝ่าย (บุคคล) ที่เชื่อมโยงกับผู้สมัคร |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล) |
| **รหัสชนิดการคัดเลือก**<br>mshr_screeningtypeid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ<br>คีย์นอก: ScreeningType | ตัวระบุของชนิดการคัดเลือกที่กําหนดในทรัพยากรบุคคล |
| **ค่ารหัสชนิดการคัดเลือก**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmscreeningtypeentityid ของ mshr_hcmscreeningtypeentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับชนิดการคัดเลือกในเอนทิตี้ที่เกี่ยวข้อง |
| **ต้องการภายใน**<br>mshr_requiredby<br>*วันเวลา* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่การคัดเลือกจำเป็นที่จะทำให้เสร็จสิ้น |
| **สถานะ**<br>mshr_status<br>*การกำหนดตัวเลือก mshr_hcmcompletionstatus*<br>อ่าน/เขียน<br>จำเป็นต้องระบุ | แสดงสถานะของผู้สมัครสำหรับการคัดเลือก |
| **วันที่เสร็จสมบูรณ์**<br>mshr_completeddate<br>*วันเวลา* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่การคัดเลือกเสร็จสมบูรณ์ |
| **บันทึกย่อ**<br>mshr_note<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเหตุที่ใช้โดยผู้จัดการการจ้างงานหรือผู้จัดหาบุคลากร |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]