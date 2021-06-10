---
title: พัฒนาแผนการสืบทอด
description: เมื่อองค์กรของคุณโตขึ้น คุณต้องเริ่มต้นการวางแผนการสืบทอด
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dae4292bed986cdc53254162f1af44a75ebdf29d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058787"
---
# <a name="develop-a-succession-plan"></a><span data-ttu-id="d193b-103">พัฒนาแผนการสืบทอด</span><span class="sxs-lookup"><span data-stu-id="d193b-103">Develop a succession plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d193b-104">เมื่อองค์กรของคุณโตขึ้น คุณต้องเริ่มต้นการวางแผนการสืบทอด</span><span class="sxs-lookup"><span data-stu-id="d193b-104">As your organization grows, you must begin succession planning.</span></span> <span data-ttu-id="d193b-105">ในระหว่างการวางแผนการสืบทอด คุณอาจต้องการค้นหาบุคคลที่มีทักษะคล้ายกับบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="d193b-105">During succession planning, you might want to find someone who has similar skills to another person.</span></span> <span data-ttu-id="d193b-106">การแม็ปทักษะช่วยให้คุณสามารถวิเคราะห์พนักงานที่มีอยู่และผู้สมัคร เพื่อดูว่าตรงกับชุดทักษะของพนักงานที่มีคุณค่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d193b-106">Skill mapping allows you to analyze your existing employees and applicants to see if they match the skill set of a valued employee.</span></span> <span data-ttu-id="d193b-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="d193b-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d193b-108">ไปที่ **ทรัพยากรบุคคล > ความสามารถ > การวิเคราะห์ทักษะ > โปรไฟล์การแม็ปทักษะ**</span><span class="sxs-lookup"><span data-stu-id="d193b-108">Go to **Human resources > Competencies > Skill analysis > Skill mapping profiles**.</span></span>
2. <span data-ttu-id="d193b-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d193b-109">Select **New**.</span></span>
3. <span data-ttu-id="d193b-110">ในฟิลด์ **การแม็ปทักษะ** ให้ป้อนชื่อสำหรับการแม็ปทักษะของคุณ</span><span class="sxs-lookup"><span data-stu-id="d193b-110">In the **Skill mapping** field, enter a name for your skill mapping.</span></span> <span data-ttu-id="d193b-111">ตัวอย่าง: พนักงาน</span><span class="sxs-lookup"><span data-stu-id="d193b-111">Example: Employee.</span></span>
4. <span data-ttu-id="d193b-112">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d193b-112">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="d193b-113">ในฟิลด์ **วันที่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d193b-113">In the **Date** field, enter a date.</span></span>
6. <span data-ttu-id="d193b-114">เลือก **เรียกข้อมูลโปรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="d193b-114">Select **Retrieve profile**.</span></span>
7. <span data-ttu-id="d193b-115">เลือก **บุคคล**</span><span class="sxs-lookup"><span data-stu-id="d193b-115">Select **Person**.</span></span>
8. <span data-ttu-id="d193b-116">ในฟิลด์ **บุคคล** ให้พิมพ์ชื่อ หรือเลือกแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="d193b-116">In the **Person** field, type in a name, or select the drop-down.</span></span>
9. <span data-ttu-id="d193b-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d193b-117">Select **OK**.</span></span>
10. <span data-ttu-id="d193b-118">ขยายแท็บด่วน **ใบรับรอง** เพื่อดูหรือแก้ไขใบรับรองที่รวมอยู่ในการแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="d193b-118">Expand the **Certificates** fast tab to view or edit the certificates included in the skill mapping.</span></span>
11. <span data-ttu-id="d193b-119">ขยายแท็บด่วน **ทักษะ** เพื่อดูหรือแก้ไขทักษะที่จะถูกรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="d193b-119">Expand the **Skills** fast tab to view or edit the skills to be included.</span></span>
12. <span data-ttu-id="d193b-120">ในรายการ ให้ทำเครื่องหมายที่แถวแรก </span><span class="sxs-lookup"><span data-stu-id="d193b-120">In the list, mark the first row.</span></span> <span data-ttu-id="d193b-121">ตัวอย่าง: การบัญชี</span><span class="sxs-lookup"><span data-stu-id="d193b-121">Example:  Accounting.</span></span>
13. <span data-ttu-id="d193b-122">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="d193b-122">Select the **Optional** checkbox.</span></span>
14. <span data-ttu-id="d193b-123">ในฟิลด์ **ความสำคัญ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d193b-123">In the **Importance** field, select an option.</span></span> <span data-ttu-id="d193b-124">เมื่อคุณทำเครื่องหมายที่ทักษะให้เป็นไม่จำเป็น คุณจะต้องเลือกระดับความสำคัญของทักษะ</span><span class="sxs-lookup"><span data-stu-id="d193b-124">When you mark a skill as optional, you must select the importance level of the skill.</span></span>  
15. <span data-ttu-id="d193b-125">ในรายการ ให้เลือกแถว 2</span><span class="sxs-lookup"><span data-stu-id="d193b-125">In the list, select row 2.</span></span>
16. <span data-ttu-id="d193b-126">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="d193b-126">Select the **Optional** checkbox.</span></span>
17. <span data-ttu-id="d193b-127">ในฟิลด์ **ความสำคัญ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d193b-127">In the **Importance** field, select an option.</span></span>
18. <span data-ttu-id="d193b-128">ในรายการ ให้เลือกแถว 3</span><span class="sxs-lookup"><span data-stu-id="d193b-128">In the list, select row 3.</span></span>
19. <span data-ttu-id="d193b-129">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="d193b-129">Select the **Optional** checkbox.</span></span>
20. <span data-ttu-id="d193b-130">ในฟิลด์ **ความสำคัญ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d193b-130">In the **Importance** field, select an option.</span></span>
21. <span data-ttu-id="d193b-131">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="d193b-131">In the list, select row 4.</span></span>
22. <span data-ttu-id="d193b-132">เลือกกล่องกาเครื่องหมาย **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="d193b-132">Select the **Optional** checkbox.</span></span>
23. <span data-ttu-id="d193b-133">ในฟิลด์ความสำคัญ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d193b-133">In the Importance field, select an option.</span></span>
24. <span data-ttu-id="d193b-134">ขยายแท็บด่วน **การศึกษา** เพื่อดูหรือแก้ไขความสามารถทางการศึกษาที่จะรวมในการแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="d193b-134">Expand the **Education** fast tab to view or edit the education competencies to be included in the skill mapping.</span></span>
25. <span data-ttu-id="d193b-135">เลือก **ปฏิบัติการ**</span><span class="sxs-lookup"><span data-stu-id="d193b-135">Select **Execute**.</span></span>
26. <span data-ttu-id="d193b-136">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d193b-136">Select **OK**.</span></span>
27. <span data-ttu-id="d193b-137">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="d193b-137">Select **Result**.</span></span>
28. <span data-ttu-id="d193b-138">เลือก **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="d193b-138">Select **Report**.</span></span> <span data-ttu-id="d193b-139">รายงานจะแสดงรายการการจับคู่ที่ดีที่สุดที่ด้านบนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="d193b-139">The report lists the best matches at the top of the report.</span></span> <span data-ttu-id="d193b-140">คุณสามารถเห็นว่ามีองค์ประกอบช่องว่างอยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="d193b-140">You can see a gap element listed.</span></span> <span data-ttu-id="d193b-141">ช่องว่างคือความแตกต่างระหว่างระดับการแม็ปทักษะและระดับทักษะของบุคคล</span><span class="sxs-lookup"><span data-stu-id="d193b-141">A gap is the difference between the skill-mapping level and the person's skill level.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]