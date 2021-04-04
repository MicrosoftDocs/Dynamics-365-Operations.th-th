---
title: สร้างกิจกรรมกระบวนการสำหรับ lean manufacturing
description: 'สร้างกิจกรรมกระบวนการสำหรับการผลิตแบบ lean '
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ef63faaf836c1ac929324d2b3cd4aaaee9b1352
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255120"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="f2e47-103">สร้างกิจกรรมกระบวนการสำหรับ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="f2e47-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2e47-104">สร้างกิจกรรมกระบวนการสำหรับการผลิตแบบ lean </span><span class="sxs-lookup"><span data-stu-id="f2e47-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="f2e47-105">ข้อกำหนดเบื้องต้น:</span><span class="sxs-lookup"><span data-stu-id="f2e47-105">Prerequisites:</span></span> 

1. <span data-ttu-id="f2e47-106">1 ต้องสร้างขั้นตอนการผลิตและเวอร์ชันที่ไม่ได้ใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="f2e47-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="f2e47-107">2. ต้องสร้างเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f2e47-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="f2e47-108">ค้นหาเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="f2e47-108">Find the production flow version</span></span>
1. <span data-ttu-id="f2e47-109">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="f2e47-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="f2e47-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2e47-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f2e47-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2e47-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="f2e47-112">สร้างกิจกรรมใหม่</span><span class="sxs-lookup"><span data-stu-id="f2e47-112">Create a new activity</span></span>
1. <span data-ttu-id="f2e47-113">คลิกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="f2e47-113">Click Activities.</span></span>
    * <span data-ttu-id="f2e47-114">ตรวจสอบให้แน่ใจว่าขั้นตอนการผลิตที่เลือกมีเวอร์ชันในแบบร่าง และเลือกเวอร์ชันนั้น</span><span class="sxs-lookup"><span data-stu-id="f2e47-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="f2e47-115">คลิกสร้างกิจกรรมการวางแผนใหม่</span><span class="sxs-lookup"><span data-stu-id="f2e47-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="f2e47-116">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f2e47-116">Click Next.</span></span>
4. <span data-ttu-id="f2e47-117">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f2e47-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f2e47-118">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f2e47-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f2e47-119">โปรดทราบว่า ชื่อต้องไม่ซ้ำกันสำหรับการระบุขั้นตอนการผลิตสำหรับเวอร์ชันทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f2e47-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="f2e47-120">ในฟิลด์ปริมาณกระบวนการ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f2e47-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="f2e47-121">โปรดทราบว่าไม่ว่าปริมาณงานใดจะถูกประมวลผล นี่เป็นปริมาณต่ำสุดสำหรับแต่ละงานในการคำนวณต้นทุนแรงงาน </span><span class="sxs-lookup"><span data-stu-id="f2e47-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="f2e47-122">ถ้าปริมาณงานแตกต่างจากปริมาณนี้ ผลต่างต้นทุนแรงงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f2e47-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="f2e47-123">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f2e47-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="f2e47-124">เลือกเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f2e47-124">Select the work cell</span></span>
1. <span data-ttu-id="f2e47-125">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="f2e47-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f2e47-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2e47-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="f2e47-127">กำหนดการอัพเดตสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f2e47-127">Define the inventory updates</span></span>
1. <span data-ttu-id="f2e47-128">เลือกหรือเคลียร์กล่องกาเครื่องหมายอัพเดตปริมาณคงคลังคงเหลือเมื่อรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="f2e47-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="f2e47-129">ถ้ามีการอัพเดตปริมาณคงคลังคงเหลือ = ไม่ใช่ คุณสามารถกำหนดกิจกรรมเพื่อรับผลิตภัณฑ์กึ่งสำเร็จรูป (กิจกรรมไม่ถึงระดับ BOM) </span><span class="sxs-lookup"><span data-stu-id="f2e47-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="f2e47-130">คุณยังสามารถเลือกที่จะใช้ผลิตภัณฑ์กึ่งสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="f2e47-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="f2e47-131">กำหนดกิจกรรมการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="f2e47-131">Define the picking activities</span></span>
1. <span data-ttu-id="f2e47-132">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f2e47-132">Click Next.</span></span>
2. <span data-ttu-id="f2e47-133">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2e47-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f2e47-134">ค่าเริ่มต้นกิจกรรมการเบิกสินค้าถูกสร้างขึ้นสำหรับที่ตั้งอินพุทของเซลล์ทำงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2e47-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="f2e47-135">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f2e47-135">Click Add.</span></span>
    * <span data-ttu-id="f2e47-136">คุณสามารถสร้างกิจกรรมการเบิกสินค้าเพิ่มเติมสำหรับผลิตภัณฑ์เฉพาะ ที่ไม่ได้แบ่งระยะกิจกรรมอินพุทของเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f2e47-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="f2e47-137">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2e47-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f2e47-138">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f2e47-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="f2e47-139">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f2e47-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f2e47-140">ด้วยคำนิยามนี้ วัตถุดิบทั้งหมดที่ใช้ในกิจกรรมการถูกเบิกจากคลังสินค้าอินพุทที่เริ่มต้นและที่ตั้ง ยกเว้นสินค้าที่กำหนดไว้ในกิจกรรมการเบิกสินค้าที่สอง </span><span class="sxs-lookup"><span data-stu-id="f2e47-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="f2e47-141">สินค้านี้จะถูกเบิกจากคลังสินค้าและสถานที่ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f2e47-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="f2e47-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2e47-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f2e47-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f2e47-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f2e47-144">เลือกหรือเคลียร์กล่องกาเครื่องหมายลงทะเบียนของเสีย </span><span class="sxs-lookup"><span data-stu-id="f2e47-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="f2e47-145">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f2e47-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="f2e47-146">กำหนดเวลากิจกรรม</span><span class="sxs-lookup"><span data-stu-id="f2e47-146">Define the activity times</span></span>
1. <span data-ttu-id="f2e47-147">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2e47-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f2e47-148">คำนิยามของรันไทม์จำเป็นต้องใช้ </span><span class="sxs-lookup"><span data-stu-id="f2e47-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="f2e47-149">รันไทม์ถูกใช้เพื่อคำนวณต้นทุนและเวลาสำหรับปริมาณที่สามารถประมวลผลได้ของงานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="f2e47-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="f2e47-150">รันไทม์ไม่ได้ใช้ในการคำนวณปริมาณการใช้วัสดุและกำลังการผลิต ซึ่งจะคำนวณโดยเวลาวงจรที่ได้รับมาจากงานเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="f2e47-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="f2e47-151">ในฟิลด์เวลา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f2e47-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="f2e47-152">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f2e47-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="f2e47-153">เลือกหน่วยเวลา</span><span class="sxs-lookup"><span data-stu-id="f2e47-153">Select the Time unit.</span></span>
5. <span data-ttu-id="f2e47-154">ในฟิลด์ต่อปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f2e47-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="f2e47-155">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2e47-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f2e47-156">เวลาในการรอไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f2e47-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="f2e47-157">ในฟิลด์เวลา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f2e47-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="f2e47-158">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f2e47-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="f2e47-159">เลือกหน่วยเวลา</span><span class="sxs-lookup"><span data-stu-id="f2e47-159">Select the Time unit.</span></span>
10. <span data-ttu-id="f2e47-160">ในฟิลด์ต่อปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f2e47-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="f2e47-161">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f2e47-161">Click Next.</span></span>
12. <span data-ttu-id="f2e47-162">คลิก Finish</span><span class="sxs-lookup"><span data-stu-id="f2e47-162">Click Finish.</span></span>
13. <span data-ttu-id="f2e47-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f2e47-163">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]