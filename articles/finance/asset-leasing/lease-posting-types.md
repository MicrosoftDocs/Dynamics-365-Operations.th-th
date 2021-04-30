---
title: ชนิดการลงรายการบัญชีสัญญาเช่า
description: หัวข้อนี้จะอธิบายถึงชนิดการลงรายการบัญชีที่ใช้สำหรับธุรกรรมการเช่าสินทรัพย์
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881143"
---
# <a name="lease-posting-types"></a><span data-ttu-id="656eb-103">ชนิดการลงรายการบัญชีสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="656eb-104">หัวข้อนี้จะอธิบายถึงชนิดการลงรายการบัญชีที่ใช้สำหรับธุรกรรมการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="656eb-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="656eb-105">สินทรัพย์สัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-105">Lease asset</span></span>

<span data-ttu-id="656eb-106">บัญชีที่สัมพันธ์กับสิทธิ์การใช้สินทรัพย์ (ROU)</span><span class="sxs-lookup"><span data-stu-id="656eb-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="656eb-107">บัญชีนี้จะถูกเดบิตเมื่อมีการรับรู้สัญญาเช่าในครั้งแรกภายใต้มาตรฐานการลงบัญชีสัญญาเช่าใหม่ การเข้ารหัสมาตรฐานทางบัญชี หัวข้อ 842 (ASC 842) และมาตรฐาน Financial Reporting ระหว่างประเทศ 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="656eb-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="656eb-108">สำหรับสัญญาเช่าที่แก้ไข บัญชีนี้อาจถูกเดบิตหรือเครดิต ทั้งนี้ขึ้นอยู่กับว่าการปรับเปลี่ยนจะเพิ่มหรือลดหนี้สินสัญญาเช่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="656eb-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="656eb-109">**ตัวอย่างรายการสมุดรายวัน:** การรับรู้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="656eb-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="656eb-110">**เดบิต:** สินทรัพย์สัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="656eb-111">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="656eb-112">หนี้สินสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-112">Lease liability</span></span>

<span data-ttu-id="656eb-113">บัญชีจะเชื่อมโยงกับหนี้สินสัญญาเช่าที่เกิดขึ้นเมื่อมีการชำระเงินที่มีส่วนลดภายใต้การใช้มาตรฐาน IFRS 16 และ ASC 842 ใหม่</span><span class="sxs-lookup"><span data-stu-id="656eb-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="656eb-114">บัญชีนี้จะถูกเครดิตเมื่อมีการรับรู้ในตอนแรกของสัญญาเช่าภายใต้มาตรฐานใหม่</span><span class="sxs-lookup"><span data-stu-id="656eb-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="656eb-115">จะมีการเดบิตสำหรับการชำระเงินค่าเช่าและเครดิตสำหรับดอกเบี้ยค้างรับ</span><span class="sxs-lookup"><span data-stu-id="656eb-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="656eb-116">**ตัวอย่างรายการสมุดรายวัน:** การรับรู้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="656eb-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="656eb-117">**เดบิต:** สินทรัพย์สัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="656eb-118">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="656eb-119">**ตัวอย่างรายการสมุดรายวัน:** ดอกเบี้ยค้างรับ</span><span class="sxs-lookup"><span data-stu-id="656eb-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="656eb-120">**เดบิต:** ดอกเบี้ยจ่าย XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="656eb-121">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="656eb-122">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="656eb-123">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="656eb-124">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="656eb-125">หนี้สินสัญญาเช่าระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="656eb-125">Short-term lease liability</span></span>

<span data-ttu-id="656eb-126">บัญชีนี้สัมพันธ์กับหนี้สินสัญญาเช่าระยะสั้นเมื่อมีการลงรายการบัญชีสมุดรายวันจัดประเภทของหนี้สินสัญญาเช่าระยะสั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="656eb-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="656eb-127">บัญชีนี้จะถูกเครดิตสำหรับหนี้สินระยะสั้นจากกำหนดการตัดบัญชีในวันสุดท้ายของเดือน</span><span class="sxs-lookup"><span data-stu-id="656eb-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="656eb-128">อย่างไรก็ตาม จำนวนเงินเดียวกันจะถูกเดบิตในวันแรกของเดือนถัดไป</span><span class="sxs-lookup"><span data-stu-id="656eb-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="656eb-129">**รายการสมุดรายวันตัวอย่าง:** จัดประเภทหนี้สินสัญญาเช่าระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="656eb-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="656eb-130">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="656eb-131">**เครดิต:** หนี้สินสัญญาเช่าระยะสั้น XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="656eb-132">**เดบิต:** หนี้สินสัญญาเช่าระยะสั้น XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="656eb-133">**เครดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="656eb-134">ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="656eb-134">Depreciation expense</span></span>

<span data-ttu-id="656eb-135">บัญชีจะเชื่อมโยงกับค่าใช้จ่ายที่เกี่ยวข้องกับค่าเสื่อมราคาของสิทธิ์การใช้สินทรัพย์ภายใต้ IFRS 16, ASC 842 และสัญญาเช่าการเงินภายใต้ IAS 17 และ ASC 840</span><span class="sxs-lookup"><span data-stu-id="656eb-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="656eb-136">บัญชีนี้จะถูกเดบิตเมื่อสินทรัพย์ที่สิทธิ์การใช้สินทรัพย์คิดค่าเสื่อมราคาในแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="656eb-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="656eb-137">**ตัวอย่างรายการสมุดรายวัน:** ค่าเสื่อมราคาค้างรับ</span><span class="sxs-lookup"><span data-stu-id="656eb-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="656eb-138">**เดบิต:** ค่าเสื่อมราคา XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="656eb-139">**เครดิต:**  ค่าเสื่อมราคาสะสม XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="656eb-140">กำไร/ขาดทุนจากการปรับเปลี่ยนสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="656eb-141">บัญชีเชื่อมโยงกับกำไรหรือขาดทุนที่เกิดขึ้นจากการปรับเปลี่ยนสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="656eb-142">กำไรอาจเกิดขึ้นในระหว่างการปรับเปลี่ยนสัญญาเช่าถ้าการปรับเปลี่ยนลดหนี้สินสัญญาเช่าโดยมียอดเงินที่เกินกว่ามูลค่าการถือครองของสิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="656eb-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="656eb-143">ตัวอย่างเช่น สัญญาเช่ามีมูลค่าการถือครองปัจจุบันของหนี้สินสัญญาเช่า $150,000 และมูลค่าการถือครองของสิทธิ์การใช้สินทรัพย์ $100,000</span><span class="sxs-lookup"><span data-stu-id="656eb-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="656eb-144">สัญญาเช่าถูกปรับเปลี่ยน และการปรับเปลี่ยนนี้ก่อให้เกิดมูลค่าปัจจุบันใหม่ของการชำระค่าเช่าขั้นต่ำในอนาคต (PVFMLP) ของ $40,000</span><span class="sxs-lookup"><span data-stu-id="656eb-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="656eb-145">ดังนั้น หนี้สินสัญญาเช่าจะถูกเดบิตโดย $110,000 ($150,000 – $40,000)</span><span class="sxs-lookup"><span data-stu-id="656eb-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="656eb-146">เนื่องจากสิทธิ์การใช้สินทรัพย์ $100,000 เท่านั้น การลดลงของ $110,000 จะลดสินทรัพย์เกิน 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="656eb-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="656eb-147">คำแนะนำการบัญชีระบุว่าควรมีการจองส่วนที่เหลือให้กับบัญชีกำไร</span><span class="sxs-lookup"><span data-stu-id="656eb-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="656eb-148">ในกรณีนี้ รายการสมุดรายวันสุดท้ายจะเป็นเดบิตกับคหนี้สินสัญญาเช่า $110,000 เครดิตของสินทรัพย์สัญญาเช่า $100,000 และเครดิตที่บัญชีกำไรสำหรับ $10,000</span><span class="sxs-lookup"><span data-stu-id="656eb-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="656eb-149">**ตัวอย่างรายการสมุดรายวัน:** การปรับเปลี่ยนสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="656eb-150">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="656eb-151">**เครดิต:** สินทรัพย์สัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="656eb-152">**เครดิต:** กำไร XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="656eb-153">ค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="656eb-153">Accumulated depreciation</span></span>

<span data-ttu-id="656eb-154">บัญชีมีการเชื่อมโยงกับบัญชีสินทรัพย์ย้อนหลังของสิทธิ์การใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="656eb-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="656eb-155">บัญชีนี้จะถูกเครดิต เมื่อมีการลงรายการบัญชีค่าใช้จ่ายของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="656eb-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="656eb-156">**ตัวอย่างรายการสมุดรายวัน:** ค่าเสื่อมราคาค้างรับ</span><span class="sxs-lookup"><span data-stu-id="656eb-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="656eb-157">**เดบิต:** ค่าเสื่อมราคา XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="656eb-158">**เครดิต:** ค่าเสื่อมราคาสะสม XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="656eb-159">การชำระเงินแบบผันแปร</span><span class="sxs-lookup"><span data-stu-id="656eb-159">Variable payment</span></span>

<span data-ttu-id="656eb-160">บัญชีจะเชื่อมโยงกับการชำระค่าเช่าผันแปรซึ่งผลิตโดยการประเมินค่าใหม่ตามดัชนีภายใต้ ASC 842, ASC 840, และสัญญาเช่า IAS 17</span><span class="sxs-lookup"><span data-stu-id="656eb-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="656eb-161">ในกำหนดการชำระค่าเช่า การชำระเงินผันแปรจะรวมอยู่ในคอลัมน์ **การชำระเงินผันแปร**</span><span class="sxs-lookup"><span data-stu-id="656eb-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="656eb-162">บัญชีนี้จะถูกเดบิตเมื่อมีการสร้างใบแจ้งหนี้โดยใช้รายการกำหนดการชำระเงินที่มีการชำระเงินผันแปร</span><span class="sxs-lookup"><span data-stu-id="656eb-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="656eb-163">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="656eb-164">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="656eb-165">**เดบิต:** การชำระเงินผันแปร XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="656eb-166">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="656eb-167">สินทรัพย์ที่มีค่าเช่ารอตัดบัญชี (หนี้สิน)</span><span class="sxs-lookup"><span data-stu-id="656eb-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="656eb-168">บัญชีจะเชื่อมโยงกับหนี้สินหรือสินทรัพย์ค่าเช่ารอตัดบัญชีซึ่งผลิตโดยสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี</span><span class="sxs-lookup"><span data-stu-id="656eb-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="656eb-169">บัญชีนี้จะถูกเดบิตเมื่อมีการลงรายการบัญชีใบแจ้งหนี้สำหรับสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี ถ้ายอดการชำระค่าเช่ามากกว่าค่าใช้จ่ายที่เป็นค่าเช่าแบบเส้นตรงของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="656eb-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="656eb-170">ถ้าการชำระค่าเช่าน้อยกว่าค่าเช่าแบบเส้นตรงของรอบระยะเวลา จะมีการเครดิต</span><span class="sxs-lookup"><span data-stu-id="656eb-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="656eb-171">**รายการสมุดรายวันตัวอย่าง:** การชำระค่าเช่า (สัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี)</span><span class="sxs-lookup"><span data-stu-id="656eb-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="656eb-172">**เดบิต:** ค่าใช้จ่ายสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="656eb-173">**เครดิต:** หนี้สินค่าเช่ารอตัดบัญชี XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="656eb-174">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="656eb-175">ค่าใช้จ่ายของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-175">Lease expense</span></span>

<span data-ttu-id="656eb-176">บัญชีจะเชื่อมโยงกับค่าใช้จ่ายสัญญาเช่า ถ้าสัญญาเช่ามีการจัดประเภทเป็นสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี</span><span class="sxs-lookup"><span data-stu-id="656eb-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="656eb-177">บัญชีนี้จะถูกเดบิตเมื่อมีการลงรายการบัญชีใบแจ้งหนี้สำหรับสัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี</span><span class="sxs-lookup"><span data-stu-id="656eb-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="656eb-178">**รายการสมุดรายวันตัวอย่าง:** การชำระค่าเช่า (สัญญาเช่าการรักษาค่าเช่ารอตัดบัญชี)</span><span class="sxs-lookup"><span data-stu-id="656eb-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="656eb-179">**เดบิต:** ค่าใช้จ่ายสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="656eb-180">**เครดิต:** หนี้สินค่าเช่ารอตัดบัญชี XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="656eb-181">**เครดิต:** เจ้าหนี้ผู้จัดจำหน่าย/การชำระเงินค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="656eb-182">ค่าใช้จ่ายการด้อยค่าของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="656eb-182">Impairment expense</span></span>

<span data-ttu-id="656eb-183">บัญชีจะมีการลงรายการบัญชีเมื่อมีสัญญาเช่ามีความบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="656eb-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="656eb-184">บัญชีนี้จะถูกเดบิต ในขณะที่บัญชีสิทธิ์การใช้สินทรัพย์จะถูกเครดิตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="656eb-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="656eb-185">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="656eb-186">**เดบิต:** ค่าใช้จ่ายการด้อยค่าของสินทรัพย์ XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="656eb-187">**เครดิต:** สิทธิ์การใช้สินทรัพย์ XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="656eb-188">การชำระค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-188">Lease payment</span></span>

<span data-ttu-id="656eb-189">บัญชีจะมีการลงรายการบัญชีถ้าพารามิเตอร์ **ชำระให้แก่ผู้จัดจำหน่าย** ปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="656eb-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="656eb-190">บัญชีนี้จะถูกเครดิตแทนที่เจ้าหนี้ของผู้จัดจำหน่ายถ้าพารามิเตอร์ปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="656eb-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="656eb-191">**ตัวอย่างรายการสมุดรายวัน:** การชำระเงินค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="656eb-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="656eb-192">**เดดิต:** หนี้สินสัญญาเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="656eb-193">**เครดิต:** การชำระค่าเช่า XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="656eb-194">การลงรายการบัญชีชนิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="656eb-194">Expense type postings</span></span>

<span data-ttu-id="656eb-195">บัญชีที่เลือกสำหรับชนิดค่าใช้จ่ายแต่ละชนิดจะถูกเดบิตเมื่อมีการสร้างการชำระเงินสำหรับชนิดค่าใช้จ่ายนั้น</span><span class="sxs-lookup"><span data-stu-id="656eb-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="656eb-196">ตัวอย่างเช่น บัญชีที่ระบุไว้สำหรับชนิดค่าใช้จ่าย **การประกันภัย** จะถูกเดบิตเมื่อใดก็ตามที่มีการสร้างรายการใบแจ้งหนี้หรือรายการสมุดรายวันการชำระเงินจากกำหนดการค่าใช้จ่ายในการจัดการสินทรัพย์สำหรับค่าใช้จ่ายการประกันภัย</span><span class="sxs-lookup"><span data-stu-id="656eb-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="656eb-197">**ตัวอย่างรายการสมุดรายวัน:** การชำระการประกันภัย</span><span class="sxs-lookup"><span data-stu-id="656eb-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="656eb-198">**เดบิต:** บัญชีชนิดค่าใช้จ่ายของการประกันภัย XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="656eb-199">**เครดิต:** บัญชีตรงข้าม XXX</span><span class="sxs-lookup"><span data-stu-id="656eb-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="656eb-200">บัญชีตรงข้ามถูกเลือกที่ระดับสัญญาเช่าบนบรรทัดสำหรับกำหนดการชำระเงินค่าใช้จ่ายในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="656eb-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="656eb-201">บัญชีตรงข้ามนี้สามารถเชื่อมโยงกับผู้จัดจำหน่าย หรือบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="656eb-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
