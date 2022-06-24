---
title: ความถี่ในการคัดกรองที่สร้างจาก
description: บทความนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 846a35a2e8ca39ed9479601d99c8c515328d8ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879321"
---
# <a name="screening-frequency-generate-from"></a>ความถี่ในการคัดกรองที่สร้างจาก


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmfrequencygeneratefrom

การกําหนดตัวเลขนี้จะให้ชุดตัวเลือกของค่าในการกําหนดวันที่เริ่มต้นของการคํานวณเพื่อคัดกรองที่ต้องการครั้งต่อไป

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 ไม่ได้เลือก | ไม่ได้เลือกค่า |
| 200000001 วันที่เสร็จสมบูรณ์ | การคํานวณจะเสร็จสิ้นจากวันที่ที่คัดกรองครั้งล่าสุดเสร็จสมบูรณ์ |
| 200000002 ต้องระบุวันที่ | การคํานวณจะเสร็จสิ้นจากวันที่ที่คัดกรองครั้งล่าสุดที่ต้องการ |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
