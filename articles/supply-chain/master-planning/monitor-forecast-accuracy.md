---
title: ตรวจสอบความถูกต้องของการคาดการณ์
description: หัวข้อนี้อธิบายชนิดของความแม่นยำในการคาดการณ์ที่ Dynamics 365 Supply Chain Management คำนวณ และอธิบายวิธีการที่คุณสามารถดูค่าความแม่นยำได้
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bc3673ba69a072d07b749ad41a1697d35abd48
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935548"
---
# <a name="monitor-forecast-accuracy"></a>ตรวจสอบความถูกต้องของการคาดการณ์

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายชนิดของความแม่นยำในการคาดการณ์ที่ Microsoft Dynamics 365 Supply Chain Management คำนวณ และอธิบายวิธีการที่คุณสามารถดูค่าความแม่นยำได้

Supply Chain Management คำนวณชนิดของความถูกต้องของการคาดการณ์ต่อไปนี้:

-   ความถูกต้องของการคาดการณ์ในอดีต โดยการเปรียบเทียบการคาดการณ์ในอดีตที่การวางแผนหลักใช้กับความต้องการในอดีต เมื่อต้องการดูค่า (ทั้งค่าสัมบูรณ์และค่าเปอร์เซ็นต์) สำหรับความถูกต้องของการคาดการณ์ในอดีต ให้คลิก **แสดงความถูกต้อง** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ**
-   ความถูกต้องที่มีการประเมินของแบบจำลองการคาดการณ์ที่ใช้ในการสร้างการคาดการณ์ คุณสามารถดูเปอร์เซ็นต์ความถูกต้องภายใต้ **รายละเอียดแบบจำลอง - MAPE** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ** ได้ 

> [!NOTE]
> ถ้าคุณใช้ Demand forecasting Microsoft Azure Machine Learning การคำนวณความแม่นยำของแบบจำลองภายในจะขึ้นอยู่กับชุดข้อมูลทดสอบ เมื่อต้องการระบุขนาดของชุดข้อมูลการทดสอบ ให้ตั้งค่าพารามิเตอร์ **TEST\_SET\_SIZE\_PERCENT** ในหน้า **พารามิเตอร์การคาดการณ์ความต้องการ** ตัวอย่างเช่น ถ้าคุณตั้งค่าเป็น **20**, 20 เปอร์เซ็นต์สุดท้ายของข้อมูลในอดีตจะถูกใช้ในการคำนวณความถูกต้องของแบบจำลองภายใน


<a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม
--------

[อนุมัติการคาดการณ์ที่ปรับปรุง](authorize-adjusted-forecast.md)

[ลบจุดนอกขอบเขตออกจากข้อมูลในอดีตเกี่ยวกับธุรกรรมเมื่อคำนวณความต้องการการคาดการณ์](remove-historical-outliers-calculating-demand-forecast.md)



