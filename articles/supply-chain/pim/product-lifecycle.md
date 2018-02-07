---
title: "สถานะรอบการขายของผลิตภัณฑ์"
description: "เอกสารสถานะรอบการขายของผลิตภัณฑ์ สถานะรอบการขายของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้"
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: conradv
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1113b5ca2ab1af474a53d359601fe53e7be64c0e
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="ebcb3-103">สถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ebcb3-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ebcb3-104">เอกสารสถานะรอบการขายของผลิตภัณฑ์ สถานะรอบการขายของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="ebcb3-105">สถานะรอบการขายของผลิตภัณฑ์ถูกกำหนดโดยผู้ใช้ โดยทั่วไป ผู้จัดการผลิตภัณฑ์หรือผู้จัดการข้อมูลหลักของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ebcb3-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="ebcb3-106">กระบวนการทางธุรกิจเฉพาะ เช่น การวางแผนหลัก สามารถได้รับผลกระทบโดยสถานะรอบการขายเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ebcb3-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="ebcb3-107">ผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยสามารถเชื่อมโยงกับสถานะรอบการขายของผลิตภัณฑ์ ที่เอกสารในสถานะรอบการขาย ผลิตภัณฑ์เฉพาะ หรือผลิตภัณฑ์ย่อยอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="ebcb3-108">คุณสามารถกำหนดสถานะรอบการขายผลิตภัณฑ์จำนวนเท่าใดก็ได้ โดยการกำหนดชื่อสถานะและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="ebcb3-109">คุณสามารถเลือกสถานะรอบการขายหนึ่งให้เป็นสถานะเริ่มต้นสำหรับผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="ebcb3-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="ebcb3-110">ผลิตภัณฑ์ย่อยที่นำออกใช้สืบทอดสถานะรอบการขายผลิตภัณฑ์จากผลิตภัณฑ์หลักที่นำออกใช้ในการสร้าง</span><span class="sxs-lookup"><span data-stu-id="ebcb3-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="ebcb3-111">เมื่อเปลี่ยนสถานะรอบการขายในผลิตภัณฑ์หลักที่นำออกใช้ คุณสามารถเลือกที่จะอัพเดตผลิตภัณฑ์ย่อยที่มีอยู่ทั้งหมดที่มีสถานะดั้งเดิมเหมือนกันได้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="ebcb3-112">สร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ebcb3-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="ebcb3-113">เพื่อสถานะสร้างรอบการขายของผลิตภัณฑ์ใหม่ เล่น หรืออ่านคู่มืองาน **สร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="ebcb3-114">เพื่อสร้างสถานะสร้างรอบการขายของผลิตภัณฑ์เริ่มต้น เล่น หรืออ่านคู่มืองาน **สร้างสถานะรอบการขายของผลิตภัณฑ์เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="ebcb3-115">เชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="ebcb3-116">มีหลายวิธีที่จะเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่นำออกใช้ หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="ebcb3-117">ในการสร้างผลิตภัณฑ์ที่นำออกใช้ใหม่ **สถานะรอบการขายของผลิตภัณฑ์** ค่าเริ่มต้น จะถูกกำหนดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ebcb3-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="ebcb3-118">ในการนำผลิตภัณฑ์ออกใช้ไปยังนิติบุคคล **สถานะรอบการขายของผลิตภัณฑ์** ค่าเริ่มต้น จะถูกกำหนดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ebcb3-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="ebcb3-119">ในการนำผลิตภัณฑ์ย่อยออกใช้ไปยังนิติบุคคล **สถานะรอบการขายของผลิตภัณฑ์** ที่เกี่ยวข้องกับการนำผลิตภัณฑ์หลักออกใช้ในนิติบุคคลนี้ จะถูกกำหนดโดยอัตโนมัติเพื่อสร้างตัวแปรใหม่</span><span class="sxs-lookup"><span data-stu-id="ebcb3-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="ebcb3-120">คุณสามารถปรับปรุงสถานะรอบการขายของผลิตภัณฑ์ได้ด้วยตนเอง โดยการใช้:</span><span class="sxs-lookup"><span data-stu-id="ebcb3-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="ebcb3-121">หน้ารายการ **ผลิตภัณฑ์ที่นำออกใช้** หรือ **มุมมองรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="ebcb3-122">หน้ารายการ **ผลิตภัณฑ์ย่อยที่นำออกใช้** หรือ **มุมมองรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="ebcb3-123">ค้นหาผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่ล้าสมัยตามความต้องการ และเชื่อมโยงสถานะรอบการขาย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="ebcb3-124">สำหรับข้อมูลโดยละเอียดเกี่ยวกับวิธีการเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์ เล่น หรืออ่านคู่มืองานสองต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="ebcb3-125">เพื่อเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์หลักที่นำออกใช้ เล่น หรืออ่านคู่มืองาน **กำหนดสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์หลักที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="ebcb3-126">เพื่อเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่นำออกใช้ เล่น หรืออ่านคู่มืองาน **กำหนดสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="ebcb3-127">ผลกระทบต่อการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ebcb3-127">Impact on master planning</span></span> 

<span data-ttu-id="ebcb3-128">สถานะรอบการขายของผลิตภัณฑ์มีเพียงแฟล็กการควบคุมหนึ่งรายการ: **ใช้งานอยู่สำหรับการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="ebcb3-129">โดยค่าเริ่มต้น รายการนี้ถูกตั้งค่าเป็น **ใช่** สำหรับสถานะรอบการขายของผลิตภัณฑ์ที่สร้างทั้งหมด แต่สามารถถูกเปลี่ยนเป็น **ไม่ใช่** ได้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="ebcb3-130">เมื่อตั้งค่าเป็น **ไม่ใช่** ผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยที่นำออกใช้ที่เกี่ยวข้องคือ:</span><span class="sxs-lookup"><span data-stu-id="ebcb3-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="ebcb3-131">แยกออกจากการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ebcb3-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="ebcb3-132">แยกออกจากการคำนวณระดับ BOM</span><span class="sxs-lookup"><span data-stu-id="ebcb3-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="ebcb3-133">สำหรับข้อมูลโดยละเอียดเกี่ยวกับวิธีการใช้สถานะรอบการขายของผลิตภัณฑ์ เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลักและการคำนวณระดับ BOM เล่น หรืออ่านคู่มืองาน **สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="ebcb3-134">สำหรับเหตุผลในด้านประสิทธิภาพ ขอแนะนำอย่างยิ่งให้เชื่อมโยงผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยที่ล้าสมัยทั้งหมด โดยเฉพาะอย่างยิ่งเมื่อทำงานกับผลิตภัณฑ์ย่อยในการตั้งค่าคอนฟิกที่ไม่สามารถนำกลับมาใช้ใหม่ได้ ซึ่งมีสถานะรอบการขายของผลิตภัณฑ์ที่ถูกปิดใช้งานสำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ebcb3-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="ebcb3-135">การย้าย การนำเข้า และการส่งออกข้อมูลค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ebcb3-135">Default migration, import, and export</span></span> 

<span data-ttu-id="ebcb3-136">ไม่มีการสนับสนุนสถานะรอบการขายของผลิตภัณฑ์โดยเอนทิตีข้อมูล และไม่สามารถตั้งค่าสถานะรอบการขายเป็นสถานะผันแปรโดยใช้เอนทิตีข้อมูลผลิตภัณฑ์ที่นำออกใช้ได้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="ebcb3-137">ในการย้ายจากรุ่นก่อน สถานะรอบการขายของผลิตภัณฑ์และผลิตภัณฑ์ย่อยทั้งหมดจะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ebcb3-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="ebcb3-138">เมื่อนำเข้าผลิตภัณฑ์ที่นำออกใช้ผ่านทางเอนทิตีข้อมูล สถานะรอบการขายเริ่มต้นจะถูกนำมาใช้ในการสร้าง</span><span class="sxs-lookup"><span data-stu-id="ebcb3-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="ebcb3-139">เมื่อนำเข้าผลิตภัณฑ์ย่อยที่นำออกใช้ผ่านทางเอนทิตีข้อมูล สถานะรอบการขายของผลิตภัณฑ์ของผลิตภัณฑ์หลักที่นำออกใช้จะถูกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="ebcb3-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="ebcb3-140">ค้นหาผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="ebcb3-141">คุณสามารถเรียกใช้การวิเคราะห์แบบจำลอง เพื่อค้นหาผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยซึ่งล้าสมัยได้ และจากนั้นอัพเดตสถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ebcb3-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="ebcb3-142">เมื่อต้องการค้นหาผลิตภัณฑ์ที่ล้าสมัย เล่น และอ่านคู่มืองาน **ค้นหาผลิตภัณฑ์ย่อยที่ล้าสมัย และกำหนดสถานะรอบการขายของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="ebcb3-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="ebcb3-143">คู่มืองานนี้แสดงวิธีการค้นหาผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยซึ่งล้าสมัย และวิธีการเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="ebcb3-144">นอกจากนี้ ยังแสดง hot เพื่อดูผลลัพธ์ของแบบจำลอง และประเมินจำนวนผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่จะเชื่อมโยงกับสถานะรอบการขายของผลิตภัณฑ์ใหม่ เมื่อรันการปรับปรุง โดยไม่มีการจำลอง</span><span class="sxs-lookup"><span data-stu-id="ebcb3-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="ebcb3-145">โดยการรันการวิเคราะห์ในโหมดจำลอง ผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่ระบุเป็นล้าสมัย ถูกแสดงอยู่ในแบบฟอร์มเฉพาะ ที่ซึ่งพวกเขาสามารถตรวจทานได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="ebcb3-146">การวิเคราะห์ค้นหาธุรกรรมและข้อมูลหลักเฉพาะในการระบุผลิตภัณฑ์ที่ไม่มีความต้องการภายในรอบระยะเวลาผันแปร และไม่มีข้อมูลหลักที่อาจส่งผลต่อความต้องการ</span><span class="sxs-lookup"><span data-stu-id="ebcb3-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="ebcb3-147">ผลิตภัณฑ์ที่นำออกใช้ใหม่ภายในรอบระยะเวลาผันแปร สามารถถูกแยกออกจากการวิเคราะห์ได้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="ebcb3-148">เมื่อการจำลองการวิเคราะห์ส่งคืนผลลัพธ์คาดไว้ ผู้ใช้สามารถรันการวิเคราะห์ และตั้งค่าสถานะรอบการขายของผลิตภัณฑ์ใหม่เป็นผลิตภัณฑ์ทั้งหมดที่ระบุเป็นล้าสมัยด้วยการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="ebcb3-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="ebcb3-149">โปรดสังเกตว่า การวิเคราะห์และปรับปรุงทั้งหมดจะต้องกระทำภายในนิติบุคคลเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ebcb3-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="ebcb3-150">เงื่อนไขในการเลือกและอัพเดตผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="ebcb3-151">ใช้เงื่อนไขต่อไปนี้ในการเลือกและอัพเดตผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้:</span><span class="sxs-lookup"><span data-stu-id="ebcb3-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="ebcb3-152">สถานะรอบการขายผลิตภัณฑ์ของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยต้องแตกต่างจากสถานะที่ต้องการใหม่</span><span class="sxs-lookup"><span data-stu-id="ebcb3-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="ebcb3-153">ผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยถูกสร้างไม่กี่วันที่ผ่านมา ตามจำนวนวันที่คุณป้อนในกล่องโต้ตอบการเลือก</span><span class="sxs-lookup"><span data-stu-id="ebcb3-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="ebcb3-154">ไม่มีใบสั่งผลิตที่เปิดค้างไว้ (= สถานะ < สิ้นสุด) สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="ebcb3-155">ไม่มีธุรกรรมไม่มีสินค้าคงคลังที่เปิด (= สถานะ ออก ReservPhysical ไปยัง QuotationIssue หรือสถานะ ใบเสร็จ Registrered เป็น QuotationReceipt) สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="ebcb3-156">ไม่มีธุรกรรมสินค้าคงคลังภายในจำนวนวันล่าสุดสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="ebcb3-157">ไม่มีการคาดการณ์ความต้องการหรือการจัดหาวัสดุในอนาคตสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="ebcb3-158">ไม่มีการกำหนดระดับสินค้าคงคลังขั้นต่ำในความครอบคลุมสินค้าสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยไว้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="ebcb3-159">ไม่มีกฎคัมบังปริมาณคงที่ที่ใช้งานอยู่สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="ebcb3-160">ไม่มีรายการใบสั่งบริการสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="ebcb3-161">ไม่มีการขายที่ใช้งานอยู่หรือในอนาคต หรือรายการข้อตกลงการซื้อ สำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="ebcb3-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="ebcb3-162">ผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยไม่ถูกใช้ใน BOM ที่เชื่อมโยงกับรุ่น BOM ที่ได้รับอนุมัติซึ่งไม่มีการหมดอายุสำหรับผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่ใช้งานอยู่สำหรับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ebcb3-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebcb3-163">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ebcb3-163">Related topics</span></span>

-  <span data-ttu-id="ebcb3-164">สร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ebcb3-164">Create a new product lifecycle state</span></span>
-  <span data-ttu-id="ebcb3-165">สร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ebcb3-165">Create a default new product lifecycle state</span></span>
-  <span data-ttu-id="ebcb3-166">มอบหมายสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์หลักที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-166">Assign a product lifecycle state to a released product master</span></span>
-  <span data-ttu-id="ebcb3-167">มอบหมายสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="ebcb3-167">Assign a product lifecycle state to a released product</span></span>
-  <span data-ttu-id="ebcb3-168">ค้นหาผลิตภัณฑ์ย่อยที่ล้าสมัย และกำหนดสถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ebcb3-168">Find obsolete product variants and assign a product lifecycle state</span></span>
-  <span data-ttu-id="ebcb3-169">สร้างสถานะรอบการขายของผลิตภัณฑ์เพื่อแยกผลิตภัณฑ์ออกจากการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ebcb3-169">Create a product lifecycle state to exclude products from Master planning</span></span>

