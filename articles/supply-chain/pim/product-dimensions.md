---
title: มิติของผลิตภัณฑ์
description: ผลิตภัณฑ์มีสี่มิติ - สี โครงแบบ ขนาด และลักษณะ คุณได้รวมมิติสินค้าในกลุ่มมิติ และกำหนดกลุ่มมิติให้กับผลิตภัณฑ์หลัก การรวมชุดมิติของผลิตภัณฑ์กำหนดวิธีกำหนดผลิตภัณฑ์ย่อย
author: cvocph
manager: tfehr
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5e9b10fa18ada9534ce5e279d4f1f09973a802b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208443"
---
# <a name="product-dimensions"></a><span data-ttu-id="c7b30-105">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c7b30-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7b30-106">ผลิตภัณฑ์มีสี่มิติ - สี โครงแบบ ขนาด และลักษณะ</span><span class="sxs-lookup"><span data-stu-id="c7b30-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="c7b30-107">คุณได้รวมมิติสินค้าในกลุ่มมิติ และกำหนดกลุ่มมิติให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="c7b30-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="c7b30-108">การรวมชุดมิติของผลิตภัณฑ์กำหนดวิธีกำหนดผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="c7b30-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="c7b30-109">มิติของผลิตภัณฑ์มีลักษณะที่ใช้ในการระบุผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="c7b30-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="c7b30-110">คุณสามารถใช้ชุดมิติของผลิตภัณฑ์เพื่อกำหนดผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="c7b30-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="c7b30-111">คุณต้องกำหนดอย่างน้อยหนึ่งมิติของผลิตภัณฑ์สำหรับผลิตภัณฑ์หลักเพื่อสร้างผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="c7b30-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>

## <a name="product-variants"></a><span data-ttu-id="c7b30-112">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="c7b30-112">Product variants</span></span>

<span data-ttu-id="c7b30-113">ผลิตภัณฑ์ย่อยยังถูกอ้างอิงถึงสินค้า</span><span class="sxs-lookup"><span data-stu-id="c7b30-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="c7b30-114">สินค้าคือผลิตภัณฑ์ที่จับต้องได้ ซึ่งไม่เหมือนกับการบริการ </span><span class="sxs-lookup"><span data-stu-id="c7b30-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="c7b30-115">จึงจะสามารถกำหนดผลิตภัณฑ์หลัก ด้วยชนิดการบริการ</span><span class="sxs-lookup"><span data-stu-id="c7b30-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="c7b30-116">โดยการใช้ชนิดการบริการ คุณสามารถระบุผลิตภัณฑ์ย่อยที่รวมการบริการ</span><span class="sxs-lookup"><span data-stu-id="c7b30-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="c7b30-117">ตัวอย่างเช่น คุณสามารถระบุผลิตภัณฑ์หลักสำหรับงานปรึกษาและผลิตภัณฑ์ย่อยสำหรับงานที่ดำเนินการ โดยที่ปรึกษาอาวุโสและที่ปรึกษาหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="c7b30-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="c7b30-118">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c7b30-118">Product dimensions</span></span>
<span data-ttu-id="c7b30-119">มิติของผลิตภัณฑ์ต่อไปนี้จะพร้อมใช้งาน: การตั้งค่าคอนฟิก สี ขนาด และลักษณะ</span><span class="sxs-lookup"><span data-stu-id="c7b30-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="c7b30-120">ผลิตภัณฑ์ย่อยสามารถถูกสร้างตามค่ามิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c7b30-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="c7b30-121">มิติของผลิตภัณฑ์ เช่น ขนาด สี และลักษณะ สามารถสร้างในหน้า **ขนาด** **สี** และ **ลักษณะ** ซึ่งสามารถเข้าถึงได้จากที่ตั้งต่อไปนี้: **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ตั้งค่า** &gt; **มิติและตัวแปรกลุ่ม** &gt; **ขนาด/สี/ลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="c7b30-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="c7b30-122">ค่ามิติของผลิตภัณฑ์สำหรับการจัดโครงแบบตามมิติถูกสร้างโดยใช้ตัวจัดโครงแบบผลิตภัณฑ์หรือตัวจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="c7b30-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="c7b30-123">มิติของผลิตภัณฑ์สร้างและรักษาในหน้า **มิติของผลิตภัณฑ์** ซึ่งสามารถเข้าถึงได้จากที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7b30-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="c7b30-124">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ผลิตภัณฑ์** &gt; **ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="c7b30-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="c7b30-125">ใน **บานหน้าต่างการดำเนินการ** คลิก **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c7b30-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="c7b30-126">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ผลิตภัณฑ์** &gt; **ผลิตภัณฑ์ทั้งหมดและผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="c7b30-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="c7b30-127">เลือกผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="c7b30-127">Select a product master.</span></span> <span data-ttu-id="c7b30-128">ใน **บานหน้าต่างการดำเนินการ** คลิก **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c7b30-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="c7b30-129">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="c7b30-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="c7b30-130">เลือกผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="c7b30-130">Select a product master.</span></span> <span data-ttu-id="c7b30-131">ใน **บานหน้าต่างการดำเนินการ** คลิก **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c7b30-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="c7b30-132">ในกลุ่ม **ผลิตภัณฑ์หลัก** คลิก **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c7b30-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="c7b30-133">หมายเลขของตัวแปรที่คุณสามารถสร้างขึ้นสำหรับสินค้าถูกจำกัด ด้วยจำนวนชุดมิติของผลิตภัณฑ์ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="c7b30-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="c7b30-134">**คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="c7b30-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b30-135">เมื่อคุณใช้ผลิตภัณฑ์ ตัวอย่างเช่น รายการใบสั่ง คุณเลือกมิติของผลิตภัณฑ์เพื่อระบุผลิตภัณฑ์ย่อยที่คุณต้องการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c7b30-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="c7b30-136">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c7b30-136">Example</span></span>
<span data-ttu-id="c7b30-137">บริษัทแห่งหนึ่งขายยีนส์ denim</span><span class="sxs-lookup"><span data-stu-id="c7b30-137">A company sells denim jeans.</span></span> <span data-ttu-id="c7b30-138">สินค้า ยีนส์ ใช้มิติของผลิตภัณฑ์ขนาดและสี</span><span class="sxs-lookup"><span data-stu-id="c7b30-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="c7b30-139">ยีนส์ถูกขายในสีต่าง ๆ สามสีและขนาดต่าง ๆ หกขนาด</span><span class="sxs-lookup"><span data-stu-id="c7b30-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="c7b30-140">สี: สีน้ำเงิน สีดำ น้ำตาล ขนาด: XS S M L XL XXL ขนาดไม่ทั้งหมดที่พร้อมใช้งานในสามสีที่มีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7b30-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="c7b30-141">ถ้าชุดทั้งหมดที่พร้อมใช้งาน จะสร้างยีนส์ชนิดต่าง ๆ 18 ชนิด</span><span class="sxs-lookup"><span data-stu-id="c7b30-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="c7b30-142">ในตัวอย่างนี้ ชุดของผลิตภัณฑ์ย่อยเก้าชุดต่อไปถูกผลิตขึ้น</span><span class="sxs-lookup"><span data-stu-id="c7b30-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="c7b30-143">สี</span><span class="sxs-lookup"><span data-stu-id="c7b30-143">Color</span></span> | <span data-ttu-id="c7b30-144">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c7b30-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="c7b30-145">สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="c7b30-145">Blue</span></span>  | <span data-ttu-id="c7b30-146">XS</span><span class="sxs-lookup"><span data-stu-id="c7b30-146">XS</span></span>   |
| <span data-ttu-id="c7b30-147">สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="c7b30-147">Blue</span></span>  | <span data-ttu-id="c7b30-148">ส.</span><span class="sxs-lookup"><span data-stu-id="c7b30-148">S</span></span>    |
| <span data-ttu-id="c7b30-149">สีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="c7b30-149">Blue</span></span>  | <span data-ttu-id="c7b30-150">จ.</span><span class="sxs-lookup"><span data-stu-id="c7b30-150">M</span></span>    |
| <span data-ttu-id="c7b30-151">สีดำ</span><span class="sxs-lookup"><span data-stu-id="c7b30-151">Black</span></span> | <span data-ttu-id="c7b30-152">จ.</span><span class="sxs-lookup"><span data-stu-id="c7b30-152">M</span></span>    |
| <span data-ttu-id="c7b30-153">สีดำ</span><span class="sxs-lookup"><span data-stu-id="c7b30-153">Black</span></span> | <span data-ttu-id="c7b30-154">L</span><span class="sxs-lookup"><span data-stu-id="c7b30-154">L</span></span>    |
| <span data-ttu-id="c7b30-155">สีดำ</span><span class="sxs-lookup"><span data-stu-id="c7b30-155">Black</span></span> | <span data-ttu-id="c7b30-156">XL</span><span class="sxs-lookup"><span data-stu-id="c7b30-156">XL</span></span>   |
| <span data-ttu-id="c7b30-157">สีน้ำตาล</span><span class="sxs-lookup"><span data-stu-id="c7b30-157">Brown</span></span> | <span data-ttu-id="c7b30-158">L</span><span class="sxs-lookup"><span data-stu-id="c7b30-158">L</span></span>    |
| <span data-ttu-id="c7b30-159">สีน้ำตาล</span><span class="sxs-lookup"><span data-stu-id="c7b30-159">Brown</span></span> | <span data-ttu-id="c7b30-160">XL</span><span class="sxs-lookup"><span data-stu-id="c7b30-160">XL</span></span>   |
| <span data-ttu-id="c7b30-161">สีน้ำตาล</span><span class="sxs-lookup"><span data-stu-id="c7b30-161">Brown</span></span> | <span data-ttu-id="c7b30-162">XXL</span><span class="sxs-lookup"><span data-stu-id="c7b30-162">XXL</span></span>  |





