---
title: กระจายแบบสอบถามโดยใช้การจัดกำหนดการ
description: 'การจัดกำหนดการแบบสอบถามอนุญาตให้คุณสามารถวางแผนและแจกจ่ายแบบสอบถามไปให้ผู้ตอบหลายคน '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0cd101bfe88ae1acb051ba11a676da66ef6a3db6
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115473"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="74bfd-103">กระจายแบบสอบถามโดยใช้การจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="74bfd-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="74bfd-104">การจัดกำหนดการแบบสอบถามอนุญาตให้คุณสามารถวางแผนและแจกจ่ายแบบสอบถามไปให้ผู้ตอบหลายคน </span><span class="sxs-lookup"><span data-stu-id="74bfd-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="74bfd-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="74bfd-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="74bfd-106">สร้างกำหนดการแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="74bfd-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="74bfd-107">ไปที่แบบสอบถาม > แจกจ่าย > กำหนดการของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="74bfd-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="74bfd-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="74bfd-108">Click New.</span></span>

3. <span data-ttu-id="74bfd-109">ในฟิลด์การจัดกำหนดการ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="74bfd-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="74bfd-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="74bfd-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="74bfd-111">ตั้งค่ากำหนดการเป็นแบบไม่ระบุชื่อ ถ้าการตอบสนองควรถูกบันทึกโดยไม่มีชื่อที่เชื่อมโยงกับการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="74bfd-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="74bfd-112">จะต้องตั้งค่าการอนุญาตผลลัพธ์ที่ไม่ระบุชื่อในพารามิเตอร์ทรัพยากรบุคคลก่อน</span><span class="sxs-lookup"><span data-stu-id="74bfd-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="74bfd-113">ในฟิลด์ชนิด เลือกชนิดการวางแผน </span><span class="sxs-lookup"><span data-stu-id="74bfd-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="74bfd-114">ในตัวอย่างนี้ เราจะใช้ชนิดความพึงพอใจ</span><span class="sxs-lookup"><span data-stu-id="74bfd-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="74bfd-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="74bfd-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="74bfd-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74bfd-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="74bfd-117">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="74bfd-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="74bfd-118">ขยายส่วนอีเมลสำหรับการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="74bfd-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="74bfd-119">ในฟิลด์ชื่อเรื่อง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="74bfd-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="74bfd-120">ตัวอย่าง: แบบสอบถามที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74bfd-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="74bfd-121">ในฟิลด์คำอธิบาย พิมพ์เนื้อความของข้อความอีเมล </span><span class="sxs-lookup"><span data-stu-id="74bfd-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="74bfd-122">โปรดทราบว่าสามารถใช้ตัวแปรเพื่อทดแทนค่าในระบบได้</span><span class="sxs-lookup"><span data-stu-id="74bfd-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="74bfd-123">ตัวอย่าง: เรียน %P% โปรดล็อกอินไปยังระบบบริการตนเองของพนักงานเพื่อกรอกแบบสอบถามสุขภาพของบุคลากร</span><span class="sxs-lookup"><span data-stu-id="74bfd-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="74bfd-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="74bfd-124">Contoso</span></span>  

12. <span data-ttu-id="74bfd-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="74bfd-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="74bfd-126">ใช้การตั้งค่ารายละเอียดเพื่อเลือกแบบสอบถามในการตอบ เช่นเดียวกับการสอบถามใดๆ ที่ใช้เพื่อเลือกผู้ตอบ</span><span class="sxs-lookup"><span data-stu-id="74bfd-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="74bfd-127">คลิกการตั้งค่ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="74bfd-127">Click Setup details.</span></span>

2. <span data-ttu-id="74bfd-128">ในรายการ ให้เลือกการสอบถามเพื่อใช้ในการค้นหาระบบสำหรับผู้ตอบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="74bfd-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="74bfd-129">ตัวอย่าง: ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="74bfd-129">Example: Workers</span></span>  

3. <span data-ttu-id="74bfd-130">คลิกดูหรือแก้ไขการสอบถามเพื่อเลือกบุคคลเฉพาะ หรือปรับเปลี่ยนการสอบถามเพื่อค้นหาบุคคลที่ตรงตามเกณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="74bfd-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="74bfd-131">หมายเหตุว่า ผู้ตอบทั้งหมดตัองเป็นผู้ใช้ในระบบด้วย</span><span class="sxs-lookup"><span data-stu-id="74bfd-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="74bfd-132">ในรายการนี้ ให้ทำเครื่องหมายแถวสำหรับบุคคล</span><span class="sxs-lookup"><span data-stu-id="74bfd-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="74bfd-133">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="74bfd-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="74bfd-134">เลือก Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="74bfd-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="74bfd-135">ในรายการ ให้เลือก Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="74bfd-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="74bfd-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="74bfd-136">Click OK.</span></span>

8. <span data-ttu-id="74bfd-137">คลิกแท็บแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="74bfd-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="74bfd-138">ในแผนภูมิ ขยาย 'โหนดสำหรับแบบสอบถาม พิมพ์ แบบสำรวจความพึงพอใจ'</span><span class="sxs-lookup"><span data-stu-id="74bfd-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="74bfd-139">ในแผนภูมิ ทำเครื่องหมายถูก 'การประเมินความสมบูรณ์ของบุคลากร'</span><span class="sxs-lookup"><span data-stu-id="74bfd-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="74bfd-140">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="74bfd-140">Click OK.</span></span>

12. <span data-ttu-id="74bfd-141">คลิกรอบเวลาของคำตอบที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="74bfd-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="74bfd-142">หมายเหตุว่ารอบเวลาของคำตอบที่วางแผนไว้ได้ถูกสร้างขึ้นสำหรับแต่ละผู้ใช้ที่เลือก/ที่สอบถาม</span><span class="sxs-lookup"><span data-stu-id="74bfd-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="74bfd-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="74bfd-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="74bfd-144">เริ่มต้นกำหนดการของแบบสอบถามเพื่อที่จะทำให้แบบสอบถามพร้อมใช้งานสำหรับผู้ตอบที่ต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="74bfd-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="74bfd-145">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="74bfd-145">Click Functions.</span></span>

2. <span data-ttu-id="74bfd-146">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="74bfd-146">Click Start.</span></span>

3. <span data-ttu-id="74bfd-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="74bfd-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="74bfd-148">ส่งอีเมลเพื่อแจ้งผู้ตอบให้ทราบถึงแบบสอบถามที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74bfd-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="74bfd-149">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="74bfd-149">Click Functions.</span></span>

2. <span data-ttu-id="74bfd-150">คลิกส่งอีเมล</span><span class="sxs-lookup"><span data-stu-id="74bfd-150">Click Send email.</span></span>

3. <span data-ttu-id="74bfd-151">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="74bfd-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="74bfd-152">ใช้รอบเวลาคำตอบที่วางแผนไว้เพื่อตรวจสอบผู้ที่ต้องดำเนินการแบบสอบถามให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="74bfd-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="74bfd-153">คลิกรอบเวลาของคำตอบที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="74bfd-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="74bfd-154">ลบรอบเวลาคำตอบที่วางแผนไว้ที่คงเหลือใดๆ เมื่อคุณพร้อมที่จะจบรอบเวลาที่กำหนดตารางไว้</span><span class="sxs-lookup"><span data-stu-id="74bfd-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="74bfd-155">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="74bfd-155">Click Delete.</span></span>

3. <span data-ttu-id="74bfd-156">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="74bfd-156">Click Yes.</span></span>

4. <span data-ttu-id="74bfd-157">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="74bfd-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="74bfd-158">สิ้นสุดกำหนดการเมื่อผู้ตอบทุกคนได้ทำแบบสอบถามเสร็จสมบูรณ์แล้ว และ/หรือรอบเวลาของคำตอบที่วางแผนไว้ถูกลบ</span><span class="sxs-lookup"><span data-stu-id="74bfd-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="74bfd-159">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="74bfd-159">Click Functions.</span></span>
2. <span data-ttu-id="74bfd-160">คลิกสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="74bfd-160">Click End.</span></span>
3. <span data-ttu-id="74bfd-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="74bfd-161">Click OK.</span></span>

