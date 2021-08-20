---
title: มีการลงรายการบัญชีรายการคงค้างของการซื้อที่มียอดเงินเป็นศูนย์ในใบรับสินค้ามูลค่าศูนย์
description: เมื่อลงรายการบัญชีใบรับสินค้าที่มีค่าเป็นศูนย์ ระบบจะสร้างการลงรายการบัญชีไปยังการรับรู้การซื้อโดยยอดเงินเป็น 0 (ศูนย์)
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 304609e065389d4f56913ae3f2f7fc562de2eadc9f0885ddbe2c8f4747081c66
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722186"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>มีการลงรายการบัญชีรายการคงค้างของการซื้อที่มียอดเงินเป็นศูนย์ในใบรับสินค้ามูลค่าศูนย์

หมายเลข KB: 4612588

## <a name="symptoms"></a>อาการ

เมื่อลงรายการบัญชีใบรับสินค้าที่มีค่าเป็นศูนย์ ระบบจะสร้างการลงรายการบัญชีไปยังการรับรู้การซื้อโดยยอดเงินเป็น 0 (ศูนย์)

## <a name="resolution"></a>ความละเอียด

โดยค่าเริ่มต้น สำหรับการลงรายการบัญชีแยกประเภทของชนิด *ซื้อ จริง* ฟิลด์ `IsTransferredIndetail` จะตั้งค่าเป็น *สรุป* ในธุรกรรมบัญชีแยกประเภทเสมอ ดังนั้น ระบบจึงสร้างรายการใบสำคัญที่เกี่ยวข้องแม้ว่าจํานวนเงินจะเป็น 0 (ศูนย์)

เมื่อต้องการข้ามชนิดการลงรายการบัญชีนี้เมื่อยอดเงินเป็น 0 (ศูนย์) ให้ขยายวิธีการ `subledgerJournalizer.markDoNotTransferEntries` เพื่อให้รวม `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` นั้นตามที่แสดงในตัวอย่างต่อไปนี้

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
