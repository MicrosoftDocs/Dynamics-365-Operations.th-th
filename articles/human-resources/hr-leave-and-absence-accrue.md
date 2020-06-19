---
title: ตั้งรายการค้างรับแผนการลางานและการขาดงาน
description: คุณสามารถรับการลางานและขาดงาน Dynamics 365 Human Resources สำหรับพนักงานหลายคนหรือสำหรับแต่ละคน
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
ms.openlocfilehash: f045cb7ab9f5e7aa4259f29e1b026f110425c236
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429070"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="3f2df-103">ตั้งรายการค้างรับแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="3f2df-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="3f2df-104">คุณสามารถรับการลางานและขาดงาน Dynamics 365 Human Resources สำหรับพนักงานหลายคนหรือสำหรับแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="3f2df-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="3f2df-105">รับรู้การลางานและขาดงานสำหรับพนักงานหลายคน</span><span class="sxs-lookup"><span data-stu-id="3f2df-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="3f2df-106">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="3f2df-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="3f2df-107">ภายใต้ **จัดการการลา** ให้เลือก **รับรู้แผนการลางานและขาดงานงาน**</span><span class="sxs-lookup"><span data-stu-id="3f2df-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="3f2df-108">กล่องโต้ตอบ **แผนการลางานและการขาดงานคงค้าง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="3f2df-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="3f2df-109">ใน **การคงค้าง** ให้เลือก **วันที่ของวันนี้** หรือเลือก **วันที่ที่กำหนดเอง** และป้อนวันที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="3f2df-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="3f2df-110">ถ้าคุณต้องการดำเนินการกระบวนการค้างรับในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3f2df-110">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="3f2df-111">ป้อนข้อมูลสำหรับการบวนการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="3f2df-111">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="3f2df-112">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-112">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="3f2df-113">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-113">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="3f2df-114">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-114">Select **OK**.</span></span> <span data-ttu-id="3f2df-115">กระบวนการค้างรับจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="3f2df-115">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="3f2df-116">รับรู้การลางานและขาดงานสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="3f2df-116">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="3f2df-117">บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**</span><span class="sxs-lookup"><span data-stu-id="3f2df-117">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="3f2df-118">ให้เลือก **การรับรู้การลางานและขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="3f2df-118">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="3f2df-119">กล่องโต้ตอบ **แผนการลางานและการขาดงานคงค้าง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="3f2df-119">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="3f2df-120">ใน **การคงค้าง** ให้เลือก **วันที่ของวันนี้** หรือเลือก **วันที่ที่กำหนดเอง** และป้อนวันที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="3f2df-120">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="3f2df-121">ถ้าคุณต้องการดำเนินการกระบวนการค้างรับในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3f2df-121">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="3f2df-122">ป้อนข้อมูลสำหรับการบวนการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="3f2df-122">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="3f2df-123">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-123">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="3f2df-124">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-124">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="3f2df-125">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-125">Select **OK**.</span></span> <span data-ttu-id="3f2df-126">กระบวนการค้างรับจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="3f2df-126">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="3f2df-127">ลบการคงค้างของการลางานและการขาดงานสำหรับพนักงานหลายคน</span><span class="sxs-lookup"><span data-stu-id="3f2df-127">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="3f2df-128">ลบเรกคอร์ดการค้างรับค้างจ่ายสำหรับแผนและช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3f2df-128">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="3f2df-129">วันที่คงค้างต้องเป็นวันที่วันนี้หรือในอนาคต</span><span class="sxs-lookup"><span data-stu-id="3f2df-129">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="3f2df-130">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="3f2df-130">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="3f2df-131">ภายใต้ **จัดการการลา** ให้เลือก **ลบการคงค้างของแผนการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="3f2df-131">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="3f2df-132">ในกล่องโต้ตอบ **ลบการคงค้างของแผนการลางานและการขาดงาน** ให้เลือก **แผนการลางาน**</span><span class="sxs-lookup"><span data-stu-id="3f2df-132">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="3f2df-133">ถ้าสามารถใช้ได้ ให้เลือก **ลบการปรับปรุงยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="3f2df-133">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="3f2df-134">ป้อนหรือเลือก **วันที่การลางานคงค้าง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-134">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="3f2df-135">วันที่นี้ต้องเป็นวันที่วันนี้หรือในอนาคต</span><span class="sxs-lookup"><span data-stu-id="3f2df-135">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="3f2df-136">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-136">Select **OK**.</span></span> <span data-ttu-id="3f2df-137">กระบวนการคงค้างจะลบการคงค้างที่มีพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="3f2df-137">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="3f2df-138">ลบการคงค้างของการลางานและการขาดงานสำหรับพนักงานคนเดียว</span><span class="sxs-lookup"><span data-stu-id="3f2df-138">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="3f2df-139">บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**</span><span class="sxs-lookup"><span data-stu-id="3f2df-139">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="3f2df-140">เลือก **ลบการคงค้างของแผนการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="3f2df-140">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="3f2df-141">ในกล่องโต้ตอบ **ลบการคงค้างของแผนการลางานและการขาดงาน** ให้เลือก **แผนการลางาน**</span><span class="sxs-lookup"><span data-stu-id="3f2df-141">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="3f2df-142">ถ้าสามารถใช้ได้ ให้เลือก **ลบการปรับปรุงยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="3f2df-142">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="3f2df-143">ป้อนหรือเลือก **วันที่การลางานคงค้าง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-143">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="3f2df-144">วันที่นี้ต้องเป็นวันที่วันนี้หรือในอนาคต</span><span class="sxs-lookup"><span data-stu-id="3f2df-144">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="3f2df-145">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3f2df-145">Select **OK**.</span></span> <span data-ttu-id="3f2df-146">กระบวนการคงค้างจะลบการคงค้างที่มีพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="3f2df-146">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="3f2df-147">ตรวจทานการคงค้างการลางานและกระบวนการลบ</span><span class="sxs-lookup"><span data-stu-id="3f2df-147">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="3f2df-148">**การตรวจสอบการคงค้างของการลางาน** จะแสดงขึ้นทุกครั้งที่คุณรันหรือลบการคงค้างสำหรับพนักงานหนึ่งคนหรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3f2df-148">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="3f2df-149">วันที่และบุคคลที่ดำเนินการจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="3f2df-149">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="3f2df-150">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="3f2df-150">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="3f2df-151">ภายใต้ **จัดการการลา** ให้เลือก **ลบการตรวจสอบการคงค้างของการลางาน**</span><span class="sxs-lookup"><span data-stu-id="3f2df-151">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="3f2df-152">ตั้งค่าคอนฟิกคุณลักษณะตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3f2df-152">Configure preview features</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="3f2df-153">ถ้าคุณได้เปิดใช้งานคุณลักษณะตัวอย่างสำหรับการลางานและการขาดงานคุณต้องตั้งค่าคอนฟิกการตั้งค่าสำหรับผู้ใช้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="3f2df-153">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

### <a name="accrue-leave-per-company-or-per-leave-plan"></a><span data-ttu-id="3f2df-154">ตั้งรายการค้างรับสำหรับแต่ละบริษัทหรือสำหรับแผนการลางานแต่ละแผน</span><span class="sxs-lookup"><span data-stu-id="3f2df-154">Accrue leave per company or per leave plan</span></span>

<span data-ttu-id="3f2df-155">เมื่อตั้งรายการค้างรับแผนการลางานและการขาดงาน คุณสามารถเลือกที่จะตั้งรายการค้างรับสำหรับบริษัททั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="3f2df-155">When accruing leave and absence plans, you can choose to accrue for all companies.</span></span> <span data-ttu-id="3f2df-156">ถ้าคุณเลือกบริษัททั้งหมด คุณไม่สามารถเลือกแผนการลางานแต่ละแผนได้</span><span class="sxs-lookup"><span data-stu-id="3f2df-156">If you choose all companies, you can't select individual leave plans.</span></span> <span data-ttu-id="3f2df-157">ถ้าคุณเลือกที่จะไม่ตั้งรายการค้างรับสำหรับบริษัททั้งหมด คุณสามารถตั้งรายการค้างรับสำหรับแผนการลางานที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="3f2df-157">If you choose to not accrue for all companies, you can accrue for a specific leave plan.</span></span> 

<span data-ttu-id="3f2df-158">ตัวเลือกเหล่านี้จะพร้อมใช้งาน เมื่อตั้งรายการค้างรับสำหรับพนักงานทุกคนหรือพนักงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="3f2df-158">These options are available when accruing for all employees or individual employees.</span></span> 

## <a name="see-also"></a><span data-ttu-id="3f2df-159">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3f2df-159">See also</span></span>

[<span data-ttu-id="3f2df-160">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="3f2df-160">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="3f2df-161">สร้างแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="3f2df-161">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
