--- 
title: "สร้างกฏคัมบังโดยใช้อีเว้นท์รายการคัมบัง"
description: "กระบวนงานนี้สร้างกฎคัมบังโดยใช้การตั้งค่าเหตุการณ์รายการคัมบังเพื่อทริกเกอร์การดึงจากกิจกรรมกระบวนการ "
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.openlocfilehash: 9d2c2fbd223bd2b410e4a5db87ec468eb25dc87f
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="07618-103">สร้างกฏคัมบังโดยใช้อีเว้นท์รายการคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-103">Create a kanban rule using a kanban line event</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07618-104">กระบวนงานนี้สร้างกฎคัมบังโดยใช้การตั้งค่าเหตุการณ์รายการคัมบังเพื่อทริกเกอร์การดึงจากกิจกรรมกระบวนการ </span><span class="sxs-lookup"><span data-stu-id="07618-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="07618-105">กฎคัมบังจะถูกทริกเกอร์โดยกิจกรรมกระบวนการคัมบังที่มีปริมาณเท่ากับหรือมากกว่า 25 สำหรับแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="07618-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="07618-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="07618-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="07618-107">งานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เนื่องจากเป็นผู้จัดเตรียมการผลิตผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยนในสภาพแวดล้อมแบบลีน</span><span class="sxs-lookup"><span data-stu-id="07618-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="07618-108">สร้างกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-108">Create a kanban rule</span></span>
1. <span data-ttu-id="07618-109">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="07618-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="07618-110">Click New.</span></span>
3. <span data-ttu-id="07618-111">ในฟิลด์กลยุทธ์การเติมสินค้า ให้เลือก 'เหตุการณ์'</span><span class="sxs-lookup"><span data-stu-id="07618-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="07618-112">ขั้นตอนนี้จะเป็นการสร้างคัมบังโดยตรงตามความต้องการ </span><span class="sxs-lookup"><span data-stu-id="07618-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="07618-113">ใช้ในการตั้งค่ากฎที่กำหนดในสถานการณ์จำลองตามสั่ง</span><span class="sxs-lookup"><span data-stu-id="07618-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="07618-114">ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="07618-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="07618-115">ป้อนหรือเลือก SpeakerAssemblyAndPolish </span><span class="sxs-lookup"><span data-stu-id="07618-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="07618-116">กิจกรรมแรกของกฎคัมบังการผลิตคือกิจกรรมกระบวนการในขั้นตอนการผลิต </span><span class="sxs-lookup"><span data-stu-id="07618-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="07618-117">เมื่อคุณเลือกกิจกรรม วันที่มีผลบังคับใช้ของกิจกรรมจะถูกคัดลอกไปยังวันที่สิ้นสุดของกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="07618-118">ขยายส่วนรายละเอียด </span><span class="sxs-lookup"><span data-stu-id="07618-118">Expand the Details section.</span></span>
6. <span data-ttu-id="07618-119">ในฟิลด์ผลิตภัณฑ์ ให้พิมพ์ 'L0001'</span><span class="sxs-lookup"><span data-stu-id="07618-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="07618-120">ขยายส่วนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="07618-120">Expand the Events section.</span></span>
8. <span data-ttu-id="07618-121">ในฟิลด์เหตุการณ์รายการคัมบัง ให้เลือก 'อัตโนมัติ'</span><span class="sxs-lookup"><span data-stu-id="07618-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="07618-122">ขั้นตอนนี้จะเป็นการสร้างคัมบังเหตุการณ์ตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="07618-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="07618-123">ฟิลด์นี้จะใช้ในการตั้งค่าคอนฟิกกฎคัมบังที่เพิ่มเติมวัสดุที่จำเป็นสำหรับกิจกรรมขั้นตอนปลายน้ำ </span><span class="sxs-lookup"><span data-stu-id="07618-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="07618-124">เมื่อคุณเลือกโดยอัตโนมัติ จะมีการสร้างคัมบังเหตุการณ์ตามความต้องการ </span><span class="sxs-lookup"><span data-stu-id="07618-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="07618-125">เราแนะนำการตั้งค่านี้ถ้าคุณคาดว่าจะดำเนินการผลิตในวันเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="07618-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="07618-126">กำหนดปริมาณเหตุการณ์ต่ำสุดไปที่ '25'</span><span class="sxs-lookup"><span data-stu-id="07618-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="07618-127">คัมบังเหตุการณ์ถูกสร้างขึ้นเมื่อปริมาณความต้องการเท่ากับหรือเกินกว่าฟิลด์นี้ </span><span class="sxs-lookup"><span data-stu-id="07618-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="07618-128">ซึ่งมีประโยชน์ถ้าคุณต้องการผลิตปริมาณการสั่งซื้อน้อยกว่าฟิลด์นี้บนเครื่องเดียวและมากกว่าฟิลด์นี้บนเครื่องอื่น</span><span class="sxs-lookup"><span data-stu-id="07618-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="07618-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="07618-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="07618-130">สร้างใบสั่งขายและทริกเกอร์ห่วงโซ่คัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="07618-131">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="07618-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="07618-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="07618-132">Click New.</span></span>
3. <span data-ttu-id="07618-133">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="07618-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="07618-134">เลือกบัญชีลูกค้า US-003, Forest Wholesales</span><span class="sxs-lookup"><span data-stu-id="07618-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="07618-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="07618-135">Click OK.</span></span>
5. <span data-ttu-id="07618-136">ในฟิลด์ หมายเลขสินค้า ให้พิมพ์ 'L0001'</span><span class="sxs-lookup"><span data-stu-id="07618-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="07618-137">L0001 คือสินค้าที่คุณสร้างกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="07618-138">กำหนดปริมาณเป็น '27'</span><span class="sxs-lookup"><span data-stu-id="07618-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="07618-139">เนื่องจาก 27 มากกว่าปริมาณต่ำสุดที่ 25 ในกฎคัมบัง ระบบจะทริกเกอร์คัมบังเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="07618-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="07618-140">ในฟิลด์ไซต์ ให้พิมพ์ '1'</span><span class="sxs-lookup"><span data-stu-id="07618-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="07618-141">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="07618-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="07618-142">เลือก คลังสินค้า 13</span><span class="sxs-lookup"><span data-stu-id="07618-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="07618-143">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="07618-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="07618-144">ดูคัมบังที่สร้างขึ้นโดยกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="07618-145">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="07618-146">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="07618-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="07618-147">ขยายส่วนคัมบัง</span><span class="sxs-lookup"><span data-stu-id="07618-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="07618-148">โปรดสังเกตว่ามีการสร้างคัมบังสำหรับ 27 เพื่อประมวลผลกิจกรรมโดยยึดตามกฎคัมบังที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="07618-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="07618-149">นี่เป็นขั้นตอนสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="07618-149">This is the last step.</span></span>  


