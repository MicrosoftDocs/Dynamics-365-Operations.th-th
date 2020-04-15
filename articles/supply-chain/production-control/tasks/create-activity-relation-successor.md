---
title: สร้างความสัมพันธ์กิจกรรม - งานที่เกิดขึ้นตามมา
description: 'ทิศทางของกิจกรรมในขั้นตอนการผลิตแบบ lean จะจัดทำเอกสารโดยใช้ความสัมพันธ์ของกิจกรรม '
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfd9d515b9417ce0142b7bf5db3485902968e4de
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149308"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="02cc4-103">สร้างความสัมพันธ์กิจกรรม - งานที่เกิดขึ้นตามมา</span><span class="sxs-lookup"><span data-stu-id="02cc4-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02cc4-104">ทิศทางของกิจกรรมในขั้นตอนการผลิตแบบ lean จะจัดทำเอกสารโดยใช้ความสัมพันธ์ของกิจกรรม </span><span class="sxs-lookup"><span data-stu-id="02cc4-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="02cc4-105">การบันทึกนี้แสดงวิธีการสร้างความสัมพันธ์ของกิจกรรม </span><span class="sxs-lookup"><span data-stu-id="02cc4-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="02cc4-106">ข้อกำหนดเบื้องต้น:</span><span class="sxs-lookup"><span data-stu-id="02cc4-106">Prerequisites:</span></span>

- <span data-ttu-id="02cc4-107">ขั้นตอนการผลิตและเวอร์ชันในโหมดร่าง</span><span class="sxs-lookup"><span data-stu-id="02cc4-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="02cc4-108">กิจกรรมสองที่ต่อเนื่องกันในขั้นตอนการผลิตถูกสร้างขึ้นแต่ไม่มีความเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="02cc4-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="02cc4-109">ค้นหาเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="02cc4-109">Find the production flow version</span></span> 
1. <span data-ttu-id="02cc4-110">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="02cc4-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="02cc4-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="02cc4-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="02cc4-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02cc4-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="02cc4-113">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02cc4-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="02cc4-114">ในรายการ ให้เลือกฟิลด์เวอร์ชันแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="02cc4-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="02cc4-115">คุณสามารถเพิ่มความสัมพันธ์ของกิจกรรมในฉบับร่างหรือเวอร์ชันที่ใช้งานอยู่ของขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="02cc4-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="02cc4-116">เปิดภาพรวมกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="02cc4-116">Open the activity overview</span></span>
1. <span data-ttu-id="02cc4-117">คลิกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="02cc4-117">Click Activities.</span></span>
    * <span data-ttu-id="02cc4-118">โปรดสังเกตว่า แบบฟอร์มจะแสดงกิจกรรมทั้งหมดของขั้นตอนการผลิตที่ปันส่วนไปยังเวอร์ชันขั้นตอนการผลิตที่คุณกำลังทำงาน</span><span class="sxs-lookup"><span data-stu-id="02cc4-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="02cc4-119">เพิ่มงานที่เกิดขึ้นตามมา</span><span class="sxs-lookup"><span data-stu-id="02cc4-119">Add a Successor</span></span>
1. <span data-ttu-id="02cc4-120">คลิกเพิ่มงานที่เกิดขึ้นตามมา</span><span class="sxs-lookup"><span data-stu-id="02cc4-120">Click Add successor.</span></span>
2. <span data-ttu-id="02cc4-121">ในฟิลด์กิจกรรม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="02cc4-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="02cc4-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="02cc4-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="02cc4-123">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02cc4-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="02cc4-124">เลือกกล่องกาเครื่องหมายข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="02cc4-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="02cc4-125">ในฟิลด์ค่าข้อจำกัด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="02cc4-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="02cc4-126">ข้อจำกัดเวลาคือเวลาจะถูกกำหนดระหว่างการสิ้นสุดตามกำหนดการที่เกิดขึ้นก่อนหน้า (วันและเวลาครบกำหนด) และเวลาเริ่มต้นตามกำหนดการจะเกิดขึ้นตามมา</span><span class="sxs-lookup"><span data-stu-id="02cc4-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="02cc4-127">ในฟิลด์หน่วย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="02cc4-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="02cc4-128">ในฟิลด์อัตราส่วนเวลาวงจร ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="02cc4-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="02cc4-129">ถ้าทั้งสองกิจกรรมรันที่สมดุลเดียวกัน อัตราส่วนเวลาวงจรควรจะเป็น 1</span><span class="sxs-lookup"><span data-stu-id="02cc4-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="02cc4-130">ถ้าก่อนหน้าการทำงานรันด้วยความเร็วสองครั้งของการเกิดขึ้นตามมา อัตราส่วนควรจะเป็น 2</span><span class="sxs-lookup"><span data-stu-id="02cc4-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="02cc4-131">อัตราส่วนเวลาวงจรจะใช้เพื่อคำนวณเวลาวงจรแต่ละรอบของกิจกรรมขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="02cc4-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="02cc4-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="02cc4-132">Click OK.</span></span>
10. <span data-ttu-id="02cc4-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02cc4-133">Close the page.</span></span>
11. <span data-ttu-id="02cc4-134">คลิกแท็บ GridPanel</span><span class="sxs-lookup"><span data-stu-id="02cc4-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="02cc4-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02cc4-135">Close the page.</span></span>
13. <span data-ttu-id="02cc4-136">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="02cc4-136">Refresh the page.</span></span>

