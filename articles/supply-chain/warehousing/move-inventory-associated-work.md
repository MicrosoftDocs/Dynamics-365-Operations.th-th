---
title: "การเคลื่อนย้ายสินค้าคงคลังที่มีงานที่เชื่อมโยงในการจัดการคลังสินค้า"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้การยืนยันการเบิกสินค้าเป็นรายชิ้นจากอุปกรณ์เคลื่อนที่"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7d81397ed30751f5b3dd7c46ffe6b27b8153c8f9
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="29c68-103">การเคลื่อนย้ายสินค้าคงคลังที่มีงานที่เชื่อมโยงในการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="29c68-103">Movement of inventory with associated work in Warehouse management</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="29c68-104">โดยการใช้ความเคลื่อนไหวของสินค้าคงคลัง คุณสามารถเลือกผู้ปฏิบัติงานคลังสินค้าที่ได้รับอนุญาตให้ย้ายสินค้าคงคลังที่จองไว้</span><span class="sxs-lookup"><span data-stu-id="29c68-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="29c68-105">ซึ่งให้ความยืดหยุ่นกับคลังสินค้าควบคุมที่คุณสามารถตัดสินใจที่จะไม่อนุญาตให้ผู้ปฏิบัติงานเลือกสถานที่เบิกสินค้าใหม่สำหรับงานการเบิกสินค้าที่สร้างขึ้นไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="29c68-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="29c68-106">นอกจากนี้ยังอนุญาตให้ผู้จัดการคลังสินค้าควบคุมความสามารถที่ผู้ปฏิบัติงานที่มีประสบการณ์น้อยบางรายควรมี</span><span class="sxs-lookup"><span data-stu-id="29c68-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="29c68-107">ความยืดหยุ่นในการจัดการการดำเนินงานประจำวันของพนักงานคลังสินค้าจะมีประโยชน์ในสถานการณ์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29c68-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="29c68-108">สถานการณ์จำลอง 1</span><span class="sxs-lookup"><span data-stu-id="29c68-108">Scenario 1</span></span>
<span data-ttu-id="29c68-109">บริษัทมีพื้นที่การรับสินค้าค่อนข้างเล็ก และถูกบีบอัดกับแท่นวางสินค้าและกล่องที่กำลังรอการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="29c68-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="29c68-110">การจัดส่งที่มีขนาดใหญ่มีการคาดการณ์ไว้ในวันปัจจุบัน เพื่อให้เจ้าหน้าที่รับสินค้าตัดสินใจที่จะล้างค่าพื้นที่การรับสินค้า ด้วยการย้ายแท่นวางสินค้าบางรายการไปยังพื้นที่จัดเตรียมขาเข้าสำรอง</span><span class="sxs-lookup"><span data-stu-id="29c68-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="29c68-111">สถานการณ์จำลอง 2</span><span class="sxs-lookup"><span data-stu-id="29c68-111">Scenario 2</span></span>
<span data-ttu-id="29c68-112">ผู้ปฏิบัติงานคลังสินค้าที่มีประสบการณ์สังเกตพบว่า โอกาสในคลังสินค้าที่จะรวมสินค้าในสถานที่หนึ่งแทนที่จะแบ่งสถานที่ใกล้เคียงเป็น 3 แห่งที่มีปริมาณสินค้าในแต่ละแห่งน้อย</span><span class="sxs-lookup"><span data-stu-id="29c68-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="29c68-113">ผู้ปฏิบัติงานต้องการรวมปริมาณโดยการย้ายสินค้าจากสถานที่เหล่านี้ในแต่ละแห่งในที่ตั้งเดียวกันและบนป้ายทะเบียนเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="29c68-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="29c68-114">สถานการณ์จำลอง 3</span><span class="sxs-lookup"><span data-stu-id="29c68-114">Scenario 3</span></span>
<span data-ttu-id="29c68-115">แท่นวางสินค้ากำลังรอการจัดส่งสินค้าในสถานที่สำหรับการจัดเตรียม เช่น STAGE01 ซึ่งอยู่ใกล้กับ BAYDOOR01</span><span class="sxs-lookup"><span data-stu-id="29c68-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="29c68-116">อย่างไรก็ตาม เนื่องจากการเปลี่ยนแปลงของแผนการ มีการกำหนดให้รถบรรทุกมาถึงที่ BAYDOOR04</span><span class="sxs-lookup"><span data-stu-id="29c68-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="29c68-117">พนักงานจัดส่งสินค้าคำนึงถึงเรื่องนี้และจำเป็นที่จะต้องทำให้แน่ใจว่ารถบรรทุกไม่จำเป็นต้องรอให้มีการโหลดจาก STAGE01</span><span class="sxs-lookup"><span data-stu-id="29c68-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="29c68-118">เจ้าหน้าที่จัดส่งสินค้าตัดสินใจที่จะย้ายสินค้าในการจัดส่งนั้นจาก STAGE01 ไปยัง STAGE04 ซึ่งเป็นใกล้กับปลายทางใหม่มากกว่า</span><span class="sxs-lookup"><span data-stu-id="29c68-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="29c68-119">ข้อจำกัดในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="29c68-119">Current limitations</span></span>

<span data-ttu-id="29c68-120">การจองงานที่คุณสามารถย้ายได้จะจำกัดเฉพาะใบสั่งขาย การออกใบสั่งโอนย้าย การรับใบสั่งโอนย้าย ใบสั่งซื้อ และงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="29c68-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="29c68-121">การย้ายสินค้าถูกจำกัดเพื่อป้องกันการแบ่งรายการงาน</span><span class="sxs-lookup"><span data-stu-id="29c68-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="29c68-122">ซึ่งหมายความว่า ถ้าคุณมีรายการงานสำหรับสินค้า A 100 ชิ้น จากสถานที่เก็บ Loc1 คุณจะไม่สามารถเคลื่อนย้ายสินค้า A เพียงแค่ 30 ชิ้นจากจุดนั้นไปยังตำแหน่งอื่นได้</span><span class="sxs-lookup"><span data-stu-id="29c68-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="29c68-123">ซึ่จะทำให้การแบ่งของรายการงานที่มีอยู่เป็น 30 และ 70 ชิ้นเนื่องจากสถานที่เก็บมีความแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="29c68-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="29c68-124">สำหรับสถานการณ์จำลองของการแบ่งระยะ ซึ่งที่คุณย้ายสินค้ามาจากป้ายทะเบียนหรือย้ายสินค้าไปยังป้ายทะเบียน ถูกตั้งเป็นป้ายทะเบียนเป้าหมายสำหรับใบสั่งงาน อนุญาตให้มีเฉพาะการย้ายป้ายทะเบียนเท่านั้น เพื่อที่จะได้ไม่ไปแบ่งค่าของป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="29c68-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="29c68-125">ในขณะนี้จะสนับสนุนเฉพาะการเคลื่อนไหวเฉพาะกิจเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="29c68-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="29c68-126">ซึ่งหมายความว่า คุณจะไม่สามารถย้ายสินค้าคงคลังที่จองไว้โดยใช้การเคลื่อนย้ายตามรายการเมนูของอุปกรณ์เคลื่อนเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="29c68-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="29c68-127">ตั้งค่าสิทธิ์ในการย้ายสินค้าคงคลังที่จองไว้สำหรับผู้ปฏิบัติงานแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="29c68-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="29c68-128">สำหรับผู้ปฏิบัติงานที่ควรจะได้รับอนุญาตให้ย้ายสินค้าคงคลังที่จองไว้ ให้เลือกกล่องกาเครื่องหมาย **อนุญาตความเคลื่อนไหวของสินค้าคงคลังที่มีการเชื่อมโยงงาน** ภายใต้ **การจัดการคลังสินค้า** > **ตั้งค่า** > **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="29c68-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="29c68-129">Backported</span><span class="sxs-lookup"><span data-stu-id="29c68-129">Backported</span></span>

<span data-ttu-id="29c68-130">คุณลักษณะนี้ยังได้รับการสนับสนุนโดย Microsoft Dynamics AX 2012 R3 และจะพร้อมใช้งานเป็นส่วนหนึ่งของ CU12</span><span class="sxs-lookup"><span data-stu-id="29c68-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="29c68-131">และยังสามารถดาวน์โหลดทีละรายการโดยใช้หมายเลข KB 3192548</span><span class="sxs-lookup"><span data-stu-id="29c68-131">It can also be downloaded individually through KB number 3192548.</span></span> 


