---
title: ที่อยู่ของบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้ที่อยู่ของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 9911362ff8260860864cfe24f0b60f59adb77186
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125893"
---
# <a name="person-address"></a>ที่อยู่ของบุคคล

หัวข้อนี้อธิบายเอนทิตี้ที่อยู่ของบุคคลสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmpersonaddressentities

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้ประกอบด้วยรายการของที่อยู่ไปรษณีย์สำหรับเรกคอร์ดผู้สมัคร

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ที่อยู่ของบุคคล**<br>mshr_hcmpersonaddressentityid<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับบันทึกเอนทิตี้ |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | รหัสของบันทึกฝ่าย (บุคคล) ที่เกี่ยวข้อง |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล) |
| **รหัสสถานที่**<br>mshr_locationid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | รหัสสถานที่เก็บของบันทึกที่อยู่ ตั้งค่าในเอนทิตี้ mshr_logisticspostaladdresslocationcdsentity |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | คำอธิบายของที่อยู่ของผู้สมัคร |
| **บทบาท**<br>mshr_roles<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | บทบาทกำหนดให้สำหรับที่อยู่นี้ สามารถกำหนดบทบาทได้มากกว่ากว่าหนึ่งบทบาท แต่ละบทบาทควรถูกแยกด้วยเครื่องหมายอัฒภาค ค่าที่ถูกต้องที่มีอยู่ในเอนทิตี้ mshr_logisticslocationroleentity |
| **ถนน**<br>mshr_street<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเลขถนน |
| **เมือง**<br>mshr_city<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | เมืองของที่อยู่ ตั้งค่าในเอนทิตี้ mshr_logisticsaddresscityentity |
| **จังหวัด**<br>mshr_state<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รัฐของที่อยู่ ตั้งค่าในเอนทิตี้ mshr_logisticsaddressstateentity |
| **เขต**<br>mshr_county<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ประเทศของที่อยู่ ตั้งค่าในเอนทิตี้ mshr_logisticsaddresscountyentity |
| **รหัสไปรษณีย์**<br>mshr_zipcode<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รหัสไปรษณีย์ของที่อยู่ ตั้งค่าในเอนทิตี้ mshr_logisticsaddresspostalcodeentity |
| **รหัสภูมิภาคของประเทศ**<br>mshr_countryregionid<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ประเทศหรือภูมิภาคของที่อยู่ |
| **ค่ารหัสภูมิภาค/ประเทศ**<br>_mshr_fk_countriregion_id_value<br>*GUID* | อ่านอย่างเดียว<br>ไม่จำเป็นต้องระบุ<br>คีย์นอก: mshr_logisticaddresscountryregionentityid ของ mshr_logisticsaddresscountryregionentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของประเทศ/ภูมิภาคของที่อยู่ |
| **เป็นหลัก**<br>mshr_isprimary<br>*ชุดตัวเลือก mshr_noyes* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ระบุว่าที่อยู่นี้เป็นที่อยู่หลักสำหรับบุคคลของบทบาทที่กําหนดหรือไม่ |
| **เป็นส่วนตัว**<br>mshr_isprivate<br>*ชุดตัวเลือก mshr_noyes* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ระบุว่าที่อยู่นี้เป็นที่อยู่ส่วนตัวสำหรับบุคคลหรือไม่ |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่ใช้เป็นตัวระบุหลักของบันทึกเอนทิตี้ ชุดของหมายเลขฝ่ายและรหัสสถานที่ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

