---
title: ตาราง Dataverse
description: Microsoft Dynamics 365 Human Resources ใช้ Dataverse เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793620"
---
# <a name="dataverse-tables"></a><span data-ttu-id="4fe8e-103">ตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="4fe8e-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4fe8e-104">Microsoft Dynamics 365 Human Resources ใช้ Dataverse เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม</span><span class="sxs-lookup"><span data-stu-id="4fe8e-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="4fe8e-105">เอนทิตี Human Resources จะสอดคล้องกับตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="4fe8e-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="4fe8e-106">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดต Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) และการอัปเดตศัพท์ โปรดดูที่ [Microsoft Dataverse คืออะไร](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="4fe8e-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="4fe8e-107">ตาราง Dataverse ต่อไปนี้พร้อมใช้งานในเอนทิตี Human Resources</span><span class="sxs-lookup"><span data-stu-id="4fe8e-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="4fe8e-108">ตารางสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-108">Benefit tables</span></span>

| <span data-ttu-id="4fe8e-109">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-109">Name</span></span> | <span data-ttu-id="4fe8e-110">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-111">ความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="4fe8e-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="4fe8e-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="4fe8e-113">รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="4fe8e-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="4fe8e-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="4fe8e-115">อัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="4fe8e-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="4fe8e-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="4fe8e-117">รายละเอียดอัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="4fe8e-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="4fe8e-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="4fe8e-119">ตัวเลือกสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-119">Benefit Option</span></span> | <span data-ttu-id="4fe8e-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="4fe8e-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="4fe8e-121">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-121">Benefit Plan</span></span> | <span data-ttu-id="4fe8e-122">cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="4fe8e-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4fe8e-123">ชนิดของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-123">Benefit Type</span></span> | <span data-ttu-id="4fe8e-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="4fe8e-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="4fe8e-125">ตารางงานของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-125">Business process tasks tables</span></span>

| <span data-ttu-id="4fe8e-126">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-126">Name</span></span> | <span data-ttu-id="4fe8e-127">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-128">ปฏิทินกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-128">Business Process Calendar</span></span> | <span data-ttu-id="4fe8e-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="4fe8e-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="4fe8e-130">การกำหนดกลุ่มกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-130">Business Process Group Assignment</span></span> | <span data-ttu-id="4fe8e-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="4fe8e-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="4fe8e-132">กลุ่มงานไลบรารีกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-132">Business Process Library Task Group</span></span> | <span data-ttu-id="4fe8e-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="4fe8e-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="4fe8e-134">ระยะของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-134">Business Process Stage</span></span> | <span data-ttu-id="4fe8e-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="4fe8e-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="4fe8e-136">ส่วนหัวเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-136">Checklist Template Header</span></span> | <span data-ttu-id="4fe8e-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="4fe8e-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="4fe8e-138">งานเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-138">Checklist Template Task</span></span> | <span data-ttu-id="4fe8e-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="4fe8e-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="4fe8e-140">ตารางค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-140">Compensation tables</span></span>

| <span data-ttu-id="4fe8e-141">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-141">Name</span></span> | <span data-ttu-id="4fe8e-142">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-143">แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="4fe8e-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="4fe8e-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="4fe8e-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="4fe8e-145">กริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-145">Compensation Grid</span></span> | <span data-ttu-id="4fe8e-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="4fe8e-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="4fe8e-147">ระดับค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-147">Compensation Level</span></span> | <span data-ttu-id="4fe8e-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="4fe8e-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="4fe8e-149">ความถี่ในการจ่ายค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="4fe8e-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="4fe8e-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="4fe8e-151">การตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="4fe8e-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="4fe8e-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="4fe8e-153">รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="4fe8e-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="4fe8e-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="4fe8e-155">ภูมิภาคของค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-155">Compensation Region</span></span> | <span data-ttu-id="4fe8e-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="4fe8e-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="4fe8e-157">โครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-157">Compensation Structure</span></span> | <span data-ttu-id="4fe8e-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="4fe8e-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="4fe8e-159">แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="4fe8e-159">Compensation Variable Plan</span></span> | <span data-ttu-id="4fe8e-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="4fe8e-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="4fe8e-161">ระดับแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="4fe8e-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="4fe8e-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="4fe8e-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="4fe8e-163">ชนิดแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="4fe8e-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="4fe8e-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="4fe8e-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="4fe8e-165">เหตุการณ์ค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="4fe8e-165">Fixed Compensation Event</span></span> | <span data-ttu-id="4fe8e-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="4fe8e-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="4fe8e-167">กฎสิทธิ์พึงได้</span><span class="sxs-lookup"><span data-stu-id="4fe8e-167">Vesting Rule</span></span> | <span data-ttu-id="4fe8e-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="4fe8e-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="4fe8e-169">ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="4fe8e-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="4fe8e-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="4fe8e-171">ตารางองค์กร</span><span class="sxs-lookup"><span data-stu-id="4fe8e-171">Organization tables</span></span>

| <span data-ttu-id="4fe8e-172">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-172">Name</span></span> | <span data-ttu-id="4fe8e-173">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-174">แผนก</span><span class="sxs-lookup"><span data-stu-id="4fe8e-174">Department</span></span> | <span data-ttu-id="4fe8e-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="4fe8e-175">cdm_department</span></span> |
| <span data-ttu-id="4fe8e-176">การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-176">Employment</span></span> | <span data-ttu-id="4fe8e-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="4fe8e-177">cdm_employment</span></span> |
| <span data-ttu-id="4fe8e-178">บริษัท</span><span class="sxs-lookup"><span data-stu-id="4fe8e-178">Company</span></span> | <span data-ttu-id="4fe8e-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="4fe8e-179">cdm_company</span></span> |
| <span data-ttu-id="4fe8e-180">หน้าที่</span><span class="sxs-lookup"><span data-stu-id="4fe8e-180">Job</span></span> | <span data-ttu-id="4fe8e-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="4fe8e-181">cdm_job</span></span> |
| <span data-ttu-id="4fe8e-182">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-182">Job Function</span></span> | <span data-ttu-id="4fe8e-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="4fe8e-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="4fe8e-184">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-184">Job Position</span></span> | <span data-ttu-id="4fe8e-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="4fe8e-185">cdm_jobposition</span></span> |
| <span data-ttu-id="4fe8e-186">ชนิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-186">Position Type</span></span> | <span data-ttu-id="4fe8e-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="4fe8e-187">cdm_positiontype</span></span> |
| <span data-ttu-id="4fe8e-188">การกำหนดตำแหน่งของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-188">Position Worker Assignment</span></span> | <span data-ttu-id="4fe8e-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="4fe8e-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="4fe8e-190">มิติตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-190">Job Position Dimension</span></span> | <span data-ttu-id="4fe8e-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="4fe8e-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="4fe8e-192">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-192">Job Type</span></span> | <span data-ttu-id="4fe8e-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="4fe8e-193">cdm_jobtype</span></span> |
| <span data-ttu-id="4fe8e-194">ภาษา</span><span class="sxs-lookup"><span data-stu-id="4fe8e-194">Language</span></span> | <span data-ttu-id="4fe8e-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="4fe8e-195">cdm_language</span></span> |
| <span data-ttu-id="4fe8e-196">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-196">Title</span></span> | <span data-ttu-id="4fe8e-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="4fe8e-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="4fe8e-198">มิติทางการเงินสำหรับ **ชนิดของตำแหน่ง** **การกำหนดผู้ปฏิบัติงานของตำแหน่ง** และ **การจ้างงาน** ให้การรวมทิศทางเดียวแก่ Dataverse</span><span class="sxs-lookup"><span data-stu-id="4fe8e-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="4fe8e-199">ในขณะนี้ การปรับปรุงมิติทางการเงินไม่สามารถซิงโครไนส์จาก Dataverse กับทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="4fe8e-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="4fe8e-200">ตารางการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-200">Leave and absence tables</span></span>

| <span data-ttu-id="4fe8e-201">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-201">Name</span></span> | <span data-ttu-id="4fe8e-202">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-203">ธุรกรรมธนาคารวันลา</span><span class="sxs-lookup"><span data-stu-id="4fe8e-203">Leave Bank Transaction</span></span> | <span data-ttu-id="4fe8e-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="4fe8e-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="4fe8e-205">การลงทะเบียนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="4fe8e-205">Leave Enrollment</span></span> | <span data-ttu-id="4fe8e-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="4fe8e-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="4fe8e-207">แผนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="4fe8e-207">Leave Plan</span></span> | <span data-ttu-id="4fe8e-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="4fe8e-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="4fe8e-209">การขอลา</span><span class="sxs-lookup"><span data-stu-id="4fe8e-209">Leave Request</span></span> | <span data-ttu-id="4fe8e-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="4fe8e-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="4fe8e-211">รายละเอียดคำขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-211">Leave Request Detail</span></span> | <span data-ttu-id="4fe8e-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="4fe8e-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="4fe8e-213">ชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="4fe8e-213">Leave Type</span></span> | <span data-ttu-id="4fe8e-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="4fe8e-214">cdm_leavetype</span></span> |
| <span data-ttu-id="4fe8e-215">รหัสเหตุผลชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="4fe8e-215">Leave Type Reason Code</span></span> | <span data-ttu-id="4fe8e-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="4fe8e-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="4fe8e-217">ตารางค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-217">Payroll tables</span></span>

| <span data-ttu-id="4fe8e-218">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-218">Name</span></span> | <span data-ttu-id="4fe8e-219">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-220">รอบการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-220">Pay Cycle</span></span> | <span data-ttu-id="4fe8e-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="4fe8e-221">cdm_paycycle</span></span> |
| <span data-ttu-id="4fe8e-222">รอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-222">Pay Period</span></span> | <span data-ttu-id="4fe8e-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="4fe8e-223">cdm_payperiod</span></span> |
| <span data-ttu-id="4fe8e-224">รหัสรายได้ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-224">Payroll Earning Code</span></span> | <span data-ttu-id="4fe8e-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="4fe8e-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="4fe8e-226">การเบิกจ่ายเงินของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="4fe8e-226">Bank Account Disbursement</span></span> | <span data-ttu-id="4fe8e-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="4fe8e-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="4fe8e-228">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="4fe8e-228">Tax Region</span></span> | <span data-ttu-id="4fe8e-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="4fe8e-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="4fe8e-230">ตารางผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-230">Worker tables</span></span>

| <span data-ttu-id="4fe8e-231">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-231">Name</span></span> | <span data-ttu-id="4fe8e-232">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-233">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-233">Worker</span></span> | <span data-ttu-id="4fe8e-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="4fe8e-234">cdm_worker</span></span> |
| <span data-ttu-id="4fe8e-235">ที่อยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-235">Worker Address</span></span> | <span data-ttu-id="4fe8e-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="4fe8e-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="4fe8e-237">รายละเอียดส่วนตัวของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-237">Worker Personal Detail</span></span> | <span data-ttu-id="4fe8e-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="4fe8e-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="4fe8e-239">หมายเลขรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-239">Worker Person Identification Number</span></span> | <span data-ttu-id="4fe8e-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="4fe8e-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="4fe8e-241">ชนิดรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-241">Worker Person Identification Type</span></span> | <span data-ttu-id="4fe8e-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="4fe8e-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="4fe8e-243">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-243">Work Calendar</span></span> | <span data-ttu-id="4fe8e-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="4fe8e-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="4fe8e-245">วันในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-245">Work Calendar Day</span></span> | <span data-ttu-id="4fe8e-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="4fe8e-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="4fe8e-247">วันหยุดในปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-247">Work Calendar Holiday</span></span> |<span data-ttu-id="4fe8e-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="4fe8e-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="4fe8e-249">รายการวันหยุดในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="4fe8e-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="4fe8e-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="4fe8e-251">ช่วงเวลาในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="4fe8e-252">cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="4fe8e-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4fe8e-253">บัญชีธนาคารของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-253">Worker Bank Account</span></span> | <span data-ttu-id="4fe8e-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="4fe8e-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="4fe8e-255">ตารางการตั้งค่าผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-255">Worker setup tables</span></span>

| <span data-ttu-id="4fe8e-256">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-256">Name</span></span> | <span data-ttu-id="4fe8e-257">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-258">สถานะทหารผ่านศึก</span><span class="sxs-lookup"><span data-stu-id="4fe8e-258">Veteran Status</span></span> | <span data-ttu-id="4fe8e-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="4fe8e-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="4fe8e-260">เชื้อชาติ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-260">Ethnic Origin</span></span> | <span data-ttu-id="4fe8e-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="4fe8e-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="4fe8e-262">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="4fe8e-262">Reason Code</span></span> | <span data-ttu-id="4fe8e-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="4fe8e-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="4fe8e-264">หน่วยงานที่ออกรหัสประจำตัวของบุคคล</span><span class="sxs-lookup"><span data-stu-id="4fe8e-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="4fe8e-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="4fe8e-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="4fe8e-266">ตารางความสามารถ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-266">Competency tables</span></span>

| <span data-ttu-id="4fe8e-267">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-267">Name</span></span> | <span data-ttu-id="4fe8e-268">ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="4fe8e-269">ชนิดทักษะ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-269">Skill Type</span></span> | <span data-ttu-id="4fe8e-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="4fe8e-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="4fe8e-271">แบบจำลองความสัมพันธ์ตาราง</span><span class="sxs-lookup"><span data-stu-id="4fe8e-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="4fe8e-272">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-272">Worker</span></span>

![ผู้ปฏิบัติงาน](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="4fe8e-274">งานและตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-274">Job and Job Position</span></span>

![งานและตำแหน่งงาน](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="4fe8e-276">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="4fe8e-276">Benefits</span></span>

![สวัสดิการ](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="4fe8e-278">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-278">Compensation</span></span>

![ค่าตอบแทน](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="4fe8e-280">ออก</span><span class="sxs-lookup"><span data-stu-id="4fe8e-280">Leave</span></span>

![ออก](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="4fe8e-282">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4fe8e-282">Work Calendar</span></span>

![ปฏิทินการทำงาน](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="4fe8e-284">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="4fe8e-284">See also</span></span>

[<span data-ttu-id="4fe8e-285">เลือกเทคโนโลยีการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4fe8e-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="4fe8e-286">ตั้งค่าคอนฟิกการรวม Dataverse</span><span class="sxs-lookup"><span data-stu-id="4fe8e-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="4fe8e-287">ตั้งค่าคอนฟิกตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="4fe8e-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="4fe8e-288">FAQ เกี่ยวกับตารางเสมือนสำหรับ Human Resources</span><span class="sxs-lookup"><span data-stu-id="4fe8e-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="4fe8e-289">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="4fe8e-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="4fe8e-290">การอัปเดตศัพท์</span><span class="sxs-lookup"><span data-stu-id="4fe8e-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]