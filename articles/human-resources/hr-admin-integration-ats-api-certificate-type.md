---
title: ชนิดของประกาศนียบัตร
description: หัวข้อนี้อธิบายเอนทิตี้ชนิดของใบรับรองสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054703"
---
# <a name="certificate-type"></a>ชนิดของประกาศนียบัตร

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายเอนทิตี้ชนิดของใบรับรองสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmcertificatetypeentity

## <a name="description"></a>คำอธิบาย

เอนทิตี้นี้จะกําหนดรายการของชนิดใบรับรองวิชาชีพที่ตั้งค่าในทรัพยากรบุคคล เอนทิตี้ไม่ได้ระบุเฉพาะกับนิติบุคคล (บริษัท)

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตี้ชนิดใบรับรอง**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ 
ระบบถูกสร้างขึ้น | ตัวระบุหลักที่ไม่ซ้ำกันสำหรับชนิดใบรับรอง |
| **ชนิดใบรับรอง**<br>mshr_certificatetype<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตัวระบุของผู้ใช้สามารถอ่านได้ที่ไม่ซ้ำกันสำหรับชนิดใบรับรอง |
| **คำอธิบาย**<br>msdyn_description<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | คำอธิบายของชนิดใบรับรอง |
| **ต้องการการต่ออายุ**<br>mshr_requirerenewal<br>*mshr_noyes ตัวเลือกที่ตั้งค่า* | อ่าน/เขียน<br>ไม่จำเป็นต้องระบุ | ระบุว่าการต่ออายุจำเป็นสำหรับใบรับรองหรือไม่ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]