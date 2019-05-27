---
title: สร้างลำดับขั้นของการจัดประภทผลิตภัณฑ์
description: 'ขั้นตอนนี้แสดงวิธีการสร้างการจัดประเภทตามลำดับชั้นใหม่และกำหนดชนิดของลำดับชั้นรหัสสินค้า '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568431"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="63d73-103">สร้างลำดับขั้นของการจัดประภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="63d73-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63d73-104">ขั้นตอนนี้แสดงวิธีการสร้างการจัดประเภทตามลำดับชั้นใหม่และกำหนดชนิดของลำดับชั้นรหัสสินค้า </span><span class="sxs-lookup"><span data-stu-id="63d73-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="63d73-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="63d73-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="63d73-106">ขั้นตอนนี้มีไว้สำหรับผู้จัดการประเภท</span><span class="sxs-lookup"><span data-stu-id="63d73-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="63d73-107">สร้างการจัดประเภทตามลำดับชั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="63d73-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="63d73-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การตั้งค่า > ประเภทและคุณลักษณะ > การจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="63d73-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="63d73-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="63d73-109">Click New.</span></span>
3. <span data-ttu-id="63d73-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="63d73-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="63d73-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="63d73-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="63d73-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="63d73-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="63d73-113">สร้างลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="63d73-113">Build the hierarchy</span></span>
1. <span data-ttu-id="63d73-114">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="63d73-114">Click New category node.</span></span>
2. <span data-ttu-id="63d73-115">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="63d73-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="63d73-116">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="63d73-117">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="63d73-118">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="63d73-118">Click New category node.</span></span>
6. <span data-ttu-id="63d73-119">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="63d73-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="63d73-120">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="63d73-121">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="63d73-122">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="63d73-122">Click New category node.</span></span>
10. <span data-ttu-id="63d73-123">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="63d73-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="63d73-124">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="63d73-125">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="63d73-126">คลิกโหนดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="63d73-126">Click New category node.</span></span>
14. <span data-ttu-id="63d73-127">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="63d73-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="63d73-128">ในฟิลด์รหัส ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="63d73-129">ในฟิลด์ชื่อที่จำง่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="63d73-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="63d73-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="63d73-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="63d73-131">จัดประเภทลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="63d73-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="63d73-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="63d73-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="63d73-133">ในบานหน้าต่างการดำเนินการ คลิกการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="63d73-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="63d73-134">คลิกเชื่อมโยงชนิดลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="63d73-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="63d73-135">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="63d73-135">Click New.</span></span>
5. <span data-ttu-id="63d73-136">ในฟิลด์ชนิดของการจัดประเภทตามลำดับชั้น ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="63d73-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="63d73-137">เลือกชนิดของการจัดประเภทตามลำดับชั้นรหัสสินค้าที่ซื้อขายกันสำหรับการจัดประเภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="63d73-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="63d73-138">ในฟิลด์การจัดประเภทตามลำดับชั้น ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="63d73-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="63d73-139">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="63d73-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="63d73-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="63d73-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="63d73-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="63d73-141">Close the page.</span></span>

