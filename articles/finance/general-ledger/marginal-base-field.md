---
title: อัตราภาษีขายที่ขึ้นอยู่กับฐานกำไรเบื้องต้นและวิธีการคำนวณ
description: หัวข้อนี้อธิบายวิธีที่ค่าในฟิลด์ฐานกำไรเบื้องต้นและวิธีการคำนวณ ระบุอัตราภาษีในธุรกรรมการขายและการซื้อ
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e7e3f37d759953b7b4f70fe9eae78154da44d1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180105"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="17328-103">อัตราภาษีขายที่ขึ้นอยู่กับฐานกำไรเบื้องต้นและวิธีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="17328-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17328-104">หัวข้อนี้อธิบายวิธีที่ค่าในฟิลด์ฐานกำไรเบื้องต้นและวิธีการคำนวณ ระบุอัตราภาษีในธุรกรรมการขายและการซื้อ</span><span class="sxs-lookup"><span data-stu-id="17328-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="17328-105">ฐานกำไรเบื้องต้นบนแท็บด่วนการคำนวณในหน้ารหัสภาษีขายกำหนดยอดเงินที่จะใช้ในการเลือกอัตราภาษีที่เหมาะสมจากอัตราในหน้าค่าของรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="17328-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="17328-106">ชนิดยอดเงินในฟิลด์พื้นฐานกำไรเบื้องต้นในชุดข้อมูลที่วิธีการในฟิลด์วิธีการคำนวณกำหนดตรรกะเพื่อการค้นหาอัตราภาษีที่ถูกต้องสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="17328-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="17328-107">ชุดของค่าที่แตกต่างกันในฟิลด์เหล่านี้ให้วิธีการคำนวณภาษีขายที่แตกต่างกันอย่างมาก ดังที่แสดงในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="17328-108">ตัวอย่างต่างๆ ใช้ค่าช่วงภาษีเดียวกัน ซึ่งมีการตั้งค่าสำหรับรหัสภาษีแต่ละรหัสในหน้าค่ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="17328-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="17328-109">เมื่อต้องการเปิดหน้านี้ คลิกรหัสภาษีขาย &gt; ค่าในหน้ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="17328-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="17328-110">ถ้าฐานส่วนเพิ่มของรหัสภาษีขายอย่างน้อยหนึ่งรายการ ขึ้นอยู่กับยอดเงินต่อรายการหรือหน่วย มูลค่าของฟิลด์วิธีการคำนวณในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไปต้องถูกตั้งค่าไปยังรายการ</span><span class="sxs-lookup"><span data-stu-id="17328-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="17328-111"> ยอดเงินสุทธิต่อรายการ</span><span class="sxs-lookup"><span data-stu-id="17328-111">Net amount per line</span></span>
<span data-ttu-id="17328-112">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามยอดเงินสุทธิของรายการใบแจ้งหนี้ โดยไม่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="17328-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="17328-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="17328-113">Example</span></span>

<span data-ttu-id="17328-114">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="17328-115">ช่วงยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="17328-115">Amount interval</span></span>    | <span data-ttu-id="17328-116">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="17328-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="17328-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="17328-117">0 - 50</span></span>             | <span data-ttu-id="17328-118">30%</span><span class="sxs-lookup"><span data-stu-id="17328-118">30%</span></span>      |
| <span data-ttu-id="17328-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="17328-119">50 - 100</span></span>           | <span data-ttu-id="17328-120">20%</span><span class="sxs-lookup"><span data-stu-id="17328-120">20%</span></span>      |
| <span data-ttu-id="17328-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="17328-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="17328-122">10%</span><span class="sxs-lookup"><span data-stu-id="17328-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="17328-123">ขีดจำกัดสูงสุดของศูนย์(0) ในช่วงสุดท้ายหมายความว่ายอดเงินทั้งหมดที่มากกว่า 100 รวมอยู่ในช่วง</span><span class="sxs-lookup"><span data-stu-id="17328-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="17328-124">ฐานกำไรเบื้องต้น: **ยอดเงินสุทธิต่อรายการ**</span><span class="sxs-lookup"><span data-stu-id="17328-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="17328-125">วิธีการคำนวณ: **ช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="17328-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="17328-126">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="17328-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="17328-127">ยอดเงินสุทธิสำหรับรายการใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="17328-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="17328-128">ภาษีมีการคำนวณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="17328-129">ภาษีขายรวม = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span><span class="sxs-lookup"><span data-stu-id="17328-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="17328-130">ยอดเงินใบแจ้งหนี้รวม = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="17328-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="17328-131">**ความแตกต่าง**</span><span class="sxs-lookup"><span data-stu-id="17328-131">**Variation**</span></span> 

<span data-ttu-id="17328-132">ถ้าใบแจ้งหนี้มีบรรทัดสองบรรทัดที่มีสินค้าอยู่บรรทัดละ 4 รายการ ยอดเงินสุทธิในแต่ละบรรทัดคือ 100.00 และภาษีขายมีการคำนวณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="17328-133">ภาษีขายบรรทัดที่ 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="17328-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="17328-134">ภาษีขายบรรทัดที่ 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="17328-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="17328-135">ภาษีขายรวม = 25.00 + 25.00 = 50.00</span><span class="sxs-lookup"><span data-stu-id="17328-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="17328-136">ยอดเงินใบแจ้งหนี้รวม = 200.00 + 50.00 = 250.00</span><span class="sxs-lookup"><span data-stu-id="17328-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="17328-137"> ยอดเงินสุทธิต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="17328-137">Net amount per unit</span></span>
<span data-ttu-id="17328-138">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่าของแต่ละหน่วย โดยไม่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="17328-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="17328-139">เมื่อมีเลือกฐานกำไรเบื้องต้นที่ยึดตามหน่วย จากนั้นแล้วหน่วยยังได้ถูกระบุไว้สำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="17328-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="17328-140">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="17328-140">Example</span></span>

<span data-ttu-id="17328-141">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="17328-142">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="17328-142">Amount</span></span>             | <span data-ttu-id="17328-143">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="17328-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="17328-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="17328-144">0 - 50</span></span>             | <span data-ttu-id="17328-145">30%</span><span class="sxs-lookup"><span data-stu-id="17328-145">30%</span></span>      |
| <span data-ttu-id="17328-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="17328-146">50 - 100</span></span>           | <span data-ttu-id="17328-147">20%</span><span class="sxs-lookup"><span data-stu-id="17328-147">20%</span></span>      |
| <span data-ttu-id="17328-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="17328-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="17328-149">10%</span><span class="sxs-lookup"><span data-stu-id="17328-149">10%</span></span>      |

<span data-ttu-id="17328-150">ฐานกำไรเบื้องต้น: **ยอดเงินสุทธิต่อหน่วย**</span><span class="sxs-lookup"><span data-stu-id="17328-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="17328-151">วิธีการคำนวณ: **ยอดเงินทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="17328-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="17328-152">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="17328-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="17328-153">ยอดเงินสุทธิสำหรับรายการใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="17328-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="17328-154">ภาษีมีคำนวณดังต่อไปนี้: ภาษีขายต่อหน่วย = 25.00 x 30% = 7.50 ภาษีขายรวม = 7.50 x 8 หน่วย = 60.00 ยอดเงินในใบแจ้งหนี้รวม = 200.00 + 60.00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="17328-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="17328-155"> ยอดเงินสุทธิของยอดดุลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="17328-155">Net amount of invoice balance</span></span>

<span data-ttu-id="17328-156">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่ารวมสำหรับใบแจ้งหนี้ โดยไม่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="17328-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="17328-157">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="17328-157">Example</span></span>

<span data-ttu-id="17328-158">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="17328-159">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="17328-159">Amount</span></span>            | <span data-ttu-id="17328-160">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="17328-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="17328-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="17328-161">0 - 50</span></span>            | <span data-ttu-id="17328-162">30%</span><span class="sxs-lookup"><span data-stu-id="17328-162">30%</span></span>      |
| <span data-ttu-id="17328-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="17328-163">50 - 100</span></span>          | <span data-ttu-id="17328-164">20%</span><span class="sxs-lookup"><span data-stu-id="17328-164">20%</span></span>      |
| <span data-ttu-id="17328-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="17328-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="17328-166">10%</span><span class="sxs-lookup"><span data-stu-id="17328-166">10%</span></span>      |

<span data-ttu-id="17328-167">ฐานกำไรเบื้องต้น: **ยอดเงินสุทธิของยอดดุลใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="17328-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="17328-168">วิธีการคำนวณ: **ช่วง** ใบแจ้งหนี้มีรายการสองรายการโดยมีโคมไฟสี่โคมในแต่ละรายการ รายการละ 25.00</span><span class="sxs-lookup"><span data-stu-id="17328-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="17328-169">ยอดเงินสุทธิของยอดดุลใบแจ้งหนี้คือ 4 x 25.00 + 4 x 25.00 = 200.00</span><span class="sxs-lookup"><span data-stu-id="17328-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="17328-170">ภาษีมีคำนวณดังต่อไปนี้: ภาษีขายรวม = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="17328-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="17328-171"> ยอดเงินรวมต่อรายการ</span><span class="sxs-lookup"><span data-stu-id="17328-171">Gross amount per line</span></span>

<span data-ttu-id="17328-172">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่าของภาษีอื่นๆทั้งหมดที่เกี่ยวข้องกับรายการสำหรับรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="17328-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="17328-173">ในกลุ่มภาษีขายหนึ่งกลุ่ม คุณสามารถมีรหัสภาษีขายที่มีการเลือกนี้อยู่ในฟิลด์ฐานกำไรเบื้องต้นได้เพียงหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="17328-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="17328-174">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="17328-174">Example</span></span>

<span data-ttu-id="17328-175">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="17328-176">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="17328-176">Amount</span></span>             | <span data-ttu-id="17328-177">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="17328-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="17328-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="17328-178">0 - 50</span></span>             | <span data-ttu-id="17328-179">30%</span><span class="sxs-lookup"><span data-stu-id="17328-179">30%</span></span>      |
| <span data-ttu-id="17328-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="17328-180">50 - 100</span></span>           | <span data-ttu-id="17328-181">20%</span><span class="sxs-lookup"><span data-stu-id="17328-181">20%</span></span>      |
| <span data-ttu-id="17328-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="17328-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="17328-183">10%</span><span class="sxs-lookup"><span data-stu-id="17328-183">10%</span></span>      |

<span data-ttu-id="17328-184">ฐานกำไรเบื้องต้น: **ยอดเงินรวมต่อรายการ** วิธีการคำนวณ: **ช่วง** นอกจากนี้ ยังมีรหัสภาษีอีกรหัสหนึ่งที่คำนวณสำหรับหน้าที่พิเศษเป็น 5.00 ในโคมไฟแต่ละโคม</span><span class="sxs-lookup"><span data-stu-id="17328-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="17328-185">ภาษีจะถูกบวกเพิ่มเข้าไปในยอดเงินสุทธิก่อนการคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="17328-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="17328-186">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="17328-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="17328-187">ยอดเงินสุทธิสำหรับรายการใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="17328-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="17328-188">ยอดเงินรวมสำหรับรายการใบแจ้งหนี้คือ 8 x 25.00 + 8 x 5.00 = 240.00</span><span class="sxs-lookup"><span data-stu-id="17328-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="17328-189">มีการคำนวณภาษีดังต่อไปนี้: ภาษีขายรวม = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 ภาษีรวม = 5.00 x 8 = 40.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="17328-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="17328-190">**ความแตกต่าง**</span><span class="sxs-lookup"><span data-stu-id="17328-190">**Variation**</span></span> 

<span data-ttu-id="17328-191">ถ้าใบแจ้งหนี้สร้างขึ้นโดยใช้บรรทัดใบแจ้งหนี้สองบรรทัดที่มีสินค้าอยู่บรรทัดละ 4 รายการ ยอดเงินสุทธิสำหรับบรรทัดใบแจ้งหนี้แต่ละบรรทัดคือ 100.00</span><span class="sxs-lookup"><span data-stu-id="17328-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="17328-192">ยอดเงินรวม (รวมภาษี 4 x 5.00) สำหรับแต่ละรายการใบแจ้งหนี้จะเป็น 120.00 และภาษีขายถูกสร้างขึ้นเป็นดังต่อไปนี้: ใบแจ้งหนี้ภาษีขายรายการที่ 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 ใบแจ้งหนี้ภาษีขายรายการที่ 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 ภาษีขายรวม = 27.00 + 27.00 = 54.00 ภาษีรวม = 5.00 x 8 = 40.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 54.00 + 40.00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="17328-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="17328-193"> ยอดเงินรวมต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="17328-193">Gross amount per unit</span></span>

<span data-ttu-id="17328-194">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่าของหน่วยที่รวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="17328-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="17328-195">ในกลุ่มภาษีขายหนึ่งกลุ่ม คุณสามารถมีรหัสภาษีขายที่มีการเลือกนี้อยู่ในฟิลด์ฐานกำไรเบื้องต้นได้เพียงหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="17328-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="17328-196">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="17328-196">Example</span></span>

<span data-ttu-id="17328-197">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="17328-198">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="17328-198">Amount</span></span>             | <span data-ttu-id="17328-199">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="17328-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="17328-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="17328-200">0 - 50</span></span>             | <span data-ttu-id="17328-201">30%</span><span class="sxs-lookup"><span data-stu-id="17328-201">30%</span></span>      |
| <span data-ttu-id="17328-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="17328-202">50 - 100</span></span>           | <span data-ttu-id="17328-203">20%</span><span class="sxs-lookup"><span data-stu-id="17328-203">20%</span></span>      |
| <span data-ttu-id="17328-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="17328-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="17328-205">10%</span><span class="sxs-lookup"><span data-stu-id="17328-205">10%</span></span>      |

<span data-ttu-id="17328-206">ฐานกำไรเบื้องต้น: **ยอดเงินรวมต่อหน่วย** มีภาษีพิเศษ 5.00 ในโคมไฟแต่ละโคม</span><span class="sxs-lookup"><span data-stu-id="17328-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="17328-207">ภาษีจะถูกบวกเพิ่มเข้าไปในยอดเงินสุทธิก่อนการคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="17328-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="17328-208">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="17328-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="17328-209">ยอดเงินรวมแต่ละหน่วยคือ 30.00</span><span class="sxs-lookup"><span data-stu-id="17328-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="17328-210">มีการคำนวณภาษีดังต่อไปนี้: ภาษีขายต่อหน่วย = 30 x 30% = 9.00 ภาษีขายรวม = 9.00 x 8 = 72.00 ยอดรวมภาษี= 5.00 x 8 = 40.00 ยอดเงินรวมในใบแจ้งหนี้ = 200.00 + 72.00 + 40.00 = 312.00</span><span class="sxs-lookup"><span data-stu-id="17328-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="17328-211"> ผลรวมใบแจ้งหนี้ รวมถึงยอดภาษีขายอื่น</span><span class="sxs-lookup"><span data-stu-id="17328-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="17328-212">เลือกตัวเลือกนี้เพื่อกำหนดอัตราภาษีขายตามมูลค่ารวมสำหรับใบแจ้งหนี้ โดยรวมภาษีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="17328-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="17328-213">ในกลุ่มภาษีขายหนึ่งกลุ่ม คุณสามารถมีรหัสภาษีขายที่มีการเลือกนี้อยู่ในฟิลด์ฐานกำไรเบื้องต้นได้เพียงหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="17328-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="17328-214">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="17328-214">Example</span></span>

<span data-ttu-id="17328-215">มีการตั้งค่าอัตราภาษีขายในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="17328-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="17328-216">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="17328-216">Amount</span></span>             | <span data-ttu-id="17328-217">อัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="17328-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="17328-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="17328-218">0 - 50</span></span>             | <span data-ttu-id="17328-219">30%</span><span class="sxs-lookup"><span data-stu-id="17328-219">30%</span></span>      |
| <span data-ttu-id="17328-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="17328-220">50 - 100</span></span>           | <span data-ttu-id="17328-221">20%</span><span class="sxs-lookup"><span data-stu-id="17328-221">20%</span></span>      |
| <span data-ttu-id="17328-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="17328-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="17328-223">10%</span><span class="sxs-lookup"><span data-stu-id="17328-223">10%</span></span>      |

<span data-ttu-id="17328-224">ฐานกำไรเบื้องต้น: **ใบแจ้งหนี้ทั้งหมดรวมถึงยอดภาษีขายอื่น** วิธีการคำนวณ: **ช่วงเวลา** </span><span class="sxs-lookup"><span data-stu-id="17328-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="17328-225">มีภาษีพิเศษในโคมไฟแต่ละโคมจำนวน 5.00</span><span class="sxs-lookup"><span data-stu-id="17328-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="17328-226">ภาษีจะถูกบวกเพิ่มเข้าไปในยอดเงินสุทธิก่อนการคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="17328-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="17328-227">คุณซื้อโคมไฟ 8 โคม ที่มีราคา 25.00 ต่อโคม</span><span class="sxs-lookup"><span data-stu-id="17328-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="17328-228">ยอดเงินสุทธิสำหรับใบแจ้งหนี้คือ 200.00</span><span class="sxs-lookup"><span data-stu-id="17328-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="17328-229">ยอดเงินรวมสำหรับใบแจ้งหนี้คือ 200.00 + (8 x 5.00) = 240.00</span><span class="sxs-lookup"><span data-stu-id="17328-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="17328-230">มีการคำนวณภาษีดังต่อไปนี้: ภาษีขายรวม = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 ภาษีรวม = 5.00 x 8 = 40.00 ยอดเงินใบแจ้งหนี้รวม = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="17328-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="17328-231">สำหรับข้อมูลเพิ่มเติม ดูที่ [ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย](whole-amount-interval-options-sales-tax-codes.md) และ [วิธีการคำนวณภาษีขายในฟิลด์จุดเริ่มต้น](sales-tax-calculation-methods-origin-field.md)</span><span class="sxs-lookup"><span data-stu-id="17328-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



