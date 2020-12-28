---
title: แก้ไขปัญหาการเบิกสินค้าและการบรรจุสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณบรรจุสินค้าใน Microsoft Dynamics 365 Supply Chain Management
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
ms.openlocfilehash: 74854fa95837dd8a133860e2a017be4c92ff84a3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645488"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="03d3d-103">แก้ไขปัญหาการเบิกสินค้าและการบรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="03d3d-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03d3d-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณบรรจุสินค้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="03d3d-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="03d3d-105">ฉันได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้: "ที่ตั้งมิติต้องไม่ว่างเปล่าถ้ามีการตั้งค่าหมายเลขลำดับประจำสินค้า"</span><span class="sxs-lookup"><span data-stu-id="03d3d-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-106">Issue description</span></span>

<span data-ttu-id="03d3d-107">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้ถ้าคุณสร้างใบสั่งโอนย้ายสำหรับชุดสินค้าโดยใช้คลังสินค้าที่เปิดใช้งานสำหรับการจัดการคลังสินค้าขั้นสูง (WMS), แล้ว หลังจากงานเสร็จสมบูรณ์แล้ว คุณพยายามยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="03d3d-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-108">Issue resolution</span></span>

<span data-ttu-id="03d3d-109">ฟิลด์ **สถานที่รับสินค้าเริ่มต้น** จะว่างเปล่าสำหรับคลังสินค้าส่งต่อของคลังสินค้า "เริ่มต้น"</span><span class="sxs-lookup"><span data-stu-id="03d3d-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="03d3d-110">เมื่อต้องการแก้ไขปัญหานี้ ให้ระบุสถานที่รับสินค้าเริ่มต้นในคลังสินค้าส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="03d3d-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="03d3d-111">ตรวจสอบให้แน่ใจว่าที่ตั้งนี้เป็นป้ายทะเบียนที่ควบคุม</span><span class="sxs-lookup"><span data-stu-id="03d3d-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="03d3d-112">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ป้ายทะเบียนไม่ถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="03d3d-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-113">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-113">Issue description</span></span>

<span data-ttu-id="03d3d-114">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้ในแอปคลังสินค้าเมื่อคุณสแกนรหัสป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="03d3d-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-115">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-115">Issue resolution</span></span>

<span data-ttu-id="03d3d-116">ตรวจสอบให้แน่ใจว่ารหัสป้ายทะเบียนมีอยู่ในตารางป้ายทะเบียน และสินค้าและปริมาณบนป้ายทะเบียนพร้อมใช้งาน (กล่าวคือไม่ถูกบล็อค)</span><span class="sxs-lookup"><span data-stu-id="03d3d-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="03d3d-117">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ฟิลด์ ' น้ำหนักโหลด ' (=-%1) สามารถมีตัวเลขค่าบวกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="03d3d-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="03d3d-118">การอัพเดตถูกยกเลิก"</span><span class="sxs-lookup"><span data-stu-id="03d3d-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-119">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-119">Issue description</span></span>

<span data-ttu-id="03d3d-120">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้ถ้ามีการเปิดงานเมื่อคุณดำเนินงานจากสถานที่จัดส่งไปยังสถานที่การแบ่งระยะ หรือจากสถานที่การแบ่งระยะไปยังสถานที่เก็บสินค้า</span><span class="sxs-lookup"><span data-stu-id="03d3d-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-121">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-121">Issue resolution</span></span>

<span data-ttu-id="03d3d-122">เมื่อต้องการแก้ไขปัญหานี้ ให้ไปที่ **การจัดการระบบ \> งานประจำงวด \> ฐานข้อมูล \> การตรวจสอบความสอดคล้องกันของข้อมูล** และรันกระบวนการสำหรับ **การตรวจสอบความสอดคล้องของน้ำหนักบรรทุกของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="03d3d-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="03d3d-123">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณไม่ถูกต้องสำหรับหน่วย %1"</span><span class="sxs-lookup"><span data-stu-id="03d3d-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-124">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-124">Issue description</span></span>

<span data-ttu-id="03d3d-125">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้เมื่อคุณพยายามดำเนินการ *แบ่งการเบิกสินค้า* ในหลายชุดงาน</span><span class="sxs-lookup"><span data-stu-id="03d3d-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-126">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-126">Issue resolution</span></span>

<span data-ttu-id="03d3d-127">ผู้ปฏิบัติงานคลังสินค้าต้องใช้กระบวนการ *เบิกสินค้าแบบสั้น* ในแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="03d3d-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="03d3d-128">ถ้าคุณกำลังพยายามเลือกหลายชุดจากสถานที่เดียวกัน คุณยังสามารถใช้ตัวเลือก **แบบเต็ม** ในแอปคลังสินค้าได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="03d3d-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="03d3d-129">ฉันไม่สามารถย้ายสินค้าคงคลังไปยังสถานที่ที่เป็นป้ายทะเบียนที่มีการควบคุม</span><span class="sxs-lookup"><span data-stu-id="03d3d-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-130">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-130">Issue description</span></span>

<span data-ttu-id="03d3d-131">คุณไม่สามารถลดปริมาณที่เบิกสินค้าไว้ในจำนวนงานในศูนย์การผลิตได้</span><span class="sxs-lookup"><span data-stu-id="03d3d-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-132">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-132">Issue resolution</span></span>

<span data-ttu-id="03d3d-133">ในรุ่นก่อน คุณไม่สามารถลดปริมาณที่เบิกสินค้าไว้ในจำนวนงานในศูนย์การผลิตได้</span><span class="sxs-lookup"><span data-stu-id="03d3d-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="03d3d-134">อย่างไรก็ตาม คุณสามารถเดี๋ยวนี้เบิกไปยังสถานที่ที่ควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="03d3d-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="03d3d-135">คุณต้องระบุทั้งค่า **สถานที่** และค่า **ป้ายทะเบียน** สำหรับรายการจำนวนงานในศูนย์การผลิตบนหน้า **ลดปริมาณที่เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="03d3d-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="03d3d-136">ฉันสามารถพิมพ์บันทึกการจัดส่งหรือจัดส่งเนื้อหาตามคลังสินค้าได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="03d3d-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-137">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-137">Issue description</span></span>

<span data-ttu-id="03d3d-138">คุณต้องการพิมพ์บันทึกการจัดส่งหรือจัดส่งเนื้อหาของคลังสินค้าหรือไซต์บนหน้า **อัพเดตบรรทัดแม่แบบการตรวจสอบงาน**</span><span class="sxs-lookup"><span data-stu-id="03d3d-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-139">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-139">Issue resolution</span></span>

<span data-ttu-id="03d3d-140">เมื่อคุณพิมพ์เอกสารโดยใช้การตั้งค่าการจัดการงานพิมพ์ ให้จำกัดขอบเขต (ไซต์/คลังสินค้า) โดยใช้การจัดการการพิมพ์แทนโดยการเลือก **แก้ไขการตั้งค่าการพิมพ์** บนหน้า **การอัพเดตบรรทัดแม่แบบการตรวจสอบงาน**</span><span class="sxs-lookup"><span data-stu-id="03d3d-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="03d3d-141">ฉันไม่สามารถยกเลิกบันทึกการจัดส่งได้หลังจากที่ลงรายการบัญชีจากใบสั่งขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="03d3d-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-142">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-142">Issue description</span></span>

<span data-ttu-id="03d3d-143">เมื่อกระบวนการเบิกสินค้าและการจัดส่งเปิดใช้งานสำหรับ WMS คุณจะไม่สามารถยกเลิกบันทึกการจัดส่งได้หลังจากที่ลงรายการบัญชีจากใบสั่งขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="03d3d-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-144">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-144">Issue resolution</span></span>

<span data-ttu-id="03d3d-145">เมื่อต้องการแก้ไขบันทึกการจัดส่งที่ลงรายการบัญชีสำหรับสินค้าที่เปิดใช้งานสำหรับ WMS การลงรายการบัญชีต้องเกิดจากจำนวนงานในศูนย์การผลิตโดยตรง ไม่ใช่จากใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="03d3d-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="03d3d-146">Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="03d3d-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="03d3d-147">โดยทั่วไป ใบสั่งขายที่มีการเบิกสินค้าและจัดส่งโดยใช้กระบวนการจัดการคลังสินค้าสามารถจัดส่งบันทึกการจัดส่งที่อัพเดตจากจำนวนงานในศูนย์การผลิต หรือการจัดส่งสินค้าและเอกสารใบสั่งขายเอง</span><span class="sxs-lookup"><span data-stu-id="03d3d-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="03d3d-148">อย่างไรก็ตาม ถ้าคุณจัดส่งในบันทึกที่อัพเดตใบสั่งขายจากเอกสารใบสั่งขายการกลับรายการ บันทึกการจัดส่งยังคงไม่สามารถทำได้จากจำนวนงานในศูนย์การผลิตหรือใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="03d3d-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="03d3d-149">ดังนั้น เราขอแนะนำให้คุณใช้การลงรายการบัญชีบันทึกการจัดส่งจากจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="03d3d-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="03d3d-150">ในกรณีนี้ จะมีการเปิดใช้งานการกลับรายการที่ต้องทำจากจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="03d3d-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="03d3d-151">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "สามารถพบงานที่ไม่เพียงพอสำหรับคลัสเตอร์"</span><span class="sxs-lookup"><span data-stu-id="03d3d-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03d3d-152">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-152">Issue description</span></span>

<span data-ttu-id="03d3d-153">เมื่อคุณใช้กระบวนการ *เบิกสินค้าของคลัสเตอร์โดยตรงของระบบ* ถ้าคุณตั้งค่าคอนฟิกโพรไฟล์ของคลัสเตอร์ ตัวอย่างเช่น 10 ตำแหน่ง สามารถเบิกสินค้า กระบวนการทำงานตามที่วางแผนไว้เมื่อมีการทำงานเพียงพอสำหรับการเบิกสินค้าไปยัง 10 ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="03d3d-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="03d3d-154">อย่างไรก็ตาม ถ้ามีเพียงแปดตำแหน่งที่จะเบิกสินค้า คุณได้รับข้อความแสดงข้อผิดพลาดนี้ เนื่องจากไม่มีการทำงานเพียงพอสำหรับหนึ่งคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="03d3d-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03d3d-155">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="03d3d-155">Issue resolution</span></span>

<span data-ttu-id="03d3d-156">เมื่อต้องการแก้ไขปัญหานี้ แก้ไขโพรไฟล์ของคลัสเตอร์ และตั้งค่าตัวเลือก **การเรียกใช้ตำแหน่ง** เป็น *ไม่*</span><span class="sxs-lookup"><span data-stu-id="03d3d-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
