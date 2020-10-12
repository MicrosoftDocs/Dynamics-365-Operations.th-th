---
title: กำหนดการใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการกำหนดใบสั่งผลิต '
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3fe8f6890c7d8ac8835503091642faa773f7f6
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826057"
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

