---
title: แนวคิดการลางานและการหยุดงาน
description: หัวข้อนี้อธิบายแนวคิดของการลางานและการขาดงาน และวิธีการกำหนดยอดดุลเวลาหยุดพัก
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462737"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="70ace-103">แนวคิดการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-103">Leave and absence concepts</span></span>

<span data-ttu-id="70ace-104">แนวคิดและเงื่อนไขที่กล่าวถึงในหัวข้อนี้จะช่วยให้คุณกำหนดวิธีที่พนักงานได้รับเวลาหยุดพัก และวิธีการที่ยอดดุลของเวลาของพนักงานมีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="70ace-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="70ace-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการการขาดงานและการลางาน ดู [การจัดการลางานและการขาดงาน](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview)</span><span class="sxs-lookup"><span data-stu-id="70ace-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="70ace-106">รายละเอียดแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="70ace-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="70ace-107">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="70ace-107">Start date</span></span>

<span data-ttu-id="70ace-108">วันที่เริ่มต้นคือ วันที่ที่เริ่มต้นการประมวลผลการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="70ace-109">นอกจากนี้ วันที่เริ่มต้นจะทำหน้าที่เป็นวันที่ครบรอบปีที่จะใช้ในการคำนวณยอดเงินยกไปด้วย</span><span class="sxs-lookup"><span data-stu-id="70ace-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="70ace-110">การรับรู้รายได้รายจ่าย</span><span class="sxs-lookup"><span data-stu-id="70ace-110">Accruals</span></span>

<span data-ttu-id="70ace-111">การรับรู้กำหนดว่าเมื่อใด และบ่อยเพียงใดที่พนักงานจะได้รับเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="70ace-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="70ace-112">มีการกำหนดนโยบายเกี่ยวกับเวลาที่ควรให้การรับรู้และนโยบายเกี่ยวกับการแบ่งตามสัดส่วนในส่วน **การรับรู้** เมื่อตั้งค่าแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="70ace-113">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-113">Accrual frequency</span></span>

<span data-ttu-id="70ace-114">ความถี่ในการรับรู้จะกำหนดความถี่ของการลาที่คงค้างหรือได้รับ</span><span class="sxs-lookup"><span data-stu-id="70ace-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="70ace-115">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="70ace-115">The following options are available:</span></span>

- <span data-ttu-id="70ace-116">ประจำวัน</span><span class="sxs-lookup"><span data-stu-id="70ace-116">Daily</span></span>
- <span data-ttu-id="70ace-117">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="70ace-117">Weekly</span></span>
- <span data-ttu-id="70ace-118">รายสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="70ace-118">Biweekly</span></span>
- <span data-ttu-id="70ace-119">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-119">Semimonthly</span></span>
- <span data-ttu-id="70ace-120">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-120">Monthly</span></span>
- <span data-ttu-id="70ace-121">รายไตรมาส</span><span class="sxs-lookup"><span data-stu-id="70ace-121">Quarterly</span></span>
- <span data-ttu-id="70ace-122">ปีละสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="70ace-122">Semiannually</span></span>
- <span data-ttu-id="70ace-123">รายปี</span><span class="sxs-lookup"><span data-stu-id="70ace-123">Annually</span></span>
- <span data-ttu-id="70ace-124">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="70ace-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="70ace-125">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-125">Accrual period basis</span></span>

<span data-ttu-id="70ace-126">เกณฑ์ระยะเวลาการยกยอดวันลากำหนดวันที่ที่ใช้ในการคำนวณระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="70ace-127">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="70ace-127">The following options are available:</span></span>

- <span data-ttu-id="70ace-128">**วันที่เริ่มต้นแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-128">**Plan start date**</span></span>
- <span data-ttu-id="70ace-129">**วันที่เฉพาะของพนักงาน** – เมื่อเลือกตัวเลือกนี้ ค่าจะกำหนดแหล่งที่มาของค่าวันที่เริ่มต้นที่จะใช้ในการคำนวณระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="70ace-130">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="70ace-130">The following options are available:</span></span>

    - <span data-ttu-id="70ace-131">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="70ace-131">Custom</span></span>
    - <span data-ttu-id="70ace-132">วันที่ครบรอบปี</span><span class="sxs-lookup"><span data-stu-id="70ace-132">Anniversary date</span></span>
    - <span data-ttu-id="70ace-133">วันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="70ace-133">Original hire date</span></span>
    - <span data-ttu-id="70ace-134">วันที่ของอายุงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-134">Seniority date</span></span>
    - <span data-ttu-id="70ace-135">วันที่เริ่มต้นที่ปรับปรุงของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="70ace-136">วันที่เริ่มต้นของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="70ace-137">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="70ace-137">Accrual award date</span></span>

<span data-ttu-id="70ace-138">วันที่มอบวันลาที่ยกยอดกำหนดว่าเมื่อใดที่พนักงานจะได้รับเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="70ace-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="70ace-139">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="70ace-139">The following options are available:</span></span>

- <span data-ttu-id="70ace-140">**วันที่สิ้นสุดรอบระยะเวลาการยกยอดวันลา** – พนักงานจะได้รับเวลาหยุดพักในวันสุดท้ายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="70ace-141">ในการรับรู้จำนวนที่ถูกต้อง กระบวนการการยกยอดวันลาต้องรวมรอบระยะเวลาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="70ace-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="70ace-142">ตัวอย่างเช่น รอบระยะเวลาการยกยอดวันลาคือ วันที่ 1 มกราคม 2018 ถึง 31 มกราคม 2018</span><span class="sxs-lookup"><span data-stu-id="70ace-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="70ace-143">ในกรณีนี้ สำหรับเดือนมกราคมที่จะถูกรวม การรับรู้ต้องถูกรันสำหรับวันที่ 1 กุมภาพันธ์ 2018</span><span class="sxs-lookup"><span data-stu-id="70ace-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="70ace-144">**วันที่เริ่มต้นรอบระยะเวลาการยกยอดวันลา** – พนักงานจะได้รับเวลาหยุดพักในวันแรกของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="70ace-145">นโยบายการรับรู้ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="70ace-146">นโยบายการรับรู้ในการลงทะเบียนจะกำหนดวิธีการคำนวณการรับรู้ เมื่อมีการลงทะเบียนพนักงานในระหว่างรอบระยะเวลาการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="70ace-147">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="70ace-147">The following options are available:</span></span>

- <span data-ttu-id="70ace-148">**ตามสัดส่วน** – ช่วงวันที่ระหว่างวันที่เริ่มต้นและวันที่ลงทะเบียน จะถูกใช้เพื่อกำหนดผลต่างในวันต่างๆ</span><span class="sxs-lookup"><span data-stu-id="70ace-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="70ace-149">ผลต่างที่นั้นจะถูกใช้เมื่อมีการประมวลผลการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="70ace-150">**การรับรู้แบบเต็ม** – จำนวนการรับรู้ทั้งหมด ตามระดับ มอบให้ระหว่างการประมวลผลการรับรู้แรก</span><span class="sxs-lookup"><span data-stu-id="70ace-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="70ace-151">**ไม่มีการรับรู้** – ไม่มีการรับรู้ที่มอบให้ จนถึงรอบระยะเวลาการรับรู้ถัดไป</span><span class="sxs-lookup"><span data-stu-id="70ace-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="70ace-152">นโยบายการรับรู้ในการยกเลิกการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="70ace-153">นโยบายการรับรู้ในการยกเลิกการลงทะเบียนจะกำหนดวิธีการคำนวณการรับรู้ เมื่อมีการยกเลิกการลงทะเบียนพนักงานในระหว่างรอบระยะเวลาการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="70ace-154">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="70ace-154">The following options are available:</span></span>

- <span data-ttu-id="70ace-155">**ตามสัดส่วน** – ช่วงวันที่ระหว่างวันที่เริ่มต้นและวันที่ลงทะเบียน จะถูกใช้เพื่อกำหนดผลต่างในวันต่างๆ</span><span class="sxs-lookup"><span data-stu-id="70ace-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="70ace-156">ผลต่างที่นั้นจะถูกใช้เมื่อมีการประมวลผลการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="70ace-157">**การรับรู้แบบเต็ม** – จำนวนการรับรู้ทั้งหมด ตามระดับ มอบให้ระหว่างการประมวลผลการรับรู้แรก</span><span class="sxs-lookup"><span data-stu-id="70ace-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="70ace-158">**ไม่มีการรับรู้** – ไม่มีการรับรู้ที่มอบให้ จนถึงรอบระยะเวลาการรับรู้ถัดไป</span><span class="sxs-lookup"><span data-stu-id="70ace-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="70ace-159">กำหนดการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-159">Accrual schedule</span></span>

<span data-ttu-id="70ace-160">กำหนดการรับรู้กำหนดวิธีที่พนักงานจะรับรู้เวลาหยุดพัก และจำนวนที่พนักงานที่จะได้รับรู้ และยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="70ace-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="70ace-161">คุณสามารถสร้างระดับเพื่อให้มีการให้เวลาหยุดพักตามระดับต่างๆ</span><span class="sxs-lookup"><span data-stu-id="70ace-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="70ace-162">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-162">Months of service</span></span>

<span data-ttu-id="70ace-163">ค่า **จำนวนเดือนของการทำงาน** กำหนดจำนวนต่ำสุดของเดือนที่พนักงานต้องทำงานเพื่อให้มีสิทธิในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="70ace-164">ถ้าไม่มีค่าต่ำสุดสำหรับพนักงาน ตั้งค่าเป็น **0**</span><span class="sxs-lookup"><span data-stu-id="70ace-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="70ace-165">ชั่วโมงที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-165">Hours worked</span></span>

<span data-ttu-id="70ace-166">ค่า **ชั่วโมงที่ทำงาน** กำหนดจำนวนต่ำสุดของชั่วโมงที่พนักงานต้องทำงานต่อรอบระยะเวลาการรับรู้ เพื่อให้มีสิทธิในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="70ace-167">ถ้าไม่มีค่าต่ำสุดสำหรับพนักงาน ตั้งค่าเป็น **0**</span><span class="sxs-lookup"><span data-stu-id="70ace-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="70ace-168">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-168">Accrual amount</span></span>

<span data-ttu-id="70ace-169">จำนวนในการรับรู้เป็นจำนวนชั่วโมงหรือจำนวนวันที่พนักงานจะรับรู้สำหรับแต่ละรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="70ace-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="70ace-170">รอบระยะเวลาจะขึ้นอยู่กับความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="70ace-171">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="70ace-171">Minimum balance</span></span>

<span data-ttu-id="70ace-172">สามารถใช้ค่าลบสำหรับยอดดุลต่ำสุด ถ้าพนักงานสามารถร้องขอการลามากกว่าที่พวกเขามี</span><span class="sxs-lookup"><span data-stu-id="70ace-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="70ace-173">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70ace-173">Maximum carry-forward</span></span>

<span data-ttu-id="70ace-174">กระบวนการรับรู้จะปรับปรุงยอดดุลการลางานที่เกินยอดดุลแบบยอดยกไปในวันครบรอบปีของวันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="70ace-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="70ace-175">จำนวนที่จัดสรร</span><span class="sxs-lookup"><span data-stu-id="70ace-175">Grant amount</span></span>

<span data-ttu-id="70ace-176">จำนวนที่จัดสรรเป็นจำนวนชั่วโมงหรือจำนวนวันเริ่มต้นที่พนักงานได้รับ เมื่อพวกเขาลงทะเบียนในแผนการลางานครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="70ace-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="70ace-177">ยอดเงินไม่รับรู้สำหรับแต่ละรอบระยะเวลาการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="70ace-178">การลงทะเบียนและยอดดุล</span><span class="sxs-lookup"><span data-stu-id="70ace-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="70ace-179">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-179">Enrollment date</span></span>

<span data-ttu-id="70ace-180">วันที่ลงทะเบียนกำหนดเวลาที่พนักงานสามารถเริ่มต้นการรับรู้เวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="70ace-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="70ace-181">ตัวอย่างเช่น ถ้ามีการลงทะเบียนพนักงานในแผนวันหยุดพักผ่อนในวันที่ 15 มิถุนายน 2018 เธอไม่สามารถรับรู้เวลาหยุดพักได้ก่อนวันที่ 15 มิถุนายน 2018</span><span class="sxs-lookup"><span data-stu-id="70ace-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="70ace-182">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="70ace-182">Current balance</span></span>

<span data-ttu-id="70ace-183">ยอดดุลปัจจุบันจะเป็นจำนวนของการลางานที่พร้อมใช้งานสำหรับคำขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="70ace-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="70ace-184">จำนวนนี้รวมถึงการรับรู้ คำขอที่อนุมัติแล้ว และการปรับปรุงถึงวันที่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="70ace-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="70ace-185">ตัวอย่างยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="70ace-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="70ace-186">แผนต่อปี</span><span class="sxs-lookup"><span data-stu-id="70ace-186">Annual plan</span></span>

<span data-ttu-id="70ace-187">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-187">**Plan setup**</span></span>

| <span data-ttu-id="70ace-188">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-188">Plan start date</span></span> | <span data-ttu-id="70ace-189">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-189">Enrollment date</span></span> | <span data-ttu-id="70ace-190">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-190">Accrual frequency</span></span> | <span data-ttu-id="70ace-191">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-191">Accrual period basis</span></span> | <span data-ttu-id="70ace-192">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="70ace-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="70ace-193">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-193">1/1/2018</span></span>        | <span data-ttu-id="70ace-194">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-194">1/1/2018</span></span>        | <span data-ttu-id="70ace-195">รายปี</span><span class="sxs-lookup"><span data-stu-id="70ace-195">Annual</span></span>            | <span data-ttu-id="70ace-196">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-196">Plan start date</span></span>      | <span data-ttu-id="70ace-197">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-197">End of accrual period</span></span> |

<span data-ttu-id="70ace-198">การรับรู้ถูกประมวลผลในวันที่ 1 มกราคม 2019 (1/1/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="70ace-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="70ace-199">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-199">**Results**</span></span>

| <span data-ttu-id="70ace-200">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-200">Accrual amount</span></span> | <span data-ttu-id="70ace-201">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="70ace-201">Minimum balance</span></span> | <span data-ttu-id="70ace-202">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70ace-202">Maximum carry-forward</span></span> | <span data-ttu-id="70ace-203">ยอดเงินที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="70ace-203">Request amount</span></span> | <span data-ttu-id="70ace-204">ยอดดุลปัจจุบัน (ณ วันที่ 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="70ace-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="70ace-205">200</span><span class="sxs-lookup"><span data-stu-id="70ace-205">200</span></span>            | <span data-ttu-id="70ace-206">0</span><span class="sxs-lookup"><span data-stu-id="70ace-206">0</span></span>               | <span data-ttu-id="70ace-207">120</span><span class="sxs-lookup"><span data-stu-id="70ace-207">120</span></span>                   | <span data-ttu-id="70ace-208">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="70ace-208">40</span></span>             | <span data-ttu-id="70ace-209">160</span><span class="sxs-lookup"><span data-stu-id="70ace-209">160</span></span>                              |

<span data-ttu-id="70ace-210">ยอดดุลปัจจุบัน (160) =ยอดเงินคงค้าง (200) – ยอดเงินที่ร้องขอ (40)</span><span class="sxs-lookup"><span data-stu-id="70ace-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="70ace-211">แผนรายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-211">Semimonthly plan</span></span>

<span data-ttu-id="70ace-212">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-212">**Plan setup**</span></span>

| <span data-ttu-id="70ace-213">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-213">Plan start date</span></span> | <span data-ttu-id="70ace-214">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-214">Enrollment date</span></span> | <span data-ttu-id="70ace-215">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-215">Accrual frequency</span></span> | <span data-ttu-id="70ace-216">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-216">Accrual period basis</span></span> | <span data-ttu-id="70ace-217">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="70ace-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="70ace-218">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-218">1/1/2018</span></span>        | <span data-ttu-id="70ace-219">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-219">2/1/2018</span></span>        | <span data-ttu-id="70ace-220">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-220">Semimonthly</span></span>       | <span data-ttu-id="70ace-221">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-221">Plan start date</span></span>      | <span data-ttu-id="70ace-222">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-222">End of accrual period</span></span> |

<span data-ttu-id="70ace-223">การรับรู้ถูกประมวลผลในวันที่ 1 พฤษภาคม 2018 (5/1/2018) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="70ace-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="70ace-224">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-224">**Results**</span></span>

| <span data-ttu-id="70ace-225">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-225">Accrual amount</span></span> | <span data-ttu-id="70ace-226">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="70ace-226">Minimum balance</span></span> | <span data-ttu-id="70ace-227">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70ace-227">Maximum carry-forward</span></span> | <span data-ttu-id="70ace-228">ยอดเงินที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="70ace-228">Request amount</span></span> | <span data-ttu-id="70ace-229">ยอดดุลปัจจุบัน (ณ วันที่ 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="70ace-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="70ace-230">5</span><span class="sxs-lookup"><span data-stu-id="70ace-230">5</span></span>              | <span data-ttu-id="70ace-231">0</span><span class="sxs-lookup"><span data-stu-id="70ace-231">0</span></span>               | <span data-ttu-id="70ace-232">120</span><span class="sxs-lookup"><span data-stu-id="70ace-232">120</span></span>                   | <span data-ttu-id="70ace-233">8</span><span class="sxs-lookup"><span data-stu-id="70ace-233">8</span></span>              | <span data-ttu-id="70ace-234">22</span><span class="sxs-lookup"><span data-stu-id="70ace-234">22</span></span>                               |

<span data-ttu-id="70ace-235">ยอดดุลปัจจุบัน (22) = ยอดเงินคงค้าง (5 × 6) – ยอดเงินที่ร้องขอ (8)</span><span class="sxs-lookup"><span data-stu-id="70ace-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="70ace-236">แผนต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-236">Monthly plan</span></span>

<span data-ttu-id="70ace-237">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-237">**Plan setup**</span></span>

| <span data-ttu-id="70ace-238">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-238">Plan start date</span></span> | <span data-ttu-id="70ace-239">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-239">Enrollment date</span></span> | <span data-ttu-id="70ace-240">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-240">Accrual frequency</span></span> | <span data-ttu-id="70ace-241">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-241">Accrual period basis</span></span> | <span data-ttu-id="70ace-242">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="70ace-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="70ace-243">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-243">1/1/2018</span></span>        | <span data-ttu-id="70ace-244">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-244">2/1/2018</span></span>        | <span data-ttu-id="70ace-245">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-245">Semimonthly</span></span>       | <span data-ttu-id="70ace-246">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-246">Plan start date</span></span>      | <span data-ttu-id="70ace-247">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-247">End of accrual period</span></span> |

<span data-ttu-id="70ace-248">การรับรู้ถูกประมวลผลในวันที่ 1 พฤษภาคม 2018 (5/1/2018) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="70ace-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="70ace-249">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-249">**Results**</span></span>

| <span data-ttu-id="70ace-250">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-250">Accrual amount</span></span> | <span data-ttu-id="70ace-251">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="70ace-251">Minimum balance</span></span> | <span data-ttu-id="70ace-252">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70ace-252">Maximum carry-forward</span></span> | <span data-ttu-id="70ace-253">ยอดเงินที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="70ace-253">Request amount</span></span> | <span data-ttu-id="70ace-254">ยอดดุลปัจจุบัน (ณ วันที่ 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="70ace-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="70ace-255">5</span><span class="sxs-lookup"><span data-stu-id="70ace-255">5</span></span>              | <span data-ttu-id="70ace-256">0</span><span class="sxs-lookup"><span data-stu-id="70ace-256">0</span></span>               | <span data-ttu-id="70ace-257">120</span><span class="sxs-lookup"><span data-stu-id="70ace-257">120</span></span>                   | <span data-ttu-id="70ace-258">8</span><span class="sxs-lookup"><span data-stu-id="70ace-258">8</span></span>              | <span data-ttu-id="70ace-259">7</span><span class="sxs-lookup"><span data-stu-id="70ace-259">7</span></span>                                |

<span data-ttu-id="70ace-260">ยอดดุลปัจจุบัน (7) = ยอดเงินคงค้าง (5 × 3) – ยอดเงินที่ร้องขอ (8)</span><span class="sxs-lookup"><span data-stu-id="70ace-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="70ace-261">ยอดดุลที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="70ace-261">Forecasted balance</span></span>

<span data-ttu-id="70ace-262">*ยอดดุลที่คาดการณ์* จะเป็นจำนวนของการลางานที่พร้อมใช้งานในวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="70ace-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="70ace-263">การรับรู้และการปรับปรุงแบบยกยอดไปจะถูกคาดการณ์จนถึงวันที่นั้น</span><span class="sxs-lookup"><span data-stu-id="70ace-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="70ace-264">โดยใช้สูตรต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="70ace-264">The following formula is used:</span></span>

<span data-ttu-id="70ace-265">ยอดดุลที่คาดการณ์ในวันจันทร์ = ยอดดุลปัจจุบัน – การร้องขอ + รายการคงค้าง – การปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="70ace-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="70ace-266">ตัวอย่างของยอดดุลที่คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="70ace-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="70ace-267">แผนต่อปี</span><span class="sxs-lookup"><span data-stu-id="70ace-267">Annual plan</span></span>

<span data-ttu-id="70ace-268">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-268">**Plan setup**</span></span>

| <span data-ttu-id="70ace-269">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-269">Plan start date</span></span> | <span data-ttu-id="70ace-270">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-270">Enrollment date</span></span> | <span data-ttu-id="70ace-271">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-271">Accrual frequency</span></span> | <span data-ttu-id="70ace-272">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-272">Accrual period basis</span></span> | <span data-ttu-id="70ace-273">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="70ace-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="70ace-274">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-274">1/1/2018</span></span>        | <span data-ttu-id="70ace-275">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-275">1/1/2018</span></span>        | <span data-ttu-id="70ace-276">รายปี</span><span class="sxs-lookup"><span data-stu-id="70ace-276">Annual</span></span>            | <span data-ttu-id="70ace-277">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-277">Plan start date</span></span>      | <span data-ttu-id="70ace-278">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-278">End of accrual period</span></span> |

<span data-ttu-id="70ace-279">การรับรู้ถูกประมวลผลในวันที่ 15 กุมภาพันธ์ 2019 (2/15/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="70ace-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="70ace-280">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-280">**Results**</span></span>

| <span data-ttu-id="70ace-281">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-281">Accrual amount</span></span> | <span data-ttu-id="70ace-282">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="70ace-282">Minimum balance</span></span> | <span data-ttu-id="70ace-283">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70ace-283">Maximum carry-forward</span></span> | <span data-ttu-id="70ace-284">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="70ace-284">Current balance</span></span> | <span data-ttu-id="70ace-285">ยอดดุลที่คาดการณ์ (ณ วันที่ 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="70ace-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="70ace-286">20</span><span class="sxs-lookup"><span data-stu-id="70ace-286">20</span></span>             | <span data-ttu-id="70ace-287">0</span><span class="sxs-lookup"><span data-stu-id="70ace-287">0</span></span>               | <span data-ttu-id="70ace-288">20</span><span class="sxs-lookup"><span data-stu-id="70ace-288">20</span></span>                    | <span data-ttu-id="70ace-289">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="70ace-289">40</span></span>              | <span data-ttu-id="70ace-290">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="70ace-290">40</span></span>                                   |

<span data-ttu-id="70ace-291">ยอดดุลที่มีการคาดการณ์ (40) = จำนวนวันลาคงค้าง (20) + ยอดดุลปัจจุบัน (40) – การปรับปรุงแบบยกยอดไป (20)</span><span class="sxs-lookup"><span data-stu-id="70ace-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="70ace-292">แผนรายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-292">Semimonthly plan</span></span>

<span data-ttu-id="70ace-293">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-293">**Plan setup**</span></span>

| <span data-ttu-id="70ace-294">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-294">Plan start date</span></span> | <span data-ttu-id="70ace-295">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-295">Enrollment date</span></span> | <span data-ttu-id="70ace-296">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-296">Accrual frequency</span></span> | <span data-ttu-id="70ace-297">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-297">Accrual period basis</span></span> | <span data-ttu-id="70ace-298">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="70ace-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="70ace-299">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-299">1/1/2018</span></span>        | <span data-ttu-id="70ace-300">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-300">2/1/2018</span></span>        | <span data-ttu-id="70ace-301">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-301">Semimonthly</span></span>       | <span data-ttu-id="70ace-302">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-302">Plan start date</span></span>      | <span data-ttu-id="70ace-303">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-303">End of accrual period</span></span> |

<span data-ttu-id="70ace-304">การรับรู้ถูกประมวลผลในวันที่ 15 กุมภาพันธ์ 2019 (2/15/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="70ace-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="70ace-305">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-305">**Results**</span></span>

| <span data-ttu-id="70ace-306">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-306">Accrual amount</span></span> | <span data-ttu-id="70ace-307">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="70ace-307">Minimum balance</span></span> | <span data-ttu-id="70ace-308">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70ace-308">Maximum carry-forward</span></span> | <span data-ttu-id="70ace-309">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="70ace-309">Current balance</span></span> | <span data-ttu-id="70ace-310">ยอดดุลที่คาดการณ์ (ณ วันที่ 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="70ace-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="70ace-311">5</span><span class="sxs-lookup"><span data-stu-id="70ace-311">5</span></span>              | <span data-ttu-id="70ace-312">0</span><span class="sxs-lookup"><span data-stu-id="70ace-312">0</span></span>               | <span data-ttu-id="70ace-313">20</span><span class="sxs-lookup"><span data-stu-id="70ace-313">20</span></span>                    | <span data-ttu-id="70ace-314">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="70ace-314">40</span></span>              | <span data-ttu-id="70ace-315">35</span><span class="sxs-lookup"><span data-stu-id="70ace-315">35</span></span>                                   |

<span data-ttu-id="70ace-316">ยอดดุลที่มีการคาดการณ์ (35) = จำนวนวันลาคงค้าง (5 × 3) + ยอดดุลปัจจุบัน (40) – การปรับปรุงแบบยกยอดไป (20)</span><span class="sxs-lookup"><span data-stu-id="70ace-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="70ace-317">แผนต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-317">Monthly plan</span></span>

<span data-ttu-id="70ace-318">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-318">**Plan setup**</span></span>

| <span data-ttu-id="70ace-319">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-319">Plan start date</span></span> | <span data-ttu-id="70ace-320">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-320">Enrollment date</span></span> | <span data-ttu-id="70ace-321">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-321">Accrual frequency</span></span> | <span data-ttu-id="70ace-322">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-322">Accrual period basis</span></span> | <span data-ttu-id="70ace-323">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="70ace-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="70ace-324">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-324">1/1/2018</span></span>        | <span data-ttu-id="70ace-325">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-325">2/1/2018</span></span>        | <span data-ttu-id="70ace-326">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-326">Semimonthly</span></span>       | <span data-ttu-id="70ace-327">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-327">Plan start date</span></span>      | <span data-ttu-id="70ace-328">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-328">End of accrual period</span></span> |

<span data-ttu-id="70ace-329">การรับรู้ถูกประมวลผลในวันที่ 15 กุมภาพันธ์ 2019 (2/15/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="70ace-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="70ace-330">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-330">**Results**</span></span>

| <span data-ttu-id="70ace-331">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-331">Accrual amount</span></span> | <span data-ttu-id="70ace-332">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="70ace-332">Minimum balance</span></span> | <span data-ttu-id="70ace-333">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70ace-333">Maximum carry-forward</span></span> | <span data-ttu-id="70ace-334">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="70ace-334">Current balance</span></span> | <span data-ttu-id="70ace-335">ยอดดุลที่คาดการณ์ (ณ วันที่ 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="70ace-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="70ace-336">10</span><span class="sxs-lookup"><span data-stu-id="70ace-336">10</span></span>             | <span data-ttu-id="70ace-337">0</span><span class="sxs-lookup"><span data-stu-id="70ace-337">0</span></span>               | <span data-ttu-id="70ace-338">20</span><span class="sxs-lookup"><span data-stu-id="70ace-338">20</span></span>                    | <span data-ttu-id="70ace-339">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="70ace-339">40</span></span>              | <span data-ttu-id="70ace-340">30</span><span class="sxs-lookup"><span data-stu-id="70ace-340">30</span></span>                                   |

<span data-ttu-id="70ace-341">ยอดดุลที่มีการคาดการณ์ (30) = จำนวนวันลาคงค้าง (10 × 1) + ยอดดุลปัจจุบัน (40) – การปรับปรุงแบบยกยอดไป (20)</span><span class="sxs-lookup"><span data-stu-id="70ace-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="70ace-342">ตัวอย่างของยอดดุลการแบ่งตามสัดส่วน</span><span class="sxs-lookup"><span data-stu-id="70ace-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="70ace-343">แผนต่อเดือนตามสัดส่วน</span><span class="sxs-lookup"><span data-stu-id="70ace-343">Prorated monthly plan</span></span>

<span data-ttu-id="70ace-344">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-344">**Plan setup**</span></span>

| <span data-ttu-id="70ace-345">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-345">Plan start date</span></span> | <span data-ttu-id="70ace-346">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-346">Accrual frequency</span></span> | <span data-ttu-id="70ace-347">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="70ace-348">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-348">1/1/2018</span></span>        | <span data-ttu-id="70ace-349">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-349">Monthly</span></span>           | <span data-ttu-id="70ace-350">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-350">Plan start date</span></span>      |

<span data-ttu-id="70ace-351">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-351">**Results**</span></span>

| <span data-ttu-id="70ace-352">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-352">Employee</span></span>            | <span data-ttu-id="70ace-353">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-353">Months of service</span></span> | <span data-ttu-id="70ace-354">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-354">Enrollment date</span></span> | <span data-ttu-id="70ace-355">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="70ace-355">Start date</span></span> | <span data-ttu-id="70ace-356">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-356">Accrual amount</span></span> | <span data-ttu-id="70ace-357">ดำเนินการการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-357">Process accrual</span></span> | <span data-ttu-id="70ace-358">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="70ace-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="70ace-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="70ace-359">Jeannette Nicholson</span></span> | <span data-ttu-id="70ace-360">0.00</span><span class="sxs-lookup"><span data-stu-id="70ace-360">0.00</span></span>              | <span data-ttu-id="70ace-361">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-361">6/1/2018</span></span>        | <span data-ttu-id="70ace-362">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-362">6/1/2018</span></span>   | <span data-ttu-id="70ace-363">1.00</span><span class="sxs-lookup"><span data-stu-id="70ace-363">1.00</span></span>           | <span data-ttu-id="70ace-364">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-364">9/1/2018</span></span>        | <span data-ttu-id="70ace-365">3.00</span><span class="sxs-lookup"><span data-stu-id="70ace-365">3.00</span></span>    |
| <span data-ttu-id="70ace-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="70ace-366">Jay Norman</span></span>          | <span data-ttu-id="70ace-367">0.00</span><span class="sxs-lookup"><span data-stu-id="70ace-367">0.00</span></span>              | <span data-ttu-id="70ace-368">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-368">6/15/2018</span></span>       | <span data-ttu-id="70ace-369">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-369">6/15/2018</span></span>  | <span data-ttu-id="70ace-370">1.00</span><span class="sxs-lookup"><span data-stu-id="70ace-370">1.00</span></span>           | <span data-ttu-id="70ace-371">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-371">9/1/2018</span></span>        | <span data-ttu-id="70ace-372">2.53</span><span class="sxs-lookup"><span data-stu-id="70ace-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="70ace-373">แผนต่อเดือนในการรับรู้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="70ace-373">Full accrual monthly plan</span></span>

<span data-ttu-id="70ace-374">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-374">**Plan setup**</span></span>

| <span data-ttu-id="70ace-375">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-375">Plan start date</span></span> | <span data-ttu-id="70ace-376">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-376">Accrual frequency</span></span> | <span data-ttu-id="70ace-377">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="70ace-378">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-378">1/1/2018</span></span>        | <span data-ttu-id="70ace-379">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-379">Monthly</span></span>           | <span data-ttu-id="70ace-380">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-380">Plan start date</span></span>      |

<span data-ttu-id="70ace-381">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-381">**Results**</span></span>

| <span data-ttu-id="70ace-382">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-382">Employee</span></span>            | <span data-ttu-id="70ace-383">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-383">Months of service</span></span> | <span data-ttu-id="70ace-384">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-384">Enrollment date</span></span> | <span data-ttu-id="70ace-385">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="70ace-385">Start date</span></span> | <span data-ttu-id="70ace-386">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-386">Accrual amount</span></span> | <span data-ttu-id="70ace-387">ดำเนินการการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-387">Process accrual</span></span> | <span data-ttu-id="70ace-388">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="70ace-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="70ace-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="70ace-389">Jeannette Nicholson</span></span> | <span data-ttu-id="70ace-390">0.00</span><span class="sxs-lookup"><span data-stu-id="70ace-390">0.00</span></span>              | <span data-ttu-id="70ace-391">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-391">6/1/2018</span></span>        | <span data-ttu-id="70ace-392">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-392">6/1/2018</span></span>   | <span data-ttu-id="70ace-393">1.00</span><span class="sxs-lookup"><span data-stu-id="70ace-393">1.00</span></span>           | <span data-ttu-id="70ace-394">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-394">9/1/2018</span></span>        | <span data-ttu-id="70ace-395">3.00</span><span class="sxs-lookup"><span data-stu-id="70ace-395">3.00</span></span>    |
| <span data-ttu-id="70ace-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="70ace-396">Jay Norman</span></span>          | <span data-ttu-id="70ace-397">0.00</span><span class="sxs-lookup"><span data-stu-id="70ace-397">0.00</span></span>              | <span data-ttu-id="70ace-398">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-398">6/15/2018</span></span>       | <span data-ttu-id="70ace-399">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-399">6/15/2018</span></span>  | <span data-ttu-id="70ace-400">1.00</span><span class="sxs-lookup"><span data-stu-id="70ace-400">1.00</span></span>           | <span data-ttu-id="70ace-401">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-401">9/1/2018</span></span>        | <span data-ttu-id="70ace-402">3.00</span><span class="sxs-lookup"><span data-stu-id="70ace-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="70ace-403">ไม่มีแผนต่อเดือนในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-403">No accrual monthly plan</span></span>

<span data-ttu-id="70ace-404">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="70ace-404">**Plan setup**</span></span>

| <span data-ttu-id="70ace-405">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-405">Plan start date</span></span> | <span data-ttu-id="70ace-406">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-406">Accrual frequency</span></span> | <span data-ttu-id="70ace-407">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="70ace-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="70ace-408">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-408">1/1/2018</span></span>        | <span data-ttu-id="70ace-409">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="70ace-409">Monthly</span></span>           | <span data-ttu-id="70ace-410">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="70ace-410">Plan start date</span></span>      |

<span data-ttu-id="70ace-411">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="70ace-411">**Results**</span></span>

| <span data-ttu-id="70ace-412">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-412">Employee</span></span>            | <span data-ttu-id="70ace-413">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="70ace-413">Months of service</span></span> | <span data-ttu-id="70ace-414">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="70ace-414">Enrollment date</span></span> | <span data-ttu-id="70ace-415">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="70ace-415">Start date</span></span> | <span data-ttu-id="70ace-416">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="70ace-416">Accrual amount</span></span> | <span data-ttu-id="70ace-417">ดำเนินการการรับรู้</span><span class="sxs-lookup"><span data-stu-id="70ace-417">Process accrual</span></span> | <span data-ttu-id="70ace-418">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="70ace-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="70ace-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="70ace-419">Jeannette Nicholson</span></span> | <span data-ttu-id="70ace-420">0.00</span><span class="sxs-lookup"><span data-stu-id="70ace-420">0.00</span></span>              | <span data-ttu-id="70ace-421">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-421">6/1/2018</span></span>        | <span data-ttu-id="70ace-422">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-422">6/1/2018</span></span>   | <span data-ttu-id="70ace-423">1.00</span><span class="sxs-lookup"><span data-stu-id="70ace-423">1.00</span></span>           | <span data-ttu-id="70ace-424">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-424">9/1/2018</span></span>        | <span data-ttu-id="70ace-425">3.00</span><span class="sxs-lookup"><span data-stu-id="70ace-425">3.00</span></span>    |
| <span data-ttu-id="70ace-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="70ace-426">Jay Norman</span></span>          | <span data-ttu-id="70ace-427">0.00</span><span class="sxs-lookup"><span data-stu-id="70ace-427">0.00</span></span>              | <span data-ttu-id="70ace-428">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-428">6/15/2018</span></span>       | <span data-ttu-id="70ace-429">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-429">6/15/2018</span></span>  | <span data-ttu-id="70ace-430">1.00</span><span class="sxs-lookup"><span data-stu-id="70ace-430">1.00</span></span>           | <span data-ttu-id="70ace-431">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="70ace-431">9/1/2018</span></span>        | <span data-ttu-id="70ace-432">2.00</span><span class="sxs-lookup"><span data-stu-id="70ace-432">2.00</span></span>    |
