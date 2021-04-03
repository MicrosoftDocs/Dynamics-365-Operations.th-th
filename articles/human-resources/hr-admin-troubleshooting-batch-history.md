---
title: ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ
description: บืความนี้จะอธิบายถึงวิธีการแก้ไขปัญหาประสิทธิภาพการทำงานบางอย่างกับ Microsoft Dynamics 365 Human Resources โดยการล้างข้อมูลประวัติชุดงาน
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 8fef2152f7c65a6678e6cb94da8ea2bbe99ea51d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466699"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**ออกใช้**

Microsoft Dynamics 365 Human Resources สามารถประสบปัญหาประสิทธิภาพการทำงานได้ ถ้าประวัติชุดงานขยายใหญ่เกินไป

**สาเหตุ**

ชุดงานที่รันบ่อยสามารถนำไปสู่การเจริญเติบโตที่ไม่ยั่งยืนของประวัติชุดงานได้ นี่อาจทำให้เกิดปัญหาประสิทธิภาพการทำงาน 

**ความละเอียด**

จัดกำหนดการงานแบบอัตโนมัติเพื่อล้างข้อมูลประวัติชุดงานของคุณ เราขอแนะนำให้ตั้งค่างานสำหรับการรันรายสัปดาห์ แต่คุณอาจต้องรันการล้างข้อมูลบ่อยขึ้นหรือน้อยลง ทั้งนี้ขึ้นอยู่กับสภาพแวดล้อมของคุณ กระบวนงานต่อไปนี้มีการตั้งค่าที่แนะนำของเรา แต่คุณสามารถเปลี่ยนแปลงข้อมูลเหล่านี้ตามความต้องการของคุณได้

1. ในทรัพยากรบุคคล เลือก **การจัดการระบบ**

2. ในแถบ **ค้นหา** ให้ป้อน **การล้างข้อมูลประวัติชุดงาน**

   ![ค้นหาการล้างข้อมูลประวัติชุดงาน](media/talent-batch-history-cleanup-search-bar.png)

3. ใน **ขีดจำกัดเวลาการเก็บประวัติ (วัน)** ให้ป้อน **30**

   ![ตั้งค่าขีดจำกัดเวลาการเก็บประวัติเป็น 30](media/talent-batch-history-cleanup-history-limit.png)

4. เลือก **รันในพื้นหลัง** แล้วจากนั้น เลือก **การเกิดซ้ำ**

   ![ตั้งค่าการเกิดซ้ำ](media/talent-batch-history-cleanup-recurrence.png)

5. ภายใต้ **กำหนดการเกิดซ้ำ** ให้กำหนด **วันที่เริ่มต้น** และ **เวลาเริ่มต้น** ที่จะเกิดขึ้นในระหว่างช่วงเวลาที่ไม่ทำงานหรือวันหยุดสุดสัปดาห์ และจากนั้น เลือก **ไม่มีวันที่สิ้นสุด** 

   ![กำหนดวันที่และเวลาเริ่มต้นของการเกิดซ้ำ](media/talent-batch-history-cleanup-define-recurrence.png)

6. ภายใต้ **รูปแบบการเกิดซ้ำ** เลือก **วัน** และตั้งค่า **ทำซ้ำหลังจากช่วงเวลาที่ระบุ** เป็น **7**

   ![ตั้งค่าการล้างข้อมูลให้ทำซ้ำรายสัปดาห์](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. เลือก **ตกลง**

8. เปลี่ยนพารามิเตอร์อื่นๆ ภายใต้ **รันในพื้นหลัง** ตามที่จำเป็น แล้วจากนั้น เลือก **ตกลง**



[!INCLUDE[footer-include](../includes/footer-banner.md)]