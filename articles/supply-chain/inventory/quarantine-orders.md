---
title: ใบสั่งตรวจสอบสินค้า
description: หัวข้อนี้อธิบายวิธีการใช้ใบสั่งตรวจสอบสินค้าเพื่อบล็อคสินค้าคงคลัง
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 03a9004aae563959dd19276268b9f81aca4b0735
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011708"
---
# <a name="quarantine-orders"></a><span data-ttu-id="86c04-103">ใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="86c04-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86c04-104">หัวข้อนี้อธิบายวิธีการใช้ใบสั่งตรวจสอบสินค้าเพื่อบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="86c04-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="86c04-105">ใบสั่งตรวจสอบสินค้าสามารถใช้เพื่อบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="86c04-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="86c04-106">ตัวอย่างเช่น คุณอาจต้องการตรวจสอบสินค้าสำหรับเหตุผลเกี่ยวกับการควบคุมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="86c04-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="86c04-107">สินค้าคงคลังที่ได้รับการตรวจสอบจะถูกโอนย้ายไปยังคลังสินค้าตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="86c04-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="86c04-108">**หมายเหตุ:** ถ้าคุณกำลังใช้กระบวนการจัดการคลังสินค้าขั้นสูง (ในการจัดการคลังสินค้า) การประมวลผลใบสั่งตรวจสอบสินค้าจะใช้สำหรับใบสั่งขายส่งคืนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="86c04-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="86c04-109">ตรวจสอบปริมาณสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="86c04-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="86c04-110">เมื่อคุณตรวจสอบสินค้า คุณสามารถสร้างใบสั่งตรวจสอบสินค้าด้วยตนเอง หรือตั้งค่าระบบเพื่อสร้างใบสั่งตรวจสอบสินค้าระหว่างการประมวลผลขาเข้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="86c04-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="86c04-111">ในการสร้างใบสั่งตรวจสอบสินค้าโดยอัตโนมัติ เลือกตัวเลือก **การจัดการตรวจสอบสินค้า** บนแท็บ **นโยบายสินค้าคงคลัง** บนหน้า **กลุ่มแบบจำลองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="86c04-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="86c04-112">นอกจากนี้ คุณต้องระบุข้อกำหนดคลังสินค้าเบื้องต้นในฟิลด์ **คลังสินค้าตรวจสอบ** สำหรับคลังสินค้าที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="86c04-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="86c04-113">เมื่อสินค้าที่ถูกเก็บในคลังสินค้าถูกบันทึกในใบสั่งซื้อหรือใบสั่งผลิต สินค้าที่ได้รับการตรวจสอบจะถูกย้ายไปยังคลังสินค้าตรวจสอบใน Supply Chain Management โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="86c04-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Supply Chain Management.</span></span> <span data-ttu-id="86c04-114">การย้ายนี้จะเกิดขึ้นเมื่อมีการเปลี่ยนสถานะของใบสั่งตรวจสอบสินค้าเป็น **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="86c04-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="86c04-115">เมื่อคุณสร้างใบสั่งตรวจสอบสินค้าด้วยตนเอง สินค้าไม่จำเป็นต้องถูกตั้งค่าสำหรับการจัดการการตรวจสอบสินค้าในกลุ่มแบบจำลองสินค้าที่เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="86c04-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="86c04-116">สำหรับกระบวนการนี้ คุณต้องระบุสินค้าคงคลังคงเหลือที่ควรตรวจสอบและคลังสินค้าตรวจสอบที่ควรใช้</span><span class="sxs-lookup"><span data-stu-id="86c04-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="86c04-117">คุณสามารถใช้สถานะใบสั่งตรวจสอบสินค้าเพื่อช่วยวางแผนกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="86c04-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="86c04-118">สถานะของใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="86c04-118">Quarantine order statuses</span></span>
<span data-ttu-id="86c04-119">ใบสั่งตรวจสอบสินค้าสามารถมีสถานะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="86c04-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="86c04-120">ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="86c04-120">Created</span></span>
-   <span data-ttu-id="86c04-121">เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="86c04-121">Started</span></span>
-   <span data-ttu-id="86c04-122">ที่รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="86c04-122">Reported as finished</span></span>
-   <span data-ttu-id="86c04-123">สิ้นสุดแล้ว</span><span class="sxs-lookup"><span data-stu-id="86c04-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="86c04-124">ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="86c04-124">Created</span></span>

<span data-ttu-id="86c04-125">เมื่อใบสั่งตรวจสอบสินค้าถูกสร้างขึ้นด้วยตนเอง แต่สินค้ายังไม่ถูกเก็บไว้ในคลังสินค้าตรวจสอบ ใบสั่งตรวจสอบสินค้ามีสถานะเป็น **สร้างแล้ว**</span><span class="sxs-lookup"><span data-stu-id="86c04-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="86c04-126">ธุรกรรมสินค้าคงคลังสองรายการจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="86c04-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="86c04-127">ธุรกรรมหนึ่งคือธุรกรรมที่ออกที่สามารถมีสถานะเป็น **อยู่ระหว่างการสั่ง**, **จองแล้วจริง** หรือ **เบิกสินค้าแล้ว**</span><span class="sxs-lookup"><span data-stu-id="86c04-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="86c04-128">ธุรกรรมอื่นคือธุรกรรมการรับสินค้าที่สามารถมีสถานะเป็น **สั่งแล้ว** หรือ **ลงทะเบียนแล้ว** ที่คลังสินค้าตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="86c04-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="86c04-129">คุณสามารถจอง รับของ และลงทะเบียนการปรับปรุงสินค้าคงคลัง โดยการใช้กระบวนการปกติ</span><span class="sxs-lookup"><span data-stu-id="86c04-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="86c04-130">เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="86c04-130">Started</span></span>

<span data-ttu-id="86c04-131">เมื่อใบสั่งตรวจสอบสินค้าอยู่ในสถานะ **เริ่มต้นแล้ว** สินค้าคงคลังจะได้รับการโอนย้ายจากคลังสินค้าปกติไปยังคลังสินค้าตรวจสอบสินค้า และธุรกรรมสินค้าคงคลังสองรายการจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="86c04-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="86c04-132">ธุรกรรมหนึ่งที่มีสถานะเป็น **หักลดแล้ว** และธุรกรรมอื่น ๆ ที่มีสถานะเป็น **ได้รับแล้ว**</span><span class="sxs-lookup"><span data-stu-id="86c04-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="86c04-133">ในเวลาเดียวกัน ธุรกรรมสินค้าคงคลังสองรายการถูกสร้างขึ้นเพื่อจัดการกับการโอนย้ายส่งคืน</span><span class="sxs-lookup"><span data-stu-id="86c04-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="86c04-134">ธุรกรรมเหล่านี้ไม่ได้ถูกลงวันที่</span><span class="sxs-lookup"><span data-stu-id="86c04-134">These transactions aren't dated.</span></span> <span data-ttu-id="86c04-135">ธุรกรรมหนึ่งที่มีสถานะเป็น **จองแล้วจริง** และธุรกรรมอื่น ๆ มีสถานะเป็น **สั่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="86c04-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="86c04-136">ที่รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="86c04-136">Reported as finished</span></span>

<span data-ttu-id="86c04-137">โดยการคลิก **รายงานว่าเสร็จสิ้น** คุณสามารถรายงานว่าใบสั่งตรวจสอบสินค้าที่เริ่มต้นนั้นเสร็จสิ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="86c04-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="86c04-138">สินค้าถูกปลดออกจากการตรวจสอบสินค้าแล้ว แต่ยังไม่ถูกย้ายกลับไปที่คลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="86c04-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="86c04-139">การย้ายกลับไปที่คลังสินค้าปกติ สามารถดำเนินการผ่านทางสมุดรายวันการมาถึงของสินค้าได้ ซึ่งจะเริ่มในระหว่างการรายงานเป็นกระบวนการที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="86c04-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="86c04-140">สิ้นสุดแล้ว</span><span class="sxs-lookup"><span data-stu-id="86c04-140">Ended</span></span>

<span data-ttu-id="86c04-141">เมื่อใบสั่งตรวจสอบสินค้าสิ้นสุด สินค้าจะถูกย้ายจากคลังสินค้าตรวจสอบกลับไปยังคลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="86c04-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="86c04-142">สถานะของธุรกรรมสินค้าถูกตั้งค่าเป็น **ขายแล้ว** ที่คลังสินค้าตรวจสอบ และ **ซื้อแล้ว** ที่คลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="86c04-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="86c04-143">ของเสียใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="86c04-143">Quarantine order scrap</span></span>
<span data-ttu-id="86c04-144">โดยเป็นส่วนหนึ่งของกระบวนการใบสั่งตรวจสอบสินค้า คุณอาจทำให้สินค้าคงคลังเสีย</span><span class="sxs-lookup"><span data-stu-id="86c04-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="86c04-145">เมื่อกำลังดำนินการกับของเสีย สถานะสินค้าคงคลังจะกำหนดเป็น **ขายแล้ว** โดยธุรกรรมการออกใช้จากคลังสินค้าตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="86c04-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="86c04-146">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="86c04-146">Additional resources</span></span>
--------

[<span data-ttu-id="86c04-147">การบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="86c04-147">Inventory blocking</span></span>](inventory-blocking.md)
