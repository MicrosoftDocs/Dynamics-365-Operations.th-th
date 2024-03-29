---
title: ระดับการประเมิน
description: บทความนี้อธิบายเอนทิตี้ระดับการจัดอันดับสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: dcd366632456c186eca9682d79a0c8690772e8bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893887"
---
# <a name="rating-level"></a>ระดับการประเมิน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายเอนทิตี้ระดับการจัดอันดับสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmratinglevelentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะให้ระดับการจัดอันดับที่พร้อมใช้งานสำหรับทักษะต่างๆ ระดับการจัดอันดับใช้ระหว่างนิติบุคคลทั้งหมด

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ระดับการจัดอันดับ**<br>mshr_hcmratinglevelentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับระดับ |
| **รหัสระดับของการจัดอันดับ**<br>mshr_ratinglevelid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่ผู้ใช้สามารถอ่านได้สำหรับระดับ |
| **รหัสแบบจำลองการจัดอันดับ**<br>mshr_ratingmodelid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | แบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่ |
| **รหัสเอนทิตี้แบบจำลองการจัดอันดับ**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>คีย์นอก: mshr_hcmratingmodelentityid ของ mshr_hcmratingmodelentity | ตัวระบุที่สร้างขึ้นสำหรับแบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่ |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | คำอธิบายของระดับการจัดอันดับ |
| **แฟคเตอร์การทำงาน**<br>mshr_factor<br>*เลขจำนวนเต็ม* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตัวคูณสำหรับระดับการจัดอันดับ เมื่อคุณเปรียบเทียบรายการที่มีหมายเลขที่แตกต่างกันของระดับการจัดอันดับ ตัวคูณจะใช้เพื่อปรับคะแนนให้เป็นค่าปกติ ค่าต้องเป็นเลขจํานวนเต็มระหว่าง 0 ถึง 9 |
| **หมายเหตุ**<br>mshr_note<br>*สตริง* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | หมายเหตุใดๆที่สัมพันธ์กับระดับการจัดอันดับ |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ | ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้ ชุดของรหัสระดับการจัดอันดับและรหัสแบบจำลองการจัดอันดับ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
