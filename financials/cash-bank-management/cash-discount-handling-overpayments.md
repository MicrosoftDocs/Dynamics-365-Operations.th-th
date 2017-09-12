---
title: "การจัดการส่วนลดเงินสดสำหรับการชำระมากเกิน"
description: "บทความนี้อธิบายสถานการณ์ที่แสดงวิธีจัดการการชำระเงินเมื่อลูกค้ามีส่วนลดเงินสด แต่ยังเกินผลรวม"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 5604f806eed81c60dfcae7cb7b1a22bba25aa454
ms.contentlocale: th-th
ms.lasthandoff: 06/29/2017


---

# <a name="handling-cash-discounts-for-overpayments"></a><span data-ttu-id="c6a82-103">การจัดการส่วนลดเงินสดสำหรับการชำระมากเกิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-103">Handling cash discounts for overpayments</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c6a82-104">บทความนี้อธิบายสถานการณ์ที่แสดงวิธีจัดการการชำระเงินเมื่อลูกค้ามีส่วนลดเงินสด แต่ยังเกินผลรวม</span><span class="sxs-lookup"><span data-stu-id="c6a82-104">This article provides scenarios that show how a payment is handled when the customer takes a cash discount but also overpays.</span></span> 

<span data-ttu-id="c6a82-105">ใบแจ้งหนี้จะถือว่ามากเกินเมื่อยอดเงินชำระเงินเกินกว่ายอดเงินใบแจ้งหนี้ลบด้วยส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-105">An invoice is considered overpaid when the payment amount is more than the invoice amount minus the cash discount.</span></span> <span data-ttu-id="c6a82-106">เมื่อต้องการระบุวิธีจัดการผลต่างของส่วนลดเงินสดที่สามารถได้รับเมื่อมีชำระใบแจ้งหนี้ ใช้ฟิลด์ **การจัดการส่วนลดเงินสด** และ **ชำระมากเกินหรือน้อยเกิน** บนหน้า **พารามิเตอร์ลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="c6a82-106">To specify how an obtainable cash discount difference is handled when an invoice is overpaid, use the **Cash discount administration** and **Maximum overpayment or underpayment** fields on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="c6a82-107">ในตัวอย่างต่อไปนี้ ลูกค้าจ่ายเกินยอดเงินใบแจ้งหนี้เป็น 0.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-107">In the following example, the customer has overpaid the invoice by 0.50.</span></span>

| <span data-ttu-id="c6a82-108">ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-108">Invoice total</span></span> | <span data-ttu-id="c6a82-109">ส่วนลดเงินสดที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="c6a82-109">Cash discount available</span></span> | <span data-ttu-id="c6a82-110">ยอดเงินที่จะชำระ รวมส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-110">Amount to be paid, which includes the cash discount</span></span> | <span data-ttu-id="c6a82-111">ยอดเงินที่ลูกค้าชำระจริง</span><span class="sxs-lookup"><span data-stu-id="c6a82-111">Amount the customer actually pays</span></span> |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="c6a82-112">105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-112">105.00</span></span>        | <span data-ttu-id="c6a82-113">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-113">10.50</span></span>                   | <span data-ttu-id="c6a82-114">94.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-114">94.50</span></span>                                               | <span data-ttu-id="c6a82-115">95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-115">95.00</span></span>                             |

## <a name="cash-discount-administration--specific"></a><span data-ttu-id="c6a82-116">ตัวเลือกการจัดการส่วนลดเงินสด: เฉพาะทาง</span><span class="sxs-lookup"><span data-stu-id="c6a82-116">Cash discount administration = Specific</span></span>
<span data-ttu-id="c6a82-117">เมื่อ **เฉพาะ** ถูกเลือกไว้ในฟิลด์ **การจัดการส่วนลดเงินสด** ในหน้า **บัญชีสำหรับธุรกรรมอัตโนมัติ** ส่วนลดเงินสดทั้งหมดถูกนำมา</span><span class="sxs-lookup"><span data-stu-id="c6a82-117">When **Specific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the full cash discount is taken.</span></span> <span data-ttu-id="c6a82-118">ยอดเงินชำระมากเกินมีการลงรายการบัญชีผลต่างของส่วนลดเงินสด หรือยอดดุลในบัญชีของลูกค้าที่คงเหลือ</span><span class="sxs-lookup"><span data-stu-id="c6a82-118">The overpayment amount either is posted to a cash discount difference ledger account or remains a balance on the customer’s account.</span></span> <span data-ttu-id="c6a82-119">ลักษณะการทำงานขึ้นอยู่ว่ายอดเงินชำระมากเกินระหว่าง 0.00 และยอดเงินที่ป้อนไว้ในฟิลด์**ชำระมากเกินหรือน้อยเกิน** หรือยอดเงินชำระมากเกินจะเกินกว่า **ชำระมากเกินหรือน้อยเกิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-119">The behavior depends on whether the overpayment amount is between 0.00 and the amount that is entered in the **Maximum overpayment or underpayment** field, or whether the overpayment amount is more than the **Maximum overpayment or underpayment** amount.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="c6a82-120">สถานการณ์จำลอง 1</span><span class="sxs-lookup"><span data-stu-id="c6a82-120">Scenario 1</span></span>

<span data-ttu-id="c6a82-121">ในสถานการณ์นี้ ยอดการชำระเงินเกินอยู่ระหว่าง 0.00 ถึงจำนวนสูงสุดของชำระมากเกินหรือน้อยเกินไป</span><span class="sxs-lookup"><span data-stu-id="c6a82-121">In this scenario, the overpayment amount is between 0.00 and the maximum overpayment or underpayment.</span></span> <span data-ttu-id="c6a82-122">ใบแจ้งหนี้สำหรับ 105.00 ถูกป้อน และส่วนลดเงินสดจะมีอายุ ถ้าชำระใบแจ้งหนี้ภายในเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="c6a82-122">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="c6a82-123">ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-123">Invoice total</span></span> | <span data-ttu-id="c6a82-124">ส่วนลดเงินสดที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="c6a82-124">Cash discount available</span></span> | <span data-ttu-id="c6a82-125">ยอดเงินที่จะชำระ รวมส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-125">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="c6a82-126">105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-126">105.00</span></span>        | <span data-ttu-id="c6a82-127">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-127">10.50</span></span>                   | <span data-ttu-id="c6a82-128">94.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-128">94.50</span></span>                                               |

<span data-ttu-id="c6a82-129">ลูกค้าส่งการชำระเงินสำหรับ 95.00 ภายในรอบระยะเวลาส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-129">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="c6a82-130">การชำระเงินจะชำระสำหรับใบแจ้งหนี้เป็นจำนวนเงิน 105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-130">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="c6a82-131">หลังจากที่ชำระใบแจ้งหนี้และการชำระเงินถูกวาง ธุรกรรมต่อไปนี้จะสร้างขึ้นสำหรับลูกค้าในบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-131">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="c6a82-132">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c6a82-132">Transaction</span></span>   | <span data-ttu-id="c6a82-133">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-133">Amount</span></span> | <span data-ttu-id="c6a82-134">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="c6a82-134">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="c6a82-135">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-135">Invoice</span></span>       | <span data-ttu-id="c6a82-136">105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-136">105.00</span></span> | <span data-ttu-id="c6a82-137">0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-137">0.00</span></span>    |
| <span data-ttu-id="c6a82-138">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-138">Payment</span></span>       | <span data-ttu-id="c6a82-139">-95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-139">-95.00</span></span> | <span data-ttu-id="c6a82-140">0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-140">0.00</span></span>    |
| <span data-ttu-id="c6a82-141">ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-141">Cash discount</span></span> | <span data-ttu-id="c6a82-142">-10.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-142">-10.50</span></span> | <span data-ttu-id="c6a82-143">0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-143">0.00</span></span>    |

<span data-ttu-id="c6a82-144">รายการบัญชีต่อไปนี้จะถูกสร้างขึ้นสำหรับการชำระเงินและการจัดการหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-144">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="c6a82-145">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-145">**Payment**</span></span>

| <span data-ttu-id="c6a82-146">บัญชี</span><span class="sxs-lookup"><span data-stu-id="c6a82-146">Account</span></span>             | <span data-ttu-id="c6a82-147">ยอดเงินเดบิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-147">Debit amount</span></span> | <span data-ttu-id="c6a82-148">ยอดเงินเครดิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-148">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="c6a82-149">เงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-149">Cash</span></span>                | <span data-ttu-id="c6a82-150">95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-150">95.00</span></span>        |               |
| <span data-ttu-id="c6a82-151">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-151">Accounts receivable</span></span> |              | <span data-ttu-id="c6a82-152">95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-152">95.00</span></span>         |

<span data-ttu-id="c6a82-153">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-153">**Settlement**</span></span>

| <span data-ttu-id="c6a82-154">บัญชี</span><span class="sxs-lookup"><span data-stu-id="c6a82-154">Account</span></span>                                                                                                          | <span data-ttu-id="c6a82-155">ยอดเงินเดบิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-155">Debit amount</span></span> | <span data-ttu-id="c6a82-156">ยอดเงินเครดิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-156">Credit amount</span></span> |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="c6a82-157">ส่วนลดเงินสด (ฟิลด์ **บัญชีหลักสำหรับส่วนลดของลูกค้า** ในหน้า **ส่วนลดเงินสด** )</span><span class="sxs-lookup"><span data-stu-id="c6a82-157">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span>                 | <span data-ttu-id="c6a82-158">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-158">10.50</span></span>        |               |
| <span data-ttu-id="c6a82-159">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-159">Accounts receivable</span></span>                                                                                              |              | <span data-ttu-id="c6a82-160">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-160">10.50</span></span>         |
| <span data-ttu-id="c6a82-161">ส่วนลดเงินสดของลูกค้า (ฟิลด์ **ส่วนลดเงินสดของลูกค้า** ในหน้า **บัญชีสำหรับธุรกรรมอัตโนมัติ** )</span><span class="sxs-lookup"><span data-stu-id="c6a82-161">Customer cash discount (the **Customer cash discount** field on the **Account for automatic transactions** page)</span></span> |              | <span data-ttu-id="c6a82-162">0.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-162">0.50</span></span>          |
| <span data-ttu-id="c6a82-163">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-163">Accounts receivable</span></span>                                                                                              | <span data-ttu-id="c6a82-164">0.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-164">0.50</span></span>         |               |

### <a name="scenario-2"></a><span data-ttu-id="c6a82-165">สถานการณ์จำลอง 2</span><span class="sxs-lookup"><span data-stu-id="c6a82-165">Scenario 2</span></span>

<span data-ttu-id="c6a82-166">ในสถานการณ์นี้ ยอดการชำระเงินเกินเกินจำนวนสูงสุดของชำระมากเกินหรือน้อยเกินไป</span><span class="sxs-lookup"><span data-stu-id="c6a82-166">In this scenario, the overpayment amount exceeds the maximum overpayment or underpayment amount.</span></span> <span data-ttu-id="c6a82-167">ใบแจ้งหนี้สำหรับ 105.00 ถูกป้อน และส่วนลดเงินสดจะมีอายุ ถ้าชำระใบแจ้งหนี้ภายในเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="c6a82-167">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="c6a82-168">ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-168">Invoice total</span></span> | <span data-ttu-id="c6a82-169">ส่วนลดเงินสดที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="c6a82-169">Cash discount available</span></span> | <span data-ttu-id="c6a82-170">ยอดเงินที่จะชำระ รวมส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-170">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="c6a82-171">105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-171">105.00</span></span>        | <span data-ttu-id="c6a82-172">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-172">10.50</span></span>                   | <span data-ttu-id="c6a82-173">94.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-173">94.50</span></span>                                               |

<span data-ttu-id="c6a82-174">ลูกค้าส่งการชำระเงินสำหรับ 95.00 ภายในรอบระยะเวลาส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-174">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="c6a82-175">การชำระเงินจะชำระสำหรับใบแจ้งหนี้เป็นจำนวนเงิน 105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-175">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="c6a82-176">หลังจากที่ชำระใบแจ้งหนี้และการชำระเงินถูกวาง ธุรกรรมต่อไปนี้จะสร้างขึ้นสำหรับลูกค้าในบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-176">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="c6a82-177">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c6a82-177">Transaction</span></span>   | <span data-ttu-id="c6a82-178">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-178">Amount</span></span> | <span data-ttu-id="c6a82-179">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="c6a82-179">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="c6a82-180">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-180">Invoice</span></span>       | <span data-ttu-id="c6a82-181">105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-181">105.00</span></span> | <span data-ttu-id="c6a82-182">0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-182">0.00</span></span>    |
| <span data-ttu-id="c6a82-183">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-183">Payment</span></span>       | <span data-ttu-id="c6a82-184">-95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-184">-95.00</span></span> | <span data-ttu-id="c6a82-185">-0.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-185">-0.50</span></span>   |
| <span data-ttu-id="c6a82-186">ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-186">Cash discount</span></span> | <span data-ttu-id="c6a82-187">-10.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-187">-10.50</span></span> | <span data-ttu-id="c6a82-188">0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-188">0.00</span></span>    |

<span data-ttu-id="c6a82-189">ยอดเงินชำระมากเกิน 0.50 จะยังคงเป็นยอดดุลเปิดในการชำระเงิน และสามารถจับคู่กับใบแจ้งหนี้อื่น</span><span class="sxs-lookup"><span data-stu-id="c6a82-189">The overpayment amount of 0.50 will remain as an open balance on the payment and can be settled against another invoice.</span></span> <span data-ttu-id="c6a82-190">รายการบัญชีต่อไปนี้จะถูกสร้างขึ้นสำหรับการชำระเงินและการจัดการหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-190">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="c6a82-191">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-191">**Payment**</span></span>

| <span data-ttu-id="c6a82-192">บัญชี</span><span class="sxs-lookup"><span data-stu-id="c6a82-192">Account</span></span>             | <span data-ttu-id="c6a82-193">ยอดเงินเดบิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-193">Debit amount</span></span> | <span data-ttu-id="c6a82-194">ยอดเงินเครดิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-194">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="c6a82-195">เงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-195">Cash</span></span>                | <span data-ttu-id="c6a82-196">95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-196">95.00</span></span>        |               |
| <span data-ttu-id="c6a82-197">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-197">Accounts receivable</span></span> |              | <span data-ttu-id="c6a82-198">95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-198">95.00</span></span>         |

<span data-ttu-id="c6a82-199">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-199">**Settlement**</span></span>

| <span data-ttu-id="c6a82-200">บัญชี</span><span class="sxs-lookup"><span data-stu-id="c6a82-200">Account</span></span>                                                                                          | <span data-ttu-id="c6a82-201">ยอดเงินเดบิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-201">Debit amount</span></span> | <span data-ttu-id="c6a82-202">ยอดเงินเครดิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-202">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="c6a82-203">ส่วนลดเงินสด (ฟิลด์ **บัญชีหลักสำหรับส่วนลดของลูกค้า** ในหน้า**ส่วนลดเงินสด** )</span><span class="sxs-lookup"><span data-stu-id="c6a82-203">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="c6a82-204">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-204">10.50</span></span>        |               |
| <span data-ttu-id="c6a82-205">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-205">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="c6a82-206">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-206">10.50</span></span>         |

## <a name="cash-discount-administration--unspecific"></a><span data-ttu-id="c6a82-207">ตัวเลือกการจัดการส่วนลดเงินสด: เฉพาะทาง</span><span class="sxs-lookup"><span data-stu-id="c6a82-207">Cash discount administration = Unspecific</span></span>
<span data-ttu-id="c6a82-208">เมื่อ **ไม่เฉพาะทาง** ถูกเลือกไว้ในฟิลด์ **การจัดการส่วนลดเงินสด** ในหน้า **บัญชีสำหรับธุรกรรมอัตโนมัติ** ส่วนลดเงินสดทั้งหมดถูกลดด้วยจำนวนการชำระเกิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-208">When **Unspecific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the cash discount amount is reduced by the overpayment amount.</span></span> <span data-ttu-id="c6a82-209">ลักษณะการทำงานนี้จะถูกใช้ ไม่ว่าจะยอดเงินชำระมากเกิน หรือต่ำ กว่าปริมาณที่ป้อนไว้ในฟิลด์ **การชำระมากเกินหรือน้อยเกิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-209">This behavior always applies, regardless of whether the overpayment amount is over or under the amount that is entered in the **Maximum overpayment or underpayment** field.</span></span>

### <a name="scenario-3"></a><span data-ttu-id="c6a82-210">สถานการณ์จำลอง 3</span><span class="sxs-lookup"><span data-stu-id="c6a82-210">Scenario 3</span></span>

<span data-ttu-id="c6a82-211">ในการจำลองนี้: ใบแจ้งหนี้สำหรับ 105.00 ถูกป้อน และส่วนลดเงินสดจะมีอายุ ถ้าชำระใบแจ้งหนี้ภายในเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="c6a82-211">In this scenario, an invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="c6a82-212">ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-212">Invoice total</span></span> | <span data-ttu-id="c6a82-213">ส่วนลดเงินสดที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="c6a82-213">Cash discount available</span></span> | <span data-ttu-id="c6a82-214">ยอดเงินที่จะชำระ รวมส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-214">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="c6a82-215">105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-215">105.00</span></span>        | <span data-ttu-id="c6a82-216">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-216">10.50</span></span>                   | <span data-ttu-id="c6a82-217">94.50</span><span class="sxs-lookup"><span data-stu-id="c6a82-217">94.50</span></span>                                               |

<span data-ttu-id="c6a82-218">ลูกค้าส่งการชำระเงินสำหรับ 95.00 ภายในวันที่รอบระยะเวลาส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-218">The customer submits a payment for 95.00 within the cash discount date.</span></span> <span data-ttu-id="c6a82-219">การชำระเงินจะชำระสำหรับใบแจ้งหนี้เป็นจำนวนเงิน 105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-219">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="c6a82-220">หลังจากที่ชำระใบแจ้งหนี้และการชำระเงินถูกวาง ธุรกรรมต่อไปนี้จะสร้างขึ้นสำหรับลูกค้าในบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-220">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="c6a82-221">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c6a82-221">Transaction</span></span>   | <span data-ttu-id="c6a82-222">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-222">Amount</span></span> | <span data-ttu-id="c6a82-223">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="c6a82-223">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="c6a82-224">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-224">Invoice</span></span>       | <span data-ttu-id="c6a82-225">105.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-225">105.00</span></span> | <span data-ttu-id="c6a82-226">0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-226">0.00</span></span>    |
| <span data-ttu-id="c6a82-227">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6a82-227">Payment</span></span>       | <span data-ttu-id="c6a82-228">-95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-228">-95.00</span></span> | <span data-ttu-id="c6a82-229">-0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-229">-0.00</span></span>   |
| <span data-ttu-id="c6a82-230">ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-230">Cash discount</span></span> | <span data-ttu-id="c6a82-231">-10.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-231">-10.00</span></span> | <span data-ttu-id="c6a82-232">0.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-232">0.00</span></span>    |

<span data-ttu-id="c6a82-233">ยอดส่วนลดเงินสดจะลดลงจาก 10.50 เป็น 10.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-233">The cash discount amount is reduced from 10.50 to 10.00.</span></span> <span data-ttu-id="c6a82-234">การชำระเงินและใบแจ้งหนี้จะถือว่าเป็นชำระ</span><span class="sxs-lookup"><span data-stu-id="c6a82-234">The payment and invoice are considered settled.</span></span> <span data-ttu-id="c6a82-235">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-235">**Payment**</span></span>

| <span data-ttu-id="c6a82-236">บัญชี</span><span class="sxs-lookup"><span data-stu-id="c6a82-236">Account</span></span>             | <span data-ttu-id="c6a82-237">ยอดเงินเดบิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-237">Debit amount</span></span> | <span data-ttu-id="c6a82-238">ยอดเงินเครดิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-238">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="c6a82-239">เงินสด</span><span class="sxs-lookup"><span data-stu-id="c6a82-239">Cash</span></span>                | <span data-ttu-id="c6a82-240">95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-240">95.00</span></span>        |               |
| <span data-ttu-id="c6a82-241">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-241">Accounts receivable</span></span> |              | <span data-ttu-id="c6a82-242">95.00</span><span class="sxs-lookup"><span data-stu-id="c6a82-242">95.00</span></span>         |

<span data-ttu-id="c6a82-243">**การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="c6a82-243">**Settlement**</span></span>

| <span data-ttu-id="c6a82-244">บัญชี</span><span class="sxs-lookup"><span data-stu-id="c6a82-244">Account</span></span>                                                                                          | <span data-ttu-id="c6a82-245">ยอดเงินเดบิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-245">Debit amount</span></span> | <span data-ttu-id="c6a82-246">ยอดเงินเครดิต</span><span class="sxs-lookup"><span data-stu-id="c6a82-246">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="c6a82-247">ส่วนลดเงินสด (ฟิลด์ **บัญชีหลักสำหรับส่วนลดของลูกค้า** ในหน้า **ส่วนลดเงินสด** )</span><span class="sxs-lookup"><span data-stu-id="c6a82-247">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="c6a82-248">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-248">10.50</span></span>        |               |
| <span data-ttu-id="c6a82-249">บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="c6a82-249">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="c6a82-250">1050</span><span class="sxs-lookup"><span data-stu-id="c6a82-250">10.50</span></span>         |






