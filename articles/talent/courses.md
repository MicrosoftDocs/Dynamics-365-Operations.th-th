---
title: "ตั้งค่าหลักสูตรการฝึกอบรม"
description: "ผู้ดูแลระบบทรัพยากรบุคคลและผู้จัดการสามารถใช้ลักษณะการทำงานของหลักสูตรในการรักษาข้อมูลเกี่ยวกับการฝึกอบรมที่ให้แก่ผู้ปฏิบัติงาน"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0b28c62fe586102a3fb98d77edbea2c06bcf852
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-training-courses"></a><span data-ttu-id="43115-103">ตั้งค่าหลักสูตรการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="43115-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="43115-104">ผู้ดูแลระบบทรัพยากรบุคคลและผู้จัดการสามารถใช้ลักษณะการทำงานของหลักสูตรในการรักษาข้อมูลเกี่ยวกับการฝึกอบรมที่ให้แก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="43115-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="43115-105"> ตั้งค่าข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="43115-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="43115-106">ข้อมูลต่อไปนี้จำเป็นและต้องตั้งค่าก่อนที่คุณจะสร้างหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="43115-107">**ชนิดของหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="43115-107">**Course types**</span></span>

<span data-ttu-id="43115-108">ข้อมูลต่อไปนี้คือข้อมูลตัวเลือกที่คุณสามารถระบุสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="43115-109">หากคุณทราบว่าคุณจะป้อนข้อมูลนี้สำหรับหลักสูตร คุณควรตั้งค่าข้อมูลนี้ก่อนที่คุณจะสร้างเรกคอร์ดหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="43115-110">**กลุ่มห้องเรียน**</span><span class="sxs-lookup"><span data-stu-id="43115-110">**Classroom groups**</span></span>
-   <span data-ttu-id="43115-111">**กลุ่มหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="43115-111">**Course groups**</span></span>
-   <span data-ttu-id="43115-112">**สถานที่จัดหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="43115-112">**Course locations**</span></span>
-   <span data-ttu-id="43115-113">**ห้องเรียน**</span><span class="sxs-lookup"><span data-stu-id="43115-113">**Classrooms**</span></span>
-   <span data-ttu-id="43115-114">**ผู้สอน**</span><span class="sxs-lookup"><span data-stu-id="43115-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="43115-115">ชนิดของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-115">Course types</span></span>
<span data-ttu-id="43115-116">คุณสามารถใช้ชนิดของหลักสูตรในการจัดประเภทหลักสูตรตามโครงสร้างหรือเนื้อหาของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="43115-117">คุณสามารถสร้างชนิดของหลักสูตรใน **หน้าชนิดของหลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="43115-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="43115-118">คุณต้องเลือกชนิดของหลักสูตรเมื่อคุณสร้างเรกคอร์ดหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="43115-119">ตั้งค่าชนิดของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-119">Course setup type</span></span>
<span data-ttu-id="43115-120">ตารางต่อไปนี้แสดงรายการสามชนิดการตั้งค่าสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="43115-121">ชนิดการตั้งค่ากำหนดโครงสร้างของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="43115-122">ชนิดการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="43115-122">Setup type</span></span></th>
<th><span data-ttu-id="43115-123">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="43115-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43115-124"><strong>มาตรฐาน</strong></span><span class="sxs-lookup"><span data-stu-id="43115-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="43115-125">เลือกชนิดนี้สำหรับหลักสูตรที่จะไม่มีการประชุมประจำวัน</span><span class="sxs-lookup"><span data-stu-id="43115-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="43115-126">นี่คือชนิดการตั้งค่าเริ่มต้นเมื่อคุณสร้างหลักสูตรใหม่</span><span class="sxs-lookup"><span data-stu-id="43115-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43115-127"><strong>วาระการประชุม</strong></span><span class="sxs-lookup"><span data-stu-id="43115-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="43115-128">เลือกชนิดนี้เพื่อวางแผนรายละเอียดของแต่ละวันของหลักสูตรที่เกิดขึ้นในช่วงหลายวัน</span><span class="sxs-lookup"><span data-stu-id="43115-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43115-129"><strong>วาระการประชุม+รอบเวลา</strong></span><span class="sxs-lookup"><span data-stu-id="43115-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="43115-130">เลือกชนิดนี้สำหรับหลักสูตรที่ซับซ้อนมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="43115-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="43115-131">ตัวอย่างเช่น คุณสามารถแบ่งวาระการประชุมสำหรับหลักสูตรเป็นแทร็คและรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="43115-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="43115-132"><strong>แทร็ค</strong> – แทร็คคือพื้นที่ชื่อเรื่องที่เฉพาะเจาะจงสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="43115-133"><strong>รอบเวลา</strong> – รอบเวลาแบ่งแทร็คและช่วยระบุกระบวนการเฉพาะหรือเทคนิคที่เกี่ยวข้องกับแทร็ค</span><span class="sxs-lookup"><span data-stu-id="43115-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="43115-134">งานหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-134">Course tasks</span></span>
<span data-ttu-id="43115-135">สำหรับแต่ละหลักสูตร คุณสามารถทำงานต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="43115-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="43115-136">ลงทะเบียนผู้เรียน</span><span class="sxs-lookup"><span data-stu-id="43115-136">Register participants</span></span>
-   <span data-ttu-id="43115-137">ระบุกำหนดเวลาสิ้นสุดของการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="43115-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="43115-138">กำหนดจำนวนต่ำสุดและสูงสุดของผู้เรียน</span><span class="sxs-lookup"><span data-stu-id="43115-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="43115-139">กำหนดสถานที่จัดหลักสูตรและห้องเรียน</span><span class="sxs-lookup"><span data-stu-id="43115-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="43115-140">แนะนำโรงแรมให้ผู้เข้าร่วมหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="43115-141">สร้างคำอธิบายหลักสูตร ซึ่งคุณสามารถโฆษณาบนการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="43115-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="43115-142">**หมายเหตุ** คุณสามารถลบหลักสูตรเมื่อไม่มีใครลงทะเบียนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="43115-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="43115-143">สถานะของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-143">Course statuses</span></span>
<span data-ttu-id="43115-144">ตารางต่อไปนี้แสดงสถานะหลักสูตรเป็นไปได้และการดำเนินการที่คุณสามารถทำได้เมื่อหลักสูตรที่มีสถานะเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="43115-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="43115-145">สถานะ</span><span class="sxs-lookup"><span data-stu-id="43115-145">Status</span></span></th>
<th><span data-ttu-id="43115-146">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="43115-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43115-147"><strong>ที่สร้าง</strong></span><span class="sxs-lookup"><span data-stu-id="43115-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="43115-148">ป้อนและแก้ไขข้อมูลหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="43115-149">เปลี่ยนสถานะหลักสูตรเป็น <strong>เปิด</strong> เพื่อให้ผู้ปฏิบัติงานสามารถลงทะเบียนสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43115-150"><strong>เปิด</strong></span><span class="sxs-lookup"><span data-stu-id="43115-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="43115-151">ลงทะเบียนผู้เข้าร่วมสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="43115-152">ลบผู้เข้าร่วมออกจากหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="43115-153">ยืนยันผู้เข้าร่วมสำหรับหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="43115-154">เปลี่ยนสถานะหลักสูตรเป็น<strong> ปิด</strong> หรือ <strong>ยกเลิกแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="43115-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="43115-155">วางแผนแบบสอบถามสำหรับผู้เรียนที่มีสถานะเป็น <strong>ยืนยันแล้ว</strong>.</span><span class="sxs-lookup"><span data-stu-id="43115-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43115-156"><strong>ปิดแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="43115-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="43115-157">คุณสามารถเปิดหลักสูตรอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="43115-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43115-158"><strong>ยกเลิกแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="43115-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="43115-159">คุณสามารถเปิดหลักสูตรอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="43115-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="43115-160">ผู้เข้าร่วมหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="43115-160">Course participants</span></span>
<span data-ttu-id="43115-161">ผู้เข้าร่วมหลักสูตรคือผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อที่มีส่วนร่วมในหลักสูตรการฝึกอบรมหรือเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="43115-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="43115-162">คุณสามารถลงทะเบียนผู้เรียนสำหรับหลักสูตรที่เปิดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="43115-162">You can only register participants for open courses.</span></span> <span data-ttu-id="43115-163">จำนวนผู้เรียนต่ำสุดและสูงสุดที่คุณสามารถลงทะเบียนได้สำหรับหลักสูตรที่มีการกำหนดไว้บนแท็บด่วน **ทั่วไป** บนหน้า **หลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="43115-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="43115-164">ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="43115-164">Workflow</span></span>
--------

<span data-ttu-id="43115-165">พนักงานที่ลงทะเบียนสำหรับหลักสูตรโดยผ่านหน้า **การบริการตนเองของพนักงาน** สามารถมีเส้นทางการลงทะเบียนผ่านลำดับงานเพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="43115-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="43115-166">ลำดับงานสามารถกำหนดให้กับหลักสูตรในแท็บด่วน **ทั่วไป** บนหน้า **หลักสูตร**</span><span class="sxs-lookup"><span data-stu-id="43115-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>






