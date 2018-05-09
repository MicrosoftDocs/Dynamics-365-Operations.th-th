--- 
title: "สร้างใบเสนอราคาขายจำนวนมาก"
description: "ขั้นตอนเหล่านี้อธิบายวิธีการสร้างใบเสนอราคาแบบมีประสิทธิภาพเพื่อนำเสนอรูปแบบของผลิตภัณฑ์หรือบริการสำหรับนำไปส่งให้กับลูกค้า "
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e3bc39912d19880258ff7dd56c74b77b52deda3a
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="84ccf-103">สร้างใบเสนอราคาขายจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="84ccf-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84ccf-104">ขั้นตอนเหล่านี้อธิบายวิธีการสร้างใบเสนอราคาแบบมีประสิทธิภาพเพื่อนำเสนอรูปแบบของผลิตภัณฑ์หรือบริการสำหรับนำไปส่งให้กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="84ccf-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="84ccf-105">การสร้างใบเสนอราคาทั้งหมดนี้จะขึ้นอยู่กับเท็มเพลตของใบเสนอราคา </span><span class="sxs-lookup"><span data-stu-id="84ccf-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="84ccf-106">คุณสามารถทำตามขั้นตอนเหล่านี้กับข้อมูลของคุณ หรือกับบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="84ccf-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="84ccf-107">สร้างเท็มเพลตใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="84ccf-107">Create a quotation template</span></span>
1. <span data-ttu-id="84ccf-108">ไปยัง การขายและการตลาด > การตั้งค่า > ใบเสนอราคา > กลุ่มเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="84ccf-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="84ccf-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="84ccf-109">Click New.</span></span>
3. <span data-ttu-id="84ccf-110">ในฟิลด์รหัสกลุ่ม พิมพ์รหัสที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="84ccf-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="84ccf-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="84ccf-112">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="84ccf-112">Click Save.</span></span>
6. <span data-ttu-id="84ccf-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="84ccf-113">Close the page.</span></span>
7. <span data-ttu-id="84ccf-114">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > ใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84ccf-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="84ccf-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="84ccf-115">Click New.</span></span>
9. <span data-ttu-id="84ccf-116">ในฟิลด์ ชนิดบัญชี ให้เลือก 'ลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="84ccf-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="84ccf-117">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="84ccf-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="84ccf-118">Click OK.</span></span>
    * <span data-ttu-id="84ccf-119">สำหรับใบเสนอราคาที่จะกลายเป็นเท็มเพลต คุณต้องดำเนินตามขั้นตอนการตั้งค่าในส่วนหัวของใบเสนอราคา </span><span class="sxs-lookup"><span data-stu-id="84ccf-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="84ccf-120">ต้องทำสิ่งนี้ก่อนที่คุณจะเพิ่มบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="84ccf-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="84ccf-121">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="84ccf-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="84ccf-122">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="84ccf-122">Click Change view.</span></span>
14. <span data-ttu-id="84ccf-123">คลิกมุมมองหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="84ccf-123">Click Header view.</span></span>
15. <span data-ttu-id="84ccf-124">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="84ccf-125">ในฟิลด์รหัสกลุ่ม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="84ccf-126">ในฟิลด์ชื่อเท็มเพลต ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="84ccf-127">เลือก ใช่ ในฟิลด์ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="84ccf-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="84ccf-128">สามารถใช้เท็มเพลตที่ใช้งานอยู่เท่านั้น เมื่อคุณใช้เท็มเพลตกับใบเสนอราคาขายใหม่</span><span class="sxs-lookup"><span data-stu-id="84ccf-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="84ccf-129">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="84ccf-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="84ccf-130">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="84ccf-130">Click Change view.</span></span>
21. <span data-ttu-id="84ccf-131">คลิกมุมมองรายการ</span><span class="sxs-lookup"><span data-stu-id="84ccf-131">Click Line view.</span></span>
22. <span data-ttu-id="84ccf-132">ในฟิลด์สินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84ccf-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="84ccf-133">ในฟิลด์สินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84ccf-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="84ccf-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="84ccf-134">Close the page.</span></span>
25. <span data-ttu-id="84ccf-135">ในฟิลด์เปอร์เซนต์ส่วนลด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="84ccf-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="84ccf-136">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="84ccf-136">Click Add line.</span></span>
27. <span data-ttu-id="84ccf-137">ในฟิลด์สินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84ccf-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="84ccf-138">ในฟิลด์สินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84ccf-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="84ccf-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="84ccf-139">Close the page.</span></span>
30. <span data-ttu-id="84ccf-140">ในฟิลด์ราคาต่อหน่วย ให้ป้อนราคาใหม่ หรือเปลี่ยนราคาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="84ccf-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="84ccf-141">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="84ccf-141">Click Add line.</span></span>
32. <span data-ttu-id="84ccf-142">ในฟิลด์สินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84ccf-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="84ccf-143">ในฟิลด์สินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84ccf-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="84ccf-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="84ccf-144">Close the page.</span></span>
35. <span data-ttu-id="84ccf-145">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="84ccf-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="84ccf-146">ในฟิลด์ส่วนลด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="84ccf-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="84ccf-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="84ccf-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="84ccf-148">ใช้เท็มเพลตเพื่อสร้างใบเสนอราคาใบเดียว</span><span class="sxs-lookup"><span data-stu-id="84ccf-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="84ccf-149">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > ใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84ccf-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="84ccf-150">โปรดทราบว่า คุณได้สร้างใบเสนอราคาซึ่งถูกทำเครื่องหมายเป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="84ccf-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="84ccf-151">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="84ccf-151">Click New.</span></span>
3. <span data-ttu-id="84ccf-152">ในฟิลด์ ชนิดบัญชี ให้เลือก 'ลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="84ccf-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="84ccf-153">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="84ccf-154">ขยายส่วนเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="84ccf-154">Expand the Template section.</span></span>
6. <span data-ttu-id="84ccf-155">ในฟิลด์รหัสกลุ่ม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="84ccf-156">ในฟิลด์ชื่อเท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="84ccf-157">ในฟิลด์วิธีการคำนวณ ให้เลือก 'ขึ้นอยู่กับค่าเท็มเพลต'</span><span class="sxs-lookup"><span data-stu-id="84ccf-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="84ccf-158">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="84ccf-158">Click OK.</span></span>
    * <span data-ttu-id="84ccf-159">ในขณะนี้ได้สร้างใบเสนอราคาใหม่แล้ว ตามข้อมูลและเงื่อนไขของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="84ccf-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="84ccf-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="84ccf-160">Close the page.</span></span>
11. <span data-ttu-id="84ccf-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="84ccf-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="84ccf-162">ใช้เท็มเพลตเพื่อสร้างใบเสนอราคาจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="84ccf-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="84ccf-163">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > อัพเดตใบเสนอราคา > สร้างใบเสนอราคาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="84ccf-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="84ccf-164">ในฟิลด์ ชนิดบัญชี ให้เลือก 'ลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="84ccf-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="84ccf-165">ในฟิลด์รหัสกลุ่ม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="84ccf-166">ในฟิลด์ชื่อเท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="84ccf-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="84ccf-167">ในฟิลด์วิธีการคำนวณ ให้เลือก 'ขึ้นอยู่กับค่าเท็มเพลต'</span><span class="sxs-lookup"><span data-stu-id="84ccf-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="84ccf-168">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="84ccf-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="84ccf-169">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="84ccf-169">Click Filter.</span></span>
8. <span data-ttu-id="84ccf-170">ในฟิลด์เงื่อนไข ให้ตั้งค่าตัวกรองเพื่อให้ครอบคลุมกลุ่มลูกค้าที่คุณต้องการรวมไว้ในการสร้างใบเสนอราคาจำนวนมาก </span><span class="sxs-lookup"><span data-stu-id="84ccf-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="84ccf-171">ใช้รูปแบบต่อไปนี้ "Customer1 ...CustomerN</span><span class="sxs-lookup"><span data-stu-id="84ccf-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="84ccf-172">ตัวอย่างเช่น คุณสามารถตั้งค่าตัวกรองเป็น สหรัฐอเมริกา-001 ... สหรัฐอเมริกา-004</span><span class="sxs-lookup"><span data-stu-id="84ccf-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="84ccf-173">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="84ccf-173">Click OK.</span></span>
10. <span data-ttu-id="84ccf-174">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="84ccf-174">Click OK.</span></span>
11. <span data-ttu-id="84ccf-175">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > ใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84ccf-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="84ccf-176">ตรวจสอบว่าใบเสนอราคาได้ถูกสร้างไว้สำหรับลูกค้าทั้งหมดที่ระบุไว้ในชุดคำสั่งการอัพเดตโดยรวม ตามเท็มเพลตที่เลือก</span><span class="sxs-lookup"><span data-stu-id="84ccf-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


