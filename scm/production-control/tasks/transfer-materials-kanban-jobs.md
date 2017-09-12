--- 
title: "โอนย้ายวัสดุด้วยงานคัมบัง (กุมภาพันธ์ 2016 เท่านั้น)"
description: "ขั้นตอนนี้มุ่งเน้นการดำเนินการงานคัมบัง ในการเบิกถอนเพื่อการโอนย้ายวัสดุและส่วนประกอบ"
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a><span data-ttu-id="042c1-103">โอนย้ายวัสดุด้วยงานคัมบัง (กุมภาพันธ์ 2016 เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="042c1-103">Transfer materials with kanban jobs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="042c1-104">ขั้นตอนนี้มุ่งเน้นการดำเนินการงานคัมบัง ในการเบิกถอนเพื่อการโอนย้ายวัสดุและส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="042c1-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="042c1-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="042c1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="042c1-106">ขั้นตอนนี้มีไว้สำหรับผู้ปฏิบัติงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="042c1-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="042c1-107">แสดงงานที่มีการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="042c1-107">Display transfer jobs</span></span>
1. <span data-ttu-id="042c1-108">ไปที่การควบคุมการผลิต > คัมบัง > บอร์ดคัมบังสำหรับงานการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="042c1-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="042c1-109">ขยายหรือยุบส่วนตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="042c1-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="042c1-110">ในฟิลด์ตัวกรอง คุณสามารถระบุงานที่คุณต้องการดู โดยการกรองข้อมูลในขั้นตอนการผลิต, ชื่อกิจกรรม, จากคลังสินค้าและที่ตั้งที่หนึ่งไปยังคลังสินค้าและที่ตั้งอีกที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="042c1-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="042c1-111">ในฟิลด์จากคลังสินค้า ให้พิมพ์ '11'</span><span class="sxs-lookup"><span data-stu-id="042c1-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="042c1-112">ในฟิลด์สถานที่ปลายทาง ให้พิมพ์'12'</span><span class="sxs-lookup"><span data-stu-id="042c1-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="042c1-113">เริ่มต้นงานการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="042c1-113">Start a transfer job</span></span>
1. <span data-ttu-id="042c1-114">ในรายการนี้ ให้ยกเลิกการทำเครื่องหมายแถวที่เลือก - ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="042c1-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="042c1-115">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="042c1-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="042c1-116">เลือกงานแรกที่ไม่ได้มีสถานะวางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="042c1-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="042c1-117">ตรวจสอบให้แน่ใจว่า นี่คืองานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="042c1-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="042c1-118">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="042c1-118">Click Start.</span></span>
    * <span data-ttu-id="042c1-119">โปรดสังเกตว่า มีไอคอนบ่งชี้ว่างานได้เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="042c1-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="042c1-120">เลือกการโอนย้ายงานที่สอง และเปลี่ยนปริมาณ</span><span class="sxs-lookup"><span data-stu-id="042c1-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="042c1-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="042c1-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="042c1-122">คุณสามารถเลือกงานได้หลากหลาย แต่ในขณะนี้ให้เลือกแถวที่ 5</span><span class="sxs-lookup"><span data-stu-id="042c1-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="042c1-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="042c1-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="042c1-124">ตรวจสอบให้แน่ใจว่า งานในขั้นตอนก่อนหน้านี้ถูกเลือกเพียงอันเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="042c1-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="042c1-125">ยกเลิกเลือกงานอื่น ๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="042c1-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="042c1-126">จดบันทึกค่าในฟิลด์ของปริมาณงาน เพื่ออ้างอิงต่อไป</span><span class="sxs-lookup"><span data-stu-id="042c1-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="042c1-127">กำหนดปริมาณงานเป็น '30'</span><span class="sxs-lookup"><span data-stu-id="042c1-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="042c1-128">โปรดสังเกตคำเตือน </span><span class="sxs-lookup"><span data-stu-id="042c1-128">Notice the warning!</span></span> <span data-ttu-id="042c1-129">คุณไม่ได้รับอนุญาตให้โอนย้าย 30</span><span class="sxs-lookup"><span data-stu-id="042c1-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="042c1-130">ตามการตั้งค่ากฎคัมบัง คุณสามารถโอนย้ายได้เฉพาะปริมาณเดิมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="042c1-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="042c1-131">ใช้ค่าที่จดไว้ก่อนหน้านี้ในฟิลด์ปริมาณงาน </span><span class="sxs-lookup"><span data-stu-id="042c1-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="042c1-132">ตั้งค่าปริมาณงานให้เป็นค่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="042c1-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="042c1-133">เริ่มต้นงานการโอนย้ายที่สอง</span><span class="sxs-lookup"><span data-stu-id="042c1-133">Start the second transfer job</span></span>
1. <span data-ttu-id="042c1-134">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="042c1-134">Click Start.</span></span>
    * <span data-ttu-id="042c1-135">ซึ่งจะเริ่มต้นงานการโอนย้ายในแถวที่ 5</span><span class="sxs-lookup"><span data-stu-id="042c1-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="042c1-136">ดำเนินการโอนย้ายงานทั้งสองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="042c1-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="042c1-137">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="042c1-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="042c1-138">ขณะนี้ มีงานโอนย้าย2แถวที่ถูกเลือก คือ แถวที่ 4 และแถวที่ 5</span><span class="sxs-lookup"><span data-stu-id="042c1-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="042c1-139">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="042c1-139">Click Complete.</span></span>
    * <span data-ttu-id="042c1-140">การโอนย้ายนี้จะสำเร็จทั้ง2งาน</span><span class="sxs-lookup"><span data-stu-id="042c1-140">This will complete the transfer of both jobs.</span></span>  


