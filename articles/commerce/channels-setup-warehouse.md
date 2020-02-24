---
title: ตั้งค่าคลังสินค้า
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคลังสินค้าที่จะใช้กับช่องทางใหม่ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fe785e3bfd503193a588958ae5df0d1c0fdb9e52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002323"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="6da54-103">การตั้งค่าคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6da54-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าคลังสินค้าที่จะใช้กับช่องทางใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6da54-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6da54-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="6da54-105">Overview</span></span>

<span data-ttu-id="6da54-106">แต่ละช่องทาง Commerce ต้องใช้คลังสินค้าที่ตั้งค่าคอนฟิกไว้เพื่อเชื่อมโยงกับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="6da54-107">ขั้นตอนต่อไปนี้จะให้การตั้งค่าคอนฟิกต่ำสุดที่จำเป็นสำหรับการตั้งค่าคลังสินค้าสำหรับช่องทาง Commerce</span><span class="sxs-lookup"><span data-stu-id="6da54-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="6da54-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าคลังสินค้า โปรดดูที่ [ภาพรวมของการจัดการคลังสินค้า](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)</span><span class="sxs-lookup"><span data-stu-id="6da54-108">For more information regarding warehouse setup, please see the [Warehouse management overview](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="6da54-109">การตั้งค่าคอนฟิกไซต์คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-109">Configure a warehouse site</span></span>

<span data-ttu-id="6da54-110">ก่อนที่จะตั้งค่าคลังสินค้า คุณจำเป็นต้องตั้งค่าคอนฟิกไซต์คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="6da54-111">เมื่อต้องการตั้งค่าคอนฟิกไซต์คลังสินค้า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6da54-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="6da54-112">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ไซต์**</span><span class="sxs-lookup"><span data-stu-id="6da54-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="6da54-113">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6da54-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6da54-114">ในฟิลด์ **ไซต์** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6da54-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="6da54-115">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6da54-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6da54-116">ในส่วน **ทั่วไป** ให้ตั้งค่า **โซนเวลา** ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6da54-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="6da54-117">ในส่วน **ที่อยู่** ป้อนที่อยู่</span><span class="sxs-lookup"><span data-stu-id="6da54-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="6da54-118">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6da54-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6da54-119">รูปภาพต่อไปนี้แสดงตัวอย่างของไซต์คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-119">The following image shows an example warehouse site.</span></span>

![ตัวอย่างไซต์คลังสินค้า](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="6da54-121">ตั้งค่าคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-121">Set up a warehouse</span></span>

<span data-ttu-id="6da54-122">หากต้องการตั้งค่าคลังสินค้า ให้ดำเนินการตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6da54-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="6da54-123">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6da54-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6da54-124">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6da54-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6da54-125">ในฟิลด์ **คลังสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6da54-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="6da54-126">ถ้านี่เป็นการแม็ป 1:1 กับร้านค้าปลีก โปรดพิจารณาใช้ชื่อร้านค้า หรือชื่อของศูนย์กระจายสินค้าในภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="6da54-126">If this is a 1:1 mapping to a retail store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="6da54-127">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6da54-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6da54-128">ในรายการแบบหล่นลงของ **ไซต์** ให้เลือกไซต์คลังสินค้าที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="6da54-129">ในฟิลด์ **ชนิด** เลือก **โดยค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="6da54-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="6da54-130">ถ้าคุณต้องการกำหนด **คลังสินค้าตรวจสอบ** ก่อนอื่นคุณจำเป็นต้องทำตามขั้นตอนต่อไปนี้เพื่อสร้างคลังสินค้าเพิ่มเติมที่ **ชนิด** ตั้งค่าเป็น **การตรวจสอบสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6da54-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="6da54-131">ถ้าคุณต้องการกำหนด **คลังสินค้าส่งต่อ** ก่อนอื่นคุณจำเป็นต้องทำตามขั้นตอนต่อไปนี้เพื่อสร้างคลังสินค้าเพิ่มเติมที่ **ชนิด** ตั้งค่าเป็น **ส่งต่อ**</span><span class="sxs-lookup"><span data-stu-id="6da54-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="6da54-132">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6da54-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="6da54-133">ตั้งค่าที่เก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="6da54-133">Set up inventory aisles</span></span>

<span data-ttu-id="6da54-134">หากต้องการตั้งค่าที่เก็บสินค้าคงคลัง ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6da54-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="6da54-135">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่าสถานที่ \> ที่เก็บสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="6da54-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="6da54-136">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6da54-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6da54-137">ในรายการแบบหล่นลงของ **คลังสินค้า** ให้เลือกคลังสินค้าที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="6da54-138">ในฟิลด์ **ที่เก็บ** ให้ป้อนชื่อ (ตัวอย่างเช่น "Def")</span><span class="sxs-lookup"><span data-stu-id="6da54-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="6da54-139">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อ (ตัวอย่างเช่น "ที่เก็บเริ่มต้น")</span><span class="sxs-lookup"><span data-stu-id="6da54-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="6da54-140">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6da54-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="6da54-141">ตั้งค่าสถานที่เก็บสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="6da54-142">เมื่อต้องการตั้งค่าสถานที่เก็บสินค้าคงคลังของคลังสินค้าสำหรับสินค้าคงคลังมาตรฐาน ที่เสียหาย และที่ส่งคืน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6da54-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="6da54-143">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6da54-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6da54-144">เลือกคลังสินค้าที่คุณสร้างขึ้นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="6da54-145">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="6da54-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6da54-146">ในบานหน้าต่างการดำเนินการ ให้เลือก **คลังสินค้า** จากนั้นเลือก **สถานที่เก็บสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="6da54-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="6da54-147">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6da54-147">On the action pane, select **New**.</span></span> <span data-ttu-id="6da54-148">รายการแบบหล่นลงของ **คลังสินค้า** ควรเป็นค่าเริ่มต้นสำหรับคลังสินค้าใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6da54-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6da54-149">ในกล่อง **ที่เก็บ** ให้ป้อนชื่อของที่เก็บสินค้าที่คุณระบุไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6da54-150">ตั้งค่า **การอัพเดตด้วยตนเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6da54-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6da54-151">ในกล่อง **สถานที่ตั้ง** ให้ป้อนชื่อของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="6da54-152">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6da54-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6da54-153">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6da54-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="6da54-154">รายการแบบหล่นลงของ **คลังสินค้า** ควรเป็นค่าเริ่มต้นสำหรับคลังสินค้าใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6da54-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6da54-155">ในกล่อง **ที่เก็บ** ให้ป้อนชื่อของที่เก็บสินค้าที่คุณระบุไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="6da54-156">ตั้งค่า **การอัพเดตด้วยตนเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6da54-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6da54-157">ในกล่อง **สถานที่** ให้ป้อน "เสียหาย"</span><span class="sxs-lookup"><span data-stu-id="6da54-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="6da54-158">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6da54-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6da54-159">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6da54-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="6da54-160">รายการแบบหล่นลงของ **คลังสินค้า** ควรเป็นค่าเริ่มต้นสำหรับคลังสินค้าใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6da54-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6da54-161">ในกล่อง **ที่เก็บ** ให้ป้อนชื่อของที่เก็บสินค้าที่คุณระบุไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6da54-162">ตั้งค่า **การอัพเดตด้วยตนเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6da54-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6da54-163">ในกล่อง **สถานที่** ให้ป้อน "การส่งคืนสินค้า"</span><span class="sxs-lookup"><span data-stu-id="6da54-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="6da54-164">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6da54-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="6da54-165">รูปภาพต่อไปนี้แสดงการตั้งค่าสถานที่เก็บสินค้าคงคลังของคลังสินค้าที่ซานฟรานซิสโก</span><span class="sxs-lookup"><span data-stu-id="6da54-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![ตัวอย่างการตั้งค่าสถานที่เก็บสินค้าคงคลัง](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="6da54-167">ทำคลังสินค้าให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6da54-167">Complete warehouse setup</span></span>

<span data-ttu-id="6da54-168">เพื่อให้การตั้งค่าคลังสินค้าเสร็จสมบูรณ์ ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="6da54-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="6da54-169">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6da54-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6da54-170">เลือกคลังสินค้าที่คุณสร้างขึ้นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="6da54-171">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="6da54-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6da54-172">ภายใต้ **การจัดการสินค้าคงคลังและคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6da54-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="6da54-173">ตั้งค่า **สถานที่รับสินค้าเริ่มต้น** เป็นสถานที่เริ่มต้นที่สร้างไว้ด้านบน</span><span class="sxs-lookup"><span data-stu-id="6da54-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="6da54-174">เลือก **สถานที่ออกใช้เริ่มต้น** เป็นสถานที่เริ่มต้นที่สร้างไว้ด้านบน</span><span class="sxs-lookup"><span data-stu-id="6da54-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="6da54-175">ภายใต้ส่วน **ที่อยู่** ให้ป้อนที่อยู่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="6da54-176">ภายใต้ส่วน **การขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="6da54-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="6da54-177">ในกล่อง **สถานที่ส่งคืนสินค้าเริ่มต้น** ให้ป้อนสถานที่ส่งคืนที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="6da54-178">ตั้งค่า **ร้านค้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6da54-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="6da54-179">ตั้งค่า **น้ำหนัก** เป็น **1.00**</span><span class="sxs-lookup"><span data-stu-id="6da54-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="6da54-180">ในกล่อง **มิติการจัดเก็บ** ให้ป้อนสถานที่เริ่มต้นที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6da54-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="6da54-181">ภายใต้ส่วน **คลังสินค้า** ตั้งค่า **สินค้าคงคลังค่าลบที่มีอยู่จริง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6da54-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="6da54-182">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6da54-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6da54-183">รูปภาพต่อไปนี้แสดงรายละเอียดสำหรับคลังสินค้าที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6da54-183">The following image shows details for a configured warehouse.</span></span>

![ตัวอย่างของคลังสินค้าที่ตั้งค่าคอนฟิก](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="6da54-185">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6da54-185">Additional resources</span></span>

[<span data-ttu-id="6da54-186">ภาพรวมของการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6da54-186">Warehouse management overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[<span data-ttu-id="6da54-187">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="6da54-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6da54-188">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="6da54-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6da54-189">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="6da54-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="6da54-190">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6da54-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="6da54-191">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="6da54-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





