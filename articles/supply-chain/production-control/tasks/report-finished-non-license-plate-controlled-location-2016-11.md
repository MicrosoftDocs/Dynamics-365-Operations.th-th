--- 
title: "รายงานเป็น เสร็จแล้ว ไปยังสถานที่ที่ควบคุมป้าย "
description: "คู่มืองานนี้แสดงตัวอย่างการรายงานเป็น เสร็จแล้ว ไปยังสถานที่ที่เป็นป้ายทะเบียนที่มีการควบคุม "
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9a7901b307cffb81cce351e4e45ac8f73f328b02
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a><span data-ttu-id="7fa3a-103">รายงานเป็น เสร็จแล้ว ไปยังสถานที่ที่ควบคุมป้าย </span><span class="sxs-lookup"><span data-stu-id="7fa3a-103">Report as finished to a plate-controlled location</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fa3a-104">คู่มืองานนี้แสดงตัวอย่างการรายงานเป็น เสร็จแล้ว ไปยังสถานที่ที่เป็นป้ายทะเบียนที่มีการควบคุม </span><span class="sxs-lookup"><span data-stu-id="7fa3a-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="7fa3a-105">นโยบายงานที่ใช้งานได้เป็นข้อกำหนดเบื้องต้นสำหรับงานนี้</span><span class="sxs-lookup"><span data-stu-id="7fa3a-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="7fa3a-106">คู่มืองานก่อนหน้าแสดงการตั้งค่าของนโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="7fa3a-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="7fa3a-107">คู่มืองานนี้ต้องการแอพพลิเคชัน Dynamics AX 7.0.1 ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="7fa3a-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="7fa3a-108">ตั้งค่าที่ตั้งเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="7fa3a-108">Set up an output location</span></span>
1. <span data-ttu-id="7fa3a-109">ไปที่การจัดการองค์กร > ทรัพยากร > กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7fa3a-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="7fa3a-110">ในรายการนี้ ให้เลือกกลุ่มทรัพยากร '5102'</span><span class="sxs-lookup"><span data-stu-id="7fa3a-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="7fa3a-111">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="7fa3a-111">Click Edit.</span></span>
4. <span data-ttu-id="7fa3a-112">ในฟิลด์คลังสินค้าเอาท์พุท ให้ป้อน '51'</span><span class="sxs-lookup"><span data-stu-id="7fa3a-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="7fa3a-113">ในฟิลด์ที่ตั้งเอาท์พุท ให้ป้อน '001'</span><span class="sxs-lookup"><span data-stu-id="7fa3a-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="7fa3a-114">สถานที่ 001 ไม่ใช่สถานที่ที่มีการควบคุมป้ายทะเบียน </span><span class="sxs-lookup"><span data-stu-id="7fa3a-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="7fa3a-115">คุณสามารถตั้งค่าสถานที่เอาท์พุทที่ควบคุมป้ายที่ไม่ใช่ป้ายทะเบียน เฉพาะเมื่อนโยบายงานมีอยู่สำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="7fa3a-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="7fa3a-116">สร้างใบสั่งผลิตและรายงานเป็น เสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="7fa3a-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="7fa3a-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7fa3a-117">Close the page.</span></span>
2. <span data-ttu-id="7fa3a-118">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="7fa3a-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="7fa3a-119">คลิกใบสั่งผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="7fa3a-119">Click New production order.</span></span>
4. <span data-ttu-id="7fa3a-120">ในฟิลด์หมายเลขสินค้า ให้ป้อน 'L0101'</span><span class="sxs-lookup"><span data-stu-id="7fa3a-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="7fa3a-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7fa3a-121">Click Create.</span></span>
6. <span data-ttu-id="7fa3a-122">ในบานหน้าต่างการดำเนินการ คลิกที่ใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="7fa3a-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="7fa3a-123">คลิกประเมิน </span><span class="sxs-lookup"><span data-stu-id="7fa3a-123">Click Estimate.</span></span>
8. <span data-ttu-id="7fa3a-124">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="7fa3a-124">Click OK.</span></span>
9. <span data-ttu-id="7fa3a-125">คลิกที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7fa3a-125">Click Start.</span></span>
10. <span data-ttu-id="7fa3a-126">คลิกแท็บ ทั่วไป </span><span class="sxs-lookup"><span data-stu-id="7fa3a-126">Click the General tab.</span></span>
11. <span data-ttu-id="7fa3a-127">ในฟิลด์การใช้ BOM อัตโนมัติ ให้เลือก 'ไม่เคย'</span><span class="sxs-lookup"><span data-stu-id="7fa3a-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="7fa3a-128">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="7fa3a-128">Click OK.</span></span>
13. <span data-ttu-id="7fa3a-129">คลิกรายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="7fa3a-129">Click Report as finished.</span></span>
14. <span data-ttu-id="7fa3a-130">คลิกแท็บ ทั่วไป </span><span class="sxs-lookup"><span data-stu-id="7fa3a-130">Click the General tab.</span></span>
15. <span data-ttu-id="7fa3a-131">เลือก ใช่ ในฟิลด์ยอมรับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="7fa3a-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="7fa3a-132">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="7fa3a-132">Click OK.</span></span>
17. <span data-ttu-id="7fa3a-133">ในบานหน้าต่างการดำเนินการ คลิกคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7fa3a-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="7fa3a-134">คลิกรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="7fa3a-134">Click Work details.</span></span>
    * <span data-ttu-id="7fa3a-135">เมื่อใบสั่งผลิตถูกรายงานเป็น เสร็จแล้ว จึงไม่มีการสร้างงานสำหรับการสำรอง </span><span class="sxs-lookup"><span data-stu-id="7fa3a-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="7fa3a-136">นี่เกิดขึ้นเนื่องจากนโยบายงานถูกกำหนดให้ป้องกันงานจากการถูกสร้าง เมื่อผลิตภัณฑ์ L0101 ถูกรายงานเป็น เสร็จแล้ว ไปยังสถานที่ 001</span><span class="sxs-lookup"><span data-stu-id="7fa3a-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  


