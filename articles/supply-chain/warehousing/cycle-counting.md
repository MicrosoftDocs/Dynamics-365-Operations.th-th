---
title: "การตรวจนับตามรอบ"
description: "บทความนี้อธิบายวิธีการใช้การตรวจนับตามรอบกับโซลูชันคลังสินค้าที่จะพร้อมใช้งานในการจัดการคลังสินค้า  บทความนี้ไม่ใช้กับโซลูชันคลังสินค้าที่พร้อมใช้งานในการบริหารสินค้าคงคลัง"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2437d3efe7841021ff4bd35f307fddddc76eb4c6
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="cycle-counting"></a><span data-ttu-id="af6d4-104">การตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-104">Cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="af6d4-105">บทความนี้อธิบายวิธีการใช้การตรวจนับตามรอบกับโซลูชันคลังสินค้าที่จะพร้อมใช้งานในการจัดการคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="af6d4-105">This article describes how you can use cycle counting with the warehousing solution that is available in Warehouse management.</span></span> <span data-ttu-id="af6d4-106">บทความนี้ไม่ใช้กับโซลูชันคลังสินค้าที่พร้อมใช้งานในการบริหารสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="af6d4-106">This article doesn't apply to the warehousing solution that's available in Inventory management.</span></span>

<span data-ttu-id="af6d4-107">การตรวจนับตามรอบเป็นกระบวนการคลังสินค้าที่คุณสามารถใช้ตรวจสอบสินค้าคงคลังคงเหลือ </span><span class="sxs-lookup"><span data-stu-id="af6d4-107">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="af6d4-108">สามารถอธิบายเกี่ยวกับกระบวนการตรวจนับตามรอบได้ในสามขั้นตอนนี้:</span><span class="sxs-lookup"><span data-stu-id="af6d4-108">The cycle counting process can be described in three steps:</span></span>

1.  <span data-ttu-id="af6d4-109">**สร้างงานวงจรการตรวจนับตามรอบ** –งานวงจรการตรวจนับตามรอบอาจถูกสร้างโดยอัตโนมัติตามพารามิเตอร์ขีดจำกัด สำหรับสินค้า หรือ โดยใช้แผนการตรวจนับวงจร</span><span class="sxs-lookup"><span data-stu-id="af6d4-109">**Create cycle counting work** – Cycle counting work can be created automatically, based on threshold parameters for items or by using a cycle counting plan.</span></span> <span data-ttu-id="af6d4-110">หรือคุณยังสามารถสร้างงานการตรวจนับตามรอบด้วยตนเอง โดยการใช้พารามิเตอร์สินค้าหรือคลังสินค้าในหน้า **งานการตรวจนับตามรอบตามสินค้า** หรือหน้า **งานการตรวจนับตามที่ตั้ง**</span><span class="sxs-lookup"><span data-stu-id="af6d4-110">Alternatively, you can manually create cycle counting work by using the item or warehouse parameters on the **Cycle count work by item** page or the **Cycle count work by location** page.</span></span>
2.  <span data-ttu-id="af6d4-111">**ดำเนินการตรวจนับตามรอบ** – หลังจากที่คุณสร้างงานการตรวจนับตามรอบแล้ว ให้คุณดำเนินการงานการตรวจนับ ด้วยการตรวจนับสินค้าในที่ตั้งคลังสินค้า และใช้อุปกรณ์เคลื่อนที่ป้อนผลลัพธ์ใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="af6d4-111">**Process the cycle count** – After cycle counting work is created, you do the cycle counting work by counting items in a warehouse location and then using a mobile device to enter the result in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="af6d4-112">อีกทางหนึ่งคือ คุณสามารถนับสินค้าในที่ตั้งคลังสินค้าโดยไม่ต้องมีการสร้างงานการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-112">Alternatively, you can count items in a warehouse location without creating cycle counting work.</span></span> <span data-ttu-id="af6d4-113">กระบวนการนี้เรียกว่า *การตรวจนับตามรอบทันที*</span><span class="sxs-lookup"><span data-stu-id="af6d4-113">This process is referred to as *spot cycle counting*.</span></span>
3.  <span data-ttu-id="af6d4-114">**แก้ไขความแตกต่างในค่าที่ตรวจนับตามรอบ** – หลังจากการตรวจนับตามรอบ รายการใดๆ ที่มีความแตกต่างของค่าที่ตรวจนับจะมีสถานะเป็น **การตรวจทานที่ค้างอยู่** ในหน้า **งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="af6d4-114">**Resolve differences in the counted value** – After a cycle count, any items that have differences in the counted value will have a work status of **Pending review** on the **All work** page.</span></span> <span data-ttu-id="af6d4-115">คุณสามารถแก้ไขความแตกต่างเหล่านี้ได้ในหน้า **การตรวจทานที่ค้างอยู่ของการตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="af6d4-115">You can resolve these differences on the **Cycle count work pending review** page.</span></span>

<span data-ttu-id="af6d4-116">ภาพต่อไปนี้แสดงกระบวนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-116">The following illustration shows the cycle counting process.</span></span> ![ลำดับกระบวนการตรวจนับตามรอบทันที](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a><span data-ttu-id="af6d4-118">ข้อกำหนดเบื้องต้นของการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-118">Cycle counting prerequisites</span></span>
<span data-ttu-id="af6d4-119">ตารางต่อไปนี้แสดงข้อกำหนดเบื้องต้นที่ต้องมีก่อนที่คุณจะใช้การตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-119">The following table shows the prerequisites that must be in place before you can use cycle counting.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af6d4-120">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="af6d4-120">Prerequisite</span></span></th>
<th><span data-ttu-id="af6d4-121">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="af6d4-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af6d4-122">สินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-122">Item</span></span></td>
<td><span data-ttu-id="af6d4-123">สินค้าที่จะต้องใช้สำหรับกระบวนการบริหารคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-123">The item must be enabled for warehouse management processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af6d4-124">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-124">Warehouse</span></span></td>
<td><span data-ttu-id="af6d4-125">คลังสินค้าที่ใช้สำหรับกระบวนการบริหารคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-125">The warehouse must be enabled for warehouse management processes.</span></span> <span data-ttu-id="af6d4-126">การเปิดใช้งานคลังสินค้าสำหรับกระบวนการบริหารคลังสินค้า ในหน้า <strong>คลังสินค้า</strong> ให้เลือกคลังสินค้า จากนั้นเลือกตัวเลือก <strong>ใช้กระบวนการจัดการคลังสินค้า</strong></span><span class="sxs-lookup"><span data-stu-id="af6d4-126">To enable the warehouse for warehouse management processes, on the <strong>Warehouses</strong> page, select the warehouse, and then select the <strong>Use warehouse management processes</strong> option.</span></span> <span data-ttu-id="af6d4-127">เมื่อต้องการให้ผู้ปฏิบัติงานสามารถย้ายแท่นวางสินค้าในระหว่างการตรวจนับตามรอบ บนแท็บด่วน <strong>การบริหารคลังสินค้า</strong> ให้เลือกตัวเลือก <strong>อนุญาตให้ย้ายแท่นวางสินค้าในระหว่างการตรวจนับตามรอบ</strong></span><span class="sxs-lookup"><span data-stu-id="af6d4-127">To enable workers to move pallets during a cycle count, on the <strong>Warehouse management</strong> FastTab, select the <strong>Allow pallet moves during cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af6d4-128">กลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="af6d4-128">Work pools</span></span></td>
<td><span data-ttu-id="af6d4-129">ตัวเลือก: สร้างกลุ่มงานเพื่อแยกงานคลังสินค้า ที่ขึ้นอยู่กับชนิดของงาน (ในกรณีนี้ งานการตรวจนับตามรอบ)</span><span class="sxs-lookup"><span data-stu-id="af6d4-129">Optional: Create a work pool to segregate the warehouse work, based on the type of work (in this case, cycle counting work).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af6d4-130">ตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="af6d4-130">Locations</span></span></td>
<td><span data-ttu-id="af6d4-131">เปิดใช้งานกระบวนการการตรวจนับตามรอบสำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-131">Enable cycle counting for locations.</span></span> <span data-ttu-id="af6d4-132">เมื่อต้องการเปิดใช้งานการตรวจนับตามรอบสำหรับที่ตั้งคลังสินค้า หน้า <strong>โพรไฟล์สถานที่</strong> เลือกตัวเลือก <strong>อนุญาตการตรวจนับตามรอบ</strong></span><span class="sxs-lookup"><span data-stu-id="af6d4-132">To enable cycle counting for a warehouse location, on the <strong>Location profiles</strong> page, select the <strong>Allow cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af6d4-133">พารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-133">Warehouse management parameters</span></span></td>
<td><span data-ttu-id="af6d4-134">ตั้งค่าพารามิเตอร์สำหรับการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-134">Set up parameters for cycle counting.</span></span> <span data-ttu-id="af6d4-135">ในหน้า <strong>พารามิเตอร์การจัดการคลังสินค้า</strong> ให้ระบุรปรับปรุงค่าเริ่มต้น รหัสคลาสงาน และระดับความสำคัญของงานสำหรับการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-135">On the <strong>Warehouse management parameters</strong> page, specify the default adjustment type code, work class ID, and work priority for cycle counting.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af6d4-136">อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-136">Mobile device</span></span></td>
<td><ul>
<li><span data-ttu-id="af6d4-137">สร้างรายการเมนูสำหรับหนึ่งในวิธีต่อไปนี้ ในหน้า <strong>รายการเมนูของอุปกรณ์เคลื่อนที่</strong> :</span><span class="sxs-lookup"><span data-stu-id="af6d4-137">Create a menu item for one of the following methods on the <strong>Mobile device menu items</strong> page:</span></span>
<ul>
<li><span data-ttu-id="af6d4-138">การตรวจนับตามรอบที่สั่งการโดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="af6d4-138">User directed cycle counting</span></span></li>
<li><span data-ttu-id="af6d4-139">การตรวจนับตามรอบที่สั่งการโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-139">System directed cycle counting</span></span></li>
<li><span data-ttu-id="af6d4-140">จัดกลุ่มการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-140">Cycle count grouping</span></span></li>
<li><span data-ttu-id="af6d4-141">การตรวจนับตามรอบทันที</span><span class="sxs-lookup"><span data-stu-id="af6d4-141">Spot cycle counting</span></span></li>
</ul>
</li>
<li><span data-ttu-id="af6d4-142">ตั้งค่าเมนูสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-142">Set up a menu for the mobile device.</span></span></li>
<li><span data-ttu-id="af6d4-143">สร้างบัญชีผู้ใช้งาน และกำหนดเมนูอุปกรณ์เคลื่อนที่ให้กับรหัสผู้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="af6d4-143">Create a work user account, and assign a mobile device menu to the work user ID.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af6d4-144">งานการตั้งค่าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="af6d4-144">Related setup task</span></span></td>
<td><span data-ttu-id="af6d4-145">ตั้งค่าการวางแผนวงจรการตรวจนับสำหรับที่ตั้งคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-145">Set up a cycle counting plan for a warehouse location.</span></span></td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a><span data-ttu-id="af6d4-146">สร้างงานการตรวจนับตามรอบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="af6d4-146">Automatically create cycle counting work</span></span>
<span data-ttu-id="af6d4-147">มีวิธีสองวิธีในการจัดกำหนดการสร้างงานที่เกิดซ้ำของการตรวจนับตามรอบ: ตั้งค่าขีดจำกัดการตรวจนับตามรอบ หรือตั้งค่าแผนการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-147">There are two ways to schedule recurring creation of cycle counting work: set up cycle counting thresholds or set up cycle counting plans.</span></span>

-   <span data-ttu-id="af6d4-148">ขีดจำกัดการตรวจนับตามรอบบ่งชี้ขีดจำกัดปริมาณหรือเปอร์เซ็นต์ของสินค้าในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="af6d4-148">A cycle counting threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="af6d4-149">งานการตรวจนับตามรอบถูกสร้างขึ้นโดยอัตโนมัติเมื่อถึงขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="af6d4-149">Cycle counting work is automatically created when the threshold limit is reached.</span></span>
-   <span data-ttu-id="af6d4-150">แผนการตรวจนับตามรอบสร้างงานการตรวจนับตามรอบโดยทันทีหรือเป็นระยะๆผ่านชุดงาน</span><span class="sxs-lookup"><span data-stu-id="af6d4-150">A cycle counting plan creates cycle counting work either immediately or periodically through a batch job.</span></span> <span data-ttu-id="af6d4-151">เมื่อมีสร้างงานการตรวจนับตามรอบ งานที่ตรวจนับจะรวมข้อมูลเกี่ยวกับที่ตั้งเพื่อตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="af6d4-151">When cycle counting work is created, the counting work line includes information about the location to count.</span></span> <span data-ttu-id="af6d4-152">สินค้าคงคลังคงเหลือที่สัมพันธ์กับตำแหน่งที่ตั้งนี้จะไม่ถูกบล็อค และดังนั้นจึงพร้อมใช้งานสำหรับการจองและการประมวลผลขาออก ถึงแม้ว่างานการตรวจนับที่เปิดจะยังมีอยู่</span><span class="sxs-lookup"><span data-stu-id="af6d4-152">The on-hand inventory that is associated with this location isn't blocked, and is therefore available for reservation and outbound processing, even though open counting work exists.</span></span>

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a><span data-ttu-id="af6d4-153">สร้างงานการตรวจนับตามรอบ ตามพารามิเตอร์ขีดจำกัดสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-153">Create cycle counting work, based on threshold parameters for items</span></span>

<span data-ttu-id="af6d4-154">งานการตรวจนับตามรอบสามารถถูกสร้างเมื่อจำนวนสินค้าลดลงต่ำกว่าค่าขีดจำกัดที่ระบุในสถานที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-154">Cycle counting work can be created when the number of items falls below a specific threshold value in a location.</span></span> <span data-ttu-id="af6d4-155">ตัวอย่างเช่น มีสินค้า 60 รายการในสถานที่ที่มีขีดจำกัดการตรวจนับตามรอบคือ 40</span><span class="sxs-lookup"><span data-stu-id="af6d4-155">For example, there are 60 items in a location that has a cycle counting threshold of 40.</span></span> <span data-ttu-id="af6d4-156">ในระหว่างธุรกรรมใบสั่งขาย สินค้า 25 รายการจะถูกเบิกจากสถานที่ และเก็บไว้ในสถานที่การจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="af6d4-156">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="af6d4-157">เนื่องจากจำนวนสินค้าใหม่ 35 รายการน้อยกว่าปริมาณขีดจำกัด งานการตรวจนับตามรอบจะมีการสร้างโดยอัตโนมัติสำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-157">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

### <a name="schedule-cycle-counting-work"></a><span data-ttu-id="af6d4-158">จัดกำหนดการงานการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-158">Schedule cycle counting work</span></span>

<span data-ttu-id="af6d4-159">คุณสามารถจัดกำหนดการแผนการตรวจนับตามรอบเพื่อสร้างงานการตรวจนับตามรอบในทันทีหรือเป็นระยะๆ</span><span class="sxs-lookup"><span data-stu-id="af6d4-159">You can schedule cycle counting plans to create cycle counting work immediately or periodically.</span></span> <span data-ttu-id="af6d4-160">คุณสามารถจัดกำหนดการแผนการตรวจนับตามรอบ เพื่อสร้างการตรวจนับตามรอบในทันทีหรือเป็นระยะๆ ด้วยการตั้งค่าแผนการตรวจนับตามรอบ คุณสามารถควบคุมกลุ่มงานที่สร้างขึ้นสำหรับงานการตรวจนับตามรอบ จำนวนสูงสุดของการตรวจนับตามรอบที่ถูกสร้างขึ้นสำหรับสินค้าในสถานที่แตกต่างกัน และจำนวนวันก่อนที่ตั้งคลังสินค้าถูกนับอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="af6d4-160">By setting up cycle counting plans, you can control the work pool that cycle counting work is created for, the maximum number of cycle counts that are created for items in different locations, and the number of days before a warehouse location is counted again.</span></span> <span data-ttu-id="af6d4-161">ตัวอย่างเช่น สินค้าจะพร้อมใช้งานในคลังสินค้าสามแห่ง และจำนวนสูงสุดของการตรวจนับตามรอบถูกกำหนดเป็น **2**</span><span class="sxs-lookup"><span data-stu-id="af6d4-161">For example, an item is available in three locations in the warehouse, and the maximum number of cycle counts is set to **2**.</span></span> <span data-ttu-id="af6d4-162">ในกรณีนี้ เมื่อคุณรันแผนการตรวจนับตามรอบ การตรวจนับตามรอบสองครั้งจะถูกสร้างสำหรับสถานที่สองแห่งซึ่งมีสินค้าอยู่</span><span class="sxs-lookup"><span data-stu-id="af6d4-162">In this case, when you run the cycle counting plan, two cycle counts are created for the two locations where the item is present.</span></span> <span data-ttu-id="af6d4-163">อีกตัวอย่างหนึ่งคือ คุณตั้งค่าจำนวนวันระหว่างการตรวจนับตามรอบเป็น **5**</span><span class="sxs-lookup"><span data-stu-id="af6d4-163">As another example, you set the number of days between cycle counts to **5**.</span></span> <span data-ttu-id="af6d4-164">ในกรณีนี้ งานการตรวจนับตามรอบจะถูกสร้างขึ้นทุกๆห้าวัน</span><span class="sxs-lookup"><span data-stu-id="af6d4-164">In this case, cycle counting work is created every five days.</span></span> <span data-ttu-id="af6d4-165">อย่างไรก็ตาม ถ้างานการตรวจนับตามรอบมีการประมวลผลในวันที่ 3 วงานการตรวจนับตามรอบจะมีการสร้างในห้าวันหลังจากการตรวจนับตามรอบล่าสุดถูกประมวลผลในวันที่ 8</span><span class="sxs-lookup"><span data-stu-id="af6d4-165">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

## <a name="create-cycle-counting-work-manually"></a><span data-ttu-id="af6d4-166">สร้างงานการตรวจนับตามรอบด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="af6d4-166">Create cycle counting work manually</span></span>
<span data-ttu-id="af6d4-167">เพื่อสร้างงานการตรวจนับตามรอบด้วยตนเอง คุณสามารถใช้หน้า **งานการตรวจนับตามรอบตามสินค้า** หรือ **งานการตรวจนับตามรอบตามสถานที่** ได้</span><span class="sxs-lookup"><span data-stu-id="af6d4-167">To create cycle counting work manually, you can use the **Cycle count work by item** or **Cycle count work by location** page.</span></span> <span data-ttu-id="af6d4-168">คุณสามารถระบุจำนวนสูงสุดของการนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-168">You can specify the maximum number of cycle counts to create.</span></span> <span data-ttu-id="af6d4-169">ตัวอย่างเช่น ถ้าผู้จัดการคลังสินค้าระบุค่าเป็น **5** มีการสร้างงานการตรวจนับตามรอบสำหรับสถานที่เก็บห้าแห่ง แม้ว่าสินค้าจะแสดงอยู่ในที่ตั้ง 10 แห่งก็ตาม</span><span class="sxs-lookup"><span data-stu-id="af6d4-169">For example, if the warehouse manager specifies a value of **5**, cycle counting work is created for five locations, even if the item is present in 10 locations.</span></span> <span data-ttu-id="af6d4-170">คุณยังสามารถเลือกรหัสกลุ่มงานเพือกำหนดให้งานการตรวจนับตามรอบรหัสที่จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="af6d4-170">You can also select a work pool ID to assign the cycle counting work IDs that are created to.</span></span> <span data-ttu-id="af6d4-171">เมื่อมีการประมวลผลรหัสกลุ่มงานสำหรับการตรวจนับตามรอบ รหัสงานการตรวจนับตามรอบที่ถูกกำหนดให้กับกลุ่มงาน จะถูกประมวลผลเป็นกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="af6d4-171">When a work pool ID is processed for cycle counting, the cycle counting work IDs that are assigned to the work pool are processed as a group.</span></span>

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a><span data-ttu-id="af6d4-172">ดำเนินการตรวจนับตามรอบโดยการใช้อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-172">Perform a cycle count by using a mobile device</span></span>
<span data-ttu-id="af6d4-173">มีวิธีหลายวิธีในการดำเนินการกับงานการตรวจนับตามรอบโดยการใช้ Finance and Operations บนอุปกรณ์เคลื่อนที่:</span><span class="sxs-lookup"><span data-stu-id="af6d4-173">There are several methods for processing cycle counting work by using Finance and Operations on a mobile device:</span></span>

-   <span data-ttu-id="af6d4-174">**สั่งการโดยผู้ใช้** – ผู้ปฏิบัติงานสามารถระบุรหัสงานการตรวจนับตามรอบที่อยู่ในสถานะ **เปิด**</span><span class="sxs-lookup"><span data-stu-id="af6d4-174">**User directed** – The worker can specify a cycle counting work ID that has a status of **Open**.</span></span>
-   <span data-ttu-id="af6d4-175">**สั่งการโดยระบบ** – Finance and Operations กำหนดรหัสงานการตรวจนับตามรอบให้กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="af6d4-175">**System directed** – Finance and Operations assigns a cycle counting work ID to the worker.</span></span>
-   <span data-ttu-id="af6d4-176">**การจัดกลุ่มการตรวจนับตามรอบ** – ผู้ปฏิบัติงานสามารถจัดกลุ่มรหัสงานการตรวจนับตามรอบที่เฉพาะเจาะจงไปยังสถานที่ โซน หรือกลุ่มงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="af6d4-176">**Cycle count grouping** – The worker can group cycle counting work IDs that are specific to a particular location, zone, or work pool.</span></span>
-   <span data-ttu-id="af6d4-177">**การตรวจนับตามรอบทันที** – ผู้ปฏิบัติงานสามารถตรวจนับสินค้าในที่ตั้งคลังสินค้าได้ตลอดเวลา โดยไม่ต้องสร้างงานการตรวจนับตามรอบด้วยการป้อนรหัสสถานที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-177">**Spot cycle counting** – The worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="af6d4-178">เพื่อดำเนินการตรวจนับตามรอบทันทีในสถานที่ ผู้ปฏิบัติงานป้อนรหัสสถานที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-178">To perform spot cycle counting in a location, the worker enters the location ID.</span></span>

<span data-ttu-id="af6d4-179">ตัวอย่างต่อไปนี้แสดงวิธีที่คุณสามารถดำเนินการตรวจนับตามรอบทันที โดยใช้อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-179">The following example shows how you can perform spot cycle counting by using a mobile device.</span></span> <span data-ttu-id="af6d4-180">คำแนะนำที่ผู้ปฏิบัติงานมองเห็นบนอุปกรณ์จะต่างกัน โดยขึ้นอยู่กับการตั้งค่าของรายการเมนูสำหรับการตรวจนับตามรอบทันที</span><span class="sxs-lookup"><span data-stu-id="af6d4-180">The instructions that the worker sees on the device vary, depending on the setup of the menu item for spot cycle counting.</span></span>

1.  <span data-ttu-id="af6d4-181">บนอุปกรณ์เคลื่อน ให้เลือกรายการในเมนูที่จะทำงานการตรวจนับตามรอบทันที</span><span class="sxs-lookup"><span data-stu-id="af6d4-181">On the mobile device, select the menu item to process spot cycle counting work.</span></span>
2.  <span data-ttu-id="af6d4-182">ลงทะเบียนที่ตั้งเพื่อดำเนินการสำหรับการตรวจนับตามรอบทันที</span><span class="sxs-lookup"><span data-stu-id="af6d4-182">Register the location to perform spot cycle counting for.</span></span>
3.  <span data-ttu-id="af6d4-183">ลงทะเบียนและยืนยันหมายเลขของสินค้าและปริมาณสินค้าที่ตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="af6d4-183">Register and confirm the item number and the counted item quantity.</span></span> <span data-ttu-id="af6d4-184">**หมายเหตุ:** สถานะของงานการตรวจนับตามรอบถูกอัพเดตเป็น **การตรวจทานที่ค้างอยู่** หรือ **ปิดแล้ว** บนหน้า **งานทั้งหมด** ขึ้นอยู่กับพารามิเตอร์ที่ถูกตั้งค่าในหน้า **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="af6d4-184">**Note:** The status of the cycle counting work is updated to either **Pending review** or **Closed** on the **All work** page, depending on the parameters that are set on the **Worker** page.</span></span>
4.  <span data-ttu-id="af6d4-185">ตัวเลือก: ทำซ้ำขั้นตอนที่ 3 สำหรับสินค้าที่เหลืออยู่ในสถานที่ และยืนยันว่าไม่มีสินค้าเพิ่มเติมพร้อมสำหรับการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="af6d4-185">Optional: Repeat step 3 for the remaining items in the location, and confirm that no additional items are available for counting.</span></span>

## <a name="resolve-cycle-counting-differences"></a><span data-ttu-id="af6d4-186">แก้ไขความแตกต่างของการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="af6d4-186">Resolve cycle counting differences</span></span>
<span data-ttu-id="af6d4-187">ความแตกต่างของการตรวจนับตามรอบจะเกิดขึ้นในสถานการณ์ต่อไปนี้ ถ้าตัวเลือก **เป็นหัวหน้างานการตรวจนับตามรอบหรือไม่** ถูกตั้งค่าเป็น **ไม่** สำหรับรหัสผู้ใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="af6d4-187">A cycle counting difference occurs in the following scenarios if the **Is a cycle count supervisor** option is set to **No** for a work user ID:</span></span>

-   <span data-ttu-id="af6d4-188">ค่าที่ตรวจนับไม่ได้อยู่ในขีดจำกัดความเบี่ยงเบนที่ระบุไว้ในฟิลด์ **ขีดจำกัดเปอร์เซ็นต์สูงสุด** หรือ **ขีดจำกัดเปอร์เซ็นต์ต่ำสุด** ในหน้า **ผู้ใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="af6d4-188">The counted value isn't within the deviation limits that are specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page.</span></span> <span data-ttu-id="af6d4-189">ตัวอย่างเช่น ปริมาณคงคลังคงเหลือในสถานที่คือ 50 และขีดจำกัดความเบี่ยงเบนสำหรับผู้ใช้งานคือ 10</span><span class="sxs-lookup"><span data-stu-id="af6d4-189">For example, the on-hand inventory quantity in a location is 50, and the deviation limit for the work user is 10.</span></span> <span data-ttu-id="af6d4-190">ถ้าผู้ใช้งานป้อนค่าที่ไม่ได้อยู่ระหว่าง 40 ถึง 60 จะมีความแตกต่างเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="af6d4-190">If the work user enters a value that isn't between 40 and 60, a difference occurs.</span></span>
-   <span data-ttu-id="af6d4-191">ค่าที่ตรวจนับแตกต่างจากปริมาณคงคลังคงเหลือ และไม่ได้มีการกำหนดขีดจำกัดความเบี่ยงเบน</span><span class="sxs-lookup"><span data-stu-id="af6d4-191">The counted value differs from the on-hand inventory quantity, and no deviation limits are set.</span></span>

<span data-ttu-id="af6d4-192">คุณสามารถปรับปรุงความแตกต่างของค่าตรวจนับ และจากนั้นยอมรับค่าที่ตรวจนับแล้วบนหน้า **การตรวจนับตามรอบการตรวจทานที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="af6d4-192">You can adjust differences in the counted value and then accept the counted value on the **Cycle count pending review** page.</span></span> <span data-ttu-id="af6d4-193">คุณสามารถตรวจสอบการนับที่แก้ไขแล้วของปริมาณของสินค้าในหน้า **คงเหลือตามสถานที่**</span><span class="sxs-lookup"><span data-stu-id="af6d4-193">You can verify the modified count of the item quantity on the **On hand by location** page.</span></span> <span data-ttu-id="af6d4-194">ค่าการตรวจนับจะถูกปฏิเสธถ้าไม่สามารถอนุมัติความแตกต่างได้</span><span class="sxs-lookup"><span data-stu-id="af6d4-194">The counted value is rejected if the difference can't be approved.</span></span>

# <a name="see-also"></a><span data-ttu-id="af6d4-195">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="af6d4-195">See also</span></span>
[<span data-ttu-id="af6d4-196">ตั้งค่าคอนฟิกอุปกรณ์เคลื่อนที่สำหรับงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="af6d4-196">Configure mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)




