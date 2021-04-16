---
title: ออบเจ็กต์ต้นทุน
description: บทความนี้แสดงข้อมูลเกี่ยวกับต้นทุนวัตถุ และอธิบายถึงวิธีสะสมต้นทุนและปริมาณ วัตถุต้นทุนเป็นเอนทิตี้ที่สะสมต้นทุนและปริมาณ เอนทิตีออบเจ็กต์ต้นทุนอาจเป็นผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย เช่นผลต่างสำหรับลักษณะและสี
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0a8c39977dacd78afc3bec977501abaf8081dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839354"
---
# <a name="cost-objects"></a><span data-ttu-id="6d61f-105">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6d61f-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d61f-106">บทความนี้แสดงข้อมูลเกี่ยวกับต้นทุนวัตถุ และอธิบายถึงวิธีสะสมต้นทุนและปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6d61f-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="6d61f-107">วัตถุต้นทุนเป็นเอนทิตี้ที่สะสมต้นทุนและปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6d61f-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="6d61f-108">เอนทิตีออบเจ็กต์ต้นทุนอาจเป็นผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย เช่นผลต่างสำหรับลักษณะและสี</span><span class="sxs-lookup"><span data-stu-id="6d61f-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="6d61f-109">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6d61f-109">Cost objects</span></span>

<span data-ttu-id="6d61f-110">หน้า **ต้นทุนวัตถุ** แสดงรายการวัตถุต้นทุนทั้งหมดที่ลงทะเบียนกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6d61f-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="6d61f-111">วัตถุต้นทุนถูกกำหนด โดยข้อมูลจากแหล่งข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6d61f-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="6d61f-112">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6d61f-112">Product</span></span>
-   <span data-ttu-id="6d61f-113">กลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6d61f-113">Product dimension group</span></span>
-   <span data-ttu-id="6d61f-114">กลุ่มมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="6d61f-114">Storage dimension group</span></span>
-   <span data-ttu-id="6d61f-115">กลุ่มมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="6d61f-115">Tracking dimension group</span></span>

<span data-ttu-id="6d61f-116">**หมายเหตุ:** ต้นทุนวัตถุแสดงถึงองค์ประกอบต้นทุนของชนิด **วัสดุทางตรง** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6d61f-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="6d61f-117">ต้นทุนวัตถุและออบเจ็กต์สินค้าคงคลังแตกต่างกันในลักษณะที่ต้นทุนวัตถุจะถูกกำหนด โดยมิติสินค้าคงคลังที่ถูกเลือกสำหรับสินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6d61f-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="6d61f-118">ตัวอย่างเช่น สินค้ามีการตั้งค่าไว้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="6d61f-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="6d61f-119">**ไซต์:** สินค้าคงคลังทางกายภาพ =ใช่, สินค้าคงคลังทางการเงิน =ใช่</span><span class="sxs-lookup"><span data-stu-id="6d61f-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="6d61f-120">**คลังสินค้า:** สินค้าคงคลังทางกายภาพ =ใช่, สินค้าคงคลังทางการเงิน =ใช่</span><span class="sxs-lookup"><span data-stu-id="6d61f-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="6d61f-121">**หมายเลขชุดงาน:** สินค้าคงคลังทางกายภาพ =ใช่, สินค้าคงคลังทางการเงิน =ใช่</span><span class="sxs-lookup"><span data-stu-id="6d61f-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="6d61f-122">ตารางต่อไปนี้แสดงว่าวัตถุต้นทุนและออบเจ็กต์สินค้าคงคลังคืออะไร</span><span class="sxs-lookup"><span data-stu-id="6d61f-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="6d61f-123">ชนิดออบเจ็กต์</span><span class="sxs-lookup"><span data-stu-id="6d61f-123">Object type</span></span>      | <span data-ttu-id="6d61f-124">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="6d61f-124">Item number</span></span> | <span data-ttu-id="6d61f-125">ไซต์</span><span class="sxs-lookup"><span data-stu-id="6d61f-125">Site</span></span> | <span data-ttu-id="6d61f-126">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6d61f-126">Warehouse</span></span> | <span data-ttu-id="6d61f-127">หมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="6d61f-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="6d61f-128">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6d61f-128">Cost object</span></span>      | <span data-ttu-id="6d61f-129"> x</span><span class="sxs-lookup"><span data-stu-id="6d61f-129">x</span></span>           | <span data-ttu-id="6d61f-130"> x</span><span class="sxs-lookup"><span data-stu-id="6d61f-130">x</span></span>    |           |           |
| <span data-ttu-id="6d61f-131">ออบเจ็กต์สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="6d61f-131">Inventory object</span></span> | <span data-ttu-id="6d61f-132"> x</span><span class="sxs-lookup"><span data-stu-id="6d61f-132">x</span></span>           | <span data-ttu-id="6d61f-133"> x</span><span class="sxs-lookup"><span data-stu-id="6d61f-133">x</span></span>    |  <span data-ttu-id="6d61f-134"> x</span><span class="sxs-lookup"><span data-stu-id="6d61f-134">x</span></span>        | <span data-ttu-id="6d61f-135"> x</span><span class="sxs-lookup"><span data-stu-id="6d61f-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="6d61f-136">รวบรวมของต้นทุนและปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6d61f-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="6d61f-137">ค่าในฟิลด์ **ค่า** เป็นผลรวมของค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6d61f-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="6d61f-138">ยอดต้นทุนจริง</span><span class="sxs-lookup"><span data-stu-id="6d61f-138">Physical cost amount</span></span>
    -   <span data-ttu-id="6d61f-139">ยอดต้นทุนทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6d61f-139">Financial cost amount</span></span>
    -   <span data-ttu-id="6d61f-140">การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="6d61f-140">Adjustments</span></span>
-   <span data-ttu-id="6d61f-141">ค่าในฟิลด์ **ปริมาณ** เป็นผลรวมของค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6d61f-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="6d61f-142">ได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="6d61f-142">Received</span></span>
    -   <span data-ttu-id="6d61f-143">หักบัญชี</span><span class="sxs-lookup"><span data-stu-id="6d61f-143">Deducted</span></span>
    -   <span data-ttu-id="6d61f-144">ปริมาณที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="6d61f-144">Posted quantity</span></span>
-   <span data-ttu-id="6d61f-145">ฟิลด์ **ต้นทุนเฉลี่ยต่อหน่วย** เป็นฟิลด์ที่คำนวณแล้ว</span><span class="sxs-lookup"><span data-stu-id="6d61f-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="6d61f-146">ค่าที่คำนวณ โดยการหาร **ค่า** ค่าโดยค่า **ปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="6d61f-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="6d61f-147">**หมายเหตุ:** พารามิเตอร์ **รวมมูลค่าจริง** จะไม่มีผลต่อการคำนวณก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6d61f-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6d61f-148">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6d61f-148">Additional resources</span></span>
--------

[<span data-ttu-id="6d61f-149">กลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6d61f-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="6d61f-150">กลุ่มมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="6d61f-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="6d61f-151">กลุ่มมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="6d61f-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="6d61f-152">มีอะไรใหม่หรือมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6d61f-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="6d61f-153">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6d61f-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]