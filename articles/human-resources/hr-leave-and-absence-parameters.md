---
title: ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน
description: กำหนดพารามิเตอร์ทรัพยากรบุคคลสำหรับการลางานและการขาดงานใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712387"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="ac898-103">ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="ac898-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="ac898-104">ก่อนที่คุณจะตั้งค่าการลางานและการขาดงานใน Dynamics 365 Human Resources คุณควรตรวจสอบความถูกต้องของการตั้งค่าสำหรับพารามิเตอร์ทรัพยากรบุคคลที่เกี่ยวข้องทั้งหมดรวมถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ac898-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="ac898-105">ลำดับหมายเลขสำหรับการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="ac898-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="ac898-106">การตั้งค่าการลาดูแลครอบครัว ลาป่วย และลางาน (FMLA)</span><span class="sxs-lookup"><span data-stu-id="ac898-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="ac898-107">การตั้งค่าระบบบริการตนเองของพนักงานสำหรับการร้องขอการลางานหรือการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="ac898-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="ac898-108">พารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="ac898-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="ac898-109">ดูและเปลี่ยนแปลงพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="ac898-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="ac898-110">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="ac898-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ac898-111">ภายใต้ **ตั้งค่า**พารามิเตอร์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="ac898-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="ac898-112">บนแท็บ **ลำดับหมายเลข** ตรวจสอบความถูกต้องของ **รหัสลำดับหมายเลข** สำหรับ **รหัสคำขอลางาน** และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ac898-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="ac898-113">การตั้งค่านี้จะกำหนดลำดับที่ใช้สำหรับการกำหนดรหัสให้กับการร้องขอโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ac898-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="ac898-114">บนแท็บ **FMLA** ให้ตรวจสอบการตั้งค่า FMLA และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ac898-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="ac898-115">บนแท็บ **ระบบบริการตนเองของพนักงาน** ให้ระบุว่าผู้จัดการสามารถป้อนการลางานและการร้องขอการขาดงานในนามของพนักงานได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="ac898-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="ac898-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ac898-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="ac898-117">ดูและเปลี่ยนแปลงพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="ac898-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="ac898-118">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="ac898-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ac898-119">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="ac898-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="ac898-120">บนแท็บ **ทั่วไป** ให้ตั้งค่าพารามิเตอร์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ac898-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="ac898-121">ตั้งค่า **หน่วยสำหรับการลางานและการขาดงาน** เป็นชั่วโมงหรือวัน</span><span class="sxs-lookup"><span data-stu-id="ac898-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="ac898-122">ถ้าเป็นวัน คุณสามารถเลือก **เปิดใช้งานข้อกำหนดครึ่งวัน** เพื่ออนุญาตให้พนักงานเลือกครึ่งแรกหรือครึ่งหลังของวันในการร้องขอการหมดเวลาของตน</span><span class="sxs-lookup"><span data-stu-id="ac898-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="ac898-123">เลือก **เดือนของวันที่มีผลบังคับใช้ของการบริการ** ที่จะกำหนดเมื่ออัตราการค้างรับมีผลบังคับใช้สำหรับแผนการลางานโดยใช้เดือนของการบริการ</span><span class="sxs-lookup"><span data-stu-id="ac898-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="ac898-124">เลือก **การคำนวณยอดดุล** เพื่อแสดงยอดดุลในวันที่วันนี้หรือตามรอบระยะเวลาการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="ac898-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="ac898-125">ถ้าคุณเลือก **ยอดดุล ณ วันที่วันนี้** ยอดดุลจะแสดงผลรวมของการค้างรับทั้งหมด การปรับปรุง และการร้องขอในวันนี้</span><span class="sxs-lookup"><span data-stu-id="ac898-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="ac898-126">ถ้าคุณเลือก **ยอดดุลของระยะเวลาการค้างรับ** ยอดดุลจะแสดงผลรวมของการค้างรับ การปรับปรุ งและการร้องขอทั้งหมดของรอบระยะเวลาการค้างรับที่กำหนดโดยความถี่ในแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="ac898-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="ac898-127">ตั้งค่าเวลาเริ่มต้นสำหรับชุดงานการหมดอายุของยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="ac898-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="ac898-128">เลือก **ใช่** สำหรับ **อนุญาตให้พนักงานซื้อวันลา** และ **อนุญาตให้พนักงานขายวันลา**</span><span class="sxs-lookup"><span data-stu-id="ac898-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="ac898-129">ถ้าคุณเลือก **ใช่** สำหรับตัวเลือกเหล่านี้ คุณสามารถสร้างนโยบายการซื้อและการขายวันลา และช่วยให้พนักงานสามารถส่งคำขอซื้อและขายวันลาได้</span><span class="sxs-lookup"><span data-stu-id="ac898-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="ac898-130">ตั้งค่าคอนฟิกพารามิเตอร์ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="ac898-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="ac898-131">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="ac898-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ac898-132">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="ac898-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="ac898-133">บนแท็บ **ปฏิทิน** เปลี่ยนแปลงปฏิทินตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ac898-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="ac898-134">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ac898-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac898-135">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="ac898-135">See also</span></span>

- [<span data-ttu-id="ac898-136">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="ac898-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
