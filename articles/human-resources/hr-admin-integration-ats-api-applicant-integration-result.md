---
title: ผลการรวมผู้สมัคร
description: หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467564"
---
# <a name="applicant-integration-result"></a>ผลการรวมผู้สมัคร

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmapplicantintegrationresult

การแจงนับนี้จะระบุสถานะเกี่ยวกับเรกคอร์ดผู้สมัคร

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 | ไม่ได้ประมวลผล | ผู้สมัครยังคงอยู่ภายใต้การพิจารณา |
| 200000001 | จ้างงานแล้ว | ผู้สมัครได้รับการว่าจ้างแล้ว |
| 200000002 | ไม่จ้าง | ได้ตัดสินใจแล้วว่าไม่ว่าจ้างผู้สมัคร |
| 200000003 | ยกเลิกแล้ว | ผู้สมัครถูกยกเลิกจากการพิจารณา |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]