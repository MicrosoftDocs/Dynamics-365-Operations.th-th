---
title: ศึกษาหรือแก้ไขข้อยกเว้น
description: 'นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกเรียกใช้เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย โดยการใช้หน้าใบแจ้งหนี้ของผู้จัดจำหน่ายและเมื่อคุณเปิดหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายในหน้าของการละเมิดนโยบาย '
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abc8dc112ab577ddcbd208f898a8d4e487bc2998
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827781"
---
# <a name="research-or-resolve-exceptions"></a><span data-ttu-id="decd0-103">ศึกษาหรือแก้ไขข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="decd0-103">Research or resolve exceptions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="decd0-104">นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกเรียกใช้เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย โดยการใช้หน้าใบแจ้งหนี้ของผู้จัดจำหน่ายและเมื่อคุณเปิดหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายในหน้าของการละเมิดนโยบาย </span><span class="sxs-lookup"><span data-stu-id="decd0-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="decd0-105">คุณยังสามารถกำหนดลำดับงานใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อเรียกใช้นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายได้ทุกครั้งที่คุณส่งใบแจ้งหนี้ไปที่ลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="decd0-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="decd0-106">นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายจะไม่ใช้กับใบแจ้งหนี้ที่สร้างไว้ในทะเบียนใบแจ้งหนี้หรือสมุดรายวันใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="decd0-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="decd0-107">การตรวจสอบการจับคู่ใบแจ้งหนี้ไม่ได้ใช้นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย แต่ถูกตั้งค่าในหน้าพารามิเตอร์เจ้าหนี้แทน </span><span class="sxs-lookup"><span data-stu-id="decd0-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="decd0-108">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="decd0-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="decd0-109">บทบาทของผู้จัดการฝ่ายบัญชีเจ้าหนี้หรือผู้จัดการฝ่ายบัญชีจะต้องดำเนินการขั้นตอนเหล่านี้ </span><span class="sxs-lookup"><span data-stu-id="decd0-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="decd0-110">ก่อนการเริ่มต้น ให้ตรวจสอบให้แน่ใจว่า มีเลือกคีย์การตั้งค่าคอนฟิกการจับคู่ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="decd0-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="decd0-111">เตรียมการสร้างนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="decd0-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="decd0-112">ไปที่บัญชีเจ้าหนี้ > การตั้งค่า > พารามิเตอร์บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="decd0-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="decd0-113">คลิกที่แท็บการตรวจสอบใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="decd0-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="decd0-114">เลือกหรือล้างกล่องกาเครื่องหมายสถานะที่หัวใบแจ้งหนี้ที่มีการอัพเดตอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="decd0-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="decd0-115">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="decd0-115">Click OK.</span></span>
5. <span data-ttu-id="decd0-116">ในฟิลด์ลงรายการบัญชีใบแจ้งหนี้ที่มีความขัดแย้ง ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="decd0-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="decd0-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="decd0-117">Close the page.</span></span>
7. <span data-ttu-id="decd0-118">ไปที่บัญชีเจ้าหนี้ > การตั้งค่านโยบาย > นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="decd0-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="decd0-119">คลิกที่พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="decd0-119">Click Parameters.</span></span>
9. <span data-ttu-id="decd0-120">คลิก btnAdd</span><span class="sxs-lookup"><span data-stu-id="decd0-120">Click btnAdd.</span></span>
10. <span data-ttu-id="decd0-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="decd0-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="decd0-122">สร้างชนิดของกฎนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="decd0-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="decd0-123">ไปที่บัญชีเจ้าหนี้ > การตั้งค่านโยบาย > ชนิดของกฎนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="decd0-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="decd0-124">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="decd0-124">Click New.</span></span>
3. <span data-ttu-id="decd0-125">ในฟิลด์ชื่อกฎ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="decd0-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="decd0-126">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="decd0-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="decd0-127">ในฟิลด์ชื่อการสอบถาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="decd0-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="decd0-128">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="decd0-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="decd0-129">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="decd0-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="decd0-130">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="decd0-130">Click Save.</span></span>
9. <span data-ttu-id="decd0-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="decd0-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="decd0-132">กำหนดนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="decd0-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="decd0-133">ไปที่บัญชีเจ้าหนี้ > การตั้งค่านโยบาย > นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="decd0-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="decd0-134">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="decd0-134">Click New.</span></span>
3. <span data-ttu-id="decd0-135">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="decd0-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="decd0-136">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="decd0-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="decd0-137">ขยายหรือยุบส่วนของนโยบายองค์กร</span><span class="sxs-lookup"><span data-stu-id="decd0-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="decd0-138">ในแผนภูมิ เลือก 'ระบบความบันเทิง Contoso USA'</span><span class="sxs-lookup"><span data-stu-id="decd0-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="decd0-139">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="decd0-139">Click Add.</span></span>
8. <span data-ttu-id="decd0-140">ขยายหรือยุบส่วนของกฎนโยบายองค์กร</span><span class="sxs-lookup"><span data-stu-id="decd0-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="decd0-141">คลิกสร้างกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="decd0-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="decd0-142">ในฟิลด์คำอธิบายกฎนโยบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="decd0-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="decd0-143">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="decd0-143">Click Filter.</span></span>
12. <span data-ttu-id="decd0-144">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="decd0-144">Click Add.</span></span>
13. <span data-ttu-id="decd0-145">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="decd0-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="decd0-146">ในฟิลด์ตาราง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="decd0-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="decd0-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="decd0-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="decd0-148">ในฟิลด์ตารางสืบทอด ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="decd0-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="decd0-149">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="decd0-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="decd0-150">ในฟิลด์ฟิลด์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="decd0-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="decd0-151">ในฟิลด์ฟิลด์ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="decd0-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="decd0-152">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="decd0-152">Close the page.</span></span>
21. <span data-ttu-id="decd0-153">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="decd0-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="decd0-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="decd0-154">Click OK.</span></span>
23. <span data-ttu-id="decd0-155">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="decd0-155">Click OK.</span></span>
24. <span data-ttu-id="decd0-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="decd0-156">Close the page.</span></span>
25. <span data-ttu-id="decd0-157">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="decd0-157">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]