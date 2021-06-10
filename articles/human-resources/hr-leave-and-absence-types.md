---
title: ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน
description: ตั้งค่าชนิดของการลางานที่พนักงานสามารถได้รับจากบริษัทใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 098f614da80a1e7e3e31b30cea707ecfbd5b0a70
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056623"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="e8467-103">ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="e8467-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e8467-104">ชนิดการลางานใน Dynamics 365 Human Resources กำหนดชนิดของการขาดงานต่างๆที่พนักงานสามารถรายงาน</span><span class="sxs-lookup"><span data-stu-id="e8467-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="e8467-105">คุณสามารถปรับแต่งชนิดของการลางานตามความต้องการขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="e8467-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="e8467-106">ตัวอย่างของชนิดการลาประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="e8467-106">Examples of leave types include:</span></span>

- <span data-ttu-id="e8467-107">เวลาหยุดพักที่ได้รับค่าจ้าง (PTO)</span><span class="sxs-lookup"><span data-stu-id="e8467-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="e8467-108">การลางานที่ไม่ได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="e8467-108">Unpaid leave</span></span>
- <span data-ttu-id="e8467-109">วันหยุดที่ได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="e8467-109">Paid vacation</span></span>
- <span data-ttu-id="e8467-110">ลาป่วย</span><span class="sxs-lookup"><span data-stu-id="e8467-110">Sick leave</span></span>
- <span data-ttu-id="e8467-111">การลาป่วย</span><span class="sxs-lookup"><span data-stu-id="e8467-111">Medical leave</span></span>
- <span data-ttu-id="e8467-112">การลาดูแลครอบครัว</span><span class="sxs-lookup"><span data-stu-id="e8467-112">Family leave</span></span>
- <span data-ttu-id="e8467-113">ทุพพลภาพระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="e8467-113">Short-term disability</span></span>
- <span data-ttu-id="e8467-114">การลาหยุดเนื่องจากญาติหรือครอบครัวเสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="e8467-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="e8467-115">เพิ่มชนิดของการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-115">Add a leave type</span></span>

1. <span data-ttu-id="e8467-116">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="e8467-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e8467-117">ภายใต้ **การตั้งค่า** ให้เลือก **ชนิดของการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="e8467-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="e8467-118">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e8467-118">Select **New**.</span></span>

4. <span data-ttu-id="e8467-119">ป้อนชื่อสำหรับชนิดการลางานภายใต้ **ชนิด** เลือกลำดับงานจาก **รหัสลำดับงาน** และป้อนคำอธิบายภายใต้ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="e8467-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="e8467-120">**โดยทั่วไป** ให้เลือก **ไม่** **จัดกำหนดการแล้ว** หรือ **ยกเลิกการจัดกำหนดการ** จาก **ประเภท** รายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="e8467-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="e8467-121">เลือกรหัสรายได้จากรายการแบบหล่นลง **รหัสรายได้**</span><span class="sxs-lookup"><span data-stu-id="e8467-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="e8467-122">ภายใต้ **รหัสเหตุผลที่จำเป็น** ให้เลือกว่าคุณต้องการใช้รหัสเหตุผลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e8467-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="e8467-123">ถ้าคุณต้องการใช้รหัสเหตุผลคุณอาจจำเป็นต้องเพิ่มรหัสดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="e8467-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="e8467-124">ภายใต้ **รหัสเหตุผล** ให้เลือก **เพิ่ม** เลือกรหัสเหตุผลแล้วเลือกกล่องกาเครื่องหมายที่ **เปิดใช้งาน** ที่อยู่ด้านข้างรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="e8467-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="e8467-125">ภายใต้ **จำกัดการเข้าถึงบทบาทที่เลือกไว้** ให้เลือกว่าคุณต้องการจำกัดการเข้าถึงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e8467-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="e8467-126">จากนั้นเลือกบทบาทความปลอดภัยภายใต้ **บทบาทความปลอดภัยสำหรับชนิดการลางานนี้**</span><span class="sxs-lookup"><span data-stu-id="e8467-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="e8467-127">บาทความปลอดภัยถูกกำหนดไว้ในลำดับงานที่คุณเลือกไว้ภายใต้ **รหัสลำดับงาน** ก่อนหน้านี้ในกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="e8467-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="e8467-128">ภายใต้ **สีของปฏิทิน** ให้เลือกสีที่จะแสดงบนปฏิทินการลางานและการขาดงานสำหรับชนิดการลางานนี้</span><span class="sxs-lookup"><span data-stu-id="e8467-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="e8467-129">ภายใต้ **ความสัมพันธ์ของการระงับ** ให้เลือกว่าคุณต้องการให้ชนิดการลางานนี้ระงับชนิดการลางานอื่น หรือถูกระงับโดยชนิดการลางานอื่น</span><span class="sxs-lookup"><span data-stu-id="e8467-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="e8467-130">เมื่อมีการส่งคำขอการลางานสำหรับชนิดการระงับการลา จะมีการสร้างการระงับการลางานโดยอัตโนมัติสำหรับชนิดการลางานที่ถูกระงับ</span><span class="sxs-lookup"><span data-stu-id="e8467-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="e8467-131">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e8467-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="e8467-132">ตั้งค่าคอนฟิกกฎชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-132">Configure leave type rules</span></span>

1. <span data-ttu-id="e8467-133">ตั้งค่าตัวเลือกการปัดเศษสำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="e8467-134">ตัวเลือกประกอบด้วย **ไม่** **ขึ้น** **ลง** และ **ใกล้ที่สุด**</span><span class="sxs-lookup"><span data-stu-id="e8467-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="e8467-135">นอกจากนี้คุณยังสามารถตั้งค่าความแม่นยำในการปัดเศษสำหรับชนิดการลางานได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="e8467-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="e8467-136">ตั้งค่า **การแก้ไขวันหยุด** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="e8467-137">เมื่อคุณเลือกตัวเลือกนี้ทรัพยากรบุคคลจะใช้จำนวนวันหยุดที่อยู่ในวันทำงานเพื่อกำหนดวิธีการยกยอดเวลาหยุดพักสำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="e8467-138">ตัวอย่างเช่นถ้าวันคริสต์มาสตรงกันในวันจันทร์ ทรัพยากรบุคคลจะหัก 1 วันออกจากชนิดของการลาเมื่อกำลังประมวลผลรายการยกยอด</span><span class="sxs-lookup"><span data-stu-id="e8467-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="e8467-139">คุณตั้งค่าวันหยุดในปฏิทินเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="e8467-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="e8467-140">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [สร้างปฏิทินเวลาทำงาน](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="e8467-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="e8467-141">ตั้งค่า **ชนิดการลางานแบบยกยอดไป** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="e8467-142">เมื่อคุณเลือกตัวเลือกนี้ จะมีการโอนย้ายยอดดุลแบบยกยอดไปไปยังชนิดการลางานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e8467-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="e8467-143">นอกจากนี้ ชนิดการลางานแบบยกยอดไปยังต้องถูกรวมอยู่ในแผนการลางานและการขาดงานด้วย</span><span class="sxs-lookup"><span data-stu-id="e8467-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="e8467-144">กำหนด **กฎการหมดอายุ** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="e8467-145">เมื่อคุณตั้งค่าคอนฟิกตัวเลือกนี้ คุณสามารถเลือกหน่วยของวันหรือเดือน และกำหนดระยะเวลาสำหรับการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="e8467-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="e8467-146">นอกจากนี้ คุณยังสามารถตั้งค่าวันที่มีผลบังคับใช้ของกฎการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="e8467-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="e8467-147">วันที่มีผลบังคับใช้จะใช้เพื่อระบุว่าเมื่อใดที่จะเริ่มต้นการรันชุดงาน ซึ่งประมวลผลการหมดอายุการลางาน หรือวันที่ที่กฎนั้นจะมีผลบังคับ</span><span class="sxs-lookup"><span data-stu-id="e8467-147">The effective date is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="e8467-148">การหมดอายุด้วยตัวเอง จะเกิดขึ้นในวันที่เริ่มต้นของแผนการลางานเสมอ เมื่อชุดงานถูกตั้งค่าให้ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="e8467-148">The expiration itself will always happen on the leave plan start date once the batch job is set to process.</span></span> <span data-ttu-id="e8467-149">ตัวอย่างเช่น วันที่เริ่มต้นของแผนอาจเป็น 1/1/2020 แต่กฎจะไม่ถูกสร้างจนกว่าวันที่ 6/1/2020</span><span class="sxs-lookup"><span data-stu-id="e8467-149">For example, the plan start date may be 1/1/2020, but the rule wasn't created until 6/1/2020.</span></span> <span data-ttu-id="e8467-150">โดยการตั้งค่า วันที่มีผลบังคับใช้เป็น 6/1/2020 กฎจะได้รับการประมวลผลบนขอบเขตปีถัดไป คือวันที่ 1/1/2021</span><span class="sxs-lookup"><span data-stu-id="e8467-150">By setting the effective date to 6/1/2020, the rule will be processed on the next year boundary, so 1/1/2021.</span></span> <span data-ttu-id="e8467-151">ยอดดุลการลางานใดๆ ที่มีอยู่ในช่วงเวลาของการหมดอายุจะถูกลบออกจากชนิดของการลางาน และจะถูกสะท้อนให้เห็นในยอดดุลการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-151">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
## <a name="see-also"></a><span data-ttu-id="e8467-152">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="e8467-152">See also</span></span>

- [<span data-ttu-id="e8467-153">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="e8467-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="e8467-154">สร้างแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="e8467-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="e8467-155">สร้างปฏิทินเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="e8467-155">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="e8467-156">ระงับการลางาน</span><span class="sxs-lookup"><span data-stu-id="e8467-156">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
