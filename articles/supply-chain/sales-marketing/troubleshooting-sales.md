---
title: แก้ไขปัญหาใบสั่งขาย
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบสั่งขาย
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974796"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="3fcb1-103">แก้ไขปัญหาใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="3fcb1-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="3fcb1-105">ข้อมูลภาษีไม่ได้รับการอัปเดตเมื่อเปลี่ยนสถานที่บนส่วนหน้าของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3fcb1-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-106">Issue description</span></span>

<span data-ttu-id="3fcb1-107">ถ้ามีการเปลี่ยนแปลงไซต์คลังสินค้าหรือที่อยู่ที่จัดส่งในส่วนหน้าของใบสั่งขายหรือในระดับบรรทัด จะไม่มีการอัปเดตข้อมูลภาษีกรณีและปัญหาสำหรับบรรทัดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3fcb1-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-108">Issue resolution</span></span>

<span data-ttu-id="3fcb1-109">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-109">This behavior is by design.</span></span> <span data-ttu-id="3fcb1-110">ปัญหานี้เกิดขึ้นเนื่องจากที่อยู่ที่จัดส่ง ไซต์ และคลังสินค้าจะไม่มีการเปลี่ยนแปลงโดยอัตโนมัติในระดับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="3fcb1-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="3fcb1-111">คุณต้องอัปเดตด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="3fcb1-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="3fcb1-112">ถ้ามีข้อตกลงทางการค้าสองฉบับสำหรับรอบระยะเวลาเดียวกันหรือรอบระยะเวลาที่ทับซ้อนกันจะมีการเลือกรายการข้อตกลงเดียวกันเสมอ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3fcb1-113">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-113">Issue description</span></span>

<span data-ttu-id="3fcb1-114">ถ้ามีการกำหนดข้อตกลงทางการค้าสองฉบับสำหรับรอบระยะเวลาเดียวกันหรือรอบระยะเวลาที่ทับซ้อนกัน ต้องเลือกข้อตกลงทางการค้าเดียวกันทุกครั้งเมื่อคุณสร้างบรรทัดใบสั่งขายที่มีสินค้าเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fcb1-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3fcb1-115">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-115">Issue resolution</span></span>

<span data-ttu-id="3fcb1-116">ถ้ามีข้อตกลงทางการค้ามากกว่าหนึ่งข้อตกลงสำหรับวันที่ที่กำหนด ข้อตกลงทางการค้าที่มีราคาต่ำสุดจะถูกเลือกเสมอ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="3fcb1-117">สำหรับข้อมูลเพิ่มเติมให้ดูที่เอกสารต่อไปนี้: [ข้อตกลงทางการค้าใน Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90)</span><span class="sxs-lookup"><span data-stu-id="3fcb1-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="3fcb1-118">ฉันสามารถเชื่อมโยงใบสั่งซื้อกับใบสั่งขายเพื่อตอบสนองความต้องการได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3fcb1-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="3fcb1-119">คุณสามารถสร้างใบสั่งซื้อจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="3fcb1-120">สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างใบสั่งซื้อจากใบสั่งขาย](tasks/create-purchase-order-sales-order.md)</span><span class="sxs-lookup"><span data-stu-id="3fcb1-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="3fcb1-121">ฉันไม่สามารถยกเลิกหรือลบใบสั่งส่งคืนสินค้าหรือใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="3fcb1-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="3fcb1-122">คุณสามารถยกเลิกได้เฉพาะใบสั่งขายและใบสั่งส่งคืนสินค้าที่อยู่ในสถานะ *สร้างแล้ว* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fcb1-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="3fcb1-123">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกใบสั่งส่งคืน](../service-management/cancel-return-order.md)</span><span class="sxs-lookup"><span data-stu-id="3fcb1-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="3fcb1-124">เมื่อฉันพยายามยกเลิกใบสั่งขาย ฉันจะได้รับข้อผิดพลาด "ไม่สามารถลบการจองได้เนื่องจากมีงานที่สร้างขึ้นซึ่งอาศัยการจอง"</span><span class="sxs-lookup"><span data-stu-id="3fcb1-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="3fcb1-125">รหัสข้อผิดพลาด: WAX4661</span><span class="sxs-lookup"><span data-stu-id="3fcb1-125">Error code: WAX4661</span></span>

<span data-ttu-id="3fcb1-126">ถ้างานสัมพันธ์กับใบสั่งขาย คุณจะไม่สามารถยกเลิกใบสั่งขายได้จนกว่างานจะถูกยกเลิกและกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="3fcb1-127">ข้อกำหนดนี้ใช้ได้ ถึงแม้ว่างานที่เชื่อมโยงกับใบสั่งขายปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="3fcb1-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="3fcb1-128">เพื่อแก้ไขปัญหานี้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="3fcb1-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="3fcb1-129">ยกเลิกงานและวางสินค้าคงคลังกลับไปยังสถานที่ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="3fcb1-130">ไปที่จำนวนงานในศูนย์การผลิตที่เกี่ยวข้องและเลือก **ลดปริมาณที่เบิกสินค้า** ในรายการจำนวนงานในศูนย์การผลิตหรือ **งานย้อนกลับ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="3fcb1-131">ขณะนี้งานมีสถานะเป็น *ยกเลิกแล้ว* และงานการเคลื่อนย้ายสินค้าคงคลังใหม่จะถูกสร้างขึ้นโดยอัตโนมัติและประมวลผลเพื่อใส่สินค้าคงคลังกลับไปยังสถานที่ที่มีการอธิบายไว้ในขณะที่มีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="3fcb1-132">ลบงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="3fcb1-132">Delete the load.</span></span> <span data-ttu-id="3fcb1-133">การจัดส่งสินค้าจะถูกลบด้วย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="3fcb1-134">ขณะนี้คุณควรจะสามารถไปที่ใบสั่งขายและยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="3fcb1-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="3fcb1-135">ฉันไม่สามารถยกเลิกใบสั่งซื้อระหว่างบริษัทที่เชื่อมโยงกับใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="3fcb1-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3fcb1-136">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-136">Issue description</span></span>

<span data-ttu-id="3fcb1-137">ถ้าคุณพยายามยกเลิกใบสั่งซื้อระหว่างบริษัทที่เชื่อมโยงกับใบสั่งขาย คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่สามารถลดปริมาณได้เนื่องจากปริมาณการอัปเดตที่เหลือเปลี่ยนเครื่องหมาย"</span><span class="sxs-lookup"><span data-stu-id="3fcb1-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3fcb1-138">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-138">Issue resolution</span></span>

<span data-ttu-id="3fcb1-139">ปัญหานี้ได้รับการแก้ไขใน Microsoft Dynamics 365 Supply Chain Management รุ่น 10.0.13</span><span class="sxs-lookup"><span data-stu-id="3fcb1-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="3fcb1-140">ขณะนี้คุณสามารถยกเลิกใบสั่งซื้อระหว่างบริษัทที่เชื่อมโยงกับใบสั่งขายได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="3fcb1-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="3fcb1-141">ฉันสามารถเรียกคืนใบสั่งขายที่ออกใบแจ้งหนี้แล้วได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3fcb1-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="3fcb1-142">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-142">Issue description</span></span>

<span data-ttu-id="3fcb1-143">ใบสั่งขายที่ออกใบแจ้งหนี้แล้วถูกลบออกโดยไม่ได้ตั้งใจและคุณต้องการคืนค่าหรือดูรายละเอียดของใบสั่งขายนั้น</span><span class="sxs-lookup"><span data-stu-id="3fcb1-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3fcb1-144">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="3fcb1-144">Issue resolution</span></span>

<span data-ttu-id="3fcb1-145">ถ้ามีการออกใบแจ้งหนี้ใบสั่งขายที่ถูกลบไปแล้ว ให้ไปที่ **บัญชีลูกค้า \> ธุรกรรม \> เอกสารต้นฉบับ \> รายละเอียดมุมมอง**</span><span class="sxs-lookup"><span data-stu-id="3fcb1-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="3fcb1-146">ค้นหาใบแจ้งหนี้ที่คุณกำลังค้นหาและเลือกใบแจ้งหนี้เพื่อดูรายละเอียดของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="3fcb1-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="3fcb1-147">รายละเอียดเหล่านี้รวมถึงการอ้างอิงใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-147">These details include the sales order reference.</span></span> <span data-ttu-id="3fcb1-148">นอกจากนี้คุณยังสามารถเข้าถึงรายละเอียดใบสั่งขายจากหน้าดังกล่าวได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="3fcb1-149">ไม่พบวันที่สิ้นสุดของส่วนหน้าของใบสั่งขายในเอนทิตีข้อมูล SalesOrderHeaderV2Entity</span><span class="sxs-lookup"><span data-stu-id="3fcb1-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="3fcb1-150">ไม่มีฟิลด์กำหนดเวลาสิ้นสุดอยู่บนเอนทิตี *SalesOrderHeaderV2Entity*</span><span class="sxs-lookup"><span data-stu-id="3fcb1-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="3fcb1-151">ฉันต้องลบเรกคอร์ดใบสั่งขายที่ถูกละเลย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="3fcb1-152">เมื่อต้องการล้างข้อมูลเรกคอร์ดใบสั่งขายที่ไม่ได้ใช้งานอยู่ ให้รันงานประจำงวดของ *การลบใบสั่งขาย* โดยไปที่สถานที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3fcb1-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="3fcb1-153">การขายและการตลาด \> งานประจำงวด \> ล้าง \> ลบใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="3fcb1-154">การขายปลีกและการค้า \> การขายปลีก และ COMMERCE IT \> ล้างข้อมูลการ \> ลบใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3fcb1-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="3fcb1-155">มีวิธีการคำนวณค่าคอมมิชชันสำหรับใบแจ้งหนี้ที่มีการลงรายการบัญชีแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3fcb1-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="3fcb1-156">ปัจจุบัน Supply Chain Management ไม่สนับสนุนการคำนวณค่าคอมมิชชันสำหรับใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="3fcb1-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="3fcb1-157">สินค้าที่มีการขายรวมไม่ได้รับการสนับสนุนในกระบวนการระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="3fcb1-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="3fcb1-158">สินค้าที่มีการขายรวมจะไม่พร้อมใช้งานสำหรับใบสั่งซื้อเนื่องจากถ้าคุณตรวจสอบบรรทัดใบสั่งขายสำหรับสินค้าที่มีการขายรวม คุณจะสังเกตเห็นว่าปริมาณเป็น *0* (ศูนย์) และสถานะคือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="3fcb1-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="3fcb1-159">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="3fcb1-159">This behavior is by design.</span></span> <span data-ttu-id="3fcb1-160">ใบสั่งขายจะซื้อเฉพาะส่วนประกอบของสินค้าที่มีการขายรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fcb1-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="3fcb1-161">ไม่มีการซื้อสินค้าที่มีการขายรวม</span><span class="sxs-lookup"><span data-stu-id="3fcb1-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="3fcb1-162">ถ้าคุณต้องการซื้อกลุ่มงาน ให้พิจารณาว่าคุณต้องทำเครื่องหมายเป็นสินค้าที่มีการขายรวม เนื่องจากฟังก์ชันนี้ได้รับการออกแบบมาสำหรับสถานการณ์การรับรู้รายได้จริงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3fcb1-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="3fcb1-163">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสินค้าที่มีการขายรวม ให้ดูที่ [การขายรวม](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles)</span><span class="sxs-lookup"><span data-stu-id="3fcb1-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
