---
title: ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ
description: บทความนี้จะอธิบายถึงวิธีการปรับปรุงประสิทธิภาพการทำงานใน Microsoft Dynamics 365 Human Resources โดยการล้างข้อมูลประวัติชุดงาน
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 10d535e54f71e7bb90c7385e09926270a446df7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902211"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**ออกใช้**

Microsoft Dynamics 365 Human Resources สามารถประสบปัญหาประสิทธิภาพการทำงานได้ ถ้าประวัติชุดงานขยายใหญ่เกินไป

**สาเหตุ**

ชุดงานที่เรียกใช้บ่อยสามารถนำไปสู่การเจริญเติบโตที่ไม่ยั่งยืนของประวัติชุดงานได้ นี่อาจทำให้เกิดปัญหาประสิทธิภาพการทำงาน 

**ความละเอียด**

จัดกำหนดการงานแบบอัตโนมัติเพื่อล้างข้อมูลประวัติชุดงานของคุณ เราขอแนะนำให้ตั้งค่างานสำหรับการเรียกใช้รายสัปดาห์ แต่คุณอาจต้องเรียกใช้การล้างข้อมูลบ่อยขึ้นหรือน้อยลง ทั้งนี้ขึ้นอยู่กับสภาพแวดล้อมของคุณ กระบวนงานต่อไปนี้มีการตั้งค่าที่แนะนำของเรา แต่คุณสามารถเปลี่ยนแปลงข้อมูลเหล่านี้ตามความต้องการของคุณได้

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. ในแถบ **ค้นหา** ให้ป้อน **การล้างข้อมูลประวัติชุดงาน**

   ![ค้นหาการล้างข้อมูลประวัติชุดงาน](media/talent-batch-history-cleanup-search-bar.png)

3. ใน **ขีดจำกัดเวลาการเก็บประวัติ (วัน)** ให้ป้อน **30**

   ![ตั้งค่าขีดจำกัดเวลาการเก็บประวัติเป็น 30](media/talent-batch-history-cleanup-history-limit.png)

4. เลือก **เรียกใช้ในพื้นหลัง** แล้วจากนั้น เลือก **การเกิดซ้ำ**

   ![ตั้งค่าการเกิดซ้ำ](media/talent-batch-history-cleanup-recurrence.png)

5. ภายใต้ **กำหนดการเกิดซ้ำ** ให้กำหนด **วันที่เริ่มต้น** และ **เวลาเริ่มต้น** ที่จะเกิดขึ้นในระหว่างช่วงเวลาที่ไม่ทำงานหรือวันหยุดสุดสัปดาห์ และจากนั้น เลือก **ไม่มีวันที่สิ้นสุด** 

   ![กำหนดวันที่และเวลาเริ่มต้นของการเกิดซ้ำ](media/talent-batch-history-cleanup-define-recurrence.png)

6. ภายใต้ **รูปแบบการเกิดซ้ำ** เลือก **วัน** และตั้งค่า **ทำซ้ำหลังจากช่วงเวลาที่ระบุ** เป็น **7**

   ![ตั้งค่าการล้างข้อมูลให้ทำซ้ำรายสัปดาห์](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. เลือก **ตกลง**

8. เปลี่ยนพารามิเตอร์อื่นๆ ภายใต้ **เรียกใช้ในพื้นหลัง** ตามที่จำเป็น แล้วจากนั้น เลือก **ตกลง**



[!INCLUDE[footer-include](../includes/footer-banner.md)]
