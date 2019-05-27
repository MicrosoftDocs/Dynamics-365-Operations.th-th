---
title: ตั้งค่านโยบายสำหรับการจัดประเภทการจัดซื้อตามลำดับชั้น
description: 'ใช้ขั้นตอนนี้เพื่อตั้งค่ากฎสำหรับการเรียงลำดับผลิตภัณฑ์ในประเภท '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569925"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="cc6d8-103">ตั้งค่านโยบายสำหรับการจัดประเภทการจัดซื้อตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="cc6d8-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc6d8-104">ใช้ขั้นตอนนี้เพื่อตั้งค่ากฎสำหรับการเรียงลำดับผลิตภัณฑ์ในประเภท </span><span class="sxs-lookup"><span data-stu-id="cc6d8-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="cc6d8-105">มีการกำหนดกฎสำหรับนโยบายการจัดซื้อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cc6d8-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="cc6d8-106">กฎการเข้าถึงประเภทควบคุมประเภทการจัดซื้อที่พนักงานมีสิทธิเข้าถึงเมื่อสร้างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cc6d8-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="cc6d8-107">เมื่อมีการสร้างใบสั่ง นโยบายการจัดซื้อและกฎการเข้าถึงประเภทที่ควรใช้จะขึ้นอยู่กับนิติบุคคลและหน่วยปฏิบัติงานที่พนักงานเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="cc6d8-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="cc6d8-108">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="cc6d8-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="cc6d8-109">โดยทั่วไปงานนี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc6d8-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="cc6d8-110">ค้นหานโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc6d8-110">Find the procurement policy</span></span>
1. <span data-ttu-id="cc6d8-111">ไปที่การจัดซื้อและการจัดหา > การตั้งค่า > นโยบาย > นโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc6d8-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="cc6d8-112">คลิกลิงค์ในนโยบาย USMF นโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc6d8-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="cc6d8-113">นี่คือนโยบายที่คุณจะเพิ่มกฎ </span><span class="sxs-lookup"><span data-stu-id="cc6d8-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="cc6d8-114">ซึ่งต้องเป็นนโยบายที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="cc6d8-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="cc6d8-115">สร้างกฎการเข้าถึงประเภท</span><span class="sxs-lookup"><span data-stu-id="cc6d8-115">Create a category access rule</span></span>
1. <span data-ttu-id="cc6d8-116">เลือกกฎนโยบายการเข้าถึงประเภท</span><span class="sxs-lookup"><span data-stu-id="cc6d8-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="cc6d8-117">ถ้าปุ่มสร้างกฎนโยบายเป็นสีเทา นั่นเป็นเพราะมีกฎนโยบายที่ใช้งานอยู่สำหรับการเข้าถึงประเภทแล้ว </span><span class="sxs-lookup"><span data-stu-id="cc6d8-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="cc6d8-118">ตรวจสอบฟิลด์วันที่มีผลบังคับใช้และวันหมดอายุเพื่อกำหนด จากนั้นคลิก ถอนกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="cc6d8-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="cc6d8-119">ถ้าปุ่มสร้างกฎนโยบายพร้อมใช้งาน คุณไม่จำเป็นต้องทำสิ่งใด</span><span class="sxs-lookup"><span data-stu-id="cc6d8-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="cc6d8-120">คลิกสร้างกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="cc6d8-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="cc6d8-121">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="cc6d8-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="cc6d8-122">เวลาจะต้องไม่ทับซ้อนกับกฎอื่นที่ใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="cc6d8-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="cc6d8-123">เลือกประเภทที่จะใช้กฎ </span><span class="sxs-lookup"><span data-stu-id="cc6d8-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="cc6d8-124">จดบันทึกว่าประเภทใด เนื่องจากคุณจำเป็นต้องใช้ในภายหลัง </span><span class="sxs-lookup"><span data-stu-id="cc6d8-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="cc6d8-125">เมื่อคุณเลือกประเภทแล้ว ประเภทหลักหรือประเภทต่าง ๆ จะถูกเพิ่มเข้าในรายการประเภทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cc6d8-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="cc6d8-126">หากคุณต้องการใช้กฎกับประเภทย่อยทั้งหมดของประเภทที่เลือก ให้เลือกกล่องกาเครื่องหมาย รวมประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="cc6d8-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="cc6d8-127">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cc6d8-127">Click Add.</span></span>
    * <span data-ttu-id="cc6d8-128">หากคุณตั้งค่าตัวเลือกรวมกฎหลักเป็นใช่ กฎนโยบายที่คุณกำหนดสำหรับประเภทหลักจะถูกกำหนดให้กับประเภทย่อยด้วยหากไม่มีการกำหนดกฎนโยบายให้แก่ประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="cc6d8-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="cc6d8-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cc6d8-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="cc6d8-130">สร้างกฎนโยบายประเภท</span><span class="sxs-lookup"><span data-stu-id="cc6d8-130">Create a category policy rule</span></span>
1. <span data-ttu-id="cc6d8-131">เลือกกฎนโยบายประเภท</span><span class="sxs-lookup"><span data-stu-id="cc6d8-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="cc6d8-132">ถ้าปุ่มสร้างกฎนโยบายเป็นสีเทา ให้เลือกกฎนโยบายที่ใช้งานอยู่ และจากนั้นคลิก ถอนกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="cc6d8-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="cc6d8-133">คลิกสร้างกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="cc6d8-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="cc6d8-134">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="cc6d8-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="cc6d8-135">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cc6d8-135">Click Add.</span></span>
5. <span data-ttu-id="cc6d8-136">เลือกประเภทเดียวกันกับที่คุณใช้สำหรับกฎการเข้าถึงประเภท</span><span class="sxs-lookup"><span data-stu-id="cc6d8-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="cc6d8-137">ในฟิลด์การเลือกผู้จัดจำหน่าย ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="cc6d8-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="cc6d8-138">เลือกกฎที่จะควบคุมชนิดของผู้จัดจำหน่ายที่สามารถเลือกสำหรับประเภทเมื่อมีการสร้างใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cc6d8-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="cc6d8-139">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="cc6d8-139">Click Close.</span></span>
    * <span data-ttu-id="cc6d8-140">กฎนโยบายที่คุณได้กำหนดไว้มีไว้สำหรับใบขอซื้อชนิดของปริมาณการใช้วัสดุ </span><span class="sxs-lookup"><span data-stu-id="cc6d8-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="cc6d8-141">ถ้าคุณต้องการกำหนดนโยบายสำหรับใบขอซื้อของการเพิ่มเติมสินค้าของชนิด ให้สร้างกฎสำหรับชนิดกฎนโยบายที่เรียกว่า "กฎนโยบายการเข้าถึงประเภทการเติมสินค้า"</span><span class="sxs-lookup"><span data-stu-id="cc6d8-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  

