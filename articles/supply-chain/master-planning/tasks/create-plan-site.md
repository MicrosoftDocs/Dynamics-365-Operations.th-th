---
title: สร้างแผนสำหรับไซต์
description: 'ผู้วางแผนการผลิตคำนวณความต้องการทางวัสดุและกำลังการผลิต สำหรับการผลิตสินค้าเฉพาะ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34d694171e690354721c87f07aa81e811ecdfdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "364775"
---
# <a name="create-a-plan-for-a-site"></a>สร้างแผนสำหรับไซต์

[!include [task guide banner](../../includes/task-guide-banner.md)]

ผู้วางแผนการผลิตคำนวณความต้องการทางวัสดุและกำลังการผลิต สำหรับการผลิตสินค้าเฉพาะ  หลังจากมีการสร้างคำแนะนำในการจัดหา จะพบใบสั่งสำหรับไซต์ที่กำลังวางแผนและยืนยันใบสั่ง ซึ่งเริ่มจากใบสั่งด่วน ใบสั่งด่วนส่วนมากคือใบสั่งที่ต้องการการยืนยันในวันที่ปัจจุบัน  ใช้บริษัทข้อมูลสาธิต USMF เพื่อดำเนินงานเหล่านี้


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>สร้างแผนวัสดุและกำลังผลิตสำหรับสินค้า
1. คลิกที่งานการวางแผนหลัก 
    * คุณต้องนำทางไปยังแดชบอร์ดเริมต้น  
2. คลิก เรียกใช้
3. ขยายเรกคอร์ดเพื่อที่จะรวมส่วน
4. คลิกตัวกรอง 
5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
6. ในฟิลด์กรณี ให้ป้อนค่า
    * ตัวอย่าง : D0001  
7. คลิก ตกลง
8. คลิก ตกลง
    * กระบวนการนี้อาจใช้เวลาหนึ่งถึงสองนาที  
9. รีเฟรชหน้า

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>ระบุใบสั่งที่วางแผนไว้ด่วนสำหรับสินค้า
1. เปิดตัวกรองคอลัมน์หมายเลขสินค้า
2. ใช้ตัวกรองในฟิลด์ "หมายเลขสินค้า" ด้วยค่า "D0001" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"
3. เปิดตัวกรองคอลัมน์วันที่ของใบสั่ง
4. ใช้ตัวกรองในฟิลด์ "วันที่ใบสั่ง" ที่มีค่าของวันที่ปัจจุบัน โดยใช้ตัวดำเนินการตัวกรอง "ตรงทุกประการ"

## <a name="firm-all-the-urgent-orders-for-the-item"></a>ยืนยันใบสั่งด่วนสำหรับสินค้า
1. ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว
2. คลิก ยืนยัน
3. คลิก ตกลง

