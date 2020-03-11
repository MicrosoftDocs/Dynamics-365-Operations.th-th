---
title: เอนทิตี้ Common Data Service
description: Microsoft Dynamics 365 Human Resources ใช้ Common Data Service เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087357"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="3be34-103">เอนทิตี้ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3be34-103">Common Data Service entities</span></span>

<span data-ttu-id="3be34-104">Microsoft Dynamics 365 Human Resources ใช้ Common Data Service เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม</span><span class="sxs-lookup"><span data-stu-id="3be34-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="3be34-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Common Data Service ให้ดูที่ [อะไรคือ Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="3be34-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="3be34-106">เอนทิตีทรัพยากรต่อไปนี้พร้อมใช้งานใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3be34-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="3be34-107">เอนทิตี้สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-107">Benefit entities</span></span>

| <span data-ttu-id="3be34-108">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-108">Name</span></span> | <span data-ttu-id="3be34-109">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-110">ความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="3be34-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="3be34-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="3be34-112">รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="3be34-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="3be34-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="3be34-114">อัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="3be34-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="3be34-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="3be34-116">รายละเอียดอัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="3be34-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="3be34-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="3be34-118">ตัวเลือกสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-118">Benefit Option</span></span> | <span data-ttu-id="3be34-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="3be34-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="3be34-120">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-120">Benefit Plan</span></span> | <span data-ttu-id="3be34-121">cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="3be34-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="3be34-122">ชนิดของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-122">Benefit Type</span></span> | <span data-ttu-id="3be34-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="3be34-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="3be34-124">เอนทิตีงานของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3be34-124">Business process tasks entities</span></span>

| <span data-ttu-id="3be34-125">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-125">Name</span></span> | <span data-ttu-id="3be34-126">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-127">ปฏิทินกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3be34-127">Business Process Calendar</span></span> | <span data-ttu-id="3be34-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="3be34-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="3be34-129">การกำหนดกลุ่มกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3be34-129">Business Process Group Assignment</span></span> | <span data-ttu-id="3be34-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="3be34-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="3be34-131">กลุ่มงานไลบรารีกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3be34-131">Business Process Library Task Group</span></span> | <span data-ttu-id="3be34-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="3be34-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="3be34-133">ระยะของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3be34-133">Business Process Stage</span></span> | <span data-ttu-id="3be34-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="3be34-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="3be34-135">ส่วนหัวเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="3be34-135">Checklist Template Header</span></span> | <span data-ttu-id="3be34-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="3be34-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="3be34-137">งานเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="3be34-137">Checklist Template Task</span></span> | <span data-ttu-id="3be34-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="3be34-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="3be34-139">เอนทิตีค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-139">Compensation entities</span></span>

| <span data-ttu-id="3be34-140">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-140">Name</span></span> | <span data-ttu-id="3be34-141">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-142">แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="3be34-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="3be34-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="3be34-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="3be34-144">กริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-144">Compensation Grid</span></span> | <span data-ttu-id="3be34-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="3be34-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="3be34-146">ระดับค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-146">Compensation Level</span></span> | <span data-ttu-id="3be34-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="3be34-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="3be34-148">ความถี่ในการจ่ายค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="3be34-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="3be34-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="3be34-150">การตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="3be34-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="3be34-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="3be34-152">รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="3be34-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="3be34-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="3be34-154">ภูมิภาคของค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-154">Compensation Region</span></span> | <span data-ttu-id="3be34-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="3be34-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="3be34-156">โครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-156">Compensation Structure</span></span> | <span data-ttu-id="3be34-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="3be34-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="3be34-158">แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="3be34-158">Compensation Variable Plan</span></span> | <span data-ttu-id="3be34-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="3be34-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="3be34-160">ระดับแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="3be34-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="3be34-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="3be34-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="3be34-162">ชนิดแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="3be34-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="3be34-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="3be34-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="3be34-164">เหตุการณ์ค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="3be34-164">Fixed Compensation Event</span></span> | <span data-ttu-id="3be34-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="3be34-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="3be34-166">กฎสิทธิ์พึงได้</span><span class="sxs-lookup"><span data-stu-id="3be34-166">Vesting Rule</span></span> | <span data-ttu-id="3be34-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="3be34-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="3be34-168">ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="3be34-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="3be34-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="3be34-170">เอนทิตี้องค์กร</span><span class="sxs-lookup"><span data-stu-id="3be34-170">Organization entities</span></span>

| <span data-ttu-id="3be34-171">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-171">Name</span></span> | <span data-ttu-id="3be34-172">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-173">แผนก</span><span class="sxs-lookup"><span data-stu-id="3be34-173">Department</span></span> | <span data-ttu-id="3be34-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="3be34-174">cdm_department</span></span> |
| <span data-ttu-id="3be34-175">การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-175">Employment</span></span> | <span data-ttu-id="3be34-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="3be34-176">cdm_employment</span></span> |
| <span data-ttu-id="3be34-177">บริษัท</span><span class="sxs-lookup"><span data-stu-id="3be34-177">Company</span></span> | <span data-ttu-id="3be34-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="3be34-178">cdm_company</span></span> |
| <span data-ttu-id="3be34-179">หน้าที่</span><span class="sxs-lookup"><span data-stu-id="3be34-179">Job</span></span> | <span data-ttu-id="3be34-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="3be34-180">cdm_job</span></span> |
| <span data-ttu-id="3be34-181">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-181">Job Function</span></span> | <span data-ttu-id="3be34-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="3be34-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="3be34-183">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-183">Job Position</span></span> | <span data-ttu-id="3be34-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="3be34-184">cdm_jobposition</span></span> |
| <span data-ttu-id="3be34-185">ชนิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="3be34-185">Position Type</span></span> | <span data-ttu-id="3be34-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="3be34-186">cdm_positiontype</span></span> |
| <span data-ttu-id="3be34-187">การกำหนดผู้ปฏิบัติงานของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="3be34-187">Position Worker Assignment</span></span> | <span data-ttu-id="3be34-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="3be34-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="3be34-189">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-189">Job Type</span></span> | <span data-ttu-id="3be34-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="3be34-190">cdm_jobtype</span></span> |
| <span data-ttu-id="3be34-191">ภาษา</span><span class="sxs-lookup"><span data-stu-id="3be34-191">Language</span></span> | <span data-ttu-id="3be34-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="3be34-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="3be34-193">เอนทิตี้การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-193">Leave and absence entities</span></span>

| <span data-ttu-id="3be34-194">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-194">Name</span></span> | <span data-ttu-id="3be34-195">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-196">ธุรกรรมการออกจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3be34-196">Leave Bank Transaction</span></span> | <span data-ttu-id="3be34-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="3be34-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="3be34-198">การลงทะเบียนการลางาน</span><span class="sxs-lookup"><span data-stu-id="3be34-198">Leave Enrollment</span></span> | <span data-ttu-id="3be34-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="3be34-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="3be34-200">แผนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="3be34-200">Leave Plan</span></span> | <span data-ttu-id="3be34-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="3be34-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="3be34-202">การขอลา</span><span class="sxs-lookup"><span data-stu-id="3be34-202">Leave Request</span></span> | <span data-ttu-id="3be34-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="3be34-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="3be34-204">รายละเอียดคำขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="3be34-204">Leave Request Detail</span></span> | <span data-ttu-id="3be34-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="3be34-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="3be34-206">ชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="3be34-206">Leave Type</span></span> | <span data-ttu-id="3be34-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="3be34-207">cdm_leavetype</span></span> |
| <span data-ttu-id="3be34-208">รหัสเหตุผลชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="3be34-208">Leave Type Reason Code</span></span> | <span data-ttu-id="3be34-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="3be34-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="3be34-210">เอนทิตี้ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="3be34-210">Payroll entities</span></span>

| <span data-ttu-id="3be34-211">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-211">Name</span></span> | <span data-ttu-id="3be34-212">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-213">รอบการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="3be34-213">Pay Cycle</span></span> | <span data-ttu-id="3be34-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="3be34-214">cdm_paycycle</span></span> |
| <span data-ttu-id="3be34-215">รอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="3be34-215">Pay Period</span></span> | <span data-ttu-id="3be34-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="3be34-216">cdm_payperiod</span></span> |
| <span data-ttu-id="3be34-217">รหัสรายได้ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="3be34-217">Payroll Earning Code</span></span> | <span data-ttu-id="3be34-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="3be34-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="3be34-219">การเบิกจ่ายเงินของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3be34-219">Bank Account Disbursement</span></span> | <span data-ttu-id="3be34-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="3be34-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="3be34-221">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="3be34-221">Tax Region</span></span> | <span data-ttu-id="3be34-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="3be34-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="3be34-223">เอนทิตี้ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-223">Worker entities</span></span>

| <span data-ttu-id="3be34-224">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-224">Name</span></span> | <span data-ttu-id="3be34-225">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-226">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-226">Worker</span></span> | <span data-ttu-id="3be34-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="3be34-227">cdm_worker</span></span> |
| <span data-ttu-id="3be34-228">ที่อยู่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-228">Worker Address</span></span> | <span data-ttu-id="3be34-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="3be34-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="3be34-230">รายละเอียดส่วนตัวของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-230">Worker Personal Detail</span></span> | <span data-ttu-id="3be34-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="3be34-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="3be34-232">หมายเลขรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-232">Worker Person Identification Number</span></span> | <span data-ttu-id="3be34-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="3be34-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="3be34-234">ชนิดรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-234">Worker Person Identification Type</span></span> | <span data-ttu-id="3be34-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="3be34-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="3be34-236">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-236">Work Calendar</span></span> | <span data-ttu-id="3be34-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="3be34-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="3be34-238">วันในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-238">Work Calendar Day</span></span> | <span data-ttu-id="3be34-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="3be34-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="3be34-240">วันหยุดในปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-240">Work Calendar Holiday</span></span> |<span data-ttu-id="3be34-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="3be34-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="3be34-242">รายการวันหยุดในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="3be34-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="3be34-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="3be34-244">ช่วงเวลาในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="3be34-245">cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="3be34-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="3be34-246">บัญชีธนาคารของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-246">Worker Bank Account</span></span> | <span data-ttu-id="3be34-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="3be34-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="3be34-248">เอนทิตีการตั้งค่าของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-248">Worker setup entities</span></span>

| <span data-ttu-id="3be34-249">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-249">Name</span></span> | <span data-ttu-id="3be34-250">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-251">สถานะทหารผ่านศึก</span><span class="sxs-lookup"><span data-stu-id="3be34-251">Veteran Status</span></span> | <span data-ttu-id="3be34-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="3be34-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="3be34-253">เชื้อชาติ</span><span class="sxs-lookup"><span data-stu-id="3be34-253">Ethnic Origin</span></span> | <span data-ttu-id="3be34-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="3be34-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="3be34-255">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="3be34-255">Reason Code</span></span> | <span data-ttu-id="3be34-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="3be34-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="3be34-257">หน่วยงานที่ออกรหัสประจำตัวของบุคคล</span><span class="sxs-lookup"><span data-stu-id="3be34-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="3be34-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="3be34-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="3be34-259">เอนทิตีความสามารถ</span><span class="sxs-lookup"><span data-stu-id="3be34-259">Competency entities</span></span>

| <span data-ttu-id="3be34-260">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="3be34-260">Name</span></span> | <span data-ttu-id="3be34-261">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="3be34-262">ชนิดของทักษะ</span><span class="sxs-lookup"><span data-stu-id="3be34-262">Skill Type</span></span> | <span data-ttu-id="3be34-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="3be34-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="3be34-264">รูปแบบความสัมพันธ์เอนทีตี้</span><span class="sxs-lookup"><span data-stu-id="3be34-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="3be34-265">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-265">Worker</span></span>

![ผู้ปฏิบัติงาน](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="3be34-267">งานและตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-267">Job and Job Position</span></span>

![งานและตำแหน่งงาน](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="3be34-269">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3be34-269">Benefits</span></span>

![สวัสดิการ](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="3be34-271">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="3be34-271">Compensation</span></span>

![ค่าตอบแทน](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="3be34-273">ออก</span><span class="sxs-lookup"><span data-stu-id="3be34-273">Leave</span></span>

![ออก](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="3be34-275">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3be34-275">Work Calendar</span></span>

![ปฏิทินการทำงาน](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="3be34-277">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3be34-277">See also</span></span>

[<span data-ttu-id="3be34-278">เลือกเทคโนโลยีการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3be34-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="3be34-279">ตั้งค่าคอนฟิกการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3be34-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)