--- 
title: "สร้างกฎคัมบังแบบปริมาณคงที่สำหรับการผลิต"
description: "ขั้นตอนนี้มุ่งเน้นการตั้งค่าที่จำเป็นเพื่อสร้างกฎคัมบังการผลิตคงสำหรับกิจกรรมการแปลงทริกเกอร์ ด้านเซลล์ทำงานในสภาพแวดล้อมแบบลีน "
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: a4ee8161803fc64e254b165ab8b8baac5dbaf0a2
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="6e936-103">สร้างกฎคัมบังแบบปริมาณคงที่สำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="6e936-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e936-104">ขั้นตอนนี้มุ่งเน้นการตั้งค่าที่จำเป็นเพื่อสร้างกฎคัมบังการผลิตคงสำหรับกิจกรรมการแปลงทริกเกอร์ ด้านเซลล์ทำงานในสภาพแวดล้อมแบบลีน </span><span class="sxs-lookup"><span data-stu-id="6e936-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="6e936-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="6e936-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e936-106">ขั้นตอนนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสตรีมค่า ตามที่พวกเขาจัดเตรียมการผลิตสำหรับผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="6e936-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="6e936-107">สร้างกฎคัมบังใหม่</span><span class="sxs-lookup"><span data-stu-id="6e936-107">Create new kanban rule</span></span>
1. <span data-ttu-id="6e936-108">ไปที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="6e936-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="6e936-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6e936-109">Click New.</span></span>
    * <span data-ttu-id="6e936-110">โปรดสังเกตว่าค่าเริ่มต้นคือการผลิตและกลยุทธ์การเติมสินค้านั้นคงที่ </span><span class="sxs-lookup"><span data-stu-id="6e936-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="6e936-111">คุณไม่จำเป็นต้องเปลี่ยนพารามิเตอร์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6e936-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="6e936-112">ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6e936-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="6e936-113">นี่คือกิจกรรมที่จะดำเนินการสำหรับคัมบังที่สร้างขึ้นตามกฎคัมบังนี้ </span><span class="sxs-lookup"><span data-stu-id="6e936-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="6e936-114">เลือก 'SpeakerTestAndPackaging'</span><span class="sxs-lookup"><span data-stu-id="6e936-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="6e936-115">ขยายส่วนรายละเอียด </span><span class="sxs-lookup"><span data-stu-id="6e936-115">Expand the Details section.</span></span>
5. <span data-ttu-id="6e936-116">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6e936-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="6e936-117">เลือก L0050</span><span class="sxs-lookup"><span data-stu-id="6e936-117">Select L0050.</span></span>  
6. <span data-ttu-id="6e936-118">ในฟิลด์หน่วยวัด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6e936-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="6e936-119">เลือกนาที</span><span class="sxs-lookup"><span data-stu-id="6e936-119">Select minutes.</span></span>  
7. <span data-ttu-id="6e936-120">ในฟิลด์ระยะเวลารอคอยสินค้า ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6e936-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="6e936-121">ป้อน 5</span><span class="sxs-lookup"><span data-stu-id="6e936-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="6e936-122">กำหนดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6e936-122">Set quantities</span></span>
1. <span data-ttu-id="6e936-123">ขยายส่วนปริมาณ </span><span class="sxs-lookup"><span data-stu-id="6e936-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="6e936-124">กำหนดปริมาณเริ่มต้นเป็น '10'</span><span class="sxs-lookup"><span data-stu-id="6e936-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="6e936-125">นี่คือปริมาณที่จะถูกโอนย้ายสำหรับแต่ละคัมบัง</span><span class="sxs-lookup"><span data-stu-id="6e936-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="6e936-126">เลือกกล่องกาเครื่องหมายของผลต่างปริมาณผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6e936-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="6e936-127">ด้วยอย่างนี้ คัมบังที่ถูกเลือกจะสามารถเสร็จสมบูรณ์โดยมีผลต่างจากปริมาณเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="6e936-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="6e936-128">เพื่ออนุญาตให้คัมบังเสร็จสมบูรณ์ด้วยปริมาณจาก 8 ถึง 12 ตั้งค่าทั้งสองผลต่างเป็น 2</span><span class="sxs-lookup"><span data-stu-id="6e936-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="6e936-129">ตั้งค่าผลต่างต่ำกว่า '2'</span><span class="sxs-lookup"><span data-stu-id="6e936-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="6e936-130">นี่จะอนุญาติให้เสร็จสมบูรณ์ลงจนถึง 10-2 = 8</span><span class="sxs-lookup"><span data-stu-id="6e936-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="6e936-131">ตั้งค่าผลต่างสูงกว่า '2'</span><span class="sxs-lookup"><span data-stu-id="6e936-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="6e936-132">นี่จะอนุญาติให้เสร็จสมบูรณ์ขึ้นจนถึง 10-2 = 12</span><span class="sxs-lookup"><span data-stu-id="6e936-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="6e936-133">ในฟิลด์ปริมาณตามระบบคัมบังแบบคงที่ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6e936-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="6e936-134">จำนวนของคัมบังที่ควรเปิดใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="6e936-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="6e936-135">ในกรณีนี้ 5 คัมบังประมวลผลแต่ละ 10</span><span class="sxs-lookup"><span data-stu-id="6e936-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="6e936-136">ในฟิลด์ค่าต่ำสุดของขอบเขตการแจ้งเตือน ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="6e936-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="6e936-137">ใช้เพื่อติดตามจำนวนเงินต่ำสุดของคัมบังทั้งหมดซึ่งควรอยู่ที่ปลายทาง </span><span class="sxs-lookup"><span data-stu-id="6e936-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="6e936-138">ตัวอย่างเช่น นี่จะถูกใช้ในภาพรวมของปริมาณคัมบัง</span><span class="sxs-lookup"><span data-stu-id="6e936-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="6e936-139">ในฟิลด์ค่าสูงสุดของขอบเขตการแจ้งเตือน ให้ป้อน '4'</span><span class="sxs-lookup"><span data-stu-id="6e936-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="6e936-140">ใช้เพื่อติดตามจำนวนเงินสูงสุดของคัมบังทั้งหมดซึ่งควรอยู่ที่ปลายทาง </span><span class="sxs-lookup"><span data-stu-id="6e936-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="6e936-141">ตัวอย่างเช่น นี่จะถูกใช้ในภาพรวมของปริมาณคัมบัง</span><span class="sxs-lookup"><span data-stu-id="6e936-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="6e936-142">ในฟิลด์ปริมาณการวางแผนอัตโนมัติ ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="6e936-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="6e936-143">การตั้งค่านี้เป็น 1 หมายถึงทุกคัมบังจะถูกวางแผนโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="6e936-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="6e936-144">หากเราป้อน 3 คัมบังจะไม่สามารถวางแผนจนกว่า 3 คัมบังจะว่างพร้อมสำหรับการวางแผน </span><span class="sxs-lookup"><span data-stu-id="6e936-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="6e936-145">ซึ่งมีประโยชน์สำหรับการจัดกลุ่มงาน และหลีกเลี่ยงการใช้การตั้งค่ามากเกินไป</span><span class="sxs-lookup"><span data-stu-id="6e936-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="6e936-146">สร้างคัมบัง</span><span class="sxs-lookup"><span data-stu-id="6e936-146">Create Kanbans</span></span>
1. <span data-ttu-id="6e936-147">ขยายส่วนคัมบัง</span><span class="sxs-lookup"><span data-stu-id="6e936-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="6e936-148">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6e936-148">Click Save.</span></span>
    * <span data-ttu-id="6e936-149">กฎคัมบังจำเป็นต้องถูกบันทึกก่อนจึงจะสามารถสร้างคัมบังได้</span><span class="sxs-lookup"><span data-stu-id="6e936-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="6e936-150">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6e936-150">Click Add.</span></span>
    * <span data-ttu-id="6e936-151">หมายเหตุว่าไม่มีคัมบังที่ใช้งานอยู่เนื่องจากสิ่งนี้แนะนำ 'จำนวนของคัมบังใหม่' เป็น 5</span><span class="sxs-lookup"><span data-stu-id="6e936-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="6e936-152">สิ่งนี้เท่ากับ 'ปริมาณตามระบบคัมบังคงที่'</span><span class="sxs-lookup"><span data-stu-id="6e936-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="6e936-153">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6e936-153">Click Create.</span></span>
    * <span data-ttu-id="6e936-154">สิ่งนี้จะสร้าง 5 คัมบัง</span><span class="sxs-lookup"><span data-stu-id="6e936-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="6e936-155">โปรดทราบว่า 5 คัมบังสำหรับแต่ละ 10 ถูกสร้างสำหรับกฎคัมบังการผลิต </span><span class="sxs-lookup"><span data-stu-id="6e936-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="6e936-156">นี่เป็นขั้นตอนสุดท้ายในกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="6e936-156">This is the last step in this procedure.</span></span>  


