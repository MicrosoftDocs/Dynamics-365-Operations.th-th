---
title: แก้ไขการจองสินค้าในการจัดการคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
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
ms.openlocfilehash: a1ea23059d56ebf387a95a1378e2a3cd47556d5f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993895"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="fe1a6-103">แก้ไขการจองสินค้าในการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fe1a6-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe1a6-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fe1a6-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="fe1a6-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่สามารถลบการจองได้เนื่องจากมีงานที่สร้างขึ้นซึ่งอาศัยการจอง"</span><span class="sxs-lookup"><span data-stu-id="fe1a6-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe1a6-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-106">Issue description</span></span>

<span data-ttu-id="fe1a6-107">คุณไม่สามารถยกเลิกการจองสินค้าคงคลังในรายการขายได้ เนื่องจากมีงานที่เปิดอยู่กับรายการ</span><span class="sxs-lookup"><span data-stu-id="fe1a6-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe1a6-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-108">Issue resolution</span></span>

<span data-ttu-id="fe1a6-109">ตรวจสอบว่างานกลุ่มการบรรจุเปิดอยู่เพื่อนำสินค้าจากสถานีบรรจุไปยังที่ตั้งอื่น (เช่น *Baydoor*)</span><span class="sxs-lookup"><span data-stu-id="fe1a6-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="fe1a6-110">ตรวจทานเรกคอร์ดในหน้า **ล็อกประวัติการสร้างงาน** และ **รายละเอียดงาน** เพื่อตรวจสอบว่ามีการจองสินค้าคงคลังทางกายภาพอย่างไร แล้วทำให้เสร็จสมบูรณ์หรือลบงานเพื่อเพิ่มความสะดวกในการจอง</span><span class="sxs-lookup"><span data-stu-id="fe1a6-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="fe1a6-111">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณสินค้าคงคลัง -%1 ไม่สามารถอัพเดตได้เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังไม่เพียงพอสำหรับสินค้า %2...."</span><span class="sxs-lookup"><span data-stu-id="fe1a6-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe1a6-112">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-112">Issue description</span></span>

<span data-ttu-id="fe1a6-113">ปัญหานี้อาจเกิดขึ้นได้ถ้าระบบไม่สามารถอัพเดตปริมาณสินค้าคงคลังได้ เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีมิติที่ระบุอยู่ไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="fe1a6-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="fe1a6-114">นี่เป็นข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fe1a6-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="fe1a6-115">ปริมาณสินค้าคงคลัง -%1 ไม่สามารถอัพเดตได้เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่ไม่เพียงพอสำหรับสินค้า %2 ที่มีขนาดมิติ=%3 สี=%4 เพิ่ม=%5 ไซต์=%6 คลังสินค้า=%7 ที่ตั้ง=%8 สถานะของสินค้าคงคลัง=พร้อมใช้งาน ป้ายทะเบียน=%9 หมายเลขชุดงาน=%10 สำหรับรหัสการอ้างอิง %11 บนรหัสล็อต %12</span><span class="sxs-lookup"><span data-stu-id="fe1a6-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe1a6-116">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-116">Issue resolution</span></span>

<span data-ttu-id="fe1a6-117">ตรวจสอบให้แน่ใจว่าไม่มีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีการจองปริมาณทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="fe1a6-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="fe1a6-118">ตัวอย่างเช่น ธุรกรรมเหล่านี้อาจเปิดใบสั่งตรวจสอบคุณภาพ เรกคอร์ดการบล็อคสินค้าคงคลัง หรือใบสั่งเอาพุต</span><span class="sxs-lookup"><span data-stu-id="fe1a6-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="fe1a6-119">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณคงคลังคงเหลือที่มีอยู่จริง... ไม่สามารถจองได้เนื่องจากมีเพียง 0.00 เท่านั้นที่พร้อมใช้งานในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fe1a6-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe1a6-120">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-120">Issue description</span></span>

<span data-ttu-id="fe1a6-121">ปัญหานี้อาจเกิดขึ้นได้ถ้าระบบไม่สามารถอัพเดตปริมาณสินค้าคงคลังได้ เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีมิติที่ระบุอยู่ไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="fe1a6-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="fe1a6-122">นี่เป็นข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fe1a6-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="fe1a6-123">ไซต์คงคลังคงเหลือที่มีอยู่จริง=%1คลังสินค้า=%2 สถานะของสินค้าคงคลัง = พร้อมใช้งานหมายเลขชุดงาน=%3 เจ้าของ=%4: %5 ไม่สามารถจองได้เนื่องจากมีเฉพาะ๐.๐๐เท่านั้นที่พร้อมใช้งานในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fe1a6-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe1a6-124">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-124">Issue resolution</span></span>

<span data-ttu-id="fe1a6-125">ปัญหานี้อาจเกิดจากการเปิดงาน</span><span class="sxs-lookup"><span data-stu-id="fe1a6-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="fe1a6-126">ทำงานให้เสร็จสมบูรณ์หรือได้รับโดยไม่มีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="fe1a6-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="fe1a6-127">ตรวจสอบให้แน่ใจว่าไม่มีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีการจองปริมาณทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="fe1a6-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="fe1a6-128">ตัวอย่างเช่น ธุรกรรมเหล่านี้อาจเปิดใบสั่งตรวจสอบคุณภาพ เรกคอร์ดการบล็อคสินค้าคงคลัง หรือใบสั่งเอาพุต</span><span class="sxs-lookup"><span data-stu-id="fe1a6-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="fe1a6-129">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "หากต้องการให้กำหนดให้กับเวฟ บรรทัดการโหลดต้องระบุมิติเหนือสถานที่</span><span class="sxs-lookup"><span data-stu-id="fe1a6-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="fe1a6-130">ถ้าต้องการกำหนดมิติเหล่านี้ ให้จองและสร้างรายการจำนวนงานในศูนย์การผลิตใหม่"</span><span class="sxs-lookup"><span data-stu-id="fe1a6-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe1a6-131">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-131">Issue description</span></span>

<span data-ttu-id="fe1a6-132">เมื่อคุณใช้สินค้าที่มีลำดับชั้นการจอง "ชุดงานข้างบน" (โดยมีมิติ **หมายเลขชุดงาน** ที่อยู่ *ด้านบน* มิติ **สถานที่เก็บ**) คำสั่ง **นำออกใช้ไปยังคลังสินค้า** บนหน้า **เวิร์กเบนช์การวางแผนการบรรทุก** สำหรับปริมาณบางส่วนไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="fe1a6-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="fe1a6-133">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้และไม่มีการสร้างงานสำหรับปริมาณบางส่วน</span><span class="sxs-lookup"><span data-stu-id="fe1a6-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="fe1a6-134">อย่างไรก็ตาม ถ้าคุณใช้สินค้าที่มีลำดับชั้นการจอง "ชุดงานด้านล่าง" (โดยมีมิติ **หมายเลขชุดงาน** ที่อยู่ *ด้านล่าง* มิติ **สถานที่เก็บ**) คุณจึงสามารถนำโหลดออกใช้ได้จากหน้า **เวิร์กเบนช์การวางแผน** สำหรับปริมาณบางส่วนไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="fe1a6-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe1a6-135">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="fe1a6-135">Issue resolution</span></span>

<span data-ttu-id="fe1a6-136">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fe1a6-136">This behavior is by design.</span></span> <span data-ttu-id="fe1a6-137">ถ้าคุณกำหนดมิติที่อยู่ด้านบนของมิติ **สถานที่** ในลำดับชั้นการจอง ต้องระบุก่อนการนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fe1a6-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="fe1a6-138">Microsoft ได้ประเมินปัญหานี้แล้ว และระบุว่าเป็นข้อจำกัดของลักษณะการทำงานในระหว่างการนำออกใช้ไปยังคลังสินค้าจากเวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="fe1a6-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="fe1a6-139">ไม่สามารถปล่อยปริมาณบางส่วนได้ ถ้าไม่ได้ระบุอย่างน้อยหนึ่งมิติข้างบน **สถานที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="fe1a6-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="fe1a6-140">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [นโยบายการจองในมิติระดับคลังสินค้าที่ยืดหยุ่น](flexible-warehouse-level-dimension-reservation.md)</span><span class="sxs-lookup"><span data-stu-id="fe1a6-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
