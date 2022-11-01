---
title: ผลการรวมผู้สมัคร
description: บทความนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 09/12/2022
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
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702242"
---
# <a name="applicant-integration-result"></a>ผลการรวมผู้สมัคร


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources

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
