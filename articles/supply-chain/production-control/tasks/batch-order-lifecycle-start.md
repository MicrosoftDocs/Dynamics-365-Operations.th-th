---
title: วงจรชีวิตของใบสั่งชุดงานตั้งแต่สร้างจนถึงเริ่มต้น
description: 'ขั้นตอนนี้นำคุณผ่านส่วนแรกของวงจรชีวิตของใบสั่งชุดงาน '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d9ed44c9e05ea815e78ae041234ad61f76d89d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825049"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>วงจรชีวิตของใบสั่งชุดงานตั้งแต่สร้างจนถึงเริ่มต้น

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้นำคุณผ่านส่วนแรกของวงจรชีวิตของใบสั่งชุดงาน 

ตั้งแต่การสร้าง การประเมินต้นทุน และการจัดกำหนดการงานการผลิตผ่านการผลิตจำนวนมาก จนถึงการเริ่มต้นใบสั่งชุดงานที่แท้จริง



บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF 



ข้อกำหนดเบื้องต้นสำหรับการรันขั้นตอนด้วยชุดข้อมูลอื่นเป็นผลิตภัณฑ์นำออกใช้ มีเวอร์ชันสูตรและกระบวนการผลิตใช้งานอยู่


## <a name="create-a-batch-order"></a>สร้างใบสั่งชุดงาน
1. ไปที่ ใบสั่งผลิตทั้งหมด
2. คลิกใบสั่งชุดงานใหม่
3. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
4. คลิก สร้าง
5. ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์การผลิต ด้วยค่า 'b'

## <a name="view-production-formula-and-expected-co-products"></a>ดูสูตรการผลิตและสินค้าร่วมที่คาดไว้
1. ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต
2. คลิกสูตร
3. ปิดหน้า
4. คลิกผลิตภัณฑ์ร่วม
5. ปิดหน้า

## <a name="estimate-the-batch-order"></a>ประเมินใบสั่งชุดงาน
1. คลิกประเมิน 
2. คลิก ตกลง
3. ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน
4. คลิกดูรายละเอียดการคำนวณ
5. ปิดหน้า

## <a name="release-the-batch-order"></a>นำออกใช้ใบสั่งชุดงาน
1. ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต
2. คลิก นำออกใช้
3. คลิก ตกลง

## <a name="schedule-production-jobs"></a>กำหนดการของงานการผลิต
1. ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ
2. การจัดส่ง กำหนดเวลางาน
3. เลือก ไม่ใช่ ในฟิลด์กำลังการผลิตที่มีจำกัด
4. เลือก ไม่ใช่ ในฟิลด์วัตถุดิบที่มีจำกัด
5. คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน
6. ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต
7. คลิกงานทั้งหมด
8. ปิดหน้า

## <a name="start-the-batch-order"></a>เริ่มต้นสั่งงานใบสั่งชุดงาน
1. คลิก เริ่มต้น
2. คลิกแท็บ ทั่วไป
3. เลือก ไม่ ในฟิลด์ ลงรายการบัญชีรายการเบิกสินค้าทันที
4. คลิก ตกลง
5. ในบานหน้าต่างการดำเนินการ ให้คลิก ดู
6. คลิกรายการเบิกสินค้า
7. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
8. ปิดหน้า
9. ปิดหน้า
10. คลิก บัตรกระบวนการผลิต
11. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
12. ปิดหน้า
13. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]