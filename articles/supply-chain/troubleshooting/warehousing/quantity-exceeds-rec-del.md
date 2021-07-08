---
title: ปริมาณที่คุณพยายามอัปเดตเกินปริมาณที่ได้รับ/ที่จัดส่ง
description: เมื่อคุณสร้างบันทึกการจัดส่ง โหลดขาออกมีปริมาณที่เกินปริมาณงานที่เบิกและจองสำหรับใบสั่งขาย
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249181"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="2034d-103">ปริมาณที่คุณพยายามอัปเดตเกินปริมาณที่ได้รับ/ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="2034d-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="2034d-104">รหัสข้อผิดพลาด: SYS7676</span><span class="sxs-lookup"><span data-stu-id="2034d-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="2034d-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="2034d-105">Symptoms</span></span>

<span data-ttu-id="2034d-106">เมื่อคุณสร้างบันทึกการจัดส่ง โหลดขาออกมีปริมาณที่เกินปริมาณงานที่เบิกและจองสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="2034d-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="2034d-107">เมื่อคุณพยายามสร้างบันทึกการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2034d-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="2034d-108">ปริมาณที่คุณพยายามอัพเดตเกินปริมาณที่ได้รับ/ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="2034d-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="2034d-109">ดังนั้นคุณจึงไม่สามารถสร้างบันทึกการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="2034d-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="2034d-110">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="2034d-110">Cause</span></span>

<span data-ttu-id="2034d-111">ปริมาณงานที่เบิกไม่ตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="2034d-112">ตัวอย่างเช่น ปัญหานี้อาจเกิดขึ้นถ้าปริมาณรายการสินค้า ปริมาณงานที่สร้าง หรือปริมาณที่เบิกสินค้าไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2034d-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="2034d-113">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="2034d-113">Resolution</span></span>

<span data-ttu-id="2034d-114">สินค้าหรือการจัดส่งอยู่ในสถานะที่การสร้างบันทึกการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="2034d-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="2034d-115">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำหนึ่งในงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2034d-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="2034d-116">ตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="2034d-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="2034d-117">ปรับปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="2034d-118">ย้อนกลับรายการการลงทะเบียนการเบิกสินค้าทั้งหมด และทําซ้ำการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="2034d-119">ตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="2034d-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="2034d-120">ใช้กระบวนงานต่อไปนี้เพื่อตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="2034d-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="2034d-121">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2034d-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2034d-122">เลือกสินค้าที่การจัดส่งไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="2034d-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="2034d-123">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="2034d-124">บันทึกค่าของฟิลด์ **ปริมาณที่สร้างขึ้นของงาน**</span><span class="sxs-lookup"><span data-stu-id="2034d-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="2034d-125">บนบานหน้าต่างการดำเนินการ บนแท็บ **สินค้า** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="2034d-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="2034d-126">ตรวจสอบว่างานเสร็จสมบูรณ์แล้วที่สถานที่จัดส่งสุดท้าย และปริมาณงานที่เบิกตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="2034d-127">ทําขั้นตอนนี้ซ้ํากับรายการสินค้าทั้งหมดเพื่อให้แน่ใจว่าตรงตามเกณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2034d-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="2034d-128">ปรับปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-128">Adjust the load line quantity</span></span>

<span data-ttu-id="2034d-129">ใช้ขั้นตอนต่อไปนี้เพื่อปรับปรุงปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="2034d-130">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2034d-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2034d-131">เลือกสินค้าที่บันทึกการจัดส่งไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="2034d-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="2034d-132">ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **กลับรายการ** ให้เลือก **กลับรายการการยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="2034d-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="2034d-133">บนแท็บ  **รายการสินค้า** ให้เลือกรายการสินค้าของสินค้าที่ก่อให้เกิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="2034d-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="2034d-134">เลือก **ลดปริมาณที่เบิกสินค้า** เพื่อปรับปรุงปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="2034d-135">ตั้งค่าฟิลด์ **ลดรายการสินค้า** เพื่อสะท้อนการปรับปรุงบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="2034d-136">ย้อนกลับรายการการลงทะเบียนการเบิกสินค้าทั้งหมด และทําซ้ำการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="2034d-137">ถ้ามีบุคคลที่ใช้การลงทะเบียนการเบิกสินค้าเพื่อปิดรายการสินค้าโดยไม่มีงาน ความขัดแย้งอาจเกิดขึ้นระหว่างปริมาณรายการสินค้าและปริมาณที่เบิก</span><span class="sxs-lookup"><span data-stu-id="2034d-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="2034d-138">ในกรณีนี้ ต้องกลับรายการการลงทะเบียนการเบิกสินค้าด้วยตนเอง และต้องเสร็จสิ้นการเบิกสินค้าโดยการใช้แอป Warehouse Management บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="2034d-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="2034d-139">ใช้กระบวนงานต่อไปนี้เพื่อกลับรายการการลงทะเบียนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="2034d-140">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2034d-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="2034d-141">เลือกใบสั่งขายที่คุณไม่สามารถลงรายการบัญชีบันทึกการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="2034d-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="2034d-142">บนแท็บ  **รายการใบสั่งขาย** ให้เลือกรายการใบสั่งขายที่เสร็จสิ้นการลงทะเบียนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="2034d-143">เลือก **อัปเดตรายการ \> การเบิกสินค้า** เพื่อยกเลิกการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="2034d-143">Select **Update line \> Pick** to unpick the items.</span></span>
