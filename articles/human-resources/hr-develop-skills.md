---
title: กำหนดค่าทักษะ
description: คุณสามารถติดตามทักษะของผู้ปฏิบัติงานของคุณใน Dynamics 365 Human Resources คุณยังสามารถระบุทักษะที่จำเป็นสำหรับงานระบุ
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076570"
---
# <a name="configure-skills"></a><span data-ttu-id="b27c8-104">กำหนดค่าทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b27c8-105">คุณสามารถติดตามทักษะของผู้ปฏิบัติงานของคุณใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="b27c8-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b27c8-106">คุณยังสามารถระบุทักษะที่จำเป็นสำหรับงานระบุ</span><span class="sxs-lookup"><span data-stu-id="b27c8-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="b27c8-107">ตัวอย่างของทักษะที่คุณจะสามารถติดตามได้รวมถึง:</span><span class="sxs-lookup"><span data-stu-id="b27c8-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="b27c8-108">การควบคุมงาน – ความสามารถในการควบคุมงานของบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="b27c8-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="b27c8-109">ความเป็นผู้นำ – ความสามารถในการนำพนักงานและโดเมนธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b27c8-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="b27c8-110">การวางแผน – ความสามารถในการมองไปข้างหน้า มีวิสัยทัศน์ และวิเคราะห์ถึงสิ่งที่จะเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="b27c8-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="b27c8-111">HTML – ความสามารถในการเขียนโค้ด HTML</span><span class="sxs-lookup"><span data-stu-id="b27c8-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="b27c8-112">ถ้าคุณยังไม่ได้ตั้งค่าชนิดทักษะและรูปแบบการประเมิน คุณจะต้องเพิ่มบางอย่างก่อนสร้างทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="b27c8-113">บุคลากรต่อไปนี้สามารถป้อนทักษะให้กับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="b27c8-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="b27c8-114">ผู้ปฏิบัติงานสามารถป้อนทักษะให้กับผู้ปฏิบัติงานเองในระบบพนักงานบริการตนเองได้</span><span class="sxs-lookup"><span data-stu-id="b27c8-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="b27c8-115">ทักษะเหล่านี้ต้องการการอนุมัติจากผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="b27c8-115">These skills require manager approval.</span></span>
- <span data-ttu-id="b27c8-116">ผู้จัดการสามารถป้อนทักษะให้กับผู้ปฏิบัติงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b27c8-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="b27c8-117">คุณสามารถสร้างลำดับงานที่อนุมัติทักษะเหล่านี้โดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="b27c8-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="b27c8-118">สร้างชนิดทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-118">Create a skill type</span></span>

<span data-ttu-id="b27c8-119">ชนิดของทักษะคือประเภทที่ทักษะแต่ละอย่างลดลง เช่น การจัดการ หรือการขาย</span><span class="sxs-lookup"><span data-stu-id="b27c8-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="b27c8-120">ในพื้นที่ทำงาน **การพัฒนาพนักงาน** ให้เลือก **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="b27c8-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="b27c8-121">ภายใต้ **การตั้งค่าความสามารถ** ให้เลือก **ชนิดทักษะ**</span><span class="sxs-lookup"><span data-stu-id="b27c8-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="b27c8-122">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b27c8-122">Select **New**.</span></span>

4. <span data-ttu-id="b27c8-123">กรอกข้อมูลในฟิลด์เหล่านี้ให้เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="b27c8-123">Complete the following fields:</span></span>

   - <span data-ttu-id="b27c8-124">**ชนิดทักษะ**: ให้ป้อนชื่อสำหรับชนิดทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="b27c8-125">**คำอธิบาย**: ให้ป้อนคำอธิบายสำหรับชนิดทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="b27c8-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b27c8-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="b27c8-127">สร้างแบบจำลองการประเมิน</span><span class="sxs-lookup"><span data-stu-id="b27c8-127">Create a rating model</span></span>

<span data-ttu-id="b27c8-128">รูปแบบการประเมินช่วยประเมินระดับจริงของทักษะของบุคคล ระดับของบุคคลควรทำงานเพื่อให้บรรลุผลสำเร็จ หรือระดับของทักษะที่จำเป็นสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="b27c8-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="b27c8-129">มีกำหนดแต่ละระดับในรูปแบบการประเมินตัวคูณ</span><span class="sxs-lookup"><span data-stu-id="b27c8-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="b27c8-130">ในพื้นที่ทำงาน **การพัฒนาพนักงาน** ให้เลือก **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="b27c8-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="b27c8-131">ภายใต้ **การตั้งค่าความสามารถ** ให้เลือก **แบบจำลองการประเมิน**</span><span class="sxs-lookup"><span data-stu-id="b27c8-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="b27c8-132">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b27c8-132">Select **New**.</span></span>

4. <span data-ttu-id="b27c8-133">กรอกข้อมูลในฟิลด์เหล่านี้ให้เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="b27c8-133">Complete the following fields:</span></span>

   - <span data-ttu-id="b27c8-134">**การประเมิน**: ป้อนชื่อของรูปแบบการประเมิน เช่น **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="b27c8-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="b27c8-135">**คำอธิบาย**: ป้อนคำอธิบายเกี่ยวกับแบบจำลองการประเมิน เช่น **การประเมินทักษะ**</span><span class="sxs-lookup"><span data-stu-id="b27c8-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="b27c8-136">ในส่วน **ระดับ** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b27c8-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="b27c8-137">ในแต่ละระดับที่คุณต้องการเพิ่ม ให้กรอกข้อมูลในฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b27c8-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="b27c8-138">**ระดับ**: ป้อนชื่อสำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="b27c8-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="b27c8-139">**คำอธิบาย**: ป้อนคำอธิบายสำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="b27c8-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="b27c8-140">**ตัวคูณ**: ป้อนค่าตัวคูณตั้งแต่ 0-9</span><span class="sxs-lookup"><span data-stu-id="b27c8-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="b27c8-141">ตัวคูณช่วยปรับคะแนนทักษะให้เป็นปกติที่ใช้รูปแบบการประเมินที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b27c8-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="b27c8-142">แต่ละระดับต้องมีตัวคูณเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-142">Each level must have a unique factor.</span></span> <span data-ttu-id="b27c8-143">ระดับที่มีค่าตัวคูณที่สูงกว่ามีน้ำหนักมากกว่าในรูปแบบการประเมิน</span><span class="sxs-lookup"><span data-stu-id="b27c8-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="b27c8-144">เพิ่มระดับต่อไปตามความจําเป็น</span><span class="sxs-lookup"><span data-stu-id="b27c8-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="b27c8-145">คุณสามารถป้อนได้ถึง 10 ระดับสำหรับแต่ละรูปแบบการประเมิน</span><span class="sxs-lookup"><span data-stu-id="b27c8-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="b27c8-146">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b27c8-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="b27c8-147">สร้างทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-147">Create a skill</span></span>

<span data-ttu-id="b27c8-148">ก่อนที่คุณจะสามารถกำหนดทักษะ สร้างการค้นหาการแม็ปทักษะหรือโปรไฟล์ทักษะ คุณต้องป้อนข้อมูลเกี่ยวกับทักษะในหน้า **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="b27c8-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="b27c8-149">สำหรับแต่ละทักษะ คุณสามารถเลือกชนิดของทักษะและแบบจำลองการประเมิน</span><span class="sxs-lookup"><span data-stu-id="b27c8-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="b27c8-150">ในพื้นที่ทำงาน **การพัฒนาพนักงาน** ให้เลือก **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="b27c8-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="b27c8-151">ภายใต้ **การตั้งค่าความสามารถ** ให้เลือก **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="b27c8-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="b27c8-152">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b27c8-152">Select **New**.</span></span>

4. <span data-ttu-id="b27c8-153">กรอกข้อมูลในฟิลด์เหล่านี้ให้เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="b27c8-153">Complete the following fields:</span></span>

   - <span data-ttu-id="b27c8-154">**ทักษะ**: ให้ป้อนชื่อสำหรับทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="b27c8-155">**คำอธิบาย**: ให้ป้อนคำอธิบายสำหรับทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="b27c8-156">**การประเมิน**: เลือกแบบจำลองการประเมินที่คุณต้องการใช้สำหรับทักษะนี้</span><span class="sxs-lookup"><span data-stu-id="b27c8-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="b27c8-157">**ชนิดทักษะ**: เลือกจากรายการของชนิดทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="b27c8-158">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b27c8-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b27c8-159">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b27c8-159">See also</span></span>

[<span data-ttu-id="b27c8-160">ป้อนทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="b27c8-161">แม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="b27c8-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]