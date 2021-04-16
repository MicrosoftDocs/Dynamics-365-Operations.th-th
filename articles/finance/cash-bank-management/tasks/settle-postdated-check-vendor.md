---
title: ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย
description: 'ชำระเช็คลงวันที่ล่วงหน้าที่ออกให้กับผู้จัดจำหน่ายเมื่อธุรกรรมเช็คได้ถูกล้างโดยธนาคารแล้ว หลังจากเช็คได้พ้นกำหนดและถูกล้างโดยธนาคาร '
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89acad0c9421960ff4d07ed8eec798b9068424d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834583"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]