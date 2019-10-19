---
title: นำเสนอโปรแกรมสวัสดิการของพนักงาน
description: 'งานนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่ '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0285c2be49edde701d6c6cf83ccdeac994434ab
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190545"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="2174e-103">นำเสนอโปรแกรมสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="2174e-103">Deliver employee benefits program</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2174e-104">งานนี้จะแสดงวิธีการสร้างองค์ประกอบของสวัสดิการที่จะใช้เมื่อสร้างสวัสดิการใหม่ </span><span class="sxs-lookup"><span data-stu-id="2174e-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="2174e-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="2174e-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="2174e-106">งานนี้มีไว้สำหรับผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="2174e-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="2174e-107">สร้างองค์ประกอบของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="2174e-107">Create benefit elements</span></span>
1. <span data-ttu-id="2174e-108">งานนี้เริ่มต้นจากหน้ารายการสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="2174e-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="2174e-109">งานจะเริ่มต้นโดยการเปิดหน้านั้นหรือการค้นหาในหน้ารายการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="2174e-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="2174e-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2174e-110">Click New.</span></span>
3. <span data-ttu-id="2174e-111">ในฟิลด์ชนิด ให้ป้อนชื่อของประเภทของสวัสดิการที่คุณกำลังสร้าง</span><span class="sxs-lookup"><span data-stu-id="2174e-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="2174e-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2174e-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2174e-113">ในฟิลด์การลงทะเบียนที่เกิดขึ้นพร้อมกัน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="2174e-114">เพื่อจำกัดความสามารถของพนักงานในการลงทะเบียนในหลายแผนการรักษาพยาบาล ให้เลือกลงทะเบียนหนึ่งรายการต่อชนิด</span><span class="sxs-lookup"><span data-stu-id="2174e-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="2174e-115">ในฟิลด์ประเภทค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="2174e-116">คลิกที่แท็บแผน</span><span class="sxs-lookup"><span data-stu-id="2174e-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="2174e-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2174e-117">Click New.</span></span>
9. <span data-ttu-id="2174e-118">ในฟิลด์แผน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2174e-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="2174e-119">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2174e-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="2174e-120">ในฟิลด์ชนิด ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2174e-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="2174e-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2174e-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="2174e-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2174e-123">ในฟิลด์ผลกระทบของค่าจ้าง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="2174e-124">คลิกที่แท็บตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-124">Click the Options tab.</span></span>
16. <span data-ttu-id="2174e-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2174e-125">Click New.</span></span>
17. <span data-ttu-id="2174e-126">ในฟิลด์ตัวเลือก ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2174e-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="2174e-127">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2174e-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="2174e-128">สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="2174e-128">Create a benefit</span></span>
1. <span data-ttu-id="2174e-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2174e-129">Close the page.</span></span>
2. <span data-ttu-id="2174e-130">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="2174e-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="2174e-131">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2174e-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="2174e-132">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="2174e-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2174e-133">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2174e-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2174e-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2174e-135">ในฟิลด์ตัวเลือก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2174e-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2174e-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2174e-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="2174e-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2174e-138">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="2174e-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="2174e-139">คลิกที่สร้างสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="2174e-139">Click Create benefit.</span></span>
12. <span data-ttu-id="2174e-140">สลับการขยายของส่วนรายละเอียดค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="2174e-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="2174e-141">ในฟิลด์ความถี่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2174e-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="2174e-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2174e-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2174e-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="2174e-144">ในฟิลด์ข้อมูลพื้นฐาน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2174e-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="2174e-145">ในฟิลด์จำนวนหรืออัตรา ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2174e-145">In the Amount or rate field, enter a number.</span></span>

