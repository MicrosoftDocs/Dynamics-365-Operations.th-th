---
title: สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่ตั้งค่าคอนฟิก
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อของหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่มีการจัดโครงแบบ และวิธีการติดไปกับผลิตภัณฑ์หลักที่จัดโครงแบบได้ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921022"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="9c940-103">สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="9c940-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c940-104">กระบวนงานนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีแนบกับผลิตภัณฑ์หลักที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="9c940-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="9c940-105">กระบวนงานนี้ยังแสดงวิธีการสร้างระบบการตั้งชื่อการจัดโครงแบบสำหรับส่วนประกอบแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c940-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="9c940-106">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="9c940-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9c940-107">ระบบการตั้งชื่อของหมายเลขผลิตภัณฑ์ใหม่ถูกกำหนดให้กับผลิตภัณฑ์หลัก D0004 </span><span class="sxs-lookup"><span data-stu-id="9c940-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="9c940-108">โดยทั่วไปงานนี้อาจดำเนินการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c940-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="9c940-109">สร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c940-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="9c940-110">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> ระบบการตั้งชื่อผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="9c940-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="9c940-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9c940-111">Select **New**.</span></span>
1. <span data-ttu-id="9c940-112">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9c940-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="9c940-113">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9c940-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="9c940-114">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-114">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-115">เลือก **หมายเลขผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="9c940-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="9c940-116">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-116">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-117">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="9c940-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="9c940-118">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-119">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9c940-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="9c940-120">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-120">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-121">เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9c940-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="9c940-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c940-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="9c940-123">กำหนดระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="9c940-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="9c940-124">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="9c940-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="9c940-125">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="9c940-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9c940-126">ตัวอย่างเช่น ตัวกรองในฟิลด์ **หมายเลขผลิตภัณฑ์** ด้วยค่า 'D'</span><span class="sxs-lookup"><span data-stu-id="9c940-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="9c940-127">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="9c940-128">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="9c940-128">Select **Edit**.</span></span>
1. <span data-ttu-id="9c940-129">เลือก *ใช่* ในฟิลด์ **ใช้ระบบการตั้งชื่อ**</span><span class="sxs-lookup"><span data-stu-id="9c940-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="9c940-130">ในฟิลด์ **ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อย** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9c940-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="9c940-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c940-131">Close the page.</span></span>
1. <span data-ttu-id="9c940-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c940-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="9c940-133">สร้างระบบการตั้งชื่อสำหรับส่วนประกอบแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c940-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="9c940-134">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="9c940-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="9c940-135">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9c940-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="9c940-136">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="9c940-137">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="9c940-137">Select **Edit**.</span></span>
1. <span data-ttu-id="9c940-138">เลือก *ใช่* ในฟิลด์ **ใช้ระบบการตั้งชื่อการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="9c940-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="9c940-139">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-139">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-140">เลือก **ค่าแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="9c940-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="9c940-141">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-142">ในฟิลด์ **แอททริบิวต์** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9c940-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="9c940-143">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-143">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-144">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="9c940-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="9c940-145">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-146">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9c940-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="9c940-147">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-147">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-148">เลือก **ค่าแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="9c940-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="9c940-149">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-150">ในฟิลด์ **แอททริบิวต์** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9c940-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="9c940-151">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-151">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-152">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="9c940-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="9c940-153">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-154">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9c940-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="9c940-155">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-155">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-156">เลือก **ค่าแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="9c940-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="9c940-157">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-158">ในฟิลด์ **แอททริบิวต์** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9c940-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="9c940-159">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-159">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-160">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="9c940-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="9c940-161">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-162">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9c940-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="9c940-163">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-163">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-164">เลือก **ค่าแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="9c940-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="9c940-165">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-166">ในฟิลด์ **แอททริบิวต์** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9c940-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="9c940-167">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-167">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-168">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="9c940-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="9c940-169">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-170">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9c940-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="9c940-171">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9c940-171">Select **Add**.</span></span>
1. <span data-ttu-id="9c940-172">เลือก **ค่าลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="9c940-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="9c940-173">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c940-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="9c940-174">ในฟิลด์ **ลำดับหมายเลข** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9c940-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="9c940-175">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c940-175">Close the page.</span></span>
1. <span data-ttu-id="9c940-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c940-176">Close the page.</span></span>
1. <span data-ttu-id="9c940-177">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9c940-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]