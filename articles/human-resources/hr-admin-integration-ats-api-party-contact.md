---
title: ผู้ติดต่อฝ่าย
description: หัวข้อนี้อธิบายเอนทิตี้ผู้ติดต่อฝ่ายสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: fca72cb73ef46a4eeee27d43e22254373a425a36
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067187"
---
# <a name="party-contact"></a>ผู้ติดต่อฝ่าย


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้ผู้ติดต่อฝ่ายสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_dirpartycontactentities

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะอธิบายถึงข้อมูลผู้ติดต่อของผู้สมัคร รวมถึงบัญชีโทรศัพท์ อีเมล และบัญชีสื่อทางสังคม

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ผู้ติดต่อฝ่าย**<br>mshr_dirpartycontactentityid<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับบันทึกเอนทิตี้ |
| **หมายเลขฝ่าย**<br>mshr_partynumber<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | รหัสของบันทึกฝ่าย (บุคคล) ที่เกี่ยวข้อง |
| **ค่ารหัสบุคคล**<br>_mshr_fk_person_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity | ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล) |
| **รหัสสถานที่**<br>mshr_locationid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | รหัสสถานที่เก็บของบันทึกที่อยู่ ตั้งค่าในเอนทิตี้ mshr_logisticspostaladdresslocationcdsentity |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | คำอธิบายของรายละเอียดผู้ติดต่อ |
| **ชนิด**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype ตัวเลือกการตั้งค่า* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ชนิดรายละเอียดของผู้ติดต่อ |
| **รหัสประเทศ/ภูมิภาค**<br>mshr_countryregioncode<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ประเทศหรือภูมิภาคของที่อยู่ |
| **ตัวระบุที่อยู่**<br>mshr_locator<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | รายละเอียดผู้ติดต่อ ตัวอย่างเช่น ถ้าชนิดคือ **ที่อยู่อีเมล** จากนั้นฟิลด์นี้จะมีที่อยู่อีเมลของผู้สมัคร |
| **จุดขยายตัวระบุที่อยู่**<br>mshr_locatorextension<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | จุดขยายตัวระบุที่อยู่ ตัวอย่างเช่น ถ้าชนิดเป็น **โทรศัพท์** จากนั้นคุณสมบัตินี้จะมีเบอร์ต่อภายใน |
| **เป็นอุปกรณ์เคลื่อนที่**<br>mshr_ismobile<br>*mshr_noyes ตัวเลือกการตั้งค่า* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ระบุว่าโทรศัพท์เป็นหมายเลขโทรศัพท์เคลื่อนที่หรือไม่ |
| **เป็นข้อความโต้ตอบแบบทันที**<br>mshr_isinstantmessage<br>*mshr_noyes ตัวเลือกการตั้งค่า* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ระบุว่าโทรศัพท์จะเปิดใช้งานสำหรับส่งข้อความโต้ตอบแบบทันทีหรือไม่ |
| **เป็นหลัก**<br>mshr_isprimary<br>*mshr_noyes ตัวเลือกการตั้งค่า* | อ่าน/เขียน<br>จำเป็นต้องระบุ | การหนดผู้ติดต่อหลักของชนิดผู้ติดต่อ ต้องมีบันทึกหลักเพียงชนิดเดียวต่อชนิดผู้ติดต่อ |
| **เป็นส่วนตัว**<br>mshr_isprivate<br>*mshr_noyes ตัวเลือกการตั้งค่า* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ระบุว่าที่อยู่นี้เป็นที่อยู่ส่วนตัวสำหรับบุคคลหรือไม่ |
| **วัตถุประสงค์**<br>mshr_purpose<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | บทบาท/วัตถุประสงค์ของรายละเอียดผู้ติดต่อ |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่ใช้เป็นตัวระบุหลักของบันทึกเอนทิตี้ ชุดข้อมูลของหมายเลข ชนิด การอธิบาย และตัวระบุที่ตั้งฝ่าย |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
