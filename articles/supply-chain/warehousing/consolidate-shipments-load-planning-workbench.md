---
title: รวมบัญชีการจัดส่งโดยใช้การนำออกใช้ไปยังคลังสินค้าจากเวิร์กเบนช์การวางแผนการบรรทุก
description: หัวข้อนี้แสดงสถานการณ์จำลองที่ใบสั่งหลายใบจะถูกนำออกใช้ไปยังคลังสินค้าในจำนวนงานในศูนย์การผลิตเดียวกัน และจากนั้น ถูกรวมบัญชีลงในการจัดส่งโดยอัตโนมัติ
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2fd13c2ceb8843b79b9dbc87acf77f219f0244f5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242264"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="88939-103">รวมบัญชีการจัดส่งโดยใช้การนำออกใช้ไปยังคลังสินค้าจากเวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="88939-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88939-104">หัวข้อนี้แสดงสถานการณ์จำลองที่ใบสั่งหลายใบจะถูกนำออกใช้ไปยังคลังสินค้าในจำนวนงานในศูนย์การผลิตเดียวกัน และจากนั้น ถูกรวมบัญชีลงในการจัดส่งโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="88939-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="88939-105">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="88939-105">Make demo data available</span></span>

<span data-ttu-id="88939-106">สถานการณ์จำลองในหัวข้อนี้จะอ้างอิงค่าและเรกคอร์ดที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="88939-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="88939-107">ถ้าคุณต้องการใช้ค่าที่ระบุไว้ที่นี่เมื่อคุณทำแบบฝึกหัด ควรตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต และตั้งค่านิติบุคคลเป็น **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="88939-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="88939-108">ตั้งค่านโยบายการรวมบัญชีการจัดส่งและตัวกรองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="88939-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="88939-109">สถานการณ์จำลองที่อธิบายไว้ที่นี่จะถือว่าคุณได้เปิดใช้งานคุณลักษณะแล้ว ทำแบบฝึกหัดแล้วใน [ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง](configure-shipment-consolidation-policies.md) และสร้างนโยบายและเรกคอร์ดอื่นๆ แล้วซึ่งอธิบายไว้ที่นั่น</span><span class="sxs-lookup"><span data-stu-id="88939-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="88939-110">ตรวจสอบให้แน่ใจว่าคุณทำแบบฝึกหัดเหล่านั้น ก่อนที่คุณจะดำเนินการต่อด้วยสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="88939-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="88939-111">สร้างใบสั่งขายสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="88939-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="88939-112">เริ่มต้นด้วยการสร้างการรวบรวมของใบสั่งขายที่คุณสามารถทำงานด้วยได้</span><span class="sxs-lookup"><span data-stu-id="88939-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="88939-113">คุณต้องทำงานกับคลังสินค้าที่ถูกเปิดใช้งานสำหรับกระบวนการของคลังสินค้าขั้นสูง (WMS)</span><span class="sxs-lookup"><span data-stu-id="88939-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="88939-114">ยกเว้นว่าจะมีการกล่าวถึงคลังสินค้าอื่นอย่างชัดแจ้ง ต้องใช้คลังสินค้าเดียวกันสำหรับชุดของใบสั่งแต่ละชุดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="88939-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="88939-115">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งขายทั้งหมด** และสร้างการรวบรวมของใบสั่งขายที่มีการตั้งค่าที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="88939-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="88939-116">สร้างชุดใบสั่ง 1</span><span class="sxs-lookup"><span data-stu-id="88939-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="88939-117">ใบสั่งขาย 1-1</span><span class="sxs-lookup"><span data-stu-id="88939-117">Sales order 1-1</span></span>

1. <span data-ttu-id="88939-118">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="88939-119">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="88939-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="88939-120">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="88939-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="88939-121">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-122">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-123">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-124">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="88939-125">ใบสั่งขาย 1-2</span><span class="sxs-lookup"><span data-stu-id="88939-125">Sales order 1-2</span></span>

1. <span data-ttu-id="88939-126">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="88939-127">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="88939-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="88939-128">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="88939-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="88939-129">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-130">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-131">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-132">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="88939-133">ใบสั่งขาย 1-3</span><span class="sxs-lookup"><span data-stu-id="88939-133">Sales order 1-3</span></span>

1. <span data-ttu-id="88939-134">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="88939-135">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="88939-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="88939-136">**โหมดการจัดส่ง:** *10*</span><span class="sxs-lookup"><span data-stu-id="88939-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="88939-137">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-138">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-139">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-140">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="88939-141">เพิ่มรายการใบสั่งที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-142">**หมายเลขสินค้า:** *A0002* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-143">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="88939-144">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="88939-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="88939-145">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่งที่สอง</span><span class="sxs-lookup"><span data-stu-id="88939-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="88939-146">สร้างชุดใบสั่ง 2</span><span class="sxs-lookup"><span data-stu-id="88939-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="88939-147">ใบสั่งขาย 2-1 และ 2-2</span><span class="sxs-lookup"><span data-stu-id="88939-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="88939-148">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88939-149">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="88939-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="88939-150">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-151">**หมายเลขสินค้า:** *M9200* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ไวไฟ*)</span><span class="sxs-lookup"><span data-stu-id="88939-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="88939-152">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-153">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="88939-154">เพิ่มรายการใบสั่งที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-155">**หมายเลขสินค้า:** *M9201* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ระเบิด*)</span><span class="sxs-lookup"><span data-stu-id="88939-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="88939-156">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="88939-157">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="88939-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="88939-158">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่งที่สอง</span><span class="sxs-lookup"><span data-stu-id="88939-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="88939-159">สร้างชุดใบสั่ง 3</span><span class="sxs-lookup"><span data-stu-id="88939-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="88939-160">ใบสั่งขาย 3-1 และ 3-2</span><span class="sxs-lookup"><span data-stu-id="88939-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="88939-161">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88939-162">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="88939-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="88939-163">**การจัดหาวัตถุดิบของลูกค้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="88939-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="88939-164">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-165">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-166">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-167">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="88939-168">ใบสั่งขาย 3-3 และ 3-4</span><span class="sxs-lookup"><span data-stu-id="88939-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="88939-169">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88939-170">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="88939-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="88939-171">**การจัดหาวัตถุดิบของลูกค้า:** *2*</span><span class="sxs-lookup"><span data-stu-id="88939-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="88939-172">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-173">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-174">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-175">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="88939-176">สร้างชุดใบสั่ง 4</span><span class="sxs-lookup"><span data-stu-id="88939-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="88939-177">ใบสั่งขาย 4-1 และ 4-2</span><span class="sxs-lookup"><span data-stu-id="88939-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="88939-178">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88939-179">**บัญชีลูกค้า:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="88939-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="88939-180">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-181">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-182">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-183">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="88939-184">ใบสั่งขาย 4-3 และ 4-4</span><span class="sxs-lookup"><span data-stu-id="88939-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="88939-185">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88939-186">**บัญชีลูกค้า:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="88939-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="88939-187">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-188">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-189">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-190">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="88939-191">ใบสั่งขาย 4-5 และ 4-6</span><span class="sxs-lookup"><span data-stu-id="88939-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="88939-192">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88939-193">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="88939-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="88939-194">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="88939-194">**Site:** *6*</span></span>
    - <span data-ttu-id="88939-195">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="88939-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="88939-196">**กลุ่ม:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="88939-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="88939-197">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-198">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-199">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-200">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="88939-201">ใบสั่งขาย 4-7 และ 4-8</span><span class="sxs-lookup"><span data-stu-id="88939-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="88939-202">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="88939-203">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="88939-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="88939-204">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="88939-204">**Site:** *6*</span></span>
    - <span data-ttu-id="88939-205">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="88939-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="88939-206">**กลุ่ม:** ปล่อยฟิลด์นี้ให้ว่าง</span><span class="sxs-lookup"><span data-stu-id="88939-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="88939-207">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88939-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="88939-208">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="88939-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="88939-209">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="88939-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="88939-210">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="88939-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="88939-211">ใช้เวิร์กเบนช์การวางแผนการบรรทุกเพื่อสร้างจำนวนงานในศูนย์การผลิตและนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="88939-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="88939-212">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างจำนวนงานในศูนย์การผลิตสำหรับชุดใบสั่งขายแต่ละชุดที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้และนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="88939-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="88939-213">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> เวิร์กเบนช์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="88939-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="88939-214">บนแท็บ **รายการขาย** ให้ค้นหาและเลือกรายการใบสั่งขายทั้งหมดจากหนึ่งในชุดใบสั่งที่คุณสร้างขึ้นสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="88939-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="88939-215">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดหาและความต้องการ** ให้เลือก **เพิ่ม \> ไปยังจำนวนงานในศูนย์การผลิตใหม่** เพื่อเพิ่มรายการใบสั่งที่เลือกไปยังจำนวนงานในศูนย์การผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="88939-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="88939-216">ในกล่องโต้ตอบ **การกำหนดเท็มเพลตจำนวนงานในศูนย์การผลิต** ในฟิลด์ **รหัสเท็มเพลตจำนวนงานในศูนย์การผลิต** ให้เลือกเท็มเพลตจำนวนงานในศูนย์การผลิต เช่น *เท็มเพลตจำนวนงานในศูนย์การผลิต Stnd*</span><span class="sxs-lookup"><span data-stu-id="88939-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="88939-217">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="88939-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="88939-218">ในส่วน **จำนวนงานในศูนย์การผลิต** และเลือกจำนวนงานในศูนย์การผลิตที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="88939-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="88939-219">เลือก **นำออกใช้ \> นำออกใช้ไปยังคลังสินค้า** เพื่อนำจำนวนงานในศูนย์การผลิตที่เลือกออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="88939-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="88939-220">ทำซ้ำกระบวนงานนี้สำหรับชุดใบสั่งขายอื่นๆ อีกสามชุดที่คุณสร้างสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="88939-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="88939-221">ตรวจสอบความถูกต้องของการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88939-221">Verify the shipments</span></span>

<span data-ttu-id="88939-222">กระบวนงานต่อไปนี้ช่วยให้คุณสามารถตรวจสอบความถูกต้องของการจัดส่งที่ถูกสร้างขึ้นหรือถูกอัพเดตเนื่องจากการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88939-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="88939-223">ใช้เพื่อตรวจทานชุดใบสั่งแต่ละชุดที่คุณสร้างสำหรับสถานการณ์จำลองนี้ และจากนั้น ตรวจสอบความถูกต้องของส่วนย่อยที่ทำตามเพื่อตรวจสอบให้แน่ใจว่าคุณได้รับผลลัพธ์ที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="88939-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="88939-224">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="88939-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="88939-225">ค้นหาและเลือกการจัดส่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="88939-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="88939-226">ถ้านโยบายการรวมบัญชีถูกใช้เมื่อมีการสร้างหรืออัพเดตการจัดส่ง คุณควรจะเห็นในฟิลด์ **นโยบายการรวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="88939-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="88939-227">นำชุดใบสั่ง 1 ออกใช้ในจำนวนงานในศูนย์การผลิตหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="88939-227">Release order set 1 in one load</span></span>

<span data-ttu-id="88939-228">ควรมีการสร้างการจัดส่งสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="88939-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="88939-229">การจัดส่งแรกมีรายการสามรายการและถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *CustomerMode*</span><span class="sxs-lookup"><span data-stu-id="88939-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="88939-230">การจัดส่งที่สองซึ่งไม่ได้ใช้โหมดการขนส่ง *สายการบิน* ในการจัดส่ง ถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="88939-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="88939-231">นำชุดใบสั่ง 2 ออกใช้ในจำนวนงานในศูนย์การผลิตหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="88939-231">Release order set 2 in one load</span></span>

<span data-ttu-id="88939-232">ควรมีการสร้างการจัดส่งสามรายการ:</span><span class="sxs-lookup"><span data-stu-id="88939-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="88939-233">การจัดส่งสินค้าครั้งแรกมีสินค้า *ไวไฟ*</span><span class="sxs-lookup"><span data-stu-id="88939-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="88939-234">แต่ละรายการของการจัดส่งอื่นๆ สองรายการมีรายการหนึ่งรายการที่มีสินค้า *ระเบิด*</span><span class="sxs-lookup"><span data-stu-id="88939-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="88939-235">นำชุดใบสั่ง 3 ออกใช้ในจำนวนงานในศูนย์การผลิตหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="88939-235">Release order set 3 in one load</span></span>

<span data-ttu-id="88939-236">ควรมีการสร้างการจัดส่งสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="88939-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="88939-237">การจัดส่งแรกมีรายการใบสั่งจากใบสั่งขายที่ซึ่งฟิลด์ **การจัดหาวัตถุดิบของลูกค้า** ถูกตั้งค่าเป็น *1*</span><span class="sxs-lookup"><span data-stu-id="88939-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="88939-238">การจัดส่งที่สองมีรายการใบสั่งจากใบสั่งขายที่ซึ่งฟิลด์ **การจัดหาวัตถุดิบของลูกค้า** ถูกตั้งค่าเป็น *2*</span><span class="sxs-lookup"><span data-stu-id="88939-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="88939-239">นำชุดใบสั่ง 4 ออกใช้ในจำนวนงานในศูนย์การผลิตหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="88939-239">Release order set 4 in one load</span></span>

<span data-ttu-id="88939-240">ควรมีการสร้างการจัดส่งสี่รายการ:</span><span class="sxs-lookup"><span data-stu-id="88939-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="88939-241">รายการจากใบสั่งสองใบสำหรับบัญชีลูกค้า *US-003* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="88939-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="88939-242">รายการจากใบสั่งสองใบสำหรับบัญชีลูกค้า *US-004* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="88939-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="88939-243">รายการจากใบสั่งขาย 4-5 และ 4-6 สำหรับบัญชีลูกค้า *US-007* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="88939-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="88939-244">รายการจากใบสั่งขาย 4-7 และ 4-8 สำหรับบัญชีลูกค้า *US-007* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *CrossOrder*</span><span class="sxs-lookup"><span data-stu-id="88939-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88939-245">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="88939-245">Additional resources</span></span>

- [<span data-ttu-id="88939-246">นโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88939-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="88939-247">ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88939-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]