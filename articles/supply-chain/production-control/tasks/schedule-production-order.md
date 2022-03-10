---
title: กำหนดการใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการกำหนดใบสั่งผลิต '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43d183764def1b1bea7bbe140c25e0eec0b692b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580587"
---
# <a name="schedule-a-production-order"></a>กำหนดการใบสั่งผลิต

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการกำหนดใบสั่งผลิต  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF นี่เป็นกระบวนงานที่สามจากเจ็ดกระบวนงานซึ่งอธิบายวงจรชีวิตของใบสั่งการผลิต


## <a name="schedule-a-production-order"></a>กำหนดการใบสั่งผลิต
1. ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด 
    * เลือกใบสั่งผลิตที่มีสถานะเป็น ประเมินแล้ว  
2. ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ
3. การจัดส่ง กำหนดเวลางาน
    * พารามิเตอร์สำหรับการวางแผนมีการตั้งค่าบนหน้านี้  คุณสามารถตั้งค่าพารามิเตอร์สำหรับผู้ใช้เฉพาะหรือผู้ใช้ทั้งหมด  
4. ในฟิลด์ทิศทางการจัดกำหนดการ ให้เลือก 'ไปข้างหน้าจากวันนี้'
5. ในฟิลด์วันที่กำหนดเวลาการดำเนินงาน ให้ป้อนวันที่
6. เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายกำลังการผลิตมีจำกัด
7. เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายวัตถุดิบมีจำกัด
8. คลิก ตกลง

## <a name="view-the-scheduling-results"></a>ดูผลลัพธ์การจัดกำหนดการ
1. ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต
2. คลิกงานทั้งหมด
    * หน้านี้แสดงงานที่ได้จัดกำหนดการที่คุณเพิ่งสร้างขึ้น  
3. ขยายหรือยุบส่วนการจัดกำหนดการ
    * บนแท็บด่วนการวางแผน คุณสามารถดูวันที่และเวลาที่จัดกำหนดไว้  
4. คลิกการสอบถาม
5. คลิกการใช้กำลังการผลิต
    * หน้าการใช้กำลังการผลิตแสดงถึงกำลังการผลิตที่ถูกจองไว้ผ่านการจัดตารางงาน จำนวนรวมของชั่วโมงที่ถูกจองบนทรัพยากรและจำนวนของชั่วโมงที่พร้อมใช้งานสำหรับงานที่จัดกำหนดบนทรัพยากร  
6. ปิดหน้า
7. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]