---
title: รวมบัญชีการจัดส่ง เมื่อนโยบายการรวมบัญชีการจัดส่งถูกแทนที่จากหน้านำออกใช้ไปยังคลังสินค้า
description: หัวข้อนี้จะแสดงสถานการณ์จำลองที่ซึ่งรายการขายหนึ่งรายการขึ้นไปต้องถูกนำออกใช้ด้วยตนเองไปยังคลังสินค้าจากหน้านำออกใช้ไปยังคลังสินค้า และนโยบายการรวมบัญชีการจัดส่งที่กำหนดโดยระบบต้องถูกแทนที่ก่อนการนำออกใช้
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
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 406ff268eede4a9d448b3b9c1729a00fcec8f21e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986755"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="303ea-103">รวมบัญชีการจัดส่ง เมื่อนโยบายการรวมบัญชีการจัดส่งถูกแทนที่จากหน้านำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="303ea-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="303ea-104">หัวข้อนี้จะแสดงสถานการณ์จำลองที่ซึ่งรายการขายหนึ่งรายการขึ้นไปต้องถูกนำออกใช้ด้วยตนเองไปยังคลังสินค้าจากหน้า **นำออกใช้ไปยังคลังสินค้า** และนโยบายการรวมบัญชีการจัดส่งที่กำหนดโดยระบบต้องถูกแทนที่ก่อนการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="303ea-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="303ea-105">คุณอาจจำเป็นต้องมีการแทนที่ของนโยบายการรวมบัญชีการจัดส่ง ตัวอย่างเช่น ใบสั่งที่โดยปกติไม่ได้ถูกรวมกับการจัดส่งที่เปิดค้างไว้จะต้องมีการรวมกับการจัดส่งที่เปิดค้างไว้</span><span class="sxs-lookup"><span data-stu-id="303ea-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="303ea-106">ในระหว่างสถานการณ์จำลอง คุณจะสร้างชุดของใบสั่งขาย และจากนั้น แทนที่นโยบายการรวมบัญชีการจัดส่งเริ่มต้น ก่อนที่คุณจะนำใบสั่งออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="303ea-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="303ea-107">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="303ea-107">Make demo data available</span></span>

<span data-ttu-id="303ea-108">สถานการณ์จำลองในหัวข้อนี้จะอ้างอิงค่าและเรกคอร์ดที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="303ea-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="303ea-109">ถ้าคุณต้องการใช้ค่าที่ระบุไว้ที่นี่เมื่อคุณทำแบบฝึกหัด ควรตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต และตั้งค่านิติบุคคลเป็น **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="303ea-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="303ea-110">ตั้งค่านโยบายการรวมบัญชีการจัดส่งและตัวกรองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="303ea-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="303ea-111">สถานการณ์จำลองที่อธิบายไว้ที่นี่จะถือว่าคุณได้เปิดใช้งานคุณลักษณะแล้ว ทำแบบฝึกหัดแล้วใน [ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง](configure-shipment-consolidation-policies.md) และสร้างนโยบายและเรกคอร์ดอื่นๆ แล้วซึ่งอธิบายไว้ที่นั่น</span><span class="sxs-lookup"><span data-stu-id="303ea-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="303ea-112">ตรวจสอบให้แน่ใจว่าคุณทำแบบฝึกหัดเหล่านั้น ก่อนที่คุณจะดำเนินการต่อด้วยสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="303ea-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="303ea-113">สร้างใบสั่งขายสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="303ea-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="303ea-114">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งขายทั้งหมด** และสร้างใบสั่งขายที่เหมือนกันสามใบที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="303ea-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="303ea-115">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="303ea-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="303ea-116">เพิ่มรายการใบสั่งที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="303ea-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="303ea-117">**หมายเลขสินค้า:** *A0001* (สินค้าที่ไม่มีการกำหนดตัวกรอง **รหัส 4** ให้)</span><span class="sxs-lookup"><span data-stu-id="303ea-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="303ea-118">**ปริมาณ:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="303ea-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="303ea-119">เลือก **สินค้าคงคลัง \> การจอง** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="303ea-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="303ea-120">นำใบสั่งขายออกใช้จากหน้านำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="303ea-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="303ea-121">ทำตามขั้นตอนต่อไปนี้เพื่อแทนที่นโยบายการรวมบัญชีการจัดส่งในระหว่างการนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="303ea-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="303ea-122">ไปที่ **การจัดการคลังสินค้า \> นำออกใช้ไปยังคลังสินค้า \> นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="303ea-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="303ea-123">ในบานหน้าต่างด้านบน ให้เลือกใบสั่งขายแรกที่คุณสร้างสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="303ea-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="303ea-124">เลือก **เพิ่ม** เพื่อเพิ่มรายการไปที่การนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="303ea-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="303ea-125">โปรดสังเกตว่า มีการใช้นโยบายการรวมบัญชีการจัดส่ง *เริ่มต้น* ในบานหน้าต่างด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="303ea-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="303ea-126">ในบานหน้าต่างด้านล่าง ให้เลือก **เลือกนโยบายการรวมบัญชีการจัดส่งใหม่**</span><span class="sxs-lookup"><span data-stu-id="303ea-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="303ea-127">เลือกนโยบายที่อนุญาตการรวมบัญชีกับการจัดส่งที่เปิดค้างไว้อื่นๆ ของนโยบายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="303ea-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="303ea-128">ตัวอย่างเช่น เลือก *นโยบาย CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="303ea-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="303ea-129">เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="303ea-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="303ea-130">เลือกใบสั่งขายที่สองและที่สามที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="303ea-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="303ea-131">เลือก **เพิ่ม** เพื่อเพิ่มรายการไปที่การนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="303ea-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="303ea-132">โปรดสังเกตว่า มีการใช้นโยบาย *เริ่มต้น* ในบานหน้าต่างด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="303ea-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="303ea-133">เลือกรายการที่สอง และจากนั้น ในฟิลด์ **เลือกนโยบายการรวมบัญชีการจัดส่งใหม่** ให้เลือกนโยบาย *CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="303ea-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="303ea-134">เลือก **นำออกใช้ไปยังคลังสินค้า** สำหรับทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="303ea-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="303ea-135">ตรวจสอบความถูกต้องของการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="303ea-135">Verify the shipments</span></span>

<span data-ttu-id="303ea-136">ควรมีการสร้างการจัดส่งสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="303ea-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="303ea-137">การจัดส่งแรกมีรายการสองรายการและถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *CustomerOrderNo*</span><span class="sxs-lookup"><span data-stu-id="303ea-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="303ea-138">การจัดส่งที่สองมีรายการหนึ่งรายการและถูกสร้างขึ้นโดยใช้นโยบายการรวมบัญชีการจัดส่ง *เริ่มต้น*</span><span class="sxs-lookup"><span data-stu-id="303ea-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="303ea-139">ทำตามขั้นตอนต่อไปนี้เพื่อตรวจทานการจัดส่งที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="303ea-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="303ea-140">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="303ea-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="303ea-141">ค้นหาและเลือกการจัดส่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="303ea-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="303ea-142">ในฟิลด์ **นโยบายการรวมบัญชีการจัดส่ง** ให้ทบทวนนโยบายการรวมบัญชีที่ถูกใช้เมื่อมีการสร้างการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="303ea-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="303ea-143">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="303ea-143">Additional resources</span></span>

- [<span data-ttu-id="303ea-144">นโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="303ea-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="303ea-145">ตั้งค่าคอนฟิกนโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="303ea-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
