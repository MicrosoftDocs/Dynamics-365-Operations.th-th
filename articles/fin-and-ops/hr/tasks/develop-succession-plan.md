--- 
title: "พัฒนาแผนการสืบทอด"
description: "เมื่อองค์กรของคุณขยายตัว และคุณพิจารณาการวางแผนการสืบทอด คุณอาจต้องการค้นหาบุคคลที่มีทักษะที่คล้ายกันกับอีกบุคคลหนึ่ง "
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b1caaf5f52282a8daae62602dcc5ef86b901e338
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="develop-a-succession-plan"></a><span data-ttu-id="49c4e-103">พัฒนาแผนการสืบทอด</span><span class="sxs-lookup"><span data-stu-id="49c4e-103">Develop a succession plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49c4e-104">เมื่อองค์กรของคุณขยายตัว และคุณพิจารณาการวางแผนการสืบทอด คุณอาจต้องการค้นหาบุคคลที่มีทักษะที่คล้ายกันกับอีกบุคคลหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="49c4e-104">As your organization grows, and you consider succession planning, you may want to find someone who has similar skills to another person.</span></span>  <span data-ttu-id="49c4e-105">การแม็ปทักษะช่วยให้คุณสามารถวิเคราะห์พนักงานที่มีอยู่และผู้สมัคร เพื่อดูว่าตรงกับชุดทักษะของพนักงานที่มีคุณค่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="49c4e-105">Skill mapping allows you to analyse your existing employees and applicants to see if they match the skill set of a valued employee.</span></span> <span data-ttu-id="49c4e-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="49c4e-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="49c4e-107">ไปที่ทรัพยากรบุคคล > ความสามารถ > การวิเคราะห์ทักษะ > โพรไฟล์การแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="49c4e-107">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="49c4e-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="49c4e-108">Click New.</span></span>
3. <span data-ttu-id="49c4e-109">ในฟิลด์การแม็ปทักษะ ให้ป้อนชื่อสำหรับการแม็ปทักษะของคุณ </span><span class="sxs-lookup"><span data-stu-id="49c4e-109">In the Skill mapping field, In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="49c4e-110">ตัวอย่าง: พนักงาน</span><span class="sxs-lookup"><span data-stu-id="49c4e-110">Example: Employee.</span></span>
4. <span data-ttu-id="49c4e-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="49c4e-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="49c4e-112">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="49c4e-112">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="49c4e-113">เลือกการดึงข้อมูลโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="49c4e-113">Click Retrieve profile.</span></span>
7. <span data-ttu-id="49c4e-114">คลิกที่บุคคล</span><span class="sxs-lookup"><span data-stu-id="49c4e-114">Click Person.</span></span>
8. <span data-ttu-id="49c4e-115">ในฟิลด์บุคคล ให้พิมพ์ชื่อ หรือเลือกแบบหล่นลง </span><span class="sxs-lookup"><span data-stu-id="49c4e-115">In the Person field, type in a name, or select the drop down.</span></span>  <span data-ttu-id="49c4e-116">ตัวอย่าง: Cassie Hicks</span><span class="sxs-lookup"><span data-stu-id="49c4e-116">Example: Cassie Hicks.</span></span>
9. <span data-ttu-id="49c4e-117">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="49c4e-117">Click OK.</span></span>
10. <span data-ttu-id="49c4e-118">ขยายใบรับรองแท็บด่วนเพื่อดูหรือแก้ไขใบรับรองที่รวมอยู่ในการแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="49c4e-118">Exapnd the certificates fast tab to view or edit the certificates included in the skill mapping.</span></span>
11. <span data-ttu-id="49c4e-119">ขยายแท็บด่วนทักษะเพื่อดูหรือแก้ไขทักษะที่จะถูกรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="49c4e-119">Expand the Skills fast tab to view or edit the skills to be included.</span></span>
12. <span data-ttu-id="49c4e-120">ในรายการ ให้ทำเครื่องหมายที่แถวแรก </span><span class="sxs-lookup"><span data-stu-id="49c4e-120">In the list, mark the first row.</span></span>  <span data-ttu-id="49c4e-121">ตัวอย่าง:  การบัญชี</span><span class="sxs-lookup"><span data-stu-id="49c4e-121">Example:  Accounting</span></span>
13. <span data-ttu-id="49c4e-122">คลิกกล่องกาเครื่องหมาย ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="49c4e-122">Click the Optional checkbox.</span></span>
14. <span data-ttu-id="49c4e-123">ในฟิลด์ความสำคัญ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="49c4e-123">In the Importance field, select an option.</span></span>
    * <span data-ttu-id="49c4e-124">เมื่อคุณทำเครื่องหมายที่ทักษะให้เป็นไม่จำเป็น คุณจะต้องเลือกระดับความสำคัญของทักษะ</span><span class="sxs-lookup"><span data-stu-id="49c4e-124">When you mark a skill as optional, you are required to select the importance level of the skill.</span></span>  
15. <span data-ttu-id="49c4e-125">ในรายการ ให้เลือกแถว 2</span><span class="sxs-lookup"><span data-stu-id="49c4e-125">In the list, select row 2.</span></span>
16. <span data-ttu-id="49c4e-126">คลิกกล่องกาเครื่องหมาย ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="49c4e-126">Click the Optional checkbox.</span></span>
17. <span data-ttu-id="49c4e-127">ในฟิลด์ความสำคัญ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="49c4e-127">In the Importance field, select an option.</span></span>
18. <span data-ttu-id="49c4e-128">ในรายการ ให้เลือกแถว 3</span><span class="sxs-lookup"><span data-stu-id="49c4e-128">In the list, select row 3.</span></span>
19. <span data-ttu-id="49c4e-129">คลิกกล่องกาเครื่องหมาย ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="49c4e-129">Click the Optional checkbox.</span></span>
20. <span data-ttu-id="49c4e-130">ในฟิลด์ความสำคัญ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="49c4e-130">In the Importance field, select an option.</span></span>
21. <span data-ttu-id="49c4e-131">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="49c4e-131">In the list, select row 4.</span></span>
22. <span data-ttu-id="49c4e-132">คลิกกล่องกาเครื่องหมาย ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="49c4e-132">Click the Optional checkbox.</span></span>
23. <span data-ttu-id="49c4e-133">ในฟิลด์ความสำคัญ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="49c4e-133">In the Importance field, select an option.</span></span>
24. <span data-ttu-id="49c4e-134">ขยายแท็บด่วนการศึกษา เพื่อดูหรือแก้ไขความสามารถทางการศึกษาที่จะรวมในการแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="49c4e-134">Expand the Education fast tab to view or edit the education competencies to be included in the skill mapping.</span></span>
25. <span data-ttu-id="49c4e-135">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="49c4e-135">Click Execute.</span></span>
26. <span data-ttu-id="49c4e-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="49c4e-136">Click OK.</span></span>
27. <span data-ttu-id="49c4e-137">คลิกผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="49c4e-137">Click Result.</span></span>
28. <span data-ttu-id="49c4e-138">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="49c4e-138">Click Report.</span></span>
    * <span data-ttu-id="49c4e-139">รายงานจะแสดงรายการการจับคู่ที่ดีที่สุดที่ด้านบนของรายงาน </span><span class="sxs-lookup"><span data-stu-id="49c4e-139">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="49c4e-140">คุณสามารถเห็นว่ามีองค์ประกอบช่องว่างอยู่ในรายการ </span><span class="sxs-lookup"><span data-stu-id="49c4e-140">You can see that there is a gap element listed.</span></span>  <span data-ttu-id="49c4e-141">นี่คือความแตกต่างระหว่างระดับที่มีการแสดงรายการอยู่ในการแม็ปทักษะ และระดับของทักษะที่กำหนดให้กับบุคคล</span><span class="sxs-lookup"><span data-stu-id="49c4e-141">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  


