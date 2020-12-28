---
title: โอนย้ายวัสดุด้วยงานคัมบัง
description: ขั้นตอนนี้มุ่งเน้นการดำเนินการงานคัมบัง ในการเบิกถอนเพื่อการโอนย้ายวัสดุและส่วนประกอบ
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96cb77b7b37fe6519a812735d9a41749da078cf2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438584"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="34414-103">โอนย้ายวัสดุด้วยงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="34414-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34414-104">ขั้นตอนนี้มุ่งเน้นการดำเนินการงานคัมบัง ในการเบิกถอนเพื่อการโอนย้ายวัสดุและส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="34414-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="34414-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="34414-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="34414-106">ขั้นตอนนี้มีไว้สำหรับผู้ปฏิบัติงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="34414-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="34414-107">แสดงงานที่มีการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="34414-107">Display transfer jobs</span></span>
1. <span data-ttu-id="34414-108">ไปที่การควบคุมการผลิต > คัมบัง > บอร์ดคัมบังสำหรับงานการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="34414-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="34414-109">ขยายหรือยุบส่วนตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="34414-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="34414-110">ในฟิลด์ตัวกรอง คุณสามารถระบุงานที่คุณต้องการดู โดยการกรองข้อมูลในขั้นตอนการผลิต, ชื่อกิจกรรม, จากคลังสินค้าและที่ตั้งที่หนึ่งไปยังคลังสินค้าและที่ตั้งอีกที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="34414-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="34414-111">ในฟิลด์จากคลังสินค้า ให้พิมพ์ '11'</span><span class="sxs-lookup"><span data-stu-id="34414-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="34414-112">ในฟิลด์สถานที่ปลายทาง ให้พิมพ์'12'</span><span class="sxs-lookup"><span data-stu-id="34414-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="34414-113">เริ่มต้นงานการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="34414-113">Start a transfer job</span></span>
1. <span data-ttu-id="34414-114">ในรายการนี้ ให้ยกเลิกการทำเครื่องหมายแถวที่เลือก - ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="34414-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="34414-115">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="34414-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="34414-116">เลือกงานแรกที่ไม่ได้มีสถานะวางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="34414-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="34414-117">ตรวจสอบให้แน่ใจว่า นี่คืองานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="34414-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="34414-118">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="34414-118">Click Start.</span></span>
    * <span data-ttu-id="34414-119">โปรดสังเกตว่า มีไอคอนบ่งชี้ว่างานได้เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="34414-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="34414-120">เลือกการโอนย้ายงานที่สอง และเปลี่ยนปริมาณ</span><span class="sxs-lookup"><span data-stu-id="34414-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="34414-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="34414-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="34414-122">คุณสามารถเลือกงานได้หลากหลาย แต่ในขณะนี้ให้เลือกแถวที่ 5</span><span class="sxs-lookup"><span data-stu-id="34414-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="34414-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="34414-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="34414-124">ตรวจสอบให้แน่ใจว่า งานในขั้นตอนก่อนหน้านี้ถูกเลือกเพียงอันเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="34414-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="34414-125">ยกเลิกเลือกงานอื่น ๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="34414-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="34414-126">จดบันทึกค่าในฟิลด์ของปริมาณงาน เพื่ออ้างอิงต่อไป</span><span class="sxs-lookup"><span data-stu-id="34414-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="34414-127">กำหนดปริมาณงานเป็น '30'</span><span class="sxs-lookup"><span data-stu-id="34414-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="34414-128">โปรดสังเกตคำเตือน </span><span class="sxs-lookup"><span data-stu-id="34414-128">Notice the warning!</span></span> <span data-ttu-id="34414-129">คุณไม่ได้รับอนุญาตให้โอนย้าย 30</span><span class="sxs-lookup"><span data-stu-id="34414-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="34414-130">ตามการตั้งค่ากฎคัมบัง คุณสามารถโอนย้ายได้เฉพาะปริมาณเดิมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="34414-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="34414-131">ใช้ค่าที่จดไว้ก่อนหน้านี้ในฟิลด์ปริมาณงาน </span><span class="sxs-lookup"><span data-stu-id="34414-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="34414-132">ตั้งค่าปริมาณงานให้เป็นค่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="34414-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="34414-133">เริ่มต้นงานการโอนย้ายที่สอง</span><span class="sxs-lookup"><span data-stu-id="34414-133">Start the second transfer job</span></span>
1. <span data-ttu-id="34414-134">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="34414-134">Click Start.</span></span>
    * <span data-ttu-id="34414-135">ซึ่งจะเริ่มต้นงานการโอนย้ายในแถวที่ 5</span><span class="sxs-lookup"><span data-stu-id="34414-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="34414-136">ดำเนินการโอนย้ายงานทั้งสองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="34414-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="34414-137">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="34414-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="34414-138">ขณะนี้ มีงานโอนย้าย2แถวที่ถูกเลือก คือ แถวที่ 4 และแถวที่ 5</span><span class="sxs-lookup"><span data-stu-id="34414-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="34414-139">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="34414-139">Click Complete.</span></span>
    * <span data-ttu-id="34414-140">การโอนย้ายนี้จะสำเร็จทั้ง2งาน</span><span class="sxs-lookup"><span data-stu-id="34414-140">This will complete the transfer of both jobs.</span></span>  

