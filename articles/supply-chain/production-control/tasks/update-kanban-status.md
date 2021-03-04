---
title: การอัพเดตสถานะคัมบัง
description: 'เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8559c0843d7e6e538b5b29dc394a50d05462ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438650"
---
# <a name="update-kanban-status"></a>การอัพเดตสถานะคัมบัง

[!include [banner](../../includes/banner.md)]

เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF กระบวนงานนี้มีไว้สำหรับผู้ดูแลร้าน


## <a name="find-the-kanban"></a>ค้นหาคัมบัง
1. ไปที่การควบคุมการผลิต > คัมบัง > คัมบัง
2. เปิดตัวกรองคอลัมน์สถานะหน่วยจัดการวัสดุ
3. คลิกล้างข้อมูล
    * นี่จะรีเซ็ตตัวกรอง  
4. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  ตัวอย่างเช่น กรองข้อมูลในฟิลด์หมายเลขบัตรด้วยค่า '000149'

## <a name="change-emptied-status-to-received-status"></a>เปลี่ยนสถานะว่างเปล่า เป็นสถานะได้รับแล้ว
1. คลิกกลับหน่วยจัดการวัสดุที่ว่าง
2. คลิก ตกลง
    * สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ได้รับแล้ว  

## <a name="change-received-status-to-emptied-status"></a>เปลี่ยนสถานะได้รับแล้ว เป็นสถานะว่างเปล่า
1. คลิกคัมบังที่ว่างเปล่า
2. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ว่างแล้ว  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]