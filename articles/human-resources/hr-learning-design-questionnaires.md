---
title: ออกแบบแบบสอบถาม
description: บทความนี้อธิบายถึงกระบวนการสร้างแบบสอบถาม ขั้นตอนแรกคือการ ออกแบบแบบสอบถาม เมื่อคุณออกแบบแบบสอบถาม คุณไม่เพียงเขียนคำถามและคำตอบ แต่ยังสร้างโครงสร้างที่คำตอบที่สามารถบันทึก และจัดทำตารางคำตอบได้
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: da4250b281438c29c82150af8db9cb8cca41c6c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420827"
---
# <a name="design-questionnaires"></a><span data-ttu-id="240c6-105">ออกแบบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-105">Design questionnaires</span></span>

<span data-ttu-id="240c6-106">บทความนี้อธิบายถึงกระบวนการสร้างแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-106">This article describes the process for creating a questionnaire.</span></span> <span data-ttu-id="240c6-107">ขั้นตอนแรกคือการ ออกแบบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-107">The first step is to design the questionnaire.</span></span> <span data-ttu-id="240c6-108">เมื่อคุณออกแบบแบบสอบถาม คุณไม่เพียงเขียนคำถามและคำตอบ แต่ยังสร้างโครงสร้างที่คำตอบที่สามารถบันทึก และจัดทำตารางคำตอบได้</span><span class="sxs-lookup"><span data-stu-id="240c6-108">When you design a questionnaire, you not only write the questions and answers, but also create the structure that enables answers to be recorded and tabulated.</span></span> 

<span data-ttu-id="240c6-109">การออกแบบแบบสอบถามอย่างรอบคอบสามารถช่วยเพิ่มคุณภาพของข้อมูลที่คุณรวบรวมได้</span><span class="sxs-lookup"><span data-stu-id="240c6-109">A carefully designed questionnaire can help increase the quality of the data that you collect.</span></span> <span data-ttu-id="240c6-110">โดยการออกแบบอย่างระมัดระวัง คุณสามารถเลือกตัวเลือกที่เหมาะสมในเวลาที่เหมาะสมได้ดีขึ้นสำหรับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-110">Through careful design, you can better select the appropriate options at the appropriate time for a questionnaire.</span></span> <span data-ttu-id="240c6-111">เนื้อหาต่อไปนี้จะช่วยให้คุณวางแผนแบบสอบถามที่มีประสิทธิภาพได้:</span><span class="sxs-lookup"><span data-stu-id="240c6-111">The following points can help you plan an effective questionnaire:</span></span>

-   <span data-ttu-id="240c6-112">กำหนดวัตถุประสงค์ของแบบสอบถามให้ชัดเจน เพื่อช่วยในการรับประกันว่าคำถามสนับสนุนวัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="240c6-112">Clearly define the purpose of the questionnaire to help guarantee that the questions support the purpose.</span></span>
-   <span data-ttu-id="240c6-113">กำหนดบุคคลหรือกลุ่มบุคคลที่คุณควรกรอกข้อมูลแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-113">Determine the individual person or the group of people who should complete the questionnaire.</span></span>
-   <span data-ttu-id="240c6-114">เขียนคำถามที่จะปรากฏในแบบสอบถาม และรวมตัวเลือกคำตอบ ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="240c6-114">Write questions that will appear on the questionnaire, and include answer choices, if applicable.</span></span>
-   <span data-ttu-id="240c6-115">ตรวจสอบให้แน่ใจว่าแบบสอบถามเรียงกันตามกันทางตรรกะ เพื่อให้ยังคงเกี่ยวข้องกับผู้ตอบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-115">Be sure that the questionnaire flows logically, so that respondents remain engaged.</span></span>
-   <span data-ttu-id="240c6-116">จัดเรียงคำถามและคำตอบในลำดับที่ควรจะแสดงต่อผู้ตอบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-116">Arrange questions and answers in the order that they should be presented to respondents in.</span></span>
-   <span data-ttu-id="240c6-117">ตัดสินใจว่า ควรประเมินผลลัพธ์อย่างไร ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="240c6-117">Decide how the results should be evaluated, if applicable.</span></span>
-   <span data-ttu-id="240c6-118">ตัดสินใจว่าคุณต้องใช้ลักษณะการทำงานเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-118">Decide whether you’ll need additional features.</span></span> <span data-ttu-id="240c6-119">ตัวอย่างเช่น กำหนดว่าผลลัพธ์ควรจะจำแนกอย่างไร ขีดจำกัดเวลาจำเป็นหรือไม่ หรือว่าคำถามทั้งหมดจะบังคับตอบหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-119">For example, determine whether and how results should be categorized, whether a time limit is required, or whether all the questions will be mandatory.</span></span>

<span data-ttu-id="240c6-120">ระยะออกแบบรวมถึงงานสี่ประเภทที่คุณต้องดำเนินการตามลำดับนี้:</span><span class="sxs-lookup"><span data-stu-id="240c6-120">The design phase includes four categories of tasks that you must complete in this order:</span></span>

1.  <span data-ttu-id="240c6-121">ตั้งค่าข้อกำหนดเบื้องต้นตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="240c6-121">Set up prerequisites, as required.</span></span>
2.  <span data-ttu-id="240c6-122">ตั้งค่ากลุ่มคำตอบและคำตอบ ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="240c6-122">Set up answer groups and answers, if applicable.</span></span>
3.  <span data-ttu-id="240c6-123">สร้างคำถามและความเชื่อมโยงกับกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="240c6-123">Set up questions and their association with the answer groups.</span></span>
4.  <span data-ttu-id="240c6-124">ตั้งค่าแบบสอบถามเอง และแนบคำถามลงไป</span><span class="sxs-lookup"><span data-stu-id="240c6-124">Set up the questionnaire itself, and attach questions to it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="240c6-125">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="240c6-125">Prerequisites</span></span>
<span data-ttu-id="240c6-126">ข้อกำหนดเบื้องต้นบางอย่างต้องอยู่ในตำแหน่งก่อนที่คุณจะสามารถสร้างแบบสอบถาม คำตอบ และคำถามได้</span><span class="sxs-lookup"><span data-stu-id="240c6-126">Some prerequisites must be in place before you can create questionnaires, answers, and questions.</span></span> <span data-ttu-id="240c6-127">อย่างไรก็ตาม ข้อกำหนดเบื้องต้นทั้งหมดไม่จำเป็นต้องใช้สำหรับงานทั้งหมดโดยสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="240c6-127">However, not all prerequisites are required for full functionality.</span></span>

### <a name="required"></a><span data-ttu-id="240c6-128">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="240c6-128">Required</span></span>

| <span data-ttu-id="240c6-129">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="240c6-129">Prerequisite</span></span>        | <span data-ttu-id="240c6-130">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="240c6-130">Description</span></span>                |
|---------------------|----------------------------|
| <span data-ttu-id="240c6-131">ชนิดของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-131">Questionnaire types</span></span> | <span data-ttu-id="240c6-132">จัดประเภทแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-132">Categorize questionnaires.</span></span> |
| <span data-ttu-id="240c6-133">ชนิดของคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-133">Question types</span></span>      | <span data-ttu-id="240c6-134">จัดประเภทแบบคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-134">Categorize questions.</span></span>      |

### <a name="optional"></a><span data-ttu-id="240c6-135">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="240c6-135">Optional</span></span>

| <span data-ttu-id="240c6-136">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="240c6-136">Prerequisite</span></span>             | <span data-ttu-id="240c6-137">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="240c6-137">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="240c6-138">พารามิเตอร์แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-138">Questionnaire parameters</span></span> | <span data-ttu-id="240c6-139">แก้ไขการควบคุมพื้นฐานและการตั้งค่าเริ่มต้นสำหรับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-139">Modify basic controls and default settings for questionnaires.</span></span> |

### <a name="questionnaire-types"></a><span data-ttu-id="240c6-140">ชนิดของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-140">Questionnaire types</span></span>

<span data-ttu-id="240c6-141">ชนิดแบบสอบถามมีความจำเป็นและต้องกำหนดเมื่อคุณสร้างแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-141">Questionnaire types are required and must be assigned when you create a questionnaire.</span></span> <span data-ttu-id="240c6-142">ชนิดแบบสอบถามช่วยคุณจัดการและจัดประเภทแบบสอบถามได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="240c6-142">Questionnaire types help you manage and classify questionnaires more easily.</span></span> <span data-ttu-id="240c6-143">ใช้ชนิดแบบสอบถามเพื่อจัดประเภทแบบสอบถาม และแยกแยะออกจากกัน</span><span class="sxs-lookup"><span data-stu-id="240c6-143">Use questionnaire types to classify questionnaires and differentiate them from each other.</span></span> <span data-ttu-id="240c6-144">ตัวอย่างเช่น ถ้าคุณมีแบบสอบถามเป็นจำนวนมากให้เลือก คุณสามารถกรองข้อมูลแบบสอบถามโดยใช้ชนิดในแบบฟอร์มเพื่อช่วยให้สามารถค้นหาแบบสอบถามที่ระบุได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="240c6-144">For example, if you have multiple questionnaires to select from, you can filter them by type to help make it easier to find a particular questionnaire.</span></span> <span data-ttu-id="240c6-145">ต่อไปนี้เป็นตัวอย่างของชนิดแบบสอบถาม:</span><span class="sxs-lookup"><span data-stu-id="240c6-145">Here are some examples of questionnaire types:</span></span>

-   <span data-ttu-id="240c6-146">การพัฒนาทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="240c6-146">Human resource development</span></span>
-   <span data-ttu-id="240c6-147">การสำรวจลูกค้า</span><span class="sxs-lookup"><span data-stu-id="240c6-147">Customer surveys</span></span>
-   <span data-ttu-id="240c6-148">กระบวนการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="240c6-148">Review process</span></span>

### <a name="question-types"></a><span data-ttu-id="240c6-149">ชนิดของคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-149">Question types</span></span>

<span data-ttu-id="240c6-150">ชนิดคำถามมีความจำเป็นและต้องกำหนดเมื่อคุณสร้างคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-150">Question types are required and must be assigned when you create a question.</span></span> 

<span data-ttu-id="240c6-151">ใช้ชนิดคำถามเพื่อจัดประเภทคำถามสำหรับการรายงาน</span><span class="sxs-lookup"><span data-stu-id="240c6-151">Use question types to categorize questions for reporting.</span></span> <span data-ttu-id="240c6-152">ชนิดคำถามยังช่วยให้สามารถค้นหาคำถามได้ง่ายขึ้น เนื่องจากคุณสามารถใช้ชนิดเป็นตัวกรองในหน้า **คำถาม** ได้</span><span class="sxs-lookup"><span data-stu-id="240c6-152">Question types also make it easier to find questions, because you can use types as filters on the **Questions** page.</span></span> <span data-ttu-id="240c6-153">ต่อไปนี้เป็นตัวอย่างของชนิดคำถาม:</span><span class="sxs-lookup"><span data-stu-id="240c6-153">Here are some examples of question types:</span></span>

-   <span data-ttu-id="240c6-154">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="240c6-154">Human resource</span></span>
-   <span data-ttu-id="240c6-155">การบริหารธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="240c6-155">Managing business</span></span>
-   <span data-ttu-id="240c6-156">การประเมินผลหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="240c6-156">Course evaluation</span></span>

### <a name="questionnaire-parameters"></a><span data-ttu-id="240c6-157">พารามิเตอร์แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-157">Questionnaire parameters</span></span>

<span data-ttu-id="240c6-158">พารามิเตอร์แบบสอบถามนั้นไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="240c6-158">Questionnaire parameters are optional.</span></span> <span data-ttu-id="240c6-159">คุณอาจไม่ใช้ ขึ้นอยู่กับความต้องการของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="240c6-159">You might not use them, depending on your company’s requirements.</span></span> 

<span data-ttu-id="240c6-160">พารามิเตอร์แบบสอบถามกำหนดตัวตน รหัสลำดับหมายเลข และชนิดการอ้างอิงของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-160">Questionnaire parameters define the anonymity, number sequence codes, and reference types of a questionnaire.</span></span> <span data-ttu-id="240c6-161">เมื่อองค์กรกระจายแบบสอบถาม ตัวเลือกเพื่ออนุญาตให้ผู้ตอบไม่ระบุชื่ออาจต้องนำมาพิจารณา</span><span class="sxs-lookup"><span data-stu-id="240c6-161">When an organization distributes a questionnaire, the option to allow respondents to remain anonymous might be of concern.</span></span> 

<span data-ttu-id="240c6-162">รหัสลำดับหมายเลขจะใช้ในการจัดระเบียบคำถามและคำตอบ</span><span class="sxs-lookup"><span data-stu-id="240c6-162">The number sequence codes are used to organize questions and answers.</span></span> <span data-ttu-id="240c6-163">ตามรหัสลำดับหมายเลขเหล่านี้ ค่าจะกำหนดโดยอัตโนมัติให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="240c6-163">Based on these number sequence codes, values are automatically assigned to items.</span></span> 

<span data-ttu-id="240c6-164">คุณควรกำหนดพารามิเตอร์ทั้งหมดก่อนที่คุณจะเริ่มสร้างข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="240c6-164">You should define all parameters before you begin to create your data.</span></span> <span data-ttu-id="240c6-165">คุณสามารถปรับเปลี่ยนการตั้งค่าพารามิเตอร์แบบสอบถามได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="240c6-165">You can modify the questionnaire parameter settings at any time.</span></span>

## <a name="questionnaire-components"></a><span data-ttu-id="240c6-166">ส่วนประกอบของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-166">Questionnaire components</span></span>
<span data-ttu-id="240c6-167">แบบสอบถามประกอบด้วยสามองค์ประกอบหลัก: กลุ่มคำตอบที่ประกอบด้วยคำตอบสำหรับคำถามเลือกตอบหลายตัวเลือก คำถาม และแบบสอบถามเอง</span><span class="sxs-lookup"><span data-stu-id="240c6-167">Questionnaires comprise three main elements: answer groups that contain the answers for multiple choice questions, questions, and the questionnaire itself.</span></span> <span data-ttu-id="240c6-168"> คุณสามารถเลือกจัดกลุ่มคำถามในแบบสอบถามเป็นกลุ่มผลลัพธ์ได้</span><span class="sxs-lookup"><span data-stu-id="240c6-168"> You can optionally group the questions on a questionnaire into result groups.</span></span> <span data-ttu-id="240c6-169">กลุ่มผลคะแนนช่วยให้คุณสามารถจัดประเภทคำถาม และให้การวิเคราะห์เพิ่มเติมในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-169">Result groups let you categorize questions and provide further analysis on the questionnaire.</span></span> 

<span data-ttu-id="240c6-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span><span class="sxs-lookup"><span data-stu-id="240c6-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span></span>

### <a name="answer-groups-and-answers"></a><span data-ttu-id="240c6-171">กลุ่มคำตอบและคำตอบ</span><span class="sxs-lookup"><span data-stu-id="240c6-171">Answer groups and answers</span></span>

<span data-ttu-id="240c6-172">ผู้ตอบแบบสอบถามสามารถตอบคำถามได้สองวิธี ขึ้นอยู่กับลักษณะของคำถาม ดังนี้</span><span class="sxs-lookup"><span data-stu-id="240c6-172">Respondents can answer a question in two ways, depending on the subject of the question:</span></span>

-   <span data-ttu-id="240c6-173">คำถามปลายเปิดไม่จำเป็นต้องตอบรับในรูปแบบที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="240c6-173">Open-ended questions don’t require responses in a specific format.</span></span> <span data-ttu-id="240c6-174">ผู้ตอบสามารถพิมพ์คำตอบเป็นข้อความ หมายเลข วัน หรือเวลา</span><span class="sxs-lookup"><span data-stu-id="240c6-174">Respondents can type a response as text, a number, a date, or a time.</span></span> <span data-ttu-id="240c6-175">โดยปกติ คำถามเหล่านี้กำหนดให้ผู้ตอบให้ข้อมูลแบบอัตนัยในคำตอบ เช่น ความคิดเห็น การประเมินค่า หรือการประเมิน</span><span class="sxs-lookup"><span data-stu-id="240c6-175">These questions typically require that the respondents provide subjective information in their answers, such as an opinion, description, evaluation, or estimate.</span></span>
-   <span data-ttu-id="240c6-176">คำถามปลายปิดจำเป็นต้องให้ผู้ตอบเลือกคำตอบในรายการคำตอบที่ถูกต้องที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="240c6-176">Closed-ended questions require that the respondent select an answer in a list of possible correct answers.</span></span>

<span data-ttu-id="240c6-177">เพื่อสร้างรายการของคำตอบที่เป็นไปได้สำหรับคำถามปลายปิด คุณสามารถสร้างคำตอบในแบบหน้า **กลุ่มคำตอบ** ได้</span><span class="sxs-lookup"><span data-stu-id="240c6-177">To provide a list of possible answers for closed-ended questions, you can create answers on the **Answer groups** page.</span></span> 

<span data-ttu-id="240c6-178">กลุ่มคำตอบและคำตอบเป็นองค์ประกอบที่สร้างเนื้อหาหลักของข้อมูลที่สร้างคำถามขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="240c6-178">Answer groups and answers are components that make up the main body of information that questions are created from.</span></span> <span data-ttu-id="240c6-179">หลังจากที่คุณสร้างกลุ่มคำตอบ คุณสามารถเชื่อมโยงกลุ่มคำตอบกับคำถามในฟิลด์ **กลุ่มคำตอบ** ในหน้า **คำถาม** ได้</span><span class="sxs-lookup"><span data-stu-id="240c6-179">After you create an answer group, you can associate the answer group with a question in the **Answer group** field on the **Questions** page.</span></span> 

<span data-ttu-id="240c6-180">กลุ่มคำตอบหนึ่งสามารถใช้กับคำถามได้มากกว่าหนึ่งข้อบนแบบสอบถามเดียวกัน และสามารถใช้ได้กับแบบสอบถามมากกว่าหนึ่งชุด</span><span class="sxs-lookup"><span data-stu-id="240c6-180">An answer group can be used for more than one question on the same questionnaire, and can also be used on more than one questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="240c6-181">ถ้าคุณปรับเปลี่ยนข้อความคำตอบในกลุ่มคำตอบที่ได้ใช้ในแบบสอบถามที่เสร็จสมบูรณ์แล้ว จะประเมินข้อมูลได้ยาก และผลลัพธ์ของแบบสอบถามอาจไม่สามารถ ใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="240c6-181">If you modify answer text in answer groups that have already been used on completed questionnaires, data can become difficult to evaluate, and questionnaire results might no longer be valid.</span></span> <span data-ttu-id="240c6-182">ถ้าคุณต้องเปลี่ยนกลุ่มคำตอบ พิจารณาสร้างกลุ่มคำตอบใหม่แทนการเปลี่ยนแปลงกลุ่มคำตอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="240c6-182">If you must change an answer group, consider creating a new answer group instead of changing an existing one.</span></span> <span data-ttu-id="240c6-183">คุณไม่สามารถลบกลุ่มคำตอบที่แนบกับคำถามหรือคำตอบ หรือได้ตอบไปแล้วได้</span><span class="sxs-lookup"><span data-stu-id="240c6-183">You can't delete answer groups that are attached to a question or answer, or that have been answered.</span></span>

### <a name="questions"></a><span data-ttu-id="240c6-184">คำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-184">Questions</span></span>

<span data-ttu-id="240c6-185">แบบสอบถามต้องมีคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-185">A questionnaire must contain questions.</span></span> <span data-ttu-id="240c6-186">คำถามสามารถเป็นได้ทั้งแบบปลายเปิดหรือปลายปิด</span><span class="sxs-lookup"><span data-stu-id="240c6-186">Questions can be either open-ended or closed-ended.</span></span>

-   <span data-ttu-id="240c6-187">การตอบรับของคำถามแบบปลายเปิดไม่ได้ควบคุม และผู้ตอบสามารถพิมพ์คำตอบของตนได้</span><span class="sxs-lookup"><span data-stu-id="240c6-187">The responses to open-ended questions aren't controlled, and respondents can type their answers.</span></span>
-   <span data-ttu-id="240c6-188">คำถามปลายปิดต้องมีรายการตัวเลือกของคำตอบที่กำหนดไว้ล่วงหน้า และสามารถจัดโครงสร้างคำถามเพื่อให้ผู้ตอบเลือกคำตอบหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="240c6-188">Closed-ended questions require a list of predefined response options, and the questions can be structured to let a respondent select multiple responses.</span></span> <span data-ttu-id="240c6-189">คำถามควรออกแบบมาเพื่อให้ได้รับข้อมูลที่เฉพาะเจาะจงจากผู้ตอบคำถาม และต้องเชื่อมโยงกับกลุ่มคำตอบที่มีตัวเลือกคำตอบสำหรับแต่ละคำถามปลายปิด</span><span class="sxs-lookup"><span data-stu-id="240c6-189">Questions should be designed to elicit specific information from a respondent and must be linked to an answer group that provides the response options for each closed-ended question.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="240c6-190">ก่อนที่คุณจะสามารถตั้งค่าคำถามปลายปิด คุณต้องสร้างกลุ่มคำตอบและคำตอบก่อน</span><span class="sxs-lookup"><span data-stu-id="240c6-190">Before you can set up closed-ended questions, you must create answer groups and answers.</span></span>

<span data-ttu-id="240c6-191">คำถามที่สามารถจัดเรียงเป็นลำดับชั้นของคำถามแบบมีเงื่อนไข เพื่อให้คำถามรองขึ้นอยู่กับคำตอบที่ผู้ตอบเลือกสำหรับคำถามก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="240c6-191">Questions can be arranged in a conditional question hierarchy, so that secondary questions depend on the answer that the respondent selects for the previous question.</span></span> <span data-ttu-id="240c6-192">คุณสามารถเขียนคำถามก่อน และจากนั้น จัดเรียงตามลำดับชั้นของคำถามในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="240c6-192">You can write the questions first and then arrange them into a hierarchy later.</span></span>

## <a name="setting-up-questionnaires"></a><span data-ttu-id="240c6-193">การตั้งค่าชนิดแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-193">Setting up questionnaires</span></span>

> [!NOTE]
> <span data-ttu-id="240c6-194">ก่อนที่คุณจะสามารถตั้งค่าแบบสอบถาม คุณต้องตั้งค่าคำตอบ คำถาม และข้อกำหนดเบื้องต้นก่อน</span><span class="sxs-lookup"><span data-stu-id="240c6-194">Before you can set up a questionnaire, you must set up answers, questions, and prerequisites.</span></span> 

<span data-ttu-id="240c6-195">สำหรับแต่ละแบบสอบถาม คุณสามารถระบุข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="240c6-195">For each questionnaire, you can specify the following information:</span></span>

-   <span data-ttu-id="240c6-196">เวลารวมหรือขีดจำกัดเวลาสำหรับการตอบคำถามบังคับ</span><span class="sxs-lookup"><span data-stu-id="240c6-196">The total time or time limit to answer mandatory questions.</span></span>
-   <span data-ttu-id="240c6-197">คำถามทั้งหมดเป็นคำถามบังคับหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-197">Whether all questions are mandatory.</span></span>
-   <span data-ttu-id="240c6-198">คำนวณคะแนนในแบบสอบถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-198">Whether to calculate points on a questionnaire.</span></span>
-   <span data-ttu-id="240c6-199">วิธีการจัดประเภทผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="240c6-199">How to categorize results.</span></span>
-   <span data-ttu-id="240c6-200">แบบสอบถามจะพร้อมใช้งานสำหรับชุดของผู้ตอบที่จำกัดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-200">Whether the questionnaire will be available to a restricted set of respondents.</span></span>
-   <span data-ttu-id="240c6-201">ให้แสดงเท็มเพลตแบบฟอร์มเป็นพื้นหลังของแบบสอบถามแต่ละหน้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-201">Whether a form template should be displayed as a background behind each page of the questionnaire.</span></span>
-   <span data-ttu-id="240c6-202">หมายเหตุเพิ่มเติมจำเป็นในการชี้แจงวัตถุประสงค์ของแบบสอบถามสำหรับผู้ตอบหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-202">Whether additional notes are required in order to clarify the intent of the questionnaire for the respondents.</span></span>
-   <span data-ttu-id="240c6-203">คุณต้องการแสดงคำถามตามลำดับที่กำหนด หรือเลือกคำถามจากกลุ่มโดยสุ่ม</span><span class="sxs-lookup"><span data-stu-id="240c6-203">Whether to display questions in a fixed order or randomly select them from a pool.</span></span>
-   <span data-ttu-id="240c6-204">ระบุว่าจะถามคำถามหากได้รับการตอบสนองที่ระบุสำหรับคำตอบก่อนหน้านี้เท่านั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="240c6-204">Whether questions will be asked only if specific responses are given for previous answers.</span></span>

### <a name="set-up-a-questionnaire"></a><span data-ttu-id="240c6-205">ตั้งค่าแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-205">Set up a questionnaire</span></span>

<span data-ttu-id="240c6-206">หน้าหลักที่คุณใช้ในการตั้งค่าแบบสอบถามคือหน้า **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="240c6-206">The primary page that you use to set up a questionnaire is the **Questionnaires** page.</span></span> <span data-ttu-id="240c6-207">เมื่อต้องการตั้งค่าแบบสอบถาม ดำเนินการงานต่อไปนี้ให้เสร็จสมบูรณ์ตามลำดับ:</span><span class="sxs-lookup"><span data-stu-id="240c6-207">To set up a questionnaire, complete the following tasks in order:</span></span>

1.  <span data-ttu-id="240c6-208">สร้างแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-208">Create a questionnaire.</span></span>
2.  <span data-ttu-id="240c6-209">ทำตามหนึ่งในขั้นตอนเหล่านี้เพื่อแนบคำถามกับแบบสอบถาม:</span><span class="sxs-lookup"><span data-stu-id="240c6-209">Follow one of these steps to attach questions to the questionnaire:</span></span>
    -   <span data-ttu-id="240c6-210">ถ้าคุณกำลังใช้กลุ่มผลลัพธ์ คุณสามารถแนบคำถามกับแบบสอบถามโดยใช้กลุ่มผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="240c6-210">If you're using result groups, you can attach questions to a questionnaire by using result groups.</span></span> <span data-ttu-id="240c6-211">อันดับแรก ตั้งค่ากลุ่มผลคะแนนสำหรับแบบสอบถาม และเพิ่มคำถามไปยังกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-211">First set up the result groups for the questionnaire, and then add questions to the result groups.</span></span>
    -   <span data-ttu-id="240c6-212">ถ้าคุณไม่ได้กำลังใช้กลุ่มผลลัพธ์ คุณสามารถแนบคำถามกับแบบสอบถามได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="240c6-212">If you aren't using result groups, you can attach questions directly to the questionnaire.</span></span>

3.  <span data-ttu-id="240c6-213">การตั้งค่าลำดับชั้นของคำถามแบบมีเงื่อนไข หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="240c6-213">Set up a conditional question hierarchy, if it's required.</span></span>
4.  <span data-ttu-id="240c6-214">ทดสอบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-214">Test the questionnaire.</span></span>

<span data-ttu-id="240c6-215">ในหน้า **แบบสอบถาม** คลิก **ตรวจสอบ** เพื่อทดสอบว่าแบบสอบถามรวบรวมไว้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="240c6-215">On the **Questionnaires** page, click **Validate** to test whether the questionnaire is assembled correctly.</span></span> <span data-ttu-id="240c6-216">อย่างไรก็ตาม ควรกรอกแบบสอบถามให้เสร็จสมบูรณ์ และทดสอบด้วยตนเองก่อนที่จะกระจายแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-216">However, it's also a good idea to complete the questionnaire and test it yourself before you distribute it.</span></span>

### <a name="modify-a-questionnaire"></a><span data-ttu-id="240c6-217">การแก้ไขแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-217">Modify a questionnaire</span></span>

<span data-ttu-id="240c6-218">คุณสามารถดำเนินการงานต่อไปนี้ให้เสร็จสมบูรณ์ในหน้า **แบบสอบถาม** ได้:</span><span class="sxs-lookup"><span data-stu-id="240c6-218">You can complete the following tasks on the **Questionnaires** page:</span></span>

-   <span data-ttu-id="240c6-219">การแก้ไขข้อมูลในแบบสอบถาม เช่น กลุ่มผลคะแนนและคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-219">Modify information in the questionnaire, such as the result groups and questions.</span></span>
-   <span data-ttu-id="240c6-220">การลบและเพิ่มคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-220">Delete and add questions.</span></span>
-   <span data-ttu-id="240c6-221">ทำการเปลี่ยนแปลงในกลุ่มผลคะแนนและหมายเลขลำดับ</span><span class="sxs-lookup"><span data-stu-id="240c6-221">Make changes in the result groups and sequence number.</span></span> 

> [!CAUTION]
> <span data-ttu-id="240c6-222">ต้องระวังเมื่อคุณเปลี่ยนแบบสอบถามที่มีการตอบไปแล้ว </span><span class="sxs-lookup"><span data-stu-id="240c6-222">Be careful when you change questionnaires that have already been answered.</span></span> <span data-ttu-id="240c6-223">การเปลี่ยนแปลงสามารถทำให้สถิติมีความถูกต้องแม่นยำลดลงได้ ซึ่งอาจส่งผลให้พื้นฐานการประเมินไม่ดีลดความแม่นยำงของสถิติ</span><span class="sxs-lookup"><span data-stu-id="240c6-223">Changes can reduce the accuracy of statistics and therefore make them a poor basis for evaluation.</span></span> <span data-ttu-id="240c6-224">ให้ลองพิจารณาถึงการสร้างคำถามใหม่ แทนการเปลี่ยนแปลงคำถามเดิมที่มีการตอบไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="240c6-224">Consider creating a new question instead of changing a question that has already been answered.</span></span>

<span data-ttu-id="240c6-225">ในแบบสอบถาม คุณไม่สามารถลบชนิดของคำถามต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="240c6-225">In a questionnaire, you can't delete the following types of questions:</span></span>

-   <span data-ttu-id="240c6-226">คำถามที่แนบกับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-226">Questions that are attached to a questionnaire</span></span>
-   <span data-ttu-id="240c6-227">คำถามที่มีการตอบไปแล้ว และปรากฏในกล่องโต้ตอบ **คำตอบ** แล้ว</span><span class="sxs-lookup"><span data-stu-id="240c6-227">Questions that have already been answered and therefore appear in the **Answers** dialog box.</span></span>

### <a name="result-groups"></a><span data-ttu-id="240c6-228">กลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-228">Result groups</span></span>

<span data-ttu-id="240c6-229">กลุ่มผลลัพธ์จะไม่จำเป็นต้องระบุเมื่อคุณแนบคำถามกับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-229">Result groups are optional when you attach questions to a questionnaire.</span></span> 

<span data-ttu-id="240c6-230">กลุ่มผลคะแนนจะใช้ในการคำนวณคะแนน และจัดประเภทผลลัพธ์ของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-230">A result group is used to calculate points and categorize the results of a questionnaire.</span></span> <span data-ttu-id="240c6-231">ถ้าคุณใช้กลุ่มผลคะแนน คุณสามารถดำเนินการงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="240c6-231">If you use result groups, you can perform the following tasks:</span></span>

-   <span data-ttu-id="240c6-232">ประเมินผลลัพธ์แบบสอบถาม โดยใช้สถิติคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-232">Evaluate questionnaire results, based on point statistics.</span></span>
-   <span data-ttu-id="240c6-233">ประเมินของคะแนนของผู้ตอบแบบสอบถามสำหรับกลุ่มผลคะแนนแต่ละกลุ่มที่คุณตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="240c6-233">Evaluate a respondent’s score for each result group that you set up.</span></span>
-   <span data-ttu-id="240c6-234">สร้างสถิติสำหรับกลุ่มผลคะแนนแต่ละกลุ่ม เพื่อช่วยคุณในการวิเคราะห์ผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-234">Generate statistics for each result group to help you analyze results.</span></span>
-   <span data-ttu-id="240c6-235">พิมพ์รายงานที่แสดงผลลัพธ์สำหรับแต่ละกลุ่มผลคะแนน และคะแนน/ข้อความที่ไม่จำเป็นต้องระบุ ซึ่งจะเป็นไปตามคะแนนที่ทำได้ในแต่ละกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-235">Print a report that shows results for each result group, and also optional points/texts that are based on points that are earned in each result group.</span></span>

> [!NOTE]
> <span data-ttu-id="240c6-236">ก่อนที่คุณจะสามารถตั้งค่าบัญชีเจ้าหนี้ คุณต้องดำเนินขั้นตอนต่อไปนี้ให้ครบถ้วน:</span><span class="sxs-lookup"><span data-stu-id="240c6-236">Before you can set up result groups, you must complete the following tasks:</span></span>

-   <span data-ttu-id="240c6-237">ตั้งค่าคำถามปลายปิด</span><span class="sxs-lookup"><span data-stu-id="240c6-237">Set up closed-ended questions.</span></span> <span data-ttu-id="240c6-238">สำหรับคำถามปลายปิด ชนิดของข้อมูลป้อนเข้าในหน้า **คำถาม** ต้องเป็น **กล่องกาเครื่องหมาย** **ปุ่มทางเลือก** หรือ **กล่องคำสั่งผสม**</span><span class="sxs-lookup"><span data-stu-id="240c6-238">For a closed-ended question, the input type on the **Questions** page must be **Check box**, **Alternative button**, or **Combo box**.</span></span>
-   <span data-ttu-id="240c6-239">กำหนดคะแนนสำหรับคำตอบในกลุ่มคำตอบที่กำหนดให้กับแต่ละคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-239">Define points for answers in the answer groups that are assigned to each question.</span></span>
-   <span data-ttu-id="240c6-240">ตั้งค่าแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-240">Set up a questionnaire.</span></span>

<span data-ttu-id="240c6-241">เมื่อต้องการแนบคำถามกับแบบสอบถามโดยใช้กลุ่มผลคะแนน ให้ตั้งค่ากลุ่มผลคะแนนสำหรับแบบสอบถาม แล้วจึงเพิ่มคำถามให้กับกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-241">To attach questions to a questionnaire by using result groups, first set up the result groups for the questionnaire, and then add questions to the result groups.</span></span> <span data-ttu-id="240c6-242">ถ้าคุณไม่ใช้กลุ่มผลลัพธ์ คุณสามารถแนบคำถามกับแบบสอบถามได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="240c6-242">If you don't use result groups, you can attach questions directly to a questionnaire.</span></span> 

<span data-ttu-id="240c6-243">คุณสามารถตั้งค่ากลุ่มผลลัพธ์หลายกลุ่ม เพื่อประเมินคะแนนที่ผู้ตอบแบบสอบถามได้รับคะแนนในแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="240c6-243">You can set up multiple result groups to evaluate the points that a respondent earns in each category.</span></span> <span data-ttu-id="240c6-244">หลังจากแบบสอบถามเสร็จสมบูรณ์ คุณสามารถดูคะแนนที่ทำได้ของแต่ละกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-244">After a questionnaire is completed, you can view the points that have been achieved for each result group.</span></span> 

> [!TIP]
> <span data-ttu-id="240c6-245">เมื่อต้องการประเมินแบบสอบถามโดย ใช้คะแนน แต่ไม่ได้แยกประเภท คุณสามารถเพิ่มคำถามทั้งหมดให้กับกลุ่มผลคะแนนเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="240c6-245">To evaluate a questionnaire by using points but not separate categories, you can add all questions to a single result group.</span></span> 

<span data-ttu-id="240c6-246">สำหรับแต่ละกลุ่มผลคะแนน คุณสามารถตั้งค่าข้อความที่ผู้ตอบได้รับหลังจากที่สมบูรณ์แบบสอบถามตามคะแนนที่ทำได้</span><span class="sxs-lookup"><span data-stu-id="240c6-246">For each result group, you can also set up one or more point-based messages that respondents receive after they complete a questionnaire.</span></span> <span data-ttu-id="240c6-247">ข้อความที่แสดงอาจแตกต่างกัน ขึ้นอยู่กับคะแนนที่ผู้ตอบได้รับในกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-247">The text that is shown can vary, depending on the score that a respondent achieves in a result group.</span></span> <span data-ttu-id="240c6-248">การใช้ข้อความตามผลคะแนน คุณต้องกำหนดช่วงคะแนนและคำอธิบายของแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="240c6-248">To use point-based messages, you must define point intervals and a description of each interval.</span></span> <span data-ttu-id="240c6-249">เมื่อผู้ตอบได้รับคะแนนในช่วงคะแนนที่ระบุ ข้อความเฉพาะสำหรับช่วงคะแนนดังกล่าวจะรวมอยู่ในรายงานผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="240c6-249">When a respondent achieves a score in a specific interval, the text for that interval is included on the results report.</span></span> 

<span data-ttu-id="240c6-250">เนื่องจากกลุ่มผลคะแนนเกี่ยวข้องกับคะแนนที่เชื่อมโยงกับชุดของคำถามที่เจาะจงในแบบสอบถาม คุณสามารถใช้กลุ่มผลคะแนนที่เฉพาะเจาะจงกลุ่มเดียวเท่านั้นสำหรับหนึ่งแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-250">Because a result group is related to the points that are associated with specific sets of questions on a questionnaire, you can use only a specific result group for a questionnaire.</span></span>

#### <a name="example-pointstexts-for-result-group-3"></a><span data-ttu-id="240c6-251">ตัวอย่าง: คะแนน/ข้อความสำหรับกลุ่มผลคะแนน 3</span><span class="sxs-lookup"><span data-stu-id="240c6-251">Example: Points/texts for result group 3</span></span>

<span data-ttu-id="240c6-252">คุณกำลังใช้แบบสอบถามสำหรับการทดสอบความเป็นผู้นำ ซึ่งมี 15 คำถามในสามประเภท</span><span class="sxs-lookup"><span data-stu-id="240c6-252">You're using a questionnaire for a leadership test that has 15 questions in three categories.</span></span> <span data-ttu-id="240c6-253">คุณสร้างกลุ่มผลคะแนนสามกลุ่ม และเพิ่มคำถามห้าคำถามไปยังแต่ละกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-253">You create three result groups and add five questions to each result group.</span></span> <span data-ttu-id="240c6-254">จากนั้น รวมคะแนนในสามกลุ่มดังนี้</span><span class="sxs-lookup"><span data-stu-id="240c6-254">Points are then totaled in the three groups.</span></span> <span data-ttu-id="240c6-255">กลุ่มผลคะแนนสามกลุ่มมีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="240c6-255">The three result groups are as follows:</span></span>

-   <span data-ttu-id="240c6-256">ความสามารถด้านความคิดสร้างสรรค์</span><span class="sxs-lookup"><span data-stu-id="240c6-256">Creative abilities</span></span>
-   <span data-ttu-id="240c6-257">ความสามารถด้านความเป็นผู้นำ</span><span class="sxs-lookup"><span data-stu-id="240c6-257">Leadership abilities</span></span>
-   <span data-ttu-id="240c6-258">ความสามารถด้านเทคนิค</span><span class="sxs-lookup"><span data-stu-id="240c6-258">Technical abilities</span></span>

<span data-ttu-id="240c6-259">เมื่อต้องการใช้ข้อความตามผลคะแนน ให้ตั้งค่าช่วงข้อความสำหรับกลุ่มผลคะแนนแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="240c6-259">To use point-based messages, you set up text intervals for each result group.</span></span> <span data-ttu-id="240c6-260">แต่ละคำถามจะได้รับสองคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-260">Each question is assigned two points.</span></span> <span data-ttu-id="240c6-261">ดังนั้น รวมคะแนนสูงสุดในแต่ละกลุ่มผลลัพธ์คือ 10</span><span class="sxs-lookup"><span data-stu-id="240c6-261">Therefore, the maximum point total in each result group is 10.</span></span> 

<span data-ttu-id="240c6-262">ตารางต่อไปนี้แสดงข้อความตามจุดที่คุณกำหนดสำหรับกลุ่มผลคะแนน "ความสามารถด้านความเป็นผู้นำ"</span><span class="sxs-lookup"><span data-stu-id="240c6-262">The following table shows the point-based messages that you define for the “leadership abilities” result group.</span></span>

| <span data-ttu-id="240c6-263">ช่วงคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-263">Point interval</span></span> | <span data-ttu-id="240c6-264">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="240c6-264">Text</span></span>                                       |
|----------------|--------------------------------------------|
| <span data-ttu-id="240c6-265">1 ถึง 3</span><span class="sxs-lookup"><span data-stu-id="240c6-265">1 to 3</span></span>         | <span data-ttu-id="240c6-266">คุณมีความสามารถด้านความเป็นผู้นำปานกลาง</span><span class="sxs-lookup"><span data-stu-id="240c6-266">You have average leadership abilities.</span></span>     |
| <span data-ttu-id="240c6-267">4 ถึง 7</span><span class="sxs-lookup"><span data-stu-id="240c6-267">4 to 7</span></span>         | <span data-ttu-id="240c6-268">คุณมีความสามารถด้านความเป็นผู้นำดี</span><span class="sxs-lookup"><span data-stu-id="240c6-268">You have good leadership abilities.</span></span>        |
| <span data-ttu-id="240c6-269">8 ถึง 10</span><span class="sxs-lookup"><span data-stu-id="240c6-269">8 to 10</span></span>        | <span data-ttu-id="240c6-270">คุณมีความสามารถด้านความเป็นผู้นำโดดเด่น</span><span class="sxs-lookup"><span data-stu-id="240c6-270">You have outstanding leadership abilities.</span></span> |

<span data-ttu-id="240c6-271">คุณสามารถตั้งค่าช่วงคะแนนและข้อความสำหรับแต่ละกลุ่มผลลัพธ์ในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-271">You can set up point intervals and texts for each result group on a questionnaire.</span></span> <span data-ttu-id="240c6-272">มีการแสดงข้อความที่ตรงกับคะแนนของผู้ตอบแต่ละราย สำหรับแต่ละกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="240c6-272">Texts that correspond to each respondent’s score are displayed for each result group.</span></span> 

> [!NOTE]
> <span data-ttu-id="240c6-273">คุณสามารถเปลี่ยนช่วงคะแนนและข้อความได้</span><span class="sxs-lookup"><span data-stu-id="240c6-273">You can change intervals and texts.</span></span> <span data-ttu-id="240c6-274">อย่างไรก็ตาม ถ้าแบบสอบถามเสร็จสมบูรณ์แล้ว การเปลี่ยนแปลงอาจก่อให้เกิดความแตกต่างระหว่างรายงานผลลัพธ์ก่อนหน้านี้ และรายงานผลลัพธ์ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="240c6-274">However, if a questionnaire has been completed, changes might cause differences between previous and new result reports.</span></span>

### <a name="conditional-question-hierarchies"></a><span data-ttu-id="240c6-275">ลำดับชั้นของคำถามแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="240c6-275">Conditional question hierarchies</span></span>

<span data-ttu-id="240c6-276">ไม่จำเป็นต้องระบุลำดับชั้นของคำถามแบบมีเงื่อนไขเมื่อคุณตั้งค่าแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-276">Conditional question hierarchies are optional when you set up a questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="240c6-277">ก่อนที่คุณจะสามารถตั้งค่าลำดับชั้นของคำถามแบบมีเงื่อนไข คำถามที่มีการกำหนดกลุ่มคำตอบต้องแนบอยู่กับแบบสอบถามแล้ว</span><span class="sxs-lookup"><span data-stu-id="240c6-277">Before you can set up a conditional question hierarchy, you must attach questions that have assigned answer groups to the questionnaire.</span></span> 

<span data-ttu-id="240c6-278">เมื่อต้องการคำถามแบบมีเงื่อนไขเพื่อสร้าลำดับชั้นของคำถามแบบมีเงื่อนไข คุณสามารถกำหนดลำดับชั้นในการแสดงคำถาม ขึ้นอยู่กับการเลือกตอบแต่ละคำถามของผู้ตอบ</span><span class="sxs-lookup"><span data-stu-id="240c6-278">To use conditional questions to create a question hierarchy in a questionnaire, you can make the sequence that questions are presented in depend on the answer that a respondent selects for each question.</span></span> <span data-ttu-id="240c6-279">โดยการกำหนดลำดับของคำถามตามคำตอบของผู้ตอบ คุณสามารถปรับเปลี่ยนแบบสอบถาม ตามที่ผู้ตอบตอบได้</span><span class="sxs-lookup"><span data-stu-id="240c6-279">By basing the question sequence on a respondent’s answer, you can modify the questionnaire as the respondent completes it.</span></span>

#### <a name="examples"></a><span data-ttu-id="240c6-280">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="240c6-280">Examples</span></span>

<span data-ttu-id="240c6-281">นิติบุคคลเสนอทั้งสินค้าและบริการแก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="240c6-281">A legal entity offers both items and services to its customers.</span></span> <span data-ttu-id="240c6-282">ตามที่เกิดขึ้นในกรณีดังกล่าวโดยทั่วไป ลูกค้าบางรายซื้อเฉพาะสินค้า บางรายการซื้อเพียงบริการ และบางรายการซื้อทั้งสินค้าและบริการ</span><span class="sxs-lookup"><span data-stu-id="240c6-282">As typically occurs in such cases, some customers purchase only items, some purchase only services, and some purchase both items and services.</span></span> <span data-ttu-id="240c6-283">ดังนั้น เมื่อนิติบุคคลกระจายแบบสำรวจความพึงพอใจของลูกค้า จะใช้เป็นโครงสร้างแบบมีเงื่อนไขกับแบบสอบถาม เพื่อให้ลูกค้าที่ซื้อบริการเท่านั้นไม่จำเป็นต้องตอบคำถามเกี่ยวกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="240c6-283">Therefore, when the legal entity distributes a customer satisfaction survey, it applies a conditional structure to the questionnaire, so that customers who purchase only services don't have to answer questions about items.</span></span> 

<span data-ttu-id="240c6-284">อีกทางหนึ่งคือ คุณตั้งค่าแบบสอบถาม หากผู้ตอบเลือกคำตอบ A สำหรับคำถามข้อ 1 คำถาม 2 จะเป็นอันดับถัดไปในลำดับคำถาม</span><span class="sxs-lookup"><span data-stu-id="240c6-284">Alternatively, you set up a questionnaire so that if a respondent selects answer A for question 1, question 2 is next in the question sequence.</span></span> <span data-ttu-id="240c6-285">อย่างไรก็ตาม ถ้าผู้ตอบเลือกคำตอบ B สำหรับคำถามข้อ 1 คำถาม 5 จะเป็นอันดับถัดไป</span><span class="sxs-lookup"><span data-stu-id="240c6-285">However, if the respondent selects answer B for question 1, question 5 is next.</span></span>