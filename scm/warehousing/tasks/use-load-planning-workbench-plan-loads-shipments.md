--- 
title: "วางแผนการบรรทุกโดยใช้เวิร์กเบนช์การวางแผนการบรรทุก"
description: "กระบวนงานนี้แสดงวิธีการใช้เวิร์กเบนช์การวางแผนการบรรทุกเพื่อสร้างจำนวนงานในศูนย์การผลิตสำหรับใบสั่งขาย "
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="680c5-103">วางแผนการบรรทุกโดยใช้เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="680c5-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="680c5-104">กระบวนงานนี้แสดงวิธีการใช้เวิร์กเบนช์การวางแผนการบรรทุกเพื่อสร้างจำนวนงานในศูนย์การผลิตสำหรับใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="680c5-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="680c5-105">เป็นข้อกำหนดเบื้องต้น เราจะสร้างใบสั่งขายเป็นอย่างแรก</span><span class="sxs-lookup"><span data-stu-id="680c5-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="680c5-106">กระบวนงานนี้เป็นส่วนหนึ่งของงานประจำวันสำหรับผู้ประสานงานด้านการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="680c5-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="680c5-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="680c5-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="680c5-108">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="680c5-108">Create a sales order</span></span>
1. <span data-ttu-id="680c5-109">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="680c5-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="680c5-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="680c5-110">Click New.</span></span>
3. <span data-ttu-id="680c5-111">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="680c5-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="680c5-112">เลือก บัญชี US-004</span><span class="sxs-lookup"><span data-stu-id="680c5-112">Select account US-004.</span></span>
5. <span data-ttu-id="680c5-113">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="680c5-113">Click OK.</span></span>
6. <span data-ttu-id="680c5-114">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="680c5-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="680c5-115">เลือก สินค้า A0001</span><span class="sxs-lookup"><span data-stu-id="680c5-115">Select item A0001.</span></span>
    * <span data-ttu-id="680c5-116">A0001 เปิดใช้งานสำหรับการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="680c5-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="680c5-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="680c5-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="680c5-118">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="680c5-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="680c5-119">ในฟิลด์คลังสินค้า พิมพ์ '24'</span><span class="sxs-lookup"><span data-stu-id="680c5-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="680c5-120">ในตัวอย่างนี้ เลือกคลังสินค้า 24</span><span class="sxs-lookup"><span data-stu-id="680c5-120">In this example select warehouse 24.</span></span> <span data-ttu-id="680c5-121">คลังสินค้านี้เปิดใช้งานสำหรับการจัดการการขนส่งและการจัดการคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="680c5-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="680c5-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="680c5-122">Click Save.</span></span>
12. <span data-ttu-id="680c5-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="680c5-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="680c5-124">สร้างจำนวนงานในศูนย์การผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="680c5-124">Create a new load</span></span>
1. <span data-ttu-id="680c5-125">ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="680c5-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="680c5-126">คลิก แท็บรายการขาย</span><span class="sxs-lookup"><span data-stu-id="680c5-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="680c5-127">ขณะนี้ คุณจะสร้างจำนวนงานในศูนย์การผลิตสำหรับใบสั่งขายที่คุณเพิ่งสร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="680c5-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="680c5-128">จำนวนงานในศูนย์การผลิตสามารถสร้างตามการจัดหาวัสดุและความต้องการจากใบสั่งซื้อ ใบสั่งโอนย้าย และใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="680c5-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="680c5-129">บนบานหน้าต่างการดำเนินการ คลิก การจัดหาและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="680c5-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="680c5-130">คลิก ไปยังจำนวนงานในศูนย์การผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="680c5-130">Click To new load.</span></span>
5. <span data-ttu-id="680c5-131">ในฟิลด์รหัสเท็มเพลตจำนวนงานในศูนย์การผลิต คลิก ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="680c5-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="680c5-132">เท็มเพลตจำนวนงานในศูนย์การผลิตกำหนดหน่วยวัดสูงสุดสำหรับน้ำหนักและปริมาตรของจำนวนงานในศูนย์การผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="680c5-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="680c5-133">ตัวอย่างเช่น เท็มเพลตจำนวนงานในศูนย์การผลิตอาจแสดงถึงขนาดของตู้บรรจุสินค้าหรือรถบรรทุก</span><span class="sxs-lookup"><span data-stu-id="680c5-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="680c5-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="680c5-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="680c5-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="680c5-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="680c5-136">อัตราและกระบวนการผลิตจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="680c5-136">Rate and route the load</span></span>
1. <span data-ttu-id="680c5-137">คลิก การจัดอันดับและการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="680c5-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="680c5-138">คลิก จัดอันดับเวิร์กเบนช์กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="680c5-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="680c5-139">คลิก จัดอันดับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="680c5-139">Click Rate shop.</span></span>
4. <span data-ttu-id="680c5-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="680c5-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="680c5-141">คลิก มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="680c5-141">Click Assign.</span></span>
6. <span data-ttu-id="680c5-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="680c5-142">Close the page.</span></span>
7. <span data-ttu-id="680c5-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="680c5-143">Close the page.</span></span>


