---
title: การชำระเงินบางส่วนของผู้ซิ้อที่มีส่วนลดในใบลดหนี้
description: บทความนี้แนะนำคุณผ่านสถานการณ์ที่ส่วนลดเงินสดจะใช้ใบลดหนี้เมื่อใบแจ้งหนี้เดิมยังมีส่วนลดเงินสด
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f64b9b9cd4fa65d17ba30fb87a688411becd5a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780554"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>การชำระเงินบางส่วนของผู้ซิ้อที่มีส่วนลดในใบลดหนี้

[!include [banner](../includes/banner.md)]

บทความนี้แนะนำคุณผ่านสถานการณ์ที่ส่วนลดเงินสดจะใช้ใบลดหนี้เมื่อใบแจ้งหนี้เดิมยังมีส่วนลดเงินสด 

Fabrikam อนุญาตให้ลูกค้านำส่วนลดเงินสด ในการชำระเงินบางส่วน และ บนใบลดหนี้ (บันทึกเครดิต) ส่วนลดเงินสดสามารถทำได้ในใบลดหนี้เมื่อมีออกใบลดหนี้สำหรับใบแจ้งหนี้ที่ลูกค้าได้ส่วนลดเงินสด แทนที่จะให้เครดิตสำหรับยอดเงินเต็มจำนวน คุณสามารถเครดิตยอดดุลของลูกค้าสำหรับยอดเงินที่ไม่รวมเปอร์เซ็นต์ส่วนลดเงินสดที่ลูกค้าใช้ พารามิเตอร์การชำระเงินอยู่ในหน้า **พารามิเตอร์บัญชีลูกหนี้**

## <a name="invoice-and-credit-note"></a>ใบแจ้งหนี้และใบลดหนี้
ลูกค้า 4035 มีใบแจ้งหนี้สำหรับยอด 1, 000.00 และใบลดหนี้ยอด 100.00 เอกสารแต่ละฉบับมีส่วนลด 1 เปอร์เซ็นต์ ถ้ามีการชำระเงินภายใน 14 วัน Arnie สามารถดูข้อมูลนี้ในหน้า **ธุรกรรมลูกค้า**

| ใบสำคัญ    | ชนิดธุรกรรม | วันที่      | ใบแจ้งหนี้  | ยอดเงินในเดบิตในสกุลเงินของธุรกรรม | ยอดเงินในเครดิตในสกุลเงินของธุรกรรม | ยอดดุล  | สกุลเงิน |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | ใบแจ้งหนี้          | วันที่ 6/28/2020 | 10050    | 1,000.00                             |                                       | 1,000.00 | USD      |
| CCRN-10050 | ใบลดหนี้      | วันที่ 6/28/2020 | CR-10050 |                                      | 100.00                                | -100.00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>จับคู่ใบลดหนี้กับใบแจ้งหนี้
จากหน้า **ธุรกรรมลูกค้า** Arnie เปิด **ธุรกรรมการชำระเงิน** Arnie สามารถใช้หน้า **ธุรกรรมการชำระเงิน** เพื่อชำระใบแจ้งหนี้และใบลดหนี้ได้ เป็นส่วนหนึ่งของกระบวนการชำระเงิน Arnie ดูวันที่และยอดเงินของส่วนลดเงินสด Arnie ทำเครื่องหมายในเอกสารสองแล้ว คลิกที่ **ลงรายการบัญชี** ไปที่ชำระธุรกรรม มีส่วนลด-1.00 ในใบลดหนี้ เนื่องจาก Fabrikam อนุญาตให้มีส่วนลดบนใบลดหนี้

| ทำเครื่องหมาย     | ใช้ส่วนลดเงินสด | ใบสำคัญ    | บัญชี | วันที่      | วันที่ครบกำหนด  | ใบแจ้งหนี้  | ยอดเงินในสกุลเงินของธุรกรรม | สกุลเงิน | ยอดเงินที่จะชำระ |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| เลือกแล้ว | ปกติ            | FTI-10050  | 4035    | วันที่ 6/28/2020 | วันที่ 7/28/2020 | 10050    | 1,000.00                       | USD      | 990.00           |
| เลือกแล้ว | ปกติ            | CCRN-10050 | 4035    | วันที่ 6/28/2020 | วันที่ 7/28/2020 | CR-10050 | -100.00                        | USD      | -99.00           |

ข้อมูลส่วนลดที่ปรากฏขึ้นที่ด้านล่างของหน้า **ธุรกรรมการชำระเงิน**

- **วันที่ให้ส่วนลดเงินสด**: 7/12/2020 
- **ยอดส่วนลดเงินสด**: -1.00     
- **ใช้ส่วนลดเงินสด**: ปกติ    
- **ส่วนลดเงินสดที่ใช้**: 0.00      
- **ยอดส่วนลดเงินสดที่ใช้**: -1.00     

การชำระเงินจะเป็น 100.00 และจะรวมการชำระเงินของ 99.00 และส่วนลด 1.00





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
