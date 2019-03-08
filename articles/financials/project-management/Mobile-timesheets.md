---
title: แผ่นเวลาโครงการบนอุปกรณ์เคลื่อนที่
description: แผ่นเวลาของฉัน (ปรับให้เหมาะกับมือถือ) ช่วยให้พนักงานสามารถสร้างและส่งแผ่นเวลาโครงการได้ เพื่อบันทึกชั่วโมงของพวกเขาสำหรับโครงการหนึ่งๆ บนอุปกรณ์เคลื่อนที่
author: abruer
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: April 2018 update
ms.openlocfilehash: 96ad2af40ffb68649dca7a90d5ae14cd64b43ce9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "360957"
---
# <a name="project-timesheets-on-a-mobile-device"></a><span data-ttu-id="319ca-103">แผ่นเวลาโครงการบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="319ca-103">Project timesheets on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

# <a name="overview"></a><span data-ttu-id="319ca-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="319ca-104">Overview</span></span>

<span data-ttu-id="319ca-105">**แผ่นเวลาของฉัน (ปรับให้เหมาะกับมือถือ)** ช่วยให้พนักงานสามารถสร้างและส่งแผ่นเวลาโครงการได้ เพื่อบันทึกชั่วโมงของพวกเขาสำหรับโครงการหนึ่งๆ บนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="319ca-105">**My timesheets (Optimized for mobile)** allows employees to create and submit project timesheets to record their hours for a specific project on a mobile device.</span></span> <span data-ttu-id="319ca-106">พนักงานสามารถสร้างแผ่นเวลาใหม่หรือคัดลอกข้อมูลจากแผ่นเวลาที่มีอยู่ เพื่อให้แน่ใจว่าการป้อนข้อมูลเวลารวดเร็ว ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="319ca-106">Employees can create a new timesheet or copy data from an existing timesheet to ensure rapid, accurate time entry.</span></span> <span data-ttu-id="319ca-107">ถ้าคุณถูกกำหนดให้เป็นผู้รับมอบสิทธิ์ คุณยังสามารถป้อนเป็นแผ่นเวลาสำหรับผู้ปฏิบัติงานอื่นได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="319ca-107">If you are designated as a delegate, you can also enter a timesheet for another worker.</span></span> <span data-ttu-id="319ca-108">แอปช่วยให้พนักงานสามารถกรองข้อมูลโดยเรียงตามโครงการ ทรัพยากร หรือสถานะการอนุมัติ เพื่อค้นหาและเลือกแผ่นเวลาได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="319ca-108">The app allows employees to filter by project, resource, or approval status to quickly locate and select a timesheet.</span></span> <span data-ttu-id="319ca-109">และยังให้พนักงานมีความสามารถในการบันทึกรายการโปรด ซึ่งจะบันทึกข้อมูลโครงการและกิจกรรมบนแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="319ca-109">It also provides employees with the ability to save favorites, which saves the project and activity information on the timesheet.</span></span> <span data-ttu-id="319ca-110">รายการโปรดที่บันทึกสามารถใช้เพื่อสร้างแผ่นเวลาในอนาคต โดยเพิ่มความเร็วในกระบวนการป้อนข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="319ca-110">The saved favorites can be used to create future timesheets, speeding the time entry process.</span></span> <span data-ttu-id="319ca-111">การแก้ไขหรือการดูข้อมูลมิติทางการเงิน ไม่ได้รับการสนับสนุนจากแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="319ca-111">Editing or viewing financial dimension information is not supported from the mobile app.</span></span> <span data-ttu-id="319ca-112">**แผ่นเวลาของฉัน (ปรับให้เหมาะกับมือถือ)** สามารถเข้าถึงได้ผ่านเว็บเบราเซอร์บนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="319ca-112">**My timesheets (Optimized for mobile)** can be accessed via the web browser on your mobile device.</span></span>

<span data-ttu-id="319ca-113">**แผ่นเวลาสำหรับการตรวจทานของฉัน (ปรับให้เหมาะกับมือถือ)** ช่วยให้ผู้จัดการ ที่มีสิทธิ์ในการอนุมัติแผ่นเวลา สามารถตรวจทานและอนุมัติแผ่นเวลาโครงการบนอุปกรณ์เคลื่อนที่ได้</span><span class="sxs-lookup"><span data-stu-id="319ca-113">**Timesheets for my review (Optimized for mobile)** allows project managers, who have timesheet approval rights, to review and approve project timesheets on a mobile device.</span></span> <span data-ttu-id="319ca-114">การแก้ไขหรือการดูข้อมูลมิติทางการเงิน ไม่ได้รับการสนับสนุนจากแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="319ca-114">Editing or viewing financial dimension information is not supported from the mobile app.</span></span> <span data-ttu-id="319ca-115">**แผ่นเวลาสำหรับการตรวจทานของฉัน (ปรับให้เหมาะกับมือถือ)** สามารถเข้าถึงได้ผ่านเว็บเบราเซอร์บนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="319ca-115">**Timesheets for my review (Optimized for mobile)** can be accessed via the web browser on your mobile device.</span></span>

<span data-ttu-id="319ca-116">แอพลิเคชันบนมือถือนี้เข้ากันได้สำหรับ iPhone กับ Dynamics 365 for Finance and Operations การปรับปรุงแพลตฟอร์ม 15</span><span class="sxs-lookup"><span data-stu-id="319ca-116">This mobile application is compatible for iPhone with Dynamics 365 for Finance and Operations platform update 15.</span></span>
<span data-ttu-id="319ca-117">Android จะเข้ากันได้กับการปรับปรุงแพลตฟอร์ม 16 เมื่อกลายเป็นพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="319ca-117">Android will be compatible with Platform update 16, when it becomes available.</span></span>

<a name="create-a-project-timesheet-on-your-mobile-device"></a><span data-ttu-id="319ca-118">สร้างแผ่นเวลาโครงการบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="319ca-118">Create a project timesheet on your mobile device</span></span>
------------------------------------------------

1.  <span data-ttu-id="319ca-119">หมายเหตุ URL ของ Dynamics 365 สำหรับ **การจัดการและการบัญชีโครงการ** \> **แผ่นเวลา** \> หน้า **แผ่นเวลาของฉัน(ปรับให้เหมาะกับมือถือ)**</span><span class="sxs-lookup"><span data-stu-id="319ca-119">Note the Dynamics 365 URL for the **Project management and accounting** \> **Timesheets** \> **My timesheets(Optimized for mobile)** page.</span></span>

2.  <span data-ttu-id="319ca-120">ในเบราเซอร์เว็บของอุปกรณ์เคลื่อนที่ของคุณ เข้าถึง URL ที่ระบุไว้ในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="319ca-120">On your mobile device’s web browser, access the URL noted in the previous step.</span></span>
 
3.  <span data-ttu-id="319ca-121">เลือก **การจัดการและการบัญชีโครงการ** \> **แผ่นเวลา** \> **แผ่นเวลาของฉัน(ปรับให้เหมาะกับมือถือ)**</span><span class="sxs-lookup"><span data-stu-id="319ca-121">Select **Project management and Accounting** \> **Timesheets** \> **My timesheets(Optimized for mobile)**.</span></span>

4.  <span data-ttu-id="319ca-122">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="319ca-122">Select **New**.</span></span>

5.  <span data-ttu-id="319ca-123">เลือกทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="319ca-123">Select a resource.</span></span>

6.  <span data-ttu-id="319ca-124">วันที่ในปฏิทินสำหรับสัปดาห์ปัจจุบันจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="319ca-124">The calendar dates for the current week are shown.</span></span>

7.  <span data-ttu-id="319ca-125">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="319ca-125">Click **OK**.</span></span>

8.  <span data-ttu-id="319ca-126">คลิก **+** เพื่อเพิ่มรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="319ca-126">Click **+** to add a new line.</span></span>

9.  <span data-ttu-id="319ca-127">เลือกข้อมูลลูกค้าและโครงการสำหรับรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="319ca-127">Select the customer and project information for the timesheet line.</span></span>

10. <span data-ttu-id="319ca-128">ป้อนชั่วโมงที่คุณทำงานสำหรับรายการโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="319ca-128">Enter the hours that you worked for the selected project line.</span></span>

11. <span data-ttu-id="319ca-129">ไม่จำเป็นต้องระบุ: ป้อนข้อคิดเห็นภายในและภายนอกสำหรับชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="319ca-129">Optional: Enter any external and internal comments for the hours.</span></span>

12. <span data-ttu-id="319ca-130">เลือกการดำเนินการย้อนกลับเพื่อบันทึกข้อมูลชั่วโมง และกลับไปยังมุมมองรายละเอียดแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="319ca-130">Select the back action to save the hour information and return to the timesheet details view.</span></span>

13. <span data-ttu-id="319ca-131">ไม่จำเป็นต้องระบุ: ป้อนรายการแผ่นเวลาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="319ca-131">Optional: Enter additional timesheet lines.</span></span>

14. <span data-ttu-id="319ca-132">หลังจากที่คุณป้อนรายการแผ่นเวลาเสร็จสมบูรณ์ เลือกการดำเนินการ **ลำดับงาน** \> **ส่ง** เพื่อส่งแผ่นเวลาของคุณไปยังกระบวนการอนุมัติลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="319ca-132">After you have completed entering the timesheet lines, select the **Workflow** \> **Submit** action to submit your timesheet to the workflow approval process.</span></span>
