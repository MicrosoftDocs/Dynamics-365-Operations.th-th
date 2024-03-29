---
title: 'กำหนดการตรวจนับตามรอบ '
description: 'การตรวจนับตามรอบเป็นกระบวนการคลังสินค้าที่คุณสามารถใช้ตรวจสอบสินค้าคงคลังคงเหลือ '
author: Mirzaab
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45107dca67ac13669c468c4c32fb4adfdab2195b
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902157"
---
# <a name="define-cycle-counting"></a>กำหนดการตรวจนับตามรอบ  

[!include [banner](../../includes/banner.md)]

การตรวจนับตามรอบเป็นกระบวนการคลังสินค้าที่คุณสามารถใช้ตรวจสอบสินค้าคงคลังคงเหลือ  การบันทึกงานนี้แสดงวิธีการตั้งค่าระดับความสำคัญของงานการตรวจนับเริ่มต้น เปิดใช้งานรายการเมนูบนอุปกรณ์เคลื่อนที่เพื่อประมวลผลทั้งการเบิกสินค้าและการดำเนินงานการตรวจนับ เปิดใช้งานทริกเกอร์ขีดจำกัดการตรวจนับเมื่อสถานที่ว่างเปล่า และเปิดใช้งานแผนการตรวจนับตามรอบสำหรับสินค้าเฉพาะภายในคลังสินค้าเฉพาะ โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการคลังสินค้า คุณสามารถดำเนินการกระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือในข้อมูลของคุณเอง


## <a name="set-the-priority-of-counting-work"></a>ตั้งค่าระดับความสำคัญของงานการตรวจนับ
1. ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า**
2. คลิกแท็บ **การตรวจนับตามรอบ**
3. ในฟิลด์ **ระดับความสำคัญของงานการตรวจนับตามรอบเริ่มต้น** ป้อนหมายเลข ขั้นตอนนี้เปลี่ยนระดับความสำคัญของงานการตรวจนับตามรอบโดยเปรียบเทียบกับชนิดอื่น ๆ ของงานในคลังสินค้า คุณสามารถยกระดับความสำคัญของงานการตรวจนับตามรอบได้โดยการป้อนหมายเลขที่ต่ำกว่าหมายเลขของงานชนิดอื่นๆ  
4. คลิก **บันทึก**
5. ปิดหน้า

## <a name="enable-the-mobile-device"></a>เปิดใช้งานอุปกรณ์เคลื่อนที่
1. ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูของอุปกรณ์เคลื่อนที่**
2. คลิก **สร้าง**
3. ในฟิลด์ **ชื่อรายการในเมนู** ให้พิมพ์ค่า
4. ในฟิลด์ **หัวข้อ** ให้พิมพ์ค่าใดค่าหนึ่ง
5. ในฟิลด์ **โหมด** เลือก 'งาน'
6. ตั้งค่าตัวเลือก **ใช้งานที่มีอยู่** เป็น ใช่ เมื่อคุณตั้งค่าตัวเลือกนี้เป็น ใช่ ระบบจะค้นหางานที่มีอยู่เมื่อรายการเมนูบนอุปกรณ์เคลื่อนที่ถูกใช้ไปแล้ว  
7. ในฟิลด์ **สั่งการโดย** เลือก 'สั่งการโดยระบบ' เมื่อมีการเลือก "สั่งการโดยระบบ" ผู้ปฏิบัติงานคลังสินค้าจะถูกส่งการให้เปิดงานที่อยู่ในคลาสงานที่กำหนด (ถัดไปเราจะสร้างคลาสงานเหล่านี้)  
8. ขยาย fastTab **คลาสงาน** ถัดไป เราจะสร้างคลาสงานสองชิ้นที่จะใช้กับรายการเมนูบนอุปกรณ์เคลื่อนที่นี้ เมื่อรายการเมนูถูกใช้ คลาสงานเหล่านี้จะถูกสอบถาม และจะแสดงงานที่มีระดับความสำคัญสูงสุดต่อผู้ใช้  
9. คลิก **สร้าง**
10. ในฟิลด์ **รหัสคลาสงาน** เลือกค่าใดค่าหนึ่ง
11. คลิก **สร้าง**
12. ในฟิลด์ **รหัสคลาสงาน** เลือกค่าใดค่าหนึ่ง
13. ใน **บานหน้าต่างการดำเนินการ** คลิก **บันทึก**
14. ปิดหน้า
15. ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > เมนูของอุปกรณ์เคลื่อนที่**
16. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
17. ในแผนภูมิ เลือก 'รายการเมนูที่คุณเพิ่งสร้างขึ้น'
18. คลิก **แก้ไข**
19. คลิก ลูกศรเพื่อเพิ่มรายการเมนูลงในเมนู
20. คลิก **บันทึก**

## <a name="create-a-counting-threshold"></a>สร้าง ขีดจำกัดการตรวจนับ
1. ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > วงจรการตรวจนับตามรอบ > ขีดจำกัดการตรวจนับตามรอบ**
2. คลิก **สร้าง**
3. ในฟิลด์ **รหัสขีดจำกัดการตรวจนับตามรอบ** พิมพ์ค่าใดค่าหนึ่ง
4. ตั้งค่าตัวเลือก **ดำเนินการตรวจนับตามรอบทันที** เป็น ใช่
5. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
6. คลิก **บันทึก**
7. คลิก **เลือกสถานที่**
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
9. ในฟิลด์ **เงื่อนไข** เลือกค่าใดค่าหนึ่ง
10. คลิก **ตกลง**
11. ปิดหน้า

## <a name="create-a-cycle-count-plan"></a>สร้าง แผนการตรวจนับตามรอบ
1. ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > วงจรการตรวจนับตามรอบ > แผนการตรวจนับตามรอบ**
2. คลิก **สร้าง**
3. ในฟิลด์ **รหัสแผนการตรวจนับตามรอบ** พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
5. ในฟิลด์ **จำนวนสูงสุดของการตรวจนับตามรอบ** ป้อนหมายเลข
6. คลิก **บันทึก**
7. คลิก **เลือกสถานที่**
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
9. ในฟิลด์ **เงื่อนไข** เลือกค่าใดค่าหนึ่ง
10. คลิก **ตกลง**
11. ในฟิลด์ **จำนวนวันระหว่างการตรวจนับตามรอบ** ป้อนหมายเลข ตัวอย่างเช่น ถ้าฟิลด์ **จำนวนวันระหว่างการตรวจนับตามรอบ** ถูกตั้งค่าเป็น 5 งานการตรวจนับตามรอบจะถูกสร้างทุกๆ ห้าวัน อย่างไรก็ตาม ถ้างานการตรวจนับตามรอบถูกประมวลผลในวันที่สาม งานการตรวจนับครั้งถัดไปจะสร้างขึ้นห้าวันหลังจากการตรวจนับตามรอบครั้งสุดท้ายที่ถูกประมวลผล ก็คือในวันที่แปด  
12. คลิก **บันทึก**
13. คลิก **สร้าง**
14. ในฟิลด์ **หมายเลขลำดับ** ให้ป้อนหมายเลข การเรียงคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด ค่าต้องมากกว่า 0 (ศูนย์)  
15. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
16. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
17. คลิก **บันทึก**
18. คลิกการสอบถาม **กำหนดผลิตภัณฑ์**
19. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
20. ในฟิลด์ **เกณฑ์** ป้อนหรือเลือกค่า
21. คลิก **ตกลง**
22. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]