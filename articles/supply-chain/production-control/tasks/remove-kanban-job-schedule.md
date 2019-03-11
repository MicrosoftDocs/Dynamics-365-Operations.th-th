---
title: ลบงานคัมบังออกจากกำหนดการ
description: ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4d994be5c6bb1edc6f0fc64494a19a5babf72ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "352079"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>ลบงานคัมบังออกจากกำหนดการ

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

