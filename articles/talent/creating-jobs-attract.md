---
title: "สร้าง อนุมัติ และลงรายการบัญชีงานใน Attract"
description: "หัวข้อนี้อธิบายองค์ประกอบของงานใน Attract และยังอธิบายถึงวิธีการสร้างงาน"
author: josaw
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: af945042c150fff1a95cdb046f2a712cb2c2c061
ms.contentlocale: th-th
ms.lasthandoff: 10/24/2018

---

# <a name="create-approve-and-post-jobs-in-attract"></a><span data-ttu-id="fee9d-104">สร้าง อนุมัติ และลงรายการบัญชีงานใน Attract</span><span class="sxs-lookup"><span data-stu-id="fee9d-104">Create, approve, and post jobs in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fee9d-105">หัวข้อนี้อธิบายองค์ประกอบของงานใน Microsoft Dynamics 365 for Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="fee9d-105">This topic describes the elements of a job in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="fee9d-106">และยังอธิบายถึงวิธีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-106">It also explains how to create a job.</span></span>

## <a name="job-creation"></a><span data-ttu-id="fee9d-107">การสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-107">Job creation</span></span>

<span data-ttu-id="fee9d-108">ผู้ดูแล ผู้สรรหา และผู้จัดการว่าจ้าง สามารถสร้างงานได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-108">Admins, recruiters, and hiring managers can create jobs.</span></span> <span data-ttu-id="fee9d-109">เมื่อคุณสร้างงาน คุณจะได้รับพร้อมท์ให้เลือกบทบาทของคุณในกระบวนการ: ผู้จัดการว่าจ้าง หรือผู้สรรหา</span><span class="sxs-lookup"><span data-stu-id="fee9d-109">When you create a job, you're prompted to select your role in the process: hiring manager or recruiter.</span></span> <span data-ttu-id="fee9d-110">หลังจากที่คุณเลือกบทบาท คุณจะได้รับพร้อมท์เพื่อเลือกเท็มเพลตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="fee9d-110">After you select a role, you're prompted to select a process template.</span></span> <span data-ttu-id="fee9d-111">ถ้าคุณเลือก **ข้าม** จะมีการใช้เท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fee9d-111">If you select **Skip**, the default template is used.</span></span> <span data-ttu-id="fee9d-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเท็มเพลตกระบวนการ ดู [สร้างเท็มเพลตกระบวนการใน Attract](./process-templates-attract.md)</span><span class="sxs-lookup"><span data-stu-id="fee9d-112">For more information about process templates, see [Create a process template in Attract](./process-templates-attract.md).</span></span>

<span data-ttu-id="fee9d-113">งานใน Attract มีรายละเอียดงาน ทีมว่าจ้าง กระบวนการว่าจ้าง การลงรายการบัญชีงาน และการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="fee9d-113">A job in Attract has job details, a hiring team, a hiring process, job postings, and analytics.</span></span>

## <a name="job-details"></a><span data-ttu-id="fee9d-114">รายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-114">Job details</span></span>

<span data-ttu-id="fee9d-115">แท็บ **รายละเอียดงาน** ประกอบด้วยรายละเอียดเกี่ยวกับความรับผิดชอบและแอททริบิวต์ของงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-115">The **Job details** tab contains details about the job's responsibilities and attributes.</span></span> <span data-ttu-id="fee9d-116">ต้องมีฟิลด์สำหรับตำแหน่งงาน คำอธิบายงาน และตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-116">The fields for the job title, job description, and job location are required.</span></span> <span data-ttu-id="fee9d-117">ฟิลด์อื่นเป็นฟิลด์ที่ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="fee9d-117">The other fields are optional.</span></span>

<span data-ttu-id="fee9d-118">โดยค่าเริ่มต้น ฟิลด์ **จำนวนตำแหน่งที่เปิดรับ** ถูกกำหนดเป็น **1**</span><span class="sxs-lookup"><span data-stu-id="fee9d-118">By default, the **Number of openings** field is set to **1**.</span></span> <span data-ttu-id="fee9d-119">อย่างไรก็ตาม คุณสามารถเปลี่ยนค่าได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-119">However, you can change the value.</span></span> <span data-ttu-id="fee9d-120">เมื่อมีการจัดเตรียมข้อเสนอสำหรับงาน มูลค่าของฟิลด์ **จำนวนตำแหน่งที่เปิดรับที่พร้อมใช้** จะถูกลดลง</span><span class="sxs-lookup"><span data-stu-id="fee9d-120">When an offer has been prepared for a job, the value of the **Number of openings available** field is decremented.</span></span>

<span data-ttu-id="fee9d-121">ถ้าการจัดการตำแหน่งถูกเปิดอยู่ในศูนย์การจัดการ การค้นหา **อัพเดตตำแหน่ง** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-121">If position management has been turned on in the Admin Center, the **Update positions** lookup is available.</span></span> <span data-ttu-id="fee9d-122">การค้นหานี้อ่านเอนทิตี JobPosition ใน Common Data Service for Apps และส่งกลับรายการของตำแหน่งที่สามารถเลือกได้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-122">This lookup reads the JobPosition entity in Common Data Service for Apps and returns a list of positions that can be selected for the job.</span></span> <span data-ttu-id="fee9d-123">ถ้าจำนวนของตำแหน่งที่คุณเลือกเกินจำนวนตำแหน่งที่เปิด คุณจะได้รับคำเตือน</span><span class="sxs-lookup"><span data-stu-id="fee9d-123">If the number of positions that you select exceeds the number of open positions, you receive a warning.</span></span> <span data-ttu-id="fee9d-124">นอกจากนี้ คุณได้รับคำเตือน ถ้ามีการใช้งานในงานหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="fee9d-124">You also receive a warning if a position is used on multiple jobs.</span></span>

> [!NOTE]
> <span data-ttu-id="fee9d-125">การจัดการตำแหน่งจะพร้อมใช้งานโดยมี add-on การว่าจ้างที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="fee9d-125">Position management is available with the Comprehensive Hiring Add-on.</span></span>

<span data-ttu-id="fee9d-126">โดยขึ้นอยู่กับการตั้งค่าในกิจกรรมข้อเสนอของกระบวนการว่าจ้าง สามารถใช้หมายเลขตำแหน่งได้สองครั้งในหนึ่งข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="fee9d-126">Depending on the settings in the Offer activity of the hiring process, a position number can be used twice in an offer.</span></span> <span data-ttu-id="fee9d-127">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [กระบวนการจ้างงาน](./activities-attract.md)</span><span class="sxs-lookup"><span data-stu-id="fee9d-127">For more information, see [Hiring process](./activities-attract.md).</span></span>

<span data-ttu-id="fee9d-128">Attract มีชุดค่าเริ่มต้นของ **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="fee9d-128">Attract includes a default set of **Skills**.</span></span> <span data-ttu-id="fee9d-129">ทักษะเหล่านี้ปรากฏเป็นคำแนะนำขณะที่คุณพิมพ์</span><span class="sxs-lookup"><span data-stu-id="fee9d-129">These skills appear as suggestions as you type.</span></span> <span data-ttu-id="fee9d-130">คุณสามารถเพิ่มทักษะเพิ่มเติมได้โดยป้อนเนื้อหาทักษะใหม่ในฟิลด์ แล้วกดป้อน</span><span class="sxs-lookup"><span data-stu-id="fee9d-130">You can add more skills by entering the new skill text in the field and then pressing Enter.</span></span>

<span data-ttu-id="fee9d-131">Attract รวมชุดค่าเริ่มต้นของ **ฟังก์ชันงาน**</span><span class="sxs-lookup"><span data-stu-id="fee9d-131">Attract includes a default set of **Job functions**.</span></span> <span data-ttu-id="fee9d-132">คุณสามารถเพิ่มฟังก์ชันงานเพิ่มเติมได้ถึงสามรายการ โดยป้อนฟังก์ชันงานใหม่ในฟิลด์ แล้วกดป้อน</span><span class="sxs-lookup"><span data-stu-id="fee9d-132">You can add up to three more job functions by entering the new job function in the field and then pressing Enter.</span></span>

<span data-ttu-id="fee9d-133">Attract รวมชุดค่าเริ่มต้นของ **อุตสาหกรรมของบริษัท**</span><span class="sxs-lookup"><span data-stu-id="fee9d-133">Attract includes a default set of **Company industry**.</span></span> <span data-ttu-id="fee9d-134">คุณสามารถเพิ่มอุตสาหกรรมบริษัทเพิ่มเติมได้ถึงสามรายการ โดยป้อนฟังก์ชันอุตสาหกรรมบริษัทใหม่ในฟิลด์ แล้วกดป้อน</span><span class="sxs-lookup"><span data-stu-id="fee9d-134">You can add up to three more company industries by entering the new company industry in the field and then pressing Enter.</span></span>

## <a name="hiring-team"></a><span data-ttu-id="fee9d-135">ทีมงานการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-135">Hiring team</span></span>

<span data-ttu-id="fee9d-136">แท็บ **ทีมการว่าจ้าง** ประกอบด้วยรายชื่อของบุคคลที่จะเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-136">The **Hiring team** tab contains the list of individuals who will be involved in the job.</span></span> <span data-ttu-id="fee9d-137">เมื่อมีการเพิ่มผู้ใช้ไปยังทีมงานที่ว่าจ้าง พวกเขาต้องถูกกำหนดบทบาทในทีมงานว่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fee9d-137">When users are added to a hiring team, they must be assigned a role on the hiring team.</span></span> <span data-ttu-id="fee9d-138">บทบาทกำหนดข้อมูลที่ผู้ใช้มีสิทธิ์ในการเข้าถึงและการแจ้งเตือนที่พวกเขาได้รับ</span><span class="sxs-lookup"><span data-stu-id="fee9d-138">The role determines the data that the users have access to and the notifications that they receive.</span></span> <span data-ttu-id="fee9d-139">บทบาทที่สามารถถูกเลือกคือ **ผู้สรรหา** **ผู้จัดการที่ว่าจ้าง** **ผู้รับมอบสิทธิ์** และ **ผู้สัมภาษณ์**</span><span class="sxs-lookup"><span data-stu-id="fee9d-139">The roles that can be selected are **Recruiter**, **Hiring manager**, **Delegate**, and **Interviewer**.</span></span> <span data-ttu-id="fee9d-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิพิเศษของบทบาท ดูเอกสาร "การจัดการบทบาท"</span><span class="sxs-lookup"><span data-stu-id="fee9d-140">For more information about role privileges, see the "Role management" document.</span></span> <span data-ttu-id="fee9d-141">ผู้สรรหาและผู้จัดการการว่าจ้างสามารถแต่งตั้งผู้รับมอบสิทธิ์อย่างน้อยหนึ่งราย เพื่อทำงานในนามของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="fee9d-141">Recruiters and hiring managers can appoint one or more delegates to work on their behalf.</span></span> <span data-ttu-id="fee9d-142">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับผู้รับมอบสิทธิ์ ดู [การจัดการความปลอดภัยและบทบาทใน Attract](./security-attract.md)</span><span class="sxs-lookup"><span data-stu-id="fee9d-142">For more information about delegates, see [Security and role management in Attract](./security-attract.md).</span></span>

<span data-ttu-id="fee9d-143">สามารถอัพเดตทีมว่าจ้างได้ หลังจากที่มีการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-143">The hiring team can be updated after the job is activated.</span></span>

## <a name="process"></a><span data-ttu-id="fee9d-144">กระบวนการ</span><span class="sxs-lookup"><span data-stu-id="fee9d-144">Process</span></span>

<span data-ttu-id="fee9d-145">ข้อมูลเริ่มต้นเกี่ยวกับกระบวนการว่าจ้างจะขึ้นอยู่กับเท็มเพลตกระบวนการที่ถูกเลือก เมื่อมีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-145">Default information about the hiring process is based on the process template that was selected when the job was created.</span></span> <span data-ttu-id="fee9d-146">ถ้าเท็มเพลตที่ระบุไม่ถูกเลือกในขณะนั้น จะมีการใช้เท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fee9d-146">If a specific template wasn't selected at that time, the default template is used.</span></span> <span data-ttu-id="fee9d-147">เมื่อคุณกำหนดกระบวนการว่าจ้าง คุณสามารถเพิ่ม หรือลบขั้นตอนต่างๆ ได้ ยกเว้นขั้นผู้ที่มีแนวโน้มจะเป็นลูกค้า แอพลิเคชัน และข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="fee9d-147">When you define the hiring process, you can add or remove various stages, except the Prospect, Application, and Offer stages.</span></span> <span data-ttu-id="fee9d-148">แม้ว่าจะไม่สามารถลบขั้นผู้ที่มีแนวโน้มจะเป็นลูกค้าได้ แต่คุณสามารถปิดได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-148">Although the Prospect stage can't be removed, it can be turned off.</span></span> <span data-ttu-id="fee9d-149">ภายในแต่ละขั้นตอน คุณสามารถเพิ่ม หรือลบกิจกรรมที่กำหนดไว้ล่วงหน้าหนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="fee9d-149">Within each stage, you can add or remove one or more predefined activities.</span></span>

<span data-ttu-id="fee9d-150">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกิจกรรมที่สามารถถูกเพิ่มลงในกระบวนการว่าจ้าง ดู [กิจกรรมกระบวนการว่าจ้างใน Attract](./activities-attract.md)</span><span class="sxs-lookup"><span data-stu-id="fee9d-150">For more information about activities that can be added to the hiring process, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fee9d-151">ไม่สามารถอัพเดตกระบวนการว่าจ้างได้ หลังจากที่มีการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-151">The process hiring can't be updated after a job is activated.</span></span>

## <a name="postings"></a><span data-ttu-id="fee9d-152">การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="fee9d-152">Postings</span></span>

<span data-ttu-id="fee9d-153">หลังจากที่มีการเรียกใช้งาน จึงสามารถลงรายการบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-153">After a job is activated, it can be posted.</span></span> <span data-ttu-id="fee9d-154">เฉพาะผู้สรรหาและผู้ดูแลระบบสามารถลงรายการบัญชีงานได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-154">Only recruiters and admins can post jobs.</span></span> <span data-ttu-id="fee9d-155">งานสามารถถูกลงรายการบัญชีไปยัง Talent Careers (ไซต์ Microsoft Dynamics 365 for Talent career) หรือ LinkedIn อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fee9d-155">The job can be posted to either Talent Careers (a Microsoft Dynamics 365 for Talent career site) or LinkedIn.</span></span> <span data-ttu-id="fee9d-156">ทีม Attract ทำงานกับคู่ค้ากับตัวรวมบอร์ดงานอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="fee9d-156">The Attract team continually works to partner with job board aggregators.</span></span> <span data-ttu-id="fee9d-157">ดังนั้น รายการนี้จะขยายตลอดช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="fee9d-157">Therefore, this list will expand over time.</span></span>

<span data-ttu-id="fee9d-158">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงรายการบัญชีงาน ดู [ฟังก์ชันไซต์ทำงานใน Attract](./career-site.md)</span><span class="sxs-lookup"><span data-stu-id="fee9d-158">For more information about job postings, see [Career site functionality in Attract](./career-site.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fee9d-159">ฟังก์ชันการลงรายการบัญชีงานพร้อมใช้งานเฉพาะกับ Add-on การว่าจ้างที่ครอบคลุมสำหรับ Attract</span><span class="sxs-lookup"><span data-stu-id="fee9d-159">The job posting functionality is available only with the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="activate"></a><span data-ttu-id="fee9d-160">เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-160">Activate</span></span>

<span data-ttu-id="fee9d-161">หลังจากที่มีการเรียกใช้งาน สามารถลงรายการบัญชี และสามารถเพิ่มผู้ที่มีแนวโน้มจะเป็นลูกค้าและผู้สมัครในนั้นได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-161">After a job is activated, it can be posted, and prospects and applicants can be added to it.</span></span> <span data-ttu-id="fee9d-162">มีการตั้งค่าตัวเลือกเพื่อเพิ่มผู้ที่มีแนวโน้มจะเป็นลูกค้า ไปยังงานในกิจกรรมผู้ที่มีแนวโน้มจะเป็นลูกค้าในกระบวนการว่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fee9d-162">The option to add prospects to a job is set in the Prospect activity in the hiring process.</span></span>

> [!NOTE]
> <span data-ttu-id="fee9d-163">ไม่สามารถอัพเดตกระบวนการว่าจ้างได้ หลังจากที่มีการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-163">The process hiring can't be updated after a job is activated.</span></span>

## <a name="prospects-and-applicants"></a><span data-ttu-id="fee9d-164">ผู้ที่มีแนวโน้มจะเป็นลูกค้าและผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="fee9d-164">Prospects and applicants</span></span>

<span data-ttu-id="fee9d-165">มีการตั้งค่าตัวเลือกเพื่อเพิ่มผู้ที่มีแนวโน้มจะเป็นลูกค้าไปยังงานใน [กิจกรรมผู้ที่มีแนวโน้มจะเป็นลูกค้า](./activities-attract.md#prospect-activity) ในกระบวนการว่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fee9d-165">The option to add prospects to a job is set in the [Prospect activity](./activities-attract.md#prospect-activity) in the hiring process.</span></span> <span data-ttu-id="fee9d-166">ควรมีการตั้งค่าตัวเลือกนี้ ก่อนที่คุณจะเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-166">This option should be set before you activate the job.</span></span> <span data-ttu-id="fee9d-167">หลังจากที่มีการเรียกใช้งาน สามารถเพิ่มผู้ที่มีแนวโน้มจะเป็นลูกค้าและผู้สมัครในนั้นได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-167">After a job is activated, prospects and applicants can be added to it.</span></span>

## <a name="approvals"></a><span data-ttu-id="fee9d-168">การอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="fee9d-168">Approvals</span></span>

<span data-ttu-id="fee9d-169">สามารถส่งงาน Attract สำหรับการอนุมัติได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-169">Attract jobs can be submitted for approval.</span></span> <span data-ttu-id="fee9d-170">ไม่จำเป็นต้องมีการอนุมัติงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fee9d-170">Not all jobs require approval.</span></span> <span data-ttu-id="fee9d-171">ความต้องการถูกตั้งค่าที่ระดับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fee9d-171">The requirement is set at the template level.</span></span> <span data-ttu-id="fee9d-172">โดยค่าเริ่มต้น การอนุมัติถูกปิดบนเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fee9d-172">By default, approvals are turned off on the template.</span></span> <span data-ttu-id="fee9d-173">ในการตั้งค่าการอนุมัติ ไปที่เท็มเพลตกระบวนการ และตั้งค่าฟิลด์ **การอนุมัติ** เป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fee9d-173">To set up approvals, go to a process template, and set the **Approval** field to Default.</span></span> <span data-ttu-id="fee9d-174">จากนั้น เลือกเท็มเพลตนั้นเมื่อคุณสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-174">Then select that template when you create the job.</span></span>

<span data-ttu-id="fee9d-175">หลังจากที่มีการบันทึกงาน จะสามารถส่งเพื่อขออนุมัติได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-175">After a job is saved, it can be submitted for approval.</span></span> <span data-ttu-id="fee9d-176">ตารางต่อไปนี้แสดงรายการสถานะของเอกสารที่ใช้การอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="fee9d-176">The following table lists the statuses of a document that uses approvals.</span></span>

| <span data-ttu-id="fee9d-177">สถานะ</span><span class="sxs-lookup"><span data-stu-id="fee9d-177">Status</span></span>   | <span data-ttu-id="fee9d-178">สถานะ</span><span class="sxs-lookup"><span data-stu-id="fee9d-178">State</span></span>                                                               |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="fee9d-179">ร่าง</span><span class="sxs-lookup"><span data-stu-id="fee9d-179">Draft</span></span>    | <span data-ttu-id="fee9d-180">มีการบันทึกงานแล้ว แต่ยังไม่ได้ถูกส่งไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-180">The job has been saved, but it hasn't been submitted to a workflow.</span></span> |
| <span data-ttu-id="fee9d-181">ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="fee9d-181">Pending</span></span>  | <span data-ttu-id="fee9d-182">งานได้ถูกส่งไปยังผู้อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="fee9d-182">The job has been submitted to approvers.</span></span>                            |
| <span data-ttu-id="fee9d-183">อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="fee9d-183">Approved</span></span> | <span data-ttu-id="fee9d-184">งานได้รับอนุมัติแล้ว แต่ยังไม่ได้ถูกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="fee9d-184">The job has been approved, but it hasn't been activated.</span></span>            |
| <span data-ttu-id="fee9d-185">ปฏิเสธแล้ว</span><span class="sxs-lookup"><span data-stu-id="fee9d-185">Rejected</span></span> | <span data-ttu-id="fee9d-186">มีการปฏิเสธงาน และไม่สามารถเรียกใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-186">The job has been rejected, and it can't be activated.</span></span>               |
| <span data-ttu-id="fee9d-187">ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-187">Active</span></span>   | <span data-ttu-id="fee9d-188">งานได้รับการอนุมัติ และถูกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="fee9d-188">The job has been approved and activated.</span></span>                            |

<span data-ttu-id="fee9d-189">ในรายการงาน คุณสามารถกรองข้อมูลในสถานะงานนั้นได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-189">In the job list, you can filter on the job statuses.</span></span>

<span data-ttu-id="fee9d-190">การอนุมัติสามารถถูกส่งให้กับผู้ใช้ Microsoft Azure Active Directory (Azure AD) ใดๆ ในบริษัทได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-190">Approvals can be sent to any Microsoft Azure Active Directory (Azure AD) user in the company.</span></span> <span data-ttu-id="fee9d-191">การอนุมัติถูกส่งพร้อมกันสำหรับทุกคนที่มีชื่อเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="fee9d-191">The approvals are sent in parallel to all the people who are listed as approvers.</span></span> <span data-ttu-id="fee9d-192">หลังจากที่มีการอนุมัติงาน จะสามารถเรียกใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-192">After a job is approved, it can be activated.</span></span>

<span data-ttu-id="fee9d-193">บุคคลที่มีรายชื่อเป็นผู้อนุมัติ จะได้รับการแจ้งเตือนใน Attract ให้ทราบว่า พวกเขามีรายการที่จะอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="fee9d-193">The people who are listed as approvers will receive a notification in Attract to inform them that they have an item to approve.</span></span> <span data-ttu-id="fee9d-194">นอกจากนี้ รายการอนุมัติจะปรากฏในส่วน **มอบหมายให้กับคุณ** ในแดชบอร์ดด้วย</span><span class="sxs-lookup"><span data-stu-id="fee9d-194">An approval item will also appear in the **Assigned to you** section on the dashboard.</span></span> <span data-ttu-id="fee9d-195">หลังจากที่มีคนยอมรับ หรืออนุมัติงาน ทีมงานว่าจ้างจะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="fee9d-195">After someone accepts or approves a job, the hiring team will receive a notification.</span></span> <span data-ttu-id="fee9d-196">ในตอนท้าย ทีมงานว่าจ้างจะได้รับการแจ้งเตือน เมื่อมีการอนุมัติงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-196">Finally, the hiring team will receive a notification when the job is approved.</span></span>

## <a name="create-a-job"></a><span data-ttu-id="fee9d-197">สร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-197">Create a job</span></span>

<span data-ttu-id="fee9d-198">ทำตามขั้นตอนเหล่านี้เพื่อสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-198">Follow these steps to create a job.</span></span>

1. <span data-ttu-id="fee9d-199">ไปที่ **งาน**</span><span class="sxs-lookup"><span data-stu-id="fee9d-199">Go to **Jobs**.</span></span>
2. <span data-ttu-id="fee9d-200">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="fee9d-200">Select **New**.</span></span>
3. <span data-ttu-id="fee9d-201">ในฟิลด์ **ตำแหน่งงาน** ป้อนตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-201">In the **Job title** field, enter the job title.</span></span> <span data-ttu-id="fee9d-202">ในฟิลด์ **บทบาท** ป้อนบทบาทของคุณ</span><span class="sxs-lookup"><span data-stu-id="fee9d-202">In the **Role** field, enter your role.</span></span>
4. <span data-ttu-id="fee9d-203">ในฟิลด์ **เท็มเพลต** ให้เลือกเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fee9d-203">In the **Template** field, select a template.</span></span> <span data-ttu-id="fee9d-204">หรือเลือก **ข้าม**</span><span class="sxs-lookup"><span data-stu-id="fee9d-204">Alternatively, select **Skip**.</span></span> <span data-ttu-id="fee9d-205">ถ้าคุณเลือก **ข้าม** จะมีการใช้เท็มเพลตที่ถูกทำเครื่องหมายเป็นเท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fee9d-205">If you select **Skip**, the template that is marked as the default template is used.</span></span>

    <span data-ttu-id="fee9d-206">ถ้าเอกสารควรผ่านกระบวนการการอนุมัติ เลือกเท็มเพลตที่ซึ่งฟิลด์ **กระบวนการอนุมัติ** ถูกกำหนดเป็น **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="fee9d-206">If the document should go through an approval process, select a template where the **Approval process** field is set to **Default**.</span></span>

5. <span data-ttu-id="fee9d-207">บนแท็บ **รายละเอียด** ป้อนรายละเอียดของงาน</span><span class="sxs-lookup"><span data-stu-id="fee9d-207">On the **Details** tab, enter the details of the job.</span></span> <span data-ttu-id="fee9d-208">ต้องมีฟิลด์ **ชื่อตำแหน่ง** **คำอธิบายงาน** และ **สถานที่**</span><span class="sxs-lookup"><span data-stu-id="fee9d-208">The **Title**, **Job description**, and **Location** fields are required.</span></span>
6. <span data-ttu-id="fee9d-209">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fee9d-209">Select **Save**.</span></span>
7. <span data-ttu-id="fee9d-210">บนแท็บ **ทีมการว่าจ้าง** เพิ่มผู้จัดการว่าจ้าง ผู้สรรหา หรือผู้สัมภาษณ์</span><span class="sxs-lookup"><span data-stu-id="fee9d-210">On the **Hiring team** tab, add a hiring manager, recruiter, or interviewer.</span></span>
8. <span data-ttu-id="fee9d-211">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fee9d-211">Select **Save**.</span></span>
9. <span data-ttu-id="fee9d-212">บนแท็บ **กระบวนการ** เพิ่ม หรือลบขั้น ตามที่คุณต้องการ:</span><span class="sxs-lookup"><span data-stu-id="fee9d-212">On the **Process** tab, add or remove stages as you require:</span></span>

    - <span data-ttu-id="fee9d-213">ในการเพิ่มขั้น เลือก **+ ขั้นใหม่**</span><span class="sxs-lookup"><span data-stu-id="fee9d-213">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="fee9d-214">ในการลบขั้น โฮเวอร์ตัวชี้เหนือขั้นเพื่อลบ แล้วเลือกปุ่มถังขยะที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="fee9d-214">To remove a stage, hover the pointer over the stage to remove, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fee9d-215">ไม่สามารถลบขั้นผู้ที่มีแนวโน้มจะเป็นลูกค้า แอพลิเคชัน และข้อเสนอได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-215">The Prospect, Application, and Offer stages can't be removed.</span></span>

10. <span data-ttu-id="fee9d-216">เพิ่ม หรือลบกิจกรรม ตามที่คุณต้องการ:</span><span class="sxs-lookup"><span data-stu-id="fee9d-216">Add or remove activities as you require:</span></span>

    - <span data-ttu-id="fee9d-217">ในการเพิ่มกิจกรรม ลากจากรายชื่อทางขวาไปยังขั้นที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="fee9d-217">To add an activity, drag it from the list on the right to the appropriate stage.</span></span> <span data-ttu-id="fee9d-218">อีกทางหนึ่งคือ ดับเบิลคลิกที่กิจกรรม และจากนั้น เลือกระยะที่จะเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="fee9d-218">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="fee9d-219">ในการลบกิจกรรม ขยายกิจกรรม และจากนั้นเลือกปุ่มถังขยะบนหัวข้อกิจกรรมนั้น</span><span class="sxs-lookup"><span data-stu-id="fee9d-219">To remove an activity, expand the activity, and then select the trash can button on the activity header.</span></span>

11. <span data-ttu-id="fee9d-220">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fee9d-220">Select **Save**.</span></span>
12. <span data-ttu-id="fee9d-221">ถ้าคุณเลือกที่จะใช้กระบวนการอนุมัติ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="fee9d-221">If you selected to use an approval process, follow these steps:</span></span>

    1. <span data-ttu-id="fee9d-222">เลือก **+ เพิ่มผู้อนุมัติ** แล้วป้อนผู้ใช้ที่มีบัญชี Azure AD</span><span class="sxs-lookup"><span data-stu-id="fee9d-222">Select **+ Add approver**, and then enter a user who has an Azure AD account.</span></span> <span data-ttu-id="fee9d-223">คุณสามารถเพิ่มผู้อนุมัติหลายคนได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-223">You can add multiple approvers.</span></span>
    2. <span data-ttu-id="fee9d-224">เลือก **ส่งไปยังผู้อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="fee9d-224">Select **Send to approvers**.</span></span>

    <span data-ttu-id="fee9d-225">ฟิลด์ **สถานะงาน** ของงาน ถูกกำหนดเป็น **ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="fee9d-225">The **Job status** field of the job is set to **Pending**.</span></span> <span data-ttu-id="fee9d-226">หลังจากค่าของฟิลด์ **สถานะงาน** เปลี่ยนเป็น **อนุมัติ** สามารถเรียกใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="fee9d-226">After the value of the **Job status** field changes to **Approved**, the job can be activated.</span></span>

13. <span data-ttu-id="fee9d-227">เมื่อต้องการเรียกใช้งาน ให้เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="fee9d-227">To activate the job, select **Activate**.</span></span>
14. <span data-ttu-id="fee9d-228">เมื่อต้องการลงรายการบัญชีงาน ไปที่ **การลงรายการบัญชี** แล้วเลือก **ลงรายการบัญชีตอนนี้** ภายใต้ไซต์ Talent Careers หรือ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="fee9d-228">To post the job, go to **Postings**, and then select **Post Now** under the Talent Careers site or LinkedIn.</span></span>

