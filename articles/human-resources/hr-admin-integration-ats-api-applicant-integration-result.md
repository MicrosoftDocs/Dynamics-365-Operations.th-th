---
title: ผลการรวมผู้สมัคร
description: หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 425fc78edc933b79879c330284ef911c6fd4fd1c
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066379"
---
# <a name="applicant-integration-result"></a>ผลการรวมผู้สมัคร


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
