---
title: สร้างกิจกรรมการโอนย้ายสำหรับ lean manufacturing
description: 'สร้างกิจกรรมการโอนย้ายสำหรับการผลิตแบบ lean '
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 04cb0afa74cb95acf4007e9292f9fb88d4c86f87
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837745"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="d2542-103">สร้างกิจกรรมการโอนย้ายสำหรับ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="d2542-103">Create transfer activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2542-104">สร้างกิจกรรมการโอนย้ายสำหรับการผลิตแบบ lean </span><span class="sxs-lookup"><span data-stu-id="d2542-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="d2542-105">ข้อกำหนดเบื้องต้น:</span><span class="sxs-lookup"><span data-stu-id="d2542-105">Prerequisites:</span></span> 

1. <span data-ttu-id="d2542-106">1 ต้องสร้างขั้นตอนการผลิตและเวอร์ชันที่ไม่ได้ใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="d2542-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="d2542-107">2. ต้องสร้างคลังสินค้าเริ่มต้นและสิ้นสุดและสถานที่เก็บ </span><span class="sxs-lookup"><span data-stu-id="d2542-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="d2542-108">-อีกอย่างหนึ่งควรสร้างการเติมสินค้าหรือการเติมเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d2542-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="d2542-109">ค้นหาเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="d2542-109">Find the production flow version</span></span>
1. <span data-ttu-id="d2542-110">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="d2542-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d2542-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2542-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2542-112">โปรดทราบว่าขั้นตอนการผลิตต้องมีเวอร์ชันในสถานะร่าง</span><span class="sxs-lookup"><span data-stu-id="d2542-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="d2542-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d2542-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="d2542-114">สร้างกิจกรรมใหม่</span><span class="sxs-lookup"><span data-stu-id="d2542-114">Create a new activity</span></span>
1. <span data-ttu-id="d2542-115">คลิกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="d2542-115">Click Activities.</span></span>
    * <span data-ttu-id="d2542-116">ตรวจสอบให้แน่ใจว่าขั้นตอนการผลิตที่เลือกมีเวอร์ชันในแบบร่าง และเลือกเวอร์ชันนั้น</span><span class="sxs-lookup"><span data-stu-id="d2542-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="d2542-117">คลิกสร้างกิจกรรมการวางแผนใหม่</span><span class="sxs-lookup"><span data-stu-id="d2542-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="d2542-118">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="d2542-118">Click Next.</span></span>
4. <span data-ttu-id="d2542-119">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d2542-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d2542-120">ในฟิลด์ชนิดของกิจกรรม ให้เลือก 'การโอนย้าย'</span><span class="sxs-lookup"><span data-stu-id="d2542-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="d2542-121">ในฟิลด์ปริมาณกระบวนการ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d2542-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="d2542-122">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="d2542-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="d2542-123">เลือกเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d2542-123">Select the Work cells</span></span>
1. <span data-ttu-id="d2542-124">ในฟิลด์การเติมสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d2542-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d2542-125">เมื่อต้องการใช้ที่ตั้งเอาท์พุทเซลล์ทำงานจากสถานที่ในกิจกรรมการโอนย้าย ให้เลือกเซลล์ทำงาน </span><span class="sxs-lookup"><span data-stu-id="d2542-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="d2542-126">เหมือนเดียวกันนั้นสามารถทำให้เสร็จด้วยกานเติมเซลล์ทำงาน ซึ่งกำหนดที่ตั้งเป้าหมายของกิจกรรมการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="d2542-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="d2542-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d2542-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="d2542-128">กำหนดการอัพเดตสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d2542-128">Define the inventory updates</span></span>
1. <span data-ttu-id="d2542-129">ในฟิลด์ชนิดของข้อมูลป้อนเข้า ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d2542-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="d2542-130">โปรดทราบว่า การโอนย้ายไม่ได้เปลี่ยนแปลงชนิดของผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="d2542-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="d2542-131">คุณสามารถโอนย้ายผลิตภัณฑ์สำเร็จรูปหรือผลิตภัณฑ์กึ่งสำเร็จรูป (การโอนย้ายระหว่างสองกิจกรรมของขั้นตอนการผลิต และอาจรวมถึงขั้นตอนคัมบัง) </span><span class="sxs-lookup"><span data-stu-id="d2542-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="d2542-132">เมื่อทำการโอนย้ายผลิตภัณฑ์สำเร็จรูป คุณสามารถเลือกว่าการเบิกหรือการรับจะส่งผลในธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d2542-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="d2542-133">กำหนดที่ตั้งการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="d2542-133">Define the transfer locations</span></span>
1. <span data-ttu-id="d2542-134">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="d2542-134">Click Next.</span></span>
2. <span data-ttu-id="d2542-135">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d2542-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d2542-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2542-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d2542-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d2542-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d2542-138">ในฟิลด์ตำแหน่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d2542-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d2542-139">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d2542-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d2542-140">ในฟิลด์ขนส่ง ให้เลือก 'ผู้จัดส่ง'</span><span class="sxs-lookup"><span data-stu-id="d2542-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="d2542-141">ตัวเลือกมีดังนี้: ผู้จัดส่ง - องค์กรที่ปฏิบัติงานคลังสินค้าจัดส่ง ผู้รับ - องค์กรที่ดำเนินการคลังสินค้าที่รับสินค้า ผู้ขนส่งสินค้า - ผู้จัดจำหน่ายบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="d2542-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="d2542-142">ถ้าองค์กรที่ปฏิบัติงานเป็นผู้จัดจำหน่าย กิจกรรมการโอนย้ายจำเป็นต้องมีข้อตกลงการรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="d2542-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="d2542-143">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="d2542-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="d2542-144">กำหนดเวลากิจกรรม</span><span class="sxs-lookup"><span data-stu-id="d2542-144">Define the activity times</span></span>
1. <span data-ttu-id="d2542-145">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2542-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2542-146">คำนิยามของรันไทม์จำเป็นต้องใช้ </span><span class="sxs-lookup"><span data-stu-id="d2542-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="d2542-147">รันไทม์ถูกใช้เพื่อคำนวณต้นทุนและเวลาสำหรับปริมาณที่สามารถประมวลผลได้ของงานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="d2542-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="d2542-148">รันไทม์ไม่ได้ใช้ในการคำนวณปริมาณการใช้กำลังการผลิต ซึ่งจะคำนวณโดยเวลาวงจรที่ได้รับมาจากงานเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="d2542-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="d2542-149">ในฟิลด์เวลา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d2542-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="d2542-150">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d2542-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="d2542-151">เลือกหน่วยเวลา</span><span class="sxs-lookup"><span data-stu-id="d2542-151">Select the Time unit.</span></span>
5. <span data-ttu-id="d2542-152">ในฟิลด์ต่อปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d2542-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="d2542-153">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2542-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2542-154">เวลาในการรอไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="d2542-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="d2542-155">ในฟิลด์เวลา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d2542-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="d2542-156">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d2542-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="d2542-157">เลือกหน่วยเวลา</span><span class="sxs-lookup"><span data-stu-id="d2542-157">Select the Time unit.</span></span>
10. <span data-ttu-id="d2542-158">ในฟิลด์ต่อปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d2542-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="d2542-159">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="d2542-159">Click Next.</span></span>
12. <span data-ttu-id="d2542-160">คลิก Finish</span><span class="sxs-lookup"><span data-stu-id="d2542-160">Click Finish.</span></span>
13. <span data-ttu-id="d2542-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d2542-161">Close the page.</span></span>

