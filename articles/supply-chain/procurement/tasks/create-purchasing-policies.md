---
title: สร้างนโยบายการจัดซื้อ
description: หัวข้อนี้แสดงวิธีการสร้างนโยบายการจัดซื้อเพื่อให้สอดคล้องกับกระบวนการทางธุรกิจของคุณสำหรับการซื้อ
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4ba2a23f84972391283eaf01cef70a161c75226
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438423"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="c71bb-103">สร้างนโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c71bb-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c71bb-104">หัวข้อนี้แสดงวิธีการสร้างนโยบายการจัดซื้อเพื่อให้สอดคล้องกับกระบวนการทางธุรกิจของคุณสำหรับการซื้อ</span><span class="sxs-lookup"><span data-stu-id="c71bb-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="c71bb-105">ก่อนที่คุณจะสามารถสร้างนโยบายการจัดซื้อ คุณจะต้องตั้งค่าพารามิเตอร์นโยบายการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c71bb-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="c71bb-106">สามารถสร้าง ปรับเปลี่ยน และถอนนโยบายการจัดซื้อได้ แต่คุณไม่สามารถลบนโยบายการจัดซื้อได้</span><span class="sxs-lookup"><span data-stu-id="c71bb-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="c71bb-107">โดยทั่วไปกระบวนงานนี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c71bb-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="c71bb-108">คุณสามารถใช้ขั้นตอนนี้ในข้อมูลสาธิตบริษัท USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="c71bb-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="c71bb-109">ตั้งค่าพารามิเตอร์นโยบาย</span><span class="sxs-lookup"><span data-stu-id="c71bb-109">Set up policy parameters</span></span>
1. <span data-ttu-id="c71bb-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > การตั้งค่า > นโยบาย > นโยบายการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="c71bb-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="c71bb-111">บนบานหน้าต่างการดำเนินการ เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="c71bb-111">On the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="c71bb-112">กฎลำดับความสำคัญของนโยบายใช้กับระดับต่าง ๆ ในองค์กรของคุณ </span><span class="sxs-lookup"><span data-stu-id="c71bb-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="c71bb-113">หน่วยงานที่แสดงขึ้นอยู่กับลำดับชั้นองค์กรของคุณ และระดับในลำดับชั้นที่ได้รับการกำหนดวัตถุประสงค์ของตัวควบคุมภายในของการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c71bb-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="c71bb-114">ตัวอย่างเช่น องค์กรของคุณอาจมีนิติบุคคล ศูนย์ต้นทุน ภูมิภาค และแผนก แต่อาจเป็นได้ว่า มีเฉพาะบางรายการเหล่านี้ที่มีวัตถุประสงค์ของลำดับชั้นของตัวควบคุมภายในของการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c71bb-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="c71bb-115">ตามค่าเริ่มต้น องค์กรชนิดบริษัทจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c71bb-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="c71bb-116">เลือกแท็บ **พารามิเตอร์ชนิดกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="c71bb-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="c71bb-117">ในแผนภูมิ ไปที่ **นโยบายการจัดซื้อ > กฎการควบคุมใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="c71bb-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="c71bb-118">คุณกำหนดลำดับความสำคัญสำหรับการแก้ปัญหานโยบายที่ระดับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="c71bb-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="c71bb-119">อย่างไรก็ตาม นโยบายบางชนิด คุณสามารถแทนที่ลำดับความสำคัญสำหรับชนิดกฎนโยบายแต่ละรายการได้</span><span class="sxs-lookup"><span data-stu-id="c71bb-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="c71bb-120">ตัวอย่างเช่น คุณอาจกำหนดลำดับความสำคัญสำหรับนโยบายการจัดซื้อเป็น: ศูนย์ต้นทุน แผนก บริษัท</span><span class="sxs-lookup"><span data-stu-id="c71bb-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="c71bb-121">สำหรับกฎนโยบายแค็ตตาล็อก คุณอาจต้องการให้ลำดับความสำคัญเป็น: แผนก ศูนย์ต้นทุน บริษัท</span><span class="sxs-lookup"><span data-stu-id="c71bb-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="c71bb-122">คุณสามารถเปลี่ยนลำดับความสำคัญสำหรับกฎนโยบายแค็ตตาล็อกได้</span><span class="sxs-lookup"><span data-stu-id="c71bb-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="c71bb-123">เมื่อผู้ปฏิบัติงานสร้างการจัดหาวัตถุดิบ แค็ตตาล็อกที่แสดงจะถูกกำหนดโดยนโยบายที่เกี่ยวข้องกับแผนกของผู้ปฏิบัติงาน จากนั้นจึงตามด้วยศูนย์ต้นทุน และบริษัทของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="c71bb-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="c71bb-124">ถ้ามีการแสดงรายการระดับองค์กรมากกว่าหนึ่งรายการ คุณสามารถใช้ลูกศรขึ้น/ลงเพื่อตั้งค่าลำดับความสำคัญสำหรับกฎการควบคุมใบขอซื้อได้</span><span class="sxs-lookup"><span data-stu-id="c71bb-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="c71bb-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c71bb-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="c71bb-126">สร้างนโยบายใหม่</span><span class="sxs-lookup"><span data-stu-id="c71bb-126">Create a new policy</span></span>
1. <span data-ttu-id="c71bb-127">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c71bb-127">Select **New**.</span></span>
2. <span data-ttu-id="c71bb-128">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c71bb-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="c71bb-129">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c71bb-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="c71bb-130">นโยบายการจัดซื้อหนึ่งสามารถใช้กับลำดับชั้นขององค์กรเดียวเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="c71bb-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="c71bb-131">ตัวอย่างเช่น คุณอาจมีลำดับชั้นหนึ่งที่ชื่อว่า "ทางภูมิศาสตร์" และอีกหนึ่งรายการที่ชื่อว่า "แผนก" และมีนโยบายการจัดซื้อที่แตกต่างกันสำหรับแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="c71bb-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="c71bb-132">เลือกหน่วยที่ควรใช้นโยบายนี้</span><span class="sxs-lookup"><span data-stu-id="c71bb-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="c71bb-133">เลือกลูกศรเพื่อเพิ่มองค์กรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c71bb-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="c71bb-134">คุณสามารถทำซ้ำกระบวนงานนี้เพื่อเพิ่มองค์กรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c71bb-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="c71bb-135">เพิ่มกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="c71bb-135">Add a policy rule</span></span>
1. <span data-ttu-id="c71bb-136">ในรายการ **ชนิดกฎนโยบาย** เลือก **กฎวัตถุประสงค์ของใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="c71bb-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="c71bb-137">คุณจะสร้างกฎที่ตั้งค่าวัตถุประสงค์ในการจัดหาวัตถุดิบเริ่มต้นเป็นชนิดของปริมาณการใช้วัสดุ แต่อนุญาตให้เลือกชนิดการเติมสินค้าแทนได้</span><span class="sxs-lookup"><span data-stu-id="c71bb-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="c71bb-138">เลือก **สร้างกฎนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="c71bb-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="c71bb-139">เลือก **ใช่** ในฟิลด์ **อนุญาตการแทนที่ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="c71bb-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="c71bb-140">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="c71bb-140">Select **Close**.</span></span>
- <span data-ttu-id="c71bb-141">ขณะนี้คุณสามารถตั้งค่ากฎนโยบายอื่น ๆ สำหรับนโยบายการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="c71bb-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="c71bb-142">หมายเหตุว่าชนิดของกฎนโยบายไม่สามารถมีกฎทับซ้อนที่ใช้งานอยู่ในเวลาเดียวกันภายในนโยบายการจัดซื้อเดียวได้</span><span class="sxs-lookup"><span data-stu-id="c71bb-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  

