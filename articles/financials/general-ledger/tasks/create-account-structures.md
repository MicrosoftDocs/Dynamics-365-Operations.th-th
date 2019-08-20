---
title: สร้างโครงสร้างทางบัญชี
description: 'คำแนะนำงานนี้ระบุขั้นตอนการสร้างโครงสร้างทางบัญชี '
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2183f88356fc8094781af147bf079c4e53ffb2b4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846714"
---
# <a name="create-account-structures"></a><span data-ttu-id="e3713-103">สร้างโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e3713-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3713-104">คำแนะนำงานนี้ระบุขั้นตอนการสร้างโครงสร้างทางบัญชี </span><span class="sxs-lookup"><span data-stu-id="e3713-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="e3713-105">ขั้นตอนเหล่านี้ใช้ข้อมูลสาธิตบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="e3713-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="e3713-106">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > ตั้งค่าคอนฟิกโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e3713-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="e3713-107">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e3713-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="e3713-108">ในฟิลด์โครงสร้างทางบัญชี ให้พิมพ์ชื่ออธิบายถึงวัตถุประสงค์ของโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e3713-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="e3713-109">ในฟิลด์คำอธิบาย ให้พิมพ์คำอธิบายระบุวัตถุประสงค์ของโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e3713-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="e3713-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e3713-110">Click Create.</span></span>
6. <span data-ttu-id="e3713-111">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="e3713-111">Click Add segment.</span></span>
7. <span data-ttu-id="e3713-112">ในรายการมิติ ให้เลือกมิติเพื่อเพิ่มโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e3713-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="e3713-113">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="e3713-113">Click Add segment.</span></span>
9. <span data-ttu-id="e3713-114">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="e3713-114">Click Add segment.</span></span>
10. <span data-ttu-id="e3713-115">ในรายการมิติ ให้เลือกมิติเพื่อเพิ่มโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e3713-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="e3713-116">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="e3713-116">Click Add segment.</span></span>
12. <span data-ttu-id="e3713-117">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="e3713-117">Click Add segment.</span></span>
13. <span data-ttu-id="e3713-118">ในรายการมิติ ให้เลือกมิติเพื่อเพิ่มโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e3713-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="e3713-119">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="e3713-119">Click Add segment.</span></span>
15. <span data-ttu-id="e3713-120">ในกริด ให้เลือกเซกเมนต์ที่จะแก้ไขค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="e3713-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e3713-121">ตัวอย่างเช่น คลิกในบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="e3713-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="e3713-122">ในฟิลด์ผู้ปฏิบัติงาน ให้เลือกตัวเลือก เช่น อยู่ระหว่าง และ รวม</span><span class="sxs-lookup"><span data-stu-id="e3713-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="e3713-123">ในฟิลด์ค่า ให้พิมพ์ค่าใดค่าหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="e3713-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e3713-124">ตัวอย่างเช่น 600000</span><span class="sxs-lookup"><span data-stu-id="e3713-124">For example, 600000.</span></span>  
18. <span data-ttu-id="e3713-125">ในฟิลด์ผ่าน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3713-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="e3713-126">ตัวอย่างเช่น 699999</span><span class="sxs-lookup"><span data-stu-id="e3713-126">For example, 699999.</span></span>  
19. <span data-ttu-id="e3713-127">คลิก ใช้</span><span class="sxs-lookup"><span data-stu-id="e3713-127">Click Apply.</span></span>
20. <span data-ttu-id="e3713-128">ในกริด ให้เลือกเซกเมนต์ที่จะแก้ไขค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="e3713-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e3713-129">ตัวอย่างเช่น แผนก</span><span class="sxs-lookup"><span data-stu-id="e3713-129">For example, Department.</span></span>  
21. <span data-ttu-id="e3713-130">ในฟิลด์ผู้ปฏิบัติงาน ให้เลือกตัวเลือก เช่น อยู่ระหว่าง และ รวม</span><span class="sxs-lookup"><span data-stu-id="e3713-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="e3713-131">ในฟิลด์ค่า ให้พิมพ์ค่าใดค่าหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="e3713-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e3713-132">ตัวอย่างเช่น 022</span><span class="sxs-lookup"><span data-stu-id="e3713-132">For example, 022.</span></span>  
23. <span data-ttu-id="e3713-133">ในฟิลด์ผ่าน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3713-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="e3713-134">ตัวอย่างเช่น 031</span><span class="sxs-lookup"><span data-stu-id="e3713-134">For example, 031.</span></span>  
24. <span data-ttu-id="e3713-135">คลิก เพิ่มเกณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="e3713-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="e3713-136">ในฟิลด์ผู้ปฏิบัติงาน ให้เลือกตัวเลือก เช่น อยู่ระหว่าง และ รวม</span><span class="sxs-lookup"><span data-stu-id="e3713-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="e3713-137">ในฟิลด์ค่า ให้พิมพ์ค่าใดค่าหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="e3713-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e3713-138">ตัวอย่างเช่น 033</span><span class="sxs-lookup"><span data-stu-id="e3713-138">For example, 033.</span></span>  
27. <span data-ttu-id="e3713-139">ในฟิลด์ผ่าน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3713-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="e3713-140">ตัวอย่างเช่น 034</span><span class="sxs-lookup"><span data-stu-id="e3713-140">For example, 034.</span></span>  
28. <span data-ttu-id="e3713-141">คลิก ใช้</span><span class="sxs-lookup"><span data-stu-id="e3713-141">Click Apply.</span></span>
29. <span data-ttu-id="e3713-142">ในกริด ให้เลือกเซกเมนต์ที่จะแก้ไขค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="e3713-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e3713-143">ตัวอย่างเช่น ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e3713-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="e3713-144">ในฟิลด์ศูนย์ต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3713-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="e3713-145">ตัวอย่างเช่น 007..021</span><span class="sxs-lookup"><span data-stu-id="e3713-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="e3713-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e3713-146">Click Add.</span></span>
32. <span data-ttu-id="e3713-147">ในฟิลด์บัญชีหลัก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3713-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="e3713-148">ตัวอย่างเช่น 600000..699999</span><span class="sxs-lookup"><span data-stu-id="e3713-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="e3713-149">ในกริด ให้เลือกเซกเมนต์ที่จะแก้ไขค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="e3713-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e3713-150">ตัวอย่างเช่น แผนก</span><span class="sxs-lookup"><span data-stu-id="e3713-150">For example, Department.</span></span>  
34. <span data-ttu-id="e3713-151">ในฟิลด์แผนก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3713-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="e3713-152">ตัวอย่างเช่น 032</span><span class="sxs-lookup"><span data-stu-id="e3713-152">For example, 032.</span></span>  
35. <span data-ttu-id="e3713-153">ในฟิลด์ศูนย์ต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3713-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="e3713-154">ตัวอย่างเช่น 086</span><span class="sxs-lookup"><span data-stu-id="e3713-154">For example, 086.</span></span>  
36. <span data-ttu-id="e3713-155">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e3713-155">Click Validate.</span></span>
37. <span data-ttu-id="e3713-156">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="e3713-156">Click Activate.</span></span>
38. <span data-ttu-id="e3713-157">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="e3713-157">Click Activate.</span></span>

