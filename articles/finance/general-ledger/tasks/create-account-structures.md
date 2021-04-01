---
title: สร้างโครงสร้างทางบัญชี
description: 'คำแนะนำงานนี้ระบุขั้นตอนการสร้างโครงสร้างทางบัญชี '
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8ce37ab642277ff843e6320a880fac40d41acb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235800"
---
# <a name="create-account-structures"></a><span data-ttu-id="3cf31-103">สร้างโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="3cf31-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cf31-104">คำแนะนำงานนี้ระบุขั้นตอนการสร้างโครงสร้างทางบัญชี </span><span class="sxs-lookup"><span data-stu-id="3cf31-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="3cf31-105">ขั้นตอนเหล่านี้ใช้ข้อมูลสาธิตบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="3cf31-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="3cf31-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > ตั้งค่าคอนฟิกโครงสร้างทางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="3cf31-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="3cf31-107">บน **บานหน้าต่างนำทาง** คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="3cf31-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="3cf31-108">ในฟิลด์ **โครงสร้างทางบัญชี** ให้พิมพ์ชื่อเพื่ออธิบายถึงวัตถุประสงค์ของโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="3cf31-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="3cf31-109">ในฟิลด์ **คำอธิบาย** ให้พิมพ์คำอธิบายเพื่อระบุวัตถุประสงค์ของโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="3cf31-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="3cf31-110">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="3cf31-110">Click **Create**.</span></span>
6. <span data-ttu-id="3cf31-111">ใน **เซ็กเมนต์และมูลค่าที่อนุญาต** ให้คลิก **เพิ่มเซ็กเมนต์**</span><span class="sxs-lookup"><span data-stu-id="3cf31-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="3cf31-112">ในมิติ ให้เลือกมิติเพื่อเพิ่มโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="3cf31-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="3cf31-113">เมื่อสิ้นสุดของรายการ คลิก **เพิ่มเซ็กเมนต์**</span><span class="sxs-lookup"><span data-stu-id="3cf31-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="3cf31-114">ทำซ้ำขั้นตอนที่ 6 ถึง 9 ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="3cf31-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="3cf31-115">ในส่วน **รายละเอียดค่าที่อนุญาต** ให้เลือกเซกเมนต์ที่จะแก้ไขค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="3cf31-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="3cf31-116">ตัวอย่างเช่น คลิกฟิลด์ **บัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="3cf31-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="3cf31-117">ในฟิลด์ **ผู้ปฏิบัติงาน** ให้เลือกตัวเลือก เช่น อยู่ระหว่าง และ รวม</span><span class="sxs-lookup"><span data-stu-id="3cf31-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="3cf31-118">ในฟิลด์ **ค่า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="3cf31-119">ตัวอย่างเช่น 600000</span><span class="sxs-lookup"><span data-stu-id="3cf31-119">For example, 600000.</span></span>  
13. <span data-ttu-id="3cf31-120">ในฟิลด์ **ผ่าน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-120">In the **through** field, type a value.</span></span> <span data-ttu-id="3cf31-121">ตัวอย่างเช่น 699999</span><span class="sxs-lookup"><span data-stu-id="3cf31-121">For example, 699999.</span></span>  
14. <span data-ttu-id="3cf31-122">ในส่วน **รายละเอียดของมูลค่าที่อนุญาต** คลิก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="3cf31-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="3cf31-123">ทำซ้ำขั้นตอนที่ 10 ถึง 15 ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="3cf31-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="3cf31-124">ในส่วน **รายละเอียดของมูลค่าที่อนุญาต** คลิก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="3cf31-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="3cf31-125">ในฟิลด์ผู้ปฏิบัติงาน ให้เลือกตัวเลือก เช่น อยู่ระหว่าง และ รวม</span><span class="sxs-lookup"><span data-stu-id="3cf31-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="3cf31-126">ในฟิลด์ **ค่า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="3cf31-127">ตัวอย่างเช่น 033</span><span class="sxs-lookup"><span data-stu-id="3cf31-127">For example, 033.</span></span>  
19. <span data-ttu-id="3cf31-128">ในฟิลด์ **ผ่าน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-128">In the **through** field, type a value.</span></span> <span data-ttu-id="3cf31-129">ตัวอย่างเช่น 034</span><span class="sxs-lookup"><span data-stu-id="3cf31-129">For example, 034.</span></span>  
20. <span data-ttu-id="3cf31-130">คลิก **ใช้**</span><span class="sxs-lookup"><span data-stu-id="3cf31-130">Click **Apply**.</span></span>
21. <span data-ttu-id="3cf31-131">ในกริด ให้เลือกเซกเมนต์ที่จะแก้ไขค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="3cf31-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="3cf31-132">ตัวอย่างเช่น ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="3cf31-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="3cf31-133">ใน **ฟิลด์ CostCenter** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="3cf31-134">ตัวอย่างเช่น 007..021</span><span class="sxs-lookup"><span data-stu-id="3cf31-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="3cf31-135">ใน **เซ็กเมนต์และมูลค่าที่อนุญาต** ให้คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3cf31-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="3cf31-136">ในฟิลด์ **MainAccount** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="3cf31-137">ตัวอย่างเช่น 600000..699999</span><span class="sxs-lookup"><span data-stu-id="3cf31-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="3cf31-138">ในกริด ให้เลือกเซกเมนต์ที่จะแก้ไขค่าที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="3cf31-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="3cf31-139">ตัวอย่างเช่น แผนก</span><span class="sxs-lookup"><span data-stu-id="3cf31-139">For example, Department.</span></span>  
26. <span data-ttu-id="3cf31-140">ในฟิลด์แผนก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-140">In the Department field, type a value.</span></span> <span data-ttu-id="3cf31-141">ตัวอย่างเช่น 032</span><span class="sxs-lookup"><span data-stu-id="3cf31-141">For example, 032.</span></span>  
27. <span data-ttu-id="3cf31-142">ในฟิลด์ศูนย์ต้นทุน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3cf31-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="3cf31-143">ตัวอย่างเช่น 086</span><span class="sxs-lookup"><span data-stu-id="3cf31-143">For example, 086.</span></span>  
28. <span data-ttu-id="3cf31-144">บน **บานหน้าต่างการดำเนินการ** คลิก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="3cf31-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="3cf31-145">บน **บานหน้าต่างการดำเนินการ** คลิก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="3cf31-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="3cf31-146">คลิก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="3cf31-146">Click **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]