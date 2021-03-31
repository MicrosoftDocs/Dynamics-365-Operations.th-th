---
title: ชนิดการลงรายการบัญชีสัญญาเช่า
description: หัวข้อนี้จะอธิบายถึงชนิดการลงรายการบัญชีที่ใช้สำหรับธุรกรรมการเช่าสินทรัพย์
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b7d8c545c1addaa570d54855bbad6c576783007
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229513"
---
# <a name="lease-posting-types"></a><span data-ttu-id="f6615-103">ชนิดการลงรายการบัญชีสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6615-104">หัวข้อนี้จะอธิบายถึงชนิดการลงรายการบัญชีที่ใช้สำหรับธุรกรรมการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f6615-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="f6615-105">สินทรัพย์สัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-105">Lease asset</span></span>

<span data-ttu-id="f6615-106">บัญชีที่สัมพันธ์กับสิทธิ์การใช้สินทรัพย์ (ROU)</span><span class="sxs-lookup"><span data-stu-id="f6615-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="f6615-107">บัญชีนี้จะถูกเดบิตเมื่อมีการรับรู้สัญญาเช่าในครั้งแรกภายใต้มาตรฐานการลงบัญชีสัญญาเช่าใหม่ การเข้ารหัสมาตรฐานทางบัญชี หัวข้อ 842 (ASC 842) และมาตรฐาน Financial Reporting ระหว่างประเทศ 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="f6615-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="f6615-108">สำหรับสัญญาเช่าที่แก้ไข บัญชีนี้อาจถูกเดบิตหรือเครดิต ทั้งนี้ขึ้นอยู่กับว่าการปรับเปลี่ยนจะเพิ่มหรือลดหนี้สินสัญญาเช่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f6615-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="f6615-109">**ตัวอย่างรายการสมุดรายวัน:** การรับรู้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6615-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="f6615-110">**เดบิต:** สินทรัพย์สัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f6615-111">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="f6615-112">หนี้สินสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-112">Lease liability</span></span>

<span data-ttu-id="f6615-113">บัญชีจะเชื่อมโยงกับหนี้สินสัญญาเช่าที่เกิดขึ้นเมื่อมีการชำระเงินที่มีส่วนลดภายใต้การใช้มาตรฐาน IFRS 16 และ ASC 842 ใหม่</span><span class="sxs-lookup"><span data-stu-id="f6615-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="f6615-114">บัญชีนี้จะถูกเครดิตเมื่อมีการรับรู้ในตอนแรกของสัญญาเช่าภายใต้มาตรฐานใหม่</span><span class="sxs-lookup"><span data-stu-id="f6615-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="f6615-115">จะมีการเดบิตสำหรับการชำระเงินค่าเช่าและเครดิตสำหรับดอกเบี้ยค้างรับ</span><span class="sxs-lookup"><span data-stu-id="f6615-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="f6615-116">**ตัวอย่างรายการสมุดรายวัน:** การรับรู้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6615-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="f6615-117">**เดบิต:** สินทรัพย์สัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f6615-118">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="f6615-119">**ตัวอย่างรายการสมุดรายวัน:** ดอกเบี้ยค้างรับ</span><span class="sxs-lookup"><span data-stu-id="f6615-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="f6615-120">**เดบิต:** ดอกเบี้ยจ่าย XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="f6615-121">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="f6615-122">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f6615-123">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f6615-124">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="f6615-125">หนี้สินสัญญาเช่าระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="f6615-125">Short-term lease liability</span></span>

<span data-ttu-id="f6615-126">บัญชีนี้สัมพันธ์กับหนี้สินสัญญาเช่าระยะสั้นเมื่อมีการลงรายการบัญชีสมุดรายวันจัดประเภทของหนี้สินสัญญาเช่าระยะสั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="f6615-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="f6615-127">บัญชีนี้จะถูกเครดิตสำหรับหนี้สินระยะสั้นจากกำหนดการตัดบัญชีในวันสุดท้ายของเดือน</span><span class="sxs-lookup"><span data-stu-id="f6615-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="f6615-128">อย่างไรก็ตาม จำนวนเงินเดียวกันจะถูกเดบิตในวันแรกของเดือนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f6615-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="f6615-129">**รายการสมุดรายวันตัวอย่าง:** จัดประเภทหนี้สินสัญญาเช่าระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="f6615-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="f6615-130">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f6615-131">**เครดิต:** หนี้สินสัญญาเช่าระยะสั้น XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="f6615-132">**เดบิต:** หนี้สินสัญญาเช่าระยะสั้น XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="f6615-133">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="f6615-134">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="f6615-134">Depreciation expense</span></span>

<span data-ttu-id="f6615-135">บัญชีจะเชื่อมโยงกับค่าใช้จ่ายที่เกี่ยวข้องกับค่าเสื่อมราคาของสิทธิ์การใช้สินทรัพย์ภายใต้ IFRS 16, ASC 842 และสัญญาเช่าการเงินภายใต้ IAS 17 และ ASC 840</span><span class="sxs-lookup"><span data-stu-id="f6615-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="f6615-136">บัญชีนี้จะถูกเดบิตเมื่อสินทรัพย์ที่สิทธิ์การใช้สินทรัพย์คิดค่าเสื่อมราคาในแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="f6615-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="f6615-137">**ตัวอย่างรายการสมุดรายวัน:** ค่าเสื่อมราคาค้างรับ</span><span class="sxs-lookup"><span data-stu-id="f6615-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="f6615-138">**เดบิต:** ค่าเสื่อมราคา XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="f6615-139">**เครดิต:**  ค่าเสื่อมราคาสะสม XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="f6615-140">กำไร/ขาดทุนจากการปรับเปลี่ยนสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="f6615-141">บัญชีเชื่อมโยงกับกำไรหรือขาดทุนที่เกิดขึ้นจากการปรับเปลี่ยนสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="f6615-142">กำไรอาจเกิดขึ้นในระหว่างการปรับเปลี่ยนสัญญาเช่าถ้าการปรับเปลี่ยนลดหนี้สินสัญญาเช่าโดยมียอดเงินที่เกินกว่ามูลค่าการถือครองของสิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f6615-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="f6615-143">ตัวอย่างเช่น สัญญาเช่ามีมูลค่าการถือครองปัจจุบันของหนี้สินสัญญาเช่า $150,000 และมูลค่าการถือครองของสิทธิ์การใช้สินทรัพย์ $100,000</span><span class="sxs-lookup"><span data-stu-id="f6615-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="f6615-144">สัญญาเช่าถูกปรับเปลี่ยน และการปรับเปลี่ยนนี้ก่อให้เกิดมูลค่าปัจจุบันใหม่ของการชำระค่าเช่าขั้นต่ำในอนาคต (PVFMLP) ของ $40,000</span><span class="sxs-lookup"><span data-stu-id="f6615-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="f6615-145">ดังนั้น หนี้สินสัญญาเช่าจะถูกเดบิตโดย $110,000 ($150,000 – $40,000)</span><span class="sxs-lookup"><span data-stu-id="f6615-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="f6615-146">เนื่องจากสิทธิ์การใช้สินทรัพย์ $100,000 เท่านั้น การลดลงของ $110,000 จะลดสินทรัพย์เกิน 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="f6615-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="f6615-147">คำแนะนำการบัญชีระบุว่าควรมีการจองส่วนที่เหลือให้กับบัญชีกำไร</span><span class="sxs-lookup"><span data-stu-id="f6615-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="f6615-148">ในกรณีนี้ รายการสมุดรายวันสุดท้ายจะเป็นเดบิตกับคหนี้สินสัญญาเช่า $110,000 เครดิตของสินทรัพย์สัญญาเช่า $100,000 และเครดิตที่บัญชีกำไรสำหรับ $10,000</span><span class="sxs-lookup"><span data-stu-id="f6615-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="f6615-149">**ตัวอย่างรายการสมุดรายวัน:** การปรับเปลี่ยนสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="f6615-150">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f6615-151">**เครดิต:** สินทรัพย์สัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="f6615-152">**เครดิต:** กำไร XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="f6615-153">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="f6615-153">Accumulated depreciation</span></span>

<span data-ttu-id="f6615-154">บัญชีมีการเชื่อมโยงกับบัญชีสินทรัพย์ย้อนหลังของสิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f6615-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="f6615-155">บัญชีนี้จะถูกเครดิต เมื่อมีการลงรายการบัญชีค่าใช้จ่ายของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="f6615-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="f6615-156">**ตัวอย่างรายการสมุดรายวัน:** ค่าเสื่อมราคาค้างรับ</span><span class="sxs-lookup"><span data-stu-id="f6615-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="f6615-157">**เดบิต:** ค่าเสื่อมราคา XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="f6615-158">**เครดิต:** ค่าเสื่อมราคาสะสม XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="f6615-159">กำไรสะสม</span><span class="sxs-lookup"><span data-stu-id="f6615-159">Retained earnings</span></span>

<span data-ttu-id="f6615-160">บัญชีที่สัมพันธ์กับกำไรสะสม</span><span class="sxs-lookup"><span data-stu-id="f6615-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="f6615-161">บัญชีนี้อาจถูกเดบิตหรือเครดิตในรายการสมุดรายวันการปรับปรุงการเปลี่ยนแปลง โดยใช้ตัวเลือกการติดตามย้อนหลังหรือสะสมแบบเต็มวิธี A</span><span class="sxs-lookup"><span data-stu-id="f6615-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="f6615-162">ผลต่างระหว่างสิทธิ์การใช้สินทรัพย์และหนี้สินสัญญาเช่าเริ่มต้นจะถูกจองเพื่อกำไรสะสม</span><span class="sxs-lookup"><span data-stu-id="f6615-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="f6615-163">ในบางกรณี รายได้สะสมอาจได้รับผลกระทบในระหว่างการปรับเปลี่ยนสัญญาเช่า ถ้าการจัดประเภทของสัญญาเช่ามีการเปลี่ยนแปลงจากการเงินไปยังการดำเนินงานเพื่อเขียนสิทธิ์การใช้สินทรัพย์ขึ้นหรือลงเพื่อให้เท่ากับหนี้สินสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="f6615-164">**รายการในสมุดรายวันตัวอย่าง:** การปรับปรุงการเปลี่ยน (ตัวเลือกการติดตามย้อนหลังหรือสะสมแบบเต็มวิธี A)</span><span class="sxs-lookup"><span data-stu-id="f6615-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="f6615-165">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f6615-166">**เครดิต:** สินทรัพย์สัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f6615-167">**เครดิต:** กำไรสะสม XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="f6615-168">การชำระเงินแบบผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6615-168">Variable payment</span></span>

<span data-ttu-id="f6615-169">บัญชีจะเชื่อมโยงกับการชำระค่าเช่าผันแปรซึ่งผลิตโดยการประเมินค่าใหม่ตามดัชนีภายใต้ ASC 842, ASC 840, และสัญญาเช่า IAS 17</span><span class="sxs-lookup"><span data-stu-id="f6615-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="f6615-170">ในกำหนดการชำระค่าเช่า การชำระเงินผันแปรจะรวมอยู่ในคอลัมน์ **การชำระเงินผันแปร**</span><span class="sxs-lookup"><span data-stu-id="f6615-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="f6615-171">บัญชีนี้จะถูกเดบิตเมื่อมีการสร้างใบแจ้งหนี้โดยใช้รายการกำหนดการชำระเงินที่มีการชำระเงินผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6615-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="f6615-172">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f6615-173">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f6615-174">**เดบิต:** การชำระเงินผันแปร XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="f6615-175">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="f6615-176">สินทรัพย์ที่มีค่าเช่ารอตัดบัญชี (หนี้สิน)</span><span class="sxs-lookup"><span data-stu-id="f6615-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="f6615-177">บัญชีจะเชื่อมโยงกับหนี้สินหรือสินทรัพย์ค่าเช่ารอตัดบัญชีซึ่งผลิตโดยสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6615-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="f6615-178">บัญชีนี้จะถูกเดบิตเมื่อมีการลงรายการบัญชีใบแจ้งหนี้สำหรับสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี ถ้ายอดการชำระค่าเช่ามากกว่าค่าใช้จ่ายที่เป็นค่าเช่าแบบเส้นตรงของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="f6615-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="f6615-179">ถ้าการชำระค่าเช่าน้อยกว่าค่าเช่าแบบเส้นตรงของรอบระยะเวลา จะมีการเครดิต</span><span class="sxs-lookup"><span data-stu-id="f6615-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="f6615-180">**รายการสมุดรายวันตัวอย่าง:** การชำระค่าเช่า (สัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี)</span><span class="sxs-lookup"><span data-stu-id="f6615-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="f6615-181">**เดบิต:** ค่าใช้จ่ายสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="f6615-182">**เครดิต:** หนี้สินค่าเช่ารอตัดบัญชี XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="f6615-183">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="f6615-184">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-184">Lease expense</span></span>

<span data-ttu-id="f6615-185">บัญชีจะเชื่อมโยงกับค่าใช้จ่ายสัญญาเช่า ถ้าสัญญาเช่ามีการจัดประเภทเป็นสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6615-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="f6615-186">บัญชีนี้จะถูกเดบิตเมื่อมีการลงรายการบัญชีใบแจ้งหนี้สำหรับสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6615-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="f6615-187">**รายการสมุดรายวันตัวอย่าง:** การชำระค่าเช่า (สัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี)</span><span class="sxs-lookup"><span data-stu-id="f6615-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="f6615-188">**เดบิต:** ค่าใช้จ่ายสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="f6615-189">**เครดิต:** หนี้สินค่าเช่ารอตัดบัญชี XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="f6615-190">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="f6615-191">ค่าใช้จ่ายการด้อยค่าของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f6615-191">Impairment expense</span></span>

<span data-ttu-id="f6615-192">บัญชีจะมีการลงรายการบัญชีเมื่อมีสัญญาเช่ามีความบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="f6615-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="f6615-193">บัญชีนี้จะถูกเดบิต ในขณะที่บัญชีสิทธิ์การใช้สินทรัพย์จะถูกเครดิตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="f6615-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="f6615-194">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f6615-195">**เดบิต:** ค่าใช้จ่ายการด้อยค่าของสินทรัพย์ XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="f6615-196">**เครดิต:** สิทธิ์การใช้สินทรัพย์ XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="f6615-197">การชำระค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-197">Lease payment</span></span>

<span data-ttu-id="f6615-198">บัญชีจะมีการลงรายการบัญชีถ้าพารามิเตอร์ **ชำระให้แก่ผู้จัดจำหน่าย** ปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="f6615-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="f6615-199">บัญชีนี้จะถูกเครดิตแทนที่เจ้าหนี้ของผู้จัดจำหน่ายถ้าพารามิเตอร์ปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="f6615-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="f6615-200">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="f6615-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f6615-201">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f6615-202">**เครดิต:** การชำระค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="f6615-203">การลงรายการบัญชีชนิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f6615-203">Expense type postings</span></span>

<span data-ttu-id="f6615-204">บัญชีที่เลือกสำหรับชนิดค่าใช้จ่ายแต่ละชนิดจะถูกเดบิตเมื่อมีการสร้างการชำระเงินสำหรับชนิดค่าใช้จ่ายนั้น</span><span class="sxs-lookup"><span data-stu-id="f6615-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="f6615-205">ตัวอย่างเช่น บัญชีที่ระบุไว้สำหรับชนิดค่าใช้จ่าย **การประกันภัย** จะถูกเดบิตเมื่อใดก็ตามที่มีการสร้างรายการใบแจ้งหนี้หรือรายการสมุดรายวันการชำระเงินจากกำหนดการค่าใช้จ่ายในการจัดการสินทรัพย์สำหรับค่าใช้จ่ายการประกันภัย</span><span class="sxs-lookup"><span data-stu-id="f6615-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="f6615-206">**ตัวอย่างรายการสมุดรายวัน:** การชำระการประกันภัย</span><span class="sxs-lookup"><span data-stu-id="f6615-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="f6615-207">**เดบิต:** บัญชีชนิดค่าใช้จ่ายของการประกันภัย XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="f6615-208">**เครดิต:** บัญชีตรงข้าม XXX</span><span class="sxs-lookup"><span data-stu-id="f6615-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="f6615-209">บัญชีตรงข้ามถูกเลือกที่ระดับสัญญาเช่าบนบรรทัดสำหรับกำหนดการชำระเงินค่าใช้จ่ายในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f6615-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="f6615-210">บัญชีตรงข้ามนี้สามารถเชื่อมโยงกับผู้จัดจำหน่าย หรือบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="f6615-210">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]