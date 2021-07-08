---
title: ปริมาณที่เบิกสินค้าไม่เพียงพอระหว่างการสร้างบันทึกการจัดส่ง
description: เมื่อคุณสร้างบันทึกการจัดส่ง โหลดขาออกมีปริมาณที่เบิกซึ่งไม่ตรงกับปริมาณงานที่สร้างบนรายการโหลด
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249180"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="cb418-103">ปริมาณที่เบิกสินค้าไม่เพียงพอระหว่างการสร้างบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="cb418-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="cb418-104">รหัสข้อผิดพลาด: SYS54073</span><span class="sxs-lookup"><span data-stu-id="cb418-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="cb418-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="cb418-105">Symptoms</span></span>

<span data-ttu-id="cb418-106">เมื่อคุณสร้างบันทึกการจัดส่ง โหลดขาออกมีปริมาณที่เบิกซึ่งไม่ตรงกับปริมาณงานที่สร้างบนรายการโหลด</span><span class="sxs-lookup"><span data-stu-id="cb418-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="cb418-107">เมื่อคุณพยายามสร้างบันทึกการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb418-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="cb418-108">เนื่องจากได้มีการเบิกสินค้า %1 แล้ว จึงมีไม่เพียงพอที่จะอัพเดต %2 เมื่อมีการกำหนดว่าส่วนที่เหลือต้องเป็น %3 ในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="cb418-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="cb418-109">ดังนั้นคุณจึงไม่สามารถสร้างบันทึกการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="cb418-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="cb418-110">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="cb418-110">Cause</span></span>

<span data-ttu-id="cb418-111">บันทึกการจัดส่งไม่สามารถสร้างในสถานะปัจจุบันได้เนื่องจากอาจมีเงื่อนไขอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb418-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="cb418-112">ยังไม่ได้เบิกสินค้าและย้ายไปยังสถานที่จัดส่งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="cb418-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="cb418-113">ปริมาณงานที่เบิกไม่ตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="cb418-114">ปริมาณรายการสินค้า ปริมาณงานที่สร้าง หรือปริมาณที่เบิกสินค้าไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cb418-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="cb418-115">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="cb418-115">Resolution</span></span>

<span data-ttu-id="cb418-116">สินค้าหรือการจัดส่งอยู่ในสถานะที่การสร้างบันทึกการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="cb418-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="cb418-117">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำหนึ่งในงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cb418-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="cb418-118">ตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cb418-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="cb418-119">ปรับปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="cb418-120">ย้อนกลับรายการการลงทะเบียนการเบิกสินค้าทั้งหมด และทําซ้ำการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="cb418-121">ตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cb418-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="cb418-122">ใช้กระบวนงานต่อไปนี้เพื่อตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cb418-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="cb418-123">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="cb418-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cb418-124">เลือกสินค้าที่บันทึกการจัดส่งไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="cb418-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cb418-125">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="cb418-126">บันทึกค่าของฟิลด์ **ปริมาณที่สร้างขึ้นของงาน**</span><span class="sxs-lookup"><span data-stu-id="cb418-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="cb418-127">บนบานหน้าต่างการดำเนินการ บนแท็บ **สินค้า** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="cb418-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="cb418-128">ตรวจสอบว่างานเสร็จสมบูรณ์แล้วที่สถานที่จัดส่งสุดท้าย และปริมาณงานที่เบิกตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="cb418-129">ทําขั้นตอนนี้ซ้ํากับรายการสินค้าทั้งหมดเพื่อให้แน่ใจว่าตรงตามเกณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cb418-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="cb418-130">ปรับปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-130">Adjust the load line quantity</span></span>

<span data-ttu-id="cb418-131">ใช้ขั้นตอนต่อไปนี้เพื่อปรับปรุงปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="cb418-132">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="cb418-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cb418-133">เลือกสินค้าที่บันทึกการจัดส่งไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="cb418-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cb418-134">ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **กลับรายการ** ให้เลือก **กลับรายการการยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="cb418-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="cb418-135">บนแท็บ  **รายการสินค้า** ให้เลือกรายการสินค้าของสินค้าที่ก่อให้เกิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="cb418-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="cb418-136">เลือก **ลดปริมาณที่เบิกสินค้า** เพื่อปรับปรุงปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="cb418-137">ตั้งค่าฟิลด์ **ลดรายการสินค้า** เพื่อสะท้อนการปรับปรุงบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="cb418-138">ย้อนกลับรายการการลงทะเบียนการเบิกสินค้าทั้งหมด และทําซ้ำการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="cb418-139">ปัญหาอาจเกิดขึ้นเนื่องจากมีบุคคลที่ใช้การลงทะเบียนการเบิกสินค้าเพื่อปิดรายการสินค้าโดยไม่มีงาน</span><span class="sxs-lookup"><span data-stu-id="cb418-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="cb418-140">ในกรณีนี้ ต้องกลับรายการการลงทะเบียนการเบิกสินค้าด้วยตนเอง และต้องเสร็จสิ้นการเบิกสินค้าโดยการใช้แอป Warehouse Management บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="cb418-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="cb418-141">ใช้กระบวนงานต่อไปนี้เพื่อกลับรายการการลงทะเบียนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="cb418-142">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="cb418-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="cb418-143">เลือกใบสั่งขายที่คุณไม่สามารถลงรายการบัญชีบันทึกการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="cb418-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="cb418-144">บนแท็บ  **รายการใบสั่งขาย** ให้เลือกรายการใบสั่งขายที่เสร็จสิ้นการลงทะเบียนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="cb418-145">เลือก **อัปเดตรายการ \> การเบิกสินค้า** เพื่อยกเลิกการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb418-145">Select **Update line \> Pick** to unpick the items.</span></span>
