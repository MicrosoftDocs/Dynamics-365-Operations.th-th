---
title: ปรับปรุงประสิทธิภาพโดยการจัดกำหนดการชุดงานหลังจากหลายชั่วโมง
description: หัวข้อนี้จะอธิบายถึงวิธีการแก้ไขปัญหาประสิทธิภาพการทำงานบางอย่างกับ Microsoft Dynamics 365 Human Resources โดยการจัดกำหนดการชุดงานที่รันเป็นเวลานานหลังจากหลายชั่วโมง
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: d2369b3209901eb2d60232a47d89284779199e1c98a56142758353d65a1faaf7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766882"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>ปรับปรุงประสิทธิภาพโดยการจัดกำหนดการชุดงานหลังจากหลายชั่วโมง

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>ออก

Microsoft Dynamics 365 Human Resources สามารถประสบปัญหาประสิทธิภาพการทำงานได้ ถ้ารันชุดงานที่รันเป็นเวลานานในระหว่างชั่วโมงการทำงานทั่วไป

## <a name="resolution"></a>ความละเอียด

จัดกำหนดการชุดงานต่อไปนี้ในช่วงเวลาที่ไม่ทำงาน นอกจากนี้เราขอแนะนำให้ตรวจสอบความถี่ของชุดงานที่รันบ่อย ถ้าเป็นไปได้ให้ลดการเกิดซ้ำของชุดงาน ในหลายกรณีที่ความถี่เริ่มต้นไม่เพียงพอ

ชุดงานต่อไปนี้ควรรันในเวลากลางคืนหรือหลังจากหลายชั่วโมง ตรวจสอบให้แน่ใจว่าได้ตรวจสอบโซนเวลาสำหรับชุดงานที่เกิดซ้ำเหล่านี้ ชุดงานบางชุดอาจใช้เวลามาตรฐานแปซิฟิก (PST)

| ชุดงาน | การเกิดซ้ำเริ่มต้น |
| --- | --- |
| การล้างประวัติชุดงาน | 1 ครั้งต่อเดือน |
| ส่งออกการล้างข้อมูลการแบ่งระยะ | 1 ครั้งต่อวัน |
| การซิงค์คำขอที่หายไปของการรวม Common Data Service | 1 ครั้งต่อวัน |
| งานระบบการบีบอัดฐานข้อมูลที่จำเป็นต้องรันเป็นประจำในช่วงเวลาที่ไม่ทำงาน | 1 ครั้งต่อวัน |
| งานระบบการสร้างดัชนีฐานข้อมูลที่จำเป็นต้องรันเป็นประจำในช่วงเวลาที่ไม่ทำงาน | 1 ครั้งต่อวัน |

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. ในแถบ **ค้นหา** ให้ค้นหาชุดงานด้านบนอย่างใดอย่างหนึ่ง

3. เลือก **รันในพื้นหลัง** แล้วจากนั้นเลือก **การเกิดซ้ำ**

   ![ตั้งค่าการเกิดซ้ำ](media/talent-batch-history-cleanup-recurrence.png)

4. ภายใต้ **กำหนดการเกิดซ้ำ** ให้กำหนด **วันที่เริ่มต้น** และ **เวลาเริ่มต้น** ที่จะเกิดขึ้นในระหว่างช่วงเวลาที่ไม่ทำงานหรือวันหยุดสุดสัปดาห์ เลือก **ไม่มีวันที่สิ้นสุด** 

   ![กำหนดวันที่และเวลาเริ่มต้นของการเกิดซ้ำ](media/talent-batch-history-cleanup-define-recurrence.png)

5. เลือก **ตกลง**

6. หากจำเป็น ให้เปลี่ยนพารามิเตอร์อื่นๆ ภายใต้ **รันในพื้นหลัง** แล้วจากนั้นเลือก **ตกลง**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]