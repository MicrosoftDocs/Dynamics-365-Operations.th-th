---
title: จัดทำแผนระหว่างบริษัท
description: 'กระบวนงานนี้แสดงวิธีการสร้างแผนระหว่างบริษัท '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 194bb78eed5a673030f7cead031cf286cddbe77c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845220"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="22ab1-103">จัดทำแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="22ab1-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22ab1-104">กระบวนงานนี้แสดงวิธีการสร้างแผนระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="22ab1-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="22ab1-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="22ab1-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="22ab1-106">ตั้งค่ากลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="22ab1-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="22ab1-107">ไปที่กลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="22ab1-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="22ab1-108">การวางแผนหลัก > การตั้งค่า > กลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="22ab1-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="22ab1-109">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="22ab1-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="22ab1-110">เช่น กรองข้อมูลในฟิลด์รายชื่อด้วยค่า 10</span><span class="sxs-lookup"><span data-stu-id="22ab1-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="22ab1-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="22ab1-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="22ab1-112">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="22ab1-112">Click Delete.</span></span>
    * <span data-ttu-id="22ab1-113">ขั้นตอนนี้เป็นสิ่งจำเป็นในการทำให้การรันการวางแผนระหว่างบริษัทสั้นลง </span><span class="sxs-lookup"><span data-stu-id="22ab1-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="22ab1-114">การวางแผนระหว่างบริษัทจะรันการวางแผนหลักในบริษัททั้งหมดในกลุ่มการวางแผน โดยเริ่มจากลำดับการวางผังงานต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="22ab1-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="22ab1-115">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="22ab1-115">Click Yes.</span></span>
6. <span data-ttu-id="22ab1-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="22ab1-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="22ab1-117">จัดทำแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="22ab1-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="22ab1-118">คลิก การวางแผนหลักระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="22ab1-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="22ab1-119">รายการนี้อยู่ในพื้นที่ทำงานการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="22ab1-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="22ab1-120">ในฟิลด์กลุ่มการวางแผนระหว่างบริษัท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="22ab1-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="22ab1-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="22ab1-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="22ab1-122">เลือกกลุ่มการวางแผนระหว่างบริษัท 10</span><span class="sxs-lookup"><span data-stu-id="22ab1-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="22ab1-123">ในฟิลด์จำนวนของการเกิดซ้ำสำหรับการวางแผนระหว่างบริษัท ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="22ab1-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="22ab1-124">กลุ่มการวางแผนระหว่างบริษัท 10 มีสมาชิกสองราย</span><span class="sxs-lookup"><span data-stu-id="22ab1-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="22ab1-125">เพื่อถ่ายทอดความล่าช้าจากบริษัทต้นทาง (USMF) ไปยังบริษัทลูกค้า (DEMF) คุณจะต้องรันระบบระหว่างบริษัทในทั้งสองบริษัทสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="22ab1-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="22ab1-126">การเกิดซ้ำครั้งแรกจะถ่ายทอดความต้องการและระบุความล่าช้าในบริษัทต้นทาง (USMF)</span><span class="sxs-lookup"><span data-stu-id="22ab1-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="22ab1-127">การเกิดซ้ำครั้งที่สองจะถ่ายทอดความล่าช้าจาก USMF ไปยัง DEMF</span><span class="sxs-lookup"><span data-stu-id="22ab1-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="22ab1-128">ในฟิลด์การเกิดซ้ำครั้งแรก ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="22ab1-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="22ab1-129">ในฟิลด์การเกิดซ้ำครั้งแรก ให้เลือก 'การสร้างใหม่'</span><span class="sxs-lookup"><span data-stu-id="22ab1-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="22ab1-130">ในฟิลด์การเกิดซ้ำลำดับต่อมา ให้เลือก 'การสร้างใหม่'</span><span class="sxs-lookup"><span data-stu-id="22ab1-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="22ab1-131">ในฟิลด์จำนวนของเธรด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="22ab1-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="22ab1-132">ซึ่งแสดงถึงจำนวนเธรดคู่ขนานที่ใช้สำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="22ab1-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="22ab1-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="22ab1-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="22ab1-134">ดูผลลัพธ์ของแผน</span><span class="sxs-lookup"><span data-stu-id="22ab1-134">View the result of the plan</span></span>
1. <span data-ttu-id="22ab1-135">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="22ab1-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="22ab1-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="22ab1-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="22ab1-137">คลิกลิงค์สำหรับ StaticPlan </span><span class="sxs-lookup"><span data-stu-id="22ab1-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="22ab1-138">คุณจำเป็นต้องอยู่ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="22ab1-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="22ab1-139">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="22ab1-139">Click Planned orders.</span></span>

