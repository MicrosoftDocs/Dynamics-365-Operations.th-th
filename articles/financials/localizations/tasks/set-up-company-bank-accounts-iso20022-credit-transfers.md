--- 
title: "ตั้งค่าบัญชีธนาคารของบริษัทสำหรับการโอนย้ายเครดิต ISO20022"
description: "กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลบัญชีธนาคารเฉพาะบริษัทที่จำเป็นสำหรับการสร้างไฟล์การชำระเงิน "
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>ตั้งค่าบัญชีธนาคารของบริษัทสำหรับการโอนย้ายเครดิต ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลบัญชีธนาคารเฉพาะบริษัทที่จำเป็นสำหรับการสร้างไฟล์การชำระเงิน  คุณตั้งค่าข้อมูลที่จำเป็นในการสร้างรูปแบบการโอนย้ายเครดิต ISO 20022 แต่ทั้งนี้ขึ้นอยู่กับรูปแบบ อาจจำเป็นต้องมีข้อมูลอื่น เช่น รหัสบริษัทหรือรหัสเรียงลำดับ  

บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF

นี่คือกระบวนงานที่สองจากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์  กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611


## <a name="set-up-iban-and-swift-code"></a>ตั้งค่ารหัส IBAN และ SWIFT
1. ไปที่การจัดการเงินสดและธนาคาร > บัญชีธนาคาร
2. ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'DEMF OPER'
3. คลิก DEMF OPER เพื่อเปิดรายละเอียดบัญชีธนาคาร
4. คลิก แก้ไข
5. ขยายส่วนการระบุรหัสประจำตัวเพิ่มเติม
6. ในฟิลด์ IBAN ให้พิมพ์ 'DE89370400440532013000'
7. ในฟิลด์รหัส SWIFT ให้พิมพ์ 'DEUTDEFF'
    * โปรดทราบว่าไม่จำเป็นต้องใช้ SWIFT\BIC สำหรับรูปแบบการชำระเงินหลายรายการ อย่างไรก็ตาม ขอแนะนำให้ลงทะเบียนสำหรับบัญชีธนาคาร  
8. คลิก บันทึก

## <a name="set-up-bank-account-for-the-legal-entity"></a>ตั้งค่าบัญชีธนาคารสำหรับนิติบุคคล
1. ไปที่การจัดการองค์กร > องค์กร > นิติบุคคล
2. คลิก แก้ไข
3. ขยายส่วนของข้อมูลบัญชีธนาคาร
4. ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
5. คลิก บันทึก


