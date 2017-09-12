--- 
title: "สร้างหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า"
description: "คู่มือนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม "
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="71c8c-103">สร้างหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="71c8c-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71c8c-104">คู่มือนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม </span><span class="sxs-lookup"><span data-stu-id="71c8c-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="71c8c-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="71c8c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="71c8c-106">ระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ใหม่ถูกกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์สีและขนาด </span><span class="sxs-lookup"><span data-stu-id="71c8c-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="71c8c-107">โดยทั่วไปงานนี้อาจดำเนินการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="71c8c-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="71c8c-108">สร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="71c8c-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="71c8c-109">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="71c8c-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="71c8c-110">คลิก ระบบการตั้งชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="71c8c-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="71c8c-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="71c8c-111">Click New.</span></span>
4. <span data-ttu-id="71c8c-112">ในฟิลด์ชื่อ ป้อนชื่อระบบการตั้งชื่อที่ช่วยในการระบุเป้าหมายกลุ่มมิติของผลิตภัณฑ์ ตัวอย่างเช่น ColorSize</span><span class="sxs-lookup"><span data-stu-id="71c8c-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="71c8c-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="71c8c-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="71c8c-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="71c8c-114">Click Add.</span></span>
7. <span data-ttu-id="71c8c-115">คลิก หมายเลขผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="71c8c-115">Click Product master number.</span></span>
8. <span data-ttu-id="71c8c-116">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="71c8c-116">Click Add.</span></span>
9. <span data-ttu-id="71c8c-117">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="71c8c-117">Click Text constant.</span></span>
10. <span data-ttu-id="71c8c-118">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="71c8c-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="71c8c-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="71c8c-119">Click Add.</span></span>
12. <span data-ttu-id="71c8c-120">คลิก สี</span><span class="sxs-lookup"><span data-stu-id="71c8c-120">Click Color.</span></span>
13. <span data-ttu-id="71c8c-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="71c8c-121">Click Add.</span></span>
14. <span data-ttu-id="71c8c-122">คลิก ค่าคงที่ของข้อความ</span><span class="sxs-lookup"><span data-stu-id="71c8c-122">Click Text constant.</span></span>
15. <span data-ttu-id="71c8c-123">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="71c8c-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="71c8c-124">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="71c8c-124">Click Add.</span></span>
17. <span data-ttu-id="71c8c-125">คลิก ขนาด</span><span class="sxs-lookup"><span data-stu-id="71c8c-125">Click Size.</span></span>
18. <span data-ttu-id="71c8c-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="71c8c-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="71c8c-127">กำหนดระบบการตั้งชื่อให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="71c8c-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="71c8c-128">คลิก กลุ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="71c8c-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="71c8c-129">เลือกกลุ่มมิติของผลิตภัณฑ์ SizeCol</span><span class="sxs-lookup"><span data-stu-id="71c8c-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="71c8c-130">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="71c8c-130">Click Edit.</span></span>
4. <span data-ttu-id="71c8c-131">เลือก ใช่ ในฟิลด์ใช้ระบบการตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="71c8c-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="71c8c-132">ในฟิลด์ ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="71c8c-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="71c8c-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="71c8c-133">Close the page.</span></span>


