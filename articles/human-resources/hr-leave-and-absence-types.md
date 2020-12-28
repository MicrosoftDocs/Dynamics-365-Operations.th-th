---
title: ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน
description: ตั้งค่าชนิดของการลางานที่พนักงานสามารถได้รับจากบริษัทใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420737"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="b75bb-103">ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-103">Configure leave and absence types</span></span>

<span data-ttu-id="b75bb-104">ชนิดการลางานใน Dynamics 365 Human Resources กำหนดชนิดของการขาดงานต่างๆที่พนักงานสามารถรายงาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="b75bb-105">คุณสามารถปรับแต่งชนิดของการลางานตามความต้องการขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="b75bb-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="b75bb-106">ตัวอย่างของชนิดการลาประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="b75bb-106">Examples of leave types include:</span></span>

- <span data-ttu-id="b75bb-107">เวลาหยุดพักที่ได้รับค่าจ้าง (PTO)</span><span class="sxs-lookup"><span data-stu-id="b75bb-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="b75bb-108">การลางานที่ไม่ได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="b75bb-108">Unpaid leave</span></span>
- <span data-ttu-id="b75bb-109">วันหยุดที่ได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="b75bb-109">Paid vacation</span></span>
- <span data-ttu-id="b75bb-110">ลาป่วย</span><span class="sxs-lookup"><span data-stu-id="b75bb-110">Sick leave</span></span>
- <span data-ttu-id="b75bb-111">การลาป่วย</span><span class="sxs-lookup"><span data-stu-id="b75bb-111">Medical leave</span></span>
- <span data-ttu-id="b75bb-112">การลาดูแลครอบครัว</span><span class="sxs-lookup"><span data-stu-id="b75bb-112">Family leave</span></span>
- <span data-ttu-id="b75bb-113">ทุพพลภาพระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="b75bb-113">Short-term disability</span></span>
- <span data-ttu-id="b75bb-114">การลาหยุดเนื่องจากญาติหรือครอบครัวเสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="b75bb-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="b75bb-115">เพิ่มชนิดของการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-115">Add a leave type</span></span>

1. <span data-ttu-id="b75bb-116">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="b75bb-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b75bb-117">ภายใต้ **การตั้งค่า** ให้เลือก **ชนิดของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="b75bb-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="b75bb-118">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b75bb-118">Select **New**.</span></span>

4. <span data-ttu-id="b75bb-119">ป้อนชื่อสำหรับชนิดการลางานภายใต้ **ชนิด** เลือกลำดับงานจาก **รหัสลำดับงาน** และป้อนคำอธิบายภายใต้ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="b75bb-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="b75bb-120">**โดยทั่วไป** ให้เลือก **ไม่** **จัดกำหนดการแล้ว** หรือ **ยกเลิกการจัดกำหนดการ** จาก **ประเภท** รายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="b75bb-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="b75bb-121">เลือกรหัสรายได้จากรายการแบบหล่นลง **รหัสรายได้**</span><span class="sxs-lookup"><span data-stu-id="b75bb-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="b75bb-122">ภายใต้ **รหัสเหตุผลที่จำเป็น** ให้เลือกว่าคุณต้องการใช้รหัสเหตุผลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b75bb-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="b75bb-123">ถ้าคุณต้องการใช้รหัสเหตุผลคุณอาจจำเป็นต้องเพิ่มรหัสดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="b75bb-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="b75bb-124">ภายใต้ **รหัสเหตุผล** ให้เลือก **เพิ่ม** เลือกรหัสเหตุผลแล้วเลือกกล่องกาเครื่องหมายที่ **เปิดใช้งาน** ที่อยู่ด้านข้างรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="b75bb-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="b75bb-125">ภายใต้ **จำกัดการเข้าถึงบทบาทที่เลือกไว้** ให้เลือกว่าคุณต้องการจำกัดการเข้าถึงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b75bb-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="b75bb-126">จากนั้นเลือกบทบาทความปลอดภัยภายใต้ **บทบาทความปลอดภัยสำหรับชนิดการลางานนี้**</span><span class="sxs-lookup"><span data-stu-id="b75bb-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="b75bb-127">บาทความปลอดภัยถูกกำหนดไว้ในลำดับงานที่คุณเลือกไว้ภายใต้ **รหัสลำดับงาน** ก่อนหน้านี้ในกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="b75bb-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="b75bb-128">ภายใต้ **สีของปฏิทิน** ให้เลือกสีที่จะแสดงบนปฏิทินการลางานและการขาดงานสำหรับชนิดการลางานนี้</span><span class="sxs-lookup"><span data-stu-id="b75bb-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="b75bb-129">ภายใต้ **ความสัมพันธ์ของการระงับ** ให้เลือกว่าคุณต้องการให้ชนิดการลางานนี้ระงับชนิดการลางานอื่น หรือถูกระงับโดยชนิดการลางานอื่น</span><span class="sxs-lookup"><span data-stu-id="b75bb-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="b75bb-130">เมื่อมีการส่งคำขอการลางานสำหรับชนิดการระงับการลา จะมีการสร้างการระงับการลางานโดยอัตโนมัติสำหรับชนิดการลางานที่ถูกระงับ</span><span class="sxs-lookup"><span data-stu-id="b75bb-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="b75bb-131">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b75bb-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="b75bb-132">ตั้งค่าคอนฟิกกฎชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-132">Configure leave type rules</span></span>

1. <span data-ttu-id="b75bb-133">ตั้งค่าตัวเลือกการปัดเศษสำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="b75bb-134">ตัวเลือกประกอบด้วย **ไม่** **ขึ้น** **ลง** และ **ใกล้ที่สุด**</span><span class="sxs-lookup"><span data-stu-id="b75bb-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="b75bb-135">นอกจากนี้คุณยังสามารถตั้งค่าความแม่นยำในการปัดเศษสำหรับชนิดการลางานได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b75bb-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="b75bb-136">ตั้งค่า **การแก้ไขวันหยุด** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="b75bb-137">เมื่อคุณเลือกตัวเลือกนี้ทรัพยากรบุคคลจะใช้จำนวนวันหยุดที่อยู่ในวันทำงานเพื่อกำหนดวิธีการยกยอดเวลาหยุดพักสำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="b75bb-138">ตัวอย่างเช่นถ้าวันคริสต์มาสตรงกันในวันจันทร์ ทรัพยากรบุคคลจะหัก 1 วันออกจากชนิดของการลาเมื่อกำลังประมวลผลรายการยกยอด</span><span class="sxs-lookup"><span data-stu-id="b75bb-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="b75bb-139">คุณตั้งค่าวันหยุดในปฏิทินเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="b75bb-140">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [สร้างปฏิทินเวลาทำงาน](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="b75bb-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="b75bb-141">ตั้งค่า **ชนิดการลางานแบบยกยอดไป** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="b75bb-142">เมื่อคุณเลือกตัวเลือกนี้ จะมีการโอนย้ายยอดดุลแบบยกยอดไปไปยังชนิดการลางานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b75bb-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="b75bb-143">นอกจากนี้ ชนิดการลางานแบบยกยอดไปยังต้องถูกรวมอยู่ในแผนการลางานและการขาดงานด้วย</span><span class="sxs-lookup"><span data-stu-id="b75bb-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="b75bb-144">กำหนด **กฎการหมดอายุ** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="b75bb-145">เมื่อคุณตั้งค่าคอนฟิกตัวเลือกนี้ คุณสามารถเลือกหน่วยของวันหรือเดือน และกำหนดระยะเวลาสำหรับการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="b75bb-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="b75bb-146">นอกจากนี้ คุณยังสามารถตั้งค่าวันที่มีผลบังคับใช้ของกฎการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="b75bb-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="b75bb-147">ยอดดุลการลางานใดๆ ที่มีอยู่ในช่วงเวลาของการหมดอายุจะถูกลบออกจากชนิดของการลางาน และจะถูกสะท้อนให้เห็นในยอดดุลการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="b75bb-148">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b75bb-148">See also</span></span>

- [<span data-ttu-id="b75bb-149">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="b75bb-150">สร้างแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="b75bb-151">สร้างปฏิทินเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="b75bb-152">ระงับการลางาน</span><span class="sxs-lookup"><span data-stu-id="b75bb-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

