---
title: "ประเมินใบสั่งผลิต"
description: "คุณสามารถรันขั้นตอนนี้ โดยใช้ข้อมูลบริษัทในการสาธิต USMF หรือชุดข้อมูลของคุณเอง "
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 862281adac67757e1ce0e9ddd1e96483363abb9a
ms.contentlocale: th-th
ms.lasthandoff: 02/06/2018

---
# <a name="estimate-a-production-order"></a>ประเมินใบสั่งผลิต

[!include [task guide banner](../../includes/task-guide-banner.md)]

คุณสามารถรันขั้นตอนนี้ โดยใช้ข้อมูลบริษัทในการสาธิต USMF หรือชุดข้อมูลของคุณเอง  ในทั้งสองกรณี คุณต้องมีใบสั่งผลิตที่มีสถานะสร้างขึ้นแล้วเปิดค้างไว้  นี่เป็นขั้นตอนที่สองจากเจ็ดขั้นตอน ซึ่งอธิบายวงจรชีวิตของใบสั่งการผลิต


## <a name="estimate-a-production-order"></a>ประเมินใบสั่งผลิต
1. ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด 
2. เลือกใบสั่งผลิตที่มีสถานะเป็นสร้างขึ้นแล้วในกริด 
3. ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต
4. คลิกประเมิน 
    * ในขั้นตอนนี้ ต้นทุนที่ถูกประเมินของใบสั่งผลิตแต่ละครั้งถูกคำนวณขึ้น   
5. คลิก ตกลง

## <a name="view-the-calculation-details"></a>ดูรายละเอียดการคำนวณ
1. ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน
2. คลิกดูรายละเอียดการคำนวณ
    * หน้านี้แสดงการแบ่งต้นทุน  ตัวอย่างเช่น คุณสามารถดูราคาต้นทุนรวมต่อหน่วยสำหรับสินค้าที่สำเร็จแล้วได้ในแถวแรก  ในแถวต่อมาประกอบด้วยต้นทุนตามสูตรการผลิต กระบวนการผลิต และต้นทุนทางอ้อม  

