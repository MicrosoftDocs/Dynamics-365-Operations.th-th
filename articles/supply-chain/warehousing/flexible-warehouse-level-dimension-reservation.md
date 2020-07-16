---
title: นโยบายการจองมิติในระดับคลังสินค้าที่ยืดหยุ่นได้
description: นี่จะอธิบายถึงนโยบายการจองสินค้าคงคลังที่ทำให้ธุรกิจซึ่งจำหน่ายผลิตภัณฑ์ที่มีการติดตามชุดงานและรันลอจิสติกส์ของตนเป็นการดำเนินงานที่เปิดใช้งาน WMS สามารถจองชุดงานเฉพาะสำหรับใบสั่งขายของลูกค้า ถึงแม้ว่าลำดับชั้นการจองที่เชื่อมโยงกับผลิตภัณฑ์จะไม่อนุญาตการจองของชุดงานเฉพาะ
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ec80346126713cc604b00e6ca7f6e8f4c242dc6f
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530316"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="71af7-103">นโยบายการจองมิติในระดับคลังสินค้าที่ยืดหยุ่นได้</span><span class="sxs-lookup"><span data-stu-id="71af7-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71af7-104">เมื่อลำดับชั้นการจองสินค้าคงคลังของชนิด "\[ชุดงาน-ข้างล่าง\]" เชื่อมโยงกับผลิตภัณฑ์ ธุรกิจที่ขายผลิตภัณฑ์ที่ติดตามชุดงานและรันลอจิสติกส์ของตนเป็นการดำเนินงานที่เปิดใช้งานสำหรับ Microsoft Dynamics 365 Warehouse Management System (WMS) จะไม่สามารถจองชุดเฉพาะของผลิตภัณฑ์เหล่านั้นสำหรับใบสั่งขายของลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="71af7-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="71af7-105">หัวข้อนี้จะอธิบายถึงนโยบายการจองสินค้าคงคลังซึ่งช่วยให้ธุรกิจเหล่านี้สามารถจองชุดงานที่ระบุได้ แม้ว่าผลิตภัณฑ์จะเชื่อมโยงกับลำดับชั้นการจอง "\[ตำแหน่ง\]ชุดงาน-ข้างล่าง"</span><span class="sxs-lookup"><span data-stu-id="71af7-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="71af7-106">ลำดับชั้นการจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="71af7-107">ส่วนนี้สรุปลำดับชั้นการจองสินค้าคงคลังที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="71af7-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="71af7-108">ซึ่งโฟกัสตามวิธีการจัดการสินค้าที่ติดตามชุดงานและสินค้าที่ติดตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="71af7-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="71af7-109">ลำดับชั้นการจองสินค้าคงคลังบอกว่า หากต้องมีมิติการจัดเก็บมาเกี่ยวข้อง ใบสั่งความต้องการจะมีมิติบังคับของไซต์ คลังสินค้า และสถานะของสินค้าคงคลัง ในขณะที่ตรรกะของคลังสินค้ามีความรับผิดชอบในการกำหนดสถานที่ให้กับปริมาณที่ร้องขอและการจองสถานที่</span><span class="sxs-lookup"><span data-stu-id="71af7-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="71af7-110">กล่าวคือ ในการโต้ตอบระหว่างใบสั่งความต้องการและการดำเนินงานของคลังสินค้า มีการคาดว่าใบสั่งความต้องการจะบ่งชี้ว่าจะต้องมีการจัดส่งใบสั่งจากที่ใด (นั่นคือ ไซต์และคลังสินค้าใด)</span><span class="sxs-lookup"><span data-stu-id="71af7-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="71af7-111">คลังสินค้าจะพึ่งพาตรรกะเพื่อหาปริมาณที่ต้องการในสถานที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="71af7-112">อย่างไรก็ตาม เพื่อให้สะท้อนถึงแบบจำลองในการดำเนินงานของธุรกิจ มิติการติดตาม (ชุดงานและหมายเลขลำดับประจำสินค้า) จะขึ้นอยู่กับความยืดหยุ่นที่มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="71af7-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="71af7-113">ลำดับชั้นการจองสินค้าคงคลังสามารถรองรับสถานการณ์ที่เงื่อนไขต่อไปนี้มีผลบังคับใช้:</span><span class="sxs-lookup"><span data-stu-id="71af7-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="71af7-114">ธุรกิจอาศัยการดำเนินงานของคลังสินค้าเพื่อจัดการการเบิกสินค้าของปริมาณที่มีชุดงานหรือหมายเลขลำดับประจำสินค้า หลังจากพบปริมาณในพื้นที่จัดเก็บคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="71af7-115">แบบจำลองนี้มักเรียกว่า *\[ตำแหน่ง\]ด้านล่างชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="71af7-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="71af7-116">โดยทั่วไปจะใช้เมื่อชุดงานของผลิตภัณฑ์หรือหมายเลขลำดับประจำสินค้าไม่มีความสำคัญต่อลูกค้าที่วางความต้องการกับบริษัทผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="71af7-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="71af7-117">ถ้าชุดงานหรือหมายเลขลำดับประจำสินค้าเป็นส่วนหนึ่งของข้อมูลจำเพาะของใบสั่งของลูกค้า และมีการบันทึกไว้ในใบสั่งความต้องการ การดำเนินงานคลังสินค้าที่ค้นหาปริมาณในคลังสินค้าจะถูกจำกัดโดยหมายเลขที่ร้องขอเฉพาะและไม่ได้รับอนุญาตให้เปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="71af7-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="71af7-118">แบบจำลองนี้มักเรียกว่า *\[ตำแหน่ง\]เหนือชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="71af7-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="71af7-119">ในสถานการณ์เหล่านี้ ความท้าทายก็คือคุณสามารถกำหนดลำดับชั้นการจองสินค้าคงคลังเพียงหนึ่งรายการให้กับผลิตภัณฑ์ที่นำออกใช้แต่ละรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="71af7-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="71af7-120">ดังนั้น สำหรับ WMS เพื่อจัดการสินค้าที่ติดตาม หลังจากการกำหนดลำดับชั้นจะกำหนดเมื่อต้องมีการจองชุดงานหรือหมายเลขลำดับประจำสินค้า (เมื่อมีการใช้ใบสั่งความต้องการ หรือระหว่างงานการเบิกสินค้าในคลังสินค้า) จะไม่สามารถเปลี่ยนแปลงช่วงเวลานี้บนพื้นฐานเฉพาะกิจได้</span><span class="sxs-lookup"><span data-stu-id="71af7-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="71af7-121">การจองสินค้าแบบยืดหยุ่นสำหรับสินค้าที่มีการติดตามชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="71af7-122">สถานการณ์จำลองทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="71af7-122">Business scenario</span></span>

<span data-ttu-id="71af7-123">ในสถานการณ์สมมตินี้ บริษัทใช้กลยุทธ์สินค้าคงคลังที่มีการติดตามสินค้าสำเร็จรูปโดยหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="71af7-124">นอกจากนี้ บริษัทนี้ยังใช้ปริมาณงาน WMS</span><span class="sxs-lookup"><span data-stu-id="71af7-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="71af7-125">เนื่องจากปริมาณนี้มีตรรกะที่มีเครื่องมือที่ดีสำหรับการวางแผนและการรันการเบิกสินค้าและการดำเนินการจัดส่งสินค้าสำหรับสินค้าที่เปิดใช้งานชุดงานสินค้า ส่วนใหญ่ของสินค้าสำเร็จรูปเกี่ยวข้องกับลำดับชั้นการจองสินค้าคงคลัง "\[สถานที่\]ด้านล่างชุดงาน"</span><span class="sxs-lookup"><span data-stu-id="71af7-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="71af7-126">ข้อดีของการตั้งค่าการดำเนินงานชนิดนี้คือ การตัดสินใจ (ซึ่งคือการตัดสินใจในการจองอย่างมีประสิทธิภาพ) เกี่ยวกับชุดงานที่จะเบิกสินค้าและสถานที่เก็บสินค้าในคลังสินค้า จะถูกเลื่อนออกไปจนกว่าการดำเนินการเบิกสินค้าของคลังสินค้าจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="71af7-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="71af7-127">ไม่มีการดำเนินการเมื่อมีการวางใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="71af7-128">ถึงแม้ว่าลำดับชั้นการจอง "\[สถานที่\]ด้านล่างชุดงาน" ตอบสนองต่อเป้าหมายธุรกิจของบริษัทเป็นอย่างดี ลูกค้าที่จัดตั้งขึ้นของบริษัทหลายรายต้องการชุดงานเดียวกันกับที่พวกเขาซื้อมาก่อนหน้านี้ เมื่อพวกเขาเรียงลำดับผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="71af7-129">ดังนั้น บริษัทกำลังมองหาความยืดหยุ่นในลักษณะที่มีการจัดการกฎการจองชุดงาน ดังนั้น ทั้งนี้ขึ้นอยู่กับความต้องการของลูกค้าสำหรับสินค้าเดียวกัน ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="71af7-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="71af7-130">คุณสามารถบันทึกหมายเลขชุดงานและสำรองไว้เมื่อใบสั่งนี้ถูกใช้โดยตัวประมวลผลการขาย และไม่สามารถเปลี่ยนแปลงได้ในระหว่างการดำเนินงานของคลังสินค้าและ/หรือถูกใช้โดยความต้องการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="71af7-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="71af7-131">ลักษณะการทำงานนี้ช่วยรับประกันได้ว่ามีการจัดส่งหมายเลขชุดงานที่สั่งให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="71af7-132">ถ้าหมายเลขชุดงานไม่ใช่สิ่งที่จำเป็นสำหรับลูกค้า การดำเนินงานคลังสินค้าสามารถกำหนดหมายเลขชุดงานในระหว่างการเบิกสินค้าได้ หลังจากดำเนินการลงทะเบียนใบสั่งขายและการจองสินค้าเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="71af7-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="71af7-133">การการอนุญาตการจองของชุดงานเฉพาะในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="71af7-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="71af7-134">เพื่อให้เหมาะสมกับความยืดหยุ่นที่ต้องการในลักษณะการทำงานของการจองชุดงานสำหรับสินค้าที่เกี่ยวข้องกับลำดับชั้นการจองสินค้าคงคลัง "\[สถานที่\] ด้านล่างชุดงาน" ผู้จัดการสินค้าคงคลังจะต้องเลือกกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าในใบสั่งความต้องการ** สำหรับระดับ **หมายเลขชุดงาน** ในหน้า **ลำดับชั้นการจองสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="71af7-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![การทำให้ลำดับชั้นการจองสินค้าคงคลังยืดหยุ่นได้](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="71af7-136">เมื่อมีการเลือกระดับ **หมายเลขชุดงาน** ในลำดับชั้น จะมีการเลือกมิติทั้งหมดด้านบนระดับนั้นและเพิ่มจนถึงระดับ **สถานที่** จะถูกเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="71af7-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="71af7-137">(โดยค่าเริ่มต้น จะมีการเลือกมิติทั้งหมดที่อยู่เหนือระดับ **สถานที่** ไว้ล่วงหน้า) ลักษณะการทำงานนี้จะสะท้อนถึงตรรกะที่ซึ่งมิติทั้งหมดในช่วงระหว่างหมายเลขชุดงานและสถานที่จะถูกจองโดยอัตโนมัติ หลังจากที่คุณจองหมายเลขชุดงานเฉพาะในรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="71af7-138">กล่องกาเครื่องหมาย **อนุญาตให้จองสินค้าในใบสั่งความต้องการ** ใช่เฉพาะกับระดับของลำดับชั้นการจองที่อยู่ต่ำกว่ามิติสถานที่คลังสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="71af7-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="71af7-139">**หมายเลขชุดงาน** คือเฉพาะระดับในลำดับชั้นที่เปิดสำหรับนโยบายการจองแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="71af7-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="71af7-140">กล่าวคือ คุณไม่สามารถเลือกกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าในใบสั่งความต้องการ** สำหรับระดับ **สถานที่** **ป้ายทะเบียน** หรือ **หมายเลขลำดับประจำสินค้า**</span><span class="sxs-lookup"><span data-stu-id="71af7-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="71af7-141">ถ้าลำดับชั้นการจองของคุณมีมิติหมายเลขลำดับประจำสินค้า (ซึ่งต้องอยู่ต่ำกว่าระดับ **หมายเลขชุดงาน** เสมอ) และถ้าคุณเปิดใช้งานการจองชุดงานเฉพาะสำหรับหมายเลขชุดงาน ระบบจะดำเนินการจัดการการจองหมายเลขลำดับประจำสินค้าและการดำเนินการเบิกสินค้า ตามกฎที่ใช้กับนโยบายการจอง "\[สถานที่\] ด้านล่างหมายเลขลำดับ"</span><span class="sxs-lookup"><span data-stu-id="71af7-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="71af7-142">เมื่อใดก็ตาม คุณสามารถอนุญาตให้มีการจองเฉพาะชุดงานสำหรับลำดับชั้นการจอง "\[สถานที่\] ด้านล่างชุดงาน" ที่มีอยู่ในการปรับใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="71af7-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="71af7-143">การเปลี่ยนแปลงนี้จะไม่มีผลกระทบต่อการจองใดๆ และงานของคลังสินค้าที่เปิดซึ่งถูกสร้างก่อนที่จะเกิดการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="71af7-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="71af7-144">อย่างไรก็ตาม ไม่สามารถล้างกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าในใบสั่งความต้องการ** หากธุรกรรมสินค้าคงคลังของชนิดปัญหา **สั่งให้สำรอง** **ถูกจองจริง** หรือ **สั่งแล้ว** สำหรับสินค้าหนึ่งรายการขึ้นไปที่สัมพันธ์กับลำดับชั้นการจองนั้น</span><span class="sxs-lookup"><span data-stu-id="71af7-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="71af7-145">ถ้าลำดับชั้นการจองที่มีอยู่ของสินค้าไม่อนุญาตให้ใช้ข้อมูลจำเพาะของชุดงานในใบสั่ง คุณสามารถกำหนดอีกครั้งให้กับลำดับชั้นการจองที่อนุญาตให้ใช้ข้อมูลจำเพาะชุดงานได้ หากโครงสร้างระดับของลำดับชั้นเหมือนกันในลำดับชั้นทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="71af7-146">ใช้ฟังก์ชัน **เปลี่ยนแปลงลำดับชั้นการจองสินค้าสำหรับสินค้า** เพื่อทำการกำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="71af7-147">การเปลี่ยนแปลงนี้อาจเกี่ยวข้องเมื่อคุณต้องการป้องกันไม่ให้มีการจองชุดงานแบบยืดหยุ่นสำหรับชุดย่อยของสินค้าที่มีการติดตามชุดงาน แต่อนุญาตสำหรับส่วนที่เหลือของพอร์ตโฟลิโอผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="71af7-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="71af7-148">ไม่ว่าคุณเลือกกล่องกาเครื่องหมาย **อนุญาตให้จองสินค้าในใบสั่งความต้องการ** หรือไม่ ถ้าคุณไม่ต้องการจองหมายเลขชุดงานเฉพาะสำหรับสินค้าในรายการใบสั่ง ตรรกะการดำเนินงานคลังสินค้าเริ่มต้นที่มีผลบังคับใช้สำหรับลำดับชั้นการจอง "\[สถานที่\] ด้านล่างชุดงาน" จะยังคงใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="71af7-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="71af7-149">จองหมายเลขชุดงานเฉพาะสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="71af7-150">หลังจากที่มีการตั้งค่าลำดับชั้นการจองสินค้าคงคลังของ "\[สถานที่\] ด้านล่างชุดงาน" ของสินค้าที่ติดตามชุดงาน เพื่ออนุญาตให้มีการจองหมายเลขชุดงานเฉพาะบนใบสั่งขาย ตัวประมวลผลใบสั่งขายสามารถใช้ใบสั่งของลูกค้าสำหรับสินค้าเดียวกันได้ในวิธีใดวิธีหนึ่งต่อไปนี้ โดยขึ้นอยู่กับคำขอของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="71af7-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="71af7-151">**ป้อนรายละเอียดใบสั่งโดยไม่มีการระบุหมายเลขชุดงาน** – ควรใช้วิธีการนี้เมื่อข้อมูลจำเพาะชุดงานของผลิตภัณฑ์ไม่สำคัญต่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="71af7-152">กระบวนการที่มีอยู่ทั้งหมดที่เชื่อมโยงกับการจัดการใบสั่งชนิดนี้ในระบบยังคงไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="71af7-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="71af7-153">ไม่จำเป็นต้องมีข้อควรพิจารณาเพิ่มเติมในส่วนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="71af7-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="71af7-154">**ป้อนรายละเอียดใบสั่งและจองหมายเลขชุดงานที่ระบุ** – ควรใช้วิธีการนี้เมื่อลูกค้าร้องขอชุดงานหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="71af7-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="71af7-155">โดยทั่วไปแล้ว ลูกค้าจะร้องขอชุดงานหนึ่งๆ เมื่อมีการสั่งซื้อผลิตภัณฑ์ซ้ำที่พวกเขาซื้อก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="71af7-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="71af7-156">ชนิดของการจองเฉพาะชุดงานนี้เรียกว่า *การจองสินค้าที่กำหนดให้กับใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="71af7-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="71af7-157">ชุดของกฎต่อไปนี้จะมีผลบังคับใช้เมื่อมีการประมวลผลปริมาณ และมีการกำหนดหมายเลขชุดงานให้กับใบสั่งที่ระบุ:</span><span class="sxs-lookup"><span data-stu-id="71af7-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="71af7-158">ถ้าต้องการอนุญาตให้มีการจองหมายเลขชุดงานเฉพาะสำหรับสินค้าภายใต้นโยบายการจอง "\[สถานที่\] ด้านล่างชุดงาน" ระบบจะต้องจองมิติทั้งหมดไปจนถึงสถานที่</span><span class="sxs-lookup"><span data-stu-id="71af7-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="71af7-159">โดยทั่วไป ช่วงนี้จะประกอบด้วยมิติป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="71af7-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="71af7-160">คำสั่งสถานที่ไม่ถูกใช้เมื่อมีการสร้างงานการเบิกสินค้าสำหรับรายการการขายที่ใช้การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="71af7-161">ในระหว่างการประมวลผลคลังสินค้าของงานสำหรับชุดงานที่กำหนดให้กับใบสั่ง ไม่อนุญาตทั้งผู้ใช้และระบบให้สามารถเปลี่ยนหมายเลขชุดงานได้</span><span class="sxs-lookup"><span data-stu-id="71af7-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="71af7-162">(การประมวลผลนี้รวมถึงการจัดการข้อยกเว้น)</span><span class="sxs-lookup"><span data-stu-id="71af7-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="71af7-163">ตัวอย่างต่อไปนี้แสดงโฟลว์ที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="71af7-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="71af7-164">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="71af7-164">Example scenario</span></span>

<span data-ttu-id="71af7-165">สำหรับตัวอย่างนี้ ต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องใช้บริษัทข้อมูลสาธิต **USMF**</span><span class="sxs-lookup"><span data-stu-id="71af7-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="71af7-166">ตั้งค่าลำดับชั้นการจองสินค้าคงคลังเพื่ออนุญาตให้มีการจองเฉพาะชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="71af7-167">ไปที่ **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **สินค้าคงคลัง \> ลำดับชั้นการจอง**</span><span class="sxs-lookup"><span data-stu-id="71af7-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="71af7-168">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="71af7-168">Select **New**.</span></span>
3. <span data-ttu-id="71af7-169">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อ (ตัวอย่างเช่น **BatchFlex**)</span><span class="sxs-lookup"><span data-stu-id="71af7-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="71af7-170">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย (ตัวอย่างเช่น **ชุดงานด้านล่างมีความยืดหยุ่น**)</span><span class="sxs-lookup"><span data-stu-id="71af7-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="71af7-171">ในฟิลด์ **ที่เลือก** ให้เลือก **หมายเลขลำดับประจำสินค้า** และ **เจ้าของ** และจากนั้น เลือกปุ่มลูกศรซ้ายเพื่อย้ายไปยังฟิลด์ **ที่พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="71af7-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="71af7-172">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="71af7-172">Select **OK**.</span></span>
7. <span data-ttu-id="71af7-173">ในแถวสำหรับระดับมิติ **หมายเลขชุดงาน** ให้เลือกกล่องกาเครื่องหมาย **อนุญาตให้มีการจองสินค้าตามความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="71af7-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="71af7-174">ระดับ **ป้ายทะเบียน** และ **สถานที่** จะถูกเลือกโดยอัตโนมัติ และคุณไม่สามารถยกเลิกการเลือกกล่องกาเครื่องหมายดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="71af7-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="71af7-175">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="71af7-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="71af7-176">สร้างผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-176">Create a new released product</span></span>

1. <span data-ttu-id="71af7-177">ตั้งค่าพารามิเตอร์ข้อมูลหลักสามรายการของผลิตภัณฑ์โดยใช้ค่าเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="71af7-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="71af7-178">ในฟิลด์ **กลุ่มมิติการจัดเก็บ** เลือก **Ware**</span><span class="sxs-lookup"><span data-stu-id="71af7-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="71af7-179">ในฟิลด์ **กลุ่มมิติการติดตาม** เลือก **ชุดงาน-Phy**</span><span class="sxs-lookup"><span data-stu-id="71af7-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="71af7-180">ในฟิลด์ **ลำดับชั้นการจอง** เลือก **BatchFlex**</span><span class="sxs-lookup"><span data-stu-id="71af7-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="71af7-181">สร้างหมายเลขชุดงานสองหมายเลข เช่น **B11** และ **B22**</span><span class="sxs-lookup"><span data-stu-id="71af7-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="71af7-182">เพิ่มปริมาณสินค้าไปยังสต็อกคงคลังคงเหลือโดยใช้ค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="71af7-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="71af7-183">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-183">Warehouse</span></span> | <span data-ttu-id="71af7-184">หมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-184">Batch number</span></span> | <span data-ttu-id="71af7-185">สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="71af7-185">Location</span></span> | <span data-ttu-id="71af7-186">ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="71af7-186">License plate</span></span> | <span data-ttu-id="71af7-187">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="71af7-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="71af7-188">24</span><span class="sxs-lookup"><span data-stu-id="71af7-188">24</span></span>        | <span data-ttu-id="71af7-189">B11</span><span class="sxs-lookup"><span data-stu-id="71af7-189">B11</span></span>          | <span data-ttu-id="71af7-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="71af7-190">BULK-001</span></span> | <span data-ttu-id="71af7-191">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="71af7-191">None</span></span>          | <span data-ttu-id="71af7-192">10</span><span class="sxs-lookup"><span data-stu-id="71af7-192">10</span></span>       |
    | <span data-ttu-id="71af7-193">24</span><span class="sxs-lookup"><span data-stu-id="71af7-193">24</span></span>        | <span data-ttu-id="71af7-194">B11</span><span class="sxs-lookup"><span data-stu-id="71af7-194">B11</span></span>          | <span data-ttu-id="71af7-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="71af7-195">FL-001</span></span>   | <span data-ttu-id="71af7-196">LP11</span><span class="sxs-lookup"><span data-stu-id="71af7-196">LP11</span></span>          | <span data-ttu-id="71af7-197">10</span><span class="sxs-lookup"><span data-stu-id="71af7-197">10</span></span>       |
    | <span data-ttu-id="71af7-198">24</span><span class="sxs-lookup"><span data-stu-id="71af7-198">24</span></span>        | <span data-ttu-id="71af7-199">B22</span><span class="sxs-lookup"><span data-stu-id="71af7-199">B22</span></span>          | <span data-ttu-id="71af7-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="71af7-200">FL-002</span></span>   | <span data-ttu-id="71af7-201">LP22</span><span class="sxs-lookup"><span data-stu-id="71af7-201">LP22</span></span>          | <span data-ttu-id="71af7-202">10</span><span class="sxs-lookup"><span data-stu-id="71af7-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="71af7-203">ป้อนรายละเอียดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="71af7-203">Enter sales order details</span></span>

1. <span data-ttu-id="71af7-204">ไปที่ **การขายและการตลาด** \> **ใบสั่งขาย** \> **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="71af7-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="71af7-205">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="71af7-205">Select **New**.</span></span>
3. <span data-ttu-id="71af7-206">บนส่วนหัวของใบสั่งขาย ในฟิลด์ **บัญชีลูกค้า** ให้ป้อน **US-003**</span><span class="sxs-lookup"><span data-stu-id="71af7-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="71af7-207">เพิ่มรายการสำหรับสินค้าใหม่ และป้อน **10** เป็นปริมาณ</span><span class="sxs-lookup"><span data-stu-id="71af7-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="71af7-208">ตรวจสอบให้แน่ใจว่าฟิลด์ **คลังสินค้า** ถูกตั้งค่าเป็น **24**</span><span class="sxs-lookup"><span data-stu-id="71af7-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="71af7-209">บน FastTab **รายการใบสั่งขาย** ให้เลือก **สินค้าคงคลัง** และจากนั้น ในกลุ่ม **รักษา** ให้เลือก **การจองชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="71af7-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="71af7-210">หน้า **การจองชุดงาน** จะแสดงรายการของชุดงานที่พร้อมใช้งานสำหรับการจองสินค้าสำหรับรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="71af7-211">สำหรับตัวอย่างนี้ จะแสดงปริมาณเป็น **20** สำหรับหมายเลขชุดงาน **B11** และปริมาณเป็น **10** สำหรับหมายเลขชุดงาน **B22**</span><span class="sxs-lookup"><span data-stu-id="71af7-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="71af7-212">โปรดทราบว่าหน้า **การจองชุดงาน** ไม่สามารถเข้าถึงได้จากรายการ ถ้าสินค้าในรายการนั้นเชื่อมโยงกับลำดับชั้นการจอง "\[สถานที่\] ด้านล่างชุดงาน" ยกเว้นว่ามีการตั้งค่าไว้เพื่ออนุญาตให้มีการจองเฉพาะชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="71af7-213">เมื่อต้องการจองชุดงานหนึ่งๆ สำหรับใบสั่งขาย คุณต้องใช้หน้า **การจองชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="71af7-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="71af7-214">ถ้าคุณป้อนหมายเลขชุดงานโดยตรงบนรายการใบสั่งขาย ระบบจะทำงานราวกับว่าคุณป้อนค่าชุดงานที่ระบุสำหรับสินค้าที่ขึ้นกับนโยบายการจอง "\[สถานที่\] ด้านล่างชุดงาน"</span><span class="sxs-lookup"><span data-stu-id="71af7-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="71af7-215">เมื่อคุณบันทึกรายการ คุณจะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="71af7-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="71af7-216">ถ้าคุณยืนยันว่าควรมีการระบุหมายเลขชุดงานโดยตรงบนรายการใบสั่ง รายการจะไม่ได้รับการจัดการโดยตรรกะการจัดการคลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="71af7-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="71af7-217">ถ้าคุณจองปริมาณจากหน้า **การจอง** จะไม่มีการจองชุดงานที่ระบุ และการดำเนินงานของคลังสินค้าสำหรับรายการจะเป็นไปตามกฎที่เกี่ยวข้องภายใต้นโยบายการจอง "\[สถานที่\] ชุดงานด้านล่าง"</span><span class="sxs-lookup"><span data-stu-id="71af7-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="71af7-218">โดยทั่วไป หน้านี้ทำงานและถูกโต้ตอบในลักษณะเดียวกับที่ทำงานและถูกโต้ตอบสำหรับสินค้าที่มีลำดับชั้นการจองที่เกี่ยวข้องของชนิด "\[สถานที่\] เหนือชุดงาน"</span><span class="sxs-lookup"><span data-stu-id="71af7-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="71af7-219">อย่างไรก็ตาม นำข้อยกเว้นต่อไปนี้ไปใช้:</span><span class="sxs-lookup"><span data-stu-id="71af7-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="71af7-220">FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** แสดงหมายเลขชุดงานที่ถูกจองไว้สำหรับรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="71af7-221">ค่าชุดงานในกริดจะแสดงขึ้นตลอดทั้งวงจรของรายการใบสั่ง ซึ่งรวมถึงขั้นตอนการประมวลผลคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="71af7-222">ในทางกลับกัน บน FastTab **ภาพรวม** การจองรายการใบสั่งปกติ (นั่นคือ การจองสินค้าที่ทำไว้สำหรับมิติด้านบนระดับ **สถานที่**) จะแสดงอยู่ในกริดจนถึงจุดเมื่อมีการสร้างงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="71af7-223">เอนทิตีงานจะควบคุมการจองรายการ และไม่มีการจองรายการปรากฏขึ้นบนหน้าอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="71af7-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="71af7-224">FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** ช่วยรับประกันว่าตัวประมวลผลใบสั่งขายสามารถดูหมายเลขชุดงานที่กำหนดให้กับใบสั่งของลูกค้าเมื่อใดก็ได้ในระหว่างรอบระยะเวลาไปจนถึงการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="71af7-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="71af7-225">นอกจากการจองชุดงานหนึ่งๆ แล้ว ผู้ใช้สามารถเลือกสถานที่และป้ายทะเบียนเฉพาะของชุดงาน แทนที่จะปล่อยให้ระบบเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="71af7-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="71af7-226">ความสามารถนี้เกี่ยวข้องกับการออกแบบกลไกการจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="71af7-227">ดังที่ได้กล่าวถึงก่อนหน้านี้ เมื่อมีการจองหมายเลขชุดงานสำหรับสินค้าภายใต้นโยบายการจอง "\[สถานที่\] ด้านล่างชุดงาน" ระบบจะต้องจองมิติทั้งหมดไปจนถึงสถานที่</span><span class="sxs-lookup"><span data-stu-id="71af7-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="71af7-228">ดังนั้น งานของคลังสินค้าจะมีมิติการจัดเก็บเดียวกันกับที่ถูกจองโดยผู้ใช้ที่ทำงานกับใบสั่ง และอาจไม่แสดงถึงการจัดเก็บสินค้าที่สะดวกเสมอ หรือแม้กระทั่งเป็นไปได้ สำหรับการดำเนินการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="71af7-229">ถ้าตัวประมวลผลใบสั่งตระหนักถึงข้อจำกัดของคลังสินค้า ตัวประมวลผลอาจต้องการเลือกสถานและป้ายทะเบียนเฉพาะด้วยตนเองเมื่อจองชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="71af7-230">ในกรณีนี้ ผู้ใช้ต้องใช้ฟังก์ชัน **แสดงมิติ** บนส่วนหัวของหน้า และต้องเพิ่มสถานที่และป้ายทะเบียนในกริดบน FastTab **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="71af7-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="71af7-231">บนหน้า **การจองชุดงาน** ให้เลือกรายการสำหรับชุดงาน **B11** และจากนั้น เลือก **รายการจอง**</span><span class="sxs-lookup"><span data-stu-id="71af7-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="71af7-232">ไม่มีตรรกะที่กำหนดสำหรับการกำหนดสถานที่และป้ายทะเบียนในระหว่างการจองสินค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="71af7-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="71af7-233">คุณสามารถป้อนปริมาณในฟิลด์ **การจอง** ด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="71af7-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="71af7-234">โปรดสังเกตว่า บน FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** ชุดงาน **B11** จะแสดงขึ้นเป็น **ผูกมัด**</span><span class="sxs-lookup"><span data-stu-id="71af7-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![การกำหนดหมายเลขชุดงานเฉพาะให้กับรายการใบสั่งขายบนหน้าการจองชุดงาน](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="71af7-236">การจองของปริมาณในรายการใบสั่งขายสามารถทำได้ในหลายชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="71af7-237">ในทำนองเดียวกัน คุณสามารถทำการจองชุดงานเดียวกันเทียบกับสถานที่และป้ายทะเบียนต่างๆ ได้ (ถ้ามีการเปิดใช้งานป้ายทะเบียนสำหรับสถานที่)</span><span class="sxs-lookup"><span data-stu-id="71af7-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="71af7-238">นอกจากนี้ การจองของชุดงานหนึ่งๆ สำหรับปริมาณในรายการใบสั่งขายยังสามารถเป็นรายการบางส่วนได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="71af7-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="71af7-239">ตัวอย่างเช่น ปริมาณรวม 100 หน่วยสามารถถูกจองได้ เพื่อให้ชุดงานหนึ่งๆ ถูกกำหนดเป็น 20 หน่วย ในขณะที่หน่วย 80 หน่วยถูกจองไว้ที่ไซต์และระดับคลังสินค้าสำหรับชุดงานใดๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="71af7-240">ในกรณีนี้ WMS จะจัดการกับการดำเนินการเบิกสินค้าโดยใช้รายการงานที่แยกต่างหากสองรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="71af7-241">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์** \> **ผลิตภัณฑ์** \> **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="71af7-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="71af7-242">เลือกสินค้าของคุณ แล้วจากนั้น เลือก **จัดการสินค้าคงคลัง** \> **ดู** \> **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="71af7-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![การจองที่ผูกมัดใบสั่งเป็นชนิดของธุรกรรมสินค้าคงคลัง](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="71af7-244">ตรวจทานธุรกรรมสินค้าคงคลังของสินค้าที่เกี่ยวข้องกับการจองใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="71af7-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="71af7-245">ธุรกรรมที่มีการตั้งค่าฟิลด์ **การอ้างอิง** เป็น **ใบสั่งขาย** และฟิลด์ **ออกใช้** ถูกตั้งค่าเป็น **ถูกจองจริง** แสดงถึงการจองจองสำหรับมิติสินค้าคงคลังที่อยู่เหนือระดับ **สถานที่**</span><span class="sxs-lookup"><span data-stu-id="71af7-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="71af7-246">ตามลำดับชั้นการจองสินค้าคงคลังของสินค้า มิติเหล่านั้นจะเป็นสถานะของไซต์ คลังสินค้า และสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="71af7-247">ธุรกรรมที่มีการตั้งค่าฟิลด์ **การอ้างอิง** เป็น **การจองที่ผูกมัดใบสั่ง** และฟิลด์ **ออกใช้** ถูกตั้งค่าเป็น **ถูกจองจริง** แสดงถึงการจองรายการใบสั่งสำหรับชุดงานเฉพาะและมิติสินค้าคงคลังที่อยู่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="71af7-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="71af7-248">ตามลำดับชั้นการจองสินค้าคงคลังของสินค้า มิติเหล่านั้นจะเป็นหมายเลขชุดงานและสถานที่</span><span class="sxs-lookup"><span data-stu-id="71af7-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="71af7-249">ในตัวอย่างนี้ สถานที่คือ **Bulk-001**</span><span class="sxs-lookup"><span data-stu-id="71af7-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="71af7-250">บนส่วนหวของใบสั่งขาย เลือก **คลังสินค้า** \> **การดำเนินการ** \> **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="71af7-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="71af7-251">ขณะนี้รายการใบสั่งถูกเวฟ และมีการสร้างจำนวนงานในศูนย์การผลิตและงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="71af7-252">ตรวจทานและประมวลผลงานของคลังสินค้าที่มีหมายเลขชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="71af7-253">บน FastTab **รายการใบสั่งขาย** เลือก **คลังสินค้า** \> **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="71af7-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="71af7-254">งานที่จัดการการดำเนินการเบิกสินค้าสำหรับปริมาณชุดงานที่ถูกกำหนดให้กับรายการใบสั่งขายจะมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="71af7-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="71af7-255">เมื่อต้องการสร้างงาน ระบบจะใช้เท็มเพลตงาน แต่ไม่ใช่คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="71af7-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="71af7-256">การตั้งค่ามาตรฐานทั้งหมดที่กำหนดไว้สำหรับเท็มเพลตงาน เช่น จำนวนรายการเบิกสินค้าสูงสุด หรือหน่วยวัดที่ระบุ จะถูกใช้เพื่อกำหนดว่าควรจะสร้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="71af7-257">อย่างไรก็ตาม กฎที่สัมพันธ์กับคำสั่งสถานที่สำหรับการระบุสถานที่เบิกสินค้าจะไม่ได้รับการพิจารณา เนื่องจากการจองที่กำหนดให้กับใบสั่งระบุมิติสินค้าคงคลังทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="71af7-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="71af7-258">มิติสินค้าคงคลังเหล่านั้นรวมถึงมิติที่ระดับการจัดเก็บคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="71af7-259">ดังนั้น งานจึงสืบทอดมิติเหล่านั้นโดยไม่มีการสอบถามคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="71af7-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="71af7-260">หมายเลขชุดงานไม่ได้แสดงอยู่บนรายการเบิกสินค้า (ตามที่เป็นกรณีของรายงานที่สร้างขึ้นสำหรับสินค้าที่มีลำดับชั้นการจอง "\[สถานที่\] ด้านบนชุดงาน") แต่หมายเลขชุดงาน "เริ่มต้น" และมิติการจัดเก็บอื่นทั้งหมดจะปรากฏบนธุรกรรมสินค้าคงคลังของรายการงานที่มีการอ้างอิงจากธุรกรรมสินค้าคงคลังที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="71af7-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![ธุรกรรมสินค้าคงคลังของคลังสินค้าสำหรับงานที่มีต้นกำเนิดมาจากการจองที่กำหนดให้กับใบสั่ง](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="71af7-262">หลังจากมีการสร้างงาน ธุรกรรมสินค้าคงคลังของสินค้าที่ซึ่งฟิลด์ **การอ้างอิง** ถูกตั้งค่าเป็น **การจองที่ผูกมัดใบสั่ง** จะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="71af7-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="71af7-263">ธุรกรรมสินค้าคงคลังที่ซึ่งฟิลด์ **การอ้างอิง** ถูกตั้งค่าเป็น **งาน** ขณะนี้มีการจองทางกายภาพในมิติสินค้าคงคลังของปริมาณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="71af7-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="71af7-264">การดำเนินงานของคลังสินค้าสามารถดำเนินการจัดการกับการดำเนินงานในลักษณะปกติได้</span><span class="sxs-lookup"><span data-stu-id="71af7-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="71af7-265">อย่างไรก็ตาม คำแนะนำบนอุปกรณ์เคลื่อนที่จะแนะนำผู้ปฏิบัติงานในการเลือกหมายเลขชุดงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="71af7-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="71af7-266">ในสภาพแวดล้อมของคลังสินค้าซึ่งสถานที่ที่ควบคุมป้ายทะเบียน หลังจากที่ผู้ปฏิบัติงานเข้าถึงสถานที่ที่จัดเก็บชุดงานเดียวกันบนป้ายทะเบียนหลายรายการ เขาหรือเธอสามารถเลือกจากป้ายทะเบียนใดๆ ที่ยังไม่ได้ถูกจองไว้แล้ว (ตัวอย่างเช่น โดยการจองสินค้าที่กำหนดให้กับใบสั่งอื่น หรืองานที่มีต้นกำเนิดมาจากการจองของชนิดนั้น)</span><span class="sxs-lookup"><span data-stu-id="71af7-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="71af7-267">ถ้าจะไม่สามารถเลือกที่จะเลือกจากสถานที่ที่ระบุไว้ในรายการงานได้ ตัวดำเนินการคลังสินค้าสามารถใช้หนึ่งในการดำเนินการต่อไปนี้ เพื่อเปลี่ยนเส้นทางการเบิกสินค้าของชุดงานที่ระบุจากสถานที่ที่มีความสะดวกมากขึ้น:</span><span class="sxs-lookup"><span data-stu-id="71af7-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="71af7-268">การดำเนินการ **แทนที่สถานที่** มาตรฐานบนอุปกรณ์เคลื่อนที่ (ซึ่งระบุว่ามีการเปิดใช้งานการตั้งค่า **อนุญาตการแทนที่สถานที่เบิกสินค้า** ของผู้ปฏิบัติงานคลังสินค้า)</span><span class="sxs-lookup"><span data-stu-id="71af7-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="71af7-269">การดำเนินการ **เปลี่ยนสถานที่** บนหน้า **รายละเอียดของรายการงาน**</span><span class="sxs-lookup"><span data-stu-id="71af7-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="71af7-270">บนอุปกรณ์เคลื่อนที่ ดำเนินการเบิกสินค้าและการใส่งานให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="71af7-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="71af7-271">ขณะนี้มีการเบิกปริมาณเท่ากับ **10** สำหรับหมายเลขชุดงาน **B11** สำหรับรายการใบสั่งขาย และวางในสถานที่ **Baydoor**</span><span class="sxs-lookup"><span data-stu-id="71af7-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="71af7-272">ณ จุดนี้ ก็พร้อมแล้วที่จะโหลดไปยังรถบรรทุกและส่งไปยังที่อยู่ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="71af7-273">การจัดการข้อยกเว้นของคลังสินค้าที่มีหมายเลขชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-273">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="71af7-274">งานของคลังสินค้าสำหรับหมายเลขชุดงานที่กำหนดให้กับใบสั่งของการเบิกสินค้า จะขึ้นอยู่กับการจัดการข้อยกเว้นของคลังสินค้ามาตรฐานเดียวกันและการดำเนินการที่เป็นงานปกติ</span><span class="sxs-lookup"><span data-stu-id="71af7-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="71af7-275">โดยทั่วไป คุณสามารถยกเลิกงานที่เปิดหรือรายการงาน ซึ่งอาจหยุดชะงักได้ เนื่องจากสถานที่ของผู้ใช้เต็ม ซึ่งอาจมีการเบิกสินค้าแบบสั้นและสามารถปรับปรุงได้เนื่องจากมีการเคลื่อนย้าย</span><span class="sxs-lookup"><span data-stu-id="71af7-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="71af7-276">ในทำนองเดียวกัน ปริมาณที่เบิกของงานที่เสร็จสมบูรณ์แล้วอาจลดลง หรือสามารถกลับรายการงานได้</span><span class="sxs-lookup"><span data-stu-id="71af7-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="71af7-277">กฎคีย์ต่อไปนี้จะใช้กับการดำเนินการการจัดการข้อยกเว้นเหล่านี้ทั้งหมด: ไม่สามารถแทนที่หมายเลขชุดงานที่จองไว้สำหรับลูกค้าด้วยหมายเลขชุดงานที่แตกต่างกันได้ แต่จะสามารถเปลี่ยนมิติการจัดเก็บ (สถานที่และป้ายทะเบียน) โดยใช้การอัพเดตด้วยตนเองโดยผู้ใช้ หรือการอัพเดตอัตโนมัติโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="71af7-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="71af7-278">การอัพเดตอัตโนมัติจะขึ้นอยู่กับการกำหนดมิติการจัดเก็บแบบสุ่มที่เหมือนกันซึ่งใช้เมื่อมีการจองชุดงานเฉพาะโดยอัตโนมัติ แต่ไม่มีการระบุมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="71af7-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="71af7-279">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="71af7-279">Example scenario</span></span>

<span data-ttu-id="71af7-280">ตัวอย่างของสถานการณ์จำลองนี้คือ สถานการณ์ที่งานที่เสร็จสมบูรณ์ก่อนหน้านี้ไม่ได้ถูกเบิกสินค้าโดยใช้ฟังก์ชัน **ลดปริมาณที่เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="71af7-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="71af7-281">ตัวอย่างนี้ยังคงเป็นตัวอย่างก่อนหน้านี้ในหัวข้อนี้ต่อไป</span><span class="sxs-lookup"><span data-stu-id="71af7-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="71af7-282">ไปที่ **การจัดการคลังสินค้า** \> **จำนวนงานในศูนย์การผลิต** \> **จำนวนงานในศูนย์การผลิตที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="71af7-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="71af7-283">เลือกจำนวนงานในศูนย์การผลิตที่สร้างขึ้นโดยสัมพันธ์กับการจัดส่งสินค้าของใบสั่งขายของคุณ</span><span class="sxs-lookup"><span data-stu-id="71af7-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="71af7-284">จาก FastTab **รายการใบสั่งจำนวนงานในศูนย์การผลิต** เลือก **ลดปริมาณที่เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="71af7-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="71af7-285">บนหน้า **ลดปริมาณที่เบิกสินค้า** ในฟิลด์ **ย้ายไปยังสถานที่** เลือก **FL-001**</span><span class="sxs-lookup"><span data-stu-id="71af7-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="71af7-286">ในฟิลด์ **ย้ายไปยังป้ายทะเบียน** เลือก **LP33**</span><span class="sxs-lookup"><span data-stu-id="71af7-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="71af7-287">ในกริด ในฟิลด์ **ปริมาณสินค้าคงคลังที่จะยกเลิกการเบิกสินค้า** ป้อน **10**</span><span class="sxs-lookup"><span data-stu-id="71af7-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="71af7-288">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="71af7-288">Select **OK**.</span></span>

<span data-ttu-id="71af7-289">ต่อไปนี้เป็นผลลัพธ์ของการดำเนินการยกเลิกการเบิกสินค้า:</span><span class="sxs-lookup"><span data-stu-id="71af7-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="71af7-290">สถานะของงานที่ปิดก่อนหน้านี้ถูกตั้งค่าเป็น **ยกเลิกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="71af7-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="71af7-291">งานใหม่ของชนิด **การเคลื่อนไหวของสินค้าคงคลัง** จะถูกสร้างขึ้นสำหรับปริมาณที่ไม่ได้เบิกสินค้าเท่ากับ **10** สำหรับหมายเลขชุดงาน **B11**</span><span class="sxs-lookup"><span data-stu-id="71af7-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="71af7-292">งานนี้แสดงถึงการเคลื่อนย้ายจากสถานที่ **Baydoor** ไปยังป้ายทะเบียน **LP33** ในสถานที่ **FL-001**</span><span class="sxs-lookup"><span data-stu-id="71af7-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="71af7-293">สถานะถูกตั้งค่าเป็น **ปิดแล้ว**</span><span class="sxs-lookup"><span data-stu-id="71af7-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="71af7-294">ระบบจองหมายเลขชุดงานที่ถูกสั่งในตอนแรกอีกครั้ง และกำหนดสถานที่และรหัสป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="71af7-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="71af7-295">(กระบวนการนี้เทียบเท่ากับการรันฟังก์ชัน **รายการจอง** สำหรับรายการใบสั่งสำหรับหมายเลขชุดงานที่ระบุ)</span><span class="sxs-lookup"><span data-stu-id="71af7-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="71af7-296">ด้วยเหตุนี้ ชุดงาน **B11** จึงถูกแสดงขึ้นตามที่กำหนดไว้ใน FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** ของหน้า **การจองชุดงาน** และฟิลด์ **การจอง** มีปริมาณเท่ากับ **10** สำหรับหมายเลขชุดงาน **B11**</span><span class="sxs-lookup"><span data-stu-id="71af7-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="71af7-297">นอกจากนี้ ฟิลด์ **สถานที่** ถูกตั้งค่าเป็น **FL-001** และฟิลด์ **ป้ายทะเบียน** ถูกตั้งค่าเป็น **LP11**</span><span class="sxs-lookup"><span data-stu-id="71af7-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="71af7-298">(คุณสามารถเพิ่มฟิลด์เหล่านี้ไปยังกริดได้ ถ้าไม่สามารถมองเห็นได้)</span><span class="sxs-lookup"><span data-stu-id="71af7-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="71af7-299">ตารางต่อไปนี้จะแสดงภาพรวมที่แสดงวิธีการที่ระบบจัดการการจองชุดงานที่กำหนดให้กับใบสั่งสำหรับการดำเนินการของคลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="71af7-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="71af7-300">เมื่อต้องการแปลเนื้อหาในตาราง สมมติว่ามีการรันการดำเนินการคลังสินค้าแต่ละรายการในบริบทของงานของคลังสินค้าที่มีอยู่ ซึ่งมีต้นกำเนิดมาจากการจองชุดงานที่กำหนดให้กับใบสั่ง หรือการดำเนินการของคลังสินค้าแต่ละรายการมีผลกระทบต่องานของชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="71af7-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="71af7-301">ในตารางเหล่านี้ คอลัมน์ "ปริมาณชุดงานพร้อมใช้งาน" บ่งชี้ว่าปริมาณชุดงานพร้อมใช้งานหรือไม่ นอกเหนือจากปริมาณที่จองไว้แล้วสำหรับการจองสินค้าที่กำหนดให้กับใบสั่งปัจจุบัน หรือจองแล้วโดยงานคลังสินค้าที่มีต้นกำเนิดมาจากการจองของชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="71af7-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="71af7-302">แทนที่สถานที่เบิกสินค้าในงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="71af7-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71af7-303">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="71af7-304">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="71af7-305">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-305">Key user steps</span></span></th>
<th><span data-ttu-id="71af7-306">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-306">Warehouse work</span></span></th>
<th><span data-ttu-id="71af7-307">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="71af7-308">ตัวเลือก <strong>อนุญาตการแทนที่สถานที่เบิกสินค้า</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="71af7-309">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-310">เลือกรายการเมนู <strong>แทนที่สถานที่</strong> บนแอปคลังสินค้า เมื่อคุณเริ่มต้นงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-310">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="71af7-311">เลือก <strong>แนะนำ</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="71af7-312">ยืนยันสถานที่ใหม่ที่แนะนำตามความพร้อมใช้งานของปริมาณของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-313">ในงานปัจจุบัน การดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="71af7-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="71af7-314">สถานที่ในรายการเบิกสินค้าจะถูกอัพเดตไปยังสถานที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="71af7-315">(ถ้าสถานที่มีการควบคุมป้ายทะเบียน ป้ายทะเบียนแบบสุ่มจะถูกกำหนดให้กับธุรกรรมสินค้าคงคลังของงาน และผู้ปฏิบัติงานสามารถเลือกจากป้ายทะเบียนใดๆ ที่มีปริมาณที่พร้อมใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="71af7-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="71af7-316">ถ้าพบปริมาณในป้ายทะเบียนมากกว่าหนึ่งป้ายในสถานที่ใหม่ รายการเบิกสินค้าดั้งเดิมจะถูกแบ่งออกเป็นหลายรายการเพื่อให้ตรงกับป้ายทะเบียนแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="71af7-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-317">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-318">จำนวน</span><span class="sxs-lookup"><span data-stu-id="71af7-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-319">เลือกรายการเมนู <strong>แทนที่สถานที่</strong> บนแอปคลังสินค้า เมื่อคุณเริ่มต้นงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-319">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="71af7-320">ป้อนสถานที่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="71af7-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-321">การดำเนินการ <strong>แทนที่สถานที่</strong> ไม่สามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="71af7-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="71af7-322">การทำงานล้มเหลว และข้อผิดพลาดแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="71af7-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="71af7-323">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="71af7-324">ปุ่มแบบเต็ม – แบ่งรายการงานเนื่องจากมีมากเกินไปบนสถานที่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="71af7-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71af7-325">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="71af7-326">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="71af7-327">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-327">Key user steps</span></span></th>
<th><span data-ttu-id="71af7-328">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-328">Warehouse work</span></span></th>
<th><span data-ttu-id="71af7-329">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="71af7-330">ตัวเลือก <strong>อนุญาตให้มีการแบ่งงาน</strong> ถูกเปิดใช้งานบนรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="71af7-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="71af7-331">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-332">เลือกรายการเมนู <strong>แบบเต็ม</strong> บนแอปคลังสินค้า เมื่อคุณประมวลผลงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-332">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="71af7-333">ในฟิลด์ <strong>ปริมาณการเบิกสินค้า</strong> ให้ป้อนปริมาณบางส่วนของการเบิกสินค้าที่จำเป็น เพื่อบ่งชี้ถึงกำลังการผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="71af7-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="71af7-334">ในงานปัจจุบัน ปริมาณจะถูกอัพเดตเป็นปริมาณคงเหลือที่ต้องมีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="71af7-335">มีการสร้างและปิดงานใหม่สำหรับปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="71af7-336">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="71af7-337">ลดปริมาณที่เบิกสินค้าของงานที่เสร็จสมบูรณ์ (จากจำนวนงานในศูนย์การผลิต)</span><span class="sxs-lookup"><span data-stu-id="71af7-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71af7-338">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="71af7-339">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="71af7-340">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-340">Key user steps</span></span></th>
<th><span data-ttu-id="71af7-341">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-341">Warehouse work</span></span></th>
<th><span data-ttu-id="71af7-342">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="71af7-343">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-343">Not applicable</span></span></td>
<td><span data-ttu-id="71af7-344">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-345">เปิดหน้า <strong>ลดปริมาณที่เบิกสินค้า</strong> จากรายการจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="71af7-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="71af7-346">ป้อนปริมาณทั้งหมดที่จะยกเลิกการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="71af7-347">เลือก "ย้ายไปที่" สถานที่/ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="71af7-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="71af7-348">งานที่เชื่อมโยงกับรายการจำนวนงานในศูนย์การผลิตถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="71af7-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="71af7-349">มีการสร้างและปิดงานใหม่สำหรับความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-350">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-351">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-352">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-352">No</span></span></td>
<td><span data-ttu-id="71af7-353">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-353">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-354">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-354">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-355">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับสถานที่เก็บและป้ายทะเบียนเดียวกัน (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ถูกป้อนไว้ในระหว่างการยกเลิกการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="71af7-356">ย้ายสินค้าภายในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="71af7-357">การดำเนินการของคลังสินค้านี้ใช้ได้กับการเคลื่อนย้ายของชนิด **กระบวนการสร้างงาน** เท่านั้น ไม่ใช่การเคลื่อนย้ายโดยเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="71af7-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71af7-358">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="71af7-359">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="71af7-360">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-360">Key user steps</span></span></th>
<th><span data-ttu-id="71af7-361">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-361">Warehouse work</span></span></th>
<th><span data-ttu-id="71af7-362">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="71af7-363">ตัวเลือก <strong>อนุญาตการเคลื่อนย้ายสินค้าคงคลังที่มีงานที่เชื่อมโยง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="71af7-364">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-365">เริ่มต้นการเคลื่อนไหวบนแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-365">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="71af7-366">ป้อนสถานที่ "ตั้งต้น" และ "สิ้นสุด"</span><span class="sxs-lookup"><span data-stu-id="71af7-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="71af7-367">ในงานที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการย้าย สถานที่เบิกสินค้าจะถูกอัพเดตเป็นสถานที่ "สิ้นสุด" ใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="71af7-368">มีการสร้างและปิดงานใหม่สำหรับความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-369">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการเคลื่อนย้ายปริมาณจากสถานที่ที่กำหนดจะถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-370">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-371">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-371">No</span></span></td>
<td><span data-ttu-id="71af7-372">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-372">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-373">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-373">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-374">การจองที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการเคลื่อนไหวของปริมาณจากสถานที่ที่กำหนดจะถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับที่ตั้งและป้ายทะเบียน "สิ้นสุด" ใหม่ (ถ้าสถานที่มีการควบคุมป้ายทะเบียน)</span><span class="sxs-lookup"><span data-stu-id="71af7-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="71af7-375">กลับรายการปริมาณที่เบิกสินค้าของงานที่เสร็จสมบูรณ์ (จากจำนวนงานในศูนย์การผลิตหรือเวฟ)</span><span class="sxs-lookup"><span data-stu-id="71af7-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71af7-376">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="71af7-377">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="71af7-378">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-378">Key user steps</span></span></th>
<th><span data-ttu-id="71af7-379">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-379">Warehouse work</span></span></th>
<th><span data-ttu-id="71af7-380">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="71af7-381">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-381">Not applicable</span></span></td>
<td><span data-ttu-id="71af7-382">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-383">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="71af7-384">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>ปล่อยสินค้าไว้ที่สถานที่ปัจจุบัน</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-385">งานทั้งหมดที่เชื่อมโยงกับจำนวนงานในศูนย์การผลิตถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="71af7-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="71af7-386">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-387">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-388">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-388">No</span></span></td>
<td><span data-ttu-id="71af7-389">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-389">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-390">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-390">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-391">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับสถานที่และป้ายทะเบียนที่ปริมาณถูกเหลือเมื่อมีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-392">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-393">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="71af7-394">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>กำหนดสินค้าไปยังสถานที่นี้</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="71af7-395">งานปัจจุบันถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="71af7-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="71af7-396">มีการสร้างและปิดงานใหม่สำหรับความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-397">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-398">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-399">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-399">No</span></span></td>
<td><span data-ttu-id="71af7-400">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-400">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-401">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-401">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-402">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับสถานที่และป้ายทะเบียนที่ปริมาณถูกกำหนดให้เมื่อมีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-403">ใช่/ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-404">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="71af7-405">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>ย้ายสินค้าไปยังสถานที่นี้</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-406">ไม่ได้สนับสนุนการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="71af7-407">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-408">ใช่/ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-409">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="71af7-410">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>ย้ายสินค้าตามคำสั่งสถานที่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-411">ไม่ได้สนับสนุนการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="71af7-412">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="71af7-413">การเบิกปริมาณที่ขาด – ลงทะเบียนปริมาณที่ไม่ได้ถูกพบในสถานที่/ป้ายทะเบียน ในขณะที่คุณดำเนินงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71af7-414">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="71af7-415">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="71af7-416">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-416">Key user steps</span></span></th>
<th><span data-ttu-id="71af7-417">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-417">Warehouse work</span></span></th>
<th><span data-ttu-id="71af7-418">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="71af7-419">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ไม่มี</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ไม่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="71af7-420">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-421">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปคลังสินค้า เมื่อคุณเรียกใช้การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-421">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="71af7-422">ในฟิลด์ <strong>ปริมาณการเบิกสินค้า</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="71af7-423">ในฟิลด์ <strong>เหตุผล</strong> ป้อน <strong>ไม่มีการปันส่วนใหม่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="71af7-424">งานปัจจุบันถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="71af7-425">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="71af7-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-426">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-427">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-428">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-428">No</span></span></td>
<td><span data-ttu-id="71af7-429">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71af7-430">การดำเนินการเบิกสินค้าที่ขาดล้มเหลว และมีการแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="71af7-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="71af7-431">งานปัจจุบันยังคงเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="71af7-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-432">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="71af7-433">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ไม่มี</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ใช่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="71af7-434">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-435">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปคลังสินค้า เมื่อคุณเรียกใช้การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-435">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="71af7-436">ในฟิลด์ <strong>ปริมาณการเบิกสินค้า</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="71af7-437">ในฟิลด์ <strong>เหตุผล</strong> ป้อน <strong>ไม่มีการปันส่วนใหม่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="71af7-438">งานปัจจุบันถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="71af7-439">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="71af7-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-440">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการปรับปรุงปริมาณในสถานที่ที่เบิกสินค้าที่ขาดสำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-441">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-442">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-442">No</span></span></td>
<td><span data-ttu-id="71af7-443">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-443">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-444">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-444">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-445">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการปรับปรุงปริมาณในสถานที่ที่เบิกสินค้าที่ขาดจะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="71af7-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-446">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ด้วยตนเอง</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ไม่/ใช่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="71af7-447">นอกจากนี้ ตัวเลือก <strong>อนุญาตการปันส่วนสินค้าด้วยตนเอง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="71af7-448">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-449">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปคลังสินค้า เมื่อคุณเรียกใช้การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-449">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="71af7-450">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="71af7-451">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนด้วยตนเอง</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="71af7-452">เลือกสถานที่/ป้ายทะเบียนในรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="71af7-453">ในงานปัจจุบัน การดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="71af7-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="71af7-454">รายการเบิกสินค้าถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="71af7-455">รายการส่งสินค้าถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="71af7-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="71af7-456">จะมีการสร้างรายการเบิกสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-456">A new pick line is created.</span></span> <span data-ttu-id="71af7-457">ซึ่งใช้สถานที่/ป้ายทะเบียนที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="71af7-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="71af7-458">จะมีการสร้างรายการส่งสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="71af7-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="71af7-459">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="71af7-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-460">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-461">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ด้วยตนเอง</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ไม่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="71af7-462">นอกจากนี้ ตัวเลือก <strong>อนุญาตการปันส่วนสินค้าด้วยตนเอง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="71af7-463">จำนวน</span><span class="sxs-lookup"><span data-stu-id="71af7-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-464">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปคลังสินค้า เมื่อคุณเรียกใช้การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-464">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="71af7-465">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="71af7-466">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนด้วยตนเอง</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-467">การดำเนินการเบิกสินค้าที่ขาดล้มเหลว และมีการแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="71af7-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="71af7-468">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-469">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ด้วยตนเอง</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ใช่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="71af7-470">นอกจากนี้ ตัวเลือก <strong>อนุญาตการปันส่วนสินค้าด้วยตนเอง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="71af7-471">จำนวน</span><span class="sxs-lookup"><span data-stu-id="71af7-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-472">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปคลังสินค้า เมื่อคุณเรียกใช้การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-472">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="71af7-473">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="71af7-474">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนด้วยตนเอง</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="71af7-475">เลือกสถานที่/ป้ายทะเบียนในรายการ</span><span class="sxs-lookup"><span data-stu-id="71af7-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="71af7-476">ในงานปัจจุบัน การดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="71af7-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="71af7-477">รายการเบิกสินค้าถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="71af7-478">รายการส่งสินค้าถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="71af7-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="71af7-479">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="71af7-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="71af7-480">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการปรับปรุงปริมาณในสถานที่/ป้ายทะเบียนที่เบิกสินค้าที่ขาดจะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="71af7-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-481">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>อัตโนมัติ</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่/ไม่</strong> และ <strong>ลบการจอง</strong> = <strong>ใช่/ไม่</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="71af7-482">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="71af7-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-483">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปคลังสินค้า เมื่อคุณเรียกใช้การเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-483">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="71af7-484">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="71af7-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="71af7-485">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-486">การเบิกสินค้าที่ขาดที่เกี่ยวข้องกับการปันผลอัตโนมัติไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="71af7-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="71af7-487">การเบิกสินค้าที่ขาดที่เกี่ยวข้องกับการปันผลอัตโนมัติไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="71af7-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="71af7-488">เปลี่ยนสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="71af7-489">การดำเนินการคลังสินค้านี้สามารถดำเนินการได้จากจุดป้อนข้อมูลหลายจุด</span><span class="sxs-lookup"><span data-stu-id="71af7-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="71af7-490">ตัวอย่างที่แสดงไว้ที่นี่ใช้การดำเนินการ **การเปลี่ยนสถานะสินค้าคงคลัง** ในหน้า **คงเหลือตามสถานที่**</span><span class="sxs-lookup"><span data-stu-id="71af7-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71af7-491">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="71af7-492">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="71af7-493">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="71af7-493">Key user steps</span></span></th>
<th><span data-ttu-id="71af7-494">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-494">Warehouse work</span></span></th>
<th><span data-ttu-id="71af7-495">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="71af7-496">บนแท็บ <strong>คลังสินค้า</strong> ในเรกคอร์ด <strong>คลังสินค้า</strong> ฟิลด์ <strong>ลบการจองและการทำเครื่องหมาย</strong> ถูกตั้งค่าเป็น <strong>การจอง</strong> หรือ <strong>การเลือกและการจอง</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="71af7-497">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-498">เลือกสถานที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="71af7-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="71af7-499">เลือกรายการที่มีสินค้า สถานที่ และป้ายทะเบียนเฉพาะ (ถ้าสถานที่มีการควบคุมป้ายทะเบียน)</span><span class="sxs-lookup"><span data-stu-id="71af7-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="71af7-500">เลือก <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="71af7-501">ตั้งค่าฟิลด์ <strong>สถานะของสินค้าคงคลัง</strong> เป็น <strong>การบล็อค</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-502">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71af7-503">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-504">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="71af7-505">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong> สองรายการ เพื่อแสดงถึงการเปลี่ยนแปลงในมิติสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="71af7-506">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การบล็อคสินค้าคงคลัง</strong> และมีการสร้างชนิดการตัดสินค้าจากคลังของ <strong>ถูกจองจริง</strong> เพื่อแสดงการจองของปริมาณที่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="71af7-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71af7-507">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-507">No</span></span></td>
<td><span data-ttu-id="71af7-508">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-508">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-509">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71af7-510">การสำรองสินค้าจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="71af7-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="71af7-511">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong> สองรายการ เพื่อแสดงถึงการเปลี่ยนแปลงในมิติสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="71af7-512">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การบล็อคสินค้าคงคลัง</strong> และมีการสร้างชนิดการตัดสินค้าจากคลังของ <strong>ถูกจองจริง</strong> เพื่อแสดงการจองของปริมาณที่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="71af7-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="71af7-513">บนแท็บ <strong>คลังสินค้า</strong> ในเรกคอร์ด <strong>คลังสินค้า</strong> ฟิลด์ <strong>ลบการจองและการทำเครื่องหมาย</strong> ถูกตั้งค่าเป็น <strong>ไม่มี</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="71af7-514">ใช่</span><span class="sxs-lookup"><span data-stu-id="71af7-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71af7-515">เลือกสถานที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="71af7-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="71af7-516">เลือกรายการที่มีสินค้า สถานที่ และป้ายทะเบียนเฉพาะ (ถ้าสถานที่มีการควบคุมป้ายทะเบียน)</span><span class="sxs-lookup"><span data-stu-id="71af7-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="71af7-517">เลือก <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="71af7-518">ตั้งค่าฟิลด์ <strong>สถานะของสินค้าคงคลัง</strong> เป็น <strong>การบล็อค</strong></span><span class="sxs-lookup"><span data-stu-id="71af7-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="71af7-519">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="71af7-520">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71af7-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="71af7-521">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71af7-522">ไม่</span><span class="sxs-lookup"><span data-stu-id="71af7-522">No</span></span></td>
<td><span data-ttu-id="71af7-523">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="71af7-523">See the previous row.</span></span></td>
<td><span data-ttu-id="71af7-524">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="71af7-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="71af7-525">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="71af7-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="71af7-526">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="71af7-526">Limitations</span></span>

- <span data-ttu-id="71af7-527">ฟังก์ชันการจองมิติของระดับคลังสินค้าแบบยืดหยุ่นไม่สนับสนุนคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="71af7-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="71af7-528">การจัดการน้ำหนักจริง</span><span class="sxs-lookup"><span data-stu-id="71af7-528">Catch weight management</span></span>
    - <span data-ttu-id="71af7-529">สินค้าคงคลังค่าลบที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="71af7-529">Physical negative inventory</span></span>
    - <span data-ttu-id="71af7-530">การจองสินค้าเทียบกับการจัดหาวัสดุที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="71af7-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="71af7-531">ใบสั่งโอนย้ายและการเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="71af7-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="71af7-532">กฎการรวมคอนเทนเนอร์สำหรับการบรรจุตามหน่วยคำสั่งมีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="71af7-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="71af7-533">สำหรับการจองที่กำหนดให้กับใบสั่ง เราขอแนะนำว่าคุณไม่ควรใช้เท็มเพลตการสร้างคอนเทนเนอร์ที่ซึ่งฟิลด์ **บรรจุตามหน่วยคำสั่ง** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="71af7-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="71af7-534">ในการออกแบบปัจจุบัน คำสั่งสถานที่ไม่ได้ถูกใช้ เมื่อมีการสร้างงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="71af7-535">ดังนั้น จึงมีการใช้เฉพาะหน่วยที่ต่ำที่สุดในกลุ่มลำดับหน่วย (หน่วยสินค้าคงคลัง) ในระหว่างขั้นตอนการเวฟการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="71af7-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
