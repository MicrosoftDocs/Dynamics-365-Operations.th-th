--- 
title: "สร้างลำดับขั้นของการจัดประภทผลิตภัณฑ์"
description: "ขั้นตอนนี้แสดงวิธีการสร้างการจัดประเภทตามลำดับชั้นใหม่และกำหนดชนิดของลำดับชั้นรหัสสินค้า "
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 86f4627688e46f98895eda0a6f1a113742c215d9
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="0f7c6-103">สร้างลำดับขั้นของการจัดประภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0f7c6-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f7c6-104">ขั้นตอนนี้แสดงวิธีการสร้างการจัดประเภทตามลำดับชั้นใหม่และกำหนดชนิดของลำดับชั้นรหัสสินค้า </span><span class="sxs-lookup"><span data-stu-id="0f7c6-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="0f7c6-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="0f7c6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0f7c6-106">ขั้นตอนนี้มีไว้สำหรับผู้จัดการประเภท</span><span class="sxs-lookup"><span data-stu-id="0f7c6-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="0f7c6-107">สร้างการจัดประเภทตามลำดับชั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="0f7c6-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="0f7c6-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การตั้งค่า > ประเภทและคุณลักษณะ > การจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="0f7c6-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="0f7c6-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-109">Click New.</span></span>
3. <span data-ttu-id="0f7c6-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="0f7c6-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0f7c6-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0f7c6-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0f7c6-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="0f7c6-113">สร้างลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="0f7c6-113">Build the hierarchy</span></span>
1. <span data-ttu-id="0f7c6-114">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="0f7c6-114">Click New category node.</span></span>
2. <span data-ttu-id="0f7c6-115">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="0f7c6-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="0f7c6-116">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="0f7c6-117">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="0f7c6-118">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="0f7c6-118">Click New category node.</span></span>
6. <span data-ttu-id="0f7c6-119">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0f7c6-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="0f7c6-120">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="0f7c6-121">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="0f7c6-122">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="0f7c6-122">Click New category node.</span></span>
10. <span data-ttu-id="0f7c6-123">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0f7c6-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="0f7c6-124">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="0f7c6-125">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="0f7c6-126">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="0f7c6-126">Click New category node.</span></span>
14. <span data-ttu-id="0f7c6-127">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0f7c6-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="0f7c6-128">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="0f7c6-129">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="0f7c6-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0f7c6-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="0f7c6-131">จัดประเภทลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="0f7c6-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="0f7c6-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0f7c6-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="0f7c6-133">ในบานหน้าต่างการดำเนินการ คลิกการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="0f7c6-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="0f7c6-134">คลิกเชื่อมโยงชนิดลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="0f7c6-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="0f7c6-135">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0f7c6-135">Click New.</span></span>
5. <span data-ttu-id="0f7c6-136">ในฟิลด์ชนิดของการจัดประเภทตามลำดับชั้น ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0f7c6-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="0f7c6-137">เลือกชนิดของการจัดประเภทตามลำดับชั้นรหัสสินค้าที่ซื้อขายกันสำหรับการจัดประเภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0f7c6-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="0f7c6-138">ในฟิลด์การจัดประเภทตามลำดับชั้น ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0f7c6-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0f7c6-139">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0f7c6-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0f7c6-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0f7c6-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0f7c6-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0f7c6-141">Close the page.</span></span>


