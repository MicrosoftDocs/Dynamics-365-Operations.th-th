---
title: เลตเตอร์ออฟเครดิตสำหรับการส่งออก
description: 'กระบวนงานนี้นำไปสู่กระบวนการเลตเตอร์ออฟเครดิตการส่งออก '
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779566"
---
# <a name="export-letter-of-credit"></a>เลตเตอร์ออฟเครดิตสำหรับการส่งออก

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้นำไปสู่กระบวนการเลตเตอร์ออฟเครดิตการส่งออก 

เลตเตอร์ออฟเครดิตคือ ข้อตกลงที่ออก โดยธนาคาร ที่ธนาคารตกลงเพื่อให้แน่ใจว่าการชำระเงินในนามของผู้ซื้อ ว่าตรงตามเงื่อนไขของข้อตกลงระหว่างผู้ซื้อและผู้ขาย



ดำเนินงานกระบวนงาน **ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์** และกระบวนงาน **เลตเตอร์ออฟเครดิต สร้างข้อตกลงสินเชื่อธนาคาร** ก่อนกระบวนงานนี้ ต้องเลือกบริษัทสาธิต USMF เพื่อเรียกใช้กระบวนงานนี้ได้อย่างเสร็จสมบูรณ์


## <a name="create-sales-order-for-export-letter-of-credit"></a>สร้างใบสั่งขายสำหรับเลตเตอร์ออฟเครดิตการส่งออก
1. ไปที่ **บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**
2. คลิก **สร้าง**
3. ในฟิลด์ **บัญชีลูกค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
6. ขยายหรือยุบส่วน **ทั่วไป**
7. ในฟิลด์ **ไซต์** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * เลือก **ไซต์** ที่สินค้าที่จะออกได้ถูกจัดเก็บ  
8. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
9. ในฟิลด์ **คลังสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * เลือก **คลังสินค้า** ที่สินค้าที่จะออกได้ถูกจัดเก็บ  
10. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * หมายเหตุ: ฟิลด์ **ชนิดเอกสารธนาคาร** ควรถูกเลือกกับ **เลตเตอร์ออฟเครดิต**  
11. ในฟิลด์ **ชนิดของเอกสารธนาคาร** ให้เลือก **เลตเตอร์ออฟเครดิต**
12. ขยายหรือยุบส่วน **การจัดส่ง**
    * เลือก **การควบคุมวันที่จัดส่ง** = **ไม่มี**  
13. ในฟิลด์ **วันที่ขอรับสินค้า** ให้ป้อนวันที่
14. คลิก **ตกลง** 
15. ในฟิลด์ **หมายเลขสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * เลือกสินค้าที่ต้องการจะออก/ขาย  
16. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
17. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
18. ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อนหมายเลข
19. ขยายหรือยุบส่วน **รายละเอียดของรายการ**
20. คลิกแท็บ **การจัดส่ง**
21. ในฟิลด์ **วันที่จัดส่งที่ร้องขอ** ให้ป้อนวันที่
22. ในฟิลด์ **วันที่จัดส่งที่ยืนยัน** ให้ป้อนวันที่
23. ในบานหน้าต่างการดำเนินการ คลิก **จัดการ**
24. คลิก **เลตเตอร์ออฟเครดิต**
25. ในฟิลด์ **หมายเลขเอกสารธนาคาร** ให้พิมพ์ค่าใดค่าหนึ่ง
26. ในฟิลด์ **วันหมดอายุ** ให้ป้อนวันที่และเวลา
27. ขยายหรือยุบส่วน **รายละเอียดธนาคาร**
28. ในฟิลด์ **ธนาคารผู้ออก** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
29. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
30. ในฟิลด์ **ธนาคารผู้แจ้งเครดิต** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
31. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
32. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
33. คลิก **นำการจัดส่งของใบสั่งขายมาใช้**
34. คลิก **ออกเอกสารธนาคาร**
35. ปิดหน้า

## <a name="post-packing-slip"></a>ลงรายการบัญชีบันทึกการจัดส่ง
1. บนบานหน้าต่างการดำเนินการ คลิก **เบิกสินค้าและจัดส่ง**
2. คลิก **ลงรายการบัญชีบันทึกการส่ง**
3. ขยายหรือยุบส่วน **พารามิเตอร์**
4. ในฟิลด์ **ปริมาณ** ให้เลือก **ทั้งหมด**
5. ขยายหรือยุบส่วน **การตั้งค่า**
6. ในฟิลด์ **วันที่ในบันทึกการจัดส่ง** ให้ป้อนวันที่
7. เลือกหมายเลขการจัดส่ง
8. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
9. คลิก **ตกลง** 
10. คลิก **ตกลง** 

## <a name="post-sales-invoice"></a>ลงรายการบัญชีใบแจ้งหนี้การขาย
1. บนบานหน้าต่างการดำเนินการ คลิก **ใบแจ้งหนี้**
2. คลิก **ใบแจ้งหนี้**
3. ขยายหรือยุบส่วน **ภาพรวม**
4. เลือก **หมายเลขการจัดส่ง**
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
6. ขยายหรือยุบส่วน **การตั้งค่า**
7. ในฟิลด์ **วันที่ของใบแจ้งหนี้** ให้ป้อนวันที่
8. คลิก **ตกลง** 
9. คลิก **ตกลง** 

## <a name="shipment-document-submitted-status"></a>สถานะการจัดส่งเอกสารแล้ว
1. ในบานหน้าต่างการดำเนินการ คลิก **จัดการ**
2. คลิก **เลตเตอร์ออฟเครดิต**
3. ขยายหรือยุบส่วน **รายการ**
    * หมายเหตุ: ฟิลด์ **เอกสารที่ส่ง** ควรถูกตั้งเป็น **ใช่**  

## <a name="verify-export-letter-of-credit"></a>ตรวจสอบเลตเตอร์ออฟเครดิตสำหรับการส่งออก
1. ไปที่ **การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > เลตเตอร์ออฟเครดิตสำหรับการส่งออกและการเรียกเก็บเงินสำหรับการนำเข้า**
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * ตรวจสอบว่า **เลตเตอร์ออฟเครดิตการส่งออก** มี **สถานะการจัดส่ง** เป็น **ออกใบแจ้งหนี้แล้ว**  

## <a name="customer-payment"></a>การชำระเงินของลูกค้า
1. ไปที่ **บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน**
2. คลิก **สร้าง**
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
4. ในฟิลด์ **ชื่อ** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
6. คลิก **รายการ**
7. ในฟิลด์ **วันที่** ให้ป้อนวันที่
8. ในฟิลด์ **บัญชี** ให้ระบุค่าที่ต้องการ
9. คลิก **การชำระเงิน**
10. เลือกกล่องกาเครื่องหมายในส่วนหัวของยอดรวม
    * หมายเหตุ: ตั้งค่าฟิลด์ **แสดง** เป็น **เลตเตอร์ออฟเครดิต**  
11. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
12. เลือกหรือล้างกล่องกาเครื่องหมาย **เครื่องหมาย**
13. คลิก **ตกลง** 
14. คลิกแท็บ **การชำระเงิน**
    * ตรวจสอบหมายเลขเอกสารของธนาคาร และรายละเอียดหมายเลขการจัดส่ง  
15. คลิก **ลงรายการบัญชี**

## <a name="verify-export-letter-of-credit-after-payment"></a>ตรวจสอบเลตเตอร์ออฟเครดิตสำหรับการส่งออกหลังจากการชำระเงิน
1. ไปที่ **การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > เลตเตอร์ออฟเครดิตสำหรับการส่งออกและการเรียกเก็บเงินสำหรับการนำเข้า**
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * ตรวจสอบว่า **สถานะการจัดส่ง** = **การชำระเงินที่ได้รับ** และ **ยอดดุล** = **0.00**  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
