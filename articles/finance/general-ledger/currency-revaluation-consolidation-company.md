---
title: การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี
description: หัวข้อนี้อธิบายวิธีการประเมินค่าสกุลเงินในบริษัทสำหรับการรวมบัญชี
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014994"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="8da13-103">การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="8da13-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8da13-104">เมื่อคุณรวมข้อมูลจากสกุลเงินทางบัญชีหนึ่งไปอีกสกุลเงินทางบัญชีหนึ่ง คุณต้องรันการประเมินค่าสกุลเงินใหม่หากมีการเปลี่ยนแปลงอัตราแลกเปลี่ยน จากนั้นยอดดุลบัญชีของคุณถึงจะได้ประเมินค่าใหม่ได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8da13-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="8da13-105">เมื่อคุณรวมข้อมูลไว้ในตอนแรก ใช้แท็บ **การแปลงสกุลเงิน** เพื่อเลือกอัตราแลกเปลี่ยนเริ่มต้นสำหรับการแปลงในระหว่างกระบวนการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="8da13-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="8da13-106">หลังจากป้อนอัตราแลกเปลี่ยนใหม่ (ตัวอย่างเช่น ในเดือนถัดไป) คุณต้องประเมินค่ายอดดุลบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="8da13-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="8da13-107">กำไรหรือขาดทุนที่ยังไม่รับรู้จะถูกอัพเดตไปตามนั้น ตามอัตราแลกเปลี่ยนและวันใหม่</span><span class="sxs-lookup"><span data-stu-id="8da13-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="8da13-108">ตัวอย่างต่อไปนี้แสดงให้เห็นรายการบัญชีที่สร้างขึ้นในระหว่างกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="8da13-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="8da13-109">การจัดเตรียมบริษัท</span><span class="sxs-lookup"><span data-stu-id="8da13-109">Company setup</span></span>
-   <span data-ttu-id="8da13-110">**แหล่งที่มา/บริษัทที่ดำเนินการ (USMF)** – ดอลลาร์สหรัฐฯ (USD) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8da13-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="8da13-111">**บริษัทแบบรวมบัญชี(CON)** – ยูโร (EUR) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8da13-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="8da13-112">**กำไรที่รับรู้** – บัญชีแยกประเภท 801500</span><span class="sxs-lookup"><span data-stu-id="8da13-112">**Realized gain** – Ledger account 801500</span></span>
    -   <span data-ttu-id="8da13-113">**ขาดทุนที่รับรู้** – บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="8da13-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="8da13-114">**กำไรที่ยังไม่รับรู้** – บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="8da13-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="8da13-115">**ขาดทุนที่ยังไม่รับรู้** – บัญชีแยกประเภท 801400</span><span class="sxs-lookup"><span data-stu-id="8da13-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="8da13-116">ธุรกรรมดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="8da13-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="8da13-117">ธุรกรรมของใบเสร็จรับเงินใน USMF</span><span class="sxs-lookup"><span data-stu-id="8da13-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="8da13-118">วันที่</span><span class="sxs-lookup"><span data-stu-id="8da13-118">Date</span></span>       | <span data-ttu-id="8da13-119">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8da13-119">Ledger account</span></span>               | <span data-ttu-id="8da13-120">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-120">Currency</span></span> | <span data-ttu-id="8da13-121">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="8da13-122">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="8da13-122">10/11/2015</span></span> | <span data-ttu-id="8da13-123">110110 - เงินสด</span><span class="sxs-lookup"><span data-stu-id="8da13-123">110110 – Cash</span></span>                | <span data-ttu-id="8da13-124">USD</span><span class="sxs-lookup"><span data-stu-id="8da13-124">USD</span></span>      | <span data-ttu-id="8da13-125">500</span><span class="sxs-lookup"><span data-stu-id="8da13-125">500</span></span>    |
| <span data-ttu-id="8da13-126">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="8da13-126">10/11/2015</span></span> | <span data-ttu-id="8da13-127">130100 – บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="8da13-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="8da13-128">USD</span><span class="sxs-lookup"><span data-stu-id="8da13-128">USD</span></span>      | <span data-ttu-id="8da13-129">-500</span><span class="sxs-lookup"><span data-stu-id="8da13-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="8da13-130">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="8da13-130">Exchange rates</span></span>

| <span data-ttu-id="8da13-131">สกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="8da13-131">From currency</span></span> | <span data-ttu-id="8da13-132">สกุลเงินสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="8da13-132">To currency</span></span> | <span data-ttu-id="8da13-133">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8da13-133">Start date</span></span> | <span data-ttu-id="8da13-134">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="8da13-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="8da13-135">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-135">EUR</span></span>           | <span data-ttu-id="8da13-136">USD</span><span class="sxs-lookup"><span data-stu-id="8da13-136">USD</span></span>         | <span data-ttu-id="8da13-137">วันที่ 1 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="8da13-137">10/1/2015</span></span>  | <span data-ttu-id="8da13-138">200</span><span class="sxs-lookup"><span data-stu-id="8da13-138">200</span></span>           |
| <span data-ttu-id="8da13-139">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-139">EUR</span></span>           | <span data-ttu-id="8da13-140">USD</span><span class="sxs-lookup"><span data-stu-id="8da13-140">USD</span></span>         | <span data-ttu-id="8da13-141">วันที่ 1 พฤษจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="8da13-141">11/1/2015</span></span>  | <span data-ttu-id="8da13-142">150</span><span class="sxs-lookup"><span data-stu-id="8da13-142">150</span></span>           |
| <span data-ttu-id="8da13-143">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-143">EUR</span></span>           | <span data-ttu-id="8da13-144">USD</span><span class="sxs-lookup"><span data-stu-id="8da13-144">USD</span></span>         | <span data-ttu-id="8da13-145">1 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="8da13-145">12/1/2012</span></span>  | <span data-ttu-id="8da13-146">100</span><span class="sxs-lookup"><span data-stu-id="8da13-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="8da13-147">ดำเนินการรวมบัญชีสำหรับเดือนตุลาคม 2015 </span><span class="sxs-lookup"><span data-stu-id="8da13-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="8da13-148">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="8da13-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="8da13-149">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8da13-149">Ledger account</span></span> | <span data-ttu-id="8da13-150">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-150">Currency</span></span> | <span data-ttu-id="8da13-151">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-151">Amount</span></span> | <span data-ttu-id="8da13-152">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8da13-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="8da13-153">110110</span><span class="sxs-lookup"><span data-stu-id="8da13-153">110110</span></span>         | <span data-ttu-id="8da13-154">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-154">EUR</span></span>      | <span data-ttu-id="8da13-155">250</span><span class="sxs-lookup"><span data-stu-id="8da13-155">250</span></span>    | <span data-ttu-id="8da13-156">500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="8da13-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="8da13-157">130100</span><span class="sxs-lookup"><span data-stu-id="8da13-157">130100</span></span>         | <span data-ttu-id="8da13-158">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-158">EUR</span></span>      | <span data-ttu-id="8da13-159">-250</span><span class="sxs-lookup"><span data-stu-id="8da13-159">-250</span></span>   | <span data-ttu-id="8da13-160">-500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="8da13-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="8da13-161">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 30 พฤศจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="8da13-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="8da13-162">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="8da13-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="8da13-163">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8da13-163">Ledger account</span></span> | <span data-ttu-id="8da13-164">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-164">Currency</span></span> | <span data-ttu-id="8da13-165">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-165">Amount</span></span>  | <span data-ttu-id="8da13-166">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8da13-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="8da13-167">110110</span><span class="sxs-lookup"><span data-stu-id="8da13-167">110110</span></span>         | <span data-ttu-id="8da13-168">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-168">EUR</span></span>      | <span data-ttu-id="8da13-169">333.33</span><span class="sxs-lookup"><span data-stu-id="8da13-169">333.33</span></span>  | <span data-ttu-id="8da13-170">ยอดเงินเดิมของ 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="8da13-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="8da13-171">130100</span><span class="sxs-lookup"><span data-stu-id="8da13-171">130100</span></span>         | <span data-ttu-id="8da13-172">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-172">EUR</span></span>      | <span data-ttu-id="8da13-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="8da13-173">-333.33</span></span> | <span data-ttu-id="8da13-174">ยอดเงินเดิมของ -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="8da13-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="8da13-175">801400</span><span class="sxs-lookup"><span data-stu-id="8da13-175">801400</span></span>         | <span data-ttu-id="8da13-176">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-176">EUR</span></span>      | <span data-ttu-id="8da13-177">83.33</span><span class="sxs-lookup"><span data-stu-id="8da13-177">83.33</span></span>   | <span data-ttu-id="8da13-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="8da13-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="8da13-179">801600</span><span class="sxs-lookup"><span data-stu-id="8da13-179">801600</span></span>         | <span data-ttu-id="8da13-180">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-180">EUR</span></span>      | <span data-ttu-id="8da13-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="8da13-181">-83.33</span></span>  | <span data-ttu-id="8da13-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="8da13-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="8da13-183">คุณจะเห็นธุรกรรมเพิ่มเติมสำหรับยอดสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8da13-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="8da13-184">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 31 ธันวาคม 2015</span><span class="sxs-lookup"><span data-stu-id="8da13-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="8da13-185">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="8da13-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="8da13-186">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="8da13-186">Ledger account</span></span> | <span data-ttu-id="8da13-187">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-187">Currency</span></span> | <span data-ttu-id="8da13-188">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8da13-188">Amount</span></span>  | <span data-ttu-id="8da13-189">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8da13-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="8da13-190">110110</span><span class="sxs-lookup"><span data-stu-id="8da13-190">110110</span></span>         | <span data-ttu-id="8da13-191">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-191">EUR</span></span>      | <span data-ttu-id="8da13-192">500.00</span><span class="sxs-lookup"><span data-stu-id="8da13-192">500.00</span></span>  | <span data-ttu-id="8da13-193">ยอดเงินเดิมของ 500 × 1</span><span class="sxs-lookup"><span data-stu-id="8da13-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="8da13-194">130100</span><span class="sxs-lookup"><span data-stu-id="8da13-194">130100</span></span>         | <span data-ttu-id="8da13-195">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-195">EUR</span></span>      | <span data-ttu-id="8da13-196">-500.00.</span><span class="sxs-lookup"><span data-stu-id="8da13-196">-500.00</span></span> | <span data-ttu-id="8da13-197">ยอดเงินเดิมของ -500 × 1</span><span class="sxs-lookup"><span data-stu-id="8da13-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="8da13-198">801400</span><span class="sxs-lookup"><span data-stu-id="8da13-198">801400</span></span>         | <span data-ttu-id="8da13-199">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-199">EUR</span></span>      | <span data-ttu-id="8da13-200">250</span><span class="sxs-lookup"><span data-stu-id="8da13-200">250</span></span>     | <span data-ttu-id="8da13-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="8da13-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="8da13-202">801600</span><span class="sxs-lookup"><span data-stu-id="8da13-202">801600</span></span>         | <span data-ttu-id="8da13-203">EUR</span><span class="sxs-lookup"><span data-stu-id="8da13-203">EUR</span></span>      | <span data-ttu-id="8da13-204">-250</span><span class="sxs-lookup"><span data-stu-id="8da13-204">-250</span></span>    | <span data-ttu-id="8da13-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="8da13-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





