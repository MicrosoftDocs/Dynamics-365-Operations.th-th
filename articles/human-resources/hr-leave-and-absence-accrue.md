---
title: ตั้งรายการค้างรับแผนการลางานและการขาดงาน
description: คุณสามารถรับการลางานและขาดงาน Dynamics 365 Human Resources สำหรับพนักงานหลายคนหรือสำหรับแต่ละคน
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: ba60fc2e5b17ec32aa6ad7eb104e8ae55ddee3bb
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092349"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="75a0e-103">ตั้งรายการค้างรับแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="75a0e-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="75a0e-104">คุณสามารถรับการลางานและขาดงาน Dynamics 365 Human Resources สำหรับพนักงานหลายคนหรือสำหรับแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="75a0e-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="75a0e-105">รับรู้การลางานและขาดงานสำหรับพนักงานหลายคน</span><span class="sxs-lookup"><span data-stu-id="75a0e-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="75a0e-106">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="75a0e-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="75a0e-107">ภายใต้ **จัดการการลา** ให้เลือก **รับรู้แผนการลางานและขาดงานงาน**</span><span class="sxs-lookup"><span data-stu-id="75a0e-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="75a0e-108">ในกล่องโต้ตอบ **รับรู้แผนการลางานและขาดงาน** ใน **ค้างรับค้าง** เลือกอย่างใดอย่างหนึ่ง **วันที่วันนี้** หรือเลือก **วันที่ที่กำหนดเอง** และป้อนวันที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="75a0e-108">In the **Accrue leave and absence plans** dialog box, in **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="75a0e-109">ถ้าคุณต้องการดำเนินการกระบวนการค้างรับในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="75a0e-109">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="75a0e-110">ป้อนข้อมูลสำหรับการบวนการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="75a0e-110">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="75a0e-111">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="75a0e-111">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="75a0e-112">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="75a0e-112">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="75a0e-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="75a0e-113">Select **OK**.</span></span> <span data-ttu-id="75a0e-114">กระบวนการค้างรับจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="75a0e-114">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="75a0e-115">รับรู้การลางานและขาดงานสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="75a0e-115">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="75a0e-116">บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**</span><span class="sxs-lookup"><span data-stu-id="75a0e-116">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="75a0e-117">ให้เลือก **การรับรู้การลางานและขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="75a0e-117">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="75a0e-118">ในกล่องโต้ตอบ **รับรู้แผนการลางานและขาดงาน** ใน **ค้างรับค้าง** เลือกอย่างใดอย่างหนึ่ง **วันที่วันนี้** หรือเลือก **วันที่ที่กำหนดเอง** และป้อนวันที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="75a0e-118">In the **Accrue leave and absence plans** dialog box, in **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="75a0e-119">ถ้าคุณต้องการดำเนินการกระบวนการค้างรับในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="75a0e-119">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="75a0e-120">ป้อนข้อมูลสำหรับการบวนการค้างรับ</span><span class="sxs-lookup"><span data-stu-id="75a0e-120">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="75a0e-121">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="75a0e-121">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="75a0e-122">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="75a0e-122">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="75a0e-123">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="75a0e-123">Select **OK**.</span></span> <span data-ttu-id="75a0e-124">กระบวนการค้างรับจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="75a0e-124">The accrual process will run with the parameters you set.</span></span>

## <a name="preview-features-for-leave-and-absence"></a><span data-ttu-id="75a0e-125">แสดงตัวอย่างคุณลักษณะสำหรับการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="75a0e-125">Preview features for Leave and absence</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="75a0e-126">คุณสามารถเปิดใช้งานลักษณะการทำงานการแสดงตัวอย่างต่อไปนี้สำหรับการลางานและการขาดงาน:</span><span class="sxs-lookup"><span data-stu-id="75a0e-126">You can enable the following preview features for Leave and absence:</span></span>

- <span data-ttu-id="75a0e-127">**ลบการรับรู้การลางานและขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="75a0e-127">**Delete leave and absence accruals**.</span></span> <span data-ttu-id="75a0e-128">ลบเรกคอร์ดการค้างรับค้างจ่ายสำหรับแผนและช่วงวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="75a0e-128">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="75a0e-129">วันที่คงค้างต้องเป็นวันที่วันนี้หรือในอนาคต</span><span class="sxs-lookup"><span data-stu-id="75a0e-129">Accrual dates must be dated today or in the future.</span></span>

- <span data-ttu-id="75a0e-130">**การตรวจสอบการลาหยุดคงค้าง**</span><span class="sxs-lookup"><span data-stu-id="75a0e-130">**Leave accrual audit**.</span></span> <span data-ttu-id="75a0e-131">แสดงแต่ละครั้งที่มีคนดำเนินการหรือลบรายการคงค้างสำหรับพนักงานหนึ่งคนหรือทั้งหมด พร้อมกับวันที่และผู้ที่ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="75a0e-131">Displays each time someone runs or deletes an accrual for one or all employees, along with the date and who performed the action.</span></span>

## <a name="see-also"></a><span data-ttu-id="75a0e-132">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="75a0e-132">See also</span></span>

- [<span data-ttu-id="75a0e-133">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="75a0e-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="75a0e-134">การสร้างแผนการลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="75a0e-134">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)