--- 
title: "สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก"
description: "กระบวนงานนี้แสดงวิธีการสร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่ ที่แยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM"
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 1685e8eb706e29ef5b195e9163bf19345fee78b6
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่ ที่แยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM


## <a name="create-an-obsolete-state"></a>สร้างสถานะที่ล้าสมัย
1. ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การตั้งค่า > สถานะรอบการขายของผลิตภัณฑ์
2. คลิก สร้าง
3. ในฟิลด์สถานะ ให้พิมพ์ค่าใดค่าหนึ่ง
4. เลือก ไม่ ในฟิลด์ ใช้งานอยู่สำหรับการวางแผน
5. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า

## <a name="associate-the-obsolete-state-to-a-released-product"></a>เชื่อมโยงสถานะที่ล้าสมัยกับผลิตภัณฑ์ที่นำออกใช้
1. ปิดหน้า
2. ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ 
3. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  ตัวอย่างเช่น กรองข้อมูลในฟิลด์ ค้นหาชื่อ ด้วยค่า 'M00'
4. คลิก แก้ไข
5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
6. ในฟิลด์สถานะรอบการขายของผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า


