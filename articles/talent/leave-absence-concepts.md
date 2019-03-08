---
title: แนวคิดการลางานและการหยุดงาน
description: หัวข้อนี้อธิบายแนวคิดของการลางานและการขาดงาน และวิธีการกำหนดยอดดุลเวลาหยุดพัก
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306489"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="f7675-103">แนวคิดการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f7675-104">แนวคิดและเงื่อนไขที่กล่าวถึงในหัวข้อนี้จะช่วยให้คุณกำหนดวิธีที่พนักงานได้รับเวลาหยุดพัก และวิธีการที่ยอดดุลของเวลาของพนักงานมีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f7675-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="f7675-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการการขาดงานและการลางาน ดู [การจัดการลางานและการขาดงาน](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview)</span><span class="sxs-lookup"><span data-stu-id="f7675-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="f7675-106">รายละเอียดแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="f7675-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="f7675-107">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f7675-107">Start date</span></span>

<span data-ttu-id="f7675-108">วันที่เริ่มต้นคือ วันที่ที่เริ่มต้นการประมวลผลการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="f7675-109">นอกจากนี้ วันที่เริ่มต้นจะทำหน้าที่เป็นวันที่ครบรอบปีที่จะใช้ในการคำนวณยอดเงินยกไปด้วย</span><span class="sxs-lookup"><span data-stu-id="f7675-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="f7675-110">การรับรู้รายได้รายจ่าย</span><span class="sxs-lookup"><span data-stu-id="f7675-110">Accruals</span></span>

<span data-ttu-id="f7675-111">การรับรู้กำหนดว่าเมื่อใด และบ่อยเพียงใดที่พนักงานจะได้รับเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="f7675-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="f7675-112">มีการกำหนดนโยบายเกี่ยวกับเวลาที่ควรให้การรับรู้และนโยบายเกี่ยวกับการแบ่งตามสัดส่วนในส่วน **การรับรู้** เมื่อตั้งค่าแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="f7675-113">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-113">Accrual frequency</span></span>

<span data-ttu-id="f7675-114">ความถี่ในการรับรู้จะกำหนดความถี่ของการลาที่คงค้างหรือได้รับ</span><span class="sxs-lookup"><span data-stu-id="f7675-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="f7675-115">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7675-115">The following options are available:</span></span>

- <span data-ttu-id="f7675-116">ประจำวัน</span><span class="sxs-lookup"><span data-stu-id="f7675-116">Daily</span></span>
- <span data-ttu-id="f7675-117">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="f7675-117">Weekly</span></span>
- <span data-ttu-id="f7675-118">รายสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="f7675-118">Biweekly</span></span>
- <span data-ttu-id="f7675-119">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-119">Semimonthly</span></span>
- <span data-ttu-id="f7675-120">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-120">Monthly</span></span>
- <span data-ttu-id="f7675-121">รายไตรมาส</span><span class="sxs-lookup"><span data-stu-id="f7675-121">Quarterly</span></span>
- <span data-ttu-id="f7675-122">ปีละสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="f7675-122">Semiannually</span></span>
- <span data-ttu-id="f7675-123">รายปี</span><span class="sxs-lookup"><span data-stu-id="f7675-123">Annually</span></span>
- <span data-ttu-id="f7675-124">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="f7675-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="f7675-125">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-125">Accrual period basis</span></span>

<span data-ttu-id="f7675-126">เกณฑ์ระยะเวลาการยกยอดวันลากำหนดวันที่ที่ใช้ในการคำนวณระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="f7675-127">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7675-127">The following options are available:</span></span>

- <span data-ttu-id="f7675-128">**วันที่เริ่มต้นแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-128">**Plan start date**</span></span>
- <span data-ttu-id="f7675-129">**วันที่เฉพาะของพนักงาน** – เมื่อเลือกตัวเลือกนี้ ค่าจะกำหนดแหล่งที่มาของค่าวันที่เริ่มต้นที่จะใช้ในการคำนวณระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="f7675-130">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7675-130">The following options are available:</span></span>

    - <span data-ttu-id="f7675-131">กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="f7675-131">Custom</span></span>
    - <span data-ttu-id="f7675-132">วันที่ครบรอบปี</span><span class="sxs-lookup"><span data-stu-id="f7675-132">Anniversary date</span></span>
    - <span data-ttu-id="f7675-133">วันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="f7675-133">Original hire date</span></span>
    - <span data-ttu-id="f7675-134">วันที่ของอายุงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-134">Seniority date</span></span>
    - <span data-ttu-id="f7675-135">วันที่เริ่มต้นที่ปรับปรุงของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="f7675-136">วันที่เริ่มต้นของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="f7675-137">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="f7675-137">Accrual award date</span></span>

<span data-ttu-id="f7675-138">วันที่มอบวันลาที่ยกยอดกำหนดว่าเมื่อใดที่พนักงานจะได้รับเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="f7675-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="f7675-139">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7675-139">The following options are available:</span></span>

- <span data-ttu-id="f7675-140">**วันที่สิ้นสุดรอบระยะเวลาการยกยอดวันลา** – พนักงานจะได้รับเวลาหยุดพักในวันสุดท้ายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="f7675-141">ในการรับรู้จำนวนที่ถูกต้อง กระบวนการการยกยอดวันลาต้องรวมรอบระยะเวลาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f7675-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="f7675-142">ตัวอย่างเช่น รอบระยะเวลาการยกยอดวันลาคือ วันที่ 1 มกราคม 2018 ถึง 31 มกราคม 2018</span><span class="sxs-lookup"><span data-stu-id="f7675-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="f7675-143">ในกรณีนี้ สำหรับเดือนมกราคมที่จะถูกรวม การรับรู้ต้องถูกรันสำหรับวันที่ 1 กุมภาพันธ์ 2018</span><span class="sxs-lookup"><span data-stu-id="f7675-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="f7675-144">**วันที่เริ่มต้นรอบระยะเวลาการยกยอดวันลา** – พนักงานจะได้รับเวลาหยุดพักในวันแรกของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="f7675-145">นโยบายการรับรู้ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="f7675-146">นโยบายการรับรู้ในการลงทะเบียนจะกำหนดวิธีการคำนวณการรับรู้ เมื่อมีการลงทะเบียนพนักงานในระหว่างรอบระยะเวลาการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="f7675-147">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7675-147">The following options are available:</span></span>

- <span data-ttu-id="f7675-148">**ตามสัดส่วน** – ช่วงวันที่ระหว่างวันที่เริ่มต้นและวันที่ลงทะเบียน จะถูกใช้เพื่อกำหนดผลต่างในวันต่างๆ</span><span class="sxs-lookup"><span data-stu-id="f7675-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="f7675-149">ผลต่างที่นั้นจะถูกใช้เมื่อมีการประมวลผลการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="f7675-150">**การรับรู้แบบเต็ม** – จำนวนการรับรู้ทั้งหมด ตามระดับ มอบให้ระหว่างการประมวลผลการรับรู้แรก</span><span class="sxs-lookup"><span data-stu-id="f7675-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="f7675-151">**ไม่มีการรับรู้** – ไม่มีการรับรู้ที่มอบให้ จนถึงรอบระยะเวลาการรับรู้ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f7675-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="f7675-152">นโยบายการรับรู้ในการยกเลิกการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="f7675-153">นโยบายการรับรู้ในการยกเลิกการลงทะเบียนจะกำหนดวิธีการคำนวณการรับรู้ เมื่อมีการยกเลิกการลงทะเบียนพนักงานในระหว่างรอบระยะเวลาการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="f7675-154">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7675-154">The following options are available:</span></span>

- <span data-ttu-id="f7675-155">**ตามสัดส่วน** – ช่วงวันที่ระหว่างวันที่เริ่มต้นและวันที่ลงทะเบียน จะถูกใช้เพื่อกำหนดผลต่างในวันต่างๆ</span><span class="sxs-lookup"><span data-stu-id="f7675-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="f7675-156">ผลต่างที่นั้นจะถูกใช้เมื่อมีการประมวลผลการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="f7675-157">**การรับรู้แบบเต็ม** – จำนวนการรับรู้ทั้งหมด ตามระดับ มอบให้ระหว่างการประมวลผลการรับรู้แรก</span><span class="sxs-lookup"><span data-stu-id="f7675-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="f7675-158">**ไม่มีการรับรู้** – ไม่มีการรับรู้ที่มอบให้ จนถึงรอบระยะเวลาการรับรู้ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f7675-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="f7675-159">กำหนดการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-159">Accrual schedule</span></span>

<span data-ttu-id="f7675-160">กำหนดการรับรู้กำหนดวิธีที่พนักงานจะรับรู้เวลาหยุดพัก และจำนวนที่พนักงานที่จะได้รับรู้ และยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="f7675-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="f7675-161">คุณสามารถสร้างระดับเพื่อให้มีการให้เวลาหยุดพักตามระดับต่างๆ</span><span class="sxs-lookup"><span data-stu-id="f7675-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="f7675-162">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-162">Months of service</span></span>

<span data-ttu-id="f7675-163">ค่า **จำนวนเดือนของการทำงาน** กำหนดจำนวนต่ำสุดของเดือนที่พนักงานต้องทำงานเพื่อให้มีสิทธิในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="f7675-164">ถ้าไม่มีค่าต่ำสุดสำหรับพนักงาน ตั้งค่าเป็น **0**</span><span class="sxs-lookup"><span data-stu-id="f7675-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="f7675-165">ชั่วโมงที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-165">Hours worked</span></span>

<span data-ttu-id="f7675-166">ค่า **ชั่วโมงที่ทำงาน** กำหนดจำนวนต่ำสุดของชั่วโมงที่พนักงานต้องทำงานต่อรอบระยะเวลาการรับรู้ เพื่อให้มีสิทธิในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="f7675-167">ถ้าไม่มีค่าต่ำสุดสำหรับพนักงาน ตั้งค่าเป็น **0**</span><span class="sxs-lookup"><span data-stu-id="f7675-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="f7675-168">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-168">Accrual amount</span></span>

<span data-ttu-id="f7675-169">จำนวนในการรับรู้เป็นจำนวนชั่วโมงหรือจำนวนวันที่พนักงานจะรับรู้สำหรับแต่ละรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="f7675-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="f7675-170">รอบระยะเวลาจะขึ้นอยู่กับความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="f7675-171">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f7675-171">Minimum balance</span></span>

<span data-ttu-id="f7675-172">สามารถใช้ค่าลบสำหรับยอดดุลต่ำสุด ถ้าพนักงานสามารถร้องขอการลามากกว่าที่พวกเขามี</span><span class="sxs-lookup"><span data-stu-id="f7675-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="f7675-173">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f7675-173">Maximum carry-forward</span></span>

<span data-ttu-id="f7675-174">กระบวนการรับรู้จะปรับปรุงยอดดุลการลางานที่เกินยอดดุลแบบยอดยกไปในวันครบรอบปีของวันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f7675-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="f7675-175">จำนวนที่จัดสรร</span><span class="sxs-lookup"><span data-stu-id="f7675-175">Grant amount</span></span>

<span data-ttu-id="f7675-176">จำนวนที่จัดสรรเป็นจำนวนชั่วโมงหรือจำนวนวันเริ่มต้นที่พนักงานได้รับ เมื่อพวกเขาลงทะเบียนในแผนการลางานครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="f7675-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="f7675-177">ยอดเงินไม่รับรู้สำหรับแต่ละรอบระยะเวลาการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="f7675-178">การลงทะเบียนและยอดดุล</span><span class="sxs-lookup"><span data-stu-id="f7675-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="f7675-179">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-179">Enrollment date</span></span>

<span data-ttu-id="f7675-180">วันที่ลงทะเบียนกำหนดเวลาที่พนักงานสามารถเริ่มต้นการรับรู้เวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="f7675-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="f7675-181">ตัวอย่างเช่น ถ้ามีการลงทะเบียนพนักงานในแผนวันหยุดพักผ่อนในวันที่ 15 มิถุนายน 2018 เธอไม่สามารถรับรู้เวลาหยุดพักได้ก่อนวันที่ 15 มิถุนายน 2018</span><span class="sxs-lookup"><span data-stu-id="f7675-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="f7675-182">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f7675-182">Current balance</span></span>

<span data-ttu-id="f7675-183">ยอดดุลปัจจุบันจะเป็นจำนวนของการลางานที่พร้อมใช้งานสำหรับคำขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="f7675-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="f7675-184">จำนวนนี้รวมถึงการรับรู้ คำขอที่อนุมัติแล้ว และการปรับปรุงถึงวันที่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f7675-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="f7675-185">ตัวอย่างยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f7675-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="f7675-186">แผนต่อปี</span><span class="sxs-lookup"><span data-stu-id="f7675-186">Annual plan</span></span>

<span data-ttu-id="f7675-187">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-187">**Plan setup**</span></span>

| <span data-ttu-id="f7675-188">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-188">Plan start date</span></span> | <span data-ttu-id="f7675-189">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-189">Enrollment date</span></span> | <span data-ttu-id="f7675-190">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-190">Accrual frequency</span></span> | <span data-ttu-id="f7675-191">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-191">Accrual period basis</span></span> | <span data-ttu-id="f7675-192">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="f7675-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f7675-193">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-193">1/1/2018</span></span>        | <span data-ttu-id="f7675-194">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-194">1/1/2018</span></span>        | <span data-ttu-id="f7675-195">รายปี</span><span class="sxs-lookup"><span data-stu-id="f7675-195">Annual</span></span>            | <span data-ttu-id="f7675-196">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-196">Plan start date</span></span>      | <span data-ttu-id="f7675-197">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-197">End of accrual period</span></span> |

<span data-ttu-id="f7675-198">การรับรู้ถูกประมวลผลในวันที่ 1 มกราคม 2019 (1/1/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="f7675-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f7675-199">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-199">**Results**</span></span>

| <span data-ttu-id="f7675-200">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-200">Accrual amount</span></span> | <span data-ttu-id="f7675-201">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f7675-201">Minimum balance</span></span> | <span data-ttu-id="f7675-202">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f7675-202">Maximum carry-forward</span></span> | <span data-ttu-id="f7675-203">ยอดเงินที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="f7675-203">Request amount</span></span> | <span data-ttu-id="f7675-204">ยอดดุลปัจจุบัน (ณ วันที่ 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="f7675-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="f7675-205">200</span><span class="sxs-lookup"><span data-stu-id="f7675-205">200</span></span>            | <span data-ttu-id="f7675-206">0</span><span class="sxs-lookup"><span data-stu-id="f7675-206">0</span></span>               | <span data-ttu-id="f7675-207">120</span><span class="sxs-lookup"><span data-stu-id="f7675-207">120</span></span>                   | <span data-ttu-id="f7675-208">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="f7675-208">40</span></span>             | <span data-ttu-id="f7675-209">160</span><span class="sxs-lookup"><span data-stu-id="f7675-209">160</span></span>                              |

<span data-ttu-id="f7675-210">ยอดดุลปัจจุบัน (160) =ยอดเงินคงค้าง (200) – ยอดเงินที่ร้องขอ (40)</span><span class="sxs-lookup"><span data-stu-id="f7675-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="f7675-211">แผนรายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-211">Semimonthly plan</span></span>

<span data-ttu-id="f7675-212">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-212">**Plan setup**</span></span>

| <span data-ttu-id="f7675-213">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-213">Plan start date</span></span> | <span data-ttu-id="f7675-214">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-214">Enrollment date</span></span> | <span data-ttu-id="f7675-215">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-215">Accrual frequency</span></span> | <span data-ttu-id="f7675-216">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-216">Accrual period basis</span></span> | <span data-ttu-id="f7675-217">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="f7675-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f7675-218">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-218">1/1/2018</span></span>        | <span data-ttu-id="f7675-219">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-219">2/1/2018</span></span>        | <span data-ttu-id="f7675-220">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-220">Semimonthly</span></span>       | <span data-ttu-id="f7675-221">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-221">Plan start date</span></span>      | <span data-ttu-id="f7675-222">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-222">End of accrual period</span></span> |

<span data-ttu-id="f7675-223">การรับรู้ถูกประมวลผลในวันที่ 1 พฤษภาคม 2018 (5/1/2018) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="f7675-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="f7675-224">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-224">**Results**</span></span>

| <span data-ttu-id="f7675-225">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-225">Accrual amount</span></span> | <span data-ttu-id="f7675-226">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f7675-226">Minimum balance</span></span> | <span data-ttu-id="f7675-227">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f7675-227">Maximum carry-forward</span></span> | <span data-ttu-id="f7675-228">ยอดเงินที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="f7675-228">Request amount</span></span> | <span data-ttu-id="f7675-229">ยอดดุลปัจจุบัน (ณ วันที่ 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="f7675-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="f7675-230">5</span><span class="sxs-lookup"><span data-stu-id="f7675-230">5</span></span>              | <span data-ttu-id="f7675-231">0</span><span class="sxs-lookup"><span data-stu-id="f7675-231">0</span></span>               | <span data-ttu-id="f7675-232">120</span><span class="sxs-lookup"><span data-stu-id="f7675-232">120</span></span>                   | <span data-ttu-id="f7675-233">8</span><span class="sxs-lookup"><span data-stu-id="f7675-233">8</span></span>              | <span data-ttu-id="f7675-234">22</span><span class="sxs-lookup"><span data-stu-id="f7675-234">22</span></span>                               |

<span data-ttu-id="f7675-235">ยอดดุลปัจจุบัน (22) = ยอดเงินคงค้าง (5 × 6) – ยอดเงินที่ร้องขอ (8)</span><span class="sxs-lookup"><span data-stu-id="f7675-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="f7675-236">แผนต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-236">Monthly plan</span></span>

<span data-ttu-id="f7675-237">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-237">**Plan setup**</span></span>

| <span data-ttu-id="f7675-238">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-238">Plan start date</span></span> | <span data-ttu-id="f7675-239">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-239">Enrollment date</span></span> | <span data-ttu-id="f7675-240">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-240">Accrual frequency</span></span> | <span data-ttu-id="f7675-241">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-241">Accrual period basis</span></span> | <span data-ttu-id="f7675-242">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="f7675-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f7675-243">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-243">1/1/2018</span></span>        | <span data-ttu-id="f7675-244">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-244">2/1/2018</span></span>        | <span data-ttu-id="f7675-245">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-245">Semimonthly</span></span>       | <span data-ttu-id="f7675-246">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-246">Plan start date</span></span>      | <span data-ttu-id="f7675-247">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-247">End of accrual period</span></span> |

<span data-ttu-id="f7675-248">การรับรู้ถูกประมวลผลในวันที่ 1 พฤษภาคม 2018 (5/1/2018) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="f7675-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="f7675-249">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-249">**Results**</span></span>

| <span data-ttu-id="f7675-250">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-250">Accrual amount</span></span> | <span data-ttu-id="f7675-251">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f7675-251">Minimum balance</span></span> | <span data-ttu-id="f7675-252">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f7675-252">Maximum carry-forward</span></span> | <span data-ttu-id="f7675-253">ยอดเงินที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="f7675-253">Request amount</span></span> | <span data-ttu-id="f7675-254">ยอดดุลปัจจุบัน (ณ วันที่ 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="f7675-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="f7675-255">5</span><span class="sxs-lookup"><span data-stu-id="f7675-255">5</span></span>              | <span data-ttu-id="f7675-256">0</span><span class="sxs-lookup"><span data-stu-id="f7675-256">0</span></span>               | <span data-ttu-id="f7675-257">120</span><span class="sxs-lookup"><span data-stu-id="f7675-257">120</span></span>                   | <span data-ttu-id="f7675-258">8</span><span class="sxs-lookup"><span data-stu-id="f7675-258">8</span></span>              | <span data-ttu-id="f7675-259">7</span><span class="sxs-lookup"><span data-stu-id="f7675-259">7</span></span>                                |

<span data-ttu-id="f7675-260">ยอดดุลปัจจุบัน (7) = ยอดเงินคงค้าง (5 × 3) – ยอดเงินที่ร้องขอ (8)</span><span class="sxs-lookup"><span data-stu-id="f7675-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="f7675-261">ยอดดุลที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="f7675-261">Forecasted balance</span></span>

<span data-ttu-id="f7675-262">*ยอดดุลที่คาดการณ์* จะเป็นจำนวนของการลางานที่พร้อมใช้งานในวันที่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="f7675-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="f7675-263">การรับรู้และการปรับปรุงแบบยกยอดไปจะถูกคาดการณ์จนถึงวันที่นั้น</span><span class="sxs-lookup"><span data-stu-id="f7675-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="f7675-264">โดยใช้สูตรต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7675-264">The following formula is used:</span></span>

<span data-ttu-id="f7675-265">ยอดดุลที่คาดการณ์ในวันจันทร์ = ยอดดุลปัจจุบัน – การร้องขอ + รายการคงค้าง – การปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="f7675-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="f7675-266">ตัวอย่างของยอดดุลที่คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="f7675-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="f7675-267">แผนต่อปี</span><span class="sxs-lookup"><span data-stu-id="f7675-267">Annual plan</span></span>

<span data-ttu-id="f7675-268">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-268">**Plan setup**</span></span>

| <span data-ttu-id="f7675-269">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-269">Plan start date</span></span> | <span data-ttu-id="f7675-270">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-270">Enrollment date</span></span> | <span data-ttu-id="f7675-271">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-271">Accrual frequency</span></span> | <span data-ttu-id="f7675-272">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-272">Accrual period basis</span></span> | <span data-ttu-id="f7675-273">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="f7675-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f7675-274">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-274">1/1/2018</span></span>        | <span data-ttu-id="f7675-275">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-275">1/1/2018</span></span>        | <span data-ttu-id="f7675-276">รายปี</span><span class="sxs-lookup"><span data-stu-id="f7675-276">Annual</span></span>            | <span data-ttu-id="f7675-277">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-277">Plan start date</span></span>      | <span data-ttu-id="f7675-278">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-278">End of accrual period</span></span> |

<span data-ttu-id="f7675-279">การรับรู้ถูกประมวลผลในวันที่ 15 กุมภาพันธ์ 2019 (2/15/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="f7675-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f7675-280">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-280">**Results**</span></span>

| <span data-ttu-id="f7675-281">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-281">Accrual amount</span></span> | <span data-ttu-id="f7675-282">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f7675-282">Minimum balance</span></span> | <span data-ttu-id="f7675-283">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f7675-283">Maximum carry-forward</span></span> | <span data-ttu-id="f7675-284">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f7675-284">Current balance</span></span> | <span data-ttu-id="f7675-285">ยอดดุลที่คาดการณ์ (ณ วันที่ 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="f7675-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="f7675-286">20</span><span class="sxs-lookup"><span data-stu-id="f7675-286">20</span></span>             | <span data-ttu-id="f7675-287">0</span><span class="sxs-lookup"><span data-stu-id="f7675-287">0</span></span>               | <span data-ttu-id="f7675-288">20</span><span class="sxs-lookup"><span data-stu-id="f7675-288">20</span></span>                    | <span data-ttu-id="f7675-289">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="f7675-289">40</span></span>              | <span data-ttu-id="f7675-290">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="f7675-290">40</span></span>                                   |

<span data-ttu-id="f7675-291">ยอดดุลที่มีการคาดการณ์ (40) = จำนวนวันลาคงค้าง (20) + ยอดดุลปัจจุบัน (40) – การปรับปรุงแบบยกยอดไป (20)</span><span class="sxs-lookup"><span data-stu-id="f7675-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="f7675-292">แผนรายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-292">Semimonthly plan</span></span>

<span data-ttu-id="f7675-293">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-293">**Plan setup**</span></span>

| <span data-ttu-id="f7675-294">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-294">Plan start date</span></span> | <span data-ttu-id="f7675-295">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-295">Enrollment date</span></span> | <span data-ttu-id="f7675-296">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-296">Accrual frequency</span></span> | <span data-ttu-id="f7675-297">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-297">Accrual period basis</span></span> | <span data-ttu-id="f7675-298">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="f7675-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f7675-299">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-299">1/1/2018</span></span>        | <span data-ttu-id="f7675-300">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-300">2/1/2018</span></span>        | <span data-ttu-id="f7675-301">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-301">Semimonthly</span></span>       | <span data-ttu-id="f7675-302">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-302">Plan start date</span></span>      | <span data-ttu-id="f7675-303">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-303">End of accrual period</span></span> |

<span data-ttu-id="f7675-304">การรับรู้ถูกประมวลผลในวันที่ 15 กุมภาพันธ์ 2019 (2/15/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="f7675-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f7675-305">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-305">**Results**</span></span>

| <span data-ttu-id="f7675-306">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-306">Accrual amount</span></span> | <span data-ttu-id="f7675-307">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f7675-307">Minimum balance</span></span> | <span data-ttu-id="f7675-308">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f7675-308">Maximum carry-forward</span></span> | <span data-ttu-id="f7675-309">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f7675-309">Current balance</span></span> | <span data-ttu-id="f7675-310">ยอดดุลที่คาดการณ์ (ณ วันที่ 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="f7675-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="f7675-311">5</span><span class="sxs-lookup"><span data-stu-id="f7675-311">5</span></span>              | <span data-ttu-id="f7675-312">0</span><span class="sxs-lookup"><span data-stu-id="f7675-312">0</span></span>               | <span data-ttu-id="f7675-313">20</span><span class="sxs-lookup"><span data-stu-id="f7675-313">20</span></span>                    | <span data-ttu-id="f7675-314">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="f7675-314">40</span></span>              | <span data-ttu-id="f7675-315">35</span><span class="sxs-lookup"><span data-stu-id="f7675-315">35</span></span>                                   |

<span data-ttu-id="f7675-316">ยอดดุลที่มีการคาดการณ์ (35) = จำนวนวันลาคงค้าง (5 × 3) + ยอดดุลปัจจุบัน (40) – การปรับปรุงแบบยกยอดไป (20)</span><span class="sxs-lookup"><span data-stu-id="f7675-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="f7675-317">แผนต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-317">Monthly plan</span></span>

<span data-ttu-id="f7675-318">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-318">**Plan setup**</span></span>

| <span data-ttu-id="f7675-319">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-319">Plan start date</span></span> | <span data-ttu-id="f7675-320">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-320">Enrollment date</span></span> | <span data-ttu-id="f7675-321">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-321">Accrual frequency</span></span> | <span data-ttu-id="f7675-322">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-322">Accrual period basis</span></span> | <span data-ttu-id="f7675-323">วันที่มอบวันลาที่ยกยอด</span><span class="sxs-lookup"><span data-stu-id="f7675-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="f7675-324">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-324">1/1/2018</span></span>        | <span data-ttu-id="f7675-325">วันที่ 2/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-325">2/1/2018</span></span>        | <span data-ttu-id="f7675-326">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-326">Semimonthly</span></span>       | <span data-ttu-id="f7675-327">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-327">Plan start date</span></span>      | <span data-ttu-id="f7675-328">ช่วงปลายของระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-328">End of accrual period</span></span> |

<span data-ttu-id="f7675-329">การรับรู้ถูกประมวลผลในวันที่ 15 กุมภาพันธ์ 2019 (2/15/2019) เพื่อให้รอบระยะเวลาทั้งหมดนั้นถูกรวม</span><span class="sxs-lookup"><span data-stu-id="f7675-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="f7675-330">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-330">**Results**</span></span>

| <span data-ttu-id="f7675-331">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-331">Accrual amount</span></span> | <span data-ttu-id="f7675-332">ยอดดุลขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f7675-332">Minimum balance</span></span> | <span data-ttu-id="f7675-333">การยกยอดไปสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f7675-333">Maximum carry-forward</span></span> | <span data-ttu-id="f7675-334">ยอดดุลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f7675-334">Current balance</span></span> | <span data-ttu-id="f7675-335">ยอดดุลที่คาดการณ์ (ณ วันที่ 2/15/2019)</span><span class="sxs-lookup"><span data-stu-id="f7675-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="f7675-336">10</span><span class="sxs-lookup"><span data-stu-id="f7675-336">10</span></span>             | <span data-ttu-id="f7675-337">0</span><span class="sxs-lookup"><span data-stu-id="f7675-337">0</span></span>               | <span data-ttu-id="f7675-338">20</span><span class="sxs-lookup"><span data-stu-id="f7675-338">20</span></span>                    | <span data-ttu-id="f7675-339">40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="f7675-339">40</span></span>              | <span data-ttu-id="f7675-340">30</span><span class="sxs-lookup"><span data-stu-id="f7675-340">30</span></span>                                   |

<span data-ttu-id="f7675-341">ยอดดุลที่มีการคาดการณ์ (30) = จำนวนวันลาคงค้าง (10 × 1) + ยอดดุลปัจจุบัน (40) – การปรับปรุงแบบยกยอดไป (20)</span><span class="sxs-lookup"><span data-stu-id="f7675-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="f7675-342">ตัวอย่างของยอดดุลการแบ่งตามสัดส่วน</span><span class="sxs-lookup"><span data-stu-id="f7675-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="f7675-343">แผนต่อเดือนตามสัดส่วน</span><span class="sxs-lookup"><span data-stu-id="f7675-343">Prorated monthly plan</span></span>

<span data-ttu-id="f7675-344">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-344">**Plan setup**</span></span>

| <span data-ttu-id="f7675-345">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-345">Plan start date</span></span> | <span data-ttu-id="f7675-346">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-346">Accrual frequency</span></span> | <span data-ttu-id="f7675-347">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="f7675-348">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-348">1/1/2018</span></span>        | <span data-ttu-id="f7675-349">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-349">Monthly</span></span>           | <span data-ttu-id="f7675-350">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-350">Plan start date</span></span>      |

<span data-ttu-id="f7675-351">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-351">**Results**</span></span>

| <span data-ttu-id="f7675-352">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-352">Employee</span></span>            | <span data-ttu-id="f7675-353">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-353">Months of service</span></span> | <span data-ttu-id="f7675-354">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-354">Enrollment date</span></span> | <span data-ttu-id="f7675-355">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f7675-355">Start date</span></span> | <span data-ttu-id="f7675-356">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-356">Accrual amount</span></span> | <span data-ttu-id="f7675-357">ดำเนินการการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-357">Process accrual</span></span> | <span data-ttu-id="f7675-358">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="f7675-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="f7675-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="f7675-359">Jeannette Nicholson</span></span> | <span data-ttu-id="f7675-360">0.00</span><span class="sxs-lookup"><span data-stu-id="f7675-360">0.00</span></span>              | <span data-ttu-id="f7675-361">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-361">6/1/2018</span></span>        | <span data-ttu-id="f7675-362">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-362">6/1/2018</span></span>   | <span data-ttu-id="f7675-363">1.00</span><span class="sxs-lookup"><span data-stu-id="f7675-363">1.00</span></span>           | <span data-ttu-id="f7675-364">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-364">9/1/2018</span></span>        | <span data-ttu-id="f7675-365">3.00</span><span class="sxs-lookup"><span data-stu-id="f7675-365">3.00</span></span>    |
| <span data-ttu-id="f7675-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="f7675-366">Jay Norman</span></span>          | <span data-ttu-id="f7675-367">0.00</span><span class="sxs-lookup"><span data-stu-id="f7675-367">0.00</span></span>              | <span data-ttu-id="f7675-368">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-368">6/15/2018</span></span>       | <span data-ttu-id="f7675-369">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-369">6/15/2018</span></span>  | <span data-ttu-id="f7675-370">1.00</span><span class="sxs-lookup"><span data-stu-id="f7675-370">1.00</span></span>           | <span data-ttu-id="f7675-371">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-371">9/1/2018</span></span>        | <span data-ttu-id="f7675-372">2.53</span><span class="sxs-lookup"><span data-stu-id="f7675-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="f7675-373">แผนต่อเดือนในการรับรู้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f7675-373">Full accrual monthly plan</span></span>

<span data-ttu-id="f7675-374">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-374">**Plan setup**</span></span>

| <span data-ttu-id="f7675-375">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-375">Plan start date</span></span> | <span data-ttu-id="f7675-376">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-376">Accrual frequency</span></span> | <span data-ttu-id="f7675-377">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="f7675-378">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-378">1/1/2018</span></span>        | <span data-ttu-id="f7675-379">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-379">Monthly</span></span>           | <span data-ttu-id="f7675-380">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-380">Plan start date</span></span>      |

<span data-ttu-id="f7675-381">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-381">**Results**</span></span>

| <span data-ttu-id="f7675-382">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-382">Employee</span></span>            | <span data-ttu-id="f7675-383">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-383">Months of service</span></span> | <span data-ttu-id="f7675-384">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-384">Enrollment date</span></span> | <span data-ttu-id="f7675-385">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f7675-385">Start date</span></span> | <span data-ttu-id="f7675-386">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-386">Accrual amount</span></span> | <span data-ttu-id="f7675-387">ดำเนินการการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-387">Process accrual</span></span> | <span data-ttu-id="f7675-388">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="f7675-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="f7675-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="f7675-389">Jeannette Nicholson</span></span> | <span data-ttu-id="f7675-390">0.00</span><span class="sxs-lookup"><span data-stu-id="f7675-390">0.00</span></span>              | <span data-ttu-id="f7675-391">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-391">6/1/2018</span></span>        | <span data-ttu-id="f7675-392">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-392">6/1/2018</span></span>   | <span data-ttu-id="f7675-393">1.00</span><span class="sxs-lookup"><span data-stu-id="f7675-393">1.00</span></span>           | <span data-ttu-id="f7675-394">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-394">9/1/2018</span></span>        | <span data-ttu-id="f7675-395">3.00</span><span class="sxs-lookup"><span data-stu-id="f7675-395">3.00</span></span>    |
| <span data-ttu-id="f7675-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="f7675-396">Jay Norman</span></span>          | <span data-ttu-id="f7675-397">0.00</span><span class="sxs-lookup"><span data-stu-id="f7675-397">0.00</span></span>              | <span data-ttu-id="f7675-398">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-398">6/15/2018</span></span>       | <span data-ttu-id="f7675-399">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-399">6/15/2018</span></span>  | <span data-ttu-id="f7675-400">1.00</span><span class="sxs-lookup"><span data-stu-id="f7675-400">1.00</span></span>           | <span data-ttu-id="f7675-401">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-401">9/1/2018</span></span>        | <span data-ttu-id="f7675-402">3.00</span><span class="sxs-lookup"><span data-stu-id="f7675-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="f7675-403">ไม่มีแผนต่อเดือนในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-403">No accrual monthly plan</span></span>

<span data-ttu-id="f7675-404">**การตั้งค่าแผน**</span><span class="sxs-lookup"><span data-stu-id="f7675-404">**Plan setup**</span></span>

| <span data-ttu-id="f7675-405">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-405">Plan start date</span></span> | <span data-ttu-id="f7675-406">ความถี่ในการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-406">Accrual frequency</span></span> | <span data-ttu-id="f7675-407">เกณฑ์ระยะเวลาการยกยอดวันลา</span><span class="sxs-lookup"><span data-stu-id="f7675-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="f7675-408">วันที่ 1/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-408">1/1/2018</span></span>        | <span data-ttu-id="f7675-409">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="f7675-409">Monthly</span></span>           | <span data-ttu-id="f7675-410">วันที่เริ่มต้นแผน</span><span class="sxs-lookup"><span data-stu-id="f7675-410">Plan start date</span></span>      |

<span data-ttu-id="f7675-411">**ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="f7675-411">**Results**</span></span>

| <span data-ttu-id="f7675-412">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-412">Employee</span></span>            | <span data-ttu-id="f7675-413">จำนวนเดือนของการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f7675-413">Months of service</span></span> | <span data-ttu-id="f7675-414">วันที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f7675-414">Enrollment date</span></span> | <span data-ttu-id="f7675-415">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f7675-415">Start date</span></span> | <span data-ttu-id="f7675-416">จำนวนวันลาคงค้าง</span><span class="sxs-lookup"><span data-stu-id="f7675-416">Accrual amount</span></span> | <span data-ttu-id="f7675-417">ดำเนินการการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f7675-417">Process accrual</span></span> | <span data-ttu-id="f7675-418">ยอดดุล</span><span class="sxs-lookup"><span data-stu-id="f7675-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="f7675-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="f7675-419">Jeannette Nicholson</span></span> | <span data-ttu-id="f7675-420">0.00</span><span class="sxs-lookup"><span data-stu-id="f7675-420">0.00</span></span>              | <span data-ttu-id="f7675-421">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-421">6/1/2018</span></span>        | <span data-ttu-id="f7675-422">วันที่ 6/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-422">6/1/2018</span></span>   | <span data-ttu-id="f7675-423">1.00</span><span class="sxs-lookup"><span data-stu-id="f7675-423">1.00</span></span>           | <span data-ttu-id="f7675-424">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-424">9/1/2018</span></span>        | <span data-ttu-id="f7675-425">3.00</span><span class="sxs-lookup"><span data-stu-id="f7675-425">3.00</span></span>    |
| <span data-ttu-id="f7675-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="f7675-426">Jay Norman</span></span>          | <span data-ttu-id="f7675-427">0.00</span><span class="sxs-lookup"><span data-stu-id="f7675-427">0.00</span></span>              | <span data-ttu-id="f7675-428">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-428">6/15/2018</span></span>       | <span data-ttu-id="f7675-429">วันที่ 6/15/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-429">6/15/2018</span></span>  | <span data-ttu-id="f7675-430">1.00</span><span class="sxs-lookup"><span data-stu-id="f7675-430">1.00</span></span>           | <span data-ttu-id="f7675-431">วันที่ 9/1/2018</span><span class="sxs-lookup"><span data-stu-id="f7675-431">9/1/2018</span></span>        | <span data-ttu-id="f7675-432">2.00</span><span class="sxs-lookup"><span data-stu-id="f7675-432">2.00</span></span>    |
