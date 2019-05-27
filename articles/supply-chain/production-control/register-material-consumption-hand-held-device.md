---
title: ลงทะเบียนปริมาณการใช้วัสดุโดยใช้อุปกรณ์เคลื่อนที่
description: หัวข้อนี้อธิบาย ลำดับงานที่เปิดใช้งานการลงทะเบียนของปริมาณการใช้วัตถุดิบในการผลิต โดยใช้อุปกรณ์มือถือ
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5b9c73cf9b23eb8ad9ed872b76b92b395609e9a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571034"
---
# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="b9c60-103">ลงทะเบียนปริมาณการใช้วัสดุโดยใช้อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="b9c60-103">Register material consumption using a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9c60-104">หัวข้อนี้อธิบาย ลำดับงานที่เปิดใช้งานการลงทะเบียนของปริมาณการใช้วัตถุดิบในการผลิต โดยใช้อุปกรณ์มือถือ</span><span class="sxs-lookup"><span data-stu-id="b9c60-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="b9c60-105">คำนำ</span><span class="sxs-lookup"><span data-stu-id="b9c60-105">Introduction</span></span>
------------

<span data-ttu-id="b9c60-106">เวิร์กโฟลว์นี้เกี่ยวข้อง ถ้ามีข้อกำหนดที่เคร่งครัดสำหรับความสามารถในการสอบกลับของวัสดุ</span><span class="sxs-lookup"><span data-stu-id="b9c60-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="b9c60-107">ในกรณี เพื่อรักษาความสามารถในการติดตามของวัสดุ เวลาและปริมาณที่แน่นอนต้องถูกรายงานสำหรับปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="b9c60-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="b9c60-108">กระบวนการนี้สามารถมองเห็นได้โดยตรงกันข้ามกับการดำเนินการล่วงหน้า หรือลบรายการย้อนหลัง ที่ซึ่งมีการออฟเซตระหว่างเวลาของการลงทะเบียนและเวลาเมื่อปริมาณการใช้จริงเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="b9c60-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="b9c60-109">นี่อธิบายว่าเพราะเหตุใดจึงไม่สามารถใช้กลยุทธ์ของปริมาณการใช้อัตโนมัติ สำหรับวัสดุบางอย่างที่มีข้อกำหนดของความสามารถในการติดตามได้</span><span class="sxs-lookup"><span data-stu-id="b9c60-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="b9c60-110">ลองดูที่สถานการณ์จำลองอย่างง่ายที่อธิบายวิธีการตั้งค่าเวิร์กโฟลว์ เพื่อเปิดใช้งานการลงทะเบียนของการใช้วัตถุดิบในการผลิตโดยใช้อุปกรณ์มือถือ</span><span class="sxs-lookup"><span data-stu-id="b9c60-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="b9c60-111">[![ตั้งค่าเวิร์กโฟลว์เพื่อเปิดใช้งานการลงทะเบียนของการใช้วัตถุดิบในการผลิตโดยใช้อุปกรณ์มือถือ](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="b9c60-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="b9c60-112">รายละเอียดของสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="b9c60-112">Scenario details</span></span>

<span data-ttu-id="b9c60-113">กระบวนการผลิตแบบต่อเนื่อง (5) ใช้วัตถุดิบที่ควบคุมชุดงาน RM-100</span><span class="sxs-lookup"><span data-stu-id="b9c60-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="b9c60-114">วัสดุจะคงเหลือในสถานที่เก็บสินค้า Bulk-001 (1) บนป้ายทะเบียน PL-1 ที่มีสองชุด B1 และ B2 ทั้งสองอย่างที่มีปริมาณ 100 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="b9c60-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="b9c60-115">งานคลังสินค้า (2) ถูกนำออกใช้และประมวลผลสำหรับ RM-100 และวัสดุจะถูกเบิกจาก Bulk-001 ไปยังสถานที่ตั้งอินพุทการผลิต PIL-01 (3) ซึ่งถูกกำหนดป้ายที่มีการควบคุมที่ไม่ได้ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="b9c60-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="b9c60-116">พนักงานควบคุมเครื่องจักรชั่งน้ำหนักวัสดุจากสถานที่ตั้งอินพุทการผลิต (3) และลงทะเบียนน้ำหนักและหมายเลขชุดงานเป็นใช้งานแล้ว (4)</span><span class="sxs-lookup"><span data-stu-id="b9c60-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="b9c60-117">จากสถานที่ตั้งอินพุทการผลิต วัสดุบางส่วนถูกเพิ่มด้วยตนเองไปยังกระบวนการผลิตในช่วงเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="b9c60-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="b9c60-118">เมื่อพนักงานควบคุมเครื่องจักรเพิ่มวัตถุดิบ จะมีการชั่งน้ำหนักบนเครื่องชั่ง และมีการลงทะเบียนหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9c60-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-theworkflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="b9c60-119">ตั้งค่าเวิร์กโฟลว์เพื่อลงทะเบียนการใช้โดยใช้อุปกรณ์มือถือ</span><span class="sxs-lookup"><span data-stu-id="b9c60-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="b9c60-120">สร้างผลิตภัณฑ์สำเร็จรูป FG-100 ที่มีสูตรการผลิตที่มีวัตถุดิบที่ควบคุมชุดงาน RM-100</span><span class="sxs-lookup"><span data-stu-id="b9c60-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="b9c60-121">เพิ่มชุดงานสองชุด B1 และ B2 ของ RM-100 ในปริมาณ 100 ไปยังสถานที่: กลุ่ม-001 บนแผ่นป้ายทะเบียน: PL-1</span><span class="sxs-lookup"><span data-stu-id="b9c60-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="b9c60-122">หลักการตัดจ่ายในรายการวัสดุและส่วนประกอบสำหรับ RM-100 ถูกตั้งค่าเป็น **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="b9c60-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="b9c60-123">ตั้งค่าสถานที่อินพุตของการผลิตเป็น PIL-01</span><span class="sxs-lookup"><span data-stu-id="b9c60-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="b9c60-124">คุณสามารถทำได้ โดยการเลือกตำแหน่งที่ตั้งนี้เป็นสถานที่ตั้งอินพุทการผลิตเริ่มต้นในคลังสินค้า 51</span><span class="sxs-lookup"><span data-stu-id="b9c60-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="b9c60-125">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่ใหม่:</span><span class="sxs-lookup"><span data-stu-id="b9c60-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="b9c60-126">**ชื่อรายการเมนู** - ลงทะเบียนการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="b9c60-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="b9c60-127">**ชื่อเรื่อง** - ลงทะเบียนปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="b9c60-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="b9c60-128">**โหมด** - ทางอ้อม</span><span class="sxs-lookup"><span data-stu-id="b9c60-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="b9c60-129">**รหัสกิจกรรม** - ลงทะเบียนการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="b9c60-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="b9c60-130">เพิ่มรายการเมนูไปยังเมนูอุปกรณ์ **การผลิตแบบเคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="b9c60-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="b9c60-131">สร้างใบสั่งผลิตสำหรับสินค้าสำเร็จรูป:</span><span class="sxs-lookup"><span data-stu-id="b9c60-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="b9c60-132">**หมายเลขสินค้า** - FG-100</span><span class="sxs-lookup"><span data-stu-id="b9c60-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="b9c60-133">**ไซต์** - 5</span><span class="sxs-lookup"><span data-stu-id="b9c60-133">**Site** - 5</span></span> 
-    <span data-ttu-id="b9c60-134">**คลังสินค้า** - 51</span><span class="sxs-lookup"><span data-stu-id="b9c60-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="b9c60-135">**ปริมาณ** - 150</span><span class="sxs-lookup"><span data-stu-id="b9c60-135">**Quantity** - 150</span></span>

<span data-ttu-id="b9c60-136">ใบสั่งผลิตถูก **ประเมิน** และ **นำออกใช้** และมีการสร้างงานของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b9c60-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="b9c60-137">ทำงานให้เสร็จสมบูรณ์ โดยใช้ลำดับงานสำหรับการเบิกวัตถุดิบสำหรับอุปกรณ์มือถือ</span><span class="sxs-lookup"><span data-stu-id="b9c60-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="b9c60-138">ซึ่งจะนำวัสดุจากสถานที่เก็บสินค้าจำนวนมากไปยังสถานที่ตั้งอินพุทการผลิต PIL-01</span><span class="sxs-lookup"><span data-stu-id="b9c60-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="b9c60-139">หลังจากที่งานเสร็จสิ้น วัสดุมีสถานะ **เลือกในสถานที่อินพุตของการผลิต**</span><span class="sxs-lookup"><span data-stu-id="b9c60-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="b9c60-140">สถานะหลังจากดำเนินงานแล้วอาจเป็น **เบิกสินค้าแล้ว** หรือ **ถูกจองจริง** ได้</span><span class="sxs-lookup"><span data-stu-id="b9c60-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="b9c60-141">นี่ถูกตั้งค่าคอนฟิกด้วยพารามิเตอร์ **สถานะการออกใช้หลังจากการวางในแบบฟอร์มคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="b9c60-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="b9c60-142">เริ่มต้นใบสั่งผลิตจากไคลเอนต์ หรือจากอุปกรณ์มือถือ โดยใช้รายการเมนู **เริ่มต้นผลิต**</span><span class="sxs-lookup"><span data-stu-id="b9c60-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="b9c60-143">หลังจากที่มีการเริ่มต้นใบสั่งผลิต คุณสามารถลงทะเบียนปริมาณการใช้วัสดุที่มีลำดับงานสำหรับอุปกรณ์มือถือได้</span><span class="sxs-lookup"><span data-stu-id="b9c60-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="b9c60-144">ลองเริ่มต้นโดยการลงทะเบียนการใช้ 25 ปอนด์ของชุดงาน B1</span><span class="sxs-lookup"><span data-stu-id="b9c60-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="b9c60-145">เลือกรายการเมนู **ลงทะเบียนวัสดุ** **การใช้** ในเมนูสำหรับอุปกรณ์มือถือ ป้อนรายละเอียดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b9c60-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="b9c60-146">หมายเลขใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b9c60-146">The production order number.</span></span> 
-    <span data-ttu-id="b9c60-147">สถานที่ที่วัสดุจะถูกใช้ ในกรณีนี้ PIL-01</span><span class="sxs-lookup"><span data-stu-id="b9c60-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="b9c60-148">หมายเลขสินค้า RM-100</span><span class="sxs-lookup"><span data-stu-id="b9c60-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="b9c60-149">หมายเลขชุดงาน B1</span><span class="sxs-lookup"><span data-stu-id="b9c60-149">Batch number B1.</span></span> 
-    <span data-ttu-id="b9c60-150">ปริมาณ 25</span><span class="sxs-lookup"><span data-stu-id="b9c60-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="b9c60-151">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b9c60-151">Select **OK**.</span></span>

<span data-ttu-id="b9c60-152">โปรดทราบว่าข้อความ "บรรทัดสมุดรายวันถูกสร้าง" ปรากฏบนจอแสดงผล</span><span class="sxs-lookup"><span data-stu-id="b9c60-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="b9c60-153">ในใบสั่งผลิต มีสมุดรายวันที่เปิดของชนิด **รายการเบิกสินค้าการผลิต** สำหรับหมายเลขสินค้า RM-100 และหมายเลขชุดงาน B1</span><span class="sxs-lookup"><span data-stu-id="b9c60-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="b9c60-154">ขณะนี้คุณสามารถเลือกที่จะดำเนินการลงทะเบียนต่อได้ ตัวอย่างเช่น ในหมายเลขชุดงาน B2 และแต่ละครั้งที่คุณเลือก **ตกลง** รายการสมุดรายวันใหม่จะถูกเพิ่มไปยังสมุดรายวันเปิดไว้</span><span class="sxs-lookup"><span data-stu-id="b9c60-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="b9c60-155">หลังจากที่คุณได้เสร็จสิ้นการลงทะเบียนของคุณ เลือก **เสร็จสิ้น** เพื่อโพสต์สมุดรายวันและสิ้นสุดเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="b9c60-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="b9c60-156">ข้อคิดเห็นเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b9c60-156">Additional comments</span></span> 

-   <span data-ttu-id="b9c60-157">ถ้าผู้ใช้ยกเลิกเวิร์กโฟลว์หลังจากบรรทัดสมุดรายวันถูกสร้าง สมุดรายวันอยู่ในสถานะที่ยังไม่ได้โพสต์ แต่ถ้าผู้ใช้ในภายหลังใช้เวิร์กโฟลว์สำหรับใบสั่งผลิตเดียวกัน จากนั้นบรรทัดจะถูกเพิ่มไปยังสมุดรายวันที่เปิด มากกว่าที่จะไปยังสมุดรายวันใหม่</span><span class="sxs-lookup"><span data-stu-id="b9c60-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="b9c60-158">นอกจากนี้ เวิร์กโฟลว์ใหม่ยังสนับสนุนการลงทะเบียนของหมายเลขประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="b9c60-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="b9c60-159">ซึ่งเป็นไปได้เฉพาะการลงทะเบียนหมายเลขสินค้าที่กำหนดในสูตรการผลิต หรือสูตรสำหรับใบสั่งผลิตที่เลือก หรือใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9c60-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="b9c60-160">วัสดุสามารถถูกใช้งานมากเกินไปได้</span><span class="sxs-lookup"><span data-stu-id="b9c60-160">Material can be overconsumed.</span></span> <span data-ttu-id="b9c60-161">ตัวอย่างเช่น ถ้ามีการประเมินวัสดุที่จะใช้ด้วยปริมาณ 100 ปอนด์ จากนั้น จะสามารถถูกใช้งานมากเกินไปได้ด้วยปริมาณ ตัวอย่างเช่น 105 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="b9c60-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>


