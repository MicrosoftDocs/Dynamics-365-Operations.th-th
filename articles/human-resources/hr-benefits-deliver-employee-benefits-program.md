---
title: นำเสนอโปรแกรมสวัสดิการของพนักงาน
description: บทความนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: b8631e4f8cb2947ec7e09de86a7ceb075a83a453
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010798"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="0ef20-103">นำเสนอโปรแกรมสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="0ef20-103">Deliver employee benefits program</span></span>

<span data-ttu-id="0ef20-104">บทความนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="0ef20-104">This article shows you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="0ef20-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="0ef20-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="0ef20-106">งานนี้มีไว้สำหรับผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="0ef20-107">สร้างองค์ประกอบของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-107">Create benefit elements</span></span>
1. <span data-ttu-id="0ef20-108">งานนี้เริ่มต้นจากหน้ารายการสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="0ef20-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="0ef20-109">งานจะเริ่มต้นโดยการเปิดหน้านั้นหรือการค้นหาในหน้ารายการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="0ef20-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0ef20-110">Click New.</span></span>
3. <span data-ttu-id="0ef20-111">ในฟิลด์ชนิด ให้ป้อนชื่อของประเภทของสวัสดิการที่คุณกำลังสร้าง</span><span class="sxs-lookup"><span data-stu-id="0ef20-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="0ef20-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0ef20-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0ef20-113">ในฟิลด์การลงทะเบียนที่เกิดขึ้นพร้อมกัน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="0ef20-114">เพื่อจำกัดความสามารถของพนักงานในการลงทะเบียนในหลายแผนการรักษาพยาบาล ให้เลือกลงทะเบียนหนึ่งรายการต่อชนิด</span><span class="sxs-lookup"><span data-stu-id="0ef20-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="0ef20-115">ในฟิลด์ประเภทค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="0ef20-116">คลิกที่แท็บแผน</span><span class="sxs-lookup"><span data-stu-id="0ef20-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="0ef20-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0ef20-117">Click New.</span></span>
9. <span data-ttu-id="0ef20-118">ในฟิลด์แผน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0ef20-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="0ef20-119">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0ef20-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="0ef20-120">ในฟิลด์ชนิด ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0ef20-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="0ef20-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="0ef20-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="0ef20-123">ในฟิลด์ผลกระทบของค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="0ef20-124">คลิกที่แท็บตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-124">Click the Options tab.</span></span>
16. <span data-ttu-id="0ef20-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0ef20-125">Click New.</span></span>
17. <span data-ttu-id="0ef20-126">ในฟิลด์ตัวเลือก ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0ef20-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="0ef20-127">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0ef20-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="0ef20-128">สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-128">Create a benefit</span></span>
1. <span data-ttu-id="0ef20-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0ef20-129">Close the page.</span></span>
2. <span data-ttu-id="0ef20-130">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="0ef20-131">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0ef20-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="0ef20-132">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="0ef20-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0ef20-133">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="0ef20-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0ef20-135">ในฟิลด์ตัวเลือก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0ef20-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0ef20-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="0ef20-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="0ef20-138">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="0ef20-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="0ef20-139">คลิกที่สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-139">Click Create benefit.</span></span>
12. <span data-ttu-id="0ef20-140">สลับการขยายของส่วนรายละเอียดค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="0ef20-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="0ef20-141">ในฟิลด์ความถี่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0ef20-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0ef20-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ef20-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="0ef20-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0ef20-144">ในฟิลด์ข้อมูลพื้นฐาน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0ef20-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="0ef20-145">ในฟิลด์จำนวนหรืออัตรา ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0ef20-145">In the Amount or rate field, enter a number.</span></span>

