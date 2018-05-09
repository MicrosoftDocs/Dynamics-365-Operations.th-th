--- 
title: "ดำเนินการงานกระบวนการคัมบัง"
description: "กระบวนงานนี้มุ่งเน้นไปที่การดำเนินงานกระบวนงานคัมบัง "
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4f0579e9bccdcf240d33bb7b936bd9f9f7619028
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="17b64-103">ดำเนินการงานกระบวนการคัมบัง</span><span class="sxs-lookup"><span data-stu-id="17b64-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17b64-104">กระบวนงานนี้มุ่งเน้นไปที่การดำเนินงานกระบวนงานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="17b64-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="17b64-105">งานแรกเสร็จสมบูรณ์พร้อมกับปริมาณที่คาดหวังไว้และไม่มีข้อผิดพลาด </span><span class="sxs-lookup"><span data-stu-id="17b64-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="17b64-106">งานที่สองเสร็จสมบูรณ์พร้อมกับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="17b64-106">The second job is completed with errors.</span></span> <span data-ttu-id="17b64-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="17b64-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="17b64-108">กระบวนงานนี้มีไว้สำหรับพนักงานควบคุมเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="17b64-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="17b64-109">เลือกงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="17b64-109">Select a kanban job</span></span>
1. <span data-ttu-id="17b64-110">ไปที่การควบคุมการผลิต > คัมบัง > บอร์ดคัมบังสำหรับงานกระบวนการ </span><span class="sxs-lookup"><span data-stu-id="17b64-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="17b64-111">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="17b64-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="17b64-112">คลิกแถวที่มีกลุ่มทรัพยากร 1250</span><span class="sxs-lookup"><span data-stu-id="17b64-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="17b64-113">ซึ่งกรองรายการงานเพื่อแสดงเฉพาะงานสำหรับเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="17b64-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="17b64-114">ทำเครื่องหมายแถวที่มีสถานะงานเป็นวางแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="17b64-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="17b64-115">ดำเนินงานที่มีปริมาณที่คาดไว้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="17b64-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="17b64-116">ขยายหรือยุบส่วนรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="17b64-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="17b64-117">ส่วนนี้แสดงข้อมูลสำคัญเกี่ยวกับหมายเลขบัตร หมายเลขสินค้า ปริมาณที่สั่ง และชื่อกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="17b64-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="17b64-118">ขยายหรือยุบส่วนคำแนะนำเกี่ยวกับการผลิต</span><span class="sxs-lookup"><span data-stu-id="17b64-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="17b64-119">ส่วนนี้แสดงคำแนะนำเกี่ยวกับการผลิตสำหรับกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="17b64-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="17b64-120">คำแนะนำสามารถเป็นข้อความ รูปภาพ ภาพวาด หรือเอกสารอื่นๆได้</span><span class="sxs-lookup"><span data-stu-id="17b64-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="17b64-121">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="17b64-121">Click Start.</span></span>
    * <span data-ttu-id="17b64-122">เลือกงานที่ยังไม่เสร็จสิ้น </span><span class="sxs-lookup"><span data-stu-id="17b64-122">Select a job that is not completed.</span></span> <span data-ttu-id="17b64-123">.ช้ไอคอนสถานะในฟิลด์สถานะงาน เพื่อดูสถานะงาน</span><span class="sxs-lookup"><span data-stu-id="17b64-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="17b64-124">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="17b64-124">Click Complete.</span></span>
    * <span data-ttu-id="17b64-125">งานเสร็จสมบูรณ์พร้อมกับปริมาณที่คาดหวังไว้</span><span class="sxs-lookup"><span data-stu-id="17b64-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="17b64-126">ดำเนินงานที่มีงานที่มีข้อผิดพลาดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="17b64-126">Complete a job with errors</span></span>
1. <span data-ttu-id="17b64-127">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="17b64-127">Click Start.</span></span>
    * <span data-ttu-id="17b64-128">เมื่องานเสร็จสมบูรณ์ งานต่อไปบนรายการจะถูกเลือกโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="17b64-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="17b64-129">นี่เป็นเหตุผลว่าทำไมคุณไม่จำเป็นต้องเลือกงานก่อนที่คุณจะคลิกเริ่ม</span><span class="sxs-lookup"><span data-stu-id="17b64-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="17b64-130">ในบานหน้าต่างการดำเนินการ คลิกผลิต</span><span class="sxs-lookup"><span data-stu-id="17b64-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="17b64-131">คลิกเสร็จสมบูรณ์ (รายละเอียด)</span><span class="sxs-lookup"><span data-stu-id="17b64-131">Click Complete (details).</span></span>
4. <span data-ttu-id="17b64-132">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="17b64-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="17b64-133">ในฟิลด์ปริมาณสินค้าที่บกพร่อง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="17b64-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="17b64-134">ในฟิลด์ปริมาณสินค้าที่ดี ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="17b64-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="17b64-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="17b64-135">Click OK.</span></span>


