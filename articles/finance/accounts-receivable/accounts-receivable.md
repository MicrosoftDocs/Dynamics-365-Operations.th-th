---
title: โฮมเพจบัญชีลูกหนี้
description: ใช้บัญชีลูกหนี้เพื่อติดตามใบแจ้งหนี้ของลูกค้าและการชำระเงินขาเข้า
author: abruer
ms.date: 10/24/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerInvoiceWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "20671"
- intro-internal
ms.assetid: 1040678e-ffcb-47fb-a1bc-626db8046504
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7c92ae7972344a6c740f5d4d94334ba0e81fd7e
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715593"
---
# <a name="accounts-receivable-home-page"></a>โฮมเพจบัญชีลูกหนี้

[!include [banner](../includes/banner.md)]

ใช้บัญชีลูกหนี้เพื่อติดตามใบแจ้งหนี้ของลูกค้าและการชำระเงินขาเข้า 

คุณสามารถสร้างใบแจ้งหนี้ของลูกค้าที่ขึ้นอยู่กับใบสั่งขายหรือบันทึกการจัดส่งได้ คุณยังสามารถป้อนใบแจ้งหนี้ข้อความอิสระที่ไม่เกี่ยวข้องกับใบสั่งขาย คุณสามารถรับการชำระเงินโดยใช้การชำระเงินที่แตกต่างกันหลายชนิด ซึ่งรวมถึงตั๋วแลกเงิน เงินสด เช็ค บัตรเครดิต และการชำระเงินทางอิเล็กทรอนิกส์ ถ้าองค์กรของคุณรวมนิติบุคคลหลายราย คุณสามารถใช้การชำระเงินส่วนกลางเพื่อบันทึกการชำระเงินในนิติบุคคลเดี่ยวในนามของนิติบุคคลอื่นๆ


**กระบวนการทางธุรกิจ**

[![กระบวนการทางธุรกิจ](./media/AR-process.PNG)](./media/AR-process.PNG)

## <a name="set-up-accounts-receivable"></a>ตั้งค่าบัญชีลูกหนี้

ใช้บัญชีลูกหนี้เพื่อติดตามใบแจ้งหนี้ของลูกค้าและการชำระเงินที่คุณได้รับจากลูกค้า คุณสามารถตั้งค่ากลุ่มลูกค้า ลูกค้า โพรไฟล์การลงรายการบัญชี ตัวเลือกการชำระเงินต่างๆ ดอกเบี้ยตั๋วเงิน จดหมายเรียกเก็บเงิน ค่าส่งเสริมการขายให้แก่ผู้ขาย และพารามิเตอร์ที่เกี่ยวข้องกับลูกค้า ค่าธรรมเนียม การจัดส่งและปลายทาง ตั๋วแลกเงิน และข้อมูลบัญชีลูกหนี้ชนิดอื่น 

- [การกระจายการลงบัญชีและรายการสมุดรายวันของบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ข้อความอิสระ](accounting-distributions-subledger-journal-entries-free-text-invoices.md)
- [โพรไฟล์การลงรายการบัญชีลูกค้า](customer-posting-profiles.md)
- [การตั้งค่า การตรวจสอบ และการรวบรวมข้อมูลบัตรเครดิต](credit-card-authorizations.md)
- [สร้างใบแจ้งหนี้ของลูกค้า](configure-customer-invoices.md)
- [ตั้งค่า และประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ](set-up-process-recurring-invoices.md)
- [แก้ไขใบแจ้งหนี้ข้อความอิสระ](correct-free-text-invoice.md)
- [ตั้งค่าตั๋วแลกเงิน](set-up-bills-exchange.md)
- [การตั้งค่าอัตราดอกเบี้ยสำหรับรหัสดอกเบี้ย](set-up-interest-rates-interest-code.md)
- [ยกเว้น กลับมาคิด หรือย้อนกลับรายการค่าธรรมเนียมดอกเบี้ย](waive-reinstate-reverse-interest-fees.md)
- [ภาพรวมการหักบัญชีเงินฝากอัตโนมัติ SEPA](sepa-direct-debit-overview.md)
- [ตั้งค่าข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ SEPA](sepa-direct-debit-mandate.md)
- [การปิดบัญชีลูกหนี้](close-accounts-receivable.md)
    
## <a name="set-up-credit-and-collections"></a>การตั้งค่าสินเชื่อและการเรียกเก็บเงิน

ข้อมูลการเรียกเก็บเงินบัญชีลูกหนี้ถูกจัดการในมุมมองส่วนกลางหนึ่งมุมมอง ในหน้าการเรียกเก็บเงิน ผู้จัดการฝ่ายสินเชื่อและการเรียกเก็บเงินสามารถใช้มุมมองส่วนกลางนี้ เพื่อจัดการการเรียกเก็บเงิน ตัวแทนเรียกเก็บเงินจะเริ่มกระบวนการเรียกเก็บเงินจากรายชื่อลูกค้า ที่ถูกสร้างขึ้นโดยการใช้เกณฑ์การเรียกเก็บเงินที่กำหนดไว้ล่วงหน้า หรือจากหน้าลูกค้า

- [สินเชื่อและการเรียกเก็บเงินในบัญชีลูกหนี้](collections-credit-accounts-receivable.md)
- [ตั้งค่าคอนฟิกบัญชีลูกหนี้และสินเชื่อและการเรียกเก็บเงิน](accounts-receivables-set-up-overview.md)
- [การตั้งค่าสินเชื่อและการเรียกเก็บเงิน](set-up-collections.md)

## <a name="set-up-payments-and-settlements"></a>ตั้งค่าการชำระเงินและการตัดจ่าย

ยอมรับการชำระเงินจากลูกค้า เช่นตั๋วแลกเงิน เงินสด เช็ค บัตรเครดิต และการชำระเงินทางอิเล็กทรอนิกส์ชนิดต่างๆ 

- [ใช้การชำระเงินของลูกค้าเพื่อชำระใบแจ้งหนี้หลายใบที่ครอบคลุมรอบระยะเวลาส่วนลดหลายรายการ](customer-payment-settle-multiple-invoices-multiple-discount-periods.md)
- [การชำระเงินส่วนกลางสำหรับบัญชีลูกหนี้](centralized-payments-accounts-receivable.md)
- [ชำระเงินบางส่วนของลูกค้า และการชำระเงินครั้งสุดท้ายเต็มจำนวนก่อนวันที่ให้ส่วนลด](../accounts-payable/settle-partial-customer-payment-or-final-payment-before-discount.md)
- [การชำระเงินบางส่วนของผู้ซิ้อก่อนวันที่ให้ส่วนลดกับการชำระเงินครั้งสุดท้ายหลังจากวันที่ให้ส่วนลด](settle-partial-customer-payment-before-discount-or-final-payment-after.md)
- [การชำระเงินบางส่วนของผู้ซิ้อที่มีส่วนลดในใบลดหนี้](settle-partial-customer-payment-discounts-credit-notes.md)
- [ชำระการชำระเงินของลูกค้าบางส่วนที่มีรอบระยะเวลาส่วนลดหลายรอบ](settle-partial-customer-payment-multiple-discount-periods.md)
- [ชำระเงินคืนลูกค้า](reimburse-customers.md)
- [การชำระเงินของลูกค้าสำหรับยอดเงินบางส่วน](customer-payments-partial-amount.md)
   
### <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

#### <a name="whats-new-and-in-development"></a>มีอะไรใหม่และอะไรที่กำลังพัฒนา

ไปที่ [แผนการทำงานของ Microsoft Dynamics 365](/dynamics365/release-plans/) เพื่อดูว่ามีคุณสมบัติใหม่ใดวางแผนไว้ 

#### <a name="blogs"></a>บล็อก

คุณสามารถค้นหาความคิดเห็น ข่าวสาร และข้อมูลอื่นๆ เกี่ยวกับบัญชีลูกหนี้และโซลูชันอื่นๆ ได้ใน [บล็อก Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) และ [บล็อกการเงินและการดำเนินงานของ Microsoft Dynamics 365 - การเงิน](https://community.dynamics.com/365/financeandoperations/b/financials)

[บล็อกชุมชนคู่ค้า Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) มอบทรัพยากรเดียวให้กับคู่ค้า Microsoft Dynamics สำหรับเรียนรู้สิ่งใหม่และแนวโน้มต่างๆ ใน Dynamics 365

#### <a name="task-guides"></a>คู่มืองาน
วิธีใช้เพิ่มเติมสามารถใช้เป็นคู่มืองานภายในแอปพลิเคชัน ในการเข้าถึงคู่มืองาน ให้คลิกปุ่มวิธีใช้บนหน้าใดๆ

#### <a name="videos"></a>วิดีโอ

ดูวิดีโอวิธีการที่ตอนนี้มีอยู่บน [ช่อง YouTube ของ Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)









[!INCLUDE[footer-include](../../includes/footer-banner.md)]

