--- 
title: "สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม"
description: "ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม "
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="56b36-103">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="56b36-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56b36-104">ผู้วางแผนการผลิตจะวางแผนความต้องการวัสดุสำหรับสินค้าที่เป็นสูตรผลิตภัณฑ์ร่วม </span><span class="sxs-lookup"><span data-stu-id="56b36-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="56b36-105">บริษัทข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือ USP2</span><span class="sxs-lookup"><span data-stu-id="56b36-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="56b36-106">สร้างความต้องการสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="56b36-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="56b36-107">ไปที่แดชบอร์ดเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="56b36-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="56b36-108">คลิกที่การประมวลผลและการสอบถามใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="56b36-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="56b36-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="56b36-109">Click New.</span></span>
4. <span data-ttu-id="56b36-110">คลิกที่ใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="56b36-110">Click Sales order.</span></span>
5. <span data-ttu-id="56b36-111">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="56b36-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="56b36-112">ตัวอย่าง: US-001</span><span class="sxs-lookup"><span data-stu-id="56b36-112">Example: US-001</span></span>  
6. <span data-ttu-id="56b36-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="56b36-113">Click OK.</span></span>
7. <span data-ttu-id="56b36-114">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="56b36-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="56b36-115">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="56b36-115">Example: P6003</span></span>  
8. <span data-ttu-id="56b36-116">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="56b36-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="56b36-117">ตัวอย่าง : 50000</span><span class="sxs-lookup"><span data-stu-id="56b36-117">Example: 50000</span></span>  
9. <span data-ttu-id="56b36-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="56b36-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="56b36-119">สร้างแผนวัสดุสำหรับผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="56b36-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="56b36-120">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="56b36-120">Click Master planning.</span></span>
2. <span data-ttu-id="56b36-121">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="56b36-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="56b36-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="56b36-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="56b36-123">ตัวอย่าง: แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="56b36-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="56b36-124">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="56b36-124">Click Run.</span></span>
5. <span data-ttu-id="56b36-125">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="56b36-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="56b36-126">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="56b36-126">Click Filter.</span></span>
7. <span data-ttu-id="56b36-127">ในรายการ ให้เลือกแถวสำหรับฟิลด์ = หมายเลขสินค้า </span><span class="sxs-lookup"><span data-stu-id="56b36-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="56b36-128">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="56b36-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="56b36-129">ตัวอย่าง : P6003</span><span class="sxs-lookup"><span data-stu-id="56b36-129">Example: P6003</span></span>  
9. <span data-ttu-id="56b36-130">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="56b36-130">Click OK.</span></span>
10. <span data-ttu-id="56b36-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="56b36-131">Click OK.</span></span>
11. <span data-ttu-id="56b36-132">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="56b36-132">Click Planned orders.</span></span>
12. <span data-ttu-id="56b36-133">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="56b36-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="56b36-134">ตัวอย่างเช่น กรองฟิลด์หมายเลขสินค้าด้วยค่า 'P6000'</span><span class="sxs-lookup"><span data-stu-id="56b36-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="56b36-135">กรองด้วยสูตรสินค้าที่เป็นผลิตภัณฑ์ร่วมของสินค้าที่คุณได้สร้างใบสั่งขายให้ </span><span class="sxs-lookup"><span data-stu-id="56b36-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="56b36-136">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="56b36-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="56b36-137">เลือกแถวใดๆที่ถูกตีกลับโดยตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="56b36-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="56b36-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="56b36-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="56b36-139">ขยายหรือยุบส่วนความเชื่อมโยงความต้องการกับการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="56b36-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="56b36-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="56b36-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="56b36-141">คำสั่งซื้อที่วางแผนไว้จะเชื่อมโยงกับใบสั่งขายสำหรับสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="56b36-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="56b36-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="56b36-142">Close the page.</span></span>


