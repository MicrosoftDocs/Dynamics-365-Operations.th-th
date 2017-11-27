--- 
title: "ตั้งค่าการบรรจุลงตู้บรรจุสินค้า"
description: "กระบวนงานนี้อธิบายวิธีการทำให้การบรรจุลงตู้บรรจุสินค้าของโหลดในการจัดการคลังสินค้าเป็นแบบอัตโนมัติ "
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: c5faf926071dec5d2ddc1c9e921a98ecd0754917
ms.contentlocale: th-th
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="c2670-103">ตั้งค่าการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2670-104">กระบวนงานนี้อธิบายวิธีการทำให้การบรรจุลงตู้บรรจุสินค้าของโหลดในการจัดการคลังสินค้าเป็นแบบอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="c2670-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="c2670-105">การบรรจุลงตู้บรรจุสินค้าแบบอัตโนมัติสร้างตู้บรรจุสินค้าและงานการเบิกสินค้าสำหรับการจัดส่ง เมื่อเวฟถูกประมวลผลและรายการงานถูกแบ่งออกเป็นปริมาณต่างๆที่พอดีกับตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="c2670-106">การดำเนินการนี้ช่วยให้ผู้ปฏิบัติงานสำหรับคลังสินค้าเบิกสินค้าได้โดยตรงในตู้บรรจุสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c2670-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="c2670-107">เมื่อเปรียบเทียบกับกระบวนการการเบิกสินค่าแบบด้วยตนเอง งาน เช่น การสร้างตู้บรรจุสินค้า การมอบหมายสินค้า และการปิดตู้บรรจุสินค้า จะถูกทำให้เป็นอัตโนมัติโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="c2670-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="c2670-108">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF และถูกดำเนินการโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="c2670-109">การตั้งค่าเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="c2670-109">Set up a wave template</span></span>
1. <span data-ttu-id="c2670-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > เวฟ > เท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="c2670-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="c2670-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-111">Click New.</span></span>
3. <span data-ttu-id="c2670-112">ในฟิลด์ชือเท็มเพลตเวฟ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="c2670-113">ในฟิลด์คำอธิบายเท็มเพลตเวฟ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="c2670-114">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="c2670-115">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="c2670-116">ขยายส่วนวิธี</span><span class="sxs-lookup"><span data-stu-id="c2670-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="c2670-117">บานหน้าต่างวิธีที่เลือกจะแสดงรายการวิธีสำหรับชนิดเท็มเพลตเวฟที่เลือก </span><span class="sxs-lookup"><span data-stu-id="c2670-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="c2670-118">เท็มเพลตเวฟต้องรวมวิธีการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="c2670-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c2670-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="c2670-120">ในฟิลด์รหัสขั้นตอนของเวฟ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="c2670-121">ป้อนรหัสขั้นตอนของเวฟสำหรับวิธีที่เพิ่ม ซึ่งสามารถเป็นรหัสใดๆ </span><span class="sxs-lookup"><span data-stu-id="c2670-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="c2670-122">สามารถเพิ่มวิธีได้มากกว่าหนึ่งครั้ง และมอบหมายรหัสขั้นตอนของเวฟที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c2670-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="c2670-123">เพื่อดำเนินงานนี้ ให้เลือก ทำซ้ำได้ สำหรับวิธีนี้ในหน้าวิธีการกระบวนการเวฟ</span><span class="sxs-lookup"><span data-stu-id="c2670-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="c2670-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c2670-124">Click Save.</span></span>
11. <span data-ttu-id="c2670-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c2670-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="c2670-126">ตั้งค่าชนิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-126">Set up a container type</span></span>
1. <span data-ttu-id="c2670-127">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > ชนิดของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="c2670-128">คุณสามารถกำหนดตู้บรรจุสินค้าของคุณในหน้าชนิดของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="c2670-129">คุณสามารถตั้งค่าคอนฟิกมิติทางกายภาพของตู้บรรจุสินค้าได้ รวมถึงน้ำหนักหีบห่อ น้ำหนักสูงสุด ปริมาณสูงสุด ความยาว ความกว้าง น้ำหนัก และความสูง </span><span class="sxs-lookup"><span data-stu-id="c2670-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="c2670-130">ในตัวอย่างนี้ เรามีขนาดของกล่องที่แตกต่างกันสามขนาด</span><span class="sxs-lookup"><span data-stu-id="c2670-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="c2670-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-131">Click New.</span></span>
3. <span data-ttu-id="c2670-132">ในฟิลด์รหัสชนิดของตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="c2670-133">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="c2670-134">ในฟิลด์น้ำหนักสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="c2670-135">ในฟิลด์จำนวน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="c2670-136">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="c2670-137">ในฟิลด์ความกว้าง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="c2670-138">ในฟิลด์ความสูง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="c2670-139">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="c2670-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c2670-140">Click Save.</span></span>
12. <span data-ttu-id="c2670-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-141">Click New.</span></span>
13. <span data-ttu-id="c2670-142">ในฟิลด์รหัสชนิดของตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="c2670-143">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="c2670-144">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="c2670-145">ในฟิลด์น้ำหนักสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="c2670-146">ในฟิลด์จำนวน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="c2670-147">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="c2670-148">ในฟิลด์ความกว้าง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="c2670-149">ในฟิลด์ความสูง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="c2670-150">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c2670-150">Click Save.</span></span>
22. <span data-ttu-id="c2670-151">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-151">Click New.</span></span>
23. <span data-ttu-id="c2670-152">ในฟิลด์รหัสชนิดของตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="c2670-153">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="c2670-154">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="c2670-155">ในฟิลด์น้ำหนักสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="c2670-156">ในฟิลด์จำนวน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="c2670-157">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="c2670-158">ในฟิลด์ความกว้าง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="c2670-159">ในฟิลด์ความสูง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2670-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="c2670-160">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c2670-160">Click Save.</span></span>
32. <span data-ttu-id="c2670-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c2670-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="c2670-162">ตั้งค่ากลุ่มตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-162">Set up a container group</span></span>
1. <span data-ttu-id="c2670-163">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > กลุ่มตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="c2670-164">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-164">Click New.</span></span>
    * <span data-ttu-id="c2670-165">คุณสามารถตั้งค่ากลุ่มเชิงตรรกะของชนิดตู้บรรจุสินค้า </span><span class="sxs-lookup"><span data-stu-id="c2670-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="c2670-166">สำหรับแต่ละกลุ่ม คุณสามารถระบุลำดับที่จะบรรจุตู้บรรจุสินค้า และเปอร์เซ็นต์ที่จะเติมของตู้บรรจุสินค้า </span><span class="sxs-lookup"><span data-stu-id="c2670-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="c2670-167">มิติขนาดของสินค้าถูกใช้เพื่อกำหนดว่าจะพอดีในตู้บรรจุสินค้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c2670-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="c2670-168">ตู้บรรจุสินค้าที่ใกล้เคียงกับมิติขนาดของสินค้าที่สุดจะถูกนำไปใช้ </span><span class="sxs-lookup"><span data-stu-id="c2670-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="c2670-169">ถ้าคุณมีตู้บรรจุสินค้าหลายชนิดในกลุ่ม เราขอแนะนำให้คุณจัดเรียงลำดับตามขนาด เพื่อให้ตู้บรรจุสินค้าที่ใหญ่ที่สุดอยู่ในลำดับที่ 1 และตู้บรรจุสินค้าที่เล็กที่สุดอยู่ในลำดับสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="c2670-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="c2670-170">ในฟิลด์รหัสกลุ่มตู้บรรจุสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="c2670-171">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c2670-172">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-172">Click New.</span></span>
6. <span data-ttu-id="c2670-173">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c2670-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c2670-174">ในฟิลด์ชนิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="c2670-175">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-175">Click New.</span></span>
9. <span data-ttu-id="c2670-176">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c2670-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="c2670-177">ในฟิลด์ชนิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="c2670-178">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-178">Click New.</span></span>
12. <span data-ttu-id="c2670-179">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c2670-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c2670-180">ในฟิลด์ชนิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="c2670-181">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c2670-181">Click Save.</span></span>
15. <span data-ttu-id="c2670-182">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c2670-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="c2670-183">ตั้งค่าเท็มเพลตการสร้างตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-183">Set up a container build template</span></span>
1. <span data-ttu-id="c2670-184">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > เท็มเพลตการสร้างตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="c2670-185">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-185">Click New.</span></span>
    * <span data-ttu-id="c2670-186">เท็มเพลตการสร้างตู้บรรจุสินค้าขี้นกับว่ากระบวนการของการบรรจุลงตู้บรรจุสินค้าใดที่ถูกดำเนินการ </span><span class="sxs-lookup"><span data-stu-id="c2670-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="c2670-187">เท็มเพลตการสร้างตู้บรรจุสินค้าแต่ละแบบกำหนดหนึ่งรหัสกระบวนการของการบรรจุลงตู้บรรจุสินค้าที่จะถูกใช้โดยเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="c2670-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="c2670-188">ตัวเลือกการแก้ไขการสอบถาม อนุญาตให้คุณกำหนดเงื่อนไขว่าเท็มเพลตที่เลือกใดจะถูกประมวลผล</span><span class="sxs-lookup"><span data-stu-id="c2670-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="c2670-189">ตัวอย่างเช่น คุณอาจต้องการรันเฉพาะการบรรจุลงตู้บรรจุสินค้าสำหรับลูกค้าเฉพาะ ผลิตภัณฑ์ หรือคลังสินค้า หรือคุณสามารถเพิ่มช่วงการสอบถามที่สอดคล้องกันไปยังเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="c2670-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="c2670-190">รหัสขั้นตอนของเวฟคือ วิธีการลิงค์เท็มเพลตการสร้างตู้บรรจุสินค้าไปยังขั้นตอนต่างๆในเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="c2670-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="c2670-191">เมื่อมีการดำเนินการเวฟ จะกำหนดว่าเท็มเพลตการสร้างตู้บรรจุสินค้าใดที่จะถูกใช้ในการเริ่มการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="c2670-192">ฟิลด์ชนิดการสอบถามพื้นฐานจะกำหนดสิ่งที่จะบรรจุ และสิ่งที่จะใช้เป็นพื้นฐานของการสอบถามตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="c2670-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="c2670-193">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c2670-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c2670-194">ในฟิลด์รหัสเท็มเพลตตู้บรรจุสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="c2670-195">ในฟิลด์รหัสกลุ่มตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="c2670-196">ในฟิลด์รหัสขั้นตอนของเวฟ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2670-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="c2670-197">เลือกกล่องกาเครื่องหมายการอนุญาตให้แบ่งการเบิกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="c2670-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="c2670-198">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c2670-198">Click Save.</span></span>
9. <span data-ttu-id="c2670-199">คลิกข้อจำกัดการผสมของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2670-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="c2670-200">การแบ่งตามตรรกะผสม อนุญาตให้คุณตั้งค่ากฎสำหรับการบรรจุรายการการปันส่วนในตู้บรรจุสินค้า </span><span class="sxs-lookup"><span data-stu-id="c2670-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="c2670-201">ตัวอย่างเช่น ถ้าคุณเพิ่มฟิลด์หมายเลขสินค้า เมื่อมีการกำหนดสินค้าให้กับตู้บรรจุสินค้า ตู้บรรจุสินค้าใหม่จะถูกสร้างเมื่อมีหมายเลขสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="c2670-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="c2670-202">นี่จะป้องกันผู้ปฏิบัติงานจากการบรรจุรายการการปันส่วน สำหรับลูกค้าที่ต่างกันสองรายในตู้บรรจุสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c2670-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="c2670-203">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2670-203">Click New.</span></span>
11. <span data-ttu-id="c2670-204">ในฟิลด์ตาราง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c2670-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="c2670-205">ในฟิลด์การเลือกฟิลด์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2670-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="c2670-206">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c2670-206">Click OK.</span></span>


