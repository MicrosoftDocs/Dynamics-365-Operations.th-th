---
title: ตั้งรายการค้างรับแผนการลางานและการขาดงาน
description: คุณสามารถรับการลางานและขาดงาน Dynamics 365 Human Resources สำหรับพนักงานหลายคนหรือสำหรับแต่ละคน
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 86ca63b1703faa6f57ed2e5591c89a5e84363481
ms.sourcegitcommit: 318e406b84d43381d450272eb83c5eea9c5cf1c0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059484"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="7c49b-103">ตั้งรายการค้างรับแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="7c49b-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7c49b-104">คุณสามารถรับการลางานและขาดงาน Dynamics 365 Human Resources สำหรับพนักงานหลายคนหรือสำหรับแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="7c49b-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="7c49b-105">รับรู้การลางานและขาดงานสำหรับพนักงานหลายคน</span><span class="sxs-lookup"><span data-stu-id="7c49b-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="7c49b-106">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="7c49b-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7c49b-107">ภายใต้ **จัดการการลา** ให้เลือก **รับรู้แผนการลางานและขาดงานงาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="7c49b-108">กล่องโต้ตอบ **แผนการลางานและการขาดงานคงค้าง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c49b-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="7c49b-109">ใน **การคงค้าง** ให้เลือก **วันที่ของวันนี้** หรือเลือก **วันที่ที่กำหนดเอง** และป้อนวันที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7c49b-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="7c49b-110">ถ้าคุณต้องการเรียกใช้รายการคงค้างสำหรับบริษัททั้งหมด ให้เลือก **บริษัททั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7c49b-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="7c49b-111">ถ้าคุณต้องการประมวลผลรายการคงค้างสำหรับแผนการลางานเดียว ให้เลือก **ไม่มี** สำหรับ **แผนทั้งหมด** แล้วเลือก **แผนการลางาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="7c49b-112">ถ้าคุณเลือกบริษัททั้งหมด คุณไม่สามารถเลือกแผนการลางานแต่ละแผนได้</span><span class="sxs-lookup"><span data-stu-id="7c49b-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="7c49b-113">ถ้าคุณต้องการดำเนินการกระบวนการค้างรับในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7c49b-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="7c49b-114">ป้อนข้อมูลสำหรับการบวนการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="7c49b-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="7c49b-115">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="7c49b-116">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="7c49b-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-117">Select **OK**.</span></span> <span data-ttu-id="7c49b-118">กระบวนการค้างรับจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="7c49b-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="7c49b-119">รับรู้การลางานและขาดงานสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="7c49b-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="7c49b-120">บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**</span><span class="sxs-lookup"><span data-stu-id="7c49b-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="7c49b-121">ให้เลือก **การรับรู้การลางานและขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="7c49b-122">กล่องโต้ตอบ **แผนการลางานและการขาดงานคงค้าง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c49b-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="7c49b-123">ใน **การคงค้าง** ให้เลือก **วันที่ของวันนี้** หรือเลือก **วันที่ที่กำหนดเอง** และป้อนวันที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7c49b-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="7c49b-124">ถ้าคุณต้องการเรียกใช้รายการคงค้างสำหรับบริษัททั้งหมด ให้เลือก **บริษัททั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7c49b-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="7c49b-125">ถ้าคุณต้องการประมวลผลรายการคงค้างสำหรับแผนการลางานเดียว ให้เลือก **ไม่มี** สำหรับ **แผนทั้งหมด** แล้วเลือก **แผนการลางาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="7c49b-126">ถ้าคุณเลือกบริษัททั้งหมด คุณไม่สามารถเลือกแผนการลางานแต่ละแผนได้</span><span class="sxs-lookup"><span data-stu-id="7c49b-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="7c49b-127">ถ้าคุณต้องการดำเนินการกระบวนการค้างรับในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7c49b-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="7c49b-128">ป้อนข้อมูลสำหรับการบวนการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="7c49b-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="7c49b-129">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="7c49b-130">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="7c49b-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-131">Select **OK**.</span></span> <span data-ttu-id="7c49b-132">กระบวนการค้างรับจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="7c49b-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="7c49b-133">ลบการคงค้างของการลางานและการขาดงานสำหรับพนักงานหลายคน</span><span class="sxs-lookup"><span data-stu-id="7c49b-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="7c49b-134">ลบเรกคอร์ดการค้างรับค้างจ่ายสำหรับแผนและช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7c49b-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="7c49b-135">วันที่คงค้างต้องเป็นวันที่วันนี้หรือในอนาคต</span><span class="sxs-lookup"><span data-stu-id="7c49b-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="7c49b-136">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="7c49b-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7c49b-137">ภายใต้ **จัดการการลา** ให้เลือก **ลบการคงค้างของแผนการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="7c49b-138">ในกล่องโต้ตอบ **ลบการคงค้างของแผนการลางานและการขาดงาน** ให้เลือก **แผนการลางาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="7c49b-139">ถ้าสามารถใช้ได้ ให้เลือก **ลบการปรับปรุงยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="7c49b-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="7c49b-140">ป้อนหรือเลือก **วันที่การลางานคงค้าง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="7c49b-141">วันที่นี้ต้องเป็นวันที่วันนี้หรือในอนาคต</span><span class="sxs-lookup"><span data-stu-id="7c49b-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="7c49b-142">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-142">Select **OK**.</span></span> <span data-ttu-id="7c49b-143">กระบวนการคงค้างจะลบการคงค้างที่มีพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="7c49b-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="7c49b-144">ลบการคงค้างของการลางานและการขาดงานสำหรับพนักงานคนเดียว</span><span class="sxs-lookup"><span data-stu-id="7c49b-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="7c49b-145">บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**</span><span class="sxs-lookup"><span data-stu-id="7c49b-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="7c49b-146">เลือก **ลบการคงค้างของแผนการลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="7c49b-147">ในกล่องโต้ตอบ **ลบการคงค้างของแผนการลางานและการขาดงาน** ให้เลือก **แผนการลางาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="7c49b-148">ถ้าสามารถใช้ได้ ให้เลือก **ลบการปรับปรุงยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="7c49b-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="7c49b-149">ป้อนหรือเลือก **วันที่การลางานคงค้าง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="7c49b-150">วันที่นี้ต้องเป็นวันที่วันนี้หรือในอนาคต</span><span class="sxs-lookup"><span data-stu-id="7c49b-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="7c49b-151">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c49b-151">Select **OK**.</span></span> <span data-ttu-id="7c49b-152">กระบวนการคงค้างจะลบการคงค้างที่มีพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="7c49b-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="7c49b-153">ตรวจทานการคงค้างการลางานและกระบวนการลบ</span><span class="sxs-lookup"><span data-stu-id="7c49b-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="7c49b-154">**การตรวจสอบการคงค้างของการลางาน** จะแสดงขึ้นทุกครั้งที่คุณรันหรือลบการคงค้างสำหรับพนักงานหนึ่งคนหรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7c49b-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="7c49b-155">วันที่และบุคคลที่ดำเนินการจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c49b-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="7c49b-156">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="7c49b-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7c49b-157">ภายใต้ **จัดการการลา** ให้เลือก **ลบการตรวจสอบการคงค้างของการลางาน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="preview-leave-accrual-transaction-auditing"></a><span data-ttu-id="7c49b-158">(พรีวิว) การตรวจสอบธุรกรรมการยกยอดวันลางาน</span><span class="sxs-lookup"><span data-stu-id="7c49b-158">(Preview) Leave accrual transaction auditing</span></span>

[!include [Preview feature](includes/preview-feature.md)]

<span data-ttu-id="7c49b-159">คุณลักษณะการแสดงตัวอย่างนี้จะช่วยในการลางานและผู้จัดการการขาดงานจะเข้าใจธุรกรรมการลางานและธุรกรรมการรับรู้การขาดงาน ที่เกี่ยวข้องกับยอดดุลการหมดเวลาของพนักงานในชนิดการลางานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7c49b-159">This preview feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="7c49b-160">หากต้องการดูรายละเอียดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7c49b-160">To view transaction details:</span></span>

1. <span data-ttu-id="7c49b-161">บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**</span><span class="sxs-lookup"><span data-stu-id="7c49b-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="7c49b-162">เลือก **ดูการหมดเวลา** แล้วเลือกแท็บ **ยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="7c49b-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="7c49b-163">เมื่อต้องการดูธุรกรรมการรับรู้ที่เกี่ยวข้องกับชนิดการลางานเฉพาะ ให้เลือกค่าที่เป็นตัวเลขในคอลัมน์ **ยอดดุลปัจจุบัน**</span><span class="sxs-lookup"><span data-stu-id="7c49b-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="7c49b-164">เมื่อต้องการดูรายละเอียดธุรกรรมเกี่ยวกับจำนวนที่ตั้งค้างรับไว้ ให้เลือกแถวที่ตั้งค้างรับ เปิดแผง **ข้อมูลที่เกี่ยวข้อง** ทางด้านขวา แล้วเปิดส่วน **รายละเอียดธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="7c49b-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="7c49b-165">ส่วนรายละเอียดธุรกรรมจะแสดงดังนี้</span><span class="sxs-lookup"><span data-stu-id="7c49b-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="7c49b-166">การเปลี่ยนแปลงยอดดุลชนิดการลางานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="7c49b-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="7c49b-167">รายละเอียดการจ้างงานที่ใช้รอบระยะเวลาการรับรู้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="7c49b-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="7c49b-168">รายละเอียดเกี่ยวกับรอบระยะเวลาและอัตราการรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="7c49b-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="7c49b-169">การเปลี่ยนแปลงใด ๆ ที่มีการเปลี่ยนแปลงเพื่อออกจากการตั้งค่าคอนฟิกแผน</span><span class="sxs-lookup"><span data-stu-id="7c49b-169">Any changes made to leave plan configurations</span></span>

![แสดงการตรวจสอบธุรกรรมการยกยอดวันลางาน](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="7c49b-171">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="7c49b-171">See also</span></span>

[<span data-ttu-id="7c49b-172">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="7c49b-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="7c49b-173">สร้างแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="7c49b-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
