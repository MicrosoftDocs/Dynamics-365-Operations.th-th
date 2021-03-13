---
title: สถานะการเสร็จสมบูรณ์
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: e9024e00b5d25117fd255084609c4f8db9284f32
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125700"
---
# <a name="completion-status"></a>สถานะการเสร็จสมบูรณ์

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
