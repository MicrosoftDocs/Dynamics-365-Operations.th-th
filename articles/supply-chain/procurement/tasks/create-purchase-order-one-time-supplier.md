---
title: สร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร
description: 'กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร '
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438879"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>สร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร  ซัพพลายเออร์จะถูกสร้างขึ้นโดยอัตโนมัติพร้อมกับใบสั่งซื้อ แทนที่จะต้องสร้างบัญชีผู้จัดจำหน่ายด้วยตนเอง โดยทั่วไป ใบสั่งซื้อจะถูกสร้างโดยเจ้าหน้าที่จัดซื้อ ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF ข้อกำหนดเบื้องต้นคือให้มีการตั้งค่าบัญชีผู้จัดจำหน่ายขาจรในหน้าพารามิเตอร์บัญชีเจ้าหนี้


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>สร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร
1. ไปที่การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด
2. คลิก สร้าง
3. เลือกใช่ในฟิลด์ซัพพลายเออร์ขาจร
    * บัญชีผู้จัดจำหน่ายถูกสร้างขึ้นโดยอัตโนมัติ และกำหนดให้กับใบสั่งซื้อ  บัญชีผู้จัดจำหน่ายจะสร้างขึ้นตามเท็มเพลที่ระบุบนแท็บทั่วไปในหน้าพารามิเตอร์บัญชีเจ้าหนี้  
4. ในฟิลด์ชื่อ ให้พิมพ์ชื่อสำหรับซัพพลายเออร์
5. คลิก ตกลง
    * ขณะนี้สามารถทำใบสั่งซื้อให้เสร็จสมบูรณ์และดำเนินการเช่นเดียวกับใบสั่งอื่น ๆ  ในการดำเนินการนี้ไม่มีลักษณะพิเศษใดๆ ที่เกี่ยวข้อง ใบแจ้งหนี้จะแสดงธุรกรรมที่ครบกำหนดในบัญชีผู้จัดจำหน่ายที่มีการสร้างพร้อมกับใบสั่ง และจึงจะมีการประมวลผลการชำระเงิน

