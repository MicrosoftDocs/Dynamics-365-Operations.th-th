---
title: 'กำหนดกระบวนการตรวจนับตามรอบในสถานที่บางแห่ง '
description: เมื่อคุณใช้แผนการตรวจนับตามรอบเพื่อสร้างงานการตรวจนับตามรอบ คุณสามารถใช้เป็นคู่มือการดำเนินงานการนับตามจริงโดยร้องขอให้เฉพาะผลิตภัณฑ์และผลิตภัณฑ์ย่อยเท่านั้นที่จะได้รับการตรวจนับแทนปริมาณคงคลังคงเหลือทั้งหมดที่สถานที่เก็บนั้น
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfea71459b80712c924912d909a0fdfa5fad09ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238953"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="e62cc-103">กำหนดกระบวนการตรวจนับตามรอบในสถานที่บางแห่ง </span><span class="sxs-lookup"><span data-stu-id="e62cc-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e62cc-104">เมื่อคุณใช้แผนการตรวจนับตามรอบเพื่อสร้างงานการตรวจนับตามรอบ คุณสามารถใช้เป็นคู่มือการดำเนินงานการนับตามจริงโดยร้องขอให้เฉพาะผลิตภัณฑ์และผลิตภัณฑ์ย่อยเท่านั้นที่จะได้รับการตรวจนับแทนปริมาณคงคลังคงเหลือทั้งหมดที่สถานที่เก็บนั้น</span><span class="sxs-lookup"><span data-stu-id="e62cc-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="e62cc-105">โดยการกรองผลิตภัณฑ์ฉพาะ ผู้จัดการคลังสินค้าสามารถลดโสหุ้ยในการตรวจทาน ช่วยป้องกันข้อผิดพลาดในการรวมบัญชี และประหยัดเวลา</span><span class="sxs-lookup"><span data-stu-id="e62cc-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="e62cc-106">โดยทั่วไปผู้จัดการคลังสินค้าจะดำเนินการงานการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="e62cc-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="e62cc-107">คุณสามารถดำเนินการกระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือในข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="e62cc-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="e62cc-108">สร้างเท็มเพลตงานการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="e62cc-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="e62cc-109">ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="e62cc-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="e62cc-110">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การตรวจนับตามรอบ'</span><span class="sxs-lookup"><span data-stu-id="e62cc-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="e62cc-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e62cc-111">Click New.</span></span>
4. <span data-ttu-id="e62cc-112">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e62cc-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="e62cc-113">การเรียงลำดับคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="e62cc-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="e62cc-114">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="e62cc-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="e62cc-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e62cc-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="e62cc-116">ในฟิลด์เท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e62cc-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="e62cc-117">ในฟิลด์คำอธิบายเท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e62cc-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="e62cc-118">ในฟิลด์รหัสกลุ่มงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e62cc-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="e62cc-119">ในฟิลด์ระดับความสำคัญของงาน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="e62cc-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="e62cc-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e62cc-120">Click Save.</span></span>
11. <span data-ttu-id="e62cc-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e62cc-121">Click New.</span></span>
12. <span data-ttu-id="e62cc-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e62cc-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="e62cc-123">ในฟิลด์ประเภทงาน ให้เลือก 'การตรวจนับ'</span><span class="sxs-lookup"><span data-stu-id="e62cc-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="e62cc-124">ในฟิลด์รหัสคลาสงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e62cc-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="e62cc-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e62cc-125">Click Save.</span></span>
16. <span data-ttu-id="e62cc-126">คลิก การจำแนกรายการงาน</span><span class="sxs-lookup"><span data-stu-id="e62cc-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="e62cc-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e62cc-127">Click New.</span></span>
18. <span data-ttu-id="e62cc-128">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e62cc-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="e62cc-129">การเรียงลำดับคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="e62cc-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="e62cc-130">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="e62cc-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="e62cc-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e62cc-131">Click Save.</span></span>
20. <span data-ttu-id="e62cc-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e62cc-132">Close the page.</span></span>
21. <span data-ttu-id="e62cc-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e62cc-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="e62cc-134">สร้าง แผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="e62cc-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="e62cc-135">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การตรวจนับตามรอบ > แผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="e62cc-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="e62cc-136">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e62cc-136">Click New.</span></span>
3. <span data-ttu-id="e62cc-137">ในฟิลด์รหัสแผนการตรวจนับตามรอบ พิมพ์ ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e62cc-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="e62cc-138">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e62cc-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e62cc-139">ในฟิลด์จำนวนสูงสุดของการตรวจนับตามรอบ ป้อน หมายเลข</span><span class="sxs-lookup"><span data-stu-id="e62cc-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="e62cc-140">ในฟิลด์เท็มเพลตงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e62cc-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="e62cc-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e62cc-141">Click New.</span></span>
8. <span data-ttu-id="e62cc-142">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e62cc-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="e62cc-143">การเรียงลำดับคือจากหมายเลขที่น้อยที่สุดไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="e62cc-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="e62cc-144">ค่าต้องมากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="e62cc-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="e62cc-145">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e62cc-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="e62cc-146">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e62cc-146">Click Save.</span></span>
11. <span data-ttu-id="e62cc-147">คลิก กำหนดการสอบถามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e62cc-147">Click Define product query.</span></span>
12. <span data-ttu-id="e62cc-148">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e62cc-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="e62cc-149">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e62cc-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="e62cc-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e62cc-150">Click OK.</span></span>
15. <span data-ttu-id="e62cc-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e62cc-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]