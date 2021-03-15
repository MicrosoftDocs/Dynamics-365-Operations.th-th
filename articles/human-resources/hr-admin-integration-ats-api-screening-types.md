---
title: ชนิดการคัดเลือก
description: หัวข้อนี้อธิบายเอนทิตีชนิดการคัดเลือกสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126181"
---
# <a name="screening-types"></a>ชนิดการคัดเลือก

หัวข้อนี้อธิบายเอนทิตีชนิดการคัดเลือกสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmscreeningtypeentity

## <a name="description"></a>คำอธิบาย

เอนทิตีนี้อธิบายชนิดการคัดเลือกและตั้งค่าโดยบริษัทสำหรับกระบวนการคัดเลือกพนักงานก่อนการจ้างงานและปัจจุบัน

## <a name="json-representation"></a>การแสดง JSON

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสเอนทิตีชนิดการคัดเลือก**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | อ่านอย่างเดียว<br>จำเป็นต้องระบุ<br>ระบบถูกสร้างขึ้น | ตัวระบุหลักเฉพาะของเรกคอร์ดชนิดการคัดเลือก |
| **รหัสชนิดการคัดเลือก**<br>mshr_screeningtypeid<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | ตัวระบุเฉพาะที่กำหนดโดยผู้ใช้ของชนิดการคัดเลือก |
| **คำอธิบาย**<br>mshr_description<br>*สตริง* | อ่าน/เขียน<br>จำเป็นต้องระบุ | คำอธิบายเกี่ยวกับชนิดการคัดเลือก |
| **หน่วยความถี่**<br>mshr_frequencyunit<br>*ชุดตัวเลือก mshr_hcmpersongender* | อ่าน/เขียน<br>จำเป็นต้องระบุ | อธิบายความถี่ที่การคัดเลือกต้องเสร็จสมบูรณ์ของบุคคลที่ได้รับมอบหมาย |
| **สร้างจาก**<br>mshr_generatefrom<br>*ชุดตัวเลือก mshr_hcmfrequencygeneratefrom* | อ่าน-เขียน<br>จำเป็นต้องระบุ | ถ้าค่าความถี่เป็นค่าอื่นใดนอกเหนือจาก "ใช้เฉพาะครั้งเท่านั้น" ค่า GenerateFrom จะระบุวันที่เริ่มต้นคํานวณเหตุการณ์การคัดเลือกถัดไป |
| **ช่วงเวลาความถี่**<br>mshr_frequencyinterval<br>*เลขจำนวนเต็ม* | อ่าน-เขียน<br>จำเป็นต้องระบุ | ถ้าค่าความถี่เป็นค่าอื่นที่ไม่ใช่ "ใช้เฉพาะครั้งเท่านั้น" คุณต้องกําหนดช่วงเวลาให้กับหน่วยเวลาระหว่างเหตุการณ์ของการคัดเลือกแต่ละเหตุการณ์ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]