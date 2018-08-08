---
title: "มิติของผลิตภัณฑ์"
description: "ผลิตภัณฑ์มีสี่มิติ - สี โครงแบบ ขนาด และลักษณะ คุณได้รวมมิติสินค้าในกลุ่มมิติ และกำหนดกลุ่มมิติให้กับผลิตภัณฑ์หลัก การรวมชุดมิติของผลิตภัณฑ์กำหนดวิธีกำหนดผลิตภัณฑ์ย่อย"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: ccb9d47bf6f081dbcc9590bddd4516cf7385ec23
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="product-dimensions"></a><span data-ttu-id="51f73-105">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="51f73-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="51f73-106">ผลิตภัณฑ์มีสี่มิติ - สี โครงแบบ ขนาด และลักษณะ</span><span class="sxs-lookup"><span data-stu-id="51f73-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="51f73-107">คุณได้รวมมิติสินค้าในกลุ่มมิติ และกำหนดกลุ่มมิติให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="51f73-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="51f73-108">การรวมชุดมิติของผลิตภัณฑ์กำหนดวิธีกำหนดผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="51f73-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="51f73-109">มิติของผลิตภัณฑ์มีลักษณะที่ใช้ในการระบุผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="51f73-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="51f73-110">คุณสามารถใช้ชุดมิติของผลิตภัณฑ์เพื่อกำหนดผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="51f73-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="51f73-111">คุณต้องกำหนดอย่างน้อยหนึ่งมิติของผลิตภัณฑ์สำหรับผลิตภัณฑ์หลักเพื่อสร้างผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="51f73-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="51f73-112">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="51f73-112">Product variants</span></span>
----------------

<span data-ttu-id="51f73-113">ผลิตภัณฑ์ย่อยยังถูกอ้างอิงถึงสินค้า</span><span class="sxs-lookup"><span data-stu-id="51f73-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="51f73-114">สินค้าคือผลิตภัณฑ์ที่จับต้องได้ ซึ่งไม่เหมือนกับการบริการ </span><span class="sxs-lookup"><span data-stu-id="51f73-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="51f73-115">จึงจะสามารถกำหนดผลิตภัณฑ์หลัก ด้วยชนิดการบริการ</span><span class="sxs-lookup"><span data-stu-id="51f73-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="51f73-116">โดยการใช้ชนิดการบริการ คุณสามารถระบุผลิตภัณฑ์ย่อยที่รวมการบริการ</span><span class="sxs-lookup"><span data-stu-id="51f73-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="51f73-117">ตัวอย่างเช่น คุณสามารถระบุผลิตภัณฑ์หลักสำหรับงานปรึกษาและผลิตภัณฑ์ย่อยสำหรับงานที่ดำเนินการ โดยที่ปรึกษาอาวุโสและที่ปรึกษาหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="51f73-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="51f73-118">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="51f73-118">Product dimensions</span></span>
<span data-ttu-id="51f73-119">มิติของผลิตภัณฑ์ต่อไปนี้จะพร้อมใช้งาน: การตั้งค่าคอนฟิก สี ขนาด และลักษณะ</span><span class="sxs-lookup"><span data-stu-id="51f73-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="51f73-120">ผลิตภัณฑ์ย่อยสามารถถูกสร้างตามค่ามิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="51f73-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="51f73-121">มิติของผลิตภัณฑ์ เช่น ขนาด สี และลักษณะ สามารถสร้างในหน้า **ขนาด** **สี** และ **ลักษณะ** ซึ่งสามารถเข้าถึงได้จากที่ตั้งต่อไปนี้: **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ตั้งค่า** &gt; **มิติและตัวแปรกลุ่ม** &gt; **ขนาด/สี/ลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="51f73-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="51f73-122">ค่ามิติของผลิตภัณฑ์สำหรับการจัดโครงแบบตามมิติถูกสร้างโดยใช้ตัวจัดโครงแบบผลิตภัณฑ์หรือตัวจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="51f73-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="51f73-123">มิติของผลิตภัณฑ์สร้างและรักษาในหน้า **มิติของผลิตภัณฑ์** ซึ่งสามารถเข้าถึงได้จากที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="51f73-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="51f73-124">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ผลิตภัณฑ์** &gt; **ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="51f73-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="51f73-125">ใน **บานหน้าต่างการดำเนินการ** คลิก **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="51f73-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="51f73-126">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ผลิตภัณฑ์** &gt; **ผลิตภัณฑ์ทั้งหมดและผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="51f73-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="51f73-127">เลือกผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="51f73-127">Select a product master.</span></span> <span data-ttu-id="51f73-128">ใน **บานหน้าต่างการดำเนินการ** คลิก **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="51f73-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="51f73-129">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="51f73-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="51f73-130">เลือกผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="51f73-130">Select a product master.</span></span> <span data-ttu-id="51f73-131">ใน **บานหน้าต่างการดำเนินการ** คลิก **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="51f73-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="51f73-132">ในกลุ่ม **ผลิตภัณฑ์หลัก** คลิก **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="51f73-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="51f73-133">หมายเลขของตัวแปรที่คุณสามารถสร้างขึ้นสำหรับสินค้าถูกจำกัด ด้วยจำนวนชุดมิติของผลิตภัณฑ์ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="51f73-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="51f73-134">**คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="51f73-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f73-135">เมื่อคุณใช้ผลิตภัณฑ์ ตัวอย่างเช่น รายการใบสั่ง คุณเลือกมิติของผลิตภัณฑ์เพื่อระบุผลิตภัณฑ์ย่อยที่คุณต้องการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="51f73-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="51f73-136">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="51f73-136">Example</span></span>
<span data-ttu-id="51f73-137">บริษัทแห่งหนึ่งขายยีนส์ denim</span><span class="sxs-lookup"><span data-stu-id="51f73-137">A company sells denim jeans.</span></span> <span data-ttu-id="51f73-138">สินค้า ยีนส์ ใช้มิติของผลิตภัณฑ์ขนาดและสี</span><span class="sxs-lookup"><span data-stu-id="51f73-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="51f73-139">ยีนส์ถูกขายในสีต่าง ๆ สามสีและขนาดต่าง ๆ หกขนาด</span><span class="sxs-lookup"><span data-stu-id="51f73-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="51f73-140">สี: สีน้ำเงิน สีดำ น้ำตาล ขนาด: XS S M L XL XXL ขนาดไม่ทั้งหมดที่พร้อมใช้งานในสามสีที่มีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="51f73-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="51f73-141">ถ้าชุดทั้งหมดที่พร้อมใช้งาน จะสร้างยีนส์ชนิดต่าง ๆ 18 ชนิด</span><span class="sxs-lookup"><span data-stu-id="51f73-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="51f73-142">ในตัวอย่างนี้ ชุดของผลิตภัณฑ์ย่อยเก้าชุดต่อไปถูกผลิตขึ้น</span><span class="sxs-lookup"><span data-stu-id="51f73-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="51f73-143">สี</span><span class="sxs-lookup"><span data-stu-id="51f73-143">Color</span></span> | <span data-ttu-id="51f73-144">ขนาด</span><span class="sxs-lookup"><span data-stu-id="51f73-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="51f73-145">สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="51f73-145">Blue</span></span>  | <span data-ttu-id="51f73-146">XS</span><span class="sxs-lookup"><span data-stu-id="51f73-146">XS</span></span>   |
| <span data-ttu-id="51f73-147">สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="51f73-147">Blue</span></span>  | <span data-ttu-id="51f73-148">ส.</span><span class="sxs-lookup"><span data-stu-id="51f73-148">S</span></span>    |
| <span data-ttu-id="51f73-149">สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="51f73-149">Blue</span></span>  | <span data-ttu-id="51f73-150">จ.</span><span class="sxs-lookup"><span data-stu-id="51f73-150">M</span></span>    |
| <span data-ttu-id="51f73-151">สีดำ</span><span class="sxs-lookup"><span data-stu-id="51f73-151">Black</span></span> | <span data-ttu-id="51f73-152">จ.</span><span class="sxs-lookup"><span data-stu-id="51f73-152">M</span></span>    |
| <span data-ttu-id="51f73-153">สีดำ</span><span class="sxs-lookup"><span data-stu-id="51f73-153">Black</span></span> | <span data-ttu-id="51f73-154">L</span><span class="sxs-lookup"><span data-stu-id="51f73-154">L</span></span>    |
| <span data-ttu-id="51f73-155">สีดำ</span><span class="sxs-lookup"><span data-stu-id="51f73-155">Black</span></span> | <span data-ttu-id="51f73-156">XL</span><span class="sxs-lookup"><span data-stu-id="51f73-156">XL</span></span>   |
| <span data-ttu-id="51f73-157">สีน้ำตาล</span><span class="sxs-lookup"><span data-stu-id="51f73-157">Brown</span></span> | <span data-ttu-id="51f73-158">L</span><span class="sxs-lookup"><span data-stu-id="51f73-158">L</span></span>    |
| <span data-ttu-id="51f73-159">สีน้ำตาล</span><span class="sxs-lookup"><span data-stu-id="51f73-159">Brown</span></span> | <span data-ttu-id="51f73-160">XL</span><span class="sxs-lookup"><span data-stu-id="51f73-160">XL</span></span>   |
| <span data-ttu-id="51f73-161">สีน้ำตาล</span><span class="sxs-lookup"><span data-stu-id="51f73-161">Brown</span></span> | <span data-ttu-id="51f73-162">XXL</span><span class="sxs-lookup"><span data-stu-id="51f73-162">XXL</span></span>  |






