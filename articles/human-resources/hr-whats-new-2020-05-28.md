---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (28 พฤษภาคม 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 28 พฤษภาคม 2020
author: andreabichsel
manager: tfehr
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e8d7f87f30286eefa1b3b53925702f4735132e6
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465281"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="55e2b-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (28 พฤษภาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="55e2b-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="55e2b-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="55e2b-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="55e2b-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3287</span><span class="sxs-lookup"><span data-stu-id="55e2b-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="55e2b-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="55e2b-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="55e2b-107">เอนทิตี LeaveRequest ไม่ทำงาน เมื่อคุณเปิดใช้งานหลายชนิดต่อแผนการลางาน (447498)</span><span class="sxs-lookup"><span data-stu-id="55e2b-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="55e2b-108">เมื่อมีการเปลี่ยนแปลงนี้ ขณะนี้ **LeaveEnrollmentV2Entity** พร้อมใช้งานเมื่อต้องการแก้ไขข้อผิดพลาดที่เกิดขึ้น เมื่อคุณเปิดใช้งานชนิดการลางานหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="55e2b-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="55e2b-109">ลักษณะการทำงานของการลดการขัดแย้งของชุดงาน (ตัวอย่าง) (446619)</span><span class="sxs-lookup"><span data-stu-id="55e2b-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="55e2b-110">เมื่อคุณเปิดใช้งานลักษณะการทำงานนี้ คุณสามารถคาดการณ์การลดในการบล็อคในตารางกรอบงานชุดงานได้ ในขณะที่เลือกงานและทำงานให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="55e2b-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="55e2b-111">UpdateConflict ขณะบันทึก ผู้ปฏิบัติงานป้องกันการแก้ไขเรกคอร์ดในบุคคล (427915)</span><span class="sxs-lookup"><span data-stu-id="55e2b-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="55e2b-112">การเปลี่ยนแปลงนี้จะแก้ไขข้อผิดพลา เมื่อเพิ่มผู้ปฏิบัติงานใหม่ การอัปเดตข้อมูลที่อยู่ และการเปลี่ยนแปลงการตั้งค่าภาษา</span><span class="sxs-lookup"><span data-stu-id="55e2b-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="55e2b-113">ในสถานการณ์จำลองที่ไม่ซ้ำกันนี้ ข้อผิดพลาดที่แสดงบ่งชี้ว่าเรกคอร์ดไม่สามารถอัปเดตได้</span><span class="sxs-lookup"><span data-stu-id="55e2b-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="55e2b-114">ไม่สามารถเพิ่มเอกสารแนบให้คำขอการลางานที่ได้รับอนุมัติส่งได้อีกครั้ง (425407)</span><span class="sxs-lookup"><span data-stu-id="55e2b-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="55e2b-115">การเปลี่ยนแปลงนี้จะอนุญาตให้มีเอกสารแนบเพื่ออนุมัติคำขอลางานแล้ว</span><span class="sxs-lookup"><span data-stu-id="55e2b-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="55e2b-116">ผู้ใช้สามารถป้อนค่าตอบแทนสำหรับพนักงานในฟอร์มนิติบุคคลอื่น (409529)</span><span class="sxs-lookup"><span data-stu-id="55e2b-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="55e2b-117">การเปลี่ยนแปลงนี้ปิดใช้งานตัวเลือกค่าตอบแทน เพื่อป้องกันไม่ให้มีการป้อนข้อมูลค่าตอบแทนโดยไม่ได้ตั้งใจสำหรับนิติบุคคลที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="55e2b-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="55e2b-118">เกิดข้อผิดพลาดเมื่อคุณโอนย้ายพนักงาน และวันที่กำหนดตำแหน่งของผู้ปฏิบัติงานอยู่ก่อนช่วงเวลาของตำแหน่งงาน (429402)</span><span class="sxs-lookup"><span data-stu-id="55e2b-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="55e2b-119">ข้อความแสดงข้อผิดพลาด เมื่อการโอนย้ายพนักงานในสถานการณ์นี้ได้รับการอัปเดตเพื่ออธิบายถึงการเปลี่ยนแปลงที่จำเป็นในการแก้ไขปัญหาให้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="55e2b-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="55e2b-120">ความสามารถของเอกสารแนบในการลงทะเบียนสวัสดิการการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="55e2b-121">ขณะนี้คุณสามารถเพิ่มเอกสารแนบระหว่างกระบวนการลงทะเบียนสวัสดิการ สำหรับแต่ละแผนงานที่มีการลงทะเบียนของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="55e2b-122">คุณสามารถดูเอกสารแนบภายในฟอร์ม **สวัสดิการของผู้ปฏิบัติงานลงทะเบียนไว้**</span><span class="sxs-lookup"><span data-stu-id="55e2b-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="55e2b-123">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="55e2b-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="55e2b-124">โปรแกรมประบุกต์ Human Resources ใน Teams</span><span class="sxs-lookup"><span data-stu-id="55e2b-124">Human Resources application in Teams</span></span>

<span data-ttu-id="55e2b-125">พนักงานสามารถดูและร้องขอเวลานอกการทำงานภายใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="55e2b-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="55e2b-126">ผู้ใช้สามารถโต้ตอบกับบอท เพื่อสร้างคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="55e2b-127">สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](https://go.microsoft.com/fwlink/?linkid=2127841)</span><span class="sxs-lookup"><span data-stu-id="55e2b-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="55e2b-128">การระงับการลางาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-128">Leave suspension</span></span>

<span data-ttu-id="55e2b-129">คุณสามารถระงับการลางานและการขาดงานในทรัพยากรบุคคลสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="55e2b-130">การระงับการลางานจะหยุดการรับรู้การลางานสำหรับชนิดการลางานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="55e2b-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="55e2b-131">ถ้าการระงับเกิดขึ้นหลังจากที่มีการประมวลผลการรับรู้ การระงับการลางานจะสร้างการปรับปรุงตามสัดส่วนให้กับยอดดุลการลางานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="55e2b-132">สำหรับข้อมูลเพิ่มเติม โปรดดู [ระงับการลางาน](hr-leave-and-absence-suspend-leave.md)</span><span class="sxs-lookup"><span data-stu-id="55e2b-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="55e2b-133">อัพเดตประสบการณ์ผู้ใช้เพื่อบ่งชี้ว่ารายการคงค้างถูกระงับแล้ว (429550)</span><span class="sxs-lookup"><span data-stu-id="55e2b-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="55e2b-134">ประสบการณ์ผู้ใช้บ่งชี้ว่าการคงค้างถูกระงับสำหรับแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="55e2b-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="55e2b-135">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="55e2b-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="55e2b-136">การบันทึกฐานข้อมูล (ในการแสดงตัวอย่างในเดือนมิถุนายน)</span><span class="sxs-lookup"><span data-stu-id="55e2b-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="55e2b-137">ลักษณะการทำงานการบันทึกฐานข้อมูลจะช่วยให้คุณสามารถกำหนดตารางและฟิลด์ที่ควรตรวจสอบได้</span><span class="sxs-lookup"><span data-stu-id="55e2b-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="55e2b-138">นอกจากนี้ยังช่วยให้คุณสามารถกำหนดเหตุการณ์ที่ควรทริกเกอร์การติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="55e2b-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="55e2b-139">ความสามารถในการสอบถามจะพร้อมใช้งานเพื่อดูการเปลี่ยนแปลงเหล่านี้เมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="55e2b-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="55e2b-140">การซื้อและการขายการลางาน (ในการแสดงตัวอย่างวันที่ 1มิถุนายน)</span><span class="sxs-lookup"><span data-stu-id="55e2b-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="55e2b-141">บางองค์กรจะให้สวัสดิการ ซึ่งช่วยให้พนักงานสามารถซื้อหรือขายการลางานของพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="55e2b-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="55e2b-142">กระบวนการนี้มักจะมีการจัดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="55e2b-142">This process is often managed manually.</span></span> <span data-ttu-id="55e2b-143">ลักษณะการทำงานนี้จะช่วยให้คุณสามารถจัดการนโยบายและคำร้องขอแผนก HR โดยอัตโนมัติได้มากขึ้น และจะช่วยลดข้อผิดพลาด ขณะดำเนินการจัดการลางาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="55e2b-144">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="55e2b-144">For more information, see:</span></span>

- [<span data-ttu-id="55e2b-145">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="55e2b-146">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="55e2b-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="55e2b-147">เอนทิตีกรอบงานการจัดการข้อมูล (DMF) สำหรับการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="55e2b-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="55e2b-148">เอนทิตีการจัดการสวัสดิการกำลังนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="55e2b-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="55e2b-149">เอนทิตี DMF อนุญาตการนำเข้าและส่งออกข้อมูล เพื่อตั้งค่าคอนฟิกการจัดการสวัสดิการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="55e2b-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="55e2b-150">แม่แบบการจัดการสวัสดิการจะพร้อมใช้งานเพื่อย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="55e2b-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="55e2b-151">แม่แบบส่งออกและนำเข้าข้อมูลในลักษณะตามลำดับตามการอ้างอิงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="55e2b-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="55e2b-152">เพิ่มรหัสเหตุผลให้กับการระงับการคงค้าง (วันที่ 1 มิถุนายน)</span><span class="sxs-lookup"><span data-stu-id="55e2b-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="55e2b-153">รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="55e2b-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="55e2b-154">กฎการยกยอดดุล (วันที่ 1 มิถุนายน)</span><span class="sxs-lookup"><span data-stu-id="55e2b-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="55e2b-155">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="55e2b-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="55e2b-156">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="55e2b-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="55e2b-157">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="55e2b-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="55e2b-158">ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ (วันที่ 1 มิถุนายน)</span><span class="sxs-lookup"><span data-stu-id="55e2b-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="55e2b-159">ในรุ่นนี้ HR สามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ยังไม่ได้ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="55e2b-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="55e2b-160">การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น</span><span class="sxs-lookup"><span data-stu-id="55e2b-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="55e2b-161">คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="55e2b-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="55e2b-162">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง (วันที่ 1 มิถุนายน)</span><span class="sxs-lookup"><span data-stu-id="55e2b-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="55e2b-163">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="55e2b-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="55e2b-164">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="55e2b-164">See also</span></span>

[<span data-ttu-id="55e2b-165">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="55e2b-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="55e2b-166">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="55e2b-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="55e2b-167">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="55e2b-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="55e2b-168">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="55e2b-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]