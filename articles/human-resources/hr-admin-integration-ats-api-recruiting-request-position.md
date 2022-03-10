---
title: ตำแหน่งของคำขอสรรหาบุคลากร
description: หัวข้อนี้อธิบายเอนทิตีตำแหน่งของคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 24ea00c13030d09fb9cda02950ac7b79bfe0d03d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065512"
---
# <a name="recruiting-request-position"></a>ตำแหน่งของคำขอสรรหาบุคลากร


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตีตำแหน่งของคำขอสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>คำอธิบาย

อธิบายตําแหน่งหรือตําแหน่งงานที่จะบรรจุให้กับคำขอการสรรหาบุคลากร การเพิ่มตําแหน่งในคำขอการสรรหาบุคลากรคุณสามารถเลือกได้ คุณสมบัติของตําแหน่งเป็นแบบอ่านอย่างเดียว เนื่องจากคุณสมบัติของตําแหน่งไม่ควรแตกต่างจากคำขอการสรรหาบุคลากร มากกว่าคุณสมบัติในเรกคอร์ดต้นแบบตําแหน่ง ถ้าคุณสมบัติต้องเปลี่ยนแปลง ควรจะจบการคุณสมบัติในเรกคอร์ดต้นแบบตําแหน่งก่อนเพิ่มตําแหน่งลงในคำขอการสรรหาบุคลากร

### <a name="json-representation"></a>การแสดง JSON
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตีการสรรหาบุคลากรที่มีคำขอตำแหน่ง**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ |    รหัสที่ระบบสร้างขึ้นของเรกคอร์ดตําแหน่งของคำขอการสรรหาบุคลากร |
| **รหัสคำขอสรรหา**<br>mshr_recruitingrequestid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | รหัสเฉพาะที่ผู้ใช้สามารถอ่านได้ของคำขอการสรรหาบุคลากร |
| **ค่ารหัสคำขอสรรหา**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmrecruitingrequestentityid ของเอนทิตี mshr_hcmrecruitingrequestentity | ตัวระบุที่ระบบสร้างขึ้นขอคำขอการสรรหาบุคลากรที่กำหนดให้ตำแหน่ง |
| **รหัสตำแหน่ง**<br>mshr_positionid<br>*สตริง* | เขียนเพียงครั้งเดียว<br>จำเป็นต้องระบุ | รหัสเฉพาะที่ผู้ใช้สามารถอ่านได้ของตำแหน่ง |
| **ค่ารหัสตําแหน่ง**<br>_mshr_fk_position_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmpositionv2entityid ของเอนทิตี mshr_hcmpositionv2entity | ตัวระบุที่ระบบสร้างขึ้นของตำแหน่ง |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | คำอธิบายตำแหน่ง |
| **รหัสชนิดตำแหน่ง**<br>mshr_positiontypeid<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | รหัสเฉพาะที่ผู้ใช้สามารถอ่านได้ของชนิดตำแหน่งของตำแหน่งนี้ |
| **ค่ารหัสชนิดตำแหน่ง**<br>_mshr_fk_positiontype_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmpositiontypeentityid ของเอนทิตี mshr_hcmpositiontypeentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของชนิดตำแหน่งของตำแหน่งนี้ |
| **สถานะ**<br>mshr_status<br>ชุดตัวเลือก *RecruitingRequestPositionStatus* | อ่าน/เขียน<br>จำเป็นต้องระบุ | สถานะของตำแหน่งสำหรับคำขอการสรรหาบุคลากร |
| **หมายเลขแผนก**<br>mshr_departmentnumber<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br> | หมายเลขของแผนกของตำแหน่ง |
| **ค่าของรหัสของแผนก**<br>_mshr_fk_department_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_omdepartmententityid ของเอนทิตี mshr_omdepartmententity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของแผนกของตำแหน่งนี้ |
| **รหัสตำแหน่งที่ต้องรายงาน**<br>mshr_reportstopositionid<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | รหัสที่อ่านได้ของผู้ใช้ของตําแหน่งงานซึ่งรายงานตําแหน่งงานสรรหาบุคลากรในลำดับชั้นองค์กร |
| **ค่ารหัสตำแหน่งที่ต้องรายงาน**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmpositionv2entityid ของเอนทิตี mshr_hcmpositionv2entity | รหัสที่ระบบสร้างขึ้นของตําแหน่งที่รายงานตําแหน่งงานสรรหาบุคลากร |
| **หมายเลขบุคลากรที่ต้องรายงาน**<br>mshr_reportstopersonnelnumber<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | รหัสผู้ปฏิบัติงานของผู้ปฏิบัติงานที่จะรายงานผู้สมัครการจ้างงานให้ |
| **ค่ารหัสผู้ปฏิบัติงานที่ต้องรายงาน**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmworkerbaseentityid ของเอนทิตี mshr_hcmworkerbaseentity | รหัสที่ระบบสร้างขึ้นของผู้ปฏิบัติงานที่จะรายงานผู้สมัครการจ้างงานให้ |
| **มิติทางการเงิน**<br>mshr_financialdimension<br>*สตริง* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ | มิติทางการเงิน (ตัวอย่างเช่น ศูนย์ต้นทุน) ที่มอบหมายให้กับตําแหน่ง มิติทางการเงินให้กำหนดกับแต่ละตําแหน่งต่อนิติบุคคล ศูนย์ต้นทุนที่กําหนดในมิติสามารถเข้าถึงผ่านเอนทิตี mshr_dimattributeomcostcenterentity ได้ |
| **รหัสพื้นที่ข้อมูล**<br>mshr_dataareaid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุนิติบุคคล (บริษัท) ของตำแหน่งคำขอการสรรหาบุคลากร |
| **ค่ารหัสพื้นที่ข้อมูล**<br>_mshr_dataareaid_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: cdm_companyid ของเอนทิตี cdm_company | ค่า GUID ที่ระบบสร้างขึ้นซึ่งระบุนิติบุคคล (บริษัท) สำหรับตำแหน่งคำขอการสรรหาบุคลากร |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | การเชื่อมต่อของค่าคำขอการสรรหาบุคลากรและรหัสตําแหน่งเป็นวิธีการอื่นเพื่อระบุเรกคอร์ดเฉพาะ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
