---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (21 มกราคม 2020)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528134"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a><span data-ttu-id="a3981-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (21 มกราคม 2020)</span><span class="sxs-lookup"><span data-stu-id="a3981-103">What's new or changed in Dynamics 365 Talent (January 21, 2020)</span></span>

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a3981-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="a3981-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="a3981-105">การเปลี่ยนแปลงใน Attract</span><span class="sxs-lookup"><span data-stu-id="a3981-105">Changes in Attract</span></span>

<span data-ttu-id="a3981-106">รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="a3981-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="a3981-107">เราได้เพิ่มฟังก์ชันไปยัง Attract เพื่อสนับสนุนประกาศล่าสุดของเรา [การสร้างบุคลากรที่ประสบความสำเร็จมากขึ้นด้วย Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/)</span><span class="sxs-lookup"><span data-stu-id="a3981-107">We've added functionality to Attract to support our recent announcement, [Building a more successful workforce with Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).</span></span>

### <a name="download-environment-data"></a><span data-ttu-id="a3981-108">ดาวน์โหลดข้อมูลสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="a3981-108">Download environment data</span></span>

<span data-ttu-id="a3981-109">ผู้ดูแลระบบสามารถดาวน์โหลดข้อมูลของสภาพแวดล้อมของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="a3981-109">Administrators can download their environment’s data.</span></span> <span data-ttu-id="a3981-110">มีการส่งออกข้อมูลในรูปแบบ JSON มาตรฐานที่มีงาน ผู้สมัคร และการตั้งค่าคอนฟิกทั้งหมดที่ส่งออกในไฟล์ซิป</span><span class="sxs-lookup"><span data-stu-id="a3981-110">The data is exported in standard JSON format with all the jobs, candidates, and configuration exported in a zip file.</span></span> <span data-ttu-id="a3981-111">สำหรับข้อมูลเพิ่มเติม ดู [ส่งออกข้อมูลจาก Attract และ Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)</span><span class="sxs-lookup"><span data-stu-id="a3981-111">For more information, see [Export data from Attract and Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).</span></span>

### <a name="restricting-access-to-environments-for-non-admin-users"></a><span data-ttu-id="a3981-112">การจำกัดการเข้าถึงสภาพแวดล้อมสำหรับผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a3981-112">Restricting access to environments for non-admin users</span></span>

<span data-ttu-id="a3981-113">ขณะนี้ผู้ดูแลระบบสามารถจำกัดการเข้าถึงสภาพแวดล้อมสำหรับผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a3981-113">Administrators can now restrict access to the environment for non-admin users.</span></span> <span data-ttu-id="a3981-114">การดำเนินการนี้ไม่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="a3981-114">This action can't be undone.</span></span> <span data-ttu-id="a3981-115">สำหรับข้อมูลเพิ่มเติม โปรดดู [จำกัดการเข้าถึง Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract)</span><span class="sxs-lookup"><span data-stu-id="a3981-115">For more information, see [Restrict access to Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="a3981-116">การเปลี่ยนแปลงในการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="a3981-116">Changes in Onboard</span></span>

<span data-ttu-id="a3981-117">รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="a3981-117">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

### <a name="exporting-onboarding-guides"></a><span data-ttu-id="a3981-118">การส่งออก Guides การเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="a3981-118">Exporting onboarding guides</span></span>

<span data-ttu-id="a3981-119">ขณะนี้ผู้ใช้สามารถส่งออก Guides การเตรียมความพร้อมและเท็มเพลตการเตรียมความพร้อมทั้งหมดของพวกเขาได้ในรูปแบบเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="a3981-119">Users can now export all of their onboarding guides and onboarding templates in Word document format.</span></span> <span data-ttu-id="a3981-120">สำหรับข้อมูลเพิ่มเติม ดู [ส่งออกข้อมูลจาก Attract และ Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)</span><span class="sxs-lookup"><span data-stu-id="a3981-120">For more information, see [Export data from Attract and Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="a3981-121">การเปลี่ยนแปลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="a3981-121">Changes in Core HR</span></span>

<span data-ttu-id="a3981-122">การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2726</span><span class="sxs-lookup"><span data-stu-id="a3981-122">Changes described in this section apply to build number 8.1.2726.</span></span> <span data-ttu-id="a3981-123">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a3981-123">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a><span data-ttu-id="a3981-124">ฟิลด์ค่าตอบแทนรายปีล่าสุดในฟอร์มตรวจสอบการจ้างงานไม่สอดคล้องกัน (392092)</span><span class="sxs-lookup"><span data-stu-id="a3981-124">Most recent annual compensation field in Verify employment form isn't consistent (392092)</span></span>

<span data-ttu-id="a3981-125">การนำออกใช้นี้มีการเปลี่ยนแปลงที่จะแสดงสกุลเงินล่าสุดอย่างสม่ำเสมอ โดยใช้ตัวเลือกบริษัทบนฟอร์ม **ตรวจสอบการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="a3981-125">This release includes a change that will consistently display the latest currency based on the company selector on the **Verify employment** form.</span></span>

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a><span data-ttu-id="a3981-126">เรียกว่า ฟิลด์ที่เพิ่มลงในการค้นหาผู้รับผลป้อนกลับ (407789)</span><span class="sxs-lookup"><span data-stu-id="a3981-126">Known as field added to the Feedback recipient lookup (407789)</span></span>

<span data-ttu-id="a3981-127">เมื่อให้ผลป้อนกลับเกี่ยวกับประสิทธิภาพ การค้นหาสำหรับผู้ปฏิบัติงานจึงไม่มีข้อมูลเพียงพอที่จะตรวจสอบว่าผลป้อนกลับไปยังบุคคลที่ถูกต้องหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a3981-127">When providing performance feedback, the lookup for workers didn't provide enough information to determine if feedback is going to the correct person.</span></span> <span data-ttu-id="a3981-128">เราได้เพิ่มคอลัมน์ **เรียกว่า** เพื่อช่วยระบุชื่อเฉพาะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="a3981-128">We added a **Known as** column to help identify the unique name of the employee.</span></span>
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a><span data-ttu-id="a3981-129">มีการสร้างเรกคอร์ด HcmWorkerPayrollInfo โดยไม่มีการเชื่อมโยงกับผู้ปฏิบัติงาน (394526)</span><span class="sxs-lookup"><span data-stu-id="a3981-129">HcmWorkerPayrollInfo record is created without an association to a worker (394526)</span></span>

<span data-ttu-id="a3981-130">การนำออกใช้นี้รวมถึงการเปลี่ยนแปลงเป็น ไม่เขียนเรกคอดร์ด HCMWorkerPayrollInfo โดยไม่มีการอ้างอิงถึงพนักงาน</span><span class="sxs-lookup"><span data-stu-id="a3981-130">This release includes a change to not write HCMWorkerPayrollInfo records without reference to an employee.</span></span>

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a><span data-ttu-id="a3981-131">สามารถแก้ไขแผนกได้ เมื่อนำทางจากลำดับชั้นของตำแหน่ง (341001)</span><span class="sxs-lookup"><span data-stu-id="a3981-131">Able to edit department when navigating from position hierarchy (341001)</span></span>

<span data-ttu-id="a3981-132">เมื่อมีการตั้งค่าการรักษาความปลอดภัยเพื่อปฏิเสธการเข้าถึงการแก้ไขแผนก การแก้ไขจะถูกปิดใช้งาน เมื่อนำทางไปยังฟอร์ม **แผนก** ในสถานการณ์จำลองทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a3981-132">When security has been set up to deny access to editing departments, editing is disabled when navigating to the **Departments** form in all scenarios.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="a3981-133">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="a3981-133">Coming soon</span></span>

<span data-ttu-id="a3981-134">โซลูชัน Common Data Service ใหม่จะพร้อมใช้งานเร็วๆ นี้ โดยมีการเปลี่ยนแปลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a3981-134">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="a3981-135">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a3981-135">Description</span></span> | <span data-ttu-id="a3981-136">เปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="a3981-136">Change</span></span> |
| --- | --- |
| <span data-ttu-id="a3981-137">เอนทิตี **งาน/ตำแหน่ง** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a3981-137">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="a3981-138">**ภูมิภาคของค่าตอบแทน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-138">**Compensation region** added</span></span></li><li><span data-ttu-id="a3981-139">**มิติทางการเงิน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-139">**Financial dimensions** added</span></span></li></ul> |
| <span data-ttu-id="a3981-140">เอนทิตี **ผู้ปฏิบัติงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a3981-140">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="a3981-141">**ลำดับชื่อ** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-141">**Name sequence** added</span></span></li><li><span data-ttu-id="a3981-142">เพิ่ม **การทำงานจากที่บ้าน** แล้ว</span><span class="sxs-lookup"><span data-stu-id="a3981-142">**Works from home** added</span></span></li><li><span data-ttu-id="a3981-143">**ภาษา** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-143">**Language** added</span></span></li><li><span data-ttu-id="a3981-144">**วันที่ของอายุงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-144">**Seniority date** added</span></span></li><li><span data-ttu-id="a3981-145">**วันที่ครบรอบปี** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-145">**Anniversary date** added</span></span></li><li><span data-ttu-id="a3981-146">เพิ่ม **วันที่จ้างงานเดิม** แล้ว</span><span class="sxs-lookup"><span data-stu-id="a3981-146">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="a3981-147">เอนทิตี **การจ้างงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a3981-147">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="a3981-148">**มิติทางการเงิน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-148">**Financial dimensions** added</span></span></li><li><span data-ttu-id="a3981-149">**เหตุผลการสิ้นสุดการจ้างงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-149">**Termination reason** added</span></span></li><li><span data-ttu-id="a3981-150">**วันที่สิ้นสุดการจ้างงาน** เปลี่ยนชื่อจาก **วันที่เปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="a3981-150">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="a3981-151">**วันที่ทดลองงาน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-151">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="a3981-152">เอนทิตี **ที่อยู่ผู้ปฏิบัติงาน** เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a3981-152">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="a3981-153">**ที่อยู่ถนน** ที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3981-153">**Street address** added</span></span></li><li><span data-ttu-id="a3981-154">**บรรทัดที่อยู่ 1** **บรรทัดที่อยู่ 2** และ **บรรทัดที่อยู่ 3** ที่ทำเครื่องหมายสำหรับค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="a3981-154">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="a3981-155">เอนทิตีการตั้งค่าค่าตอบแทนผันแปรใหม่</span><span class="sxs-lookup"><span data-stu-id="a3981-155">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="a3981-156">**ชนิดแผนตัวแปรค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="a3981-156">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="a3981-157">**แผนค่าตอบแทนผันแปร**</span><span class="sxs-lookup"><span data-stu-id="a3981-157">**Compensation variable plan**</span></span></li><li><span data-ttu-id="a3981-158">**กฎสิทธิพึงได้**</span><span class="sxs-lookup"><span data-stu-id="a3981-158">**Vesting rules**</span></span></li><li><span data-ttu-id="a3981-159">**ระดับแผนตัวแปรค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="a3981-159">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="a3981-160">เอนทตี **การจ้างงานในปฏิทินของผู้ปฏิบัติงาน** ใหม่</span><span class="sxs-lookup"><span data-stu-id="a3981-160">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="a3981-161">เพิ่ม **เอนทิตีปฏิทินงาน** แล้ว</span><span class="sxs-lookup"><span data-stu-id="a3981-161">**Work calendar entity** added</span></span></li></ul> |
