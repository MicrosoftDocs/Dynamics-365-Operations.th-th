---
title: สถานะคำขอการสรรหาบุคลากร
description: บทความนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859617"
---
# <a name="recruiting-request-status"></a>สถานะคำขอการสรรหาบุคลากร


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources

ชื่อทางกายภาพ: mshr_hcmrecruitingrequeststatus

การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสถานะสำหรับ RecruitingRequest

| มูลค่า | ป้ายชื่อ | คำอธิบาย |
| --- | --- | --- |
| 200000000 | ฉบับร่าง | คำขออยู่ในแบบร่างและยังไม่พร้อมรับการสรรหาบุคลากรที่ใช้งานอยู่ |
| 200000001 | อยู่ระหว่างการตรวจทาน | ส่งคำขอแล้วและถูกส่งเพื่ออนุมัติตามลำดับงาน พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น |
| 200000002 | รอดำเนินการ | คำขออยู่ระหว่างการดำเนินการของลำดับงาน พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น |
| 200000003 | ถูกยกเลิก | คำขอได้รับการยกเลิกแล้ว พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น |
| 200000004 | ถูกปฏิเสธ | ปฏิเสธคำขอ พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น |
| 200000005 | ที่ใช้งาน | ลำดับงานเสร็จสมบูรณ์และได้รับอนุมัติแล้ว และคำขอพร้อมแล้วที่จะสรรหาบุคลากรที่ใช้งานอยู่ |
| 200000006 | ปิดแล้ว | ปิดคำขอสรรหาบุคลากร |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนํา API การรวมระบบการติดตามผู้สมัคร](hr-admin-integration-ats-api-introduction.md)<br>
[ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
