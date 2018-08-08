---
title: "อัตราภาษีขายที่ขึ้นอยู่กับฐานกำไรเบื้องต้นและวิธีการคำนวณ"
description: "หัวข้อนี้อธิบายวิธีที่ค่าในฟิลด์ฐานกำไรเบื้องต้นและวิธีการคำนวณ ระบุอัตราภาษีในธุรกรรมการขายและการซื้อ"
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 0128743e608ec56bea2301ac576551065a1ff290
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="53992-103">อัตราภาษีขายที่ขึ้นอยู่กับฐานกำไรเบื้องต้นและวิธีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="53992-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53992-104">หัวข้อนี้อธิบายวิธีที่ค่าในฟิลด์ฐานกำไรเบื้องต้นและวิธีการคำนวณ ระบุอัตราภาษีในธุรกรรมการขายและการซื้อ</span><span class="sxs-lookup"><span data-stu-id="53992-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="53992-105">ฐานกำไรเบื้องต้นบนแท็บด่วนการคำนวณในหน้ารหัสภาษีขายกำหนดยอดเงินที่จะใช้ในการเลือกอัตราภาษีที่เหมาะสมจากอัตราในหน้าค่าของรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="53992-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="53992-106">ชนิดยอดเงินในฟิลด์พื้นฐานกำไรเบื้องต้นในชุดข้อมูลที่วิธีการในฟิลด์วิธีการคำนวณกำหนดตรรกะเพื่อการค้นหาอัตราภาษีที่ถูกต้องสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="53992-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="53992-107">ชุดของค่าที่แตกต่างกันในฟิลด์เหล่านี้ให้วิธีการคำนวณภาษีขายที่แตกต่างกันอย่างมาก ดังที่แสดงในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="53992-108">ตัวอย่างต่างๆ ใช้ค่าช่วงภาษีเดียวกัน ซึ่งมีการตั้งค่าสำหรับรหัสภาษีแต่ละรหัสในหน้าค่ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="53992-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="53992-109">เมื่อต้องการเปิดหน้านี้ คลิกรหัสภาษีขาย &gt; ค่าในหน้ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="53992-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="53992-110">ถ้าฐานส่วนเพิ่มของรหัสภาษีขายอย่างน้อยหนึ่งรายการ ขึ้นอยู่กับยอดเงินต่อรายการหรือหน่วย มูลค่าของฟิลด์วิธีการคำนวณในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไปต้องถูกตั้งค่าไปยังรายการ</span><span class="sxs-lookup"><span data-stu-id="53992-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="53992-111"> ยอดเงินสุทธิต่อรายการ</span><span class="sxs-lookup"><span data-stu-id="53992-111">Net amount per line</span></span>
<span data-ttu-id="53992-112">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามยอดเงินสุทธิของรายการใบแจ้งหนี้ โดยไม่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="53992-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="53992-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="53992-113">Example</span></span>

<span data-ttu-id="53992-114">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="53992-115">ช่วงยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="53992-115">Amount interval</span></span>    | <span data-ttu-id="53992-116">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="53992-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="53992-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="53992-117">0 - 50</span></span>             | <span data-ttu-id="53992-118">30%</span><span class="sxs-lookup"><span data-stu-id="53992-118">30%</span></span>      |
| <span data-ttu-id="53992-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="53992-119">50 - 100</span></span>           | <span data-ttu-id="53992-120">20%</span><span class="sxs-lookup"><span data-stu-id="53992-120">20%</span></span>      |
| <span data-ttu-id="53992-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="53992-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="53992-122">10%</span><span class="sxs-lookup"><span data-stu-id="53992-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="53992-123">ขีดจำกัดสูงสุดของศูนย์(0) ในช่วงสุดท้ายหมายความว่ายอดเงินทั้งหมดที่มากกว่า 100 รวมอยู่ในช่วง</span><span class="sxs-lookup"><span data-stu-id="53992-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="53992-124">ฐานกำไรเบื้องต้น: **ยอดเงินสุทธิต่อรายการ**</span><span class="sxs-lookup"><span data-stu-id="53992-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="53992-125">วิธีการคำนวณ: **ช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="53992-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="53992-126">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="53992-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="53992-127">ยอดเงินสุทธิสำหรับรายการใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="53992-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="53992-128">ภาษีมีการคำนวณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="53992-129">ภาษีขายรวม = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span><span class="sxs-lookup"><span data-stu-id="53992-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="53992-130">ยอดเงินใบแจ้งหนี้รวม = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="53992-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="53992-131">**ความแตกต่าง**</span><span class="sxs-lookup"><span data-stu-id="53992-131">**Variation**</span></span> 

<span data-ttu-id="53992-132">ถ้าใบแจ้งหนี้มีบรรทัดสองบรรทัดที่มีสินค้าอยู่บรรทัดละ 4 รายการ ยอดเงินสุทธิในแต่ละบรรทัดคือ 100.00 และภาษีขายมีการคำนวณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="53992-133">ภาษีขายบรรทัดที่ 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="53992-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="53992-134">ภาษีขายบรรทัดที่ 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="53992-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="53992-135">ภาษีขายรวม = 25.00 + 25.00 = 50.00</span><span class="sxs-lookup"><span data-stu-id="53992-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="53992-136">ยอดเงินใบแจ้งหนี้รวม = 200.00 + 50.00 = 250.00</span><span class="sxs-lookup"><span data-stu-id="53992-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="53992-137"> ยอดเงินสุทธิต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="53992-137">Net amount per unit</span></span>
<span data-ttu-id="53992-138">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่าของแต่ละหน่วย โดยไม่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="53992-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="53992-139">เมื่อมีเลือกฐานกำไรเบื้องต้นที่ยึดตามหน่วย จากนั้นแล้วหน่วยยังได้ถูกระบุไว้สำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="53992-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="53992-140">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="53992-140">Example</span></span>

<span data-ttu-id="53992-141">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="53992-142">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="53992-142">Amount</span></span>             | <span data-ttu-id="53992-143">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="53992-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="53992-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="53992-144">0 - 50</span></span>             | <span data-ttu-id="53992-145">30%</span><span class="sxs-lookup"><span data-stu-id="53992-145">30%</span></span>      |
| <span data-ttu-id="53992-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="53992-146">50 - 100</span></span>           | <span data-ttu-id="53992-147">20%</span><span class="sxs-lookup"><span data-stu-id="53992-147">20%</span></span>      |
| <span data-ttu-id="53992-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="53992-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="53992-149">10%</span><span class="sxs-lookup"><span data-stu-id="53992-149">10%</span></span>      |

<span data-ttu-id="53992-150">ฐานกำไรเบื้องต้น: **ยอดเงินสุทธิต่อหน่วย**</span><span class="sxs-lookup"><span data-stu-id="53992-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="53992-151">วิธีการคำนวณ: **ยอดเงินทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="53992-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="53992-152">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="53992-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="53992-153">ยอดเงินสุทธิสำหรับรายการใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="53992-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="53992-154">ภาษีมีคำนวณดังต่อไปนี้: ภาษีขายต่อหน่วย = 25.00 x 30% = 7.50 ภาษีขายรวม = 7.50 x 8 หน่วย = 60.00 ยอดเงินในใบแจ้งหนี้รวม = 200.00 + 60.00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="53992-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="53992-155"> ยอดเงินสุทธิของยอดดุลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="53992-155">Net amount of invoice balance</span></span>

<span data-ttu-id="53992-156">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่ารวมสำหรับใบแจ้งหนี้ โดยไม่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="53992-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="53992-157">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="53992-157">Example</span></span>

<span data-ttu-id="53992-158">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="53992-159">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="53992-159">Amount</span></span>            | <span data-ttu-id="53992-160">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="53992-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="53992-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="53992-161">0 - 50</span></span>            | <span data-ttu-id="53992-162">30%</span><span class="sxs-lookup"><span data-stu-id="53992-162">30%</span></span>      |
| <span data-ttu-id="53992-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="53992-163">50 - 100</span></span>          | <span data-ttu-id="53992-164">20%</span><span class="sxs-lookup"><span data-stu-id="53992-164">20%</span></span>      |
| <span data-ttu-id="53992-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="53992-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="53992-166">10%</span><span class="sxs-lookup"><span data-stu-id="53992-166">10%</span></span>      |

<span data-ttu-id="53992-167">ฐานกำไรเบื้องต้น: **ยอดเงินสุทธิของยอดดุลใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="53992-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="53992-168">วิธีการคำนวณ: **ช่วง** ใบแจ้งหนี้มีรายการสองรายการโดยมีโคมไฟสี่โคมในแต่ละรายการ รายการละ 25.00</span><span class="sxs-lookup"><span data-stu-id="53992-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="53992-169">ยอดเงินสุทธิของยอดดุลใบแจ้งหนี้คือ 4 x 25.00 + 4 x 25.00 = 200.00</span><span class="sxs-lookup"><span data-stu-id="53992-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="53992-170">ภาษีมีคำนวณดังต่อไปนี้: ภาษีขายรวม = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="53992-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="53992-171"> ยอดเงินรวมต่อรายการ</span><span class="sxs-lookup"><span data-stu-id="53992-171">Gross amount per line</span></span>

<span data-ttu-id="53992-172">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่าของภาษีอื่นๆทั้งหมดที่เกี่ยวข้องกับรายการสำหรับรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="53992-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="53992-173">ในกลุ่มภาษีขายหนึ่งกลุ่ม คุณสามารถมีรหัสภาษีขายที่มีการเลือกนี้อยู่ในฟิลด์ฐานกำไรเบื้องต้นได้เพียงหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="53992-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="53992-174">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="53992-174">Example</span></span>

<span data-ttu-id="53992-175">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="53992-176">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="53992-176">Amount</span></span>             | <span data-ttu-id="53992-177">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="53992-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="53992-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="53992-178">0 - 50</span></span>             | <span data-ttu-id="53992-179">30%</span><span class="sxs-lookup"><span data-stu-id="53992-179">30%</span></span>      |
| <span data-ttu-id="53992-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="53992-180">50 - 100</span></span>           | <span data-ttu-id="53992-181">20%</span><span class="sxs-lookup"><span data-stu-id="53992-181">20%</span></span>      |
| <span data-ttu-id="53992-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="53992-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="53992-183">10%</span><span class="sxs-lookup"><span data-stu-id="53992-183">10%</span></span>      |

<span data-ttu-id="53992-184">ฐานกำไรเบื้องต้น: **ยอดเงินรวมต่อรายการ** วิธีการคำนวณ: **ช่วง** นอกจากนี้ ยังมีรหัสภาษีอีกรหัสหนึ่งที่คำนวณสำหรับหน้าที่พิเศษเป็น 5.00 ในโคมไฟแต่ละโคม</span><span class="sxs-lookup"><span data-stu-id="53992-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="53992-185">ภาษีจะถูกบวกเพิ่มเข้าไปในยอดเงินสุทธิก่อนการคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="53992-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="53992-186">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="53992-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="53992-187">ยอดเงินสุทธิสำหรับรายการใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="53992-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="53992-188">ยอดเงินรวมสำหรับรายการใบแจ้งหนี้คือ 8 x 25.00 + 8 x 5.00 = 240.00</span><span class="sxs-lookup"><span data-stu-id="53992-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="53992-189">มีการคำนวณภาษีดังต่อไปนี้: ภาษีขายรวม = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 ภาษีรวม = 5.00 x 8 = 40.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="53992-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="53992-190">**ความแตกต่าง**</span><span class="sxs-lookup"><span data-stu-id="53992-190">**Variation**</span></span> 

<span data-ttu-id="53992-191">ถ้าใบแจ้งหนี้สร้างขึ้นโดยใช้บรรทัดใบแจ้งหนี้สองบรรทัดที่มีสินค้าอยู่บรรทัดละ 4 รายการ ยอดเงินสุทธิสำหรับบรรทัดใบแจ้งหนี้แต่ละบรรทัดคือ 100.00</span><span class="sxs-lookup"><span data-stu-id="53992-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="53992-192">ยอดเงินรวม (รวมภาษี 4 x 5.00) สำหรับแต่ละรายการใบแจ้งหนี้จะเป็น 120.00 และภาษีขายถูกสร้างขึ้นเป็นดังต่อไปนี้: ใบแจ้งหนี้ภาษีขายรายการที่ 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 ใบแจ้งหนี้ภาษีขายรายการที่ 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 ภาษีขายรวม = 27.00 + 27.00 = 54.00 ภาษีรวม = 5.00 x 8 = 40.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 54.00 + 40.00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="53992-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="53992-193"> ยอดเงินรวมต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="53992-193">Gross amount per unit</span></span>

<span data-ttu-id="53992-194">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่าของหน่วยที่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="53992-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="53992-195">ในกลุ่มภาษีขายหนึ่งกลุ่ม คุณสามารถมีรหัสภาษีขายที่มีการเลือกนี้อยู่ในฟิลด์ฐานกำไรเบื้องต้นได้เพียงหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="53992-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="53992-196">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="53992-196">Example</span></span>

<span data-ttu-id="53992-197">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="53992-198">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="53992-198">Amount</span></span>             | <span data-ttu-id="53992-199">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="53992-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="53992-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="53992-200">0 - 50</span></span>             | <span data-ttu-id="53992-201">30%</span><span class="sxs-lookup"><span data-stu-id="53992-201">30%</span></span>      |
| <span data-ttu-id="53992-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="53992-202">50 - 100</span></span>           | <span data-ttu-id="53992-203">20%</span><span class="sxs-lookup"><span data-stu-id="53992-203">20%</span></span>      |
| <span data-ttu-id="53992-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="53992-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="53992-205">10%</span><span class="sxs-lookup"><span data-stu-id="53992-205">10%</span></span>      |

<span data-ttu-id="53992-206">ฐานกำไรเบื้องต้น: **ยอดเงินรวมต่อหน่วย** มีภาษีพิเศษ 5.00 ในโคมไฟแต่ละโคม</span><span class="sxs-lookup"><span data-stu-id="53992-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="53992-207">ภาษีจะถูกบวกเพิ่มเข้าไปในยอดเงินสุทธิก่อนการคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="53992-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="53992-208">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="53992-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="53992-209">ยอดเงินรวมแต่ละหน่วยคือ 30.00</span><span class="sxs-lookup"><span data-stu-id="53992-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="53992-210">มีการคำนวณภาษีดังต่อไปนี้: ภาษีขายต่อหน่วย = 30 x 30% = 9.00 ภาษีขายรวม = 9.00 x 8 = 72.00 ยอดรวมภาษี= 5.00 x 8 = 40.00 ยอดเงินรวมในใบแจ้งหนี้ = 200.00 + 72.00 + 40.00 = 312.00</span><span class="sxs-lookup"><span data-stu-id="53992-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="53992-211"> ผลรวมใบแจ้งหนี้ รวมถึงยอดภาษีขายอื่น</span><span class="sxs-lookup"><span data-stu-id="53992-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="53992-212">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่ารวมสำหรับใบแจ้งหนี้ โดยรวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="53992-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="53992-213">ในกลุ่มภาษีขายหนึ่งกลุ่ม คุณสามารถมีรหัสภาษีขายที่มีการเลือกนี้อยู่ในฟิลด์ฐานกำไรเบื้องต้นได้เพียงหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="53992-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="53992-214">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="53992-214">Example</span></span>

<span data-ttu-id="53992-215">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53992-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="53992-216">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="53992-216">Amount</span></span>             | <span data-ttu-id="53992-217">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="53992-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="53992-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="53992-218">0 - 50</span></span>             | <span data-ttu-id="53992-219">30%</span><span class="sxs-lookup"><span data-stu-id="53992-219">30%</span></span>      |
| <span data-ttu-id="53992-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="53992-220">50 - 100</span></span>           | <span data-ttu-id="53992-221">20%</span><span class="sxs-lookup"><span data-stu-id="53992-221">20%</span></span>      |
| <span data-ttu-id="53992-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="53992-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="53992-223">10%</span><span class="sxs-lookup"><span data-stu-id="53992-223">10%</span></span>      |

<span data-ttu-id="53992-224">ฐานกำไรเบื้องต้น: **ใบแจ้งหนี้ทั้งหมดรวมถึงยอดภาษีขายอื่น** วิธีการคำนวณ: **ช่วงเวลา** </span><span class="sxs-lookup"><span data-stu-id="53992-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="53992-225">มีภาษีพิเศษในโคมไฟแต่ละโคมจำนวน 5.00</span><span class="sxs-lookup"><span data-stu-id="53992-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="53992-226">ภาษีจะถูกบวกเพิ่มเข้าไปในยอดเงินสุทธิก่อนการคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="53992-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="53992-227">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="53992-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="53992-228">ยอดเงินสุทธิสำหรับใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="53992-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="53992-229">ยอดเงินรวมสำหรับใบแจ้งหนี้คือ 200.00 + (8 x 5.00) = 240.00</span><span class="sxs-lookup"><span data-stu-id="53992-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="53992-230">มีการคำนวณภาษีดังต่อไปนี้: ภาษีขายรวม = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 ภาษีรวม = 5.00 x 8 = 40.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="53992-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="53992-231">สำหรับข้อมูลเพิ่มเติม ดูที่ [ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย](whole-amount-interval-options-sales-tax-codes.md) และ [วิธีการคำนวณภาษีขายในฟิลด์จุดเริ่มต้น](sales-tax-calculation-methods-origin-field.md)</span><span class="sxs-lookup"><span data-stu-id="53992-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>




