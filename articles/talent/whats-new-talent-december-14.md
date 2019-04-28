---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (14 ธันวาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/12/2019
ms.locfileid: "949862"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="cdec2-103">มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (14 ธันวาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="cdec2-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cdec2-104">**สร้าง 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="cdec2-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="cdec2-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="cdec2-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="cdec2-106">การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="cdec2-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="cdec2-107">การสนับสนุน US - ACA (Affordable Care Act) สำหรับปีภาษี 2018 ฟอร์ม 1095-B และ 1095-C</span><span class="sxs-lookup"><span data-stu-id="cdec2-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="cdec2-108">แต่ละปี Applicable Large Employers (ALEs) ต้องให้ 1095-C แก่พนักงานเต็มเวลาแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="cdec2-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="cdec2-109">นอกจากนี้ ถ้านายจ้างให้ความคุ้มครองแบบประกันด้วยตนเอง พวกเขาจะต้องให้ 1095-C (หากพวกเขาเป็น ALE) และ1095-B (หากพวกเขาเป็นนายจ้างขนาดเล็ก) ให้กับพนักงานใดๆ แบบเต็มเวลา หรือชั่วคราว โดยครอบคลุมภายใต้แผนใดแผนหนึ่งของสุขภาพที่เสนอให้</span><span class="sxs-lookup"><span data-stu-id="cdec2-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="cdec2-110">คุณลักษณะนี้แสดงแบบฟอร์มที่สามารถพิมพ์ได้สำหรับทั้ง 1095-C และ 1095-B</span><span class="sxs-lookup"><span data-stu-id="cdec2-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="cdec2-111">ในระหว่างการนำเข้า ฟิลด์ SubmittedByPersonId บน HcmPerfJournalEntity จะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="cdec2-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="cdec2-112">เมื่อนำเข้า/ส่งออกรายการสมุดรายวันประสิทธิภาพ ฟิลด์ **ส่งโดย** จะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="cdec2-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="cdec2-113">ด้วยการเปลี่ยนแปลงนี้ ค่า **ที่นำเข้า/ที่ส่งออก** จะสะท้อนถึงค่าในตารางในระหว่างการส่งออก เมื่อนำเข้า ระบบจะถูกปรับปรุงด้วยค่าที่ระบุในไฟล์การนำเข้า</span><span class="sxs-lookup"><span data-stu-id="cdec2-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="cdec2-114">แท็บการวิเคราะห์บนพื้นที่ทำงาน 'การลางานและการขาดงาน' แสดงข้อผิดพลาด "OpenConnectionError" สำหรับบทบาทผู้ดูแลที่ไม่ใช่ระบบ</span><span class="sxs-lookup"><span data-stu-id="cdec2-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="cdec2-115">ด้วยการอัพเดตนี้ ไม่มีการออกข้อผิดพลาดใดๆ เมื่อเปิดแท็บ **การวิเคราะห์** บนพื้นที่ทำงาน **การลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="cdec2-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="cdec2-116">การบริการตนเองของพนักงาน ลำดับชั้นของตำแหน่งที่เลื่อนจากไทล์ล้มเหลวในการเรียกโหนดหลัก</span><span class="sxs-lookup"><span data-stu-id="cdec2-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="cdec2-117">มีการทำการเปลี่ยนแปลงเพื่อแก้ไขข้อผิดพลาด "การเรียกโหนดหลักล้มเหลว" เมื่อลำดับชั้นของตำแหน่งได้ถูกกำหนดเป็นแบบส่วนบุคคลให้ปรากฏในพื้นที่ทำงานที่มีอยู่ และมีการเลือกตำแหน่งในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="cdec2-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="cdec2-118">ต้องเป็นผู้ดูแลระบบ เมื่อต้องการดูแท็บค่าจ้างในหน้าของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="cdec2-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="cdec2-119">มีการทำการเปลี่ยนแปลงเพื่อรวมองค์ประกอบความปลอดภัยที่ถูกต้องในสิทธิ์ที่มีอยู่: "รักษารายละเอียดค่าจ้าง ผู้ปฏิบัติงาน และตำแหน่ง"</span><span class="sxs-lookup"><span data-stu-id="cdec2-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="cdec2-120">ด้วยการเปลี่ยนแปลงนี้ ตามค่าเริ่มต้น ผู้ดูแลค่าจ้างจะสามารถเข้าถึงฟิลด์ค่าจ้างได้ในหน้าตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="cdec2-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="cdec2-121">ข้อผิดพลาดเมื่อส่งตรวจทานประสิทธิภาพการทำงานกับผู้จัดการ และตัวยึดตำแหน่ง %Reviews.PerfPeriod% ถูกใช้ในคำแนะนำการส่ง</span><span class="sxs-lookup"><span data-stu-id="cdec2-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="cdec2-122">มีการทำการเปลี่ยนแปลงที่แก้ไขข้อผิดพลาด "การอ้างอิง Null" เมื่อใช้ตัวยึดตำแหน่ง %Reviews.PerfPeriod% ในคำแนะนำการส่ง</span><span class="sxs-lookup"><span data-stu-id="cdec2-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="cdec2-123">รายงาน Power BI ของพนักงานแสดงข้อผิดพลาด เมื่อวันที่อาวุโสของพนักงานคือวันอธิกสุรทิน</span><span class="sxs-lookup"><span data-stu-id="cdec2-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="cdec2-124">ด้วยการเปลี่ยนแปลงนี้ ขณะนี้วันอธิกสุรทินได้รับการสนับสนุนใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cdec2-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="cdec2-125">การรวมระหว่าง Core HR และ Attract</span><span class="sxs-lookup"><span data-stu-id="cdec2-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="cdec2-126">มีการทำการเปลี่ยนแปลงเพื่อปรับปรุงการรวมระหว่าง Core HR และ Attract ที่เกี่ยวข้องกับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="cdec2-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="cdec2-127">สำหรับผู้สมัครที่จะจ้างงานที่จะปรากฏให้เห็นในพื้นที่ทำงาน **การจัดการบุคลากร** เอนทิตี Common Data Service ต่อไปนี้จะถูกใช้:</span><span class="sxs-lookup"><span data-stu-id="cdec2-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="cdec2-128">ใบสมัครงาน</span><span class="sxs-lookup"><span data-stu-id="cdec2-128">Job Application</span></span>
- <span data-ttu-id="cdec2-129">เหตุผลของสถานะต้องถูกตั้งค่าเป็น มีการยอมรับข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="cdec2-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="cdec2-130">แสดงผู้สมัครและงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="cdec2-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="cdec2-131">ผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="cdec2-131">Candidate</span></span>
-   <span data-ttu-id="cdec2-132">แสดงข้อมูลของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="cdec2-132">Provides Candidate information</span></span>

<span data-ttu-id="cdec2-133">งานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="cdec2-133">Job Opening</span></span>
-   <span data-ttu-id="cdec2-134">แสดงรหัสงานที่เปิดและผู้เข้าร่วมในงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="cdec2-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="cdec2-135">ผู้เข้าร่วมในงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="cdec2-135">Job Opening Participants</span></span>
-   <span data-ttu-id="cdec2-136">แสดงผู้จัดการที่ว่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="cdec2-136">Provides Hiring Manager</span></span>

<span data-ttu-id="cdec2-137">เมื่อมีการเพิ่มผู้สมัครไปยังการจัดการบุคลากร ขณะนี้ผู้สมัครสามารถถูกยกเลิกได้โดยใช้ตัวเลือกใหม่ที่พร้อมใช้งานบนบัตรผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="cdec2-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="cdec2-138">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="cdec2-139">การลางานและการขาดงาน: การลางานในอนาคตและการคาดการณ์ยอดดุลการลางาน</span><span class="sxs-lookup"><span data-stu-id="cdec2-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="cdec2-140">ด้วยการเปลี่ยนแปลงที่ทำเพื่ออนุญาตให้พนักงานสามารถคาดการณ์เวลาหยุดพักและคำขอเวลาหยุดพักในอนาคตที่ร้องขอได้ โดยไม่มีผลกระทบต่อยอดดุลเวลาหยุดพักปัจจุบันของพวกเขา วิธีที่ยอดดุลเวลาหยุดพักแสดงขึ้นก็ยังมีการเปลี่ยนแปลงด้วย</span><span class="sxs-lookup"><span data-stu-id="cdec2-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="cdec2-141">ยอดดุลที่พร้อมใช้งานที่แสดงอยู่ในขณะนี้คือจำนวนเวลาหยุดพักที่พร้อมใช้งานสำหรับการร้องขอ ที่รวมถึงการรับรู้ตลอดวันนี้และคำขอลางานที่ได้รับอนุมัติทั้งหมดจนสิ้นสุดรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="cdec2-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="cdec2-142">เมื่อความสามารถในการคาดการณ์ถูกนำออกใช้ ยอดดุลที่แสดงจะเปลี่ยนแปลงไปเป็นยอดดุลปัจจุบันของเวลาหยุดพักซึ่งรวมถึงการรับรู้ตลอดวันนี้และการร้องขอตลอดวันนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="cdec2-143">พนักงานและผู้จัดการจะเห็นยอดดุลที่ปรับปรุงเหล่านี้ในระบบบริการตนเองของผู้จัดการและพนักงานในบัตร **เวลาหยุดพัก** และในหน้าต่าง **ยอดดุลเวลาหยุดพัก**</span><span class="sxs-lookup"><span data-stu-id="cdec2-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="cdec2-144">ผู้จัดการฝ่าย HR จะเห็นยอดดุลที่ปรับปรุงเหล่านี้ในพื้นที่ทำงาน **บุคลากร** และในหน้าต่าง **แผนการลางานที่กำหนด** ของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="cdec2-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="cdec2-145">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="cdec2-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="cdec2-146">การแม็ปข้อผิดพลาดในการรวมกับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cdec2-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="cdec2-147">มีการตรวจพบปัญหาต่อไปนี้ในเท็มเพลตปัจจุบันสำหรับการรวม Talent กับ Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cdec2-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="cdec2-148">เท็มเพลตใหม่จะเผยแพร่เร็วๆ นี้ และจะใช้กับโครงการการรวมใหม่ทั้งหมดที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="cdec2-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="cdec2-149">สำหรับโครงการการรวมที่มีอยู่ สามารถปรับปรุงการแม็ปงานได้</span><span class="sxs-lookup"><span data-stu-id="cdec2-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="cdec2-150">โปรดอ้างอิงตารางต่อไปนี้สำหรับการแม็ปที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="cdec2-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="cdec2-151">ตำแหน่งงานไปยังงานกำหนดงานหลักของตำแหน่งจะไม่รวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cdec2-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="cdec2-152">นี่เป็นปัญหาที่มีอยู่ในขณะนี้กำลังทำการวิจัย</span><span class="sxs-lookup"><span data-stu-id="cdec2-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="cdec2-153">ไม่มีวิธีการแก้ไขปัญหาในการแม็ปปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="cdec2-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="cdec2-154">งานของแผนกไปยังหน่วยปฏิบัติงาน จำเป็นต้องปรับปรุงการแม็ปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="cdec2-155">ฟิลด์ต้นทางที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="cdec2-155">Existing source field</span></span>          | <span data-ttu-id="cdec2-156">ฟิลด์ต้นทางใหม่</span><span class="sxs-lookup"><span data-stu-id="cdec2-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="cdec2-157">cdm_description (คำอธิบาย)</span><span class="sxs-lookup"><span data-stu-id="cdec2-157">cdm_description (Description)</span></span>  | <span data-ttu-id="cdec2-158">cdm_name (ชื่อ)</span><span class="sxs-lookup"><span data-stu-id="cdec2-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="cdec2-159">การแม็ปเพิ่มเติมยังต้องการจะถูกเพิ่มด้วย</span><span class="sxs-lookup"><span data-stu-id="cdec2-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="cdec2-160">เลือกฟิลด์ **ไม่มี** ล่าสุด เพื่อเพิ่มการแม็ปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="cdec2-161">ฟิลด์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="cdec2-161">Source field</span></span>                   | <span data-ttu-id="cdec2-162">ฟิลด์ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="cdec2-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="cdec2-163">cdm_description (คำอธิบาย)</span><span class="sxs-lookup"><span data-stu-id="cdec2-163">cdm_description (Description)</span></span>  | <span data-ttu-id="cdec2-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="cdec2-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="cdec2-165">การแม็ปที่ปรับปรุงแล้วควรมีลักษณะดังภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-165">The updated mappings should look like the following image.</span></span>

![งานของแผนกไปยังหน่วยปฏิบัติงาน](./media/DepartmentMapping.png)


<span data-ttu-id="cdec2-167">งานไปยังงานรายละเอียดงาน จำเป็นต้องปรับปรุงการแม็ปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="cdec2-168">ฟิลด์แหล่งข้อมูลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="cdec2-168">Existing source field</span></span>          | <span data-ttu-id="cdec2-169">ฟิลด์ต้นทางใหม่</span><span class="sxs-lookup"><span data-stu-id="cdec2-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="cdec2-170">cdm_name (ชื่อ)</span><span class="sxs-lookup"><span data-stu-id="cdec2-170">cdm_name (Name)</span></span>                | <span data-ttu-id="cdec2-171">cdm_description (คำอธิบาย)</span><span class="sxs-lookup"><span data-stu-id="cdec2-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="cdec2-172">ชื่อ (คำอธิบาย)</span><span class="sxs-lookup"><span data-stu-id="cdec2-172">cdm_name (Description)</span></span>         | <span data-ttu-id="cdec2-173">cdm_jobdescription(คำอธิบายงาน)</span><span class="sxs-lookup"><span data-stu-id="cdec2-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="cdec2-174">การแม็ปที่ปรับปรุงแล้วควรมีลักษณะดังภาพด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cdec2-174">The updated mappings should look like the image below.</span></span>

![งานไปยังงานรายละเอียดงาน](./media/JobMapping.png)

<span data-ttu-id="cdec2-176">งานผู้ปฏิบัติงานไปยังงาน จำเป็นต้องปรับปรุงการแม็ปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="cdec2-177">ฟิลด์แหล่งข้อมูลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="cdec2-177">Existing source field</span></span>                 | <span data-ttu-id="cdec2-178">ฟิลด์ต้นทางใหม่</span><span class="sxs-lookup"><span data-stu-id="cdec2-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="cdec2-179">cdm_emailaddress1 (ที่อยู่อีเมล 1)</span><span class="sxs-lookup"><span data-stu-id="cdec2-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="cdec2-180">cdm_primaryemailaddress (ที่อยู่อีเมลหลัก)</span><span class="sxs-lookup"><span data-stu-id="cdec2-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="cdec2-181">cdm_telephone1 (โทรศัพท์ 1)</span><span class="sxs-lookup"><span data-stu-id="cdec2-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="cdec2-182">cdm_primarytelephone (โทรศัพท์หลัก)</span><span class="sxs-lookup"><span data-stu-id="cdec2-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="cdec2-183">การแปลงฟิลด์เพศยังจำเป็นต้องได้รับการอัพเดตด้วย</span><span class="sxs-lookup"><span data-stu-id="cdec2-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="cdec2-184">เลือกชนิดแม็ป **fn** (ฟังก์ชัน) สำหรับเพศ และปรับปรุงการแม็ปค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="cdec2-185">ค่า Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cdec2-185">Common Data Service value</span></span>                   | <span data-ttu-id="cdec2-186">ค่า Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cdec2-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="cdec2-187">75440000</span><span class="sxs-lookup"><span data-stu-id="cdec2-187">75440000</span></span>                    | <span data-ttu-id="cdec2-188">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="cdec2-188">Male</span></span>                                             |
| <span data-ttu-id="cdec2-189">75440001</span><span class="sxs-lookup"><span data-stu-id="cdec2-189">75440001</span></span>                    | <span data-ttu-id="cdec2-190">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="cdec2-190">Female</span></span>                                           |
| <span data-ttu-id="cdec2-191">75440002</span><span class="sxs-lookup"><span data-stu-id="cdec2-191">75440002</span></span>                    | <span data-ttu-id="cdec2-192">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="cdec2-192">None</span></span>                                             | 
| <span data-ttu-id="cdec2-193">75440003</span><span class="sxs-lookup"><span data-stu-id="cdec2-193">75440003</span></span>                    | <span data-ttu-id="cdec2-194">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="cdec2-194">NonSpecific</span></span>                                      |

<span data-ttu-id="cdec2-195">แม็ปที่ปรับปรุงแล้วควรมีลักษณะดังภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cdec2-195">The updated mappings should look like the following images.</span></span>

![ผู้ปฏิบัติงานไปยังงานของผู้ปฏิบัติงาน](./media/WorkerMapping.png)

![การแปลงฟิลด์เพศ](./media/WorkerTransform.png)
