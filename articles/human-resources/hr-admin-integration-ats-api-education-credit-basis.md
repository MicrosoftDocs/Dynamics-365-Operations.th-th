---
title: เกณฑ์เครดิตการศึกษา
description: หัวข้อนี้อธิบายตัวเลือกเกณฑ์เครดิตการศึกษาที่ตั้งค่าสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: a52c91574d9001dad9e8175c666e2ad7e91daeaedba47c05e60dbcb6a8670811
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743733"
---
# <a name="education-credit-basis"></a>เกณฑ์เครดิตการศึกษา

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายตัวเลือกเกณฑ์เครดิตการศึกษาที่ตั้งค่าสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmeducationcreditbasis

การแจงนับนี้จะให้การตั้งต่าของเกณฑ์เครดิตการศึกษาของบันทึกการศึกษาของผู้สมัคร

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 | ว่างเปล่า | ไม่ได้เลือกค่า |
| 200000001 | ภาคการศึกษา | ทุกครึ่งปี |
| 200000002 | ไตรมาส | ไตรมาส |
| 200000003 | ช่วงสามเดือน | ทุกสามเดือน |
| 200000004 | เงื่อนไข | เงื่อนไข |
| 200000005 | อื่นๆ | อื่นๆ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]