---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (25 กุมภาพันธ์ 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 25 กุมภาพันธ์ 2020
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1302686aeba52de484ad520efe292fafefc39ebf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526821"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="5450f-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (25 กุมภาพันธ์ 2020)</span><span class="sxs-lookup"><span data-stu-id="5450f-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5450f-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="5450f-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5450f-105">การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.2927</span><span class="sxs-lookup"><span data-stu-id="5450f-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="5450f-106">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="5450f-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="5450f-107">เปิดใช้งานการนำทางการจัดการกรณีและปัญหาและเอนทิตีกรอบงานการจัดการข้อมูล (DMF) (414754)</span><span class="sxs-lookup"><span data-stu-id="5450f-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="5450f-108">คุณลักษณะการแสดงตัวอย่างนี้เปิดใช้งานการนำทางเพิ่มเติมไปยังกรณีของการจัดการกรณีและปัญหา</span><span class="sxs-lookup"><span data-stu-id="5450f-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="5450f-109">คุณสามารถเปิดใช้งานคุณลักษณะการแสดงตัวอย่างนี้ได้ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="5450f-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="5450f-110">รายการเมนูเหล่านี้จะปรากฏในพื้นที่ทำงาน **การปฏิบัติตาม** ของ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="5450f-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5450f-111">ด้วยการเปลี่ยนแปลงนี้ ทรัพยากรบุคคลสามารถเข้าถึง:</span><span class="sxs-lookup"><span data-stu-id="5450f-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="5450f-112">กรณีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5450f-112">All cases</span></span>
- <span data-ttu-id="5450f-113">กรณีของฉัน</span><span class="sxs-lookup"><span data-stu-id="5450f-113">My cases</span></span>
- <span data-ttu-id="5450f-114">กรณีที่เปิดของฉัน</span><span class="sxs-lookup"><span data-stu-id="5450f-114">My open cases</span></span>
- <span data-ttu-id="5450f-115">กรณีที่พ้นกำหนดของฉัน</span><span class="sxs-lookup"><span data-stu-id="5450f-115">My overdue cases</span></span>
- <span data-ttu-id="5450f-116">กรณีที่กำหนดให้กับฉันผ่านลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="5450f-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="5450f-117">พร้อมกับมุมมองใหม่เหล่านี้เข้าไปในกรณีและปัญหา เอนทิตี DMF **รายละเอียดของกรณีและปัญหา** จะพร้อมใช้งานด้วย</span><span class="sxs-lookup"><span data-stu-id="5450f-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="5450f-118">เปิดใช้งานข้อกำหนดความสัมพันธ์ในสมุดที่อยู่สากล (414762)</span><span class="sxs-lookup"><span data-stu-id="5450f-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="5450f-119">ขณะนี้ความสัมพันธ์ถูกเปิดใช้งานอยู่ในสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="5450f-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="5450f-120">ก่อนการนำออกใช้ของสัปดาห์นี้ กล่องแสดงข้อมูลย่อ **ความสัมพันธ์** แสดงความสัมพันธ์ที่ระบบกำหนดไว้ใดๆ</span><span class="sxs-lookup"><span data-stu-id="5450f-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="5450f-121">ขณะนี้คุณสามารถกำหนดความสัมพันธ์ดังกล่าวได้ภายในหน้าสมุดที่อยู่สากล</span><span class="sxs-lookup"><span data-stu-id="5450f-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="5450f-122">ตำแหน่งสามารถลบออกได้ เมื่อมีเรกคอร์ดค่าตอบแทนที่ใช้งานอยู่สำหรับตำแหน่ง (414568)</span><span class="sxs-lookup"><span data-stu-id="5450f-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="5450f-123">ด้วยการเปลี่ยนแปลงนี้ คำเตือนจะปรากฏขึ้นเมื่อคุณพยายามลบตำแหน่ง และผู้ปฏิบัติงานมีเรกคอร์ดค่าตอบแทนที่ใช้งานอยู่สำหรับตำแหน่งเดียวกันนั้น</span><span class="sxs-lookup"><span data-stu-id="5450f-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="5450f-124">เมื่อเหตุการณ์นี้เกิดขึ้น คุณต้องอัพเดตเรกคอร์ดค่าตอบแทนคงที่ของพนักงาน ก่อนที่จะลบตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="5450f-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="5450f-125">ในบางครั้ง ลำดับงานการตรวจทานประสิทธิภาพเพิ่มการลงชื่อออกจากผู้ที่ไม่ได้เป็นส่วนหนึ่งของกระบวนการ (414171)</span><span class="sxs-lookup"><span data-stu-id="5450f-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="5450f-126">การเปลี่ยนแปลงนี้แก้ไขปัญหาที่ซึ่งผู้เข้าร่วมที่มีการลงชื่อออกเพิ่มเติมจะถูกเพิ่มเข้าในการตรวจทานประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="5450f-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="5450f-127">การกำหนดตำแหน่งของผู้ปฏิบัติงานไม่ถูกสร้างใน Common Data Service เมื่อมีการเลือกไว้ในกล่องโต้ตอบผู้ปฏิบัติงานใหม่ (413479)</span><span class="sxs-lookup"><span data-stu-id="5450f-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="5450f-128">การเปลี่ยนแปลงนี้แก้ไขปัญหา เมื่อจ้างผู้ปฏิบัติงานใหม่และกำหนดการจ้างงานใหม่ให้กับตำแหน่งผ่านกล่องโต้ตอบ **ผู้ปฏิบัติงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="5450f-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="5450f-129">ขณะนี้การกำหนดตำแหน่งจะถูกสะท้อนใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5450f-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="5450f-130">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="5450f-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="5450f-131">โซลูชัน Common Data Service ที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="5450f-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="5450f-132">โซลูชัน Common Data Service ใหม่จะพร้อมใช้งานเร็วๆ นี้ โดยมีการเปลี่ยนแปลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5450f-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="5450f-133">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5450f-133">Description</span></span> | <span data-ttu-id="5450f-134">เปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="5450f-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="5450f-135">เอนทิตี **งาน/ตำแหน่ง** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5450f-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="5450f-136">**ภูมิภาคของค่าตอบแทน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-136">**Compensation region** added</span></span></br><span data-ttu-id="5450f-137">**มิติทางการเงิน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="5450f-138">เอนทิตี **ผู้ปฏิบัติงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5450f-138">**Worker** entity changes</span></span> | <span data-ttu-id="5450f-139">**ลำดับชื่อ** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-139">**Name sequence** added</span></span></br><span data-ttu-id="5450f-140">เพิ่ม **การทำงานจากที่บ้าน** แล้ว</span><span class="sxs-lookup"><span data-stu-id="5450f-140">**Works from home** added</span></span></br><span data-ttu-id="5450f-141">**ภาษา** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-141">**Language** added</span></span></br><span data-ttu-id="5450f-142">**วันที่ของอายุงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-142">**Seniority date** added</span></span></br><span data-ttu-id="5450f-143">**วันที่ครบรอบปี** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-143">**Anniversary date** added</span></span></br><span data-ttu-id="5450f-144">เพิ่ม **วันที่จ้างงานเดิม** แล้ว</span><span class="sxs-lookup"><span data-stu-id="5450f-144">**Original hire date** added</span></span> |
| <span data-ttu-id="5450f-145">เอนทิตี **การจ้างงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5450f-145">**Employment** entity changes</span></span> | <span data-ttu-id="5450f-146">**มิติทางการเงิน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-146">**Financial dimensions** added</span></span></br><span data-ttu-id="5450f-147">**เหตุผลการสิ้นสุดการจ้างงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-147">**Termination reason** added</span></span></br><span data-ttu-id="5450f-148">**วันที่สิ้นสุดการจ้างงาน** เปลี่ยนชื่อจาก **วันที่เปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="5450f-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="5450f-149">**วันที่ทดลองงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-149">**Probation date** added</span></span> |
| <span data-ttu-id="5450f-150">เอนทิตี **ที่อยู่ผู้ปฏิบัติงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5450f-150">**Worker address** entity changes</span></span> | <span data-ttu-id="5450f-151">**ที่อยู่ถนน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5450f-151">**Street address** added</span></span></br><span data-ttu-id="5450f-152">**บรรทัดที่อยู่ 1** **บรรทัดที่อยู่ 2** และ **บรรทัดที่อยู่ 3** ที่ทำเครื่องหมายสำหรับค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="5450f-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="5450f-153">เอนทิตีการตั้งค่าค่าตอบแทนผันแปรใหม่</span><span class="sxs-lookup"><span data-stu-id="5450f-153">New variable compensation setup entities</span></span> | <span data-ttu-id="5450f-154">**ชนิดแผนตัวแปรค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="5450f-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="5450f-155">**แผนค่าตอบแทนผันแปร**</span><span class="sxs-lookup"><span data-stu-id="5450f-155">**Compensation variable plan**</span></span></br><span data-ttu-id="5450f-156">**กฎสิทธิพึงได้**</span><span class="sxs-lookup"><span data-stu-id="5450f-156">**Vesting rules**</span></span></br><span data-ttu-id="5450f-157">**ระดับแผนตัวแปรค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="5450f-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="5450f-158">เอนทตี **การจ้างงานในปฏิทินของผู้ปฏิบัติงาน** ใหม่</span><span class="sxs-lookup"><span data-stu-id="5450f-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="5450f-159">เพิ่ม **เอนทิตีปฏิทินงาน** แล้ว</span><span class="sxs-lookup"><span data-stu-id="5450f-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="5450f-160">เอนทตี **รายละเอียดตำแหน่งที่มีค่าจ้าง** ใหม่</span><span class="sxs-lookup"><span data-stu-id="5450f-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="5450f-161">เพิ่ม **รายละเอียดตำแหน่งที่มีค่าจ้าง** แล้ว</span><span class="sxs-lookup"><span data-stu-id="5450f-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="5450f-162">เอนทิตี้ **ชื่อ** ใหม่</span><span class="sxs-lookup"><span data-stu-id="5450f-162">New **Title** entity</span></span> | <span data-ttu-id="5450f-163">เพิ่ม **ชื่อ** แล้ว</span><span class="sxs-lookup"><span data-stu-id="5450f-163">**Title** added.</span></span> <span data-ttu-id="5450f-164">เอนทิตี **ชื่อเรื่อง** ใหม่ จะรวมอยู่ในกระบวนการซิงค์ระหว่างทรัพยากรบุคคลและ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5450f-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="5450f-165">จะไม่มีการอ้างอิงจากเอนทิตี **ตำแหน่งงาน** หรือ **งาน** ในตอนแรก</span><span class="sxs-lookup"><span data-stu-id="5450f-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="5450f-166">ในช่วงสองถึงสามสัปดาห์ข้างหน้า การเปลี่ยนแปลงเอนทิตีเหล่านี้จะพร้อมใช้งานในสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5450f-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="5450f-167">เมื่อต้องการติดตั้งโซลูชัน Common Data Service ล่าสุดสำหรับทรัพยากรบุคคลด้วยตนเอง:</span><span class="sxs-lookup"><span data-stu-id="5450f-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="5450f-168">ไปยัง [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="5450f-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="5450f-169">เลือก **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="5450f-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="5450f-170">ค้นหาสภาพแวดล้อมที่คุณต้องการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="5450f-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="5450f-171">นี่ควรตรงกับ **ชื่อสภาพแวดล้อม** ในส่วน **ข้อมูล Common Data Service** ในฟอร์ม **เกี่ยวกับ** ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5450f-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="5450f-172">เลือกสภาพแวดล้อมเพื่อดูรายละเอียดของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="5450f-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="5450f-173">ในแถบการดำเนินการที่ส่วนบนสุด เลือก **จัดการโซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="5450f-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="5450f-174">หน้าต่างเบราเซอร์ใหม่จะเปิดขึ้นและนำทางไปยัง **ศูนย์การจัดการ Dynamics 365** ในบริบทของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="5450f-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="5450f-175">ในรายการ **โซลูชัน** ให้เลือก **จุดยึด Dynamics 365 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="5450f-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="5450f-176">เลือก **อัพเกรด** เพื่อใช้โซลูชันล่าสุด</span><span class="sxs-lookup"><span data-stu-id="5450f-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5450f-177">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="5450f-177">In preview</span></span>

<span data-ttu-id="5450f-178">คุณลักษณะการแสดงตัวอย่างต่อไปนี้จะพร้อมใช้งานในวันที่ 3 กุมภาพันธ์ 2020:</span><span class="sxs-lookup"><span data-stu-id="5450f-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="5450f-179">**ตัวอย่างคุณลักษณะการลางานและขาดงาน** - สำหรับข้อมูลเพิ่มเติมโปรดดู [ตัวอย่างคุณลักษณะการลางานและขาดงาน](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="5450f-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="5450f-180">**ตัวอย่างคุณลักษณะการจัดการสวัสดิการ** - สำหรับข้อมูลเพิ่มเติมรวมทั้งปัญหาที่ทราบโปรดดู [ภาพรวมการจัดการสวัสดิการ](hr-benefits-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5450f-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5450f-181">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="5450f-181">See also</span></span>

[<span data-ttu-id="5450f-182">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="5450f-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="5450f-183">ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2</span><span class="sxs-lookup"><span data-stu-id="5450f-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="5450f-184">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="5450f-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="5450f-185">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5450f-185">Manage features</span></span>](hr-admin-manage-features.md)