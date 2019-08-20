---
title: ย้ายงานคัมบังที่จัดกำหนด
description: 'ขั้นตอนนี้มุ่งเน้นไปที่การย้ายกระบวนงานคัมบังที่วางแผนไว้แล้วไปยังรอบระยะเวลาอื่น '
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2526c2bd106e35c736e930b5b5114d019718dc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836251"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="386f6-103">ย้ายงานคัมบังที่จัดกำหนด</span><span class="sxs-lookup"><span data-stu-id="386f6-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="386f6-104">ขั้นตอนนี้มุ่งเน้นไปที่การย้ายกระบวนงานคัมบังที่วางแผนไว้แล้วไปยังรอบระยะเวลาอื่น </span><span class="sxs-lookup"><span data-stu-id="386f6-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="386f6-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="386f6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="386f6-106">ขั้นตอนนี้มีไว้สำหรับหัวหน้างานผลิตหรือนักวางแผนการผลิตที่ทำงานกับคัมบัง</span><span class="sxs-lookup"><span data-stu-id="386f6-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="386f6-107">เลือกงานคัมบังที่จัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="386f6-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="386f6-108">ไปที่ **การควบคุมการผลิต > คัมบัง > การกำหนดการงานคัมบัง**</span><span class="sxs-lookup"><span data-stu-id="386f6-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="386f6-109">ในฟิลด์ **เซลล์ทำงาน** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="386f6-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="386f6-110">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="386f6-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="386f6-111">เลือกเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="386f6-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="386f6-112">คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="386f6-112">Click **Select**.</span></span> 

5. <span data-ttu-id="386f6-113">ในฟิลด์ **แสดงสถานะงาน** เลือก **จัดกำหนดการแล้ว**</span><span class="sxs-lookup"><span data-stu-id="386f6-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="386f6-114">ซึ่งนี่จะกรองรายการงานเพื่อแสดงเฉพาะงานคัมบังที่จัดกำหนดการไว้</span><span class="sxs-lookup"><span data-stu-id="386f6-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="386f6-115">ย้ายงานคัมบังไปยังรอบระยะเวลาอื่น</span><span class="sxs-lookup"><span data-stu-id="386f6-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="386f6-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="386f6-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="386f6-117">เลือกงานที่มีสถานะ **งานที่วางแผนไว้** ตัวอย่างเช่น งานที่จัดกำหนดการไว้ในวันที่ 20 ธันวาคม 2012 ในฟิลด์ **รอบระยะเวลาที่วางแผนไว้**</span><span class="sxs-lookup"><span data-stu-id="386f6-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="386f6-118">จากนั้นย้ายงานไปยังรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="386f6-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="386f6-119">คลิก **รอบระยะเวลาก่อนหน้านี้**</span><span class="sxs-lookup"><span data-stu-id="386f6-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="386f6-120">คลิก **สิ้นสุด** เพื่อย้ายงานไปตอนท้ายของรายการงาน เหมือนงานล่าสุดในรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="386f6-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="386f6-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="386f6-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="386f6-122">เลือกงานที่มีสถานะ **งานที่วางแผนไว้** ตัวอย่างเช่น งานที่จัดกำหนดการไว้ในวันที่ 18 ธันวาคม 2012 ในฟิลด์ **รอบระยะเวลาที่วางแผนไว้**</span><span class="sxs-lookup"><span data-stu-id="386f6-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="386f6-123">จากนั้นย้ายงานไปยังรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="386f6-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="386f6-124">คลิก **รอบระยะเวลาถัดไป**</span><span class="sxs-lookup"><span data-stu-id="386f6-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="386f6-125">คลิก **เริ่มต้น** เพื่อย้ายงานไปตอนต้นของรายการงาน เหมือนงานแรกในรอบระยะเวลาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="386f6-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="386f6-126">ย้ายงานภายในรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="386f6-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="386f6-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="386f6-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="386f6-128">เลือกงานที่มีสถานะงานที่วางแผนไว้ ตัวอย่างเช่น งานที่สองที่จัดกำหนดการไว้ในวันที่ 19 ธันวาคม 2012 ในฟิลด์ **รอบระยะเวลาที่วางแผนไว้**</span><span class="sxs-lookup"><span data-stu-id="386f6-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="386f6-129">จากนั้นย้ายงานภายในรอบระยะเวลาที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="386f6-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="386f6-130">คลิก **ไปข้างหน้า**</span><span class="sxs-lookup"><span data-stu-id="386f6-130">Click **Forward**.</span></span> <span data-ttu-id="386f6-131">ให้สังเกตว่างานถูกย้ายลงไปหนึ่งบรรทัดในรายการ</span><span class="sxs-lookup"><span data-stu-id="386f6-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="386f6-132">คลิก **ย้อนหลัง**</span><span class="sxs-lookup"><span data-stu-id="386f6-132">Click **Backward**.</span></span> <span data-ttu-id="386f6-133">ให้สังเกตว่างานถูกย้ายขึ้นไปหนึ่งบรรทัดในรายการ</span><span class="sxs-lookup"><span data-stu-id="386f6-133">Notice that the job is moved one line up on the list.</span></span>
