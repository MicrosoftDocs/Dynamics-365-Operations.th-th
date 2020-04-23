---
title: สร้างกฏคัมบังโดยใช้อีเว้นท์ของสินค้าคงคลังต่ำสุด
description: 'กระบวนงานนี้มุ่งเน้นการตั้งค่าที่จำเป็นสำหรับการสร้างกฎคัมบังโดยใช้เหตุการณ์ของสินค้าคงคลังต่ำสุดเพื่อให้แน่ใจว่าผลิตภัณฑ์เฉพาะจะพร้อมใช้งานเสมอที่สถานที่เฉพาะ '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b295000e132b8551045520df1af55a37673f131d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212261"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="3f1c7-103">สร้างกฏคัมบังโดยใช้อีเว้นท์ของสินค้าคงคลังต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="3f1c7-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f1c7-104">กระบวนงานนี้มุ่งเน้นการตั้งค่าที่จำเป็นสำหรับการสร้างกฎคัมบังโดยใช้เหตุการณ์ของสินค้าคงคลังต่ำสุดเพื่อให้แน่ใจว่าผลิตภัณฑ์เฉพาะจะพร้อมใช้งานเสมอที่สถานที่เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="3f1c7-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="3f1c7-105">มีการสร้างกฎคัมบังเพื่อโอนย้ายวัสดุไปยังสถานที่เมื่อระดับสินค้าคงคลังลดลงต่ำกว่า 200 ชิ้น </span><span class="sxs-lookup"><span data-stu-id="3f1c7-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="3f1c7-106">โดยการรันการประมวลผลเหตุการณ์การเชื่อมโยงความต้องการกับการจัดซื้อ จะมีการสร้างคัมบังที่จำเป็นขึ้น </span><span class="sxs-lookup"><span data-stu-id="3f1c7-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="3f1c7-107">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="3f1c7-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="3f1c7-108">งานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เนื่องจากเป็นผู้จัดเตรียมการผลิตผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยนในสภาพแวดล้อมแบบลีน</span><span class="sxs-lookup"><span data-stu-id="3f1c7-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="3f1c7-109">สร้างกฎคัมบังใหม่</span><span class="sxs-lookup"><span data-stu-id="3f1c7-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="3f1c7-110">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="3f1c7-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-111">Click New.</span></span>
3. <span data-ttu-id="3f1c7-112">ในฟิลด์ชนิด เลือก 'การถอน'</span><span class="sxs-lookup"><span data-stu-id="3f1c7-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="3f1c7-113">ชนิดนี้จะใช้เพื่อสร้างคัมบังการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="3f1c7-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="3f1c7-114">ในฟิลด์กลยุทธ์การเติมสินค้า ให้เลือก 'เหตุการณ์'</span><span class="sxs-lookup"><span data-stu-id="3f1c7-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="3f1c7-115">กลยุทธ์เหตุการณ์จะใช้เพื่อสร้างคัมบังการโอนย้ายตามเหตุการณ์ </span><span class="sxs-lookup"><span data-stu-id="3f1c7-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="3f1c7-116">ภายหลังในกระบวนงานนี้ คุณจะทริกเกอร์คัมบังการโอนย้ายโดยใช้การเติมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="3f1c7-117">ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="3f1c7-118">ป้อนหรือเลือก ReplenishSpeakerComponents </span><span class="sxs-lookup"><span data-stu-id="3f1c7-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="3f1c7-119">กิจกรรมการโอนย้ายนี้มีคลังสินค้าที่รับสินค้า (ผลลัพธ์) และสถานที่ 12 ซึ่งหมายถึงวัสดุจะถูกย้ายไปยังสถานที่ 12 ในคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="3f1c7-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="3f1c7-120">ขยายส่วนรายละเอียด </span><span class="sxs-lookup"><span data-stu-id="3f1c7-120">Expand the Details section.</span></span>
7. <span data-ttu-id="3f1c7-121">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="3f1c7-122">เลือก M0007</span><span class="sxs-lookup"><span data-stu-id="3f1c7-122">Select M0007.</span></span>  
8. <span data-ttu-id="3f1c7-123">ขยายส่วนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="3f1c7-123">Expand the Events section.</span></span>
9. <span data-ttu-id="3f1c7-124">ในฟิลด์เหตุการณ์การเติมสินค้าคงคลัง ให้เลือก 'ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="3f1c7-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="3f1c7-125">วิธีนี้จะเป็นการสร้างคัมบังเพื่อตอบสนองความต้องการทางวัสดุที่สถานที่ที่เกี่ยวข้องในระหว่างการประมวลผลเหตุการณ์การเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="3f1c7-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="3f1c7-126">ตั้งค่าปริมาณขั้นต่ำของสินค้า</span><span class="sxs-lookup"><span data-stu-id="3f1c7-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="3f1c7-127">คลิกเพื่อติดตามลิงค์ในฟิลด์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3f1c7-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="3f1c7-128">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="3f1c7-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="3f1c7-129">ขยายกล่องแสดงข้อมูลย่อรูปภาพผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3f1c7-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="3f1c7-130">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="3f1c7-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="3f1c7-131">คลิกความครอบคลุมสินค้า</span><span class="sxs-lookup"><span data-stu-id="3f1c7-131">Click Item coverage.</span></span>
6. <span data-ttu-id="3f1c7-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-132">Click New.</span></span>
7. <span data-ttu-id="3f1c7-133">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3f1c7-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="3f1c7-134">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="3f1c7-135">เซ็ตคลังสินค้าไปที่ 12</span><span class="sxs-lookup"><span data-stu-id="3f1c7-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="3f1c7-136">ตั้งค่าน้อยที่สุดเป็น '200'</span><span class="sxs-lookup"><span data-stu-id="3f1c7-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="3f1c7-137">รันงานการสร้างเหตุการณ์ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3f1c7-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="3f1c7-138">ไปที่ การควบคุมการผลิต > งานประจำงวด > การประมวลผลชุดงานคัมบัง > การประมวลผลเหตุการณ์การเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="3f1c7-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="3f1c7-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-139">Click OK.</span></span>
3. <span data-ttu-id="3f1c7-140">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="3f1c7-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3f1c7-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3f1c7-142">เลือกกฎคัมบังที่คุณสร้างก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="3f1c7-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="3f1c7-143">ขยายส่วนคัมบัง</span><span class="sxs-lookup"><span data-stu-id="3f1c7-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="3f1c7-144">โปรดสังเกตว่ามีการสร้างคัมบังเพื่อโอนย้ายวัสดุที่จำเป็นไปยังคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="3f1c7-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

