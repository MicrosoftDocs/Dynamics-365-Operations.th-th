---
title: ตั้งค่าคอนฟิกผู้ปฏิบัติงานโดยใช้อุปกรณ์เคลื่อนที่ของงาน
description: หัวข้อนี้อธิบายวิธีการกำหนดบทบาทที่ถูกต้องให้กับบัญชีผู้ใช้ของผู้ปฏิบัติงาน และจากนั้น เปิดการใช้งานให้ผู้ปฏิบัติงานทำการลงทะเบียนการผลิต
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89b75936ea9c0f25f82175a1871088da8fd74ad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980942"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="8afad-103">ตั้งค่าคอนฟิกผู้ปฏิบัติงานโดยใช้อุปกรณ์เคลื่อนที่ของงาน</span><span class="sxs-lookup"><span data-stu-id="8afad-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8afad-104">หัวข้อนี้อธิบายวิธีการกำหนดบทบาทที่ถูกต้องให้กับบัญชีผู้ใช้ของผู้ปฏิบัติงาน และจากนั้น เปิดการใช้งานให้ผู้ปฏิบัติงานทำการลงทะเบียนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8afad-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="8afad-105">ตรวจสอบว่าผู้ปฏิบัติงานได้รับการกำหนดบทบาทที่แน่นอน</span><span class="sxs-lookup"><span data-stu-id="8afad-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="8afad-106">สำหรับตัวอย่างนี้ ให้ตรวจสอบว่าผู้ใช้ "SHANNON" ได้รับการกำหนดบทบาทตัวดำเนินการเครื่องจักร ก่อนที่คุณตั้งค่าคอนฟิกบัญชีผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="8afad-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="8afad-107">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > ผู้ใช้ > ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="8afad-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="8afad-108">ค้นหาผู้ใช้ในตัวกรองข้อมูลด่วน</span><span class="sxs-lookup"><span data-stu-id="8afad-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="8afad-109">สำหรับตัวอย่างนี้ ให้ป้อน `shannon`</span><span class="sxs-lookup"><span data-stu-id="8afad-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="8afad-110">เลือกการเชื่อมโยงในคอลัมน์ **รหัสผู้ใช้** ของบัญชีผู้ใช้ที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8afad-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="8afad-111">ในแผนภูมิ **บทบาทของผู้ใช้** เลือก **บทบาท > พนักงานควบคุมเครื่องจักร**</span><span class="sxs-lookup"><span data-stu-id="8afad-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="8afad-112">ปิดหน้า **รายละเอียดผู้ใช้** และหน้า **ผู้ใช้** เพื่อกลับไปยังโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="8afad-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="8afad-113">ตั้งค่าคอนฟิกบัญชีผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="8afad-113">Configure worker account</span></span>
1. <span data-ttu-id="8afad-114">ไปที่ **บานหน้าต่างนำทาง > โมดูล > ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="8afad-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="8afad-115">ค้นหาผู้ใช้ในตัวกรองข้อมูลด่วน</span><span class="sxs-lookup"><span data-stu-id="8afad-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="8afad-116">สำหรับตัวอย่างนี้ ให้ป้อน `shannon`</span><span class="sxs-lookup"><span data-stu-id="8afad-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="8afad-117">เลือกการเชื่อมโยงในคอลัมน์ **ชื่อ** ของบัญชีผู้ใช้ที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8afad-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="8afad-118">เลือกแท็บ **การลงทะเบียนเวลา**</span><span class="sxs-lookup"><span data-stu-id="8afad-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="8afad-119">เลือก **เปิดใช้งานบนเทอร์มินัลการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="8afad-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="8afad-120">ป้อนหรือเลือกค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8afad-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="8afad-121">**กลุ่มการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="8afad-121">**Calculation group**</span></span>  
    - <span data-ttu-id="8afad-122">**กลุ่มการคำนวณเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="8afad-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="8afad-123">**กลุ่มการอนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="8afad-123">**Approval group**</span></span>  
    - <span data-ttu-id="8afad-124">**โพรไฟล์มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="8afad-124">**Standard profile**</span></span>  
    - <span data-ttu-id="8afad-125">**กลุ่มโพรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="8afad-125">**Profile group**</span></span>  

7. <span data-ttu-id="8afad-126">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8afad-126">Select **OK**.</span></span>
8. <span data-ttu-id="8afad-127">เลือก **แก้ไข** เพื่อป้อนหมายเลขป้ายชื่อสำหรับผู้ปฏิบัติงานการลงทะเบียนเวลาใหม่</span><span class="sxs-lookup"><span data-stu-id="8afad-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="8afad-128">ป้อนค่าในฟิลด์ **รหัสป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="8afad-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="8afad-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8afad-129">Select **Save**.</span></span>
10. <span data-ttu-id="8afad-130">ปิดหน้า **รายละเอียด** และหน้า **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="8afad-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="8afad-131">กำหนดผู้ปฏิบัติงานให้กับกลุ่มอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="8afad-131">Assign worker to device group</span></span>
1. <span data-ttu-id="8afad-132">ไปที่ **การควบคุมการผลิต > การตั้งค่า > การดำเนินการผลิต > ตั้งค่าคอนฟิกบัตรงานสำหรับอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="8afad-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="8afad-133">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8afad-133">Select **Add**.</span></span>
3. <span data-ttu-id="8afad-134">ในรายการ เลือกผู้ใช้ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8afad-134">In the list, select the desired worker.</span></span> <span data-ttu-id="8afad-135">สำหรับตัวอย่างนี้ ให้เลือก **SHANNON**</span><span class="sxs-lookup"><span data-stu-id="8afad-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="8afad-136">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8afad-136">Select **OK**.</span></span>
5. <span data-ttu-id="8afad-137">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8afad-137">Select **Edit**.</span></span>
6. <span data-ttu-id="8afad-138">ในฟิลด์ **หน่วยการผลิต** คุณสามารถตั้งค่าตัวกรองเริ่มต้นสำหรับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="8afad-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="8afad-139">ซึ่งจะกำหนดว่า จะแสดงเฉพาะงานการผลิตสำหรับหน่วยการผลิตที่เลือกเมื่อผู้ปฏิบัติงานที่ล็อกออนที่อุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="8afad-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="8afad-140">ป้อนค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8afad-140">Enter the desired value.</span></span>
7. <span data-ttu-id="8afad-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8afad-141">Close the page.</span></span>

