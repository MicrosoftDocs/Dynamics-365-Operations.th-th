---
title: ตั้งค่าลูกค้าและบัญชีธนาคารของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022
description: 'งานนี้จะช่วยคุณในการตั้งค่าบัญชีธนาคารของลูกค้าและข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของลูกค้าที่จำเป็นในการสร้างไฟล์การชำระเงินของลูกค้า เช่น การหักบัญชีเงินฝากอัตโนมัติ ISO20022 '
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595e89faa1e24ca937d399994e15ce53e3f5308b1c6fd7f43e4e831e70c15ad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736878"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>ตั้งค่าลูกค้าและบัญชีธนาคารของลูกค้าสำหรับการหักบัญชีเงินฝากอัตโนมัติ ISO20022

[!include [banner](../../includes/banner.md)]

งานนี้จะช่วยคุณในการตั้งค่าบัญชีธนาคารของลูกค้าและข้อตกลงการหักบัญชีเงินฝากอัตโนมัติของลูกค้าที่จำเป็นในการสร้างไฟล์การชำระเงินของลูกค้า เช่น การหักบัญชีเงินฝากอัตโนมัติ ISO20022  ทั้งนี้ขึ้นอยู่กับรูปแบบการชำระเงินของลูกค้าที่ตั้งค่าไว้ อาจจำเป็นต้องมีรายละเอียดเพิ่มเติมซึ่งไม่ครอบคลุมอยู่ในกระบวนงานนี้สำหรับลูกค้าหรือบัญชีธนาคารของลูกค้า 

งานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF ที่มีที่อยู่หลักของนิติบุคคลในเยอรมนี



นี่คือกระบวนงานที่สี่จากกระบวนงานห้ารายการที่แสดงให้เห็นถึงขั้นตอนการชำระเงินของลูกค้าโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์


## <a name="set-up-a-customer-bank-account"></a>ตั้งค่าบัญชีธนาคารลูกค้า
1. ไปที่บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด
2. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  เช่น กรองข้อมูลในฟิลด์บัญชี ด้วยค่า 'DE-010'
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. ในบานหน้าต่างการดำเนินการ คลิก ลูกค้า
5. คลิก บัญชีธนาคาร
6. คลิก สร้าง
7. ในฟิลด์บัญชีธนาคาร ให้พิมพ์ค่า
8. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
    * ตัวอย่างเช่น ป้อน 'ธนาคาร EUR'  
9. ในฟิลด์กลุ่มธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
10. ในฟิลด์ IBAN ให้พิมพ์ค่า
    * ตัวอย่างเช่น ป้อน 'DE36200400000628808808'  
11. ในฟิลด์รหัส SWIFT ให้พิมพ์ค่าใดค่าหนึ่ง
    * ตัวอย่างเช่น: พิมพ์ 'COBADEFFXXX'  โปรดทราบว่าไม่จำเป็นต้องใช้ SWIFT \ BIC สำหรับรูปแบบการชำระเงินหลายรายการ อย่างไรก็ตาม ขอแนะนำให้ลงทะเบียนสำหรับบัญชีธนาคาร  
12. คลิก บันทึก
13. ปิดหน้า
14. คลิก แก้ไข
15. ขยายส่วนค่าเริ่มต้นของการชำระเงิน
16. ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง

## <a name="add-a-direct-debit-mandate"></a>เพิ่มข้อบังคับการหักบัญชีเงินฝากอัตโนมัติ
1. ขยายส่วนข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ
2. คลิก เพิ่ม
3. ในฟิลด์บัญชีธนาคารของเจ้าหนี้ ให้ป้อนหรือเลือกค่า
    * ตัวอย่างเช่น เลือก DEMF OPER  
4. ในฟิลด์วันที่ที่เซ็นรับรอง ให้ป้อนวันที่
5. คลิก ใช่ เพื่อยืนยันการปรับปรุงวันที่
6. ในฟิลด์สถานที่ที่เซ็นรับรอง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
7. ในฟิลด์การชำระเงินของตัวเลขที่คาดการณ์ ให้ป้อนหมายเลข
8. คลิก ตกลง
9. คลิก บันทึก



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]