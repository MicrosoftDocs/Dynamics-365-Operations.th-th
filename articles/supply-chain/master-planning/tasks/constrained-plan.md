---
title: จัดทำแผนที่มีข้อจำกัด
description: 'กระบวนงานนี้แสดงวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556034"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="f1e58-103">จัดทำแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="f1e58-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1e58-104">กระบวนงานนี้แสดงวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต </span><span class="sxs-lookup"><span data-stu-id="f1e58-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="f1e58-105">แผนช่วยให้มั่นใจว่าจะไม่เริ่มการผลิตก่อนที่จะมีวัสดุพร้อมใช้งานและทรัพยากรจะไม่ถูกจองเกินเวลา </span><span class="sxs-lookup"><span data-stu-id="f1e58-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="f1e58-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="f1e58-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f1e58-107">กระบวนงานนี้มีไว้สำหรับผู้วางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="f1e58-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="f1e58-108">ตั้งค่าแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="f1e58-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="f1e58-109">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="f1e58-109">Click Master planning.</span></span>
2. <span data-ttu-id="f1e58-110">คลิกที่แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f1e58-110">Click Master plans.</span></span>
3. <span data-ttu-id="f1e58-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f1e58-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f1e58-112">ตัวอย่างเช่น StaticPlan</span><span class="sxs-lookup"><span data-stu-id="f1e58-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="f1e58-113">เลือกใช่ในฟิลด์กำลังการผลิตที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="f1e58-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="f1e58-114">ในฟิลด์กรอบกำลังการผลิตที่มีจำกัด ให้ป้อน '30'</span><span class="sxs-lookup"><span data-stu-id="f1e58-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="f1e58-115">ขยายกรอบเวลาในส่วนของวัน</span><span class="sxs-lookup"><span data-stu-id="f1e58-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="f1e58-116">เลือกใช่ในฟิลด์กำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="f1e58-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="f1e58-117">ในฟิลด์กรอบเวลากำลังการผลิต(วัน) ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f1e58-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="f1e58-118">ตัวอย่างเช่น 60</span><span class="sxs-lookup"><span data-stu-id="f1e58-118">Example: 60</span></span>  
9. <span data-ttu-id="f1e58-119">เลือกใช่ในฟิลด์ความล่าช้าที่ถูกคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f1e58-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="f1e58-120">ในฟิลด์กรอบเวลากำลังการผลิต (วัน) ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f1e58-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="f1e58-121">ตัวอย่างเช่น 60</span><span class="sxs-lookup"><span data-stu-id="f1e58-121">Example: 60</span></span>  
11. <span data-ttu-id="f1e58-122">ขยายส่วนความล่าช้าที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="f1e58-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="f1e58-123">เลือกใช่ในฟิลด์เพิ่มความล่าช้าที่คำนวณไปยังวันที่ของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f1e58-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="f1e58-124">เลือกใช่ในฟิลด์เพิ่มความล่าช้าที่คำนวณไปยังวันที่ของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f1e58-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="f1e58-125">เลือกใช่ในฟิลด์เพิ่มความล่าช้าที่คำนวณไปยังวันที่ของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f1e58-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="f1e58-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f1e58-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="f1e58-127">สร้างแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="f1e58-127">Create a constrained plan</span></span>
1. <span data-ttu-id="f1e58-128">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="f1e58-128">Click Run.</span></span>
2. <span data-ttu-id="f1e58-129">ในฟิลด์แผนหลัก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f1e58-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="f1e58-130">เลือกแผนสำหรับข้อจำกัดซึ่งคุณได้ตั้งค่าไว้</span><span class="sxs-lookup"><span data-stu-id="f1e58-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="f1e58-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f1e58-131">Click OK.</span></span>
    * <span data-ttu-id="f1e58-132">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="f1e58-132">This may take a while.</span></span>  
4. <span data-ttu-id="f1e58-133">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="f1e58-133">Click Planned orders.</span></span>

