---
title: กำหนดเวลาใบสั่งผลิตที่มีการจัดตารางการผลิตระดับการดำเนินงานและระดับงาน
description: 'กระบวนงานนี้มุ่งเน้นการจัดกำหนดการใบสั่งผลิตด้วยการจัดตารางการผลิตระดับการดำเนินงานและการจัดตารางการผลิตระดับงาน '
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2019
ms.locfileid: "352470"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="1c636-103">กำหนดเวลาใบสั่งผลิตที่มีการจัดตารางการผลิตระดับการดำเนินงานและระดับงาน</span><span class="sxs-lookup"><span data-stu-id="1c636-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c636-104">กระบวนงานนี้มุ่งเน้นการจัดกำหนดการใบสั่งผลิตด้วยการจัดตารางการผลิตระดับการดำเนินงานและการจัดตารางการผลิตระดับงาน </span><span class="sxs-lookup"><span data-stu-id="1c636-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="1c636-105">จะไม่มีการสร้างงานด้วยการจัดตารางการผลิตระดับการดำเนินงาน แต่งานจะถูกสร้างขึ้นด้วยการจัดตารางการผลิตระดับงาน</span><span class="sxs-lookup"><span data-stu-id="1c636-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="1c636-106">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="1c636-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="1c636-107">กระบวนงานนี้มีไว้สำหรับผู้จัดการฝ่ายผลิต ผู้วางแผนการผลิต หรือหัวหน้างานฝ่ายผลิตที่ทำงานในสภาพแวดล้อมการผลิตที่ไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="1c636-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="1c636-108">สร้างใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="1c636-108">Create a production order</span></span>
1. <span data-ttu-id="1c636-109">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="1c636-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="1c636-110">คลิกใบสั่งผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="1c636-110">Click New production order.</span></span>
3. <span data-ttu-id="1c636-111">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1c636-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="1c636-112">เลือกหมายเลขสินค้า D0001 </span><span class="sxs-lookup"><span data-stu-id="1c636-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="1c636-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1c636-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="1c636-114">กำหนดเวลาการดำเนินงานสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="1c636-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="1c636-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1c636-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1c636-116">เลือกใบสั่งผลิตที่คุณเพิ่งสร้าง </span><span class="sxs-lookup"><span data-stu-id="1c636-116">Select the production order that you have just created.</span></span> <span data-ttu-id="1c636-117">ซึ่งควรอยู่ที่ด้านบนของรายการ</span><span class="sxs-lookup"><span data-stu-id="1c636-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="1c636-118">ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="1c636-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="1c636-119">คลิกกำหนดเวลาการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="1c636-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="1c636-120">ในฟิลด์คำสั่งการกำหนดเวลา เลือก 'ไปข้างหน้าจากวันที่กำหนดเวลาไว้'</span><span class="sxs-lookup"><span data-stu-id="1c636-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="1c636-121">ในฟิลด์วันที่กำหนดเวลาการดำเนินงาน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="1c636-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="1c636-122">เลือกวันที่ในอนาคต ตัวอย่างเช่น วันนี้บวกอีกหนึ่งสัปดาห์ </span><span class="sxs-lookup"><span data-stu-id="1c636-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="1c636-123">ด้วยคำสั่งการจัดกำหนดการที่เลือก สามารถจัดกำหนดการใบสั่งผลิตไปข้างหน้านับจากวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="1c636-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="1c636-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="1c636-124">Click OK.</span></span>
7. <span data-ttu-id="1c636-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1c636-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1c636-126">โปรดทราบว่าสถานะจะผลิตเปลี่ยนจัดกำหนดการแล้ว</span><span class="sxs-lookup"><span data-stu-id="1c636-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="1c636-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1c636-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1c636-128">คลิกงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1c636-128">Click All jobs.</span></span>
    * <span data-ttu-id="1c636-129">โปรดทราบว่าไม่มีการสร้างงานขึ้นด้วยการจัดตารางการผลิตระดับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="1c636-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="1c636-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1c636-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="1c636-131">กำหนดเวลางานสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="1c636-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="1c636-132">ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="1c636-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="1c636-133">การจัดส่ง กำหนดเวลางาน</span><span class="sxs-lookup"><span data-stu-id="1c636-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="1c636-134">ในฟิลด์คำสั่งการกำหนดเวลา เลือก 'ไปข้างหน้าจากวันที่กำหนดเวลาไว้'</span><span class="sxs-lookup"><span data-stu-id="1c636-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="1c636-135">ในฟิลด์วันที่กำหนดเวลาการดำเนินงาน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="1c636-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="1c636-136">เลือกวันที่ในอนาคต ตัวอย่างเช่น วันนี้บวกอีกหนึ่งสัปดาห์ </span><span class="sxs-lookup"><span data-stu-id="1c636-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="1c636-137">ด้วยคำสั่งการจัดกำหนดการที่เลือก สามารถจัดกำหนดการใบสั่งผลิตไปข้างหน้านับจากวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="1c636-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="1c636-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="1c636-138">Click OK.</span></span>
6. <span data-ttu-id="1c636-139">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="1c636-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="1c636-140">คลิกงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1c636-140">Click All jobs.</span></span>
    * <span data-ttu-id="1c636-141">โปรดทราบว่ามีการสร้างงานขึ้น 5 รายการที่มีการจัดตารางการผลิตระดับงานตามกระบวนการผลิตที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1c636-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

