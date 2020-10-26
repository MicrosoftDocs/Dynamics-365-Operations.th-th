---
title: วางแผนการบรรทุกและการจัดส่งโดยใช้เวิร์กเบนช์การวางแผนการบรรทุก
description: หัวข้อนี้แสดงวิธีการใช้เวิร์กเบนช์การวางแผนการบรรทุกเพื่อสร้างจำนวนงานในศูนย์การผลิตสำหรับใบสั่งขาย
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7966c6e445e0e44cd4ff8518926aa6b410502e13
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980446"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="a91ad-103">วางแผนการบรรทุกและการจัดส่งโดยใช้เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="a91ad-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a91ad-104">หัวข้อนี้แสดงวิธีการใช้เวิร์กเบนช์การวางแผนการบรรทุกเพื่อสร้างจำนวนงานในศูนย์การผลิตสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a91ad-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="a91ad-105">เป็นข้อกำหนดเบื้องต้น เราจะสร้างใบสั่งขายเป็นอย่างแรก</span><span class="sxs-lookup"><span data-stu-id="a91ad-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="a91ad-106">กระบวนงานนี้เป็นส่วนหนึ่งของงานประจำวันสำหรับผู้ประสานงานด้านการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a91ad-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="a91ad-107">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="a91ad-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="a91ad-108">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a91ad-108">Create a sales order</span></span>
1. <span data-ttu-id="a91ad-109">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ใบสั่ง > ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a91ad-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="a91ad-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a91ad-110">Select **New**.</span></span>
3. <span data-ttu-id="a91ad-111">ในฟิลด์ **บัญชีลูกค้า** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a91ad-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a91ad-112">เลือกบัญชี **US-004**</span><span class="sxs-lookup"><span data-stu-id="a91ad-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="a91ad-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a91ad-113">Select **OK**.</span></span>
6. <span data-ttu-id="a91ad-114">ในฟิลด์ **หมายเลขสินค้า** ให้เลือกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a91ad-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a91ad-115">เลือกสินค้า **A0001**</span><span class="sxs-lookup"><span data-stu-id="a91ad-115">Select item **A0001**.</span></span> <span data-ttu-id="a91ad-116">**A0001** ถูกเปิดใช้งานสำหรับการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a91ad-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="a91ad-117">ในฟิลด์ **ไซต์** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา และจากนั้น เลือกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a91ad-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="a91ad-118">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="a91ad-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="a91ad-119">ในฟิลด์ **คลังสินค้า** ให้พิมพ์ '24' สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="a91ad-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="a91ad-120">คลังสินค้านี้เปิดใช้งานสำหรับการจัดการการขนส่งและการจัดการคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="a91ad-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="a91ad-121">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a91ad-121">Select **Save**.</span></span>
12. <span data-ttu-id="a91ad-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a91ad-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="a91ad-123">สร้างจำนวนงานในศูนย์การผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="a91ad-123">Create a new load</span></span>
1. <span data-ttu-id="a91ad-124">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="a91ad-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="a91ad-125">เลือกแท็บ **รายการขาย** ขณะนี้คุณจะสร้างจำนวนงานในศูนย์การผลิตสำหรับใบสั่งขายที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a91ad-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="a91ad-126">จำนวนงานในศูนย์การผลิตสามารถสร้างตามการจัดหาวัสดุและความต้องการจากใบสั่งซื้อ ใบสั่งโอนย้าย และใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a91ad-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="a91ad-127">บนบานหน้าต่างการดำเนินการ เลือก **การจัดหาวัสดุและความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="a91ad-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="a91ad-128">เลือก **ไปยังจำนวนงานในศูนย์การผลิตใหม่**</span><span class="sxs-lookup"><span data-stu-id="a91ad-128">Select **To new load**.</span></span>
5. <span data-ttu-id="a91ad-129">ในฟิลด์ **รหัสเท็มเพลตจำนวนงานในศูนย์การผลิต** เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a91ad-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="a91ad-130">เท็มเพลตจำนวนงานในศูนย์การผลิตกำหนดหน่วยวัดสูงสุดสำหรับน้ำหนักและปริมาตรของจำนวนงานในศูนย์การผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a91ad-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="a91ad-131">ตัวอย่างเช่น เท็มเพลตจำนวนงานในศูนย์การผลิตอาจแสดงถึงขนาดของตู้บรรจุสินค้าหรือรถบรรทุก</span><span class="sxs-lookup"><span data-stu-id="a91ad-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="a91ad-132">เลือกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a91ad-132">Select an item.</span></span>
6. <span data-ttu-id="a91ad-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a91ad-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="a91ad-134">อัตราและกระบวนการผลิตจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="a91ad-134">Rate and route the load</span></span>
1. <span data-ttu-id="a91ad-135">เลือก **การจัดอันดับและการกำหนดเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="a91ad-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="a91ad-136">เลือก **จัดอันดับเวิร์กเบนช์กระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="a91ad-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="a91ad-137">เลือก **จัดอันดับร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="a91ad-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="a91ad-138">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a91ad-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a91ad-139">เลือก **กำหนด**</span><span class="sxs-lookup"><span data-stu-id="a91ad-139">Select **Assign**.</span></span>
6. <span data-ttu-id="a91ad-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a91ad-140">Close the page.</span></span>

