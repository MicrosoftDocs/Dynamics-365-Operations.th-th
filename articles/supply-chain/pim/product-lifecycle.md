---
title: ภาพรวมของสถานะของวงจรการใช้ผลิตภัณฑ์
description: เอกสารสถานะรอบการขายของผลิตภัณฑ์ สถานะรอบการขายของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้
author: cvocph
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: b5b0ceb1926de6efda239fdbc69fb36a9d4b28e0
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934851"
---
# <a name="product-lifecycle-state-overview"></a><span data-ttu-id="172a3-103">ภาพรวมของสถานะของวงจรการใช้ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="172a3-103">Product lifecycle state overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="172a3-104">เอกสารสถานะรอบการขายของผลิตภัณฑ์ สถานะรอบการขายของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="172a3-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="172a3-105">สถานะรอบการขายของผลิตภัณฑ์ถูกกำหนดโดยผู้ใช้ โดยทั่วไป ผู้จัดการผลิตภัณฑ์หรือผู้จัดการข้อมูลหลักของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="172a3-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="172a3-106">กระบวนการทางธุรกิจเฉพาะ เช่น การวางแผนหลัก สามารถได้รับผลกระทบโดยสถานะรอบการขายเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="172a3-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   

<span data-ttu-id="172a3-107">ผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยสามารถเชื่อมโยงกับสถานะรอบการขายของผลิตภัณฑ์ ที่เอกสารในสถานะรอบการขาย ผลิตภัณฑ์เฉพาะ หรือผลิตภัณฑ์ย่อยอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="172a3-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="172a3-108">คุณสามารถกำหนดสถานะรอบการขายผลิตภัณฑ์จำนวนเท่าใดก็ได้ โดยการกำหนดชื่อสถานะและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="172a3-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="172a3-109">คุณสามารถเลือกสถานะรอบการขายหนึ่งให้เป็นสถานะเริ่มต้นสำหรับผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="172a3-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="172a3-110">ผลิตภัณฑ์ย่อยที่นำออกใช้สืบทอดสถานะรอบการขายผลิตภัณฑ์จากผลิตภัณฑ์หลักที่นำออกใช้ในการสร้าง</span><span class="sxs-lookup"><span data-stu-id="172a3-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="172a3-111">เมื่อเปลี่ยนสถานะรอบการขายในผลิตภัณฑ์หลักที่นำออกใช้ คุณสามารถเลือกที่จะอัพเดตผลิตภัณฑ์ย่อยที่มีอยู่ทั้งหมดที่มีสถานะดั้งเดิมเหมือนกันได้</span><span class="sxs-lookup"><span data-stu-id="172a3-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="172a3-112">สร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="172a3-112">Create a new product lifecycle state</span></span> 

- <span data-ttu-id="172a3-113">เพื่อสถานะสร้างรอบการขายของผลิตภัณฑ์ใหม่ เล่น หรืออ่านคู่มืองาน **สร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="172a3-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="172a3-114">เพื่อสร้างสถานะสร้างรอบการขายของผลิตภัณฑ์เริ่มต้น เล่น หรืออ่านคู่มืองาน **สร้างสถานะรอบการขายของผลิตภัณฑ์เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="172a3-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="172a3-115">เชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="172a3-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="172a3-116">มีหลายวิธีที่จะเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่นำออกใช้ หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="172a3-117">ในการสร้างผลิตภัณฑ์ที่นำออกใช้ใหม่ **สถานะรอบการขายของผลิตภัณฑ์** ค่าเริ่มต้น จะถูกกำหนดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="172a3-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="172a3-118">ในการนำผลิตภัณฑ์ออกใช้ไปยังนิติบุคคล **สถานะรอบการขายของผลิตภัณฑ์** ค่าเริ่มต้น จะถูกกำหนดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="172a3-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="172a3-119">ในการนำผลิตภัณฑ์ย่อยออกใช้ไปยังนิติบุคคล **สถานะรอบการขายของผลิตภัณฑ์** ที่เกี่ยวข้องกับการนำผลิตภัณฑ์หลักออกใช้ในนิติบุคคลนี้ จะถูกกำหนดโดยอัตโนมัติเพื่อสร้างตัวแปรใหม่</span><span class="sxs-lookup"><span data-stu-id="172a3-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="172a3-120">คุณสามารถปรับปรุงสถานะรอบการขายของผลิตภัณฑ์ได้ด้วยตนเอง โดยการใช้:</span><span class="sxs-lookup"><span data-stu-id="172a3-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="172a3-121">หน้ารายการ **ผลิตภัณฑ์ที่นำออกใช้** หรือ **มุมมองรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="172a3-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="172a3-122">หน้ารายการ **ผลิตภัณฑ์ย่อยที่นำออกใช้** หรือ **มุมมองรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="172a3-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="172a3-123">ค้นหาผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่ล้าสมัยตามความต้องการ และเชื่อมโยงสถานะรอบการขาย</span><span class="sxs-lookup"><span data-stu-id="172a3-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="172a3-124">สำหรับข้อมูลโดยละเอียดเกี่ยวกับวิธีการเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์ เล่น หรืออ่านคู่มืองานสองต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="172a3-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="172a3-125">เพื่อเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์หลักที่นำออกใช้ เล่น หรืออ่านคู่มืองาน **กำหนดสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์หลักที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="172a3-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="172a3-126">เพื่อเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่นำออกใช้ เล่น หรืออ่านคู่มืองาน **กำหนดสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="172a3-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="172a3-127">ผลกระทบต่อการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="172a3-127">Impact on master planning</span></span> 

<span data-ttu-id="172a3-128">สถานะรอบการขายของผลิตภัณฑ์มีเพียงแฟล็กการควบคุมหนึ่งรายการ: **ใช้งานอยู่สำหรับการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="172a3-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="172a3-129">โดยค่าเริ่มต้น รายการนี้ถูกตั้งค่าเป็น **ใช่** สำหรับสถานะรอบการขายของผลิตภัณฑ์ที่สร้างทั้งหมด แต่สามารถถูกเปลี่ยนเป็น **ไม่ใช่** ได้</span><span class="sxs-lookup"><span data-stu-id="172a3-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="172a3-130">เมื่อตั้งค่าเป็น **ไม่ใช่** ผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยที่นำออกใช้ที่เกี่ยวข้องคือ:</span><span class="sxs-lookup"><span data-stu-id="172a3-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="172a3-131">แยกออกจากการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="172a3-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="172a3-132">แยกออกจากการคำนวณระดับ BOM</span><span class="sxs-lookup"><span data-stu-id="172a3-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="172a3-133">สำหรับข้อมูลโดยละเอียดเกี่ยวกับวิธีการใช้สถานะรอบการขายของผลิตภัณฑ์ เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM เล่น หรืออ่านคู่มืองาน **สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="172a3-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="172a3-134">สำหรับเหตุผลในด้านประสิทธิภาพ ขอแนะนำอย่างยิ่งให้เชื่อมโยงผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยที่ล้าสมัยทั้งหมด โดยเฉพาะอย่างยิ่งเมื่อทำงานกับผลิตภัณฑ์ย่อยในการตั้งค่าคอนฟิกที่ไม่สามารถนำกลับมาใช้ใหม่ได้ ซึ่งมีสถานะรอบการขายของผลิตภัณฑ์ที่ถูกปิดใช้งานสำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="172a3-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  

## <a name="default-migration-import-and-export"></a><span data-ttu-id="172a3-135">การย้าย การนำเข้า และการส่งออกข้อมูลค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="172a3-135">Default migration, import, and export</span></span> 

<span data-ttu-id="172a3-136">ไม่มีการสนับสนุนสถานะของวงจรการใช้ของผลิตภัณฑ์โดยเอนทิตีข้อมูล และไม่สามารถตั้งค่าสถานะของวงจรการใช้เป็นสถานะผันแปร โดยใช้เอนทิตีข้อมูลผลิตภัณฑ์ที่นำออกใช้ หรือเอนทิตีข้อมูลตัวแปรที่นำออกใช้ อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="172a3-136">The product lifecycle states are supported by data entities, and the lifecycle state can be set to a variable state through either the released product data entity or the released variant data entity.</span></span>

## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="172a3-137">ค้นหาผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="172a3-137">Find obsolete products and products variants</span></span> 

<span data-ttu-id="172a3-138">คุณสามารถเรียกใช้การวิเคราะห์แบบจำลอง เพื่อค้นหาผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยซึ่งล้าสมัยได้ และจากนั้นอัพเดตสถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="172a3-138">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="172a3-139">เมื่อต้องการค้นหาผลิตภัณฑ์ที่ล้าสมัย เล่น และอ่านคู่มืองาน **ค้นหาผลิตภัณฑ์ย่อยที่ล้าสมัย และกำหนดสถานะรอบการขายของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="172a3-139">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="172a3-140">คู่มืองานนี้แสดงวิธีการค้นหาผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยซึ่งล้าสมัย และวิธีการเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="172a3-140">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="172a3-141">นอกจากนี้ ยังแสดง hot เพื่อดูผลลัพธ์ของแบบจำลอง และประเมินจำนวนผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่จะเชื่อมโยงกับสถานะรอบการขายของผลิตภัณฑ์ใหม่ เมื่อรันการปรับปรุง โดยไม่มีการจำลอง</span><span class="sxs-lookup"><span data-stu-id="172a3-141">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

<span data-ttu-id="172a3-142">โดยการรันการวิเคราะห์ในโหมดจำลอง ผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่ระบุเป็นล้าสมัย ถูกแสดงอยู่ในแบบฟอร์มเฉพาะ ที่ซึ่งพวกเขาสามารถตรวจทานได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="172a3-142">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="172a3-143">การวิเคราะห์ค้นหาธุรกรรมและข้อมูลหลักเฉพาะในการระบุผลิตภัณฑ์ที่ไม่มีความต้องการภายในรอบระยะเวลาผันแปร และไม่มีข้อมูลหลักที่อาจส่งผลต่อความต้องการ</span><span class="sxs-lookup"><span data-stu-id="172a3-143">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="172a3-144">ผลิตภัณฑ์ที่นำออกใช้ใหม่ภายในรอบระยะเวลาผันแปร สามารถถูกแยกออกจากการวิเคราะห์ได้</span><span class="sxs-lookup"><span data-stu-id="172a3-144">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="172a3-145">เมื่อการจำลองการวิเคราะห์ส่งคืนผลลัพธ์คาดไว้ ผู้ใช้สามารถรันการวิเคราะห์ และตั้งค่าสถานะรอบการขายของผลิตภัณฑ์ใหม่เป็นผลิตภัณฑ์ทั้งหมดที่ระบุเป็นล้าสมัยด้วยการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="172a3-145">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  

> [!NOTE]
> <span data-ttu-id="172a3-146">โปรดสังเกตว่า การวิเคราะห์และปรับปรุงทั้งหมดจะต้องกระทำภายในนิติบุคคลเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="172a3-146">Note that all analysis and updates must be done within the same legal entity.</span></span>  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="172a3-147">เงื่อนไขในการเลือกและอัพเดตผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="172a3-147">Criteria to select and update released products or product variants</span></span> 

<span data-ttu-id="172a3-148">ใช้เงื่อนไขต่อไปนี้ในการเลือกและอัพเดตผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้:</span><span class="sxs-lookup"><span data-stu-id="172a3-148">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="172a3-149">สถานะรอบการขายผลิตภัณฑ์ของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยต้องแตกต่างจากสถานะที่ต้องการใหม่</span><span class="sxs-lookup"><span data-stu-id="172a3-149">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="172a3-150">ผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยถูกสร้างไม่กี่วันที่ผ่านมา ตามจำนวนวันที่คุณป้อนในกล่องโต้ตอบการเลือก</span><span class="sxs-lookup"><span data-stu-id="172a3-150">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="172a3-151">ไม่มีใบสั่งผลิตที่เปิดค้างไว้ (= สถานะ < สิ้นสุด) สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-151">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="172a3-152">ไม่มีธุรกรรมไม่มีสินค้าคงคลังที่เปิด (= สถานะ ออก ReservPhysical ไปยัง QuotationIssue หรือสถานะ ใบเสร็จ Registrered เป็น QuotationReceipt) สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-152">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="172a3-153">ไม่มีธุรกรรมสินค้าคงคลังภายในจำนวนวันล่าสุดสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-153">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="172a3-154">ไม่มีการคาดการณ์ความต้องการหรือการจัดหาวัสดุในอนาคตสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-154">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="172a3-155">ไม่มีการกำหนดระดับสินค้าคงคลังขั้นต่ำในความครอบคลุมสินค้าสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยไว้</span><span class="sxs-lookup"><span data-stu-id="172a3-155">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="172a3-156">ไม่มีกฎคัมบังปริมาณคงที่ที่ใช้งานอยู่สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-156">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="172a3-157">ไม่มีรายการใบสั่งบริการสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-157">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="172a3-158">ไม่มีการขายที่ใช้งานอยู่หรือในอนาคต หรือรายการข้อตกลงการซื้อ สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="172a3-158">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="172a3-159">ผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยไม่ถูกใช้ใน BOM ที่เชื่อมโยงกับรุ่น BOM ที่ได้รับอนุมัติซึ่งไม่มีการหมดอายุสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่ใช้งานอยู่สำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="172a3-159">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="172a3-160">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="172a3-160">Related topics</span></span>

-  [<span data-ttu-id="172a3-161">สร้างสถานะของวงจรการใช้ผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="172a3-161">Create a new product lifecycle state</span></span>](tasks/new-product-lifecycle-state.md)
-  [<span data-ttu-id="172a3-162">สร้างสถานะของวงจรการใช้ผลิตภัณฑ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="172a3-162">Create a default product lifecycle state</span></span>](tasks/default-product-lifecycle-state.md)
-  [<span data-ttu-id="172a3-163">กำหนดสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์หลักที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="172a3-163">Assign a product lifecycle state to a released product master</span></span>](tasks/product-lifecycle-state-released-product-master.md)
-  [<span data-ttu-id="172a3-164">กำหนดสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="172a3-164">Assign a product lifecycle state to a released product</span></span>](tasks/product-lifecycle-state-released-product.md)
-  [<span data-ttu-id="172a3-165">ค้นหาผลิตภัณฑ์ย่อยที่ล้าสมัย และกำหนดสถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="172a3-165">Find obsolete product variants and assign a product lifecycle state</span></span>](tasks/obsolete-product-variants.md)
-  [<span data-ttu-id="172a3-166">สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="172a3-166">Create a product lifecycle state to exclude products from Master planning</span></span>](tasks/exclude-products-master-planning.md)
