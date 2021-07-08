---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301316"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="f518e-103">คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก</span><span class="sxs-lookup"><span data-stu-id="f518e-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="f518e-104">รหัสข้อผิดพลาด: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="f518e-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="f518e-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="f518e-105">Symptoms</span></span>

<span data-ttu-id="f518e-106">เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f518e-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f518e-107">สินค้าบางอย่างที่จำเป็นสำหรับจำนวนงานในศูนย์การผลิต %1 ยังไม่ได้รับการเบิกและเคลื่อนย้ายไปยังสถานที่จัดส่งขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f518e-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="f518e-108">ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="f518e-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f518e-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="f518e-109">Cause</span></span>

<span data-ttu-id="f518e-110">ไม่สามารถยืนยันสินค้าหรือการจัดส่งในสถานะปัจจุบันได้เนื่องจากอาจมีเงื่อนไขอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f518e-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="f518e-111">ยังไม่ได้เบิกสินค้าและย้ายไปยังสถานที่จัดส่งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f518e-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="f518e-112">ปริมาณงานที่เบิกไม่ตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="f518e-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="f518e-113">คำสั่งสถานที่ได้รับการตั้งค่าคอนฟิกด้วยสถานที่การบรรจุเป็นสถานที่จัดส่งขั้นสุดท้ายในขณะที่ใช้การบรรจุลงตู้บรรจุสินค้าแม่แบบเวฟ</span><span class="sxs-lookup"><span data-stu-id="f518e-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="f518e-114">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="f518e-114">Resolution</span></span>

<span data-ttu-id="f518e-115">สินค้าหรือการจัดส่งอยู่ในสถานะที่การยืนยันการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="f518e-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="f518e-116">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำหนึ่งในงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f518e-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="f518e-117">ตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="f518e-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="f518e-118">ยกเลิกรหัสงานที่สร้างด้วยสถานที่จัดส่งซึ่งเป็นสถานที่จัดส่งสุดท้าย ตั้งค่าคอนฟิกข้อกําหนดสถานที่อีกครั้ง และยกเลิกปล่อยสินค้าลงในสายการผลิต</span><span class="sxs-lookup"><span data-stu-id="f518e-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="f518e-119">ตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="f518e-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="f518e-120">ใช้กระบวนงานต่อไปนี้เพื่อตรวจทานรายการสินค้าของคุณ และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="f518e-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="f518e-121">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f518e-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f518e-122">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="f518e-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f518e-123">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="f518e-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="f518e-124">บันทึกค่าของฟิลด์ **ปริมาณที่สร้างขึ้นของงาน**</span><span class="sxs-lookup"><span data-stu-id="f518e-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="f518e-125">บนบานหน้าต่างการดำเนินการ บนแท็บ **สินค้า** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="f518e-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="f518e-126">ตรวจสอบว่างานเสร็จสมบูรณ์แล้วที่สถานที่จัดส่งสุดท้าย และปริมาณงานที่เบิกตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="f518e-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="f518e-127">ทําขั้นตอนนี้ซ้ํากับรายการสินค้าทั้งหมดเพื่อให้แน่ใจว่าตรงตามเกณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f518e-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="f518e-128">ยกเลิกรหัสงานที่สร้างด้วยสถานที่จัดส่งซึ่งเป็นสถานที่จัดส่งสุดท้าย ตั้งค่าคอนฟิกข้อกําหนดสถานที่อีกครั้ง และยกเลิกปล่อยสินค้าลงในสายการผลิต</span><span class="sxs-lookup"><span data-stu-id="f518e-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="f518e-129">ใช้กระบวนงานต่อไปนี้เพื่อยกเลิกรหัสงานที่มีสถานที่บรรจุเป็นสถานที่ส่งสินค้าขั้นสุดท้ายที่มีการบรรจุลงตู้บรรจุสินค้าอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f518e-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="f518e-130">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="f518e-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="f518e-131">กล่องโต้ตอบ **ยกเลิกงาน** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="f518e-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="f518e-132">ในฟิลด์ **รหัสงาน** ให้ระบุรหัสงานที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="f518e-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="f518e-133">รหัสงานที่เลือกต้องมีค่า **สถานะของงาน** เป็น *เปิด* *อยู่ระหว่างดำเนินการ* *ยกเลิก* *รวม* หรือ *ปิด*</span><span class="sxs-lookup"><span data-stu-id="f518e-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="f518e-134">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f518e-134">Select **OK**.</span></span>
1. <span data-ttu-id="f518e-135">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="f518e-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="f518e-136">ทํากระบวนงานนี้ซ้ำสำหรับรหัสงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f518e-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="f518e-137">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกงานของคลังสินค้าสำหรับการจัดการข้อยกเว้น](../../warehousing/cancel-warehouse-work.md)</span><span class="sxs-lookup"><span data-stu-id="f518e-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="f518e-138">ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคำสั่งสถานที่ใหม่ ดังนั้นจะไม่ใช้สถานที่บรรจุสินค้าเป็นสถานที่จัดส่งขั้นสุดท้ายเมื่อตั้งค่าการบรรจุลงในตู้บรรจุสินค้าอัตโนมัติให้กับแม่แบบเวฟ</span><span class="sxs-lookup"><span data-stu-id="f518e-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="f518e-139">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="f518e-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f518e-140">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="f518e-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="f518e-141">เลือกคำสั่งสถานที่ที่คุณใช้อยู่เพื่อการบรรจุลงในตู้บรรจุสินค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f518e-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="f518e-142">บนแถบเครื่องมือแท็บด่วน **การดำเนินการของคำสั่งสถานที่** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="f518e-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="f518e-143">ในกล่องโต้ตอบโปรแกรมแก้ไขการสอบถาม บนแท็บ **ช่วง** ให้ค้นหาแถวที่ **ฟิลด์** ถูกกําหนดเป็น *โปรไฟล์สถานที่* และตรวจสอบว่าไม่ได้ตั้งค่าฟิลด์ **เงื่อนไข** ของแถวนั้นให้กับโปรไฟล์สถานที่ที่มี **ชนิดสถานที่** เป็น *การบรรจุ*</span><span class="sxs-lookup"><span data-stu-id="f518e-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="f518e-144">ปรับปรุงฟิลด์ **เงื่อนไข** เพื่อแก้ไขสถานที่เก็บสำรองขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f518e-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="f518e-145">ใช้กระบวนงานต่อไปนี้เพื่อปล่อยสินค้าลงในสายการผลิตและสร้างรหัสงานด้วยสถานที่จัดส่งสุดท้ายที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f518e-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="f518e-146">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> เวิร์กเบนช์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="f518e-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="f518e-147">ในส่วน **สินค้า** ให้ค้นหาสินค้าที่ต้องปล่อยลงในสายการผลิต</span><span class="sxs-lookup"><span data-stu-id="f518e-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="f518e-148">บนแถบเครื่องมือส่วน **สินค้า** เลือก **นำออกใช้ \> นำออกใช้ไปยังคลังสินค้า** เพื่อนำจำนวนงานในศูนย์การผลิตที่เลือกออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f518e-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="f518e-149">ทํากระบวนงานนี้ซ้ำสำหรับสินค้าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f518e-149">Repeat this procedure for the other loads as needed.</span></span>
