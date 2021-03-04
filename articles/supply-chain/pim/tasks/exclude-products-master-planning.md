---
title: สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก
description: กระบวนงานนี้แสดงวิธีการสร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่ ที่แยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9573fd220cd8b6a58f81e4d17ca65234f41beb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438342"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]