---
title: " กำหนดโปรแกรมตอบแทนลูกค้าสมาชิก"
description: 'กระบวนการนี้แสดงวิธีการตั้งค่าโปรแกรมตอบแทนลูกค้าสมาชิกที่มีระดับสมาชิกสองขั้น '
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e57bb9c9e3348f2a9853dfda1351a8a75261beb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "355322"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="b4e1d-103"> กำหนดโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b4e1d-104">กระบวนการนี้แสดงวิธีการตั้งค่าโปรแกรมตอบแทนลูกค้าสมาชิกที่มีระดับสมาชิกสองขั้น </span><span class="sxs-lookup"><span data-stu-id="b4e1d-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="b4e1d-105">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="b4e1d-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="b4e1d-106">ไปที่ การขายปลีกและการค้า > ..</span><span class="sxs-lookup"><span data-stu-id="b4e1d-106">Go to Retail and commerce > ..</span></span> <span data-ttu-id="b4e1d-107">> โปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="b4e1d-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b4e1d-108">Click New.</span></span>
3. <span data-ttu-id="b4e1d-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="b4e1d-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b4e1d-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b4e1d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b4e1d-111">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="b4e1d-111">Click Add line.</span></span>
6. <span data-ttu-id="b4e1d-112">ในฟิลด์ระดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b4e1d-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="b4e1d-113">ในฟิลด์ระดับ ให้ป้อนชื่อสำหรับระดับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="b4e1d-114">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b4e1d-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="b4e1d-115">ในฟิลด์ช่วงวันที่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b4e1d-116">ช่วงวันที่นี้ควรขยายไปในอนาคต</span><span class="sxs-lookup"><span data-stu-id="b4e1d-116">This date interval should extend into the future.</span></span> <span data-ttu-id="b4e1d-117">ตัวอย่างเช่น ถ้าช่วงวันที่ที่เลือกไว้สำหรับระดับทองเป็นระยะเวลาหนึ่งปี ลูกค้าใดๆที่ตรงตามเงื่อนไขสำหรับระดับทอง สามารถรับรางวัลที่ถูกกำหนดให้กับระดับทองเป็นเวลาหนึ่งปี</span><span class="sxs-lookup"><span data-stu-id="b4e1d-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="b4e1d-118">ถ้าลูกค้ามีการเปลี่ยนแปลงคุณสมบัติเป็นระดับทองขณะที่ลูกค้ายังอยู่ในระดับนั้น วันที่ระดับหมดอายุจะถูกขยายออกไปอีกหนึ่งปีหลังจากวันที่ลูกค้ามีการเปลี่ยนแปลงคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b4e1d-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="b4e1d-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b4e1d-120">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="b4e1d-120">Click Add line.</span></span>
12. <span data-ttu-id="b4e1d-121">ในฟิลด์ระดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b4e1d-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="b4e1d-122">ในฟิลด์ระดับ ให้ป้อนชื่อสำหรับระดับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="b4e1d-123">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b4e1d-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="b4e1d-124">ในฟิลด์ช่วงวันที่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="b4e1d-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b4e1d-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-126">Click Save.</span></span>
18. <span data-ttu-id="b4e1d-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b4e1d-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b4e1d-128">กฎของระดับกำหนดจำนวนคะแนนขั้นต่ำสำหรับคะแนนรางวัลที่จำเป็นต้องได้รับในช่วงเวลานั้น เพื่อที่ลูกค้าจะได้มีคุณสมบัติเหมาะสมตามระดับนั้น</span><span class="sxs-lookup"><span data-stu-id="b4e1d-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="b4e1d-129">สลับการขยายส่วนกฎของระดับ</span><span class="sxs-lookup"><span data-stu-id="b4e1d-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="b4e1d-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b4e1d-130">Click New.</span></span>
    * <span data-ttu-id="b4e1d-131">คุณสามารถมีกฎระดับมากกว่าหนึ่งกฎสำหรับระดับแต่ละขั้น </span><span class="sxs-lookup"><span data-stu-id="b4e1d-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="b4e1d-132">ตัวอย่างเช่น คุณอาจมีเงื่อนไขที่แตกต่างกันได้ 3 ประเภทเพื่อที่จะได้เข้าไปอยู่ในระดับนั้น; โดยการใช้จ่าย $500 ในหนึ่งเดือน โดยการใช้จ่ายมากกว่า $1000 ในหนึ่งปี และมีธุรกรรม 20 รายการในหนึ่งปี </span><span class="sxs-lookup"><span data-stu-id="b4e1d-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="b4e1d-133">การทำเช่นนี้คุณจะต้องสร้างกฎของระดับ 3 ประเภท</span><span class="sxs-lookup"><span data-stu-id="b4e1d-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="b4e1d-134">ในฟิลด์คะแนนรางวัล ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b4e1d-135">นี่ควรเป็นคะแนนรางวัลที่ไม่สามารถแลกได้สำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="b4e1d-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="b4e1d-137">ในฟิลด์คะแนนต่ำสุดที่ออกให้ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b4e1d-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="b4e1d-138">สำหรับระดับระดับต่ำสุด ถ้าลูกค้าทั้งหมดมีคุณสมบัติได้รับเพียงแค่การเข้าร่วมในโปรแกรม ให้ป้อน '0'</span><span class="sxs-lookup"><span data-stu-id="b4e1d-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="b4e1d-139">ในฟิลด์ช่วงวันที่การประเมิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b4e1d-140">ช่วงวันที่นี้ควรขยายไปในอดีต</span><span class="sxs-lookup"><span data-stu-id="b4e1d-140">This date interval should extend into the past.</span></span> <span data-ttu-id="b4e1d-141">เฉพาะคะแนนที่ได้ในระหว่างช่วงวันที่นี้จะถูกนำไปนับ เพื่อให้ถึงค่าต่ำสุดของคะแนนสะสมที่ออกให้</span><span class="sxs-lookup"><span data-stu-id="b4e1d-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="b4e1d-142">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="b4e1d-143">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-143">Click Save.</span></span>
27. <span data-ttu-id="b4e1d-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b4e1d-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="b4e1d-145">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b4e1d-145">Click New.</span></span>
29. <span data-ttu-id="b4e1d-146">ในฟิลด์คะแนนรางวัล ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="b4e1d-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="b4e1d-148">ในฟิลด์คะแนนต่ำสุดที่ออกให้ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b4e1d-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="b4e1d-149">ในฟิลด์ช่วงวันที่การประเมิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b4e1d-150">ช่วงวันที่นี้ควรขยายไปสู่ในอดีต </span><span class="sxs-lookup"><span data-stu-id="b4e1d-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="b4e1d-151">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="b4e1d-152">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-152">Click Save.</span></span>
35. <span data-ttu-id="b4e1d-153">คลิกกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-153">Click Price groups.</span></span>
    * <span data-ttu-id="b4e1d-154">ถ้าคุณต้องการให้ส่วนลดแก่ลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="b4e1d-155">คุณจะต้องกำหนดกลุ่มราคาหนึ่งกลุ่มหรือมากกว่านั้นสำหรับโปรแกรมตอบแทนลูกค้าสมาชิก และกำหนดกลุ่มราคาเพื่อให้ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="b4e1d-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="b4e1d-156">เป็นแนวทางปฏิบัติที่ดีที่สุดเพื่อไม่ให้มีการผสมกันของกลุ่มราคาระหว่างชนิดต่างๆของเอนทิตีส่วนลด</span><span class="sxs-lookup"><span data-stu-id="b4e1d-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="b4e1d-157">ตัวอย่างเช่น อย่าใช้กลุ่มราคาเดียวกันสำหรับส่วนลดสำหรับสมาชิกและช่องทางส่วนลด</span><span class="sxs-lookup"><span data-stu-id="b4e1d-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="b4e1d-158">ในฟิลด์กลุ่มราคา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b4e1d-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b4e1d-159">ลิงค์กลุ่มราคาที่ด้านบนของหน้าเป็นของโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="b4e1d-160">กลุ่มราคาที่ลิงค์ระดับโปรแกรมในแท็บด่วน เฉพาะลูกค้าระดับสมาชิกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b4e1d-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="b4e1d-161">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="b4e1d-162">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-162">Click Save.</span></span>
39. <span data-ttu-id="b4e1d-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b4e1d-163">Close the page.</span></span>
40. <span data-ttu-id="b4e1d-164">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b4e1d-164">Click Save.</span></span>

