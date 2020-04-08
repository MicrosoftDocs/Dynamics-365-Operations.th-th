---
title: สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม
description: 'ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148089"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9c208-103">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="9c208-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c208-104">ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม </span><span class="sxs-lookup"><span data-stu-id="9c208-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="9c208-105">บริษัทข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือ USP2</span><span class="sxs-lookup"><span data-stu-id="9c208-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="9c208-106">สร้างความต้องการสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="9c208-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="9c208-107">ไปที่แดชบอร์ดเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="9c208-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="9c208-108">คลิกที่การประมวลผลและการสอบถามใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="9c208-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="9c208-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9c208-109">Click New.</span></span>
4. <span data-ttu-id="9c208-110">คลิกที่ใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="9c208-110">Click Sales order.</span></span>
5. <span data-ttu-id="9c208-111">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="9c208-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="9c208-112">ตัวอย่าง: US-001</span><span class="sxs-lookup"><span data-stu-id="9c208-112">Example: US-001</span></span>  
6. <span data-ttu-id="9c208-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9c208-113">Click OK.</span></span>
7. <span data-ttu-id="9c208-114">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9c208-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9c208-115">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="9c208-115">Example: P6003</span></span>  
8. <span data-ttu-id="9c208-116">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9c208-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9c208-117">ตัวอย่าง : 50000</span><span class="sxs-lookup"><span data-stu-id="9c208-117">Example: 50000</span></span>  
9. <span data-ttu-id="9c208-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9c208-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9c208-119">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="9c208-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="9c208-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c208-120">Close the page.</span></span>
2. <span data-ttu-id="9c208-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c208-121">Close the page.</span></span>
3. <span data-ttu-id="9c208-122">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="9c208-122">Click Master planning.</span></span>
4. <span data-ttu-id="9c208-123">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="9c208-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9c208-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9c208-125">ตัวอย่าง: แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="9c208-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="9c208-126">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="9c208-126">Click Run.</span></span>
7. <span data-ttu-id="9c208-127">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="9c208-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="9c208-128">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9c208-128">Click Filter.</span></span>
9. <span data-ttu-id="9c208-129">ในรายการ ให้เลือกแถวสำหรับฟิลด์ = หมายเลขสินค้า </span><span class="sxs-lookup"><span data-stu-id="9c208-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="9c208-130">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="9c208-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9c208-131">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="9c208-131">Example: P6003</span></span>  
11. <span data-ttu-id="9c208-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9c208-132">Click OK.</span></span>
12. <span data-ttu-id="9c208-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9c208-133">Click OK.</span></span>
13. <span data-ttu-id="9c208-134">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="9c208-134">Click Planned orders.</span></span>
14. <span data-ttu-id="9c208-135">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="9c208-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9c208-136">ตัวอย่างเช่น กรองฟิลด์หมายเลขสินค้าด้วยค่า 'P6000'</span><span class="sxs-lookup"><span data-stu-id="9c208-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="9c208-137">กรองด้วยสูตรสินค้าที่เป็นผลิตภัณฑ์ร่วมของสินค้าที่คุณได้สร้างใบสั่งขายให้ </span><span class="sxs-lookup"><span data-stu-id="9c208-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="9c208-138">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9c208-139">เลือกแถวใดๆที่ถูกตีกลับโดยตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="9c208-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="9c208-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9c208-141">ขยายหรือยุบส่วนความเชื่อมโยงความต้องการกับการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="9c208-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="9c208-142">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9c208-143">คำสั่งซื้อที่วางแผนไว้จะเชื่อมโยงกับใบสั่งขายสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="9c208-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="9c208-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c208-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="9c208-145">สร้างความต้องการสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="9c208-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="9c208-146">ไปที่แดชบอร์ดเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="9c208-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="9c208-147">คลิกที่การประมวลผลและการสอบถามใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="9c208-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="9c208-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9c208-148">Click New.</span></span>
4. <span data-ttu-id="9c208-149">คลิกที่ใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="9c208-149">Click Sales order.</span></span>
5. <span data-ttu-id="9c208-150">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="9c208-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="9c208-151">ตัวอย่าง: US-001</span><span class="sxs-lookup"><span data-stu-id="9c208-151">Example: US-001</span></span>  
6. <span data-ttu-id="9c208-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9c208-152">Click OK.</span></span>
7. <span data-ttu-id="9c208-153">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9c208-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9c208-154">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="9c208-154">Example: P6003</span></span>  
8. <span data-ttu-id="9c208-155">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9c208-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9c208-156">ตัวอย่าง : 50000</span><span class="sxs-lookup"><span data-stu-id="9c208-156">Example: 50000</span></span>  
9. <span data-ttu-id="9c208-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9c208-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9c208-158">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="9c208-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="9c208-159">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="9c208-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="9c208-160">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9c208-161">ตัวอย่าง: แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="9c208-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="9c208-162">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="9c208-162">Click Run.</span></span>
4. <span data-ttu-id="9c208-163">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="9c208-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="9c208-164">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9c208-164">Click Filter.</span></span>
6. <span data-ttu-id="9c208-165">ในรายการ ให้เลือกแถวสำหรับฟิลด์ = หมายเลขสินค้า </span><span class="sxs-lookup"><span data-stu-id="9c208-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="9c208-166">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="9c208-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9c208-167">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="9c208-167">Example: P6003</span></span>  
8. <span data-ttu-id="9c208-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9c208-168">Click OK.</span></span>
9. <span data-ttu-id="9c208-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9c208-169">Click OK.</span></span>
10. <span data-ttu-id="9c208-170">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="9c208-170">Click Planned orders.</span></span>
11. <span data-ttu-id="9c208-171">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="9c208-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9c208-172">ตัวอย่างเช่น กรองฟิลด์หมายเลขสินค้าด้วยค่า 'P6000'</span><span class="sxs-lookup"><span data-stu-id="9c208-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="9c208-173">กรองด้วยสูตรสินค้าที่เป็นผลิตภัณฑ์ร่วมของสินค้าที่คุณได้สร้างใบสั่งขายให้ </span><span class="sxs-lookup"><span data-stu-id="9c208-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="9c208-174">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9c208-175">เลือกแถวใดๆที่ถูกตีกลับโดยตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="9c208-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="9c208-176">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9c208-177">ขยายหรือยุบส่วนความเชื่อมโยงความต้องการกับการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="9c208-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="9c208-178">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c208-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9c208-179">คำสั่งซื้อที่วางแผนไว้จะเชื่อมโยงกับใบสั่งขายสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="9c208-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="9c208-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c208-180">Close the page.</span></span>
17. <span data-ttu-id="9c208-181">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="9c208-181">Click Master planning.</span></span>
18. <span data-ttu-id="9c208-182">ไปที่การวางแผนหลัก > การตั้งค่า > การวางแผนหลัก > พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="9c208-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="9c208-183">เลือก ไม่ ในฟิลด์การปิดใช้งานกระบวนการวางแผนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9c208-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="9c208-184">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c208-184">Close the page.</span></span>

