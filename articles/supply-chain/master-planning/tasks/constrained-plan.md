---
title: จัดทำแผนที่มีข้อจำกัด
description: บทความนี้อธิบายวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65884d556724cd6132fe328e95a5bec78885c174
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904027"
---
# <a name="generate-a-constrained-plan"></a>จัดทำแผนที่มีข้อจำกัด

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต แผนช่วยให้มั่นใจว่าจะไม่เริ่มการผลิตก่อนที่จะมีวัสดุพร้อมใช้งานและทรัพยากรจะไม่ถูกจองเกินเวลา  

ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF กระบวนงานนี้มีไว้สำหรับผู้วางแผนการผลิต


## <a name="set-up-a-constrained-plan"></a>ตั้งค่าแผนที่มีข้อจำกัด
1. ในโฮมเพจ ให้เลือกพื้นที่ทำงาน **การวางแผนหลัก**
2. เลือก **แผนหลัก** ในรายการของลิงค์ที่อยู่ด้านขวาสุดของพื้นที่ทำงาน
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ ตัวอย่าง: **StaticPlan**  
4. เลือก **ใช่** ในฟิลด์ **กำลังการผลิตที่มีจำกัด**
5. ในฟิลด์ **กรอบกำลังการผลิตที่มีจำกัด** ให้ป้อน `30`
6. ขยายส่วน **กรอบเวลาเป็นจำนวนวัน**
7. เลือก **ใช่** ในฟิลด์ **กำลังการผลิต**
8. ในฟิลด์ **กรอบเวลาการจัดกำหนดการกำลังการผลิต (วัน)** ให้ป้อนตัวเลข ตัวอย่าง: `60`  
9. เลือก **ใช่** ในฟิลด์ **ความล่าช้าที่มีการคำนวณ**
10. ในฟิลด์ **คำนวณกรอบเวลาความล่าช้า (วัน)** ให้ป้อนตัวเลข ตัวอย่าง: `60` 
11. ขยายส่วน **ความล่าช้าที่มีการคำนวณ**
12. เลือก **ใช่** ในฟิลด์ **เพิ่มความล่าช้าที่มีการคำนวณไปยังวันที่ของความต้องการ** ทั้งหมด
13. ปิดหน้า

## <a name="create-a-constrained-plan"></a>สร้างแผนที่มีข้อจำกัด
1. เลือก **รัน**
2. ในฟิลด์ **แผนหลัก** ให้ป้อนหรือเลือกแผนที่คุณได้ตั้งค่าข้อจำกัด  
3. เลือก **ตกลง**
4. เลือก **แผนการใบสั่ง**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]