---
title: สร้างและกำหนดนโยบายพฤติกรรมต้นทุนสำหรับหน่วยการควบคุมต้นทุน
description: พฤติกรรมต้นทุนคือการจัดประเภทของต้นทุนคงที่หรือต้นทุนผันแปร
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841380"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="d475c-103">สร้างและกำหนดนโยบายพฤติกรรมต้นทุนสำหรับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d475c-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d475c-104">พฤติกรรมต้นทุนคือการจัดประเภทของต้นทุนคงที่หรือต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="d475c-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="d475c-105">นโยบายและกฎที่สอดคล้องกันต้องถูกกำหนดให้กับหน่วยการควบคุมต้นทุนสำหรับนโยบายเพื่อให้เริ่มมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="d475c-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="d475c-106">ใช้กระบวนงานนี้เพื่อสร้างนโยบายและกำหนดนโยบายหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d475c-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="d475c-107">สร้างลำดับชั้นพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d475c-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="d475c-108">ไปที่ การบัญชีต้นทุน > มิติ > ลำดับชั้นของมิติ</span><span class="sxs-lookup"><span data-stu-id="d475c-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="d475c-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-109">Click New.</span></span>
3. <span data-ttu-id="d475c-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-110">Click Create.</span></span>
4. <span data-ttu-id="d475c-111">ในฟิลด์ชื่อลำดับชั้นมิติ พิมพ์ 'ลำดับชั้นพฤติกรรมต้นทุน'</span><span class="sxs-lookup"><span data-stu-id="d475c-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="d475c-112">ในฟิลด์มิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d475c-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-113">เลือกองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d475c-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="d475c-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d475c-114">Click Save.</span></span>
7. <span data-ttu-id="d475c-115">คลิกดูลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="d475c-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="d475c-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-116">Click New.</span></span>
9. <span data-ttu-id="d475c-117">ในฟิลด์ชื่อโหนด ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d475c-118">ป้อนอัตราคงที่</span><span class="sxs-lookup"><span data-stu-id="d475c-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="d475c-119">ในแผนภูมิ เลือก 'ลำดับชั้นพฤติกรรมต้นทุน'</span><span class="sxs-lookup"><span data-stu-id="d475c-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="d475c-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-120">Click New.</span></span>
12. <span data-ttu-id="d475c-121">ในฟิลด์ชื่อโหนด ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d475c-122">ป้อนต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="d475c-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="d475c-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d475c-123">Click Save.</span></span>
14. <span data-ttu-id="d475c-124">ในแผนภูมิ เลือก 'ลำดับชั้นพฤติกรรมต้นทุน\ต้นทุนคงที่'</span><span class="sxs-lookup"><span data-stu-id="d475c-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="d475c-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-125">Click New.</span></span>
16. <span data-ttu-id="d475c-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d475c-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d475c-127">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-128">ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="d475c-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="d475c-129">ในฟิลด์สมาชิกมิติสิ้นสุด ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-130">ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="d475c-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="d475c-131">ในแผนภูมิ เลือก 'ลำดับชั้นพฤติกรรมต้นทุน\ต้นทุนผันแปร'</span><span class="sxs-lookup"><span data-stu-id="d475c-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="d475c-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-132">Click New.</span></span>
21. <span data-ttu-id="d475c-133">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d475c-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="d475c-134">ในฟิลด์สมาชิกมิติเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-135">ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="d475c-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="d475c-136">ในฟิลด์สมาชิกมิติสิ้นสุด ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-137">ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="d475c-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="d475c-138">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d475c-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="d475c-139">สร้างนโยบายและกฎ</span><span class="sxs-lookup"><span data-stu-id="d475c-139">Create the policy and rules</span></span>
1. <span data-ttu-id="d475c-140">ไปที่ การบัญชีต้นทุน > นโยบาย > นโยบายพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d475c-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="d475c-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-141">Click New.</span></span>
3. <span data-ttu-id="d475c-142">ในฟิลด์ชื่อนโยบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="d475c-143">ในฟิลด์ลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-144">เลือกลำดับชั้นของนโยบายที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d475c-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="d475c-145">ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-146">เลือกองค์กร</span><span class="sxs-lookup"><span data-stu-id="d475c-146">Select Organization.</span></span>  
6. <span data-ttu-id="d475c-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d475c-147">Click Save.</span></span>
7. <span data-ttu-id="d475c-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-148">Click New.</span></span>
8. <span data-ttu-id="d475c-149">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d475c-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d475c-150">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-151">ขยายทั้งลำดับชั้นเพื่อเลือกต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="d475c-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="d475c-152">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d475c-153">โดยค่าเริ่มต้น เปอร์เซ็นต์ผันแปรเท่ากับ 100 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="d475c-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="d475c-154">คลิก การกำหนดนโยบายสำหรับหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d475c-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="d475c-155">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d475c-155">Click New.</span></span>
13. <span data-ttu-id="d475c-156">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d475c-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="d475c-157">ในฟิลด์ มีผลบังคับใช้นับจากวันที่ทางการบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d475c-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="d475c-158">กฎมีผลบังคับวันที่ และผู้ใช้หรือระบบอาจยกเลิกการใช้กฎได้ถ้ามีการสร้างเวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="d475c-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="d475c-159">ในฟิลด์หน่วยการควบคุมต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d475c-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="d475c-160">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d475c-160">Click Save.</span></span>

