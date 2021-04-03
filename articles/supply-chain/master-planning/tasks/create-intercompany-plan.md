---
title: จัดทำแผนระหว่างบริษัท
description: 'กระบวนงานนี้แสดงวิธีการสร้างแผนระหว่างบริษัท '
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b64ababa618d58feb6095704e5978295060c96f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261128"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="29a7b-103">จัดทำแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="29a7b-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29a7b-104">กระบวนงานนี้แสดงวิธีการสร้างแผนระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="29a7b-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="29a7b-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="29a7b-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="29a7b-106">ตั้งค่ากลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="29a7b-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="29a7b-107">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การวางแผนหลัก >** การตั้งค่า > กลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="29a7b-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="29a7b-108">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="29a7b-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="29a7b-109">เช่น กรองข้อมูลในฟิลด์รายชื่อด้วยค่า 10</span><span class="sxs-lookup"><span data-stu-id="29a7b-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="29a7b-110">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="29a7b-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="29a7b-111">คลิก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="29a7b-111">Click **Delete**.</span></span> <span data-ttu-id="29a7b-112">ขั้นตอนนี้เป็นสิ่งจำเป็นในการทำให้การรันการวางแผนระหว่างบริษัทสั้นลง </span><span class="sxs-lookup"><span data-stu-id="29a7b-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="29a7b-113">การวางแผนระหว่างบริษัทจะรันการวางแผนหลักในบริษัททั้งหมดในกลุ่มการวางแผน โดยเริ่มจากลำดับการวางผังงานต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="29a7b-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="29a7b-114">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="29a7b-114">Click **Yes**.</span></span>
6. <span data-ttu-id="29a7b-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="29a7b-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="29a7b-116">จัดทำแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="29a7b-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="29a7b-117">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การวางแผนหลัก > พื้นที่ทำงาน > การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="29a7b-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="29a7b-118">คลิก **การวางแผนหลักระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="29a7b-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="29a7b-119">ในฟิลด์ **กลุ่มการวางแผนระหว่างบริษัท** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="29a7b-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="29a7b-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="29a7b-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="29a7b-121">เลือกกลุ่มการวางแผนระหว่างบริษัท 10</span><span class="sxs-lookup"><span data-stu-id="29a7b-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="29a7b-122">ในฟิลด์ **จำนวนของการเกิดซ้ำสำหรับการวางแผนระหว่างบริษัท** ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="29a7b-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="29a7b-123">กลุ่มการวางแผนระหว่างบริษัท 10 มีสมาชิกสองราย</span><span class="sxs-lookup"><span data-stu-id="29a7b-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="29a7b-124">เพื่อถ่ายทอดความล่าช้าจากบริษัทต้นทาง (USMF) ไปยังบริษัทลูกค้า (DEMF) คุณจะต้องรันระบบระหว่างบริษัทในทั้งสองบริษัทสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="29a7b-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="29a7b-125">การเกิดซ้ำครั้งแรกจะถ่ายทอดความต้องการและระบุความล่าช้าในบริษัทต้นทาง (USMF)</span><span class="sxs-lookup"><span data-stu-id="29a7b-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="29a7b-126">การเกิดซ้ำครั้งที่สองจะถ่ายทอดความล่าช้าจาก USMF ไปยัง DEMF</span><span class="sxs-lookup"><span data-stu-id="29a7b-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="29a7b-127">ในฟิลด์ **การเกิดซ้ำครั้งแรก** ให้เลือก 'การสร้างใหม่'</span><span class="sxs-lookup"><span data-stu-id="29a7b-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="29a7b-128">ในฟิลด์ **การเกิดซ้ำลำดับต่อมา** ให้เลือก 'การสร้างใหม่'</span><span class="sxs-lookup"><span data-stu-id="29a7b-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="29a7b-129">ในฟิลด์ **จำนวนของเธรด** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="29a7b-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="29a7b-130">ซึ่งแสดงถึงจำนวนเธรดคู่ขนานที่ใช้สำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="29a7b-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="29a7b-131">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="29a7b-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="29a7b-132">ดูผลลัพธ์ของแผน</span><span class="sxs-lookup"><span data-stu-id="29a7b-132">View the result of the plan</span></span>
1. <span data-ttu-id="29a7b-133">ในฟิลด์ **แผน** ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="29a7b-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="29a7b-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="29a7b-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="29a7b-135">คลิกลิงค์สำหรับ StaticPlan </span><span class="sxs-lookup"><span data-stu-id="29a7b-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="29a7b-136">คุณจำเป็นต้องอยู่ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="29a7b-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="29a7b-137">คลิก **แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="29a7b-137">Click **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]