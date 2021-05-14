---
title: สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม
description: 'ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920740"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="5f00e-103">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="5f00e-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f00e-104">ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม </span><span class="sxs-lookup"><span data-stu-id="5f00e-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="5f00e-105">บริษัทข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือ USP2</span><span class="sxs-lookup"><span data-stu-id="5f00e-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="5f00e-106">สร้างความต้องการสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="5f00e-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="5f00e-107">ไปที่ **การขายและการตลาด \> พื้นที่ทำงาน \> การประมวลผลและการสอบถามใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="5f00e-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="5f00e-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5f00e-108">Select **New**.</span></span>
1. <span data-ttu-id="5f00e-109">เลือก **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="5f00e-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="5f00e-110">ในฟิลด์ **บัญชีลูกค้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5f00e-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="5f00e-111">ตัวอย่าง: US-001</span><span class="sxs-lookup"><span data-stu-id="5f00e-111">Example: US-001</span></span>  
1. <span data-ttu-id="5f00e-112">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-112">Select **OK**.</span></span>
1. <span data-ttu-id="5f00e-113">ในฟิลด์ **หมายเลขสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5f00e-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="5f00e-114">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="5f00e-114">Example: P6003</span></span>  
1. <span data-ttu-id="5f00e-115">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="5f00e-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="5f00e-116">ตัวอย่าง : 50000</span><span class="sxs-lookup"><span data-stu-id="5f00e-116">Example: 50000</span></span>  
1. <span data-ttu-id="5f00e-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5f00e-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="5f00e-118">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="5f00e-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="5f00e-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5f00e-119">Close the page.</span></span>
1. <span data-ttu-id="5f00e-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5f00e-120">Close the page.</span></span>
1. <span data-ttu-id="5f00e-121">เลือก **การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="5f00e-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="5f00e-122">ในฟิลด์ **แผน** ให้เลือกปุ่มแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5f00e-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="5f00e-123">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="5f00e-124">ตัวอย่าง: แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="5f00e-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="5f00e-125">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="5f00e-125">Select **Run**.</span></span>
1. <span data-ttu-id="5f00e-126">ขยายหรือยุบส่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="5f00e-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="5f00e-127">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-127">Select **Filter**.</span></span>
1. <span data-ttu-id="5f00e-128">ในรายการ ให้เลือกแถวสำหรับ **ฟิลด์** = *หมายเลขสินค้า*</span><span class="sxs-lookup"><span data-stu-id="5f00e-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="5f00e-129">ในฟิลด์ **เงื่อนไข** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5f00e-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="5f00e-130">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="5f00e-130">Example: P6003</span></span>  
1. <span data-ttu-id="5f00e-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-131">Select **OK**.</span></span>
1. <span data-ttu-id="5f00e-132">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-132">Select **OK**.</span></span>
1. <span data-ttu-id="5f00e-133">เลือก **แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="5f00e-134">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="5f00e-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5f00e-135">ตัวอย่างเช่น กรองฟิลด์ **หมายเลขสินค้า** ด้วยค่า 'P6000'</span><span class="sxs-lookup"><span data-stu-id="5f00e-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="5f00e-136">กรองด้วยสูตรสินค้าที่เป็นผลิตภัณฑ์ร่วมของสินค้าที่คุณได้สร้างใบสั่งขายให้ </span><span class="sxs-lookup"><span data-stu-id="5f00e-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="5f00e-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5f00e-138">เลือกแถวใดๆที่ถูกตีกลับโดยตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="5f00e-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="5f00e-139">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5f00e-140">ขยายส่วน **การเชื่อมโยงความต้องการกับการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="5f00e-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="5f00e-141">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="5f00e-142">คำสั่งซื้อที่วางแผนไว้จะเชื่อมโยงกับใบสั่งขายสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="5f00e-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="5f00e-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5f00e-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="5f00e-144">สร้างข้อกำหนดที่สองสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="5f00e-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="5f00e-145">ไปที่ **การขายและการตลาด \> พื้นที่ทำงาน \> การประมวลผลและการสอบถามใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="5f00e-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="5f00e-146">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5f00e-146">Select **New**.</span></span>
1. <span data-ttu-id="5f00e-147">เลือก **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="5f00e-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="5f00e-148">ในฟิลด์ **บัญชีลูกค้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5f00e-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="5f00e-149">ตัวอย่าง: US-001</span><span class="sxs-lookup"><span data-stu-id="5f00e-149">Example: US-001</span></span>  
1. <span data-ttu-id="5f00e-150">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-150">Select **OK**.</span></span>
1. <span data-ttu-id="5f00e-151">ในฟิลด์ **หมายเลขสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5f00e-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="5f00e-152">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="5f00e-152">Example: P6003</span></span>  
1. <span data-ttu-id="5f00e-153">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="5f00e-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="5f00e-154">ตัวอย่าง : 50000</span><span class="sxs-lookup"><span data-stu-id="5f00e-154">Example: 50000</span></span>  
1. <span data-ttu-id="5f00e-155">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5f00e-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="5f00e-156">สร้างแผนวัสดุที่สองสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="5f00e-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="5f00e-157">ในฟิลด์ **แผน** ให้เลือกปุ่มแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5f00e-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="5f00e-158">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="5f00e-159">ตัวอย่าง: แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="5f00e-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="5f00e-160">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="5f00e-160">Select **Run**.</span></span>
4. <span data-ttu-id="5f00e-161">ขยายหรือยุบส่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="5f00e-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="5f00e-162">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-162">Select **Filter**.</span></span>
6. <span data-ttu-id="5f00e-163">ในรายการ ให้เลือกแถวสำหรับ **ฟิลด์** = *หมายเลขสินค้า*</span><span class="sxs-lookup"><span data-stu-id="5f00e-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="5f00e-164">ในฟิลด์ *เงื่อนไข* ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5f00e-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="5f00e-165">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="5f00e-165">Example: P6003</span></span>  
8. <span data-ttu-id="5f00e-166">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-166">Select **OK**.</span></span>
9. <span data-ttu-id="5f00e-167">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-167">Select **OK**.</span></span>
10. <span data-ttu-id="5f00e-168">เลือก **แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="5f00e-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="5f00e-169">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="5f00e-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5f00e-170">ตัวอย่างเช่น กรองฟิลด์ **หมายเลขสินค้า** ด้วยค่า 'P6000'</span><span class="sxs-lookup"><span data-stu-id="5f00e-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="5f00e-171">กรองด้วยสูตรสินค้าที่เป็นผลิตภัณฑ์ร่วมของสินค้าที่คุณได้สร้างใบสั่งขายให้ </span><span class="sxs-lookup"><span data-stu-id="5f00e-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="5f00e-172">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5f00e-173">เลือกแถวใดๆที่ถูกตีกลับโดยตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="5f00e-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="5f00e-174">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="5f00e-175">ขยายหรือยุบส่วน **ความเชื่อมโยงความต้องการกับการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="5f00e-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="5f00e-176">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5f00e-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="5f00e-177">คำสั่งซื้อที่วางแผนไว้จะเชื่อมโยงกับใบสั่งขายสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="5f00e-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="5f00e-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5f00e-178">Close the page.</span></span>
17. <span data-ttu-id="5f00e-179">เลือก **การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="5f00e-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="5f00e-180">ไปที่ **การวางแผนหลัก \> การตั้งค่า \> พารามิเตอร์การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="5f00e-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="5f00e-181">เลือก *ไม่* ในฟิลด์ **ปิดใช้งานกระบวนการวางแผนทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5f00e-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="5f00e-182">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5f00e-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]