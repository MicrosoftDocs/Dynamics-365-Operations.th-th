---
title: พัฒนาแผนการสืบทอด
description: เมื่อองค์กรของคุณโตขึ้น คุณต้องเริ่มต้นการวางแผนการสืบทอด
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 203dbc5463bfcc4249e9ed73802a9a1fc153f260
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130216"
---
# <a name="develop-a-succession-plan"></a><span data-ttu-id="46a91-103">พัฒนาแผนการสืบทอด</span><span class="sxs-lookup"><span data-stu-id="46a91-103">Develop a succession plan</span></span>

<span data-ttu-id="46a91-104">เมื่อองค์กรของคุณโตขึ้น คุณต้องเริ่มต้นการวางแผนการสืบทอด</span><span class="sxs-lookup"><span data-stu-id="46a91-104">As your organization grows, you must begin succession planning.</span></span> <span data-ttu-id="46a91-105">ในระหว่างการวางแผนการสืบทอด คุณอาจต้องการค้นหาบุคคลที่มีทักษะคล้ายกับบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="46a91-105">During succession planning, you might want to find someone who has similar skills to another person.</span></span> <span data-ttu-id="46a91-106">การแม็ปทักษะช่วยให้คุณสามารถวิเคราะห์พนักงานที่มีอยู่และผู้สมัคร เพื่อดูว่าตรงกับชุดทักษะของพนักงานที่มีคุณค่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="46a91-106">Skill mapping allows you to analyze your existing employees and applicants to see if they match the skill set of a valued employee.</span></span> <span data-ttu-id="46a91-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="46a91-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="46a91-108">ไปที่ **ทรัพยากรบุคคล > ความสามารถ > การวิเคราะห์ทักษะ > โปรไฟล์การแม็ปทักษะ**</span><span class="sxs-lookup"><span data-stu-id="46a91-108">Go to **Human resources > Competencies > Skill analysis > Skill mapping profiles**.</span></span>
2. <span data-ttu-id="46a91-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="46a91-109">Select **New**.</span></span>
3. <span data-ttu-id="46a91-110">ในฟิลด์ **การแม็ปทักษะ** ให้ป้อนชื่อสำหรับการแม็ปทักษะของคุณ</span><span class="sxs-lookup"><span data-stu-id="46a91-110">In the **Skill mapping** field, enter a name for your skill mapping.</span></span> <span data-ttu-id="46a91-111">ตัวอย่าง: พนักงาน</span><span class="sxs-lookup"><span data-stu-id="46a91-111">Example: Employee.</span></span>
4. <span data-ttu-id="46a91-112">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="46a91-112">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="46a91-113">ในฟิลด์ **วันที่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="46a91-113">In the **Date** field, enter a date.</span></span>
6. <span data-ttu-id="46a91-114">เลือก **เรียกข้อมูลโปรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="46a91-114">Select **Retrieve profile**.</span></span>
7. <span data-ttu-id="46a91-115">เลือก **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="46a91-115">Select **Person**.</span></span>
8. <span data-ttu-id="46a91-116">ในฟิลด์ **บุคคล** ให้พิมพ์ชื่อ หรือเลือกแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="46a91-116">In the **Person** field, type in a name, or select the drop-down.</span></span>
9. <span data-ttu-id="46a91-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="46a91-117">Select **OK**.</span></span>
10. <span data-ttu-id="46a91-118">ขยายแท็บด่วน **ใบรับรอง** เพื่อดูหรือแก้ไขใบรับรองที่รวมอยู่ในการแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="46a91-118">Expand the **Certificates** fast tab to view or edit the certificates included in the skill mapping.</span></span>
11. <span data-ttu-id="46a91-119">ขยายแท็บด่วน **ทักษะ** เพื่อดูหรือแก้ไขทักษะที่จะถูกรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="46a91-119">Expand the **Skills** fast tab to view or edit the skills to be included.</span></span>
12. <span data-ttu-id="46a91-120">ในรายการ ให้ทำเครื่องหมายที่แถวแรก </span><span class="sxs-lookup"><span data-stu-id="46a91-120">In the list, mark the first row.</span></span> <span data-ttu-id="46a91-121">ตัวอย่าง: การบัญชี</span><span class="sxs-lookup"><span data-stu-id="46a91-121">Example:  Accounting.</span></span>
13. <span data-ttu-id="46a91-122">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="46a91-122">Select the **Optional** checkbox.</span></span>
14. <span data-ttu-id="46a91-123">ในฟิลด์ **ความสำคัญ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="46a91-123">In the **Importance** field, select an option.</span></span> <span data-ttu-id="46a91-124">เมื่อคุณทำเครื่องหมายที่ทักษะให้เป็นไม่จำเป็น คุณจะต้องเลือกระดับความสำคัญของทักษะ</span><span class="sxs-lookup"><span data-stu-id="46a91-124">When you mark a skill as optional, you must select the importance level of the skill.</span></span>  
15. <span data-ttu-id="46a91-125">ในรายการ ให้เลือกแถว 2</span><span class="sxs-lookup"><span data-stu-id="46a91-125">In the list, select row 2.</span></span>
16. <span data-ttu-id="46a91-126">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="46a91-126">Select the **Optional** checkbox.</span></span>
17. <span data-ttu-id="46a91-127">ในฟิลด์ **ความสำคัญ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="46a91-127">In the **Importance** field, select an option.</span></span>
18. <span data-ttu-id="46a91-128">ในรายการ ให้เลือกแถว 3</span><span class="sxs-lookup"><span data-stu-id="46a91-128">In the list, select row 3.</span></span>
19. <span data-ttu-id="46a91-129">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="46a91-129">Select the **Optional** checkbox.</span></span>
20. <span data-ttu-id="46a91-130">ในฟิลด์ **ความสำคัญ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="46a91-130">In the **Importance** field, select an option.</span></span>
21. <span data-ttu-id="46a91-131">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="46a91-131">In the list, select row 4.</span></span>
22. <span data-ttu-id="46a91-132">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="46a91-132">Select the **Optional** checkbox.</span></span>
23. <span data-ttu-id="46a91-133">ในฟิลด์ความสำคัญ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="46a91-133">In the Importance field, select an option.</span></span>
24. <span data-ttu-id="46a91-134">ขยายแท็บด่วน **การศึกษา** เพื่อดูหรือแก้ไขความสามารถทางการศึกษาที่จะรวมในการแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="46a91-134">Expand the **Education** fast tab to view or edit the education competencies to be included in the skill mapping.</span></span>
25. <span data-ttu-id="46a91-135">เลือก **ปฏิบัติการ**</span><span class="sxs-lookup"><span data-stu-id="46a91-135">Select **Execute**.</span></span>
26. <span data-ttu-id="46a91-136">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="46a91-136">Select **OK**.</span></span>
27. <span data-ttu-id="46a91-137">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="46a91-137">Select **Result**.</span></span>
28. <span data-ttu-id="46a91-138">เลือก **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="46a91-138">Select **Report**.</span></span> <span data-ttu-id="46a91-139">รายงานจะแสดงรายการการจับคู่ที่ดีที่สุดที่ด้านบนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="46a91-139">The report lists the best matches at the top of the report.</span></span> <span data-ttu-id="46a91-140">คุณสามารถเห็นว่ามีองค์ประกอบช่องว่างอยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="46a91-140">You can see a gap element listed.</span></span> <span data-ttu-id="46a91-141">ช่องว่างคือความแตกต่างระหว่างระดับการแม็ปทักษะและระดับทักษะของบุคคล</span><span class="sxs-lookup"><span data-stu-id="46a91-141">A gap is the difference between the skill-mapping level and the person's skill level.</span></span>  

