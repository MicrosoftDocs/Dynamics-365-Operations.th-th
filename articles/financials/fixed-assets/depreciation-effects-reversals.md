---
title: "ผลกระทบของค่าเสื่อมราคากับการกลับรายการ"
description: "บทความนี้กล่าวถึงผลกระทบที่เป็นไปได้ของการกลับรายการธุรกรรมสินทรัพย์ถาวร"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7309cb3175f65bc6b806edb875ac9406a8faaf66
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="b3647-103">ผลกระทบของค่าเสื่อมราคากับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b3647-103">Depreciation effects with reversals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b3647-104">บทความนี้กล่าวถึงผลกระทบที่เป็นไปได้ของการกลับรายการธุรกรรมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b3647-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="b3647-105">คุณสามารถกลับรายการธุรกรรมสินทรัพย์ถาวร และธุรกรรมที่เกี่ยวข้องกับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b3647-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="b3647-106">นอกจากนี้คุณยังสามารถยกเลิกธุรกรรมที่กลับรายการได้</span><span class="sxs-lookup"><span data-stu-id="b3647-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="b3647-107">คุณสามารถกลับรายการหรือยกเลิกธุรกรรมที่ไม่ใช่ธุรกรรมล่าสุดที่ลงรายการบัญชีในสมุดบัญชีสำหรับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b3647-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="b3647-108">คุณควรกำหนดก่อนว่ามีธุรกรรมค่าเสื่อมราคาใดจะลงรายการบัญชีหลังจากธุรกรรมที่คุณกลับรายการอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="b3647-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="b3647-109">ทั้งนี้เนื่องจากค่าเสื่อมราคาจะไม่ได้รับการคำนวณใหม่เมื่อคุณกลับรายการธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b3647-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="b3647-110">ดังนั้น ค่าเสื่อมราคาจะมักมีการระบุมากกว่าหรือน้อยกว่าความเป็นจริงภายหลังการกลับรายการ ดังที่แสดงในตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b3647-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="b3647-111">เพื่อให้แน่ใจว่า ค่าเสื่อมราคาถูกต้องเมื่อคุณกลับรายการธุรกรรม อย่าดำเนินการกลับรายการหากคุณได้รับข้อความที่ระบุว่าค่าเสื่อมราคาจะไม่ได้รับการคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="b3647-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="b3647-112">แต่ให้ กลับรายการธุรกรรมค่าเสื่อมราคาที่ได้ลงรายการบัญชีภายหลังธุรกรรมที่คุณพยายามจะกลับรายการก่อน แล้วค่อยดำเนินการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b3647-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="b3647-113">คุณจะไม่ได้รับการเตือนเกี่ยวกับการคำนวณค่าเสื่อมราคาใหม่ และคุณสามารถดำเนินการกลับรายการได้</span><span class="sxs-lookup"><span data-stu-id="b3647-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="b3647-114">ตัวอย่างต่อไปนี้แสดงการคำนวณที่เกิดขึ้นหากคุณเลือกที่จะดำเนินการต่อโดยไม่ใส่ใจข้อความโดยไม่กลับรายการแรกของธุรกรรมค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b3647-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="b3647-115">ตัวอย่าง 1: การระบุค่าเสื่อมราคามากกว่าความเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="b3647-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="b3647-116">สินทรัพย์มีการตั้งค่าให้มีอายุการใช้งาน 5 ปีและค่าเสื่อมราคาแบบเส้นตรง (60 รอบระยะเวลาค่าเสื่อมราคา)</span><span class="sxs-lookup"><span data-stu-id="b3647-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="b3647-117">ในตัวอย่างนี้ การระบุค่าเสื่อมราคามากกว่าความเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="b3647-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="b3647-118">ประวัติธุรกรรมสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b3647-118">Asset transaction history</span></span>

| <span data-ttu-id="b3647-119">วันที่</span><span class="sxs-lookup"><span data-stu-id="b3647-119">Date</span></span>       | <span data-ttu-id="b3647-120">ชนิดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b3647-120">Transaction type</span></span>                                                          | <span data-ttu-id="b3647-121">ยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="b3647-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b3647-122">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-122">January 1</span></span>  | <span data-ttu-id="b3647-123">การซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b3647-123">Acquisition</span></span>                                                               | <span data-ttu-id="b3647-124">59,000.00</span><span class="sxs-lookup"><span data-stu-id="b3647-124">59,000.00</span></span>                                 |
| <span data-ttu-id="b3647-125">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-125">January 1</span></span>  | <span data-ttu-id="b3647-126">การปรับปรุงการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b3647-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="b3647-127">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b3647-127">1,000.00</span></span>                                  |
| <span data-ttu-id="b3647-128">31 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-128">January 31</span></span> | <span data-ttu-id="b3647-129">ค่าเสื่อมราคา (สร้างขึ้นโดยใช้ข้อเสนอสำหรับรอบระยะเวลาหนึ่งของค่าเสื่อมราคา)</span><span class="sxs-lookup"><span data-stu-id="b3647-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="b3647-130">การคำนวณ 1,000.00: มูลค่าตามบัญชี (59,000 + 1,000) / จำนวนของรอบระยะเวลาการคิดค่าเสื่อมราคาที่เหลือ (60)</span><span class="sxs-lookup"><span data-stu-id="b3647-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="b3647-131">การดำเนินการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b3647-131">Reversal action</span></span>

| <span data-ttu-id="b3647-132">วันที่</span><span class="sxs-lookup"><span data-stu-id="b3647-132">Date</span></span>      | <span data-ttu-id="b3647-133">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b3647-133">Transaction type</span></span>                | <span data-ttu-id="b3647-134">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="b3647-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="b3647-135">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-135">January 1</span></span> | <span data-ttu-id="b3647-136">การกลับรายการการปรับปรุงการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b3647-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="b3647-137">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="b3647-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="b3647-138">ผลกระทบของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b3647-138">Depreciation effect</span></span>

| <span data-ttu-id="b3647-139">วันที่</span><span class="sxs-lookup"><span data-stu-id="b3647-139">Date</span></span>        | <span data-ttu-id="b3647-140">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b3647-140">Transaction type</span></span>        | <span data-ttu-id="b3647-141">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="b3647-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3647-142">28 กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="b3647-142">February 28</span></span> | <span data-ttu-id="b3647-143">ค่าเสื่อมราคา (ข้อเสนอ)</span><span class="sxs-lookup"><span data-stu-id="b3647-143">Depreciation (proposal)</span></span> | <span data-ttu-id="b3647-144">การคำนวณ 983.05: มูลค่าตามบัญชี (ค่าเสื่อมราคา 59,000 - 1,000) / จำนวนของรอบระยะเวลาการคิดค่าเสื่อมราคาที่เหลือ (59)</span><span class="sxs-lookup"><span data-stu-id="b3647-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="b3647-145">มีการระบุค่าเสื่อมราคามากกว่าความเป็นจริง 16.95 (1000 - 983.05)</span><span class="sxs-lookup"><span data-stu-id="b3647-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="b3647-146">ตัวอย่าง 2: การระบุค่าเสื่อมราคาน้อยกว่าความเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="b3647-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="b3647-147">สินทรัพย์มีการตั้งค่าให้มีอายุการใช้งาน 5 ปีและค่าเสื่อมราคาแบบเส้นตรง (60 รอบระยะเวลาค่าเสื่อมราคา)</span><span class="sxs-lookup"><span data-stu-id="b3647-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="b3647-148">ในตัวอย่างนี้ การระบุค่าเสื่อมราคาน้อยกว่าความเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="b3647-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="b3647-149">ประวัติธุรกรรมสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b3647-149">Asset transaction history</span></span>

| <span data-ttu-id="b3647-150">วันที่</span><span class="sxs-lookup"><span data-stu-id="b3647-150">Date</span></span>       | <span data-ttu-id="b3647-151">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b3647-151">Transaction type</span></span>                                                          | <span data-ttu-id="b3647-152">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="b3647-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="b3647-153">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-153">January 1</span></span>  | <span data-ttu-id="b3647-154">การซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b3647-154">Acquisition</span></span>                                                               | <span data-ttu-id="b3647-155">59,000.00</span><span class="sxs-lookup"><span data-stu-id="b3647-155">59,000.00</span></span>                                   |
| <span data-ttu-id="b3647-156">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-156">January 1</span></span>  | <span data-ttu-id="b3647-157">การปรับปรุงแบบลดค่า</span><span class="sxs-lookup"><span data-stu-id="b3647-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="b3647-158">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b3647-158">1,000.00</span></span>                                    |
| <span data-ttu-id="b3647-159">31 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-159">January 31</span></span> | <span data-ttu-id="b3647-160">ค่าเสื่อมราคา (สร้างขึ้นโดยใช้ข้อเสนอสำหรับรอบระยะเวลาหนึ่งของค่าเสื่อมราคา)</span><span class="sxs-lookup"><span data-stu-id="b3647-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="b3647-161">การคำนวณ 966.67 : มูลค่าตามบัญชี (59,000 - 1,000) / จำนวนของรอบระยะเวลาการคิดค่าเสื่อมราคาที่เหลือ (60)</span><span class="sxs-lookup"><span data-stu-id="b3647-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="b3647-162">การดำเนินการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b3647-162">Reversal action</span></span>

| <span data-ttu-id="b3647-163">วันที่</span><span class="sxs-lookup"><span data-stu-id="b3647-163">Date</span></span>      | <span data-ttu-id="b3647-164">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b3647-164">Transaction type</span></span>               | <span data-ttu-id="b3647-165">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="b3647-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="b3647-166">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="b3647-166">January 1</span></span> | <span data-ttu-id="b3647-167">การกลับรายการการปรับปรุงแบบลดค่า</span><span class="sxs-lookup"><span data-stu-id="b3647-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="b3647-168">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="b3647-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="b3647-169">ผลกระทบของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b3647-169">Depreciation effect</span></span>

| <span data-ttu-id="b3647-170">วันที่</span><span class="sxs-lookup"><span data-stu-id="b3647-170">Date</span></span>        | <span data-ttu-id="b3647-171">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b3647-171">Transaction type</span></span>        | <span data-ttu-id="b3647-172">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="b3647-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3647-173">28 กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="b3647-173">February 28</span></span> | <span data-ttu-id="b3647-174">ค่าเสื่อมราคา (ข้อเสนอ)</span><span class="sxs-lookup"><span data-stu-id="b3647-174">Depreciation (proposal)</span></span> | <span data-ttu-id="b3647-175">การคำนวณ 983.62: มูลค่าตามบัญชี (ค่าเสื่อมราคา 59,000 - 966.67) / จำนวนของรอบระยะเวลาการคิดค่าเสื่อมราคาที่เหลือ (59)</span><span class="sxs-lookup"><span data-stu-id="b3647-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="b3647-176">มีระบุค่าเสื่อมราคาน้อยกว่าความเป็นจริง 16.95 (983.62 - 966.67)</span><span class="sxs-lookup"><span data-stu-id="b3647-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="see-also"></a><span data-ttu-id="b3647-177">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b3647-177">See also</span></span>
--------

[<span data-ttu-id="b3647-178">ค่าเสื่อมราคาของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b3647-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)




