---
title: สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง
description: บทความนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846427"
---
# <a name="recruiting-request-position-status"></a>สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
