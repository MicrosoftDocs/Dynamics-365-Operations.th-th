---
title: "ตรวจสอบความถูกต้องที่คาดการณ์"
description: "บทความนี้อธิบายถึงชนิดของความแม่นยำของการคาดการณ์ว่า 365 Dynamics Microsoft สำหรับการดำเนินการคำนวณ และอธิบายวิธีที่คุณสามารถดูค่าความแม่นยำ"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>ตรวจสอบความถูกต้องที่คาดการณ์

บทความนี้อธิบายถึงชนิดของความแม่นยำของการคาดการณ์ว่า 365 Dynamics Microsoft สำหรับการดำเนินการคำนวณ และอธิบายวิธีที่คุณสามารถดูค่าความแม่นยำ

Dynamics 365 สำหรับการดำเนินงานคำนวณความแม่นยำของการคาดการณ์ชนิดต่อไปนี้:

-   ความถูกต้องของการคาดการณ์ในอดีต โดยการเปรียบเทียบการคาดการณ์ในอดีตที่การวางแผนหลักใช้กับความต้องการในอดีต เมื่อต้องการดูค่า (ทั้งค่าสัมบูรณ์และค่าเปอร์เซ็นต์) สำหรับความถูกต้องของการคาดการณ์ในอดีต ให้คลิก **แสดงความถูกต้อง** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ**
-   ความถูกต้องที่มีการประเมินของแบบจำลองการคาดการณ์ที่ใช้ในการสร้างการคาดการณ์ คุณสามารถดูเปอร์เซ็นต์ความถูกต้องภายใต้ **รายละเอียดแบบจำลอง - MAPE** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ** ได้ 

**หมายเหตุ:**ถ้าคุณใช้ 365 Dynamics สำหรับบริการเรียนรู้เครื่องจักรของ Microsoft Azure การคาดการณ์ความต้องการการดำเนินงาน การคำนวณความถูกต้องของแบบจำลองภายในเป็นไปตามชุดข้อมูลการทดสอบ เมื่อต้องการระบุขนาดของชุดข้อมูลทดสอบ ตั้ง**ทดสอบ\_ตั้ง\_ขนาด\_เปอร์เซ็นต์**พารามิเตอร์บน**อุปสงค์ที่คาดการณ์พารามิเตอร์**หน้า ตัวอย่างเช่น ถ้าคุณตั้งค่าเป็น **20**, 20 เปอร์เซ็นต์สุดท้ายของข้อมูลในอดีตจะถูกใช้ในการคำนวณความถูกต้องของแบบจำลองภายใน


<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


