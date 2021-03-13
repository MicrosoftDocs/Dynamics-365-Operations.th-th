---
title: พัฒนาโครงสร้างค่าตอบแทน
description: บทความนี้นำไปสู่กระบวนการในการสร้างแผนค่าตอบแทนคงที่ และการลงทะเบียนพนักงานในแผนโดยใช้กฎการมีคุณสมบัติเหมาะสม
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a5e7ef2021e41c13b82523f2dc6a1b09bd1ba9f
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115907"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="70485-103">พัฒนาโครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="70485-103">Develop a compensation structure</span></span>

<span data-ttu-id="70485-104">บทความนี้นำไปสู่กระบวนการในการสร้างแผนค่าตอบแทนคงที่ และการลงทะเบียนพนักงานในแผนโดยใช้กฎการมีคุณสมบัติเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="70485-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="70485-105">บทความนี้ใช้ข้อมูลสาธิต USMF และใช้กับผู้จัดการฝ่ายผลตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="70485-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="70485-106">สร้างแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="70485-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="70485-107">เลือก **การจัดการค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="70485-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="70485-108">เลือก **แผนค่าตอบแทนคงที่**</span><span class="sxs-lookup"><span data-stu-id="70485-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="70485-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="70485-109">Select **New**.</span></span>

4. <span data-ttu-id="70485-110">ในฟิลด์ **แผน** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="70485-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="70485-111">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="70485-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="70485-112">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="70485-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="70485-113">ในฟิลด์ **ชนิด** ให้เลือกว่าแผนค่าตอบแทนคงที่เป็นแผน **แถบ** **ระดับ** หรือ **ลำดับขั้น**</span><span class="sxs-lookup"><span data-stu-id="70485-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="70485-114">กล่องกาเครื่องหมาย **อนุญาตคำแนะนำแล้ว** ทำหน้าที่เป็นค่าเริ่มต้นสำหรับการดำเนินการใดๆ ที่เพิ่มเข้าไปในแผนนี้ในเหตุการณ์ของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="70485-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="70485-115">คำแนะนำที่ได้อนุญาตทำให้คุณสามารถแทนที่ยอดเงินตามผลงานที่คำนวณได้ เมื่อมีการประมวลผลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="70485-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="70485-116">ฟิลด์ **การยอมรับการอยู่นอกช่วง** ช่วยให้คุณสามารถระบุวิธีที่คุณต้องการจัดการกับยอดเงินค่าตอบแทนที่อยู่นอกช่วงโครงสร้างค่าตอบแทนที่ระบุไว้สำหรับระดับที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="70485-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="70485-117">การตั้งค่าฟิลด์ **การยอมรับการอยู่นอกช่วง** เป็น **ไม่** ช่วยให้คุณสามารถใช้ยอดเงินค่าตอบแทนใดๆ ได้</span><span class="sxs-lookup"><span data-stu-id="70485-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="70485-118">**ค่าเผื่อแบบผ่อนปรน** จะแจ้งเตือนผู้ใช้ ถ้ายอดเงินค่าตอบแทนน้อยกว่าปริมาณขั้นต่ำหรือมากกว่าปริมาณสูงสุดของจุดอ้างอิงสำหรับระดับนั้น</span><span class="sxs-lookup"><span data-stu-id="70485-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="70485-119">ผู้ใช้สามารถละเว้นคำเตือนและดำเนินการต่อได้</span><span class="sxs-lookup"><span data-stu-id="70485-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="70485-120">**ค่าเผื่อแบบเข้มขวด** จะสร้างข้อผิดพลาด ถ้าค่าตอบแทนของพนักงานอยู่นอกเหนือจุดอ้างอิงระดับต่ำสุดและสูงสุดสำหรับระดับนั้น และจะปรับค่าตอบแทนของพนักงานให้อยู่ภายในช่วงโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="70485-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="70485-121">ฟิลด์ **กฎการจ้างงาน** จะคำนวณค่าตอบแทนของพนักงานในระหว่างเหตุการณ์ในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="70485-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="70485-122">**กฎการจ้างงาน** ของ **เปอร์เซ็นต์** จะคำนวณการเพิ่มขึ้นที่เป็นสัดส่วนสำหรับระยะเวลาที่ผู้ปฏิบัติงานได้ถูกจ้างงานในวงจร</span><span class="sxs-lookup"><span data-stu-id="70485-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="70485-123">ในฟิลด์ **สกุลเงิน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="70485-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="70485-124">ในฟิลด์ **การแปลงอัตราค่าจ้าง** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="70485-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="70485-125">ขยายส่วน **เมทริกซ์การใช้ช่วง**</span><span class="sxs-lookup"><span data-stu-id="70485-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="70485-126">อีกทางเลือกหนึ่งคือ เพิ่มช่วงเรกคอร์ดที่ใช้ประโยชน์ให้พนักงานได้เข้าถึงจุดกึ่งกลางเร็วขึ้น และทำให้พนักงานเข้าถึงจำนวนสูงสุดของช่วงช้าลง</span><span class="sxs-lookup"><span data-stu-id="70485-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="70485-127">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="70485-127">Select **Save**.</span></span> <span data-ttu-id="70485-128">การดำเนินการนี้จะเปิดใช้งานปุ่ม **ตั้งค่าค่าตอบแทน** และดำเนินการกำหนดโครงสร้างค่าตอบแทนสำหรับแผนของคุณต่อ</span><span class="sxs-lookup"><span data-stu-id="70485-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="70485-129">เลือก **ตั้งค่าค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="70485-129">Select **Set up compensation**.</span></span> <span data-ttu-id="70485-130">คุณสามารถสร้างโครงสร้างค่าตอบแทนโดยใช้หนึ่งในสามวิธีเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="70485-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="70485-131">สร้างโครงสร้างใหม่ทั้งหมดโดยการเลือกชุดของจุดอ้างอิงและการเพิ่มระดับเพื่อสร้างโครงสร้างของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="70485-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="70485-132">คัดลอกโครงสร้างค่าตอบแทนจากแผนที่มีอยู่เสมือนเป็นจุดเริ่มต้นและปรับเปลี่ยนสำหรับแผนใหม่</span><span class="sxs-lookup"><span data-stu-id="70485-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="70485-133">เลือกกริดค่าตอบแทนที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="70485-133">Select an existing compensation grid.</span></span> <span data-ttu-id="70485-134">ถ้าแผนอื่นใช้กริดค่าตอบแทนอยู่แล้ว แผนอื่นยังจะมีผลต่อการเปลี่ยนแปลงใดๆ ที่คุณทำต่อกริดด้วย</span><span class="sxs-lookup"><span data-stu-id="70485-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="70485-135">เลือก **สร้างเมทริกซ์ค่าตอบแทนใหม่จากเมทริกซ์ค่าตอบแทนที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="70485-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="70485-136">ในฟิลด์ **คัดลอกจากกริด** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="70485-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="70485-137">อีกทางหนึ่งคือ คุณสามารถเปลี่ยนชื่อของกริดค่าตอบแทนใหม่ที่คุณสร้าง โดยการคัดลอกกริดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="70485-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="70485-138">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="70485-138">Select **OK**.</span></span>

19. <span data-ttu-id="70485-139">เลือก **การเปลี่ยนแปลงโดยรวม**</span><span class="sxs-lookup"><span data-stu-id="70485-139">Select **Mass change**.</span></span> <span data-ttu-id="70485-140">**การเปลี่ยนแปลงโดยรวม** ช่วยให้คุณสามารถรักษายอดเมทริกซ์ค่าตอบแทน ด้วยการใช้เปอร์เซ็นต์หรือยอดเงินคงที่ที่เพิ่มขึ้นหนึ่งระดับหรือหลายระดับ หรือจุดอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="70485-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="70485-141">ในฟิลด์ **ยอดการปรับปรุง** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="70485-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="70485-142">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="70485-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="70485-143">คลิก **นำไปใช้กับกริด**</span><span class="sxs-lookup"><span data-stu-id="70485-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="70485-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70485-144">Close the page.</span></span> <span data-ttu-id="70485-145">หลังจากที่คุณสร้างโครงสร้างค่าตอบแทน คุณสามารถเลือกจุดอ้างอิงที่จะใช้เป็นจุดควบคุมสำหรับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="70485-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="70485-146">จุดควบคุมจะใช้ในการคำนวณอัตราส่วนค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="70485-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="70485-147">ในฟิลด์ **จุดควบคุม** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="70485-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="70485-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70485-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="70485-149">สร้างกฎการมีคุณสมบัติเหมาะสมสำหรับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="70485-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="70485-150">คุณไม่สามารถกำหนดแผนค่าตอบแทนคงที่ให้กับพนักงานได้จนกว่าคุณจะกำหนดกฎการมีคุณสมบัติเหมาะสมสำหรับแผน</span><span class="sxs-lookup"><span data-stu-id="70485-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="70485-151">เลือก **กฎการมีคุณสมบัติเหมาะสม**</span><span class="sxs-lookup"><span data-stu-id="70485-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="70485-152">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="70485-152">Select **New**.</span></span>

3. <span data-ttu-id="70485-153">ในฟิลด์ **การมีสิทธิ์** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="70485-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="70485-154">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="70485-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="70485-155">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="70485-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="70485-156">ทั้งแผนค่าตอบแทนคงที่และผันแปรใช้กฎการมีคุณสมบัติเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="70485-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="70485-157">ในฟิลด์ **ชนิด** ให้เลือกชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="70485-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="70485-158">ในฟิลด์ **แผน** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="70485-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="70485-159">เลือกเกณฑ์ที่พนักงานต้องปฏิบัติตามเพื่อให้มีสิทธิ์ในแผนค่าตอบแทน </span><span class="sxs-lookup"><span data-stu-id="70485-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="70485-160">เกณฑ์อาจประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="70485-160">Criteria can include:</span></span>

    - <span data-ttu-id="70485-161">**แผนก**</span><span class="sxs-lookup"><span data-stu-id="70485-161">**Department**</span></span>
    - <span data-ttu-id="70485-162">**สหภาพแรงงาน**</span><span class="sxs-lookup"><span data-stu-id="70485-162">**Labor union**</span></span>
    - <span data-ttu-id="70485-163">**สถานที่** (**ภูมิภาคของค่าตอบแทน**)</span><span class="sxs-lookup"><span data-stu-id="70485-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="70485-164">**งาน**</span><span class="sxs-lookup"><span data-stu-id="70485-164">**Job**</span></span>
    - <span data-ttu-id="70485-165">**ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="70485-165">**Function**</span></span>
    - <span data-ttu-id="70485-166">**ชนิดงาน**</span><span class="sxs-lookup"><span data-stu-id="70485-166">**Job type**</span></span>
    - <span data-ttu-id="70485-167">**ระดับค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="70485-167">**Compensation level**</span></span>
    
    <span data-ttu-id="70485-168">พนักงานต้องปฏิบัติตรงตามเกณฑ์ที่ระบุทั้งหมดเพื่อให้มีสิทธิ์ในแผนค่าตอบแทน </span><span class="sxs-lookup"><span data-stu-id="70485-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="70485-169">ถ้าคุณไม่ได้ระบุเกณฑ์ใดๆ พนักงานทั้งหมดมีสิทธิ์ในแผนค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="70485-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="70485-170">ถ้าพนักงานไม่ตรงตามเกณฑ์ที่ระบุในกฎการมีคุณสมบัติเหมาะสม หรือไม่ได้ระบุกฎการมีคุณสมบัติเหมาะสมสำหรับแผนค่าตอบแทน แผนค่าตอบแทนจะไม่ปรากฏในการค้นหา เมื่อคุณสร้างเรกคอร์ดค่าตอบแทนคงที่สำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="70485-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="70485-171">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70485-171">Close the page.</span></span>

8. <span data-ttu-id="70485-172">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70485-172">Close the page.</span></span>

