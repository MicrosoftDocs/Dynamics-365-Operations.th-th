---
title: ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย
description: 'ชำระเช็คลงวันที่ล่วงหน้าที่ออกให้กับผู้จัดจำหน่ายเมื่อธุรกรรมเช็คได้ถูกล้างโดยธนาคารแล้ว หลังจากเช็คได้พ้นกำหนดและถูกล้างโดยธนาคาร '
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448473"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย

[!include [banner](../../includes/banner.md)]

ชำระเช็คลงวันที่ล่วงหน้าที่ออกให้กับผู้จัดจำหน่ายเมื่อธุรกรรมเช็คได้ถูกล้างโดยธนาคารแล้ว หลังจากเช็คได้พ้นกำหนดและถูกล้างโดยธนาคาร  

กระบวนงานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนที่คุณเริ่มการทำงานนี้ 

1) ตั้งค่าเช็คลงวันที่ล่วงหน้า

2) ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย



บทบาทของกระบวนงานนี้คือเจ้าหน้าที่ฝ่ายบริหารเงิน  กระบวนงานนี้ใช้บริษัทสาธิต USMF

1. ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > เช็คลงวันที่ล่วงหน้าของผู้จัดจำหน่าย
2. คลิกการชำระเงิน
3. คลิกการชำระรายการหักบัญชี
    * ชำระบัญชีผู้จัดจำหน่ายสำหรับธุรกรรมเช็ค  
4. ปิดหน้า
5. ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป
6. ในฟิลด์แสดง ให้เลือก "ทั้งหมด"
7. เลือกหรือยกเลิกกล่องกาเครื่องหมายการแสดงเฉพาะที่ผู้ใช้ที่สร้างขึ้นเท่านั้น
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
9. คลิกรายการ
10. คลิกใบสำคัญ
11. ปิดหน้า

