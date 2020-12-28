---
title: ค่าออบเจ็กต์สินค้าคงคลัง
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีคำนวณมูลค่าออบเจ็กต์สินค้าคงคลัง
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daa36dad4009cc25b89363dcff6b4496205522e3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438369"
---
# <a name="inventory-object-values"></a><span data-ttu-id="0aee1-103">ค่าออบเจ็กต์สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aee1-104">บทความนี้แสดงข้อมูลเกี่ยวกับวิธีคำนวณมูลค่าออบเจ็กต์สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="0aee1-105">ฟังก์ชันแบบใหม่ที่ชื่อ **ปริมาณทางกายภาพ** ช่วยให้คุณเห็นมูลค่าของสินค้าคงคลังเฉพาะออบเจ็กต์</span><span class="sxs-lookup"><span data-stu-id="0aee1-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="0aee1-106">ออบเจ็กต์ต้นทุนแสดงถึงระดับของเอนทิตี้ที่ทำการลงบัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="0aee1-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับต้นทุนวัตถุ ดูที่ [ต้นทุนวัตถุ](cost-object.md)</span><span class="sxs-lookup"><span data-stu-id="0aee1-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="0aee1-108">เมื่เมื่อต้องการดูค่าของสินค้าคงคลังเฉพาะออบเจ็กต์ คลิก **ปริมาณทางกายภาพ** ในหน้า **ออบเจ็กต์ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="0aee1-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="0aee1-109">นี่เป็นวิธีคำนวณมูลค่าของสินค้าคงคลังวัตถุ:</span><span class="sxs-lookup"><span data-stu-id="0aee1-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="0aee1-110">วัตถุสินค้าคงคลัง มูลค่า = ออบเจ็กต์ต้นทุน.ต้นทุนเฉลี่ยต่อหน่วยxออบเจ็กต์สินค้าคงคลัง.ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="0aee1-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="0aee1-111">ตัวอย่างต่อไปนี้แสดงวิธีคำนวณค่าของออบเจ็กต์สินค้าคงคลังและต้นทุนวัตถุ</span><span class="sxs-lookup"><span data-stu-id="0aee1-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="0aee1-112">เหตุการณ์ใบรับสินค้าสองใบถูกลงทะเบียนในสินค้า A:</span><span class="sxs-lookup"><span data-stu-id="0aee1-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="0aee1-113">ใบรับสินค้า 1: ปริมาณ = 100 ชิ้น จำนวนเงิน = $1,000.00 ไซต์ = 1 คลังสินค้า = 11 หมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0aee1-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="0aee1-114">= B1</span><span class="sxs-lookup"><span data-stu-id="0aee1-114">= B1</span></span>
-   <span data-ttu-id="0aee1-115">ใบรับสินค้า 2: ปริมาณ = 50 ชิ้น จำนวนเงิน = $8,00.00 ไซต์ = 1 คลังสินค้า = 11 หมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0aee1-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="0aee1-116">= B2</span><span class="sxs-lookup"><span data-stu-id="0aee1-116">= B2</span></span>

<span data-ttu-id="0aee1-117">ตารางต่อไปนี้แสดงผลลัพธ์การคำนวณสำหรับออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0aee1-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="0aee1-118">คุณสามารถดูผลลัพธ์ในหน้า **ออบเจ็กต์ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="0aee1-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aee1-119">ชนิดออบเจ็กต์</span><span class="sxs-lookup"><span data-stu-id="0aee1-119">Object type</span></span></th>
<th><span data-ttu-id="0aee1-120">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="0aee1-120">Item number</span></span></th>
<th><span data-ttu-id="0aee1-121">ไซต์</span><span class="sxs-lookup"><span data-stu-id="0aee1-121">Site</span></span></th>
<th><span data-ttu-id="0aee1-122">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="0aee1-122">Quantity</span></span></th>
<th><span data-ttu-id="0aee1-123">หน่วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-123">Inventory unit</span></span></th>
<th><span data-ttu-id="0aee1-124">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="0aee1-124">Value</span></span></th>
<th><span data-ttu-id="0aee1-125">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="0aee1-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aee1-126">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0aee1-126">Cost object</span></span></td>
<td><span data-ttu-id="0aee1-127">A</span><span class="sxs-lookup"><span data-stu-id="0aee1-127">A</span></span></td>
<td><span data-ttu-id="0aee1-128">1</span><span class="sxs-lookup"><span data-stu-id="0aee1-128">1</span></span></td>
<td><span data-ttu-id="0aee1-129">150</span><span class="sxs-lookup"><span data-stu-id="0aee1-129">150</span></span></td>
<td><span data-ttu-id="0aee1-130">หน่วย</span><span class="sxs-lookup"><span data-stu-id="0aee1-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="0aee1-131">$1800.00</span><span class="sxs-lookup"><span data-stu-id="0aee1-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="0aee1-132">$12.00</span><span class="sxs-lookup"><span data-stu-id="0aee1-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0aee1-133">ตารางต่อไปนี้แสดงผลลัพธ์การคำนวณสำหรับออบเจ็กต์สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="0aee1-134">คุณสามารถดูผลลัพธ์โดยการคลิก **ปริมาณกายภาพ** บนหน้า **ออบเจ็กต์ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="0aee1-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0aee1-135">ชนิดออบเจ็กต์</span><span class="sxs-lookup"><span data-stu-id="0aee1-135">Object type</span></span></th>
<th><span data-ttu-id="0aee1-136">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="0aee1-136">Item number</span></span></th>
<th><span data-ttu-id="0aee1-137">ไซต์</span><span class="sxs-lookup"><span data-stu-id="0aee1-137">Site</span></span></th>
<th><span data-ttu-id="0aee1-138">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0aee1-138">Warehouse</span></span></th>
<th><span data-ttu-id="0aee1-139">หมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0aee1-139">Batch No.</span></span></th>
<th><span data-ttu-id="0aee1-140">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="0aee1-140">Quantity</span></span></th>
<th><span data-ttu-id="0aee1-141">หน่วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-141">Inventory unit</span></span></th>
<th><span data-ttu-id="0aee1-142">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="0aee1-142">Value</span></span></th>
<th><span data-ttu-id="0aee1-143">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="0aee1-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aee1-144">ออบเจ็กต์สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-144">Inventory object</span></span></td>
<td><span data-ttu-id="0aee1-145">A</span><span class="sxs-lookup"><span data-stu-id="0aee1-145">A</span></span></td>
<td><span data-ttu-id="0aee1-146">1</span><span class="sxs-lookup"><span data-stu-id="0aee1-146">1</span></span></td>
<td><span data-ttu-id="0aee1-147">11</span><span class="sxs-lookup"><span data-stu-id="0aee1-147">11</span></span></td>
<td><span data-ttu-id="0aee1-148">B1</span><span class="sxs-lookup"><span data-stu-id="0aee1-148">B1</span></span></td>
<td><span data-ttu-id="0aee1-149">100</span><span class="sxs-lookup"><span data-stu-id="0aee1-149">100</span></span></td>
<td><span data-ttu-id="0aee1-150">หน่วย</span><span class="sxs-lookup"><span data-stu-id="0aee1-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="0aee1-151">$1200.00</span><span class="sxs-lookup"><span data-stu-id="0aee1-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="0aee1-152">$12.00</span><span class="sxs-lookup"><span data-stu-id="0aee1-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aee1-153">ออบเจ็กต์สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0aee1-153">Inventory object</span></span></td>
<td><span data-ttu-id="0aee1-154">A</span><span class="sxs-lookup"><span data-stu-id="0aee1-154">A</span></span></td>
<td><span data-ttu-id="0aee1-155">1</span><span class="sxs-lookup"><span data-stu-id="0aee1-155">1</span></span></td>
<td><span data-ttu-id="0aee1-156">11</span><span class="sxs-lookup"><span data-stu-id="0aee1-156">11</span></span></td>
<td><span data-ttu-id="0aee1-157">B2</span><span class="sxs-lookup"><span data-stu-id="0aee1-157">B2</span></span></td>
<td><span data-ttu-id="0aee1-158">50</span><span class="sxs-lookup"><span data-stu-id="0aee1-158">50</span></span></td>
<td><span data-ttu-id="0aee1-159">หน่วย</span><span class="sxs-lookup"><span data-stu-id="0aee1-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="0aee1-160">$600.00</span><span class="sxs-lookup"><span data-stu-id="0aee1-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="0aee1-161">$12.00</span><span class="sxs-lookup"><span data-stu-id="0aee1-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="0aee1-162">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0aee1-162">Additional resources</span></span>
--------

[<span data-ttu-id="0aee1-163">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0aee1-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="0aee1-164">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0aee1-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="0aee1-165">มีอะไรใหม่และมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="0aee1-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



