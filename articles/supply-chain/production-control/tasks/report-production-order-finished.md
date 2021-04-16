---
title: รายงานการเสร็จงานของใบสั่งผลิต
description: 'ขั้นตอนนี้แสดงถึงวิธีการรายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์ '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9b676ffefa9fd4b8d66a5c35012630295f8a263
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828621"
---
# <a name="report-a-production-order-as-finished"></a>รายงานการเสร็จงานของใบสั่งผลิต

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้แสดงถึงวิธีการรายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF นี่เป็นขั้นตอนที่หกจากเจ็ดซึ่งอธิบายวงจรชีวิตใบสั่งผลิต


## <a name="report-a-production-order-as-finished"></a>รายงานการเสร็จงานของใบสั่งผลิต
1. ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด 
    * เลือกใบสั่งผลิตที่มีสถานะเริ่มต้นแล้ว  
2. ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต
3. คลิก รายงาน เมื่อเสร็จสิ้น
    * บนหน้านี้ คุณสามารถยืนยันปริมาณของผลิตภัณฑ์สำเร็จรูปที่จะรายงานเมื่อเสร็จสมบูรณ์  
4. คลิกแท็บ ทั่วไป
5. ตั้งค่าปริมาณสินค้าที่ดีเป็น '18'
6. กำหนดปริมาณสินค้าที่บกพร่องเป็น '2'
7. ในฟิลด์สาเหตุของข้อผิดพลาด เลือก 'วัสดุ'
8. เลือกหรือล้างจบงานกล่องกาเครื่องหมาย
9. เลือกหรือยกเลิกยอมรับข้อผิดพลาดกล่องกาเครื่องหมาย
10. คลิก ตกลง

## <a name="verify-the-report-as-finished-journal"></a>ตรวจสอบรายงานสมุดรายวันเมื่อเสร็จสมบูรณ์
1. ในบานหน้าต่างการดำเนินการ ให้คลิก ดู
2. คลิก รายงานเมื่อเสร็จสมบูรณ์แล้ว
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
4. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * มีการงรายการบัญชีรายงานเมื่อสมุดรายวันเสร็จสมบูรณ์  ถ้าคุณต้องการทำการปรับปรุงสมุดรายวัน คุณสามารถสร้างสมุดรายวันใหม่ที่คุณสามารถสร้างการเปลี่ยนแปลงด้วยตนเอง  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]