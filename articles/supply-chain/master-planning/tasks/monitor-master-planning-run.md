--- 
title: "ตรวจสอบการรันการวางแผนหลัก"
description: "ผู้วางแผนการผลิตต้องการดูว่า การรันการวางแผนหลักอยู่ระหว่างดำเนินการหรือไม่ "
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-a-master-planning-run"></a>ตรวจสอบการรันการวางแผนหลัก

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

ผู้วางแผนการผลิตต้องการดูว่า การรันการวางแผนหลักอยู่ระหว่างดำเนินการหรือไม่  ใช้บริษัทข้อมูลสาธิต USMF เพื่อทำให้กระบวนงานนี้เสร็จสิ้น


## <a name="run-master-planning"></a>ดำเนินการวางแผนหลัก
1. คลิกที่งานการวางแผนหลัก 
    * คุณจะพบสิ่งนี้บนแดชบอร์ดเริมต้น  
2. ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ตัวอย่างเช่น StaticPlan  
3. คลิก เรียกใช้
4. เลือก ใช่ ในฟิลด์เวลาของการประมวลผลการติดตาม
    * ถ้าฟิลด์ถูกเลือกแล้ว ให้ข้ามขั้นตอนนี้  
5. ในฟิลด์จำนวนของเธรด ให้ป้อนหมายเลข
6. ขยายเรกคอร์ดเพื่อที่จะรวมส่วน
7. คลิกตัวกรอง 
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * ทำเครื่องหมายแถว ที่ซึ่งฟิลด์ = หมายเลขสินค้า  
9. ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ตัวอย่าง : T0001  
10. คลิก ตกลง
11. คลิก ตกลง

## <a name="monitor-the-master-planning-run"></a>ตรวจสอบการรันการวางแผนหลัก
1. คลิกประวัติ
2. คลิกการสอบถาม
3. คลิกระยะเวลาของงานกระบวนการ
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * สำหรับสินค้าแต่ละรายการ คุณสามารถได้รับภาพรวมของระยะเวลาในการดำเนินขั้นตอนการวางแผนแต่ละขั้นให้เสร็จสมบูรณ์  


