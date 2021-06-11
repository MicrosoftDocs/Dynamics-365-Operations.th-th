---
title: นโยบายการจองมิติในระดับคลังสินค้าที่ยืดหยุ่นได้
description: นี่จะอธิบายถึงนโยบายการจองสินค้าคงคลังที่ทำให้ธุรกิจซึ่งจำหน่ายผลิตภัณฑ์ที่มีการติดตามชุดงานและรันลอจิสติกส์ของตนเป็นการดำเนินงานที่เปิดใช้งาน WMS สามารถจองชุดงานเฉพาะสำหรับใบสั่งขายของลูกค้า ถึงแม้ว่าลำดับชั้นการจองที่เชื่อมโยงกับผลิตภัณฑ์จะไม่อนุญาตการจองของชุดงานเฉพาะ
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ed90e773e1b8c90afc119a471cf844941ad19226
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/26/2021
ms.locfileid: "6103057"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="cde33-103">นโยบายการจองในมิติระดับคลังสินค้าที่ยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="cde33-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cde33-104">เมื่อลำดับชั้นการจองสินค้าคงคลังของชนิด *ชุดงาน-ข้างล่าง\[สถานที่\]* เชื่อมโยงกับผลิตภัณฑ์ ธุรกิจที่ขายผลิตภัณฑ์ที่ติดตามชุดงานและรันลอจิสติกส์ของตนเป็นการดำเนินงานที่เปิดใช้งานสำหรับ Microsoft Dynamics 365 Warehouse Management System (WMS) จะไม่สามารถจองชุดเฉพาะของผลิตภัณฑ์เหล่านั้นสำหรับใบสั่งขายของลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="cde33-104">When an inventory reservation hierarchy of the *Batch-below\[location\]* type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="cde33-105">เช่นเดียวกับการที่ไม่สามารถจองป้ายทะเบียนสำหรับผลิตภัณฑ์ในใบสั่งขายได้ เมื่อผลิตภัณฑ์ดังกล่าวเชื่อมโยงกับลำดับชั้นการจองเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cde33-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="cde33-106">หัวข้อนี้จะอธิบายถึงนโยบายการจองสินค้าคงคลัง ซึ่งช่วยให้ธุรกิจเหล่านี้สามารถจองชุดงานหรือป้ายทะเบียนที่ระบุได้ แม้ว่าผลิตภัณฑ์จะเชื่อมโยงกับลำดับชั้นการจอง *ชุดงาน-ข้างล่าง\[สถานที่\]*</span><span class="sxs-lookup"><span data-stu-id="cde33-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a *Batch-below\[location\]* reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="cde33-107">ลำดับชั้นการจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="cde33-108">ส่วนนี้สรุปลำดับชั้นการจองสินค้าคงคลังที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="cde33-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="cde33-109">ลำดับชั้นการจองสินค้าคงคลังคาดการณ์ว่าหากมิติการจัดเก็บเกี่ยวข้องกับมิติการจัดเก็บ ใบสั่งความต้องการจะประกอบมิติบังคับของไซต์ คลังสินค้า และสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status.</span></span> <span data-ttu-id="cde33-110">กล่าวอีกอย่างคือ มิติบังคับคือมิติทั้งหมดที่อยู่เหนือมิติที่ตั้งในลำดับชั้นการจอง ขณะที่ตรรกะของคลังสินค้าจะรับผิดชอบการกําหนดสถานที่เก็บให้กับปริมาณที่ร้องขอและการจองสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="cde33-110">In other words, the mandatory dimensions are all the dimensions above the location dimension in the reservation hierarchy, while the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="cde33-111">ในการโต้ตอบระหว่างใบสั่งความต้องการและการดำเนินงานของคลังสินค้า มีการคาดว่าใบสั่งความต้องการจะบ่งชี้ว่าจะต้องมีการจัดส่งใบสั่งจากที่ใด (นั่นคือ ไซต์และคลังสินค้าใด)</span><span class="sxs-lookup"><span data-stu-id="cde33-111">In the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="cde33-112">คลังสินค้าจะพึ่งพาตรรกะเพื่อหาปริมาณที่ต้องการในสถานที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-112">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="cde33-113">อย่างไรก็ตาม เพื่อให้สะท้อนถึงแบบจำลองในการดำเนินงานของธุรกิจ มิติการติดตาม (ชุดงานและหมายเลขลำดับประจำสินค้า) จะขึ้นอยู่กับความยืดหยุ่นที่มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="cde33-113">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="cde33-114">ลำดับชั้นการจองสินค้าคงคลังสามารถรองรับสถานการณ์ที่เงื่อนไขต่อไปนี้มีผลบังคับใช้:</span><span class="sxs-lookup"><span data-stu-id="cde33-114">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="cde33-115">ธุรกิจอาศัยการดำเนินงานของคลังสินค้าเพื่อจัดการการเบิกสินค้าของปริมาณที่มีชุดงานหรือหมายเลขลำดับประจำสินค้า *หลังจาก* พบปริมาณในพื้นที่จัดเก็บคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-115">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *after* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="cde33-116">แบบจำลองนี้มักเรียกว่า *\[ตำแหน่ง\]ด้านล่างชุดงาน* หรือ *\[ตำแหน่ง\]ด้านล่างหมายเลขลำดับ*</span><span class="sxs-lookup"><span data-stu-id="cde33-116">This model is often referred to as *Batch-below\[location\]* or *Serial-below\[location\]*.</span></span> <span data-ttu-id="cde33-117">โดยทั่วไปจะใช้เมื่อชุดงานของผลิตภัณฑ์หรือหมายเลขลำดับประจำสินค้าไม่มีความสำคัญต่อลูกค้าที่วางความต้องการกับบริษัทผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="cde33-117">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="cde33-118">ธุรกิจอาศัยการดำเนินงานของคลังสินค้าเพื่อจัดการการเบิกสินค้าของปริมาณที่มีชุดงานหรือหมายเลขลำดับประจำสินค้า *ก่อน* พบปริมาณในพื้นที่จัดเก็บคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-118">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *before* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="cde33-119">ถ้าชุดงานหรือหมายเลขลำดับประจำสินค้าเป็นส่วนหนึ่งของข้อมูลจำเพาะของใบสั่งของลูกค้า และมีการบันทึกไว้ในใบสั่งความต้องการ การดำเนินงานคลังสินค้าที่ค้นหาปริมาณในคลังสินค้าไม่ได้รับอนุญาตให้เปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="cde33-119">If batch or serial numbers are necessary as part of a customer's order specification, they are recorded on the demand order, and the warehouse operations that find the quantities in the warehouse aren't allowed to change them.</span></span> <span data-ttu-id="cde33-120">แบบจำลองนี้เรียกว่า *\[ตำแหน่ง\]เหนือชุดงาน* หรือ *\[ตำแหน่ง\]เหนือหมายเลขลำดับ*</span><span class="sxs-lookup"><span data-stu-id="cde33-120">This model is referred to as *Batch-above\[location\]* or *Serial-above\[location\]*.</span></span> <span data-ttu-id="cde33-121">เนื่องจากมิติข้างต้นสถานที่เป็นความต้องการเฉพาะของความต้องการที่ต้องตอบสนอง ดังนั้นตรรกะของคลังสินค้าจะไม่ปันส่วน</span><span class="sxs-lookup"><span data-stu-id="cde33-121">Because the dimensions above location are the specific requirements for the demands that must be fulfilled, the warehouse logic won't allocate them.</span></span> <span data-ttu-id="cde33-122">ต้อง **ระบุ** มิติเหล่านี้เสมอบนใบสั่งความต้องการหรือในการจองที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cde33-122">These dimensions **must** always be specified on the demand order or in the related reservations.</span></span>

<span data-ttu-id="cde33-123">ในสถานการณ์เหล่านี้ ความท้าทายก็คือคุณสามารถกำหนดลำดับชั้นการจองสินค้าคงคลังเพียงหนึ่งรายการให้กับผลิตภัณฑ์ที่นำออกใช้แต่ละรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cde33-123">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="cde33-124">ดังนั้น สำหรับ WMS เพื่อจัดการสินค้าที่ติดตาม หลังจากการกำหนดลำดับชั้นจะกำหนดเมื่อต้องมีการจองชุดงานหรือหมายเลขลำดับประจำสินค้า (เมื่อมีการใช้ใบสั่งความต้องการ หรือระหว่างงานการเบิกสินค้าในคลังสินค้า) จะไม่สามารถเปลี่ยนแปลงช่วงเวลานี้บนพื้นฐานเฉพาะกิจได้</span><span class="sxs-lookup"><span data-stu-id="cde33-124">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="cde33-125">การจองสินค้าแบบยืดหยุ่นสำหรับสินค้าที่มีการติดตามชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-125">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="cde33-126">สถานการณ์จำลองทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="cde33-126">Business scenario</span></span>

<span data-ttu-id="cde33-127">ในสถานการณ์สมมตินี้ บริษัทใช้กลยุทธ์สินค้าคงคลังที่มีการติดตามสินค้าสำเร็จรูปโดยหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-127">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="cde33-128">นอกจากนี้ บริษัทนี้ยังใช้ปริมาณงาน WMS</span><span class="sxs-lookup"><span data-stu-id="cde33-128">This company also uses the WMS workload.</span></span> <span data-ttu-id="cde33-129">เนื่องจากปริมาณนี้มีตรรกะที่มีเครื่องมือที่ดีสำหรับการวางแผนและการรันการเบิกสินค้าและการดำเนินการจัดส่งสินค้าสำหรับสินค้าที่เปิดใช้งานชุดงานสินค้า ส่วนใหญ่ของสินค้าสำเร็จรูปเกี่ยวข้องกับลำดับชั้นการจองสินค้าคงคลัง *\[ตำแหน่ง\]ด้านล่างชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="cde33-129">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a *Batch-below\[location\]* inventory reservation hierarchy.</span></span> <span data-ttu-id="cde33-130">ข้อดีของการตั้งค่าการดำเนินงานชนิดนี้คือ การตัดสินใจ (ซึ่งคือการตัดสินใจในการจองอย่างมีประสิทธิภาพ) เกี่ยวกับชุดงานที่จะเบิกสินค้าและสถานที่เก็บสินค้าในคลังสินค้า จะถูกเลื่อนออกไปจนกว่าการดำเนินการเบิกสินค้าของคลังสินค้าจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cde33-130">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="cde33-131">ไม่มีการดำเนินการเมื่อมีการวางใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-131">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="cde33-132">ถึงแม้ว่าลำดับชั้นการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน* ตอบสนองต่อเป้าหมายธุรกิจของบริษัทเป็นอย่างดี ลูกค้าที่จัดตั้งขึ้นของบริษัทหลายรายต้องการชุดงานเดียวกันกับที่พวกเขาซื้อมาก่อนหน้านี้ เมื่อพวกเขาเรียงลำดับผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-132">Although the *Batch-below\[location\]* reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="cde33-133">ดังนั้น บริษัทกำลังมองหาความยืดหยุ่นในลักษณะที่มีการจัดการกฎการจองชุดงาน ดังนั้น ทั้งนี้ขึ้นอยู่กับความต้องการของลูกค้าสำหรับสินค้าเดียวกัน ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="cde33-133">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="cde33-134">คุณสามารถบันทึกหมายเลขชุดงานและสำรองไว้เมื่อใบสั่งนี้ถูกใช้โดยตัวประมวลผลการขาย และไม่สามารถเปลี่ยนแปลงได้ในระหว่างการดำเนินงานของคลังสินค้าและ/หรือถูกใช้โดยความต้องการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="cde33-134">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="cde33-135">ลักษณะการทำงานนี้ช่วยรับประกันได้ว่ามีการจัดส่งหมายเลขชุดงานที่สั่งให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-135">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="cde33-136">ถ้าหมายเลขชุดงานไม่ใช่สิ่งที่จำเป็นสำหรับลูกค้า การดำเนินงานคลังสินค้าสามารถกำหนดหมายเลขชุดงานในระหว่างการเบิกสินค้าได้ หลังจากดำเนินการลงทะเบียนใบสั่งขายและการจองสินค้าเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="cde33-136">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="cde33-137">การการอนุญาตการจองของชุดงานเฉพาะในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cde33-137">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="cde33-138">เพื่อให้เหมาะสมกับความยืดหยุ่นที่ต้องการในลักษณะการทำงานของการจองชุดงานสำหรับสินค้าที่เกี่ยวข้องกับลำดับชั้นการจองสินค้าคงคลัง *\[ตำแหน่ง\]ด้านล่างชุดงาน* ผู้จัดการสินค้าคงคลังจะต้องเลือกกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าในใบสั่งความต้องการ** สำหรับระดับ **หมายเลขชุดงาน** ในหน้า **ลำดับชั้นการจองสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="cde33-138">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a *Batch-below\[location\]* inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![การทำให้ลำดับชั้นการจองสินค้าคงคลังยืดหยุ่นได้](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="cde33-140">เมื่อมีการเลือกระดับ **หมายเลขชุดงาน** ในลำดับชั้น จะมีการเลือกมิติทั้งหมดด้านบนระดับนั้นและเพิ่มจนถึงระดับ **สถานที่** จะถูกเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cde33-140">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="cde33-141">(โดยค่าเริ่มต้น จะมีการเลือกมิติทั้งหมดที่อยู่เหนือระดับ **สถานที่** ไว้ล่วงหน้า) ลักษณะการทำงานนี้จะสะท้อนถึงตรรกะที่ซึ่งมิติทั้งหมดในช่วงระหว่างหมายเลขชุดงานและสถานที่จะถูกจองโดยอัตโนมัติ หลังจากที่คุณจองหมายเลขชุดงานเฉพาะในรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-141">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="cde33-142">กล่องกาเครื่องหมาย **อนุญาตให้จองสินค้าในใบสั่งความต้องการ** ใช่เฉพาะกับระดับของลำดับชั้นการจองที่อยู่ต่ำกว่ามิติสถานที่คลังสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cde33-142">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="cde33-143">**หมายเลขชุดงาน** และ **ป้ายทะเบียน** เป็นระดับเดียวในลำดับชั้นที่เปิดสำหรับนโยบายการจองแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="cde33-143">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="cde33-144">กล่าวคือ คุณไม่สามารถเลือกกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าในใบสั่งความต้องการ** สำหรับระดับ **สถานที่** หรือ **หมายเลขลำดับประจำสินค้า**</span><span class="sxs-lookup"><span data-stu-id="cde33-144">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="cde33-145">ถ้าลำดับชั้นการจองของคุณมีมิติหมายเลขลำดับประจำสินค้า (ซึ่งต้องอยู่ต่ำกว่าระดับ **หมายเลขชุดงาน** เสมอ) และถ้าคุณเปิดใช้งานการจองชุดงานเฉพาะสำหรับหมายเลขชุดงาน ระบบจะดำเนินการจัดการการจองหมายเลขลำดับประจำสินค้าและการดำเนินการเบิกสินค้า ตามกฎที่ใช้กับนโยบายการจอง *\[ตำแหน่ง\]ด้านล่างหมายเลขลำดับ*</span><span class="sxs-lookup"><span data-stu-id="cde33-145">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the *Serial-below\[location\]* reservation policy.</span></span>

<span data-ttu-id="cde33-146">เมื่อใดก็ตาม คุณสามารถอนุญาตให้มีการจองเฉพาะชุดงานสำหรับลำดับชั้นการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน* ที่มีอยู่ในการปรับใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde33-146">At any point, you can allow batch-specific reservation for an existing *Batch-below\[location\]* reservation hierarchy in your deployment.</span></span> <span data-ttu-id="cde33-147">การเปลี่ยนแปลงนี้จะไม่มีผลกระทบต่อการจองใดๆ และงานของคลังสินค้าที่เปิดซึ่งถูกสร้างก่อนที่จะเกิดการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="cde33-147">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="cde33-148">อย่างไรก็ตาม ไม่สามารถล้างกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าในใบสั่งความต้องการ** หากธุรกรรมสินค้าคงคลังของชนิดปัญหา **สั่งให้สำรอง** **ถูกจองจริง** หรือ **สั่งแล้ว** สำหรับสินค้าหนึ่งรายการขึ้นไปที่สัมพันธ์กับลำดับชั้นการจองนั้น</span><span class="sxs-lookup"><span data-stu-id="cde33-148">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="cde33-149">ถ้าลำดับชั้นการจองที่มีอยู่ของสินค้าไม่อนุญาตให้ใช้ข้อมูลจำเพาะของชุดงานในใบสั่ง คุณสามารถกำหนดอีกครั้งให้กับลำดับชั้นการจองที่อนุญาตให้ใช้ข้อมูลจำเพาะชุดงานได้ หากโครงสร้างระดับของลำดับชั้นเหมือนกันในลำดับชั้นทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-149">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="cde33-150">ใช้ฟังก์ชัน **เปลี่ยนแปลงลำดับชั้นการจองสินค้าสำหรับสินค้า** เพื่อทำการกำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-150">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="cde33-151">การเปลี่ยนแปลงนี้อาจเกี่ยวข้องเมื่อคุณต้องการป้องกันไม่ให้มีการจองชุดงานแบบยืดหยุ่นสำหรับชุดย่อยของสินค้าที่มีการติดตามชุดงาน แต่อนุญาตสำหรับส่วนที่เหลือของพอร์ตโฟลิโอผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cde33-151">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="cde33-152">ไม่ว่าคุณเลือกกล่องกาเครื่องหมาย **อนุญาตให้จองสินค้าในใบสั่งความต้องการ** หรือไม่ ถ้าคุณไม่ต้องการจองหมายเลขชุดงานเฉพาะสำหรับสินค้าในรายการใบสั่ง ตรรกะการดำเนินงานคลังสินค้าเริ่มต้นที่มีผลบังคับใช้สำหรับลำดับชั้นการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน* จะยังคงใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="cde33-152">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a *Batch-below\[location\]* reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="cde33-153">จองหมายเลขชุดงานเฉพาะสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-153">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="cde33-154">หลังจากที่มีการตั้งค่าลำดับชั้นการจองสินค้าคงคลังของ *\[ตำแหน่ง\]ด้านล่างชุดงาน* ของสินค้าที่ติดตามชุดงาน เพื่ออนุญาตให้มีการจองหมายเลขชุดงานเฉพาะบนใบสั่งขาย ตัวประมวลผลใบสั่งขายสามารถใช้ใบสั่งของลูกค้าสำหรับสินค้าเดียวกันได้ในวิธีใดวิธีหนึ่งต่อไปนี้ โดยขึ้นอยู่กับคำขอของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="cde33-154">After a batch-tracked item's *Batch-below\[location\]* inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="cde33-155">**ป้อนรายละเอียดใบสั่งโดยไม่มีการระบุหมายเลขชุดงาน** – ควรใช้วิธีการนี้เมื่อข้อมูลจำเพาะชุดงานของผลิตภัณฑ์ไม่สำคัญต่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-155">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="cde33-156">กระบวนการที่มีอยู่ทั้งหมดที่เชื่อมโยงกับการจัดการใบสั่งชนิดนี้ในระบบยังคงไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="cde33-156">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="cde33-157">ไม่จำเป็นต้องมีข้อควรพิจารณาเพิ่มเติมในส่วนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cde33-157">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="cde33-158">**ป้อนรายละเอียดใบสั่งและจองหมายเลขชุดงานที่ระบุ** – ควรใช้วิธีการนี้เมื่อลูกค้าร้องขอชุดงานหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="cde33-158">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="cde33-159">โดยทั่วไปแล้ว ลูกค้าจะร้องขอชุดงานหนึ่งๆ เมื่อมีการสั่งซื้อผลิตภัณฑ์ซ้ำที่พวกเขาซื้อก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="cde33-159">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="cde33-160">ชนิดของการจองเฉพาะชุดงานนี้เรียกว่า *การจองสินค้าที่กำหนดให้กับใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="cde33-160">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="cde33-161">ชุดของกฎต่อไปนี้จะมีผลบังคับใช้เมื่อมีการประมวลผลปริมาณ และมีการกำหนดหมายเลขชุดงานให้กับใบสั่งที่ระบุ:</span><span class="sxs-lookup"><span data-stu-id="cde33-161">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="cde33-162">ถ้าต้องการอนุญาตให้มีการจองหมายเลขชุดงานเฉพาะสำหรับสินค้าภายใต้นโยบายการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน* ระบบจะต้องจองมิติทั้งหมดไปจนถึงสถานที่</span><span class="sxs-lookup"><span data-stu-id="cde33-162">To allow reservation of a specific batch number for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="cde33-163">โดยทั่วไป ช่วงนี้จะประกอบด้วยมิติป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-163">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="cde33-164">คำสั่งสถานที่ไม่ถูกใช้เมื่อมีการสร้างงานการเบิกสินค้าสำหรับรายการการขายที่ใช้การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-164">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="cde33-165">ในระหว่างการประมวลผลคลังสินค้าของงานสำหรับชุดงานที่กำหนดให้กับใบสั่ง ไม่อนุญาตทั้งผู้ใช้และระบบให้สามารถเปลี่ยนหมายเลขชุดงานได้</span><span class="sxs-lookup"><span data-stu-id="cde33-165">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="cde33-166">(การประมวลผลนี้รวมถึงการจัดการข้อยกเว้น)</span><span class="sxs-lookup"><span data-stu-id="cde33-166">(This processing includes exception handling.)</span></span>

<span data-ttu-id="cde33-167">ตัวอย่างต่อไปนี้แสดงโฟลว์ที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="cde33-167">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="cde33-168">ตัวอย่างสถานการณ์จำลอง: การปันส่วนหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-168">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="cde33-169">สำหรับตัวอย่างนี้ ต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องใช้บริษัทข้อมูลสาธิต **USMF**</span><span class="sxs-lookup"><span data-stu-id="cde33-169">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="cde33-170">ตั้งค่าลำดับชั้นการจองสินค้าคงคลังเพื่ออนุญาตให้มีการจองเฉพาะชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-170">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="cde33-171">ไปที่ **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **สินค้าคงคลัง \> ลำดับชั้นการจอง**</span><span class="sxs-lookup"><span data-stu-id="cde33-171">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="cde33-172">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cde33-172">Select **New**.</span></span>
3. <span data-ttu-id="cde33-173">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อ (ตัวอย่างเช่น **BatchFlex**)</span><span class="sxs-lookup"><span data-stu-id="cde33-173">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="cde33-174">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย (ตัวอย่างเช่น **ชุดงานด้านล่างมีความยืดหยุ่น**)</span><span class="sxs-lookup"><span data-stu-id="cde33-174">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="cde33-175">ในฟิลด์ **ที่เลือก** ให้เลือก **หมายเลขลำดับประจำสินค้า** และ **เจ้าของ** และจากนั้น เลือกปุ่มลูกศรซ้ายเพื่อย้ายไปยังฟิลด์ **ที่พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-175">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="cde33-176">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cde33-176">Select **OK**.</span></span>
7. <span data-ttu-id="cde33-177">ในแถวสำหรับระดับมิติ **หมายเลขชุดงาน** ให้เลือกกล่องกาเครื่องหมาย **อนุญาตให้มีการจองสินค้าตามความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="cde33-177">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="cde33-178">ระดับ **ป้ายทะเบียน** และ **สถานที่** จะถูกเลือกโดยอัตโนมัติ และคุณไม่สามารถยกเลิกการเลือกกล่องกาเครื่องหมายดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="cde33-178">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="cde33-179">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cde33-179">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="cde33-180">สร้างผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-180">Create a new released product</span></span>

1. <span data-ttu-id="cde33-181">ตั้งค่าพารามิเตอร์ข้อมูลหลักสามรายการของผลิตภัณฑ์โดยใช้ค่าเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-181">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="cde33-182">ในฟิลด์ **กลุ่มมิติการจัดเก็บ** เลือก **Ware**</span><span class="sxs-lookup"><span data-stu-id="cde33-182">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="cde33-183">ในฟิลด์ **กลุ่มมิติการติดตาม** เลือก **ชุดงาน-Phy**</span><span class="sxs-lookup"><span data-stu-id="cde33-183">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="cde33-184">ในฟิลด์ **ลำดับชั้นการจอง** เลือก **BatchFlex**</span><span class="sxs-lookup"><span data-stu-id="cde33-184">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="cde33-185">สร้างหมายเลขชุดงานสองหมายเลข เช่น **B11** และ **B22**</span><span class="sxs-lookup"><span data-stu-id="cde33-185">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="cde33-186">เพิ่มปริมาณสินค้าไปยังสต็อกคงคลังคงเหลือโดยใช้ค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cde33-186">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="cde33-187">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-187">Warehouse</span></span> | <span data-ttu-id="cde33-188">หมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-188">Batch number</span></span> | <span data-ttu-id="cde33-189">สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="cde33-189">Location</span></span> | <span data-ttu-id="cde33-190">ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-190">License plate</span></span> | <span data-ttu-id="cde33-191">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="cde33-191">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="cde33-192">24</span><span class="sxs-lookup"><span data-stu-id="cde33-192">24</span></span>        | <span data-ttu-id="cde33-193">B11</span><span class="sxs-lookup"><span data-stu-id="cde33-193">B11</span></span>          | <span data-ttu-id="cde33-194">BULK-001</span><span class="sxs-lookup"><span data-stu-id="cde33-194">BULK-001</span></span> | <span data-ttu-id="cde33-195">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="cde33-195">None</span></span>          | <span data-ttu-id="cde33-196">10</span><span class="sxs-lookup"><span data-stu-id="cde33-196">10</span></span>       |
    | <span data-ttu-id="cde33-197">24</span><span class="sxs-lookup"><span data-stu-id="cde33-197">24</span></span>        | <span data-ttu-id="cde33-198">B11</span><span class="sxs-lookup"><span data-stu-id="cde33-198">B11</span></span>          | <span data-ttu-id="cde33-199">FL-001</span><span class="sxs-lookup"><span data-stu-id="cde33-199">FL-001</span></span>   | <span data-ttu-id="cde33-200">LP11</span><span class="sxs-lookup"><span data-stu-id="cde33-200">LP11</span></span>          | <span data-ttu-id="cde33-201">10</span><span class="sxs-lookup"><span data-stu-id="cde33-201">10</span></span>       |
    | <span data-ttu-id="cde33-202">24</span><span class="sxs-lookup"><span data-stu-id="cde33-202">24</span></span>        | <span data-ttu-id="cde33-203">B22</span><span class="sxs-lookup"><span data-stu-id="cde33-203">B22</span></span>          | <span data-ttu-id="cde33-204">FL-002</span><span class="sxs-lookup"><span data-stu-id="cde33-204">FL-002</span></span>   | <span data-ttu-id="cde33-205">LP22</span><span class="sxs-lookup"><span data-stu-id="cde33-205">LP22</span></span>          | <span data-ttu-id="cde33-206">10</span><span class="sxs-lookup"><span data-stu-id="cde33-206">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="cde33-207">ป้อนรายละเอียดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cde33-207">Enter sales order details</span></span>

1. <span data-ttu-id="cde33-208">ไปที่ **การขายและการตลาด** \> **ใบสั่งขาย** \> **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="cde33-208">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="cde33-209">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cde33-209">Select **New**.</span></span>
3. <span data-ttu-id="cde33-210">บนส่วนหัวของใบสั่งขาย ในฟิลด์ **บัญชีลูกค้า** ให้ป้อน **US-003**</span><span class="sxs-lookup"><span data-stu-id="cde33-210">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="cde33-211">เพิ่มรายการสำหรับสินค้าใหม่ และป้อน **10** เป็นปริมาณ</span><span class="sxs-lookup"><span data-stu-id="cde33-211">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="cde33-212">ตรวจสอบให้แน่ใจว่าฟิลด์ **คลังสินค้า** ถูกตั้งค่าเป็น **24**</span><span class="sxs-lookup"><span data-stu-id="cde33-212">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="cde33-213">บน FastTab **รายการใบสั่งขาย** ให้เลือก **สินค้าคงคลัง** และจากนั้น ในกลุ่ม **รักษา** ให้เลือก **การจองชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-213">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="cde33-214">หน้า **การจองชุดงาน** จะแสดงรายการของชุดงานที่พร้อมใช้งานสำหรับการจองสินค้าสำหรับรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-214">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="cde33-215">สำหรับตัวอย่างนี้ จะแสดงปริมาณเป็น **20** สำหรับหมายเลขชุดงาน **B11** และปริมาณเป็น **10** สำหรับหมายเลขชุดงาน **B22**</span><span class="sxs-lookup"><span data-stu-id="cde33-215">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="cde33-216">โปรดทราบว่าหน้า **การจองชุดงาน** ไม่สามารถเข้าถึงได้จากรายการ ถ้าสินค้าในรายการนั้นเชื่อมโยงกับลำดับชั้นการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน* ยกเว้นว่ามีการตั้งค่าไว้เพื่ออนุญาตให้มีการจองเฉพาะชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-216">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with *Batch-below\[location\]* reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cde33-217">เมื่อต้องการจองชุดงานหนึ่งๆ สำหรับใบสั่งขาย คุณต้องใช้หน้า **การจองชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-217">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="cde33-218">ถ้าคุณป้อนหมายเลขชุดงานโดยตรงบนรายการใบสั่งขาย ระบบจะทำงานราวกับว่าคุณป้อนค่าชุดงานที่ระบุสำหรับสินค้าที่ขึ้นกับนโยบายการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="cde33-218">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the *Batch-below\[location\]* reservation policy.</span></span> <span data-ttu-id="cde33-219">เมื่อคุณบันทึกรายการ คุณจะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="cde33-219">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="cde33-220">ถ้าคุณยืนยันว่าควรมีการระบุหมายเลขชุดงานโดยตรงบนรายการใบสั่ง รายการจะไม่ได้รับการจัดการโดยตรรกะการจัดการคลังสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="cde33-220">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="cde33-221">ถ้าคุณจองปริมาณจากหน้า **การจอง** จะไม่มีการจองชุดงานที่ระบุ และการดำเนินงานของคลังสินค้าสำหรับรายการจะเป็นไปตามกฎที่เกี่ยวข้องภายใต้นโยบายการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="cde33-221">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the *Batch-below\[location\]* reservation policy.</span></span>

    <span data-ttu-id="cde33-222">โดยทั่วไป หน้านี้ทำงานและถูกโต้ตอบในลักษณะเดียวกับที่ทำงานสำหรับสินค้าที่มีลำดับชั้นการจองที่เกี่ยวข้องของชนิด *\[ตำแหน่ง\]เหนือชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="cde33-222">In general, this page works and is interacted with in the same way for items that have an associated reservation hierarchy of the *Batch-above\[location\]* type.</span></span> <span data-ttu-id="cde33-223">อย่างไรก็ตาม นำข้อยกเว้นต่อไปนี้ไปใช้:</span><span class="sxs-lookup"><span data-stu-id="cde33-223">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="cde33-224">FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** แสดงหมายเลขชุดงานที่ถูกจองไว้สำหรับรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-224">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="cde33-225">ค่าชุดงานในกริดจะแสดงขึ้นตลอดทั้งวงจรของรายการใบสั่ง ซึ่งรวมถึงขั้นตอนการประมวลผลคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-225">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="cde33-226">ในทางกลับกัน บน FastTab **ภาพรวม** การจองรายการใบสั่งปกติ (นั่นคือ การจองสินค้าที่ทำไว้สำหรับมิติด้านบนระดับ **สถานที่**) จะแสดงอยู่ในกริดจนถึงจุดเมื่อมีการสร้างงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-226">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="cde33-227">เอนทิตีงานจะควบคุมการจองรายการ และไม่มีการจองรายการปรากฏขึ้นบนหน้าอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="cde33-227">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="cde33-228">FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** ช่วยรับประกันว่าตัวประมวลผลใบสั่งขายสามารถดูหมายเลขชุดงานที่กำหนดให้กับใบสั่งของลูกค้าเมื่อใดก็ได้ในระหว่างรอบระยะเวลาไปจนถึงการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cde33-228">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="cde33-229">นอกจากการจองชุดงานหนึ่งๆ แล้ว ผู้ใช้สามารถเลือกสถานที่และป้ายทะเบียนเฉพาะของชุดงาน แทนที่จะปล่อยให้ระบบเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cde33-229">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="cde33-230">ความสามารถนี้เกี่ยวข้องกับการออกแบบกลไกการจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-230">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="cde33-231">ดังที่ได้กล่าวถึงก่อนหน้านี้ เมื่อมีการจองหมายเลขชุดงานสำหรับสินค้าภายใต้นโยบายการจอง *\[ตำแหน่ง\]ด้านล่างชุดงาน* ระบบจะต้องจองมิติทั้งหมดไปจนถึงสถานที่</span><span class="sxs-lookup"><span data-stu-id="cde33-231">As was mentioned earlier, when a batch number is reserved for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="cde33-232">ดังนั้น งานของคลังสินค้าจะมีมิติการจัดเก็บเดียวกันกับที่ถูกจองโดยผู้ใช้ที่ทำงานกับใบสั่ง และอาจไม่แสดงถึงการจัดเก็บสินค้าที่สะดวกเสมอ หรือแม้กระทั่งเป็นไปได้ สำหรับการดำเนินการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-232">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="cde33-233">ถ้าตัวประมวลผลใบสั่งตระหนักถึงข้อจำกัดของคลังสินค้า ตัวประมวลผลอาจต้องการเลือกสถานและป้ายทะเบียนเฉพาะด้วยตนเองเมื่อจองชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-233">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="cde33-234">ในกรณีนี้ ผู้ใช้ต้องใช้ฟังก์ชัน **แสดงมิติ** บนส่วนหัวของหน้า และต้องเพิ่มสถานที่และป้ายทะเบียนในกริดบน FastTab **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="cde33-234">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="cde33-235">บนหน้า **การจองชุดงาน** ให้เลือกรายการสำหรับชุดงาน **B11** และจากนั้น เลือก **รายการจอง**</span><span class="sxs-lookup"><span data-stu-id="cde33-235">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="cde33-236">ไม่มีตรรกะที่กำหนดสำหรับการกำหนดสถานที่และป้ายทะเบียนในระหว่างการจองสินค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cde33-236">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="cde33-237">คุณสามารถป้อนปริมาณในฟิลด์ **การจอง** ด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="cde33-237">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="cde33-238">โปรดสังเกตว่า บน FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** ชุดงาน **B11** จะแสดงขึ้นเป็น **ผูกมัด**</span><span class="sxs-lookup"><span data-stu-id="cde33-238">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![การกำหนดหมายเลขชุดงานเฉพาะให้กับรายการใบสั่งขายบนหน้าการจองชุดงาน](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="cde33-240">การจองของปริมาณในรายการใบสั่งขายสามารถทำได้ในหลายชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-240">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="cde33-241">ในทำนองเดียวกัน คุณสามารถทำการจองชุดงานเดียวกันเทียบกับสถานที่และป้ายทะเบียนต่างๆ ได้ (ถ้ามีการเปิดใช้งานป้ายทะเบียนสำหรับสถานที่)</span><span class="sxs-lookup"><span data-stu-id="cde33-241">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="cde33-242">นอกจากนี้ การจองของชุดงานหนึ่งๆ สำหรับปริมาณในรายการใบสั่งขายยังสามารถเป็นรายการบางส่วนได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="cde33-242">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="cde33-243">ตัวอย่างเช่น ปริมาณรวม 100 หน่วยสามารถถูกจองได้ เพื่อให้ชุดงานหนึ่งๆ ถูกกำหนดเป็น 20 หน่วย ในขณะที่หน่วย 80 หน่วยถูกจองไว้ที่ไซต์และระดับคลังสินค้าสำหรับชุดงานใดๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-243">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="cde33-244">ในกรณีนี้ WMS จะจัดการกับการดำเนินการเบิกสินค้าโดยใช้รายการงานที่แยกต่างหากสองรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-244">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="cde33-245">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์** \> **ผลิตภัณฑ์** \> **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="cde33-245">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="cde33-246">เลือกสินค้าของคุณ แล้วจากนั้น เลือก **จัดการสินค้าคงคลัง** \> **ดู** \> **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="cde33-246">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![การจองที่ผูกมัดใบสั่งเป็นชนิดของธุรกรรมสินค้าคงคลัง](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="cde33-248">ตรวจทานธุรกรรมสินค้าคงคลังของสินค้าที่เกี่ยวข้องกับการจองใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cde33-248">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="cde33-249">ธุรกรรมที่มีการตั้งค่าฟิลด์ **การอ้างอิง** เป็น **ใบสั่งขาย** และฟิลด์ **ออกใช้** ถูกตั้งค่าเป็น **ถูกจองจริง** แสดงถึงการจองจองสำหรับมิติสินค้าคงคลังที่อยู่เหนือระดับ **สถานที่**</span><span class="sxs-lookup"><span data-stu-id="cde33-249">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="cde33-250">ตามลำดับชั้นการจองสินค้าคงคลังของสินค้า มิติเหล่านั้นจะเป็นสถานะของไซต์ คลังสินค้า และสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-250">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="cde33-251">ธุรกรรมที่มีการตั้งค่าฟิลด์ **การอ้างอิง** เป็น **การจองที่ผูกมัดใบสั่ง** และฟิลด์ **ออกใช้** ถูกตั้งค่าเป็น **ถูกจองจริง** แสดงถึงการจองรายการใบสั่งสำหรับชุดงานเฉพาะและมิติสินค้าคงคลังที่อยู่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="cde33-251">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="cde33-252">ตามลำดับชั้นการจองสินค้าคงคลังของสินค้า มิติเหล่านั้นจะเป็นหมายเลขชุดงานและสถานที่</span><span class="sxs-lookup"><span data-stu-id="cde33-252">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="cde33-253">ในตัวอย่างนี้ สถานที่คือ **Bulk-001**</span><span class="sxs-lookup"><span data-stu-id="cde33-253">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="cde33-254">บนส่วนหวของใบสั่งขาย เลือก **คลังสินค้า** \> **การดำเนินการ** \> **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="cde33-254">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="cde33-255">ขณะนี้รายการใบสั่งถูกเวฟ และมีการสร้างจำนวนงานในศูนย์การผลิตและงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-255">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="cde33-256">ตรวจทานและประมวลผลงานของคลังสินค้าที่มีหมายเลขชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-256">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="cde33-257">บน FastTab **รายการใบสั่งขาย** เลือก **คลังสินค้า** \> **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-257">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="cde33-258">งานที่จัดการการดำเนินการเบิกสินค้าสำหรับปริมาณชุดงานที่ถูกกำหนดให้กับรายการใบสั่งขายจะมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cde33-258">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="cde33-259">เมื่อต้องการสร้างงาน ระบบจะใช้เท็มเพลตงาน แต่ไม่ใช่คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="cde33-259">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="cde33-260">การตั้งค่ามาตรฐานทั้งหมดที่กำหนดไว้สำหรับเท็มเพลตงาน เช่น จำนวนรายการเบิกสินค้าสูงสุด หรือหน่วยวัดที่ระบุ จะถูกใช้เพื่อกำหนดว่าควรจะสร้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-260">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="cde33-261">อย่างไรก็ตาม กฎที่สัมพันธ์กับคำสั่งสถานที่สำหรับการระบุสถานที่เบิกสินค้าจะไม่ได้รับการพิจารณา เนื่องจากการจองที่กำหนดให้กับใบสั่งระบุมิติสินค้าคงคลังทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="cde33-261">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="cde33-262">มิติสินค้าคงคลังเหล่านั้นรวมถึงมิติที่ระดับการจัดเก็บคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-262">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="cde33-263">ดังนั้น งานจึงสืบทอดมิติเหล่านั้นโดยไม่มีการสอบถามคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="cde33-263">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="cde33-264">หมายเลขชุดงานไม่ได้แสดงอยู่บนรายการเบิกสินค้า (ตามที่เป็นกรณีของรายงานที่สร้างขึ้นสำหรับสินค้าที่มีลำดับชั้นการจอง *\[ตำแหน่ง\]ด้านบนชุดงาน*) แต่หมายเลขชุดงาน "เริ่มต้น" และมิติการจัดเก็บอื่นทั้งหมดจะปรากฏบนธุรกรรมสินค้าคงคลังของรายการงานที่มีการอ้างอิงจากธุรกรรมสินค้าคงคลังที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cde33-264">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated *Batch-above\[location\]* reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![ธุรกรรมสินค้าคงคลังของคลังสินค้าสำหรับงานที่มีต้นกำเนิดมาจากการจองที่กำหนดให้กับใบสั่ง](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="cde33-266">หลังจากมีการสร้างงาน ธุรกรรมสินค้าคงคลังของสินค้าที่ซึ่งฟิลด์ **การอ้างอิง** ถูกตั้งค่าเป็น **การจองที่ผูกมัดใบสั่ง** จะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="cde33-266">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="cde33-267">ธุรกรรมสินค้าคงคลังที่ซึ่งฟิลด์ **การอ้างอิง** ถูกตั้งค่าเป็น **งาน** ขณะนี้มีการจองทางกายภาพในมิติสินค้าคงคลังของปริมาณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cde33-267">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="cde33-268">การดำเนินงานของคลังสินค้าสามารถดำเนินการจัดการกับการดำเนินงานในลักษณะปกติได้</span><span class="sxs-lookup"><span data-stu-id="cde33-268">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="cde33-269">อย่างไรก็ตาม คำแนะนำบนอุปกรณ์เคลื่อนที่จะแนะนำผู้ปฏิบัติงานในการเลือกหมายเลขชุดงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="cde33-269">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="cde33-270">ในสภาพแวดล้อมของคลังสินค้าซึ่งสถานที่ที่ควบคุมป้ายทะเบียน หลังจากที่ผู้ปฏิบัติงานเข้าถึงสถานที่ที่จัดเก็บชุดงานเดียวกันบนป้ายทะเบียนหลายรายการ พวกเขาสามารถเลือกจากป้ายทะเบียนใดๆ ที่ยังไม่ได้ถูกจองไว้แล้ว (ตัวอย่างเช่น โดยการจองสินค้าที่กำหนดให้กับใบสั่งอื่น หรืองานที่มีต้นกำเนิดมาจากการจองของชนิดนั้น)</span><span class="sxs-lookup"><span data-stu-id="cde33-270">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, they can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="cde33-271">ถ้าจะไม่สามารถเลือกที่จะเลือกจากสถานที่ที่ระบุไว้ในรายการงานได้ ตัวดำเนินการคลังสินค้าสามารถใช้หนึ่งในการดำเนินการต่อไปนี้ เพื่อเปลี่ยนเส้นทางการเบิกสินค้าของชุดงานที่ระบุจากสถานที่ที่มีความสะดวกมากขึ้น:</span><span class="sxs-lookup"><span data-stu-id="cde33-271">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="cde33-272">การดำเนินการ **แทนที่สถานที่** มาตรฐานบนอุปกรณ์เคลื่อนที่ (ซึ่งระบุว่ามีการเปิดใช้งานการตั้งค่า **อนุญาตการแทนที่สถานที่เบิกสินค้า** ของผู้ปฏิบัติงานคลังสินค้า)</span><span class="sxs-lookup"><span data-stu-id="cde33-272">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="cde33-273">การดำเนินการ **เปลี่ยนสถานที่** บนหน้า **รายละเอียดของรายการงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-273">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="cde33-274">บนอุปกรณ์เคลื่อนที่ ดำเนินการเบิกสินค้าและการใส่งานให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="cde33-274">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="cde33-275">ขณะนี้มีการเบิกปริมาณเท่ากับ **10** สำหรับหมายเลขชุดงาน **B11** สำหรับรายการใบสั่งขาย และวางในสถานที่ **Baydoor**</span><span class="sxs-lookup"><span data-stu-id="cde33-275">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="cde33-276">ณ จุดนี้ ก็พร้อมแล้วที่จะโหลดไปยังรถบรรทุกและส่งไปยังที่อยู่ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-276">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="cde33-277">การจองป้ายทะเบียนแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="cde33-277">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="cde33-278">สถานการณ์จำลองทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="cde33-278">Business scenario</span></span>

<span data-ttu-id="cde33-279">ในสถานการณ์นี้ บริษัทจะใช้การจัดการคลังสินค้าและการประมวลผลงาน และจัดการการวางแผนการบรรทุกที่ระดับของแท่นวางสินค้า/ตู้บรรจุสินค้า แต่ละรายการนอก Supply Chain Management ก่อนที่จะมีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-279">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="cde33-280">บรรจุภัณฑ์เหล่านี้จะแสดงด้วยป้ายทะเบียนในมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-280">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="cde33-281">ดังนั้นในการทำเช่นนี้ จึงต้องกำหนดป้ายทะเบียนเฉพาะของใบสั่งขายให้กับบรรทัดใบสั่งขาย ก่อนที่จะทำงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-281">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="cde33-282">บริษัทกำลังมองหาความยืดหยุ่นในลักษณะที่กฎการจองป้ายทะเบียนมีการจัดการ เพื่อให้เกิดลักษณะการทำงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-282">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="cde33-283">คุณสามารถบันทึกป้ายทะเบียนและสำรองไว้เมื่อใบสั่งนี้ถูกใช้โดยตัวประมวลผลการขาย และไม่สามารถถูกใช้โดยความต้องการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="cde33-283">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="cde33-284">ลักษณะการทำงานนี้ช่วยรับประกันได้ว่ามีการจัดส่งป้ายทะเบียนที่วางแผนไว้ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-284">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="cde33-285">ถ้าป้ายทะเบียนยังไม่ได้รับการกำหนดให้กับบรรทัดใบสั่งขาย เจ้าหน้าที่คลังสินค้าสามารถเลือกป้ายทะเบียนในระหว่างงานการเบิกสินค้า หลังจากการลงทะเบียนใบสั่งขายและการจองเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cde33-285">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="cde33-286">เปิดการจองป้ายทะเบียนแบบยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="cde33-286">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="cde33-287">ก่อนที่คุณจะสามารถใช้การจองป้ายทะเบียนแบบยืดหยุ่น สองคุณลักษณะต้องถูกเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde33-287">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="cde33-288">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะนี้ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="cde33-288">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="cde33-289">คุณต้องเปิดคุณลักษณะตามลำดับต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cde33-289">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="cde33-290">**ชื่อคุณลักษณะ:** *การจองในมิติระดับคลังสินค้าที่ยืดหยุ่น*</span><span class="sxs-lookup"><span data-stu-id="cde33-290">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="cde33-291">**ชื่อคุณลักษณะ** *การจองป้ายทะเบียนตามใบสั่งแบบยืดหยุ่น*</span><span class="sxs-lookup"><span data-stu-id="cde33-291">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="cde33-292">จองป้ายทะเบียนเฉพาะในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cde33-292">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="cde33-293">เมื่อต้องการเปิดใช้งานการจองป้ายทะเบียนสำหรับใบสั่ง คุณต้องเลือกกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าตามใบสั่ง** สำหรับระดับ **ป้ายทะเบียน** บนหน้า **ลำดับชั้นการจองสินค้าคงคลัง** สำหรับลำดับชั้นที่สัมพันธ์กับสินค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cde33-293">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![หน้าลำดับชั้นการจองสินค้าคงคลัง สำหรับลำดับชั้นการจองป้ายทะเบียนแบบยืดหยุ่น](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="cde33-295">คุณสามารถเปิดใช้งานการจองป้ายทะเบียนสำหรับใบสั่งที่จุดใดก็ได้ในการปรับใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde33-295">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="cde33-296">การเปลี่ยนแปลงนี้จะไม่มีผลกระทบต่อการจองใด ๆ หรืองานของคลังสินค้าที่เปิดซึ่งถูกสร้างก่อนที่จะเกิดการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="cde33-296">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="cde33-297">อย่างไรก็ตาม คุณไม่สามารถล้างกล่องกาเครื่องหมาย **อนุญาตให้ทำการจองสินค้าในใบสั่งความต้องการ** ความเคลื่อนไหวของสินค้าคงคลังขาออกที่เปิดและมีสถานะ *อยู่ระหว่างการสั่ง* *สั่งที่จองไว้* หรือ *ถูกจองจริง* สำหรับสินค้าหนึ่งรายการขึ้นไปที่สัมพันธ์กับลำดับชั้นการจองนั้น</span><span class="sxs-lookup"><span data-stu-id="cde33-297">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="cde33-298">ถึงแม้ว่าจะมีการเลือกกล่องกาเครื่องหมาย **อนุญาตให้จองสินค้าสำหรับใบสั่งตามความต้องการ** สำหรับระดับ **ป้ายทะเบียน** ก็ยังคง *ไม่* จองป้ายทะเบียนโดยระบุตามใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="cde33-298">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="cde33-299">ในกรณีนี้ ตรรกะการดำเนินงานคลังสินค้าเริ่มต้นที่ใช้ได้สำหรับลำดับชั้นการจองจะมีผลบังคับ</span><span class="sxs-lookup"><span data-stu-id="cde33-299">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="cde33-300">เมื่อต้องการจองป้ายทะเบียนเฉพาะ คุณต้องใช้กระบวนการ [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md)</span><span class="sxs-lookup"><span data-stu-id="cde33-300">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.</span></span> <span data-ttu-id="cde33-301">ในโปรแกรมประยุกต์ คุณสามารถจองสินค้านี้จากใบสั่งขายได้โดยตรงโดยใช้ตัวเลือก **การจองที่ยืนยันใบสั่งต่อป้ายทะเบียน** ของคำสั่ง **เปิดใน Excel**</span><span class="sxs-lookup"><span data-stu-id="cde33-301">In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="cde33-302">ในข้อมูลเอนทิตี้ที่เปิดใน Excel add-in คุณต้องป้อนข้อมูลที่เกี่ยวข้องกับการจองต่อไปนี้แล้วเลือก **เผยแพร่** เพื่อส่งข้อมูลกลับไปยัง Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="cde33-302">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="cde33-303">การอ้างอิง (มีการสนับสนุนเฉพาะค่า *ใบสั่งขาย*)</span><span class="sxs-lookup"><span data-stu-id="cde33-303">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="cde33-304">หมายเลขใบสั่ง (ค่าอาจได้รับมาจากล็อต)</span><span class="sxs-lookup"><span data-stu-id="cde33-304">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="cde33-305">รหัสล็อต</span><span class="sxs-lookup"><span data-stu-id="cde33-305">Lot ID</span></span>
- <span data-ttu-id="cde33-306">ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-306">License plate</span></span>
- <span data-ttu-id="cde33-307">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="cde33-307">Quantity</span></span>

<span data-ttu-id="cde33-308">ถ้าคุณต้องจองป้ายทะเบียนเฉพาะสำหรับสินค้าที่มีการติดตามชุดงาน ให้ใช้ **หน้าการจองชุดงาน** ดังที่อธิบายไว้ในส่วน [ป้อนรายละเอียดใบสั่งขาย](#sales-order-details)</span><span class="sxs-lookup"><span data-stu-id="cde33-308">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="cde33-309">เมื่อมีการประมวลผลบรรทัดใบสั่งขายที่ใช้การจองป้ายทะเบียนตามใบสั่งโดยการดำเนินงานคลังสินค้า จะไม่มีการใช้คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="cde33-309">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="cde33-310">ถ้ารายการงานของคลังสินค้าประกอบด้วยบรรทัดที่เท่ากับแท่นวางสินค้าที่เสร็จสมบูรณ์และมีป้ายทะเบียน–ปริมาณที่กำหนดให้ คุณสามารถปรับปรุงประสิทธิภาพของกระบวนการเบิกสินค้า โดยใช้รายการเมนูของอุปกรณ์เคลื่อนที่ที่ตั้งค่า **กำหนดตามป้ายทะเบียน** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="cde33-310">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="cde33-311">ผู้ปฏิบัติงานคลังสินค้าจะสามารถสแกนป้ายทะเบียนเพื่อดำเนินการเบิกสินค้า แทนที่จะต้องสแกนสินค้าจากงานหนึ่งโดยหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-311">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![รายการเมนูของอุปกรณ์เคลื่อนที่ที่มีการกำหนดตัวเลือกที่จัดการตามป้ายทะเบียนเป็น ใช่](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="cde33-313">เนื่องจากฟังก์ชัน **กำหนดตามป้ายทะเบียน** ไม่สนับสนุนงานที่ครอบคลุมแท่นวางสินค้าหลายแท่น จึงดีกว่าที่จะมีรายการงานแยกต่างหากสำหรับป้ายทะเบียนที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-313">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="cde33-314">เมื่อต้องการใช้วิธีการนี้ให้เพิ่มฟิลด์ **รหัสป้ายทะเบียนที่กำหนดให้กับใบสั่ง** เป็นการแบ่งหัวข้องานบนหน้า **แม่แบบงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-314">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="cde33-315">สำหรับกระบวนการสร้างงานที่กำหนดให้กับใบสั่ง จะมีการกำหนดค่า "มิติสินค้าคงคลังที่กำหนดตามใบสั่ง" ให้กับบรรทัดงานการเบิกสินค้า และจะไม่สามารถดูมูลค่าป้ายทะเบียนโดยตรงได้</span><span class="sxs-lookup"><span data-stu-id="cde33-315">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="cde33-316">สนับสนุนเฉพาะกระบวนการ *ที่ผู้ใช้โดยตรง* ได้รับการสนับสนุนเมื่อตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="cde33-316">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="cde33-317">ตัวอย่างสถานการณ์จำลอง: ตั้งค่าและประมวลผลการจองป้ายทะเบียนตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-317">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="cde33-318">สถานการณ์จำลองนี้แสดงการตั้งค่าและประมวลผลการจองป้ายทะเบียนตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-318">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="cde33-319">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-319">Make demo data available</span></span>

<span data-ttu-id="cde33-320">สถานการณ์จำลองนี้จะอ้างอิงค่าและเรกคอร์ดที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cde33-320">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="cde33-321">หากคุณต้องการดำเนินการสถานการณ์โดยใช้ค่าที่แสดงที่นี่ ตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="cde33-321">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="cde33-322">นอกจากนี้ คุณยังต้องตั้งค่านิติบุคคลเป็น **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cde33-322">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="cde33-323">สร้างลำดับชั้นการจองสินค้าคงคลังซึ่งอนุญาตให้มีการจองป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-323">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="cde33-324">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> สินค้าคงคลัง \> ลำดับชั้นการจอง**</span><span class="sxs-lookup"><span data-stu-id="cde33-324">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="cde33-325">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cde33-325">Select **New**.</span></span>
1. <span data-ttu-id="cde33-326">ในฟิลด์ **ชื่อ** ให้ป้อนค่า (ตัวอย่างเช่น *FlexibleLP*)</span><span class="sxs-lookup"><span data-stu-id="cde33-326">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="cde33-327">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า (ตัวอย่างเช่น *การจอง LP แบบยืดหยุ่น*)</span><span class="sxs-lookup"><span data-stu-id="cde33-327">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="cde33-328">ในรายการ **ที่เลือก** ให้เลือก **หมายเลขชุดงาน** **หมายเลขลำดับประจำสินค้า** และ **เจ้าของ**</span><span class="sxs-lookup"><span data-stu-id="cde33-328">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="cde33-329">เลือกปุ่ม **ลบ** ![ลูกศรย้อนกลับ](media/backward-button.png) เพื่อย้ายเรกคอร์ดที่เลือกไปยังรายการ **พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-329">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="cde33-330">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cde33-330">Select **OK**.</span></span>
1. <span data-ttu-id="cde33-331">ในแถวสำหรับระดับมิติ **ป้ายทะเบียน** ให้เลือกกล่องกาเครื่องหมาย **อนุญาตให้มีการจองสินค้าตามความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="cde33-331">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="cde33-332">ระดับ **สถานที่** จะถูกเลือกโดยอัตโนมัติ และคุณไม่สามารถยกเลิกการเลือกกล่องกาเครื่องหมายดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="cde33-332">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="cde33-333">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cde33-333">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="cde33-334">สร้างผลิตภัณฑ์ที่นำออกใช้แล้ว สองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cde33-334">Create two released products</span></span>

1. <span data-ttu-id="cde33-335">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="cde33-335">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="cde33-336">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cde33-336">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cde33-337">ในกล่องโต้ตอบ **ผลิตภัณฑ์ที่นำออกใช้ใหม่** ให้ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-337">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="cde33-338">**หมายเลขผลิตภัณฑ์:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="cde33-338">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="cde33-339">**หมายเลขสินค้า:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="cde33-339">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="cde33-340">**กลุ่มแบบจำลองสินค้า:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="cde33-340">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="cde33-341">**กลุ่มสินค้า:** *Audio*</span><span class="sxs-lookup"><span data-stu-id="cde33-341">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="cde33-342">**กลุ่มมิติการจัดเก็บ:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="cde33-342">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="cde33-343">**กลุ่มมิติการติดตาม:** *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="cde33-343">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="cde33-344">**ลำดับชั้นการจอง:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="cde33-344">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="cde33-345">เลือก **ตกลง** เพื่อสร้างผลิตภัณฑ์ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="cde33-345">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="cde33-346">ผลิตภัณฑ์ใหม่จะเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="cde33-346">The new product is opened.</span></span> <span data-ttu-id="cde33-347">บนแท็บด่วน **คลังสินค้า** ตั้งค่าฟิลด์ **รหัสกลุ่มลำดับของหน่วย** เป็น *ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="cde33-347">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="cde33-348">ทำซ้ำขั้นตอนก่อนหน้านี้เพื่อสร้างผลิตภัณฑ์สองที่มีการตั้งค่าเดียวกันแต่ตั้งค่าฟิลด์ **หมายเลขผลิตภัณฑ์** และ **หมายเลขสินค้า** เป็น *Item2*</span><span class="sxs-lookup"><span data-stu-id="cde33-348">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="cde33-349">บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการสินค้าคงคลัง** ในกลุ่ม **แสดง** เลือก **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="cde33-349">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="cde33-350">เลือก **การปรับปรุงปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="cde33-350">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="cde33-351">ปรับปรุงปริมาณคงคลังคงเหลือของสินค้าใหม่ตามที่ระบุไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cde33-351">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="cde33-352">สินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-352">Item</span></span>  | <span data-ttu-id="cde33-353">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-353">Warehouse</span></span> | <span data-ttu-id="cde33-354">ตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="cde33-354">Location</span></span> | <span data-ttu-id="cde33-355">ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-355">License plate</span></span> | <span data-ttu-id="cde33-356">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="cde33-356">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="cde33-357">Item1</span><span class="sxs-lookup"><span data-stu-id="cde33-357">Item1</span></span> | <span data-ttu-id="cde33-358">24</span><span class="sxs-lookup"><span data-stu-id="cde33-358">24</span></span>        | <span data-ttu-id="cde33-359">FL-010</span><span class="sxs-lookup"><span data-stu-id="cde33-359">FL-010</span></span>   | <span data-ttu-id="cde33-360">LP01</span><span class="sxs-lookup"><span data-stu-id="cde33-360">LP01</span></span>          | <span data-ttu-id="cde33-361">10</span><span class="sxs-lookup"><span data-stu-id="cde33-361">10</span></span>       |
    | <span data-ttu-id="cde33-362">Item1</span><span class="sxs-lookup"><span data-stu-id="cde33-362">Item1</span></span> | <span data-ttu-id="cde33-363">24</span><span class="sxs-lookup"><span data-stu-id="cde33-363">24</span></span>        | <span data-ttu-id="cde33-364">FL-011</span><span class="sxs-lookup"><span data-stu-id="cde33-364">FL-011</span></span>   | <span data-ttu-id="cde33-365">LP02</span><span class="sxs-lookup"><span data-stu-id="cde33-365">LP02</span></span>          | <span data-ttu-id="cde33-366">10</span><span class="sxs-lookup"><span data-stu-id="cde33-366">10</span></span>       |
    | <span data-ttu-id="cde33-367">Item2</span><span class="sxs-lookup"><span data-stu-id="cde33-367">Item2</span></span> | <span data-ttu-id="cde33-368">24</span><span class="sxs-lookup"><span data-stu-id="cde33-368">24</span></span>        | <span data-ttu-id="cde33-369">FL-010</span><span class="sxs-lookup"><span data-stu-id="cde33-369">FL-010</span></span>   | <span data-ttu-id="cde33-370">LP01</span><span class="sxs-lookup"><span data-stu-id="cde33-370">LP01</span></span>          | <span data-ttu-id="cde33-371">5</span><span class="sxs-lookup"><span data-stu-id="cde33-371">5</span></span>        |
    | <span data-ttu-id="cde33-372">Item2</span><span class="sxs-lookup"><span data-stu-id="cde33-372">Item2</span></span> | <span data-ttu-id="cde33-373">24</span><span class="sxs-lookup"><span data-stu-id="cde33-373">24</span></span>        | <span data-ttu-id="cde33-374">FL-011</span><span class="sxs-lookup"><span data-stu-id="cde33-374">FL-011</span></span>   | <span data-ttu-id="cde33-375">LP02</span><span class="sxs-lookup"><span data-stu-id="cde33-375">LP02</span></span>          | <span data-ttu-id="cde33-376">5</span><span class="sxs-lookup"><span data-stu-id="cde33-376">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="cde33-377">คุณต้องสร้างสองป้ายทะเบียน และใช้สถานที่เก็บที่อนุญาตสำหรับสินค้าผสมเช่น *fl-010* และ *fl-011*</span><span class="sxs-lookup"><span data-stu-id="cde33-377">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="cde33-378">สร้างใบสั่งขายและจองป้ายทะเบียนเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cde33-378">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="cde33-379">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="cde33-379">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="cde33-380">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cde33-380">Select **New**.</span></span>
1. <span data-ttu-id="cde33-381">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="cde33-382">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="cde33-382">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="cde33-383">**คลังสินค้า:** *24*</span><span class="sxs-lookup"><span data-stu-id="cde33-383">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="cde33-384">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ **สร้างใบสั่งขาย** และเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-384">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="cde33-385">บนกริดแท็บด่วน **บรรทัดใบสั่งขาย** ให้เพิ่มบรรทัดที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-385">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="cde33-386">**หมายเลขสินค้า:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="cde33-386">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="cde33-387">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="cde33-387">**Quantity:** *10*</span></span>

1. <span data-ttu-id="cde33-388">เพิ่มรายการใบสั่งขายที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-388">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="cde33-389">**หมายเลขสินค้า:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="cde33-389">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="cde33-390">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="cde33-390">**Quantity:** *5*</span></span>

1. <span data-ttu-id="cde33-391">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cde33-391">Select **Save**.</span></span>
1. <span data-ttu-id="cde33-392">บนแท็บด่วน **รายละเอียดของฟิลด์** บนแท็บ **การตั้งค่า** ให้จดบันทึก **ค่ารหัสล็อต** สำหรับแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="cde33-392">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="cde33-393">ค่าเหล่านี้จะต้องใช้ในระหว่างการจองป้ายทะเบียนเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cde33-393">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cde33-394">เมื่อต้องการจองป้ายทะเบียนที่เฉพาะ คุณต้องใช้เอนทิตี้ข้อมูล **การจองที่กำหนดตามใบสั่งสำหรับแต่ละป้ายทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="cde33-394">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="cde33-395">ในการจองสินค้าที่มีการติดตามชุดงานที่มีป้ายทะเบียนเฉพาะ คุณสามารถใช้หน้า **การจองชุดงาน** ดังที่อธิบายไว้ในส่วน [ป้อนรายละเอียดใบสั่งขาย](#sales-order-details)</span><span class="sxs-lookup"><span data-stu-id="cde33-395">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="cde33-396">ถ้าคุณป้อนป้ายทะเบียนโดยตรงบนบรรทัดใบสั่งขาย และยืนยันไปยังระบบ การประมวลผลการจัดการคลังสินค้าจะไม่มีถูกใช้สำหรับบรรทัดนี้</span><span class="sxs-lookup"><span data-stu-id="cde33-396">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="cde33-397">เลือก **เปิดใน Microsoft Office** เลือก **การจองที่กำหนดตามใบสั่งสำหรับแต่ละป้ายทะเบียน** และดาวน์โหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="cde33-397">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="cde33-398">เปิดไฟล์ที่ดาน์โหลดมาใน Excel และเลือก **เปิดใช้งานการแก้ไข** เพื่อเปิดใช้งาน Add-in ของ Excel เพื่อให้รัน</span><span class="sxs-lookup"><span data-stu-id="cde33-398">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="cde33-399">ถ้าคุณกำลังเรียกใช้ Add-in ของ Excel เป็นครั้งแรก เลือก **เชื่อถือ Add-in นี้**</span><span class="sxs-lookup"><span data-stu-id="cde33-399">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="cde33-400">ถ้าคุณได้รับการพร้อมท์ให้เข้าสู่ระบบ เลือก **เข้าสู่ระบบ** และจากนั้นเข้าสู่ระบบโดยใช้ข้อมูลประจำตัวเดียวกับที่คุณใช้เพื่อเข้าสู่ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cde33-400">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="cde33-401">เมื่อต้องการจองสินค้าบนป้ายทะเบียนที่ระบุใน Excel add-in ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดการจองแล้วตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-401">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="cde33-402">**รหัสล็อต:** ป้อนค่า **รหัสล็อต** ที่คุณพบสำหรับบรรทัดใบสั่งขายสำหรับ *Item1*</span><span class="sxs-lookup"><span data-stu-id="cde33-402">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="cde33-403">**ป้ายทะเบียน:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="cde33-403">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="cde33-404">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="cde33-404">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="cde33-405">เลือก **สร้าง** เพื่อเพิ่มบรรทัดการจองอื่น และตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-405">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="cde33-406">**รหัสล็อต:** ป้อนค่า **รหัสล็อต** ที่คุณพบสำหรับบรรทัดใบสั่งขายสำหรับ *Item2*</span><span class="sxs-lookup"><span data-stu-id="cde33-406">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="cde33-407">**ป้ายทะเบียน:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="cde33-407">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="cde33-408">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="cde33-408">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="cde33-409">ใน add-in ของ Excel ให้เลือก **เผยแพร่** เพื่อส่งข้อมูลกลับไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cde33-409">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cde33-410">บรรทัดการจองจะปรากฏในระบบก็ต่อเมื่อมีการเผยแพร่เสร็จสมบูรณ์โดยไม่มีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="cde33-410">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="cde33-411">กลับไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cde33-411">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="cde33-412">ถ้าต้องการตรวจสอบการจองสินค้าบนแท็บด่วน **บรรทัดใบสั่งขาย** บน **เมนูสินค้าคงคลัง** ให้เลือก **รักษาการ \> จอง**</span><span class="sxs-lookup"><span data-stu-id="cde33-412">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="cde33-413">โปรดสังเกตว่าสำหรับบรรทัดใบสั่งขายสำหรับ *Item1* สินค้าคงคลัง *10* รายการถูกจองและสำหรับบรรทัดใบสั่งขายสำหรับ *Item2* สินค้าคงคลัง *5* รายการถูกจองไว้</span><span class="sxs-lookup"><span data-stu-id="cde33-413">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="cde33-414">เมื่อต้องการตรวจทานรายการความเคลื่อนไหวของสินค้าคงคลังที่เกี่ยวข้องกับการจองบรรทัดใบสั่งขายบนแท็บด่วน **บรรทัดใบสั่งขาย** บน **เมนูสินค้าคงคลัง** ให้เลือก **ดู \> ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="cde33-414">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="cde33-415">โปรดสังเกตว่ามีสองธุรกรรมที่เกี่ยวข้องกับการจอง: อันหนึ่งที่มีการตั้งค่าฟิลด์ **อ้างอิง** *เป็น* ใบสั่งขายและฟิลด์ **อ้างอิง** ที่จะมีการตั้งค่าให้กับการ *จองตามใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="cde33-415">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cde33-416">ธุรกรรมที่มีการตั้งค่าฟิลด์ **การอ้างอิง** เป็น *ใบสั่งขาย* แสดงถึงการจองจองสำหรับมิติสินค้าคงคลังที่อยู่เหนือระดับ **สถานที่** (ไซต์ คลังสินค้า และสถานะสินค้าคงคลัง)</span><span class="sxs-lookup"><span data-stu-id="cde33-416">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="cde33-417">ธุรกรรมที่มีการตั้งค่าฟิลด์ **การอ้างอิง** เป็น *การจองที่กำหนดให้กับใบสั่ง* แสดงถึงการจองบรรทัดใบสั่งสำหรับป้ายทะเบียนและสถานที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="cde33-417">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="cde33-418">ในการนำใบสั่งขายออกใช้ บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="cde33-418">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="cde33-419">ตรวจทานและประมวลผลงานของคลังสินค้าด้วยป้ายทะเบียนใบสั่งที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-419">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="cde33-420">บนแท็บด่วน **รายการใบสั่งขาย** บนเมนู **คลังสินค้า** เลือก **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-420">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="cde33-421">เมื่อทำการจองสำหรับชุดงานหนึ่ง ๆ ระบบจะไม่ใช้คำสั่งของสถานที่เมื่อสร้างงานสำหรับใบสั่งขายที่ใช้การจองป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-421">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="cde33-422">เนื่องจากการจองที่กำหนดตามใบสั่งระบุมิติสินค้าคงคลังทั้งหมด รวมถึงสถานที่คำสั่งสถานที่ไม่จำเป็นต้องมีการใช้เนื่องจากมิติสินค้าคงคลังเหล่านั้นจะถูกป้อนในงานนั้นไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cde33-422">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="cde33-423">มีการแสดงในส่วนของ **มิติสินค้าคงคลัง** ในหน้า **รายการความเคลื่อนไหวของสินค้าคงคลังของงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-423">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cde33-424">หลังจากมีการสร้างงาน ธุรกรรมสินค้าคงคลังของสินค้าที่ซึ่งฟิลด์ **การอ้างอิง** ถูกตั้งค่าเป็น *การจองที่ผูกมัดใบสั่ง* จะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="cde33-424">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="cde33-425">ธุรกรรมสินค้าคงคลังที่ซึ่งฟิลด์ **การอ้างอิง** ถูกตั้งค่าเป็น *งาน* ขณะนี้มีการจองทางกายภาพในมิติสินค้าคงคลังของปริมาณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cde33-425">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="cde33-426">บนอุปกรณ์เคลื่อนที่ให้เสร็จสิ้นการเบิกสินค้าและการวางงานโดยใช้รายการเมนูที่มีการเลือกกล่องกาเครื่องหมาย **กำหนดตามป้ายทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="cde33-426">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cde33-427">ฟังก์ชัน **กำหนดตามป้ายทะเบียน** จะช่วยให้คุณประมวลผลป้ายทะเบียนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cde33-427">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="cde33-428">ถ้าคุณต้องประมวลผลบางส่วนของป้ายทะเบียนคุณจะไม่สามารถใช้ฟังก์ชันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-428">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="cde33-429">เราขอแนะนำให้คุณมีงานที่สร้างขึ้นแยกต่างหากสำหรับแต่ละป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-429">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="cde33-430">เมื่อต้องการให้ผลลัพธ์นี้สำเร็จให้ใช้ **คุณลักษณะการแบ่งหัวข้องาน** บนหน้า **แม่แบบงาน**</span><span class="sxs-lookup"><span data-stu-id="cde33-430">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="cde33-431">ตอนนี้ป้ายทะเบียน *LP02* ถูกเลือกสำหรับบรรทัดใบสั่งขายและใส่ไปยัง *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="cde33-431">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="cde33-432">ณ จุดนี้ ก็พร้อมแล้วที่จะโหลดและส่งไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-432">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="cde33-433">การจัดการข้อยกเว้นของคลังสินค้าที่มีหมายเลขชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-433">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="cde33-434">งานของคลังสินค้าสำหรับหมายเลขชุดงานที่กำหนดให้กับใบสั่งของการเบิกสินค้า จะขึ้นอยู่กับการจัดการข้อยกเว้นของคลังสินค้ามาตรฐานเดียวกันและการดำเนินการที่เป็นงานปกติ</span><span class="sxs-lookup"><span data-stu-id="cde33-434">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="cde33-435">โดยทั่วไป คุณสามารถยกเลิกงานที่เปิดหรือรายการงาน ซึ่งอาจหยุดชะงักได้ เนื่องจากสถานที่ของผู้ใช้เต็ม ซึ่งอาจมีการเบิกสินค้าแบบสั้นและสามารถปรับปรุงได้เนื่องจากมีการเคลื่อนย้าย</span><span class="sxs-lookup"><span data-stu-id="cde33-435">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="cde33-436">ในทำนองเดียวกัน ปริมาณที่เบิกของงานที่เสร็จสมบูรณ์แล้วอาจลดลง หรือสามารถกลับรายการงานได้</span><span class="sxs-lookup"><span data-stu-id="cde33-436">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="cde33-437">กฎคีย์ต่อไปนี้จะใช้กับการดำเนินการการจัดการข้อยกเว้นเหล่านี้ทั้งหมด: ไม่สามารถแทนที่หมายเลขชุดงานที่จองไว้สำหรับลูกค้าด้วยหมายเลขชุดงานที่แตกต่างกันได้ แต่จะสามารถเปลี่ยนมิติการจัดเก็บ (สถานที่และป้ายทะเบียน) โดยใช้การอัพเดตด้วยตนเองโดยผู้ใช้ หรือการอัพเดตอัตโนมัติโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="cde33-437">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="cde33-438">การอัพเดตอัตโนมัติจะขึ้นอยู่กับการกำหนดมิติการจัดเก็บแบบสุ่มที่เหมือนกันซึ่งใช้เมื่อมีการจองชุดงานเฉพาะโดยอัตโนมัติ แต่ไม่มีการระบุมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="cde33-438">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="cde33-439">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="cde33-439">Example scenario</span></span>

<span data-ttu-id="cde33-440">ตัวอย่างของสถานการณ์จำลองนี้คือ สถานการณ์ที่งานที่เสร็จสมบูรณ์ก่อนหน้านี้ไม่ได้ถูกเบิกสินค้าโดยใช้ฟังก์ชัน **ลดปริมาณที่เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="cde33-440">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="cde33-441">ตัวอย่างนี้อนุมานว่าคุณได้ดำเนินการขั้นตอนต่าง ๆ ที่อธิบายไว้ใน [สถานการณ์จำลองตัวอย่าง: การปันส่วนหมายเลขชุดงาน](#Example-batch-allocation)</span><span class="sxs-lookup"><span data-stu-id="cde33-441">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="cde33-442">ดำเนินการต่อจากตัวอย่างดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="cde33-442">It continues from that example.</span></span>

1. <span data-ttu-id="cde33-443">ไปที่ **การจัดการคลังสินค้า** \> **จำนวนงานในศูนย์การผลิต** \> **จำนวนงานในศูนย์การผลิตที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="cde33-443">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="cde33-444">เลือกจำนวนงานในศูนย์การผลิตที่สร้างขึ้นโดยสัมพันธ์กับการจัดส่งสินค้าของใบสั่งขายของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde33-444">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="cde33-445">จาก FastTab **รายการใบสั่งจำนวนงานในศูนย์การผลิต** เลือก **ลดปริมาณที่เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="cde33-445">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="cde33-446">บนหน้า **ลดปริมาณที่เบิกสินค้า** ในฟิลด์ **ย้ายไปยังสถานที่** เลือก **FL-001**</span><span class="sxs-lookup"><span data-stu-id="cde33-446">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="cde33-447">ในฟิลด์ **ย้ายไปยังป้ายทะเบียน** เลือก **LP33**</span><span class="sxs-lookup"><span data-stu-id="cde33-447">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="cde33-448">ในกริด ในฟิลด์ **ปริมาณสินค้าคงคลังที่จะยกเลิกการเบิกสินค้า** ป้อน **10**</span><span class="sxs-lookup"><span data-stu-id="cde33-448">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="cde33-449">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cde33-449">Select **OK**.</span></span>

<span data-ttu-id="cde33-450">ต่อไปนี้เป็นผลลัพธ์ของการดำเนินการยกเลิกการเบิกสินค้า:</span><span class="sxs-lookup"><span data-stu-id="cde33-450">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="cde33-451">สถานะของงานที่ปิดก่อนหน้านี้ถูกตั้งค่าเป็น **ยกเลิกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="cde33-451">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="cde33-452">งานใหม่ของชนิด **การเคลื่อนไหวของสินค้าคงคลัง** จะถูกสร้างขึ้นสำหรับปริมาณที่ไม่ได้เบิกสินค้าเท่ากับ **10** สำหรับหมายเลขชุดงาน **B11**</span><span class="sxs-lookup"><span data-stu-id="cde33-452">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="cde33-453">งานนี้แสดงถึงการเคลื่อนย้ายจากสถานที่ **Baydoor** ไปยังป้ายทะเบียน **LP33** ในสถานที่ **FL-001**</span><span class="sxs-lookup"><span data-stu-id="cde33-453">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="cde33-454">สถานะถูกตั้งค่าเป็น **ปิดแล้ว**</span><span class="sxs-lookup"><span data-stu-id="cde33-454">The status is set to **Closed**.</span></span>
- <span data-ttu-id="cde33-455">ระบบจองหมายเลขชุดงานที่ถูกสั่งในตอนแรกอีกครั้ง และกำหนดสถานที่และรหัสป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-455">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="cde33-456">(กระบวนการนี้เทียบเท่ากับการรันฟังก์ชัน **รายการจอง** สำหรับรายการใบสั่งสำหรับหมายเลขชุดงานที่ระบุ)</span><span class="sxs-lookup"><span data-stu-id="cde33-456">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="cde33-457">ด้วยเหตุนี้ ชุดงาน **B11** จึงถูกแสดงขึ้นตามที่กำหนดไว้ใน FastTab **หมายเลขชุดงานที่กำหนดให้กับรายการต้นทาง** ของหน้า **การจองชุดงาน** และฟิลด์ **การจอง** มีปริมาณเท่ากับ **10** สำหรับหมายเลขชุดงาน **B11**</span><span class="sxs-lookup"><span data-stu-id="cde33-457">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="cde33-458">นอกจากนี้ ฟิลด์ **สถานที่** ถูกตั้งค่าเป็น **FL-001** และฟิลด์ **ป้ายทะเบียน** ถูกตั้งค่าเป็น **LP11**</span><span class="sxs-lookup"><span data-stu-id="cde33-458">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="cde33-459">(คุณสามารถเพิ่มฟิลด์เหล่านี้ไปยังกริดได้ ถ้าไม่สามารถมองเห็นได้)</span><span class="sxs-lookup"><span data-stu-id="cde33-459">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="cde33-460">ตารางต่อไปนี้จะแสดงภาพรวมที่แสดงวิธีการที่ระบบจัดการการจองชุดงานที่กำหนดให้กับใบสั่งสำหรับการดำเนินการของคลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cde33-460">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="cde33-461">เมื่อต้องการแปลเนื้อหาในตาราง สมมติว่ามีการรันการดำเนินการคลังสินค้าแต่ละรายการในบริบทของงานของคลังสินค้าที่มีอยู่ ซึ่งมีต้นกำเนิดมาจากการจองชุดงานที่กำหนดให้กับใบสั่ง หรือการดำเนินการของคลังสินค้าแต่ละรายการมีผลกระทบต่องานของชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="cde33-461">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="cde33-462">ในตารางเหล่านี้ คอลัมน์ "ปริมาณชุดงานพร้อมใช้งาน" บ่งชี้ว่าปริมาณชุดงานพร้อมใช้งานหรือไม่ นอกเหนือจากปริมาณที่จองไว้แล้วสำหรับการจองสินค้าที่กำหนดให้กับใบสั่งปัจจุบัน หรือจองแล้วโดยงานคลังสินค้าที่มีต้นกำเนิดมาจากการจองของชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="cde33-462">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="cde33-463">แทนที่สถานที่เบิกสินค้าในงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="cde33-463">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cde33-464">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-464">Key setup parameter</span></span></th>
<th><span data-ttu-id="cde33-465">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-465">Batch quantity is available</span></span></th>
<th><span data-ttu-id="cde33-466">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-466">Key user steps</span></span></th>
<th><span data-ttu-id="cde33-467">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-467">Warehouse work</span></span></th>
<th><span data-ttu-id="cde33-468">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-468">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="cde33-469">ตัวเลือก <strong>อนุญาตการแทนที่สถานที่เบิกสินค้า</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-469">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="cde33-470">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-470">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-471">เลือกรายการเมนู <strong>แทนที่สถานที่</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณเริ่มต้นงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-471">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="cde33-472">เลือก <strong>แนะนำ</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-472">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="cde33-473">ยืนยันสถานที่ใหม่ที่แนะนำตามความพร้อมใช้งานของปริมาณของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-473">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-474">ในงานปัจจุบัน การดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="cde33-474">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="cde33-475">สถานที่ในรายการเบิกสินค้าจะถูกอัพเดตไปยังสถานที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-475">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="cde33-476">(ถ้าสถานที่มีการควบคุมป้ายทะเบียน ป้ายทะเบียนแบบสุ่มจะถูกกำหนดให้กับธุรกรรมสินค้าคงคลังของงาน และผู้ปฏิบัติงานสามารถเลือกจากป้ายทะเบียนใดๆ ที่มีปริมาณที่พร้อมใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="cde33-476">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="cde33-477">ถ้าพบปริมาณในป้ายทะเบียนมากกว่าหนึ่งป้ายในสถานที่ใหม่ รายการเบิกสินค้าดั้งเดิมจะถูกแบ่งออกเป็นหลายรายการเพื่อให้ตรงกับป้ายทะเบียนแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="cde33-477">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-478">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-478">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-479">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-479">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-480">เลือกรายการเมนู <strong>แทนที่สถานที่</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณเริ่มต้นงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-480">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="cde33-481">ป้อนสถานที่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="cde33-481">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-482">การดำเนินการ <strong>แทนที่สถานที่</strong> ไม่สามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="cde33-482">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="cde33-483">การทำงานล้มเหลว และข้อผิดพลาดแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="cde33-483">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="cde33-484">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-484">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="cde33-485">ปุ่มแบบเต็ม – แบ่งรายการงานเนื่องจากมีมากเกินไปบนสถานที่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cde33-485">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cde33-486">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-486">Key setup parameter</span></span></th>
<th><span data-ttu-id="cde33-487">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-487">Batch quantity is available</span></span></th>
<th><span data-ttu-id="cde33-488">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-488">Key user steps</span></span></th>
<th><span data-ttu-id="cde33-489">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-489">Warehouse work</span></span></th>
<th><span data-ttu-id="cde33-490">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-490">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cde33-491">ตัวเลือก <strong>อนุญาตให้มีการแบ่งงาน</strong> ถูกเปิดใช้งานบนรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="cde33-491">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="cde33-492">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-492">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-493">เลือกรายการเมนู <strong>แบบเต็ม</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณประมวลผลงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-493">Select the <strong>Full</strong> menu item on the Warehouse Management mobile app when you process picking work.</span></span></li>
<li><span data-ttu-id="cde33-494">ในฟิลด์ <strong>ปริมาณการเบิกสินค้า</strong> ให้ป้อนปริมาณบางส่วนของการเบิกสินค้าที่จำเป็น เพื่อบ่งชี้ถึงกำลังการผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cde33-494">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="cde33-495">ในงานปัจจุบัน ปริมาณจะถูกอัพเดตเป็นปริมาณคงเหลือที่ต้องมีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-495">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="cde33-496">มีการสร้างและปิดงานใหม่สำหรับปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-496">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="cde33-497">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-497">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="cde33-498">ลดปริมาณที่เบิกสินค้าของงานที่เสร็จสมบูรณ์ (จากจำนวนงานในศูนย์การผลิต)</span><span class="sxs-lookup"><span data-stu-id="cde33-498">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cde33-499">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-499">Key setup parameter</span></span></th>
<th><span data-ttu-id="cde33-500">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-500">Batch quantity is available</span></span></th>
<th><span data-ttu-id="cde33-501">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-501">Key user steps</span></span></th>
<th><span data-ttu-id="cde33-502">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-502">Warehouse work</span></span></th>
<th><span data-ttu-id="cde33-503">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-503">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="cde33-504">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-504">Not applicable</span></span></td>
<td><span data-ttu-id="cde33-505">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-505">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-506">เปิดหน้า <strong>ลดปริมาณที่เบิกสินค้า</strong> จากรายการจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="cde33-506">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="cde33-507">ป้อนปริมาณทั้งหมดที่จะยกเลิกการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-507">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="cde33-508">เลือก "ย้ายไปที่" สถานที่/ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-508">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="cde33-509">งานที่เชื่อมโยงกับรายการจำนวนงานในศูนย์การผลิตถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="cde33-509">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="cde33-510">มีการสร้างและปิดงานใหม่สำหรับความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-510">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-511">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-511">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-512">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-512">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-513">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-513">No</span></span></td>
<td><span data-ttu-id="cde33-514">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-514">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-515">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-515">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-516">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับสถานที่เก็บและป้ายทะเบียนเดียวกัน (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ถูกป้อนไว้ในระหว่างการยกเลิกการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-516">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="cde33-517">ย้ายสินค้าภายในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-517">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="cde33-518">การดำเนินการของคลังสินค้านี้ใช้ได้กับการเคลื่อนย้ายของชนิด **กระบวนการสร้างงาน** เท่านั้น ไม่ใช่การเคลื่อนย้ายโดยเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="cde33-518">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cde33-519">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-519">Key setup parameter</span></span></th>
<th><span data-ttu-id="cde33-520">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-520">Batch quantity is available</span></span></th>
<th><span data-ttu-id="cde33-521">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-521">Key user steps</span></span></th>
<th><span data-ttu-id="cde33-522">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-522">Warehouse work</span></span></th>
<th><span data-ttu-id="cde33-523">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-523">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="cde33-524">ตัวเลือก <strong>อนุญาตการเคลื่อนย้ายสินค้าคงคลังที่มีงานที่เชื่อมโยง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-524">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="cde33-525">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-525">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-526">เริ่มการเคลื่อนย้ายบนแอปการบริหารคลังสินค้าบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="cde33-526">Start a movement on the Warehouse Management mobile app.</span></span></li>
<li><span data-ttu-id="cde33-527">ป้อนสถานที่ "ตั้งต้น" และ "สิ้นสุด"</span><span class="sxs-lookup"><span data-stu-id="cde33-527">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="cde33-528">ในงานที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการย้าย สถานที่เบิกสินค้าจะถูกอัพเดตเป็นสถานที่ "สิ้นสุด" ใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-528">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="cde33-529">มีการสร้างและปิดงานใหม่สำหรับความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-529">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-530">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการเคลื่อนย้ายปริมาณจากสถานที่ที่กำหนดจะถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-531">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-531">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-532">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-532">No</span></span></td>
<td><span data-ttu-id="cde33-533">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-533">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-534">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-534">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-535">การจองที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการเคลื่อนไหวของปริมาณจากสถานที่ที่กำหนดจะถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับที่ตั้งและป้ายทะเบียน "สิ้นสุด" ใหม่ (ถ้าสถานที่มีการควบคุมป้ายทะเบียน)</span><span class="sxs-lookup"><span data-stu-id="cde33-535">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="cde33-536">กลับรายการปริมาณที่เบิกสินค้าของงานที่เสร็จสมบูรณ์ (จากจำนวนงานในศูนย์การผลิตหรือเวฟ)</span><span class="sxs-lookup"><span data-stu-id="cde33-536">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cde33-537">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-537">Key setup parameter</span></span></th>
<th><span data-ttu-id="cde33-538">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-538">Batch quantity is available</span></span></th>
<th><span data-ttu-id="cde33-539">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-539">Key user steps</span></span></th>
<th><span data-ttu-id="cde33-540">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-540">Warehouse work</span></span></th>
<th><span data-ttu-id="cde33-541">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-541">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="cde33-542">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-542">Not applicable</span></span></td>
<td><span data-ttu-id="cde33-543">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-543">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-544">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-544">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="cde33-545">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>ปล่อยสินค้าไว้ที่สถานที่ปัจจุบัน</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-545">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-546">งานทั้งหมดที่เชื่อมโยงกับจำนวนงานในศูนย์การผลิตถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="cde33-546">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="cde33-547">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-547">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-548">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-548">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-549">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-549">No</span></span></td>
<td><span data-ttu-id="cde33-550">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-550">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-551">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-551">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-552">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับสถานที่และป้ายทะเบียนที่ปริมาณถูกเหลือเมื่อมีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-552">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-553">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-553">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-554">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-554">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="cde33-555">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>กำหนดสินค้าไปยังสถานที่นี้</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-555">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="cde33-556">งานปัจจุบันถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="cde33-556">The current work is canceled.</span></span></li>
<li><span data-ttu-id="cde33-557">มีการสร้างและปิดงานใหม่สำหรับความเคลื่อนไหวของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-557">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-558">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-558">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-559">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-559">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-560">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-560">No</span></span></td>
<td><span data-ttu-id="cde33-561">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-561">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-562">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-562">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-563">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน และสำหรับสถานที่และป้ายทะเบียนที่ปริมาณถูกกำหนดให้เมื่อมีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-563">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-564">ใช่/ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-565">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="cde33-566">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>ย้ายสินค้าไปยังสถานที่นี้</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-566">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-567">ไม่ได้สนับสนุนการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-567">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="cde33-568">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-568">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-569">ใช่/ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-569">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-570">เปิดหน้า <strong>กลับรายการงาน</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-570">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="cde33-571">บนหน้าคำขอ ให้เลือกตัวเลือก <strong>ย้ายสินค้าตามคำสั่งสถานที่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-571">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-572">ไม่ได้สนับสนุนการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-572">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="cde33-573">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-573">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="cde33-574">การเบิกปริมาณที่ขาด – ลงทะเบียนปริมาณที่ไม่ได้ถูกพบในสถานที่/ป้ายทะเบียน ในขณะที่คุณดำเนินงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-574">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cde33-575">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-575">Key setup parameter</span></span></th>
<th><span data-ttu-id="cde33-576">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-576">Batch quantity is available</span></span></th>
<th><span data-ttu-id="cde33-577">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-577">Key user steps</span></span></th>
<th><span data-ttu-id="cde33-578">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-578">Warehouse work</span></span></th>
<th><span data-ttu-id="cde33-579">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-579">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="cde33-580">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ไม่มี</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ไม่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-580">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="cde33-581">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-581">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-582">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณทำงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-582">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="cde33-583">ในฟิลด์ <strong>ปริมาณการเบิกสินค้า</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-583">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="cde33-584">ในฟิลด์ <strong>เหตุผล</strong> ป้อน <strong>ไม่มีการปันส่วนใหม่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-584">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="cde33-585">งานปัจจุบันถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-585">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="cde33-586">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="cde33-586">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-587">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-587">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-588">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-588">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-589">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-589">No</span></span></td>
<td><span data-ttu-id="cde33-590">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-590">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="cde33-591">การดำเนินการเบิกสินค้าที่ขาดล้มเหลว และมีการแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="cde33-591">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="cde33-592">งานปัจจุบันยังคงเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="cde33-592">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-593">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-593">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="cde33-594">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ไม่มี</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ใช่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-594">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="cde33-595">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-595">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-596">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณทำงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-596">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="cde33-597">ในฟิลด์ <strong>ปริมาณการเบิกสินค้า</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-597">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="cde33-598">ในฟิลด์ <strong>เหตุผล</strong> ป้อน <strong>ไม่มีการปันส่วนใหม่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-598">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="cde33-599">งานปัจจุบันถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-599">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="cde33-600">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="cde33-600">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-601">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการปรับปรุงปริมาณในสถานที่ที่เบิกสินค้าที่ขาดสำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-602">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-602">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-603">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-603">No</span></span></td>
<td><span data-ttu-id="cde33-604">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-604">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-605">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-605">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-606">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการปรับปรุงปริมาณในสถานที่ที่เบิกสินค้าที่ขาดจะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="cde33-606">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-607">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ด้วยตนเอง</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ไม่/ใช่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-607">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="cde33-608">นอกจากนี้ ตัวเลือก <strong>อนุญาตการปันส่วนสินค้าด้วยตนเอง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-608">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="cde33-609">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-609">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-610">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณทำงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-610">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="cde33-611">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-611">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="cde33-612">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนด้วยตนเอง</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-612">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="cde33-613">เลือกสถานที่/ป้ายทะเบียนในรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-613">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="cde33-614">ในงานปัจจุบัน การดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="cde33-614">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="cde33-615">รายการเบิกสินค้าถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-615">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="cde33-616">รายการส่งสินค้าถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="cde33-616">The put line is canceled.</span></span></li>
<li><span data-ttu-id="cde33-617">จะมีการสร้างรายการเบิกสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-617">A new pick line is created.</span></span> <span data-ttu-id="cde33-618">ซึ่งใช้สถานที่/ป้ายทะเบียนที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="cde33-618">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="cde33-619">จะมีการสร้างรายการส่งสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="cde33-619">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cde33-620">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="cde33-620">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-621">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-621">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-622">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ด้วยตนเอง</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ไม่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-622">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="cde33-623">นอกจากนี้ ตัวเลือก <strong>อนุญาตการปันส่วนสินค้าด้วยตนเอง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-623">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="cde33-624">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-624">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-625">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณทำงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-625">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="cde33-626">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-626">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="cde33-627">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนด้วยตนเอง</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-627">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-628">การดำเนินการเบิกสินค้าที่ขาดล้มเหลว และมีการแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="cde33-628">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="cde33-629">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-629">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-630">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>ด้วยตนเอง</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่</strong> และ <strong>ลบการจอง</strong> = <strong>ใช่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-630">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="cde33-631">นอกจากนี้ ตัวเลือก <strong>อนุญาตการปันส่วนสินค้าด้วยตนเอง</strong> ถูกเปิดใช้งานในผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-631">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="cde33-632">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-632">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-633">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณทำงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-633">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="cde33-634">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-634">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="cde33-635">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนด้วยตนเอง</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-635">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="cde33-636">เลือกสถานที่/ป้ายทะเบียนในรายการ</span><span class="sxs-lookup"><span data-stu-id="cde33-636">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="cde33-637">ในงานปัจจุบัน การดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="cde33-637">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="cde33-638">รายการเบิกสินค้าถูกปิด และปริมาณที่เบิกสินค้าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-638">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="cde33-639">รายการส่งสินค้าถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="cde33-639">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cde33-640">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การนับ</strong> และชนิดการตัดสินค้าจากคลัง <strong>ที่ขายแล้ว</strong> เพื่อแสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="cde33-640">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cde33-641">การจองสินค้าที่มีอยู่ทั้งหมดที่ได้รับผลกระทบจากการปรับปรุงปริมาณในสถานที่/ป้ายทะเบียนที่เบิกสินค้าที่ขาดจะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="cde33-641">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-642">มีการตั้งค่าข้อยกเว้นของงานของชนิด <strong>การเบิกสินค้าที่ขาด</strong> ที่ซึ่ง <strong>การปันส่วนใหม่ของสินค้า</strong> = <strong>อัตโนมัติ</strong> <strong>ปรับปรุงสินค้าคงคลัง</strong> = <strong>ใช่/ไม่</strong> และ <strong>ลบการจอง</strong> = <strong>ใช่/ไม่</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-642">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="cde33-643">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cde33-643">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-644">เลือกรายการเมนู <strong>การเบิกสินค้าที่ขาด</strong> บนแอปการจัดการคลังสินค้าบนมือถือ เมื่อคุณทำงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-644">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="cde33-645">ในฟิลด์ <strong>ปริมาณการเบิกสินค้าที่ขาด</strong> ให้ป้อน <strong>0</strong> (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="cde33-645">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="cde33-646">ในฟิลด์ <strong>เหตุผล</strong> ให้เลือก <strong>การเบิกสินค้าที่ขาดด้วยการปันส่วนอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-646">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-647">การเบิกสินค้าที่ขาดที่เกี่ยวข้องกับการปันผลอัตโนมัติไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="cde33-647">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="cde33-648">การเบิกสินค้าที่ขาดที่เกี่ยวข้องกับการปันผลอัตโนมัติไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="cde33-648">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="cde33-649">เปลี่ยนสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-649">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="cde33-650">การดำเนินการคลังสินค้านี้สามารถดำเนินการได้จากจุดป้อนข้อมูลหลายจุด</span><span class="sxs-lookup"><span data-stu-id="cde33-650">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="cde33-651">ตัวอย่างที่แสดงไว้ที่นี่ใช้การดำเนินการ **การเปลี่ยนสถานะสินค้าคงคลัง** ในหน้า **คงเหลือตามสถานที่**</span><span class="sxs-lookup"><span data-stu-id="cde33-651">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cde33-652">พารามิเตอร์การตั้งค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-652">Key setup parameter</span></span></th>
<th><span data-ttu-id="cde33-653">ปริมาณชุดงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-653">Batch quantity is available</span></span></th>
<th><span data-ttu-id="cde33-654">ขั้นตอนของผู้ใช้คีย์</span><span class="sxs-lookup"><span data-stu-id="cde33-654">Key user steps</span></span></th>
<th><span data-ttu-id="cde33-655">งานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-655">Warehouse work</span></span></th>
<th><span data-ttu-id="cde33-656">การจองชุดงานที่กำหนดให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-656">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="cde33-657">บนแท็บ <strong>คลังสินค้า</strong> ในเรกคอร์ด <strong>คลังสินค้า</strong> ฟิลด์ <strong>ลบการจองและการทำเครื่องหมาย</strong> ถูกตั้งค่าเป็น <strong>การจอง</strong> หรือ <strong>การเลือกและการจอง</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-657">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="cde33-658">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-658">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-659">เลือกสถานที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cde33-659">Select a specific location.</span></span></li>
<li><span data-ttu-id="cde33-660">เลือกรายการที่มีสินค้า สถานที่ และป้ายทะเบียนเฉพาะ (ถ้าสถานที่มีการควบคุมป้ายทะเบียน)</span><span class="sxs-lookup"><span data-stu-id="cde33-660">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="cde33-661">เลือก <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-661">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="cde33-662">ตั้งค่าฟิลด์ <strong>สถานะของสินค้าคงคลัง</strong> เป็น <strong>การบล็อค</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-662">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-663">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="cde33-664">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-664">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-665">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-665">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="cde33-666">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong> สองรายการ เพื่อแสดงถึงการเปลี่ยนแปลงในมิติสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-666">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="cde33-667">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การบล็อคสินค้าคงคลัง</strong> และมีการสร้างชนิดการตัดสินค้าจากคลังของ <strong>ถูกจองจริง</strong> เพื่อแสดงการจองของปริมาณที่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="cde33-667">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="cde33-668">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-668">No</span></span></td>
<td><span data-ttu-id="cde33-669">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-669">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-670">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-670">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="cde33-671">การสำรองสินค้าจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="cde33-671">The reservation is removed.</span></span></li>
<li><span data-ttu-id="cde33-672">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong> สองรายการ เพื่อแสดงถึงการเปลี่ยนแปลงในมิติสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-672">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="cde33-673">มีการสร้างธุรกรรมสินค้าคงคลังของชนิด <strong>การบล็อคสินค้าคงคลัง</strong> และมีการสร้างชนิดการตัดสินค้าจากคลังของ <strong>ถูกจองจริง</strong> เพื่อแสดงการจองของปริมาณที่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="cde33-673">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="cde33-674">บนแท็บ <strong>คลังสินค้า</strong> ในเรกคอร์ด <strong>คลังสินค้า</strong> ฟิลด์ <strong>ลบการจองและการทำเครื่องหมาย</strong> ถูกตั้งค่าเป็น <strong>ไม่มี</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-674">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="cde33-675">ใช่</span><span class="sxs-lookup"><span data-stu-id="cde33-675">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cde33-676">เลือกสถานที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cde33-676">Select a specific location.</span></span></li>
<li><span data-ttu-id="cde33-677">เลือกรายการที่มีสินค้า สถานที่ และป้ายทะเบียนเฉพาะ (ถ้าสถานที่มีการควบคุมป้ายทะเบียน)</span><span class="sxs-lookup"><span data-stu-id="cde33-677">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="cde33-678">เลือก <strong>การเปลี่ยนแปลงสถานะสินค้าคงคลัง</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-678">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="cde33-679">ตั้งค่าฟิลด์ <strong>สถานะของสินค้าคงคลัง</strong> เป็น <strong>การบล็อค</strong></span><span class="sxs-lookup"><span data-stu-id="cde33-679">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="cde33-680">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="cde33-681">ปริมาณถูกจองใหม่สำหรับชุดงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cde33-681">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="cde33-682">ระบบจะกำหนดสถานที่และป้ายทะเบียนแบบสุ่ม (ถ้าสถานที่มีการควบคุมป้ายทะเบียน) ที่ซึ่งปริมาณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-682">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cde33-683">ไม่</span><span class="sxs-lookup"><span data-stu-id="cde33-683">No</span></span></td>
<td><span data-ttu-id="cde33-684">ดูแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cde33-684">See the previous row.</span></span></td>
<td><span data-ttu-id="cde33-685">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลังสำหรับปริมาณที่จองไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="cde33-685">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="cde33-686">ไม่อนุญาตให้มีการเปลี่ยนแปลงสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cde33-686">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="cde33-687">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="cde33-687">Limitations</span></span>

- <span data-ttu-id="cde33-688">ฟังก์ชันการจองมิติของระดับคลังสินค้าแบบยืดหยุ่นไม่สนับสนุนคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cde33-688">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="cde33-689">การจัดการน้ำหนักจริง</span><span class="sxs-lookup"><span data-stu-id="cde33-689">Catch weight management</span></span>
    - <span data-ttu-id="cde33-690">สินค้าคงคลังค่าลบที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="cde33-690">Physical negative inventory</span></span>
    - <span data-ttu-id="cde33-691">การจองสินค้าเทียบกับการจัดหาวัสดุที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="cde33-691">Reservation against ordered supply</span></span>
    - <span data-ttu-id="cde33-692">ใบสั่งโอนย้ายและการเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="cde33-692">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="cde33-693">กฎการรวมคอนเทนเนอร์สำหรับการบรรจุตามหน่วยคำสั่งมีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="cde33-693">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="cde33-694">สำหรับการจองที่กำหนดให้กับใบสั่ง เราขอแนะนำว่าคุณไม่ควรใช้เท็มเพลตการสร้างคอนเทนเนอร์ที่ซึ่งฟิลด์ **บรรจุตามหน่วยคำสั่ง** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cde33-694">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="cde33-695">ในการออกแบบปัจจุบัน คำสั่งสถานที่ไม่ได้ถูกใช้ เมื่อมีการสร้างงานในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-695">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="cde33-696">ดังนั้น จึงมีการใช้เฉพาะหน่วยที่ต่ำที่สุดในกลุ่มลำดับหน่วย (หน่วยสินค้าคงคลัง) ในระหว่างขั้นตอนการเวฟการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-696">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>

## <a name="see-also"></a><span data-ttu-id="cde33-697">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="cde33-697">See also</span></span>

- [<span data-ttu-id="cde33-698">หมายเลขชุดงานในการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-698">Batch numbers in Warehouse management</span></span>](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [<span data-ttu-id="cde33-699">สำรองชุดงานเดียวกันสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cde33-699">Reserve the same batch for a sales order</span></span>](../sales-marketing/reserve-same-batch-sales-order.md)
- [<span data-ttu-id="cde33-700">เลือกชุดงานที่เก่าที่สุดในอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="cde33-700">Pick oldest batch on a mobile device</span></span>](pick-oldest-batch.md)
- [<span data-ttu-id="cde33-701">การยืนยันชุดงานและป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="cde33-701">Batch and license plate confirmation</span></span>](batch-and-license-plate-confirmation.md)
- [<span data-ttu-id="cde33-702">แก้ไขการจองสินค้าในการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cde33-702">Troubleshoot reservations in warehouse management</span></span>](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]