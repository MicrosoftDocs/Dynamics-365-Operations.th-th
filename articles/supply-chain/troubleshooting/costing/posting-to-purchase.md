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
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026965"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="beb40-103">มีการลงรายการบัญชีรายการคงค้างของการซื้อที่มียอดเงินเป็นศูนย์ในใบรับสินค้ามูลค่าศูนย์</span><span class="sxs-lookup"><span data-stu-id="beb40-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="beb40-104">หมายเลข KB: 4612588</span><span class="sxs-lookup"><span data-stu-id="beb40-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="beb40-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="beb40-105">Symptoms</span></span>

<span data-ttu-id="beb40-106">เมื่อลงรายการบัญชีใบรับสินค้าที่มีค่าเป็นศูนย์ ระบบจะสร้างการลงรายการบัญชีไปยังการรับรู้การซื้อโดยยอดเงินเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="beb40-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="beb40-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="beb40-107">Resolution</span></span>

<span data-ttu-id="beb40-108">โดยค่าเริ่มต้น สำหรับการลงรายการบัญชีแยกประเภทของชนิด *ซื้อ จริง* ฟิลด์ `IsTransferredIndetail` จะตั้งค่าเป็น *สรุป* ในธุรกรรมบัญชีแยกประเภทเสมอ</span><span class="sxs-lookup"><span data-stu-id="beb40-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="beb40-109">ดังนั้น ระบบจึงสร้างรายการใบสำคัญที่เกี่ยวข้องแม้ว่าจํานวนเงินจะเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="beb40-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="beb40-110">เมื่อต้องการข้ามชนิดการลงรายการบัญชีนี้เมื่อยอดเงินเป็น 0 (ศูนย์) ให้ขยายวิธีการ `subledgerJournalizer.markDoNotTransferEntries` เพื่อให้รวม `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` นั้นตามที่แสดงในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="beb40-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
