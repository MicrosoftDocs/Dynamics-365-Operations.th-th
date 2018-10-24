---
title: "การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี"
description: "หัวข้อนี้อธิบายวิธีการประเมินค่าสกุลเงินในบริษัทสำหรับการรวมบัญชี"
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.contentlocale: th-th
ms.lasthandoff: 10/02/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="34798-103">การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="34798-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34798-104">เมื่อคุณรวมข้อมูลจากสกุลเงินทางบัญชีหนึ่งไปอีกสกุลเงินทางบัญชีหนึ่ง คุณต้องรันการประเมินค่าสกุลเงินใหม่หากมีการเปลี่ยนแปลงอัตราแลกเปลี่ยน จากนั้นยอดดุลบัญชีของคุณถึงจะได้ประเมินค่าใหม่ได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="34798-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="34798-105">เมื่อคุณรวมข้อมูลไว้ในตอนแรก ใช้แท็บ **การแปลงสกุลเงิน** เพื่อเลือกอัตราแลกเปลี่ยนเริ่มต้นสำหรับการแปลงในระหว่างกระบวนการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="34798-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="34798-106">หลังจากป้อนอัตราแลกเปลี่ยนใหม่ (ตัวอย่างเช่น ในเดือนถัดไป) คุณต้องประเมินค่ายอดดุลบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="34798-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="34798-107">กำไรหรือขาดทุนที่ยังไม่รับรู้จะถูกอัพเดตไปตามนั้น ตามอัตราแลกเปลี่ยนและวันใหม่</span><span class="sxs-lookup"><span data-stu-id="34798-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="34798-108">ตัวอย่างต่อไปนี้แสดงให้เห็นรายการบัญชีที่สร้างขึ้นในระหว่างกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="34798-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="34798-109">การจัดเตรียมบริษัท</span><span class="sxs-lookup"><span data-stu-id="34798-109">Company setup</span></span>
-   <span data-ttu-id="34798-110">**แหล่งที่มา/บริษัทที่ดำเนินการ (USMF)** – ดอลลาร์สหรัฐฯ (USD) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="34798-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="34798-111">**บริษัทแบบรวมบัญชี(CON)** – ยูโร (EUR) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="34798-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="34798-112">**กำไรที่รับรู้**– บัญชีแยกประเภท 801500</span><span class="sxs-lookup"><span data-stu-id="34798-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="34798-113">**ขาดทุนที่รับรู้** – บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="34798-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="34798-114">**กำไรที่ยังไม่รับรู้**– บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="34798-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="34798-115">**ขาดทุนที่ยังไม่รับรู้**– บัญชีแยกประเภท 801400</span><span class="sxs-lookup"><span data-stu-id="34798-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="34798-116">ธุรกรรมดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="34798-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="34798-117">ธุรกรรมของใบเสร็จรับเงินใน USMF</span><span class="sxs-lookup"><span data-stu-id="34798-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="34798-118">วันที่</span><span class="sxs-lookup"><span data-stu-id="34798-118">Date</span></span>       | <span data-ttu-id="34798-119">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="34798-119">Ledger account</span></span>               | <span data-ttu-id="34798-120">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-120">Currency</span></span> | <span data-ttu-id="34798-121">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="34798-122">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="34798-122">10/11/2015</span></span> | <span data-ttu-id="34798-123">110110 - เงินสด</span><span class="sxs-lookup"><span data-stu-id="34798-123">110110 – Cash</span></span>                | <span data-ttu-id="34798-124">USD</span><span class="sxs-lookup"><span data-stu-id="34798-124">USD</span></span>      | <span data-ttu-id="34798-125">500</span><span class="sxs-lookup"><span data-stu-id="34798-125">500</span></span>    |
| <span data-ttu-id="34798-126">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="34798-126">10/11/2015</span></span> | <span data-ttu-id="34798-127">130100 – บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="34798-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="34798-128">USD</span><span class="sxs-lookup"><span data-stu-id="34798-128">USD</span></span>      | <span data-ttu-id="34798-129">-500</span><span class="sxs-lookup"><span data-stu-id="34798-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="34798-130">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="34798-130">Exchange rates</span></span>

| <span data-ttu-id="34798-131">สกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="34798-131">From currency</span></span> | <span data-ttu-id="34798-132">สกุลเงินสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="34798-132">To currency</span></span> | <span data-ttu-id="34798-133">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="34798-133">Start date</span></span> | <span data-ttu-id="34798-134">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="34798-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="34798-135">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-135">EUR</span></span>           | <span data-ttu-id="34798-136">USD</span><span class="sxs-lookup"><span data-stu-id="34798-136">USD</span></span>         | <span data-ttu-id="34798-137">วันที่ 1 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="34798-137">10/1/2015</span></span>  | <span data-ttu-id="34798-138">200</span><span class="sxs-lookup"><span data-stu-id="34798-138">200</span></span>           |
| <span data-ttu-id="34798-139">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-139">EUR</span></span>           | <span data-ttu-id="34798-140">USD</span><span class="sxs-lookup"><span data-stu-id="34798-140">USD</span></span>         | <span data-ttu-id="34798-141">วันที่ 1 พฤษจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="34798-141">11/1/2015</span></span>  | <span data-ttu-id="34798-142">150</span><span class="sxs-lookup"><span data-stu-id="34798-142">150</span></span>           |
| <span data-ttu-id="34798-143">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-143">EUR</span></span>           | <span data-ttu-id="34798-144">USD</span><span class="sxs-lookup"><span data-stu-id="34798-144">USD</span></span>         | <span data-ttu-id="34798-145">1 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="34798-145">12/1/2012</span></span>  | <span data-ttu-id="34798-146">100</span><span class="sxs-lookup"><span data-stu-id="34798-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="34798-147">ดำเนินการรวมบัญชีสำหรับเดือนตุลาคม 2015 </span><span class="sxs-lookup"><span data-stu-id="34798-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="34798-148">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="34798-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="34798-149">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="34798-149">Ledger account</span></span> | <span data-ttu-id="34798-150">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-150">Currency</span></span> | <span data-ttu-id="34798-151">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-151">Amount</span></span> | <span data-ttu-id="34798-152">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="34798-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="34798-153">110110</span><span class="sxs-lookup"><span data-stu-id="34798-153">110110</span></span>         | <span data-ttu-id="34798-154">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-154">EUR</span></span>      | <span data-ttu-id="34798-155">250</span><span class="sxs-lookup"><span data-stu-id="34798-155">250</span></span>    | <span data-ttu-id="34798-156">500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="34798-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="34798-157">130100</span><span class="sxs-lookup"><span data-stu-id="34798-157">130100</span></span>         | <span data-ttu-id="34798-158">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-158">EUR</span></span>      | <span data-ttu-id="34798-159">-250</span><span class="sxs-lookup"><span data-stu-id="34798-159">-250</span></span>   | <span data-ttu-id="34798-160">-500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="34798-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="34798-161">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 30 พฤศจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="34798-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="34798-162">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="34798-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="34798-163">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="34798-163">Ledger account</span></span> | <span data-ttu-id="34798-164">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-164">Currency</span></span> | <span data-ttu-id="34798-165">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-165">Amount</span></span>  | <span data-ttu-id="34798-166">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="34798-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="34798-167">110110</span><span class="sxs-lookup"><span data-stu-id="34798-167">110110</span></span>         | <span data-ttu-id="34798-168">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-168">EUR</span></span>      | <span data-ttu-id="34798-169">333.33</span><span class="sxs-lookup"><span data-stu-id="34798-169">333.33</span></span>  | <span data-ttu-id="34798-170">ยอดเงินเดิมของ 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="34798-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="34798-171">130100</span><span class="sxs-lookup"><span data-stu-id="34798-171">130100</span></span>         | <span data-ttu-id="34798-172">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-172">EUR</span></span>      | <span data-ttu-id="34798-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="34798-173">-333.33</span></span> | <span data-ttu-id="34798-174">ยอดเงินเดิมของ -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="34798-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="34798-175">801400</span><span class="sxs-lookup"><span data-stu-id="34798-175">801400</span></span>         | <span data-ttu-id="34798-176">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-176">EUR</span></span>      | <span data-ttu-id="34798-177">83.33</span><span class="sxs-lookup"><span data-stu-id="34798-177">83.33</span></span>   | <span data-ttu-id="34798-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="34798-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="34798-179">801600</span><span class="sxs-lookup"><span data-stu-id="34798-179">801600</span></span>         | <span data-ttu-id="34798-180">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-180">EUR</span></span>      | <span data-ttu-id="34798-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="34798-181">-83.33</span></span>  | <span data-ttu-id="34798-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="34798-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="34798-183">คุณจะเห็นธุรกรรมเพิ่มเติมสำหรับยอดสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="34798-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="34798-184">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 31 ธันวาคม 2015</span><span class="sxs-lookup"><span data-stu-id="34798-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="34798-185">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="34798-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="34798-186">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="34798-186">Ledger account</span></span> | <span data-ttu-id="34798-187">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-187">Currency</span></span> | <span data-ttu-id="34798-188">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="34798-188">Amount</span></span>  | <span data-ttu-id="34798-189">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="34798-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="34798-190">110110</span><span class="sxs-lookup"><span data-stu-id="34798-190">110110</span></span>         | <span data-ttu-id="34798-191">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-191">EUR</span></span>      | <span data-ttu-id="34798-192">500.00</span><span class="sxs-lookup"><span data-stu-id="34798-192">500.00</span></span>  | <span data-ttu-id="34798-193">ยอดเงินเดิมของ 500 × 1</span><span class="sxs-lookup"><span data-stu-id="34798-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="34798-194">130100</span><span class="sxs-lookup"><span data-stu-id="34798-194">130100</span></span>         | <span data-ttu-id="34798-195">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-195">EUR</span></span>      | <span data-ttu-id="34798-196">-500.00.</span><span class="sxs-lookup"><span data-stu-id="34798-196">-500.00</span></span> | <span data-ttu-id="34798-197">ยอดเงินเดิมของ -500 × 1</span><span class="sxs-lookup"><span data-stu-id="34798-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="34798-198">801400</span><span class="sxs-lookup"><span data-stu-id="34798-198">801400</span></span>         | <span data-ttu-id="34798-199">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-199">EUR</span></span>      | <span data-ttu-id="34798-200">250</span><span class="sxs-lookup"><span data-stu-id="34798-200">250</span></span>     | <span data-ttu-id="34798-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="34798-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="34798-202">801600</span><span class="sxs-lookup"><span data-stu-id="34798-202">801600</span></span>         | <span data-ttu-id="34798-203">EUR</span><span class="sxs-lookup"><span data-stu-id="34798-203">EUR</span></span>      | <span data-ttu-id="34798-204">-250</span><span class="sxs-lookup"><span data-stu-id="34798-204">-250</span></span>    | <span data-ttu-id="34798-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="34798-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






