---
title: ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย
description: 'ชำระเช็คลงวันที่ล่วงหน้าที่ออกให้กับผู้จัดจำหน่ายเมื่อธุรกรรมเช็คได้ถูกล้างโดยธนาคารแล้ว หลังจากเช็คได้พ้นกำหนดและถูกล้างโดยธนาคาร '
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e3816a2f1c95d568a173cb07daad0473703da9c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779513"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย

[!include [banner](../../includes/banner.md)]

ชำระเช็คลงวันที่ล่วงหน้าที่ออกให้กับผู้จัดจำหน่ายเมื่อธุรกรรมเช็คได้ถูกล้างโดยธนาคารแล้ว หลังจากเช็คได้พ้นกำหนดและถูกล้างโดยธนาคาร  

กระบวนงานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนที่คุณเริ่มการทำงานนี้ 

1) ตั้งค่าเช็คลงวันที่ล่วงหน้า

2) ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย



บทบาทของกระบวนงานนี้คือเจ้าหน้าที่ฝ่ายบริหารเงิน  กระบวนงานนี้ใช้บริษัทสาธิต USMF

1. ไปที่ **บัญชีเจ้าหนี้ > การชำระเงิน > เช็คลงวันที่ล่วงหน้าของผู้จัดจำหน่าย**
2. คลิก **การชำระเงิน**
3. คลิก **การชำระรายการหักบัญชี**
    * ชำระบัญชีผู้จัดจำหน่ายสำหรับธุรกรรมเช็ค  
4. ปิดหน้า
5. ไปที่ **บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป**
6. ในฟิลด์ **แสดง** ให้เลือก **ทั้งหมด**
7. เลือกหรือยกเลิกกล่องกาเครื่องหมาย **แสดงเฉพาะที่ผู้ใช้ที่สร้างขึ้นเท่านั้น**
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
9. คลิก **รายการ**
10. คลิก **ใบสำคัญ**
11. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
