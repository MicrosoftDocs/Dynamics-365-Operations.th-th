---
title: สร้างและกำหนดนโยบายการปันส่วนต้นทุนสำหรับหน่วยการควบคุมต้นทุน
description: ใช้ขั้กระบวนงานนี้เพื่อสร้างและกำหนดนโยบายการปันส่วนต้นทุนและกฎที่สอดคล้องกันกับหน่วยการควบคุมต้นทุน
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cff10132e8007be885e9c69d97cf96c30d69f50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822866"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="68818-103">สร้างและกำหนดนโยบายการปันส่วนต้นทุนสำหรับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="68818-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68818-104">ใช้ขั้กระบวนงานนี้เพื่อสร้างและกำหนดนโยบายการปันส่วนต้นทุนและกฎที่สอดคล้องกันกับหน่วยการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="68818-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="68818-105">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="68818-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="68818-106">สร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="68818-106">Create a policy</span></span>
1. <span data-ttu-id="68818-107">ไปที่ การบัญชีต้นทุน > นโยบาย > นโยบายการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="68818-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="68818-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="68818-108">Click New.</span></span>
3. <span data-ttu-id="68818-109">ในฟิลด์ชื่อนโยบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="68818-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="68818-110">ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="68818-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="68818-111">เลือกองค์กร</span><span class="sxs-lookup"><span data-stu-id="68818-111">Select Organization.</span></span>  
5. <span data-ttu-id="68818-112">ในฟิลด์มิติทางสถิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="68818-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="68818-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="68818-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="68818-114">สร้างกฎการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="68818-114">Create allocation rules</span></span>
1. <span data-ttu-id="68818-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="68818-115">Click New.</span></span>
2. <span data-ttu-id="68818-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="68818-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="68818-117">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="68818-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="68818-118">ในฟิลด์ พฤติกรรมต้นทุน เลือก 'รวม'</span><span class="sxs-lookup"><span data-stu-id="68818-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="68818-119">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="68818-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="68818-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="68818-120">Click New.</span></span>
7. <span data-ttu-id="68818-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="68818-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="68818-122">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="68818-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="68818-123">ในฟิลด์ พฤติกรรมต้นทุน เลือก 'รวม'</span><span class="sxs-lookup"><span data-stu-id="68818-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="68818-124">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="68818-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="68818-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="68818-125">Click New.</span></span>
12. <span data-ttu-id="68818-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="68818-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="68818-127">ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="68818-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="68818-128">ในฟิลด์ พฤติกรรมต้นทุน เลือก 'รวม'</span><span class="sxs-lookup"><span data-stu-id="68818-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="68818-129">ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="68818-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="68818-130">ทำต่อไปจนกว่าคุณจะได้สร้างกฎทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="68818-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="68818-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="68818-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="68818-132">กำหนดนโยบายให้กับหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="68818-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="68818-133">คลิก การกำหนดนโยบายสำหรับหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="68818-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="68818-134">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="68818-134">Click New.</span></span>
3. <span data-ttu-id="68818-135">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="68818-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="68818-136">ในฟิลด์ มีผลบังคับใช้นับจากวันที่ทางการบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="68818-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="68818-137">กฎมีผลบังคับวันที่</span><span class="sxs-lookup"><span data-stu-id="68818-137">The rules are date-effective.</span></span> <span data-ttu-id="68818-138">ผู้ใช้หรือระบบอาจยกเลิกการใช้กฎได้ถ้ามีการสร้างเวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="68818-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="68818-139">ในฟิลด์หน่วยการควบคุมต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="68818-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="68818-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="68818-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]