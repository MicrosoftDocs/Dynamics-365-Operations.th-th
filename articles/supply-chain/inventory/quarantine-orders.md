---
title: ใบสั่งตรวจสอบสินค้า
description: หัวข้อนี้อธิบายวิธีการใช้ใบสั่งตรวจสอบสินค้าเพื่อบล็อคสินค้าคงคลัง
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956193"
---
# <a name="quarantine-orders"></a><span data-ttu-id="3b113-103">ใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b113-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b113-104">หัวข้อนี้อธิบายวิธีการใช้ใบสั่งตรวจสอบสินค้าเพื่อบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3b113-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="3b113-105">ใบสั่งตรวจสอบสินค้าช่วยให้คุณสามารถบล็อคสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="3b113-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="3b113-106">ตัวอย่างเช่น คุณอาจต้องการตรวจสอบสินค้าสำหรับเหตุผลเกี่ยวกับการควบคุมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="3b113-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="3b113-107">สินค้าคงคลังที่ได้รับการตรวจสอบจะถูกโอนย้ายไปยังคลังสินค้าตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b113-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="3b113-108">ถ้าคุณกำลังใช้กระบวนการจัดการคลังสินค้าขั้นสูง (ในการจัดการคลังสินค้า) การประมวลผลใบสั่งตรวจสอบสินค้าจะใช้สำหรับใบสั่งขายส่งคืนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3b113-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="3b113-109">ตรวจสอบปริมาณสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="3b113-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="3b113-110">เมื่อคุณตรวจสอบสินค้า คุณสามารถสร้างใบสั่งตรวจสอบสินค้าด้วยตนเอง หรือตั้งค่าระบบเพื่อสร้างใบสั่งตรวจสอบสินค้าระหว่างการประมวลผลขาเข้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3b113-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="3b113-111">ตั้งค่าระบบเพื่อสร้างใบสั่งตรวจสอบสินค้าโดยอัตโนมัติ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b113-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="3b113-112">ไปที่ **การจัดการสินค้าคงคลัง \> การตั้งค่า \> สินค้าคงคลัง \> กลุ่มแบบจำลองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3b113-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="3b113-113">เลือกกลุ่มแบบจำลองที่เกี่ยวข้องในบานหน้าต่างรายการ หรือสร้างกลุ่มแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="3b113-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="3b113-114">บนแท็บด่วน **นโยบายสินค้าคงคลัง** ให้เลือกกล่องกาเครื่องหมาย **การบริหารการตรวจสอบสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3b113-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="3b113-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3b113-115">Close the page.</span></span>
1. <span data-ttu-id="3b113-116">ในฟิลด์ **คลังสินค้าตรวจสอบ** สำหรับคลังสินค้าที่ได้รับ ระบุคลังสินค้าตรวจสอบเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="3b113-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="3b113-117">เมื่อสินค้าที่ลงทะเบียนเป็นได้รับแล้วที่คลังสินค้าเป็นของกลุ่มแบบจำลองที่มีการเลือกกล่องกาเครื่องหมาย **การบริหารการตรวจสอบสินค้า** ไว้ ระบบจะสร้างใบสั่งตรวจสอบสินค้าให้</span><span class="sxs-lookup"><span data-stu-id="3b113-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="3b113-118">ใบสั่งตรวจสอบสินค้าจะสั่งให้ผู้ปฏิบัติงานย้ายสินค้าไปที่คลังสินค้าตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="3b113-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="3b113-119">เมื่อคุณสร้างใบสั่งตรวจสอบสินค้าด้วยตนเองบนหน้า **ใบสั่งตรวจสอบสินค้า** สินค้าไม่จำเป็นต้องถูกตั้งค่าสำหรับการจัดการการตรวจสอบสินค้าในกลุ่มแบบจำลองสินค้าที่เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="3b113-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="3b113-120">สำหรับกระบวนการนี้ คุณต้องระบุสินค้าคงคลังคงเหลือที่ควรตรวจสอบและคลังสินค้าตรวจสอบที่ควรใช้</span><span class="sxs-lookup"><span data-stu-id="3b113-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="3b113-121">คุณสามารถใช้สถานะใบสั่งตรวจสอบสินค้าเพื่อช่วยวางแผนกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="3b113-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="3b113-122">สถานะของใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b113-122">Quarantine order statuses</span></span>

<span data-ttu-id="3b113-123">ใบสั่งตรวจสอบสินค้าสามารถมีสถานะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b113-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="3b113-124">ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="3b113-124">Created</span></span>
- <span data-ttu-id="3b113-125">เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="3b113-125">Started</span></span>
- <span data-ttu-id="3b113-126">ที่รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b113-126">Reported as finished</span></span>
- <span data-ttu-id="3b113-127">สิ้นสุดแล้ว</span><span class="sxs-lookup"><span data-stu-id="3b113-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="3b113-128">ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="3b113-128">Created</span></span>

<span data-ttu-id="3b113-129">เมื่อใบสั่งตรวจสอบสินค้าถูกสร้างขึ้นด้วยตนเอง แต่สินค้ายังไม่ถูกเก็บไว้ในคลังสินค้าตรวจสอบ ใบสั่งตรวจสอบสินค้ามีสถานะเป็น **สร้างแล้ว**</span><span class="sxs-lookup"><span data-stu-id="3b113-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="3b113-130">ธุรกรรมสินค้าคงคลังสองรายการจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b113-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="3b113-131">ธุรกรรมหนึ่งคือธุรกรรมที่ออกที่สามารถมีสถานะเป็น **อยู่ระหว่างการสั่ง**, **จองแล้วจริง** หรือ **เบิกสินค้าแล้ว**</span><span class="sxs-lookup"><span data-stu-id="3b113-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="3b113-132">ธุรกรรมอื่นคือธุรกรรมการรับสินค้าที่สามารถมีสถานะเป็น **สั่งแล้ว** หรือ **ลงทะเบียนแล้ว** ที่คลังสินค้าตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="3b113-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="3b113-133">คุณสามารถจอง รับของ และลงทะเบียนการปรับปรุงสินค้าคงคลัง โดยการใช้กระบวนการปกติ</span><span class="sxs-lookup"><span data-stu-id="3b113-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="3b113-134">เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="3b113-134">Started</span></span>

<span data-ttu-id="3b113-135">เมื่อใบสั่งตรวจสอบสินค้าอยู่ในสถานะ **เริ่มต้นแล้ว** สินค้าคงคลังจะได้รับการโอนย้ายจากคลังสินค้าปกติไปยังคลังสินค้าตรวจสอบสินค้า และธุรกรรมสินค้าคงคลังสองรายการจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b113-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="3b113-136">ธุรกรรมหนึ่งที่มีสถานะเป็น **หักลดแล้ว** และธุรกรรมอื่น ๆ ที่มีสถานะเป็น **ได้รับแล้ว**</span><span class="sxs-lookup"><span data-stu-id="3b113-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="3b113-137">ในเวลาเดียวกัน ธุรกรรมสินค้าคงคลังสองรายการถูกสร้างขึ้นเพื่อจัดการกับการโอนย้ายส่งคืน</span><span class="sxs-lookup"><span data-stu-id="3b113-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="3b113-138">ธุรกรรมเหล่านี้ไม่ได้ถูกลงวันที่</span><span class="sxs-lookup"><span data-stu-id="3b113-138">These transactions aren't dated.</span></span> <span data-ttu-id="3b113-139">ธุรกรรมหนึ่งที่มีสถานะเป็น **จองแล้วจริง** และธุรกรรมอื่น ๆ มีสถานะเป็น **สั่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="3b113-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="3b113-140">ที่รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3b113-140">Reported as finished</span></span>

<span data-ttu-id="3b113-141">เมื่อต้องการรายงานการเสร็จงานของใบสั่งตรวจสอบสินค้าที่เริ่มต้นไว้ ให้เปิดใบสั่ง และเลือก **รายงานการเสร็จงาน** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="3b113-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="3b113-142">สินค้าถูกปลดออกจากการตรวจสอบสินค้าแล้ว แต่ยังไม่ถูกย้ายกลับไปที่คลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="3b113-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="3b113-143">การย้ายกลับไปที่คลังสินค้าปกติ สามารถดำเนินการผ่านทางสมุดรายวันการมาถึงของสินค้าได้ ซึ่งจะเริ่มในระหว่างการรายงานเป็นกระบวนการที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="3b113-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="3b113-144">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="3b113-144">Ended</span></span>

<span data-ttu-id="3b113-145">เมื่อใบสั่งตรวจสอบสินค้าสิ้นสุด สินค้าจะถูกย้ายจากคลังสินค้าตรวจสอบกลับไปยังคลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="3b113-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="3b113-146">สถานะของธุรกรรมสินค้าถูกตั้งค่าเป็น *ขายแล้ว* ที่คลังสินค้าตรวจสอบ และ *ซื้อแล้ว* ที่คลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="3b113-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="3b113-147">ของเสียใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b113-147">Quarantine order scrap</span></span>

<span data-ttu-id="3b113-148">โดยเป็นส่วนหนึ่งของกระบวนการใบสั่งตรวจสอบสินค้า คุณอาจทำให้สินค้าคงคลังเสีย</span><span class="sxs-lookup"><span data-stu-id="3b113-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="3b113-149">เมื่อกำลังดำนินการกับของเสีย สถานะสินค้าคงคลังจะกำหนดเป็น *ขายแล้ว* โดยธุรกรรมการออกใช้จากคลังสินค้าตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="3b113-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b113-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3b113-150">Additional resources</span></span>

- [<span data-ttu-id="3b113-151">การบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3b113-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
