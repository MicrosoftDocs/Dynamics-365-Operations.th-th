--- 
title: "สร้างและส่งออกการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบการชำระเงิน ISO20022"
description: "กระบวนงานนี้แสดงวิธีการสร้างบรรทัดการชำระเงินในสมุดรายวันการชำระเงินของผู้จัดจำหน่ายและการสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายโดยใช้ตัวอย่างการโอนย้าย ISO2022 "
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>สร้างและส่งออกการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบการชำระเงิน ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างบรรทัดการชำระเงินในสมุดรายวันการชำระเงินของผู้จัดจำหน่ายและการสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายโดยใช้ตัวอย่างการโอนย้าย ISO2022  

บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ DEMF

นี่คือกระบวนงานที่ห้าจากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611


## <a name="create-payment-lines"></a>สร้างบรรทัดรายการการชำระเงิน
1. ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน
2. คลิก สร้าง
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
4. ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
5. คลิก รายการ
6. คลิก ข้อเสนอการชำระเงิน
7. คลิกสร้างข้อเสนอการชำระเงิน
8. ขยายเรกคอร์ดเพื่อที่จะรวมส่วน
9. คลิกตัวกรอง 
10. ในรายการ เลือกแถวสำหรับตารางผู้จัดจำหน่ายและฟิลด์บัญชีผู้จัดจำหน่าย
11. ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * คุณสามารถใช้เกณฑ์ใดๆ สำหรับการเลือกธุรกรรมของผู้จัดจำหน่ายที่จะชำระเงิน สำหรับตัวอย่างนี้จะใช้ DE-001 เป็นบัญชีผู้จัดจำหน่าย  
12. คลิก ตกลง
13. คลิก ตกลง
14. คลิกสร้างการชำระเงิน

## <a name="generate-an-iso20022-payment-file"></a>สร้างไฟล์การชำระเงิน ISO20022


