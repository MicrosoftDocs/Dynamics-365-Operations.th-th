---
title: แก้ไขปัญหาการตั้งค่าคอนฟิกคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณตั้ตั้งค่าคอนฟิก Microsoft Dynamics 365 Supply Chain Management
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646118"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="e0d17-103">แก้ไขปัญหาการตั้งค่าคอนฟิกคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="e0d17-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0d17-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณตั้ตั้งค่าคอนฟิก Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e0d17-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="e0d17-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ป้ายทะเบียนหรือสถานที่ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0d17-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d17-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-106">Issue description</span></span>

<span data-ttu-id="e0d17-107">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้เมื่อคุณสแกนรหัสป้ายทะเบียนหรือสถานที่</span><span class="sxs-lookup"><span data-stu-id="e0d17-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d17-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-108">Issue resolution</span></span>

<span data-ttu-id="e0d17-109">ตรวจสอบให้แน่ใจว่ารหัสป้ายทะเบียนไม่ถูกจองโดยอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="e0d17-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="e0d17-110">ปัญหานี้จะเกิดขึ้นเมื่อมีการใช้ค่าที่ผู้ใช้สแกนในแอปคลังสินค้าเป็นทั้งสถานที่ที่ถูกต้องและรหัสป้ายทะเบียนที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0d17-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="e0d17-111">อย่างไรก็ตาม ปัญหานี้ได้รับการแก้ไขแล้วในรุ่น10.0.11</span><span class="sxs-lookup"><span data-stu-id="e0d17-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="e0d17-112">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ป้ายทะเบียต้องระบุสำหรับสถานที่"</span><span class="sxs-lookup"><span data-stu-id="e0d17-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d17-113">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-113">Issue description</span></span>

<span data-ttu-id="e0d17-114">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้ถ้าคุณสร้างใบสั่งโอนย้ายโดยใช้คลังสินค้าที่เปิดใช้งานสำหรับการจัดการคลังสินค้าขั้นสูง (WMS), แล้ว หลังจากงานเสร็จสมบูรณ์แล้ว คุณพยายามยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="e0d17-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d17-115">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-115">Issue resolution</span></span>

<span data-ttu-id="e0d17-116">ฟิลด์ **สถานที่รับสินค้าเริ่มต้น** จะว่างเปล่าสำหรับคลังสินค้าส่งต่อของคลังสินค้า "เริ่มต้น"</span><span class="sxs-lookup"><span data-stu-id="e0d17-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="e0d17-117">เมื่อต้องการแก้ไขปัญหานี้ ให้ระบุสถานที่รับสินค้าเริ่มต้นในคลังสินค้าส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="e0d17-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="e0d17-118">ตรวจสอบให้แน่ใจว่าที่ตั้งนี้เป็นป้ายทะเบียนที่ควบคุม</span><span class="sxs-lookup"><span data-stu-id="e0d17-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="e0d17-119">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "คุณไม่สามารถสร้างรายการแม่แบบงานสำหรับการเปลี่ยนสถานะสินค้าคงคลังได้เนื่องจากชนิดงานไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0d17-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="e0d17-120">เลือกชนิดงานที่แตกต่างกัน"</span><span class="sxs-lookup"><span data-stu-id="e0d17-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d17-121">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-121">Issue description</span></span>

<span data-ttu-id="e0d17-122">สำหรับแม่แบบงาน คุณไม่สามารถเลือก *การเปลี่ยนสถานะสินค้าคงคลัง* ในคอลัมน์ **ชนิดงาน** ของส่วน **รายละเอียดแม่แบบงาน**</span><span class="sxs-lookup"><span data-stu-id="e0d17-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d17-123">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-123">Issue resolution</span></span>

<span data-ttu-id="e0d17-124">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="e0d17-124">This behavior is by design.</span></span> <span data-ttu-id="e0d17-125">ชนิดงาน *การเปลี่ยนสถานะสินค้าคงคลัง* จะใช้โดยกระบวนการของระบบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e0d17-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="e0d17-126">ซึ่งไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="e0d17-126">It can't be configured.</span></span> <span data-ttu-id="e0d17-127">เนื่องจากรายการของชนิดงานได้รับการแก้ไขเป็นการแจงนับ รายการพิเศษจะไม่สามารถถูกกรองออกจากเมนูแบบหล่นลง **ชนิดงาน**</span><span class="sxs-lookup"><span data-stu-id="e0d17-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="e0d17-128">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณไม่ถูกต้องสำหรับหน่วย 1%"</span><span class="sxs-lookup"><span data-stu-id="e0d17-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d17-129">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-129">Issue description</span></span>

<span data-ttu-id="e0d17-130">ปริมาณไม่ถูกต้องสำหรับหน่วย *ea* เมื่อมีงานการเบิกสินค้าที่มีป้ายทะเบียนหลายใบในสถานที่เดียว</span><span class="sxs-lookup"><span data-stu-id="e0d17-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d17-131">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-131">Issue resolution</span></span>

<span data-ttu-id="e0d17-132">ตรวจสอบว่ามีการตั้งค่า **รหัสกลุ่มลำดับของหน่วย** และ **การแปลงหน่วย** บนผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0d17-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="e0d17-133">โปรดสังเกตว่าข้อความแสดงข้อผิดพลาดได้รับการปรับปรุงในรุ่น 10.0.15 (โปรดดูที่ [4581627 KB](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531))</span><span class="sxs-lookup"><span data-stu-id="e0d17-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="e0d17-134">ข้อความแสดงข้อผิดพลาดใหม่คือ "ปริมาณไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0d17-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="e0d17-135">ที่คาดไว้ %1 %2"</span><span class="sxs-lookup"><span data-stu-id="e0d17-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="e0d17-136">ในคำสั่งสถานที่สำหรับการทำงานการนำใบสั่งขายออกใช้ ตัวเลือกหลาย SKU จะไม่ประเมินการดำเนินการคำสั่งของสถานที่ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="e0d17-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d17-137">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-137">Issue description</span></span>

<span data-ttu-id="e0d17-138">คำสั่งสถานที่ของชนิดใบสั่งงาน *ใบสั่งขาย* และชนิดงาน *สำรอง* ไม่ประเมินการดำเนินการคำสั่งของสถานที่ต่าง ๆ เมื่อตัวเลือก **หลาย SKU** ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="e0d17-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="e0d17-139">มีการประเมินเฉพาะการดำเนินการคำสั่งสถานที่แรกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e0d17-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d17-140">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-140">Issue resolution</span></span>

<span data-ttu-id="e0d17-141">ลักษณะการทำงานใหม่ *ประเมินการดำเนินการทั้งหมดสำหรับคำสั่งที่ตั้งหลาย SKU* ซึ่งถูกเพิ่มเข้าในรุ่น 10.0.15 (โปรดดูที่ [4579866 KB](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091))</span><span class="sxs-lookup"><span data-stu-id="e0d17-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="e0d17-142">ลักษณะการทำงานนี้จะประเมินการดำเนินการทั้งหมดสำหรับคำสั่งที่ตั้งหลาย SKU</span><span class="sxs-lookup"><span data-stu-id="e0d17-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="e0d17-143">ถ้าคุณต้องการใช้ลักษณะการทำงานนี้ ให้ใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e0d17-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="e0d17-144">ฉันไม่สามารถใช้แอปคลังสินค้าเพื่อทำการเบิกสินค้าบางส่วน</span><span class="sxs-lookup"><span data-stu-id="e0d17-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d17-145">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-145">Issue description</span></span>

<span data-ttu-id="e0d17-146">สำหรับใบสั่งขายและใบสั่งโอนย้าย คุณไม่สามารถข้ามสินค้าและทำการเบิกสินค้าบางส่วน</span><span class="sxs-lookup"><span data-stu-id="e0d17-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d17-147">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-147">Issue resolution</span></span>

<span data-ttu-id="e0d17-148">บนหน้า **รายการเมนูของอุปกรณ์เคลื่อนที่** สำหรับรายการเมนูแต่ละรายการที่มีการตั้งค่าให้ประมวลผลใบสั่งขายหรือใบสั่งโอนย้าย ให้ตั้งค่าตัวเลือก **อนุญาตให้มีการแบ่งงาน** บนแท็บด่วน **ทั่วไป** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="e0d17-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="e0d17-149">ฉันจะเปลี่ยนสถานะสินค้าคงคลังสำหรับการทำงานของปริมาณบางส่วนได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="e0d17-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d17-150">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-150">Issue description</span></span>

<span data-ttu-id="e0d17-151">คุณต้องการทำการเปลี่ยนสถานะสินค้าคงคลังสำหรับปริมาณบางส่วนของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="e0d17-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d17-152">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e0d17-152">Issue resolution</span></span>

<span data-ttu-id="e0d17-153">เมื่อต้องการให้ผู้ปฏิบัติงานสามารถทำการเปลี่ยนแปลงนี้ได้ คุณสามารถสร้างรายการเมนูสำหรับแอปคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="e0d17-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="e0d17-154">ในหน้า **รายการเมนูของอุปกรณ์เคลื่อนที่** สร้าง (หรือแก้ไข) รายการเมนูสำหรับหนึ่งในวิธีต่อไปนี้ :</span><span class="sxs-lookup"><span data-stu-id="e0d17-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="e0d17-155">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="e0d17-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="e0d17-156">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="e0d17-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="e0d17-157">**กระบวนการสร้างงาน:** *ความเคลื่อนไหว*</span><span class="sxs-lookup"><span data-stu-id="e0d17-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="e0d17-158">**แสดงสถานะสินค้าคงคลัง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="e0d17-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="e0d17-159">คุณสามารถตั้งฟิลด์อื่น ๆ บนหน้าได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="e0d17-159">You can set other fields on the page as you require.</span></span>
