---
title: ตั้งค่าหลักสูตรการฝึกอบรม
description: ผู้ดูแลระบบทรัพยากรบุคคลและผู้จัดการสามารถใช้ลักษณะการทำงานของหลักสูตรในการรักษาข้อมูลเกี่ยวกับการฝึกอบรมที่ให้แก่ผู้ปฏิบัติงาน
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 253f0d07679b6327a0ed1e3cc20ede66249750b8
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429347"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="9d2d3-103">ตั้งค่าหลักสูตรการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="9d2d3-103">Set up training courses</span></span>

<span data-ttu-id="9d2d3-104">ผู้ดูแลระบบทรัพยากรบุคคลและผู้จัดการสามารถใช้ลักษณะการทำงานของหลักสูตรในการรักษาข้อมูลเกี่ยวกับการฝึกอบรมที่ให้แก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="9d2d3-105"> ตั้งค่าข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9d2d3-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="9d2d3-106">ข้อมูลต่อไปนี้จำเป็นและต้องตั้งค่าก่อนที่คุณจะสร้างหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="9d2d3-107">**ชนิดของหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-107">**Course types**</span></span>

<span data-ttu-id="9d2d3-108">ข้อมูลต่อไปนี้คือข้อมูลตัวเลือกที่คุณสามารถระบุสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="9d2d3-109">หากคุณทราบว่าคุณจะป้อนข้อมูลนี้สำหรับหลักสูตร คุณควรตั้งค่าข้อมูลนี้ก่อนที่คุณจะสร้างเรกคอร์ดหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="9d2d3-110">**กลุ่มห้องเรียน**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-110">**Classroom groups**</span></span>
-   <span data-ttu-id="9d2d3-111">**กลุ่มหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-111">**Course groups**</span></span>
-   <span data-ttu-id="9d2d3-112">**สถานที่จัดหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-112">**Course locations**</span></span>
-   <span data-ttu-id="9d2d3-113">**ห้องเรียน**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-113">**Classrooms**</span></span>
-   <span data-ttu-id="9d2d3-114">**ผู้สอน**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="9d2d3-115">ชนิดของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-115">Course types</span></span>
<span data-ttu-id="9d2d3-116">คุณสามารถใช้ชนิดของหลักสูตรในการจัดประเภทหลักสูตรตามโครงสร้างหรือเนื้อหาของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="9d2d3-117">คุณสามารถสร้างชนิดของหลักสูตรใน **หน้าชนิดของหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="9d2d3-118">คุณต้องเลือกชนิดของหลักสูตรเมื่อคุณสร้างเรกคอร์ดหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="9d2d3-119">ตั้งค่าชนิดของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-119">Course setup type</span></span>
<span data-ttu-id="9d2d3-120">ตารางต่อไปนี้แสดงรายการสามชนิดการตั้งค่าสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="9d2d3-121">ชนิดการตั้งค่ากำหนดโครงสร้างของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d2d3-122">ชนิดการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9d2d3-122">Setup type</span></span></th>
<th><span data-ttu-id="9d2d3-123">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9d2d3-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d2d3-124"><strong>มาตรฐาน</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="9d2d3-125">เลือกชนิดนี้สำหรับหลักสูตรที่จะไม่มีการประชุมประจำวัน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="9d2d3-126">นี่คือชนิดการตั้งค่าเริ่มต้นเมื่อคุณสร้างหลักสูตรใหม่</span><span class="sxs-lookup"><span data-stu-id="9d2d3-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d2d3-127"><strong>วาระการประชุม</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="9d2d3-128">เลือกชนิดนี้เพื่อวางแผนรายละเอียดของแต่ละวันของหลักสูตรที่เกิดขึ้นในช่วงหลายวัน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d2d3-129"><strong>วาระการประชุม+รอบเวลา</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="9d2d3-130">เลือกชนิดนี้สำหรับหลักสูตรที่ซับซ้อนมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="9d2d3-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="9d2d3-131">ตัวอย่างเช่น คุณสามารถแบ่งวาระการประชุมสำหรับหลักสูตรเป็นแทร็คและรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="9d2d3-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="9d2d3-132"><strong>แทร็ค</strong> – แทร็คคือพื้นที่ชื่อเรื่องที่เฉพาะเจาะจงสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="9d2d3-133"><strong>รอบเวลา</strong> – รอบเวลาแบ่งแทร็คและช่วยระบุกระบวนการเฉพาะหรือเทคนิคที่เกี่ยวข้องกับแทร็ค</span><span class="sxs-lookup"><span data-stu-id="9d2d3-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="9d2d3-134">งานหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-134">Course tasks</span></span>
<span data-ttu-id="9d2d3-135">สำหรับแต่ละหลักสูตร คุณสามารถทำงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9d2d3-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="9d2d3-136">ลงทะเบียนผู้เรียน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-136">Register participants</span></span>
- <span data-ttu-id="9d2d3-137">ระบุกำหนดเวลาสิ้นสุดของการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-137">Specify a registration deadline</span></span>
- <span data-ttu-id="9d2d3-138">กำหนดจำนวนต่ำสุดและสูงสุดของผู้เรียน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="9d2d3-139">กำหนดสถานที่จัดหลักสูตรและห้องเรียน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="9d2d3-140">แนะนำโรงแรมให้ผู้เข้าร่วมหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="9d2d3-141">สร้างคำอธิบายหลักสูตร ซึ่งคุณสามารถโฆษณาบนการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="9d2d3-142">**หมายเหตุ** คุณสามารถลบหลักสูตรเมื่อไม่มีใครลงทะเบียนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9d2d3-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="9d2d3-143">สถานะของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-143">Course statuses</span></span>
<span data-ttu-id="9d2d3-144">ตารางต่อไปนี้แสดงสถานะหลักสูตรเป็นไปได้และการดำเนินการที่คุณสามารถทำได้เมื่อหลักสูตรที่มีสถานะเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="9d2d3-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d2d3-145">สถานะ</span><span class="sxs-lookup"><span data-stu-id="9d2d3-145">Status</span></span></th>
<th><span data-ttu-id="9d2d3-146">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9d2d3-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d2d3-147"><strong>ที่สร้าง</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="9d2d3-148">ป้อนและแก้ไขข้อมูลหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="9d2d3-149">เปลี่ยนสถานะหลักสูตรเป็น <strong>เปิด</strong> เพื่อให้ผู้ปฏิบัติงานสามารถลงทะเบียนสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d2d3-150"><strong>เปิด</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="9d2d3-151">ลงทะเบียนผู้เข้าร่วมสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="9d2d3-152">ลบผู้เข้าร่วมออกจากหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="9d2d3-153">ยืนยันผู้เข้าร่วมสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="9d2d3-154">เปลี่ยนสถานะหลักสูตรเป็น<strong> ปิด</strong> หรือ <strong>ยกเลิกแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="9d2d3-155">วางแผนแบบสอบถามสำหรับผู้เรียนที่มีสถานะเป็น <strong>ยืนยันแล้ว</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d2d3-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d2d3-156"><strong>ปิดแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="9d2d3-157">คุณสามารถเปิดหลักสูตรอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="9d2d3-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d2d3-158"><strong>ยกเลิกแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="9d2d3-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="9d2d3-159">คุณสามารถเปิดหลักสูตรอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="9d2d3-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="9d2d3-160">ผู้เข้าร่วมหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="9d2d3-160">Course participants</span></span>
<span data-ttu-id="9d2d3-161">ผู้เข้าร่วมหลักสูตรคือ ผู้ปฏิบัติงานที่มีส่วนร่วมในหลักสูตรการฝึกอบรมหรือเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="9d2d3-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="9d2d3-162">คุณสามารถลงทะเบียนผู้เรียนสำหรับหลักสูตรที่เปิดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9d2d3-162">You can only register participants for open courses.</span></span> <span data-ttu-id="9d2d3-163">จำนวนผู้เรียนต่ำสุดและสูงสุดที่คุณสามารถลงทะเบียนได้สำหรับหลักสูตรที่มีการกำหนดไว้บนแท็บด่วน **ทั่วไป** บนหน้า **หลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="9d2d3-164">ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9d2d3-164">Workflow</span></span>
--------

<span data-ttu-id="9d2d3-165">พนักงานที่ลงทะเบียนสำหรับหลักสูตรโดยผ่านหน้า **การบริการตนเองของพนักงาน** สามารถมีเส้นทางการลงทะเบียนผ่านลำดับงานเพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="9d2d3-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="9d2d3-166">คุณสามารถกำหนดลำดับงานให้กับหลักสูตรใน FastTab **ทั่วไป** บนหน้า **หลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="9d2d3-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





