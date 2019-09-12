---
title: จัดทำแผนที่มีข้อจำกัด
description: หัวข้อนี้อธิบายวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b5d37de41fe68845cec3f2285aed2484ac117aa
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867184"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="c7f07-103">จัดทำแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="c7f07-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7f07-104">หัวข้อนี้อธิบายวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="c7f07-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="c7f07-105">แผนช่วยให้มั่นใจว่าจะไม่เริ่มการผลิตก่อนที่จะมีวัสดุพร้อมใช้งานและทรัพยากรจะไม่ถูกจองเกินเวลา </span><span class="sxs-lookup"><span data-stu-id="c7f07-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="c7f07-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c7f07-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c7f07-107">กระบวนงานนี้มีไว้สำหรับผู้วางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="c7f07-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="c7f07-108">ตั้งค่าแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="c7f07-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="c7f07-109">ในโฮมเพจ ให้เลือกพื้นที่ทำงาน **การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="c7f07-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="c7f07-110">เลือก **แผนหลัก** ในรายการของลิงค์ที่อยู่ด้านขวาสุดของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c7f07-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="c7f07-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c7f07-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="c7f07-112">ตัวอย่าง: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="c7f07-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="c7f07-113">เลือก **ใช่** ในฟิลด์ **กำลังการผลิตที่มีจำกัด**</span><span class="sxs-lookup"><span data-stu-id="c7f07-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="c7f07-114">ในฟิลด์ **กรอบกำลังการผลิตที่มีจำกัด** ให้ป้อน `30`</span><span class="sxs-lookup"><span data-stu-id="c7f07-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="c7f07-115">ขยายส่วน **กรอบเวลาเป็นจำนวนวัน**</span><span class="sxs-lookup"><span data-stu-id="c7f07-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="c7f07-116">เลือก **ใช่** ในฟิลด์ **กำลังการผลิต**</span><span class="sxs-lookup"><span data-stu-id="c7f07-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="c7f07-117">ในฟิลด์ **กรอบเวลาการจัดกำหนดการกำลังการผลิต (วัน)** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c7f07-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="c7f07-118">ตัวอย่าง: `60`</span><span class="sxs-lookup"><span data-stu-id="c7f07-118">Example: `60`</span></span>  
9. <span data-ttu-id="c7f07-119">เลือก **ใช่** ในฟิลด์ **ความล่าช้าที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="c7f07-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="c7f07-120">ในฟิลด์ **คำนวณกรอบเวลาความล่าช้า (วัน)** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c7f07-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="c7f07-121">ตัวอย่าง: `60`</span><span class="sxs-lookup"><span data-stu-id="c7f07-121">Example: `60`</span></span> 
11. <span data-ttu-id="c7f07-122">ขยายส่วน **ความล่าช้าที่มีการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="c7f07-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="c7f07-123">เลือก **ใช่** ในฟิลด์ **เพิ่มความล่าช้าที่มีการคำนวณไปยังวันที่ของความต้องการ** ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7f07-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="c7f07-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c7f07-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="c7f07-125">สร้างแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="c7f07-125">Create a constrained plan</span></span>
1. <span data-ttu-id="c7f07-126">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="c7f07-126">Select **Run**.</span></span>
2. <span data-ttu-id="c7f07-127">ในฟิลด์ **แผนหลัก** ให้ป้อนหรือเลือกแผนที่คุณได้ตั้งค่าข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="c7f07-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="c7f07-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c7f07-128">Select **OK**.</span></span>
4. <span data-ttu-id="c7f07-129">เลือก **แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="c7f07-129">Select **Planned orders**.</span></span>

