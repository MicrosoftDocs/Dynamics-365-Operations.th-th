---
title: แปลงกลับสถานะงานคัมบัง
description: 'กระบวนงานนี้มุ่งเน้นการเปลี่ยนกลับสถานะงานคัมบังที่ไม่ถูกต้อง '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94618494b9c338ed27b2558c91dc662c853d3cda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261105"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="b9479-103">แปลงกลับสถานะงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="b9479-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9479-104">กระบวนงานนี้มุ่งเน้นการเปลี่ยนกลับสถานะงานคัมบังที่ไม่ถูกต้อง </span><span class="sxs-lookup"><span data-stu-id="b9479-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="b9479-105">ซึ่งมีประโยชน์ในกรณีที่พนักงานควบคุมเครื่องจักรอัพเดตงานไม่ถูกต้อง หรือตั้งค่าสถานะไม่ถูกต้องโดยไม่ได้ตั้งใจ </span><span class="sxs-lookup"><span data-stu-id="b9479-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="b9479-106">ในกระบวนงานนี้ งานคัมบังได้ถูกลงทะเบียนเป็นการถูกจัดเตรียมไว้โดยไม่ได้ตั้งใจ และสถานะจะถูกแปลงกลับ </span><span class="sxs-lookup"><span data-stu-id="b9479-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="b9479-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="b9479-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b9479-108">กระบวนงานนี้มีไว้สำหรับผู้ดูแลร้านหรือพนักงานควบคุมเครื่องจักรที่ทำงานในบริษัท lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="b9479-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="b9479-109">เปิดบอร์ดกระบวนการสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="b9479-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="b9479-110">ไปที่บอร์ดคัมบังสำหรับงานกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="b9479-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="b9479-111">ในฟิลด์เซลล์งาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b9479-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="b9479-112">เลือกเซลล์ทำงาน 1260</span><span class="sxs-lookup"><span data-stu-id="b9479-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="b9479-113">จัดเตรียมงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="b9479-113">Prepare kanban job</span></span>
1. <span data-ttu-id="b9479-114">คลิกจัดเตรียม </span><span class="sxs-lookup"><span data-stu-id="b9479-114">Click Prepare.</span></span>
    * <span data-ttu-id="b9479-115">ถ้าคุณไม่สามารถคลิก การจัดเตรียม เนื่องจากจะกลายเป็นสีเทา ให้ตรวจสอบให้แน่ใจว่างานคัมบังที่เลือกมีสถานะว่าวางแผนแล้ว ซึ่งจะบ่งชี้ได้ด้วยไอคอนคัมบังที่ว่างเปล่า </span><span class="sxs-lookup"><span data-stu-id="b9479-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="b9479-116">หากการจัดเตรียมล้มเหลว ให้ตรวจสอบให้แน่ใจว่ามีวัตถุดิบทั้งหมดในรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="b9479-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="b9479-117">ในรายการ ให้เลือกงานที่เตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="b9479-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="b9479-118">เลือกงานแรกที่คุณเพิ่งจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="b9479-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="b9479-119">โปรดสังเกตว่า สถานะงานที่เตรียมไว้ซึ่งถูกระบุด้วยรูปสามเหลี่ยมภายในไอคอนคัมบัง</span><span class="sxs-lookup"><span data-stu-id="b9479-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="b9479-120">แปลงกลับสถานะของงานคัมบังที่จัดเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="b9479-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="b9479-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b9479-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b9479-122">เลือกงานแรกที่จัดเตรียมแล้ว</span><span class="sxs-lookup"><span data-stu-id="b9479-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="b9479-123">ในบานหน้าต่างการดำเนินการ คลิกผลิต</span><span class="sxs-lookup"><span data-stu-id="b9479-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="b9479-124">คลิกแปลงกลับสถานะ</span><span class="sxs-lookup"><span data-stu-id="b9479-124">Click Revert status.</span></span>
    * <span data-ttu-id="b9479-125">คุณสามารถใช้กฎคัมบังสำรองเมื่อตรงตามเงื่อนไขต่อไปนี้: - กลยุทธ์การเติมสินค้าสำหรับกฎทั้งสองเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="b9479-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="b9479-126">- เวอร์ชันของขั้นตอนการผลิตจะเหมือนกันสำหรับกฎทั้งสอง </span><span class="sxs-lookup"><span data-stu-id="b9479-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="b9479-127">- ผลิตภัณฑ์ที่ได้รับการจัดหาจะเหมือนกันสำหรับกฎทั้งสอง </span><span class="sxs-lookup"><span data-stu-id="b9479-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="b9479-128">- กิจกรรมปลายน้ำใดๆที่ถูกกำหนดสำหรับกิจกรรมสุดท้ายของกฎคัมบังต้องเหมือนกันสำหรับกฎทั้งสอง </span><span class="sxs-lookup"><span data-stu-id="b9479-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="b9479-129">- ต้องตั้งค่าคอนฟิกมิติสินค้าคงคลังที่ได้จัดหามาแบบเดียวกันสำหรับกฎทั้งสอง </span><span class="sxs-lookup"><span data-stu-id="b9479-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="b9479-130">- สถานะของหน่วยจัดการวัสดุต้องเป็นไม่ถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="b9479-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="b9479-131">- การตั้งค่าคอนฟิกสำหรับเหตุการณ์คัมบังต้องเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="b9479-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="b9479-132">ตรวจสอบให้แน่ใจว่าสถานะใหม่คือ วางแผนแล้ว</span><span class="sxs-lookup"><span data-stu-id="b9479-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="b9479-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b9479-133">Click OK.</span></span>
5. <span data-ttu-id="b9479-134">ในรายการนี้ ให้ยกเลิกการทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b9479-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="b9479-135">เลือกงานที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="b9479-135">Select the same job.</span></span>  
    * <span data-ttu-id="b9479-136">โปรดสังเกตว่าสถานะงานสำหรับงานคัมบังถูกแปลงกลับเป็น วางแผนแล้ว ซึ่งถูกบ่งชี้ด้วยไอคอนคัมบังที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="b9479-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]