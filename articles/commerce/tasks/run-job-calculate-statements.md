---
title: ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด
description: 'กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก '
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141211"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด

[!include [banner](../includes/banner.md)]

กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก  กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต

1. ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้า
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

