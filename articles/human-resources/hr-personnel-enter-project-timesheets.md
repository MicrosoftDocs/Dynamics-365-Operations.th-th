---
title: ป้อนแผ่นเวลาโครงการ
description: 'ขั้นตอนนี้ช่วยให้คุณสร้างแผ่นเวลา โดยใช้แบบฟอร์มที่มีแผ่นเวลาที่ว่างเปล่า '
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 136efa1178089adb88820002a19e99ef83e1b47e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010765"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="2819a-103">ป้อนแผ่นเวลาโครงการ</span><span class="sxs-lookup"><span data-stu-id="2819a-103">Enter project timesheets</span></span>



<span data-ttu-id="2819a-104">ขั้นตอนนี้ช่วยให้คุณสร้างแผ่นเวลา โดยใช้แบบฟอร์มที่มีแผ่นเวลาที่ว่างเปล่า </span><span class="sxs-lookup"><span data-stu-id="2819a-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="2819a-105">แผ่นเวลาใหม่สามารถยึดตามข้อมูลจากแผ่นเวลาก่อนหน้านี้ หรือจากการกำหนดโครงการและกิจกรรมในหน้า **รายการโปรดของฉัน**</span><span class="sxs-lookup"><span data-stu-id="2819a-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="2819a-106">โดยค่าเริ่มต้น หน้ารายการ **แผ่นเวลาทั้งหมด** แสดงแผ่นเวลาทั้งหมดของคุณสำหรับรอบระยะเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2819a-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="2819a-107">คุณสามารถใช้รายการดรอปดาวน์สำหรับฟิลด์ **แสดง** ในหน้า **แผ่นเวลาของฉัน** เพื่อกรองรายการแผ่นเวลาตามรอบระยะเวลาหรือโครงการ หรือเพื่อดูแผ่นเวลาที่ถูกสร้างขึ้นในนามของผู้ปฏิบัติงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2819a-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="2819a-108">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างขั้นตอนนี้คือ USSI </span><span class="sxs-lookup"><span data-stu-id="2819a-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="2819a-109">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > แผ่นเวลา > แผ่นเวลาของฉัน**</span><span class="sxs-lookup"><span data-stu-id="2819a-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="2819a-110">เพื่อป้อนแผ่นเวลาใหม่ คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2819a-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="2819a-111">รายการดร็อปดาวน์ของทรัพยากรแสดงผู้ปฏิบัติงานที่มอบหมายให้กับผู้ใช้ปัจจุบัน ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2819a-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="2819a-112">ถ้ามีกำหนดผู้ใช้เป็นผู้รับมอบสิทธิ์ มันจะแสดงรายชื่อเพื่อให้ผู้ใช้สามารถป้อนแผ่นเวลาในนามของผู้ใต้บังคับบัญชา</span><span class="sxs-lookup"><span data-stu-id="2819a-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="2819a-113">ในฟิลด์ **วันที่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="2819a-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="2819a-114">ถ้าเลือกตัวเลือกนี้ จะมีสร้างรายการแผ่นเวลาใหม่ โดยใช้การตั้งค่าแผ่นเวลาที่มีการตั้งค่าคอนฟิกเป็นรายการโปรด</span><span class="sxs-lookup"><span data-stu-id="2819a-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="2819a-115">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2819a-115">Click **OK**.</span></span>
5. <span data-ttu-id="2819a-116">คลิก **รายการใหม่**</span><span class="sxs-lookup"><span data-stu-id="2819a-116">Click **New line**.</span></span>
6. <span data-ttu-id="2819a-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2819a-117">In the list, mark the selected row.</span></span> <span data-ttu-id="2819a-118">ฟิลด์ **นิติบุคคล** แสดงนิติบุคคลปัจจุบันตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2819a-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="2819a-119">ในฟิลด์ **โครงการ** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2819a-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2819a-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2819a-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="2819a-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2819a-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2819a-122">ในฟิลด์ **หมายเลขกิจกรรม** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2819a-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2819a-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2819a-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2819a-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2819a-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2819a-125">ในฟิลด์ **ประเภท** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2819a-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="2819a-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2819a-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2819a-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2819a-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="2819a-128">ป้อนจำนวนชั่วโมงที่ทำงานในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="2819a-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="2819a-129">ป้อนชั่วโมงในรูปแบบเลขฐานสิบ</span><span class="sxs-lookup"><span data-stu-id="2819a-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="2819a-130">ตัวอย่างเช่น ถ้าคุณเคยทำงานสองชั่วโมงสิบห้านาที ป้อน 2.25</span><span class="sxs-lookup"><span data-stu-id="2819a-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="2819a-131">ใน **รายละเอียดรายการ** ตัวเลือกต่อไปนี้จะพร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="2819a-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="2819a-132">เพิ่มข้อมูลเกี่ยวกับภาษีและมิติทางการเงินในแท็บ **ทั่วไป** และ **มิติทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="2819a-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="2819a-133">เพิ่มข้อคิดเห็นเกี่ยวกับรายการแผ่นเวลาในแท็บ **ข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="2819a-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="2819a-134">ใน **บานหน้าต่างนำทาง** คลิก **ลำดับงาน** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2819a-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="2819a-135">คลิก **ส่ง** </span><span class="sxs-lookup"><span data-stu-id="2819a-135">Click **Submit**.</span></span>
22. <span data-ttu-id="2819a-136">คลิก **ส่ง** </span><span class="sxs-lookup"><span data-stu-id="2819a-136">Click **Submit**.</span></span>

