---
title: ใช้ลำดับงานเพื่อจัดการข้อมูลพนักงาน
description: บทความนี้อธิบายถึงวิธีการที่คุณสามารถใช้ความสามารถของลำดับงานสำหรับฝ่ายทรัพยากรบุคคลเพื่อจัดการข้อมูลพนักงาน ตัวอย่างเช่น คุณสามารถเชื่อมโยงลำดับงานกับตำแหน่งงาน และตั้งค่าคอนฟิกลำดับงานการอนุมัติที่เริ่มต้นเมื่อพนักงานเปลี่ยนบันทึกของพวกเขา
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aba7627877cd9b79dce5930e528f892e2d80baac
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058763"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="03a52-104">ใช้ลำดับงานเพื่อจัดการข้อมูลพนักงาน</span><span class="sxs-lookup"><span data-stu-id="03a52-104">Use workflows to manage employee information</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="03a52-105">บทความนี้อธิบายถึงวิธีการที่คุณสามารถใช้ความสามารถของลำดับงานสำหรับฝ่ายทรัพยากรบุคคลเพื่อจัดการข้อมูลพนักงาน</span><span class="sxs-lookup"><span data-stu-id="03a52-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="03a52-106">ตัวอย่างเช่น คุณสามารถเชื่อมโยงลำดับงานกับตำแหน่งงาน และตั้งค่าคอนฟิกลำดับงานการอนุมัติที่เริ่มต้นเมื่อพนักงานเปลี่ยนบันทึกของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="03a52-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="03a52-107">ความสามารถของลำดับงานสำหรับฝ่ายทรัพยากรบุคคลให้ลำดับงานจำนวนมากสำหรับการจัดการกิจกรรมของฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="03a52-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="03a52-108">นอกจากนี้ ยังมีตัวเลือกจำนวนมากที่พร้อมใช้งานเพื่อให้คุณสามารถปรับเปลี่ยนลำดับงานที่เฉพาะเจาะจง และเชื่อมโยงกับลำดับชั้นการรายงาน</span><span class="sxs-lookup"><span data-stu-id="03a52-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="03a52-109">ลำดับงานจะพร้อมใช้งานเพื่อช่วยในการจัดการการเปลี่ยนแปลงข้อมูลพนักงานชนิดมาตรฐานจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="03a52-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="03a52-110">คุณสามารถเชื่อมโยงลำดับงานกับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="03a52-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="03a52-111">จากนั้น ถ้าพนักงานเปลี่ยนบันทึกพนักงานของตน ลำดับงานจะเริ่มต้นซึ่งต้องมีการอนุมัติก่อนที่จะบันทึกข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="03a52-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="03a52-112">ลำดับงานจะถูกกำหนดล่วงหน้าสำหรับชนิดของข้อมูลต่อไปนี้เพื่อช่วยคุณในการจัดการการเปลี่ยนแปลงได้อย่างมีประสิทธิภาพ และรักษาให้ข้อมูลของพนักงานของคุณถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="03a52-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="03a52-113">หมายเลขรหัส</span><span class="sxs-lookup"><span data-stu-id="03a52-113">Identification numbers</span></span>
-   <span data-ttu-id="03a52-114">หลักสูตร</span><span class="sxs-lookup"><span data-stu-id="03a52-114">Courses</span></span>
-   <span data-ttu-id="03a52-115">การศึกษา</span><span class="sxs-lookup"><span data-stu-id="03a52-115">Education</span></span>
-   <span data-ttu-id="03a52-116">รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="03a52-116">Image</span></span>
-   <span data-ttu-id="03a52-117">รายการที่ยืม</span><span class="sxs-lookup"><span data-stu-id="03a52-117">Loaned items</span></span>
-   <span data-ttu-id="03a52-118">ประสบการณ์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="03a52-118">Professional experience</span></span>
-   <span data-ttu-id="03a52-119">ประสบการณ์โครงการ</span><span class="sxs-lookup"><span data-stu-id="03a52-119">Project experience</span></span>
-   <span data-ttu-id="03a52-120">ทักษะ</span><span class="sxs-lookup"><span data-stu-id="03a52-120">Skills</span></span>
-   <span data-ttu-id="03a52-121">ตำแหน่งตัวแทนของบริษัท</span><span class="sxs-lookup"><span data-stu-id="03a52-121">Positions of trust</span></span>
-   <span data-ttu-id="03a52-122">การดำเนินการของฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="03a52-122">Human resources actions</span></span>
-   <span data-ttu-id="03a52-123">การลงทะเบียนหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="03a52-123">Course registration</span></span>

<span data-ttu-id="03a52-124">เมื่อพนักงานได้รับการจ้างงาน โอนย้าย สิ้นสุดการจ้างงาน ลำดับงานอาจรวมถึงกระบวนการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="03a52-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="03a52-125">ด้วยวิธีนี้ คุณสามารถแก้ไขเอกสารหรือกำหนดเงื่อนไขของการดำเนินการโดยเป็นส่วนหนึ่งของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="03a52-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="03a52-126">เมื่อกระบวนการตรวจทานเสร็จสมบูรณ์ เอกสารหรือการดำเนินการจะเสร็จสมบูรณ์ และลำดับงานจะย้ายไปยังขั้นตอนการอนุมัติขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="03a52-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="03a52-127">เชื่อมโยงลำดับงานกับลำดับชั้นของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="03a52-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="03a52-128">คุณสามารถเชื่อมโยงลำดับงานกับลำดับชั้นใด ๆ ที่คุณตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="03a52-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="03a52-129">ตัวอย่างเช่น ถ้าตำแหน่งถูกเชื่อมโยงกับลำดับชั้นการรายงานเมทริกซ์ คุณอาจตั้งค่าคอนฟิกลำดับงานที่ใช้ในค่าใช้จ่ายสำหรับโครงการที่เฉพาะเจาะจงไปยังลูกค้าเป้าหมายของโครงการแทนผู้จัดการของพนักงานที่เกี่ยวข้องกับตำแหน่งงานนั้น</span><span class="sxs-lookup"><span data-stu-id="03a52-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="03a52-130">เมื่อต้องการสร้างลำดับงานใหม่หรือปรับเปลี่ยนลำดับงานที่มีอยู่ บนหน้า **ลำดับงานของฝ่ายทรัพยากรบุคคล** คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="03a52-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="03a52-131">เลือกลำดับงานในรายการเพื่อเริ่มการทำงานของโปรแกรมออกแบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="03a52-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="03a52-132">คุณสามารถใช้ตัวออกแบบในการสร้างลำดับงานใหม่หรือเปลี่ยนแปลงขั้นตอนในลำดับงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="03a52-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="03a52-133">เมื่อคุณเปลี่ยนลำดับงานที่มีอยู่ การเปลี่ยนแปลงของคุณจะถูกบันทึกเป็นเวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="03a52-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="03a52-134">ดังนั้น คุณสามารถกลับไปยังเวอร์ชันก่อนหน้านี้ได้เสมอถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="03a52-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="03a52-135">ตั้งค่าคอนฟิกลำดับงานของฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="03a52-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="03a52-136">เมื่อต้องการตั้งค่าคอนฟิกลำดับงานพื้นฐานที่เริ่มต้นเมื่อพนักงานร้องขอการเปลี่ยนแปลงรหัสประจำตัวของพวกเขา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="03a52-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="03a52-137">ในหน้า **ลำดับงานของฝ่ายทรัพยากรบุคคล** คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="03a52-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="03a52-138">ในรายการของลำดับงานที่พร้อมใช้งาน เลือก **หมายเลขประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="03a52-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="03a52-139">คลิก **รัน** เพื่อเริ่มการทำงานของโปรแกรมออกแบบลำดับงาน และจากนั้น ป้อนชื่อผู้ใช้และรหัสผ่านของคุณเมื่อคุณได้รับพร้อมท์</span><span class="sxs-lookup"><span data-stu-id="03a52-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="03a52-140">ลากองค์ประกอบ **อนุมัติหมายเลขรหัส** จากรายการขององค์ประกอบลำดับงานไปยังผืนผ้าใบโปรแกรมออกแบบ</span><span class="sxs-lookup"><span data-stu-id="03a52-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="03a52-141">เชื่อมต่อองค์ประกอบการอนุมัติเพื่อ **เริ่มต้น** และ **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="03a52-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="03a52-142">คลิกสองครั้งที่ **อนุมัติองค์ประกอบ** แล้วคลิกขวาและเลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="03a52-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="03a52-143">ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มคำแนะนำเกี่ยวกับรายการงาน:</span><span class="sxs-lookup"><span data-stu-id="03a52-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="03a52-144">เลือก **การกำหนด** และจากนั้นเลือก **ลำดับชั้น** ภายใต้ชนิดการกำหนด</span><span class="sxs-lookup"><span data-stu-id="03a52-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="03a52-145">ภายใต้การเลือก **ลำดับชั้น** เลือก **ลำดับชั้นที่ตั้งค่าคอนฟิกได้**</span><span class="sxs-lookup"><span data-stu-id="03a52-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="03a52-146">เพิ่มเงื่อนไขการหยุด และปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="03a52-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="03a52-147">ทำคำแนะนำเพิ่มเติมใดๆ ให้เสร็จสมบูรณ์ (ไม่ควรมีคำเตือนเพิ่มเติมใดๆ)</span><span class="sxs-lookup"><span data-stu-id="03a52-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="03a52-148">คลิก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="03a52-148">Click **Save and close**.</span></span> <span data-ttu-id="03a52-149">เรียกใช้ลำดับงานใหม่เมื่อกล่องโต้ตอบเปิดขึ้น และเลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="03a52-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="03a52-150">ไปที่ **ทรัพยากรบุคคล** &gt; **ตำแหน่ง** &gt; **ชนิดลำดับชั้นของตำแหน่งงาน**</span><span class="sxs-lookup"><span data-stu-id="03a52-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="03a52-151">เลือก **เมทริกซ์**</span><span class="sxs-lookup"><span data-stu-id="03a52-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="03a52-152">เพิ่มลำดับงาน **หมายเลขรหัสผู้ปฏิบัติงาน** ลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="03a52-152">Add the **Worker identification number** workflow to the list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03a52-153">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="03a52-153">Additional resources</span></span>

[<span data-ttu-id="03a52-154">ดูและจัดการการเปลี่ยนแปลงที่อยู่</span><span class="sxs-lookup"><span data-stu-id="03a52-154">View and manage address changes</span></span>](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]