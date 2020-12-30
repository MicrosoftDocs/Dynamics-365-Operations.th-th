---
title: ระบุและปรับใช้เครื่องมือการคัดเลือกผู้สมัคร
description: 'การค้นหากลุ่มผู้สมัครที่เข้าเกณฑ์เพื่อบรรจุลงในตำแหน่งว่างอาจเป็นเรื่องยาก โดยเฉพาะอย่างยิ่งเมื่อตำแหน่งต้องการชุดของทักษะเฉพาะ '
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4e7ed6feaa1b5b27fcfc0ec99a2d75415fe7d6a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693075"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="4ba9c-103">ระบุและปรับใช้เครื่องมือการคัดเลือกผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="4ba9c-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ba9c-104">การค้นหากลุ่มผู้สมัครที่เข้าเกณฑ์เพื่อบรรจุลงในตำแหน่งว่างอาจเป็นเรื่องยาก โดยเฉพาะอย่างยิ่งเมื่อตำแหน่งต้องการชุดของทักษะเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="4ba9c-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="4ba9c-105">อย่างไรก็ตาม คุณอาจมีผู้สมัคร ที่มีทักษะตามที่คุณต้องการทำงานอยู่ในองค์กรของคุณอยู่แล้ว </span><span class="sxs-lookup"><span data-stu-id="4ba9c-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="4ba9c-106">คุณสามารถค้นหาชุดของทักษะเฉพาะของพนักงานที่คุณมีอยู่ หรือผู้สมัครใหม่</span><span class="sxs-lookup"><span data-stu-id="4ba9c-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="4ba9c-107">ซึ่งช่วยให้ผู้สรรหารวบรวมและกรั่นกรองผู้สมัครที่ได้มาสมัครในตำแหน่งงานที่เปิดรับทั้งในอดีตและปัจจุบันได้อย่างรวดเร็ว หรือช่วยให้ค้นหาผู้สมัครที่มีศักยภาพจากกลุ่มพนักงานที่มีอยู่แล้ว </span><span class="sxs-lookup"><span data-stu-id="4ba9c-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="4ba9c-108">ใช้การบันทึกงานนี้เพื่อเรียนรู้ว่าฟังก์ชันการแม็ปทักษะสามารถช่วยคุณค้นหาบุคคลที่เหมาะสมสำหรับตำแหน่งที่เปิดรับได้อย่างไร </span><span class="sxs-lookup"><span data-stu-id="4ba9c-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="4ba9c-109">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="4ba9c-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4ba9c-110">ไปที่ทรัพยากรบุคคล > ความสามารถ > การวิเคราะห์ทักษะ > โพรไฟล์การแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="4ba9c-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="4ba9c-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ba9c-111">Click New.</span></span>
3. <span data-ttu-id="4ba9c-112">ในฟิลด์การแม็ปทักษะ ให้ป้อนชื่อสำหรับการแม็ปทักษะของคุณ </span><span class="sxs-lookup"><span data-stu-id="4ba9c-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="4ba9c-113">ตัวอย่าง: นักบัญชี</span><span class="sxs-lookup"><span data-stu-id="4ba9c-113">Example: Accountant.</span></span>
4. <span data-ttu-id="4ba9c-114">ในฟิลด์คำอธิบายงาน ให้ป้อนคำอธิบายของการแม็ปทักษะ</span><span class="sxs-lookup"><span data-stu-id="4ba9c-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="4ba9c-115">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4ba9c-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="4ba9c-116">เลือกการดึงข้อมูลโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="4ba9c-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="4ba9c-117">ใช้การดึงข้อมูลโพรไฟล์เพื่อดึงข้อมูลใบรับรอง ทักษะ และข้อมูลการศึกษาจากบุคคลที่ถูกเลือก งานหรือหลักสูตรเป็นข้อมูลพื้นฐานสำหรับการค้นหาของคุณ จากนั้นคุณสามารถเพิ่มหรือลบเกณฑ์ </span><span class="sxs-lookup"><span data-stu-id="4ba9c-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="4ba9c-118">คุณสามารถบอกได้หากเงื่อนไขนั้นไม่จำเป็นและจัดอันดับความสำคัญของเกณฑ์</span><span class="sxs-lookup"><span data-stu-id="4ba9c-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="4ba9c-119">คลิกงาน</span><span class="sxs-lookup"><span data-stu-id="4ba9c-119">Click Job.</span></span>
8. <span data-ttu-id="4ba9c-120">ในฟิลด์งาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4ba9c-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="4ba9c-121">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="4ba9c-121">Click OK.</span></span>
10. <span data-ttu-id="4ba9c-122">ขยายแท็บด่วนช่วง และเพิ่มเติมข้อมูลอื่นๆเช่น แผนก</span><span class="sxs-lookup"><span data-stu-id="4ba9c-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="4ba9c-123">ขยายแท็บด่วนใบรับรอง เพื่อดูหรือแก้ไขประกาศนียบัตร</span><span class="sxs-lookup"><span data-stu-id="4ba9c-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="4ba9c-124">ขยายแท็บด่วนทักษะ เพื่อดูหรือแก้ไขทักษะ</span><span class="sxs-lookup"><span data-stu-id="4ba9c-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="4ba9c-125">ขยายแท็บด่วนการศึกษา เพื่อดูหรือแก้ไขเกณฑ์การศึกษา</span><span class="sxs-lookup"><span data-stu-id="4ba9c-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="4ba9c-126">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4ba9c-126">Click Execute.</span></span>
15. <span data-ttu-id="4ba9c-127">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="4ba9c-127">Click OK.</span></span>
16. <span data-ttu-id="4ba9c-128">คลิกผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4ba9c-128">Click Result.</span></span>
17. <span data-ttu-id="4ba9c-129">คลิกผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4ba9c-129">Click Result.</span></span>
18. <span data-ttu-id="4ba9c-130">คลิก ดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="4ba9c-130">Click Resume.</span></span>
19. <span data-ttu-id="4ba9c-131">คลิกประกาศนียบัตร</span><span class="sxs-lookup"><span data-stu-id="4ba9c-131">Click Certificates.</span></span>
    * <span data-ttu-id="4ba9c-132">คุณสามารถดูรายละเอียดเพิ่มเติมในแต่ละบุคคลที่แสดงในรายการ และดูรายละเอียดเกี่ยวกับการศึกษา ทักษะ และประสบการณ์การทำงานได้</span><span class="sxs-lookup"><span data-stu-id="4ba9c-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="4ba9c-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ba9c-133">Close the page.</span></span>
21. <span data-ttu-id="4ba9c-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ba9c-134">Close the page.</span></span>
22. <span data-ttu-id="4ba9c-135">เลือกผลลัพธ์อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="4ba9c-135">Select result again.</span></span>
23. <span data-ttu-id="4ba9c-136">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="4ba9c-136">Click Report.</span></span>
    * <span data-ttu-id="4ba9c-137">รายงานจะแสดงรายการการจับคู่ที่ดีที่สุดที่ด้านบนของรายงาน </span><span class="sxs-lookup"><span data-stu-id="4ba9c-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="4ba9c-138">คุณสามารถเห็นว่ามีองค์ประกอบช่องว่างอยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="4ba9c-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="4ba9c-139">นี่คือความแตกต่างระหว่างระดับที่มีการแสดงรายการอยู่ในการแม็ปทักษะ และระดับของทักษะที่กำหนดให้กับบุคคล</span><span class="sxs-lookup"><span data-stu-id="4ba9c-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="4ba9c-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ba9c-140">Close the page.</span></span>
25. <span data-ttu-id="4ba9c-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4ba9c-141">Click Save.</span></span>

