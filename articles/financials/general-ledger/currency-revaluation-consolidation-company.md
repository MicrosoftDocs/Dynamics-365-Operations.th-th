---
title: การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี
description: หัวข้อนี้อธิบายวิธีการประเมินค่าสกุลเงินในบริษัทสำหรับการรวมบัญชี
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567294"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="bcc08-103">การประเมินค่าสกุลเงินใหม่ในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="bcc08-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcc08-104">เมื่อคุณรวมข้อมูลจากสกุลเงินทางบัญชีหนึ่งไปอีกสกุลเงินทางบัญชีหนึ่ง คุณต้องรันการประเมินค่าสกุลเงินใหม่หากมีการเปลี่ยนแปลงอัตราแลกเปลี่ยน จากนั้นยอดดุลบัญชีของคุณถึงจะได้ประเมินค่าใหม่ได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="bcc08-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="bcc08-105">เมื่อคุณรวมข้อมูลไว้ในตอนแรก ใช้แท็บ **การแปลงสกุลเงิน** เพื่อเลือกอัตราแลกเปลี่ยนเริ่มต้นสำหรับการแปลงในระหว่างกระบวนการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="bcc08-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="bcc08-106">หลังจากป้อนอัตราแลกเปลี่ยนใหม่ (ตัวอย่างเช่น ในเดือนถัดไป) คุณต้องประเมินค่ายอดดุลบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="bcc08-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="bcc08-107">กำไรหรือขาดทุนที่ยังไม่รับรู้จะถูกอัพเดตไปตามนั้น ตามอัตราแลกเปลี่ยนและวันใหม่</span><span class="sxs-lookup"><span data-stu-id="bcc08-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="bcc08-108">ตัวอย่างต่อไปนี้แสดงให้เห็นรายการบัญชีที่สร้างขึ้นในระหว่างกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="bcc08-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="bcc08-109">การจัดเตรียมบริษัท</span><span class="sxs-lookup"><span data-stu-id="bcc08-109">Company setup</span></span>
-   <span data-ttu-id="bcc08-110">**แหล่งที่มา/บริษัทที่ดำเนินการ (USMF)** – ดอลลาร์สหรัฐฯ (USD) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="bcc08-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="bcc08-111">**บริษัทแบบรวมบัญชี(CON)** – ยูโร (EUR) จะถูกใช้ในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="bcc08-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="bcc08-112">**กำไรที่รับรู้**– บัญชีแยกประเภท 801500</span><span class="sxs-lookup"><span data-stu-id="bcc08-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="bcc08-113">**ขาดทุนที่รับรู้** – บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="bcc08-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="bcc08-114">**กำไรที่ยังไม่รับรู้**– บัญชีแยกประเภท 801600</span><span class="sxs-lookup"><span data-stu-id="bcc08-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="bcc08-115">**ขาดทุนที่ยังไม่รับรู้**– บัญชีแยกประเภท 801400</span><span class="sxs-lookup"><span data-stu-id="bcc08-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="bcc08-116">ธุรกรรมดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="bcc08-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="bcc08-117">ธุรกรรมของใบเสร็จรับเงินใน USMF</span><span class="sxs-lookup"><span data-stu-id="bcc08-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="bcc08-118">วันที่</span><span class="sxs-lookup"><span data-stu-id="bcc08-118">Date</span></span>       | <span data-ttu-id="bcc08-119">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="bcc08-119">Ledger account</span></span>               | <span data-ttu-id="bcc08-120">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-120">Currency</span></span> | <span data-ttu-id="bcc08-121">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="bcc08-122">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="bcc08-122">10/11/2015</span></span> | <span data-ttu-id="bcc08-123">110110 - เงินสด</span><span class="sxs-lookup"><span data-stu-id="bcc08-123">110110 – Cash</span></span>                | <span data-ttu-id="bcc08-124">USD</span><span class="sxs-lookup"><span data-stu-id="bcc08-124">USD</span></span>      | <span data-ttu-id="bcc08-125">500</span><span class="sxs-lookup"><span data-stu-id="bcc08-125">500</span></span>    |
| <span data-ttu-id="bcc08-126">วันที่ 11 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="bcc08-126">10/11/2015</span></span> | <span data-ttu-id="bcc08-127">130100 – บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="bcc08-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="bcc08-128">USD</span><span class="sxs-lookup"><span data-stu-id="bcc08-128">USD</span></span>      | <span data-ttu-id="bcc08-129">-500</span><span class="sxs-lookup"><span data-stu-id="bcc08-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="bcc08-130">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="bcc08-130">Exchange rates</span></span>

| <span data-ttu-id="bcc08-131">สกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="bcc08-131">From currency</span></span> | <span data-ttu-id="bcc08-132">สกุลเงินสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="bcc08-132">To currency</span></span> | <span data-ttu-id="bcc08-133">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bcc08-133">Start date</span></span> | <span data-ttu-id="bcc08-134">อัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="bcc08-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="bcc08-135">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-135">EUR</span></span>           | <span data-ttu-id="bcc08-136">USD</span><span class="sxs-lookup"><span data-stu-id="bcc08-136">USD</span></span>         | <span data-ttu-id="bcc08-137">วันที่ 1 ตุลาคม 2015</span><span class="sxs-lookup"><span data-stu-id="bcc08-137">10/1/2015</span></span>  | <span data-ttu-id="bcc08-138">200</span><span class="sxs-lookup"><span data-stu-id="bcc08-138">200</span></span>           |
| <span data-ttu-id="bcc08-139">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-139">EUR</span></span>           | <span data-ttu-id="bcc08-140">USD</span><span class="sxs-lookup"><span data-stu-id="bcc08-140">USD</span></span>         | <span data-ttu-id="bcc08-141">วันที่ 1 พฤษจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="bcc08-141">11/1/2015</span></span>  | <span data-ttu-id="bcc08-142">150</span><span class="sxs-lookup"><span data-stu-id="bcc08-142">150</span></span>           |
| <span data-ttu-id="bcc08-143">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-143">EUR</span></span>           | <span data-ttu-id="bcc08-144">USD</span><span class="sxs-lookup"><span data-stu-id="bcc08-144">USD</span></span>         | <span data-ttu-id="bcc08-145">1 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="bcc08-145">12/1/2012</span></span>  | <span data-ttu-id="bcc08-146">100</span><span class="sxs-lookup"><span data-stu-id="bcc08-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="bcc08-147">ดำเนินการรวมบัญชีสำหรับเดือนตุลาคม 2015 </span><span class="sxs-lookup"><span data-stu-id="bcc08-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="bcc08-148">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="bcc08-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="bcc08-149">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="bcc08-149">Ledger account</span></span> | <span data-ttu-id="bcc08-150">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-150">Currency</span></span> | <span data-ttu-id="bcc08-151">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-151">Amount</span></span> | <span data-ttu-id="bcc08-152">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="bcc08-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="bcc08-153">110110</span><span class="sxs-lookup"><span data-stu-id="bcc08-153">110110</span></span>         | <span data-ttu-id="bcc08-154">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-154">EUR</span></span>      | <span data-ttu-id="bcc08-155">250</span><span class="sxs-lookup"><span data-stu-id="bcc08-155">250</span></span>    | <span data-ttu-id="bcc08-156">500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="bcc08-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="bcc08-157">130100</span><span class="sxs-lookup"><span data-stu-id="bcc08-157">130100</span></span>         | <span data-ttu-id="bcc08-158">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-158">EUR</span></span>      | <span data-ttu-id="bcc08-159">-250</span><span class="sxs-lookup"><span data-stu-id="bcc08-159">-250</span></span>   | <span data-ttu-id="bcc08-160">-500 ดอลลาร์สหรัฐ × 50%</span><span class="sxs-lookup"><span data-stu-id="bcc08-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="bcc08-161">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 30 พฤศจิกายน 2015</span><span class="sxs-lookup"><span data-stu-id="bcc08-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="bcc08-162">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="bcc08-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="bcc08-163">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="bcc08-163">Ledger account</span></span> | <span data-ttu-id="bcc08-164">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-164">Currency</span></span> | <span data-ttu-id="bcc08-165">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-165">Amount</span></span>  | <span data-ttu-id="bcc08-166">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="bcc08-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="bcc08-167">110110</span><span class="sxs-lookup"><span data-stu-id="bcc08-167">110110</span></span>         | <span data-ttu-id="bcc08-168">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-168">EUR</span></span>      | <span data-ttu-id="bcc08-169">333.33</span><span class="sxs-lookup"><span data-stu-id="bcc08-169">333.33</span></span>  | <span data-ttu-id="bcc08-170">ยอดเงินเดิมของ 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="bcc08-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="bcc08-171">130100</span><span class="sxs-lookup"><span data-stu-id="bcc08-171">130100</span></span>         | <span data-ttu-id="bcc08-172">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-172">EUR</span></span>      | <span data-ttu-id="bcc08-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="bcc08-173">-333.33</span></span> | <span data-ttu-id="bcc08-174">ยอดเงินเดิมของ -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="bcc08-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="bcc08-175">801400</span><span class="sxs-lookup"><span data-stu-id="bcc08-175">801400</span></span>         | <span data-ttu-id="bcc08-176">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-176">EUR</span></span>      | <span data-ttu-id="bcc08-177">83.33</span><span class="sxs-lookup"><span data-stu-id="bcc08-177">83.33</span></span>   | <span data-ttu-id="bcc08-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="bcc08-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="bcc08-179">801600</span><span class="sxs-lookup"><span data-stu-id="bcc08-179">801600</span></span>         | <span data-ttu-id="bcc08-180">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-180">EUR</span></span>      | <span data-ttu-id="bcc08-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="bcc08-181">-83.33</span></span>  | <span data-ttu-id="bcc08-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="bcc08-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="bcc08-183">คุณจะเห็นธุรกรรมเพิ่มเติมสำหรับยอดสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="bcc08-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="bcc08-184">ดำเนินการประเมินค่าสกุลเงินใหม่สำหรับบัญชีจาก 1 ตุลาคม 2015 ถึง 31 ธันวาคม 2015</span><span class="sxs-lookup"><span data-stu-id="bcc08-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="bcc08-185">ยอดดุลในบริษัทที่รวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="bcc08-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="bcc08-186">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="bcc08-186">Ledger account</span></span> | <span data-ttu-id="bcc08-187">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-187">Currency</span></span> | <span data-ttu-id="bcc08-188">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="bcc08-188">Amount</span></span>  | <span data-ttu-id="bcc08-189">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="bcc08-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="bcc08-190">110110</span><span class="sxs-lookup"><span data-stu-id="bcc08-190">110110</span></span>         | <span data-ttu-id="bcc08-191">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-191">EUR</span></span>      | <span data-ttu-id="bcc08-192">500.00</span><span class="sxs-lookup"><span data-stu-id="bcc08-192">500.00</span></span>  | <span data-ttu-id="bcc08-193">ยอดเงินเดิมของ 500 × 1</span><span class="sxs-lookup"><span data-stu-id="bcc08-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="bcc08-194">130100</span><span class="sxs-lookup"><span data-stu-id="bcc08-194">130100</span></span>         | <span data-ttu-id="bcc08-195">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-195">EUR</span></span>      | <span data-ttu-id="bcc08-196">-500.00.</span><span class="sxs-lookup"><span data-stu-id="bcc08-196">-500.00</span></span> | <span data-ttu-id="bcc08-197">ยอดเงินเดิมของ -500 × 1</span><span class="sxs-lookup"><span data-stu-id="bcc08-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="bcc08-198">801400</span><span class="sxs-lookup"><span data-stu-id="bcc08-198">801400</span></span>         | <span data-ttu-id="bcc08-199">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-199">EUR</span></span>      | <span data-ttu-id="bcc08-200">250</span><span class="sxs-lookup"><span data-stu-id="bcc08-200">250</span></span>     | <span data-ttu-id="bcc08-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="bcc08-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="bcc08-202">801600</span><span class="sxs-lookup"><span data-stu-id="bcc08-202">801600</span></span>         | <span data-ttu-id="bcc08-203">EUR</span><span class="sxs-lookup"><span data-stu-id="bcc08-203">EUR</span></span>      | <span data-ttu-id="bcc08-204">-250</span><span class="sxs-lookup"><span data-stu-id="bcc08-204">-250</span></span>    | <span data-ttu-id="bcc08-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="bcc08-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





