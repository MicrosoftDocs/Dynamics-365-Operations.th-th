---
title: ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน
description: ตั้งค่าชนิดของการลางานที่พนักงานสามารถได้รับจากบริษัทใน Dynamics 365 Human Resources
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
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198061"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="99316-103">ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="99316-103">Configure leave and absence types</span></span>

<span data-ttu-id="99316-104">ชนิดการลางานใน Dynamics 365 Human Resources กำหนดชนิดของการขาดงานต่างๆที่พนักงานสามารถรายงาน</span><span class="sxs-lookup"><span data-stu-id="99316-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="99316-105">คุณสามารถปรับแต่งชนิดของการลางานตามความต้องการขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="99316-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="99316-106">ตัวอย่างของชนิดการลาประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="99316-106">Examples of leave types include:</span></span>

- <span data-ttu-id="99316-107">เวลาหยุดพักที่ได้รับค่าจ้าง (PTO)</span><span class="sxs-lookup"><span data-stu-id="99316-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="99316-108">การลางานที่ไม่ได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="99316-108">Unpaid leave</span></span>
- <span data-ttu-id="99316-109">วันหยุดที่ได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="99316-109">Paid vacation</span></span>
- <span data-ttu-id="99316-110">ลาป่วย</span><span class="sxs-lookup"><span data-stu-id="99316-110">Sick leave</span></span>
- <span data-ttu-id="99316-111">การลาป่วย</span><span class="sxs-lookup"><span data-stu-id="99316-111">Medical leave</span></span>
- <span data-ttu-id="99316-112">การลาดูแลครอบครัว</span><span class="sxs-lookup"><span data-stu-id="99316-112">Family leave</span></span>
- <span data-ttu-id="99316-113">ทุพพลภาพระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="99316-113">Short-term disability</span></span>
- <span data-ttu-id="99316-114">การลาหยุดเนื่องจากญาติหรือครอบครัวเสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="99316-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="99316-115">เพิ่มชนิดของการลางาน</span><span class="sxs-lookup"><span data-stu-id="99316-115">Add a leave type</span></span>

1. <span data-ttu-id="99316-116">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="99316-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="99316-117">ภายใต้ **การตั้งค่า** ให้เลือก **ชนิดของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="99316-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="99316-118">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="99316-118">Select **New**.</span></span>

4. <span data-ttu-id="99316-119">ป้อนชื่อสำหรับชนิดการลางานภายใต้ **ชนิด** เลือกลำดับงานจาก **รหัสลำดับงาน** และป้อนคำอธิบายภายใต้ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="99316-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="99316-120">**โดยทั่วไป** ให้เลือก **ไม่** **จัดกำหนดการแล้ว** หรือ **ยกเลิกการจัดกำหนดการ** จาก **ประเภท** รายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="99316-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="99316-121">เลือกรหัสรายได้จากรายการแบบหล่นลง **รหัสรายได้**</span><span class="sxs-lookup"><span data-stu-id="99316-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="99316-122">ภายใต้ **รหัสเหตุผลที่จำเป็น** ให้เลือกว่าคุณต้องการใช้รหัสเหตุผลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="99316-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="99316-123">ถ้าคุณต้องการใช้รหัสเหตุผลคุณอาจจำเป็นต้องเพิ่มรหัสดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="99316-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="99316-124">ภายใต้ **รหัสเหตุผล** ให้เลือก **เพิ่ม** เลือกรหัสเหตุผลแล้วเลือกกล่องกาเครื่องหมายที่ **เปิดใช้งาน** ที่อยู่ด้านข้างรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="99316-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="99316-125">ภายใต้ **จำกัดการเข้าถึงบทบาทที่เลือกไว้** ให้เลือกว่าคุณต้องการจำกัดการเข้าถึงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="99316-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="99316-126">จากนั้นเลือกบทบาทความปลอดภัยภายใต้ **บทบาทความปลอดภัยสำหรับชนิดการลางานนี้**</span><span class="sxs-lookup"><span data-stu-id="99316-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="99316-127">บาทความปลอดภัยถูกกำหนดไว้ในลำดับงานที่คุณเลือกไว้ภายใต้ **รหัสลำดับงาน** ก่อนหน้านี้ในกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="99316-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="99316-128">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="99316-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="99316-129">ตั้งค่าคอนฟิกกฎชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="99316-129">Configure leave type rules</span></span>

1. <span data-ttu-id="99316-130">ตั้งค่าตัวเลือกการปัดเศษสำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="99316-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="99316-131">ตัวเลือกประกอบด้วย **ไม่** **ขึ้น** **ลง** และ **ใกล้ที่สุด**</span><span class="sxs-lookup"><span data-stu-id="99316-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="99316-132">นอกจากนี้คุณยังสามารถตั้งค่าความแม่นยำในการปัดเศษสำหรับชนิดการลางานได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="99316-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="99316-133">ตั้งค่า **การแก้ไขวันหยุด** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="99316-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="99316-134">เมื่อคุณเลือกตัวเลือกนี้ทรัพยากรบุคคลจะใช้จำนวนวันหยุดที่อยู่ในวันทำงานเพื่อกำหนดวิธีการยกยอดเวลาหยุดพักสำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="99316-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="99316-135">ตัวอย่างเช่นถ้าวันคริสต์มาสตรงกันในวันจันทร์ ทรัพยากรบุคคลจะหัก 1 วันออกจากชนิดของการลาเมื่อกำลังประมวลผลรายการยกยอด</span><span class="sxs-lookup"><span data-stu-id="99316-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="99316-136">คุณตั้งค่าวันหยุดในปฏิทินเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="99316-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="99316-137">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [สร้างปฏิทินเวลาทำงาน](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="99316-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="99316-138">ตั้งค่าคอนฟิกคุณลักษณะตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="99316-138">Configure preview features</span></span>

<span data-ttu-id="99316-139">ถ้าคุณได้เปิดใช้งานคุณลักษณะตัวอย่างสำหรับการลางานและการขาดงานคุณต้องตั้งค่าคอนฟิกการตั้งค่าสำหรับผู้ใช้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="99316-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="99316-140">เลือกชนิดการลางานสำหรับยอดดุลแบบยกยอดไปที่จะโอนย้ายไป</span><span class="sxs-lookup"><span data-stu-id="99316-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="99316-141">นอกจากนี้คุณยังสามารถสร้างชนิดการลางานใหม่สำหรับการยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="99316-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="99316-142">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="99316-142">See also</span></span>

- [<span data-ttu-id="99316-143">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="99316-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="99316-144">สร้างแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="99316-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="99316-145">สร้างปฏิทินเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="99316-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
