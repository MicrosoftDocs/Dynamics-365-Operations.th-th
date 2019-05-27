---
title: ตั้งค่าการบรรจุลงตู้บรรจุสินค้า
description: 'กระบวนงานนี้อธิบายวิธีการทำให้การบรรจุลงตู้บรรจุสินค้าของโหลดในการจัดการคลังสินค้าเป็นแบบอัตโนมัติ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558067"
---
# <a name="set-up-containerization"></a><span data-ttu-id="7a69e-103">ตั้งค่าการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a69e-104">กระบวนงานนี้อธิบายวิธีการทำให้การบรรจุลงตู้บรรจุสินค้าของโหลดในการจัดการคลังสินค้าเป็นแบบอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="7a69e-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="7a69e-105">การบรรจุลงตู้บรรจุสินค้าแบบอัตโนมัติสร้างตู้บรรจุสินค้าและงานการเบิกสินค้าสำหรับการจัดส่ง เมื่อเวฟถูกประมวลผลและรายการงานถูกแบ่งออกเป็นปริมาณต่างๆที่พอดีกับตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="7a69e-106">การดำเนินการนี้ช่วยให้ผู้ปฏิบัติงานสำหรับคลังสินค้าเบิกสินค้าได้โดยตรงในตู้บรรจุสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7a69e-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="7a69e-107">เมื่อเปรียบเทียบกับกระบวนการการเบิกสินค่าแบบด้วยตนเอง งาน เช่น การสร้างตู้บรรจุสินค้า การมอบหมายสินค้า และการปิดตู้บรรจุสินค้า จะถูกทำให้เป็นอัตโนมัติโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="7a69e-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="7a69e-108">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF และถูกดำเนินการโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="7a69e-109">การตั้งค่าเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="7a69e-109">Set up a wave template</span></span>
1. <span data-ttu-id="7a69e-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > เวฟ > เท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="7a69e-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="7a69e-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-111">Click New.</span></span>
3. <span data-ttu-id="7a69e-112">ในฟิลด์ชือเท็มเพลตเวฟ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="7a69e-113">ในฟิลด์คำอธิบายเท็มเพลตเวฟ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="7a69e-114">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="7a69e-115">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="7a69e-116">ขยายส่วนวิธี</span><span class="sxs-lookup"><span data-stu-id="7a69e-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="7a69e-117">บานหน้าต่างวิธีที่เลือกจะแสดงรายการวิธีสำหรับชนิดเท็มเพลตเวฟที่เลือก </span><span class="sxs-lookup"><span data-stu-id="7a69e-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="7a69e-118">เท็มเพลตเวฟต้องรวมวิธีการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="7a69e-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7a69e-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="7a69e-120">ในฟิลด์รหัสขั้นตอนของเวฟ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="7a69e-121">ป้อนรหัสขั้นตอนของเวฟสำหรับวิธีที่เพิ่ม ซึ่งสามารถเป็นรหัสใดๆ </span><span class="sxs-lookup"><span data-stu-id="7a69e-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="7a69e-122">สามารถเพิ่มวิธีได้มากกว่าหนึ่งครั้ง และมอบหมายรหัสขั้นตอนของเวฟที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7a69e-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="7a69e-123">เพื่อดำเนินงานนี้ ให้เลือก ทำซ้ำได้ สำหรับวิธีนี้ในหน้าวิธีการกระบวนการเวฟ</span><span class="sxs-lookup"><span data-stu-id="7a69e-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="7a69e-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7a69e-124">Click Save.</span></span>
11. <span data-ttu-id="7a69e-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="7a69e-126">ตั้งค่าชนิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-126">Set up a container type</span></span>
1. <span data-ttu-id="7a69e-127">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > ชนิดของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="7a69e-128">คุณสามารถกำหนดตู้บรรจุสินค้าของคุณในหน้าชนิดของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="7a69e-129">คุณสามารถตั้งค่าคอนฟิกมิติทางกายภาพของตู้บรรจุสินค้าได้ รวมถึงน้ำหนักหีบห่อ น้ำหนักสูงสุด ปริมาณสูงสุด ความยาว ความกว้าง น้ำหนัก และความสูง </span><span class="sxs-lookup"><span data-stu-id="7a69e-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="7a69e-130">ในตัวอย่างนี้ เรามีขนาดของกล่องที่แตกต่างกันสามขนาด</span><span class="sxs-lookup"><span data-stu-id="7a69e-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="7a69e-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-131">Click New.</span></span>
3. <span data-ttu-id="7a69e-132">ในฟิลด์รหัสชนิดของตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="7a69e-133">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="7a69e-134">ในฟิลด์น้ำหนักสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="7a69e-135">ในฟิลด์จำนวน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="7a69e-136">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="7a69e-137">ในฟิลด์ความกว้าง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="7a69e-138">ในฟิลด์ความสูง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="7a69e-139">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="7a69e-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7a69e-140">Click Save.</span></span>
12. <span data-ttu-id="7a69e-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-141">Click New.</span></span>
13. <span data-ttu-id="7a69e-142">ในฟิลด์รหัสชนิดของตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="7a69e-143">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="7a69e-144">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="7a69e-145">ในฟิลด์น้ำหนักสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="7a69e-146">ในฟิลด์จำนวน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="7a69e-147">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="7a69e-148">ในฟิลด์ความกว้าง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="7a69e-149">ในฟิลด์ความสูง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="7a69e-150">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7a69e-150">Click Save.</span></span>
22. <span data-ttu-id="7a69e-151">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-151">Click New.</span></span>
23. <span data-ttu-id="7a69e-152">ในฟิลด์รหัสชนิดของตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="7a69e-153">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="7a69e-154">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="7a69e-155">ในฟิลด์น้ำหนักสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="7a69e-156">ในฟิลด์จำนวน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="7a69e-157">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="7a69e-158">ในฟิลด์ความกว้าง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="7a69e-159">ในฟิลด์ความสูง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7a69e-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="7a69e-160">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7a69e-160">Click Save.</span></span>
32. <span data-ttu-id="7a69e-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="7a69e-162">ตั้งค่ากลุ่มตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-162">Set up a container group</span></span>
1. <span data-ttu-id="7a69e-163">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > กลุ่มตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="7a69e-164">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-164">Click New.</span></span>
    * <span data-ttu-id="7a69e-165">คุณสามารถตั้งค่ากลุ่มเชิงตรรกะของชนิดตู้บรรจุสินค้า </span><span class="sxs-lookup"><span data-stu-id="7a69e-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="7a69e-166">สำหรับแต่ละกลุ่ม คุณสามารถระบุลำดับที่จะบรรจุตู้บรรจุสินค้า และเปอร์เซ็นต์ที่จะเติมของตู้บรรจุสินค้า ใช้มิติขนาดของสินค้าเพื่อกำหนดว่าจะพอดีในตู้บรรจุสินค้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7a69e-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="7a69e-167">ตู้บรรจุสินค้าที่ใกล้เคียงกับมิติขนาดของสินค้าที่สุดจะถูกนำไปใช้ </span><span class="sxs-lookup"><span data-stu-id="7a69e-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="7a69e-168">ถ้าคุณมีตู้บรรจุสินค้าหลายชนิดในกลุ่ม เราขอแนะนำให้คุณจัดเรียงลำดับตามขนาด เพื่อให้ตู้บรรจุสินค้าที่ใหญ่ที่สุดอยู่ในลำดับที่ 1 และตู้บรรจุสินค้าที่เล็กที่สุดอยู่ในลำดับสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="7a69e-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="7a69e-169">ในฟิลด์รหัสกลุ่มตู้บรรจุสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="7a69e-170">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7a69e-171">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-171">Click New.</span></span>
6. <span data-ttu-id="7a69e-172">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7a69e-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="7a69e-173">ในฟิลด์ชนิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="7a69e-174">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-174">Click New.</span></span>
9. <span data-ttu-id="7a69e-175">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7a69e-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="7a69e-176">ในฟิลด์ชนิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="7a69e-177">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-177">Click New.</span></span>
12. <span data-ttu-id="7a69e-178">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7a69e-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="7a69e-179">ในฟิลด์ชนิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="7a69e-180">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7a69e-180">Click Save.</span></span>
15. <span data-ttu-id="7a69e-181">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="7a69e-182">ตั้งค่าเท็มเพลตการสร้างตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-182">Set up a container build template</span></span>
1. <span data-ttu-id="7a69e-183">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > เท็มเพลตการสร้างตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="7a69e-184">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-184">Click New.</span></span>
    * <span data-ttu-id="7a69e-185">เท็มเพลตการสร้างตู้บรรจุสินค้าขี้นกับว่ากระบวนการของการบรรจุลงตู้บรรจุสินค้าใดที่ถูกดำเนินการ </span><span class="sxs-lookup"><span data-stu-id="7a69e-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="7a69e-186">เท็มเพลตการสร้างตู้บรรจุสินค้าแต่ละแบบกำหนดหนึ่งรหัสกระบวนการของการบรรจุลงตู้บรรจุสินค้าที่จะถูกใช้โดยเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="7a69e-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="7a69e-187">ตัวเลือกการแก้ไขการสอบถาม อนุญาตให้คุณกำหนดเงื่อนไขว่าเท็มเพลตที่เลือกใดจะถูกประมวลผล</span><span class="sxs-lookup"><span data-stu-id="7a69e-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="7a69e-188">ตัวอย่างเช่น คุณอาจต้องการรันเฉพาะการบรรจุลงตู้บรรจุสินค้าสำหรับลูกค้าเฉพาะ ผลิตภัณฑ์ หรือคลังสินค้า หรือคุณสามารถเพิ่มช่วงการสอบถามที่สอดคล้องกันไปยังเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="7a69e-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="7a69e-189">รหัสขั้นตอนของเวฟคือ วิธีการลิงค์เท็มเพลตการสร้างตู้บรรจุสินค้าไปยังขั้นตอนต่างๆในเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="7a69e-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="7a69e-190">เมื่อมีการดำเนินการเวฟ จะกำหนดว่าเท็มเพลตการสร้างตู้บรรจุสินค้าใดที่จะถูกใช้ในการเริ่มการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="7a69e-191">ฟิลด์ชนิดการสอบถามพื้นฐานจะกำหนดสิ่งที่จะบรรจุ และสิ่งที่จะใช้เป็นพื้นฐานของการสอบถามตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="7a69e-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="7a69e-192">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7a69e-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7a69e-193">ในฟิลด์รหัสเท็มเพลตตู้บรรจุสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="7a69e-194">ในฟิลด์รหัสกลุ่มตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="7a69e-195">ในฟิลด์รหัสขั้นตอนของเวฟ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a69e-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="7a69e-196">เลือกกล่องกาเครื่องหมายการอนุญาตให้แบ่งการเบิกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="7a69e-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="7a69e-197">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7a69e-197">Click Save.</span></span>
9. <span data-ttu-id="7a69e-198">คลิกข้อจำกัดการผสมของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="7a69e-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="7a69e-199">การแบ่งตามตรรกะผสม อนุญาตให้คุณตั้งค่ากฎสำหรับการบรรจุรายการการปันส่วนในตู้บรรจุสินค้า </span><span class="sxs-lookup"><span data-stu-id="7a69e-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="7a69e-200">ตัวอย่างเช่น ถ้าคุณเพิ่มฟิลด์หมายเลขสินค้า เมื่อมีการกำหนดสินค้าให้กับตู้บรรจุสินค้า ตู้บรรจุสินค้าใหม่จะถูกสร้างเมื่อมีหมายเลขสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="7a69e-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="7a69e-201">นี่จะป้องกันผู้ปฏิบัติงานจากการบรรจุรายการการปันส่วน สำหรับลูกค้าที่ต่างกันสองรายในตู้บรรจุสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="7a69e-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="7a69e-202">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a69e-202">Click New.</span></span>
11. <span data-ttu-id="7a69e-203">ในฟิลด์ตาราง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7a69e-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="7a69e-204">ในฟิลด์การเลือกฟิลด์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a69e-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="7a69e-205">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7a69e-205">Click OK.</span></span>

