---
title: กระบวนการขาออก
description: หัวข้อนี้แสดงภาพรวมของกระบวนการขาออกในการจัดการสินค้าคงคลัง
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 5ac3260f128acbc819d7207f68f17adb085da11c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570490"
---
# <a name="outbound-process"></a><span data-ttu-id="d2fe5-103">กระบวนการขาออก</span><span class="sxs-lookup"><span data-stu-id="d2fe5-103">Outbound process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2fe5-104">หัวข้อนี้แสดงภาพรวมของกระบวนการขาออกในการจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d2fe5-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="d2fe5-105">ใบสั่งผลผลิต</span><span class="sxs-lookup"><span data-stu-id="d2fe5-105">Output orders</span></span>

<span data-ttu-id="d2fe5-106">ใบสั่งผลผลิตถูกใช้เพื่อเชื่อมโยงรายการใบสั่งขาย และโอนย้ายบรรทัดใบสั่งด้วยกระบวนการเบิกสินค้าขาออกที่ใช้รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="d2fe5-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="d2fe5-107">เมื่อรายการเบิกสินค้าถูกสร้างขึ้นจากใบสั่งขายหรือใบสั่งโอนย้ายอย่างใดอย่างหนึ่ง ใบสั่งผลผลิตและการจัดส่งจะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d2fe5-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="d2fe5-108">รายการเบิกสินค้ามีความสัมพันธ์แบบหนึ่งต่อหนึ่งกับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d2fe5-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="d2fe5-109">คุณสามารถประมวลผลการจัดส่งใบสั่งโอนย้ายหรือบันทึกการจัดส่งของใบสั่งขายได้จากการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d2fe5-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="d2fe5-110">แผนภาพต่อไปนี้แสดงภาพรวมของกระบวนการใบสั่งขาออก</span><span class="sxs-lookup"><span data-stu-id="d2fe5-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="d2fe5-111">[![ภาพรวมของกระบวนการใบสั่งขาออก](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="d2fe5-112">คุณสามารถตั้งค่ากฎขาออกเพื่อกำหนดว่าโปรแกรมควรจัดการกับกระบวนการขาออกอย่างไร</span><span class="sxs-lookup"><span data-stu-id="d2fe5-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="d2fe5-113">คุณสามารถใช้กฎเหล่านี้เพื่อควบคุมกระบวนการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d2fe5-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="d2fe5-114">โดยเฉพาะอย่างยิ่ง คุณสามารถใช้กฎเพื่อควบคุมว่าขั้นใดในกระบวนการที่สามารถมีการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="d2fe5-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="d2fe5-115">การตั้งค่าต่อไปนี้กำหนดวิธีการจัดการกระบวนการขาออก</span><span class="sxs-lookup"><span data-stu-id="d2fe5-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="d2fe5-116">สถานะเส้นทางการเบิกสินค้าสำหรับใบสั่งขายและใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="d2fe5-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="d2fe5-117">ไปที่ **บัญชีลูกหนี้** \> **ตั้งค่า** \> **บัญชีพารามิเตอร์ลูกหนี้** จากนั้นบนแท็บ **การอัพเดต** เลือกค่าในฟิลด์ **สถานะเส้นทางการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d2fe5-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="d2fe5-118">[![ฟิลด์สถานะเส้นทางการเบิกสินค้าสำหรับใบสั่งขาย](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="d2fe5-119">ถ้าฟิลด์ **สถานะเส้นทางการเบิกสินค้า** ถูกกำหนดเป็น **เสร็จสมบูรณ์** กระบวนการเบิกสินค้าจะเกิดขึ้นโดยอัตโนมัติโดยเป็นส่วนหนึ่งของกระบวนการสร้างรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="d2fe5-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="d2fe5-120">ถ้าฟิลด์ถูกกำหนดเป็น **เรียกใช้แล้ว** จะต้องมีการอัพเดตบรรทัดรายการเบิกสินค้าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d2fe5-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="d2fe5-121">การตั้งค่านี้ยังใช้กับใบสั่งโอนย้ายอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="d2fe5-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="d2fe5-122">ไปที่ **การจัดการสินค้าคงคลัง** \> **ตั้งค่า** \> **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** จากนั้น บนแท็บ **ขนส่ง** เลือกค่าในฟิลด์ **สถานะของเส้นทางการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d2fe5-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="d2fe5-123">[![ฟิลด์สถานะเส้นทางการเบิกสินค้าสำหรับใบสั่งโอนย้าย](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="d2fe5-124">สิ้นสุดใบสั่งสินค้าคงคลังของผลผลิต</span><span class="sxs-lookup"><span data-stu-id="d2fe5-124">End output inventory orders</span></span>

<span data-ttu-id="d2fe5-125">ไปที่ **การจัดการสินค้าคงคลัง** \> **ตั้งค่า** \> **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** จากนั้น บนแท็บ **ทั่วไป** ตั้งค่าตัวเลือก **สิ้นสุดใบสั่งสินค้าคงคลังของผลผลิต**</span><span class="sxs-lookup"><span data-stu-id="d2fe5-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="d2fe5-126">[![ตัวเลือกสิ้นสุดใบสั่งสินค้าคงคลังของผลผลิต](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="d2fe5-127">เมื่อผู้ปฏิบัติงานคลังสินค้าลดปริมาณรายการเบิกสินค้า แล้วปริมาณของใบสั่งสินค้าคงคลังที่สอดคล้องกันจะถูกลบออกจากการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d2fe5-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="d2fe5-128">เมื่อรายการเบิกสินค้ามีการอัพเดต ณ จุดเวลา ปริมาณคงเหลือที่ได้รับรายงานกลับไปยังใบสั่งถ้าตัวเลือก **สิ้นสุดใบสั่งสินค้าคงคลังแสดงผล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="d2fe5-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="d2fe5-129">ถ้าตัวเลือก **สิ้นสุดใบสั่งสินค้าคงคลังแสดงผล** ถูกตั้งค่าเป็น **ไม่ใช่** ปริมาณคงเหลือจะถูกเก็บไว้เป็นปริมาณใบสั่งเอาพุตที่เปิด และต้องถูกเพิ่มเข้าไปยังรายการเบิกสินค้าใหม่เป็นส่วนหนึ่งของฟังก์ชัน **ใบสั่งเอาพุตที่เปิด**</span><span class="sxs-lookup"><span data-stu-id="d2fe5-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="d2fe5-130">[![คำสั่งของใบสั่งผลผลิตที่เปิดบนเมนูฟังก์ชัน](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="d2fe5-131">[![เมนูฟังก์ชันบนหน้าใบสั่งผลผลิตที่เปิด](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="d2fe5-132">ลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="d2fe5-132">Reduce quantity</span></span>

<span data-ttu-id="d2fe5-133">พารามิเตอร์ที่สามที่คุณสามารถใช้เป็นส่วนหนึ่งของกระบวนการสร้างรายการเบิกสินค้าคือพารามิเตอร์ **ลดปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="d2fe5-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="d2fe5-134">การตั้งค่าของพารามิเตอร์นี้ทำงานร่วมกับการตั้งค่า **การจอง** ที่ก่อให้เกิดกระบวนการสำรองสินค้าโดยเป็นส่วนหนึ่งของการนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="d2fe5-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="d2fe5-135">[![พารามิเตอร์ลดปริมาณ](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="d2fe5-136">ตัวอย่างของกระบวนการขาออกสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d2fe5-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="d2fe5-137">ในตัวอย่างนี้ มีใบสั่งขายสำหรับสินค้าสองรายการ</span><span class="sxs-lookup"><span data-stu-id="d2fe5-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="d2fe5-138">ในระหว่างการสร้างรายการเบิกสินค้า ให้คุณเลือกพารามิเตอร์ **ลดปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="d2fe5-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="d2fe5-139">ดังนั้น ให้คุณนำออกใช้และสร้างรายการเบิกสินค้าสำหรับสินค้าคงคลังคงเหลือที่พร้อมใช้งานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d2fe5-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="d2fe5-140">ต้องมีการรายงานการเบิกสินค้าผ่านทางกระบวนการลงทะเบียนสำหรับรายการเบิกสินค้า (**สถานะของเส้นทางการเบิกสินค้า** = **เรียกใช้แล้ว**)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="d2fe5-141">สินค้าคงคลังที่ยังไม่ได้ถูกจองจะถูกจองในระหว่างการสร้างรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="d2fe5-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="d2fe5-142">คุณสามารถลบสินค้าคงคลังที่ไม่พร้อมใช้งานออกจากใบสั่งขาย หรือนำออกใช้ไปยังคลังสินค้าสำหรับการประมวลผลขาออกในภายหลัง เมื่อสินค้าคงคลังมีเพียงพอสำหรับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="d2fe5-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="d2fe5-143">[![อัพเดตรายการเบิกสินค้า](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="d2fe5-144">ทันทีที่มีการเบิกสินค้ารายการเบิกสินค้าทั้งหมดในหน้า **การลงทะเบียนรายการเบิกสินค้า** การจัดส่งที่เกี่ยวข้องจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d2fe5-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="d2fe5-145">จากนั้นจะเริ่มกระบวนการสำหรับบันทึกการจัดส่งของใบสั่งขายตามสินค้าคงคลังที่เบิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="d2fe5-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="d2fe5-146">[![อัพเดตการจัดส่งขาออก](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="d2fe5-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
