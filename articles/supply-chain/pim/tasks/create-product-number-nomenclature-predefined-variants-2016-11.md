---
title: สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า
description: 'คู่มือนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "364890"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="e7e07-103">สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="e7e07-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7e07-104">คู่มือนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม </span><span class="sxs-lookup"><span data-stu-id="e7e07-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="e7e07-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e7e07-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e7e07-106">ระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ใหม่ถูกกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์สีและขนาด </span><span class="sxs-lookup"><span data-stu-id="e7e07-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="e7e07-107">โดยทั่วไปงานนี้อาจดำเนินการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7e07-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="e7e07-108">สร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7e07-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="e7e07-109">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="e7e07-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e7e07-110">คลิก ระบบการตั้งชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7e07-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="e7e07-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e7e07-111">Click New.</span></span>
4. <span data-ttu-id="e7e07-112">ในฟิลด์ชื่อ ป้อนชื่อระบบการตั้งชื่อที่ช่วยในการระบุเป้าหมายกลุ่มมิติของผลิตภัณฑ์ ตัวอย่างเช่น ColorSize</span><span class="sxs-lookup"><span data-stu-id="e7e07-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="e7e07-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7e07-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e7e07-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e7e07-114">Click Add.</span></span>
7. <span data-ttu-id="e7e07-115">คลิก หมายเลขผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="e7e07-115">Click Product master number.</span></span>
8. <span data-ttu-id="e7e07-116">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e7e07-116">Click Add.</span></span>
9. <span data-ttu-id="e7e07-117">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="e7e07-117">Click Text constant.</span></span>
10. <span data-ttu-id="e7e07-118">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e7e07-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="e7e07-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e7e07-119">Click Add.</span></span>
12. <span data-ttu-id="e7e07-120">คลิก สี</span><span class="sxs-lookup"><span data-stu-id="e7e07-120">Click Color.</span></span>
13. <span data-ttu-id="e7e07-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e7e07-121">Click Add.</span></span>
14. <span data-ttu-id="e7e07-122">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="e7e07-122">Click Text constant.</span></span>
15. <span data-ttu-id="e7e07-123">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e7e07-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="e7e07-124">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e7e07-124">Click Add.</span></span>
17. <span data-ttu-id="e7e07-125">คลิก ขนาด</span><span class="sxs-lookup"><span data-stu-id="e7e07-125">Click Size.</span></span>
18. <span data-ttu-id="e7e07-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e7e07-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="e7e07-127">กำหนดระบบการตั้งชื่อให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="e7e07-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="e7e07-128">คลิก กลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7e07-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="e7e07-129">เลือกกลุ่มมิติของผลิตภัณฑ์ SizeCol</span><span class="sxs-lookup"><span data-stu-id="e7e07-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="e7e07-130">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="e7e07-130">Click Edit.</span></span>
4. <span data-ttu-id="e7e07-131">เลือก ใช่ ในฟิลด์ใช้ระบบการตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="e7e07-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="e7e07-132">ในฟิลด์ ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7e07-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="e7e07-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e7e07-133">Close the page.</span></span>

