---
title: ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย
description: บทความนี้อธิบายตัวเลือกสำหรับฟิลด์วิธีการคำนวณรหัสภาษีขายและวิธีคำนวณภาษีขายสำหรับช่วงและจำนวนเต็ม
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb737e6600b1812c44d6101814fc858ac27013e9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834646"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="0da3d-103">ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="0da3d-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="0da3d-104">บทความนี้อธิบายตัวเลือกสำหรับฟิลด์วิธีการคำนวณรหัสภาษีขายและวิธีคำนวณภาษีขายสำหรับช่วงและจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="0da3d-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="0da3d-105">คุณสามารถตั้งค่ารหัสภาษีขายที่จะคำนวณตามยอดเงินทั้งหมดเป็นหรือช่วงยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="0da3d-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="0da3d-106">ในหน้ารหัสภาษีขาย ใช้ฟิลด์วิธีการคำนวณบนแท็บด่วนการคำนวณเพื่อเลือกวิธีการคำนวณรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="0da3d-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="0da3d-107">ยอดเงินทั้งหมด – อัตราภาษีถูกใช้กับยอดเงินที่ต้องเสียภาษีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0da3d-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="0da3d-108">ช่วงเวลา – ยอดเงินที่ต้องเสียภาษีถูกแบ่งออกเป็นส่วนต่าง ๆ ซึ่งอยู่ในช่วงที่มีอัตราภาษีขายเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0da3d-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="0da3d-109">ส่วนของยอดเงินที่อยู่ในช่วงที่ระบุถูกคิดภาษีตามอัตราภาษีสำหรับช่วงดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="0da3d-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="0da3d-110">ภาษีขายคือผลรวมของยอดภาษีซึ่งคำนวณได้สำหรับช่วงยอดเงินแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="0da3d-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="0da3d-111">ตัวเลือกช่วงเวลาจะพร้อมใช้งานเฉพาะเมื่อคุณเลือกรายการในฟิลด์วิธีการคำนวณในพื้นที่ภาษีขายของหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="0da3d-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="0da3d-112">ช่วงถูกตั้งค่าอยู่ในหน้าค่ารหัสภาษีขาย ด้วยการป้อนยอดเงินขีดจำกัดต่ำสุดและสูงสุดต่ออัตราภาษี</span><span class="sxs-lookup"><span data-stu-id="0da3d-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="0da3d-113">สำหรับภาษีที่ถูกคำนวณในยอดเงินที่ต้องเสียภาษีทั้งหมด โดยไม่คำนึงถึงวิธีการคำนวณที่เลือก ช่วงต้องเป็นไปตามกฎต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0da3d-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="0da3d-114">ช่วงแรกต้องมีขีดจำกัดต่ำสุดเท่ากับ 0</span><span class="sxs-lookup"><span data-stu-id="0da3d-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="0da3d-115">ช่วงสุดท้ายต้องมีขีดจำกัดสูงสุดเท่ากับศูนย์ ซึ่งบ่งชี้ถึงที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="0da3d-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="0da3d-116">ขีดจำกัดสูงสุดของช่วงเวลาต้องเป็นขีดจำกัดต่ำสุดของช่วงถัดไป</span><span class="sxs-lookup"><span data-stu-id="0da3d-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="0da3d-117">ถ้ายอดเงินเป็นขีดจำกัดสูงสุดของช่วงก่อนหน้าและขีดจำกัดต่ำสุดของช่วงถัดไป อัตราภาษีขายของช่วงแรกจะใช้กับยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="0da3d-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="0da3d-118">ถ้ายอดเงินอยู่ภายนอกช่วงต่างๆ ที่กำหนดโดยขีดจำกัดสูงสุดและต่ำสุด อัตราภาษีขายเท่ากับ 0 จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="0da3d-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="0da3d-119">ตัวอย่าง:วิธีการยอดเงินทั้งหมดของการคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="0da3d-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="0da3d-120">ในหน้าค่ารหัสภาษีขาย อัตราภาษีขายถูกตั้งค่าในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0da3d-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="0da3d-121">**ขีดจำกัดขั้นต่ำ**</span><span class="sxs-lookup"><span data-stu-id="0da3d-121">**Minimum limit**</span></span> | <span data-ttu-id="0da3d-122">**ขีดจำกัดสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="0da3d-122">**Maximum limit**</span></span> | <span data-ttu-id="0da3d-123">**อัตราภาษี**</span><span class="sxs-lookup"><span data-stu-id="0da3d-123">**Tax rate**</span></span> |
| <span data-ttu-id="0da3d-124">0.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-124">0.00</span></span>              | <span data-ttu-id="0da3d-125">50.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-125">50.00</span></span>             | <span data-ttu-id="0da3d-126">30%</span><span class="sxs-lookup"><span data-stu-id="0da3d-126">30%</span></span>          |
| <span data-ttu-id="0da3d-127">50.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-127">50.00</span></span>             | <span data-ttu-id="0da3d-128">100.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-128">100.00</span></span>            | <span data-ttu-id="0da3d-129">20%</span><span class="sxs-lookup"><span data-stu-id="0da3d-129">20%</span></span>          |
| <span data-ttu-id="0da3d-130">100.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-130">100.00</span></span>            | <span data-ttu-id="0da3d-131">0.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-131">0.00</span></span>              | <span data-ttu-id="0da3d-132">10%</span><span class="sxs-lookup"><span data-stu-id="0da3d-132">10%</span></span>          |

<span data-ttu-id="0da3d-133">ภาษีขายถูกคำนวณจากยอดเงินที่ต้องเสียภาษี</span><span class="sxs-lookup"><span data-stu-id="0da3d-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="0da3d-134">ยอดเงินที่ต้องเสียภาษี (ราคา)</span><span class="sxs-lookup"><span data-stu-id="0da3d-134">Taxable amount (price)</span></span> | <span data-ttu-id="0da3d-135">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="0da3d-135">Calculation</span></span>    | <span data-ttu-id="0da3d-136">ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="0da3d-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="0da3d-137">35.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-137">35.00</span></span>                  | <span data-ttu-id="0da3d-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="0da3d-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="0da3d-139">10.50</span><span class="sxs-lookup"><span data-stu-id="0da3d-139">10.50</span></span>     |
| <span data-ttu-id="0da3d-140">50.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-140">50.00</span></span>                  | <span data-ttu-id="0da3d-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="0da3d-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="0da3d-142">15.00 น.</span><span class="sxs-lookup"><span data-stu-id="0da3d-142">15.00</span></span>     |
| <span data-ttu-id="0da3d-143">85.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-143">85.00</span></span>                  | <span data-ttu-id="0da3d-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="0da3d-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="0da3d-145">17.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-145">17.00</span></span>     |
| <span data-ttu-id="0da3d-146">305.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-146">305.00</span></span>                 | <span data-ttu-id="0da3d-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="0da3d-147">305.00 \* 0.10</span></span> | <span data-ttu-id="0da3d-148">30.50</span><span class="sxs-lookup"><span data-stu-id="0da3d-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="0da3d-149">ตัวอย่าง: วิธีการช่วงของการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="0da3d-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="0da3d-150">ในหน้าค่า อัตราภาษีขายถูกตั้งค่าในช่วงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0da3d-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="0da3d-151">**ขีดจำกัดขั้นต่ำ**</span><span class="sxs-lookup"><span data-stu-id="0da3d-151">**Minimum limit**</span></span> | <span data-ttu-id="0da3d-152">**ขีดจำกัดสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="0da3d-152">**Maximum limit**</span></span> | <span data-ttu-id="0da3d-153">**อัตราภาษี**</span><span class="sxs-lookup"><span data-stu-id="0da3d-153">**Tax rate**</span></span> |
| <span data-ttu-id="0da3d-154">0.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-154">0.00</span></span>              | <span data-ttu-id="0da3d-155">50.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-155">50.00</span></span>             | <span data-ttu-id="0da3d-156">30%</span><span class="sxs-lookup"><span data-stu-id="0da3d-156">30%</span></span>          |
| <span data-ttu-id="0da3d-157">50.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-157">50.00</span></span>             | <span data-ttu-id="0da3d-158">100.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-158">100.00</span></span>            | <span data-ttu-id="0da3d-159">20%</span><span class="sxs-lookup"><span data-stu-id="0da3d-159">20%</span></span>          |
| <span data-ttu-id="0da3d-160">100.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-160">100.00</span></span>            | <span data-ttu-id="0da3d-161">0.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-161">0.00</span></span>              | <span data-ttu-id="0da3d-162">10%</span><span class="sxs-lookup"><span data-stu-id="0da3d-162">10%</span></span>          |

<span data-ttu-id="0da3d-163">ภาษีขายคือผลรวมของยอดภาษีซึ่งคำนวณได้สำหรับช่วงยอดเงินแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="0da3d-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="0da3d-164">ยอดเงินที่ต้องเสียภาษี (ราคา)</span><span class="sxs-lookup"><span data-stu-id="0da3d-164">Taxable amount (price)</span></span> | <span data-ttu-id="0da3d-165">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="0da3d-165">Calculation</span></span>                                                               | <span data-ttu-id="0da3d-166">ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="0da3d-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0da3d-167">35.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-167">35.00</span></span>                  | <span data-ttu-id="0da3d-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="0da3d-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="0da3d-169">10.50</span><span class="sxs-lookup"><span data-stu-id="0da3d-169">10.50</span></span>     |
| <span data-ttu-id="0da3d-170">50.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-170">50.00</span></span>                  | <span data-ttu-id="0da3d-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="0da3d-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="0da3d-172">15.00 น.</span><span class="sxs-lookup"><span data-stu-id="0da3d-172">15.00</span></span>     |
| <span data-ttu-id="0da3d-173">85.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-173">85.00</span></span>                  | <span data-ttu-id="0da3d-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span><span class="sxs-lookup"><span data-stu-id="0da3d-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="0da3d-175">22.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-175">22.00</span></span>     |
| <span data-ttu-id="0da3d-176">305.00</span><span class="sxs-lookup"><span data-stu-id="0da3d-176">305.00</span></span>                 | <span data-ttu-id="0da3d-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span><span class="sxs-lookup"><span data-stu-id="0da3d-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="0da3d-178">45.50</span><span class="sxs-lookup"><span data-stu-id="0da3d-178">45.50</span></span>     |



<span data-ttu-id="0da3d-179">สำหรับข้อมูลเพิ่มเติม ดู [การกำหนดอัตราภาษีขายตามฐานกำไรเบื้องต้นและฟิลด์วิธีการคำนวณ](marginal-base-field.md)</span><span class="sxs-lookup"><span data-stu-id="0da3d-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





