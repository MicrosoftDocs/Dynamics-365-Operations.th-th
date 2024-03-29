---
title: สร้างสมุดรายวันการตัดจ่ายสำหรับลูกค้า
description: 'คู่มือการทำงานนี้จะแสดงวิธีการตั้งค่าพารามิเตอร์สำหรับการตัดจ่าย และตัดธุรกรรมจากหน้าการเรียกเก็บเงิน หน้าใบแจ้งหนี้ของลูกค้าเปิดและหน้าของลูกค้า '
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21aaeda413e767fed1815423b0262127c6692bb6
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775311"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>สร้างสมุดรายวันการตัดจ่ายสำหรับลูกค้า

[!include [banner](../../includes/banner.md)]

คู่มือการทำงานนี้จะแสดงวิธีการตั้งค่าพารามิเตอร์สำหรับการตัดจ่าย และตัดธุรกรรมจากหน้าการเรียกเก็บเงิน หน้าใบแจ้งหนี้ของลูกค้าเปิดและหน้าของลูกค้า  งานนี้ใช้บริษัทสาธิต USMF 


## <a name="set-up-the-write-off-parameters"></a>ตั้งค่าพารามิเตอร์การตัดจ่าย
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > พารามิเตอร์บัญชีลูกหนี้**
2. คลิกแท็บ **การเรียกเก็บเงิน**
3. ขยายหรือยุบส่วน **ตัดจ่าย**
    - **สมุดรายวันการตัดจ่าย** คือสมุดรายวันทั่วไปที่จะเก็บธุรกรรมการตัดจ่ายที่คุณสร้างขึ้น  
    - คุณสามารถแนบรหัสเหตุผลสำหรับการตัดจ่ายได้ทุกครั้ง  คุณสามารถแทนค่าเริ่มต้นนี้ในขณะการตัดจ่ายได้  
    - ตั้งค่า **แยกภาษีขาย** เป็นใช่ ถ้าคุณต้องการแยกภาษีขายออกจากธุรกรรมดั้งเดิมในการตัดจ่าย  
4. ปิดหน้า
5. ไปที่ **สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > โพรไฟล์การลงรายการบัญชีลูกค้า** บัญชีตัดจ่ายจะถูกใช้เป็นบัญชีค่าใช้จ่าย หรือจองการปรับปรุงในสมุดรายวันทั่วไป
6. ปิดหน้า

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>ตัดจ่ายยอดดุลของลูกค้าจากหน้ายอดดุลตามอายุหนี้
1. ไปที่ **สินเชื่อและการเรียกเก็บเงิน > การเรียกเก็บเงิน > ยอดดุลตามอายุหนี้**
2. ทำเครื่องหมายที่แถวสำหรับลูกค้าที่คุณต้องการตัดจ่าย  ตัวอย่างเช่น ทำเครื่องหมายบรรทัดรายการที่มี บริษัท Birch อยู่
3. ใน **บานหน้าต่างการดำเนินการ** คลิก **รวบรวม**
4. คลิก **ตัดจ่าย**
5. คลิก **ตกลง**
6. ปิดหน้า
7. ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > บัญชีแยกประเภททั่วไป**
8. เลือกหมายเลขชุดงานสมุดรายวันสำหรับสมุดรายวันที่มีการตัดจ่ายของคุณอยู่ หนึ่งบรรทัดจะถูกสร้างขึ้นมาเพื่อกลับรายการยอดดุลลูกค้า  อีกอย่างน้อยหนึ่งบรรทัดจะถูกสร้างขึ้นเพื่อลงรายการการตัดจ่ายไปยังบัญชีตัดจ่าย  
9. ปิดหน้า


## <a name="write-off-transactions-from-the-collections-page"></a>ตัดจ่ายธุรกรรมจากหน้าการเรียกเก็บเงิน
1. ไปที่ **สินเชื่อและการเรียกเก็บเงิน > การเรียกเก็บเงิน > ยอดดุลตามอายุหนี้**
2. เลือกชื่อของลูกค้าที่มีธุรกรรมที่คุณต้องการตัดจ่าย  ตัวอย่างเช่น เลือก Cave Wholesales (สหรัฐอเมริกา-004)
3. ทำเครื่องหมายบนแถวธุรกรรมที่หนึ่ง
4. ทำเครื่องหมายบนแถวธุรกรรมที่สอง
5. คลิก **ตัดจ่าย**
6. ในฟิลด์ **ข้อคิดเห็นเกี่ยวกับเหตุผล** พิมพ์ 'Bad debts'
7. คลิก **ตกลง**
8. ปิดหน้า
9. ปิดหน้า
10. ไปที่ **บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป**
11. เลือกหมายเลขชุดงานสมุดรายวันสำหรับสมุดรายวันที่มีการตัดจ่ายของคุณอยู่ หนึ่งบรรทัดจะถูกสร้างขึ้นมาเพื่อกลับรายการยอดดุลลูกค้า  อีกอย่างน้อยหนึ่งบรรทัดจะถูกสร้างขึ้นเพื่อลงรายการการตัดจ่ายไปยังบัญชีตัดจ่าย  
12. ปิดหน้า


## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>ตัดจ่ายใบแจ้งหนี้จากหน้าใบแจ้งหนี้ของลูกค้าที่เปิดไว้
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ใบแจ้งหนี้ > เปิดใบแจ้งหนี้ของลูกค้า**
2. ทำเครื่องหมายบรรทัดรายการสำหรับใบแจ้งหนี้  ตัวอย่างเช่น ทำเครื่องหมายในรายการสำหรับ CIV-000667
3. บน **บานหน้าต่างการดำเนินการ** คลิก **ใบแจ้งหนี้**
4. คลิก **ตัดจ่าย**
5. คลิก **ตกลง**
6. ปิดหน้า

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>ตัดจ่ายยอดดุลของลูกค้าจากหน้าเพจของลูกค้า
1. ไปที่ **บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด**
2. เลือกรหัสลูกค้า  ตัวอย่างเช่น เลือก สหรัฐอเมริกา-001 (Contoso Retail Diego San)
3. ใน **บานหน้าต่างการดำเนินการ** คลิก **รวบรวม**
4. คลิก **ตัดจ่าย**
5. คลิก **ตกลง**
6. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
