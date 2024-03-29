---
title: ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน
description: บทความนี้แสดงวิธีดำเนินการตั้งค่าอย่างน้อยที่สุดที่จำเป็นให้เสร็จสมบูรณ์ก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในรุ่น BOM
author: t-benebo
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a403600bfdc257587441b5b5a907981d5eebaf58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844892"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>ตั้งค่าพื้นฐานของผลิตภัณฑ์หลักที่นำออกใช้ให้ครบถ้วน

[!include [banner](../../includes/banner.md)]

บทความนี้แสดงวิธีดำเนินการตั้งค่าอย่างน้อยที่สุดที่จำเป็นให้เสร็จสมบูรณ์ก่อนที่ผลิตภัณฑ์หลักจะถูกใช้ในรุ่น BOM

นี่คือกระบวนงานที่สามจากแปดกระบวนงานที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF

1. ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ เลือกผลิตภัณฑ์หลักที่คุณได้นำออกใช้ในขั้นตอนที่สอง  ผลิตภัณฑ์หลักนี้ถูกสร้างขึ้นด้วยเทคโนโลยีการจัดโครงแบบตามมิติ  
3. ในบานหน้าต่างการดำเนินการ เลือก **ผลิตภัณฑ์**
4. เลือก **กลุ่มมิติ** เพื่อเปิดกล่องโต้ตอบการวาง
5. ในฟิลด์ **กลุ่มมิติการจัดเก็บ** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
6. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ กลุ่มมิติการจัดเก็บจะกำหนดว่ามิติการจัดเก็บใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์  เลือก **ไซต์** สำหรับกระบวนงานนี้  
7. ในฟิลด์ **กลุ่มมิติการติดตาม** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
8. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ กลุ่มมิติการติดตามจะกำหนดว่ามิติการติดตามใดที่จะใช้สำหรับธุรกรรมผลิตภัณฑ์  เลือก **ไม่มี** สำหรับกระบวนงานนี้  
9. คลิก **ตกลง**
10. คลิก **แก้ไข**
11. ในฟิลด์ **กลุ่มแบบจำลองสินค้า** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
12. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ กลุ่มแบบจำลองสินค้าประกอบด้วยการตั้งค่าที่กำหนดวิธีควบคุมและจัดการกับการรับสินค้าและการตัดสินค้าจากคลัง นอกจากนี้ ยังกำหนดวิธีการคำนวณการใช้สินค้าด้วย  เลือก **FIFO** สำหรับกระบวนงานนี้  
13. ขยายส่วน **จัดการต้นทุน**
14. ในฟิลด์ **กลุ่มสินค้า** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
15. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ กลุ่มสินค้าจะใช้ในการจัดการสินค้าคงคลังโดยการแบ่งสินค้าคงคลังออกเป็นกลุ่ม  เลือก **CarAudio** สำหรับกระบวนงานนี้  
16. บนบานหน้าต่างการดำเนินการ เลือก **วางแผน**
17. เลือก **การตั้งค่าใบสั่งเริ่มต้น**
18. ใน **ฟิลด์ชนิดใบสั่งเริ่มต้น** ให้เลือกตัวเลือก เลือก **การผลิต** เพื่อระบุว่าตัวเลือกค่าเริ่มต้นในการจัดหาวัสดุสำหรับผลิตภัณฑ์หลักนี้คือ เพื่อทำการผลิต  
19. เลือก **บันทึก**
20. ปิดหน้า
21. ปิดฟอร์ม **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]