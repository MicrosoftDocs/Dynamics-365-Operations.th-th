--- 
title: "ย้ายงานคัมบังที่จัดกำหนด"
description: "ขั้นตอนนี้มุ่งเน้นไปที่การย้ายกระบวนงานคัมบังที่วางแผนไว้แล้วไปยังรอบระยะเวลาอื่น "
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="31d55-103">ย้ายงานคัมบังที่จัดกำหนด</span><span class="sxs-lookup"><span data-stu-id="31d55-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31d55-104">ขั้นตอนนี้มุ่งเน้นไปที่การย้ายกระบวนงานคัมบังที่วางแผนไว้แล้วไปยังรอบระยะเวลาอื่น </span><span class="sxs-lookup"><span data-stu-id="31d55-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="31d55-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="31d55-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="31d55-106">ขั้นตอนนี้มีไว้สำหรับหัวหน้างานผลิตหรือนักวางแผนการผลิตที่ทำงานกับคัมบัง</span><span class="sxs-lookup"><span data-stu-id="31d55-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="31d55-107">เลือก งานคัมบังที่จัดกำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="31d55-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="31d55-108">Gå til Produktionsstyring > คัมบัง > Tidsplanlægning-งานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="31d55-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="31d55-109">!MtCMR!ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="31d55-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="31d55-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="31d55-110">áçêìõý !</span></span>
3. <span data-ttu-id="31d55-111">Markér den valgte række på ฟัง</span><span class="sxs-lookup"><span data-stu-id="31d55-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="31d55-112">เลือกเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="31d55-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="31d55-113">คลิก เลือก</span><span class="sxs-lookup"><span data-stu-id="31d55-113">Klik på Select.</span></span>
5. <span data-ttu-id="31d55-114">Vælg 'Planlagt' feltet แสดงสถานะของงาน</span><span class="sxs-lookup"><span data-stu-id="31d55-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="31d55-115">ซึ่งนี่จะกรองรายการงานเพื่อแสดงเฉพาะงานคัมบังที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="31d55-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="31d55-116">ย้ายงานคัมบังไปยังรอบระยะเวลาอื่น</span><span class="sxs-lookup"><span data-stu-id="31d55-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="31d55-117">ค้นหา vælg den ønskede ไปรษณีย์ på ฟัง</span><span class="sxs-lookup"><span data-stu-id="31d55-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="31d55-118">เลือกงานที่มีสถานะงานที่วางแผนไว้ ตัวอย่างเช่น งานที่จัดกำหนดการไว้ในวันที่ 20 ธันวาคม 2012 ในฟิลด์รอบระยะเวลาที่วางแผนไว้ </span><span class="sxs-lookup"><span data-stu-id="31d55-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="31d55-119">จากนั้นย้ายงานไปยังรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="31d55-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="31d55-120">คลิก รอบระยะเวลาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="31d55-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="31d55-121">คลิก สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="31d55-121">Klik på End.</span></span>
    * <span data-ttu-id="31d55-122">นี่จะย้ายงานไปตอนท้ายของรายการงานเหมือนงานล่าสุดในรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="31d55-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="31d55-123">ค้นหา vælg den ønskede ไปรษณีย์ på ฟัง</span><span class="sxs-lookup"><span data-stu-id="31d55-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="31d55-124">เลือกงานที่มีสถานะงานที่วางแผนไว้ ตัวอย่างเช่น งานที่จัดกำหนดการไว้ในวันที่ 18 ธันวาคม 2012 ในฟิลด์รอบระยะเวลาที่วางแผนไว้ </span><span class="sxs-lookup"><span data-stu-id="31d55-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="31d55-125">จากนั้นย้ายงานไปยังรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="31d55-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="31d55-126">คลิก รอบระยะเวลาถัดไป</span><span class="sxs-lookup"><span data-stu-id="31d55-126">Klik på Next period.</span></span>
6. <span data-ttu-id="31d55-127">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="31d55-127">Klik på Start.</span></span>
    * <span data-ttu-id="31d55-128">นี่จะย้ายงานไปตอนต้นของรายการงานเหมือนงานแรกในรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="31d55-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="31d55-129">งาน: ย้ายงานภายในรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="31d55-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="31d55-130">ค้นหา vælg den ønskede ไปรษณีย์ på ฟัง</span><span class="sxs-lookup"><span data-stu-id="31d55-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="31d55-131">เลือกงานที่มีสถานะงานที่วางแผนไว้ ตัวอย่างเช่น งานที่สองที่จัดกำหนดการไว้ในวันที่ 19 ธันวาคม 2012 ในฟิลด์รอบระยะเวลาที่วางแผนไว้ </span><span class="sxs-lookup"><span data-stu-id="31d55-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="31d55-132">จากนั้นย้ายงานภายในรอบระยะเวลาที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="31d55-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="31d55-133">คลิก ไปหน้า</span><span class="sxs-lookup"><span data-stu-id="31d55-133">Klik på Forward.</span></span>
    * <span data-ttu-id="31d55-134">ให้สังเกตว่างานถูกย้ายลงไปหนึ่งบรรทัดในรายการ</span><span class="sxs-lookup"><span data-stu-id="31d55-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="31d55-135">คลิก ย้อนหลัง</span><span class="sxs-lookup"><span data-stu-id="31d55-135">Klik på Backward.</span></span>
    * <span data-ttu-id="31d55-136">ให้สังเกตว่างานถูกย้ายขึ้นไปหนึ่งบรรทัดในรายการ</span><span class="sxs-lookup"><span data-stu-id="31d55-136">Notice that the job is moved one line up on the list.</span></span>  


