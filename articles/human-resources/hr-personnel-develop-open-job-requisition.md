---
title: พัฒนาและเปิดคำขอจัดจ้างพนักงาน
description: 'โครงการสรรหาบุคลากรช่วยในการจัดการกระบวนการสรรหาบุคลากร '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3207d61536422255b574fd126f16075fcddc2c93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420700"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="c488e-103">พัฒนาและเปิดคำขอจัดจ้างพนักงาน</span><span class="sxs-lookup"><span data-stu-id="c488e-103">Develop and open job requisition</span></span>



<span data-ttu-id="c488e-104">โครงการสรรหาบุคลากรช่วยในการจัดการกระบวนการสรรหาบุคลากร </span><span class="sxs-lookup"><span data-stu-id="c488e-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="c488e-105">สำหรับแต่ละโครงการสรรหาบุคลากร คุณสามารถตั้งค่าข้อมูล เช่น งานที่มาจากการสรรหาบุคลากร ชื่อของผู้ที่สรรหา สถานะของโครงการและแผนกที่งานจะอยู่</span><span class="sxs-lookup"><span data-stu-id="c488e-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="c488e-106">หลังจากการสร้างโครงการสรรหาบุคลากร คุณสามารถเขียนการโฆษณารับสมัครงานสำหรับโครงการ การเผยแพร่โฆษณารับสมัครในหน้าบริการตนเองของพนักงาน เชื่อมโยงใบสมัครสำหรับการจ้างงานกับโครงการ และติดตามกิจกรรมสำหรับโครงการนั้น</span><span class="sxs-lookup"><span data-stu-id="c488e-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="c488e-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c488e-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c488e-108">ในการเริ่มต้นกระบวนงาน ให้ไปที่ ทรัพยากรบุคคล > การสรรหาบุคลากร > โครงการสรรหาบุคลากร > โครงการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="c488e-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="c488e-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c488e-109">Click New.</span></span>
2. <span data-ttu-id="c488e-110">ในฟิลด์การสรรหาบุคลากร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c488e-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="c488e-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c488e-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="c488e-112">ในฟิลด์ผู้สรรหาบุคลากร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c488e-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c488e-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c488e-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c488e-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c488e-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c488e-115">คลิก เลือก</span><span class="sxs-lookup"><span data-stu-id="c488e-115">Click Select.</span></span>
8. <span data-ttu-id="c488e-116">ในฟิลด์แผนก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c488e-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c488e-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c488e-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c488e-118">ในฟิลด์งาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c488e-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="c488e-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c488e-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="c488e-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c488e-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="c488e-121">ในฟิลด์จำนวนตำแหน่งที่เปิดรับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="c488e-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="c488e-122">ในฟิลด์การว่าจ้างผู้จัดการ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c488e-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c488e-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c488e-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="c488e-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c488e-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="c488e-125">คลิก เลือก</span><span class="sxs-lookup"><span data-stu-id="c488e-125">Click Select.</span></span>
18. <span data-ttu-id="c488e-126">ในฟิลด์กำหนดเวลาของใบสมัคร ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c488e-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="c488e-127">คลิกที่สื่อ</span><span class="sxs-lookup"><span data-stu-id="c488e-127">Click Media.</span></span>
    * <span data-ttu-id="c488e-128">โครงการสรรหาบุคลากรได้รวมตัวเลือกเพื่อระบุเต้ารับสื่อที่จะใช้เพื่อลงโฆษณาตำแหน่งที่เปิด</span><span class="sxs-lookup"><span data-stu-id="c488e-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="c488e-129">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c488e-129">Click New.</span></span>
21. <span data-ttu-id="c488e-130">ในฟิลด์สื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c488e-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="c488e-131">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c488e-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="c488e-132">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="c488e-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="c488e-133">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c488e-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="c488e-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c488e-134">Click Save.</span></span>
26. <span data-ttu-id="c488e-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c488e-135">Close the page.</span></span>
27. <span data-ttu-id="c488e-136">คลิกที่โฆษณารับสมัครงาน</span><span class="sxs-lookup"><span data-stu-id="c488e-136">Click Job ads.</span></span>
28. <span data-ttu-id="c488e-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c488e-137">Click Save.</span></span>
29. <span data-ttu-id="c488e-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c488e-138">Close the page.</span></span>
30. <span data-ttu-id="c488e-139">เลือกหรือยกเลิกการแสดงผลที่กล่องกาเครื่องหมายบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="c488e-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="c488e-140">เลือกการแสดงผลกล่องกาเครื่องหมายด้วยตนเองของพนักงาน เพื่อให้พนักงานสามารถมองเห็นโครงการสรรหาบุคลากรในหน้าบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="c488e-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="c488e-141">คลิกที่สถานะของโครงการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="c488e-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="c488e-142">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c488e-142">Click Start.</span></span>
    * <span data-ttu-id="c488e-143">สถานะเริ่มต้นหมายถึงโครงการพร้อมที่จะรับใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="c488e-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="c488e-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c488e-144">Click OK.</span></span>

