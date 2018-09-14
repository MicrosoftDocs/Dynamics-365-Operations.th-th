--- 
title: "งานคัมบังตามกำหนดการ"
description: "ขั้นตอนนี้มุ่งเน้นการจัดกำหนดการกระบวนการงานคัมบังสำหรับเซลล์ทำงานเฉพาะ "
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5170fecf0190591d74f45d35fecc4472e7f5e900
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="45547-103">งานคัมบังตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="45547-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45547-104">ขั้นตอนนี้มุ่งเน้นการจัดกำหนดการกระบวนการงานคัมบังสำหรับเซลล์ทำงานเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="45547-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="45547-105">ขั้นตอน "การเตรียมงานกระบวนการคัมบังเมื่อไม่มีวัสดุอยู่" เป็นข้อกำหนดเบื้องต้นสำหรับการสร้างขั้นตอนนี้ </span><span class="sxs-lookup"><span data-stu-id="45547-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="45547-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="45547-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="45547-107">งานนี้มีไว้สำหรับผู้ควบคุมงานการผลิตและผู้วางแผนการผลิตที่ทำงานกับคัมบัง</span><span class="sxs-lookup"><span data-stu-id="45547-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="45547-108">เลือกงานคัมบังสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="45547-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="45547-109">ไปที่การควบคุมการผลิต > คัมบัง > การกำหนดเวลางานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="45547-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="45547-110">ขยายกล่องแสดงข้อมูลย่อกำลังการผลิตในรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="45547-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="45547-111">ขยายกล่องแสดงข้อมูลย่อคัมบัง</span><span class="sxs-lookup"><span data-stu-id="45547-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="45547-112">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="45547-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="45547-113">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="45547-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="45547-114">เลือกเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="45547-114">Select work cell 1250.</span></span> <span data-ttu-id="45547-115">ซึ่งจะกรองมุมมองเพื่อแสดงเฉพาะงานสำหรับเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="45547-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="45547-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="45547-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="45547-117">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="45547-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="45547-118">กำหนดตารางงานคัมบังในรอบระยะเวลาแรกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="45547-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="45547-119">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="45547-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="45547-120">เลือกแถวแรกในรายการที่อยู่ในสถานะที่ไม่ได้วางแผนไว้ </span><span class="sxs-lookup"><span data-stu-id="45547-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="45547-121">ไอคอนที่มีจุดในฟิลด์สถานะงานบ่งชี้ว่าไม่ได้วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="45547-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="45547-122">คลิก กำหนดเวลางาน</span><span class="sxs-lookup"><span data-stu-id="45547-122">Click Schedule.</span></span>
    * <span data-ttu-id="45547-123">ซึ่งนี่จะกำหนดตารางงานคัมบังในรอบระยะเวลาแรกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="45547-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="45547-124">โปรดสังเกตว่างานคัมบังถูกย้ายไปตอนท้ายของรายการเพราะมันถูกเพิ่มไปยังรอบระยะเวลาเริ่มนับจากวันนี้</span><span class="sxs-lookup"><span data-stu-id="45547-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="45547-125">ถ้ารอบระยะเวลานับจากวันนี้ถูกจองจนหมด งานจะถูกย้ายไปรอบระยะเวลาแรกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="45547-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="45547-126">กำหนดตารางงานคัมบังสำหรับวันที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="45547-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="45547-127">ในรายการ ให้เลือกแถว 1</span><span class="sxs-lookup"><span data-stu-id="45547-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="45547-128">คุณจะเห็นได้ว่าแถวแรกนั้นอยู่ในสถานะที่ไม่ได้วางแผนไว้ในฟิลด์สถานะงาน</span><span class="sxs-lookup"><span data-stu-id="45547-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="45547-129">ในรายการ ให้เลือกแถว 2</span><span class="sxs-lookup"><span data-stu-id="45547-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="45547-130">คุณจะเห็นได้ว่าแถวที่สองนั้นอยู่ในสถานะที่ไม่ได้วางแผนไว้ในฟิลด์สถานะงาน </span><span class="sxs-lookup"><span data-stu-id="45547-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="45547-131">ตอนนี้คุณได้ทำการเลือกสองงานแรกไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="45547-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="45547-132">คลิก กำหนดเวลาจากวันที่ เพื่อเปิดกล่องโต้ตอบดรอป</span><span class="sxs-lookup"><span data-stu-id="45547-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="45547-133">ทำเครื่องหมายเลือกหรือเอาเครื่องหมายเลือกออกจากกล่องแทนที่การตอบสนองต่อภาวะกำลังการผลิตไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="45547-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="45547-134">ตัวเลือกนี้จะอนุญาตให้คุณสามารถแทนที่การตอบสนองต่อภาวะกำลังการผลิตไม่เพียงพอตั้งต้น</span><span class="sxs-lookup"><span data-stu-id="45547-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="45547-135">ในฟิลด์การตอบสนองต่อภาวะกำลังการผลิต เลือก 'เพิ่มไปยังรอบระยะเวลาที่ร้องขอไว้'</span><span class="sxs-lookup"><span data-stu-id="45547-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="45547-136">ตัวเลือกนี้จะทำให้แน่ใจว่างานได้ถูกเพิ่มไปยังรอบระยะเวลาที่ร้องขอไว้ โดยไม่คำนึงถึงว่าเซลล์ทำงานอาจมีการโอเวอร์โหลด</span><span class="sxs-lookup"><span data-stu-id="45547-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="45547-137">คลิก กำหนดเวลางาน</span><span class="sxs-lookup"><span data-stu-id="45547-137">Click Schedule.</span></span>
    * <span data-ttu-id="45547-138">โปรดสังเกตว่างานทั้งสองถูกเพิ่มไปยังรอบระยะเวลาที่ต้องการแล้ว</span><span class="sxs-lookup"><span data-stu-id="45547-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="45547-139">ในส่วนรอบระยะเวลากำลังการผลิต คุณสามารถดูจำนวนงานในศูนย์การผลิตสำหรับแต่ละรอบระยะเวลาได้</span><span class="sxs-lookup"><span data-stu-id="45547-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="45547-140">ฟิลด์ปริมาณการใช้จะแสดงปริมาณการใช้วัสดุที่จัดกำหนดการไว้ในรอบระยะเวลานี้ </span><span class="sxs-lookup"><span data-stu-id="45547-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="45547-141">ถ้าปริมาณการใช้วัสดุที่จัดกำหนดการไว้สูงกว่ากำลังการผลิตที่พร้อมใช้งานในรอบระยะเวลานี้ ปริมาณการใช้วัสดุที่โอเวอร์โหลดจะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="45547-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  


