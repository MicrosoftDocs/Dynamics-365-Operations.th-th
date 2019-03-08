---
title: สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่ตั้งค่าคอนฟิก
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อของหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่มีการจัดโครงแบบ และวิธีการติดไปกับผลิตภัณฑ์หลักที่จัดโครงแบบได้ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800afdf075f0675185514158f3b712a0fe7675e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "336094"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="247cf-103">สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="247cf-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="247cf-104">กระบวนงานนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีแนบกับผลิตภัณฑ์หลักที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="247cf-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="247cf-105">กระบวนงานนี้ยังแสดงวิธีการสร้างระบบการตั้งชื่อการจัดโครงแบบสำหรับส่วนประกอบแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="247cf-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="247cf-106">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="247cf-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="247cf-107">ระบบการตั้งชื่อของหมายเลขผลิตภัณฑ์ใหม่ถูกกำหนดให้กับผลิตภัณฑ์หลัก D0004 </span><span class="sxs-lookup"><span data-stu-id="247cf-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="247cf-108">โดยทั่วไปงานนี้อาจดำเนินการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="247cf-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="247cf-109">สร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="247cf-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="247cf-110">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="247cf-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="247cf-111">คลิก ระบบการตั้งชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="247cf-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="247cf-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="247cf-112">Click New.</span></span>
4. <span data-ttu-id="247cf-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="247cf-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="247cf-114">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="247cf-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="247cf-115">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-115">Click Add.</span></span>
7. <span data-ttu-id="247cf-116">คลิก หมายเลขผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="247cf-116">Click Product master number.</span></span>
8. <span data-ttu-id="247cf-117">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-117">Click Add.</span></span>
9. <span data-ttu-id="247cf-118">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="247cf-118">Click Text constant.</span></span>
10. <span data-ttu-id="247cf-119">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="247cf-120">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="247cf-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="247cf-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-121">Click Add.</span></span>
13. <span data-ttu-id="247cf-122">คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="247cf-122">Click Configuration.</span></span>
14. <span data-ttu-id="247cf-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="247cf-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="247cf-124">กำหนดระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="247cf-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="247cf-125">คลิก ผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="247cf-125">Click Product masters.</span></span>
2. <span data-ttu-id="247cf-126">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="247cf-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="247cf-127">เช่น กรองข้อมูลในฟิลด์ หมายเลขผลิตภัณฑ์ ด้วยค่า 'D'</span><span class="sxs-lookup"><span data-stu-id="247cf-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="247cf-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="247cf-129">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="247cf-129">Click Edit.</span></span>
5. <span data-ttu-id="247cf-130">เลือก ใช่ ในฟิลด์ใช้ระบบการตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="247cf-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="247cf-131">ในฟิลด์ ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="247cf-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="247cf-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="247cf-132">Close the page.</span></span>
8. <span data-ttu-id="247cf-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="247cf-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="247cf-134">สร้างระบบการตั้งชื่อสำหรับส่วนประกอบแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="247cf-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="247cf-135">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="247cf-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="247cf-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="247cf-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="247cf-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="247cf-138">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="247cf-138">Click Edit.</span></span>
5. <span data-ttu-id="247cf-139">เลือก ใช่ ในฟิลด์ ใช้ระบบการตั้งชื่อการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="247cf-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="247cf-140">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-140">Click Add.</span></span>
7. <span data-ttu-id="247cf-141">คลิก ค่าแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="247cf-141">Click Attribute value.</span></span>
8. <span data-ttu-id="247cf-142">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="247cf-143">ในฟิลด์ แอททริบิวต์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="247cf-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="247cf-144">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-144">Click Add.</span></span>
11. <span data-ttu-id="247cf-145">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="247cf-145">Click Text constant.</span></span>
12. <span data-ttu-id="247cf-146">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="247cf-147">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="247cf-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="247cf-148">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-148">Click Add.</span></span>
15. <span data-ttu-id="247cf-149">คลิก ค่าแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="247cf-149">Click Attribute value.</span></span>
16. <span data-ttu-id="247cf-150">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="247cf-151">ในฟิลด์ แอททริบิวต์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="247cf-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="247cf-152">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-152">Click Add.</span></span>
19. <span data-ttu-id="247cf-153">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="247cf-153">Click Text constant.</span></span>
20. <span data-ttu-id="247cf-154">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="247cf-155">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="247cf-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="247cf-156">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-156">Click Add.</span></span>
23. <span data-ttu-id="247cf-157">คลิก ค่าแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="247cf-157">Click Attribute value.</span></span>
24. <span data-ttu-id="247cf-158">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="247cf-159">ในฟิลด์ แอททริบิวต์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="247cf-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="247cf-160">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-160">Click Add.</span></span>
27. <span data-ttu-id="247cf-161">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="247cf-161">Click Text constant.</span></span>
28. <span data-ttu-id="247cf-162">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="247cf-163">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="247cf-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="247cf-164">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-164">Click Add.</span></span>
31. <span data-ttu-id="247cf-165">คลิก ค่าแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="247cf-165">Click Attribute value.</span></span>
32. <span data-ttu-id="247cf-166">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="247cf-167">ในฟิลด์ แอททริบิวต์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="247cf-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="247cf-168">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-168">Click Add.</span></span>
35. <span data-ttu-id="247cf-169">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="247cf-169">Click Text constant.</span></span>
36. <span data-ttu-id="247cf-170">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="247cf-171">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="247cf-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="247cf-172">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="247cf-172">Click Add.</span></span>
39. <span data-ttu-id="247cf-173">คลิก ค่าของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="247cf-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="247cf-174">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="247cf-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="247cf-175">ในฟิลด์ลำดับหมายเลข ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="247cf-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="247cf-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="247cf-176">Close the page.</span></span>
43. <span data-ttu-id="247cf-177">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="247cf-177">Close the page.</span></span>
44. <span data-ttu-id="247cf-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="247cf-178">Close the page.</span></span>

