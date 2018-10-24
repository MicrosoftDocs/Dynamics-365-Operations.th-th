--- 
title: "สร้างคำถามปลายปิดแบบสิ้นสุด"
description: "คำถามแบบปิดอนุญาตให้คุณระบุตัวเลือกให้ผู้ตอบให้เลือกได้ "
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6b08988a3872cec39b7592732d23862e959aae79
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="c4582-103">สร้างคำถามปลายปิดแบบสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="c4582-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4582-104">คำถามแบบปิดอนุญาตให้คุณระบุตัวเลือกให้ผู้ตอบให้เลือกได้ </span><span class="sxs-lookup"><span data-stu-id="c4582-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="c4582-105">อย่างแรกคุณจำเป็นต้องสร้างกลุ่มคำตอบกับคำตอบ จากนั้นสร้างคำถามที่จะใช้สำหรับกลุ่มคำตอบ </span><span class="sxs-lookup"><span data-stu-id="c4582-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="c4582-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c4582-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="c4582-107">สร้างกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="c4582-107">Create an answer group</span></span>
1. <span data-ttu-id="c4582-108">ไปที่ แบบสอบถาม > การออกแบบ > กลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="c4582-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="c4582-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4582-109">Click New.</span></span>
3. <span data-ttu-id="c4582-110">ในฟิลด์กลุ่มคำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4582-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="c4582-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c4582-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c4582-112">ใช้ฟังก์ชัน Randomize เพื่อสุ่มวางคำตอบในลำดับแตกต่างกันทุกครั้งที่กลุ่มคำตอบถูกใช้สำหรับคำถาม</span><span class="sxs-lookup"><span data-stu-id="c4582-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="c4582-113">คลิกคำตอบ</span><span class="sxs-lookup"><span data-stu-id="c4582-113">Click Answer.</span></span>
6. <span data-ttu-id="c4582-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4582-114">Click New.</span></span>
    * <span data-ttu-id="c4582-115">หมายเลขลำดับควบคุมลำดับที่ของคำตอบที่ถูกแสดง ยกเว้นว่า Randomize ถูกเลือกสำหรับกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="c4582-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="c4582-116">คะแนนสะสมสามาถใช้เป็นรางวัลแก่คำตอบสำหรับใช้ในการให้คะแนนแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="c4582-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="c4582-117">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c4582-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="c4582-118">คำตอบถูกต้องที่สามารถถูกทำเครื่องหมายว่าอันที่ถูกเลือกนั้นถูกต้องหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="c4582-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="c4582-119">สิ่งนี้สามารถใช้เพื่อให้คะแนนในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="c4582-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="c4582-120">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4582-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="c4582-121">ดำเนินต่อเพื่อสร้างตัวเลือกคำตอบสำหรับกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="c4582-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="c4582-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4582-122">Click New.</span></span>
10. <span data-ttu-id="c4582-123">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c4582-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="c4582-124">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4582-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="c4582-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4582-125">Click New.</span></span>
13. <span data-ttu-id="c4582-126">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c4582-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="c4582-127">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4582-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="c4582-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4582-128">Click New.</span></span>
16. <span data-ttu-id="c4582-129">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c4582-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="c4582-130">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4582-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="c4582-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4582-131">Click New.</span></span>
19. <span data-ttu-id="c4582-132">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c4582-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="c4582-133">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4582-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="c4582-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c4582-134">Close the page.</span></span>
22. <span data-ttu-id="c4582-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c4582-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="c4582-136">สร้างคำถาม</span><span class="sxs-lookup"><span data-stu-id="c4582-136">Create the question</span></span>
1. <span data-ttu-id="c4582-137">ไปที่แบบสอบถาม > การออกแบบ > คำถาม</span><span class="sxs-lookup"><span data-stu-id="c4582-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="c4582-138">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4582-138">Click New.</span></span>
3. <span data-ttu-id="c4582-139">ใช้ฟิลด์การจัดกลุ่มเพื่อจัดกลุ่มคำถามที่เกี่ยวข้องกัน</span><span class="sxs-lookup"><span data-stu-id="c4582-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="c4582-140">คุณสามารถใช้ข้อมูลป้อนเข้าของกล่องกาเครื่องหมาย,ปุ่มทางเลือก,หรือกล่องคำสั่งผสมสำหรับคำถามแบบปิด</span><span class="sxs-lookup"><span data-stu-id="c4582-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="c4582-141">ในฟิลด์ชนิดของข้อมูลป้อนเข้า ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c4582-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="c4582-142">ในฟิลด์กลุ่มคำตอบ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4582-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="c4582-143">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="c4582-143">In the Text field, type a value.</span></span>


