---
title: ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน
description: กำหนดพารามิเตอร์ทรัพยากรบุคคลสำหรับการลางานและการขาดงานใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197992"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="d4ac2-103">ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="d4ac2-104">ก่อนที่คุณจะตั้งค่าการลางานและการขาดงานใน Dynamics 365 Human Resources คุณควรตรวจสอบความถูกต้องของการตั้งค่าสำหรับพารามิเตอร์ทรัพยากรบุคคลที่เกี่ยวข้องทั้งหมดรวมถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d4ac2-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="d4ac2-105">ลำดับหมายเลขสำหรับการร้องขอการลางาน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="d4ac2-106">การตั้งค่าการลาดูแลครอบครัว ลาป่วย และลางาน (FMLA)</span><span class="sxs-lookup"><span data-stu-id="d4ac2-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="d4ac2-107">การตั้งค่าระบบบริการตนเองของพนักงานสำหรับการร้องขอการลางานหรือการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="d4ac2-108">พารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="d4ac2-109">ดูและเปลี่ยนแปลงพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="d4ac2-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="d4ac2-110">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d4ac2-111">ภายใต้ **ตั้งค่า**พารามิเตอร์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="d4ac2-112">บนแท็บ **ลำดับหมายเลข** ตรวจสอบความถูกต้องของ **รหัสลำดับหมายเลข** สำหรับ **รหัสคำขอลางาน** และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d4ac2-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="d4ac2-113">การตั้งค่านี้จะกำหนดลำดับที่ใช้สำหรับการกำหนดรหัสให้กับการร้องขอโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d4ac2-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="d4ac2-114">บนแท็บ **FMLA** ให้ตรวจสอบการตั้งค่า FMLA และเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d4ac2-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="d4ac2-115">บนแท็บ **ระบบบริการตนเองของพนักงาน** ให้ระบุว่าผู้จัดการสามารถป้อนการลางานและการร้องขอการขาดงานในนามของพนักงานได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="d4ac2-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="d4ac2-116">บนแท็บ **การลางานและการขาดงาน** ให้ตรวจสอบการตั้งค่าและเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d4ac2-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="d4ac2-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-117">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="d4ac2-118">ดูและเปลี่ยนแปลงพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-118">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="d4ac2-119">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-119">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d4ac2-120">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-120">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="d4ac2-121">บนแท็บ **ทั่วไป** ให้ตั้งค่าพารามิเตอร์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d4ac2-121">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="d4ac2-122">ตั้งค่า **หน่วยสำหรับการลางานและการขาดงาน** เป็นชั่วโมงหรือวัน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-122">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="d4ac2-123">ถ้าเป็นวัน คุณสามารถเลือก **เปิดใช้งานข้อกำหนดครึ่งวัน** เพื่ออนุญาตให้พนักงานเลือกครึ่งแรกหรือครึ่งหลังของวันในการร้องขอการหมดเวลาของตน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-123">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="d4ac2-124">เลือก **เดือนของวันที่มีผลบังคับใช้ของการบริการ** ที่จะกำหนดเมื่ออัตราการค้างรับมีผลบังคับใช้สำหรับแผนการลางานโดยใช้เดือนของการบริการ</span><span class="sxs-lookup"><span data-stu-id="d4ac2-124">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="d4ac2-125">เลือก **การคำนวณยอดดุล** เพื่อแสดงยอดดุลที่แสดงเป็นวันที่วันนี้หรือตามรอบระยะเวลาการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="d4ac2-125">Select **Balance calculation** to display balances display as of today or as of the accrual period.</span></span> <span data-ttu-id="d4ac2-126">ถ้าคุณเลือก **ยอดดุล ณ วันที่วันนี้** ยอดดุลจะแสดงผลรวมของการค้างรับทั้งหมด การปรับปรุง และการร้องขอในวันนี้</span><span class="sxs-lookup"><span data-stu-id="d4ac2-126">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="d4ac2-127">ถ้าคุณเลือก **ยอดดุลของระยะเวลาการค้างรับ** ยอดดุลจะแสดงผลรวมของการค้างรับ การปรับปรุ งและการร้องขอทั้งหมดของรอบระยะเวลาการค้างรับที่กำหนดโดยความถี่ในแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-127">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

## <a name="configure-calendar-parameters"></a><span data-ttu-id="d4ac2-128">ตั้งค่าคอนฟิกพารามิเตอร์ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-128">Configure calendar parameters</span></span>

1. <span data-ttu-id="d4ac2-129">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-129">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d4ac2-130">ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-130">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="d4ac2-131">บนแท็บ **ปฏิทิน** เปลี่ยนแปลงปฏิทินตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d4ac2-131">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="d4ac2-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d4ac2-132">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4ac2-133">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d4ac2-133">See also</span></span>

- [<span data-ttu-id="d4ac2-134">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="d4ac2-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
