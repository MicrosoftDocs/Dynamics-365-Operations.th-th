---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (3 มีนาคม 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 3 มีนาคม 2020
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
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
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e4007daa51d661a2a6b67c323cfaf05c22543371
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128052"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a><span data-ttu-id="976f3-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (3 มีนาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="976f3-103">What's new or changed in Dynamics 365 Human Resources (March 3, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="976f3-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="976f3-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="976f3-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.2955</span><span class="sxs-lookup"><span data-stu-id="976f3-105">Changes apply to build number 8.1.2955.</span></span> <span data-ttu-id="976f3-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="976f3-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="976f3-107">ขณะนี้โซลูชัน Dataverse พร้อมใช้งาน โดยมีการเปลี่ยนแปลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="976f3-107">Dataverse solution is now available with the following changes:</span></span>

<span data-ttu-id="976f3-108">โซลูชัน Dataverse ใหม่จะพร้อมใช้งานเร็วๆ นี้ โดยมีการเปลี่ยนแปลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="976f3-108">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="976f3-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="976f3-109">Description</span></span> | <span data-ttu-id="976f3-110">เปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="976f3-110">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="976f3-111">เอนทิตี **งาน/ตำแหน่ง** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="976f3-111">**Job/Position** entity changes</span></span> | <span data-ttu-id="976f3-112">**ภูมิภาคของค่าตอบแทน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-112">**Compensation region** added</span></span></br><span data-ttu-id="976f3-113">**มิติทางการเงิน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-113">**Financial dimensions** added</span></span> |
| <span data-ttu-id="976f3-114">เอนทิตี **ผู้ปฏิบัติงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="976f3-114">**Worker** entity changes</span></span> | <span data-ttu-id="976f3-115">**ลำดับชื่อ** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-115">**Name sequence** added</span></span></br><span data-ttu-id="976f3-116">เพิ่ม **การทำงานจากที่บ้าน** แล้ว</span><span class="sxs-lookup"><span data-stu-id="976f3-116">**Works from home** added</span></span></br><span data-ttu-id="976f3-117">**ภาษา** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-117">**Language** added</span></span></br><span data-ttu-id="976f3-118">**วันที่ของอายุงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-118">**Seniority date** added</span></span></br><span data-ttu-id="976f3-119">**วันที่ครบรอบปี** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-119">**Anniversary date** added</span></span></br><span data-ttu-id="976f3-120">เพิ่ม **วันที่จ้างงานเดิม** แล้ว</span><span class="sxs-lookup"><span data-stu-id="976f3-120">**Original hire date** added</span></span> |
| <span data-ttu-id="976f3-121">เอนทิตี **การจ้างงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="976f3-121">**Employment** entity changes</span></span> | <span data-ttu-id="976f3-122">**มิติทางการเงิน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-122">**Financial dimensions** added</span></span></br><span data-ttu-id="976f3-123">**เหตุผลการสิ้นสุดการจ้างงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-123">**Termination reason** added</span></span></br><span data-ttu-id="976f3-124">**วันที่สิ้นสุดการจ้างงาน** เปลี่ยนชื่อจาก **วันที่เปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="976f3-124">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="976f3-125">**วันที่ทดลองงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-125">**Probation date** added</span></span> |
| <span data-ttu-id="976f3-126">เอนทิตี **ที่อยู่ผู้ปฏิบัติงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="976f3-126">**Worker address** entity changes</span></span> | <span data-ttu-id="976f3-127">**ที่อยู่ถนน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="976f3-127">**Street address** added</span></span></br><span data-ttu-id="976f3-128">**บรรทัดที่อยู่ 1** **บรรทัดที่อยู่ 2** และ **บรรทัดที่อยู่ 3** ที่ทำเครื่องหมายสำหรับค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="976f3-128">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="976f3-129">เอนทิตีการตั้งค่าค่าตอบแทนผันแปรใหม่</span><span class="sxs-lookup"><span data-stu-id="976f3-129">New variable compensation setup entities</span></span> | <span data-ttu-id="976f3-130">**ชนิดแผนตัวแปรค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="976f3-130">**Compensation variable plan type**</span></span></br><span data-ttu-id="976f3-131">**แผนค่าตอบแทนผันแปร**</span><span class="sxs-lookup"><span data-stu-id="976f3-131">**Compensation variable plan**</span></span></br><span data-ttu-id="976f3-132">**กฎสิทธิพึงได้**</span><span class="sxs-lookup"><span data-stu-id="976f3-132">**Vesting rules**</span></span></br><span data-ttu-id="976f3-133">**ระดับแผนตัวแปรค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="976f3-133">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="976f3-134">เอนทตี **การจ้างงานในปฏิทินของผู้ปฏิบัติงาน** ใหม่</span><span class="sxs-lookup"><span data-stu-id="976f3-134">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="976f3-135">เพิ่ม **เอนทิตีปฏิทินงาน** แล้ว</span><span class="sxs-lookup"><span data-stu-id="976f3-135">**Work calendar entity** added</span></span> |
| <span data-ttu-id="976f3-136">เอนทตี **รายละเอียดตำแหน่งที่มีค่าจ้าง** ใหม่</span><span class="sxs-lookup"><span data-stu-id="976f3-136">New **Payroll position detail** entity</span></span> | <span data-ttu-id="976f3-137">เพิ่ม **รายละเอียดตำแหน่งที่มีค่าจ้าง** แล้ว</span><span class="sxs-lookup"><span data-stu-id="976f3-137">**Payroll position detail** added</span></span> |
| <span data-ttu-id="976f3-138">เอนทิตี้ **ชื่อ** ใหม่</span><span class="sxs-lookup"><span data-stu-id="976f3-138">New **Title** entity</span></span> | <span data-ttu-id="976f3-139">เพิ่ม **ชื่อ** แล้ว</span><span class="sxs-lookup"><span data-stu-id="976f3-139">**Title** added.</span></span> <span data-ttu-id="976f3-140">เอนทิตี **ชื่อเรื่อง** ใหม่ จะรวมอยู่ในกระบวนการซิงค์ระหว่างทรัพยากรบุคคลและ Dataverse</span><span class="sxs-lookup"><span data-stu-id="976f3-140">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="976f3-141">จะไม่มีการอ้างอิงจากเอนทิตี **ตำแหน่งงาน** หรือ **งาน** ในตอนแรก</span><span class="sxs-lookup"><span data-stu-id="976f3-141">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="976f3-142">ในช่วงสองถึงสามสัปดาห์ข้างหน้า การเปลี่ยนแปลงเอนทิตีเหล่านี้จะพร้อมใช้งานในสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="976f3-142">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="976f3-143">เมื่อต้องการติดตั้งโซลูชัน Dataverse ล่าสุดสำหรับทรัพยากรบุคคลด้วยตนเอง:</span><span class="sxs-lookup"><span data-stu-id="976f3-143">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="976f3-144">ไปยัง [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="976f3-144">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="976f3-145">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="976f3-145">Select **Environments**.</span></span>

3.  <span data-ttu-id="976f3-146">ค้นหาสภาพแวดล้อมที่คุณต้องการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="976f3-146">Find the environment you want to upgrade.</span></span> <span data-ttu-id="976f3-147">สภาพแวดล้อมควรตรงกับ **ชื่อสภาพแวดล้อม** ในส่วน **ข้อมูล Common Data Service** ในฟอร์ม **เกี่ยวกับ** ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="976f3-147">The environment should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="976f3-148">เลือกสภาพแวดล้อมเพื่อดูรายละเอียดของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="976f3-148">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="976f3-149">ในแถบการดำเนินการที่ส่วนบนสุด เลือก **จัดการโซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="976f3-149">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="976f3-150">หน้าต่างเบราเซอร์ใหม่จะเปิดขึ้นและนำทางไปยัง **ศูนย์การจัดการ Dynamics 365** ในบริบทของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="976f3-150">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="976f3-151">ในรายการ **โซลูชัน** ให้เลือก **จุดยึด Dynamics 365 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="976f3-151">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="976f3-152">เลือก **อัพเกรด** เพื่อใช้โซลูชันล่าสุด</span><span class="sxs-lookup"><span data-stu-id="976f3-152">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a><span data-ttu-id="976f3-153">นำเข้าปัญหาด้วยเอนทิตีข้อมูลการลงทะเบียนการลางาน (406082)</span><span class="sxs-lookup"><span data-stu-id="976f3-153">Import issues with the Leave enrollment data entity (406082)</span></span>

<span data-ttu-id="976f3-154">ขณะนี้คุณสามารถลงทะเบียนพนักงานในแผนการลางานใหม่ของชนิดเดียวกันได้ ตราบใดที่วันที่ลงทะเบียนใหม่เป็นวันที่หลังจากวันที่ลงทะเบียนที่หมดอายุของแผนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="976f3-154">You can now enroll an employee in a new leave plan of the same type, as long as the new enrollment date is later than the expired enrollment date of the previous plan.</span></span>

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a><span data-ttu-id="976f3-155">ปัญหาเกี่ยวกับการส่งออกอัตราเงินสมทบในเอนทิตี 401k payrollWorkerEnrolledBenefitDetail ใน DMF (420700)</span><span class="sxs-lookup"><span data-stu-id="976f3-155">Issue with exporting contribution rates in the 401k payrollWorkerEnrolledBenefitDetail entity in DMF (420700)</span></span>

<span data-ttu-id="976f3-156">การเปลี่ยนแปลงนี้จะแก้ไขฟังก์ชันการส่งออกสำหรับเอนทิตี **payrollWorkerEnrolledBenefitDetail** เพื่อให้สะท้อนถึงค่าปัจจุบันสำหรับเงินสมทบของนายจ้าง</span><span class="sxs-lookup"><span data-stu-id="976f3-156">This change corrects the export functionality for the **payrollWorkerEnrolledBenefitDetail** entity to reflect the current values for employer contribution.</span></span>

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a><span data-ttu-id="976f3-157">การค้นหาในฟอร์มผู้ปฏิบัติงานที่มีความคล่องตัวทำให้เกิดข้อความที่ระบุว่า ต้องกรอกข้อมูลในฟิลด์บุคคล (402525)</span><span class="sxs-lookup"><span data-stu-id="976f3-157">Searching in the streamlined Worker form causes message saying Person field must be filled in (402525)</span></span>

<span data-ttu-id="976f3-158">เมื่อคุณค้นหาพนักงาน คุณจะไม่ได้รับข้อความที่ระบุว่าคุณต้องกรอกข้อมูลในฟิลด์ **บุคคล** อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="976f3-158">When you search for an employee, you'll no longer receive a message saying you must fill in the **Person** field.</span></span>

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a><span data-ttu-id="976f3-159">หมายเหตุ ค่าฟิลด์ไม่แสดงบนฟอร์มเพิ่มทักษะเพิ่มเติม (380134)</span><span class="sxs-lookup"><span data-stu-id="976f3-159">Note field value doesn't render on the Add more skills form (380134)</span></span>

<span data-ttu-id="976f3-160">การเปลี่ยนแปลงนี้แก้ไขปัญหา เมื่อคุณปรับแต่งฟอร์ม **เพิ่มทักษะเพิ่มเติม** ในบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="976f3-160">This change corrects an issue when you personalize the **Add more skills** form in Employee self service.</span></span>

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a><span data-ttu-id="976f3-161">แผนค่าตอบแทนคงที่หลายแผนไม่หมดอายุ เมื่อโอนย้ายพนักงาน (389466)</span><span class="sxs-lookup"><span data-stu-id="976f3-161">Multiple fixed compensation plans don't expire when transferring employees (389466)</span></span>

<span data-ttu-id="976f3-162">ด้วยการเปลี่ยนแปลงนี้ เรกคอร์ดค่าตอบแทนคงที่ที่ใช้งานอยู่ทั้งหมดสำหรับตำแหน่งเดิมจะหมดอายุในวันที่เปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="976f3-162">With this change, all active fixed compensation records for the old position will expire on the transition date.</span></span>

## <a name="in-preview"></a><span data-ttu-id="976f3-163">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="976f3-163">In preview</span></span>

<span data-ttu-id="976f3-164">คุณลักษณะการแสดงตัวอย่างต่อไปนี้จะพร้อมใช้งานในวันที่ 3 กุมภาพันธ์ 2020:</span><span class="sxs-lookup"><span data-stu-id="976f3-164">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="976f3-165">**ตัวอย่างคุณลักษณะการลางานและขาดงาน** - สำหรับข้อมูลเพิ่มเติมโปรดดู [ตัวอย่างคุณลักษณะการลางานและขาดงาน](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="976f3-165">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="976f3-166">**ตัวอย่างคุณลักษณะการจัดการสวัสดิการ** - สำหรับข้อมูลเพิ่มเติมรวมทั้งปัญหาที่ทราบโปรดดู [ภาพรวมการจัดการสวัสดิการ](hr-benefits-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="976f3-166">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="976f3-167">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="976f3-167">See also</span></span>

[<span data-ttu-id="976f3-168">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="976f3-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="976f3-169">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="976f3-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="976f3-170">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="976f3-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="976f3-171">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="976f3-171">Manage features</span></span>](hr-admin-manage-features.md)