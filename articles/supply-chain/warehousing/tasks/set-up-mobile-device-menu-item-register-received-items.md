--- 
title: "ตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่ในการลงทะเบียนสินค้าที่ได้รับ"
description: "งานนี้มุ่งเน้นการตั้งค่ารายการเมนูอุปกรณ์เคลื่อนที่ "
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e13f644f6d5a817cd3fe24de10f44433ce491f4d
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a><span data-ttu-id="2d4a1-103">ตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่ในการลงทะเบียนสินค้าที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="2d4a1-103">Set up a mobile device menu item to register received items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d4a1-104">งานนี้มุ่งเน้นการตั้งค่ารายการเมนูอุปกรณ์เคลื่อนที่ </span><span class="sxs-lookup"><span data-stu-id="2d4a1-104">This task focuses on the setup of a mobile device menu item.</span></span> <span data-ttu-id="2d4a1-105">รายการเมนูนี้จะใช้สำหรับการลงทะเบียนการรับสินค้าที่สั่งซื้อผ่านใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="2d4a1-105">This menu item is used for registration of the receipt of items ordered via purchase orders.</span></span> 

<span data-ttu-id="2d4a1-106">คุณสามารถใช้คำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="2d4a1-106">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="2d4a1-107">ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d4a1-107">This procedure is intended for the warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="2d4a1-108">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2d4a1-108">Create a mobile device menu item</span></span>
1. <span data-ttu-id="2d4a1-109">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2d4a1-109">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="2d4a1-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2d4a1-110">Click New.</span></span>
3. <span data-ttu-id="2d4a1-111">ในฟิลด์ชื่อเมนูสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2d4a1-111">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="2d4a1-112">นี่คือตัวระบุเฉพาะสำหรับรายการเมนูนี้อุปกรณ์เคลื่อนที่ </span><span class="sxs-lookup"><span data-stu-id="2d4a1-112">This is the unique identifier for this mobile device menu item.</span></span> <span data-ttu-id="2d4a1-113">ตัวอย่างเช่น คุณสามารถพิมพ์ 'การลงทะเบียนในใบสั่งซื้อของฉัน'</span><span class="sxs-lookup"><span data-stu-id="2d4a1-113">For example, you could type 'My PO registration'.</span></span>  
4. <span data-ttu-id="2d4a1-114">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2d4a1-114">In the Title field, type a value.</span></span>
    * <span data-ttu-id="2d4a1-115">นี่คือหัวข้อที่จะแสดงต่อผู้ใช้บนอุปกรณ์เคลื่อนที่ </span><span class="sxs-lookup"><span data-stu-id="2d4a1-115">This is the title, which will be displayed to the user on the mobile device.</span></span> <span data-ttu-id="2d4a1-116">ตัวอย่างเช่น คุณสามารถพิมพ์ 'การลงทะเบียนใบสั่งซื้อ'</span><span class="sxs-lookup"><span data-stu-id="2d4a1-116">For example, you could type 'PO registration'.</span></span>  
5. <span data-ttu-id="2d4a1-117">ในฟิลด์โหมด เลือก 'งาน'</span><span class="sxs-lookup"><span data-stu-id="2d4a1-117">In the Mode field, select 'Work'.</span></span>
    * <span data-ttu-id="2d4a1-118">การลงทะเบียนปริมาณคงคลังคงเหลือที่ได้รับสำหรับรายการใบสั่งซื้อ จะสร้างงานเพื่อย้ายสินค้าจากพื้นที่รับสินค้าไปที่สินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="2d4a1-118">Registration of on-hand quantities received for a purchase order line will create work to move the items from the receiving area into the inventory.</span></span> <span data-ttu-id="2d4a1-119">จะไม่มีการสร้างงานจนกว่าจะมีการลงทะเบียนสินค้า </span><span class="sxs-lookup"><span data-stu-id="2d4a1-119">Work isn’t created until the items are registered.</span></span>  <span data-ttu-id="2d4a1-120">ดังนั้นจึงปล่อยตัวเลือกการใช้งานที่มีอยู่ ให้ตั้งค่าเป็น ไม่</span><span class="sxs-lookup"><span data-stu-id="2d4a1-120">Therefore, leave the Use existing work option set to No.</span></span>  
6. <span data-ttu-id="2d4a1-121">ขยายหรือยุบส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="2d4a1-121">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="2d4a1-122">ในฟิลด์กระบวนการสร้างงาน ให้เลือก 'การรับสินค้าตามใบสั่งซื้อ'</span><span class="sxs-lookup"><span data-stu-id="2d4a1-122">In the Work creation process field, select 'Purchase order item receiving'.</span></span>
    * <span data-ttu-id="2d4a1-123">รายการใบสั่งซื้อต้องถูกระบุเฉพาะก่อนที่สามารถลงทะเบียนปริมาณคงคลังคงเหลือในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d4a1-123">A purchase order line must be uniquely identified before on-hand can be registered in the warehouse.</span></span> <span data-ttu-id="2d4a1-124">ในสถานการณ์นี้ อุปกรณ์เคลื่อนที่จะลงทะเบียนหมายเลขใบสั่งซื้อและหมายเลขสินค้า และซึ่งจะทำให้ระบบสามารถระบุรายการใบสั่งซื้อได้</span><span class="sxs-lookup"><span data-stu-id="2d4a1-124">In this scenario, the mobile device will register the purchase order number and item number, and this will allow the system to identify the PO line.</span></span> <span data-ttu-id="2d4a1-125">การย้ายงานจะถูกสร้างขึ้นและสามารถเบิกได้โดยผู้ปฏิบัติงานอื่น</span><span class="sxs-lookup"><span data-stu-id="2d4a1-125">Put away work will be created and can be picked up by another worker.</span></span>    <span data-ttu-id="2d4a1-126">วิธีการสร้างงานที่คุณเลือกจะกำหนดว่าฟิลด์ใดพร้อมใช้งานบนแท็บด่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="2d4a1-126">The work creation method that you select determines which fields become available on the General fast tab.</span></span>  
    * <span data-ttu-id="2d4a1-127">ถ้าคุณเลือกตัวเลือกการใช้ค่าข้อมูลเริ่มต้น ปุ่มข้อมูลเริ่มต้นจะถูกเปิดใช้งาน </span><span class="sxs-lookup"><span data-stu-id="2d4a1-127">If you select the Use default data option, the Default data button is enabled.</span></span> <span data-ttu-id="2d4a1-128">ที่นี่คุณสามารถเลือกฟิลด์เพื่อแสดงข้อมูลที่โดยทั่วไปผู้ปฏิบัติงานจำเป็นต้องใช้ในการทำงานประจำวัน ดังนั้นค่าเหล่านี้จะแสดงอยู่บนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2d4a1-128">Here you can select fields to display data that a worker typically needs in their daily work, so that these values are shown on the mobile device.</span></span>  
    * <span data-ttu-id="2d4a1-129">พารามิเตอร์การจัดกลุ่มป้ายทะเบียนทำงานร่วมกับกลุ่มลำดับหน่วยที่กำหนดให้กับสินค้าที่ได้รับ </span><span class="sxs-lookup"><span data-stu-id="2d4a1-129">The License plate grouping parameter  works in combination with the unit sequence group that’s assigned to the item that’s being received.</span></span> <span data-ttu-id="2d4a1-130">คุณสามารถระบุได้ว่าใบรับสินค้าที่น้อยกว่า หรือมากกว่าหนึ่งแท่นวางสินค้าควรรวมเป็นเป็นป้ายทะเบียนเดียวกัน หรือแบ่งเป็นป้ายแยกต่างหากสำหรับแต่ละหน่วย</span><span class="sxs-lookup"><span data-stu-id="2d4a1-130">You can specify whether receipts of less than or more than one pallet should be grouped into one license plate, or divided into a separate license plate for each unit.</span></span>  
    * <span data-ttu-id="2d4a1-131">ถ้าคุณเลือกตัวเลือกการสร้างป้ายทะเบียน จะมีการสร้างหมายเลขป้ายทะเบียนเฉพาะตามการเลือกลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2d4a1-131">If you select the Generate license plate  option, this generates a unique license plate number based on the number sequence selection.</span></span>   
    * <span data-ttu-id="2d4a1-132">คุณสามารถเลือกเท็มเพลตที่จะใช้เมื่อมีสร้างงาน </span><span class="sxs-lookup"><span data-stu-id="2d4a1-132">You can select the template that will be used when work is created.</span></span> <span data-ttu-id="2d4a1-133">ตัวอย่างเช่น ถ้าคุณลงทะเบียนสินค้าสำหรับใบสั่งซื้อ งานสำรองจะถูกสร้างขึ้นตามเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="2d4a1-133">For example, if you register an item for a purchase order, the put away work will be generated based on the work template.</span></span> <span data-ttu-id="2d4a1-134">ถ้าคุณไม่เลือกเท็มเพลตงานที่นี่ ระบบจะกำหนดเท็มเพลตตามเกณฑ์การสอบถามที่เชื่อมโยงกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="2d4a1-134">If you don’t select a work template here, the system will assign a template based on the query criteria that are associated with the templates.</span></span>  
    * <span data-ttu-id="2d4a1-135">ถ้ารหัสการโอนการครอบครองถูกแสดงบนอุปกรณ์เคลื่อนที่ ผู้ปฏิบัติงานจะสามารถประเมินสถานะหรือคุณภาพของสินค้าได้ และสามารถเลือกรหัสที่เหมาะสมได้ </span><span class="sxs-lookup"><span data-stu-id="2d4a1-135">If disposition codes are displayed on the mobile device, workers can evaluate the status or quality of the items, and select the appropriate code.</span></span> <span data-ttu-id="2d4a1-136">กฎของรหัสการโอนการครอบครองจะกำหนดว่าสินค้าจะพร้อมสำหรับกระบวนการคลังสินค้าอื่นๆ หรือไม่ </span><span class="sxs-lookup"><span data-stu-id="2d4a1-136">The rules for  the disposition code determine whether the items will be available to other warehouse processes.</span></span> <span data-ttu-id="2d4a1-137">กฎยังกำหนดคำสั่งสถานที่ที่ถูกใช้ในการทำงานที่สร้างขึ้นอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="2d4a1-137">The rules also determine which location directive is used for the work that’s created.</span></span>   
    * <span data-ttu-id="2d4a1-138">ถ้าคุณเลือกตัวเลือกรหัสการโอนการครอบครองชุดงาน ผู้ปฏิบัติงานสามารถประเมินสถานะหรือตรวจสอบคุณภาพของชุดงาน และเลือกรหัสการโอนการครอบครองที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="2d4a1-138">If you select the Batch disposition codes option, workers can evaluate the status or quality of a batch, and select the appropriate disposition code.</span></span>  <span data-ttu-id="2d4a1-139">กฎที่ตั้งในรหัสการโอนการครอบครองชุดงานกำหนดว่า ชุดงานจะพร้อมใช้งานสำหรับกระบวนการคลังสินค้าอื่นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2d4a1-139">The rules that are set on the batch disposition code determine whether the batch will be available to other warehouse processes.</span></span>  
    * <span data-ttu-id="2d4a1-140">ถ้าคุณเลือกตัวเลือกการพิมพ์ป้ายชื่อ ป้ายชื่อทะเบียนจะมีการพิมพ์โดยอัตโนมัติเมื่อมีการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d4a1-140">If you select the Print labels option a license plate label will be printed automatically when items are received.</span></span>  
8. <span data-ttu-id="2d4a1-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2d4a1-141">Click Save.</span></span>
9. <span data-ttu-id="2d4a1-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2d4a1-142">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="2d4a1-143">เพิ่มรายการเมนูที่เมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2d4a1-143">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="2d4a1-144">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > เมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="2d4a1-144">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
2. <span data-ttu-id="2d4a1-145">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์ชื่อด้วยค่า 'ขาเข้า'</span><span class="sxs-lookup"><span data-stu-id="2d4a1-145">Use the Quick Filter to filter on the Name field with a value of 'inbound'.</span></span>
3. <span data-ttu-id="2d4a1-146">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="2d4a1-146">Click Edit.</span></span>
4. <span data-ttu-id="2d4a1-147">ในแผนภูมิ ให้เลือก 'ในแผนภูมิเมนูและรายการเมนูที่มีอยู่ ให้เลือกรายการเมนูที่ได้คุณสร้างขึ้นก่อนหน้า'</span><span class="sxs-lookup"><span data-stu-id="2d4a1-147">In the tree, select 'In the Available menu's and items tree, select the menu item that you created before.'.</span></span>
    * <span data-ttu-id="2d4a1-148">เลือกรายการเมนูที่คุณสร้างขึ้นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="2d4a1-148">Select the menu item that you created before.</span></span>  
5. <span data-ttu-id="2d4a1-149">คลิกที่ลูกศรที่ชี้ไปทางขวา</span><span class="sxs-lookup"><span data-stu-id="2d4a1-149">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="2d4a1-150">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2d4a1-150">Click Save.</span></span>
7. <span data-ttu-id="2d4a1-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2d4a1-151">Close the page.</span></span>


