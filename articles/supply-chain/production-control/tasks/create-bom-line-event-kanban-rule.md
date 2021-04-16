---
title: สร้างกฏคัมบังสำหรับอีเว้นท์รายการ BOM
description: 'งานนี้มุ่งเน้นการตั้งค่าที่จำเป็นเพื่อสร้างกฎคัมบังเหตุการณ์ เพื่อให้มั่นใจว่าการจัดหาวัสดุสำหรับรายการ BOM การผลิตในลีนแบบผสมและสภาพแวดล้อมการผลิตแบบดั้งเดิม '
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d415e146f33224bcbbfb73498040d584e07f10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829221"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="2899a-103">สร้างกฏคัมบังสำหรับอีเว้นท์รายการ BOM</span><span class="sxs-lookup"><span data-stu-id="2899a-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2899a-104">งานนี้มุ่งเน้นการตั้งค่าที่จำเป็นเพื่อสร้างกฎคัมบังเหตุการณ์ เพื่อให้มั่นใจว่าการจัดหาวัสดุสำหรับรายการ BOM การผลิตในลีนแบบผสมและสภาพแวดล้อมการผลิตแบบดั้งเดิม </span><span class="sxs-lookup"><span data-stu-id="2899a-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="2899a-105">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="2899a-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="2899a-106">งานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เนื่องจากพวกเขาจัดเตรียมการผลิตสำหรับผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2899a-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="2899a-107">สร้างกฎคัมบังใหม่</span><span class="sxs-lookup"><span data-stu-id="2899a-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="2899a-108">ไปที่การควบคุมการผลิต > งานประจำงวด > การคำนวณปริมาณตามระบบคัมบัง > กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2899a-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="2899a-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2899a-109">Click New.</span></span>
3. <span data-ttu-id="2899a-110">ในฟิลด์ชนิด เลือก 'การถอน'</span><span class="sxs-lookup"><span data-stu-id="2899a-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="2899a-111">ชนิดการถอนถูกใช้เพื่อสร้างคัมบังการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="2899a-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="2899a-112">ในฟิลด์กลยุทธ์การเติมสินค้า ให้เลือก 'เหตุการณ์'</span><span class="sxs-lookup"><span data-stu-id="2899a-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="2899a-113">กลยุทธ์เหตุการณ์ถูกใช้เพื่อสร้างการโอนย้ายของคัมบังตามเหตุการณ์ </span><span class="sxs-lookup"><span data-stu-id="2899a-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="2899a-114">ภายหลังในคู่มืองานนี้ เราจะทริกเกอร์โดยการประมาณใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="2899a-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="2899a-115">ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2899a-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="2899a-116">ป้อนหรือเลือก ReplenishSpeakerComponents </span><span class="sxs-lookup"><span data-stu-id="2899a-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="2899a-117">กิจกรรมการโอนย้ายนี้มีคลังสินค้าที่รับสินค้า (ผลลัพธ์) และสถานที่ 12 ซึ่งหมายถึงวัสดุจะถูกย้ายไปยังสถานที่ 12 ในคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="2899a-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="2899a-118">ขยายส่วนรายละเอียด </span><span class="sxs-lookup"><span data-stu-id="2899a-118">Expand the Details section.</span></span>
7. <span data-ttu-id="2899a-119">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือก M0001</span><span class="sxs-lookup"><span data-stu-id="2899a-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="2899a-120">ขยายส่วนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="2899a-120">Expand the Events section.</span></span>
9. <span data-ttu-id="2899a-121">ในฟิลด์เหตุการณ์รายการ BOM ให้เลือก 'อัตโนมัติ'</span><span class="sxs-lookup"><span data-stu-id="2899a-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="2899a-122">ด้วยฟิลด์เหตุการณ์ของรายการ BOM ถูกตั้งค่าเป็นอัตโนมัติ คัมบังจะถูกสร้างเพื่อเติมเต็มความต้องการทางวัสดุสำหรับรายการ BOM ของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="2899a-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="2899a-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2899a-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="2899a-124">สร้างและแก้ไขใบสั่งผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="2899a-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="2899a-125">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="2899a-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="2899a-126">คลิกใบสั่งผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="2899a-126">Click New production order.</span></span>
3. <span data-ttu-id="2899a-127">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2899a-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2899a-128">ป้อนหรือเลือก 'L0001' </span><span class="sxs-lookup"><span data-stu-id="2899a-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="2899a-129">เราใช้สินค้า L0001 เนื่องจากสินค้า M0001 ถูกรวมอยู่ใน BOM สำหรับสินค้า L0001</span><span class="sxs-lookup"><span data-stu-id="2899a-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="2899a-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2899a-130">Click Create.</span></span>
5. <span data-ttu-id="2899a-131">ในรายการ ให้คลิกลิงค์ในแถวสำหรับ L0001</span><span class="sxs-lookup"><span data-stu-id="2899a-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="2899a-132">คลิก BOM</span><span class="sxs-lookup"><span data-stu-id="2899a-132">Click BOM.</span></span>
7. <span data-ttu-id="2899a-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2899a-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2899a-134">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="2899a-134">Click Edit.</span></span>
9. <span data-ttu-id="2899a-135">ในฟิลด์ชนิดรายการ เลือก 'การจัดหาวัสดุที่มีการเชื่อมโยงความต้องการกับการจัดซื้อ'</span><span class="sxs-lookup"><span data-stu-id="2899a-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="2899a-136">การจัดหาวัสดุที่มีการเชื่อมโยงความต้องการกับการจัดซื้อ ถูกเลือกให้ทริกเกอร์การสร้างการจัดหาวัสดุของคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2899a-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="2899a-137">เลือก ไม่ใช่ ในฟิลด์ปริมาณการใช้ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2899a-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="2899a-138">การยกเลิกการเลือกกล่องกาเครื่องหมายของปริมาณการใช้ทรัพยากร ทำให้เราสามารถเปลี่ยนคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="2899a-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="2899a-139">ขยายส่วนมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2899a-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="2899a-140">ในฟิลด์คลังสินค้า พิมพ์ '12'</span><span class="sxs-lookup"><span data-stu-id="2899a-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="2899a-141">คลังสินค้าถูกตั้งค่าเป็น 12 เนื่องจากนี่คือสินค้าเอาท์พุทสำหรับกิจกรรมการถอน</span><span class="sxs-lookup"><span data-stu-id="2899a-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="2899a-142">ในฟิลด์สถานที่ ให้พิมพ์ '12'</span><span class="sxs-lookup"><span data-stu-id="2899a-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="2899a-143">สถานที่ถูกตั้งค่าเป็น 12 เนื่องจากนี่คือสถานที่เอาท์พุทของกิจกรรมการถอน</span><span class="sxs-lookup"><span data-stu-id="2899a-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="2899a-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2899a-144">Close the page.</span></span>
15. <span data-ttu-id="2899a-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2899a-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="2899a-146">ประมาณใบสั่งผลิตและดูคัมบังที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="2899a-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="2899a-147">คลิกประเมิน </span><span class="sxs-lookup"><span data-stu-id="2899a-147">Click Estimate.</span></span>
    * <span data-ttu-id="2899a-148">การประมาณใบสั่งผลิตจะทริกเกอร์การสร้างของคัมบังที่เกี่ยวข้องไปยังรายการการจัดหาวัสดุ M0001</span><span class="sxs-lookup"><span data-stu-id="2899a-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="2899a-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2899a-149">Click OK.</span></span>
3. <span data-ttu-id="2899a-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2899a-150">Close the page.</span></span>
4. <span data-ttu-id="2899a-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2899a-151">Close the page.</span></span>
5. <span data-ttu-id="2899a-152">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2899a-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="2899a-153">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2899a-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2899a-154">เลือกกฎคัมบังเหตุการณ์ที่สร้างสำหรับสินค้า M0001</span><span class="sxs-lookup"><span data-stu-id="2899a-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="2899a-155">ขยายส่วนคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2899a-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="2899a-156">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2899a-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2899a-157">สังเกตคัมบังที่สร้างเพื่อจัดหาวัสดุ M0001 สำหรับใบสั่งผลิตที่ประเมินได้</span><span class="sxs-lookup"><span data-stu-id="2899a-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="2899a-158">นี่เป็นขั้นตอนสุดท้าย!</span><span class="sxs-lookup"><span data-stu-id="2899a-158">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]