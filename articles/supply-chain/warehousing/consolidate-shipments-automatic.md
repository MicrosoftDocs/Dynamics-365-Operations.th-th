---
title: รวมบัญชีการจัดส่ง เมื่อมีการนำออกใช้ไปยังคลังสินค้าโดยใช้การนำใบสั่งขายออกใช้โดยอัตโนมัติ
description: หัวข้อนี้จะแสดงสถานการณ์จำลองที่ใบสั่งหลายใบถูกนำออกใช้ไปยังคลังสินค้าในกระบวนงานประจำงวดที่มีการนำออกใช้ไปยังคลังสินค้าแบบอัตโนมัติเดียวกัน
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac3ab25dc1355ee15e1209950ff0f3b3933b7095
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438826"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="b95f7-103">รวมบัญชีการจัดส่ง เมื่อมีการนำออกใช้ไปยังคลังสินค้าโดยใช้การนำใบสั่งขายออกใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b95f7-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b95f7-104">หัวข้อนี้จะแสดงสถานการณ์จำลองที่ใบสั่งหลายใบถูกนำออกใช้ไปยังคลังสินค้าในกระบวนงานประจำงวดที่มีการนำออกใช้ไปยังคลังสินค้าแบบอัตโนมัติเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b95f7-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="b95f7-105">ใบสั่งจะถูกรวมบัญชีไปยังการจัดส่งโดยอัตโนมัติ โดยยึดตามกฎที่ถูกกำหนดเป็นนโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b95f7-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="b95f7-106">ในระหว่างสถานการณ์จำลอง คุณจะสร้างชุดของใบสั่งขายและนำออกใช้ชุดแต่ละชุดไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b95f7-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="b95f7-107">จากนั้น คุณจะตรวจสอบการจัดส่งที่ถูกสร้างหรือถูกอัพเดตในระหว่างการรวมบัญชีการจัดส่ง โดยยึดตามนโยบายที่มีการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b95f7-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="b95f7-108">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b95f7-108">Make demo data available</span></span>

<span data-ttu-id="b95f7-109">สถานการณ์จำลองในหัวข้อนี้จะอ้างอิงค่าและเรกคอร์ดที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b95f7-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b95f7-110">ถ้าคุณต้องการใช้ค่าที่ระบุไว้ที่นี่เมื่อคุณทำแบบฝึกหัด ควรตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต และตั้งค่านิติบุคคลเป็น **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b95f7-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="b95f7-111">ตั้งค่านโยบายการรวมบัญชีการจัดส่งและตัวกรองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b95f7-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="b95f7-112">สถานการณ์จำลองที่อธิบายไว้ที่นี่จะถือว่าคุณได้เปิดใช้งานคุณลักษณะแล้ว ทำแบบฝึกหัดแล้วใน [ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง](configure-shipment-consolidation-policies.md) และสร้างนโยบายและเรกคอร์ดอื่นๆ แล้วซึ่งอธิบายไว้ที่นั่น</span><span class="sxs-lookup"><span data-stu-id="b95f7-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="b95f7-113">ตรวจสอบให้แน่ใจว่าคุณทำแบบฝึกหัดเหล่านั้น ก่อนที่คุณจะดำเนินการต่อด้วยสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="b95f7-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="b95f7-114">สร้างใบสั่งขายสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="b95f7-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="b95f7-115">เริ่มต้นด้วยการสร้างการรวบรวมของใบสั่งขายที่คุณสามารถทำงานด้วยได้</span><span class="sxs-lookup"><span data-stu-id="b95f7-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="b95f7-116">คุณต้องทำงานกับคลังสินค้าที่ถูกเปิดใช้งานสำหรับกระบวนการของคลังสินค้าขั้นสูง (WMS)</span><span class="sxs-lookup"><span data-stu-id="b95f7-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="b95f7-117">ยกเว้นว่าจะมีการกล่าวถึงคลังสินค้าอื่นอย่างชัดแจ้ง ต้องใช้คลังสินค้าเดียวกันสำหรับชุดของใบสั่งแต่ละชุดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b95f7-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="b95f7-118">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งขายทั้งหมด** และสร้างการรวบรวมของใบสั่งขายที่มีการตั้งค่าที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b95f7-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="b95f7-119">สร้างชุดใบสั่ง 1</span><span class="sxs-lookup"><span data-stu-id="b95f7-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="b95f7-120">ใบสั่งขาย 1-1</span><span class="sxs-lookup"><span data-stu-id="b95f7-120">Sales order 1-1</span></span>

1. <span data-ttu-id="b95f7-121">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-122">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b95f7-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b95f7-123">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b95f7-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b95f7-124">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-125">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-126">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="b95f7-127">ใบสั่งขาย 1-2</span><span class="sxs-lookup"><span data-stu-id="b95f7-127">Sales order 1-2</span></span>

1. <span data-ttu-id="b95f7-128">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-129">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b95f7-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b95f7-130">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b95f7-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b95f7-131">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-132">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-133">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="b95f7-134">ใบสั่งขาย 1-3</span><span class="sxs-lookup"><span data-stu-id="b95f7-134">Sales order 1-3</span></span>

1. <span data-ttu-id="b95f7-135">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-136">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b95f7-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b95f7-137">**โหมดการจัดส่ง:** *10*</span><span class="sxs-lookup"><span data-stu-id="b95f7-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="b95f7-138">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-139">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-140">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b95f7-141">เพิ่มรายการใบสั่งที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-142">**หมายเลขสินค้า:** *A0002* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-143">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b95f7-144">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b95f7-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="b95f7-145">สร้างชุดใบสั่ง 2</span><span class="sxs-lookup"><span data-stu-id="b95f7-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="b95f7-146">ใบสั่งขาย 2-1 และ 2-2</span><span class="sxs-lookup"><span data-stu-id="b95f7-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="b95f7-147">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b95f7-148">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b95f7-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="b95f7-149">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-150">**หมายเลขสินค้า:** *M9200* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ไวไฟ*)</span><span class="sxs-lookup"><span data-stu-id="b95f7-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="b95f7-151">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b95f7-152">เพิ่มรายการใบสั่งที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-153">**หมายเลขสินค้า:** *M9201* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ระเบิด*)</span><span class="sxs-lookup"><span data-stu-id="b95f7-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="b95f7-154">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b95f7-155">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b95f7-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="b95f7-156">สร้างชุดใบสั่ง 3</span><span class="sxs-lookup"><span data-stu-id="b95f7-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="b95f7-157">ใบสั่งขาย 3-1</span><span class="sxs-lookup"><span data-stu-id="b95f7-157">Sales order 3-1</span></span>

1. <span data-ttu-id="b95f7-158">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-159">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b95f7-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="b95f7-160">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-161">**หมายเลขสินค้า:** *M9200* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ไวไฟ*)</span><span class="sxs-lookup"><span data-stu-id="b95f7-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="b95f7-162">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b95f7-163">เพิ่มรายการใบสั่งที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-164">**หมายเลขสินค้า:** *M9201* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ระเบิด*)</span><span class="sxs-lookup"><span data-stu-id="b95f7-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="b95f7-165">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b95f7-166">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b95f7-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="b95f7-167">ใบสั่งนี้จะเหมือนกับใบสั่งสองใบที่คุณสร้างไว้สำหรับชุดใบสั่ง 2</span><span class="sxs-lookup"><span data-stu-id="b95f7-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="b95f7-168">อย่างไรก็ตาม มีการแสดงรายการเป็นชุดใบสั่งของตนเอง เนื่องจากคุณจะนำออกใช้โดยแยกต่างหากในภายหลังในสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="b95f7-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="b95f7-169">สร้างชุดใบสั่ง 4</span><span class="sxs-lookup"><span data-stu-id="b95f7-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="b95f7-170">ใบสั่งขาย 4-1</span><span class="sxs-lookup"><span data-stu-id="b95f7-170">Sales order 4-1</span></span>

1. <span data-ttu-id="b95f7-171">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-172">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b95f7-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b95f7-173">**การจัดหาวัตถุดิบของลูกค้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="b95f7-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b95f7-174">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-175">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-176">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="b95f7-177">สร้างชุดใบสั่ง 5</span><span class="sxs-lookup"><span data-stu-id="b95f7-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="b95f7-178">ใบสั่งขาย 5-1 และ 5-2</span><span class="sxs-lookup"><span data-stu-id="b95f7-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="b95f7-179">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b95f7-180">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b95f7-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b95f7-181">**การจัดหาวัตถุดิบของลูกค้า:** *2*</span><span class="sxs-lookup"><span data-stu-id="b95f7-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b95f7-182">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-183">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-184">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="b95f7-185">ใบสั่งขาย 5-3</span><span class="sxs-lookup"><span data-stu-id="b95f7-185">Sales order 5-3</span></span>

1. <span data-ttu-id="b95f7-186">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-187">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b95f7-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b95f7-188">**การจัดหาวัตถุดิบของลูกค้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="b95f7-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b95f7-189">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-190">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-191">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="b95f7-192">สร้างชุดใบสั่ง 6</span><span class="sxs-lookup"><span data-stu-id="b95f7-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="b95f7-193">ใบสั่งขาย 6-1 และ 6-2</span><span class="sxs-lookup"><span data-stu-id="b95f7-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="b95f7-194">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b95f7-195">**บัญชีลูกค้า:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="b95f7-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="b95f7-196">**การจัดหาวัตถุดิบของลูกค้า:** *2*</span><span class="sxs-lookup"><span data-stu-id="b95f7-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b95f7-197">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-198">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-199">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="b95f7-200">ใบสั่งขาย 6-3 และ 6-4</span><span class="sxs-lookup"><span data-stu-id="b95f7-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="b95f7-201">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b95f7-202">**บัญชีลูกค้า:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="b95f7-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="b95f7-203">**การจัดหาวัตถุดิบของลูกค้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="b95f7-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b95f7-204">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-205">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-206">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="b95f7-207">ใบสั่งขาย 6-5 และ 6-6</span><span class="sxs-lookup"><span data-stu-id="b95f7-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="b95f7-208">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b95f7-209">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b95f7-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b95f7-210">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="b95f7-210">**Site:** *6*</span></span>
    - <span data-ttu-id="b95f7-211">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="b95f7-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b95f7-212">**กลุ่ม:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="b95f7-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="b95f7-213">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-214">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-215">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="b95f7-216">ใบสั่งขาย 6-7 และ 6-8</span><span class="sxs-lookup"><span data-stu-id="b95f7-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="b95f7-217">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b95f7-218">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b95f7-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b95f7-219">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="b95f7-219">**Site:** *6*</span></span>
    - <span data-ttu-id="b95f7-220">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="b95f7-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b95f7-221">**กลุ่ม:** ปล่อยฟิลด์นี้ให้ว่าง</span><span class="sxs-lookup"><span data-stu-id="b95f7-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="b95f7-222">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b95f7-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b95f7-223">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="b95f7-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b95f7-224">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b95f7-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="b95f7-225">การนำใบสั่งขายออกใช้ไปยังคลังสินค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b95f7-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="b95f7-226">สำหรับใบสั่งขายแต่ละชุดที่คุณสร้างไว้ก่อนหน้านี้ คุณจะดำเนินการกระบวนงานให้เสร็จสมบูรณ์สำหรับการนำออกใช้ไปยังคลังสินค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b95f7-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="b95f7-227">ในกรณีแต่ละกรณี คุณจะดำเนินการ [กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน](#release-procedure) ที่ให้ไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="b95f7-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="b95f7-228">กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="b95f7-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="b95f7-229">สำหรับใบสั่งขายแต่ละชุดที่คุณสร้างไว้ก่อนหน้านี้ คุณจะดำเนินการกระบวนงานสามรายการที่ระบุไว้ในส่วนย่อยต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b95f7-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="b95f7-230">อัพเดตเท็มเพลตเวฟที่จะใช้ในระหว่างการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="b95f7-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="b95f7-231">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="b95f7-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b95f7-232">ตั้งค่าฟิลด์ **ชนิดเท็มเพลตเวฟ** เป็น *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="b95f7-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="b95f7-233">ค้นหาและเลือกเท็มเพลตเวฟที่สัมพันธ์กับคลังสินค้าที่คุณใช้ในชุดใบสั่งที่คุณสร้างขึ้นสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="b95f7-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="b95f7-234">ตัวอย่างเช่น ถ้าคุณใช้คลังสินค้า *24* ให้เลือกเท็มเพลตเวฟ **ค่าเริ่มต้นการจัดส่ง 24**</span><span class="sxs-lookup"><span data-stu-id="b95f7-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="b95f7-235">ถ้าคุณใช้คลังสินค้า *61* ให้เลือกเท็มเพลตเวฟ **การจัดส่ง 61**</span><span class="sxs-lookup"><span data-stu-id="b95f7-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="b95f7-236">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b95f7-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b95f7-237">ตั้งค่าตัวเลือก **ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า** เป็น *ไม่*</span><span class="sxs-lookup"><span data-stu-id="b95f7-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="b95f7-238">นำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b95f7-238">Release to the warehouse</span></span>

1. <span data-ttu-id="b95f7-239">ไปที่ **การจัดการคลังสินค้า \> นำออกใช้ไปยังคลังสินค้า \> การนำออกใช้โดยอัตโนมัติของใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="b95f7-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="b95f7-240">ตั้งค่าฟิลด์ **ปริมาณที่จะนำออกใช้** เป็น *ทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="b95f7-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="b95f7-241">บน FastTab **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="b95f7-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="b95f7-242">บนแท็บ **ช่วง** เลือก **เพิ่ม** เพื่อเพิ่มแถวที่มีการตั้งค่าต่อไปนี้ไปยังกริด:</span><span class="sxs-lookup"><span data-stu-id="b95f7-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="b95f7-243">**ตาราง:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="b95f7-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="b95f7-244">**ตารางสืบทอด:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="b95f7-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="b95f7-245">**ฟิลด์:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="b95f7-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="b95f7-246">**เงื่อนไข:** ให้ป้อนรายการที่คั่นด้วยเครื่องหมายจุลภาคของหมายเลขใบสั่งขายจากชุดใบสั่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b95f7-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="b95f7-247">เลือก **ตกลง** เพื่อบันทึกการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="b95f7-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="b95f7-248">เลือก **ตกลง** เพื่อเริ่มต้นกระบวนงาน *นำออกใช้ไปยังคลังสินค้าโดยอัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="b95f7-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="b95f7-249">ตรวจทานการจัดส่งที่ถูกสร้างขึ้นหรืออัพเดต</span><span class="sxs-lookup"><span data-stu-id="b95f7-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="b95f7-250">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b95f7-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="b95f7-251">ค้นหาและเลือกการจัดส่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b95f7-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="b95f7-252">ถ้านโยบายการรวมบัญชีถูกใช้เมื่อมีการสร้างหรืออัพเดตการจัดส่ง คุณควรจะเห็นในฟิลด์ **นโยบายการรวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="b95f7-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="b95f7-253">นำใบสั่งขายออกใช้จากชุดใบสั่ง 1</span><span class="sxs-lookup"><span data-stu-id="b95f7-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="b95f7-254">ทำตาม [กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน](#release-procedure) เพื่อนำใบสั่งขายออกใช้จากชุดใบสั่ง 1</span><span class="sxs-lookup"><span data-stu-id="b95f7-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="b95f7-255">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว คุณควรเห็นว่ามีการสร้างการจัดส่งสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="b95f7-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="b95f7-256">การจัดส่งแรกมีรายการสามรายการและถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *CustomerMode*</span><span class="sxs-lookup"><span data-stu-id="b95f7-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="b95f7-257">การจัดส่งที่สองซึ่งไม่ได้ใช้โหมดการขนส่ง *สายการบิน* ในการจัดส่ง ถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="b95f7-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="b95f7-258">นำใบสั่งขายออกใช้จากชุดใบสั่ง 2</span><span class="sxs-lookup"><span data-stu-id="b95f7-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="b95f7-259">ทำตาม [กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน](#release-procedure) เพื่อนำใบสั่งขายออกใช้จากชุดใบสั่ง 2</span><span class="sxs-lookup"><span data-stu-id="b95f7-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="b95f7-260">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว คุณควรเห็นว่ามีการสร้างการจัดส่งสามรายการ:</span><span class="sxs-lookup"><span data-stu-id="b95f7-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="b95f7-261">การจัดส่งสินค้าครั้งแรกมีสินค้า *ไวไฟ*</span><span class="sxs-lookup"><span data-stu-id="b95f7-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="b95f7-262">แต่ละรายการของการจัดส่งอื่นๆ สองรายการมีรายการหนึ่งรายการที่มีสินค้า *ระเบิด*</span><span class="sxs-lookup"><span data-stu-id="b95f7-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="b95f7-263">นำใบสั่งขายออกใช้จากชุดใบสั่ง 3</span><span class="sxs-lookup"><span data-stu-id="b95f7-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="b95f7-264">ทำตาม [กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน](#release-procedure) เพื่อนำใบสั่งขายออกใช้จากชุดใบสั่ง 3</span><span class="sxs-lookup"><span data-stu-id="b95f7-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="b95f7-265">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว คุณจะเห็นว่าการดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="b95f7-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="b95f7-266">การจัดส่งที่มีอยู่หนึ่งรายการ (การจัดส่งที่ถูกสร้างขึ้นเมื่อมีการนำชุดใบสั่ง 2 ออกใช้ไปยังคลังสินค้า) ถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b95f7-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="b95f7-267">มีการเพิ่มรายการที่มีสินค้า *ไวไฟ*</span><span class="sxs-lookup"><span data-stu-id="b95f7-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="b95f7-268">มีการสร้างการจัดส่งใหม่หนึ่งรายการที่ประกอบด้วยสินค้า *ระเบิด*</span><span class="sxs-lookup"><span data-stu-id="b95f7-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="b95f7-269">นำใบสั่งขายออกใช้จากชุดใบสั่ง 4</span><span class="sxs-lookup"><span data-stu-id="b95f7-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="b95f7-270">ทำตาม [กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน](#release-procedure) เพื่อนำใบสั่งขายออกใช้จากชุดใบสั่ง 4</span><span class="sxs-lookup"><span data-stu-id="b95f7-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="b95f7-271">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว คุณจะเห็นว่าการจัดส่งที่มีอยู่หนึ่งรายการ (ซึ่งฟิลด์ **การจัดหาวัตถุดิบของลูกค้า** ถูกตั้งค่าเป็น *1*) ถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b95f7-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="b95f7-272">รายการใหม่หนึ่งรายการถูกเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="b95f7-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="b95f7-273">นำใบสั่งขายออกใช้จากชุดใบสั่ง 5</span><span class="sxs-lookup"><span data-stu-id="b95f7-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="b95f7-274">ทำตาม [กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน](#release-procedure) เพื่อนำใบสั่งขายออกใช้จากชุดใบสั่ง 5</span><span class="sxs-lookup"><span data-stu-id="b95f7-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="b95f7-275">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว คุณจะเห็นว่าการดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="b95f7-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="b95f7-276">การจัดส่งที่มีอยู่หนึ่งรายการ (ซึ่งฟิลด์ **การจัดหาวัตถุดิบของลูกค้า** ถูกตั้งค่าเป็น *1*) ถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b95f7-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="b95f7-277">รายการจากใบสั่งขาย 5-3 (ซึ่งฟิลด์ **การจัดหาวัตถุดิบของลูกค้า** ถูกตั้งค่าเป็น *1*) ถูกเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="b95f7-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="b95f7-278">มีการสร้างการจัดส่งสินค้าใหม่หนึ่งรายการ ที่ซึ่งมีการจัดกลุ่มรายการจากใบสั่งขาย 5-1 และ 5-2 เป็นการจัดส่งหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="b95f7-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="b95f7-279">นำใบสั่งขายออกใช้จากชุดใบสั่ง 6</span><span class="sxs-lookup"><span data-stu-id="b95f7-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="b95f7-280">ทำตาม [กระบวนงานการนำออกใช้ไปยังคลังสินค้าพื้นฐาน](#release-procedure) เพื่อนำใบสั่งขายออกใช้จากชุดใบสั่ง 6</span><span class="sxs-lookup"><span data-stu-id="b95f7-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="b95f7-281">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว คุณควรเห็นว่ามีการสร้างการจัดส่งสี่รายการ:</span><span class="sxs-lookup"><span data-stu-id="b95f7-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="b95f7-282">รายการจากใบสั่งสองใบสำหรับลูกค้า *US-003* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="b95f7-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b95f7-283">รายการจากใบสั่งสองใบสำหรับลูกค้า *US-004* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="b95f7-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b95f7-284">รายการจากใบสั่งขาย 6-5 และ 6-6 สำหรับลูกค้า *US-007* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="b95f7-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b95f7-285">รายการจากใบสั่งขาย 6-7 และ 6-8 สำหรับลูกค้า *US-007* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *CrossOrder*</span><span class="sxs-lookup"><span data-stu-id="b95f7-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b95f7-286">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b95f7-286">Additional resources</span></span>

- [<span data-ttu-id="b95f7-287">นโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b95f7-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="b95f7-288">ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b95f7-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
