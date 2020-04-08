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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166509"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="c39d3-103">เอนทิตี้ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c39d3-103">Common Data Service entities</span></span>

<span data-ttu-id="c39d3-104">Microsoft Dynamics 365 Human Resources ใช้ Common Data Service เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม</span><span class="sxs-lookup"><span data-stu-id="c39d3-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="c39d3-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Common Data Service ให้ดูที่ [อะไรคือ Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="c39d3-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="c39d3-106">เอนทิตีทรัพยากรต่อไปนี้พร้อมใช้งานใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c39d3-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="c39d3-107">เอนทิตี้สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-107">Benefit entities</span></span>

| <span data-ttu-id="c39d3-108">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-108">Name</span></span> | <span data-ttu-id="c39d3-109">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-110">ความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="c39d3-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="c39d3-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="c39d3-112">รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="c39d3-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="c39d3-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="c39d3-114">อัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="c39d3-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="c39d3-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="c39d3-116">รายละเอียดอัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="c39d3-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="c39d3-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="c39d3-118">ตัวเลือกสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-118">Benefit Option</span></span> | <span data-ttu-id="c39d3-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="c39d3-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="c39d3-120">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-120">Benefit Plan</span></span> | <span data-ttu-id="c39d3-121">cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="c39d3-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="c39d3-122">ชนิดของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-122">Benefit Type</span></span> | <span data-ttu-id="c39d3-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="c39d3-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="c39d3-124">เอนทิตีงานของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c39d3-124">Business process tasks entities</span></span>

| <span data-ttu-id="c39d3-125">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-125">Name</span></span> | <span data-ttu-id="c39d3-126">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-127">ปฏิทินกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c39d3-127">Business Process Calendar</span></span> | <span data-ttu-id="c39d3-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="c39d3-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="c39d3-129">การกำหนดกลุ่มกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c39d3-129">Business Process Group Assignment</span></span> | <span data-ttu-id="c39d3-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="c39d3-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="c39d3-131">กลุ่มงานไลบรารีกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c39d3-131">Business Process Library Task Group</span></span> | <span data-ttu-id="c39d3-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="c39d3-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="c39d3-133">ระยะของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c39d3-133">Business Process Stage</span></span> | <span data-ttu-id="c39d3-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="c39d3-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="c39d3-135">ส่วนหัวเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="c39d3-135">Checklist Template Header</span></span> | <span data-ttu-id="c39d3-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="c39d3-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="c39d3-137">งานเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="c39d3-137">Checklist Template Task</span></span> | <span data-ttu-id="c39d3-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="c39d3-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="c39d3-139">เอนทิตีค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-139">Compensation entities</span></span>

| <span data-ttu-id="c39d3-140">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-140">Name</span></span> | <span data-ttu-id="c39d3-141">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-142">แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="c39d3-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="c39d3-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="c39d3-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="c39d3-144">กริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-144">Compensation Grid</span></span> | <span data-ttu-id="c39d3-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="c39d3-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="c39d3-146">ระดับค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-146">Compensation Level</span></span> | <span data-ttu-id="c39d3-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="c39d3-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="c39d3-148">ความถี่ในการจ่ายค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="c39d3-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="c39d3-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="c39d3-150">การตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="c39d3-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="c39d3-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="c39d3-152">รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="c39d3-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="c39d3-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="c39d3-154">ภูมิภาคของค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-154">Compensation Region</span></span> | <span data-ttu-id="c39d3-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="c39d3-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="c39d3-156">โครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-156">Compensation Structure</span></span> | <span data-ttu-id="c39d3-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="c39d3-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="c39d3-158">แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c39d3-158">Compensation Variable Plan</span></span> | <span data-ttu-id="c39d3-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="c39d3-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="c39d3-160">ระดับแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c39d3-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="c39d3-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="c39d3-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="c39d3-162">ชนิดแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c39d3-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="c39d3-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="c39d3-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="c39d3-164">เหตุการณ์ค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="c39d3-164">Fixed Compensation Event</span></span> | <span data-ttu-id="c39d3-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="c39d3-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="c39d3-166">กฎสิทธิ์พึงได้</span><span class="sxs-lookup"><span data-stu-id="c39d3-166">Vesting Rule</span></span> | <span data-ttu-id="c39d3-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="c39d3-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="c39d3-168">ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="c39d3-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="c39d3-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="c39d3-170">เอนทิตี้องค์กร</span><span class="sxs-lookup"><span data-stu-id="c39d3-170">Organization entities</span></span>

| <span data-ttu-id="c39d3-171">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-171">Name</span></span> | <span data-ttu-id="c39d3-172">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-173">แผนก</span><span class="sxs-lookup"><span data-stu-id="c39d3-173">Department</span></span> | <span data-ttu-id="c39d3-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="c39d3-174">cdm_department</span></span> |
| <span data-ttu-id="c39d3-175">การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-175">Employment</span></span> | <span data-ttu-id="c39d3-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="c39d3-176">cdm_employment</span></span> |
| <span data-ttu-id="c39d3-177">บริษัท</span><span class="sxs-lookup"><span data-stu-id="c39d3-177">Company</span></span> | <span data-ttu-id="c39d3-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="c39d3-178">cdm_company</span></span> |
| <span data-ttu-id="c39d3-179">หน้าที่</span><span class="sxs-lookup"><span data-stu-id="c39d3-179">Job</span></span> | <span data-ttu-id="c39d3-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="c39d3-180">cdm_job</span></span> |
| <span data-ttu-id="c39d3-181">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-181">Job Function</span></span> | <span data-ttu-id="c39d3-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="c39d3-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="c39d3-183">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-183">Job Position</span></span> | <span data-ttu-id="c39d3-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="c39d3-184">cdm_jobposition</span></span> |
| <span data-ttu-id="c39d3-185">ชนิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="c39d3-185">Position Type</span></span> | <span data-ttu-id="c39d3-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="c39d3-186">cdm_positiontype</span></span> |
| <span data-ttu-id="c39d3-187">การกำหนดตำแหน่งของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-187">Position Worker Assignment</span></span> | <span data-ttu-id="c39d3-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="c39d3-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="c39d3-189">มิติตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-189">Job Position Dimension</span></span> | <span data-ttu-id="c39d3-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="c39d3-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="c39d3-191">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-191">Job Type</span></span> | <span data-ttu-id="c39d3-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="c39d3-192">cdm_jobtype</span></span> |
| <span data-ttu-id="c39d3-193">ภาษา</span><span class="sxs-lookup"><span data-stu-id="c39d3-193">Language</span></span> | <span data-ttu-id="c39d3-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="c39d3-194">cdm_language</span></span> |
| <span data-ttu-id="c39d3-195">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="c39d3-195">Title</span></span> | <span data-ttu-id="c39d3-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="c39d3-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="c39d3-197">มิติทางการเงินสำหรับ **ชนิดของตำแหน่ง** **การกำหนดผู้ปฏิบัติงานของตำแหน่ง** และ **การจ้างงาน** ให้การรวมทิศทางเดียวแก่ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c39d3-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="c39d3-198">ในขณะนี้ การปรับปรุงมิติทางการเงินไม่สามารถซิงโครไนส์จาก Common Data Service กับทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="c39d3-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="c39d3-199">เอนทิตี้การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-199">Leave and absence entities</span></span>

| <span data-ttu-id="c39d3-200">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-200">Name</span></span> | <span data-ttu-id="c39d3-201">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-202">ธุรกรรมธนาคารวันลา</span><span class="sxs-lookup"><span data-stu-id="c39d3-202">Leave Bank Transaction</span></span> | <span data-ttu-id="c39d3-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="c39d3-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="c39d3-204">การลงทะเบียนการลางาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-204">Leave Enrollment</span></span> | <span data-ttu-id="c39d3-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="c39d3-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="c39d3-206">แผนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="c39d3-206">Leave Plan</span></span> | <span data-ttu-id="c39d3-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="c39d3-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="c39d3-208">การขอลา</span><span class="sxs-lookup"><span data-stu-id="c39d3-208">Leave Request</span></span> | <span data-ttu-id="c39d3-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="c39d3-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="c39d3-210">รายละเอียดคำขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-210">Leave Request Detail</span></span> | <span data-ttu-id="c39d3-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="c39d3-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="c39d3-212">ชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="c39d3-212">Leave Type</span></span> | <span data-ttu-id="c39d3-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="c39d3-213">cdm_leavetype</span></span> |
| <span data-ttu-id="c39d3-214">รหัสเหตุผลชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="c39d3-214">Leave Type Reason Code</span></span> | <span data-ttu-id="c39d3-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="c39d3-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="c39d3-216">เอนทิตี้ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="c39d3-216">Payroll entities</span></span>

| <span data-ttu-id="c39d3-217">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-217">Name</span></span> | <span data-ttu-id="c39d3-218">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-219">รอบการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="c39d3-219">Pay Cycle</span></span> | <span data-ttu-id="c39d3-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="c39d3-220">cdm_paycycle</span></span> |
| <span data-ttu-id="c39d3-221">รอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="c39d3-221">Pay Period</span></span> | <span data-ttu-id="c39d3-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="c39d3-222">cdm_payperiod</span></span> |
| <span data-ttu-id="c39d3-223">รหัสรายได้ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="c39d3-223">Payroll Earning Code</span></span> | <span data-ttu-id="c39d3-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="c39d3-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="c39d3-225">การเบิกจ่ายเงินของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="c39d3-225">Bank Account Disbursement</span></span> | <span data-ttu-id="c39d3-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="c39d3-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="c39d3-227">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="c39d3-227">Tax Region</span></span> | <span data-ttu-id="c39d3-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="c39d3-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="c39d3-229">เอนทิตี้ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-229">Worker entities</span></span>

| <span data-ttu-id="c39d3-230">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-230">Name</span></span> | <span data-ttu-id="c39d3-231">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-232">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-232">Worker</span></span> | <span data-ttu-id="c39d3-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="c39d3-233">cdm_worker</span></span> |
| <span data-ttu-id="c39d3-234">ที่อยู่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-234">Worker Address</span></span> | <span data-ttu-id="c39d3-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="c39d3-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="c39d3-236">รายละเอียดส่วนตัวของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-236">Worker Personal Detail</span></span> | <span data-ttu-id="c39d3-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="c39d3-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="c39d3-238">หมายเลขรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-238">Worker Person Identification Number</span></span> | <span data-ttu-id="c39d3-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="c39d3-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="c39d3-240">ชนิดรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-240">Worker Person Identification Type</span></span> | <span data-ttu-id="c39d3-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="c39d3-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="c39d3-242">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-242">Work Calendar</span></span> | <span data-ttu-id="c39d3-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="c39d3-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="c39d3-244">วันในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-244">Work Calendar Day</span></span> | <span data-ttu-id="c39d3-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="c39d3-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="c39d3-246">วันหยุดในปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-246">Work Calendar Holiday</span></span> |<span data-ttu-id="c39d3-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="c39d3-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="c39d3-248">รายการวันหยุดในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="c39d3-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="c39d3-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="c39d3-250">ช่วงเวลาในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="c39d3-251">cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="c39d3-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="c39d3-252">บัญชีธนาคารของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-252">Worker Bank Account</span></span> | <span data-ttu-id="c39d3-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="c39d3-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="c39d3-254">เอนทิตีการตั้งค่าของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-254">Worker setup entities</span></span>

| <span data-ttu-id="c39d3-255">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-255">Name</span></span> | <span data-ttu-id="c39d3-256">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-257">สถานะทหารผ่านศึก</span><span class="sxs-lookup"><span data-stu-id="c39d3-257">Veteran Status</span></span> | <span data-ttu-id="c39d3-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="c39d3-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="c39d3-259">เชื้อชาติ</span><span class="sxs-lookup"><span data-stu-id="c39d3-259">Ethnic Origin</span></span> | <span data-ttu-id="c39d3-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="c39d3-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="c39d3-261">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="c39d3-261">Reason Code</span></span> | <span data-ttu-id="c39d3-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="c39d3-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="c39d3-263">หน่วยงานที่ออกรหัสประจำตัวของบุคคล</span><span class="sxs-lookup"><span data-stu-id="c39d3-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="c39d3-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="c39d3-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="c39d3-265">เอนทิตีความสามารถ</span><span class="sxs-lookup"><span data-stu-id="c39d3-265">Competency entities</span></span>

| <span data-ttu-id="c39d3-266">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="c39d3-266">Name</span></span> | <span data-ttu-id="c39d3-267">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="c39d3-268">ชนิดของทักษะ</span><span class="sxs-lookup"><span data-stu-id="c39d3-268">Skill Type</span></span> | <span data-ttu-id="c39d3-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="c39d3-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="c39d3-270">รูปแบบความสัมพันธ์เอนทีตี้</span><span class="sxs-lookup"><span data-stu-id="c39d3-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="c39d3-271">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-271">Worker</span></span>

![ผู้ปฏิบัติงาน](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="c39d3-273">งานและตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-273">Job and Job Position</span></span>

![งานและตำแหน่งงาน](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="c39d3-275">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="c39d3-275">Benefits</span></span>

![สวัสดิการ](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="c39d3-277">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c39d3-277">Compensation</span></span>

![ค่าตอบแทน](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="c39d3-279">ออก</span><span class="sxs-lookup"><span data-stu-id="c39d3-279">Leave</span></span>

![ออก](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="c39d3-281">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="c39d3-281">Work Calendar</span></span>

![ปฏิทินการทำงาน](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="c39d3-283">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="c39d3-283">See also</span></span>

[<span data-ttu-id="c39d3-284">เลือกเทคโนโลยีการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c39d3-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="c39d3-285">ตั้งค่าคอนฟิกการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c39d3-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
