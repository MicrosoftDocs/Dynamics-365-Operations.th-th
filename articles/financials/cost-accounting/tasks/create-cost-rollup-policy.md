--- 
title: "สร้างนโยบายการรวบรวมต้นทุน"
description: "กระบวนงานนี้แสดงวิธีการสร้างนโยบายการรวบรวมต้นทุนและการสร้างกฎสำหรับนโยบาย"
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e6eddaf80d7b508a2d477bdd731b2b19cb02acd5
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="440c8-103">สร้างนโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="440c8-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="440c8-104">กระบวนงานนี้แสดงวิธีการสร้างนโยบายการรวบรวมต้นทุนและการสร้างกฎสำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="440c8-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="440c8-105">ข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือ USP2</span><span class="sxs-lookup"><span data-stu-id="440c8-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="440c8-106">สร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="440c8-106">Create a policy</span></span>
1. <span data-ttu-id="440c8-107">ไปที่ การบัญชีต้นทุน > นโยบาย > นโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="440c8-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="440c8-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="440c8-108">Click New.</span></span>
3. <span data-ttu-id="440c8-109">ในฟิลด์ชื่อนโยบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="440c8-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="440c8-111">ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-112">เลือก การรวบรวมต้นทุน CC</span><span class="sxs-lookup"><span data-stu-id="440c8-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="440c8-113">ในฟิลด์ลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-114">เลือก การรวบรวมต้นทุน CC</span><span class="sxs-lookup"><span data-stu-id="440c8-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="440c8-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="440c8-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="440c8-116">สร้างกฎสำหรับนโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="440c8-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="440c8-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="440c8-117">Click New.</span></span>
2. <span data-ttu-id="440c8-118">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="440c8-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="440c8-119">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-120">เลือก 007</span><span class="sxs-lookup"><span data-stu-id="440c8-120">Select 007.</span></span>  
4. <span data-ttu-id="440c8-121">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-122">เลือก การรวบรวมต้นทุน CE</span><span class="sxs-lookup"><span data-stu-id="440c8-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="440c8-123">ในฟิลด์ ต้นทุนองค์ประกอบรอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-124">สำหรับตัวอย่างนี้ แม็ปต้นทุนองค์ประกอบรอง CC-007 ไปยังศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="440c8-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="440c8-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="440c8-125">Click New.</span></span>
7. <span data-ttu-id="440c8-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="440c8-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="440c8-127">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-128">เลือก 008</span><span class="sxs-lookup"><span data-stu-id="440c8-128">Select 008.</span></span>  
9. <span data-ttu-id="440c8-129">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-130">เลือก การรวบรวมต้นทุน CE</span><span class="sxs-lookup"><span data-stu-id="440c8-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="440c8-131">ในฟิลด์ ต้นทุนองค์ประกอบรอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-132">สำหรับตัวอย่างนี้ แม็ปต้นทุนองค์ประกอบรอง CC-008 ไปยังศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="440c8-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="440c8-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="440c8-133">Click New.</span></span>
12. <span data-ttu-id="440c8-134">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="440c8-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="440c8-135">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-136">เลือก 009</span><span class="sxs-lookup"><span data-stu-id="440c8-136">Select 009.</span></span>  
14. <span data-ttu-id="440c8-137">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-138">เลือก การรวบรวมต้นทุน CE</span><span class="sxs-lookup"><span data-stu-id="440c8-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="440c8-139">ในฟิลด์ ต้นทุนองค์ประกอบรอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="440c8-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="440c8-140">สำหรับตัวอย่างนี้ แม็ปต้นทุนองค์ประกอบรอง CC-009 ไปยังศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="440c8-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="440c8-141">ทำต่อไปจนกว่าศูนย์ต้นทุนทั้งหมดจะถูกแม็ปไปยังองค์ประกอบต้นทุนรองที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="440c8-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="440c8-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="440c8-142">Click Save.</span></span>


