---
title: การชำระเงินของผู้จัดจำหน่ายสำหรับยอดเงินเป็นบางส่วน
description: บางครั้ง คุณอาจทำการชำระเงินให้ผู้จัดจำหน่ายน้อยกว่ายอดเงินของใบแจ้งหนี้ บทความนี้อธิบายถึงตัวเลือกต่างๆ สำหรับการจัดการสถานการณ์นี้
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617aa35cf1510e90c8c0b5dcfcff070d7db075b8
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/25/2019
ms.locfileid: "896614"
---
# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="878f0-104">การชำระเงินของผู้จัดจำหน่ายสำหรับยอดเงินบางส่วน</span><span class="sxs-lookup"><span data-stu-id="878f0-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="878f0-105">บางครั้ง คุณอาจทำการชำระเงินให้ผู้จัดจำหน่ายน้อยกว่ายอดเงินของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="878f0-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="878f0-106">บทความนี้อธิบายถึงตัวเลือกต่างๆ สำหรับการจัดการสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="878f0-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="878f0-107">ตัวเลือกที่พร้อมใช้งานสำหรับคุณขึ้นอยู่กับความต้องการทางธุรกิจของคุณและตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="878f0-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="878f0-108">ยอดส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="878f0-108">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="878f0-109">ผู้จัดจำหน่ายสามารถเสนอส่วนลดเงินสดสำหรับการชำระเงินตามใบแจ้งหนี้ก่อนวันครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="878f0-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="878f0-110">ตัวอย่างเช่น คุณป้อนใบแจ้งหนี้จำนวน 100.00 ที่ระบุส่วนลดเงินสด 2 เปอร์เซ็นต์หากชำระใบแจ้งหนี้ภายใน 10 วัน</span><span class="sxs-lookup"><span data-stu-id="878f0-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="878f0-111">เงื่อนไขวันครบกำหนดชำระคือ 30 วัน</span><span class="sxs-lookup"><span data-stu-id="878f0-111">The due date terms are 30 days.</span></span> <span data-ttu-id="878f0-112">ถ้าข้อเสนอการชำระเงินใช้ส่วนลดเงินสดเป็นหลักเกณฑ์สำหรับการเลือกใบแจ้งหนี้ และถ้าข้อเสนอเกิดขึ้นภายในหรือ ก่อนวันส่วนลดเงินสด ใบแจ้งหนี้จะถูกเลือกสำหรับการชำระเงิน และมีสร้างการชำระเงินเป็นจำนวน 98.00</span><span class="sxs-lookup"><span data-stu-id="878f0-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="878f0-113">นอกจากนี้ ยังสามารถมอบส่วนลดเงินสดสำหรับการชำระเงินชนิดเกิดขึ้นครั้งเดียวที่ถูกสร้างขึ้นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="878f0-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="878f0-114">คำนวณส่วนลดเงินสดสำหรับการชำระเงินบางส่วน</span><span class="sxs-lookup"><span data-stu-id="878f0-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="878f0-115">เมื่อคุณทำการชำระเงินบางส่วน คุณอาจจะวางแผนเพื่อทำการชำระเงินบางส่วนเพิ่มเติมเพื่อชำระใบแจ้งหนี้เต็มจำนวน</span><span class="sxs-lookup"><span data-stu-id="878f0-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="878f0-116">เมื่อต้องการส่วนลดเงินสดสำหรับการชำระเงินบางส่วน จะต้องเลือก **คำนวณส่วนลดเงินสดสำหรับการชำระเงินบางส่วน** ให้เป็น **ใช่** บนหน้า **บัญชีพารามิเตอร์เจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="878f0-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="878f0-117">ตัวอย่างเช่น คุณได้รับส่วนลดเงินสด 2 เปอร์เซ็นต์ถ้าชำระเงินภายใน 10 วันหลังจากวันออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="878f0-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="878f0-118">มีการลงรายการบัญชีใบแจ้งหนี้จำนวน 100.00</span><span class="sxs-lookup"><span data-stu-id="878f0-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="878f0-119">ถ้าคุณทำการชำระเงิน 49.00 ภายใน 10 วัน คุณป้อนรายการชำระเงิน 49.00</span><span class="sxs-lookup"><span data-stu-id="878f0-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="878f0-120">เมื่อคุณตั้งการชำระเงินบางส่วนบนหน้า **ชำระธุรกรรมที่ค้างอยู่** **1.00** ปรากฏในฟิลด์ **ยอดส่วนลดเงินสดที่จะใช้**</span><span class="sxs-lookup"><span data-stu-id="878f0-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="878f0-121">หมายเหตุ: ถ้าคุณป้อนการชำระเงินบางส่วน และออกจากยอดเงินใบแจ้งหนี้เต็มจำนวนในฟิลด์ **ยอดเงินที่จะชำระ** ฟิลด์ **ยอดส่วนลดเงินสดที่จะใช้** จะถูกคำนวณโดยอัตโนมัติเมื่อคุณลงรายบัญชีธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="878f0-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="878f0-122">ใบลดหนี้ที่มีส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="878f0-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="878f0-123">คุณอาจส่งคืนสินค้าบางรายการในใบแจ้งหนี้ และได้รับใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="878f0-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="878f0-124">ถ้าในใบแจ้งหนี้เดิมได้รับส่วนลดเงินสด คุณสามารถลบมูลค่าของส่วนลด และได้รับเงินคืนเป็นยอดเงินที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="878f0-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="878f0-125">ถ้าตัวเลือก **คำนวณส่วนลดเงินสดสำหรับใบลดหนี้** ตั้งค่าอยู่ที่ **ใช่** บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้** ส่วนลดสำหรับใบลดหนี้จะถูกคำนวณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="878f0-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="878f0-126">ตัวอย่างเช่น คุณได้รับส่วนลดเงินสด 2 เปอร์เซ็นต์ถ้าชำระเงินภายใน 10 วันหลังจากวันออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="878f0-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="878f0-127">มีการลงรายการบัญชีใบแจ้งหนี้จำนวน 100.00</span><span class="sxs-lookup"><span data-stu-id="878f0-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="878f0-128">ถ้าคุณส่งคืนสินค้าและได้รับใบลดหนี้ คุณสามารถป้อนใบลดหนี้สำหรับยอดเงินเต็มจำนวนในใบแจ้งหนี้เดิม 100.00 ร่วมกับส่วนลดเงินสด 2 เปอร์เซ็นต์ที่กำหนดบนใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="878f0-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="878f0-129">เมื่อคุณดูใบลดหนี้ในหน้า **ชำระธุรกรรม** ยอด **98.00** จะปรากฏขึ้นในฟิลด์ **ยอดเงินที่จะชำระ** และยอด **-2.00** จะปรากฏขึ้นในฟิลด์ **ส่วนลดเงินสด**</span><span class="sxs-lookup"><span data-stu-id="878f0-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="878f0-130">รายการบัญชียอดส่วนลดจะบันทึกลงในบัญชีส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="878f0-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="878f0-131">การชำระเงินมากเกินหรือน้อยเกิน</span><span class="sxs-lookup"><span data-stu-id="878f0-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="878f0-132">คุณอาจทำการชำระเงินบางส่วน โดยที่ยอดเงินคงเหลือที่ต้องชำระมีจำนวนน้อยมาก</span><span class="sxs-lookup"><span data-stu-id="878f0-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="878f0-133">ตัวอย่างเช่น ใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับ 1,000.00 และคุณจ่าย 999.90</span><span class="sxs-lookup"><span data-stu-id="878f0-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="878f0-134">หากยอดคงเหลือน้อยกว่ายอดเงินที่ระบุไว้สำหรับการชำระมากเกินหรือน้อยเกินในหน้า **พารามิเตอร์บัญชีเจ้าหนี้** ผลต่างจะลงรายการบัญชีไปยังบัญชีแยกประเภทการชำระมากเกิน/น้อยเกินโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="878f0-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="878f0-135">สำหรับข้อมูลเพิ่มเติม โปรดดู [ภาพรวมการชำระเงินของผู้จัดจำหน่าย](../cash-bank-management/tasks/vendor-payment-overview.md)</span><span class="sxs-lookup"><span data-stu-id="878f0-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>
