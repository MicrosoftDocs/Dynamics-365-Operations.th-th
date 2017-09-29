--- 
title: "ตั้งค่ากระบวนการการเพิ่มเติมสินค้าต่ำสุด-สูงสุด"
description: "กระบวนงานนี้แสดงวิธีการตั้งค่ากระบวนการการเติมสินค้าใหม่ซึ่งใช้กลยุทธ์การเติมสินค้าต่ำสุด/สูงสุด "
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a><span data-ttu-id="518a2-103">ตั้งค่ากระบวนการการเพิ่มเติมสินค้าต่ำสุด-สูงสุด</span><span class="sxs-lookup"><span data-stu-id="518a2-103">Set up a min-max replenishment process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="518a2-104">กระบวนงานนี้แสดงวิธีการตั้งค่ากระบวนการการเติมสินค้าใหม่ซึ่งใช้กลยุทธ์การเติมสินค้าต่ำสุด/สูงสุด </span><span class="sxs-lookup"><span data-stu-id="518a2-104">This procedure shows you how to set up a new replenishment process which uses the minimum/maximum replenishment strategy.</span></span> <span data-ttu-id="518a2-105">เมื่อสินค้าคงคลังอยู่ต่ำกว่าระดับต่ำสุด งานจะถูกสร้างเพื่อเติมสินค้าให้สถานที่</span><span class="sxs-lookup"><span data-stu-id="518a2-105">When inventory falls below the minimum level, work will be created to replenish the location.</span></span> <span data-ttu-id="518a2-106">กระบวนงานยังแสดงวิธีการใช้สถานที่เบิกที่คงที่ แม้ว่าสินค้าคงคลังอยู่ต่ำกว่าระดับต่ำสุด และวิธีการเปิดใช้งานกระบวนการการเติมสินค้าเพื่อรันตามปกติโดยใช้ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="518a2-106">The procedure also shows how to use fixed picking locations to allow restocking even if inventory falls below the minimum level, and how to enable the replenishment process to run regularly using a batch job.</span></span> <span data-ttu-id="518a2-107">งานเหล่านี้โดยทั่วไปจะถูกดำเนินการโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-107">These tasks would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="518a2-108">คุณสามารถรันกระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF ในหมายเหตุ หรือสามารถรันได้ในข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="518a2-108">You can run this procedure in the USMF demo data company using the example values in the notes, or can run it on your own data.</span></span> <span data-ttu-id="518a2-109">ถ้าคุณกำลังใช้ข้อมูลของคุณเอง ตรวจสอบให้แน่ใจว่า คุณมีคลังสินค้าที่ได้เปิดใช้งานสำหรับกระบวนการการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-109">If you’re using your own data, make sure that you have a warehouse that’s enabled for Warehouse management processes.</span></span>


## <a name="create-a-fixed-picking-location"></a><span data-ttu-id="518a2-110">สร้างสถานที่เบิกที่คงที่</span><span class="sxs-lookup"><span data-stu-id="518a2-110">Create a fixed picking location</span></span>
1. <span data-ttu-id="518a2-111">ไปที่การจัดการคลังสินค้า > การตั้งค่า > คลังสินค้า > สถานที่คงที่</span><span class="sxs-lookup"><span data-stu-id="518a2-111">Go to Warehouse management > Setup > Warehouse > Fixed locations.</span></span>
    * <span data-ttu-id="518a2-112">นี่คืองานทางเลือกสำหรับการเพิ่มเติมสินค้าต่ำสุด-สูงสุด แต่ถ้าคุณใช้สถานที่เบิกที่คงที่ นี่จะอนุญาตให้สินค้าคงคลังได้รับการเติมสินค้า ถึงแม้ว่าจะอยู่ต่ำกว่าระดับต่ำสุด เนื่องจากระบบสามารถกำหนดได้ว่าสินค้าใดที่ต้องการการเติม ถึงแม้ว่าจะไม่มีเหลืออยู่เลย</span><span class="sxs-lookup"><span data-stu-id="518a2-112">This is an optional task for min-max replenishment, but if you use fixed picking location, this allows stock to be replenished even if it falls below the minimum level, because the system can determine which items need to be replenished, even if there aren't any left.</span></span>  
2. <span data-ttu-id="518a2-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-113">Click New.</span></span>
3. <span data-ttu-id="518a2-114">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="518a2-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-115">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกสินค้า A0001 ได้</span><span class="sxs-lookup"><span data-stu-id="518a2-115">If you’re using USMF, you can select item A0001.</span></span>  
4. <span data-ttu-id="518a2-116">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-117">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกไซต์ 2 ได้</span><span class="sxs-lookup"><span data-stu-id="518a2-117">If you’re using USMF, you can select site 2.</span></span>  
5. <span data-ttu-id="518a2-118">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-119">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกคลังสินค้า 24 ได้</span><span class="sxs-lookup"><span data-stu-id="518a2-119">If you’re using USMF, you can select warehouse 24.</span></span>  
6. <span data-ttu-id="518a2-120">ในฟิลด์สถานที่ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-120">In the Location field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-121">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก CP-003 ได้</span><span class="sxs-lookup"><span data-stu-id="518a2-121">If you’re using USMF, you can select CP-003.</span></span>  
7. <span data-ttu-id="518a2-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="518a2-122">Close the page.</span></span>

## <a name="create-a-replenishment-location-directive"></a><span data-ttu-id="518a2-123">สร้างคำสั่งสถานที่ของการเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-123">Create a replenishment location directive</span></span>
1. <span data-ttu-id="518a2-124">ไปที่คลังสินค้าจัดการ > การตั้งค่า > คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="518a2-124">Go to Warehouse management > Setup > Location directives.</span></span>
    * <span data-ttu-id="518a2-125">คำสั่งสถานที่ถูกใช้เพื่อกำหนดสถานที่ที่สินค้าควรถูกเบิกจาก ในกระบวนการการเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-125">Location directives are used to determine where items should be picked from in the replenishment process.</span></span>  
2. <span data-ttu-id="518a2-126">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การเพิ่มเติมสินค้า'</span><span class="sxs-lookup"><span data-stu-id="518a2-126">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="518a2-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-127">Click New.</span></span>
4. <span data-ttu-id="518a2-128">ในฟิลด์ชื่อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-128">In the Name field, type a value.</span></span>
5. <span data-ttu-id="518a2-129">ในฟิลด์ประเภทงาน ให้เลือก 'เบิกสินค้า'</span><span class="sxs-lookup"><span data-stu-id="518a2-129">In the Work type field, select 'Pick'.</span></span>
6. <span data-ttu-id="518a2-130">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-130">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-131">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกไซต์ 2 ได้</span><span class="sxs-lookup"><span data-stu-id="518a2-131">If you’re using USMF, you can select site 2.</span></span>  
7. <span data-ttu-id="518a2-132">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-132">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-133">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกคลังสินค้า 24 ได้</span><span class="sxs-lookup"><span data-stu-id="518a2-133">If you’re using USMF, you can select warehouse 24.</span></span>  
8. <span data-ttu-id="518a2-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="518a2-134">Click Save.</span></span>
9. <span data-ttu-id="518a2-135">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-135">Click New.</span></span>
10. <span data-ttu-id="518a2-136">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="518a2-136">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="518a2-137">ในฟิลด์ถึงปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="518a2-137">In the To quantity field, enter a number.</span></span>
    * <span data-ttu-id="518a2-138">ตัวอย่างเช่น คุณสามารถตั้งค่าเป็น 9999 ได้</span><span class="sxs-lookup"><span data-stu-id="518a2-138">For example, you can set it to 9999.</span></span>  
12. <span data-ttu-id="518a2-139">เลือกกล่องกาเครื่องหมายการอนุญาตให้แบ่งได้</span><span class="sxs-lookup"><span data-stu-id="518a2-139">Select the Allow split check box.</span></span>
    * <span data-ttu-id="518a2-140">ถ้าคุณเลือกตัวเลือกนี้ กระบวนการสร้างงานจะอนุญาตให้ปริมาณรายการของงานถูกแบ่งข้ามสถานที่หลายแห่งได้</span><span class="sxs-lookup"><span data-stu-id="518a2-140">If you select this option, the work creation process will allow work line quantities to be split across multiple locations.</span></span>  
13. <span data-ttu-id="518a2-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="518a2-141">Click Save.</span></span>
14. <span data-ttu-id="518a2-142">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-142">Click New.</span></span>
15. <span data-ttu-id="518a2-143">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="518a2-143">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="518a2-144">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="518a2-144">In the Name field, type a value.</span></span>
17. <span data-ttu-id="518a2-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="518a2-145">Click Save.</span></span>
18. <span data-ttu-id="518a2-146">(คลิกแก้ไขการสอบถาม)</span><span class="sxs-lookup"><span data-stu-id="518a2-146">Click Edit query.</span></span>
    * <span data-ttu-id="518a2-147">คุณสามารถแก้ไขการสอบถามนี้เพื่อเพิ่มข้อจำกัดที่สินค้าคงคลังสามารถถูกเลือกได้ในกระบวนการการเพิ่มเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="518a2-147">You can edit this query to add restrictions where inventory can be selected from in the replenishment process.</span></span> <span data-ttu-id="518a2-148">ตัวอย่างเช่น นี่สามารถเป็น สินค้าคงคลังควรถูกใช้เฉพาะจากพื้นที่เทกองของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-148">For example, it could be that inventory should only be used from the Bulk area of the warehouse.</span></span>  
19. <span data-ttu-id="518a2-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="518a2-149">Click OK.</span></span>
20. <span data-ttu-id="518a2-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="518a2-150">Close the page.</span></span>

## <a name="create-a-replenishment-work-template"></a><span data-ttu-id="518a2-151">สร้างเท็มเพลตงานของการเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-151">Create a replenishment work template</span></span>
1. <span data-ttu-id="518a2-152">ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="518a2-152">Go to Warehouse management > Setup > Work > Work templates.</span></span>
    * <span data-ttu-id="518a2-153">เท็มเพลตงานถูกใช้ในการนำทางระบบซึ่งเป็นวิธีการสร้างงานการเพิ่มเติมสินค้าต่ำสุด/สูงสุด </span><span class="sxs-lookup"><span data-stu-id="518a2-153">The work template is use to guide the system as to how the min/max replenishment work must be created.</span></span> <span data-ttu-id="518a2-154">เมื่อเป็นค่าต่ำสุด ต้องมีรายการเท็มเพลตงานสำหรับการเบิกสินค้าและการส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-154">As a minimum, there must be a work template line for a pick and a put.</span></span> <span data-ttu-id="518a2-155">เท็มเพลตงานจะบอกว่า ไม่ถูกต้อง จนกว่าข้อมูลที่จำเป็นทั้งหมดจะถูกเติม</span><span class="sxs-lookup"><span data-stu-id="518a2-155">The work template will say that it’s Invalid until all the necessary information has been filled in.</span></span>  
2. <span data-ttu-id="518a2-156">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การเพิ่มเติมสินค้า'</span><span class="sxs-lookup"><span data-stu-id="518a2-156">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="518a2-157">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-157">Click New.</span></span>
4. <span data-ttu-id="518a2-158">ในฟิลด์เท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-158">In the Work template field, type a value.</span></span>
5. <span data-ttu-id="518a2-159">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="518a2-159">Click Save.</span></span>
6. <span data-ttu-id="518a2-160">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-160">Click New.</span></span>
7. <span data-ttu-id="518a2-161">ในฟิลด์ประเภทงาน ให้เลือก 'เบิกสินค้า'</span><span class="sxs-lookup"><span data-stu-id="518a2-161">In the Work type field, select 'Pick'.</span></span>
8. <span data-ttu-id="518a2-162">ในฟิลด์รหัสคลาสงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-162">In the Work class ID field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-163">นี่ควรเป็นคลาสงานที่เกี่ยวข้องกับการเพิ่มเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="518a2-163">This should be a work class related to replenishment.</span></span> <span data-ttu-id="518a2-164">ถ้าคุณกำลังใช้ USMF ให้เลือกการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-164">If you’re using USMF, select Replenish.</span></span>  
9. <span data-ttu-id="518a2-165">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-165">Click New.</span></span>
10. <span data-ttu-id="518a2-166">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="518a2-166">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="518a2-167">ในฟิลด์ประเภทงาน ให้เลือก 'ส่งสินค้า'</span><span class="sxs-lookup"><span data-stu-id="518a2-167">In the Work type field, select 'Put'.</span></span>
12. <span data-ttu-id="518a2-168">ในฟิลด์รหัสคลาสงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-168">In the Work class ID field, enter or select a value.</span></span>
13. <span data-ttu-id="518a2-169">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="518a2-169">Click Save.</span></span>
14. <span data-ttu-id="518a2-170">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="518a2-170">Close the page.</span></span>

## <a name="create-a-new-replenishment-template"></a><span data-ttu-id="518a2-171">สร้างเท็มเพลตการเพิ่มเติมสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="518a2-171">Create a new replenishment template</span></span>
1. <span data-ttu-id="518a2-172">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การเพิ่มเติมสินค้า > เท็มเพลตการเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-172">Go to Warehouse management > Setup > Replenishment > Replenishment templates.</span></span>
    * <span data-ttu-id="518a2-173">เท็มเพลตการเติมสินค้าถูกใช้ในการกำหนดสินค้าและปริมาณ และสถานที่ที่จะเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-173">The replenishment template is used to define the items and quantities, and the location to replenish.</span></span>  
2. <span data-ttu-id="518a2-174">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-174">Click New.</span></span>
3. <span data-ttu-id="518a2-175">ในฟิลด์เท็มเพลตการเพิ่มเติมสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-175">In the Replenish template field, type a value.</span></span>
    * <span data-ttu-id="518a2-176">ตั้งชื่อเท็มเพลตเพื่อระบุว่า เป็นสำหรับการเพิ่มเติมสินค้าต่ำสุด/สูงสุด</span><span class="sxs-lookup"><span data-stu-id="518a2-176">Give the template a name to indicate that it’s for min/max replenishment.</span></span>  
4. <span data-ttu-id="518a2-177">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="518a2-177">In the Description field, type a value.</span></span>
5. <span data-ttu-id="518a2-178">เลือกกล่องกาเครื่องหมายการอนุญาตให้ความต้องการของเวฟใช้ปริมาณที่ไม่ได้จอง</span><span class="sxs-lookup"><span data-stu-id="518a2-178">Select the Allow wave demand to use unreserved quantities check box.</span></span>
    * <span data-ttu-id="518a2-179">ถ้าคุณเลือกตัวเลือกนี้ จะเปิดใช้งานการเพิ่มเติมสินค้าของความต้องการของเวฟ เพื่อใช้ปริมาณที่สัมพันธ์กับการเพิ่มเติมสินค้าต่ำสุด/สูงสุด</span><span class="sxs-lookup"><span data-stu-id="518a2-179">If you select this option, it enables wave demand replenishment to consume quantities that are related to min/max replenishment.</span></span> <span data-ttu-id="518a2-180">ตัวอย่างเช่น นี่อาจเป็นประโยชน์ถ้างานการเพิ่มเติมสินค้าต่ำสุด/สูงสุดไม่ได้ถูกประมวลผลโดยทันที เพื่อหลีกเลี่ยงงานการเพิ่มเติมสินค้าของความต้องการที่ไม่จำเป็นจากการที่จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="518a2-180">For example, this might be useful if the min/max replenishment work isn’t processed immediately, to avoid unnecessary demand replenishment work from being created.</span></span>  
6. <span data-ttu-id="518a2-181">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="518a2-181">Click New.</span></span>
7. <span data-ttu-id="518a2-182">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="518a2-182">In the Sequence number field, enter a number.</span></span>
8. <span data-ttu-id="518a2-183">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="518a2-183">In the Description field, type a value.</span></span>
9. <span data-ttu-id="518a2-184">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="518a2-184">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="518a2-185">ในฟิลด์หน่วยการเพิ่มเติมสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="518a2-185">In the Replenishment unit field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-186">ตัวอย่างเช่น: เลือก pcs</span><span class="sxs-lookup"><span data-stu-id="518a2-186">For example, select pcs.</span></span> <span data-ttu-id="518a2-187">การตั้งค่านี้เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="518a2-187">This setting is mandatory.</span></span> <span data-ttu-id="518a2-188">ซึ่งอนุญาตให้คุณระบุหน่วยการวัดที่ต่างกันสำหรับงานการเพิ่มเติมสินค้า ที่เปรียบเทียบกับหน่วยที่ระบุไว้สำหรับระดับสินค้าคงคลังต่ำสุดและสูงสุดในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="518a2-188">It allows you to specify a different unit of measurement for replenishment work compared to the unit specified for the minimum and maximum stock levels in this template.</span></span>  
11. <span data-ttu-id="518a2-189">ในฟิลด์เท็มเพลตงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-189">In the Work template field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-190">เลือกเท็มเพลตงานที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="518a2-190">Choose the work template that you created earlier.</span></span>  
12. <span data-ttu-id="518a2-191">ในฟิลด์ปริมาณต่ำสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="518a2-191">In the Minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="518a2-192">เลือกปริมาณต่ำสุดที่ควรทริกเกอร์การเพิ่มเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="518a2-192">Select the minimum quantity that should trigger the replenishment.</span></span> <span data-ttu-id="518a2-193">ตัวอย่างเช่น ตั้งค่าเป็น 50</span><span class="sxs-lookup"><span data-stu-id="518a2-193">For example, set this to 50.</span></span> <span data-ttu-id="518a2-194">ซึ่งสามารถปล่อยให้เป็นศูนย์ได้ ถ้าคุณกำลังเติมสินค้าที่สถานที่คงที่ และตัวเลือกการเพิ่มเติมสินค้าในสถานที่คงที่ที่ว่างเปล่าถูกตั้งค่าเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="518a2-194">It is possible to leave this set to zero, if you’re replenishing a fixed location and the Replenish empty fixed locations option is set to Yes.</span></span> <span data-ttu-id="518a2-195">เรายังแนะนำให้คุณเลือกตัวเลือกการเพิ่มเติมสินค้าเฉพาะในสถานที่คงที่สำหรับเหตุผลด้านประสิทธิภาพการทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="518a2-195">We also recommend that you select the Replenish only fixed locations option for performance reasons.</span></span>  
13. <span data-ttu-id="518a2-196">ในฟิลด์ปริมาณสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="518a2-196">In the Maximum quantity field, enter a number.</span></span>
    * <span data-ttu-id="518a2-197">ตัวอย่างเช่น ตั้งค่าเป็น 100</span><span class="sxs-lookup"><span data-stu-id="518a2-197">For example, set this to 100.</span></span>  
14. <span data-ttu-id="518a2-198">ในฟิลด์หน่วย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="518a2-198">In the Unit field, enter or select a value.</span></span>
    * <span data-ttu-id="518a2-199">กำหนดหน่วยสำหรับปริมาณต่ำสุดและสูงสุด </span><span class="sxs-lookup"><span data-stu-id="518a2-199">Assign the unit for the minimum and maximum quantities.</span></span> <span data-ttu-id="518a2-200">ตัวอย่างเช่น ตั้งค่าเป็น pcs</span><span class="sxs-lookup"><span data-stu-id="518a2-200">For example, set this to pcs.</span></span>  
15. <span data-ttu-id="518a2-201">เลือกกล่องกาเครื่องหมายการเพิ่มเติมสินค้าในสถานที่คงที่ที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="518a2-201">Select the Replenish empty fixed locations check box.</span></span>
    * <span data-ttu-id="518a2-202">เลือกกล่องกาเครื่องหมายนี้เพื่อเติมสินค้าในสถานที่คงที่ เมื่อไม่มีสินค้าอยู่ </span><span class="sxs-lookup"><span data-stu-id="518a2-202">Select this check box to replenish fixed locations when they are empty.</span></span> <span data-ttu-id="518a2-203">มิฉะนั้น จะมีเฉพาะสถานที่ซึ่งมีปริมาณคงคลังคงเหลืออยู่ที่จะถูกเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-203">Otherwise, only the locations where there is a quantity on hand will be replenished.</span></span>  
16. <span data-ttu-id="518a2-204">เลือกกล่องกาเครื่องหมายการเพิ่มเติมสินค้าเฉพาะในสถานที่คงที่</span><span class="sxs-lookup"><span data-stu-id="518a2-204">Select the Replenish only fixed locations check box.</span></span>
17. <span data-ttu-id="518a2-205">คลิกเลือกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="518a2-205">Click Select products.</span></span>
    * <span data-ttu-id="518a2-206">นี่คือสถานที่ที่จะกำหนดว่าผลิตภัณฑ์ใดควรถูกเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="518a2-206">This is the place to define which products should be replenished.</span></span> <span data-ttu-id="518a2-207">ถ้าตัวเลือกสถานที่เบิกที่คงที่ถูกเลือก คุณยังต้องกำหนดสถานที่ในการสอบถามนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="518a2-207">If the Fixed picking locations option is selected, you also need to define the locations in this query.</span></span> <span data-ttu-id="518a2-208">การสอบถามเฉพาะ-ตัวแปรจะพร้อมใช้งานเช่นเดียวกับการสอบถามเฉพาะ-ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="518a2-208">Variant-specific queries are available as well product-specific queries.</span></span>  
18. <span data-ttu-id="518a2-209">เลือกแถวสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-209">Select the Items row.</span></span>
19. <span data-ttu-id="518a2-210">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="518a2-210">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="518a2-211">เลือกสินค้าที่ควรถูกเติมสินค้าที่สถานที่คงที่ </span><span class="sxs-lookup"><span data-stu-id="518a2-211">Select the items that should be replenished at the fixed locations.</span></span> <span data-ttu-id="518a2-212">ตัวอย่างเช่น พิมพ์ชนิด A* เพื่อเลือกหมายเลขสินค้าทั้งหมดที่ขึ้นต้นด้วย A</span><span class="sxs-lookup"><span data-stu-id="518a2-212">For example, type A* to select all item numbers beginning with A.</span></span>  
20. <span data-ttu-id="518a2-213">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="518a2-213">Click Add.</span></span>
    * <span data-ttu-id="518a2-214">เพิ่มเอนทิตีสถานที่ (ถ้าไม่ได้มีอยู่แล้ว) ให้สามารถที่จะจำกัดงานการเพิ่มเติมสินค้าได้ ไปยังสถานที่เบิกที่คงที่ภายในพื้นที่เฉพาะของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-214">Add the Location entity (unless it already exists) to be able to restrict the replenishment work to the fixed picking locations within a specific area of the warehouse.</span></span>  
21. <span data-ttu-id="518a2-215">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="518a2-215">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="518a2-216">ตั้งค่าฟิลด์ตารางให้กับสถานที่</span><span class="sxs-lookup"><span data-stu-id="518a2-216">Set the Table field to Locations.</span></span>
23. <span data-ttu-id="518a2-217">ในฟิลด์ฟิลด์ ให้เลือกรหัสโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="518a2-217">In the Field field, select Location profile ID.</span></span>
24. <span data-ttu-id="518a2-218">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-218">In the Criteria field, enter or select a value.</span></span>
25. <span data-ttu-id="518a2-219">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="518a2-219">Click OK.</span></span>
26. <span data-ttu-id="518a2-220">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="518a2-220">Close the page.</span></span>

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a><span data-ttu-id="518a2-221">ตั้งค่ากระบวนการการเพิ่มเติมสินค้าเพื่อรันเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="518a2-221">Set the replenishment process to run as a batch job</span></span>
1. <span data-ttu-id="518a2-222">ไปที่การจัดการคลังสินค้า > การเพิ่มเติมสินค้า > การเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="518a2-222">Go to Warehouse management > Replenishment > Replenishments.</span></span>
    * <span data-ttu-id="518a2-223">หน้าการเพิ่มเติมสินค้าอนุญาตให้คุณสามารถตั้งค่าการเติมสินค้าได้ เพื่อให้รันชุดงาน หรือเพื่อต้องการให้มีการเริ่มต้นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="518a2-223">The Replenishments page allows you to set up replenishment to run as a batch job, or to require that it’s started manually.</span></span>  
2. <span data-ttu-id="518a2-224">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="518a2-224">Click Filter.</span></span>
3. <span data-ttu-id="518a2-225">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="518a2-225">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="518a2-226">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="518a2-226">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="518a2-227">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="518a2-227">Click OK.</span></span>
6. <span data-ttu-id="518a2-228">ขยายการดำเนินงานในส่วนเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="518a2-228">Expand the Run in the background section.</span></span>
7. <span data-ttu-id="518a2-229">ตั้งค่าตัวเลือกการประมวลผลชุดงานเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="518a2-229">Set the Batch processing option to Yes.</span></span>
8. <span data-ttu-id="518a2-230">การเกิดซ้ำ </span><span class="sxs-lookup"><span data-stu-id="518a2-230">Click Recurrence.</span></span>
9. <span data-ttu-id="518a2-231">เลือกตัวเลือกไม่มีวันที่สิ้นสุด </span><span class="sxs-lookup"><span data-stu-id="518a2-231">Select the No end date option.</span></span>
10. <span data-ttu-id="518a2-232">ตั้งค่ารูปแบบการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="518a2-232">Set the Recurrance pattern.</span></span>
    * <span data-ttu-id="518a2-233">ตัวอย่างเช่น เลือกวัน</span><span class="sxs-lookup"><span data-stu-id="518a2-233">For example, select Days.</span></span>  
11. <span data-ttu-id="518a2-234">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="518a2-234">Click OK.</span></span>
12. <span data-ttu-id="518a2-235">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="518a2-235">Click OK.</span></span>


