---
title: สร้างและกำหนดนโยบายการกระจายต้นทุนสำหรับหน่วยการควบคุมต้นทุน
description: กฎการกระจายต้นทุนถูกใช้เพื่อกระจายต้นทุนที่มีการตรวจนับทางการเงินในศูนย์ต้นทุนรวม
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
ms.openlocfilehash: 1d040f9495c7fb36985b5f96c15ac43aa226da24
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841332"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="c7395-103">สร้างและกำหนดนโยบายการกระจายต้นทุนสำหรับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c7395-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7395-104">กฎการกระจายต้นทุนถูกใช้เพื่อกระจายต้นทุนที่มีการตรวจนับทางการเงินในศูนย์ต้นทุนรวม</span><span class="sxs-lookup"><span data-stu-id="c7395-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="c7395-105">นักบัญชีต้นทุนตรวจสอบให้แน่ใจว่ามีการกระจายต้นทุนไปยังศูนย์ต้นทุนโดยขึ้นอยู่กับฐานการปันส่วนที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c7395-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="c7395-106">นโยบายและกฎที่สอดคล้องกันถูกกำหนดให้กับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c7395-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="c7395-107">คู่มืองานนี้ใช้ตัวอย่างในการแสดงวิธีการสร้างนโยบายการกระจายต้นทุนและกฎที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="c7395-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="c7395-108">สร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="c7395-108">Create a policy</span></span>
1. <span data-ttu-id="c7395-109">ไปที่ การบัญชีต้นทุน > นโยบาย > นโยบายการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c7395-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="c7395-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c7395-110">Click New.</span></span>
3. <span data-ttu-id="c7395-111">ในฟิลด์ชื่อนโยบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="c7395-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c7395-113">ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c7395-114">เลือกองค์กร</span><span class="sxs-lookup"><span data-stu-id="c7395-114">Select Organization.</span></span>  
6. <span data-ttu-id="c7395-115">ในฟิลด์ลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c7395-116">เลือก CDS P/L</span><span class="sxs-lookup"><span data-stu-id="c7395-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="c7395-117">ในฟิลด์มิติทางสถิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c7395-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="c7395-118">เลือก องค์ประกอบทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="c7395-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="c7395-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c7395-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="c7395-120">สร้างกฎสำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="c7395-120">Create rules for the policy</span></span>
1. <span data-ttu-id="c7395-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c7395-121">Click New.</span></span>
2. <span data-ttu-id="c7395-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c7395-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c7395-123">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c7395-124">ขยายทั้งลำดับชั้นเพื่อเลือก 094</span><span class="sxs-lookup"><span data-stu-id="c7395-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="c7395-125">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c7395-126">เลือกค่าใช้จ่ายการดำเนินงานอื่น และจากนั้นเลือกการทำความสะอาด 605110</span><span class="sxs-lookup"><span data-stu-id="c7395-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="c7395-127">ในฟิลด์พฤติกรรมต้นทุน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c7395-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="c7395-128">เลือก ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c7395-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="c7395-129">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c7395-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="c7395-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c7395-130">Click New.</span></span>
8. <span data-ttu-id="c7395-131">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c7395-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c7395-132">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c7395-133">ขยายทั้งลำดับชั้นเพื่อเลือก 094</span><span class="sxs-lookup"><span data-stu-id="c7395-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="c7395-134">ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c7395-135">เลือกค่าใช้จ่ายการดำเนินงานอื่น และจากนั้นเลือก 605150 ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="c7395-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="c7395-136">ในฟิลด์พฤติกรรมต้นทุน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c7395-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="c7395-137">เลือก ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c7395-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="c7395-138">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c7395-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="c7395-139">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c7395-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="c7395-140">กำหนดกฎให้กับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c7395-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="c7395-141">คลิก การกำหนดนโยบายสำหรับหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c7395-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="c7395-142">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c7395-142">Click New.</span></span>
3. <span data-ttu-id="c7395-143">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c7395-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c7395-144">ในฟิลด์ มีผลบังคับใช้นับจากวันที่ทางการบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c7395-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="c7395-145">เลือก วันที่ 1 กันยายนในปีบัญชีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c7395-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="c7395-146">ในฟิลด์หน่วยการควบคุมต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c7395-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="c7395-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c7395-147">Click Save.</span></span>

