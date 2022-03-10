---
title: ลบงานคัมบังออกจากกำหนดการ
description: ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 838270189e08065f791c9e58888351025e0a6df8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573644"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>ลบงานคัมบังออกจากกำหนดการ

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]