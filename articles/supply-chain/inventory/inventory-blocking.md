---
title: "การบล็อคสินค้าคงคลัง"
description: "บทความนี้แสดงภาพรวมของการบล็อคสินค้าคงคลัง ซึ่งเป็นส่วนหนึ่งของกระบวนการตรวจสอบคุณภาพใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition คุณสามารถใช้การบล็อคสินค้าคงคลังเพื่อป้องกันไม่ให้สินค้ามีการประมวลผลหรือใช้"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: eb8040531ec0c2b9c13fc927e5330772ad11ee1d
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-blocking"></a><span data-ttu-id="844e7-104">การบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="844e7-104">Inventory blocking</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="844e7-105">บทความนี้แสดงภาพรวมของการบล็อคสินค้าคงคลัง ซึ่งเป็นส่วนหนึ่งของกระบวนการตรวจสอบคุณภาพใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="844e7-105">This article provides an overview of inventory blocking, which is part of the quality inspection process in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="844e7-106">คุณสามารถใช้การบล็อคสินค้าคงคลังเพื่อป้องกันไม่ให้สินค้ามีการประมวลผลหรือใช้</span><span class="sxs-lookup"><span data-stu-id="844e7-106">You can use inventory blocking to prevent items from being processed or consumed.</span></span>

<span data-ttu-id="844e7-107">คุณสามารถบล็อคสินค้าคงคลังได้ดังวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="844e7-107">You can block inventory items in the following ways:</span></span>
-   <span data-ttu-id="844e7-108">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="844e7-108">Manually</span></span>
-   <span data-ttu-id="844e7-109">โดยการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-109">By creating a quality order</span></span>
-   <span data-ttu-id="844e7-110">โดยใช้กระบวนการที่สร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-110">By using a process that generates a quality order</span></span>
-   <span data-ttu-id="844e7-111">โดยใช้การบล็อคสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="844e7-111">By using inventory status blocking</span></span>

## <a name="blocking-items-manually"></a><span data-ttu-id="844e7-112">การบล็อคสินค้าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="844e7-112">Blocking items manually</span></span>
<span data-ttu-id="844e7-113">คุณสามารถบล็อคปริมาณสินค้าด้วยการสร้างธุรกรรมในหน้า **การบล็อคสินค้าคงคลัง** ได้</span><span class="sxs-lookup"><span data-stu-id="844e7-113">You can block a quantity of an item by creating a transaction on the **Inventory blocking** page.</span></span> <span data-ttu-id="844e7-114">เฉพาะสินค้าที่พร้อมใช้ที่เป็นสินค้าคงคลังคงเหลือทสามารถถูกบล็อคได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="844e7-114">Only items that are available as on-hand inventory can be blocked manually.</span></span> <span data-ttu-id="844e7-115">สำหรับปริมาณที่ถูกบล็อคด้วยตนเอง คุณต้องตัดสินใจว่ากิจกรรมการวางแผนจะรวมใบรับสินค้าที่คาดไว้เป็นปริมาณคงเหลือคาดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="844e7-115">For manually blocked quantities, you must decide whether planning activities include expected receipts as an expected on-hand quantity.</span></span> <span data-ttu-id="844e7-116">การรับสินค้าที่คาดไว้เป็นสินค้าที่ถูกบล็อคที่คุณคาดว่าจะพร้อมใช้งาน ซึ่งอยู่ในรูปของสินค้าคงคลังคงเหลือหลังจากการตรวจสอบเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="844e7-116">Expected receipts are blocked items that you expect to be available as on-hand inventory after inspection is completed.</span></span> <span data-ttu-id="844e7-117">คุณสามารถเก็บรักษาวันที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="844e7-117">You can maintain the expected date.</span></span> <span data-ttu-id="844e7-118">โดยค่าเริ่มต้น ตัวเลือก **การรับสินค้าที่คาดไว้** จะถูกเลือกสำหรับสินค้าที่ถูกบล็อคโดยใช้ใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-118">By default, the **Expected receipts** option is selected for items that are blocked through a quality order.</span></span> <span data-ttu-id="844e7-119">คุณสามารถยกเลิกการบล็อคปริมาณด้วยตนเอง ด้วยการลบธุรกรรมในหน้า **การบล็อคสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="844e7-119">You can cancel a manual block on a quantity by deleting the transaction on the **Inventory blocking** page.</span></span>

## <a name="blocking-items-by-creating-a-quality-order"></a><span data-ttu-id="844e7-120">การบล็อคสินค้าโดยการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-120">Blocking items by creating a quality order</span></span>
<span data-ttu-id="844e7-121">คุณสามารถระบุสินค้าที่ต้องถูกตรวจสอบได้โดยการสร้างใบสั่งตรวจสอบคุณภาพในหน้า **ใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="844e7-121">You can specify items that must be inspected by creating a quality order on the **Quality orders** page.</span></span> <span data-ttu-id="844e7-122">เมื่อคุณสร้างใบสั่งตรวจสอบคุณภาพ ปริมาณที่คุณระบุไว้สำหรับสินค้าจะถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="844e7-122">When you create a quality order, the quantity that you specify for an item is blocked.</span></span> <span data-ttu-id="844e7-123">แผนการสุ่มตัวอย่างที่เชื่อมโยงกับใบสั่งตรวจสอบคุณภาพควบคุมเฉพาะปริมาณของสินค้าที่ต้องถูกตรวจสอบ ไม่ใช่ปริมาณที่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="844e7-123">The sampling plan that is associated with a quality order controls only the quantity of items that must be inspected, not the quantity that is blocked.</span></span> <span data-ttu-id="844e7-124">ปริมาณที่ถูกป้อนบนใบสั่งตรวจสอบคุณภาพคือปริมาณที่ถูกบล็อค โดยไม่คำนึงถึงปริมาณที่การระบุแผนการสุ่มตัวอย่างควรถูกส่งไปเพื่อการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="844e7-124">The quantity that is entered on the quality order is the quantity that is blocked, regardless of the quantity that the sampling plan specifies should be sent for inspection.</span></span>

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a><span data-ttu-id="844e7-125">การบล็อคสินค้าโดยใช้กระบวนการที่สร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-125">Blocking items by using a process that generates a quality order</span></span>
<span data-ttu-id="844e7-126">ถ้ากระบวนการตรวจสอบคุณภาพระบุว่าต้องตรวจสอบสินค้า ปริมาณของสินค้าจะถูกบล็อคโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="844e7-126">If a quality process specifies that an item must be inspected, a quantity of the item is blocked automatically.</span></span> <span data-ttu-id="844e7-127">ดังนั้น เมื่อมีการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ แผนการสุ่มตัวอย่างสินค้าที่เชื่อมโยงกับใบสั่งตรวจสอบคุณภาพจะควบคุมทั้งปริมาณของสินค้าที่ถูกบล็อคและปริมาณที่ต้องถูกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="844e7-127">Therefore, when a quality order is generated automatically, the item sampling plan that is associated with the quality order controls the both quantity of items that is blocked and the quantity that must be inspected.</span></span> <span data-ttu-id="844e7-128">ถ้าตัวเลือก **การบล็อคทั้งหมด** ในหน้า **การสุ่มตัวอย่างสินค้า** ถูกเลือก ปริมาณทั้งหมดของ ตัวอย่างเช่น รายการใบสั่งซื้อจะถูกบล็อคในระหว่างการตรวจสอบ โดยไม่คำนึงถึงปริมาณการสุ่มตัวอย่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="844e7-128">If the **Full blocking** option on the **Item sampling** page is selected, the full quantity of, for example, a purchase order line is blocked during inspection, regardless of the item sampling quantity.</span></span>
### <a name="example"></a><span data-ttu-id="844e7-129">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="844e7-129">Example</span></span>

<span data-ttu-id="844e7-130">ในตัวอย่างต่อไปนี้ ใบสั่งตรวจสอบคุณภาพจะถูกสร้างขึ้นเมื่อมีการลงรายการบัญชีบันทึกการจัดส่งใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="844e7-130">In the following example, a quality order is generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="844e7-131">ในหน้า **การเชื่อมโยงคุณภาพ** คุณระบุว่าการลงรายการบัญชีบันทึกการจัดส่งใบสั่งซื้อเป็นกระบวนการที่เรียกใช้งานใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-131">On the **Quality associations** page, you specified that posting of a purchase order packing slip is the process that activates a quality order.</span></span>

|<span data-ttu-id="844e7-132">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="844e7-132">Setup</span></span>                                                                     |<span data-ttu-id="844e7-133">การดำเนินการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="844e7-133">User action</span></span>                 |<span data-ttu-id="844e7-134">ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="844e7-134">Result</span></span>             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| <span data-ttu-id="844e7-135">การเชื่อมโยงคุณภาพระบุว่าต้องมีการสร้างใบสั่งตรวจสอบคุณภาพ เมื่อมีการลงรายการบัญชีบันทึกการจัดส่งใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="844e7-135">A quality association specifies that a quality order must be generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="844e7-136">การตั้งค่าการสุ่มตัวอย่างสินค้าของใบสั่งตรวจสอบคุณภาพระบุว่าต้องตรวจสอบ 10% ของปริมาณในรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="844e7-136">The item sampling setup of the quality order specifies that 10 percent of the quantity on the purchase order line must be inspected.</span></span> <span data-ttu-id="844e7-137">นอกจากนี้ เนื่องจากตัวเลือก **การบล็อคทั้งหมด** ได้เลือกการตั้งค่าการสุ่มตัวอย่างสินค้า ปริมาณทั้งหมดของรายการใบสั่งซื้อต้องถูกบล็อคในระหว่างการตรวจสอบอย่างละเอียด โดยไม่คำนึงถึงปริมาณที่ถูกส่งไปตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="844e7-137">Furthermore, because the **Full blocking** option selected in the item sampling setup, the full quantity of the purchase order line must be blocked during inspection, regardless of the quantity that is sent for inspection.</span></span> | <span data-ttu-id="844e7-138">ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="844e7-138">The packing slip is posted.</span></span> | <span data-ttu-id="844e7-139">มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-139">A quality order is generated.</span></span> <span data-ttu-id="844e7-140">10% ของปริมาณใบสั่งซื้อสำหรับสินค้าที่ถูกส่งไปตรวจสอบอย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="844e7-140">Ten percent of the purchase order quantity for the item is sent to inspection.</span></span> <span data-ttu-id="844e7-141">ปริมาณทั้งหมดของบรรทัดใบสั่งซื้อทั้งหมดถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="844e7-141">The full quantity of the purchase order line is blocked.</span></span> |

## <a name="blocking-items-by-using-inventory-status-blocking"></a><span data-ttu-id="844e7-142">การบล็อคสินค้าโดยใช้การบล็อคสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="844e7-142">Blocking items by using inventory status blocking</span></span>
<span data-ttu-id="844e7-143">คุณสามารถระบุว่าสถานะสินค้าคงคลังใดเป็นสถานะการบล็อคโดยใช้พารามิเตอร์ **การบล็อคสินค้าคงคลัง** บนหน้า **สถานะสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="844e7-143">You can specify which inventory statuses are blocking statuses by using the **Inventory blocking** parameter on the **Inventory statuses** page.</span></span> <span data-ttu-id="844e7-144"> คุณไม่สามารถใช้สถานะสินค้าคงคลังเป็นสถานะการบล็อคสำหรับใบสั่งผลิต ใบสั่งขาย ใบสั่งโอนย้าย ธุรกรรมขาออก หรือการรวมโครงการได้</span><span class="sxs-lookup"><span data-stu-id="844e7-144">You can't use inventory statuses as blocking statuses for production orders, sales orders, transfer orders, outbound transactions, or project integrations.</span></span> <span data-ttu-id="844e7-145">สำหรับงานขาออก ใช้สินค้าที่มีสถานะสินค้าคงคลังที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="844e7-145">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="844e7-146">ถ้าสินค้ามีสถานะเป็น **ไม่ทำงาน**และการวางแผนหลักมีการดำเนินงานกับสินค้าเหล่านั้น สินค้าจะถูกพิจารณาเป็นการขาด และสินค้าคงคลังจะมีการเติมโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="844e7-146">If items have a status of **Broken**, and master planning is run on those items, the items are considered missing, and inventory is automatically replenished.</span></span>



<a name="see-also"></a><span data-ttu-id="844e7-147">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="844e7-147">See also</span></span>
--------

<span data-ttu-id="844e7-148">[สร้างและรักษาการบล็อคสินค้าคงคลัง (คู่มืองาน)](tasks/create-maintain-inventory-blocking.md</span><span class="sxs-lookup"><span data-stu-id="844e7-148">[Create and maintain an inventory blocking (Task guide)](tasks/create-maintain-inventory-blocking.md</span></span>

[<span data-ttu-id="844e7-149">กระบวนการการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="844e7-149">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="844e7-150">ตรวจสอบคุณภาพของสินค้า (คู่มืองาน)</span><span class="sxs-lookup"><span data-stu-id="844e7-150">Inspect the quality of goods (Task guide)</span></span>](tasks/inspect-quality-goods.md)

