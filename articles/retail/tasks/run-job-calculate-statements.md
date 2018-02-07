--- 
title: " ตั้งค่าคอนฟิกและดำเนินงานเพื่อการคำนวณใบแจ้งยอด"
description: "กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก "
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2bae81073fa6561c02d2dac0cd83db6a10ad00c3
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a> ตั้งค่าคอนฟิกและดำเนินงานเพื่อการคำนวณใบแจ้งยอด

[!include[task guide banner](../includes/task-guide-banner.md)]

กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก  กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต

1. ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้าปลีก 
2. คลิกคำนวณใบแจ้งยอด 
    * เลือกร้านค้าหรือโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า   
    * คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก   
3. คลิกรันในแท็บเบื้องหลัง 
4. ภายใต้การประมวลผลชุดงาน เลือก 'ใช่' 
5. คลิกการเกิดซ้ำ
6. ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ 
7. ในฟิลด์เวลาเริ่มต้น ให้ป้อนเวลา 
8. เลือกตัวเลือก ไม่มีวันที่สิ้นสุด
9. ในฟิลด์ PatternUnit ให้ป้อน 'วัน' 
10. ในฟิลด์ Per ให้ป้อนตัวเลข
11. คลิก ตกลง
12. คลิก ตกลง


