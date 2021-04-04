---
title: สร้างคำถามปลายปิดแบบสิ้นสุด
description: 'คำถามแบบปิดอนุญาตให้คุณระบุตัวเลือกให้ผู้ตอบให้เลือกได้ '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09bf57b26111be0e3de358a6c955b3df7bf50668
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467902"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="5b2bb-103">สร้างคำถามปลายปิดแบบสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="5b2bb-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="5b2bb-104">คำถามแบบปิดอนุญาตให้คุณระบุตัวเลือกให้ผู้ตอบให้เลือกได้ </span><span class="sxs-lookup"><span data-stu-id="5b2bb-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="5b2bb-105">อย่างแรกคุณจำเป็นต้องสร้างกลุ่มคำตอบกับคำตอบ จากนั้นสร้างคำถามที่จะใช้สำหรับกลุ่มคำตอบ </span><span class="sxs-lookup"><span data-stu-id="5b2bb-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="5b2bb-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="5b2bb-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="5b2bb-107">สร้างกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="5b2bb-107">Create an answer group</span></span>
1. <span data-ttu-id="5b2bb-108">ไปที่ แบบสอบถาม > การออกแบบ > กลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="5b2bb-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="5b2bb-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-109">Click New.</span></span>
3. <span data-ttu-id="5b2bb-110">ในฟิลด์กลุ่มคำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="5b2bb-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5b2bb-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="5b2bb-112">ใช้ฟังก์ชัน Randomize เพื่อสุ่มวางคำตอบในลำดับแตกต่างกันทุกครั้งที่กลุ่มคำตอบถูกใช้สำหรับคำถาม</span><span class="sxs-lookup"><span data-stu-id="5b2bb-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="5b2bb-113">คลิกคำตอบ</span><span class="sxs-lookup"><span data-stu-id="5b2bb-113">Click Answer.</span></span>
6. <span data-ttu-id="5b2bb-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-114">Click New.</span></span>
    * <span data-ttu-id="5b2bb-115">หมายเลขลำดับควบคุมลำดับที่ของคำตอบที่ถูกแสดง ยกเว้นว่า Randomize ถูกเลือกสำหรับกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="5b2bb-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="5b2bb-116">คะแนนสะสมสามาถใช้เป็นรางวัลแก่คำตอบสำหรับใช้ในการให้คะแนนแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="5b2bb-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="5b2bb-117">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5b2bb-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="5b2bb-118">คำตอบถูกต้องที่สามารถถูกทำเครื่องหมายว่าอันที่ถูกเลือกนั้นถูกต้องหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="5b2bb-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="5b2bb-119">สิ่งนี้สามารถใช้เพื่อให้คะแนนในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="5b2bb-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="5b2bb-120">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="5b2bb-121">ดำเนินต่อเพื่อสร้างตัวเลือกคำตอบสำหรับกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="5b2bb-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="5b2bb-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-122">Click New.</span></span>
10. <span data-ttu-id="5b2bb-123">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5b2bb-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="5b2bb-124">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="5b2bb-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-125">Click New.</span></span>
13. <span data-ttu-id="5b2bb-126">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5b2bb-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="5b2bb-127">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="5b2bb-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-128">Click New.</span></span>
16. <span data-ttu-id="5b2bb-129">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5b2bb-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="5b2bb-130">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="5b2bb-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-131">Click New.</span></span>
19. <span data-ttu-id="5b2bb-132">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5b2bb-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="5b2bb-133">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="5b2bb-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5b2bb-134">Close the page.</span></span>
22. <span data-ttu-id="5b2bb-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5b2bb-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="5b2bb-136">สร้างคำถาม</span><span class="sxs-lookup"><span data-stu-id="5b2bb-136">Create the question</span></span>
1. <span data-ttu-id="5b2bb-137">ไปที่แบบสอบถาม > การออกแบบ > คำถาม</span><span class="sxs-lookup"><span data-stu-id="5b2bb-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="5b2bb-138">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-138">Click New.</span></span>
3. <span data-ttu-id="5b2bb-139">ใช้ฟิลด์การจัดกลุ่มเพื่อจัดกลุ่มคำถามที่เกี่ยวข้องกัน</span><span class="sxs-lookup"><span data-stu-id="5b2bb-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="5b2bb-140">คุณสามารถใช้ข้อมูลป้อนเข้าของกล่องกาเครื่องหมาย,ปุ่มทางเลือก,หรือกล่องคำสั่งผสมสำหรับคำถามแบบปิด</span><span class="sxs-lookup"><span data-stu-id="5b2bb-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="5b2bb-141">ในฟิลด์ชนิดของข้อมูลป้อนเข้า ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="5b2bb-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="5b2bb-142">ในฟิลด์กลุ่มคำตอบ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b2bb-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="5b2bb-143">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="5b2bb-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]