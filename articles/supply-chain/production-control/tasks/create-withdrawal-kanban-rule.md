--- 
title: "สร้างกฎคัมบังการเบิกถอน"
description: "กระบวนงานนี้แสดงการตั้งค่าที่จำเป็นในการสร้างกฎคัมบังการถอน สำหรับการโอนย้ายวัสดุในสภาพแวดล้อมแบบลีน "
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b0c1f0f4ea3035ffb7c5a12c83c12a132cc65fd5
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="c92da-103">สร้างกฎคัมบังการเบิกถอน</span><span class="sxs-lookup"><span data-stu-id="c92da-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c92da-104">กระบวนงานนี้แสดงการตั้งค่าที่จำเป็นในการสร้างกฎคัมบังการถอน สำหรับการโอนย้ายวัสดุในสภาพแวดล้อมแบบลีน </span><span class="sxs-lookup"><span data-stu-id="c92da-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="c92da-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c92da-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c92da-106">กระบวนงานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เนื่องจากพวกเขาจัดเตรียมการเพิ่มเติมสินค้าหรือวัสดุที่มีการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c92da-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="c92da-107">สร้างกฎคัมบังใหม่</span><span class="sxs-lookup"><span data-stu-id="c92da-107">Create new kanban rule</span></span>
1. <span data-ttu-id="c92da-108">ไปที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="c92da-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="c92da-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c92da-109">Click New.</span></span>
3. <span data-ttu-id="c92da-110">ในฟิลด์ชนิด เลือก 'การถอน'</span><span class="sxs-lookup"><span data-stu-id="c92da-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="c92da-111">ชนิดการถอนถูกใช้สำหรับกฎคัมบัง เพื่อโอนย้ายวัสดุหรือสินค้า</span><span class="sxs-lookup"><span data-stu-id="c92da-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="c92da-112">ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c92da-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c92da-113">เลือก ReplenishSpeakerComponents </span><span class="sxs-lookup"><span data-stu-id="c92da-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="c92da-114">กิจกรรมนี้ถูกตั้งขึ้นเพื่อย้ายส่วนประกอบจากคลังสินค้า 11 สถานที่ 11 ไปยังคลังสินค้า 12 สถานที่ 12</span><span class="sxs-lookup"><span data-stu-id="c92da-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="c92da-115">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c92da-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="c92da-116">เลือก M0007</span><span class="sxs-lookup"><span data-stu-id="c92da-116">Select M0007.</span></span>  
6. <span data-ttu-id="c92da-117">ในฟิลด์ระยะเวลารอคอยสินค้า ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="c92da-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="c92da-118">ตัวอย่างเช่น 60</span><span class="sxs-lookup"><span data-stu-id="c92da-118">For example, 60.</span></span>  
7. <span data-ttu-id="c92da-119">ในฟิลด์หน่วยวัด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c92da-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="c92da-120">ตัวอย่างเช่น นาที</span><span class="sxs-lookup"><span data-stu-id="c92da-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="c92da-121">ตั้งค่าปริมาณสำหรับคัมบัง</span><span class="sxs-lookup"><span data-stu-id="c92da-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="c92da-122">กำหนดปริมาณเริ่มต้นเป็น '5'</span><span class="sxs-lookup"><span data-stu-id="c92da-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="c92da-123">นี่คือปริมาณที่จะถูกโอนย้ายสำหรับแต่ละคัมบัง</span><span class="sxs-lookup"><span data-stu-id="c92da-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="c92da-124">ในฟิลด์ปริมาณตามระบบคัมบังแบบคงที่ ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="c92da-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="c92da-125">จำนวนของคัมบังที่ควรเปิดใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="c92da-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="c92da-126">ในกรณีนี้ คัมบัง 2 รายการ ซึ่งแต่ละรายการโอนย้าย 5 รายการ</span><span class="sxs-lookup"><span data-stu-id="c92da-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="c92da-127">ในฟิลด์ค่าต่ำสุดของขอบเขตการแจ้งเตือน ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="c92da-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="c92da-128">ใช้เพื่อติดตามจำนวนเงินต่ำสุดของคัมบังทั้งหมดซึ่งควรอยู่ที่ปลายทาง </span><span class="sxs-lookup"><span data-stu-id="c92da-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="c92da-129">ตัวอย่างเช่น นี่จะถูกใช้ในภาพรวมของปริมาณคัมบัง</span><span class="sxs-lookup"><span data-stu-id="c92da-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="c92da-130">ในฟิลด์ค่าสูงสุดของขอบเขตการแจ้งเตือน ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="c92da-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="c92da-131">ใช้เพื่อติดตามจำนวนเงินสูงสุดของคัมบังทั้งหมดซึ่งควรอยู่ที่ปลายทาง </span><span class="sxs-lookup"><span data-stu-id="c92da-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="c92da-132">ตัวอย่างเช่น นี่จะถูกใช้ในภาพรวมของปริมาณคัมบัง</span><span class="sxs-lookup"><span data-stu-id="c92da-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="c92da-133">สร้างคัมบัง</span><span class="sxs-lookup"><span data-stu-id="c92da-133">Create kanbans</span></span>
1. <span data-ttu-id="c92da-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c92da-134">Click Save.</span></span>
    * <span data-ttu-id="c92da-135">กฎคัมบังจำเป็นต้องถูกบันทึกก่อนจึงจะสามารถสร้างคัมบังได้</span><span class="sxs-lookup"><span data-stu-id="c92da-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="c92da-136">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="c92da-136">Click Add.</span></span>
    * <span data-ttu-id="c92da-137">หมายเหตุว่า ไม่มีคัมบังที่ใช้งานอยู่ เนื่องจาก 'จำนวนของคัมบังใหม่' ที่แนะนำคือ 2 ซึ่งเท่ากับ 'คัมบังแบบปริมาณคงที่'</span><span class="sxs-lookup"><span data-stu-id="c92da-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="c92da-138">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c92da-138">Click Create.</span></span>
    * <span data-ttu-id="c92da-139">นี่จะสร้างสองคัมบัง</span><span class="sxs-lookup"><span data-stu-id="c92da-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="c92da-140">หมายเหตุว่า คัมบัง 2 คัมบังสำหรับแต่ละ 5 รายการ ถูกสร้างขึ้นสำหรับกฎคัมบังการถอน </span><span class="sxs-lookup"><span data-stu-id="c92da-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="c92da-141">นี่เป็นขั้นตอนสุดท้ายในกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="c92da-141">This is the last step in this procedure.</span></span>  


