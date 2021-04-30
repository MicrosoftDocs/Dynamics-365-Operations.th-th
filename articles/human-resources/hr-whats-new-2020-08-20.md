---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (20 สิงหาคม 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 20 สิงหาคม 2020
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 95ffe90795b9781408607257f3f63bf68c489b56
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891828"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="49fcc-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources (20 สิงหาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="49fcc-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="49fcc-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="49fcc-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="49fcc-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3478</span><span class="sxs-lookup"><span data-stu-id="49fcc-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="49fcc-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุน Lifecycle Services (LCS) สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="49fcc-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="49fcc-107">แสดงข้อมูลการลางานและการขาดงานที่กำลังจะเกิดขึ้นและที่ค้างอยู่ของบัตรในพื้นที่ทำงานของบุคคล</span><span class="sxs-lookup"><span data-stu-id="49fcc-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="49fcc-108">มีตัวเลือกคำขอการลางานและการขาดงานที่กำลังจะเกิดขึ้นและที่ค้างอยู่ในบัตรการลางานและการขาดงานในพื้นที่ทำงานของ **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="49fcc-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="49fcc-109">ฟิลด์ส่วนตัวไม่ได้เป็นค่า ใช่ โดยค่าเริ่มต้นสำหรับบทบาทพนักงานในระบบบริการตนเองของพนักงาน (477106)</span><span class="sxs-lookup"><span data-stu-id="49fcc-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="49fcc-110">ตอนนี้ฟิลด์ **ส่วนตัว** มีค่าเริ่มต้นเป็น **ใช่** เมื่อพนักงานเพิ่มเรกคอร์ดที่อยู่ใหม่ผ่านหน้า **ข้อมูลส่วนบุคคล** ในระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="49fcc-111">แท็บด่วนผู้สมัครที่จะจ้างในการจัดการบุคลากรแสดงจำนวนของผู้สมัครที่ไม่ถูกต้อง (470110)</span><span class="sxs-lookup"><span data-stu-id="49fcc-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="49fcc-112">ตอนนี้หน้า **การจัดการบุคลากร** สามารถแสดงจำนวนผู้สมัครที่จะจ้างได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="49fcc-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="49fcc-113">ไม่สามารถป้อนการลาป่วยสำหรับพนักงานที่ออกไปแล้วเมื่อมีการตั้งค่ารายการคงค้างเป็นศูนย์ (446195)</span><span class="sxs-lookup"><span data-stu-id="49fcc-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="49fcc-114">ขณะนี้อนุญาตให้ใช้ธุรกรรมการลางานสำหรับพนักงานที่ออกไปแล้วในอนาคตและตั้งค่ารายการคงค้างเป็นศูนย์แล้ว</span><span class="sxs-lookup"><span data-stu-id="49fcc-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="49fcc-115">ธุรกรรมการลางานสามารถป้อนได้จนถึงวันที่สิ้นสุดการจ้างงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="49fcc-116">การเพิ่มฟิลด์ที่กำหนดเองให้กับแบบฟอร์มผู้ปฏิบัติงานใหม่จะปิดใช้งานฟิลด์ในบานหน้าต่างการดำเนินการสำหรับ จัดการการลางาน (473314)</span><span class="sxs-lookup"><span data-stu-id="49fcc-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="49fcc-117">ตัวเลือกบานหน้าต่างการดำเนินการในแบบฟอร์ม **ผู้ปฏิบัติงาน** ใหม่ใน **จัดการการลางาน** จะไม่สามารถปิดใช้งานได้อีกต่อไปถ้ามีการเพิ่มฟิลด์ที่กำหนดเองลงในแบบฟอร์ม **ผู้ปฏิบัติงาน** ใหม่</span><span class="sxs-lookup"><span data-stu-id="49fcc-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="49fcc-118">การทำให้ฟิลด์ข้อคิดเห็นการลางานเป็นบังคับจะอนุญาตให้มีการส่งคำขอลางานเมื่อไม่มีการป้อนข้อคิดเห็น (473543)</span><span class="sxs-lookup"><span data-stu-id="49fcc-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="49fcc-119">ในขณะนี้ฟิลด์ข้อคิดเห็นสามารถเป็นบังคับและคำขอลางานใช้การตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="49fcc-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="49fcc-120">ฟิลด์บังคับเป็นคุณลักษณะรุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="49fcc-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="49fcc-121">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="49fcc-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="49fcc-122">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="49fcc-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="49fcc-123">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="49fcc-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="49fcc-124">ฟิลด์บังคับ</span><span class="sxs-lookup"><span data-stu-id="49fcc-124">Mandatory fields</span></span>

<span data-ttu-id="49fcc-125">คุณสามารถทำให้ฟิลด์บังคับโดยใช้ความสามารถในการตั้งค่าส่วนบุคคลของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="49fcc-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="49fcc-126">ลักษณะการทำงานนี้จำเป็นต้องใช้ **มุมมองที่บันทึกไว้**</span><span class="sxs-lookup"><span data-stu-id="49fcc-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="49fcc-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมุมมองที่บันทึกไว้ ให้ดูที่:</span><span class="sxs-lookup"><span data-stu-id="49fcc-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="49fcc-128">[มุมมองที่บันทึกไว้ - มีความพร้อมใช้งานทั่วไป](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 2</span><span class="sxs-lookup"><span data-stu-id="49fcc-128">[Saved views - general availability](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="49fcc-129">สร้างแบบฟอร์มที่ใช้มุมมองที่บันทึกไว้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="49fcc-129">Build forms that fully utilize saved views</span></span>](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="49fcc-130">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="49fcc-130">Human Resources application in Teams</span></span>

<span data-ttu-id="49fcc-131">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="49fcc-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="49fcc-132">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="49fcc-133">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="49fcc-133">For more information, see:</span></span>

- <span data-ttu-id="49fcc-134">[การใช้งานการลางานและการขาดงานของพนักงานใน Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) ในแผน Dynamics 365 การนำออกใช้ 2020 เวฟ 1</span><span class="sxs-lookup"><span data-stu-id="49fcc-134">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="49fcc-135">แอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="49fcc-135">Human Resources app in Teams</span></span>](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a><span data-ttu-id="49fcc-136">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="49fcc-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="49fcc-137">คุณลักษณะรุ่นพรีวิวของแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="49fcc-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="49fcc-138">**การแจ้งเตือน**: ผู้ส่งและผู้อนุมัติที่ส่งคำขอการลาหยุดจะได้รับการแจ้งเตือนในแอป Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="49fcc-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="49fcc-139">ผู้อนุมัติจะสามารถอนุมัติหรือปฏิเสธคำขอการลาหยุด และผู้ส่งจะได้รับการแจ้งเตือนถ้าคำขอได้รับการอนุมัติหรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="49fcc-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="49fcc-140">**ปฏิทินการลาหยุดของผู้จัดการ**: ผู้จัดการจะสามารถดูการลาหยุดที่อนุมัติและที่ค้างอยู่สำหรับผู้ใต้บังคับบัญชาโดยตรงของตนในมุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="49fcc-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="49fcc-141">มุมมองนี้จะทำให้เข้าใจง่ายเมื่อสมาชิกในทีมของตนไม่มาทำงาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="49fcc-142">เอนทิตีรายการตรวจสอบที่รวมอยู่ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="49fcc-142">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="49fcc-143">เอนทิตีรายการตรวจสอบสำหรับการเตรียมความพร้อม ปัจฉิมนิเทศ การโอนย้าย และกระบวนการทางธุรกิจ จะพร้อมใช้งานเร็วๆ นี้ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="49fcc-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="49fcc-144">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="49fcc-144">Known issues</span></span>

<span data-ttu-id="49fcc-145">พื้นที่ทำงาน **การจัดการคุณลักษณะ** อาจแสดงคุณลักษณะที่ถูกปิดใช้งานจากการเป็นคุณลักษณะรุ่นพรีวิวเมื่อมีความพร้อมใช้งานทั่วไป</span><span class="sxs-lookup"><span data-stu-id="49fcc-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="49fcc-146">ด้านล่างนี้เป็นรายการของคุณลักษณะที่พร้อมใช้งานโดยทั่วไปที่แสดงสถานะที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="49fcc-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="49fcc-147">การจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="49fcc-147">Benefits management</span></span>
- <span data-ttu-id="49fcc-148">การจัดการกรณี</span><span class="sxs-lookup"><span data-stu-id="49fcc-148">Case management</span></span>
- <span data-ttu-id="49fcc-149">การลงบันทึกฐานข้อมูล (การตรวจสอบ)</span><span class="sxs-lookup"><span data-stu-id="49fcc-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="49fcc-150">การลางานคงค้างสำหรับบริษัทเดียวหรือแผนเดียว</span><span class="sxs-lookup"><span data-stu-id="49fcc-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="49fcc-151">การระงับการยกยอดวันลาและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="49fcc-152">รหัสเหตุผลการปรับปรุงยอดคงเหลือและความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="49fcc-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="49fcc-153">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-153">Buy and sell leave</span></span>
- <span data-ttu-id="49fcc-154">ปฏิทินการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-154">Leave and absence calendar</span></span>
- <span data-ttu-id="49fcc-155">กฎการยกยอดไปของการลางาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="49fcc-156">การตรวจสอบการลางานคงค้าง</span><span class="sxs-lookup"><span data-stu-id="49fcc-156">Leave accrual auditing</span></span>
- <span data-ttu-id="49fcc-157">การลบการลางานคงค้าง</span><span class="sxs-lookup"><span data-stu-id="49fcc-157">Leave accrual deletion</span></span>
- <span data-ttu-id="49fcc-158">การปัดเศษการลางานคงค้าง</span><span class="sxs-lookup"><span data-stu-id="49fcc-158">Leave accrual rounding</span></span>
- <span data-ttu-id="49fcc-159">ตั้งค่าคอนฟิกชนิดการลางานหลายรายการแผนการลางานเดียว</span><span class="sxs-lookup"><span data-stu-id="49fcc-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="49fcc-160">อัพเดตการปรับปรุงเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="49fcc-160">Update time-off enhancements</span></span>
- <span data-ttu-id="49fcc-161">ใช้ FTE ของพนักงานสำหรับรายการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="49fcc-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="49fcc-162">มุมมองค่าตอบแทนข้ามบริษัท</span><span class="sxs-lookup"><span data-stu-id="49fcc-162">Cross company compensation view</span></span>
- <span data-ttu-id="49fcc-163">พิมพ์การตรวจทานประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="49fcc-163">Print performance reviews</span></span>
- <span data-ttu-id="49fcc-164">การแก้ไขวันหยุดคงค้างของการลางาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="49fcc-165">เอนทิตี้พนักงานในแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="49fcc-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="49fcc-166">เมื่อเร็วๆ นี้เราได้ค้นพบสองประเด็นเกี่ยวกับเอนทิตี้ **BenefitsPlanEmployee**</span><span class="sxs-lookup"><span data-stu-id="49fcc-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="49fcc-167">เมื่อมีการนำเข้าการลงทะเบียนของผู้ปฏิบัติงาน **รหัสความคุ้มครอง** และ **รหัสชนิดของแผน** จะตั้งค่าอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="49fcc-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="49fcc-168">ปัญหานี้ทำให้แผนสวัสดิการของพนักงานแสดงอย่างไม่ถูกต้องในแบบฟอร์ม **แผนสวัสดิการของผู้ปฏิบัติงาน** และในแบบฟอร์ม **การลงทะเบียนที่เปิด** ในระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="49fcc-169">นอกจากนี้ ปัญหานี้อาจส่งผลกระทบต่อความสามารถของพนักงานในการเลือกแผนในระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="49fcc-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="49fcc-170">ตอนนี้ยังไม่มีวิธีการแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="49fcc-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="49fcc-171">เรากำลังให้ความสำคัญอย่างสูงกับการแก้ไขปัญหานี้และจะนำเสนอวิธีแก้ไขในการเผยแพร่ถัดไปของเรา</span><span class="sxs-lookup"><span data-stu-id="49fcc-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="49fcc-172">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="49fcc-172">See also</span></span>

[<span data-ttu-id="49fcc-173">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="49fcc-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="49fcc-174">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="49fcc-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="49fcc-175">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="49fcc-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="49fcc-176">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="49fcc-176">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]