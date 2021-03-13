---
title: สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126061"
---
# <a name="recruiting-request-position-status"></a>สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง

หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmrecruitingrequestpositionstatus

การแจงนับนี้จะมีตัวเลือกการตั้งค่าสถานะของแต่ละตําแหน่งเป็นคำขอการสรรหาบุคลากรในเอนทิตี RecruitingRequestPosition

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 | เปิดอยู่ | ตําแหน่งในคำขอการสรรหาบุคลากรเปิดรับการสรรหาบุคลากร การมอบหมายตําแหน่งงานนี้จะไม่ได้บ่งชี้ว่าไม่มีการมอบหมายตําแหน่งที่ใช้งานอยู่ในปัจจุบันให้กับตําแหน่งงาน อาจมีพนักงานในตําแหน่งเมื่อสรรหาบุคลากร ตําแหน่งนี้บ่งชี้ว่าตําแหน่งนี้ว่างเฉพาะสำหรับการสรรหาบุคลากรในบริบทของคำขอการสรรหาบุคลากรเท่านั้น |
| 200000001 | บรรจุแล้ว | ผู้ปฏิบัติงานถูกเลือกเพื่อมอบหมายตําแหน่งงานให้กับตําแหน่งงาน |
| 200000002 | ถูกยกเลิก | คำขอสรรหาบุคลากรให้กับตําแหน่งนี้ถูกยกเลิก |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)
