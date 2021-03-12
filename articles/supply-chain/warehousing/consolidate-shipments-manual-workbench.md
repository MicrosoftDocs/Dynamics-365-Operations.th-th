---
title: รวมบัญชีการจัดส่งโดยใช้เวิร์กเบนช์การรวมบัญชีการจัดส่ง
description: หัวข้อนี้แสดงสถานการณ์จำลองที่ใบสั่งหลายใบจะถูกนำออกใช้ไปยังคลังสินค้า และจากนั้น ถูกรวมบัญชีลงในการจัดส่งในภายหลังโดยใช้เวิร์กเบนช์หน้ารวมบัญชีการจัดส่ง
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9d0a2671e18603f701d343a4150128a04c626952
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963396"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="7dd60-103">รวมบัญชีการจัดส่งโดยใช้เวิร์กเบนช์การรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dd60-104">หัวข้อนี้แสดงสถานการณ์จำลองที่ใบสั่งหลายใบจะถูกนำออกใช้ไปยังคลังสินค้า และจากนั้น ถูกรวมบัญชีลงในการจัดส่งในภายหลังโดยใช้เวิร์กเบนช์หน้ารวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="7dd60-105">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7dd60-105">Make demo data available</span></span>

<span data-ttu-id="7dd60-106">สถานการณ์จำลองในหัวข้อนี้จะอ้างอิงค่าและเรกคอร์ดที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7dd60-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="7dd60-107">ถ้าคุณต้องการใช้ค่าที่ระบุไว้ที่นี่เมื่อคุณทำแบบฝึกหัด ควรตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต และตั้งค่านิติบุคคลเป็น **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7dd60-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="7dd60-108">ตั้งค่านโยบายการรวมบัญชีการจัดส่งและตัวกรองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7dd60-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="7dd60-109">สถานการณ์จำลองที่อธิบายไว้ที่นี่จะถือว่าคุณได้เปิดใช้งานคุณลักษณะแล้ว ทำแบบฝึกหัดแล้วใน [ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง](configure-shipment-consolidation-policies.md) และสร้างนโยบายและเรกคอร์ดอื่นๆ แล้วซึ่งอธิบายไว้ที่นั่น</span><span class="sxs-lookup"><span data-stu-id="7dd60-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="7dd60-110">ตรวจสอบให้แน่ใจว่าคุณทำแบบฝึกหัดเหล่านั้น ก่อนที่คุณจะดำเนินการต่อด้วยสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="7dd60-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="7dd60-111">เปิดคุณลักษณะการรวมบัญชีการจัดส่งด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="7dd60-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="7dd60-112">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การรวมบัญชีการจัดส่งด้วยตนเอง* คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="7dd60-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="7dd60-113">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7dd60-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="7dd60-114">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7dd60-115">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="7dd60-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7dd60-116">**ชื่อคุณลักษณะ:** *การรวมบัญชีการจัดส่งด้วยตนเอง*</span><span class="sxs-lookup"><span data-stu-id="7dd60-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="7dd60-117">ตามที่ระบุไว้ใน [ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง](configure-shipment-consolidation-policies.md) คุณยังต้องเปิดใช้งานคุณลักษณะ *รวมบัญชีการจัดส่ง* ก่อนที่คุณจะสามารถสร้างนโยบายได้</span><span class="sxs-lookup"><span data-stu-id="7dd60-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="7dd60-118">อย่างไรก็ตาม คุณควรดำเนินการขั้นตอนนั้นเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="7dd60-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="7dd60-119">สร้างใบสั่งขายสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="7dd60-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="7dd60-120">เริ่มต้นด้วยการสร้างการรวบรวมของใบสั่งขายที่คุณสามารถทำงานด้วยได้</span><span class="sxs-lookup"><span data-stu-id="7dd60-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="7dd60-121">คุณต้องทำงานกับคลังสินค้าที่ถูกเปิดใช้งานสำหรับกระบวนการของคลังสินค้าขั้นสูง (WMS)</span><span class="sxs-lookup"><span data-stu-id="7dd60-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="7dd60-122">ยกเว้นว่าจะมีการกล่าวถึงคลังสินค้าอื่นอย่างชัดแจ้ง ต้องใช้คลังสินค้าเดียวกันสำหรับชุดของใบสั่งแต่ละชุดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7dd60-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="7dd60-123">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งขายทั้งหมด** และสร้างการรวบรวมของใบสั่งขายที่มีการตั้งค่าที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7dd60-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="7dd60-124">สร้างชุดใบสั่ง 1</span><span class="sxs-lookup"><span data-stu-id="7dd60-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="7dd60-125">ใบสั่งขาย 1-1 และ 1-2</span><span class="sxs-lookup"><span data-stu-id="7dd60-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="7dd60-126">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-127">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7dd60-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7dd60-128">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7dd60-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7dd60-129">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-130">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-131">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-132">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="7dd60-133">ใบสั่งขาย 1-3</span><span class="sxs-lookup"><span data-stu-id="7dd60-133">Sales order 1-3</span></span>

1. <span data-ttu-id="7dd60-134">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-135">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7dd60-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7dd60-136">**โหมดการจัดส่ง:** *10*</span><span class="sxs-lookup"><span data-stu-id="7dd60-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="7dd60-137">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-138">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-139">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-140">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="7dd60-141">เพิ่มรายการใบสั่งที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-142">**หมายเลขสินค้า:** *A0002* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-143">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="7dd60-144">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7dd60-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7dd60-145">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่งที่สอง</span><span class="sxs-lookup"><span data-stu-id="7dd60-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="7dd60-146">สร้างชุดใบสั่ง 2</span><span class="sxs-lookup"><span data-stu-id="7dd60-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="7dd60-147">ใบสั่งขาย 2-1 และ 2-2</span><span class="sxs-lookup"><span data-stu-id="7dd60-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="7dd60-148">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-149">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="7dd60-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="7dd60-150">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7dd60-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7dd60-151">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-152">**หมายเลขสินค้า:** *M9200* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ไวไฟ*)</span><span class="sxs-lookup"><span data-stu-id="7dd60-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="7dd60-153">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-154">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="7dd60-155">เพิ่มรายการใบสั่งที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-156">**หมายเลขสินค้า:** *M9201* (สินค้าที่มีการตั้งค่าตัวกรอง **รหัส 4** เป็น *ระเบิด*)</span><span class="sxs-lookup"><span data-stu-id="7dd60-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="7dd60-157">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="7dd60-158">**โหมดการจัดส่ง:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7dd60-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7dd60-159">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่งที่สอง</span><span class="sxs-lookup"><span data-stu-id="7dd60-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="7dd60-160">สร้างชุดใบสั่ง 3</span><span class="sxs-lookup"><span data-stu-id="7dd60-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="7dd60-161">ใบสั่งขาย 3-1 และ 3-2</span><span class="sxs-lookup"><span data-stu-id="7dd60-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="7dd60-162">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-163">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7dd60-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7dd60-164">**การจัดหาวัตถุดิบของลูกค้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="7dd60-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="7dd60-165">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-166">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-167">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-168">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="7dd60-169">ใบสั่งขาย 3-3 และ 3-4</span><span class="sxs-lookup"><span data-stu-id="7dd60-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="7dd60-170">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-171">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7dd60-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7dd60-172">**การจัดหาวัตถุดิบของลูกค้า:** *2*</span><span class="sxs-lookup"><span data-stu-id="7dd60-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="7dd60-173">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-174">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-175">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-176">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="7dd60-177">สร้างชุดใบสั่ง 4</span><span class="sxs-lookup"><span data-stu-id="7dd60-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="7dd60-178">ใบสั่งขาย 4-1 และ 4-2</span><span class="sxs-lookup"><span data-stu-id="7dd60-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="7dd60-179">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-180">**บัญชีลูกค้า:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="7dd60-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="7dd60-181">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-182">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-183">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-184">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="7dd60-185">ใบสั่งขาย 4-3 และ 4-4</span><span class="sxs-lookup"><span data-stu-id="7dd60-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="7dd60-186">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-187">**บัญชีลูกค้า:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="7dd60-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="7dd60-188">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-189">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-190">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-191">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="7dd60-192">ใบสั่งขาย 4-5 และ 4-6</span><span class="sxs-lookup"><span data-stu-id="7dd60-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="7dd60-193">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-194">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="7dd60-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="7dd60-195">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="7dd60-195">**Site:** *6*</span></span>
    - <span data-ttu-id="7dd60-196">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="7dd60-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="7dd60-197">**กลุ่ม:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="7dd60-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="7dd60-198">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-199">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-200">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-201">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="7dd60-202">ใบสั่งขาย 4-7 และ 4-8</span><span class="sxs-lookup"><span data-stu-id="7dd60-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="7dd60-203">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7dd60-204">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="7dd60-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="7dd60-205">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="7dd60-205">**Site:** *6*</span></span>
    - <span data-ttu-id="7dd60-206">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="7dd60-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="7dd60-207">**กลุ่ม:** ปล่อยฟิลด์นี้ให้ว่าง</span><span class="sxs-lookup"><span data-stu-id="7dd60-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="7dd60-208">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7dd60-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7dd60-209">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="7dd60-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7dd60-210">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7dd60-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7dd60-211">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="7dd60-212">นำใบสั่งออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7dd60-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="7dd60-213">ทำตามขั้นตอนต่อไปนี้เพื่อนำออกใช้ใบสั่งขายแต่ละใบที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ไปที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7dd60-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="7dd60-214">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7dd60-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7dd60-215">ค้นหาและเลือกใบสั่งขายที่จะนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="7dd60-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="7dd60-216">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** เลือก **การดำเนินการ \> นำออกใช้ไปยังคลังสินค้า** เพื่อนำออกใช้ใบสั่งขายที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7dd60-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="7dd60-217">ทำซ้ำกระบวนงานนี้สำหรับใบสั่งขายอื่นทั้งหมดที่คุณสร้างสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="7dd60-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="7dd60-218">รวมบัญชีการจัดส่งโดยใช้เวิร์กเบนช์การรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="7dd60-219">ไปที่ **การจัดการคลังสินค้า \> นำออกใช้ไปยังคลังสินค้า \> เวิร์กเบนช์การรวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="7dd60-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="7dd60-220">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="7dd60-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="7dd60-221">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวที่มีการตั้งค่าต่อไปนี้ไปยังกริด:</span><span class="sxs-lookup"><span data-stu-id="7dd60-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="7dd60-222">**ตาราง:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="7dd60-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="7dd60-223">**ฟิลด์:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="7dd60-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="7dd60-224">**เงื่อนไข:** ให้ป้อนรายการที่คั่นด้วยเครื่องหมายจุลภาคของหมายเลขใบสั่งขายสำหรับชุดใบสั่งแต่ละชุดที่คุณสร้างสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="7dd60-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="7dd60-225">เลือก **ตกลง** เพื่อบันทึกการสอบถามของคุณและปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="7dd60-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="7dd60-226">บนบานหน้าต่างการดำเนินการ เลือก **รวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="7dd60-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="7dd60-227">เลือกการจัดส่งทั้งหมด และจากนั้น บนบานหน้าต่างการดำเนินการ ให้เลือก **รวมบัญชี**</span><span class="sxs-lookup"><span data-stu-id="7dd60-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="7dd60-228">ตรวจสอบความถูกต้องของการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-228">Verify the shipments</span></span>

<span data-ttu-id="7dd60-229">กระบวนงานต่อไปนี้ช่วยให้คุณสามารถตรวจสอบความถูกต้องของการจัดส่งที่ถูกสร้างขึ้นหรือถูกอัพเดตเนื่องจากการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="7dd60-230">ใช้เพื่อตรวจทานชุดใบสั่งแต่ละชุดที่คุณสร้างสำหรับสถานการณ์จำลองนี้ และจากนั้น ตรวจสอบความถูกต้องของส่วนย่อยที่ทำตามเพื่อตรวจสอบให้แน่ใจว่าคุณได้รับผลลัพธ์ที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="7dd60-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="7dd60-231">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7dd60-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="7dd60-232">ค้นหาและเลือกการจัดส่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7dd60-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="7dd60-233">ถ้านโยบายการรวมบัญชีถูกใช้เมื่อมีการสร้างหรืออัพเดตการจัดส่ง คุณควรจะเห็นในฟิลด์ **นโยบายการรวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="7dd60-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="7dd60-234">การจัดส่งที่เกี่ยวข้องสำหรับชุดใบสั่ง 1</span><span class="sxs-lookup"><span data-stu-id="7dd60-234">Related shipments for order set 1</span></span>

<span data-ttu-id="7dd60-235">ควรมีการสร้างการจัดส่งสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="7dd60-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="7dd60-236">การจัดส่งแรกมีรายการสามรายการและถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *CustomerMode*</span><span class="sxs-lookup"><span data-stu-id="7dd60-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="7dd60-237">การจัดส่งที่สองซึ่งไม่ได้ใช้โหมดการขนส่ง *สายการบิน* ในการจัดส่ง ถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="7dd60-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="7dd60-238">การจัดส่งที่เกี่ยวข้องสำหรับชุดใบสั่ง 2</span><span class="sxs-lookup"><span data-stu-id="7dd60-238">Related shipments for order set 2</span></span>

<span data-ttu-id="7dd60-239">ควรมีการสร้างการจัดส่งสามรายการ:</span><span class="sxs-lookup"><span data-stu-id="7dd60-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="7dd60-240">การจัดส่งสินค้าครั้งแรกมีสินค้า *ไวไฟ*</span><span class="sxs-lookup"><span data-stu-id="7dd60-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="7dd60-241">แต่ละรายการของการจัดส่งอื่นๆ สองรายการมีรายการหนึ่งรายการที่มีสินค้า *ระเบิด*</span><span class="sxs-lookup"><span data-stu-id="7dd60-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="7dd60-242">การจัดส่งที่เกี่ยวข้องสำหรับชุดใบสั่ง 3</span><span class="sxs-lookup"><span data-stu-id="7dd60-242">Related shipments for order set 3</span></span>

<span data-ttu-id="7dd60-243">ควรมีการสร้างการจัดส่งสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="7dd60-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="7dd60-244">การจัดส่งแรกมีรายการใบสั่งจากใบสั่งขายที่ซึ่งฟิลด์ **การจัดหาวัตถุดิบของลูกค้า** ถูกตั้งค่าเป็น *1*</span><span class="sxs-lookup"><span data-stu-id="7dd60-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="7dd60-245">การจัดส่งที่สองมีรายการใบสั่งจากใบสั่งขายที่ซึ่งฟิลด์ **การจัดหาวัตถุดิบของลูกค้า** ถูกตั้งค่าเป็น *2*</span><span class="sxs-lookup"><span data-stu-id="7dd60-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="7dd60-246">การจัดส่งที่เกี่ยวข้องสำหรับชุดใบสั่ง 4</span><span class="sxs-lookup"><span data-stu-id="7dd60-246">Related shipments for order set 4</span></span>

<span data-ttu-id="7dd60-247">ควรมีการสร้างการจัดส่งสี่รายการ:</span><span class="sxs-lookup"><span data-stu-id="7dd60-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="7dd60-248">รายการจากใบสั่งสองใบสำหรับลูกค้า *US-003* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="7dd60-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7dd60-249">รายการจากใบสั่งสองใบสำหรับลูกค้า *US-004* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="7dd60-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7dd60-250">รายการจากใบสั่งขาย 4-5 และ 4-6 สำหรับลูกค้า *US-007* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *กลุ่มใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="7dd60-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7dd60-251">รายการจากใบสั่งขาย 4-7 และ 4-8 สำหรับลูกค้า *US-007* ถูกจัดกลุ่มเป็นการจัดส่งหนึ่งรายการ โดยใช้นโยบายการรวมบัญชีการจัดส่งของ *CrossOrder*</span><span class="sxs-lookup"><span data-stu-id="7dd60-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dd60-252">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7dd60-252">Additional resources</span></span>

- [<span data-ttu-id="7dd60-253">นโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="7dd60-254">ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7dd60-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
