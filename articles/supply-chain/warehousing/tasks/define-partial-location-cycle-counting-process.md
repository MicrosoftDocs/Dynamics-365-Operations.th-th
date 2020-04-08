---
title: 'กำหนดกระบวนการตรวจนับตามรอบในสถานที่บางแห่ง '
description: เมื่อคุณใช้แผนการตรวจนับตามรอบเพื่อสร้างงานการตรวจนับตามรอบ คุณสามารถใช้เป็นคู่มือการดำเนินงานการนับตามจริงโดยร้องขอให้เฉพาะผลิตภัณฑ์และผลิตภัณฑ์ย่อยเท่านั้นที่จะได้รับการตรวจนับแทนปริมาณคงคลังคงเหลือทั้งหมดที่สถานที่เก็บนั้น
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67f719d5990a4331559cab34412bf82f15eca735
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148365"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="0d086-103">กำหนดกระบวนการตรวจนับตามรอบในสถานที่บางแห่ง </span><span class="sxs-lookup"><span data-stu-id="0d086-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d086-104">เมื่อคุณใช้แผนการตรวจนับตามรอบเพื่อสร้างงานการตรวจนับตามรอบ คุณสามารถใช้เป็นคู่มือการดำเนินงานการนับตามจริงโดยร้องขอให้เฉพาะผลิตภัณฑ์และผลิตภัณฑ์ย่อยเท่านั้นที่จะได้รับการตรวจนับแทนปริมาณคงคลังคงเหลือทั้งหมดที่สถานที่เก็บนั้น</span><span class="sxs-lookup"><span data-stu-id="0d086-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="0d086-105">โดยการกรองผลิตภัณฑ์ฉพาะ ผู้จัดการคลังสินค้าสามารถลดโสหุ้ยในการตรวจทาน ช่วยป้องกันข้อผิดพลาดในการรวมบัญชี และประหยัดเวลา</span><span class="sxs-lookup"><span data-stu-id="0d086-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="0d086-106">โดยทั่วไปผู้จัดการคลังสินค้าจะดำเนินการงานการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="0d086-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="0d086-107">คุณสามารถดำเนินการกระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือในข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="0d086-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="0d086-108">สร้างเท็มเพลตงานการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="0d086-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="0d086-109">ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="0d086-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="0d086-110">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การตรวจนับตามรอบ'</span><span class="sxs-lookup"><span data-stu-id="0d086-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="0d086-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d086-111">Click New.</span></span>
4. <span data-ttu-id="0d086-112">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0d086-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="0d086-113">การเรียงลำดับคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="0d086-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="0d086-114">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="0d086-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="0d086-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0d086-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0d086-116">ในฟิลด์เท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0d086-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="0d086-117">ในฟิลด์คำอธิบายเท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0d086-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="0d086-118">ในฟิลด์รหัสกลุ่มงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0d086-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="0d086-119">ในฟิลด์ระดับความสำคัญของงาน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0d086-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="0d086-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d086-120">Click Save.</span></span>
11. <span data-ttu-id="0d086-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d086-121">Click New.</span></span>
12. <span data-ttu-id="0d086-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0d086-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="0d086-123">ในฟิลด์ประเภทงาน ให้เลือก 'การตรวจนับ'</span><span class="sxs-lookup"><span data-stu-id="0d086-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="0d086-124">ในฟิลด์รหัสคลาสงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0d086-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="0d086-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d086-125">Click Save.</span></span>
16. <span data-ttu-id="0d086-126">คลิก การจำแนกรายการงาน</span><span class="sxs-lookup"><span data-stu-id="0d086-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="0d086-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d086-127">Click New.</span></span>
18. <span data-ttu-id="0d086-128">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0d086-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="0d086-129">การเรียงลำดับคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="0d086-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="0d086-130">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="0d086-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="0d086-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d086-131">Click Save.</span></span>
20. <span data-ttu-id="0d086-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0d086-132">Close the page.</span></span>
21. <span data-ttu-id="0d086-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0d086-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="0d086-134">สร้าง แผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="0d086-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="0d086-135">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การตรวจนับตามรอบ > แผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="0d086-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="0d086-136">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d086-136">Click New.</span></span>
3. <span data-ttu-id="0d086-137">ในฟิลด์รหัสแผนการตรวจนับตามรอบ พิมพ์ ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0d086-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="0d086-138">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0d086-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0d086-139">ในฟิลด์จำนวนสูงสุดของการตรวจนับตามรอบ ป้อน หมายเลข</span><span class="sxs-lookup"><span data-stu-id="0d086-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="0d086-140">ในฟิลด์เท็มเพลตงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0d086-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="0d086-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d086-141">Click New.</span></span>
8. <span data-ttu-id="0d086-142">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0d086-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="0d086-143">การเรียงลำดับคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="0d086-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="0d086-144">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="0d086-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="0d086-145">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0d086-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="0d086-146">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d086-146">Click Save.</span></span>
11. <span data-ttu-id="0d086-147">คลิก กำหนดการสอบถามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0d086-147">Click Define product query.</span></span>
12. <span data-ttu-id="0d086-148">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0d086-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="0d086-149">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0d086-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="0d086-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0d086-150">Click OK.</span></span>
15. <span data-ttu-id="0d086-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0d086-151">Close the page.</span></span>

