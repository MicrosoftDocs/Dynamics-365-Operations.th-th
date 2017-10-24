---
title: "ระบบการตั้งชื่อสำหรับชื่อและหมายเลขผลิตภัณฑ์ย่อย"
description: "หัวข้อนี้อธิบายวิธีที่คุณสามารถตั้งค่าระบบการตั้งชื่อหมายเลขผลิตภัณฑ์เพื่อแทนที่รูปแบบ [หมายเลขผลิตภัณฑ์หลัก - การจัดโครงแบบ - ขนาด -สี - ลักษณะ] ที่คงที่ ระบบการตั้งชื่อใหม่มีรูปแบบที่เป็นเป้าหมายที่มีหมายเลขผลิตภัณฑ์หลัก มิติของผลิตภัณฑ์ที่ใช้งานอยู่ และตัวกำหนดเขตข้อความที่คุณเลือก นอกจากนี้ คุณยังสามารถสร้างระบบการตั้งชื่อสำหรับชื่อผลิตภัณฑ์ ท้ายสุด คุณยังสามารถสร้างระบบการตั้งชื่อเพื่อระบุการจัดโครงแบบที่สร้างขึ้นโดยตัวจัดโครงแบบผลิตภัณฑ์ตามข้อจำกัดได้อีกด้วย ระบบการตั้งชื่อเหล่านี้อาจประกอบด้วยแอททริบิวต์ที่คุณเลือก"
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 4ebebc1d287908dbe8ac7557c34fc6693c88bfae
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="a1a8b-107">ระบบการตั้งชื่อสำหรับชื่อและหมายเลขผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="a1a8b-108">หัวข้อนี้อธิบายวิธีที่คุณสามารถตั้งค่าระบบการตั้งชื่อหมายเลขผลิตภัณฑ์เพื่อแทนที่รูปแบบ [หมายเลขผลิตภัณฑ์หลัก - การจัดโครงแบบ - ขนาด -สี - ลักษณะ] ที่คงที่</span><span class="sxs-lookup"><span data-stu-id="a1a8b-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="a1a8b-109">ระบบการตั้งชื่อใหม่มีรูปแบบที่เป็นเป้าหมายที่มีหมายเลขผลิตภัณฑ์หลัก มิติของผลิตภัณฑ์ที่ใช้งานอยู่ และตัวกำหนดเขตข้อความที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="a1a8b-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="a1a8b-110">นอกจากนี้ คุณยังสามารถสร้างระบบการตั้งชื่อสำหรับชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a1a8b-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="a1a8b-111">ท้ายสุด คุณยังสามารถสร้างระบบการตั้งชื่อเพื่อระบุการจัดโครงแบบที่สร้างขึ้นโดยตัวจัดโครงแบบผลิตภัณฑ์ตามข้อจำกัดได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="a1a8b-112">ระบบการตั้งชื่อเหล่านี้อาจประกอบด้วยแอททริบิวต์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="a1a8b-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="a1a8b-113">ระบบการตั้งชื่อใหม่สำหรับหมายเลขผลิตภัณฑ์ย่อยและชื่อผลิตภัณฑ์ย่อยช่วยให้คุณสามารถรวมเซ็กเมนต์ในตัวระบุสำหรับผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="a1a8b-114">เซ็กเมนต์เหล่านี้อาจรวมถึงชื่อและหมายเลขผลิตภัณฑ์หลัก รหัสและชื่อมิติของผลิตภัณฑ์ ลำดับหมายเลข ค่าคงที่ข้อความ และแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a1a8b-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="a1a8b-115">ฟังก์ชันนี้ช่วยให้คุณสามารถค้นหาผลิตภัณฑ์ย่อยเฉพาะได้อย่างรวดเร็วเมื่อคุณสร้างใบสั่งซื้อหรือใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="a1a8b-116">คุณสร้างระบบการตั้งชื่อสำหรับทั้งหมายเลขผลิตภัณฑ์ย่อยและชื่อผลิตภัณฑ์ย่อยโดยใช้หน้า **ระบบการตั้งชื่อผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="a1a8b-117">เมื่อต้องการเปิดหน้านี้ คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="a1a8b-118">ระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="a1a8b-119">มีการสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลักตามค่าใดค่าหนึ่งในเทคโนโลยีการตั้งค่าคอนฟิกสามรายการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="a1a8b-120">ผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-120">Predefined variants</span></span>
-   <span data-ttu-id="a1a8b-121">ตามข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="a1a8b-121">Constraint-based</span></span>
-   <span data-ttu-id="a1a8b-122">ตามมิติ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-122">Dimension-based</span></span>

<span data-ttu-id="a1a8b-123">ผลิตภัณฑ์ย่อยแต่ละรายการมีหมายเลขและชื่อ และระบบการตั้งชื่อการระบุผลิตภัณฑ์ย่อยช่วยให้คุณสามารถเลือกเซ็กเมนต์ที่จะรวมอยู่ในแต่ละหมายเลขหรือชื่อผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="a1a8b-124">คุณสามารถเลือกเซ็กเมนต์ต่อไปนี้ในหน้า **ระบบการตั้งชื่อผลิตภัณฑ์** ได้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="a1a8b-125">หมายเลขผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="a1a8b-125">Product master number</span></span>
-   <span data-ttu-id="a1a8b-126">ชื่อผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="a1a8b-126">Product master name</span></span>
-   <span data-ttu-id="a1a8b-127">ค่าของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a1a8b-127">Number sequence value</span></span>
-   <span data-ttu-id="a1a8b-128">ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-128">Text constant</span></span>
-   <span data-ttu-id="a1a8b-129">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a1a8b-129">Product dimensions</span></span>
    -   <span data-ttu-id="a1a8b-130">รหัสหรือชื่อการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="a1a8b-131">รหัสหรือชื่อสี</span><span class="sxs-lookup"><span data-stu-id="a1a8b-131">Color ID or name</span></span>
    -   <span data-ttu-id="a1a8b-132">รหัสหรือชื่อขนาด</span><span class="sxs-lookup"><span data-stu-id="a1a8b-132">Size ID or name</span></span>
    -   <span data-ttu-id="a1a8b-133">รหัสหรือชื่อลักษณะ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-133">Style ID or name</span></span>

<span data-ttu-id="a1a8b-134">หลังจากที่คุณกำหนดระบบการตั้งชื่อหมายเลขการระบุผลิตภัณฑ์ย่อย คุณสามารถเชื่อมโยงกับกลุ่มมิติของผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="a1a8b-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="a1a8b-135">ดังนั้นผลิตภัณฑ์หลักทั้งหมดที่อ้างอิงถึงกลุ่มมิติของผลิตภัณฑ์นี้จะถูกกำหนดหมายเลขผลิตภัณฑ์ย่อยตามระบบการตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="a1a8b-136">อย่างไรก็ตาม ระบบการตั้งชื่อของชื่อผลิตภัณฑ์ย่อยไม่สามารถเชื่อมโยงกับกลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a1a8b-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="a1a8b-137">คุณยังสามารถกำหนดระบบการตั้งชื่อเป็นการระบุผลิตภัณฑ์ย่อยโดยตรงให้กับผลิตภัณฑ์หลักได้</span><span class="sxs-lookup"><span data-stu-id="a1a8b-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="a1a8b-138">ในกรณีนี้ ผลิตภัณฑ์ย่อยที่เป็นของผลิตภัณฑ์หลักจะถูกกำหนดหมายเลขและชื่อผลิตภัณฑ์ย่อยตามระบบการตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="a1a8b-139">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-139">Example</span></span>

<span data-ttu-id="a1a8b-140">มีการผลิตเสื้อยืดคอกลม (TS1234) ขึ้นสามขนาด (S, M, L) สี่สี (สีแดง สีเขียว สีน้ำเงิน สีเหลือง) และสองลักษณะ (Polo, V)</span><span class="sxs-lookup"><span data-stu-id="a1a8b-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="a1a8b-141">ดังนั้น อาจมีผลิตภัณ์ย่อยได้ 24 รายการ (= 3 × 4 × 2)</span><span class="sxs-lookup"><span data-stu-id="a1a8b-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="a1a8b-142">คุณสร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ย่อยที่มีเซ็กเมนต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="a1a8b-143">หมายเลขผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="a1a8b-143">Product master number</span></span>
2.  <span data-ttu-id="a1a8b-144">ค่าคงที่ของข้อความ: "-"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="a1a8b-145">สี</span><span class="sxs-lookup"><span data-stu-id="a1a8b-145">Color</span></span>
4.  <span data-ttu-id="a1a8b-146">ค่าคงที่ของข้อความ: "-"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="a1a8b-147">ขนาด</span><span class="sxs-lookup"><span data-stu-id="a1a8b-147">Size</span></span>
6.  <span data-ttu-id="a1a8b-148">ค่าคงที่ของข้อความ: "-"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="a1a8b-149">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-149">Style</span></span>

<span data-ttu-id="a1a8b-150">ในกรณีนี้ หมายเลขผลิตภัณฑ์ย่อยสำหรับเสื้อยืดคอกลมสีแดง ขนาดเล็ก แบบ Polo คือ TS1234-Red-Small-Polo</span><span class="sxs-lookup"><span data-stu-id="a1a8b-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="a1a8b-151">ระบบการตั้งชื่อของการจัดโครงแบบตามข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="a1a8b-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="a1a8b-152">สำหรับการจัดโครงแบบตามข้อจำกัด คุณสามารถสร้างระบบการตั้งชื่อเฉพาะสำหรับมิติของผลิตภัณฑ์การจัดการโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="a1a8b-153">คุณสามารถเลือกเซ็กเมนต์ต่อไปนี้ในหน้า **ระบบการตั้งชื่อผลิตภัณฑ์** ได้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="a1a8b-154">ค่าของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a1a8b-154">Number sequence value</span></span>
-   <span data-ttu-id="a1a8b-155">ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-155">Text constant</span></span>
-   <span data-ttu-id="a1a8b-156">ค่าแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a1a8b-156">Attribute value</span></span>

<span data-ttu-id="a1a8b-157">แต่ละส่วนประกอบในแบบจำลองการจัดโครงแบบผลิตภัณฑ์สามารถมีระบบการตั้งชื่อการจัดโครงแบบของตนเอง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="a1a8b-158">สามารถใช้ได้เฉพาะแอททริบิวต์ของส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="a1a8b-159">ไม่สามารถใช้แอททริบิวต์จากส่วนประกอบย่อยหรือความต้องการของผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="a1a8b-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="a1a8b-160">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-160">Example</span></span>

<span data-ttu-id="a1a8b-161">แบบจำลองการจัดโครงแบบผลิตภัณฑ์มีส่วนประกอบรากที่มีแอททริบิวต์สองรายการ:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="a1a8b-162">วัสดุ (พลาสติก ไม้ เหล็ก)</span><span class="sxs-lookup"><span data-stu-id="a1a8b-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="a1a8b-163">ความยาว (10...100)</span><span class="sxs-lookup"><span data-stu-id="a1a8b-163">Length (10...100)</span></span>

<span data-ttu-id="a1a8b-164">คุณสร้างระบบการตั้งชื่อสำหรับการจัดโครงแบบที่มีเซ็กเมนต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="a1a8b-165">ค่าแอททริบิวต์: วัสดุ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="a1a8b-166">ค่าคงที่ของข้อความ: "AAA"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="a1a8b-167">ค่าแอททริบิวต์: ความยาว</span><span class="sxs-lookup"><span data-stu-id="a1a8b-167">Attribute value: Length</span></span>

<span data-ttu-id="a1a8b-168">ในกรณีนี้ รหัสการจัดโครงแบบสำหรับชิ้นไม้วัสดุซึ่งมีความยาวเท่ากับ 78 จะเป็น WoodAAA78</span><span class="sxs-lookup"><span data-stu-id="a1a8b-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="a1a8b-169">ระบบการตั้งชื่อการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="a1a8b-170">สำหรับการจัดโครงแบบตามมิติ คุณสามารถสร้างระบบการตั้งชื่อเฉพาะสำหรับมิติของผลิตภัณฑ์การจัดการโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="a1a8b-171">คุณสามารถเลือกเซ็กเมนต์ต่อไปนี้ในหน้า **ระบบการตั้งชื่อผลิตภัณฑ์** ได้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="a1a8b-172">ค่าของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a1a8b-172">Number sequence value</span></span>
-   <span data-ttu-id="a1a8b-173">ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-173">Text constant</span></span>
-   <span data-ttu-id="a1a8b-174">สินค้าในกลุ่มการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-174">Configuration group item</span></span>

<span data-ttu-id="a1a8b-175">คุณสามารถกำหนดระบบการตั้งชื่อการจัดโครงแบบสำหรับสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="a1a8b-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="a1a8b-176">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-176">Example</span></span>

<span data-ttu-id="a1a8b-177">BOM มีรายการ BOM สี่รายการที่มีการแบ่งกลุ่มการจัดโครงแบบออกเป็นสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="a1a8b-178">รายการ BOM: M0007 Cabinet มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="a1a8b-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="a1a8b-179">กลุ่มการจัดโครงแบบ: Cabinet</span><span class="sxs-lookup"><span data-stu-id="a1a8b-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="a1a8b-180">รายการ BOM: M0008 Cabinet ชั้นสูง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="a1a8b-181">กลุ่มการจัดโครงแบบ: Cabinet</span><span class="sxs-lookup"><span data-stu-id="a1a8b-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="a1a8b-182">รายการ BOM: M0021 ผ้า Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="a1a8b-183">กลุ่มการจัดโครงแบบ: Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="a1a8b-184">รายการ BOM: M0022 โลหะ Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="a1a8b-185">กลุ่มการจัดโครงแบบ: Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-185">Configuration group: Front grill</span></span>

<span data-ttu-id="a1a8b-186">คุณสร้างระบบการตั้งชื่อสำหรับการจัดโครงแบบที่มีเซ็กเมนต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="a1a8b-187">กลุ่มการจัดโครงแบบ: Cabinet</span><span class="sxs-lookup"><span data-stu-id="a1a8b-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="a1a8b-188">ค่าคงที่ของข้อความ: "&"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="a1a8b-189">กลุ่มการจัดโครงแบบ: Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-189">Configuration group: Front grill</span></span>

<span data-ttu-id="a1a8b-190">ในกรณีนี้ รหัสการจัดโครงแบบสำหรับ Cabinet มาตรฐานที่มีผ้า Grill หน้าคือ M0007&M0021</span><span class="sxs-lookup"><span data-stu-id="a1a8b-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="a1a8b-191">ระบบการตั้งชื่อสำหรับชุดผลิตภัณฑ์ย่อยและการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="a1a8b-192">เมื่อคุณใช้เทคโนโลยีการจัดโครงแบบตามข้อจำกัดหรือตามมิติอย่างใดอย่างหนึ่งเพื่อจัดโครงแบบผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก หมายเลขผลิตภัณฑ์ย่อยของผลิตภัณฑ์ย่อยสามารถรวมระบบการตั้งชื่อจากมิติการจัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="a1a8b-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="a1a8b-193">ทำตามขั้นตอนเหล่านี้เพื่อจัดโครงแบบผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="a1a8b-194">ในหน้า **ระบบการตั้งชื่อผลิตภัณฑ์** กำหนดระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อยที่มีมิติการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="a1a8b-195">กำหนดระบบการตั้งชื่อให้กับกลุ่มมิติของผลิตภัณฑ์ที่มีมิติการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="a1a8b-196">กำหนดระบบการตั้งชื่อการจัดโครงแบบสำหรับส่วนประกอบหรือ BOM ที่จะใช้ในการจัดโครงแบบผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="a1a8b-197">นอกจากนี้ คุณยังสามารถสร้างระบบการตั้งชื่อสำหรับชื่อผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="a1a8b-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="a1a8b-198">สามารถจัดโครงแบบชื่อผลิตภัณฑ์ย่อยให้รวมรหัสหรือชื่อการจัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="a1a8b-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="a1a8b-199">ตัวอย่างการจัดโครงแบบตามข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="a1a8b-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="a1a8b-200">สำหรับตัวอย่างนี้ ให้ใช้ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อยที่ประกอบด้วยเซ็กเมนต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="a1a8b-201">หมายเลขผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="a1a8b-201">Product master number</span></span>
2.  <span data-ttu-id="a1a8b-202">ค่าคงที่ของข้อความ "\_"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="a1a8b-203">โครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-203">Configuration</span></span>

<span data-ttu-id="a1a8b-204">ระบบการตั้งชื่อการจัดโครงแบบประกอบด้วยเซ็กเมนต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="a1a8b-205">ค่าแอททริบิวต์: วัสดุ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="a1a8b-206">ค่าคงที่ของข้อความ: "AAA"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="a1a8b-207">ค่าแอททริบิวต์: ความยาว</span><span class="sxs-lookup"><span data-stu-id="a1a8b-207">Attribute value: Length</span></span>

<span data-ttu-id="a1a8b-208">ให้ป้อนค่าต่อไปนี้สำหรับเซ็กเมนต์:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="a1a8b-209">หมายเลขผลิตภัณฑ์หลัก = **M0099**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="a1a8b-210">วัสดุ = **พลาสติก**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="a1a8b-211">ความยาว = **12**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-211">Length = **12**</span></span>

<span data-ttu-id="a1a8b-212">ในกรณีนี้ หมายเลขผลิตภัณฑ์ย่อยจะเป็น M0099\_PlasticAAA12</span><span class="sxs-lookup"><span data-stu-id="a1a8b-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="a1a8b-213">ตัวอย่างการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="a1a8b-214">สำหรับตัวอย่างนี้ ให้ใช้ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อยที่ประกอบด้วยเซ็กเมนต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="a1a8b-215">หมายเลขผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="a1a8b-215">Product master number</span></span>
2.  <span data-ttu-id="a1a8b-216">ค่าคงที่ของข้อความ "//"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-216">Text constant "//"</span></span>
3.  <span data-ttu-id="a1a8b-217">โครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-217">Configuration</span></span>

<span data-ttu-id="a1a8b-218">ระบบการตั้งชื่อการจัดโครงแบบประกอบด้วยเซ็กเมนต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="a1a8b-219">กลุ่มการจัดโครงแบบ: Cabinet</span><span class="sxs-lookup"><span data-stu-id="a1a8b-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="a1a8b-220">ค่าคงที่ของข้อความ: "&"</span><span class="sxs-lookup"><span data-stu-id="a1a8b-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="a1a8b-221">กลุ่มการจัดโครงแบบ: Grill หน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-221">Configuration group: Front grill</span></span>

<span data-ttu-id="a1a8b-222">ให้ป้อนค่าต่อไปนี้สำหรับเซ็กเมนต์:</span><span class="sxs-lookup"><span data-stu-id="a1a8b-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="a1a8b-223">หมายเลขผลิตภัณฑ์หลัก = **D0123**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="a1a8b-224">Cabinet = **M0008**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="a1a8b-225">Grill หน้า = **M0022**</span><span class="sxs-lookup"><span data-stu-id="a1a8b-225">Front grill = **M0022**</span></span>

<span data-ttu-id="a1a8b-226">ในกรณีนี้ หมายเลขผลิตภัณฑ์ย่อยจะเป็น D0123//M0008&M0022</span><span class="sxs-lookup"><span data-stu-id="a1a8b-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="a1a8b-227">การกำหนดหมายเลขความขัดแย้ง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-227">Numbering conflicts</span></span>
<span data-ttu-id="a1a8b-228">ในบางกรณี ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อยที่คุณตั้งค่าอาจไม่ได้สร้างหมายเลขผลิตภัณฑ์ย่อยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="a1a8b-229">ตัวอย่างเช่น หมายเลขผลิตภัณฑ์ย่อยจะซ้ำกันถ้าไม่มีมิติของผลิตภัณฑ์ที่ใช้งานอยู่หนึ่งรายการรวมอยู่ในระบบการตั้งชื่อสำหรับผลิตภัณฑ์หลักที่ใช้เทคโนโลยีการจัดโครงแบบผันแปรที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="a1a8b-230">วิธีการที่คุณจัดการกับความขัดแย้งแตกต่างกันไปขึ้นอยู่กับเทคโนโลยีการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="a1a8b-231">ผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-231">Predefined variants</span></span>

<span data-ttu-id="a1a8b-232">ข้อผิดพลาดจะเกิดขึ้นถ้าคุณพยายามสร้างผลิตภัณฑ์ย่อยหนึ่งหรือหลายรายการที่ลงท้ายด้วยหมายเลขผลิตภัณฑ์ย่อยโดยอัตโนมัติหรือด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="a1a8b-233">เพื่อหลีกเลี่ยงสถานการณ์นี้ คุณควรใช้มิติของผลิตภัณฑ์ที่ใช้งานอยู่ทั้งหมดในกลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a1a8b-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="a1a8b-234">อีกทางหนึ่งคือ รวมลำดับหมายเลขเพื่อช่วยในการรับประกันว่าหมายเลขผลิตภัณฑ์ย่อยไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="a1a8b-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="a1a8b-235">การจัดโครงแบบตามข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="a1a8b-235">Constraint-based configurations</span></span>

<span data-ttu-id="a1a8b-236">โดยขึ้นอยู่กับระบบการตั้งชื่อ ระบบอาจพยายามที่จะกำหนดหมายเลขผลิตภัณฑ์ย่อยที่ซ้ำกันให้กับการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="a1a8b-237">ในกรณีนี้ ระบบจะใช้ลำดับหมายเลขสำหรับมิติการจัดโครงแบบตามหมายเลขผลิตภัณฑ์ย่อยแทน และคุณจะได้รับคำเตือน</span><span class="sxs-lookup"><span data-stu-id="a1a8b-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="a1a8b-238">เพื่อหลีกเลี่ยงสถานการณ์นี้ คุณควรรวมแอททริบิวต์ที่มากพอลงในระบบการตั้งชื่อเพื่อช่วยในการรับประกันหมายเลขผลิตภัณฑ์ย่อยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="a1a8b-239">คุณควรตรวจสอบให้แน่ใจว่าตัวเลือก **นำมาใช้ใหม่** เปิดอยู่สำหรับส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="a1a8b-240">การจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-240">Dimension-based configurations</span></span>

<span data-ttu-id="a1a8b-241">ในระหว่างขั้นตอนหนึ่งของกระบวนการจัดโครงแบบ ระบบจะแนะนำค่าการจัดโครงแบบตามระบบการตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="a1a8b-242">ในขั้นตอนนี้ คุณสามารถเปลี่ยนค่าการจัดโครงแบบด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a1a8b-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="a1a8b-243">เมื่อคุณบันทึกการจัดโครงแบบ ระบบจะตรวจสอบว่ามีค่าการจัดโครงแบบที่ซ้ำกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a1a8b-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="a1a8b-244">ถ้าค่าที่คุณป้อนไม่ใช่ค่าที่ไม่ซ้ำกัน คุณจะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a1a8b-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="a1a8b-245">เมื่อต้องการบันทึกการจัดโครงแบบ คุณต้องป้อนค่าการจัดโครงแบบที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="a1a8b-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="a1a8b-246">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="a1a8b-246">See also</span></span>
--------

[<span data-ttu-id="a1a8b-247">สร้างระบบการตั้งชื่อหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a1a8b-247">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="a1a8b-248">สร้างระบบการตั้งชื่อหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่มีการจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="a1a8b-248">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


