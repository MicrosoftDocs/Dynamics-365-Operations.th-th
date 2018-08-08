--- 
title: "สร้างผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า"
description: "กระบวนงานนี้จะแนะนำวิธีการสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก โดยใช้ชุดของมิติของผลิตภัณฑ์ "
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 2b9202c24b2c1511da6344df6b54326b4d3106c5
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="6b9ac-103">สร้างผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="6b9ac-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b9ac-104">กระบวนงานนี้จะแนะนำวิธีการสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก โดยใช้ชุดของมิติของผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="6b9ac-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="6b9ac-105">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="6b9ac-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="6b9ac-106">สร้างผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="6b9ac-106">Create a product master</span></span>
1. <span data-ttu-id="6b9ac-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="6b9ac-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="6b9ac-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-108">Click New.</span></span>
3. <span data-ttu-id="6b9ac-109">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b9ac-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="6b9ac-110">การป้อนหมายเลขผลิตภัณฑ์ด้วยตนเอง มีความจำเป็นเฉพาะเมื่อไม่มีการตั้งค่าลำดับหมายเลขสำหรับฟิลด์หมายเลขผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="6b9ac-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="6b9ac-111">กล่าวได้อีกอย่างหนึ่งว่า ให้ข้ามขั้นตอนนี้ ถ้ามีการตั้งค่าลำดับหมายเลขสำหรับฟิลด์</span><span class="sxs-lookup"><span data-stu-id="6b9ac-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="6b9ac-112">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b9ac-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="6b9ac-113">ในฟิลด์กลุ่มมิติของผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b9ac-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6b9ac-114">เลือก SizeCol ของกลุ่มมิติของผลิตภัณฑ์ (ขนาดและสี)</span><span class="sxs-lookup"><span data-stu-id="6b9ac-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="6b9ac-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="6b9ac-116">เพิ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6b9ac-116">Add product dimensions</span></span>
1. <span data-ttu-id="6b9ac-117">คลิกมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6b9ac-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="6b9ac-118">ตัวอย่างนี้แสดงวิธีการป้อนมิติของผลิตภัณฑ์ด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="6b9ac-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="6b9ac-119">คุณยังสามารถเลือกขนาด สี หรือกลุ่มลักษณะที่รวมค่ามิติของผลิตภัณฑ์ที่คุณต้องการใช้ได้</span><span class="sxs-lookup"><span data-stu-id="6b9ac-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="6b9ac-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-120">Click New.</span></span>
3. <span data-ttu-id="6b9ac-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6b9ac-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6b9ac-122">ในฟิลด์ขนาด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="6b9ac-123">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="6b9ac-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="6b9ac-124">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-124">Click New.</span></span>
7. <span data-ttu-id="6b9ac-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6b9ac-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="6b9ac-126">ในฟิลด์ขนาด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="6b9ac-127">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="6b9ac-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="6b9ac-128">คลิกแท็บสี</span><span class="sxs-lookup"><span data-stu-id="6b9ac-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="6b9ac-129">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-129">Click New.</span></span>
12. <span data-ttu-id="6b9ac-130">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6b9ac-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="6b9ac-131">ในฟิลด์สี ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="6b9ac-132">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="6b9ac-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="6b9ac-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-133">Click New.</span></span>
16. <span data-ttu-id="6b9ac-134">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6b9ac-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="6b9ac-135">ในฟิลด์สี ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="6b9ac-136">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="6b9ac-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="6b9ac-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6b9ac-137">Click Save.</span></span>
20. <span data-ttu-id="6b9ac-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6b9ac-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="6b9ac-139">สร้างผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="6b9ac-139">Generate product variants</span></span>
1. <span data-ttu-id="6b9ac-140">คลิกผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="6b9ac-140">Click Product variants.</span></span>
2. <span data-ttu-id="6b9ac-141">คำแนะนำผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="6b9ac-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="6b9ac-142">คลิกเลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6b9ac-142">Click Select all.</span></span>
    * <span data-ttu-id="6b9ac-143">ในตัวอย่างนี้ ตัวแปรที่เป็นไปได้ทั้งหมดจะถูกเลือก </span><span class="sxs-lookup"><span data-stu-id="6b9ac-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="6b9ac-144">ถ้าเฉพาะเซ็ตย่อยของชุดมิติของผลิตภัณฑ์ที่เป็นไปได้จะถูกใช้เพื่อสร้างตัวแปร คุณสามารถเลือกรายการแต่ละรายการได้</span><span class="sxs-lookup"><span data-stu-id="6b9ac-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="6b9ac-145">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b9ac-145">Click Create.</span></span>
    * <span data-ttu-id="6b9ac-146">คุณสามารถสร้างคำอธิบายสำหรับตัวแปรของคุณทั้งหมด ตามชุดของค่ามิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6b9ac-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="6b9ac-147"> ไม่จำเป็นต้องระบุคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6b9ac-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="6b9ac-148">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6b9ac-148">Click Save.</span></span>


