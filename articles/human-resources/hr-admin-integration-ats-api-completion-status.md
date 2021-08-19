---
title: สถานะการเสร็จสมบูรณ์
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 67e464262897d89f80bd615156d56cc12a822dd4a0dfa6d5eb206c38ddd61ec5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732884"
---
# <a name="completion-status"></a>สถานะการเสร็จสมบูรณ์

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmcompletionstatus

การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสถานะสำหรับการคัดเลือกผู้สมัคร 

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 | ไม่สมบูรณ์ | ผู้สมัครยังไม่เสร็จสิ้นการคัดเลือก |
| 200000001 | ผ่าน | ผู้สมัครได้ผ่านคัดเลือกแล้ว |
| 200000002 | ล้มเหลว | ผู้สมัครไม่ได้ผ่านคัดเลือก |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]