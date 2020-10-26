---
title: รวมบัญชีการจัดส่งด้วยตนเองโดยใช้หน้ารวมบัญชีการจัดส่ง
description: หัวข้อนี้แสดงสถานการณ์จำลองที่ใบสั่งหลายใบจะถูกนำออกใช้ไปยังคลังสินค้า และจากนั้น ถูกรวมบัญชีในภายหลังโดยใช้หน้ารวมบัญชีการจัดส่ง
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac60bef797d8e0bbe0d20f1585d5c3c0163f8788
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986803"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="606e1-103">รวมบัญชีการจัดส่งด้วยตนเองโดยใช้หน้ารวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="606e1-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="606e1-104">หัวข้อนี้แสดงสถานการณ์จำลองที่ซึ่งใบสั่งหลายใบถูกนำออกใช้ไปยังคลังสินค้า และจากนั้น ถูกรวมบัญชีในภายหลังโดยใช้หน้า **รวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="606e1-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="606e1-105">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="606e1-105">Make demo data available</span></span>

<span data-ttu-id="606e1-106">สถานการณ์จำลองในหัวข้อนี้จะอ้างอิงค่าและเรกคอร์ดที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="606e1-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="606e1-107">ถ้าคุณต้องการใช้ค่าที่ระบุไว้ที่นี่เมื่อคุณทำแบบฝึกหัด ควรตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต และตั้งค่านิติบุคคลเป็น **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="606e1-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="606e1-108">ตั้งค่านโยบายการรวมบัญชีการจัดส่งและตัวกรองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="606e1-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="606e1-109">สถานการณ์จำลองที่อธิบายไว้ที่นี่จะถือว่าคุณได้เปิดใช้งานคุณลักษณะแล้ว ทำแบบฝึกหัดแล้วใน [ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง](configure-shipment-consolidation-policies.md) และสร้างนโยบายและเรกคอร์ดอื่นๆ แล้วซึ่งอธิบายไว้ที่นั่น</span><span class="sxs-lookup"><span data-stu-id="606e1-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="606e1-110">ตรวจสอบให้แน่ใจว่าคุณทำแบบฝึกหัดเหล่านั้น ก่อนที่คุณจะดำเนินการต่อด้วยสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="606e1-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="606e1-111">สร้างใบสั่งขายสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="606e1-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="606e1-112">เริ่มต้นด้วยการสร้างการรวบรวมของใบสั่งขายที่คุณสามารถทำงานด้วยได้</span><span class="sxs-lookup"><span data-stu-id="606e1-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="606e1-113">คุณต้องทำงานกับคลังสินค้าที่ถูกเปิดใช้งานสำหรับกระบวนการของคลังสินค้าขั้นสูง (WMS)</span><span class="sxs-lookup"><span data-stu-id="606e1-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="606e1-114">ยกเว้นว่าจะมีการกล่าวถึงคลังสินค้าอื่นอย่างชัดแจ้ง ต้องใช้คลังสินค้าเดียวกันสำหรับชุดของใบสั่งแต่ละชุดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="606e1-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="606e1-115">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งขายทั้งหมด** และสร้างการรวบรวมของใบสั่งขายที่มีการตั้งค่าที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="606e1-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="606e1-116">สร้างใบสั่งขาย 1 และ 2</span><span class="sxs-lookup"><span data-stu-id="606e1-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="606e1-117">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="606e1-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="606e1-118">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="606e1-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="606e1-119">**กลุ่ม:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="606e1-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="606e1-120">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="606e1-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="606e1-121">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="606e1-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="606e1-122">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="606e1-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="606e1-123">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="606e1-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="606e1-124">สร้างใบสั่งขาย 3 และ 4</span><span class="sxs-lookup"><span data-stu-id="606e1-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="606e1-125">สร้างใบสั่งขายที่เหมือนกันสองใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="606e1-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="606e1-126">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="606e1-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="606e1-127">**กลุ่ม:** ปล่อยฟิลด์นี้ให้ว่าง</span><span class="sxs-lookup"><span data-stu-id="606e1-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="606e1-128">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="606e1-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="606e1-129">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="606e1-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="606e1-130">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="606e1-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="606e1-131">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="606e1-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="606e1-132">นำใบสั่งออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="606e1-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="606e1-133">ทำตามขั้นตอนต่อไปนี้เพื่อนำออกใช้ใบสั่งขายแต่ละใบที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ไปที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="606e1-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="606e1-134">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="606e1-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="606e1-135">ค้นหาและเลือกใบสั่งขายที่จะนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="606e1-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="606e1-136">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** เลือก **การดำเนินการ \> นำออกใช้ไปยังคลังสินค้า** เพื่อนำออกใช้ใบสั่งขายที่เลือก</span><span class="sxs-lookup"><span data-stu-id="606e1-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="606e1-137">ทำซ้ำกระบวนงานนี้สำหรับใบสั่งขายอื่นทั้งหมดที่คุณสร้างสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="606e1-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="606e1-138">รวมการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="606e1-138">Consolidate shipments</span></span>

1. <span data-ttu-id="606e1-139">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="606e1-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="606e1-140">ค้นหาและเลือกการจัดส่งที่ถูกสร้างขึ้น เมื่อมีการนำใบสั่งขาย 1 ออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="606e1-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="606e1-141">(ฟิลด์ **นโยบายการรวมบัญชีการจัดส่ง** ควรถูกตั้งค่าเป็น *กลุ่มใบสั่ง*)</span><span class="sxs-lookup"><span data-stu-id="606e1-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="606e1-142">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดส่ง** เลือก **การจัดส่ง \> รวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="606e1-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="606e1-143">ตรวจสอบความถูกต้องที่แนะนำสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="606e1-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="606e1-144">ควรมีการแนะนำการจัดส่งสินค้าเพียงรายการเดียวที่มีนโยบายเดียวกันสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="606e1-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="606e1-145">ปิดหน้า **การรวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="606e1-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="606e1-146">ค้นหาและเลือกการจัดส่งที่ถูกสร้างขึ้น เมื่อมีการนำใบสั่งขาย 3 ออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="606e1-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="606e1-147">(ฟิลด์ **นโยบายการรวมบัญชีการจัดส่ง** ควรถูกตั้งค่าเป็น *เริ่มต้น*)</span><span class="sxs-lookup"><span data-stu-id="606e1-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="606e1-148">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดส่ง** เลือก **การจัดส่ง \> รวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="606e1-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="606e1-149">ตรวจสอบความถูกต้องว่าไม่มีการแนะนำการจัดส่งสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="606e1-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="606e1-150">เลือก **แสดงตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="606e1-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="606e1-151">ในบานหน้าต่าง **ตัวกรอง** ให้ลบตัวกรอง **หมายเลขใบสั่ง** และจากนั้น เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="606e1-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="606e1-152">ตรวจสอบความถูกต้องที่แนะนำสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="606e1-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="606e1-153">ควรมีการแนะนำการจัดส่งสินค้าเพียงรายการเดียวที่มีนโยบายเดียวกันสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="606e1-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="606e1-154">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="606e1-154">Additional resources</span></span>

- [<span data-ttu-id="606e1-155">นโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="606e1-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="606e1-156">ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="606e1-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)