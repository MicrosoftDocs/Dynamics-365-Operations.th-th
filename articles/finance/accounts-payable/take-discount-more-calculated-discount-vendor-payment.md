---
title: ใช้มากกว่าส่วนลดที่คำนวณได้สำหรับการชำระเงินของผู้จัดจำหน่าย
description: บทความนี้แนะนำคุณผ่านสถานการณ์สมมติเมื่อรับส่วนลดเงินสดสำหรับยอดเงินที่เพิ่มเติมจากส่วนลดที่มีไว้เดิมในใบแจ้งหนี้ สถานการณ์นี้อาจเกิดขึ้นถ้าองค์กรตกลงกับผู้จัดจำหน่ายในการชำระเงินน้อยกว่าบนใบแจ้งหนี้
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ee74bad071d546724f6ffe336bbe3bdf47e2a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971914"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>ใช้มากกว่าส่วนลดที่คำนวณได้สำหรับการชำระเงินของผู้จัดจำหน่าย

[!include [banner](../includes/banner.md)]

บทความนี้แนะนำคุณผ่านสถานการณ์สมมติเมื่อรับส่วนลดเงินสดสำหรับยอดเงินที่เพิ่มเติมจากส่วนลดที่มีไว้เดิมในใบแจ้งหนี้ สถานการณ์นี้อาจเกิดขึ้นถ้าองค์กรตกลงกับผู้จัดจำหน่ายในการชำระเงินน้อยกว่าบนใบแจ้งหนี้ 

ผู้จัดจำหน่าย 3051 ให้ส่วนลดเงินสด 4 เปอร์เซ็นต์ แก่ Fabrikam หากใบแจ้งหนี้ถูกชำระภายในเจ็ดวัน ในวันที่ 29 มิถุนายน เดือนเมษายนป้อนใบแจ้งหนี้เป็นจำนวนเงิน 1,000.00 ผู้จัดจำหน่ายให้เดือนเมษายนใช้ส่วนลด 60.00 แทนที่เป็นส่วนลดเริ่มต้น 40.00 ที่พร้อมใช้งานสำหรับใบแจ้งหนี้ เดือนเมษายนจะเรกคอร์ดการชำระเงินที่ใช้ครั้งเดียว โดยใช้สมุดรายวันการชำระเงินของบัญชีเจ้าหนี้ เธอป้อนการชำระเงินให้แก่ผู้จัดจำหน่าย และจากนั้น เปิดหน้า **ชำระธุรกรรม** เธอทำเครื่องหมายใบแจ้งหนี้ และเปลี่ยนแปลงมูลค่าในฟิลด์ **จำนวนส่วนลดเงินสด** เป็น **60.00**

| ทำเครื่องหมาย     | ใช้ส่วนลดเงินสด | ใบสำคัญ   | บัญชี | วันที่      | วันที่ครบกำหนด  | ใบแจ้งหนี้ | ยอดเงินในสกุลเงินของธุรกรรม | สกุลเงิน | ยอดเงินที่จะชำระ |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| เลือกแล้ว | ปกติ            | Inv-10040 | 3051    | วันที่ 29 มิถุนายน 2015 | วันที่ 29 กรกฎาคม 2015 | 10040   | 1,000.00                       | USD      | 940.00           |

ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ธุรกรรมการชำระเงิน**

|                              |           |
|------------------------------|-----------|
| วันที่ให้ส่วนลดเงินสด           | วันที่ 12 กรกฏาคม 2015 |
| ยอดส่วนลดเงินสด         | 60.00     |
| ใช้ส่วนลดเงินสด            | ปกติ    |
| ส่วนลดเงินสดที่ใช้          | 0.00      |
| ยอดส่วนลดเงินสดที่จะใช้ | 60.00     |

เดือนเมษายนลงรายการบัญชีสมุดรายวันการชำระเงิน ใบแจ้งหนี้ถูกชำระเต็มจำนวน โดยใช้การชำระเงิน 940.00 และส่วนลด 60.00



