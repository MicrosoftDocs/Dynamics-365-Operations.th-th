---
title: รายงานความคืบหน้าของอุปกรณ์เคลื่อนที่ของงาน
description: 'กระบวนการนี้จะแสดงวิธีการเริ่มต้นและวิธีการรายงานการดำเนินการของงานการผลิตในแบบฟอร์มการลงทะเบียนงานบนอุปกรณ์ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a659dbb851dd6beeb59228116095577d2b4cb97a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210536"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="eb034-103">รายงานความคืบหน้าของอุปกรณ์เคลื่อนที่ของงาน</span><span class="sxs-lookup"><span data-stu-id="eb034-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb034-104">กระบวนการนี้จะแสดงวิธีการเริ่มต้นและวิธีการรายงานการดำเนินการของงานการผลิตในแบบฟอร์มการลงทะเบียนงานบนอุปกรณ์ </span><span class="sxs-lookup"><span data-stu-id="eb034-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="eb034-105">เพื่อเป็นการรันกระบวนงานนี้ คุณต้องมีผู้ดูแลระบบหรือบทบาทพนักงานควบคุมเครื่องจักรที่เชื่อมโยงกับบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="eb034-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="eb034-106">ไปที่ การควบคุมการผลิต > การดำเนินการผลิต > อุปกรณ์สำหรับบัตรงาน</span><span class="sxs-lookup"><span data-stu-id="eb034-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="eb034-107">ในฟิลด์ WorkerTextField ป้อนป้ายชื่อของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="eb034-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="eb034-108">ในข้อมูลสาธิต USMF พิมพ์ '123' สำหรับ Christina Portra ...</span><span class="sxs-lookup"><span data-stu-id="eb034-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="eb034-109">คลิกเพื่อเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="eb034-109">Click Log in.</span></span>
4. <span data-ttu-id="eb034-110">คลิกปุ่มตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="eb034-110">Click the Filter button.</span></span>
5. <span data-ttu-id="eb034-111">ตรวจสอบความถูกต้องหรือยกเลิกการประยุกต์ใช้กล่องกาเครื่องหมายตัวกรองการตั้งค่าคอนฟิก </span><span class="sxs-lookup"><span data-stu-id="eb034-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="eb034-112">ถ้าคุณกำหนดตัวกรอง คุณสามารถใช้หน่วยการผลิต 110 ใน USMF</span><span class="sxs-lookup"><span data-stu-id="eb034-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="eb034-113">ในฟิลด์หน่วยการผลิต เลือกกลุ่มทรัพยากรสำหรับงานการผลิตที่ผู้ปฏิบัติงานสามารถทำงานได้</span><span class="sxs-lookup"><span data-stu-id="eb034-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="eb034-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eb034-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="eb034-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="eb034-115">Click OK.</span></span>
9. <span data-ttu-id="eb034-116">คลิกปุ่มเริ่มต้นงาน</span><span class="sxs-lookup"><span data-stu-id="eb034-116">Click the Start job button.</span></span>
10. <span data-ttu-id="eb034-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="eb034-117">Click OK.</span></span>
11. <span data-ttu-id="eb034-118">คลิกปุ่มความคืบหน้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="eb034-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="eb034-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="eb034-119">Click OK.</span></span>
13. <span data-ttu-id="eb034-120">คลิกปุ่มงานถัดไป</span><span class="sxs-lookup"><span data-stu-id="eb034-120">Click the Next job button.</span></span>
14. <span data-ttu-id="eb034-121">คลิกมอบหมายเพื่อดูภาพรวมของปุ่มงานการผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="eb034-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="eb034-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="eb034-122">Close the page.</span></span>
16. <span data-ttu-id="eb034-123">คลิกปุ่มหยุด</span><span class="sxs-lookup"><span data-stu-id="eb034-123">Click the Break button.</span></span>
17. <span data-ttu-id="eb034-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="eb034-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="eb034-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="eb034-125">Click OK.</span></span>
19. <span data-ttu-id="eb034-126">คลิกปุ่มการสิ้นสุดการทำงาน </span><span class="sxs-lookup"><span data-stu-id="eb034-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="eb034-127">เลือกเพื่อออกจากระบบ</span><span class="sxs-lookup"><span data-stu-id="eb034-127">Select to log out.</span></span>
21. <span data-ttu-id="eb034-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="eb034-128">Click OK.</span></span>
22. <span data-ttu-id="eb034-129">ในฟิลด์ WorkerTextField ให้เข้าสู่ระบบอีกครั้ง </span><span class="sxs-lookup"><span data-stu-id="eb034-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="eb034-130">คุณสามารถเลือกผู้ปฏิบัติงาน '123' ใน USMF ข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="eb034-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="eb034-131">คลิกเพื่อเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="eb034-131">Click Log in.</span></span>
24. <span data-ttu-id="eb034-132">คลิกหยุดการหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="eb034-132">Click Stop break.</span></span>
25. <span data-ttu-id="eb034-133">คลิกปุ่มกิจกรรม </span><span class="sxs-lookup"><span data-stu-id="eb034-133">Click the Activity button.</span></span>
26. <span data-ttu-id="eb034-134">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="eb034-134">Click Cancel.</span></span>
27. <span data-ttu-id="eb034-135">คลิกปุ่มการสิ้นสุดการทำงาน </span><span class="sxs-lookup"><span data-stu-id="eb034-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="eb034-136">เลือกเพื่อตอกบัตรออกจากระบบ</span><span class="sxs-lookup"><span data-stu-id="eb034-136">Select to clock out.</span></span>
29. <span data-ttu-id="eb034-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="eb034-137">Click OK.</span></span>
30. <span data-ttu-id="eb034-138">เลือกเหตุผลที่คุณจะตอกบัตรออกก่อนเวลา</span><span class="sxs-lookup"><span data-stu-id="eb034-138">Select a reason why you are clocking out early.</span></span>

