---
title: รายงานการเสร็จงานไปยังสถานที่ที่ควบคุมป้ายที่ไม่ใช่ป้ายทะเบียน (ใบสมัคร พฤษภาคม 2016)
description: 'คู่มืองานนี้แสดงตัวอย่างการรายงานเป็น เสร็จแล้ว ไปยังสถานที่ที่เป็นป้ายทะเบียนที่มีการควบคุม '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9aeac631e32876d6c19cb964f28e65491137049a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204507"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>รายงานการเสร็จงานไปยังสถานที่ที่ควบคุมป้ายที่ไม่ใช่ป้ายทะเบียน (ใบสมัคร พฤษภาคม 2016)

[!include [banner](../../includes/banner.md)]

คู่มืองานนี้แสดงตัวอย่างการรายงานเป็น เสร็จแล้ว ไปยังสถานที่ที่เป็นป้ายทะเบียนที่มีการควบคุม  นโยบายงานที่ใช้งานได้เป็นข้อกำหนดเบื้องต้นสำหรับงานนี้ คู่มืองานก่อนหน้าแสดงการตั้งค่าของนโยบายงาน คำแนะนำงานนี้ต้องการแอพลิเคชัน Dynamics AX 7.0.1 หรือใหม่กว่า




## <a name="set-up-an-output-location"></a>ตั้งค่าที่ตั้งเอาท์พุท
1. ไปที่การจัดการองค์กร > ทรัพยากร > กลุ่มทรัพยากร
2. ในรายการนี้ ให้เลือกกลุ่มทรัพยากร '5102'
3. คลิกแก้ไข
4. ในฟิลด์คลังสินค้าเอาท์พุท ให้ป้อน '51'
5. ในฟิลด์ที่ตั้งเอาท์พุท ให้ป้อน '001'
    * สถานที่ 001 ไม่ใช่สถานที่ที่มีการควบคุมป้ายทะเบียน  คุณสามารถตั้งค่าสถานที่เอาท์พุทที่ควบคุมป้ายที่ไม่ใช่ป้ายทะเบียน เฉพาะเมื่อนโยบายงานมีอยู่สำหรับสถานที่  

## <a name="create-a-production-order-and-report-it-as-finished"></a>สร้างใบสั่งผลิตและรายงานเป็น เสร็จแล้ว
1. ปิดหน้า
2. ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด 
3. คลิกใบสั่งผลิตใหม่
4. ในฟิลด์หมายเลขสินค้า ให้ป้อน 'L0101'
5. คลิก สร้าง
6. ในบานหน้าต่างการดำเนินการ คลิกที่ใบสั่งผลิต 
7. คลิกประเมิน 
8. คลิก ตกลง 
9. คลิกที่เริ่มต้น
10. คลิกแท็บ ทั่วไป 
11. ในฟิลด์การใช้ BOM อัตโนมัติ ให้เลือก 'ไม่เคย'
12. คลิก ตกลง 
13. คลิกรายงานเมื่อเสร็จสมบูรณ์
14. คลิกแท็บ ทั่วไป 
15. เลือก ใช่ ในฟิลด์ยอมรับข้อผิดพลาด
16. คลิก ตกลง 
17. ในบานหน้าต่างการดำเนินการ คลิกคลังสินค้า
18. คลิกรายละเอียดงาน
    * เมื่อใบสั่งผลิตถูกรายงานเป็น เสร็จแล้ว จึงไม่มีการสร้างงานสำหรับการสำรอง  นี่เกิดขึ้นเนื่องจากนโยบายงานถูกกำหนดให้ป้องกันงานจากการถูกสร้าง เมื่อผลิตภัณฑ์ L0101 ถูกรายงานเป็น เสร็จแล้ว ไปยังสถานที่ 001  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]