---
title: การแบ่งช่วงเวลาของคลังสินค้า
description: หัวข้อนี้มีข้อมูลเกี่ยวกับการแบ่งช่วงเวลาของคลังสินค้า การแบ่งช่วงเวลาของคลังสินค้าช่วยให้คุณสามารถรวมความต้องการตามสินค้าและหน่วยวัดจากใบสั่งที่มีสถานะเป็นสั่งแล้ว จองแล้ว หรือนำออกใช้แล้ว ซึ่งช่วยผู้จัดการคลังสินค้าในการวางแผนสถานที่เบิกสินค้าอย่างชาญฉลาด ก่อนที่พวกเขาจะนำใบสั่งออกใช้ไปยังคลังสินค้าและสร้างงานการเบิกสินค้า
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 31b86837735ca16610a1d304eab611b12a6aceeb
ms.sourcegitcommit: be4b9d557511bbb43e71a93f2c3b23b5f1a4669d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/24/2020
ms.locfileid: "4627760"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="f78fc-105">การแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f78fc-106">หลายคุณลักษณะการแบ่งช่วงเวลาของคลังสินค้านี้ช่วยผู้จัดการคลังสินค้าในการวางแผนสถานที่เบิกสินค้าอย่างชาญฉลาด ก่อนที่พวกเขาจะนำใบสั่งออกใช้ไปยังคลังสินค้าและสร้างงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="f78fc-107">*คุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า* ช่วยให้คุณสามารถรวมความต้องการตามสินค้าและหน่วยวัดจากใบสั่งที่มีสถานะเป็น *สั่งแล้ว* *จองแล้ว* หรือ *นำออกใช้แล้ว*</span><span class="sxs-lookup"><span data-stu-id="f78fc-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="f78fc-108">จากนั้น ความต้องการที่สร้างขึ้นสามารถนำไปใช้กับสถานที่ที่จะใช้สำหรับการเบิกสินค้าตามปริมาณ หน่วย มิติทางกายภาพ สถานที่คงที่ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f78fc-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="f78fc-109">หลังจากที่มีการสร้างแผนการแบ่งช่วงเวลาแล้ว คุณสามารถสร้างงานการเติมสินค้าเพื่อนำจำนวนของสินค้าคงคลังที่เหมาะสมไปยังสถานที่แต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="f78fc-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="f78fc-110">ลักษณะการทำงาน *การแบ่งช่วงเวลาของคลังสินค้าของใบสั่งโอนย้าย* ให้ผู้จัดการคลังสินค้าเป็นผู้จัดการคลังสินค้าในสถานที่เบิกสินค้าตามความต้องการจากใบสั่งโอนย้ายที่ยังไม่ได้นำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="f78fc-111">ตรวจสอบให้แน่ใจว่าสถานที่เบิกสินค้าจะรวมสินค้าทั้งหมดที่จำเป็นสำหรับใบสั่งโอนย้ายหลังจากที่มีการนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="f78fc-112">ลักษณะการทำงานนี้จำเป็นต้องใช้ในการเปิดใช้งานลักษณะการทำงาน *คุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f78fc-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="f78fc-113">ลักษณะการทำงาน *การปรับปรุงการปันส่วนการแบ่งช่วงเวลาของคลังสินค้า* การปันส่วนเพิ่มตัวเลือกสำหรับบรรทัดแม่แบบที่ใช้โดยคุณลักษณะ *คุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f78fc-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="f78fc-114">ตัวเลือกนี้จะเปิดใช้งานระบบเพื่อพิจารณาปริมาณคงคลังคงเหลือที่มีอยู่ในที่ตั้งเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f78fc-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="f78fc-115">ดังนั้น จึงอาจมีการเติมสินค้าน้อยกว่าสำหรับการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="f78fc-116">ลักษณะการทำงาน *การปรับปรุงการปันส่วนการแบ่งช่วงเวลาของคลังสินค้า* จำเป็นต้องเปิดคุณลักษณะ *คุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f78fc-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="f78fc-117">คุณสามารถเลือกที่จะใช้ร่วมกับลักษณะการทำงาน *การแบ่งช่วงเวลาของคลังสินค้าสำหรับใบสั่งโอนย้าย* ได้</span><span class="sxs-lookup"><span data-stu-id="f78fc-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="f78fc-118">เปิดคุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="f78fc-119">ก่อนที่คุณจะสามารถใช้คุณลักษณะเหล่านี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="f78fc-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="f78fc-120">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะนี้ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="f78fc-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="f78fc-121">เปิดใช้งานลักษณะการทำงานต่อไปนี้ตามต้องการ:</span><span class="sxs-lookup"><span data-stu-id="f78fc-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="f78fc-122">คุณสมบัติการแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="f78fc-123">การจัดเรียงสินค้าในคลังสินค้าสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="f78fc-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f78fc-124">ลักษณะการทำงาน *คุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า* ต้องเปิดอยู่ก่อนหน้าลักษณะการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="f78fc-125">การปรับปรุงการจัดสรรการจัดเรียงสินค้าในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f78fc-126">ลักษณะการทำงาน *คุณลักษณะการแบ่งช่วงเวลาของคลังสินค้า* ต้องเปิดอยู่ก่อนหน้าลักษณะการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="f78fc-127">การตั้งค่าการแบ่งช่วงเวลาของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-127">Set up warehouse slotting</span></span>

<span data-ttu-id="f78fc-128">เมื่อต้องการใช้การแบ่งช่วงเวลาของคลังสินค้า คุณต้องตั้งค่าองค์ประกอบต่อไปนี้ในระบบของคุณ:</span><span class="sxs-lookup"><span data-stu-id="f78fc-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="f78fc-129">ชั้นหน่วยวัดที่มีการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="f78fc-130">รหัสคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="f78fc-130">Directive codes</span></span>
- <span data-ttu-id="f78fc-131">เท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-131">Slotting templates</span></span>
- <span data-ttu-id="f78fc-132">คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="f78fc-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="f78fc-133">สร้างระดับหน่วยวัดสำหรับการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="f78fc-134">ระดับหน่วยวัดทำให้สามารถมีการจัดกลุ่มหน่วยวัดต่างๆ เข้าด้วยกันสำหรับวัตถุประสงค์ของการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="f78fc-135">ตัวอย่างเช่น ถ้ามีการเบิกกล่องหลายขนาดทั้งหมดจากพื้นที่เบิกกล่องเดียวกัน คุณสามารถสร้างระดับเดียวสำหรับทุกขนาดได้</span><span class="sxs-lookup"><span data-stu-id="f78fc-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="f78fc-136">**ต้องสร้างบรรทัดสำหรับแต่ละหน่วยวัดที่ควรจะเป็นส่วนหนึ่งของระดับ**</span><span class="sxs-lookup"><span data-stu-id="f78fc-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="f78fc-137">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> ระดับหน่วยวัดสำหรับการแบ่งช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="f78fc-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="f78fc-138">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f78fc-138">Select **New**.</span></span>
1. <span data-ttu-id="f78fc-139">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="f78fc-140">**ระดับหน่วยวัด:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="f78fc-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="f78fc-141">**คำอธิบาย:** *แท่นวางสินค้าแต่ละกล่อง*</span><span class="sxs-lookup"><span data-stu-id="f78fc-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="f78fc-142">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f78fc-142">Select **Save**.</span></span>
1. <span data-ttu-id="f78fc-143">บน FastTab **หน่วยวัด:** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f78fc-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f78fc-144">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-145">**หน่วย:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="f78fc-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="f78fc-146">**คำอธิบาย:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f78fc-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f78fc-147">จะมีการเติมข้อมูลนี้โดยอัตโนมัติ เมื่อคุณบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="f78fc-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f78fc-148">**คลาสหน่วย:** *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="f78fc-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f78fc-149">เลือก **สร้าง** เพื่อเพิ่มบรรทัดที่สองลงในกริด</span><span class="sxs-lookup"><span data-stu-id="f78fc-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="f78fc-150">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-151">**หน่วย:** *ea*</span><span class="sxs-lookup"><span data-stu-id="f78fc-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="f78fc-152">**คำอธิบาย:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f78fc-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f78fc-153">จะมีการเติมข้อมูลนี้โดยอัตโนมัติ เมื่อคุณบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="f78fc-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f78fc-154">**คลาสหน่วย:** *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="f78fc-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f78fc-155">เลือก **สร้าง** เพื่อเพิ่มบรรทัดที่สามลงในกริด</span><span class="sxs-lookup"><span data-stu-id="f78fc-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="f78fc-156">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-157">**หน่วย:** *PL*</span><span class="sxs-lookup"><span data-stu-id="f78fc-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="f78fc-158">**คำอธิบาย:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f78fc-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f78fc-159">จะมีการเติมข้อมูลนี้โดยอัตโนมัติ เมื่อคุณบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="f78fc-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f78fc-160">**คลาสหน่วย:** *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="f78fc-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f78fc-161">เลือก **บันทึก** เพื่อบันทึกระดับ</span><span class="sxs-lookup"><span data-stu-id="f78fc-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="f78fc-162">สร้างรหัสคำสั่งสำหรับการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-162">Create a directive code for slotting</span></span>

<span data-ttu-id="f78fc-163">คุณต้องเลือกรหัสคำสั่งที่ควรเชื่อมโยงกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f78fc-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="f78fc-164">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> รหัสคำสั่ง**</span><span class="sxs-lookup"><span data-stu-id="f78fc-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="f78fc-165">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f78fc-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f78fc-166">ในฟิลด์ **รหัสคำสั่ง** ให้ป้อน *การแบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="f78fc-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="f78fc-167">ในฟิลด์ **คำอธิบายคำสั่ง** ให้ป้อน *การแบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="f78fc-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="f78fc-168">การตั้งค่าเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-168">Set up slotting templates</span></span>

<span data-ttu-id="f78fc-169">เท็มเพลตการแบ่งช่วงเวลาแต่ละรายการจะควบคุมวิธีการกำหนดสินค้าคงคลังให้กับสถานที่สำหรับคลังสินค้าหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="f78fc-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="f78fc-170">เท็มเพลตแต่ละรายการจะต้องรวมบรรทัดสำหรับข้อมูลจำเพาะของการแบ่งช่วงเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="f78fc-171">ใช้กระบวนงานในส่วนนี้เพื่อตั้งค่าเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="f78fc-172">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f78fc-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="f78fc-173">เลือก **สร้าง** เพื่อสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f78fc-173">Select **New** to create a template.</span></span>

<span data-ttu-id="f78fc-174">ถัดไป คุณต้องตั้งค่าส่วนหัวของเท็มเพลต ข้อมูลจำเพาะของการแบ่งช่วงเวลา และคำสั่งสถานที่ ดังที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="f78fc-175">การตั้งค่าสำหรับการแบ่งช่วงเวลาสำหรับใบสั่งโอนย้ายคล้ายกับการตั้งค่าสำหรับการแบ่งช่วงเวลาสำหรับใบสั่งขาย แต่ฟิลด์ **ชนิดความต้องการ** มีการตั้งค่า *ใบสั่งโอนย้าย* แทน *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="f78fc-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="f78fc-176">ตั้งค่าหัวข้อสำหรับแม่แบบการแบ่งช่วงเวลาใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f78fc-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="f78fc-177">ในส่วนหัวสำหรับเท็มเพลต ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="f78fc-178">**เท็มเพลตการแบ่งช่วงเวลา:** _61_</span><span class="sxs-lookup"><span data-stu-id="f78fc-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="f78fc-179">**คำอธิบาย:** _61_</span><span class="sxs-lookup"><span data-stu-id="f78fc-179">**Description:** _61_</span></span>
    - <span data-ttu-id="f78fc-180">**ชนิดความต้องการ:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="f78fc-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="f78fc-181">ปัจจุบัน *ใบสั่งขาย* และ *ใบสั่งโอนย้าย* เป็นชนิดความต้องการที่ได้รับการสนับสนุนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f78fc-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="f78fc-182">คุณสามารถเลือก *ใบสั่งโอนย้าย* เฉพาะเมื่อ *เปิดใช้งานลักษณะการทำงานการแบ่งช่วงเวลาของคลังสินค้าสำหรับใบสั่งโอนย้าย*</span><span class="sxs-lookup"><span data-stu-id="f78fc-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="f78fc-183">**กลยุทธ์ความต้องการ:** _สั่งแล้ว_</span><span class="sxs-lookup"><span data-stu-id="f78fc-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="f78fc-184">ค่าต่อไปนี้จะพร้อมใช้งานในฟิลด์นี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="f78fc-185">**สั่งแล้ว** – ปริมาณที่สั่งทั้งหมดในใบสั่งขายควรมีการพิจารณาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="f78fc-186">**จองแล้ว** – เฉพาะปริมาณของบรรทัดใบสั่งขายที่จองไว้เท่านั้น (มีจริง และสั่งแล้ว) ที่ควรมีการพิจารณาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="f78fc-187">**นำออกใช้** – ปริมาณที่นำออกใช้ควรมีการพิจารณาตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="f78fc-188">**คลังสินค้า:** _61_</span><span class="sxs-lookup"><span data-stu-id="f78fc-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="f78fc-189">**อนุญาตให้ความต้องการเวฟใช้ปริมาณที่ไม่ได้จอง:** _ใช่_</span><span class="sxs-lookup"><span data-stu-id="f78fc-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="f78fc-190">นอกจากนี้ คุณยังสามารถระบุการสอบถามเพื่อจำกัดขอบเขตของความต้องการที่จะประเมิน</span><span class="sxs-lookup"><span data-stu-id="f78fc-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="f78fc-191">ตั้งค่าข้อมูลจำเพาะของการแบ่งช่วงเวลาสำหรับเท็มเพลตแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="f78fc-192">สำหรับม่แบบใบสั่งขายแต่ละรายการที่คุณสร้าง ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มบรรทัดสำหรับข้อมูลจำเพาะของการแบ่งช่วงเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="f78fc-193">บน FastTab **รายละเอียดเท็มเพลตการแบ่งช่วงเวลา** ให้เลือก **สร้าง** เพื่อสร้างบรรทัดเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f78fc-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="f78fc-194">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-195">**ลำดับ:** _1_</span><span class="sxs-lookup"><span data-stu-id="f78fc-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="f78fc-196">**คำอธิบาย:** _สถานที่คงที่_</span><span class="sxs-lookup"><span data-stu-id="f78fc-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="f78fc-197">**ปริมาณต่ำสุด:** _1_</span><span class="sxs-lookup"><span data-stu-id="f78fc-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="f78fc-198">ฟิลด์นี้จะกำหนดปริมาณต่ำสุดของความต้องการที่จำเป็นสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="f78fc-199">**ปริมาณสูงสุด:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="f78fc-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="f78fc-200">ฟิลด์นี้จะกำหนดปริมาณสูงสุดของความต้องการที่มีผลบังคับใช้สำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="f78fc-201">**หน่วย:** ให้ปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f78fc-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="f78fc-202">ฟิลด์นี้จะกำหนดหน่วยวัดที่ปริมาณต่ำสุดและสูงสุดอ้างอิงถึง</span><span class="sxs-lookup"><span data-stu-id="f78fc-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="f78fc-203">**ระดับหน่วยวัด:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="f78fc-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="f78fc-204">ฟิลด์นี้จะกำหนดหน่วยวัดของความต้องการที่มีผลบังคับใช้สำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="f78fc-205">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ตั้งค่าระดับหน่วยวัดสำหรับการแบ่งช่วงเวลา](#unit-tiers) ก่อนหน้าในหัวข้อนี้)</span><span class="sxs-lookup"><span data-stu-id="f78fc-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="f78fc-206">**กำหนดเกณฑ์ของช่วงเวลา:** _พิจารณาปริมาณ_</span><span class="sxs-lookup"><span data-stu-id="f78fc-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="f78fc-207">ค่าต่อไปนี้จะพร้อมใช้งานในฟิลด์นี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="f78fc-208">**สมมติว่าว่างเปล่า** – ระบบนี้ควรสันนิษฐานว่าสถานที่ทั้งหมดในพื้นที่เบิกสินค้าว่างเปล่า และไม่ควรตรวจสอบสถานที่เหล่านั้นสำหรับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f78fc-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="f78fc-209">**พิจารณาปริมาณ** – ระบบนี้ควรตรวจสอบสถานที่ทั้งหมดในพื้นที่เบิกสินค้าสำหรับสินค้าคงคลัง และควรข้ามสถานที่ใดๆ ที่ไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f78fc-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="f78fc-210">**พิจารณาปริมาณคงคลังคงเหลือ** – ระบบควรตรวจสอบว่าที่ตั้งเป้าหมายใด ๆ มีปริมาณที่ตั๋วสำหรับสินค้าในบรรทัดความต้องการหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f78fc-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="f78fc-211">ถ้าปริมาณมีขนาดใหญ่พอที่จะตอบสนองอย่างน้อยหนึ่งหน่วยของบรรทัดความต้องการเรกคอร์ดของแผนการแบ่งช่วงเวลาสร้างขึ้นจะลดลงตามยอดเงินที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f78fc-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="f78fc-212">ตัวอย่างเช่น หากความต้องการเป็น 10 กรณี และมีกรณีเดียวกันอยู่ ความต้องการที่มีอยู่จะมี 9 กรณี</span><span class="sxs-lookup"><span data-stu-id="f78fc-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="f78fc-213">หากความต้องการเป็น 10 กรณี และแต่ละกรณีมีกรณีเดียวกันอยู่ ความต้องการที่มีอยู่จะมี 10 กรณี</span><span class="sxs-lookup"><span data-stu-id="f78fc-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="f78fc-214">ค่านี้จะใช้ได้เฉพาะเมื่อมีการเปิดใช้งานคุณลักษณะ *การปรับปรุงการจัดสรรการจัดเรียงสินค้าในคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f78fc-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="f78fc-215">**รหัสคำสั่ง:** _การแบ่งช่วงเวลา_</span><span class="sxs-lookup"><span data-stu-id="f78fc-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="f78fc-216">ฟิลด์นี้จะกำหนดคำสั่งสถานที่ที่ใช้ในการค้นหาสถานที่เบิกสินค้าของงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="f78fc-217">**สถานที่ที่มีปริมาณมากเกินไป:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f78fc-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="f78fc-218">ฟิลด์นี้จะกำหนดสถานที่ที่มีการเก็บสินค้าคงคลัง ถ้าไม่พบสถานที่สำหรับปริมาณ เมื่อมีการประมวลผลรายการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="f78fc-219">**อนุญาตให้หยุด:** _ใช่_</span><span class="sxs-lookup"><span data-stu-id="f78fc-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="f78fc-220">เมื่อมีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ถ้าความต้องการใดๆ ไม่สามารถถูกจัดช่วงเวลาได้ งานการเคลื่อนไหวงานจะถูกสร้างขึ้นเพื่อนำสินค้าคงคลังออกจากสถานที่ที่ซึ่งมีสินค้าคงคลัง แต่ที่ซึ่งไม่มีการจัดช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="f78fc-221">แล้วรันเท็มเพลตอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="f78fc-221">The template is then run again.</span></span> <span data-ttu-id="f78fc-222">ในเวลานี้ จะละเว้นสินค้าคงคลังในสถานที่</span><span class="sxs-lookup"><span data-stu-id="f78fc-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="f78fc-223">ฟังก์ชันนี้จะทำงานได้ดีที่สุด เมื่อฟิลด์ **กำหนดเกณฑ์ของช่วงเวลา** ถูกตั้งค่าเป็น _พิจารณาปริมาณ_</span><span class="sxs-lookup"><span data-stu-id="f78fc-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="f78fc-224">**การใช้สถานที่คงที่:** _เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์_</span><span class="sxs-lookup"><span data-stu-id="f78fc-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="f78fc-225">ค่าต่อไปนี้จะพร้อมใช้งานในฟิลด์นี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="f78fc-226">**สถานที่คงที่และไม่คงที่** – ระบบไม่ควรถูกจำกัดให้ใช้เฉพาะสถานที่คงที่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f78fc-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="f78fc-227">**เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์** – ระบบควรจะใช้เฉพาะกับสถานที่ที่เป็นสถานที่คงที่สำหรับผลิตภัณฑ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f78fc-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="f78fc-228">**เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์ย่อย** – ระบบควรจะใช้เฉพาะกับสถานที่ที่เป็นสถานที่คงที่สำหรับผลิตภัณฑ์ย่อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f78fc-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="f78fc-229">ถ้าแม่แบบการแบ่งช่วงเวลามีบรรทัดอย่างน้อยหนึ่งรายการที่มีการตั้งค่าฟิลด์ **กำหนดเงื่อนไขช่อง** เป็น *พิจารณาปริมาณคงคลังคงเหลือ* จะไม่อนุญาตให้ใช้สำหรับบรรทัดใด ๆ ในแม่แบบได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="f78fc-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="f78fc-230">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f78fc-230">Select **Save**.</span></span>
1. <span data-ttu-id="f78fc-231">เลือก **สร้าง** เพื่อเพิ่มบรรทัดเท็มเพลตที่สอง</span><span class="sxs-lookup"><span data-stu-id="f78fc-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="f78fc-232">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-233">**ลำดับ:** _2_</span><span class="sxs-lookup"><span data-stu-id="f78fc-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="f78fc-234">**คำอธิบาย:** _อื่นๆ_</span><span class="sxs-lookup"><span data-stu-id="f78fc-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="f78fc-235">**ปริมาณต่ำสุด:** _1_</span><span class="sxs-lookup"><span data-stu-id="f78fc-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="f78fc-236">**ปริมาณสูงสุด:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="f78fc-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="f78fc-237">**หน่วย:** ให้ปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f78fc-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="f78fc-238">**ระดับหน่วยวัด:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="f78fc-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="f78fc-239">**กำหนดเกณฑ์ของช่วงเวลา:** _พิจารณาปริมาณ_</span><span class="sxs-lookup"><span data-stu-id="f78fc-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="f78fc-240">**รหัสคำสั่ง:** _การแบ่งช่วงเวลา_</span><span class="sxs-lookup"><span data-stu-id="f78fc-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="f78fc-241">**สถานที่ที่มีปริมาณมากเกินไป:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f78fc-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="f78fc-242">**อนุญาตให้หยุด:** _ใช่_</span><span class="sxs-lookup"><span data-stu-id="f78fc-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="f78fc-243">**ใช้สถานที่คงที่:** _สถานที่คงที่และไม่คงที่_</span><span class="sxs-lookup"><span data-stu-id="f78fc-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="f78fc-244">ในการสอบถามสำหรับบรรทัดที่สอง คุณจะระบุเกณฑ์ที่จะใช้ในการกำหนดสถานที่ที่ความต้องการสำหรับบรรทัดดังกล่าวถูกจัดช่วงเวลาให้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="f78fc-245">เลือกบรรทัดที่ฟิลด์ **ลำดับ** ถูกตั้งค่าเป็น *2*</span><span class="sxs-lookup"><span data-stu-id="f78fc-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="f78fc-246">เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="f78fc-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="f78fc-247">บนแท็บ **ช่วงระยะ** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f78fc-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f78fc-248">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-249">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="f78fc-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="f78fc-250">**ตารางสืบทอด:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="f78fc-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="f78fc-251">**ฟิลด์:** *รหัสโพรไฟล์สถานที่*</span><span class="sxs-lookup"><span data-stu-id="f78fc-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="f78fc-252">**เงื่อนไข:** *เบิกสินค้า-06* (เลือกเครื่องหมายบวกคู่ \[**++**\] ในฟิลด์เพื่อขยายรายการ แล้วจากนั้น เลือก *เบิกสินค้า-06* - *ไซต์เบิกสินค้า 6*)</span><span class="sxs-lookup"><span data-stu-id="f78fc-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="f78fc-253">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f78fc-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="f78fc-254">ตั้งค่าคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="f78fc-254">Set up location directives</span></span>

<span data-ttu-id="f78fc-255">ต้องมีการตั้งค่าคำสั่งสถานที่อย่างน้อยหนึ่งรายการเพื่อสนับสนุนการเบิกสินค้าที่แบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="f78fc-256">ใช้กระบวนงานในส่วนนี้เพื่อตั้งค่า *คำสั่งสถานที่การเติมสินค้า* สำหรับการเบิกสินค้าที่แบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="f78fc-257">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="f78fc-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f78fc-258">ในบานหน้าต่างด้านซ้าย ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *การเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f78fc-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="f78fc-259">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f78fc-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f78fc-260">ในส่วนหัวของคำสั่งสถานที่ใหม่ ในฟิลด์ **ชื่อ** ให้ป้อน *61 การเบิกสินค้าที่แบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="f78fc-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="f78fc-261">ในฟิลด์ **ลำดับหมายเลข** ยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f78fc-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="f78fc-262">ตั้งค่าคอนฟิก FastTab ของคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="f78fc-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="f78fc-263">บน FastTab **คำสั่งสถานที่** ให้กำหนดค่าดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="f78fc-264">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f78fc-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f78fc-265">**ชนิดงาน:** _เบิกสินค้า_</span><span class="sxs-lookup"><span data-stu-id="f78fc-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="f78fc-266">**ไซต์:** _6_</span><span class="sxs-lookup"><span data-stu-id="f78fc-266">**Site:** _6_</span></span>
    - <span data-ttu-id="f78fc-267">**คลังสินค้า:** _61_</span><span class="sxs-lookup"><span data-stu-id="f78fc-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="f78fc-268">**รหัสคำสั่ง:** _การแบ่งช่วงเวลา_</span><span class="sxs-lookup"><span data-stu-id="f78fc-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="f78fc-269">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f78fc-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="f78fc-270">ตั้งค่าคอนฟิก FastTab บรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="f78fc-271">บน FastTab **รายการ** เลือก **สร้าง** เพื่อสร้างบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="f78fc-272">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="f78fc-273">**ปริมาณเริ่มต้น:** _0_</span><span class="sxs-lookup"><span data-stu-id="f78fc-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="f78fc-274">**ปริมาณสิ้นสุด:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="f78fc-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="f78fc-275">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f78fc-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="f78fc-276">เลือก **บันทึก** เพื่อให้แท็บด่วน **การดำเนินคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f78fc-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="f78fc-277">ตั้งค่าคอนฟิก FastTab การดำเนินการของคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="f78fc-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="f78fc-278">บน FastTab **การดำเนินการของคำสั่งสถานที่** เลือก **สร้าง** เพื่อสร้างบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="f78fc-279">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-279">On the new line, set the following values.</span></span> <span data-ttu-id="f78fc-280">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f78fc-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f78fc-281">**หมายเลขลำดับ:** ยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f78fc-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="f78fc-282">**ชื่อ:** _จำนวนมาก_</span><span class="sxs-lookup"><span data-stu-id="f78fc-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="f78fc-283">**กลยุทธ์:** _ไม่มี_</span><span class="sxs-lookup"><span data-stu-id="f78fc-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="f78fc-284">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f78fc-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="f78fc-285">เลือก **บันทึก** เพื่อทำให้ปุ่ม **แก้ไขแบบสอบถาม** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f78fc-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="f78fc-286">แก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="f78fc-286">Edit the query</span></span>

1. <span data-ttu-id="f78fc-287">บน FastTab **การดำเนินการของคำสั่งสถานที่** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="f78fc-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="f78fc-288">บนแท็บ **ช่วงระยะ** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f78fc-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f78fc-289">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-290">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="f78fc-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="f78fc-291">**ตารางสืบทอด:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="f78fc-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="f78fc-292">**ฟิลด์:** *รหัสโซน*</span><span class="sxs-lookup"><span data-stu-id="f78fc-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="f78fc-293">**เงื่อนไข:** *จำนวนมาก* (เลือกเครื่องหมายบวกคู่ \[**++**\] ในฟิลด์เพื่อขยายรายการ แล้วจากนั้น เลือก *จำนวนมาก*)</span><span class="sxs-lookup"><span data-stu-id="f78fc-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="f78fc-294">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f78fc-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="f78fc-295">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="f78fc-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="f78fc-296">ตั้งค่าสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="f78fc-296">Set up the scenario</span></span>

<span data-ttu-id="f78fc-297">สำหรับสถานการณ์จำลองนี้ ให้ใช้ข้อมูลตัวอย่างที่มีอยู่แล้วภายใน และสร้างเรกคอร์ดที่อธิบายไว้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="f78fc-298">ใช้ข้อมูลตัวอย่าง USMF</span><span class="sxs-lookup"><span data-stu-id="f78fc-298">Use the USMF sample data</span></span>

<span data-ttu-id="f78fc-299">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="f78fc-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="f78fc-300">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f78fc-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="f78fc-301">สร้างความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-301">Create demand</span></span>

<span data-ttu-id="f78fc-302">ทำตามขั้นตอนเหล่านี้เพื่อสร้างความต้องการที่คุณจะนำการแบ่งช่วงเวลาไปใช้</span><span class="sxs-lookup"><span data-stu-id="f78fc-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="f78fc-303">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f78fc-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="f78fc-304">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f78fc-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f78fc-305">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ในฟิลด์ **บัญชีลูกค้า** ให้เลือก _US-007_</span><span class="sxs-lookup"><span data-stu-id="f78fc-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="f78fc-306">ในฟิลด์  **คลังสินค้า** เลือก _61_</span><span class="sxs-lookup"><span data-stu-id="f78fc-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="f78fc-307">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f78fc-307">Select **OK**.</span></span>
1. <span data-ttu-id="f78fc-308">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="f78fc-308">The new sales order is opened.</span></span> <span data-ttu-id="f78fc-309">ซึ่งมีบรรทัดว่างบน FastTab **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="f78fc-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f78fc-310">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-311">**สินค้า:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="f78fc-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="f78fc-312">**ปริมาณ:** _20_</span><span class="sxs-lookup"><span data-stu-id="f78fc-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="f78fc-313">เลือก **สร้างบรรทัด** เพื่อเพิ่มบรรทัดใหม่ และตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="f78fc-314">**สินค้า:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="f78fc-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="f78fc-315">**ปริมาณ:** _8_</span><span class="sxs-lookup"><span data-stu-id="f78fc-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="f78fc-316">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f78fc-316">Select **Save**.</span></span>
1. <span data-ttu-id="f78fc-317">เลือก **สร้าง** เพื่อสร้างใบสั่งขายที่สอง</span><span class="sxs-lookup"><span data-stu-id="f78fc-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="f78fc-318">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ในฟิลด์ **บัญชีลูกค้า** ให้เลือก _US-008_</span><span class="sxs-lookup"><span data-stu-id="f78fc-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="f78fc-319">ในฟิลด์  **คลังสินค้า** เลือก _61_</span><span class="sxs-lookup"><span data-stu-id="f78fc-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="f78fc-320">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="f78fc-320">The new sales order is opened.</span></span> <span data-ttu-id="f78fc-321">ซึ่งมีบรรทัดว่างบน FastTab **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="f78fc-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f78fc-322">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f78fc-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="f78fc-323">**สินค้า:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="f78fc-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="f78fc-324">**ปริมาณ:** _1_</span><span class="sxs-lookup"><span data-stu-id="f78fc-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="f78fc-325">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f78fc-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="f78fc-326">ศึกษาสถานการณ์จำลองการแบ่งช่วงเวลาทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f78fc-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="f78fc-327">หลังจากที่มีองค์ประกอบของข้อกำหนดเบื้องต้นทั้งหมดแล้ว ตามที่อธิบายไว้ในหัวข้อก่อนหน้านี้ คุณก็พร้อมแล้วที่จะลองใช้คุณลักษณะนี้โดยการศึกษาแบบฝึกหัดแต่ละรายการในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="f78fc-328">สร้างความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-328">Generate demand</span></span>

1. <span data-ttu-id="f78fc-329">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการแบ่งช่วงเวลา** และเลือกเท็มเพลตการแบ่งช่วงเวลาที่คุณสร้างก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="f78fc-330">ในบานหน้าต่างการดำเนินการ เลือก **สร้างความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="f78fc-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="f78fc-331">คำสั่งนี้จะประเมินความต้องการทั้งหมดที่อยู่ในระบบ และที่ตรงกับการสอบถามเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="f78fc-332">จากนั้น จะมีการรวมความต้องการทั้งหมดในใบสั่งทั้งหมดไปยังบรรทัดเดียวต่อปริมาณ/หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="f78fc-333">ข้อความแสดงข้อมูลจะปรากฏขึ้น เมื่อกระบวนการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f78fc-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="f78fc-334">ความต้องการในการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-334">Slotting demand</span></span>

<span data-ttu-id="f78fc-335">*ความต้องการการแบ่งช่วงเวลา* แสดงผลลัพธ์ของการสร้างความต้องการ ตามการตั้งค่าของเท็มเพลตการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="f78fc-336">ในบานหน้าต่างการดำเนินการ ให้เลือก **ความต้องการการแบ่งช่วงเวลา** เพื่อดูผลลัพธ์จากคำสั่ง **สร้างความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="f78fc-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="f78fc-337">บรรทัดในความต้องการการแบ่งช่วงเวลาสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="f78fc-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="f78fc-338">คุณสามารถลบบรรทัด เพิ่มบรรทัดใหม่ หรือแก้ไขรายละเอียดของบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="f78fc-339">คุณสามารถแก้ไขความต้องการด้วยตนเอง หรือคุณสามารถนำเข้าจากระบบภายนอกโดยใช้การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f78fc-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="f78fc-340">สิ่งใดก็ตามที่อยู่ในความต้องการการแบ่งช่วงเวลาจะถูกนำมาใช้ในขั้นตอนต่อไป โดยไม่คำนึงถึงสถานที่ที่มา</span><span class="sxs-lookup"><span data-stu-id="f78fc-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="f78fc-341">ค้นหาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-341">Locate demand</span></span>

<span data-ttu-id="f78fc-342">หลังจากที่สร้างความต้องการแล้ว คุณต้องใช้คำสั่ง **ค้นหาความต้องการ** เพื่อสร้าง *แผนการแบ่งช่วงเวลา*</span><span class="sxs-lookup"><span data-stu-id="f78fc-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="f78fc-343">ในบานหน้าต่างการดำเนินการ เลือก **ค้นหาความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="f78fc-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="f78fc-344">กระบวนการแบ่งช่วงเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="f78fc-344">The slotting process runs.</span></span> <span data-ttu-id="f78fc-345">ข้อความแสดงข้อมูลจะปรากฏขึ้น เมื่อกระบวนการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f78fc-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="f78fc-346">แผนการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f78fc-346">Slotting plan</span></span>

<span data-ttu-id="f78fc-347">แผนการแบ่งช่วงเวลาแสดงสถานที่ที่กำหนดให้กับสินค้า/ปริมาณแต่ละรายการ ไม่ว่าจะมีการใช้มากเกินไปหรือไม่ หรือไม่ว่าจะมีการสร้างงานการหยุดหรือไม่ และบรรทัดเท็มเพลตที่ใช้</span><span class="sxs-lookup"><span data-stu-id="f78fc-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="f78fc-348">*ความต้องการใดๆ ที่ไม่สามารถแบ่งช่วงเวลาได้ ถูกเน้นเป็นสีแดง*</span><span class="sxs-lookup"><span data-stu-id="f78fc-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="f78fc-349">ในบานหน้าต่างการดำเนินการ ให้เลือก **แผนการแบ่งช่วงเวลา** เพื่อดูผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f78fc-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="f78fc-350">กระบวนการ **สร้างความต้องการ** **ค้นหาความต้องการ** และ **การรันเติมสินค้า** จะรันใน Sandbox ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="f78fc-351">(กระบวนการเหล่านี้จะพร้อมใช้งานจากบานหน้าต่างการดำเนินการบนหน้า **แม่แบบการแบ่งช่วงเวลา**)</span><span class="sxs-lookup"><span data-stu-id="f78fc-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="f78fc-352">กระบวนการ **สร้างความต้องการ** **ค้นหาความต้องการ** และ **รันการเติมสินค้า** มีล็อคเพื่อให้มั่นใจว่าจะไม่สามารถทริกเกอร์ในเวลาเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="f78fc-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="f78fc-353">มิฉะนั้น อาจลบข้อมูลที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="f78fc-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="f78fc-354">กระบวนการ **สร้างความต้องการ** และ **ค้นหาความต้องการ** แสดงคำเตือนถ้าการรันไม่ได้สร้างเรกคอร์ดหรือถ้าเรกคอร์ดขาดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f78fc-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="f78fc-355">เมื่อคุณเลือก **แผนการแบ่งช่วงเวลา** หน้าไม่มีปุ่ม **สร้าง** **แก้ไข** หรือ **ลบ** บนบานหน้าต่างการดำเนินการ เนื่องจากไม่สามารถแก้ไขแหล่งข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="f78fc-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="f78fc-356">เมื่อคุณเลือก **รันการเติมสินค้า** ระบบจะตรวจสอบความถูกต้องของแม่แบบและกระบวนการของช่องทางที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f78fc-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="f78fc-357">สร้างการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-357">Create replenishment</span></span>

<span data-ttu-id="f78fc-358">หลังจากที่สร้างแผนการแบ่งช่วงเวลาแล้ว คุณต้องสร้าง *งานการเติมสินค้า* ตามแผน</span><span class="sxs-lookup"><span data-stu-id="f78fc-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="f78fc-359">บนบานหน้าต่างการดำเนินการ เลือก **รันการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f78fc-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="f78fc-360">ข้อความแสดงข้อมูลจะปรากฏขึ้น เมื่อกระบวนการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f78fc-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="f78fc-361">ข้อความนี้แสดงจำนวนของส่วนหัวที่สร้างขึ้นสำหรับรหัสการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="f78fc-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="f78fc-362">มีการระบุคำสั่งสถานที่ที่จะใช้ตามรหัสคำสั่งที่มีการระบุไว้ในบรรทัดเท็มเพลตแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f78fc-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="f78fc-363">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="f78fc-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="f78fc-364">ตั้งค่าการแบ่งช่วงเวลาแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f78fc-364">Set up automatic slotting</span></span>

<span data-ttu-id="f78fc-365">หลังจากที่มีองค์ประกอบที่ต้องการทั้งหมด คุณสามารถตั้งค่าการแบ่งช่วงเวลาเพื่อรันโดยอัตโนมัติโดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f78fc-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="f78fc-366">ไปที่ **การจัดการคลังสินค้า \> การเติมสินค้า \> รันการแบ่งช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="f78fc-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="f78fc-367">ระบุขั้นตอนการแบ่งช่วงเวลาที่จะรัน</span><span class="sxs-lookup"><span data-stu-id="f78fc-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="f78fc-368">เลือกขั้นตอนการแบ่งช่วงเวลาต่อไปนี้อย่างน้อยหนึ่งขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="f78fc-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="f78fc-369">สร้างความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-369">Generate demand</span></span>
    - <span data-ttu-id="f78fc-370">ค้นหาความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-370">Locate demand</span></span>
    - <span data-ttu-id="f78fc-371">สร้างงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="f78fc-372">ขั้นตอนการแบ่งช่วงเวลามีความก้าวหน้า</span><span class="sxs-lookup"><span data-stu-id="f78fc-372">The slotting steps are progressive.</span></span> <span data-ttu-id="f78fc-373">ถ้าคุณต้องการเลือก *ค้นหาความต้องการ* คุณต้องเลือก *สร้างความต้องการ* ก่อน</span><span class="sxs-lookup"><span data-stu-id="f78fc-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="f78fc-374">ระบุเท็มเพลตการแบ่งช่วงเวลาที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="f78fc-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="f78fc-375">ตั้งค่าการเกิดซ้ำเพื่อรันโดยอัตโนมัติ ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f78fc-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="f78fc-376">สำหรับแบบฝึกหัดในสถานการณ์สมมติ **อย่า** ตั้งค่าการแบ่งช่วงเวลาแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f78fc-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
