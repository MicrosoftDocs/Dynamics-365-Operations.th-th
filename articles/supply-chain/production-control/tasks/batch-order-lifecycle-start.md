--- 
title: "วงจรชีวิตของใบสั่งชุดงานตั้งแต่สร้างจนถึงเริ่มต้น"
description: "ขั้นตอนนี้นำคุณผ่านส่วนแรกของวงจรชีวิตของใบสั่งชุดงาน "
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b04960c0f92e8871e0de99b4ebb0c69e1225d21c
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="882de-103">วงจรชีวิตของใบสั่งชุดงานตั้งแต่สร้างจนถึงเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="882de-103">Batch order lifecycle from create to start</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="882de-104">ขั้นตอนนี้นำคุณผ่านส่วนแรกของวงจรชีวิตของใบสั่งชุดงาน </span><span class="sxs-lookup"><span data-stu-id="882de-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="882de-105">ตั้งแต่การสร้าง การประเมินต้นทุน และการจัดกำหนดการงานการผลิตผ่านการผลิตจำนวนมาก จนถึงการเริ่มต้นใบสั่งชุดงานที่แท้จริง</span><span class="sxs-lookup"><span data-stu-id="882de-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="882de-106">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="882de-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="882de-107">ข้อกำหนดเบื้องต้นสำหรับการรันขั้นตอนด้วยชุดข้อมูลอื่นเป็นผลิตภัณฑ์นำออกใช้ มีเวอร์ชันสูตรและกระบวนการผลิตใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="882de-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="882de-108">สร้างใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="882de-108">Create a batch order</span></span>
1. <span data-ttu-id="882de-109">ไปที่ ใบสั่งผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="882de-109">Go to All production orders.</span></span>
2. <span data-ttu-id="882de-110">คลิกใบสั่งชุดงานใหม่</span><span class="sxs-lookup"><span data-stu-id="882de-110">Click New batch order.</span></span>
3. <span data-ttu-id="882de-111">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="882de-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="882de-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="882de-112">Click Create.</span></span>
5. <span data-ttu-id="882de-113">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์การผลิต ด้วยค่า 'b'</span><span class="sxs-lookup"><span data-stu-id="882de-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="882de-114">ดูสูตรการผลิตและสินค้าร่วมที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="882de-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="882de-115">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="882de-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="882de-116">คลิกสูตร</span><span class="sxs-lookup"><span data-stu-id="882de-116">Click Formula.</span></span>
3. <span data-ttu-id="882de-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-117">Close the page.</span></span>
4. <span data-ttu-id="882de-118">คลิกผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="882de-118">Click Co-products.</span></span>
5. <span data-ttu-id="882de-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="882de-120">ประเมินใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="882de-120">Estimate the batch order</span></span>
1. <span data-ttu-id="882de-121">คลิกประเมิน </span><span class="sxs-lookup"><span data-stu-id="882de-121">Click Estimate.</span></span>
2. <span data-ttu-id="882de-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="882de-122">Click OK.</span></span>
3. <span data-ttu-id="882de-123">ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="882de-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="882de-124">คลิกดูรายละเอียดการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="882de-124">Click View calculation details.</span></span>
5. <span data-ttu-id="882de-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="882de-126">นำออกใช้ใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="882de-126">Release the batch order</span></span>
1. <span data-ttu-id="882de-127">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="882de-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="882de-128">คลิก นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="882de-128">Click Release.</span></span>
3. <span data-ttu-id="882de-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="882de-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="882de-130">กำหนดการของงานการผลิต</span><span class="sxs-lookup"><span data-stu-id="882de-130">Schedule production jobs</span></span>
1. <span data-ttu-id="882de-131">ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="882de-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="882de-132">การจัดส่ง กำหนดเวลางาน</span><span class="sxs-lookup"><span data-stu-id="882de-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="882de-133">เลือก ไม่ใช่ ในฟิลด์กำลังการผลิตที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="882de-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="882de-134">เลือก ไม่ใช่ ในฟิลด์วัตถุดิบที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="882de-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="882de-135">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="882de-135">Click OK.</span></span>
6. <span data-ttu-id="882de-136">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="882de-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="882de-137">คลิกงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="882de-137">Click All jobs.</span></span>
8. <span data-ttu-id="882de-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="882de-139">เริ่มต้นสั่งงานใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="882de-139">Start the batch order</span></span>
1. <span data-ttu-id="882de-140">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="882de-140">Click Start.</span></span>
2. <span data-ttu-id="882de-141">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="882de-141">Click the General tab.</span></span>
3. <span data-ttu-id="882de-142">เลือก ไม่ ในฟิลด์ ลงรายการบัญชีรายการเบิกสินค้าทันที</span><span class="sxs-lookup"><span data-stu-id="882de-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="882de-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="882de-143">Click OK.</span></span>
5. <span data-ttu-id="882de-144">ในบานหน้าต่างการดำเนินการ ให้คลิก ดู</span><span class="sxs-lookup"><span data-stu-id="882de-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="882de-145">คลิกรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="882de-145">Click Picking list.</span></span>
7. <span data-ttu-id="882de-146">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="882de-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="882de-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-147">Close the page.</span></span>
9. <span data-ttu-id="882de-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-148">Close the page.</span></span>
10. <span data-ttu-id="882de-149">คลิก บัตรกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="882de-149">Click Route card.</span></span>
11. <span data-ttu-id="882de-150">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="882de-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="882de-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-151">Close the page.</span></span>
13. <span data-ttu-id="882de-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="882de-152">Close the page.</span></span>


