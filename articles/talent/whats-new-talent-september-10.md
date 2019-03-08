---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (10 กันยายน 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306474"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a><span data-ttu-id="1312f-103">มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (10 กันยายน 2018)</span><span class="sxs-lookup"><span data-stu-id="1312f-103">What's new or changed in Dynamics 365 for Talent Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1312f-104">**สร้าง 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="1312f-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="1312f-105">หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR</span><span class="sxs-lookup"><span data-stu-id="1312f-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="1312f-106">อนุญาตเวลาที่เฉพาะเจาะจงของวันในคำร้องขอเวลาหยุดพัก (ครึ่งวัน)</span><span class="sxs-lookup"><span data-stu-id="1312f-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="1312f-107">หากการลางานและการขาดงานถูกตั้งค่า เพื่อให้เวลาหยุดพักถูกส่งในหน่วยวัน ขณะนี้ คุณยังสามารถเปิดใช้งานคำนิยามครึ่งวันอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="1312f-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="1312f-108">จากนั้น เมื่อผู้ใช้ส่งคำขอของเวลาหยุดพัก พวกเขาสามารถระบุได้ว่า พวกเขาร้องขอวันหยุดครึ่งวันแรก หรือครึ่งวันหลัง</span><span class="sxs-lookup"><span data-stu-id="1312f-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="1312f-109">โดยค่าเริ่มต้น ตัวเลือกนี้จะถูกปิดไว้</span><span class="sxs-lookup"><span data-stu-id="1312f-109">By default, this option is turned off.</span></span> <span data-ttu-id="1312f-110">สำหรับพนักงานที่จะร้องขอวันหยุดครึ่งวันแรกหรือครึ่งวันหลัง คุณต้องเปิดใช้งานตัวเลือกนี้ในพื้นที่ **การลางานและการขาดงาน** ของพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="1312f-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="1312f-111">สิทธิ์ความปลอดภัยสำหรับคุณลักษณะนี้คือ รักษาพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="1312f-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="1312f-112">การตรวจสอบของรายการการขาดงานและการลางาน</span><span class="sxs-lookup"><span data-stu-id="1312f-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="1312f-113">โดยขึ้นอยู่กับวิธีการตั้งค่าคอนฟิกการลางาน พนักงานที่พยายามส่งคำขอเวลาหยุดพักที่ยาวเกินกว่าจำนวนวันทำงานของพวกเขา จะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="1312f-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="1312f-114">กล่าวคือ รายการเหล่านั้นจะได้รับการเตือน ถ้าพวกเขาใช้เวลามากกว่าหนึ่งวันเต็มๆ ในวันที่ใด ๆ ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1312f-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="1312f-115">การตรวจสอบนี้ถูกเปิดอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="1312f-115">This validation is always turned on.</span></span> <span data-ttu-id="1312f-116">เวลาใดๆ ที่พนักงานเกินขีดจำกัดวันที่กำหนดไว้ พวกเขาจะได้รับคำเตือนในคำขอเวลาหยุดพักของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="1312f-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="1312f-117">ฟิลด์เพิ่มเติมสำหรับการกำหนดเงื่อนไขในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="1312f-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="1312f-118">มีการเพิ่มฟิลด์เพิ่มเติมไปยังการกำหนดเงื่อนไขและตัวยึดตำแหน่งสำหรับลำดับงานหลายรายการใน Core HR</span><span class="sxs-lookup"><span data-stu-id="1312f-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="1312f-119">ระบบได้เพิ่มฟิลด์ต่อไปนี้ ไปยังค่าตอบแทน การสิ้นสุดการจ้างงาน และลำดับงานการโอนย้าย:</span><span class="sxs-lookup"><span data-stu-id="1312f-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="1312f-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="1312f-120">EmploymentType</span></span>
- <span data-ttu-id="1312f-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="1312f-121">LegalEntity</span></span>
- <span data-ttu-id="1312f-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="1312f-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="1312f-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="1312f-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="1312f-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="1312f-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="1312f-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="1312f-125">TransitionDate</span></span>
- <span data-ttu-id="1312f-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="1312f-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="1312f-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="1312f-127">WorkerStartDate</span></span>
- <span data-ttu-id="1312f-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="1312f-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="1312f-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="1312f-129">ProbationEndDate</span></span>
- <span data-ttu-id="1312f-130">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1312f-130">Position</span></span>
- <span data-ttu-id="1312f-131">สหภาพ</span><span class="sxs-lookup"><span data-stu-id="1312f-131">Union</span></span>
- <span data-ttu-id="1312f-132">แผนก</span><span class="sxs-lookup"><span data-stu-id="1312f-132">Department</span></span>
- <span data-ttu-id="1312f-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="1312f-133">PositionType</span></span>
- <span data-ttu-id="1312f-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="1312f-134">CompLocation</span></span>
- <span data-ttu-id="1312f-135">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1312f-135">Title</span></span>
- <span data-ttu-id="1312f-136">งาน</span><span class="sxs-lookup"><span data-stu-id="1312f-136">Job</span></span>
- <span data-ttu-id="1312f-137">JobType</span><span class="sxs-lookup"><span data-stu-id="1312f-137">JobType</span></span>
- <span data-ttu-id="1312f-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="1312f-138">JobFamily</span></span>
- <span data-ttu-id="1312f-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="1312f-139">JobFunction</span></span>

<span data-ttu-id="1312f-140">ระบบได้เพิ่มฟิลด์ต่อไปนี้ลงในเวิร์กโฟลว์ตำแหน่ง:</span><span class="sxs-lookup"><span data-stu-id="1312f-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="1312f-141">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1312f-141">Position</span></span>
- <span data-ttu-id="1312f-142">สหภาพ</span><span class="sxs-lookup"><span data-stu-id="1312f-142">Union</span></span>
- <span data-ttu-id="1312f-143">แผนก</span><span class="sxs-lookup"><span data-stu-id="1312f-143">Department</span></span>
- <span data-ttu-id="1312f-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="1312f-144">PositionType</span></span>
- <span data-ttu-id="1312f-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="1312f-145">CompLocation</span></span>
- <span data-ttu-id="1312f-146">ชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1312f-146">Title</span></span>
- <span data-ttu-id="1312f-147">งาน</span><span class="sxs-lookup"><span data-stu-id="1312f-147">Job</span></span>
- <span data-ttu-id="1312f-148">JobType</span><span class="sxs-lookup"><span data-stu-id="1312f-148">JobType</span></span>
- <span data-ttu-id="1312f-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="1312f-149">JobFamily</span></span>
- <span data-ttu-id="1312f-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="1312f-150">JobFunction</span></span>

<span data-ttu-id="1312f-151">ฟิลด์ในคำสั่งแบบมีเงื่อนไขและตัวยึดตำแหน่ง จะพร้อมใช้งานสำหรับผู้ใช้ทั้งหมดที่สามารถเข้าถึงการตั้งค่าคอนฟิกลำดับงานที่กล่าวไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="1312f-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="1312f-152">การนำทางไปยัง Attract จากการจัดการบุคลากร</span><span class="sxs-lookup"><span data-stu-id="1312f-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="1312f-153">ในการจัดการบุคลากร ถ้า Attract ยังไม่ได้ถูกตั้งค่า ส่วน **ผู้สมัครที่จะจ้าง** กำหนดให้ผู้ใช้เริ่มต้นด้วย Attract แทนที่จะแสดงข้อความ "เราไม่พบสิ่งที่จะแสดงไว้ที่นี่"</span><span class="sxs-lookup"><span data-stu-id="1312f-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="1312f-154">การเปลี่ยนแปลงอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1312f-154">Other changes</span></span>

<span data-ttu-id="1312f-155">รุ่นนี้ประกอบด้วยการแก้ไขบักเพิ่มเติมหลายรายการ:</span><span class="sxs-lookup"><span data-stu-id="1312f-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="1312f-156">เมื่อมีการว่าจ้างผู้รับจ้าง แท็บ **ค่าตอบแทน** ไม่ควรพร้อมใช้งานบนหน้าคำขอ/การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1312f-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="1312f-157">ในระหว่างกระบวนการร้องขอการเลิกจ้าง คุณไม่สามารถทำต่อไปได้ จนกว่าฟิลด์ที่จำเป็นทั้งหมดประกอบด้วยข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1312f-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="1312f-158">เรียงปัญหาในการเรียงลำดับและการแสดงวันที่ในการจัดการบุคลากร ได้ถูกระบุ</span><span class="sxs-lookup"><span data-stu-id="1312f-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
