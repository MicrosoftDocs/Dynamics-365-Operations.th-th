---
title: การระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน
description: ระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2b1468328433a67253bafc21ac9c9b3a2398872
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438152"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="2fb11-103">การระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="2fb11-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2fb11-104">เมื่อคุณจัดการใบสั่งส่งคืนสินค้า คุณต้องระบุรหัสเหตุผลการส่งคืนเพื่อระบุสาเหตุที่ส่งคืนผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="2fb11-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="2fb11-105">และคุณยังต้องระบุรหัสการโอนการครอบครองและการดำเนินการจัดการต่อรายการสินค้าเพื่อกำหนดสิ่งที่ควรจะดำเนินการกับตัวสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="2fb11-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="2fb11-106">รหัสการโอนการครอบครองสามารถใช้ได้เมื่อคุณสร้างใบสั่งส่งคืนสินค้า ลงทะเบียนการมาถึงของสินค้า หรืออัพเดตบันทึกการจัดส่งตามการมาถึงของสินค้า และเมื่อสิ้นสุดใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="2fb11-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="2fb11-107">คุณสามารถกำหนดรหัสการโอนการครอบครองใดๆ ที่คุณต้องใช้เพื่อสนับสนุนกระบวนการทางธุรกิจได้ </span><span class="sxs-lookup"><span data-stu-id="2fb11-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="2fb11-108">ตารางต่อไปนี้แสดงชุดของรหัสที่ใช้กันโดยทั่วไปเพื่อกำหนดการโอนการครอบครองสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="2fb11-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fb11-109">ชนิดการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="2fb11-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="2fb11-110">รหัสทั่วไป</span><span class="sxs-lookup"><span data-stu-id="2fb11-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="2fb11-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2fb11-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-112">การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2fb11-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="2fb11-113">SC</span><span class="sxs-lookup"><span data-stu-id="2fb11-113">SC</span></span></p></td>
<td><p><span data-ttu-id="2fb11-114">การกำจัดเป็นเศษซาก/ทำลาย</span><span class="sxs-lookup"><span data-stu-id="2fb11-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-115">การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2fb11-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="2fb11-116">DC</span><span class="sxs-lookup"><span data-stu-id="2fb11-116">DC</span></span></p></td>
<td><p><span data-ttu-id="2fb11-117">การบริจาค</span><span class="sxs-lookup"><span data-stu-id="2fb11-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-118">การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2fb11-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="2fb11-119">TD</span><span class="sxs-lookup"><span data-stu-id="2fb11-119">TD</span></span></p></td>
<td><p><span data-ttu-id="2fb11-120">การตัดจำหน่ายให้แก่บุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="2fb11-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-121">การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2fb11-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="2fb11-122">SL</span><span class="sxs-lookup"><span data-stu-id="2fb11-122">SL</span></span></p></td>
<td><p><span data-ttu-id="2fb11-123">เศษซาก</span><span class="sxs-lookup"><span data-stu-id="2fb11-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-124">การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2fb11-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="2fb11-125">TS</span><span class="sxs-lookup"><span data-stu-id="2fb11-125">TS</span></span></p></td>
<td><p><span data-ttu-id="2fb11-126">การขายให้แก่บุคคลที่สาม (ตลาดสินค้ามือสอง)</span><span class="sxs-lookup"><span data-stu-id="2fb11-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-127">การซ่อมแซม/ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2fb11-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="2fb11-128">RW</span><span class="sxs-lookup"><span data-stu-id="2fb11-128">RW</span></span></p></td>
<td><p><span data-ttu-id="2fb11-129">การทำใหม่</span><span class="sxs-lookup"><span data-stu-id="2fb11-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-130">การซ่อมแซม/ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2fb11-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="2fb11-131">RF</span><span class="sxs-lookup"><span data-stu-id="2fb11-131">RF</span></span></p></td>
<td><p><span data-ttu-id="2fb11-132">การผลิตใหม่/ตกแต่งใหม่</span><span class="sxs-lookup"><span data-stu-id="2fb11-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-133">การซ่อมแซม/ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2fb11-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="2fb11-134">MD</span><span class="sxs-lookup"><span data-stu-id="2fb11-134">MD</span></span></p></td>
<td><p><span data-ttu-id="2fb11-135">การปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2fb11-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-136">การซ่อมแซม/ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2fb11-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="2fb11-137">RP</span><span class="sxs-lookup"><span data-stu-id="2fb11-137">RP</span></span></p></td>
<td><p><span data-ttu-id="2fb11-138">การซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="2fb11-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-139">การซ่อมแซม/ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2fb11-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="2fb11-140">RV</span><span class="sxs-lookup"><span data-stu-id="2fb11-140">RV</span></span></p></td>
<td><p><span data-ttu-id="2fb11-141">การส่งคืนให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2fb11-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-142">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2fb11-142">Other</span></span></p></td>
<td><p><span data-ttu-id="2fb11-143">AI</span><span class="sxs-lookup"><span data-stu-id="2fb11-143">AI</span></span></p></td>
<td><p><span data-ttu-id="2fb11-144">การใช้ตามสภาพ</span><span class="sxs-lookup"><span data-stu-id="2fb11-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-145">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2fb11-145">Other</span></span></p></td>
<td><p><span data-ttu-id="2fb11-146">RS</span><span class="sxs-lookup"><span data-stu-id="2fb11-146">RS</span></span></p></td>
<td><p><span data-ttu-id="2fb11-147">การขายใหม่</span><span class="sxs-lookup"><span data-stu-id="2fb11-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-148">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2fb11-148">Other</span></span></p></td>
<td><p><span data-ttu-id="2fb11-149">EX</span><span class="sxs-lookup"><span data-stu-id="2fb11-149">EX</span></span></p></td>
<td><p><span data-ttu-id="2fb11-150">แลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="2fb11-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-151">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2fb11-151">Other</span></span></p></td>
<td><p><span data-ttu-id="2fb11-152">MS</span><span class="sxs-lookup"><span data-stu-id="2fb11-152">MS</span></span></p></td>
<td><p><span data-ttu-id="2fb11-153">เบ็ดเตล็ด</span><span class="sxs-lookup"><span data-stu-id="2fb11-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2fb11-154">สำหรับแต่ละรหัสการโอนการครอบครองที่คุณกำหนด คุณต้องเลือกการดำเนินการโอนการครอบครอง </span><span class="sxs-lookup"><span data-stu-id="2fb11-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="2fb11-155">การดำเนินการโอนการครอบครองจะกำหนดผลกระทบทางกายภาพและทางการเงินของรหัสการโอนการครอบครอง </span><span class="sxs-lookup"><span data-stu-id="2fb11-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="2fb11-156">ตัวอย่างเช่น การดำเนินการโอนการครอบครองจะกำหนดว่าการจัดการที่เกิดขึ้นจริงของสินค้าที่ส่งคืน ผลกระทบทางการเงินของสินค้าที่ส่งคืน และถ้าสินค้าทดแทนต้องถูกส่งไปยังลูกค้า </span><span class="sxs-lookup"><span data-stu-id="2fb11-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="2fb11-157">คุณสามารถกำหนดจำนวนที่ไม่จำกัดของรหัสการโอนการครอบครองตามความต้องการทางธุรกิจของคุณได้ แต่คุณสามารถเลือกการดำเนินการโอนการครอบครองที่กำหนดไว้ล่วงหน้าได้เพียงหกแบบเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="2fb11-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="2fb11-158">ตารางต่อไปนี้แสดงการดำเนินการโอนการครอบครองและคำนิยาม</span><span class="sxs-lookup"><span data-stu-id="2fb11-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fb11-159">การดำเนินการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="2fb11-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="2fb11-160">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2fb11-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-161"><strong>เครดิต</strong></span><span class="sxs-lookup"><span data-stu-id="2fb11-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="2fb11-162">ส่งคืนสินค้าไปยังสินค้าคงคลังและให้เครดิตลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2fb11-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-163"><strong>เครดิตอย่างเดียว</strong></span><span class="sxs-lookup"><span data-stu-id="2fb11-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="2fb11-164">ให้เครดิตลูกค้าได้โดยไม่จำเป็นต้องใช้หรือต้องการรับสินค้าคืน</span><span class="sxs-lookup"><span data-stu-id="2fb11-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-165"><strong>เศษซาก</strong></span><span class="sxs-lookup"><span data-stu-id="2fb11-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="2fb11-166">คิดสินค้าเป็นของเสีย และให้เครดิตลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2fb11-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-167"><strong>แทนที่และเครดิต</strong></span><span class="sxs-lookup"><span data-stu-id="2fb11-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="2fb11-168">ส่งคืนสินค้าไปยังสินค้าคงคลัง สร้างใบสั่งเปลี่ยนทดแทน และให้เครดิตลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2fb11-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-169"><strong>แทนที่และหักของเสีย</strong></span><span class="sxs-lookup"><span data-stu-id="2fb11-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="2fb11-170">คิดสินค้าเป็นของเสีย สร้างใบสั่งเปลี่ยนทดแทน และให้เครดิตลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2fb11-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fb11-171"><strong>ส่งคืนให้ลูกค้า</strong></span><span class="sxs-lookup"><span data-stu-id="2fb11-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="2fb11-172">ปฏิเสธสินค้าที่ส่งคืน และส่งคืนสินค้าให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2fb11-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="2fb11-173">การเลือกรหัสการโอนการครอบครองสำหรับใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="2fb11-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="2fb11-174">คลิก **การบริหารสินค้าคงคลังt** \> **งานประจำงวด** \> **การจัดการคุณภาพ** \> **ใบสั่งตรวจสอบสินค้า**</span><span class="sxs-lookup"><span data-stu-id="2fb11-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="2fb11-175">สำหรับใบสั่งตรวจสอบสินค้าที่มีอยู่ ให้เลือกการดำเนินการจากฟิลด์ **รหัสการโอนการครอบครอง** บนแท็บ **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="2fb11-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="2fb11-176">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="2fb11-176">See also</span></span>

<span data-ttu-id="2fb11-177">[ใบสั่งตรวจสอบสินค้า (แบบฟอร์ม)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="2fb11-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="2fb11-178">[รหัสการจัดการ (แบบฟอร์ม)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="2fb11-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  


