---
title: ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน
description: กำหนดพารามิเตอร์ทรัพยากรบุคคลสำหรับการลางานและการขาดงานใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db96073f0a16f1c710fbfebb2d08a1d693eab1e1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463393"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="21552-103">ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21552-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="21552-104">ก่อนที่คุณจะตั้งค่าการลางานและการขาดงานใน Dynamics 365 Human Resources คุณควรตรวจสอบความถูกต้องของการตั้งค่าสำหรับพารามิเตอร์ทรัพยากรบุคคลที่เกี่ยวข้องทั้งหมดรวมถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="21552-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="21552-105">ลำดับหมายเลขสำหรับการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="21552-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="21552-106">การตั้งค่าการลาดูแลครอบครัว ลาป่วย และลางาน (FMLA)</span><span class="sxs-lookup"><span data-stu-id="21552-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="21552-107">การตั้งค่าระบบบริการตนเองของพนักงานสำหรับการร้องขอการลางานหรือการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21552-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="21552-108">พารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21552-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="21552-109">ดูและเปลี่ยนแปลงพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="21552-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="21552-110">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="21552-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="21552-111">ภายใต้ **ตั้งค่า** พารามิเตอร์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="21552-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="21552-112">บนแท็บ **ลำดับหมายเลข** ตรวจสอบความถูกต้องของ **รหัสลำดับหมายเลข** สำหรับ **รหัสคำขอลางาน** และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21552-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="21552-113">การตั้งค่านี้จะกำหนดลำดับที่ใช้สำหรับการกำหนดรหัสให้กับการร้องขอโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="21552-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="21552-114">บนแท็บ **FMLA** ให้ตรวจสอบการตั้งค่า FMLA และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21552-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="21552-115">บนแท็บ **ระบบบริการตนเองของพนักงาน** ให้ระบุว่าผู้จัดการสามารถป้อนการลางานและการร้องขอการขาดงานในนามของพนักงานได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="21552-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="21552-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="21552-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="21552-117">ขณะนี้การดูการลาและการขาดงานระหว่างบริษัทอยู่ในพรีวิว</span><span class="sxs-lookup"><span data-stu-id="21552-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="21552-118">คุณจำเป็นต้องเปิดใช้งานในสภาพแวดล้อม **Sandbox** ของคุณ เพื่อแสดงตัวเลือกสำหรับการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21552-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="21552-119">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะรุ่นพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="21552-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="21552-120">ดูและเปลี่ยนแปลงพารามิเตอร์ที่ใช้ร่วมกันของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="21552-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="21552-121">บนหน้า **การจัดการบุคลากร** ให้เลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="21552-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="21552-122">ภายใต้ **ตั้งค่า** เลือก **พารามิเตอร์ที่ใช้ร่วมกันของทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="21552-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="21552-123">บนแท็บ **การเข้าถึงขั้นสูง** ให้เลือก **ใช่** เพื่อ **เปิดใช้งานมุมมองการลางานข้ามบริษัท** เพื่ออนุญาตให้มีการดูการลางานข้ามบริษัทได้</span><span class="sxs-lookup"><span data-stu-id="21552-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="21552-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="21552-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="21552-125">ดูและเปลี่ยนแปลงพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21552-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="21552-126">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="21552-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="21552-127">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="21552-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="21552-128">บนแท็บ **ทั่วไป** ให้ตั้งค่าพารามิเตอร์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="21552-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="21552-129">ตั้งค่า **หน่วยสำหรับการลางานและการขาดงาน** เป็นชั่วโมงหรือวัน</span><span class="sxs-lookup"><span data-stu-id="21552-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="21552-130">ถ้าเป็นวัน คุณสามารถเลือก **เปิดใช้งานข้อกำหนดครึ่งวัน** เพื่ออนุญาตให้พนักงานเลือกครึ่งแรกหรือครึ่งหลังของวันในการร้องขอการหมดเวลาของตน</span><span class="sxs-lookup"><span data-stu-id="21552-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="21552-131">เลือก **เดือนของวันที่มีผลบังคับใช้ของการบริการ** ที่จะกำหนดเมื่ออัตราการค้างรับมีผลบังคับใช้สำหรับแผนการลางานโดยใช้เดือนของการบริการ</span><span class="sxs-lookup"><span data-stu-id="21552-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="21552-132">เลือก **การคำนวณยอดดุล** เพื่อแสดงยอดดุลในวันที่วันนี้หรือตามรอบระยะเวลาการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="21552-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="21552-133">ถ้าคุณเลือก **ยอดดุล ณ วันที่วันนี้** ยอดดุลจะแสดงผลรวมของการค้างรับทั้งหมด การปรับปรุง และการร้องขอในวันนี้</span><span class="sxs-lookup"><span data-stu-id="21552-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="21552-134">ถ้าคุณเลือก **ยอดดุลของระยะเวลาการค้างรับ** ยอดดุลจะแสดงผลรวมของการค้างรับ การปรับปรุ งและการร้องขอทั้งหมดของรอบระยะเวลาการค้างรับที่กำหนดโดยความถี่ในแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="21552-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="21552-135">ตั้งค่าเวลาเริ่มต้นสำหรับชุดงานการหมดอายุของยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="21552-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="21552-136">เลือก **ใช่** สำหรับ **อนุญาตให้พนักงานซื้อวันลา** และ **อนุญาตให้พนักงานขายวันลา**</span><span class="sxs-lookup"><span data-stu-id="21552-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="21552-137">ถ้าคุณเลือก **ใช่** สำหรับตัวเลือกเหล่านี้ คุณสามารถสร้างนโยบายการซื้อและการขายวันลา และช่วยให้พนักงานสามารถส่งคำขอซื้อและขายวันลาได้</span><span class="sxs-lookup"><span data-stu-id="21552-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="21552-138">ตั้งค่าคอนฟิกพารามิเตอร์ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="21552-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="21552-139">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="21552-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="21552-140">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="21552-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="21552-141">บนแท็บ **ปฏิทิน** เปลี่ยนแปลงปฏิทินตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21552-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="21552-142">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="21552-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="21552-143">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="21552-143">See also</span></span>

- [<span data-ttu-id="21552-144">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="21552-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]