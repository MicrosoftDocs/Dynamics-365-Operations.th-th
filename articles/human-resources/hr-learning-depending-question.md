---
title: กำหนดคำถามโดยขึ้นอยู่กับคำตอบของคำถามก่อนหน้านี้
description: 'คำถามแบบมีเงื่อนไขอนุญาตให้คุณสามารถระบุคำถามที่ติดตามเพื่อผลจากผู้ตอบ โดยอาศัยคำตอบของคำถามก่อนหน้านี้ '
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae4a792e53127196aacdf659bb483867d5c17494
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794744"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="ee871-103">กำหนดคำถามโดยขึ้นอยู่กับคำตอบของคำถามก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ee871-103">Make a question dependent on the answer of the previous question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="ee871-104">คำถามแบบมีเงื่อนไขอนุญาตให้คุณสามารถระบุคำถามที่ติดตามเพื่อผลจากผู้ตอบ โดยอาศัยคำตอบของคำถามก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="ee871-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="ee871-105">ตัวอย่างเช่น ถ้าคุณถามถึง "คุณชอบกาแฟหรือชามากกว่ากัน" คำถามการติดตามผลแบบมีตรรกะจะถูกกำหนดโดยขึ้นอยู่กับว่าผู้ตอบเลือกกาแฟหรือชาเป็นคำตอบของตน </span><span class="sxs-lookup"><span data-stu-id="ee871-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="ee871-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="ee871-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="ee871-107">ค้นหาแบบสอบถามที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="ee871-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="ee871-108">ไปที่แบบสอบถาม > การออกแบบ > แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="ee871-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="ee871-109">ในรายการนี้ ให้เลือกแบบสอบถาม WorkFH</span><span class="sxs-lookup"><span data-stu-id="ee871-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="ee871-110">เพิ่มคำถามและคำถามย่อยทั้งหมดลงในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="ee871-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="ee871-111">คลิกคำถาม</span><span class="sxs-lookup"><span data-stu-id="ee871-111">Click Questions.</span></span>
2. <span data-ttu-id="ee871-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ee871-112">Click New.</span></span>
3. <span data-ttu-id="ee871-113">ในฟิลด์คำถาม ให้เลือกคำถามหมายเลข 00016</span><span class="sxs-lookup"><span data-stu-id="ee871-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="ee871-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ee871-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ee871-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ee871-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ee871-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ee871-116">Click Save.</span></span>
7. <span data-ttu-id="ee871-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ee871-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="ee871-118">ตั้งค่าลำดับแบบสอบถามเป็นแบบมีเงื่อนไข และกำหนดคำถามให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="ee871-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="ee871-119">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ee871-119">Click Edit.</span></span>
2. <span data-ttu-id="ee871-120">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="ee871-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="ee871-121">ในฟิลด์คำถาม ให้เลือก'มีเงื่อนไข'</span><span class="sxs-lookup"><span data-stu-id="ee871-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="ee871-122">คลิกคำถามแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="ee871-122">Click Conditional question.</span></span>
5. <span data-ttu-id="ee871-123">ในแผนภูมิ เลือก 'คำถาม\อธิบายว่าเพราะเหตุใดคุณถึงตอบคำถามก่อนหน้าแบบนั้น'</span><span class="sxs-lookup"><span data-stu-id="ee871-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="ee871-124">ในฟิลด์คำถามหลัก ให้เลือกคำถามหมายเลข 00009</span><span class="sxs-lookup"><span data-stu-id="ee871-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="ee871-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ee871-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ee871-126">ในฟิลด์คำตอบ ให้เรียงลำดับคำตอบโดยขึ้นอยู่กับตัวเลือกคำตอบที่คุณต้องการกำหนดคำถาม </span><span class="sxs-lookup"><span data-stu-id="ee871-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="ee871-127">ตัวอย่างเช่น ป้อน 1 สำหรับตัวเลือกคำตอบแรก</span><span class="sxs-lookup"><span data-stu-id="ee871-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="ee871-128">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="ee871-128">Click Save.</span></span>
10. <span data-ttu-id="ee871-129">ในแผนภูมิ เลือก 'คำถาม\ฉันได้รับเงินเดือนพอประมาณสำหรับงานที่ฉันทำ'</span><span class="sxs-lookup"><span data-stu-id="ee871-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="ee871-130">โปรดสังเกตว่า แผนภูมิคำถามการอัพเดตเพื่อแสดงการขึ้นต่อกัน</span><span class="sxs-lookup"><span data-stu-id="ee871-130">Note that the question tree updated to show the dependency.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]