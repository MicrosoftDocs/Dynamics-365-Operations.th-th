--- 
title: "เปิดใช้งานกระบวนการค่าจ้างของเวลาและการเข้างาน"
description: "กระบวนงานนี้แสดงวิธีการเปิดใช้งานกระบวนการค่าจ้างสำหรับเวลาและการเข้างาน "
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 22ce633f65847f10fbe507b71bfc2bb33f595501
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="ec46f-103">เปิดใช้งานกระบวนการค่าจ้างของเวลาและการเข้างาน</span><span class="sxs-lookup"><span data-stu-id="ec46f-103">Enable the payroll process for time and attendance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec46f-104">กระบวนงานนี้แสดงวิธีการเปิดใช้งานกระบวนการค่าจ้างสำหรับเวลาและการเข้างาน </span><span class="sxs-lookup"><span data-stu-id="ec46f-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="ec46f-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="ec46f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="ec46f-106">สร้างชนิดค่าจ้างด้วยอัตราค่าจ้างที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="ec46f-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="ec46f-107">เวลาและการเข้างาน > การตั้งค่า > ค่าจ้าง > ชนิดค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="ec46f-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-108">Click New.</span></span>
3. <span data-ttu-id="ec46f-109">ในฟิลด์ชนิดค่าจ้าง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ec46f-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="ec46f-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ec46f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec46f-111">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ec46f-111">Click Save.</span></span>
6. <span data-ttu-id="ec46f-112">คลิกอัตรา</span><span class="sxs-lookup"><span data-stu-id="ec46f-112">Click Rates.</span></span>
    * <span data-ttu-id="ec46f-113">อัตราสำหรับชนิดค่าจ้างได้มีการตั้งค่าสำหรับช่วงเวลาเฉพาะ และคุณสามารถสร้างอัตราแต่ละอัตราสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="ec46f-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="ec46f-114">ไม่จำเป็นเสมอที่จะต้องสร้างอัตราสำหรับชนิดค่าจ้างในเวลาและการเข้างาน </span><span class="sxs-lookup"><span data-stu-id="ec46f-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="ec46f-115">ข้อมูลนี้อาจมีอยู่แล้วในระบบค่าจ้างที่ใช้ในการสร้างค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="ec46f-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-116">Click New.</span></span>
8. <span data-ttu-id="ec46f-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ec46f-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ec46f-118">ในฟิลด์อัตรา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ec46f-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="ec46f-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ec46f-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="ec46f-120">การสร้างข้อตกลงการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-120">Create a pay agreement</span></span>
1. <span data-ttu-id="ec46f-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ec46f-121">Close the page.</span></span>
2. <span data-ttu-id="ec46f-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ec46f-122">Close the page.</span></span>
3. <span data-ttu-id="ec46f-123">ไปที่ข้อตกลงการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="ec46f-124">เวลาและการเข้างาน > การตั้งค่า > ข้อตกลงการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="ec46f-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-125">Click New.</span></span>
5. <span data-ttu-id="ec46f-126">ในฟิลด์ข้อตกลงการชำระค่าจ้าง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ec46f-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="ec46f-127">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ec46f-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="ec46f-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ec46f-128">Click Save.</span></span>
8. <span data-ttu-id="ec46f-129">คลิกรายการข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="ec46f-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="ec46f-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ec46f-130">Click New.</span></span>
10. <span data-ttu-id="ec46f-131">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ec46f-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ec46f-132">ในฟิลด์ชนิดโพรไฟล์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ec46f-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="ec46f-133">ในฟิลด์ชนิดค่าจ้าง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ec46f-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="ec46f-134">ตั้งค่าข้อตกลงการชำระค่าจ้างสำหรับเวลาและการลงทะเบียนผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="ec46f-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="ec46f-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ec46f-135">Close the page.</span></span>
2. <span data-ttu-id="ec46f-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ec46f-136">Close the page.</span></span>
3. <span data-ttu-id="ec46f-137">ไปที่ผู้ปฏิบัติงานของการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="ec46f-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="ec46f-138">เวลาและการเข้างาน > การตั้งค่า > ผู้ปฏิบัติงานของการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="ec46f-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="ec46f-139">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ec46f-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ec46f-140">คลิกแท็บการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="ec46f-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="ec46f-141">ขยายส่วนเวลาของการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="ec46f-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="ec46f-142">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ec46f-142">Click Edit.</span></span>
8. <span data-ttu-id="ec46f-143">ในฟิลด์ข้อตกลงการชำระค่าจ้าง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ec46f-143">In the Pay agreement field, enter or select a value.</span></span>


