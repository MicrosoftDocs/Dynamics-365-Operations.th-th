---
title: จัดทำแผนระหว่างบริษัท
description: 'กระบวนงานนี้แสดงวิธีการสร้างแผนระหว่างบริษัท '
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867361"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="4fec9-103">จัดทำแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fec9-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fec9-104">กระบวนงานนี้แสดงวิธีการสร้างแผนระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="4fec9-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="4fec9-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="4fec9-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="4fec9-106">ตั้งค่ากลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fec9-106">Set up an intercompany planning group</span></span>

1. <span data-ttu-id="4fec9-107">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การวางแผนหลัก >** การตั้งค่า > กลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fec9-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="4fec9-108">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="4fec9-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4fec9-109">เช่น กรองข้อมูลในฟิลด์รายชื่อด้วยค่า 10</span><span class="sxs-lookup"><span data-stu-id="4fec9-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="4fec9-110">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4fec9-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4fec9-111">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="4fec9-111">Select **Delete**.</span></span> <span data-ttu-id="4fec9-112">ขั้นตอนนี้เป็นสิ่งจำเป็นในการทำให้การรันการวางแผนระหว่างบริษัทสั้นลง </span><span class="sxs-lookup"><span data-stu-id="4fec9-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="4fec9-113">การวางแผนระหว่างบริษัทจะรันการวางแผนหลักในบริษัททั้งหมดในกลุ่มการวางแผน โดยเริ่มจากลำดับการวางผังงานต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="4fec9-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="4fec9-114">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4fec9-114">Select **Yes**.</span></span>
6. <span data-ttu-id="4fec9-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4fec9-115">Close the page.</span></span>

## <a name="create-an-intercompany-master-plan"></a><span data-ttu-id="4fec9-116">จัดทำแผนหลักระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fec9-116">Create an intercompany master plan</span></span>

1. <span data-ttu-id="4fec9-117">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การวางแผนหลัก > พื้นที่ทำงาน > การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="4fec9-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="4fec9-118">เลือก **การวางแผนหลักระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="4fec9-118">Select **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="4fec9-119">ในฟิลด์ **กลุ่มการวางแผนระหว่างบริษัท** ให้เลือกปุ่มแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4fec9-119">In the **Intercompany planning group** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4fec9-120">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4fec9-120">In the list, select the link in the selected row.</span></span> <span data-ttu-id="4fec9-121">เลือกกลุ่มการวางแผนระหว่างบริษัท 10</span><span class="sxs-lookup"><span data-stu-id="4fec9-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="4fec9-122">ในฟิลด์ **จำนวนของการเกิดซ้ำสำหรับการวางแผนระหว่างบริษัท** ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="4fec9-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="4fec9-123">กลุ่มการวางแผนระหว่างบริษัท 10 มีสมาชิกสองราย</span><span class="sxs-lookup"><span data-stu-id="4fec9-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="4fec9-124">เพื่อถ่ายทอดความล่าช้าจากบริษัทต้นทาง (USMF) ไปยังบริษัทลูกค้า (DEMF) คุณจะต้องรันระบบระหว่างบริษัทในทั้งสองบริษัทสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="4fec9-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="4fec9-125">การเกิดซ้ำครั้งแรกจะถ่ายทอดความต้องการและระบุความล่าช้าในบริษัทต้นทาง (USMF)</span><span class="sxs-lookup"><span data-stu-id="4fec9-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="4fec9-126">การเกิดซ้ำครั้งที่สองจะถ่ายทอดความล่าช้าจาก USMF ไปยัง DEMF</span><span class="sxs-lookup"><span data-stu-id="4fec9-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="4fec9-127">ในฟิลด์ **การเกิดซ้ำครั้งแรก** ให้เลือก 'การสร้างใหม่'</span><span class="sxs-lookup"><span data-stu-id="4fec9-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="4fec9-128">ในฟิลด์ **การเกิดซ้ำลำดับต่อมา** ให้เลือก 'การสร้างใหม่'</span><span class="sxs-lookup"><span data-stu-id="4fec9-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="4fec9-129">ในฟิลด์ **จำนวนของเธรด** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="4fec9-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="4fec9-130">ซึ่งแสดงถึงจำนวนเธรดคู่ขนานที่ใช้สำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4fec9-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="4fec9-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4fec9-131">Select **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="4fec9-132">ดูผลลัพธ์ของแผน</span><span class="sxs-lookup"><span data-stu-id="4fec9-132">View the result of the plan</span></span>

1. <span data-ttu-id="4fec9-133">ในฟิลด์ **แผน** ให้เลือกปุ่มแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4fec9-133">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="4fec9-134">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4fec9-134">In the list, select the link in the selected row.</span></span> <span data-ttu-id="4fec9-135">เลือกลิงค์สำหรับ StaticPlan</span><span class="sxs-lookup"><span data-stu-id="4fec9-135">Select the link for StaticPlan.</span></span> <span data-ttu-id="4fec9-136">คุณจำเป็นต้องอยู่ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="4fec9-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="4fec9-137">เลือก **แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="4fec9-137">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]