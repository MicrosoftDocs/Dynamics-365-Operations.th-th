---
title: "การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: th-th
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="507c8-102">การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="507c8-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="507c8-103">เมื่อคุณรวมข้อมูลจากสกุลเงินทางบัญชีหนึ่งไปอีกสกุลเงินทางบัญชีหนึ่ง คุณต้องรันการประเมินค่าสกุลเงินใหม่หากมีการเปลี่ยนแปลงอัตราแลกเปลี่ยน จากนั้นยอดดุลบัญชีของคุณถึงจะได้ประเมินค่าใหม่ได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="507c8-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="507c8-104">เมื่อคุณรวมข้อมูลไว้ในตอนแรก ใช้แท็บ **การแปลงสกุลเงิน** เพื่อเลือกอัตราแลกเปลี่ยนเริ่มต้นสำหรับการแปลงในระหว่างกระบวนการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="507c8-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="507c8-105">หลังจากป้อนอัตราแลกเปลี่ยนใหม่ (ตัวอย่างเช่น ในเดือนถัดไป) คุณต้องประเมินค่ายอดดุลบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="507c8-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="507c8-106">กำไรหรือขาดทุนที่ยังไม่รับรู้จะถูกอัพเดตไปตามนั้น ตามอัตราแลกเปลี่ยนและวันใหม่</span><span class="sxs-lookup"><span data-stu-id="507c8-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="507c8-107">ตัวอย่างต่อไปนี้แสดงให้เห็นรายการบัญชีที่สร้างขึ้นในระหว่างกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="507c8-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="507c8-108">การจัดเตรียมบริษัท</span><span class="sxs-lookup"><span data-stu-id="507c8-108">Company setup</span></span>
-   <span data-ttu-id="507c8-109">**แหล่งที่มา/บริษัทที่ดำเนินการ (USMF)** – ดอลลาร์สหรัฐฯ (USD) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="507c8-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="507c8-110">**บริษัทแบบรวมบัญชี(CON)** – ยูโร (EUR) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="507c8-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="507c8-111">**กำไรที่รับรู้ **– บัญชีแยกประเภท 801500</span><span class="sxs-lookup"><span data-stu-id="507c8-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="507c8-112">**ขาดทุนที่รับรู้** – บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="507c8-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="507c8-113">**กำไรที่ยังไม่รับรู้**– บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="507c8-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="507c8-114">**ขาดทุนที่ยังไม่รับรู้**– บัญชีแยกประเภท 801400</span><span class="sxs-lookup"><span data-stu-id="507c8-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="507c8-115">ธุรกรรมดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="507c8-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="507c8-116">ธุรกรรมของใบเสร็จรับเงินใน USMF</span><span class="sxs-lookup"><span data-stu-id="507c8-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="507c8-117">วันที่</span><span class="sxs-lookup"><span data-stu-id="507c8-117">Date</span></span>       | <span data-ttu-id="507c8-118">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="507c8-118">Ledger account</span></span>               | <span data-ttu-id="507c8-119">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-119">Currency</span></span> | <span data-ttu-id="507c8-120">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="507c8-121">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="507c8-121">10/11/2015</span></span> | <span data-ttu-id="507c8-122">110110 - เงินสด</span><span class="sxs-lookup"><span data-stu-id="507c8-122">110110 – Cash</span></span>                | <span data-ttu-id="507c8-123">USD</span><span class="sxs-lookup"><span data-stu-id="507c8-123">USD</span></span>      | <span data-ttu-id="507c8-124">500</span><span class="sxs-lookup"><span data-stu-id="507c8-124">500</span></span>    |
| <span data-ttu-id="507c8-125">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="507c8-125">10/11/2015</span></span> | <span data-ttu-id="507c8-126">130100 – บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="507c8-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="507c8-127">USD</span><span class="sxs-lookup"><span data-stu-id="507c8-127">USD</span></span>      | <span data-ttu-id="507c8-128">-500</span><span class="sxs-lookup"><span data-stu-id="507c8-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="507c8-129">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="507c8-129">Exchange rates</span></span>
| <span data-ttu-id="507c8-130">สกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="507c8-130">From currency</span></span> | <span data-ttu-id="507c8-131">สกุลเงินสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="507c8-131">To currency</span></span> | <span data-ttu-id="507c8-132">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="507c8-132">Start date</span></span> | <span data-ttu-id="507c8-133">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="507c8-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="507c8-134">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-134">EUR</span></span>           | <span data-ttu-id="507c8-135">USD</span><span class="sxs-lookup"><span data-stu-id="507c8-135">USD</span></span>         | <span data-ttu-id="507c8-136">วันที่ 1 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="507c8-136">10/1/2015</span></span>  | <span data-ttu-id="507c8-137">200</span><span class="sxs-lookup"><span data-stu-id="507c8-137">200</span></span>           |
| <span data-ttu-id="507c8-138">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-138">EUR</span></span>           | <span data-ttu-id="507c8-139">USD</span><span class="sxs-lookup"><span data-stu-id="507c8-139">USD</span></span>         | <span data-ttu-id="507c8-140">วันที่ 1 พฤษจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="507c8-140">11/1/2015</span></span>  | <span data-ttu-id="507c8-141">150</span><span class="sxs-lookup"><span data-stu-id="507c8-141">150</span></span>           |
| <span data-ttu-id="507c8-142">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-142">EUR</span></span>           | <span data-ttu-id="507c8-143">USD</span><span class="sxs-lookup"><span data-stu-id="507c8-143">USD</span></span>         | <span data-ttu-id="507c8-144">1 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="507c8-144">12/1/2012</span></span>  | <span data-ttu-id="507c8-145">100</span><span class="sxs-lookup"><span data-stu-id="507c8-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="507c8-146">ดำเนินการรวมบัญชีสำหรับเดือนตุลาคม 2015 </span><span class="sxs-lookup"><span data-stu-id="507c8-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="507c8-147">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="507c8-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="507c8-148">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="507c8-148">Ledger account</span></span> | <span data-ttu-id="507c8-149">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-149">Currency</span></span> | <span data-ttu-id="507c8-150">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-150">Amount</span></span> | <span data-ttu-id="507c8-151">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="507c8-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="507c8-152">110110</span><span class="sxs-lookup"><span data-stu-id="507c8-152">110110</span></span>         | <span data-ttu-id="507c8-153">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-153">EUR</span></span>      | <span data-ttu-id="507c8-154">250</span><span class="sxs-lookup"><span data-stu-id="507c8-154">250</span></span>    | <span data-ttu-id="507c8-155">500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="507c8-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="507c8-156">130100</span><span class="sxs-lookup"><span data-stu-id="507c8-156">130100</span></span>         | <span data-ttu-id="507c8-157">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-157">EUR</span></span>      | <span data-ttu-id="507c8-158">-250</span><span class="sxs-lookup"><span data-stu-id="507c8-158">-250</span></span>   | <span data-ttu-id="507c8-159">-500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="507c8-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="507c8-160">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 30 พฤศจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="507c8-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="507c8-161">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="507c8-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="507c8-162">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="507c8-162">Ledger account</span></span> | <span data-ttu-id="507c8-163">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-163">Currency</span></span> | <span data-ttu-id="507c8-164">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-164">Amount</span></span>  | <span data-ttu-id="507c8-165">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="507c8-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="507c8-166">110110</span><span class="sxs-lookup"><span data-stu-id="507c8-166">110110</span></span>         | <span data-ttu-id="507c8-167">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-167">EUR</span></span>      | <span data-ttu-id="507c8-168">333.33</span><span class="sxs-lookup"><span data-stu-id="507c8-168">333.33</span></span>  | <span data-ttu-id="507c8-169">ยอดเงินเดิมของ 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="507c8-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="507c8-170">130100</span><span class="sxs-lookup"><span data-stu-id="507c8-170">130100</span></span>         | <span data-ttu-id="507c8-171">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-171">EUR</span></span>      | <span data-ttu-id="507c8-172">-333.33</span><span class="sxs-lookup"><span data-stu-id="507c8-172">-333.33</span></span> | <span data-ttu-id="507c8-173">ยอดเงินเดิมของ -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="507c8-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="507c8-174">801400</span><span class="sxs-lookup"><span data-stu-id="507c8-174">801400</span></span>         | <span data-ttu-id="507c8-175">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-175">EUR</span></span>      | <span data-ttu-id="507c8-176">83.33</span><span class="sxs-lookup"><span data-stu-id="507c8-176">83.33</span></span>   | <span data-ttu-id="507c8-177">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="507c8-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="507c8-178">801600</span><span class="sxs-lookup"><span data-stu-id="507c8-178">801600</span></span>         | <span data-ttu-id="507c8-179">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-179">EUR</span></span>      | <span data-ttu-id="507c8-180">-83.33</span><span class="sxs-lookup"><span data-stu-id="507c8-180">-83.33</span></span>  | <span data-ttu-id="507c8-181">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="507c8-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="507c8-182">คุณจะเห็นธุรกรรมเพิ่มเติมสำหรับยอดสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="507c8-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="507c8-183">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 31 ธันวาคม 2015</span><span class="sxs-lookup"><span data-stu-id="507c8-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="507c8-184">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="507c8-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="507c8-185">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="507c8-185">Ledger account</span></span> | <span data-ttu-id="507c8-186">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-186">Currency</span></span> | <span data-ttu-id="507c8-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="507c8-187">Amount</span></span>  | <span data-ttu-id="507c8-188">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="507c8-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="507c8-189">110110</span><span class="sxs-lookup"><span data-stu-id="507c8-189">110110</span></span>         | <span data-ttu-id="507c8-190">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-190">EUR</span></span>      | <span data-ttu-id="507c8-191">500.00</span><span class="sxs-lookup"><span data-stu-id="507c8-191">500.00</span></span>  | <span data-ttu-id="507c8-192">ยอดเงินเดิมของ 500 × 1</span><span class="sxs-lookup"><span data-stu-id="507c8-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="507c8-193">130100</span><span class="sxs-lookup"><span data-stu-id="507c8-193">130100</span></span>         | <span data-ttu-id="507c8-194">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-194">EUR</span></span>      | <span data-ttu-id="507c8-195">-500.00.</span><span class="sxs-lookup"><span data-stu-id="507c8-195">-500.00</span></span> | <span data-ttu-id="507c8-196">ยอดเงินเดิมของ -500 × 1</span><span class="sxs-lookup"><span data-stu-id="507c8-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="507c8-197">801400</span><span class="sxs-lookup"><span data-stu-id="507c8-197">801400</span></span>         | <span data-ttu-id="507c8-198">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-198">EUR</span></span>      | <span data-ttu-id="507c8-199">250</span><span class="sxs-lookup"><span data-stu-id="507c8-199">250</span></span>     | <span data-ttu-id="507c8-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="507c8-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="507c8-201">801600</span><span class="sxs-lookup"><span data-stu-id="507c8-201">801600</span></span>         | <span data-ttu-id="507c8-202">EUR</span><span class="sxs-lookup"><span data-stu-id="507c8-202">EUR</span></span>      | <span data-ttu-id="507c8-203">-250</span><span class="sxs-lookup"><span data-stu-id="507c8-203">-250</span></span>    | <span data-ttu-id="507c8-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="507c8-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






