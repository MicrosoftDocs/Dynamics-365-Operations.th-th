---
title: แก้ไขปัญหาการสร้างและการจัดส่งสินค้าบรรทุก
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการสร้างการบรรทุกและการจัดส่งใน Microsoft Dynamics 365 Supply Chain Management
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994065"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="97daa-103">แก้ไขปัญหาการสร้างและการจัดส่งสินค้าบรรทุก</span><span class="sxs-lookup"><span data-stu-id="97daa-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97daa-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการสร้างการบรรทุกและการจัดส่งใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="97daa-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="97daa-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "คุณไม่สามารถสร้างรายการจำนวนงานในศูนย์การผลิตสำหรับบรรทัดใบสั่งนี้ได้เนื่องจากมีมิติสินค้าคงคลังที่ไม่ถูกต้อง..."</span><span class="sxs-lookup"><span data-stu-id="97daa-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="97daa-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-106">Issue description</span></span>

<span data-ttu-id="97daa-107">คุณได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้เมื่อคุณพยายามนำใบสั่งขายส่งคืนไปยังคลังสินค้า:</span><span class="sxs-lookup"><span data-stu-id="97daa-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="97daa-108">คุณไม่สามารถสร้างรายการจำนวนงานในศูนย์การผลิตสำหรับบรรทัดใบสั่งนี้ได้เนื่องจากมีมิติสินค้าคงคลังที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="97daa-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="97daa-109">คุณไม่สามารถอ้างอิงมิติสินค้าคงคลังที่อยู่ใต้มิติที่ตั้งในลำดับชั้นการจอง</span><span class="sxs-lookup"><span data-stu-id="97daa-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="97daa-110">ลบมิติที่ไม่ถูกต้องออกจากบรรทัดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="97daa-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="97daa-111">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-111">Issue resolution</span></span>

<span data-ttu-id="97daa-112">แต่ผลิตภัณฑ์ไม่สนับสนุนการประมวลผลการโหลดสำหรับกระบวนการส่งคืนสินค้าขาย</span><span class="sxs-lookup"><span data-stu-id="97daa-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="97daa-113">ดังนั้น คุณจึงไม่สามารถนำใบสั่งขายส่งคืนไปยังคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="97daa-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="97daa-114">ในธุรกรรมใบสั่งขาย คุณไม่สามารถอ้างอิงมิติสินค้าคงคลังที่อยู่ใต้มิติ **ที่ตั้ง** ในลำดับชั้นการจอง</span><span class="sxs-lookup"><span data-stu-id="97daa-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="97daa-115">การแก้ปัญหาคือลบมิติที่ไม่ถูกต้องออกจากบรรทัดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="97daa-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="97daa-116">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "บรรทัดใดบรรทัดหนึ่งมีอยู่บนโหลดแล้ว</span><span class="sxs-lookup"><span data-stu-id="97daa-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="97daa-117">ไม่สามารถนำออกใช้ที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="97daa-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="97daa-118">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-118">Issue description</span></span>

<span data-ttu-id="97daa-119">ถ้าคุณสร้างจำนวนงานในศูนย์การผลิตด้วยตนเอง หรือหากคุณตั้งค่ากระบวนการเพื่อให้การโหลดมีการสร้างขึ้นแล้วก่อนที่จะมีการป้อนรายการใบสั่งขายจะเกิดขึ้น สมมติฐานดังกล่าวคือการนำออกใช้ในเวลาต่อมาจะทำด้วยตนเอง และจะมีการใช้กระบวนการผลิตและการจัดอันดับจากจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="97daa-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="97daa-120">ในสถานการณ์อื่น ๆ ที่เป็นไปได้ คุณกำลังพยายามดำเนินการนำออกใช้โดยอัตโนมัติไปยังคลังสินค้า แต่กระบวนการเวฟจึงไม่สามารถสร้างงานได้</span><span class="sxs-lookup"><span data-stu-id="97daa-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="97daa-121">ดังนั้น จึงยังคงมีการสร้างการจัดส่งหรือจำนวนงานในศูนย์การผลิตที่เปิดค้างไว้</span><span class="sxs-lookup"><span data-stu-id="97daa-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="97daa-122">การจัดส่งหรือโหลดที่เปิดนี้ปิดกั้นความพยายามในเวลาต่อมาเพื่อนำใบสั่งออกใช้โดยอัตโนมัติจนกว่าคุณจะลบการจัดส่ง หรือจำนวนงานในศูนย์การผลิตที่เปิดค้างไว้หรือประมวลเวฟด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="97daa-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="97daa-123">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-123">Issue resolution</span></span>

<span data-ttu-id="97daa-124">คุณสามารถนำออกใช้จากหน้าใบสั่งขาย หรือการนำออกใช้โดยอัตโนมัติสามารถทำได้จากหน้าใบสั่งขายที่นำออกใช้ เฉพาะเมื่อไม่มีการโหลดอยู่ก่อนการนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="97daa-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="97daa-125">จำนวนงานในศูนย์การผลิตจะถูกสร้างขึ้นโดยอัตโนมัติหลังจากที่มีการประมวลผลเวฟ</span><span class="sxs-lookup"><span data-stu-id="97daa-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="97daa-126">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่สามารถประมวลผลการแก้ไขบันทึกการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="97daa-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="97daa-127">บันทึกการจัดส่งมีเฉพาะสินค้าที่อยู่ภายใต้กระบวนการจัดการคลังสินค้า เนื่องจากไม่ได้รับการสนับสนุนโดยการแก้ไขบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="97daa-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="97daa-128">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-128">Issue description</span></span>

<span data-ttu-id="97daa-129">หลังจากที่คุณลงรายการบัญชีบันทึกการจัดส่ง คุณไม่สามารถยกเลิกได้ เนื่องจากไม่มีปุ่ม **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="97daa-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="97daa-130">นอกจากนี้คุณยังไม่สามารถแก้ไขบันทึกการจัดส่งได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="97daa-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="97daa-131">ถ้าคุณพยายาม คุณจะได้รับข้อความแสดงข้อผิดพลาดนี้</span><span class="sxs-lookup"><span data-stu-id="97daa-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="97daa-132">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-132">Issue resolution</span></span>

<span data-ttu-id="97daa-133">เมื่อต้องการแก้ไขบันทึกการจัดส่งที่ลงรายการบัญชีสำหรับสินค้าที่เปิดใช้งานสำหรับการจัดการคลังสินค้าขั้นสูง (WMS) คุณต้องทำการลงรายการบัญชีจากจำนวนงานในศูนย์การผลิตโดยตรง ไม่ใช่จากใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="97daa-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="97daa-134">ฉันสามารถสร้างงานจากโหลดขาออกแทนเวฟได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="97daa-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="97daa-135">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-135">Issue description</span></span>

<span data-ttu-id="97daa-136">ต่อไปนี้เป็นวิธีหนึ่งในการทบทวนการเกิดปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="97daa-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="97daa-137">สร้างการบรรทุกขาออกโดยใช้ใบสั่งขายหรือใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="97daa-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="97daa-138">นำโหลดออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="97daa-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="97daa-139">โปรดสังเกตว่ายังไม่มีการสร้างงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="97daa-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="97daa-140">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-140">Issue resolution</span></span>

<span data-ttu-id="97daa-141">ถ้าต้องสร้างงานทันทีเมื่อมีการนำโหลดออกใช้ คุณต้องตั้งค่าคอนฟิกแม่แบบเวฟตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="97daa-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="97daa-142">บนแม่แบบเวฟ ให้ตั้งค่าตัวเลือกต่อไปนี้เป็น *ใช่*:</span><span class="sxs-lookup"><span data-stu-id="97daa-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="97daa-143">การสร้างเวฟอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="97daa-143">Automate wave creation</span></span>
- <span data-ttu-id="97daa-144">ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="97daa-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="97daa-145">นำเวฟออกใช้อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="97daa-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="97daa-146">ฉันไม่สามารถนำโหลดบางครั้งไปใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="97daa-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="97daa-147">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-147">Issue description</span></span>

<span data-ttu-id="97daa-148">คุณไม่สามารถนำโหลดบางอย่างไปใช้กับคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="97daa-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="97daa-149">เมื่อคุณทำการนำออกใช้ไปยังคลังสินค้าจะมีข้อความ "ดำเนินการเสร็จสมบูรณ์" แต่ไม่มีอะไรเกิดขึ้นและไม่มีการสร้างงานสำหรับปริมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="97daa-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="97daa-150">ปัญหานี้เกิดขึ้นเมื่อคุณใช้ฟังก์ชันโหลดการขนส่งและไม่มีการจองสินค้าที่ไม่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="97daa-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="97daa-151">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="97daa-151">Issue resolution</span></span>

<span data-ttu-id="97daa-152">[ปัญหา KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("โหลดที่จัดส่งบางส่วนอาจเวฟและประมวลผลใหม่") เป็นแบบคงที่ใน [รุ่น 10.0.15](../get-started/whats-new-scm-10-0-15.md)</span><span class="sxs-lookup"><span data-stu-id="97daa-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
