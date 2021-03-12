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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bb18f876e7d279624f60f01c5fbf4e449e9ab27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986890"
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

