---
title: การสร้างเท็มเพลตเวลาการทำงาน
description: เท็มเพลตเวลาการทำงานกำหนดชั่วโมงการทำงานตลอดทั้งสัปดาห์ และใช้เพื่อสร้างระยะเวลาทำงานแบบเป็นช่วงเวลา
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920940"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="15369-103">การสร้างเท็มเพลตเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="15369-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15369-104">เท็มเพลตเวลาการทำงานกำหนดชั่วโมงการทำงานตลอดทั้งสัปดาห์ และใช้เพื่อสร้างระยะเวลาทำงานแบบเป็นช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="15369-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="15369-105">ขั้นตอนนี้แสดงวิธีการกำหนดเท็มเพลตเวลาการทำงานโดยใช้เวลาทำงานที่จัดสรรตามคุณสมบัติสำหรับการจัดประเภทช่วงเวลาทำงาน </span><span class="sxs-lookup"><span data-stu-id="15369-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="15369-106">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="15369-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="15369-107">ไปที่ **พื้นที่ทำงาน > การจัดการรอบการใช้งานทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="15369-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="15369-108">เลือก **เท็มเพลตเวลาการทำงาน**</span><span class="sxs-lookup"><span data-stu-id="15369-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="15369-109">สร้างเท็มเพลตเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="15369-109">Create working time template</span></span>

1. <span data-ttu-id="15369-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="15369-110">Select **New**.</span></span>
1. <span data-ttu-id="15369-111">ในฟิลด์ **เท็มเพลตเวลาการทำงาน** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="15369-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="15369-112">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="15369-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="15369-113">ขยายส่วน **วันจันทร์**</span><span class="sxs-lookup"><span data-stu-id="15369-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="15369-114">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="15369-114">Select **Add**.</span></span>
1. <span data-ttu-id="15369-115">ในฟิลด์ **ตั้งแต่** ให้ป้อนเวลา</span><span class="sxs-lookup"><span data-stu-id="15369-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="15369-116">ระบุเวลาเริ่มทำงานในตอนเช้า</span><span class="sxs-lookup"><span data-stu-id="15369-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="15369-117">ในฟิลด์ **จนถึง** ให้ป้อนเวลา</span><span class="sxs-lookup"><span data-stu-id="15369-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="15369-118">ระบุเวลาที่พนักงานพักกลางวัน</span><span class="sxs-lookup"><span data-stu-id="15369-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="15369-119">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="15369-119">Select **Add**.</span></span>
1. <span data-ttu-id="15369-120">ในฟิลด์ **ตั้งแต่** ให้ป้อนเวลา</span><span class="sxs-lookup"><span data-stu-id="15369-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="15369-121">ระบุเวลาที่เริ่มทำงานหลังจากพักกลางวัน</span><span class="sxs-lookup"><span data-stu-id="15369-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="15369-122">ในฟิลด์ **จนถึง** ให้ป้อนเวลา</span><span class="sxs-lookup"><span data-stu-id="15369-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="15369-123">ระบุการสิ้นสุดของวันทำงาน</span><span class="sxs-lookup"><span data-stu-id="15369-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="15369-124">ใช้เวลาทำงานนี้กับวันทำการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="15369-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="15369-125">เลือก **คัดลอกวัน**</span><span class="sxs-lookup"><span data-stu-id="15369-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="15369-126">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันอังคาร</span><span class="sxs-lookup"><span data-stu-id="15369-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="15369-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="15369-127">Select **OK**.</span></span>
1. <span data-ttu-id="15369-128">เลือก **คัดลอกวัน**</span><span class="sxs-lookup"><span data-stu-id="15369-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="15369-129">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันพุธ</span><span class="sxs-lookup"><span data-stu-id="15369-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="15369-130">ในฟิลด์ **จนถึงวันทำการ** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="15369-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="15369-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="15369-131">Select **OK**.</span></span>
1. <span data-ttu-id="15369-132">เลือก **คัดลอกวัน**</span><span class="sxs-lookup"><span data-stu-id="15369-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="15369-133">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันพฤหัสบดี</span><span class="sxs-lookup"><span data-stu-id="15369-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="15369-134">ในฟิลด์ **จนถึงวันทำการ** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="15369-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="15369-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="15369-135">Select **OK**.</span></span>
1. <span data-ttu-id="15369-136">เลือก **คัดลอกวัน**</span><span class="sxs-lookup"><span data-stu-id="15369-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="15369-137">คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงศุกร์</span><span class="sxs-lookup"><span data-stu-id="15369-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="15369-138">ในฟิลด์ **จนถึงวันทำการ** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="15369-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="15369-139">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="15369-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="15369-140">กำหนดช่วงเวลาสำหรับการดำเนินงานพิเศษ</span><span class="sxs-lookup"><span data-stu-id="15369-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="15369-141">ขยายส่วน **วันศุกร์**</span><span class="sxs-lookup"><span data-stu-id="15369-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="15369-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="15369-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="15369-143">ในฟิลด์ **คุณสมบัติ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="15369-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="15369-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="15369-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="15369-145">ในฟิลด์ **คุณสมบัติ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="15369-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="15369-146">ทำเครื่องหมายในวันสุดสัปดาห์เป็นปิดการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="15369-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="15369-147">ขยายส่วน **วันเสาร์**</span><span class="sxs-lookup"><span data-stu-id="15369-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="15369-148">เลือก *ใช่* ในฟิลด์ **ปิดสำหรับการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="15369-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="15369-149">ขยายส่วน **วันอาทิตย์**</span><span class="sxs-lookup"><span data-stu-id="15369-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="15369-150">เลือก *ใช่* ในฟิลด์ **ปิดสำหรับการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="15369-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]