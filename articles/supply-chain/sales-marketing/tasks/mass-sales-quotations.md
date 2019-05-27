---
title: สร้างใบเสนอราคาขายจำนวนมาก
description: 'ขั้นตอนเหล่านี้อธิบายวิธีการสร้างใบเสนอราคาแบบมีประสิทธิภาพเพื่อนำเสนอรูปแบบของผลิตภัณฑ์หรือบริการสำหรับนำไปส่งให้กับลูกค้า '
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0e9ddf38106fce3ed6a6f908826f2196c97a45a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562126"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="b1a6c-103">สร้างใบเสนอราคาขายจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1a6c-104">ขั้นตอนเหล่านี้อธิบายวิธีการสร้างใบเสนอราคาแบบมีประสิทธิภาพเพื่อนำเสนอรูปแบบของผลิตภัณฑ์หรือบริการสำหรับนำไปส่งให้กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="b1a6c-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="b1a6c-105">การสร้างใบเสนอราคาทั้งหมดนี้จะขึ้นอยู่กับเท็มเพลตของใบเสนอราคา </span><span class="sxs-lookup"><span data-stu-id="b1a6c-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="b1a6c-106">คุณสามารถทำตามขั้นตอนเหล่านี้กับข้อมูลของคุณ หรือกับบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="b1a6c-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="b1a6c-107">สร้างเท็มเพลตใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="b1a6c-107">Create a quotation template</span></span>
1. <span data-ttu-id="b1a6c-108">ไปยัง การขายและการตลาด > การตั้งค่า > ใบเสนอราคา > กลุ่มเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="b1a6c-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="b1a6c-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-109">Click New.</span></span>
3. <span data-ttu-id="b1a6c-110">ในฟิลด์รหัสกลุ่ม พิมพ์รหัสที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="b1a6c-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b1a6c-112">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-112">Click Save.</span></span>
6. <span data-ttu-id="b1a6c-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-113">Close the page.</span></span>
7. <span data-ttu-id="b1a6c-114">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > ใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b1a6c-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="b1a6c-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-115">Click New.</span></span>
9. <span data-ttu-id="b1a6c-116">ในฟิลด์ ชนิดบัญชี ให้เลือก 'ลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="b1a6c-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="b1a6c-117">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="b1a6c-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-118">Click OK.</span></span>
    * <span data-ttu-id="b1a6c-119">สำหรับใบเสนอราคาที่จะกลายเป็นเท็มเพลต คุณต้องดำเนินตามขั้นตอนการตั้งค่าในส่วนหัวของใบเสนอราคา </span><span class="sxs-lookup"><span data-stu-id="b1a6c-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="b1a6c-120">ต้องทำสิ่งนี้ก่อนที่คุณจะเพิ่มบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="b1a6c-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="b1a6c-121">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="b1a6c-122">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-122">Click Change view.</span></span>
14. <span data-ttu-id="b1a6c-123">คลิกมุมมองหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="b1a6c-123">Click Header view.</span></span>
15. <span data-ttu-id="b1a6c-124">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="b1a6c-125">ในฟิลด์รหัสกลุ่ม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="b1a6c-126">ในฟิลด์ชื่อเท็มเพลต ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="b1a6c-127">เลือก ใช่ ในฟิลด์ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b1a6c-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="b1a6c-128">สามารถใช้เท็มเพลตที่ใช้งานอยู่เท่านั้น เมื่อคุณใช้เท็มเพลตกับใบเสนอราคาขายใหม่</span><span class="sxs-lookup"><span data-stu-id="b1a6c-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="b1a6c-129">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="b1a6c-130">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-130">Click Change view.</span></span>
21. <span data-ttu-id="b1a6c-131">คลิกมุมมองรายการ</span><span class="sxs-lookup"><span data-stu-id="b1a6c-131">Click Line view.</span></span>
22. <span data-ttu-id="b1a6c-132">ในฟิลด์สินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="b1a6c-133">ในฟิลด์สินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="b1a6c-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-134">Close the page.</span></span>
25. <span data-ttu-id="b1a6c-135">ในฟิลด์เปอร์เซนต์ส่วนลด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b1a6c-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="b1a6c-136">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="b1a6c-136">Click Add line.</span></span>
27. <span data-ttu-id="b1a6c-137">ในฟิลด์สินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="b1a6c-138">ในฟิลด์สินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="b1a6c-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-139">Close the page.</span></span>
30. <span data-ttu-id="b1a6c-140">ในฟิลด์ราคาต่อหน่วย ให้ป้อนราคาใหม่ หรือเปลี่ยนราคาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b1a6c-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="b1a6c-141">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="b1a6c-141">Click Add line.</span></span>
32. <span data-ttu-id="b1a6c-142">ในฟิลด์สินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="b1a6c-143">ในฟิลด์สินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="b1a6c-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-144">Close the page.</span></span>
35. <span data-ttu-id="b1a6c-145">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b1a6c-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="b1a6c-146">ในฟิลด์ส่วนลด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b1a6c-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="b1a6c-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="b1a6c-148">ใช้เท็มเพลตเพื่อสร้างใบเสนอราคาใบเดียว</span><span class="sxs-lookup"><span data-stu-id="b1a6c-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="b1a6c-149">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > ใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b1a6c-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="b1a6c-150">โปรดทราบว่า คุณได้สร้างใบเสนอราคาซึ่งถูกทำเครื่องหมายเป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="b1a6c-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="b1a6c-151">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-151">Click New.</span></span>
3. <span data-ttu-id="b1a6c-152">ในฟิลด์ ชนิดบัญชี ให้เลือก 'ลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="b1a6c-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="b1a6c-153">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="b1a6c-154">ขยายส่วนเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="b1a6c-154">Expand the Template section.</span></span>
6. <span data-ttu-id="b1a6c-155">ในฟิลด์รหัสกลุ่ม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="b1a6c-156">ในฟิลด์ชื่อเท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="b1a6c-157">ในฟิลด์วิธีการคำนวณ ให้เลือก 'ขึ้นอยู่กับค่าเท็มเพลต'</span><span class="sxs-lookup"><span data-stu-id="b1a6c-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="b1a6c-158">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-158">Click OK.</span></span>
    * <span data-ttu-id="b1a6c-159">ในขณะนี้ได้สร้างใบเสนอราคาใหม่แล้ว ตามข้อมูลและเงื่อนไขของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="b1a6c-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="b1a6c-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-160">Close the page.</span></span>
11. <span data-ttu-id="b1a6c-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="b1a6c-162">ใช้เท็มเพลตเพื่อสร้างใบเสนอราคาจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="b1a6c-163">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > อัพเดตใบเสนอราคา > สร้างใบเสนอราคาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="b1a6c-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="b1a6c-164">ในฟิลด์ ชนิดบัญชี ให้เลือก 'ลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="b1a6c-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="b1a6c-165">ในฟิลด์รหัสกลุ่ม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="b1a6c-166">ในฟิลด์ชื่อเท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b1a6c-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="b1a6c-167">ในฟิลด์วิธีการคำนวณ ให้เลือก 'ขึ้นอยู่กับค่าเท็มเพลต'</span><span class="sxs-lookup"><span data-stu-id="b1a6c-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="b1a6c-168">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="b1a6c-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="b1a6c-169">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b1a6c-169">Click Filter.</span></span>
8. <span data-ttu-id="b1a6c-170">ในฟิลด์เงื่อนไข ให้ตั้งค่าตัวกรองเพื่อให้ครอบคลุมกลุ่มลูกค้าที่คุณต้องการรวมไว้ในการสร้างใบเสนอราคาจำนวนมาก </span><span class="sxs-lookup"><span data-stu-id="b1a6c-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="b1a6c-171">ใช้รูปแบบต่อไปนี้ "Customer1 ...CustomerN</span><span class="sxs-lookup"><span data-stu-id="b1a6c-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="b1a6c-172">ตัวอย่างเช่น คุณสามารถตั้งค่าตัวกรองเป็น สหรัฐอเมริกา-001 ... สหรัฐอเมริกา-004</span><span class="sxs-lookup"><span data-stu-id="b1a6c-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="b1a6c-173">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-173">Click OK.</span></span>
10. <span data-ttu-id="b1a6c-174">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1a6c-174">Click OK.</span></span>
11. <span data-ttu-id="b1a6c-175">ไปยัง การขายและการตลาด > ใบเสนอราคาขาย > ใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b1a6c-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="b1a6c-176">ตรวจสอบว่าใบเสนอราคาได้ถูกสร้างไว้สำหรับลูกค้าทั้งหมดที่ระบุไว้ในชุดคำสั่งการอัพเดตโดยรวม ตามเท็มเพลตที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b1a6c-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

