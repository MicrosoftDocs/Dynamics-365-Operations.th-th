---
title: สถานะยกเว้นงาน
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะยกเว้นงานสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 29d3c4fd37a219b520172c6866c5fec488c698f7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065002"
---
# <a name="job-exempt-status"></a>สถานะยกเว้นงาน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายชุดตัวเลือกสถานะยกเว้นงานสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: cdm_jobexemptstatus

การแจงนับนี้ระบุชุดตัวเลือกสำหรับค่าสถานะยกเว้นงานสำหรับ FLSA มีอยู่ในชุดตัวเลือก cdm_jobexemptstatus ที่มีอยู่

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 | ยกเว้น | งานมีสถานะยกเว้นตามแนวทาง FLSA |
| 200000001 | NonExempt | งานมีสถานะไม่ยกเว้นตามแนวทาง FLSA |
| 200000002 | ไม่ได้ใช้ | แนวทางสถานะ FLSA ไม่ใช้กับงาน |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
