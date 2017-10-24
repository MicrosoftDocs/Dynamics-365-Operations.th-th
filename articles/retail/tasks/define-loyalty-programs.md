--- 
title: " กำหนดโปรแกรมตอบแทนลูกค้าสมาชิก"
description: "กระบวนการนี้แสดงวิธีการตั้งค่าโปรแกรมตอบแทนลูกค้าสมาชิกที่มีระดับสมาชิกสองขั้น "
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a949d5cb4f01518b46bc4b1769de34196109050
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="define-loyalty-programs"></a><span data-ttu-id="28e01-103"> กำหนดโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="28e01-103">Define loyalty programs</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="28e01-104">กระบวนการนี้แสดงวิธีการตั้งค่าโปรแกรมตอบแทนลูกค้าสมาชิกที่มีระดับสมาชิกสองขั้น </span><span class="sxs-lookup"><span data-stu-id="28e01-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="28e01-105">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="28e01-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="28e01-106">ไปที่ การขายปลีกและการค้า > ..</span><span class="sxs-lookup"><span data-stu-id="28e01-106">Go to Retail and commerce > ..</span></span> <span data-ttu-id="28e01-107">> โปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="28e01-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="28e01-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="28e01-108">Click New.</span></span>
3. <span data-ttu-id="28e01-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="28e01-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="28e01-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="28e01-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="28e01-111">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="28e01-111">Click Add line.</span></span>
6. <span data-ttu-id="28e01-112">ในฟิลด์ระดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="28e01-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="28e01-113">ในฟิลด์ระดับ ให้ป้อนชื่อสำหรับระดับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="28e01-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="28e01-114">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="28e01-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="28e01-115">ในฟิลด์ช่วงวันที่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="28e01-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="28e01-116">ช่วงวันที่นี้ควรขยายไปในอนาคต</span><span class="sxs-lookup"><span data-stu-id="28e01-116">This date interval should extend into the future.</span></span> <span data-ttu-id="28e01-117">ตัวอย่างเช่น ถ้าช่วงวันที่ที่เลือกไว้สำหรับระดับทองเป็นระยะเวลาหนึ่งปี ลูกค้าใดๆที่ตรงตามเงื่อนไขสำหรับระดับทอง สามารถรับรางวัลที่ถูกกำหนดให้กับระดับทองเป็นเวลาหนึ่งปี</span><span class="sxs-lookup"><span data-stu-id="28e01-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="28e01-118">ถ้าลูกค้ามีการเปลี่ยนแปลงคุณสมบัติเป็นระดับทองขณะที่ลูกค้ายังอยู่ในระดับนั้น วันที่ระดับหมดอายุจะถูกขยายออกไปอีกหนึ่งปีหลังจากวันที่ลูกค้ามีการเปลี่ยนแปลงคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="28e01-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="28e01-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28e01-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="28e01-120">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="28e01-120">Click Add line.</span></span>
12. <span data-ttu-id="28e01-121">ในฟิลด์ระดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="28e01-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="28e01-122">ในฟิลด์ระดับ ให้ป้อนชื่อสำหรับระดับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="28e01-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="28e01-123">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="28e01-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="28e01-124">ในฟิลด์ช่วงวันที่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="28e01-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="28e01-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28e01-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="28e01-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="28e01-126">Click Save.</span></span>
18. <span data-ttu-id="28e01-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="28e01-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28e01-128">กฎของระดับกำหนดจำนวนคะแนนขั้นต่ำสำหรับคะแนนรางวัลที่จำเป็นต้องได้รับในช่วงเวลานั้น เพื่อที่ลูกค้าจะได้มีคุณสมบัติเหมาะสมตามระดับนั้น</span><span class="sxs-lookup"><span data-stu-id="28e01-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="28e01-129">สลับการขยายส่วนกฎของระดับ</span><span class="sxs-lookup"><span data-stu-id="28e01-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="28e01-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="28e01-130">Click New.</span></span>
    * <span data-ttu-id="28e01-131">คุณสามารถมีกฎระดับมากกว่าหนึ่งกฎสำหรับระดับแต่ละขั้น </span><span class="sxs-lookup"><span data-stu-id="28e01-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="28e01-132">ตัวอย่างเช่น คุณอาจมีเงื่อนไขที่แตกต่างกันได้ 3 ประเภทเพื่อที่จะได้เข้าไปอยู่ในระดับนั้น; โดยการใช้จ่าย $500 ในหนึ่งเดือน โดยการใช้จ่ายมากกว่า $1000 ในหนึ่งปี และมีธุรกรรม 20 รายการในหนึ่งปี </span><span class="sxs-lookup"><span data-stu-id="28e01-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="28e01-133">การทำเช่นนี้คุณจะต้องสร้างกฎของระดับ 3 ประเภท</span><span class="sxs-lookup"><span data-stu-id="28e01-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="28e01-134">ในฟิลด์คะแนนรางวัล ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="28e01-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="28e01-135">นี่ควรเป็นคะแนนรางวัลที่ไม่สามารถแลกได้สำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="28e01-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="28e01-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28e01-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="28e01-137">ในฟิลด์คะแนนต่ำสุดที่ออกให้ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="28e01-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="28e01-138">สำหรับระดับระดับต่ำสุด ถ้าลูกค้าทั้งหมดมีคุณสมบัติได้รับเพียงแค่การเข้าร่วมในโปรแกรม ให้ป้อน '0'</span><span class="sxs-lookup"><span data-stu-id="28e01-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="28e01-139">ในฟิลด์ช่วงวันที่การประเมิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="28e01-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="28e01-140">ช่วงวันที่นี้ควรขยายไปในอดีต</span><span class="sxs-lookup"><span data-stu-id="28e01-140">This date interval should extend into the past.</span></span> <span data-ttu-id="28e01-141">เฉพาะคะแนนที่ได้ในระหว่างช่วงวันที่นี้จะถูกนำไปนับ เพื่อให้ถึงค่าต่ำสุดของคะแนนสะสมที่ออกให้</span><span class="sxs-lookup"><span data-stu-id="28e01-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="28e01-142">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28e01-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="28e01-143">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="28e01-143">Click Save.</span></span>
27. <span data-ttu-id="28e01-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="28e01-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="28e01-145">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="28e01-145">Click New.</span></span>
29. <span data-ttu-id="28e01-146">ในฟิลด์คะแนนรางวัล ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="28e01-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="28e01-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28e01-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="28e01-148">ในฟิลด์คะแนนต่ำสุดที่ออกให้ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="28e01-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="28e01-149">ในฟิลด์ช่วงวันที่การประเมิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="28e01-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="28e01-150">ช่วงวันที่นี้ควรขยายไปสู่ในอดีต </span><span class="sxs-lookup"><span data-stu-id="28e01-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="28e01-151">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28e01-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="28e01-152">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="28e01-152">Click Save.</span></span>
35. <span data-ttu-id="28e01-153">คลิกกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="28e01-153">Click Price groups.</span></span>
    * <span data-ttu-id="28e01-154">ถ้าคุณต้องการให้ส่วนลดแก่ลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="28e01-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="28e01-155">คุณจะต้องกำหนดกลุ่มราคาหนึ่งกลุ่มหรือมากกว่านั้นสำหรับโปรแกรมตอบแทนลูกค้าสมาชิก และกำหนดกลุ่มราคาเพื่อให้ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="28e01-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="28e01-156">นี่คือแนวทางปฏิบัติที่ดีที่สุด โดยการไม่ผสมกลุ่มราคาระหว่างเอนทิตี้ต่างๆที่ลดราคา</span><span class="sxs-lookup"><span data-stu-id="28e01-156">It is a best practise to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="28e01-157">ตัวอย่างเช่น อย่าใช้กลุ่มราคาเดียวกันสำหรับส่วนลดสำหรับสมาชิกและช่องทางส่วนลด</span><span class="sxs-lookup"><span data-stu-id="28e01-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="28e01-158">ในฟิลด์กลุ่มราคา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="28e01-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="28e01-159">ลิงค์กลุ่มราคาที่ด้านบนของหน้าเป็นของโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="28e01-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="28e01-160">กลุ่มราคาที่ลิงค์ระดับโปรแกรมในแท็บด่วน เฉพาะลูกค้าระดับสมาชิกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="28e01-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="28e01-161">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28e01-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="28e01-162">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="28e01-162">Click Save.</span></span>
39. <span data-ttu-id="28e01-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="28e01-163">Close the page.</span></span>
40. <span data-ttu-id="28e01-164">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="28e01-164">Click Save.</span></span>


