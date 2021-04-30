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
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893411"
---
# <a name="dataverse-tables"></a><span data-ttu-id="9985c-103">ตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="9985c-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9985c-104">Microsoft Dynamics 365 Human Resources ใช้ Dataverse เพื่อเปิดใช้งานความสามารถในการเพิ่มและสถานการณ์การรวม</span><span class="sxs-lookup"><span data-stu-id="9985c-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="9985c-105">เอนทิตี Human Resources จะสอดคล้องกับตาราง Dataverse</span><span class="sxs-lookup"><span data-stu-id="9985c-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="9985c-106">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดต Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service) และการอัปเดตศัพท์ โปรดดูที่ [Microsoft Dataverse คืออะไร](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="9985c-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="9985c-107">ตาราง Dataverse ต่อไปนี้พร้อมใช้งานในเอนทิตี Human Resources</span><span class="sxs-lookup"><span data-stu-id="9985c-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="9985c-108">ตารางสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-108">Benefit tables</span></span>

| <span data-ttu-id="9985c-109">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-109">Name</span></span> | <span data-ttu-id="9985c-110">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-111">ความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="9985c-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="9985c-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="9985c-113">รอบระยะเวลาการชำระเงินตามความถี่ในการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="9985c-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="9985c-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="9985c-115">อัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="9985c-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="9985c-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="9985c-117">รายละเอียดอัตราการคำนวณสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="9985c-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="9985c-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="9985c-119">ตัวเลือกสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-119">Benefit Option</span></span> | <span data-ttu-id="9985c-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="9985c-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="9985c-121">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-121">Benefit Plan</span></span> | <span data-ttu-id="9985c-122">cdm_benefitplan (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="9985c-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="9985c-123">ชนิดของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-123">Benefit Type</span></span> | <span data-ttu-id="9985c-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="9985c-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="9985c-125">ตารางงานของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9985c-125">Business process tasks tables</span></span>

| <span data-ttu-id="9985c-126">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-126">Name</span></span> | <span data-ttu-id="9985c-127">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-128">ปฏิทินกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9985c-128">Business Process Calendar</span></span> | <span data-ttu-id="9985c-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="9985c-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="9985c-130">การกำหนดกลุ่มกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9985c-130">Business Process Group Assignment</span></span> | <span data-ttu-id="9985c-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="9985c-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="9985c-132">กลุ่มงานไลบรารีกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9985c-132">Business Process Library Task Group</span></span> | <span data-ttu-id="9985c-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="9985c-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="9985c-134">ระยะของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9985c-134">Business Process Stage</span></span> | <span data-ttu-id="9985c-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="9985c-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="9985c-136">ส่วนหัวเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9985c-136">Checklist Template Header</span></span> | <span data-ttu-id="9985c-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="9985c-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="9985c-138">งานเท็มเพลตรายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9985c-138">Checklist Template Task</span></span> | <span data-ttu-id="9985c-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="9985c-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="9985c-140">ตารางค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-140">Compensation tables</span></span>

| <span data-ttu-id="9985c-141">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-141">Name</span></span> | <span data-ttu-id="9985c-142">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-143">แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="9985c-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="9985c-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="9985c-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="9985c-145">กริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-145">Compensation Grid</span></span> | <span data-ttu-id="9985c-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="9985c-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="9985c-147">ระดับค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-147">Compensation Level</span></span> | <span data-ttu-id="9985c-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="9985c-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="9985c-149">ความถี่ในการจ่ายค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="9985c-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="9985c-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="9985c-151">การตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="9985c-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="9985c-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="9985c-153">รายการการตั้งค่าจุดอ้างอิงค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="9985c-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="9985c-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="9985c-155">ภูมิภาคของค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-155">Compensation Region</span></span> | <span data-ttu-id="9985c-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="9985c-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="9985c-157">โครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-157">Compensation Structure</span></span> | <span data-ttu-id="9985c-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="9985c-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="9985c-159">แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="9985c-159">Compensation Variable Plan</span></span> | <span data-ttu-id="9985c-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="9985c-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="9985c-161">ระดับแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="9985c-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="9985c-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="9985c-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="9985c-163">ชนิดแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="9985c-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="9985c-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="9985c-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="9985c-165">เหตุการณ์ค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="9985c-165">Fixed Compensation Event</span></span> | <span data-ttu-id="9985c-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="9985c-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="9985c-167">กฎสิทธิ์พึงได้</span><span class="sxs-lookup"><span data-stu-id="9985c-167">Vesting Rule</span></span> | <span data-ttu-id="9985c-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="9985c-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="9985c-169">ค่าตอบแทนคงที่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="9985c-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="9985c-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="9985c-171">ตารางองค์กร</span><span class="sxs-lookup"><span data-stu-id="9985c-171">Organization tables</span></span>

| <span data-ttu-id="9985c-172">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-172">Name</span></span> | <span data-ttu-id="9985c-173">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-174">แผนก</span><span class="sxs-lookup"><span data-stu-id="9985c-174">Department</span></span> | <span data-ttu-id="9985c-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="9985c-175">cdm_department</span></span> |
| <span data-ttu-id="9985c-176">การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-176">Employment</span></span> | <span data-ttu-id="9985c-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="9985c-177">cdm_employment</span></span> |
| <span data-ttu-id="9985c-178">บริษัท</span><span class="sxs-lookup"><span data-stu-id="9985c-178">Company</span></span> | <span data-ttu-id="9985c-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="9985c-179">cdm_company</span></span> |
| <span data-ttu-id="9985c-180">หน้าที่</span><span class="sxs-lookup"><span data-stu-id="9985c-180">Job</span></span> | <span data-ttu-id="9985c-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="9985c-181">cdm_job</span></span> |
| <span data-ttu-id="9985c-182">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-182">Job Function</span></span> | <span data-ttu-id="9985c-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="9985c-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="9985c-184">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-184">Job Position</span></span> | <span data-ttu-id="9985c-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="9985c-185">cdm_jobposition</span></span> |
| <span data-ttu-id="9985c-186">ชนิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="9985c-186">Position Type</span></span> | <span data-ttu-id="9985c-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="9985c-187">cdm_positiontype</span></span> |
| <span data-ttu-id="9985c-188">การกำหนดตำแหน่งของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-188">Position Worker Assignment</span></span> | <span data-ttu-id="9985c-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="9985c-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="9985c-190">มิติตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-190">Job Position Dimension</span></span> | <span data-ttu-id="9985c-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="9985c-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="9985c-192">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-192">Job Type</span></span> | <span data-ttu-id="9985c-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="9985c-193">cdm_jobtype</span></span> |
| <span data-ttu-id="9985c-194">ภาษา</span><span class="sxs-lookup"><span data-stu-id="9985c-194">Language</span></span> | <span data-ttu-id="9985c-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="9985c-195">cdm_language</span></span> |
| <span data-ttu-id="9985c-196">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="9985c-196">Title</span></span> | <span data-ttu-id="9985c-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="9985c-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="9985c-198">มิติทางการเงินสำหรับ **ชนิดของตำแหน่ง** **การกำหนดผู้ปฏิบัติงานของตำแหน่ง** และ **การจ้างงาน** ให้การรวมทิศทางเดียวแก่ Dataverse</span><span class="sxs-lookup"><span data-stu-id="9985c-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="9985c-199">ในขณะนี้ การปรับปรุงมิติทางการเงินไม่สามารถซิงโครไนส์จาก Dataverse กับทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="9985c-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="9985c-200">ตารางการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-200">Leave and absence tables</span></span>

| <span data-ttu-id="9985c-201">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-201">Name</span></span> | <span data-ttu-id="9985c-202">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-203">ธุรกรรมธนาคารวันลา</span><span class="sxs-lookup"><span data-stu-id="9985c-203">Leave Bank Transaction</span></span> | <span data-ttu-id="9985c-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="9985c-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="9985c-205">การลงทะเบียนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="9985c-205">Leave Enrollment</span></span> | <span data-ttu-id="9985c-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="9985c-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="9985c-207">แผนการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="9985c-207">Leave Plan</span></span> | <span data-ttu-id="9985c-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="9985c-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="9985c-209">การขอลา</span><span class="sxs-lookup"><span data-stu-id="9985c-209">Leave Request</span></span> | <span data-ttu-id="9985c-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="9985c-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="9985c-211">รายละเอียดคำขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="9985c-211">Leave Request Detail</span></span> | <span data-ttu-id="9985c-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="9985c-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="9985c-213">ชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="9985c-213">Leave Type</span></span> | <span data-ttu-id="9985c-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="9985c-214">cdm_leavetype</span></span> |
| <span data-ttu-id="9985c-215">รหัสเหตุผลชนิดการลา</span><span class="sxs-lookup"><span data-stu-id="9985c-215">Leave Type Reason Code</span></span> | <span data-ttu-id="9985c-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="9985c-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="9985c-217">ตารางค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="9985c-217">Payroll tables</span></span>

| <span data-ttu-id="9985c-218">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-218">Name</span></span> | <span data-ttu-id="9985c-219">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-220">รอบการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="9985c-220">Pay Cycle</span></span> | <span data-ttu-id="9985c-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="9985c-221">cdm_paycycle</span></span> |
| <span data-ttu-id="9985c-222">รอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="9985c-222">Pay Period</span></span> | <span data-ttu-id="9985c-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="9985c-223">cdm_payperiod</span></span> |
| <span data-ttu-id="9985c-224">รหัสรายได้ค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="9985c-224">Payroll Earning Code</span></span> | <span data-ttu-id="9985c-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="9985c-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="9985c-226">การเบิกจ่ายเงินของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9985c-226">Bank Account Disbursement</span></span> | <span data-ttu-id="9985c-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="9985c-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="9985c-228">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="9985c-228">Tax Region</span></span> | <span data-ttu-id="9985c-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="9985c-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="9985c-230">ตารางผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-230">Worker tables</span></span>

| <span data-ttu-id="9985c-231">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-231">Name</span></span> | <span data-ttu-id="9985c-232">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-233">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-233">Worker</span></span> | <span data-ttu-id="9985c-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="9985c-234">cdm_worker</span></span> |
| <span data-ttu-id="9985c-235">ที่อยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-235">Worker Address</span></span> | <span data-ttu-id="9985c-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="9985c-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="9985c-237">รายละเอียดส่วนตัวของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-237">Worker Personal Detail</span></span> | <span data-ttu-id="9985c-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="9985c-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="9985c-239">หมายเลขรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-239">Worker Person Identification Number</span></span> | <span data-ttu-id="9985c-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="9985c-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="9985c-241">ชนิดรหัสของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-241">Worker Person Identification Type</span></span> | <span data-ttu-id="9985c-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="9985c-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="9985c-243">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-243">Work Calendar</span></span> | <span data-ttu-id="9985c-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="9985c-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="9985c-245">วันในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-245">Work Calendar Day</span></span> | <span data-ttu-id="9985c-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="9985c-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="9985c-247">วันหยุดในปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-247">Work Calendar Holiday</span></span> |<span data-ttu-id="9985c-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="9985c-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="9985c-249">รายการวันหยุดในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="9985c-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="9985c-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="9985c-251">ช่วงเวลาในปฏิทินงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="9985c-252">cdm_workcalendartimeinterval (ไม่ได้เปิดใช้งานสำหรับการสนับสนุนฟิลด์แบบกำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="9985c-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="9985c-253">บัญชีธนาคารของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-253">Worker Bank Account</span></span> | <span data-ttu-id="9985c-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="9985c-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="9985c-255">ตารางการตั้งค่าผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-255">Worker setup tables</span></span>

| <span data-ttu-id="9985c-256">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-256">Name</span></span> | <span data-ttu-id="9985c-257">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-258">สถานะทหารผ่านศึก</span><span class="sxs-lookup"><span data-stu-id="9985c-258">Veteran Status</span></span> | <span data-ttu-id="9985c-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="9985c-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="9985c-260">เชื้อชาติ</span><span class="sxs-lookup"><span data-stu-id="9985c-260">Ethnic Origin</span></span> | <span data-ttu-id="9985c-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="9985c-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="9985c-262">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="9985c-262">Reason Code</span></span> | <span data-ttu-id="9985c-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="9985c-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="9985c-264">หน่วยงานที่ออกรหัสประจำตัวของบุคคล</span><span class="sxs-lookup"><span data-stu-id="9985c-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="9985c-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="9985c-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="9985c-266">ตารางความสามารถ</span><span class="sxs-lookup"><span data-stu-id="9985c-266">Competency tables</span></span>

| <span data-ttu-id="9985c-267">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9985c-267">Name</span></span> | <span data-ttu-id="9985c-268">ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9985c-269">ชนิดทักษะ</span><span class="sxs-lookup"><span data-stu-id="9985c-269">Skill Type</span></span> | <span data-ttu-id="9985c-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="9985c-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="9985c-271">แบบจำลองความสัมพันธ์ตาราง</span><span class="sxs-lookup"><span data-stu-id="9985c-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="9985c-272">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-272">Worker</span></span>

![ผู้ปฏิบัติงาน](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="9985c-274">งานและตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-274">Job and Job Position</span></span>

![งานและตำแหน่งงาน](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="9985c-276">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="9985c-276">Benefits</span></span>

![สวัสดิการ](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="9985c-278">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="9985c-278">Compensation</span></span>

![ค่าตอบแทน](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="9985c-280">ออก</span><span class="sxs-lookup"><span data-stu-id="9985c-280">Leave</span></span>

![ออก](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="9985c-282">ปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="9985c-282">Work Calendar</span></span>

![ปฏิทินการทำงาน](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="9985c-284">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="9985c-284">See also</span></span>

[<span data-ttu-id="9985c-285">เลือกเทคโนโลยีการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9985c-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="9985c-286">ตั้งค่าคอนฟิกการรวม Dataverse</span><span class="sxs-lookup"><span data-stu-id="9985c-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="9985c-287">ตั้งค่าคอนฟิกตารางเสมือน Dataverse</span><span class="sxs-lookup"><span data-stu-id="9985c-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="9985c-288">FAQ เกี่ยวกับตารางเสมือนสำหรับ Human Resources</span><span class="sxs-lookup"><span data-stu-id="9985c-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="9985c-289">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="9985c-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="9985c-290">การอัปเดตศัพท์</span><span class="sxs-lookup"><span data-stu-id="9985c-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]