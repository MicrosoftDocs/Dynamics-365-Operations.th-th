--- 
title: "สร้างคำถามปลายปิดแบบสิ้นสุด"
description: "คำถามแบบปิดอนุญาตให้คุณระบุตัวเลือกให้ผู้ตอบให้เลือกได้ "
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: a3a043fd8c8b312ccfa2a87c2fdfb96ae05e9609
ms.contentlocale: th-th
ms.lasthandoff: 02/02/2018

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="55454-103">สร้างคำถามปลายปิดแบบสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="55454-103">Create a closed ended question</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55454-104">คำถามแบบปิดอนุญาตให้คุณระบุตัวเลือกให้ผู้ตอบให้เลือกได้ </span><span class="sxs-lookup"><span data-stu-id="55454-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="55454-105">อย่างแรกคุณจำเป็นต้องสร้างกลุ่มคำตอบกับคำตอบ จากนั้นสร้างคำถามที่จะใช้สำหรับกลุ่มคำตอบ </span><span class="sxs-lookup"><span data-stu-id="55454-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="55454-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="55454-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="55454-107">สร้างกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="55454-107">Create an answer group</span></span>
1. <span data-ttu-id="55454-108">ไปที่ แบบสอบถาม > การออกแบบ > กลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="55454-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="55454-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55454-109">Click New.</span></span>
3. <span data-ttu-id="55454-110">ในฟิลด์กลุ่มคำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55454-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="55454-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="55454-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="55454-112">ใช้ฟังก์ชัน Randomize เพื่อสุ่มวางคำตอบในลำดับแตกต่างกันทุกครั้งที่กลุ่มคำตอบถูกใช้สำหรับคำถาม</span><span class="sxs-lookup"><span data-stu-id="55454-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="55454-113">คลิกคำตอบ</span><span class="sxs-lookup"><span data-stu-id="55454-113">Click Answer.</span></span>
6. <span data-ttu-id="55454-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55454-114">Click New.</span></span>
    * <span data-ttu-id="55454-115">หมายเลขลำดับควบคุมลำดับที่ของคำตอบที่ถูกแสดง ยกเว้นว่า Randomize ถูกเลือกสำหรับกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="55454-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="55454-116">คะแนนสะสมสามาถใช้เป็นรางวัลแก่คำตอบสำหรับใช้ในการให้คะแนนแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="55454-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="55454-117">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="55454-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="55454-118">คำตอบถูกต้องที่สามารถถูกทำเครื่องหมายว่าอันที่ถูกเลือกนั้นถูกต้องหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="55454-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="55454-119">สิ่งนี้สามารถใช้เพื่อให้คะแนนในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="55454-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="55454-120">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55454-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="55454-121">ดำเนินต่อเพื่อสร้างตัวเลือกคำตอบสำหรับกลุ่มคำตอบ</span><span class="sxs-lookup"><span data-stu-id="55454-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="55454-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55454-122">Click New.</span></span>
10. <span data-ttu-id="55454-123">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="55454-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="55454-124">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55454-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="55454-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55454-125">Click New.</span></span>
13. <span data-ttu-id="55454-126">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="55454-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="55454-127">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55454-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="55454-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55454-128">Click New.</span></span>
16. <span data-ttu-id="55454-129">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="55454-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="55454-130">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55454-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="55454-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55454-131">Click New.</span></span>
19. <span data-ttu-id="55454-132">ให้ป้อนตัวเลขในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="55454-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="55454-133">ในฟิลด์คำตอบ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55454-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="55454-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="55454-134">Close the page.</span></span>
22. <span data-ttu-id="55454-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="55454-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="55454-136">สร้างคำถาม</span><span class="sxs-lookup"><span data-stu-id="55454-136">Create the question</span></span>
1. <span data-ttu-id="55454-137">ไปที่แบบสอบถาม > การออกแบบ > คำถาม</span><span class="sxs-lookup"><span data-stu-id="55454-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="55454-138">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55454-138">Click New.</span></span>
3. <span data-ttu-id="55454-139">ใช้ฟิลด์การจัดกลุ่มเพื่อจัดกลุ่มคำถามที่เกี่ยวข้องกัน</span><span class="sxs-lookup"><span data-stu-id="55454-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="55454-140">คุณสามารถใช้ข้อมูลป้อนเข้าของกล่องกาเครื่องหมาย,ปุ่มทางเลือก,หรือกล่องคำสั่งผสมสำหรับคำถามแบบปิด</span><span class="sxs-lookup"><span data-stu-id="55454-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="55454-141">ในฟิลด์ชนิดของข้อมูลป้อนเข้า ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="55454-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="55454-142">ในฟิลด์กลุ่มคำตอบ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="55454-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="55454-143">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="55454-143">In the Text field, type a value.</span></span>


