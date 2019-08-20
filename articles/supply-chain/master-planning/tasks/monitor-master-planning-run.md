---
title: ตรวจสอบการรันการวางแผนหลัก
description: 'ผู้วางแผนการผลิตต้องการดูว่า การรันการวางแผนหลักอยู่ระหว่างดำเนินการหรือไม่ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845125"
---
# <a name="monitor-a-master-planning-run"></a>ตรวจสอบการรันการวางแผนหลัก

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

