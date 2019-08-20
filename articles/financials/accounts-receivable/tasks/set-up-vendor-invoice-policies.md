---
title: ตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีการตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายใน Dynamics 365 for Finance and Operatoins
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 328aafd16496fdbb963c9aa40a5c13005be7a382
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842820"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="2c3f1-103">ตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c3f1-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c3f1-104">หัวข้อนี้อธิบายวิธีการตั้งค่านโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายใน Dynamics 365 for Finance and Operatoins</span><span class="sxs-lookup"><span data-stu-id="2c3f1-104">This topic explains how to set up vendor invoice policies in Dynamics 365 for Finance and Operatoins.</span></span> <span data-ttu-id="2c3f1-105">นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกเรียกใช้เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย โดยการใช้หน้าใบแจ้งหนี้ของผู้จัดจำหน่ายและเมื่อคุณเปิดหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายในหน้าของการละเมิดนโยบาย </span><span class="sxs-lookup"><span data-stu-id="2c3f1-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="2c3f1-106">คุณยังสามารถกำหนดลำดับงานใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อเรียกใช้นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายได้ทุกครั้งที่คุณส่งใบแจ้งหนี้ไปที่ลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="2c3f1-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="2c3f1-107">นโยบายใบแจ้งหนี้ของผู้จัดจำหน่ายจะไม่ใช้กับใบแจ้งหนี้ที่สร้างไว้ในทะเบียนใบแจ้งหนี้หรือสมุดรายวันใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="2c3f1-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="2c3f1-108">การตรวจสอบการจับคู่ใบแจ้งหนี้ไม่ได้ใช้นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย แต่ถูกตั้งค่าในหน้าพารามิเตอร์เจ้าหนี้แทน </span><span class="sxs-lookup"><span data-stu-id="2c3f1-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="2c3f1-109">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="2c3f1-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="2c3f1-110">บทบาทของผู้จัดการฝ่ายบัญชีเจ้าหนี้หรือผู้จัดการฝ่ายบัญชีจะต้องดำเนินการขั้นตอนเหล่านี้ </span><span class="sxs-lookup"><span data-stu-id="2c3f1-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="2c3f1-111">ก่อนการเริ่มต้น ให้ตรวจสอบให้แน่ใจว่า มีเลือกคีย์การตั้งค่าคอนฟิกการจับคู่ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="2c3f1-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="2c3f1-112">เตรียมการสร้างนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c3f1-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="2c3f1-113">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ > การตั้งค่า > พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="2c3f1-114">เลือกแท็บ **การตรวจสอบใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="2c3f1-115">เลือกหรือล้างกล่องกาเครื่องหมายสถานะ **ปรับปรุงส่วนหัวของใบแจ้งหนี้โดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="2c3f1-116">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-116">Select **OK**.</span></span>
5. <span data-ttu-id="2c3f1-117">ในฟิลด์ **ลงรายการบัญชีใบแจ้งหนี้ที่มีความขัดแย้ง** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2c3f1-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="2c3f1-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c3f1-118">Close the page.</span></span>
7. <span data-ttu-id="2c3f1-119">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ >การตั้งค่านโยบาย >นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="2c3f1-120">เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="2c3f1-121">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-121">Select **Add**.</span></span>
10. <span data-ttu-id="2c3f1-122">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="2c3f1-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="2c3f1-123">สร้างชนิดของกฎนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c3f1-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="2c3f1-124">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ >การตั้งค่านโยบาย > ชนิดกฎนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="2c3f1-125">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-125">Select **New**.</span></span>
3. <span data-ttu-id="2c3f1-126">ในฟิลด์ **ชื่อกฎ** และ **คำอธิบาย** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2c3f1-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="2c3f1-127">ในฟิลด์ **ชื่อของแบบสอบถาม** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา จากนั้น เลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c3f1-127">In the **Query name** field, select the drop-down button to open the lookup, then selec the desired record.</span></span>
5. <span data-ttu-id="2c3f1-128">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-128">Select **Save**.</span></span>
6. <span data-ttu-id="2c3f1-129">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="2c3f1-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="2c3f1-130">กำหนดนโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2c3f1-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="2c3f1-131">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ >การตั้งค่านโยบาย >นโยบายใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="2c3f1-132">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-132">Select **New**.</span></span>
3. <span data-ttu-id="2c3f1-133">ในฟิลด์ **ชื่อ** และ **คำอธิบาย** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2c3f1-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="2c3f1-134">ขยายหรือยุบส่วน **นโยบายองค์กร**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="2c3f1-135">ในแผนภูมิ เลือก **Contoso Entertainment System USA**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="2c3f1-136">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-136">Select **Add**.</span></span>
7. <span data-ttu-id="2c3f1-137">ขยายหรือยุบส่วน **กฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="2c3f1-138">เลือก **สร้างกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="2c3f1-139">ในฟิลด์ **คำอธิบายกฎนโยบาย** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2c3f1-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="2c3f1-140">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-140">Select **Filter**.</span></span>
11. <span data-ttu-id="2c3f1-141">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-141">Select **Add**.</span></span> <span data-ttu-id="2c3f1-142">เลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c3f1-142">Select the desired record.</span></span>
12. <span data-ttu-id="2c3f1-143">ในฟิลด์ **ตาราง** **ตารางสืบทอด** และ **ฟิลด์** ให้เลือกหรือป้อนตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="2c3f1-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="2c3f1-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c3f1-144">Close the page.</span></span>
14. <span data-ttu-id="2c3f1-145">ในฟิลด์ **เงื่อนไข** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2c3f1-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="2c3f1-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-146">Select **OK**.</span></span>
16. <span data-ttu-id="2c3f1-147">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2c3f1-147">Select **OK**.</span></span>
17. <span data-ttu-id="2c3f1-148">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="2c3f1-148">Close the pages to return to the home page.</span></span>

