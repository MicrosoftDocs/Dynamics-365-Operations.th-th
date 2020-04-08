---
title: สร้างลำดับขั้นของการจัดประภทผลิตภัณฑ์
description: 'ขั้นตอนนี้แสดงวิธีการสร้างการจัดประเภทตามลำดับชั้นใหม่และกำหนดชนิดของลำดับชั้นรหัสสินค้า '
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ac87356f46edc118a592acd393823603815917a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150134"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="f367a-103">สร้างลำดับขั้นของการจัดประภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f367a-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f367a-104">ขั้นตอนนี้แสดงวิธีการสร้างการจัดประเภทตามลำดับชั้นใหม่และกำหนดชนิดของลำดับชั้นรหัสสินค้า </span><span class="sxs-lookup"><span data-stu-id="f367a-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="f367a-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="f367a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f367a-106">ขั้นตอนนี้มีไว้สำหรับผู้จัดการประเภท</span><span class="sxs-lookup"><span data-stu-id="f367a-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="f367a-107">สร้างการจัดประเภทตามลำดับชั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="f367a-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="f367a-108">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ > การตั้งค่า > ประเภทและแอททริบิวต์ > การจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="f367a-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="f367a-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f367a-109">Click **New**.</span></span>
3. <span data-ttu-id="f367a-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f367a-111">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f367a-112">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f367a-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="f367a-113">สร้างลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f367a-113">Build the hierarchy</span></span>
1. <span data-ttu-id="f367a-114">คลิกโหนดประเภท **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f367a-114">Click **New** category node.</span></span>
2. <span data-ttu-id="f367a-115">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="f367a-116">ในฟิลด์ **รหัส** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="f367a-117">ในฟิลด์ **ชื่อที่จำง่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="f367a-118">คลิกโหนดประเภท **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f367a-118">Click **New** category node.</span></span>
6. <span data-ttu-id="f367a-119">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="f367a-120">ในฟิลด์ **รหัส** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="f367a-121">ในฟิลด์ **ชื่อที่จำง่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="f367a-122">คลิกโหนดประเภท **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f367a-122">Click **New** category node.</span></span>
10. <span data-ttu-id="f367a-123">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="f367a-124">ในฟิลด์ **รหัส** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="f367a-125">ในฟิลด์ **ชื่อที่จำง่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="f367a-126">คลิกโหนดประเภท **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f367a-126">Click **New** category node.</span></span>
14. <span data-ttu-id="f367a-127">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="f367a-128">ในฟิลด์ **รหัส** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="f367a-129">ในฟิลด์ **ชื่อที่จำง่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f367a-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="f367a-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f367a-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="f367a-131">จัดประเภทลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f367a-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="f367a-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f367a-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f367a-133">ใน **บานหน้าต่างการดำเนินการ** คลิก **การจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="f367a-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="f367a-134">คลิก **เชื่อมโยงชนิดลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="f367a-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="f367a-135">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f367a-135">Click **New**.</span></span>
5. <span data-ttu-id="f367a-136">ในฟิลด์ **ชนิดของการจัดประเภทตามลำดับชั้น** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f367a-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="f367a-137">เลือก **ชนิดของการจัดประเภทตามลำดับชั้นรหัสโภคภัณฑ์สำหรับการจัดประเภทผลิตภัณฑ์โภคภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="f367a-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="f367a-138">ในฟิลด์ **การจัดประเภทตามลำดับชั้น** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f367a-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f367a-139">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f367a-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f367a-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f367a-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f367a-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f367a-141">Close the page.</span></span>

