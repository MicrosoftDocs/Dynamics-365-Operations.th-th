---
title: "ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย"
description: "บทความนี้อธิบายตัวเลือกสำหรับฟิลด์วิธีการคำนวณรหัสภาษีขายและวิธีคำนวณภาษีขายสำหรับช่วงและจำนวนเต็ม"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 647252c7b47ee9c3c6b33b0c1413a1d44ede7c30
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="1ad3c-103">ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="1ad3c-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="1ad3c-104">บทความนี้อธิบายตัวเลือกสำหรับฟิลด์วิธีการคำนวณรหัสภาษีขายและวิธีคำนวณภาษีขายสำหรับช่วงและจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="1ad3c-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="1ad3c-105">คุณสามารถตั้งค่ารหัสภาษีขายที่จะคำนวณตามยอดเงินทั้งหมดเป็นหรือช่วงยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="1ad3c-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="1ad3c-106">ในหน้ารหัสภาษีขาย ใช้ฟิลด์วิธีการคำนวณบนแท็บด่วนการคำนวณเพื่อเลือกวิธีการคำนวณรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="1ad3c-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="1ad3c-107">ยอดเงินทั้งหมด – อัตราภาษีถูกใช้กับยอดเงินที่ต้องเสียภาษีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1ad3c-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="1ad3c-108">ช่วงเวลา – ยอดเงินที่ต้องเสียภาษีถูกแบ่งออกเป็นส่วนต่าง ๆ ซึ่งอยู่ในช่วงที่มีอัตราภาษีขายเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="1ad3c-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="1ad3c-109">ส่วนของยอดเงินที่อยู่ในช่วงที่ระบุถูกคิดภาษีตามอัตราภาษีสำหรับช่วงดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="1ad3c-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="1ad3c-110">ภาษีขายคือผลรวมของยอดภาษีซึ่งคำนวณได้สำหรับช่วงยอดเงินแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="1ad3c-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="1ad3c-111">ตัวเลือกช่วงเวลาจะพร้อมใช้งานเฉพาะเมื่อคุณเลือกรายการในฟิลด์วิธีการคำนวณในพื้นที่ภาษีขายของหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="1ad3c-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="1ad3c-112">ช่วงถูกตั้งค่าอยู่ในหน้าค่ารหัสภาษีขาย ด้วยการป้อนยอดเงินขีดจำกัดต่ำสุดและสูงสุดต่ออัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="1ad3c-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="1ad3c-113">สำหรับภาษีที่ถูกคำนวณในยอดเงินที่ต้องเสียภาษีทั้งหมด โดยไม่คำนึงถึงวิธีการคำนวณที่เลือก ช่วงต้องเป็นไปตามกฎต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1ad3c-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="1ad3c-114">ช่วงแรกต้องมีขีดจำกัดต่ำสุดเท่ากับ 0</span><span class="sxs-lookup"><span data-stu-id="1ad3c-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="1ad3c-115">ช่วงสุดท้ายต้องมีขีดจำกัดสูงสุดเท่ากับศูนย์ ซึ่งบ่งชี้ถึงที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="1ad3c-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="1ad3c-116">ขีดจำกัดสูงสุดของช่วงเวลาต้องเป็นขีดจำกัดต่ำสุดของช่วงถัดไป</span><span class="sxs-lookup"><span data-stu-id="1ad3c-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="1ad3c-117">ถ้ายอดเงินเป็นขีดจำกัดสูงสุดของช่วงก่อนหน้าและขีดจำกัดต่ำสุดของช่วงถัดไป อัตราภาษีขายของช่วงแรกจะใช้กับยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="1ad3c-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="1ad3c-118">ถ้ายอดเงินอยู่ภายนอกช่วงต่างๆ ที่กำหนดโดยขีดจำกัดสูงสุดและต่ำสุด อัตราภาษีขายเท่ากับ 0 จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="1ad3c-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="1ad3c-119">ตัวอย่าง:วิธีการยอดเงินทั้งหมดของการคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="1ad3c-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="1ad3c-120">ในหน้าค่ารหัสภาษีขาย อัตราภาษีขายถูกตั้งค่าในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1ad3c-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="1ad3c-121">**ขีดจำกัดขั้นต่ำ**</span><span class="sxs-lookup"><span data-stu-id="1ad3c-121">**Minimum limit**</span></span> | <span data-ttu-id="1ad3c-122">**ขีดจำกัดสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="1ad3c-122">**Maximum limit**</span></span> | <span data-ttu-id="1ad3c-123">**อัตราภาษี**</span><span class="sxs-lookup"><span data-stu-id="1ad3c-123">**Tax rate**</span></span> |
| <span data-ttu-id="1ad3c-124">0.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-124">0.00</span></span>              | <span data-ttu-id="1ad3c-125">50.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-125">50.00</span></span>             | <span data-ttu-id="1ad3c-126">30%</span><span class="sxs-lookup"><span data-stu-id="1ad3c-126">30%</span></span>          |
| <span data-ttu-id="1ad3c-127">50.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-127">50.00</span></span>             | <span data-ttu-id="1ad3c-128">100.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-128">100.00</span></span>            | <span data-ttu-id="1ad3c-129">20%</span><span class="sxs-lookup"><span data-stu-id="1ad3c-129">20%</span></span>          |
| <span data-ttu-id="1ad3c-130">100.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-130">100.00</span></span>            | <span data-ttu-id="1ad3c-131">0.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-131">0.00</span></span>              | <span data-ttu-id="1ad3c-132">10%</span><span class="sxs-lookup"><span data-stu-id="1ad3c-132">10%</span></span>          |

<span data-ttu-id="1ad3c-133">ภาษีขายถูกคำนวณจากยอดเงินที่ต้องเสียภาษี</span><span class="sxs-lookup"><span data-stu-id="1ad3c-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="1ad3c-134">ยอดเงินที่ต้องเสียภาษี (ราคา)</span><span class="sxs-lookup"><span data-stu-id="1ad3c-134">Taxable amount (price)</span></span> | <span data-ttu-id="1ad3c-135">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1ad3c-135">Calculation</span></span>    | <span data-ttu-id="1ad3c-136">ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="1ad3c-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="1ad3c-137">35.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-137">35.00</span></span>                  | <span data-ttu-id="1ad3c-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="1ad3c-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="1ad3c-139">10.50</span><span class="sxs-lookup"><span data-stu-id="1ad3c-139">10.50</span></span>     |
| <span data-ttu-id="1ad3c-140">50.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-140">50.00</span></span>                  | <span data-ttu-id="1ad3c-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="1ad3c-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="1ad3c-142">15.00 น.</span><span class="sxs-lookup"><span data-stu-id="1ad3c-142">15.00</span></span>     |
| <span data-ttu-id="1ad3c-143">85.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-143">85.00</span></span>                  | <span data-ttu-id="1ad3c-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="1ad3c-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="1ad3c-145">17.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-145">17.00</span></span>     |
| <span data-ttu-id="1ad3c-146">305.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-146">305.00</span></span>                 | <span data-ttu-id="1ad3c-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="1ad3c-147">305.00 \* 0.10</span></span> | <span data-ttu-id="1ad3c-148">30.50</span><span class="sxs-lookup"><span data-stu-id="1ad3c-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="1ad3c-149">ตัวอย่าง: วิธีการช่วงของการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1ad3c-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="1ad3c-150">ในหน้าค่า อัตราภาษีขายถูกตั้งค่าในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1ad3c-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="1ad3c-151">**ขีดจำกัดขั้นต่ำ**</span><span class="sxs-lookup"><span data-stu-id="1ad3c-151">**Minimum limit**</span></span> | <span data-ttu-id="1ad3c-152">**ขีดจำกัดสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="1ad3c-152">**Maximum limit**</span></span> | <span data-ttu-id="1ad3c-153">**อัตราภาษี**</span><span class="sxs-lookup"><span data-stu-id="1ad3c-153">**Tax rate**</span></span> |
| <span data-ttu-id="1ad3c-154">0.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-154">0.00</span></span>              | <span data-ttu-id="1ad3c-155">50.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-155">50.00</span></span>             | <span data-ttu-id="1ad3c-156">30%</span><span class="sxs-lookup"><span data-stu-id="1ad3c-156">30%</span></span>          |
| <span data-ttu-id="1ad3c-157">50.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-157">50.00</span></span>             | <span data-ttu-id="1ad3c-158">100.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-158">100.00</span></span>            | <span data-ttu-id="1ad3c-159">20%</span><span class="sxs-lookup"><span data-stu-id="1ad3c-159">20%</span></span>          |
| <span data-ttu-id="1ad3c-160">100.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-160">100.00</span></span>            | <span data-ttu-id="1ad3c-161">0.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-161">0.00</span></span>              | <span data-ttu-id="1ad3c-162">10%</span><span class="sxs-lookup"><span data-stu-id="1ad3c-162">10%</span></span>          |

<span data-ttu-id="1ad3c-163">ภาษีขายคือผลรวมของยอดภาษีซึ่งคำนวณได้สำหรับช่วงยอดเงินแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="1ad3c-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="1ad3c-164">ยอดเงินที่ต้องเสียภาษี (ราคา)</span><span class="sxs-lookup"><span data-stu-id="1ad3c-164">Taxable amount (price)</span></span> | <span data-ttu-id="1ad3c-165">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1ad3c-165">Calculation</span></span>                                                               | <span data-ttu-id="1ad3c-166">ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="1ad3c-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1ad3c-167">35.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-167">35.00</span></span>                  | <span data-ttu-id="1ad3c-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="1ad3c-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="1ad3c-169">10.50</span><span class="sxs-lookup"><span data-stu-id="1ad3c-169">10.50</span></span>     |
| <span data-ttu-id="1ad3c-170">50.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-170">50.00</span></span>                  | <span data-ttu-id="1ad3c-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="1ad3c-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="1ad3c-172">15.00 น.</span><span class="sxs-lookup"><span data-stu-id="1ad3c-172">15.00</span></span>     |
| <span data-ttu-id="1ad3c-173">85.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-173">85.00</span></span>                  | <span data-ttu-id="1ad3c-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span><span class="sxs-lookup"><span data-stu-id="1ad3c-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="1ad3c-175">22.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-175">22.00</span></span>     |
| <span data-ttu-id="1ad3c-176">305.00</span><span class="sxs-lookup"><span data-stu-id="1ad3c-176">305.00</span></span>                 | <span data-ttu-id="1ad3c-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span><span class="sxs-lookup"><span data-stu-id="1ad3c-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="1ad3c-178">45.50</span><span class="sxs-lookup"><span data-stu-id="1ad3c-178">45.50</span></span>     |



<span data-ttu-id="1ad3c-179">สำหรับข้อมูลเพิ่มเติม ดู [การกำหนดอัตราภาษีขายตามฐานกำไรเบื้องต้นและฟิลด์วิธีการคำนวณ](marginal-base-field.md)</span><span class="sxs-lookup"><span data-stu-id="1ad3c-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






