---
title: เปิดใช้งานกระบวนการค่าจ้างของเวลาและการเข้างาน
description: 'กระบวนงานนี้แสดงวิธีการเปิดใช้งานกระบวนการค่าจ้างสำหรับเวลาและการเข้างาน '
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a52ad77d3f03898d26c225900fe79ca30493a67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843540"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="fd7d7-103">เปิดใช้งานกระบวนการค่าจ้างของเวลาและการเข้างาน</span><span class="sxs-lookup"><span data-stu-id="fd7d7-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd7d7-104">กระบวนงานนี้แสดงวิธีการเปิดใช้งานกระบวนการค่าจ้างสำหรับเวลาและการเข้างาน </span><span class="sxs-lookup"><span data-stu-id="fd7d7-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="fd7d7-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="fd7d7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="fd7d7-106">สร้างชนิดค่าจ้างด้วยอัตราค่าจ้างที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="fd7d7-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="fd7d7-107">เวลาและการเข้างาน > การตั้งค่า > ค่าจ้าง > ชนิดค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="fd7d7-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-108">Click New.</span></span>
3. <span data-ttu-id="fd7d7-109">ในฟิลด์ชนิดค่าจ้าง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="fd7d7-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fd7d7-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fd7d7-111">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fd7d7-111">Click Save.</span></span>
6. <span data-ttu-id="fd7d7-112">คลิกอัตรา</span><span class="sxs-lookup"><span data-stu-id="fd7d7-112">Click Rates.</span></span>
    * <span data-ttu-id="fd7d7-113">อัตราสำหรับชนิดค่าจ้างได้มีการตั้งค่าสำหรับช่วงเวลาเฉพาะ และคุณสามารถสร้างอัตราแต่ละอัตราสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="fd7d7-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="fd7d7-114">ไม่จำเป็นเสมอที่จะต้องสร้างอัตราสำหรับชนิดค่าจ้างในเวลาและการเข้างาน </span><span class="sxs-lookup"><span data-stu-id="fd7d7-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="fd7d7-115">ข้อมูลนี้อาจมีอยู่แล้วในระบบค่าจ้างที่ใช้ในการสร้างค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="fd7d7-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-116">Click New.</span></span>
8. <span data-ttu-id="fd7d7-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fd7d7-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fd7d7-118">ในฟิลด์อัตรา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="fd7d7-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="fd7d7-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fd7d7-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="fd7d7-120">การสร้างข้อตกลงการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-120">Create a pay agreement</span></span>
1. <span data-ttu-id="fd7d7-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fd7d7-121">Close the page.</span></span>
2. <span data-ttu-id="fd7d7-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fd7d7-122">Close the page.</span></span>
3. <span data-ttu-id="fd7d7-123">ไปที่ข้อตกลงการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="fd7d7-124">เวลาและการเข้างาน > การตั้งค่า > ข้อตกลงการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="fd7d7-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-125">Click New.</span></span>
5. <span data-ttu-id="fd7d7-126">ในฟิลด์ข้อตกลงการชำระค่าจ้าง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="fd7d7-127">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fd7d7-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="fd7d7-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fd7d7-128">Click Save.</span></span>
8. <span data-ttu-id="fd7d7-129">คลิกรายการข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="fd7d7-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-130">Click New.</span></span>
10. <span data-ttu-id="fd7d7-131">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fd7d7-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="fd7d7-132">ในฟิลด์ชนิดโพรไฟล์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fd7d7-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="fd7d7-133">ในฟิลด์ชนิดค่าจ้าง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="fd7d7-134">ตั้งค่าข้อตกลงการชำระค่าจ้างสำหรับเวลาและการลงทะเบียนผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="fd7d7-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="fd7d7-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fd7d7-135">Close the page.</span></span>
2. <span data-ttu-id="fd7d7-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fd7d7-136">Close the page.</span></span>
3. <span data-ttu-id="fd7d7-137">ไปที่ผู้ปฏิบัติงานของการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="fd7d7-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="fd7d7-138">เวลาและการเข้างาน > การตั้งค่า > ผู้ปฏิบัติงานของการลงทะเบียนเวลา</span><span class="sxs-lookup"><span data-stu-id="fd7d7-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="fd7d7-139">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fd7d7-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="fd7d7-140">คลิกแท็บการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="fd7d7-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="fd7d7-141">ขยายส่วนเวลาของการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="fd7d7-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="fd7d7-142">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="fd7d7-142">Click Edit.</span></span>
8. <span data-ttu-id="fd7d7-143">ในฟิลด์ข้อตกลงการชำระค่าจ้าง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fd7d7-143">In the Pay agreement field, enter or select a value.</span></span>

