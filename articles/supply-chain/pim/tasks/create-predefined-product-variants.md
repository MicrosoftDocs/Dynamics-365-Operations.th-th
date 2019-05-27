---
title: สร้างผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า
description: 'กระบวนงานนี้จะแนะนำวิธีการสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก โดยใช้ชุดของมิติของผลิตภัณฑ์ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4f43957f7c661349714dbb0933ac3c1d19ab0e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550663"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="e174b-103">สร้างผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="e174b-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e174b-104">กระบวนงานนี้จะแนะนำวิธีการสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก โดยใช้ชุดของมิติของผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="e174b-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="e174b-105">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e174b-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="e174b-106">สร้างผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="e174b-106">Create a product master</span></span>
1. <span data-ttu-id="e174b-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="e174b-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="e174b-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e174b-108">Click New.</span></span>
3. <span data-ttu-id="e174b-109">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e174b-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e174b-110">การป้อนหมายเลขผลิตภัณฑ์ด้วยตนเอง มีความจำเป็นเฉพาะเมื่อไม่มีการตั้งค่าลำดับหมายเลขสำหรับฟิลด์หมายเลขผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="e174b-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="e174b-111">กล่าวได้อีกอย่างหนึ่งว่า ให้ข้ามขั้นตอนนี้ ถ้ามีการตั้งค่าลำดับหมายเลขสำหรับฟิลด์</span><span class="sxs-lookup"><span data-stu-id="e174b-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="e174b-112">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e174b-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="e174b-113">ในฟิลด์กลุ่มมิติของผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e174b-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e174b-114">เลือก SizeCol ของกลุ่มมิติของผลิตภัณฑ์ (ขนาดและสี)</span><span class="sxs-lookup"><span data-stu-id="e174b-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="e174b-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e174b-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="e174b-116">เพิ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e174b-116">Add product dimensions</span></span>
1. <span data-ttu-id="e174b-117">คลิกมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e174b-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="e174b-118">ตัวอย่างนี้แสดงวิธีการป้อนมิติของผลิตภัณฑ์ด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="e174b-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="e174b-119">คุณยังสามารถเลือกขนาด สี หรือกลุ่มลักษณะที่รวมค่ามิติของผลิตภัณฑ์ที่คุณต้องการใช้ได้</span><span class="sxs-lookup"><span data-stu-id="e174b-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="e174b-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e174b-120">Click New.</span></span>
3. <span data-ttu-id="e174b-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e174b-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e174b-122">ในฟิลด์ขนาด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e174b-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="e174b-123">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e174b-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="e174b-124">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e174b-124">Click New.</span></span>
7. <span data-ttu-id="e174b-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e174b-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="e174b-126">ในฟิลด์ขนาด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e174b-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="e174b-127">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e174b-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="e174b-128">คลิกแท็บสี</span><span class="sxs-lookup"><span data-stu-id="e174b-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="e174b-129">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e174b-129">Click New.</span></span>
12. <span data-ttu-id="e174b-130">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e174b-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="e174b-131">ในฟิลด์สี ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e174b-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="e174b-132">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e174b-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="e174b-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e174b-133">Click New.</span></span>
16. <span data-ttu-id="e174b-134">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e174b-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="e174b-135">ในฟิลด์สี ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e174b-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="e174b-136">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e174b-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="e174b-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e174b-137">Click Save.</span></span>
20. <span data-ttu-id="e174b-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e174b-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="e174b-139">สร้างผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="e174b-139">Generate product variants</span></span>
1. <span data-ttu-id="e174b-140">คลิกผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="e174b-140">Click Product variants.</span></span>
2. <span data-ttu-id="e174b-141">คำแนะนำผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="e174b-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="e174b-142">คลิกเลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e174b-142">Click Select all.</span></span>
    * <span data-ttu-id="e174b-143">ในตัวอย่างนี้ ตัวแปรที่เป็นไปได้ทั้งหมดจะถูกเลือก </span><span class="sxs-lookup"><span data-stu-id="e174b-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="e174b-144">ถ้าเฉพาะเซ็ตย่อยของชุดมิติของผลิตภัณฑ์ที่เป็นไปได้จะถูกใช้เพื่อสร้างตัวแปร คุณสามารถเลือกรายการแต่ละรายการได้</span><span class="sxs-lookup"><span data-stu-id="e174b-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="e174b-145">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e174b-145">Click Create.</span></span>
    * <span data-ttu-id="e174b-146">คุณสามารถสร้างคำอธิบายสำหรับตัวแปรของคุณทั้งหมด ตามชุดของค่ามิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e174b-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="e174b-147"> ไม่จำเป็นต้องระบุคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e174b-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="e174b-148">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e174b-148">Click Save.</span></span>

