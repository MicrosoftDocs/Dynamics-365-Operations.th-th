---
title: ชนิดของประกาศนียบัตร
description: หัวข้อนี้อธิบายเอนทิตี้ชนิดของใบรับรองสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125724"
---
# <a name="certificate-type"></a>ชนิดของประกาศนียบัตร

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

