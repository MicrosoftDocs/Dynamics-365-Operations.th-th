--- 
title: "จัดทำแผนที่มีข้อจำกัด"
description: "กระบวนงานนี้แสดงวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต "
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9deb615d05b90865ea6a050599bf91879b5688d0
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="53daf-103">จัดทำแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="53daf-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53daf-104">กระบวนงานนี้แสดงวิธีการสร้างแผนที่พิจารณาทั้งข้อจำกัดของวัสดุและกำลังการผลิต </span><span class="sxs-lookup"><span data-stu-id="53daf-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="53daf-105">แผนช่วยให้มั่นใจว่าจะไม่เริ่มการผลิตก่อนที่จะมีวัสดุพร้อมใช้งานและทรัพยากรจะไม่ถูกจองเกินเวลา </span><span class="sxs-lookup"><span data-stu-id="53daf-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="53daf-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="53daf-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="53daf-107">กระบวนงานนี้มีไว้สำหรับผู้วางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="53daf-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="53daf-108">ตั้งค่าแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="53daf-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="53daf-109">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="53daf-109">Click Master planning.</span></span>
2. <span data-ttu-id="53daf-110">คลิกที่แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="53daf-110">Click Master plans.</span></span>
3. <span data-ttu-id="53daf-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="53daf-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="53daf-112">ตัวอย่างเช่น StaticPlan</span><span class="sxs-lookup"><span data-stu-id="53daf-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="53daf-113">เลือกใช่ในฟิลด์กำลังการผลิตที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="53daf-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="53daf-114">ในฟิลด์กรอบกำลังการผลิตที่มีจำกัด ให้ป้อน '30'</span><span class="sxs-lookup"><span data-stu-id="53daf-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="53daf-115">ขยายกรอบเวลาในส่วนของวัน</span><span class="sxs-lookup"><span data-stu-id="53daf-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="53daf-116">เลือกใช่ในฟิลด์กำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="53daf-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="53daf-117">ในฟิลด์กรอบเวลากำลังการผลิต(วัน) ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="53daf-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="53daf-118">ตัวอย่างเช่น 60</span><span class="sxs-lookup"><span data-stu-id="53daf-118">Example: 60</span></span>  
9. <span data-ttu-id="53daf-119">เลือกใช่ในฟิลด์ความล่าช้าที่ถูกคำนวณ</span><span class="sxs-lookup"><span data-stu-id="53daf-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="53daf-120">ในฟิลด์กรอบเวลากำลังการผลิต (วัน) ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="53daf-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="53daf-121">ตัวอย่างเช่น 60</span><span class="sxs-lookup"><span data-stu-id="53daf-121">Example: 60</span></span>  
11. <span data-ttu-id="53daf-122">ขยายส่วนความล่าช้าที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="53daf-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="53daf-123">เลือกใช่ในฟิลด์เพิ่มความล่าช้าที่คำนวณไปยังวันที่ของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="53daf-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="53daf-124">เลือกใช่ในฟิลด์เพิ่มความล่าช้าที่คำนวณไปยังวันที่ของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="53daf-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="53daf-125">เลือกใช่ในฟิลด์เพิ่มความล่าช้าที่คำนวณไปยังวันที่ของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="53daf-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="53daf-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="53daf-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="53daf-127">สร้างแผนที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="53daf-127">Create a constrained plan</span></span>
1. <span data-ttu-id="53daf-128">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="53daf-128">Click Run.</span></span>
2. <span data-ttu-id="53daf-129">ในฟิลด์แผนหลัก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="53daf-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="53daf-130">เลือกแผนสำหรับข้อจำกัดซึ่งคุณได้ตั้งค่าไว้</span><span class="sxs-lookup"><span data-stu-id="53daf-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="53daf-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="53daf-131">Click OK.</span></span>
    * <span data-ttu-id="53daf-132">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="53daf-132">This may take a while.</span></span>  
4. <span data-ttu-id="53daf-133">คลิกที่แผนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="53daf-133">Click Planned orders.</span></span>


