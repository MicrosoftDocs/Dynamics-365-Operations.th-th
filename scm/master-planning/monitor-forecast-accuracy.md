---
title: "ตรวจสอบความถูกต้องของการคาดการณ์"
description: "บทความนี้อธิบายชนิดของการคาดการณ์ความถูกต้องที่ Microsoft Dynamics 365 for Finance and Operations คำนวณ และอธิบายวิธีการดูค่าความถูกต้อง"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 56d3f0312e684ab076f9116ac6638bcd67b52e58
ms.contentlocale: th-th
ms.lasthandoff: 06/13/2017


---

# <a name="monitor-forecast-accuracy"></a>ตรวจสอบความถูกต้องของการคาดการณ์

[!include[banner](../includes/banner.md)]


บทความนี้อธิบายชนิดของการคาดการณ์ความถูกต้องที่ Microsoft Dynamics 365 for Finance and Operations คำนวณ และอธิบายวิธีการดูค่าความถูกต้อง

Finance and Operations คำนวณชนิดของความถูกต้องของการคาดการณ์ต่อไปนี้:

-   ความถูกต้องของการคาดการณ์ในอดีต โดยการเปรียบเทียบการคาดการณ์ในอดีตที่การวางแผนหลักใช้กับความต้องการในอดีต เมื่อต้องการดูค่า (ทั้งค่าสัมบูรณ์และค่าเปอร์เซ็นต์) สำหรับความถูกต้องของการคาดการณ์ในอดีต ให้คลิก **แสดงความถูกต้อง** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ**
-   ความถูกต้องที่มีการประเมินของแบบจำลองการคาดการณ์ที่ใช้ในการสร้างการคาดการณ์ คุณสามารถดูเปอร์เซ็นต์ความถูกต้องภายใต้ **รายละเอียดแบบจำลอง - MAPE** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ** ได้ 

**หมายเหตุ:** ถ้าคุณใช้บริการ Machine Learning ของ Microsoft Azure ของการคาดการณ์ความต้องการใน Finance and Operations การคำนวณความถูกต้องของแบบจำลองภายในจะขึ้นอยู่กับชุดข้อมูลการทดสอบ เมื่อต้องการระบุขนาดของชุดข้อมูลการทดสอบ ให้ตั้งค่าพารามิเตอร์ **TEST\_SET\_SIZE\_PERCENT** ในหน้า **พารามิเตอร์การคาดการณ์ความต้องการ** ตัวอย่างเช่น ถ้าคุณตั้งค่าเป็น **20**, 20 เปอร์เซ็นต์สุดท้ายของข้อมูลในอดีตจะถูกใช้ในการคำนวณความถูกต้องของแบบจำลองภายใน


<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[การอนุมัติการคาดการณ์ที่มีการปรับปรุง](authorize-adjusted-forecast.md)

[ลบจุดนอกขอบเขตออกจากข้อมูลในอดีตเกี่ยวกับธุรกรรมเมื่อคำนวณความต้องการการคาดการณ์](remove-historical-outliers-calculating-demand-forecast.md)




