---
title: สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม
description: 'ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982220"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="51cb2-103">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="51cb2-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51cb2-104">ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม </span><span class="sxs-lookup"><span data-stu-id="51cb2-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="51cb2-105">บริษัทข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือ USP2</span><span class="sxs-lookup"><span data-stu-id="51cb2-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="51cb2-106">สร้างความต้องการสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="51cb2-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="51cb2-107">ไปที่แดชบอร์ดเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="51cb2-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="51cb2-108">คลิกที่การประมวลผลและการสอบถามใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="51cb2-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="51cb2-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="51cb2-109">Click New.</span></span>
4. <span data-ttu-id="51cb2-110">คลิกที่ใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="51cb2-110">Click Sales order.</span></span>
5. <span data-ttu-id="51cb2-111">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="51cb2-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="51cb2-112">ตัวอย่าง: US-001</span><span class="sxs-lookup"><span data-stu-id="51cb2-112">Example: US-001</span></span>  
6. <span data-ttu-id="51cb2-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="51cb2-113">Click OK.</span></span>
7. <span data-ttu-id="51cb2-114">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="51cb2-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="51cb2-115">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="51cb2-115">Example: P6003</span></span>  
8. <span data-ttu-id="51cb2-116">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="51cb2-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="51cb2-117">ตัวอย่าง : 50000</span><span class="sxs-lookup"><span data-stu-id="51cb2-117">Example: 50000</span></span>  
9. <span data-ttu-id="51cb2-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="51cb2-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="51cb2-119">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="51cb2-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="51cb2-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51cb2-120">Close the page.</span></span>
2. <span data-ttu-id="51cb2-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51cb2-121">Close the page.</span></span>
3. <span data-ttu-id="51cb2-122">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="51cb2-122">Click Master planning.</span></span>
4. <span data-ttu-id="51cb2-123">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="51cb2-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="51cb2-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="51cb2-125">ตัวอย่าง: แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="51cb2-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="51cb2-126">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="51cb2-126">Click Run.</span></span>
7. <span data-ttu-id="51cb2-127">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="51cb2-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="51cb2-128">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="51cb2-128">Click Filter.</span></span>
9. <span data-ttu-id="51cb2-129">ในรายการ ให้เลือกแถวสำหรับฟิลด์ = หมายเลขสินค้า </span><span class="sxs-lookup"><span data-stu-id="51cb2-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="51cb2-130">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="51cb2-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="51cb2-131">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="51cb2-131">Example: P6003</span></span>  
11. <span data-ttu-id="51cb2-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="51cb2-132">Click OK.</span></span>
12. <span data-ttu-id="51cb2-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="51cb2-133">Click OK.</span></span>
13. <span data-ttu-id="51cb2-134">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="51cb2-134">Click Planned orders.</span></span>
14. <span data-ttu-id="51cb2-135">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="51cb2-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="51cb2-136">ตัวอย่างเช่น กรองฟิลด์หมายเลขสินค้าด้วยค่า 'P6000'</span><span class="sxs-lookup"><span data-stu-id="51cb2-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="51cb2-137">กรองด้วยสูตรสินค้าที่เป็นผลิตภัณฑ์ร่วมของสินค้าที่คุณได้สร้างใบสั่งขายให้ </span><span class="sxs-lookup"><span data-stu-id="51cb2-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="51cb2-138">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="51cb2-139">เลือกแถวใดๆที่ถูกตีกลับโดยตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="51cb2-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="51cb2-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="51cb2-141">ขยายหรือยุบส่วนความเชื่อมโยงความต้องการกับการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="51cb2-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="51cb2-142">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="51cb2-143">คำสั่งซื้อที่วางแผนไว้จะเชื่อมโยงกับใบสั่งขายสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="51cb2-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="51cb2-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51cb2-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="51cb2-145">สร้างความต้องการสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="51cb2-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="51cb2-146">ไปที่แดชบอร์ดเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="51cb2-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="51cb2-147">คลิกที่การประมวลผลและการสอบถามใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="51cb2-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="51cb2-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="51cb2-148">Click New.</span></span>
4. <span data-ttu-id="51cb2-149">คลิกที่ใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="51cb2-149">Click Sales order.</span></span>
5. <span data-ttu-id="51cb2-150">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="51cb2-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="51cb2-151">ตัวอย่าง: US-001</span><span class="sxs-lookup"><span data-stu-id="51cb2-151">Example: US-001</span></span>  
6. <span data-ttu-id="51cb2-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="51cb2-152">Click OK.</span></span>
7. <span data-ttu-id="51cb2-153">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="51cb2-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="51cb2-154">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="51cb2-154">Example: P6003</span></span>  
8. <span data-ttu-id="51cb2-155">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="51cb2-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="51cb2-156">ตัวอย่าง : 50000</span><span class="sxs-lookup"><span data-stu-id="51cb2-156">Example: 50000</span></span>  
9. <span data-ttu-id="51cb2-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="51cb2-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="51cb2-158">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="51cb2-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="51cb2-159">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="51cb2-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="51cb2-160">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="51cb2-161">ตัวอย่าง: แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="51cb2-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="51cb2-162">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="51cb2-162">Click Run.</span></span>
4. <span data-ttu-id="51cb2-163">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="51cb2-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="51cb2-164">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="51cb2-164">Click Filter.</span></span>
6. <span data-ttu-id="51cb2-165">ในรายการ ให้เลือกแถวสำหรับฟิลด์ = หมายเลขสินค้า </span><span class="sxs-lookup"><span data-stu-id="51cb2-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="51cb2-166">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="51cb2-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="51cb2-167">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="51cb2-167">Example: P6003</span></span>  
8. <span data-ttu-id="51cb2-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="51cb2-168">Click OK.</span></span>
9. <span data-ttu-id="51cb2-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="51cb2-169">Click OK.</span></span>
10. <span data-ttu-id="51cb2-170">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="51cb2-170">Click Planned orders.</span></span>
11. <span data-ttu-id="51cb2-171">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="51cb2-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="51cb2-172">ตัวอย่างเช่น กรองฟิลด์หมายเลขสินค้าด้วยค่า 'P6000'</span><span class="sxs-lookup"><span data-stu-id="51cb2-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="51cb2-173">กรองด้วยสูตรสินค้าที่เป็นผลิตภัณฑ์ร่วมของสินค้าที่คุณได้สร้างใบสั่งขายให้ </span><span class="sxs-lookup"><span data-stu-id="51cb2-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="51cb2-174">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="51cb2-175">เลือกแถวใดๆที่ถูกตีกลับโดยตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="51cb2-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="51cb2-176">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="51cb2-177">ขยายหรือยุบส่วนความเชื่อมโยงความต้องการกับการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="51cb2-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="51cb2-178">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51cb2-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="51cb2-179">คำสั่งซื้อที่วางแผนไว้จะเชื่อมโยงกับใบสั่งขายสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="51cb2-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="51cb2-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51cb2-180">Close the page.</span></span>
17. <span data-ttu-id="51cb2-181">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="51cb2-181">Click Master planning.</span></span>
18. <span data-ttu-id="51cb2-182">ไปที่การวางแผนหลัก > การตั้งค่า > การวางแผนหลัก > พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="51cb2-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="51cb2-183">เลือก ไม่ ในฟิลด์การปิดใช้งานกระบวนการวางแผนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="51cb2-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="51cb2-184">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51cb2-184">Close the page.</span></span>

