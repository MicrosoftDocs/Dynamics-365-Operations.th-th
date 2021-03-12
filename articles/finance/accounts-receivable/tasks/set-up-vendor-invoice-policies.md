---
title: ตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79cbabba74fdb76d8fcc0553d39e0f140aacf03e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995473"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="d8434-103">ตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="d8434-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8434-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="d8434-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="d8434-105">นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกเรียกใช้เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย โดยการใช้หน้าใบแจ้งหนี้ของผู้จัดจำหน่ายและเมื่อคุณเปิดหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายในหน้าของการละเมิดนโยบาย </span><span class="sxs-lookup"><span data-stu-id="d8434-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="d8434-106">คุณยังสามารถกำหนดลำดับงานใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อเรียกใช้นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายได้ทุกครั้งที่คุณส่งใบแจ้งหนี้ไปที่ลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="d8434-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="d8434-107">นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายจะไม่ใช้กับใบแจ้งหนี้ที่สร้างไว้ในทะเบียนใบแจ้งหนี้หรือสมุดรายวันใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="d8434-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="d8434-108">การตรวจสอบการจับคู่ใบแจ้งหนี้ไม่ได้ใช้นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย แต่ถูกตั้งค่าในหน้าพารามิเตอร์เจ้าหนี้แทน </span><span class="sxs-lookup"><span data-stu-id="d8434-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="d8434-109">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="d8434-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="d8434-110">บทบาทของผู้จัดการฝ่ายบัญชีเจ้าหนี้หรือผู้จัดการฝ่ายบัญชีจะต้องดำเนินการขั้นตอนเหล่านี้ </span><span class="sxs-lookup"><span data-stu-id="d8434-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="d8434-111">ก่อนการเริ่มต้น ให้ตรวจสอบให้แน่ใจว่า มีเลือกคีย์การตั้งค่าคอนฟิกการจับคู่ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="d8434-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="d8434-112">เตรียมการสร้างนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="d8434-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="d8434-113">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ > การตั้งค่า > พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="d8434-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="d8434-114">เลือกแท็บ **การตรวจสอบใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="d8434-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="d8434-115">เลือกหรือล้างกล่องกาเครื่องหมายสถานะ **ปรับปรุงส่วนหัวของใบแจ้งหนี้โดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="d8434-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="d8434-116">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d8434-116">Select **OK**.</span></span>
5. <span data-ttu-id="d8434-117">ในฟิลด์ **ลงรายการบัญชีใบแจ้งหนี้ที่มีความขัดแย้ง** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d8434-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="d8434-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d8434-118">Close the page.</span></span>
7. <span data-ttu-id="d8434-119">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ >การตั้งค่านโยบาย >นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="d8434-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="d8434-120">เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="d8434-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="d8434-121">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d8434-121">Select **Add**.</span></span>
10. <span data-ttu-id="d8434-122">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="d8434-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="d8434-123">สร้างชนิดของกฎนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="d8434-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="d8434-124">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ >การตั้งค่านโยบาย > ชนิดกฎนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="d8434-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="d8434-125">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d8434-125">Select **New**.</span></span>
3. <span data-ttu-id="d8434-126">ในฟิลด์ **ชื่อกฎ** และ **คำอธิบาย** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d8434-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d8434-127">ในฟิลด์ **ชื่อของแบบสอบถาม** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา จากนั้น เลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d8434-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="d8434-128">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d8434-128">Select **Save**.</span></span>
6. <span data-ttu-id="d8434-129">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="d8434-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="d8434-130">กำหนดนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="d8434-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="d8434-131">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ >การตั้งค่านโยบาย >นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="d8434-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="d8434-132">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d8434-132">Select **New**.</span></span>
3. <span data-ttu-id="d8434-133">ในฟิลด์ **ชื่อ** และ **คำอธิบาย** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d8434-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d8434-134">ขยายหรือยุบส่วน **นโยบายองค์กร**</span><span class="sxs-lookup"><span data-stu-id="d8434-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="d8434-135">ในแผนภูมิ เลือก **Contoso Entertainment System USA**</span><span class="sxs-lookup"><span data-stu-id="d8434-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="d8434-136">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d8434-136">Select **Add**.</span></span>
7. <span data-ttu-id="d8434-137">ขยายหรือยุบส่วน **กฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="d8434-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="d8434-138">เลือก **สร้างกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="d8434-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="d8434-139">ในฟิลด์ **คำอธิบายกฎนโยบาย** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d8434-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="d8434-140">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="d8434-140">Select **Filter**.</span></span>
11. <span data-ttu-id="d8434-141">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d8434-141">Select **Add**.</span></span> <span data-ttu-id="d8434-142">เลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d8434-142">Select the desired record.</span></span>
12. <span data-ttu-id="d8434-143">ในฟิลด์ **ตาราง** **ตารางสืบทอด** และ **ฟิลด์** ให้เลือกหรือป้อนตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="d8434-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="d8434-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d8434-144">Close the page.</span></span>
14. <span data-ttu-id="d8434-145">ในฟิลด์ **เงื่อนไข** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d8434-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="d8434-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d8434-146">Select **OK**.</span></span>
16. <span data-ttu-id="d8434-147">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d8434-147">Select **OK**.</span></span>
17. <span data-ttu-id="d8434-148">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="d8434-148">Close the pages to return to the home page.</span></span>

