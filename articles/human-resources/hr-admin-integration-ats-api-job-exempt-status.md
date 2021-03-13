---
title: สถานะยกเว้นงาน
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะยกเว้นงานสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125580"
---
# <a name="job-exempt-status"></a>สถานะยกเว้นงาน

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
