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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054367"
---
# <a name="dataverse-tables"></a><span data-ttu-id="39fa6-103">ตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="39fa6-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="39fa6-104">Microsoft Dynamics 365 Human Resources ใช้ Dataverse เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม</span><span class="sxs-lookup"><span data-stu-id="39fa6-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="39fa6-105">เอนทิตี Human Resources จะสอดคล้องกับตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="39fa6-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="39fa6-106">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดต Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) และการอัปเดตศัพท์ โปรดดูที่ [Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="39fa6-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="39fa6-107">ตาราง Dataverse ต่อไปนี้พร้อมใช้งานในเอนทิตี Human Resources</span><span class="sxs-lookup"><span data-stu-id="39fa6-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="39fa6-108">ตารางสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-108">Benefit tables</span></span>

| <span data-ttu-id="39fa6-109">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-109">Name</span></span> | <span data-ttu-id="39fa6-110">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-111">ความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="39fa6-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="39fa6-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="39fa6-113">รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="39fa6-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="39fa6-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="39fa6-115">อัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="39fa6-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="39fa6-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="39fa6-117">รายละเอียดอัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="39fa6-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="39fa6-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="39fa6-119">ตัวเลือกสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-119">Benefit Option</span></span> | <span data-ttu-id="39fa6-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="39fa6-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="39fa6-121">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-121">Benefit Plan</span></span> | <span data-ttu-id="39fa6-122">cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="39fa6-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="39fa6-123">ชนิดของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-123">Benefit Type</span></span> | <span data-ttu-id="39fa6-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="39fa6-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="39fa6-125">ตารางงานของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="39fa6-125">Business process tasks tables</span></span>

| <span data-ttu-id="39fa6-126">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-126">Name</span></span> | <span data-ttu-id="39fa6-127">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-128">ปฏิทินกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="39fa6-128">Business Process Calendar</span></span> | <span data-ttu-id="39fa6-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="39fa6-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="39fa6-130">การกำหนดกลุ่มกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="39fa6-130">Business Process Group Assignment</span></span> | <span data-ttu-id="39fa6-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="39fa6-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="39fa6-132">กลุ่มงานไลบรารีกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="39fa6-132">Business Process Library Task Group</span></span> | <span data-ttu-id="39fa6-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="39fa6-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="39fa6-134">ระยะของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="39fa6-134">Business Process Stage</span></span> | <span data-ttu-id="39fa6-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="39fa6-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="39fa6-136">ส่วนหัวเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="39fa6-136">Checklist Template Header</span></span> | <span data-ttu-id="39fa6-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="39fa6-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="39fa6-138">งานเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="39fa6-138">Checklist Template Task</span></span> | <span data-ttu-id="39fa6-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="39fa6-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="39fa6-140">ตารางค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-140">Compensation tables</span></span>

| <span data-ttu-id="39fa6-141">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-141">Name</span></span> | <span data-ttu-id="39fa6-142">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-143">แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="39fa6-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="39fa6-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="39fa6-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="39fa6-145">กริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-145">Compensation Grid</span></span> | <span data-ttu-id="39fa6-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="39fa6-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="39fa6-147">ระดับค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-147">Compensation Level</span></span> | <span data-ttu-id="39fa6-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="39fa6-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="39fa6-149">ความถี่ในการจ่ายค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="39fa6-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="39fa6-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="39fa6-151">การตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="39fa6-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="39fa6-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="39fa6-153">รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="39fa6-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="39fa6-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="39fa6-155">ภูมิภาคของค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-155">Compensation Region</span></span> | <span data-ttu-id="39fa6-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="39fa6-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="39fa6-157">โครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-157">Compensation Structure</span></span> | <span data-ttu-id="39fa6-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="39fa6-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="39fa6-159">แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="39fa6-159">Compensation Variable Plan</span></span> | <span data-ttu-id="39fa6-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="39fa6-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="39fa6-161">ระดับแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="39fa6-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="39fa6-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="39fa6-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="39fa6-163">ชนิดแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="39fa6-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="39fa6-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="39fa6-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="39fa6-165">เหตุการณ์ค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="39fa6-165">Fixed Compensation Event</span></span> | <span data-ttu-id="39fa6-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="39fa6-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="39fa6-167">กฎสิทธิ์พึงได้</span><span class="sxs-lookup"><span data-stu-id="39fa6-167">Vesting Rule</span></span> | <span data-ttu-id="39fa6-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="39fa6-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="39fa6-169">ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="39fa6-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="39fa6-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="39fa6-171">ตารางองค์กร</span><span class="sxs-lookup"><span data-stu-id="39fa6-171">Organization tables</span></span>

| <span data-ttu-id="39fa6-172">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-172">Name</span></span> | <span data-ttu-id="39fa6-173">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-174">แผนก</span><span class="sxs-lookup"><span data-stu-id="39fa6-174">Department</span></span> | <span data-ttu-id="39fa6-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="39fa6-175">cdm_department</span></span> |
| <span data-ttu-id="39fa6-176">การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-176">Employment</span></span> | <span data-ttu-id="39fa6-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="39fa6-177">cdm_employment</span></span> |
| <span data-ttu-id="39fa6-178">บริษัท</span><span class="sxs-lookup"><span data-stu-id="39fa6-178">Company</span></span> | <span data-ttu-id="39fa6-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="39fa6-179">cdm_company</span></span> |
| <span data-ttu-id="39fa6-180">หน้าที่</span><span class="sxs-lookup"><span data-stu-id="39fa6-180">Job</span></span> | <span data-ttu-id="39fa6-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="39fa6-181">cdm_job</span></span> |
| <span data-ttu-id="39fa6-182">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-182">Job Function</span></span> | <span data-ttu-id="39fa6-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="39fa6-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="39fa6-184">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-184">Job Position</span></span> | <span data-ttu-id="39fa6-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="39fa6-185">cdm_jobposition</span></span> |
| <span data-ttu-id="39fa6-186">ชนิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="39fa6-186">Position Type</span></span> | <span data-ttu-id="39fa6-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="39fa6-187">cdm_positiontype</span></span> |
| <span data-ttu-id="39fa6-188">การกำหนดตำแหน่งของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-188">Position Worker Assignment</span></span> | <span data-ttu-id="39fa6-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="39fa6-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="39fa6-190">มิติตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-190">Job Position Dimension</span></span> | <span data-ttu-id="39fa6-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="39fa6-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="39fa6-192">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-192">Job Type</span></span> | <span data-ttu-id="39fa6-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="39fa6-193">cdm_jobtype</span></span> |
| <span data-ttu-id="39fa6-194">ภาษา</span><span class="sxs-lookup"><span data-stu-id="39fa6-194">Language</span></span> | <span data-ttu-id="39fa6-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="39fa6-195">cdm_language</span></span> |
| <span data-ttu-id="39fa6-196">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="39fa6-196">Title</span></span> | <span data-ttu-id="39fa6-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="39fa6-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="39fa6-198">มิติทางการเงินสำหรับ **ชนิดของตำแหน่ง** **การกำหนดผู้ปฏิบัติงานของตำแหน่ง** และ **การจ้างงาน** ให้การรวมทิศทางเดียวแก่ Dataverse</span><span class="sxs-lookup"><span data-stu-id="39fa6-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="39fa6-199">ในขณะนี้ การปรับปรุงมิติทางการเงินไม่สามารถซิงโครไนส์จาก Dataverse กับทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="39fa6-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="39fa6-200">ตารางการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-200">Leave and absence tables</span></span>

| <span data-ttu-id="39fa6-201">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-201">Name</span></span> | <span data-ttu-id="39fa6-202">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-203">ธุรกรรมธนาคารวันลา</span><span class="sxs-lookup"><span data-stu-id="39fa6-203">Leave Bank Transaction</span></span> | <span data-ttu-id="39fa6-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="39fa6-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="39fa6-205">การลงทะเบียนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="39fa6-205">Leave Enrollment</span></span> | <span data-ttu-id="39fa6-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="39fa6-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="39fa6-207">แผนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="39fa6-207">Leave Plan</span></span> | <span data-ttu-id="39fa6-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="39fa6-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="39fa6-209">การขอลา</span><span class="sxs-lookup"><span data-stu-id="39fa6-209">Leave Request</span></span> | <span data-ttu-id="39fa6-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="39fa6-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="39fa6-211">รายละเอียดคำขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-211">Leave Request Detail</span></span> | <span data-ttu-id="39fa6-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="39fa6-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="39fa6-213">ชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="39fa6-213">Leave Type</span></span> | <span data-ttu-id="39fa6-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="39fa6-214">cdm_leavetype</span></span> |
| <span data-ttu-id="39fa6-215">รหัสเหตุผลชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="39fa6-215">Leave Type Reason Code</span></span> | <span data-ttu-id="39fa6-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="39fa6-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="39fa6-217">ตารางค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="39fa6-217">Payroll tables</span></span>

| <span data-ttu-id="39fa6-218">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-218">Name</span></span> | <span data-ttu-id="39fa6-219">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-220">รอบการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="39fa6-220">Pay Cycle</span></span> | <span data-ttu-id="39fa6-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="39fa6-221">cdm_paycycle</span></span> |
| <span data-ttu-id="39fa6-222">รอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="39fa6-222">Pay Period</span></span> | <span data-ttu-id="39fa6-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="39fa6-223">cdm_payperiod</span></span> |
| <span data-ttu-id="39fa6-224">รหัสรายได้ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="39fa6-224">Payroll Earning Code</span></span> | <span data-ttu-id="39fa6-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="39fa6-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="39fa6-226">การเบิกจ่ายเงินของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="39fa6-226">Bank Account Disbursement</span></span> | <span data-ttu-id="39fa6-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="39fa6-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="39fa6-228">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="39fa6-228">Tax Region</span></span> | <span data-ttu-id="39fa6-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="39fa6-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="39fa6-230">ตารางผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-230">Worker tables</span></span>

| <span data-ttu-id="39fa6-231">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-231">Name</span></span> | <span data-ttu-id="39fa6-232">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-233">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-233">Worker</span></span> | <span data-ttu-id="39fa6-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="39fa6-234">cdm_worker</span></span> |
| <span data-ttu-id="39fa6-235">ที่อยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-235">Worker Address</span></span> | <span data-ttu-id="39fa6-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="39fa6-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="39fa6-237">รายละเอียดส่วนตัวของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-237">Worker Personal Detail</span></span> | <span data-ttu-id="39fa6-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="39fa6-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="39fa6-239">หมายเลขรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-239">Worker Person Identification Number</span></span> | <span data-ttu-id="39fa6-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="39fa6-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="39fa6-241">ชนิดรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-241">Worker Person Identification Type</span></span> | <span data-ttu-id="39fa6-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="39fa6-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="39fa6-243">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-243">Work Calendar</span></span> | <span data-ttu-id="39fa6-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="39fa6-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="39fa6-245">วันในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-245">Work Calendar Day</span></span> | <span data-ttu-id="39fa6-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="39fa6-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="39fa6-247">วันหยุดในปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-247">Work Calendar Holiday</span></span> |<span data-ttu-id="39fa6-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="39fa6-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="39fa6-249">รายการวันหยุดในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="39fa6-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="39fa6-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="39fa6-251">ช่วงเวลาในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="39fa6-252">cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="39fa6-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="39fa6-253">บัญชีธนาคารของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-253">Worker Bank Account</span></span> | <span data-ttu-id="39fa6-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="39fa6-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="39fa6-255">ตารางการตั้งค่าผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-255">Worker setup tables</span></span>

| <span data-ttu-id="39fa6-256">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-256">Name</span></span> | <span data-ttu-id="39fa6-257">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-258">สถานะทหารผ่านศึก</span><span class="sxs-lookup"><span data-stu-id="39fa6-258">Veteran Status</span></span> | <span data-ttu-id="39fa6-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="39fa6-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="39fa6-260">เชื้อชาติ</span><span class="sxs-lookup"><span data-stu-id="39fa6-260">Ethnic Origin</span></span> | <span data-ttu-id="39fa6-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="39fa6-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="39fa6-262">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="39fa6-262">Reason Code</span></span> | <span data-ttu-id="39fa6-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="39fa6-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="39fa6-264">หน่วยงานที่ออกรหัสประจำตัวของบุคคล</span><span class="sxs-lookup"><span data-stu-id="39fa6-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="39fa6-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="39fa6-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="39fa6-266">ตารางความสามารถ</span><span class="sxs-lookup"><span data-stu-id="39fa6-266">Competency tables</span></span>

| <span data-ttu-id="39fa6-267">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39fa6-267">Name</span></span> | <span data-ttu-id="39fa6-268">ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="39fa6-269">ชนิดทักษะ</span><span class="sxs-lookup"><span data-stu-id="39fa6-269">Skill Type</span></span> | <span data-ttu-id="39fa6-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="39fa6-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="39fa6-271">แบบจำลองความสัมพันธ์ตาราง</span><span class="sxs-lookup"><span data-stu-id="39fa6-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="39fa6-272">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-272">Worker</span></span>

![ผู้ปฏิบัติงาน](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="39fa6-274">งานและตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-274">Job and Job Position</span></span>

![งานและตำแหน่งงาน](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="39fa6-276">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="39fa6-276">Benefits</span></span>

![สวัสดิการ](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="39fa6-278">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="39fa6-278">Compensation</span></span>

![ค่าตอบแทน](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="39fa6-280">ออก</span><span class="sxs-lookup"><span data-stu-id="39fa6-280">Leave</span></span>

![ออก](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="39fa6-282">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="39fa6-282">Work Calendar</span></span>

![ปฏิทินการทำงาน](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="39fa6-284">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="39fa6-284">See also</span></span>

[<span data-ttu-id="39fa6-285">เลือกเทคโนโลยีการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="39fa6-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="39fa6-286">ตั้งค่าคอนฟิกการรวม Dataverse</span><span class="sxs-lookup"><span data-stu-id="39fa6-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="39fa6-287">ตั้งค่าคอนฟิกตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="39fa6-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="39fa6-288">FAQ เกี่ยวกับตารางเสมือนสำหรับ Human Resources</span><span class="sxs-lookup"><span data-stu-id="39fa6-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="39fa6-289">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="39fa6-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="39fa6-290">การอัปเดตศัพท์</span><span class="sxs-lookup"><span data-stu-id="39fa6-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]