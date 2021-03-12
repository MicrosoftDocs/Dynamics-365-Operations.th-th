---
title: สร้างและกำหนดนโยบายการปันส่วนต้นทุนสำหรับหน่วยการควบคุมต้นทุน
description: ใช้ขั้กระบวนงานนี้เพื่อสร้างและกำหนดนโยบายการปันส่วนต้นทุนและกฎที่สอดคล้องกันกับหน่วยการควบคุมต้นทุน
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006310d07dfa5b75941ca248736800bbb9e8e7b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969339"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="e3973-103">สร้างและกำหนดนโยบายการปันส่วนต้นทุนสำหรับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e3973-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3973-104">ใช้ขั้กระบวนงานนี้เพื่อสร้างและกำหนดนโยบายการปันส่วนต้นทุนและกฎที่สอดคล้องกันกับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e3973-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="e3973-105">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="e3973-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="e3973-106">สร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="e3973-106">Create a policy</span></span>
1. <span data-ttu-id="e3973-107">ไปที่ การบัญชีต้นทุน > นโยบาย > นโยบายการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e3973-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="e3973-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e3973-108">Click New.</span></span>
3. <span data-ttu-id="e3973-109">ในฟิลด์ชื่อนโยบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e3973-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="e3973-110">ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e3973-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="e3973-111">เลือกองค์กร</span><span class="sxs-lookup"><span data-stu-id="e3973-111">Select Organization.</span></span>  
5. <span data-ttu-id="e3973-112">ในฟิลด์มิติทางสถิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3973-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="e3973-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e3973-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="e3973-114">สร้างกฎการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e3973-114">Create allocation rules</span></span>
1. <span data-ttu-id="e3973-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e3973-115">Click New.</span></span>
2. <span data-ttu-id="e3973-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e3973-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e3973-117">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e3973-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="e3973-118">ในฟิลด์ พฤติกรรมต้นทุน เลือก 'รวม'</span><span class="sxs-lookup"><span data-stu-id="e3973-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="e3973-119">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3973-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="e3973-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e3973-120">Click New.</span></span>
7. <span data-ttu-id="e3973-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e3973-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="e3973-122">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e3973-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="e3973-123">ในฟิลด์ พฤติกรรมต้นทุน เลือก 'รวม'</span><span class="sxs-lookup"><span data-stu-id="e3973-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="e3973-124">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3973-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="e3973-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e3973-125">Click New.</span></span>
12. <span data-ttu-id="e3973-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e3973-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="e3973-127">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e3973-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="e3973-128">ในฟิลด์ พฤติกรรมต้นทุน เลือก 'รวม'</span><span class="sxs-lookup"><span data-stu-id="e3973-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="e3973-129">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e3973-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="e3973-130">ทำต่อไปจนกว่าคุณจะได้สร้างกฎทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e3973-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="e3973-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e3973-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="e3973-132">กำหนดนโยบายให้กับหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e3973-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="e3973-133">คลิก การกำหนดนโยบายสำหรับหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e3973-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="e3973-134">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e3973-134">Click New.</span></span>
3. <span data-ttu-id="e3973-135">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e3973-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e3973-136">ในฟิลด์ มีผลบังคับใช้นับจากวันที่ทางการบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="e3973-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="e3973-137">กฎมีผลบังคับวันที่</span><span class="sxs-lookup"><span data-stu-id="e3973-137">The rules are date-effective.</span></span> <span data-ttu-id="e3973-138">ผู้ใช้หรือระบบอาจยกเลิกการใช้กฎได้ถ้ามีการสร้างเวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="e3973-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="e3973-139">ในฟิลด์หน่วยการควบคุมต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e3973-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="e3973-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e3973-140">Click Save.</span></span>

