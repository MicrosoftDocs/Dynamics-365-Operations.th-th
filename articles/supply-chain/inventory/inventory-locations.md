---
title: "สถานที่เก็บสินค้าคงคลัง"
description: "สถานที่เก็บสินค้าคงคลังจะใช้กับคลังสินค้าพื้นฐาน (WMS I) เพื่อกำหนดที่จัดเก็บสินค้าและเบิกสินค้าในคลังสินค้า WMS"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 186ad9fbf2920ce9cc01a686b133a2de568d7fef
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-locations"></a><span data-ttu-id="89953-103">สถานที่เก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="89953-103">Inventory locations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="89953-104">สถานที่เก็บสินค้าคงคลังจะใช้กับคลังสินค้าพื้นฐาน (WMS I) เพื่อกำหนดที่จัดเก็บสินค้าและเบิกสินค้าในคลังสินค้า WMS</span><span class="sxs-lookup"><span data-stu-id="89953-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="89953-105">หัวข้อนี้ใช้กับลักษณะการทำงานในโมดูลการบริหารสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="89953-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="89953-106">ไม่นำไปใช้กับลักษณะการทำงานในโมดูลการบริหารคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="89953-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="89953-107">คำว่า สถานที่ หมายถึงสถานที่ที่สินค้าถูกเก็บและถูกนำออกมา</span><span class="sxs-lookup"><span data-stu-id="89953-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="89953-108">สำหรับแต่ละสถานที่ สถานที่ที่มีสินค้าถูกเก็บสามารถระบุได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="89953-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="89953-109">โดยค่าเริ่มต้น พวกเขาจะเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="89953-109">By default, they are the same.</span></span> <span data-ttu-id="89953-110">โดยปกติสินค้าจะถูกเก็บและนำสินค้าออกจากสถานที่เก็บด้านเดียวกัน แต่ก็ไม่เสมอไป</span><span class="sxs-lookup"><span data-stu-id="89953-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="89953-111">ตัวอย่างเช่น สินค้าที่ถูกจัดเก็บในชั้นเก็บสินค้าของที่จัดเก็บของสดจะถูกใส่จากที่เก็บหนึ่งและถูกนำออกใช้จากอีกที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89953-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="89953-112">อินพุตหลักถูกกำหนด โดยชื่อสถานที่ ซึ่งโดยปกติถูกกำหนด โดยระยะพิกัด: คลังสินค้า ที่เก็บ ชั้นเก็บสินค้า ชั้น และช่องเก็บ</span><span class="sxs-lookup"><span data-stu-id="89953-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="89953-113">ชื่อหรือรหัสนี้สามารถป้อนด้วยตนเอง หรือสร้างจากระยะพิกัดสถานที่—ตัวอย่างเช่น 01-02-03-4 สำหรับที่เก็บ 1 ชั้นเก็บสินค้า 2 ชั้น 3 ช่องเก็บ 4 ในหน้าสถานที่เก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="89953-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="89953-114">คุณสมบัติของสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="89953-114">Location properties</span></span>

<span data-ttu-id="89953-115">สถานที่เก็บจะมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="89953-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="89953-116">ขนาด (ความสูง ความกว้าง ความลึก และตามปริมาตร)</span><span class="sxs-lookup"><span data-stu-id="89953-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="89953-117">ตำแหน่งคลังสินค้า ที่เก็บ ชั้นเก็บสินค้า ชั้น และช่องเก็บ</span><span class="sxs-lookup"><span data-stu-id="89953-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="89953-118">ชนิดของสถานที่ (สถานที่เก็บสินค้าจำนวนมาก สถานที่เบิกสินค้า ท่าสินค้าขาเข้า ท่าสินค้าขาออก สถานที่ตั้งอินพุทการผลิต สถานที่ตรวจสอบ หรือซุปเปอร์มาร์เก็ตคัมบัง)</span><span class="sxs-lookup"><span data-stu-id="89953-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="89953-119">ตรวจสอบข้อความสามารถใช้ในระบบออนไลน์เพื่อตรวจสอบว่า ผู้ปฏิบัติงานได้เลือกสถานที่ที่ถูกต้องสำหรับสินค้าที่ระบุไว้</span><span class="sxs-lookup"><span data-stu-id="89953-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="89953-120">ข้อความการตรวจสอบนี้สามารถสร้างได้ด้วยตนเองหรือโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="89953-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="89953-121">รหัสการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="89953-121">Sort codes</span></span>
<span data-ttu-id="89953-122">ใช้รหัสการเรียงลำดับเพื่อเพิ่มประสิทธิภาพในการจัดการรายการเบิกสินค้า ซึ่งอธิบายข้อมูลที่จำเป็นสำหรับการเบิกสินค้าจากสินค้าคงคลัง รวมถึงใบสั่งการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="89953-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="89953-123">รหัสการเรียงลำดับสามารถระบุตามที่เก็บและระยะพิกัดอื่น ๆ หรือกำหนดด้วยตนเองสำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="89953-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="89953-124">สถานที่เก็บที่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="89953-124">Blocked locations</span></span>
<span data-ttu-id="89953-125">บางครั้ง คุณอาจต้องการระบุว่า สถานที่ที่ถูกบล็อคสำหรับรอบระยะเวลา ตัวอย่างเช่น ต้องอนุญาตเพื่อซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="89953-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="89953-126">ในบางครั้ง คุณอาจต้องการระบุการบล็อคเฉพาะของอินพุตหรือเอาท์พุทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="89953-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="89953-127">โครงสร้างแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="89953-127">Tree structure</span></span>

<span data-ttu-id="89953-128">ในหน้าสถานที่เก็บสินค้าคงคลัง คุณสามารถดูโครงร่างของคลังสินค้าในโครงสร้างแผนภูมิตามระยะพิกัดของสถานที่เก็บสินค้าคงคลัง ในรูปแบบการแสดงที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="89953-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="89953-129">รักษาสถานที่เก็บสินค้าคงคลัง ผ่านทางแบบฟอร์มคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="89953-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="89953-130">เป็นไปได้ที่คัดลอกสถานที่จากคลังสินค้าหนึ่งไปยังอีกที่หนึ่ง และสร้างสถานที่ผ่านทางวิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="89953-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="89953-131">ก่อนที่คุณรันวิซาร์ด คุณควรตรวจสอบให้แน่ใจว่า คุณได้กำหนดชื่อสถานที่เริ่มต้นบนหน้าคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="89953-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="see-also"></a><span data-ttu-id="89953-132">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="89953-132">See also</span></span>
--------

[<span data-ttu-id="89953-133">สร้างการจัดวางพื้นที่คลังสินค้าใหม่ (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="89953-133">Create a new warehouse layout (Task guide)</span></span>](tasks/create-new-warehouse-layout.md)

