---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (1 พฤษภาคม 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 1 พฤษภาคม 2020
author: andreabichsel
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8ceea10b3157fee410e5db6e1d8c9a0366e30e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6050980"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="942a9-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (1 พฤษภาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="942a9-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="942a9-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="942a9-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="942a9-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3196</span><span class="sxs-lookup"><span data-stu-id="942a9-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="942a9-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="942a9-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="942a9-107">เอนทิตีการบริหารประสิทธิภาพใหม่พร้อมใช้งานในกรอบงานการจัดการข้อมูล (DMF)</span><span class="sxs-lookup"><span data-stu-id="942a9-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="942a9-108">เอนทิตี้ต่อไปนี้พร้อมใช้งานแล้วในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="942a9-108">The following entities are now available.</span></span> <span data-ttu-id="942a9-109">ถ้าคุณไม่เห็นเอนทิตี้เหล่านี้แสดงรายการอยู่ในรายการเอนทิตี้ ให้ใช้ตัวเลือก **รีเฟรชเอนทิตี้** ใน **พารามิเตอร์กรอบงาน > การตั้งค่าเอนทิตี้ > รีเฟรชรายการเอนทิตี้**</span><span class="sxs-lookup"><span data-stu-id="942a9-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="942a9-110">**ความสามารถในการสนทนา**</span><span class="sxs-lookup"><span data-stu-id="942a9-110">**Discussion Competency**</span></span>
- <span data-ttu-id="942a9-111">**เป้าหมายการสนทนา**</span><span class="sxs-lookup"><span data-stu-id="942a9-111">**Discussion Goals**</span></span>
- <span data-ttu-id="942a9-112">**การวัดการสนทนา**</span><span class="sxs-lookup"><span data-stu-id="942a9-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="942a9-113">**หัวข้อการสนทนา**</span><span class="sxs-lookup"><span data-stu-id="942a9-113">**Discussion Topic**</span></span>
- <span data-ttu-id="942a9-114">**สมุดรายวันประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="942a9-114">**Performance Journal**</span></span>
- <span data-ttu-id="942a9-115">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="942a9-115">**Measurement**</span></span>
- <span data-ttu-id="942a9-116">**การวัดเป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="942a9-116">**Goal Measurement**</span></span>

<span data-ttu-id="942a9-117">นอกจากนี้ **คะแนนรวม** และ **คะแนนเฉลี่ย** ถูกเพิ่มเข้าในเอนทิตี **การสนทนา**</span><span class="sxs-lookup"><span data-stu-id="942a9-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="942a9-118">เพิ่มความยาวของความคิดเห็นของคำขอลางาน (275641)</span><span class="sxs-lookup"><span data-stu-id="942a9-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="942a9-119">ในปัจจุบันข้อคิดเห็นเกี่ยวกับคำขอลางานอนุญาตให้มีอักขระมากกว่า 100 ตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="942a9-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="942a9-120">ความคิดเห็นสุดท้ายเกี่ยวกับการตรวจทานไม่ปรากฏขึ้น เมื่อผู้จัดการหรือพนักงานลงชื่อเข้าใช้สู่บริษัทอื่น (431688)</span><span class="sxs-lookup"><span data-stu-id="942a9-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="942a9-121">ข้อคิดเห็นทั้งหมดจะปรากฏในขณะที่ดูการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="942a9-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="942a9-122">ลิงค์ที่กำหนดโดยผู้ใช้ไม่ได้รับการสนับสนุนบนฟอร์มผู้ปฏิบัติงานใหม่ (390374)</span><span class="sxs-lookup"><span data-stu-id="942a9-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="942a9-123">ขณะนี้มีการเปิดใช้งานลิงค์ที่ผู้ใช้กำหนดบนฟอร์ม **ผู้ปฏิบัติงาน** ที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="942a9-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="942a9-124">HcmRatingLevelEntity ทำให้เกิด ความล้มเหลวของ API OData (439476)</span><span class="sxs-lookup"><span data-stu-id="942a9-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="942a9-125">การเปลี่ยนแปลงนี้จะแก้ไขความล้มเหลวของ API</span><span class="sxs-lookup"><span data-stu-id="942a9-125">This change corrects the API crash.</span></span> <span data-ttu-id="942a9-126">ชื่อที่ซ้ำกันทำให้เกิดข้อผิดพลาดนี้</span><span class="sxs-lookup"><span data-stu-id="942a9-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="942a9-127">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="942a9-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="942a9-128">การระงับการลางาน</span><span class="sxs-lookup"><span data-stu-id="942a9-128">Leave suspension</span></span>

<span data-ttu-id="942a9-129">คุณสามารถระงับการลางานและการขาดงานในทรัพยากรบุคคลสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="942a9-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="942a9-130">การระงับการลางานจะหยุดการรับรู้การลางานสำหรับชนิดการลางานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="942a9-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="942a9-131">ถ้าการระงับเกิดขึ้นหลังจากที่มีการประมวลผลการรับรู้ การระงับการลางานจะสร้างการปรับปรุงตามสัดส่วนให้กับยอดดุลการลางานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="942a9-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="942a9-132">สำหรับข้อมูลเพิ่มเติม โปรดดู [ระงับการลางาน](hr-leave-and-absence-suspend-leave.md)</span><span class="sxs-lookup"><span data-stu-id="942a9-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="942a9-133">อัพเดตประสบการณ์ผู้ใช้เพื่อบ่งชี้ว่ารายการคงค้างถูกระงับแล้ว (429550)</span><span class="sxs-lookup"><span data-stu-id="942a9-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="942a9-134">ประสบการณ์ผู้ใช้บ่งชี้ว่าการคงค้างถูกระงับสำหรับแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="942a9-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="942a9-135">ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ (272447)</span><span class="sxs-lookup"><span data-stu-id="942a9-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="942a9-136">ในรุ่นนี้ HR สามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ยังไม่ได้ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="942a9-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="942a9-137">การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น</span><span class="sxs-lookup"><span data-stu-id="942a9-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="942a9-138">คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="942a9-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="942a9-139">เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง (429549)</span><span class="sxs-lookup"><span data-stu-id="942a9-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="942a9-140">ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="942a9-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="942a9-141">เพิ่มรหัสเหตุผลให้กับการระงับการคงค้าง (429547)</span><span class="sxs-lookup"><span data-stu-id="942a9-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="942a9-142">รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง</span><span class="sxs-lookup"><span data-stu-id="942a9-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="942a9-143">เริ่มต้นการเปลี่ยนจากพารามิเตอร์ทรัพยากรบุคคลเป็นพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="942a9-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="942a9-144">การนำออกใช้นี้จะเริ่มต้นโดยรวมพารามิเตอร์ทรัพยากรบุคคลที่มีพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="942a9-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="942a9-145">กฎการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="942a9-145">Carry forward rules</span></span>

<span data-ttu-id="942a9-146">คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="942a9-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="942a9-147">ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน</span><span class="sxs-lookup"><span data-stu-id="942a9-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="942a9-148">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)</span><span class="sxs-lookup"><span data-stu-id="942a9-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="942a9-149">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="942a9-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="942a9-150">การแสดงตัวอย่าง SharePoint ไม่ทำงานในสภาพแวดล้อมบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="942a9-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="942a9-151">ถ้าการแสดงตัวอย่างเอกสารสำหรับเอกสารที่จัดเก็บไว้ใน SharePoint ไม่ทำงาน ให้ลองกระบวนงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="942a9-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="942a9-152">ตรวจสอบความถูกต้องว่าบัญชีผู้ใช้ของผู้ดูแลระบบมีอีเมลที่เชื่อมโยงกับเรกคอร์ดผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="942a9-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="942a9-153">คุณสามารถดูข้อมูลนี้ได้ในหน้า **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="942a9-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="942a9-154">ถ้าไม่ได้ตั้งค่าอีเมล คุณจำเป็นต้องเพิ่มอีเมลและผู้ให้บริการที่มี add-in ของ OData Excel</span><span class="sxs-lookup"><span data-stu-id="942a9-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="942a9-155">โดยค่าเริ่มต้น ที่อยู่อีเมลไม่มีอยู่ในการออกแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="942a9-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="942a9-156">คุณต้องแก้ไขการออกแบบ Excel เพิ่มฟิลด์ทั้งหมด นำไปใช้ และรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="942a9-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="942a9-157">หลังจากที่คุณดำเนินการขั้นตอนดังกล่าวเสร็จเรียบร้อยแล้ว คุณจะสามารถปรับปรุงบัญชีผู้ดูแลระบบได้</span><span class="sxs-lookup"><span data-stu-id="942a9-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="942a9-158">หลังจากที่บัญชีผู้ดูแลระบบมีบัญชีอีเมลที่เชื่อมโยง ให้ลงชื่อเข้าใช้ใน Human Resources โดยใช้ข้อมูลประจำตัวของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="942a9-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="942a9-159">เข้าถึงเอกสารแนบใน SharePoint เพื่อเริ่มต้นการแสดงตัวอย่างเอกสาร</span><span class="sxs-lookup"><span data-stu-id="942a9-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="942a9-160">ลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้อื่นที่มีสิทธิ์เข้าถึงเอกสารแนบ และตรวจสอบว่ามีการทำงานของการแสดงตัวอย่างตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="942a9-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="942a9-161">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="942a9-161">See also</span></span>

[<span data-ttu-id="942a9-162">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="942a9-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="942a9-163">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="942a9-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="942a9-164">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="942a9-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="942a9-165">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="942a9-165">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]