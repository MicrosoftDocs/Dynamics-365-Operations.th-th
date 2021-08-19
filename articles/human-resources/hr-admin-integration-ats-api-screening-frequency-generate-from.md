---
title: ความถี่ในการคัดกรองที่สร้างจาก
description: หัวข้อนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 7b87bff6925721a20ad9d8bf92e64113d30333defd2d6708b445bcd2126e485a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766253"
---
# <a name="screening-frequency-generate-from"></a>ความถี่ในการคัดกรองที่สร้างจาก

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources

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