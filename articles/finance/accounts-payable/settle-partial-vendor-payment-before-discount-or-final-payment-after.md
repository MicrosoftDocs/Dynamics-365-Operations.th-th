---
title: การชำระเงินบางส่วนก่อนวันที่ให้ส่วนลดและการชำระเงินครั้งสุดท้ายหลังจากวันที่ให้ส่วนลด
description: บทความนี้แนะนำคุณผ่านสถานการณ์ที่มีการชำระเงินบางส่วนหลายรายการ บางรายการภายในรอบระยะเวลาส่วนลดเงินสดและอื่นๆ นอกรอบระยะเวลาส่วนลดเงินสด
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a30bd1c032d27405c17388465eb813d6c87c270
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971989"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>การชำระเงินบางส่วนก่อนวันที่ให้ส่วนลดและการชำระเงินครั้งสุดท้ายหลังจากวันที่ให้ส่วนลด

[!include [banner](../includes/banner.md)]

บทความนี้แนะนำคุณผ่านสถานการณ์ที่มีการชำระเงินบางส่วนหลายรายการ บางรายการภายในรอบระยะเวลาส่วนลดเงินสดและอื่นๆ นอกรอบระยะเวลาส่วนลดเงินสด

Fabrikam ซื้อสินค้าจากผู้จัดจำหน่าย 3057 Fabrikam ได้รับส่วนลดเงินสด 1 เปอร์เซ็นต์ หากใบแจ้งหนี้ถูกชำระภายใน 14 วัน ใบแจ้งหนี้ต้องชำระใน 30 วัน ผู้จัดจำหน่ายยังอนุญาตให้ใช้ส่วนลดเงินสดในการชำระเงินบางส่วนของ Fabrikam ได้ พารามิเตอร์การชำระเงิน ตั้งอยู่บนหน้า **พารามิเตอร์บัญชีลูกหนี้**

## <a name="invoice-on-june-25"></a>ออกใบแจ้งหนี้ : 25 มิถุนายน
ในวันที่ 25 มิถุนายน April ป้อนและลงรายการบัญชีใบแจ้งหนี้เป็นจำนวนเงิน 1,000.00 สำหรับผู้จัดจำหน่าย 3057 April สามารถดูธุรกรรมนี้ในหน้า **ธุรกรรมผู้จัดจำหน่าย**

| ใบสำคัญ   | ชนิดธุรกรรม | วันที่      | ใบแจ้งหนี้ | ยอดเงินในเดบิตในสกุลเงินของธุรกรรม | ยอดเงินในเครดิตในสกุลเงินของธุรกรรม | ยอดดุล   | สกุลเงิน |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | ใบแจ้งหนี้          | วันที่ 25 มิถุนายน 2015 | 10020   |                                      | 1,000.00                              | -1,000.00. | USD      |

## <a name="partial-payment-on-july-2"></a>การชำระเงินเป็นบางส่วนในวันที่ 2 กรกฏาคม
ในวันที่ 2 กรกฎาคม April ต้องการชำระ 300.00 ของใบแจ้งหนี้นี้ การชำระเงินมีสิทธิได้รับส่วนลด เนื่องจาก Fabrikam ใช้ส่วนลดในการชำระเงินบางส่วน ดังนั้น April จะจ่าย 297.00 และใช้ส่วนลด 3.00 เธอสร้างสมุดรายวันการชำระเงิน และป้อนบรรทัดหนึ่งบรรทัดสำหรับผู้จัดจำหน่าย 3057 จากนั้น เธอจะเปิดหน้า **ธุรกรรมการชำระเงิน** เพื่อให้เธอสามารถทำเครื่องหมายใบแจ้งหนี้ที่จะถูกชำระเงิน

| ทำเครื่องหมาย     | ใช้ส่วนลดเงินสด | ใบสำคัญ   | บัญชี | วันที่      | วันที่ครบกำหนด  | ใบแจ้งหนี้ | ยอดเงินในสกุลเงินของธุรกรรม | สกุลเงิน | ยอดเงินที่จะชำระ |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| เลือกแล้ว | ปกติ            | Inv-10020 | 3057    | วันที่ 25 มิถุนายน 2015 | วันที่ 25 กรกฏาคม 2015 | 10020   | -1,000.00.                      | USD      | -297.00          |

ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ชำระธุรกรรมที่ค้างอยู่**

|                              |           |
|------------------------------|-----------|
| วันที่ให้ส่วนลดเงินสด           | วันที่ 9 กรกฎาคม 2015 |
| ยอดส่วนลดเงินสด         | -10.00    |
| ใช้ส่วนลดเงินสด            | ปกติ    |
| ส่วนลดเงินสดที่ใช้          | 0.00      |
| ยอดส่วนลดเงินสดที่จะใช้ | -3.00     |

จากนั้น April ลงรายการบัญชีการชำระเงิน ใบแจ้งหนี้ตอนนี้มียอดดุล 700.00 April สามารถดูธุรกรรมนี้ในหน้า **ธุรกรรมผู้จัดจำหน่าย**

| ใบสำคัญ    | ชนิดธุรกรรม | วันที่      | ใบแจ้งหนี้ | ยอดเงินในเดบิตในสกุลเงินของธุรกรรม | ยอดเงินในเครดิตในสกุลเงินของธุรกรรม | ยอดดุล | สกุลเงิน |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | ใบแจ้งหนี้          | วันที่ 25 มิถุนายน 2015 | 10020   |                                      | 1,000.00                              | -700.00. | USD      |
| APP-10020  | การชำระเงิน          | วันที่ 1 กรกฎาคม 2015  |         | 297.00                               |                                       | 0.00    | USD      |
| DISC-10020 | ส่วนลดเงินสด    | วันที่ 1 กรกฎาคม 2015  |         | 3.00                                 |                                       | 0.00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>การชำระเงินที่เหลืออยู่ในวันที่ 15 มิถุนายน ใช้ส่วนลดเงินสด =ปกติ
April ชำระเงินส่วนที่เหลือของใบแจ้งหนี้ในวันที่ 15 กรกฎาคม ซึ่งเป็นวันหลังจากรอบระยะเวลาส่วนลด ในหน้า **ชำระธุรกรรมที่ค้างอยู่** ยอดส่วนลดจะไม่ปรากฏขึ้นในฟิลด์ **ส่วนลดเงินสดที่ประเมิน** และค่าในฟิลด์ **ยอดส่วนลดเงินสด** เป็น **0.00** เมื่อ April จ่ายเงินคงเหลือ 700.00 จะไม่นำส่วนลดเพิ่มเติมมาใช้

| ทำเครื่องหมาย     | ใช้ส่วนลดเงินสด | ใบสำคัญ   | บัญชี | วันที่      | วันที่ครบกำหนด  | ใบแจ้งหนี้ | ยอดเงินในสกุลเงินของธุรกรรม | สกุลเงิน | ยอดเงินที่จะชำระ |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| เลือกแล้ว | ปกติ            | Inv-10020 | 3057    | วันที่ 25 มิถุนายน 2015 | วันที่ 25 กรกฏาคม 2015 | 10020   | -700.00.                        | USD      | -700.00.          |

ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ธุรกรรมการชำระเงิน** April สามารถดูว่า เธอได้ใช้ส่วนลด 3.00 แล้ว

|                              |           |
|------------------------------|-----------|
| วันที่ให้ส่วนลดเงินสด           | วันที่ 9 กรกฎาคม 2015 |
| ยอดส่วนลดเงินสด         | 0.00      |
| ใช้ส่วนลดเงินสด            | ปกติ    |
| ส่วนลดเงินสดที่ใช้          | -3.00     |
| ยอดส่วนลดเงินสดที่จะใช้ | 0.00      |

หลังจากนั้น April ลงรายการบัญชีการชำระเงิน เมื่อเธอเปิดหน้า **ธุรกรรมผู้จัดจำหน่าย** เธอจะเห็นว่าใบแจ้งหนี้มียอดดุลเท่ากับ 0.00 เธอยังเห็นด้วยว่ามีการชำระเงินสองรายการ การชำระเงินหนึ่งรายการสำหรับ 297.00 และมีส่วนลด 3.00 และมีการชำระเงินอีกรายการสำหรับ 700.00

| ใบสำคัญ    | ชนิดธุรกรรม | วันที่      | ใบแจ้งหนี้ | ยอดเงินในเดบิตในสกุลเงินของธุรกรรม | ยอดเงินในเครดิตในสกุลเงินของธุรกรรม | ยอดดุล | สกุลเงิน |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | ใบแจ้งหนี้          | วันที่ 25 มิถุนายน 2015 | 10020   |                                      | 1,000.00                              | 0.00    | USD      |
| APP-10020  | การชำระเงิน          | วันที่ 1 กรกฎาคม 2015  |         | 297.00                               |                                       | 0.00    | USD      |
| DISC-10020 | ส่วนลดเงินสด    | วันที่ 1 กรกฎาคม 2015  |         | 3.00                                 |                                       | 0.00    | USD      |
| APP-10021  | การชำระเงิน          | วันที่ 15 กรกฎาคม 2015 |         | 700.00                               |                                       | 0.00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>การชำระเงินที่เหลืออยู่ในวันที่ 15 มิถุนายน ใช้ส่วนลดเงินสด =เสมอ
ถ้าผู้จัดจำหน่ายให้ April ใช้ส่วนลด ถึงแม้ว่าเธอจะชำระเงินหลังจากวันส่วนลด เธอสามารถเปลี่ยนค่าในฟิลด์  **ใช้ส่วนลดเงินสด** เป็น **เสมอ** การตั้งค่า **คำนวณส่วนลดเงินสดสำหรับการชำระเงินบางส่วน** จะถูกแทนที่ และส่วนลดจะถูกใช้ ยอดการชำระเงินคือ 693.00 และส่วนลดที่คงเหลือคือ 7.00

| ทำเครื่องหมาย     | ใช้ส่วนลดเงินสด | ใบสำคัญ   | บัญชี | วันที่      | วันที่ครบกำหนด  | ใบแจ้งหนี้ | ยอดเงินในเดบิตในสกุลเงินของธุรกรรม | ยอดเงินในเครดิตในสกุลเงินของธุรกรรม | สกุลเงิน | ยอดเงินที่จะชำระ |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| เลือกแล้ว | เสมอ            | Inv-10020 | 3057    | วันที่ 25 มิถุนายน 2015 | วันที่ 25 กรกฏาคม 2015 | 10020   | 700.00                               |                                       | USD      | -693.00          |

ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ธุรกรรมการชำระเงิน**

|                              |           |
|------------------------------|-----------|
| วันที่ให้ส่วนลดเงินสด           | วันที่ 9 กรกฎาคม 2015 |
| ยอดส่วนลดเงินสด         | 7.00 น.      |
| ใช้ส่วนลดเงินสด            | เสมอ    |
| ส่วนลดเงินสดที่ใช้          | -3.00     |
| ยอดส่วนลดเงินสดที่จะใช้ | -7.00     |

หลังจากนั้น April ลงรายการบัญชีการชำระเงิน เมื่อเธอเปิดหน้า **ธุรกรรมผู้จัดจำหน่าย** เธอจะเห็นว่าใบแจ้งหนี้มียอดดุลเท่ากับ 0.00 เธอยังเห็นด้วยว่ามีการชำระเงินสองรายการ การชำระเงินหนึ่งรายการสำหรับ 297.00 และมีส่วนลด 3.00 และมีการชำระเงินอีกรายการสำหรับ 693.00 และมีส่วนลด 7.00

| ใบสำคัญ    | ชนิดธุรกรรม | วันที่      | ใบแจ้งหนี้ | ยอดเงินในเดบิตในสกุลเงินของธุรกรรม | ยอดเงินในเครดิตในสกุลเงินของธุรกรรม | ยอดดุล | สกุลเงิน |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | ใบแจ้งหนี้          | วันที่ 25 มิถุนายน 2015 | 10020   |                                      | 1,000.00                              | 0.00    | USD      |
| APP-10020  | การชำระเงิน          | วันที่ 1 กรกฎาคม 2015  |         | 297.00                               |                                       | 0.00    | USD      |
| DISC-10020 | ส่วนลดเงินสด    | วันที่ 1 กรกฎาคม 2015  |         | 3.00                                 |                                       | 0.00    | USD      |
| APP-10021  | การชำระเงิน          | วันที่ 15 กรกฎาคม 2015 |         | 693.00                               |                                       | 0.00    | USD      |
| DISC-10021 | ส่วนลดเงินสด    | วันที่ 15 กรกฎาคม 2015 |         | 7.00 น.                                 |                                       | 0.00    | USD      |





