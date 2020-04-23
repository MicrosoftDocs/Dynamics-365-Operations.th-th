---
title: สร้างกฏคัมบังสำหรับอีเว้นท์การขาย
description: 'ขั้นตอนนี้มุ่งเน้นการตั้งค่าที่จำเป็นเพื่อสร้างกฎคัมบังการผลิตที่มีการทริกเกอร์ขณะการสร้างใบสั่งขาย '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1759adea6db8120078e2f32bff79178545c2328a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210869"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="e94de-103">สร้างกฏคัมบังสำหรับอีเว้นท์การขาย</span><span class="sxs-lookup"><span data-stu-id="e94de-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e94de-104">ขั้นตอนนี้มุ่งเน้นการตั้งค่าที่จำเป็นเพื่อสร้างกฎคัมบังการผลิตที่มีการทริกเกอร์ขณะการสร้างใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="e94de-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="e94de-105">เหตุการณ์กฎคัมบังความต้องการการเติมสินค้าที่มาจากรายการใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="e94de-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="e94de-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e94de-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e94de-107">ขั้นตอนนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสตรีมค่า ตามที่พวกเขาจัดเตรียมการผลิตสำหรับผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="e94de-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="e94de-108">สร้างกฎคัมบังใหม่</span><span class="sxs-lookup"><span data-stu-id="e94de-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="e94de-109">ไปที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="e94de-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="e94de-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e94de-110">Click New.</span></span>
3. <span data-ttu-id="e94de-111">ในฟิลด์กลยุทธ์การเติมสินค้า ให้เลือก 'เหตุการณ์'</span><span class="sxs-lookup"><span data-stu-id="e94de-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="e94de-112">การเลือกเหตุการณ์หมายความว่ากฎคัมบังถูกทริกเกอร์โดยเหตุการณ์ ตัวอย่างเช่น การสร้างรายการใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="e94de-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="e94de-113">ซึ่งจะใช้กับพื้นที่ที่แต่ละคัมบังควรครอบคลุมความต้องการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="e94de-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="e94de-114">ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e94de-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="e94de-115">เลือกการประกอบชิ้นส่วนขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="e94de-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="e94de-116">ขยายส่วนรายละเอียด </span><span class="sxs-lookup"><span data-stu-id="e94de-116">Expand the Details section.</span></span>
6. <span data-ttu-id="e94de-117">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e94de-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="e94de-118">เลือก L0050</span><span class="sxs-lookup"><span data-stu-id="e94de-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="e94de-119">กำหนดเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="e94de-119">Define an event</span></span>
1. <span data-ttu-id="e94de-120">ขยายส่วนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="e94de-120">Expand the Events section.</span></span>
2. <span data-ttu-id="e94de-121">ในฟิลด์เหตุการณ์การขาย ให้เลือก 'อัตโนมัติ'</span><span class="sxs-lookup"><span data-stu-id="e94de-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="e94de-122">โดยการเลือกเหตุการณ์การขายอัตโนมัติ กฎคัมบังนี้จะถูกทริกเกอร์โดยอัตโนมัติเมื่อรายการการขายตรงกับสถานที่รับสินค้าและผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="e94de-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="e94de-123">ในขั้นตอนนี้เป็นผลิตภัณฑ์ L0050 บน คลังสินค้าที่ 13</span><span class="sxs-lookup"><span data-stu-id="e94de-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="e94de-124">กำหนดปริมาณเหตุการณ์ต่ำสุดไปที่ '50'</span><span class="sxs-lookup"><span data-stu-id="e94de-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="e94de-125">ด้วยปริมาณเหตุการณ์ต่ำสุดของ 50 กฎคัมบังจะถูกทริกเกอร์โดยเหตุการณ์เท่านั้นด้วยปริมาณ 50 ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="e94de-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="e94de-126">ขยายส่วนขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="e94de-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="e94de-127">โปรดสังเกตว่าสถานรับสินค้าเป็นคลังสินค้า 13</span><span class="sxs-lookup"><span data-stu-id="e94de-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="e94de-128">ซึ่งหมายความว่ากฎคัมบังนี้จะถูกทริกเกอร์สำหรับตำแหน่งนี้</span><span class="sxs-lookup"><span data-stu-id="e94de-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="e94de-129">ในตัวอย่างนี้ รายการการขายสำหรับผลิตภัณฑ์ L0050 ด้วยปริมาณ 50 หรือมากกว่าที่คลังสินค้า 13 จะทริกเกอร์กฎคัมบังนี้</span><span class="sxs-lookup"><span data-stu-id="e94de-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="e94de-130">สร้างรายการขายเพื่อทริกเกอร์กฎคัมบังของเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="e94de-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="e94de-131">ไปที่ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e94de-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="e94de-132">คำเตือนจะแสดงขึ้นเมื่อกฎคัมบังบันทึก ซึ่งหมายความว่าคัมบังนั้นจะถูกสร้างแบบเรียลไทม์ในระหว่างการสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="e94de-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="e94de-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e94de-133">Click New.</span></span>
3. <span data-ttu-id="e94de-134">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e94de-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="e94de-135">ตัวอย่างเช่น เลือก 003 ของสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="e94de-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="e94de-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e94de-136">Click OK.</span></span>
5. <span data-ttu-id="e94de-137">ในฟิลด์ หมายเลขสินค้า ให้พิมพ์ 'L0050'</span><span class="sxs-lookup"><span data-stu-id="e94de-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="e94de-138">ในฟิลด์ไซต์ ให้พิมพ์ '1'</span><span class="sxs-lookup"><span data-stu-id="e94de-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="e94de-139">เลือกไซต์ 1 เนื่องจากคลังสินค้า 13 อยู่ที่ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="e94de-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="e94de-140">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e94de-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="e94de-141">เซ็ตคลังสินค้าไปที่ 13</span><span class="sxs-lookup"><span data-stu-id="e94de-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="e94de-142">กำหนดปริมาณเป็น '75'</span><span class="sxs-lookup"><span data-stu-id="e94de-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="e94de-143">ป้อนปริมาณ 50 หรือมากกว่า เพื่อทริกเกอร์กฎคัมบังที่สร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="e94de-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="e94de-144">ตรวจสอบว่าคัมบังได้ถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="e94de-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="e94de-145">คลิกที่ผลิตภัณฑ์และการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="e94de-145">Click Product and supply.</span></span>
2. <span data-ttu-id="e94de-146">คลิกดูแผนภูมิการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="e94de-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="e94de-147">โปรดสังเกตว่า มีสร้างคัมบังด้วยปริมาณเดียวกันกับรายการการขาย </span><span class="sxs-lookup"><span data-stu-id="e94de-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="e94de-148">คุณยังสามารถดูการตัดสินค้าจากคลังวัสดุที่จำเป็นต่อการผลิต L0050 </span><span class="sxs-lookup"><span data-stu-id="e94de-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="e94de-149">นี่เป็นขั้นตอนสุดท้ายในกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="e94de-149">This is the last step in this procedure.</span></span>  

