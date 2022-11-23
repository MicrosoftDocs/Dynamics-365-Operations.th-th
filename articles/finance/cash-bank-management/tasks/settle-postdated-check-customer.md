---
title: ชำระเช็คลงวันที่ล่วงหน้าจากลูกค้า
description: 'คุณสามารถชำระเช็คลงวันที่ล่วงหน้าได้หลังจากที่เช็คได้ถูกล้างข้อมูลโดยธนาคารแล้ว '
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e61ac6d6785dd0383d5e5dcaca4cc55bf6deb52
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780027"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>ชำระเช็คลงวันที่ล่วงหน้าจากลูกค้า

[!include [banner](../../includes/banner.md)]

คุณสามารถชำระเช็คลงวันที่ล่วงหน้าได้หลังจากที่เช็คได้ถูกล้างข้อมูลโดยธนาคารแล้ว  นอกจากนี้ธุรกรรมทางการเงินนี้จะล้างข้อมูลธุรกรรมข้ามบัญชีสำหรับเช็คลงวันล่วงหน้าอีกด้วย  

งานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนที่คุณเริ่มการทำงานนี้ 

1) ตั้งค่าเช็คลงวันที่ล่วงหน้า

2) ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับลูกค้า 



บทบาทสำหรับกระบวนงานนี้คือฝ่ายการเงิน 



กระบวนงานนี้ใช้บริษัทสาธิต USMF

1. ไปที่ **สินเชื่อและการเรียกเก็บเงิน > การสอบถามและรายงาน > การชำระเงิน > เช็คลงวันที่ล่วงหน้าของลูกค้า**
2. คลิก **การชำระเงิน**
3. คลิก **การชำระรายการหักบัญชี**
    * ชำระบัญชีลูกค้าสำหรับธุรกรรมเช็ค  
4. ปิดหน้า
5. ไปที่ **บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป**
6. ในฟิลด์ **แสดง** ให้เลือกหนึ่งตัวเลือก
7. เลือกหรือยกเลิกกล่องกาเครื่องหมาย **แสดงเฉพาะที่ผู้ใช้ที่สร้างขึ้นเท่านั้น**
8. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
9. คลิก **รายการ**
10. คลิก **ใบสำคัญ**
11. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
