---
title: ผลรวมย่อยแบบสรุปของคำสั่งซื้อไม่รวมภาษีเกี่ยวกับค่าธรรมเนียมเมื่อใช้โมดูลแบบสรุปของคำสั่งซื้อที่กำหนดเอง
description: บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อคุณใช้โมดูลสรุปใบสั่งที่เลือกเอง และผลรวมย่อยของสรุปใบสั่งไม่รวมภาษีในค่าธรรมเนียมในสถานการณ์ที่ "ราคารวมภาษีขาย"
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848848"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>ผลรวมย่อยแบบสรุปของคำสั่งซื้อไม่รวมภาษีเกี่ยวกับค่าธรรมเนียมเมื่อใช้โมดูลแบบสรุปของคำสั่งซื้อที่กำหนดเอง

บทความนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อคุณใช้โมดูลสรุปใบสั่งที่เลือกเอง และผลรวมย่อยของสรุปใบสั่งไม่รวมภาษีในค่าธรรมเนียมในสถานการณ์ที่ "ราคารวมภาษีขาย"

## <a name="description"></a>คำอธิบาย

Microsoft Dynamics 365 Commerce รุ่น 10.0.27 ได้มีการเปลี่ยนแปลงต่อไปนี้ในสถานการณ์ "ราคารวมภาษีขาย" เพื่อให้ประสบการณ์ที่สอดคล้องกันในโมดูลสรุปใบสั่งในหน้าไซต์อีคอมเมิร์ซ

- มีการเพิ่มฟิลด์ใหม่สองฟิลด์: **TaxOnShippingCharge** และ **TaxOnNonShippingCharges**
- Application Programming Interface (API) ของ **GetSalesOrderBySalesId** และ **GetSalesOrderByTransactionId** มีค่าที่ถูกต้องต่อฟิลด์ต่อไปนี้ในสถานการณ์ "ราคารวมภาษีขาย":

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

อย่างไรก็ตาม ถ้าคุณไม่ได้ใช้โมดูลสรุปใบสั่งที่เลือกเอง การเปลี่ยนแปลงเหล่านี้อาจส่งผลกระทบต่อมูลค่าผลรวมย่อยของสรุปใบสั่ง โดยไม่รวมภาษีที่คิดจากค่าธรรมเนียม

## <a name="resolution"></a>การแก้ปัญหา

ถ้าคุณใช้โมดูลสรุปใบสั่งที่เลือกเอง และไม่ต้องการสืบทอดการเปลี่ยนแปลงที่ได้สร้างขึ้นในสถานการณ์ "ราคารวมภาษีขาย" ใน Commerce รุ่น 10.0.27 และรุ่นที่ใหม่กว่า ให้ปฏิบัติตามคําแนะนําในส่วนนี้

ด้วยการย้อนกลับเป็นลักษณะการทำงานสรุปใบสั่ง (ก่อนรุ่น 10.0.27) ก่อนหน้านี้ของฟิลด์ **salesTransaction.SubtotalAmount** และ **salesTransaction.SubtotalAmountWithoutTax** คุณคืนค่าการรวมของยอดภาษีค่าธรรมเนียมรวม (**TaxOnShippingCharge** และ **TaxOnNonShippingCharges**) ในยอดผลรวมย่อย (**SubtotalAmount** และ **SubtotalAmountWithoutTax**)

เมื่อต้องการย้อนกลับเป็นลักษณะการทำงานสรุปใบสั่งก่อนหน้านี้ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ใน Commerce headquarters เปิดหน้าพารามิเตอร์ Commerce (**การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ Commerce**)
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **พารามิเตอร์การตั้งค่าคอนฟิก**
1. เพิ่มพารามิเตอร์การตั้งค่าคอนฟิกต่อไปนี้ และตั้งค่าของแต่ละค่าเป็น **true**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> ถ้าคุณเคยใช้พารามิเตอร์การตั้งค่าคอนฟิก **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** และต้องการรักษาลักษณะการทำงานเช่นเดียวกันให้กับคุณสมบัติ **order.NetAmountWithoutTax** คุณควรเพิ่มพารามิเตอร์การตั้งค่าคอนฟิก **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** และตั้งค่าให้เป็น **true**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ซ่อนข้อมูลการแจกแจงรายละเอียดภาษีในสรุปใบสั่ง](../hide-taxes-breakup.md)
