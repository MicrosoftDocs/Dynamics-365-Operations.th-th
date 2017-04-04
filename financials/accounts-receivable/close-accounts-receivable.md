---
title: "การปิดบัญชีลูกหนี้"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 013c638b93bf2fe97b594de57a363c11e9a98dad
ms.lasthandoff: 03/31/2017


---

# <a name="close-accounts-receivable"></a>การปิดบัญชีลูกหนี้



ตารางต่อไปนี้แสดงรายการหน้าที่สนับสนุนกระบวนการทางธุรกิจการปิดบัญชีลูกหนี้

> [!NOTE] 
> เมื่อต้องการเปิดบางหน้าในตาราง คุณต้องป้อนข้อมูล หรือระบุการตั้งค่าพารามิเตอร์

**Business process component task**                   

ปิดรอบระยะเวลาในบัญชีแยกประเภททั่วไป

| ชื่อหน้า                            | การใช้                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|ชุดงาน                             | ดูหรือสร้างชุดงาน ชุดงานอาจไม่เสร็จสมบูรณ์ และคุณต้องตรวจสอบให้แน่ใจว่าการลงรายการบัญชีทั้งหมดเสร็จสมบูรณ์แล้ว                                                                                                               |
|ยืนยันใบสั่งขาย                   | อัพเดตใบสั่งขาย                                                                       |
|การประเมินค่าใหม่ตามสกุลเงินต่างประเทศ          | สร้างธุรกรรมที่อัพเดตมูลค่าของธุรกรรมลูกค้าที่เปิดค้างไว้ในสกุลเงินต่างประเทศ                                                                                                                         |
| สมุดรายวัน                              | ลงรายการบัญชีใบแจ้งหนี้ การชำระเงิน และตั๋วสัญญาใช้เงิน                                             |
| ใบสำคัญสมุดรายวัน                      | -   **Payment journal** – Generate, process, and post payments.
                                         -   **Draw bill of exchange journal** – Post bills of exchange.
                                         -   **Protest bill of exchange journal** – Post protested bills of exchange.
                                         -   **Redraw bill of exchange journal** – Post redrawn bills of exchange.
                                         -   **Remittance journal** – Post remittances.
                                         -   **Settle bill of exchange journal** – Post settled bills of exchange                   |
| ลงรายการบัญชีบันทึกการจัดส่งสินค้า | อัพเดตบันทึกการจัดส่งสำหรับใบสั่งขาย                                                     | | ใบแจ้งหนี้ข้อความอิสระประกาศ | ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ                                                                   | | ลงรายการบัญชีใบแจ้งหนี้ | ลงรายการบัญชีใบแจ้งหนี้สำหรับใบสั่งขาย                                                            | | ลงรายการบัญชีรายการเบิกสินค้า | ปรับปรุงรายการเบิกสินค้าสำหรับใบสั่งขาย                                                      |

**Business process component task**   

การสร้างและการส่งรายการขายใน EU

| ชื่อหน้า                            | การใช้                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|รายการขายใน EU                         | รายงานการขายในสหภาพยุโรป (EU) ไปยังหน่วยงานจัดเก็บภาษีสำหรับวัตถุประสงค์การรายงานภาษีมูลค่าเพิ่ม (VAT)                                                                                                                           |





