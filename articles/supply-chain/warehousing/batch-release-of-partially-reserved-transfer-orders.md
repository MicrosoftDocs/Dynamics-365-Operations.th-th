---
title: "การนำชุดงานออกใช้ของใบสั่งการถ่ายโอนที่สำรองบางส่วน"
description: "หัวข้อนี้อธิบายวิธีตั้งค่าและใช้การนำชุดงานออกใช้ของใบสั่งการถ่ายโอนที่สำรองบางส่วนจากอุปกรณ์เคลื่อนที่"
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4569ba5d24f84166254cfce86d9fe2cc9b98ac09
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="3b10c-103">การนำชุดงานออกใช้ของใบสั่งการถ่ายโอนที่สำรองบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3b10c-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3b10c-104">ฟังก์ชันสำหรับการนำชุดงานออกใช้ของใบสั่งการถ่ายโอนที่สำรองบางส่วนช่วยให้คุณสามารถนำใบสั่งการถ่ายโอนออกใช้บางส่วนไปยังคลังสินค้า โดยใช้ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3b10c-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="3b10c-105">เนื่องจากคุณสามารถเลือกที่จะนำปริมาณบางส่วนออกใช้ คุณไม่ต้องรอให้ปริมาณในใบสั่งทั้งหมดพร้อมใช้งานในคลังสินค้าก่อนที่คุณจะนำใบสั่งออกใช้</span><span class="sxs-lookup"><span data-stu-id="3b10c-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="3b10c-106">การนำใบสั่งออกใช้ไปยังคลังสินค้าคือกระบวนการจัดการคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="3b10c-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="3b10c-107">กระบวนการนี้เกี่ยวข้องกับกิจกรรมต่าง ๆ เช่น การเบิกสินค้า การบันทึก และการจัดส่ง ซึ่งผู้ปฏิบัติงานคลังสินค้าสามารถทำได้โดยใช้อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="3b10c-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="3b10c-108">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="3b10c-108">Where it applies</span></span>

<span data-ttu-id="3b10c-109">สำหรับฟังก์ชันนี้ ใบสั่งโอนย้ายถูกนำออกใช้ไปยังคลังสินค้าโดยใช้ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3b10c-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="3b10c-110">ฟังก์ชันนี้มีประโยชน์เมื่อคุณมีสินค้าคงคลังในคลังสินค้าไม่เพียงพอ แต่คุณยังคงต้องการโอนย้ายสินค้าจากคลังสินค้าหนึ่งไปอีกแห่งหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3b10c-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="3b10c-111">วิธีตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3b10c-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="3b10c-112">ระบุเกณฑ์การเติมสินค้าสำหรับใบสั่งโอนย้ายและใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3b10c-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="3b10c-113">ก่อนที่ใบสั่งจะถูกนำออกใช้บางส่วนไปยังคลังสินค้าในชุดงาน จะต้องเป็นไปตามเกณฑ์การเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b10c-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="3b10c-114">เกณฑ์การเติมสินค้าเหล่านี้ขึ้นอยู่กับนโยบายการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b10c-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="3b10c-115">นโยบายการเติมสินค้าสำหรับใบสั่งโอนย้ายและใบสั่งขายถูกระบุไว้ในระดับบริษัท</span><span class="sxs-lookup"><span data-stu-id="3b10c-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="3b10c-116">การนำใบสั่งออกใช้ในชุดงานจะได้รับการยอมรับหรือปฏิเสธโดยขึ้นอยู่กับการตั้งค่านโยบายการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="3b10c-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="3b10c-117">จากนั้นใบสั่งจะถูกประมวลผลให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="3b10c-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="3b10c-118">เมื่อต้องการสร้างนโยบายการเติมสินค้าสำหรับการโอนย้ายและใบสั่งขาย คลิก **การจัดการคลังสินค้า** \> **ตั้งค่า** \> **นำออกใช้ไปยังคลังสินค้า** \> **นโยบายการเติมสินค้า** และจากนั้น สร้างนโยบายการเติมสินค้าด้วยการป้อนชื่อและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3b10c-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="3b10c-119">เมื่อต้องการระบุอัตราการเติมสินค้า ชนิดของมูลค่าและข้อความที่แสดงขึ้นถ้ามีการละเมิดนโยบายการเติมสินค้า คลิก **การจัดการคลังสินค้า** \> **ตั้งค่า** \> **นำออกใช้ไปยังคลังสินค้า** \> **นโยบายการเติมสินค้า** และจากนั้นตั้งค่าฟิลด์ **อัตราการเติมสินค้า** **ชนิดมูลค่า** และ **ข้อความการละเมิดการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3b10c-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="3b10c-120">ตั้งค่านโยบายการเติมสินค้าสำหรับใบสั่งโอนย้ายและใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3b10c-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="3b10c-121">เมื่อต้องการตั้งค่านโยบายการเติมสินค้าสำหรับการโอนย้ายใบสั่ง คลิก **การจัดการสินค้าคงคลัง** \> **ตั้งค่า** \> **พารามิเตอร์การจัดการสินค้าคงคลังและคลังสินค้า** \> **ใบสั่งโอนย้าย** \> **การจัดการคลังสินค้า** แล้วเลือกนโยบายการเติมสินค้าตามใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="3b10c-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="3b10c-122">เมื่อต้องการตั้งค่านโยบายการเติมสินค้าสำหรับใบสั่งขาย คลิก **บัญชีลูกหนี้** \> **ตั้งค่า** \> **พารามิเตอร์ลูกหนี้** \> **การจัดการคลังสินค้า** แล้วเลือกนโยบายการเติมสินค้าตามใบสั่งขายนั้น</span><span class="sxs-lookup"><span data-stu-id="3b10c-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="3b10c-123">อนุญาตให้นำออกใช้ในชุดงานและระบุปริมาณที่ควรจะนำออกใช้ในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3b10c-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="3b10c-124">ชุดงานจะถูกใช้ในการนำใบสั่งออกใช้ไปยังคลังสินค้าในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3b10c-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="3b10c-125">มีการตั้งค่าพารามิเตอร์ที่แยกความแตกต่างของใบสั่งที่ควรรันในชุดงานในชุดงานเอง</span><span class="sxs-lookup"><span data-stu-id="3b10c-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="3b10c-126">พารามิเตอร์ **ปริมาณ** ระบุว่าปริมาณทั้งหมดหรือปริมาณที่จองทางกายภาพควรถูกนำออกใช้ในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="3b10c-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="3b10c-127">พารามิเตอร์ **อนุญาตการนำออกใช้ใบสั่งที่นำออกใช้บางส่วน** กำหนดว่าใบสั่งในชุดงานควรได้รับการยอมรับหรือปฏิเสธถ้ามีการนำออกใช้บางส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3b10c-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="3b10c-128">เมื่อต้องการตั้งค่าพารามิเตอร์ **ปริมาณ** และ **อนุญาตการนำออกใช้ใบสั่งที่นำออกใช้บางส่วน** สำหรับใบสั่งโอนย้าย คลิก **การจัดการคลังสินค้า** \> **นำออกใช้ไปยังคลังสินค้า** \> **นำใบสั่งโอนย้ายออกใช้โดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="3b10c-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="3b10c-129">เมื่อต้องการตั้งค่าพารามิเตอร์ **ปริมาณ** และ **อนุญาตการนำออกใช้ใบสั่งที่นำออกใช้บางส่วน** สำหรับใบสั่งขาย คลิก **การจัดการคลังสินค้า** \> **นำออกใช้ไปยังคลังสินค้า** \> **นำใบสั่งขายออกใช้โดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="3b10c-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

