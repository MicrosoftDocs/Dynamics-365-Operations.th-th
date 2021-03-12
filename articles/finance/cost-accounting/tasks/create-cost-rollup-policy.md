---
title: สร้างนโยบายการรวบรวมต้นทุน
description: กระบวนงานนี้แสดงวิธีการสร้างนโยบายการรวบรวมต้นทุนและการสร้างกฎสำหรับนโยบาย
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0a648984a8b4aaa314707e72a615f516116a193
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990753"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="44e84-103">สร้างนโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44e84-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44e84-104">กระบวนงานนี้แสดงวิธีการสร้างนโยบายการรวบรวมต้นทุนและการสร้างกฎสำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="44e84-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="44e84-105">ข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือ USP2</span><span class="sxs-lookup"><span data-stu-id="44e84-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="44e84-106">สร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="44e84-106">Create a policy</span></span>
1. <span data-ttu-id="44e84-107">ไปที่ การบัญชีต้นทุน > นโยบาย > นโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44e84-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="44e84-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="44e84-108">Click New.</span></span>
3. <span data-ttu-id="44e84-109">ในฟิลด์ชื่อนโยบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="44e84-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="44e84-111">ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-112">เลือก การรวบรวมต้นทุน CC</span><span class="sxs-lookup"><span data-stu-id="44e84-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="44e84-113">ในฟิลด์ลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-114">เลือก การรวบรวมต้นทุน CC</span><span class="sxs-lookup"><span data-stu-id="44e84-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="44e84-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="44e84-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="44e84-116">สร้างกฎสำหรับนโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44e84-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="44e84-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="44e84-117">Click New.</span></span>
2. <span data-ttu-id="44e84-118">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44e84-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="44e84-119">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-120">เลือก 007</span><span class="sxs-lookup"><span data-stu-id="44e84-120">Select 007.</span></span>  
4. <span data-ttu-id="44e84-121">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-122">เลือก การรวบรวมต้นทุน CE</span><span class="sxs-lookup"><span data-stu-id="44e84-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="44e84-123">ในฟิลด์ ต้นทุนองค์ประกอบรอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-124">สำหรับตัวอย่างนี้ แม็ปต้นทุนองค์ประกอบรอง CC-007 ไปยังศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44e84-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="44e84-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="44e84-125">Click New.</span></span>
7. <span data-ttu-id="44e84-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44e84-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="44e84-127">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-128">เลือก 008</span><span class="sxs-lookup"><span data-stu-id="44e84-128">Select 008.</span></span>  
9. <span data-ttu-id="44e84-129">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-130">เลือก การรวบรวมต้นทุน CE</span><span class="sxs-lookup"><span data-stu-id="44e84-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="44e84-131">ในฟิลด์ ต้นทุนองค์ประกอบรอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-132">สำหรับตัวอย่างนี้ แม็ปต้นทุนองค์ประกอบรอง CC-008 ไปยังศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44e84-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="44e84-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="44e84-133">Click New.</span></span>
12. <span data-ttu-id="44e84-134">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="44e84-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="44e84-135">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-136">เลือก 009</span><span class="sxs-lookup"><span data-stu-id="44e84-136">Select 009.</span></span>  
14. <span data-ttu-id="44e84-137">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-138">เลือก การรวบรวมต้นทุน CE</span><span class="sxs-lookup"><span data-stu-id="44e84-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="44e84-139">ในฟิลด์ ต้นทุนองค์ประกอบรอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44e84-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="44e84-140">สำหรับตัวอย่างนี้ แม็ปต้นทุนองค์ประกอบรอง CC-009 ไปยังศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44e84-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="44e84-141">ทำต่อไปจนกว่าศูนย์ต้นทุนทั้งหมดจะถูกแม็ปไปยังองค์ประกอบต้นทุนรองที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="44e84-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="44e84-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="44e84-142">Click Save.</span></span>

