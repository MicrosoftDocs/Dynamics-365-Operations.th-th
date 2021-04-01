---
title: การสร้างเท็มเพลตเวลาการทำงาน
description: เท็มเพลตเวลาการทำงานกำหนดชั่วโมงการทำงานตลอดทั้งสัปดาห์ และใช้เพื่อสร้างระยะเวลาทำงานแบบเป็นช่วงเวลา
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9829e91500abf8cba3f7cbfe2f89863cb2b1f4c4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257374"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="f5b66-103">การสร้างเท็มเพลตเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f5b66-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5b66-104">เท็มเพลตเวลาการทำงานกำหนดชั่วโมงการทำงานตลอดทั้งสัปดาห์ และใช้เพื่อสร้างระยะเวลาทำงานแบบเป็นช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="f5b66-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="f5b66-105">ขั้นตอนนี้แสดงวิธีการกำหนดเท็มเพลตเวลาการทำงานโดยใช้เวลาทำงานที่จัดสรรตามคุณสมบัติสำหรับการจัดประเภทช่วงเวลาทำงาน </span><span class="sxs-lookup"><span data-stu-id="f5b66-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="f5b66-106">คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="f5b66-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="f5b66-107">ไปที่พื้นที่ทำงานทั้งหมด > การจัดการรอบการใช้งานทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="f5b66-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="f5b66-108">คลิกเท็มเพลตเวลาการทำงาน </span><span class="sxs-lookup"><span data-stu-id="f5b66-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="f5b66-109">สร้างเท็มเพลตเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="f5b66-109">Create working time template</span></span>
1. <span data-ttu-id="f5b66-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f5b66-110">Click New.</span></span>
2. <span data-ttu-id="f5b66-111">ในฟิลด์เท็มเพลตเวลาการทำงาน พิมพ์มูลค่า </span><span class="sxs-lookup"><span data-stu-id="f5b66-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="f5b66-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="f5b66-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f5b66-113">ขยายส่วนวันจันทร์ </span><span class="sxs-lookup"><span data-stu-id="f5b66-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="f5b66-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f5b66-114">Click Add.</span></span>
6. <span data-ttu-id="f5b66-115">ในฟิลด์ตั้งแต่ ให้ป้อนเวลา</span><span class="sxs-lookup"><span data-stu-id="f5b66-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="f5b66-116">ระบุเวลาเริ่มทำงานในตอนเช้า</span><span class="sxs-lookup"><span data-stu-id="f5b66-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="f5b66-117">ในฟิลด์จนถึง ให้ป้อนเวลา </span><span class="sxs-lookup"><span data-stu-id="f5b66-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="f5b66-118">ระบุเวลาที่พนักงานพักกลางวัน</span><span class="sxs-lookup"><span data-stu-id="f5b66-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="f5b66-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f5b66-119">Click Add.</span></span>
9. <span data-ttu-id="f5b66-120">ในฟิลด์ตั้งแต่ ให้ป้อนเวลา</span><span class="sxs-lookup"><span data-stu-id="f5b66-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="f5b66-121">ระบุเวลาที่เริ่มทำงานหลังจากพักกลางวัน</span><span class="sxs-lookup"><span data-stu-id="f5b66-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="f5b66-122">ในฟิลด์จนถึง ให้ป้อนเวลา </span><span class="sxs-lookup"><span data-stu-id="f5b66-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="f5b66-123">ระบุการสิ้นสุดของวันทำงาน</span><span class="sxs-lookup"><span data-stu-id="f5b66-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="f5b66-124">ใช้เวลาทำงานนี้กับวันทำการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f5b66-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="f5b66-125">คลิกคัดลอกวัน</span><span class="sxs-lookup"><span data-stu-id="f5b66-125">Click Copy day.</span></span>
    * <span data-ttu-id="f5b66-126">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันอังคาร</span><span class="sxs-lookup"><span data-stu-id="f5b66-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="f5b66-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f5b66-127">Click OK.</span></span>
3. <span data-ttu-id="f5b66-128">คลิกคัดลอกวัน</span><span class="sxs-lookup"><span data-stu-id="f5b66-128">Click Copy day.</span></span>
    * <span data-ttu-id="f5b66-129">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันพุธ</span><span class="sxs-lookup"><span data-stu-id="f5b66-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="f5b66-130">ในฟิลด์จนถึงวันทำการ ให้เลือกตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="f5b66-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="f5b66-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f5b66-131">Click OK.</span></span>
6. <span data-ttu-id="f5b66-132">คลิกคัดลอกวัน</span><span class="sxs-lookup"><span data-stu-id="f5b66-132">Click Copy day.</span></span>
    * <span data-ttu-id="f5b66-133">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันพฤหัสบดี</span><span class="sxs-lookup"><span data-stu-id="f5b66-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="f5b66-134">ในฟิลด์จนถึงวันทำการ ให้เลือกตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="f5b66-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="f5b66-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f5b66-135">Click OK.</span></span>
9. <span data-ttu-id="f5b66-136">คลิกคัดลอกวัน</span><span class="sxs-lookup"><span data-stu-id="f5b66-136">Click Copy day.</span></span>
    * <span data-ttu-id="f5b66-137">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงศุกร์</span><span class="sxs-lookup"><span data-stu-id="f5b66-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="f5b66-138">ในฟิลด์จนถึงวันทำการ ให้เลือกตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="f5b66-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="f5b66-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f5b66-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="f5b66-140">กำหนดช่วงเวลาสำหรับการดำเนินงานพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f5b66-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="f5b66-141">ขยายส่วนวันศุกร์</span><span class="sxs-lookup"><span data-stu-id="f5b66-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="f5b66-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f5b66-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f5b66-143">ในฟิลด์คุณสมบัติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f5b66-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="f5b66-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f5b66-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f5b66-145">ในฟิลด์คุณสมบัติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="f5b66-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="f5b66-146">ทำเครื่องหมายในวันสุดสัปดาห์เป็นปิดการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="f5b66-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="f5b66-147">ขยายส่วนวันเสาร์ </span><span class="sxs-lookup"><span data-stu-id="f5b66-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="f5b66-148">เลือกใช่ในฟิลด์ปิดการเบิกสินค้า </span><span class="sxs-lookup"><span data-stu-id="f5b66-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="f5b66-149">ขยายส่วนวันอาทิตย์ </span><span class="sxs-lookup"><span data-stu-id="f5b66-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="f5b66-150">เลือกใช่ในฟิลด์ปิดการเบิกสินค้า </span><span class="sxs-lookup"><span data-stu-id="f5b66-150">Select Yes in the Closed for pickup field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]