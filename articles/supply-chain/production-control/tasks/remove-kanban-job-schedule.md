--- 
title: "ลบงานคัมบังออกจากกำหนดการ"
description: "ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a>ลบงานคัมบังออกจากกำหนดการ

[!include[task guide banner](../../includes/task-guide-banner.md)]

ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF ขั้นตอนนี้มีไว้สำหรับหัวหน้างานผลิตหรือนักวางแผนการผลิต


## <a name="find-a-planned-kanban-job"></a>ค้นหางานคัมบังที่วางแผนไว้แล้ว
1. ไปที่การควบคุมการผลิต > คัมบัง > การกำหนดเวลางานคัมบัง 
2. ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา 
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * เลือกเซลล์ทำงาน 1250  
4. คลิกเลือก 
5. ในฟิลด์แสดงสถานะงาน เลือก 'จัดกำหนดการแล้ว' 

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>ลบงานคัมบังที่วางแผนไว้แล้วออกจากกำหนดการ
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกงานที่มีสถานะวางแผนไว้แล้ว ตัวอย่างเช่น งานจากวันที่ 19 ธันวาคม 2012  
2. ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน
3. คลิก แปลงกลับสถานะงาน 
4. คลิก ตกลง
    * นี่จะแปลงกลับสถานะของงานปัจจุบันจาก 'วางแผนไว้แล้ว' เป็น 'ไม่ได้วางแผน' และลบออกจากบอร์ดกระบวนการ   


