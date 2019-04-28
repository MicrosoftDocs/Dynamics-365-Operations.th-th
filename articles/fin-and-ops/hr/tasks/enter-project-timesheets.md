---
title: ป้อนแผ่นเวลาโครงการ
description: 'ขั้นตอนนี้ช่วยให้คุณสร้างแผ่นเวลา โดยใช้แบบฟอร์มที่มีแผ่นเวลาที่ว่างเปล่า '
author: andreabichsel
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1be02f0080ee23359ad905b1e997d8cd5adfd2
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "859148"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="32b1c-103">ป้อนแผ่นเวลาโครงการ</span><span class="sxs-lookup"><span data-stu-id="32b1c-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32b1c-104">ขั้นตอนนี้ช่วยให้คุณสร้างแผ่นเวลา โดยใช้แบบฟอร์มที่มีแผ่นเวลาที่ว่างเปล่า </span><span class="sxs-lookup"><span data-stu-id="32b1c-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="32b1c-105">แผ่นเวลาใหม่สามารถยึดตามข้อมูลจากแผ่นเวลาก่อนหน้านี้ หรือการกำหนดโครงการและกิจกรรมในหน้ารายการโปรดของฉันก็ได้ </span><span class="sxs-lookup"><span data-stu-id="32b1c-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="32b1c-106">โดยค่าเริ่มต้น หน้ารายการแผ่นเวลาทั้งหมดแสดงแผ่นเวลาทั้งหมดของคุณสำหรับรอบระยะเวลาปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="32b1c-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="32b1c-107">คุณสามารถใช้รายการดร็อปดาวน์สำหรับฟิลด์แสดงในหน้าแผ่นเวลาของฉัน เพื่อกรองรายการแผ่นเวลาตามรอบระยะเวลาหรือโครงการ หรือดูแผ่นเวลาที่ถูกสร้างขึ้นในนามของผู้ปฏิบัติงานอื่นๆ </span><span class="sxs-lookup"><span data-stu-id="32b1c-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="32b1c-108">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างขั้นตอนนี้คือ USSI </span><span class="sxs-lookup"><span data-stu-id="32b1c-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="32b1c-109">เมื่อต้องการเริ่มต้นขั้นตอนนี้ ไปที่การจัดการโครงการและบัญชี > แผ่นเวลา > แผ่นเวลาของฉัน</span><span class="sxs-lookup"><span data-stu-id="32b1c-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="32b1c-110">ป้อนแผ่นเวลาใหม่ โดยคลิกสร้าง</span><span class="sxs-lookup"><span data-stu-id="32b1c-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="32b1c-111">รายการดร็อปดาวน์ของทรัพยากรแสดงผู้ปฏิบัติงานที่มอบหมายให้กับผู้ใช้ปัจจุบัน ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32b1c-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="32b1c-112">ถ้ามีกำหนดผู้ใช้เป็นผู้รับมอบสิทธิ์ มันจะแสดงรายชื่อเพื่อให้ผู้ใช้สามารถป้อนแผ่นเวลาในนามของผู้ใต้บังคับบัญชา</span><span class="sxs-lookup"><span data-stu-id="32b1c-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="32b1c-113">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="32b1c-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="32b1c-114">ถ้าเลือกตัวเลือกนี้ จะมีสร้างรายการแผ่นเวลาใหม่ โดยใช้การตั้งค่าแผ่นเวลาที่มีการตั้งค่าคอนฟิกเป็นรายการโปรด</span><span class="sxs-lookup"><span data-stu-id="32b1c-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="32b1c-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="32b1c-115">Click OK.</span></span>
4. <span data-ttu-id="32b1c-116">คลิกรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="32b1c-116">Click New line.</span></span>
5. <span data-ttu-id="32b1c-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="32b1c-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="32b1c-118">ฟิลด์นิติบุคคลแสดงนิติบุคคลล่าสุดโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32b1c-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="32b1c-119">ในฟิลด์โครงการ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="32b1c-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="32b1c-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="32b1c-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="32b1c-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="32b1c-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="32b1c-122">ในฟิลด์กิจกรรม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="32b1c-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="32b1c-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="32b1c-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="32b1c-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="32b1c-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="32b1c-125">ในฟิลด์ประเภท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="32b1c-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="32b1c-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="32b1c-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="32b1c-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="32b1c-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="32b1c-128">ป้อนจำนวนชั่วโมงที่ทำงานในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="32b1c-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="32b1c-129">ควรป้อนชั่วโมงในรูปแบบทศนิยม </span><span class="sxs-lookup"><span data-stu-id="32b1c-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="32b1c-130">ตัวอย่างเช่น ถ้าคุณเคยทำงานสองชั่วโมงสิบห้านาที ป้อน 2.25</span><span class="sxs-lookup"><span data-stu-id="32b1c-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="32b1c-131">ป้อนจำนวนชั่วโมงที่ทำงานในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="32b1c-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="32b1c-132">ควรป้อนชั่วโมงในรูปแบบทศนิยม </span><span class="sxs-lookup"><span data-stu-id="32b1c-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="32b1c-133">ตัวอย่างเช่น ถ้าคุณเคยทำงานสองชั่วโมงสิบห้านาที ป้อน 2.25</span><span class="sxs-lookup"><span data-stu-id="32b1c-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="32b1c-134">ป้อนจำนวนชั่วโมงที่ทำงานในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="32b1c-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="32b1c-135">ควรป้อนชั่วโมงในรูปแบบทศนิยม </span><span class="sxs-lookup"><span data-stu-id="32b1c-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="32b1c-136">ตัวอย่างเช่น ถ้าคุณเคยทำงานสองชั่วโมงสิบห้านาที ป้อน 2.25</span><span class="sxs-lookup"><span data-stu-id="32b1c-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="32b1c-137">ป้อนจำนวนชั่วโมงที่ทำงานในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="32b1c-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="32b1c-138">ควรป้อนชั่วโมงในรูปแบบทศนิยม </span><span class="sxs-lookup"><span data-stu-id="32b1c-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="32b1c-139">ตัวอย่างเช่น ถ้าคุณเคยทำงานสองชั่วโมงสิบห้านาที ป้อน 2.25</span><span class="sxs-lookup"><span data-stu-id="32b1c-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="32b1c-140">ป้อนจำนวนชั่วโมงที่ทำงานในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="32b1c-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="32b1c-141">ควรป้อนชั่วโมงในรูปแบบทศนิยม </span><span class="sxs-lookup"><span data-stu-id="32b1c-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="32b1c-142">ตัวอย่างเช่น ถ้าคุณเคยทำงานสองชั่วโมงสิบห้านาที ป้อน 2.25</span><span class="sxs-lookup"><span data-stu-id="32b1c-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="32b1c-143">ในรายละเอียดรายการ ตัวเลือกต่อไปนี้จะพร้อมใช้งาน: o เพิ่มข้อมูลเกี่ยวกับภาษีและมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="32b1c-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="32b1c-144">o เพิ่มข้อคิดเห็นเกี่ยวกับรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="32b1c-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="32b1c-145">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="32b1c-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="32b1c-146">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="32b1c-146">Click Submit.</span></span>
22. <span data-ttu-id="32b1c-147">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="32b1c-147">Click Submit.</span></span>

