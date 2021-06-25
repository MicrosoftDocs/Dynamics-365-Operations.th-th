---
title: ป้อนทักษะ
description: งานและผู้จัดการสามารถป้อนทักษะใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193988"
---
# <a name="enter-skills"></a><span data-ttu-id="e68d8-103">ป้อนทักษะ</span><span class="sxs-lookup"><span data-stu-id="e68d8-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e68d8-104">คุณสามารถป้อนเป้าหมายทักษะทักษะที่แท้จริงสำหรับผู้ปฏิบัติงาน ผู้สมัคร หรือผู้ติดต่อใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="e68d8-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e68d8-105">ทักษะเป้าหมายเป็นทักษะที่บุคคลวางแผนเพื่อให้บรรลุผลสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="e68d8-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="e68d8-106">ทักษะที่แท้จริงเป็นทักษะที่บุคคลมีอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e68d8-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="e68d8-107">สร้างลำดับงานเพื่ออนุมัติทักษะโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e68d8-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="e68d8-108">หากต้องการป้อนทักษะโดยไม่ต้องใช้การอนุมัติ คุณต้องสร้างลำดับงานเพื่ออนุมัติทักษะโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e68d8-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="e68d8-109">ทักษะที่ป้อนโดยผู้ปฏิบัติงานจะต้องมีการอนุมัติจากผู้จัดการเสมอ</span><span class="sxs-lookup"><span data-stu-id="e68d8-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="e68d8-110">ลำดับงานนี้จะอนุมัติเฉพาะทักษะที่ป้อนโดยผู้จัดการในนามของผู้ปฏิบัติงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e68d8-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="e68d8-111">ในพื้นที่ทำงาน **การจัดการบุคลากร** ให้เลือก **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="e68d8-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="e68d8-112">ภายใต้ **ตั้งค่า** โปรดเลือก **ลำดับงานของฝ่ายทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="e68d8-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="e68d8-113">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e68d8-113">Select **New**.</span></span>

4. <span data-ttu-id="e68d8-114">ในบานหน้าต่าง **สร้างลำดับงาน** ให้เลือก **ทักษะของผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="e68d8-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="e68d8-115">[![เลือกลำดับงานทักษะของผู้ปฏิบัติงาน](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="e68d8-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="e68d8-116">ในกล่องโต้ตอบ **เปิดไฟล์นี้** ให้เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="e68d8-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="e68d8-117">เมื่อได้รับการพร้อมต์ ป้อนข้อมูลส่วนตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="e68d8-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="e68d8-118">ในฟิลด์แก้ไขลลำดับงาน เลือกลำดับงาน **อนุมัติทักษะ** และลากไปที่พื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="e68d8-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="e68d8-119">[![เลือกอนุมัติองค์ประกอบลำดับงานทักษะ](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="e68d8-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="e68d8-120">เชื่อมต่อองค์ประกอบ **เริ่มต้น** กับองค์ประกอบ **อนุมัติทักษะ 1** แล้วเชื่อมต่อองค์ประกอบ **อนุมัติทักษะ 1** กับองค์ประกอบ **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="e68d8-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="e68d8-121">คุณอาจต้องเลื่อนลงเพื่อดูองค์ประกอบ **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="e68d8-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="e68d8-122">คุณสามารถลากองค์ประกอบใกล้กับองค์ประกอบอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="e68d8-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="e68d8-123">[![เชื่อมต่อองค์ประกอบลำดับงาน](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="e68d8-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="e68d8-124">คลิกสองครั้งที่องค์ประกอบลำดับงาน **อนุมัติทักษะ 1** แล้วคลิกขวาที่องค์ประกอบ **ขั้นตอนที่ 1**</span><span class="sxs-lookup"><span data-stu-id="e68d8-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="e68d8-125">คลิกขวาที่องค์ประกอบ **ขั้นตอนที่ 1** แล้วเลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="e68d8-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="e68d8-126">ในหน้าต่าง **คุณสมบัติ** ให้เลือก **เงื่อนไข** บนแถบทางซ้ายมือ</span><span class="sxs-lookup"><span data-stu-id="e68d8-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="e68d8-127">เลือก **รันขั้นตอนนี้เมื่อเป็นไปตามเงื่อนไขต่อไปนี้เท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="e68d8-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="e68d8-128">เลือก **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="e68d8-128">Select **Add condition**.</span></span> <span data-ttu-id="e68d8-129">หลังจาก **Where** เลือก **ทักษะการให้บริการตนเองของพนักงาน** แล้วเลือก **ทักษะการให้บริการตนเองของพนักงาน.บุคคล**</span><span class="sxs-lookup"><span data-stu-id="e68d8-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="e68d8-130">หลังจาก **is** เลือก **ฟิลด์** แล้วเลือก **ความสัมพันธ์ผู้ใช้กับบุคคล.บุคคล**</span><span class="sxs-lookup"><span data-stu-id="e68d8-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="e68d8-131">[![ระบุเงื่อนไข](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="e68d8-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="e68d8-132">เลือก **การมอบหมาย** บนแถบทางซ้ายมือ</span><span class="sxs-lookup"><span data-stu-id="e68d8-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="e68d8-133">บนแท็บ **ชนิดการมอบหมาย** ให้เลือก **ลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="e68d8-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="e68d8-134">บนแท็บ **การเลือกลำดับชั้น** ในฟิลด์ **ชนิดของลำดับชั้น:** ให้เลือก **ลำดับชั้นด้านการจัดการ**</span><span class="sxs-lookup"><span data-stu-id="e68d8-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="e68d8-135">[![ระบุลำดับชั้นด้านการจัดการ](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="e68d8-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="e68d8-136">เลือก **ปิด** เลือก **ลำดับงาน** ในการแสดงเส้นทางพื้นที่ทำงาน แล้วเลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="e68d8-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="e68d8-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างลำดับงาน โปรดดูที่ [ภาพรวมของระบบลำดับงาน](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json)</span><span class="sxs-lookup"><span data-stu-id="e68d8-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="e68d8-138">ป้อนทักษะของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e68d8-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="e68d8-139">เลือกผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e68d8-139">Select a worker.</span></span>

2. <span data-ttu-id="e68d8-140">ในแถบการมอบหมายของหน้า **ผู้ปฏิบัติงาน** ให้เลือก **บุคคล** แล้วเลือก **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="e68d8-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="e68d8-141">บนหน้า **ทักษะ** ให้กรอกข้อมูลในฟิลด์ต่อไปนี้ของทักษะแต่ละอย่าง</span><span class="sxs-lookup"><span data-stu-id="e68d8-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="e68d8-142">**ทักษะ**: เลือกทักษะ</span><span class="sxs-lookup"><span data-stu-id="e68d8-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="e68d8-143">**ชนิดระดับ**: เลือก **ค่าจริง** สำหรับทักษะที่ผู้ปฏิบัติงานมีอยู่แล้ว หรือเลือก **เป้าหมาย** ของทักษะที่ผู้ปฏิบัติงานใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="e68d8-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="e68d8-144">**ระดับ**: เลือกระดับสำหรับทักษะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e68d8-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="e68d8-145">**วันที่ระดับ**: เลือกวันที่ในเครื่องมือปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="e68d8-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="e68d8-146">**ผู้ตรวจสอบ**: ถ้าเหมาะสม ให้เลือกผู้ตรวจสอบจากรายการ</span><span class="sxs-lookup"><span data-stu-id="e68d8-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="e68d8-147">คุณสามารถกรองข้อมูลการค้นหาของคุณได้</span><span class="sxs-lookup"><span data-stu-id="e68d8-147">You can filter your search.</span></span>
   - <span data-ttu-id="e68d8-148">**ปีประสบการณ์**: ป้อนปีประสบการณ์</span><span class="sxs-lookup"><span data-stu-id="e68d8-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="e68d8-149">**ตรวจสอบความถูกต้อง**: ถ้ามีการตรวจสอบความถูกต้องของทักษะ ให้เลือกกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="e68d8-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="e68d8-150">**ตรวจสอบโดย**: ป้อนชื่อของผู้ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e68d8-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="e68d8-151">เมื่อคุณป้อนทักษะเสร็จแล้ว ให้เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e68d8-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e68d8-152">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="e68d8-152">See also</span></span>

[<span data-ttu-id="e68d8-153">กำหนดค่าทักษะ</span><span class="sxs-lookup"><span data-stu-id="e68d8-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="e68d8-154">แม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="e68d8-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]