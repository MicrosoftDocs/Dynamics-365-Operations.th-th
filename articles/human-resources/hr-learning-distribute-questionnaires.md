---
title: แจกจ่ายและจัดกำหนดการแบบสอบถาม
description: บทความนี้อธิบายวิธีกระจายแบบสอบถามที่คุณออกแบบ เพื่อให้สามารถใช้งานกับบุคคลหรือกลุ่มของบุคคลที่จะตอบ
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0329b80615eed6efcc22bb0b140970988f5c306a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429531"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="10c94-103">แจกจ่ายและจัดกำหนดการแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-103">Distribute and schedule questionnaires</span></span>

<span data-ttu-id="10c94-104">บทความนี้อธิบายวิธีกระจายแบบสอบถามที่คุณออกแบบ เพื่อให้สามารถใช้งานกับบุคคลหรือกลุ่มของบุคคลที่จะตอบ</span><span class="sxs-lookup"><span data-stu-id="10c94-104">This article explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="10c94-105">มีหลายวิธีการในการกระจายแบบสอบถาม:</span><span class="sxs-lookup"><span data-stu-id="10c94-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="10c94-106">กำหนดให้แบบสอบถามเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="10c94-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="10c94-107">แบบสอบถามจะพร้อมใช้งานสำหรับพนักงานทั้งหมด ยกเว้นว่ามีการตั้งค่ากลุ่มแบบสอบถามเป็นจำกัดการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="10c94-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="10c94-108">กำหนดสิทธิ์ให้แก่กลุ่มแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="10c94-109">จากนั้น แบบสอบถามจะพร้อมใช้งานสำหรับสมาชิกทั้งหมดของกลุ่มที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10c94-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="10c94-110">สร้างรอบเวลาคำตอบที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="10c94-110">Create planned answer sessions.</span></span> <span data-ttu-id="10c94-111">แบบสอบถามจะพร้อมใช้งานเฉพาะสำหรับบุคคลที่ระบุเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="10c94-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="10c94-112">สร้างกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="10c94-112">Create a schedule.</span></span> <span data-ttu-id="10c94-113">แบบสอบถามสามารถใช้ได้กับหลายบุคคล</span><span class="sxs-lookup"><span data-stu-id="10c94-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="10c94-114">กำหนดให้แบบสอบถามเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="10c94-114">Marking a questionnaire as active</span></span>

<span data-ttu-id="10c94-115">โดยการตั้งค่า **ใช้งานอยู่** ให้เป็น **ใช่** ในหน้า **แบบสอบถาม** คุณสามารถทำให้แบบสอบถามพร้อมใช้งานสำหรับให้พนักงานทั้งหมดตอบได้</span><span class="sxs-lookup"><span data-stu-id="10c94-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="10c94-116">ผู้ตอบสามารถกรอกแบบสอบถามหลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="10c94-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="10c94-117">ฟังก์ชันนี้มีประโยชน์ถ้าคุณต้องการรวบรวมความคิดเห็นติดต่อกันตลอดปี</span><span class="sxs-lookup"><span data-stu-id="10c94-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="10c94-118">ตัวอย่างเช่น คุณสามารถทำแบบสอบถามที่ให้พนักงานแสดงความคิดเห็นเกี่ยวกับบริการอาหารกลางวันในโรงอาหารได้</span><span class="sxs-lookup"><span data-stu-id="10c94-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="10c94-119">กลุ่มแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-119">Questionnaire groups</span></span>

<span data-ttu-id="10c94-120">คุณสามารถตั้งค่ากลุ่มแบบสอบถาม และรวบรวมผู้ตอบที่ควรจะกระจายแบบสอบถามไปให้</span><span class="sxs-lookup"><span data-stu-id="10c94-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="10c94-121">คุณสามารถสร้างกลุ่มแบบสอบถามจากหน้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="10c94-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="10c94-122">**กลุ่มแบบสอบถาม** – บุคคลเดียวในกลุ่มแบบสอบถามเท่านั้นที่สามารถกรอกแบบสอบถามที่เลือกไว้ได้</span><span class="sxs-lookup"><span data-stu-id="10c94-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="10c94-123">ตัวอย่างเช่น ผู้ชมเป้าหมายของคุณคือผู้รับเหมา คุณจึงสร้างกลุ่มแบบสอบถามที่เจาะจงผู้ตอบเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="10c94-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="10c94-124">**สมาชิกของกลุ่มแบบสอบถาม** – คุณสามารถเพิ่มบุคคลเข้าในกลุ่มแบบสอบถามได้</span><span class="sxs-lookup"><span data-stu-id="10c94-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="10c94-125">การกำหนดกลุ่มแบบสอบถามไปยังแบบสอบถาม ในหน้า **แบบสอบถาม** คลิก **สิทธิ์ของผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="10c94-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="10c94-126">หลังจากบันทึกแบบสอบถามเป็นใช้งานอยู่ สมาชิกของกลุ่มแบบสอบถามสามารถกรอกแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="10c94-127">ฟังก์ชันนี้มีประโยชน์ ถ้าคุณต้องการทดสอบแบบสอบถามบนกลุ่มบุคคลที่เลือกก่อนที่คุณจะนำออกไปใช้กับกลุ่มใหญ่ หรือถ้าคุณต้องการระบุเป้าหมายที่เป็นผู้ชมเฉพาะเจาะจงให้แก่แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="10c94-128">รอบเวลาคำตอบที่วางแผนไว้สำหรับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-128">Planned answer sessions in a questionnaire</span></span>

<span data-ttu-id="10c94-129">รอบเวลาคำตอบที่วางแผนไว้เป็นแบบสอบถามที่คุณการออกแบบและเลือกผู้ตอบไว้</span><span class="sxs-lookup"><span data-stu-id="10c94-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> [!NOTE]
> <span data-ttu-id="10c94-130">ก่อนที่คุณจะสามารถตั้งค่ารอบเวลาคำตอบที่วางแผนไว้ คุณจะต้องออกแบบแบบสอบถามเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="10c94-130">Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="10c94-131">ในหน้า **รอบเวลาคำตอบที่วางแผนไว้** คุณสามารถสร้างรอบเวลาคำตอบที่วางแผนไว้สำหรับพนักงานแต่ละคนได้</span><span class="sxs-lookup"><span data-stu-id="10c94-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="10c94-132">รายการในหน้าแสดงแบบสอบถามที่วางแผนไว้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="10c94-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="10c94-133">รอบเวลาคำตอบที่วางแผนไว้ยังใช้ในหน้า **กำหนดการแบบสอบถาม** ซึ่งคุณสามารถวางแผนแบบสอบถามสำหรับบุคคลต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="10c94-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="10c94-134">พนักงาน</span><span class="sxs-lookup"><span data-stu-id="10c94-134">Employees</span></span>
-   <span data-ttu-id="10c94-135">ผู้เข้าร่วมหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="10c94-135">Course participants</span></span>
-   <span data-ttu-id="10c94-136">หน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="10c94-136">Organizational units</span></span>

<span data-ttu-id="10c94-137">แต่ละบุคคลสามารถตอบแบบสอบถามเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="10c94-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="10c94-138">การจัดกำหนดการแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-138">Scheduling a questionnaire</span></span>

<span data-ttu-id="10c94-139">คุณสามารถเลือกจัดกำหนดการแบบสอบถามสำหรับผู้ตอบหลายคนได้</span><span class="sxs-lookup"><span data-stu-id="10c94-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="10c94-140">ชนิดของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="10c94-140">Planning types</span></span>

<span data-ttu-id="10c94-141">ชนิดการวางแผนจะจำเป็นถ้าคุณต้องการจัดกำหนดการรอบเวลาคำตอบที่วางแผนไว้สำหรับผู้ตอบหลายคน</span><span class="sxs-lookup"><span data-stu-id="10c94-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="10c94-142">ชนิดการวางแผนจะใช้ในการจัดกำหนดการแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="10c94-143">ตัวอย่างเช่น คุณสามารถตั้งค่ากำหนดการแบบสอบถามเพื่อจุดประสงค์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="10c94-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="10c94-144">การประเมิน</span><span class="sxs-lookup"><span data-stu-id="10c94-144">Evaluation</span></span>
-   <span data-ttu-id="10c94-145">การสำรวจความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="10c94-145">Survey</span></span>
-   <span data-ttu-id="10c94-146">การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="10c94-146">Testing</span></span>

<span data-ttu-id="10c94-147">คุณสามารถระบุชนิดการวางแผนสำหรับกำหนดการแบบสอบถามในหน้า **กำหนดการแบบสอบถาม** ได้</span><span class="sxs-lookup"><span data-stu-id="10c94-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="10c94-148">ชนิดการอ้างอิงสำหรับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-148">Reference types for questionnaire</span></span>

<span data-ttu-id="10c94-149">คุณสามารถใช้ชนิดข้อมูลอ้างอิงเพื่อป้อนเกณฑ์สำหรับผู้ตอบที่คุณอาจเลือกเมื่อคุณจัดกำหนดการแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="10c94-150">ใช้หน้า **ชนิดการอ้างอิง** เพื่อตั้งค่าชนิดการอ้างอิงสำหรับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="10c94-151">ชนิดการอ้างอิงแต่ละชนิดสอดคล้องกับตารางใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="10c94-151">Each reference type corresponds to a table in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="10c94-152">เมื่อคุณสร้างกำหนดการแบบสอบถาม คุณสามารถระบุแต่ละเรกคอร์ดในตารางหรือช่วงของเรกคอร์ดที่จะเกี่ยวข้องกับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="10c94-153">ตัวอย่างเช่น ถ้าคุณเลือกตารางหลักสูตร คุณสามารถเลือกว่าหลักสูตรใดที่แบบสอบถามจะระบุให้ใช้</span><span class="sxs-lookup"><span data-stu-id="10c94-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="10c94-154">เมื่อคุณตั้งค่าการอ้างอิงสำหรับตารางหลักสูตร บางฟิลด์และปุ่มบนหน้า **หลักสูตร** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="10c94-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="10c94-155">กำหนดการแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-155">Questionnaire schedules</span></span>

<span data-ttu-id="10c94-156">คุณสามารถใช้กำหนดการแบบสอบถามเพื่อสร้างรอบเวลาคำตอบที่วางแผนไว้หลายรายการสำหรับกลุ่มผู้ใช้ ขึ้นอยู่กับชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="10c94-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="10c94-157">สร้างการจัดกำหนดการบนหน้า **กำหนดการแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="10c94-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="10c94-158">เลือกชนิดการวางแผนเพื่อกำหนดการจัดประเภท และเลือกชนิดการอ้างอิงที่ควรใช้การสอบถามระบบสำหรับผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="10c94-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="10c94-159">ตัวอย่างเช่น ถ้าคุณตั้งค่าชนิดการอ้างอิงไปยังตารางหลักสูตร คุณสามารถเลือกหลักสูตรเฉพาะในฟิลด์ **อ้างอิง** ได้</span><span class="sxs-lookup"><span data-stu-id="10c94-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="10c94-160">คลิก **ตั้งค่ารายละเอียด** เพื่อเลือกแบบสอบถามและเงื่อนไขอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="10c94-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="10c94-161">ตัวอย่างเช่น ระบุชื่อผู้สอนเป็นเงื่อนไขถ้าแบบสอบถามคือการประเมินผู้สอน</span><span class="sxs-lookup"><span data-stu-id="10c94-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="10c94-162">หลังจากที่คุณป้อนรายละเอียดการตั้งค่าเสร็จเรียบร้อยแล้ว ระบบจะสร้างรอบเวลาคำตอบที่วางแผนไว้สำหรับผู้ใช้ที่รวมอยู่ในการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="10c94-163">คลิก **รอบเวลาคำตอบที่วางแผนไว้** เพื่อดูรอบเวลาคำตอบสำหรับกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="10c94-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="10c94-164">คุณสามารถสร้างรอบเวลาคำตอบที่วางแผนไว้เพิ่มเติมด้วยตนเอง หรือลบรอบเวลาคำตอบที่วางแผนไว้ซึ่งยังไม่ได้ตอบได้</span><span class="sxs-lookup"><span data-stu-id="10c94-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="10c94-165">คลิก **ฟังก์ชัน** &gt; **เริ่มต้น** เพื่อสร้างแบบสอบถามพร้อมใช้งานสำหรับผู้ใช้ในรอบเวลาคำตอบที่วางแผนไว้ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="10c94-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="10c94-166">คลิก **คำตอบ** เพื่อดูคำตอบที่เสร็จสมบูรณ์แล้วของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="10c94-167">คุณสามารถเลือกที่จะคัดลอกการตั้งค่ากำหนดการแบบสอบถาม รอบเวลาคำตอบที่วางแผนไว้ และคำตอบ ไปยังแบบสอบถามที่ตั้งกำหนดการใหม่</span><span class="sxs-lookup"><span data-stu-id="10c94-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="10c94-168">การแจ้งผู้ตอบเกี่ยวกับแบบสอบถามที่พร้อมใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="10c94-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="10c94-169">เมื่อคุณแจกจ่ายแบบสอบถาม คุณจะต้องแจ้งให้ผู้ตอบว่าแบบสอบถามพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="10c94-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="10c94-170">การแจ้งผู้ตอบแบบสอบถามเกี่ยวกับรอบเวลาคำตอบที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="10c94-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="10c94-171">ถ้าคุณใช้รอบเวลาคำตอบที่วางแผนไว้ คุณต้องแจ้งบุคคลนั้นโดยตรง เช่น ทางโทรศัพท์ หรืออีเมล</span><span class="sxs-lookup"><span data-stu-id="10c94-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="10c94-172">การแจ้งผู้ตอบแบบสอบถามเกี่ยวกับการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="10c94-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="10c94-173">ใช้หน้า **กำหนดการแบบสอบถาม** เพื่อจัดเตรียมและส่งอีเมลไปยังผู้ตอบทั้งหมดที่กำหนดให้ตอบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="10c94-174">ป้อนข้อความอีเมลบนแท็บ **อีเมลสำหรับการบริการตนเองของพนักงาน** หลังจากกำหนดการเริ่มต้นแล้ว คลิก **ฟังก์ชัน** &gt; **ส่งอีเมล** เพื่อสร้างและส่งอีเมลไปยังผู้ตอบ</span><span class="sxs-lookup"><span data-stu-id="10c94-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="10c94-175">ผู้ตอบสามารถลงชื่อเข้าใช้งานในเว็บไซต์ และกรอกแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="10c94-176">ก่อนที่คุณจะใช้ฟังก์ชันอีเมลได้ ผู้ดูแลระบบไอทีของคุณต้องป้อนการตั้งค่าอีเมลในหน้า **พารามิเตอร์อีเมล์** ก่อน</span><span class="sxs-lookup"><span data-stu-id="10c94-176">Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="10c94-177">การสิ้นสุดแบบสอบถามที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="10c94-177">Ending a scheduled questionnaire</span></span>

<span data-ttu-id="10c94-178">คุณสามารถสิ้นสุดแบบสอบถามที่จัดกำหนดการไว้ หลังจากที่ผู้ตอบทั้งหมดเสร็จสิ้นการตอบแบบสอบถามตามรอบเวลาที่กำหนดของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="10c94-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="10c94-179">หลังจากแบบสอบถามที่จัดกำหนดการไว้สิ้นสุดลง คุณไม่สามารถคัดลอกการตั้งค่าไปยังการจัดกำหนดการใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="10c94-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> [!NOTE]
>   <span data-ttu-id="10c94-180">หมายเหต ถ้าผู้ตอบหนึ่งคนขึ้นไปยังไม่ได้กรอกข้อมูลแบบสอบถาม แต่คุณยังคงต้องการสิ้นสุดการจัดกำหนดการ คุณจะต้องลบผู้ตอบที่เกี่ยวข้องออกจากรายการในหน้า **รอบเวลาของคำตอบที่วางแผนไว้** ก่อน</span><span class="sxs-lookup"><span data-stu-id="10c94-180">If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="10c94-181">จากนั้นคุณจึงสามารถจบกำหนดการได้</span><span class="sxs-lookup"><span data-stu-id="10c94-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="10c94-182">การกรอกแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="10c94-182">Completing questionnaires</span></span>

<span data-ttu-id="10c94-183">หลังจากที่คุณได้รับการออกแบบและแจกจ่ายแบบสอบถาม สามารถกรอกแบบสอบถามโดยผู้ตอบที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="10c94-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="10c94-184">คุณสามารถกรอกแบบสอบถามที่พร้อมใช้งานสำหรับคุณให้สมบูรณ์ได้จากสองตำแหน่งดังนี้</span><span class="sxs-lookup"><span data-stu-id="10c94-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="10c94-185">ในบานหน้าต่างนำทาง คลิก **แบบสอบถาม** &gt; **กระจาย** &gt; **ตอบแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="10c94-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="10c94-186">ในระบบบริการตนเองของพนักงาน คลิก **แบบสอบถามที่ต้องตอบ**</span><span class="sxs-lookup"><span data-stu-id="10c94-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="10c94-187">สามารถทำแบบสอบถามให้พร้อมใช้งานเฉพาะผู้ใช้หรือกลุ่มผู้ใช้ หรือผู้ใช้ทุกคนในเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="10c94-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>


