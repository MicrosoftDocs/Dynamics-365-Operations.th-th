---
title: แก้ไขปัญหาการตั้งค่าคอนฟิกคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณตั้ตั้งค่าคอนฟิก Microsoft Dynamics 365 Supply Chain Management
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814403"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="abde8-103">แก้ไขปัญหาการตั้งค่าคอนฟิกคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="abde8-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abde8-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณตั้ตั้งค่าคอนฟิก Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="abde8-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="abde8-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ป้ายทะเบียนหรือสถานที่ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="abde8-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-106">Issue description</span></span>

<span data-ttu-id="abde8-107">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้เมื่อคุณสแกนรหัสป้ายทะเบียนหรือสถานที่</span><span class="sxs-lookup"><span data-stu-id="abde8-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-108">Issue resolution</span></span>

<span data-ttu-id="abde8-109">ตรวจสอบให้แน่ใจว่ารหัสป้ายทะเบียนไม่ถูกจองโดยอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="abde8-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="abde8-110">ปัญหานี้จะเกิดขึ้นเมื่อมีการใช้ค่าที่ผู้ใช้สแกนในแอปการจัดการคลังสินค้าบนมือถือเป็นทั้งสถานที่ที่ถูกต้องและรหัสป้ายทะเบียนที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="abde8-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="abde8-111">อย่างไรก็ตาม ปัญหานี้ได้รับการแก้ไขแล้วในรุ่น10.0.11</span><span class="sxs-lookup"><span data-stu-id="abde8-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="abde8-112">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ป้ายทะเบียต้องระบุสำหรับสถานที่"</span><span class="sxs-lookup"><span data-stu-id="abde8-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-113">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-113">Issue description</span></span>

<span data-ttu-id="abde8-114">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้ถ้าคุณสร้างใบสั่งโอนย้ายโดยใช้คลังสินค้าที่เปิดใช้งานสำหรับการจัดการคลังสินค้าขั้นสูง (WMS), แล้ว หลังจากงานเสร็จสมบูรณ์แล้ว คุณพยายามยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="abde8-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-115">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-115">Issue resolution</span></span>

<span data-ttu-id="abde8-116">ฟิลด์ **สถานที่รับสินค้าเริ่มต้น** จะว่างเปล่าสำหรับคลังสินค้าส่งต่อของคลังสินค้า "เริ่มต้น"</span><span class="sxs-lookup"><span data-stu-id="abde8-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="abde8-117">เมื่อต้องการแก้ไขปัญหานี้ ให้ระบุสถานที่รับสินค้าเริ่มต้นในคลังสินค้าส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="abde8-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="abde8-118">ตรวจสอบให้แน่ใจว่าที่ตั้งนี้เป็นป้ายทะเบียนที่ควบคุม</span><span class="sxs-lookup"><span data-stu-id="abde8-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="abde8-119">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "คุณไม่สามารถสร้างรายการแม่แบบงานสำหรับการเปลี่ยนสถานะสินค้าคงคลังได้เนื่องจากชนิดงานไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="abde8-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="abde8-120">เลือกชนิดงานที่แตกต่างกัน"</span><span class="sxs-lookup"><span data-stu-id="abde8-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-121">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-121">Issue description</span></span>

<span data-ttu-id="abde8-122">สำหรับแม่แบบงาน คุณไม่สามารถเลือก *การเปลี่ยนสถานะสินค้าคงคลัง* ในคอลัมน์ **ชนิดงาน** ของส่วน **รายละเอียดแม่แบบงาน**</span><span class="sxs-lookup"><span data-stu-id="abde8-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-123">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-123">Issue resolution</span></span>

<span data-ttu-id="abde8-124">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="abde8-124">This behavior is by design.</span></span> <span data-ttu-id="abde8-125">ชนิดงาน *การเปลี่ยนสถานะสินค้าคงคลัง* จะใช้โดยกระบวนการของระบบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="abde8-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="abde8-126">ซึ่งไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="abde8-126">It can't be configured.</span></span> <span data-ttu-id="abde8-127">เนื่องจากรายการของชนิดงานได้รับการแก้ไขเป็นการแจงนับ รายการพิเศษจะไม่สามารถถูกกรองออกจากเมนูแบบหล่นลง **ชนิดงาน**</span><span class="sxs-lookup"><span data-stu-id="abde8-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="abde8-128">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณไม่ถูกต้องสำหรับหน่วย 1%"</span><span class="sxs-lookup"><span data-stu-id="abde8-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-129">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-129">Issue description</span></span>

<span data-ttu-id="abde8-130">ปริมาณไม่ถูกต้องสำหรับหน่วย *ea* เมื่อมีงานการเบิกสินค้าที่มีป้ายทะเบียนหลายใบในสถานที่เดียว</span><span class="sxs-lookup"><span data-stu-id="abde8-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-131">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-131">Issue resolution</span></span>

<span data-ttu-id="abde8-132">ตรวจสอบว่ามีการตั้งค่า **รหัสกลุ่มลำดับของหน่วย** และ **การแปลงหน่วย** บนผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="abde8-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="abde8-133">โปรดสังเกตว่าข้อความแสดงข้อผิดพลาดได้รับการปรับปรุงในรุ่น 10.0.15 (โปรดดูที่ [4581627 KB](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531))</span><span class="sxs-lookup"><span data-stu-id="abde8-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="abde8-134">ข้อความแสดงข้อผิดพลาดใหม่คือ "ปริมาณไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="abde8-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="abde8-135">ที่คาดไว้ %1 %2"</span><span class="sxs-lookup"><span data-stu-id="abde8-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="abde8-136">ในคำสั่งสถานที่สำหรับการทำงานการนำใบสั่งขายออกใช้ ตัวเลือกหลาย SKU จะไม่ประเมินการดำเนินการคำสั่งของสถานที่ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="abde8-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-137">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-137">Issue description</span></span>

<span data-ttu-id="abde8-138">คำสั่งสถานที่ของชนิดใบสั่งงาน *ใบสั่งขาย* และชนิดงาน *สำรอง* ไม่ประเมินการดำเนินการคำสั่งของสถานที่ต่าง ๆ เมื่อตัวเลือก **หลาย SKU** ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="abde8-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="abde8-139">มีการประเมินเฉพาะการดำเนินการคำสั่งสถานที่แรกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="abde8-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-140">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-140">Issue resolution</span></span>

<span data-ttu-id="abde8-141">ลักษณะการทำงานใหม่ *ประเมินการดำเนินการทั้งหมดสำหรับคำสั่งที่ตั้งหลาย SKU* ซึ่งถูกเพิ่มเข้าในรุ่น 10.0.15 (โปรดดูที่ [4579866 KB](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091))</span><span class="sxs-lookup"><span data-stu-id="abde8-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="abde8-142">ลักษณะการทำงานนี้จะประเมินการดำเนินการทั้งหมดสำหรับคำสั่งที่ตั้งหลาย SKU</span><span class="sxs-lookup"><span data-stu-id="abde8-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="abde8-143">ถ้าคุณต้องการใช้ลักษณะการทำงานนี้ ให้ใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="abde8-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="abde8-144">ฉันไม่สามารถใช้แอปการจัดการคลังสินค้าบนมือถือเพื่อทำการเบิกสินค้าบางส่วน</span><span class="sxs-lookup"><span data-stu-id="abde8-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-145">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-145">Issue description</span></span>

<span data-ttu-id="abde8-146">สำหรับใบสั่งขายและใบสั่งโอนย้าย คุณไม่สามารถข้ามสินค้าและทำการเบิกสินค้าบางส่วน</span><span class="sxs-lookup"><span data-stu-id="abde8-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-147">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-147">Issue resolution</span></span>

<span data-ttu-id="abde8-148">บนหน้า **รายการเมนูของอุปกรณ์เคลื่อนที่** สำหรับรายการเมนูแต่ละรายการที่มีการตั้งค่าให้ประมวลผลใบสั่งขายหรือใบสั่งโอนย้าย ให้ตั้งค่าตัวเลือก **อนุญาตให้มีการแบ่งงาน** บนแท็บด่วน **ทั่วไป** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="abde8-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="abde8-149">ฉันจะเปลี่ยนสถานะสินค้าคงคลังสำหรับการทำงานของปริมาณบางส่วนได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="abde8-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-150">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-150">Issue description</span></span>

<span data-ttu-id="abde8-151">คุณต้องการทำการเปลี่ยนสถานะสินค้าคงคลังสำหรับปริมาณบางส่วนของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="abde8-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-152">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-152">Issue resolution</span></span>

<span data-ttu-id="abde8-153">เมื่อต้องการให้ผู้ปฏิบัติงานสามารถทำการเปลี่ยนแปลงนี้ได้ คุณสามารถสร้างรายการเมนูสำหรับแอปการจัดการคลังสินค้าบนมือถือได้</span><span class="sxs-lookup"><span data-stu-id="abde8-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="abde8-154">ในหน้า **รายการเมนูของอุปกรณ์เคลื่อนที่** สร้าง (หรือแก้ไข) รายการเมนูสำหรับหนึ่งในวิธีต่อไปนี้ :</span><span class="sxs-lookup"><span data-stu-id="abde8-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="abde8-155">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="abde8-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="abde8-156">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="abde8-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="abde8-157">**กระบวนการสร้างงาน:** *ความเคลื่อนไหว*</span><span class="sxs-lookup"><span data-stu-id="abde8-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="abde8-158">**แสดงสถานะสินค้าคงคลัง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="abde8-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="abde8-159">คุณสามารถตั้งฟิลด์อื่น ๆ บนหน้าได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="abde8-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="abde8-160">โปรไฟล์การจัดการท่าสินค้าของโพรไฟล์สถานที่ไม่ได้ป้องกันไม่ให้มีการผสมชนิดสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="abde8-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="abde8-161">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-161">Issue description</span></span>

<span data-ttu-id="abde8-162">คุณกำลังใช้ *นโยบายการรวมบัญชีการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="abde8-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="abde8-163">คุณได้ตั้งค่า *โปรไฟล์การจัดการท่าสินค้า* เป็น *โปรไฟล์สถานที่* แต่เมื่อสร้างงาน ชนิดของสินค้าคงคลังจะถูกผสมในสถานที่สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="abde8-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="abde8-164">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="abde8-164">Issue resolution</span></span>

<span data-ttu-id="abde8-165">โปรไฟล์การจัดการท่าสินค้าต้องมีการแบ่งงานล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="abde8-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="abde8-166">กล่าวอีกอย่างคือ โปรไฟล์การจัดการท่าสินค้าคาดหวังให้หัวข้องานไม่มีสถานที่ส่งสินค้าหลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="abde8-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="abde8-167">เพื่อให้โปรไฟล์การจัดการท่าสินค้าจัดการการผสมสินค้าคงคลังอย่างมีประสิทธิภาพ ต้องตั้งค่าการแบ่งหัวข้องาน</span><span class="sxs-lookup"><span data-stu-id="abde8-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="abde8-168">ในตัวอย่างนี้ โปรไฟล์การจัดการท่าสินค้าของเรามีการตั้งค่าคอนฟิกในลักษณะดังกล่าวว่า **ชนิดของสินค้าคงคลังที่ไม่ควรผสม** จะถูกตั้งค่าเป็น *รหัสการจัดส่ง* และเราจะตั้งค่าการหยุดพักหัวข้องานให้:</span><span class="sxs-lookup"><span data-stu-id="abde8-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="abde8-169">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="abde8-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="abde8-170">เลือก **ชนิดใบสั่งงาน** ที่จะแก้ไข (ตัวอย่างเช่น *ใบสั่งซื้อ*)</span><span class="sxs-lookup"><span data-stu-id="abde8-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="abde8-171">เลือกแม่แบบงานที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="abde8-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="abde8-172">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="abde8-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="abde8-173">เปิดแท็บ **การเรียงลำดับ** และเพิ่มแถวที่มีการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="abde8-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="abde8-174">**ตาราง** - *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="abde8-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="abde8-175">**ตารางที่ได้รับมา** - *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="abde8-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="abde8-176">**ฟิลด์** - *รหัสการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="abde8-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="abde8-177">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="abde8-177">Select **OK**.</span></span>
1. <span data-ttu-id="abde8-178">คุณกลับไปที่หน้า **แม่แบบงาน**</span><span class="sxs-lookup"><span data-stu-id="abde8-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="abde8-179">ในบานหน้าต่างการดำเนินการ ให้เลือก **ตัวแบ่งส่วนหัวของงาน**</span><span class="sxs-lookup"><span data-stu-id="abde8-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="abde8-180">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="abde8-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="abde8-181">เลือกกล่องกาเครื่องหมายที่สัมพันธ์กับ **รหัสการจัดส่ง** ของ *ชื่อฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="abde8-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="abde8-182">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="abde8-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
