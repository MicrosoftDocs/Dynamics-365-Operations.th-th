---
title: สร้างความสัมพันธ์กิจกรรม - งานที่เกิดขึ้นตามมา
description: 'ทิศทางของกิจกรรมในขั้นตอนการผลิตแบบ lean จะจัดทำเอกสารโดยใช้ความสัมพันธ์ของกิจกรรม '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cee0c75de1fee24cfb6df018de62ece102c96cc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579219"
---
# <a name="create-activity-relation---successor"></a>สร้างความสัมพันธ์กิจกรรม - งานที่เกิดขึ้นตามมา

[!include [banner](../../includes/banner.md)]

ทิศทางของกิจกรรมในขั้นตอนการผลิตแบบ lean จะจัดทำเอกสารโดยใช้ความสัมพันธ์ของกิจกรรม  การบันทึกนี้แสดงวิธีการสร้างความสัมพันธ์ของกิจกรรม 

ข้อกำหนดเบื้องต้น:

- ขั้นตอนการผลิตและเวอร์ชันในโหมดร่าง 

- กิจกรรมสองที่ต่อเนื่องกันในขั้นตอนการผลิตถูกสร้างขึ้นแต่ไม่มีความเกี่ยวข้อง


## <a name="find-the-production-flow-version"></a>ค้นหาเวอร์ชันขั้นตอนการผลิต 
1. ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
5. ในรายการ ให้เลือกฟิลด์เวอร์ชันแบบร่าง
    * คุณสามารถเพิ่มความสัมพันธ์ของกิจกรรมในฉบับร่างหรือเวอร์ชันที่ใช้งานอยู่ของขั้นตอนการผลิต  

## <a name="open-the-activity-overview"></a>เปิดภาพรวมกิจกรรม
1. คลิกกิจกรรม
    * โปรดสังเกตว่า แบบฟอร์มจะแสดงกิจกรรมทั้งหมดของขั้นตอนการผลิตที่ปันส่วนไปยังเวอร์ชันขั้นตอนการผลิตที่คุณกำลังทำงาน  

## <a name="add-a-successor"></a>เพิ่มงานที่เกิดขึ้นตามมา
1. คลิกเพิ่มงานที่เกิดขึ้นตามมา
2. ในฟิลด์กิจกรรม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
4. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
5. เลือกกล่องกาเครื่องหมายข้อจำกัด
6. ในฟิลด์ค่าข้อจำกัด ให้ป้อนหมายเลข
    * ข้อจำกัดเวลาคือเวลาจะถูกกำหนดระหว่างการสิ้นสุดตามกำหนดการที่เกิดขึ้นก่อนหน้า (วันและเวลาครบกำหนด) และเวลาเริ่มต้นตามกำหนดการจะเกิดขึ้นตามมา  
7. ในฟิลด์หน่วย ให้พิมพ์ค่าใดค่าหนึ่ง
8. ในฟิลด์อัตราส่วนเวลาวงจร ให้ป้อนหมายเลข
    * ถ้าทั้งสองกิจกรรมรันที่สมดุลเดียวกัน อัตราส่วนเวลาวงจรควรจะเป็น 1 ถ้าก่อนหน้าการทำงานรันด้วยความเร็วสองครั้งของการเกิดขึ้นตามมา อัตราส่วนควรจะเป็น 2   อัตราส่วนเวลาวงจรจะใช้เพื่อคำนวณเวลาวงจรแต่ละรอบของกิจกรรมขั้นตอนการผลิต  
9. คลิก ตกลง
10. ปิดหน้า
11. คลิกแท็บ GridPanel
12. ปิดหน้า
13. รีเฟรชหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]