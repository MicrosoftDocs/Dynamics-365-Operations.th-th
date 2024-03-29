---
title: สร้างกิจกรรมกระบวนการสำหรับ lean manufacturing
description: 'สร้างกิจกรรมกระบวนการสำหรับการผลิตแบบ lean '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 214e54cc93379948e4c25b3b28d835bbbbd40b72
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570164"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>สร้างกิจกรรมกระบวนการสำหรับ lean manufacturing

[!include [banner](../../includes/banner.md)]

สร้างกิจกรรมกระบวนการสำหรับการผลิตแบบ lean  

ข้อกำหนดเบื้องต้น: 

1. 1 ต้องสร้างขั้นตอนการผลิตและเวอร์ชันที่ไม่ได้ใช้งานอยู่ 

2. 2. ต้องสร้างเซลล์ทำงาน


## <a name="find-the-production-flow-version"></a>ค้นหาเวอร์ชันขั้นตอนการผลิต
1. ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก

## <a name="create-a-new-activity"></a>สร้างกิจกรรมใหม่
1. คลิกกิจกรรม
    * ตรวจสอบให้แน่ใจว่าขั้นตอนการผลิตที่เลือกมีเวอร์ชันในแบบร่าง และเลือกเวอร์ชันนั้น  
2. คลิกสร้างกิจกรรมการวางแผนใหม่
3. คลิก ถัดไป
4. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
5. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
    * โปรดทราบว่า ชื่อต้องไม่ซ้ำกันสำหรับการระบุขั้นตอนการผลิตสำหรับเวอร์ชันทั้งหมด  
6. ในฟิลด์ปริมาณกระบวนการ ให้ป้อนตัวเลข
    * โปรดทราบว่าไม่ว่าปริมาณงานใดจะถูกประมวลผล นี่เป็นปริมาณต่ำสุดสำหรับแต่ละงานในการคำนวณต้นทุนแรงงาน  ถ้าปริมาณงานแตกต่างจากปริมาณนี้ ผลต่างต้นทุนแรงงานจะถูกสร้างขึ้น  
7. คลิก ถัดไป

## <a name="select-the-work-cell"></a>เลือกเซลล์ทำงาน
1. ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา 
2. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก

## <a name="define-the-inventory-updates"></a>กำหนดการอัพเดตสินค้าคงคลัง
1. เลือกหรือเคลียร์กล่องกาเครื่องหมายอัพเดตปริมาณคงคลังคงเหลือเมื่อรับสินค้า 
    * ถ้ามีการอัพเดตปริมาณคงคลังคงเหลือ = ไม่ใช่ คุณสามารถกำหนดกิจกรรมเพื่อรับผลิตภัณฑ์กึ่งสำเร็จรูป (กิจกรรมไม่ถึงระดับ BOM)     คุณยังสามารถเลือกที่จะใช้ผลิตภัณฑ์กึ่งสำเร็จรูป  

## <a name="define-the-picking-activities"></a>กำหนดกิจกรรมการเบิกสินค้า
1. คลิก ถัดไป
2. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * ค่าเริ่มต้นกิจกรรมการเบิกสินค้าถูกสร้างขึ้นสำหรับที่ตั้งอินพุทของเซลล์ทำงานที่เลือก  
3. คลิก เพิ่ม
    * คุณสามารถสร้างกิจกรรมการเบิกสินค้าเพิ่มเติมสำหรับผลิตภัณฑ์เฉพาะ ที่ไม่ได้แบ่งระยะกิจกรรมอินพุทของเซลล์ทำงาน  
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า
6. ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * ด้วยคำนิยามนี้ วัตถุดิบทั้งหมดที่ใช้ในกิจกรรมการถูกเบิกจากคลังสินค้าอินพุทที่เริ่มต้นและที่ตั้ง ยกเว้นสินค้าที่กำหนดไว้ในกิจกรรมการเบิกสินค้าที่สอง  สินค้านี้จะถูกเบิกจากคลังสินค้าและสถานที่ที่แตกต่างกัน  
7. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
8. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
9. เลือกหรือเคลียร์กล่องกาเครื่องหมายลงทะเบียนของเสีย 
10. คลิก ถัดไป

## <a name="define-the-activity-times"></a>กำหนดเวลากิจกรรม
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * คำนิยามของรันไทม์จำเป็นต้องใช้  รันไทม์ถูกใช้เพื่อคำนวณต้นทุนและเวลาสำหรับปริมาณที่สามารถประมวลผลได้ของงานคัมบัง  รันไทม์ไม่ได้ใช้ในการคำนวณปริมาณการใช้วัสดุและกำลังการผลิต ซึ่งจะคำนวณโดยเวลาวงจรที่ได้รับมาจากงานเวอร์ชันขั้นตอนการผลิต  
2. ในฟิลด์เวลา ให้ป้อนตัวเลข
3. ในฟิลด์หน่วย ให้พิมพ์ค่า 
4. เลือกหน่วยเวลา
5. ในฟิลด์ต่อปริมาณ ให้ป้อนตัวเลข
6. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เวลาในการรอไม่จำเป็น  
7. ในฟิลด์เวลา ให้ป้อนตัวเลข
8. ในฟิลด์หน่วย ให้พิมพ์ค่า 
9. เลือกหน่วยเวลา
10. ในฟิลด์ต่อปริมาณ ให้ป้อนตัวเลข
11. คลิก ถัดไป
12. คลิก Finish
13. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]