---
title: ตั้งค่านโยบายสำหรับการจัดประเภทการจัดซื้อตามลำดับชั้น
description: 'ใช้ขั้นตอนนี้เพื่อตั้งค่ากฎสำหรับการเรียงลำดับผลิตภัณฑ์ในประเภท '
author: mkirknel
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8c259ad081d02395c6ae3c3b7cf66b89933fdf
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149515"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="f6537-103">ตั้งค่านโยบายสำหรับการจัดประเภทการจัดซื้อตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f6537-103">Set up policies for procurement category hierarchies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6537-104">ใช้ขั้นตอนนี้เพื่อตั้งค่ากฎสำหรับการเรียงลำดับผลิตภัณฑ์ในประเภท </span><span class="sxs-lookup"><span data-stu-id="f6537-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="f6537-105">มีการกำหนดกฎสำหรับนโยบายการจัดซื้อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="f6537-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="f6537-106">กฎการเข้าถึงประเภทควบคุมประเภทการจัดซื้อที่พนักงานมีสิทธิเข้าถึงเมื่อสร้างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f6537-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="f6537-107">เมื่อมีการสร้างใบสั่ง นโยบายการจัดซื้อและกฎการเข้าถึงประเภทที่ควรใช้จะขึ้นอยู่กับนิติบุคคลและหน่วยปฏิบัติงานที่พนักงานเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="f6537-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="f6537-108">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="f6537-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="f6537-109">โดยทั่วไปงานนี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="f6537-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="f6537-110">ค้นหานโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="f6537-110">Find the procurement policy</span></span>
1. <span data-ttu-id="f6537-111">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > การตั้งค่า > นโยบาย > นโยบายการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="f6537-111">In the Navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="f6537-112">คลิกลิงค์ในนโยบาย 'นโยบายการจัดซื้อ USMF'</span><span class="sxs-lookup"><span data-stu-id="f6537-112">Click the link on the 'Procurement Policy USMF' policy.</span></span> <span data-ttu-id="f6537-113">นี่คือนโยบายที่คุณจะเพิ่มกฎเข้าไป</span><span class="sxs-lookup"><span data-stu-id="f6537-113">This is the policy that you'll add a rule to.</span></span> <span data-ttu-id="f6537-114">ซึ่งต้องเป็นนโยบายที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="f6537-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="f6537-115">สร้างกฎการเข้าถึงประเภท</span><span class="sxs-lookup"><span data-stu-id="f6537-115">Create a category access rule</span></span>
1. <span data-ttu-id="f6537-116">ขยาย fastTab **กฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="f6537-116">Expand the **Policy rules** fastTab.</span></span>
2. <span data-ttu-id="f6537-117">ในรายการ **ชนิดของกฎนโยบาย** เลือก **กฎนโยบายการเข้าถึงประเภท**</span><span class="sxs-lookup"><span data-stu-id="f6537-117">In the **Policy rule type** list, select the **Category access policy rule**.</span></span> <span data-ttu-id="f6537-118">ถ้าปุ่ม **สร้างกฎนโยบาย** เป็นสีเทา นั่นเป็นเพราะมีกฎนโยบายที่ใช้งานอยู่สำหรับการเข้าถึงประเภทแล้ว</span><span class="sxs-lookup"><span data-stu-id="f6537-118">If the **Create policy rule** button is dimmed, it's because there's already an active policy rule for Category access.</span></span> <span data-ttu-id="f6537-119">ตรวจสอบฟิลด์ **มีผลบังคับใช้** และฟิลด์ **การหมดอายุ** เพื่อกำหนด จากนั้นเลือก และคลิก **ถอนกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="f6537-119">Check the **Effective** and **Expiration** fields to determine which it is, then select it, and click **Retire policy rule**.</span></span> <span data-ttu-id="f6537-120">ถ้าปุ่ม **สร้างกฎนโยบาย** พร้อมใช้งาน คุณไม่จำเป็นต้องทำสิ่งใด</span><span class="sxs-lookup"><span data-stu-id="f6537-120">If the **Create policy rule** button is available, you don't need to do anything.</span></span>  
3. <span data-ttu-id="f6537-121">คลิก **สร้างกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="f6537-121">Click **Create policy rule**.</span></span>
4. <span data-ttu-id="f6537-122">ในฟิลด์ **วันที่มีผลบังคับใช้** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f6537-122">In the **Effective date** field, enter a date and time.</span></span> <span data-ttu-id="f6537-123">เวลาจะต้องไม่ทับซ้อนกับกฎอื่นที่ใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="f6537-123">The time must not overlap with another rule that's already active.</span></span>  
5. <span data-ttu-id="f6537-124">เลือกประเภทที่จะใช้กฎ </span><span class="sxs-lookup"><span data-stu-id="f6537-124">Select a category that the rule will apply to.</span></span> <span data-ttu-id="f6537-125">จดบันทึกว่านี่คือประเภทใด – คุณจะต้องใช้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="f6537-125">Make a note of which category this is – you'll need it later.</span></span> <span data-ttu-id="f6537-126">เมื่อคุณเลือกประเภทแล้ว ประเภทหลักหรือประเภทต่าง ๆ จะถูกเพิ่มเข้าในรายการประเภทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f6537-126">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span> <span data-ttu-id="f6537-127">หากคุณต้องการใช้กฎกับประเภทย่อยทั้งหมดของประเภทที่เลือก ให้เลือกกล่องกาเครื่องหมาย **รวมประเภทย่อย**</span><span class="sxs-lookup"><span data-stu-id="f6537-127">If you want the rule to apply to all subcategories of the selected category, select the **Include subcategories** check box.</span></span>
6. <span data-ttu-id="f6537-128">คลิกลูกศรทางขวาเพื่อเพิ่มลงในรายการ **ประเภทที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="f6537-128">Click the right arrow to add to the **Selected categories** list.</span></span>  
4. <span data-ttu-id="f6537-129">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f6537-129">Click **OK**.</span></span> <span data-ttu-id="f6537-130">หากคุณตั้งค่าตัวเลือก **รวมกฎหลัก** เป็น ใช่ กฎนโยบายที่คุณกำหนดสำหรับประเภทหลักยังจะถูกกำหนดให้กับประเภทรองด้วย หากไม่มีการกำหนดกฎนโยบายให้แก่ประเภทรอง</span><span class="sxs-lookup"><span data-stu-id="f6537-130">If you set the **Include parent rule** option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="f6537-131">สร้างกฎนโยบายประเภท</span><span class="sxs-lookup"><span data-stu-id="f6537-131">Create a category policy rule</span></span>
1. <span data-ttu-id="f6537-132">ในรายการ **ชนิดของกฎนโยบาย** เลือก **กฎนโยบายประเภท**</span><span class="sxs-lookup"><span data-stu-id="f6537-132">In the **Policy rule type** list, select the **Category policy rule**.</span></span> <span data-ttu-id="f6537-133">ถ้าปุ่ม **สร้างกฎนโยบายเป็นสีเทา** ให้เลือกกฎนโยบายที่ใช้งานอยู่ และจากนั้นคลิก **ถอนกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="f6537-133">If the **Create policy rule** button is dimmed, select the active policy rule, and then click **Retire policy rule**.</span></span>  
2. <span data-ttu-id="f6537-134">คลิก **สร้างกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="f6537-134">Click **Create policy rule**.</span></span>
3. <span data-ttu-id="f6537-135">ในฟิลด์ **วันที่มีผลบังคับใช้** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f6537-135">In the **Effective date** field, enter a date and time.</span></span>
4. <span data-ttu-id="f6537-136">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="f6537-136">Click **Add**.</span></span>
5. <span data-ttu-id="f6537-137">ในฟิลด์ **ประเภท** เลือกประเภทเดียวกันกับที่คุณใช้สำหรับ **กฎการเข้าถึงประเภท**</span><span class="sxs-lookup"><span data-stu-id="f6537-137">In the **Category** field, select the same category that you used for the **Category access rule**.</span></span>
6. <span data-ttu-id="f6537-138">ในฟิลด์ **การเลือกผู้จัดจำหน่าย** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f6537-138">In the **Vendor selection** field, select an option.</span></span> <span data-ttu-id="f6537-139">เลือกกฎที่จะควบคุมชนิดของผู้จัดจำหน่ายที่สามารถเลือกสำหรับประเภทเมื่อมีการสร้างใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="f6537-139">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="f6537-140">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="f6537-140">Click **Close**.</span></span> <span data-ttu-id="f6537-141">กฎนโยบายที่คุณได้กำหนดไว้มีไว้สำหรับใบขอซื้อชนิดของปริมาณการใช้วัสดุ </span><span class="sxs-lookup"><span data-stu-id="f6537-141">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="f6537-142">ถ้าคุณต้องการกำหนดนโยบายสำหรับใบขอซื้อของชนิดการเติมสินค้า คุณต้องสร้างกฎสำหรับชนิดกฎนโยบายที่เรียกว่า "กฎนโยบายการเข้าถึงประเภทการเติมสินค้า"</span><span class="sxs-lookup"><span data-stu-id="f6537-142">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called "Replenishment category access policy rule".</span></span>  

