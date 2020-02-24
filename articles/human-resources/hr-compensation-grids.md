---
title: ตั้งค่ากริดค่าตอบแทน
description: 'กริดค่าตอบแทนจะใช้ในการกำหนด และรักษาโครงสร้างค่าตอบแทนสำหรับแผนค่าตอบแทนที่คงที่ '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7caa740d091a9ffd85ab9e2bec382099efd05298
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010735"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="89296-103">ตั้งค่ากริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="89296-103">Set up compensation grids</span></span>

<span data-ttu-id="89296-104">กริดค่าตอบแทนจะใช้ในการกำหนด และรักษาโครงสร้างค่าตอบแทนสำหรับแผนค่าตอบแทนที่คงที่ </span><span class="sxs-lookup"><span data-stu-id="89296-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="89296-105">กริดค่าตอบแทนสามารถใช้ร่วมกันระหว่างหลายแผน หรือคัดลอกมาเมื่อสร้างแผนค่าตอบแทนใหม่ </span><span class="sxs-lookup"><span data-stu-id="89296-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="89296-106">ก่อนที่จะสร้างกริดค่าตอบแทน ระดับ และจุดอ้างอิงต้องถูกตั้งค่าก่อน </span><span class="sxs-lookup"><span data-stu-id="89296-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="89296-107">ตัวอย่างนี้จะสร้างชนิดของระดับใหม่ของกริดค่าตอบแทนโดยใช้ข้อมูลสาธิตสำหรับระดับ และจุดอ้างอิง </span><span class="sxs-lookup"><span data-stu-id="89296-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="89296-108">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="89296-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="89296-109">ตั้งค่าข้อมูลเกี่ยวกับกริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="89296-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="89296-110">ไปที่ทรัพยากรบุคคล > ค่าตอบแทน > ค่าตอบแทนคงที่ > กริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="89296-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="89296-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="89296-111">Click New.</span></span>
3. <span data-ttu-id="89296-112">ในฟิลด์กริด ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89296-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="89296-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="89296-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="89296-114">ในฟิลด์ชนิด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89296-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="89296-115">ในฟิลด์การตั้งค่าการอ้างอิง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="89296-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="89296-116">ในฟิลด์สกุลเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89296-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="89296-117">ในฟิลด์สกุลเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="89296-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="89296-118">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="89296-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="89296-119">เพิ่มระดับในโครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="89296-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="89296-120">คลิก โครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="89296-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="89296-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="89296-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="89296-122">ในฟิลด์ระดับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89296-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="89296-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="89296-123">Click New.</span></span>
5. <span data-ttu-id="89296-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="89296-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="89296-125">ในฟิลด์ระดับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89296-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="89296-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="89296-126">Click New.</span></span>
8. <span data-ttu-id="89296-127">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="89296-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="89296-128">ในฟิลด์ระดับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89296-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="89296-129">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="89296-129">Click New.</span></span>
11. <span data-ttu-id="89296-130">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="89296-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="89296-131">ในฟิลด์ระดับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89296-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="89296-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="89296-132">Click New.</span></span>
14. <span data-ttu-id="89296-133">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="89296-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="89296-134">ในฟิลด์ระดับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89296-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="89296-135">กรอกข้อมูลในโครงสร้างค่าตอบแทนด้วยค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="89296-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="89296-136">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="89296-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="89296-137">ในจำแหน่งนี้ มูลค่าค่าตอบแทนสามารถใส่ด้วยตนเองลงไปในแต่ละตารางได้ หรือสามารถใช้ฟังก์ชันการเปลี่ยนแปลงโดยรวมเพื่อกรอกข้อมูลในฟิลด์ต่างๆ ได้อย่างง่ายดาย และทำการคำนวณข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89296-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="89296-138">คลิกที่การเปลี่ยนแปลงโดยรวม</span><span class="sxs-lookup"><span data-stu-id="89296-138">Click Mass change.</span></span>
    * <span data-ttu-id="89296-139">สำหรับกริดนี้ เราจะใช้ค่าสำหรับจุดกึ่งกลางระดับแรกของฟิลด์ทั้งหมดในตาราง </span><span class="sxs-lookup"><span data-stu-id="89296-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="89296-140">นี่จะเป็นข้อมูลพื้นฐานสำหรับเมทริกซ์ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="89296-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="89296-141">ในฟิลด์ชนิดการปรับปรุง ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89296-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="89296-142">ในฟิลด์ยอดการปรับปรุง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="89296-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="89296-143">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="89296-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="89296-144">คลิกที่นำไปใช้กับกริด</span><span class="sxs-lookup"><span data-stu-id="89296-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="89296-145">ขณะนี้ เราจะใช้ฟังก์ชันการเปลี่ยนแปลงโดยรวมเพื่อเพิ่มยอดเงินในแต่ละระดับในลำดับต่อมาตามเปอร์เซ็นต์หรือยอดเงินที่แน่นอน </span><span class="sxs-lookup"><span data-stu-id="89296-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="89296-146">ในตัวอย่างนี้ แต่ละระดับจะมีการกระจาย 12.5% ระหว่างจ้างของตน</span><span class="sxs-lookup"><span data-stu-id="89296-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="89296-147">ในฟิลด์ชนิดการปรับปรุง ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89296-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="89296-148">ในฟิลด์ยอดการปรับปรุง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="89296-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="89296-149">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="89296-150">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="89296-151">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="89296-152">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="89296-153">คลิกที่นำไปใช้กับกริด</span><span class="sxs-lookup"><span data-stu-id="89296-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="89296-154">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="89296-155">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="89296-156">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="89296-157">คลิกที่นำไปใช้กับกริด</span><span class="sxs-lookup"><span data-stu-id="89296-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="89296-158">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="89296-159">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="89296-160">คลิกที่นำไปใช้กับกริด</span><span class="sxs-lookup"><span data-stu-id="89296-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="89296-161">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89296-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="89296-162">คลิกที่นำไปใช้กับกริด</span><span class="sxs-lookup"><span data-stu-id="89296-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="89296-163">ขณะนี้ เราจะใช้ฟังก์ชันเปลี่ยนแปลงโดยรวมเพื่อปรับปรุงจุดอ้างอิงค่าต่ำสุดและสูงสุดสำหรับแต่ละระดับ </span><span class="sxs-lookup"><span data-stu-id="89296-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="89296-164">ตัวอย่างนี้จะใช้การกระจาย 50% จุดอ้างอิงค่าต่ำสุดจะถูก ปรับปรุงเป็น -20% และจำนวนสูงสุดจะปรับปรุง +20%</span><span class="sxs-lookup"><span data-stu-id="89296-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="89296-165">ในฟิลด์ยอดการปรับปรุง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="89296-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="89296-166">ในฟิลด์จุดอ้างอิง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="89296-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="89296-167">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="89296-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="89296-168">คลิกที่นำไปใช้กับกริด</span><span class="sxs-lookup"><span data-stu-id="89296-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="89296-169">ในฟิลด์ยอดการปรับปรุง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="89296-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="89296-170">ในฟิลด์จุดอ้างอิง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="89296-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="89296-171">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="89296-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="89296-172">คลิกที่นำไปใช้กับกริด</span><span class="sxs-lookup"><span data-stu-id="89296-172">Click Apply to grid.</span></span>

