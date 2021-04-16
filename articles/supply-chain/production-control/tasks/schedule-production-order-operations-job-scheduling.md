---
title: กำหนดเวลาใบสั่งผลิตที่มีการจัดตารางการผลิตระดับการดำเนินงานและระดับงาน
description: หัวข้อนี้มุ่งเน้นการจัดกำหนดการใบสั่งผลิตด้วยการจัดกำหนดการดำเนินงานและการจัดกำหนดการงาน
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841394"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="9f6ad-103">กำหนดเวลาใบสั่งผลิตที่มีการจัดตารางการผลิตระดับการดำเนินงานและระดับงาน</span><span class="sxs-lookup"><span data-stu-id="9f6ad-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f6ad-104">หัวข้อนี้มุ่งเน้นการจัดกำหนดการใบสั่งผลิตด้วยการจัดกำหนดการดำเนินงานและการจัดกำหนดการงาน</span><span class="sxs-lookup"><span data-stu-id="9f6ad-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="9f6ad-105">จะไม่มีการสร้างงานด้วยการจัดตารางการผลิตระดับการดำเนินงาน แต่งานจะถูกสร้างขึ้นด้วยการจัดตารางการผลิตระดับงาน</span><span class="sxs-lookup"><span data-stu-id="9f6ad-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="9f6ad-106">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="9f6ad-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="9f6ad-107">กระบวนงานนี้มีไว้สำหรับผู้จัดการฝ่ายผลิต ผู้วางแผนการผลิต หรือหัวหน้างานฝ่ายผลิตที่ทำงานในสภาพแวดล้อมการผลิตที่ไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="9f6ad-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="9f6ad-108">สร้างใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9f6ad-108">Create a production order</span></span>
1. <span data-ttu-id="9f6ad-109">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="9f6ad-110">เลือก **ใบสั่งผลิตใหม่**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-110">Select **New production order**.</span></span>
3. <span data-ttu-id="9f6ad-111">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9f6ad-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="9f6ad-112">เลือกหมายเลขสินค้า **D0001**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="9f6ad-113">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="9f6ad-114">กำหนดเวลาการดำเนินงานสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9f6ad-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="9f6ad-115">ทำเครื่องหมายแถวที่สร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="9f6ad-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="9f6ad-116">บนบานหน้าต่างการดำเนินการ เลือก **กำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="9f6ad-117">เลือก **จัดกำหนดการดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="9f6ad-118">ในฟิลด์ **คำสั่งการจัดกำหนดการ** เลือก **ไปข้างหน้าจากวันที่จัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="9f6ad-119">ในฟิลด์ **วันที่จัดกำหนดการ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9f6ad-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="9f6ad-120">เลือกวันที่ในอนาคต ตัวอย่างเช่น วันนี้บวกอีกหนึ่งสัปดาห์ </span><span class="sxs-lookup"><span data-stu-id="9f6ad-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="9f6ad-121">ด้วยคำสั่งการจัดกำหนดการที่เลือก สามารถจัดกำหนดการใบสั่งผลิตไปข้างหน้านับจากวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="9f6ad-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="9f6ad-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-122">Select **OK**.</span></span>
7. <span data-ttu-id="9f6ad-123">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9f6ad-123">In the list, mark the selected row.</span></span> <span data-ttu-id="9f6ad-124">โปรดทราบว่าสถานะจะถูกเปลี่ยนเป็น **จัดกำหนดการแล้ว**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="9f6ad-125">เลือก **งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-125">Select **All jobs**.</span></span> <span data-ttu-id="9f6ad-126">โปรดทราบว่าไม่มีการสร้างงานขึ้นด้วยการจัดตารางการผลิตระดับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="9f6ad-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="9f6ad-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9f6ad-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="9f6ad-128">กำหนดเวลางานสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9f6ad-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="9f6ad-129">บนบานหน้าต่างการดำเนินการ เลือก **กำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="9f6ad-130">เลือก **จัดกำหนดการงาน**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="9f6ad-131">ในฟิลด์ **คำสั่งการจัดกำหนดการ** เลือก **ไปข้างหน้าจากวันที่จัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="9f6ad-132">ในฟิลด์ **วันที่จัดกำหนดการ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9f6ad-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="9f6ad-133">เลือกวันที่ในอนาคต ตัวอย่างเช่น วันนี้บวกอีกหนึ่งสัปดาห์ </span><span class="sxs-lookup"><span data-stu-id="9f6ad-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="9f6ad-134">ด้วยคำสั่งการจัดกำหนดการที่เลือก สามารถจัดกำหนดการใบสั่งผลิตไปข้างหน้านับจากวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="9f6ad-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="9f6ad-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-135">Select **OK**.</span></span>
6. <span data-ttu-id="9f6ad-136">ในบานหน้าต่างการดำเนินการ เลือก **ใบสั่งผลิต**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="9f6ad-137">เลือก **งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9f6ad-137">Select **All jobs**.</span></span> <span data-ttu-id="9f6ad-138">โปรดทราบว่ามีการสร้างงานขึ้น 5 รายการที่มีการจัดตารางการผลิตระดับงานตามกระบวนการผลิตที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="9f6ad-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]