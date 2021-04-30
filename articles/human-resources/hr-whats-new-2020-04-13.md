---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (13 เมษายน 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 13 เมษายน 2020
author: andreabichsel
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 93873707703ce7148c353735ce1abce795796a5e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892020"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="132f8-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (13 เมษายน 2020)</span><span class="sxs-lookup"><span data-stu-id="132f8-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="132f8-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="132f8-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="132f8-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3136</span><span class="sxs-lookup"><span data-stu-id="132f8-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="132f8-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="132f8-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="132f8-107">ระยะความถี่การนำออกใช้ของการผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="132f8-107">New production release cadence</span></span>

<span data-ttu-id="132f8-108">ด้วยการนำออกใช้ของสัปดาห์นี้ ระยะความถี่การนำออกใช้สำหรับ Human Resources จะเลื่อนจากการปรับปรุงรายสัปดาห์เป็นการปรับปรุงรายสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="132f8-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="132f8-109">เพื่อให้แน่ใจว่ามีความสอดคล้องกับแนวทางปฏิบัติในการปรับใช้งานที่ปลอดภัยและรักษามาตรฐานที่สูงของความมั่นคงและความน่าเชื่อถือในบริการ กระบวนการของการปรับใช้งานการอัปเดตบริการในภูมิภาคทั้งหมดเป็นการเปิดตัวสองสัปดาห์ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="132f8-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="132f8-110">การทดสอบและการตรวจสอบเพิ่มเติมพร้อมสำหรับการตรวจสอบการปรับใช้งานที่สำเร็จในแต่ละขั้นตอนของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="132f8-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="132f8-111">สำหรับข้อมูลเพิ่มเติมของระยะความถี่การนำออกใช้ ให้ดูที่ [กระบวนการปรับปรุง](hr-admin-setup-update-process.md)</span><span class="sxs-lookup"><span data-stu-id="132f8-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="132f8-112">ฟิลด์ความแม่นยำในการปัดเศษไม่สามารถแก้ไขได้ หลังจากที่ระบุชนิดของการปัดเศษ (435616)</span><span class="sxs-lookup"><span data-stu-id="132f8-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="132f8-113">ด้วยการเปลี่ยนแปลงนี้ ฟิลด์ **ความแม่นยำในการปัดเศษ** จะพร้อมใช้งาน หลังจากที่คุณอัปเดตฟิลด์ **ชนิดการปัดเศษ**</span><span class="sxs-lookup"><span data-stu-id="132f8-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="132f8-114">ไม่สามารถแก้ไขการออกจากวันที่สิ้นสุดการลงทะเบียน เมื่อแผนการลางานไม่มีรอบระยะเวลาการรับรู้ (413628)</span><span class="sxs-lookup"><span data-stu-id="132f8-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="132f8-115">ขณะนี้คุณสามารถแก้ไขวันที่สิ้นสุดการลงทะเบียนได้โดยไม่ได้รับข้อผิดพลาด "ต้องป้อนข้อมูลพื้นฐานของวันที่รับรู้ของฟิลด์"</span><span class="sxs-lookup"><span data-stu-id="132f8-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="132f8-116">เอนทิตี้การจ้างงานไม่ได้ซิงค์กับ Dataverse (430834)</span><span class="sxs-lookup"><span data-stu-id="132f8-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="132f8-117">การเปลี่ยนแปลงนี้แก้ไขปัญหาที่ไม่มีการซิงค์ข้อมูลการจ้างงานกับ Dataverse หลังจากที่เพิ่มมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="132f8-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="132f8-118">ลบการทำให้เป็นรายการหลักที่หลากหลายสำหรับเอนทิตี้ช่วงเวลาปฎิทินงาน (431775)</span><span class="sxs-lookup"><span data-stu-id="132f8-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="132f8-119">การเปลี่ยนแปลงนี้จะลบการทำให้เป็นรายการหลักที่หลากหลายสำหรับเอนทิตี้ **ช่วงเวลาปฎิทินงาน**</span><span class="sxs-lookup"><span data-stu-id="132f8-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="132f8-120">ตัวกรองข้อมูลที่มีฟังก์ชัน CAST ไม่ทำงานบน OData ที่เรียกว่าเอนทิตี้การกำหนดตำแหน่งของผู้ปฏิบัติงาน (431699)</span><span class="sxs-lookup"><span data-stu-id="132f8-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="132f8-121">การอัปเดตนี้มีการเปลี่ยนแปลงเพื่ออนุญาตให้ตัวกรองที่มีฟังก์ชัน CAST ภายใน OData สำหรับเอนทิตี้ **การกำหนดตำแหน่งของผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="132f8-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="132f8-122">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="132f8-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="132f8-123">การระงับการลางาน</span><span class="sxs-lookup"><span data-stu-id="132f8-123">Leave suspension</span></span>

<span data-ttu-id="132f8-124">คุณสามารถระงับการลางานและการขาดงานในทรัพยากรบุคคลสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="132f8-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="132f8-125">การระงับการลางานจะหยุดการรับรู้การลางานสำหรับชนิดการลางานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="132f8-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="132f8-126">ถ้าการระงับเกิดขึ้นหลังจากที่มีการประมวลผลการรับรู้ การระงับการลางานจะสร้างการปรับปรุงตามสัดส่วนให้กับยอดดุลการลางานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="132f8-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="132f8-127">สำหรับข้อมูลเพิ่มเติม โปรดดู [ระงับการลางาน](hr-leave-and-absence-suspend-leave.md)</span><span class="sxs-lookup"><span data-stu-id="132f8-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="132f8-128">กฎการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="132f8-128">Carry forward rules</span></span>

<span data-ttu-id="132f8-129">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="132f8-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="132f8-130">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="132f8-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="132f8-131">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="132f8-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="132f8-132">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="132f8-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="132f8-133">เอนทิตี้รายละเอียดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="132f8-133">Employment Details entity</span></span>

<span data-ttu-id="132f8-134">เอนทิตี้ **รายละเอียดการจ้างงาน** ได้รับการอัปเดตด้วยฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="132f8-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="132f8-135">**PayFrequency**</span><span class="sxs-lookup"><span data-stu-id="132f8-135">**PayFrequency**</span></span>
- <span data-ttu-id="132f8-136">**รหัสประเภทการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="132f8-136">**Employment Category ID**</span></span>
- <span data-ttu-id="132f8-137">**ชนิดการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="132f8-137">**Employment Type**</span></span>
- <span data-ttu-id="132f8-138">**รหัส EmploymentType**</span><span class="sxs-lookup"><span data-stu-id="132f8-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="132f8-139">**สถานะการจ้างงานของสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="132f8-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="132f8-140">ข้อมูลการตั้งค่าสำหรับฟิลด์เหล่านี้ขึ้นอยู่กับการจัดการสวัสดิการที่ถูกเปิดใช้งานในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="132f8-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="132f8-141">อย่าเติมข้อมูลหรืออัปเดตฟิลด์เหล่านี้ในเอนทิตี้ **รายละเอียดการจ้างงาน** เนื่องจากจะทำให้เกิดข้อผิดพลาดในระหว่างการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="132f8-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="132f8-142">การแสดงตัวอย่าง SharePoint ไม่ทำงานในสภาพแวดล้อมบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="132f8-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="132f8-143">ถ้าการแสดงตัวอย่างเอกสารสำหรับเอกสารที่จัดเก็บไว้ใน SharePoint ไม่ทำงาน ให้ลองกระบวนงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="132f8-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="132f8-144">ตรวจสอบความถูกต้องว่าบัญชีผู้ใช้ของผู้ดูแลระบบมีอีเมลที่เชื่อมโยงกับเรกคอร์ดผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="132f8-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="132f8-145">คุณสามารถดูข้อมูลนี้ได้ในหน้า **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="132f8-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="132f8-146">ถ้าไม่ได้ตั้งค่าอีเมล คุณจำเป็นต้องเพิ่มอีเมลและผู้ให้บริการที่มี add-in ของ OData Excel</span><span class="sxs-lookup"><span data-stu-id="132f8-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="132f8-147">โดยค่าเริ่มต้น ที่อยู่อีเมลไม่มีอยู่ในการออกแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="132f8-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="132f8-148">คุณต้องแก้ไขการออกแบบ Excel เพิ่มฟิลด์ทั้งหมด นำไปใช้ และรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="132f8-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="132f8-149">หลังจากที่คุณดำเนินการขั้นตอนดังกล่าวเสร็จเรียบร้อยแล้ว คุณจะสามารถปรับปรุงบัญชีผู้ดูแลระบบได้</span><span class="sxs-lookup"><span data-stu-id="132f8-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="132f8-150">หลังจากที่บัญชีผู้ดูแลระบบมีบัญชีอีเมลที่เชื่อมโยง ให้ลงชื่อเข้าใช้ใน Human Resources โดยใช้ข้อมูลประจำตัวของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="132f8-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="132f8-151">เข้าถึงเอกสารแนบใน SharePoint เพื่อเริ่มต้นการแสดงตัวอย่างเอกสาร</span><span class="sxs-lookup"><span data-stu-id="132f8-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="132f8-152">ลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้อื่นที่มีสิทธิ์เข้าถึงเอกสารแนบ และตรวจสอบว่ามีการทำงานของการแสดงตัวอย่างตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="132f8-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="132f8-153">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="132f8-153">See also</span></span>

[<span data-ttu-id="132f8-154">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="132f8-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="132f8-155">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="132f8-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="132f8-156">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="132f8-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="132f8-157">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="132f8-157">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]