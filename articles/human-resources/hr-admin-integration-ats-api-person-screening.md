---
title: การคัดเลือกบุคคล
description: บทความนี้อธิบายเอนทิตี้การสรรหาบุคลากรของบุคคลสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831902"
---
# <a name="person-screening"></a>การคัดเลือกบุคคล


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายเอนทิตี้การสรรหาบุคลากรของบุคคลสำหรับ Dynamics 365 Human Resources

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
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **บันทึกย่อ**<br>mshr_note<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเหตุที่ใช้โดยผู้จัดการการจ้างงานหรือผู้จัดหาบุคลากร |
| **ต้องการภายใน**<br>mshr_requiredby<br>*วันเวลา* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่การคัดเลือกจำเป็นที่จะทำให้เสร็จสิ้น |
| **สถานะ**<br>mshr_status<br>*การกำหนดตัวเลือก mshr_hcmcompletionstatus*|อ่าน/เขียน<br>จำเป็นต้องระบุ | แสดงสถานะของผู้สมัครสำหรับการคัดเลือก |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | หมายเลขฝ่าย (บุคคล) ที่เชื่อมโยงกับผู้สมัคร |
| **รหัสชนิดการคัดเลือก**<br>mshr_screeningtypeid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ<br>คีย์นอก: ScreeningType | ตัวระบุของชนิดการคัดเลือกที่กําหนดในทรัพยากรบุคคล |
| **ค่ารหัสชนิดการคัดเลือก**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmscreeningtypeentityid ของ mshr_hcmscreeningtypeentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับชนิดการคัดเลือกในเอนทิตี้ที่เกี่ยวข้อง |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* |  อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้ |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล) |
| **รหัสเอนทิตี้การสรรหาของบุคคล**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น| ตัวระบุหลักเฉพาะของเรกคอร์ดการสรรหาของบุคคล |
| **วันที่เสร็จสมบูรณ์**<br>mshr_completeddate<br>*วันเวลา* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | วันที่ที่การคัดเลือกเสร็จสมบูรณ์ |


## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
