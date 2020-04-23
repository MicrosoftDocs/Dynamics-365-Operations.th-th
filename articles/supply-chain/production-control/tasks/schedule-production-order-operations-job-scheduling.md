---
title: กำหนดเวลาใบสั่งผลิตที่มีการจัดตารางการผลิตระดับการดำเนินงานและระดับงาน
description: หัวข้อนี้มุ่งเน้นการจัดกำหนดการใบสั่งผลิตด้วยการจัดกำหนดการดำเนินงานและการจัดกำหนดการงาน
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a69339bc678de8343dbf2646a4d6fe0ace9964c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210490"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="7e36d-103">กำหนดเวลาใบสั่งผลิตที่มีการจัดตารางการผลิตระดับการดำเนินงานและระดับงาน</span><span class="sxs-lookup"><span data-stu-id="7e36d-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e36d-104">หัวข้อนี้มุ่งเน้นการจัดกำหนดการใบสั่งผลิตด้วยการจัดกำหนดการดำเนินงานและการจัดกำหนดการงาน</span><span class="sxs-lookup"><span data-stu-id="7e36d-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="7e36d-105">จะไม่มีการสร้างงานด้วยการจัดตารางการผลิตระดับการดำเนินงาน แต่งานจะถูกสร้างขึ้นด้วยการจัดตารางการผลิตระดับงาน</span><span class="sxs-lookup"><span data-stu-id="7e36d-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="7e36d-106">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="7e36d-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="7e36d-107">กระบวนงานนี้มีไว้สำหรับผู้จัดการฝ่ายผลิต ผู้วางแผนการผลิต หรือหัวหน้างานฝ่ายผลิตที่ทำงานในสภาพแวดล้อมการผลิตที่ไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="7e36d-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="7e36d-108">สร้างใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="7e36d-108">Create a production order</span></span>
1. <span data-ttu-id="7e36d-109">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7e36d-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="7e36d-110">เลือก **ใบสั่งผลิตใหม่**</span><span class="sxs-lookup"><span data-stu-id="7e36d-110">Select **New production order**.</span></span>
3. <span data-ttu-id="7e36d-111">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7e36d-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="7e36d-112">เลือกหมายเลขสินค้า **D0001**</span><span class="sxs-lookup"><span data-stu-id="7e36d-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="7e36d-113">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7e36d-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="7e36d-114">กำหนดเวลาการดำเนินงานสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="7e36d-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="7e36d-115">ทำเครื่องหมายแถวที่สร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="7e36d-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="7e36d-116">บนบานหน้าต่างการดำเนินการ เลือก **กำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="7e36d-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="7e36d-117">เลือก **จัดกำหนดการดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="7e36d-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="7e36d-118">ในฟิลด์ **คำสั่งการจัดกำหนดการ** เลือก **ไปข้างหน้าจากวันที่จัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="7e36d-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="7e36d-119">ในฟิลด์ **วันที่จัดกำหนดการ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="7e36d-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="7e36d-120">เลือกวันที่ในอนาคต ตัวอย่างเช่น วันนี้บวกอีกหนึ่งสัปดาห์ </span><span class="sxs-lookup"><span data-stu-id="7e36d-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="7e36d-121">ด้วยคำสั่งการจัดกำหนดการที่เลือก สามารถจัดกำหนดการใบสั่งผลิตไปข้างหน้านับจากวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="7e36d-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="7e36d-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7e36d-122">Select **OK**.</span></span>
7. <span data-ttu-id="7e36d-123">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7e36d-123">In the list, mark the selected row.</span></span> <span data-ttu-id="7e36d-124">โปรดทราบว่าสถานะจะถูกเปลี่ยนเป็น **จัดกำหนดการแล้ว**</span><span class="sxs-lookup"><span data-stu-id="7e36d-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="7e36d-125">เลือก **งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7e36d-125">Select **All jobs**.</span></span> <span data-ttu-id="7e36d-126">โปรดทราบว่าไม่มีการสร้างงานขึ้นด้วยการจัดตารางการผลิตระดับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="7e36d-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="7e36d-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7e36d-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="7e36d-128">กำหนดเวลางานสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="7e36d-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="7e36d-129">บนบานหน้าต่างการดำเนินการ เลือก **กำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="7e36d-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="7e36d-130">เลือก **จัดกำหนดการงาน**</span><span class="sxs-lookup"><span data-stu-id="7e36d-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="7e36d-131">ในฟิลด์ **คำสั่งการจัดกำหนดการ** เลือก **ไปข้างหน้าจากวันที่จัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="7e36d-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="7e36d-132">ในฟิลด์ **วันที่จัดกำหนดการ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="7e36d-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="7e36d-133">เลือกวันที่ในอนาคต ตัวอย่างเช่น วันนี้บวกอีกหนึ่งสัปดาห์ </span><span class="sxs-lookup"><span data-stu-id="7e36d-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="7e36d-134">ด้วยคำสั่งการจัดกำหนดการที่เลือก สามารถจัดกำหนดการใบสั่งผลิตไปข้างหน้านับจากวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="7e36d-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="7e36d-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7e36d-135">Select **OK**.</span></span>
6. <span data-ttu-id="7e36d-136">ในบานหน้าต่างการดำเนินการ เลือก **ใบสั่งผลิต**</span><span class="sxs-lookup"><span data-stu-id="7e36d-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="7e36d-137">เลือก **งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7e36d-137">Select **All jobs**.</span></span> <span data-ttu-id="7e36d-138">โปรดทราบว่ามีการสร้างงานขึ้น 5 รายการที่มีการจัดตารางการผลิตระดับงานตามกระบวนการผลิตที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="7e36d-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

