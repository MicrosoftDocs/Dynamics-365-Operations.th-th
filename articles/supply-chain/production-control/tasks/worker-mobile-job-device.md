--- 
title: "ตั้งค่าคอนฟิกผู้ปฏิบัติงานโดยใช้อุปกรณ์เคลื่อนที่ของงาน"
description: "กระบวนงานนี้แสดงวิธีการกำหนดบทบาทที่ถูกต้องให้กับบัญชีผู้ปฏิบัติงานและเปิดการใช้งานของผู้ปฏิบัติงานในการลงทะเบียนการผลิต"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d56f861dbbf579e44fcd3fc4d8b45c24029acecc
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="93054-103">ตั้งค่าคอนฟิกผู้ปฏิบัติงานโดยใช้อุปกรณ์เคลื่อนที่ของงาน</span><span class="sxs-lookup"><span data-stu-id="93054-103">Configure a worker using the mobile job device</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93054-104">กระบวนงานนี้แสดงวิธีการกำหนดบทบาทที่ถูกต้องให้กับบัญชีผู้ปฏิบัติงานและเปิดการใช้งานของผู้ปฏิบัติงานในการลงทะเบียนการผลิต</span><span class="sxs-lookup"><span data-stu-id="93054-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="93054-105">กำหนดบทบาทให้กับบัญชีผู้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="93054-105">Assign roles to user account</span></span>
1. <span data-ttu-id="93054-106">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="93054-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="93054-107">ใช้ตัวกรองข้อมูลอย่างรวดเร็วเพื่อกรองข้อมูลเกี่ยวกับชื่อของผู้ปฏิบัติงานที่เป็นบัญชีผู้ใช้ที่สัมพันธ์กับบทบาทของผู้ปฏิบัติงานเครื่องจักร </span><span class="sxs-lookup"><span data-stu-id="93054-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="93054-108">ในข้อมูลตัวอย่าง ชื่อจะเป็น Shannon</span><span class="sxs-lookup"><span data-stu-id="93054-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="93054-109">เน้นเรกคอร์ดบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="93054-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="93054-110">ในรายการ คลิกลิงค์ "ชื่อ" ในแถวที่เลือกเพื่อดูรายละเอียดของบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="93054-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="93054-111">ในแผนภูมิ เลือก 'ตัวดำเนินการ Roles\Machine'</span><span class="sxs-lookup"><span data-stu-id="93054-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="93054-112">ปิดหน้ารายละเอียดบัญชีผู้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="93054-112">Close the user account details page.</span></span>
7. <span data-ttu-id="93054-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93054-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="93054-114">ตั้งค่าคอนฟิกบัญชีผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="93054-114">Configure worker account.</span></span>
1. <span data-ttu-id="93054-115">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="93054-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="93054-116">ใช้ตัวกรองข้อมูลอย่างรวดเร็วเพื่อกรองข้อมูลเกี่ยวกับชื่อของผู้ปฏิบัติงานที่เป็นบัญชีผู้ใช้ที่สัมพันธ์กับบทบาทของผู้ปฏิบัติงานเครื่องจักร </span><span class="sxs-lookup"><span data-stu-id="93054-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="93054-117">ในข้อมูลตัวอย่าง ชื่อจะเป็น Shannon</span><span class="sxs-lookup"><span data-stu-id="93054-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="93054-118">เน้นเรกคอร์ดบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="93054-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="93054-119">ในรายการ คลิกลิงค์ "ชื่อ" ในแถวที่เลือกเพื่อดูรายละเอียดของบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="93054-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="93054-120">คลิกแท็บการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="93054-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="93054-121">ขยายแท็บด่วนระยะเวลาการลงทะเบียน และคลิกเรียกใช้บนเทอร์มินัลการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="93054-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="93054-122">คลิกเรียกใช้บนเทอร์มินัลการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="93054-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="93054-123">ในฟิลด์กลุ่มแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93054-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="93054-124">ในฟิลด์กลุ่มกลุ่มการคำนวณเริ่มต้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93054-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="93054-125">ในฟิลด์กลุ่มการอนุมัติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93054-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="93054-126">ในฟิลด์โพรไฟล์มาตรฐาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93054-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="93054-127">ในฟิลด์กลุ่มโพรไฟล์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93054-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="93054-128">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="93054-128">Click OK.</span></span>
14. <span data-ttu-id="93054-129">คลิกแก้ไขเพื่อป้อนหมายเลขป้ายชื่อสำหรับผู้ปฏิบัติงานลงทะเบียนเวลาใหม่</span><span class="sxs-lookup"><span data-stu-id="93054-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="93054-130">ในฟิลด์รหัสป้ายชื่อพนักงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="93054-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="93054-131">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="93054-131">Click Save.</span></span>
17. <span data-ttu-id="93054-132">ใช้ทางลัด SaveRecord</span><span class="sxs-lookup"><span data-stu-id="93054-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="93054-133">ปิดหน้ารายละเอียดผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="93054-133">Close the worker details page.</span></span>
19. <span data-ttu-id="93054-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93054-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="93054-135">มอบหมายผู้ปฏิบัติงานให้กับกลุ่มอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="93054-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="93054-136">ไปที่การควบคุมการผลิต > การตั้งค่า > การดำเนินการผลิต > ตั้งค่าคอนฟิกบัตรงานสำหรับอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="93054-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="93054-137">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="93054-137">Click Add.</span></span>
3. <span data-ttu-id="93054-138">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93054-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="93054-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="93054-139">Click OK.</span></span>
5. <span data-ttu-id="93054-140">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="93054-140">Click Edit.</span></span>
6. <span data-ttu-id="93054-141">ในฟิลด์หน่วยการผลิต คุณสามารถตั้งค่าตัวกรองเริ่มต้นสำหรับผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="93054-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="93054-142">ซึ่งจะกำหนดว่า จะแสดงเฉพาะงานการผลิตสำหรับหน่วยการผลิตที่เลือกเมื่อผู้ปฏิบัติงานที่ล็อกออนที่อุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="93054-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="93054-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93054-143">Close the page.</span></span>


