---
title: ตั้งค่าคอนฟิกต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่าย
description: กระบวนงานนี้แสดงวิธีการตั้งค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่ายสำหรับโครงการ
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845910"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="70f4b-103">ตั้งค่าคอนฟิกต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="70f4b-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70f4b-104">กระบวนงานนี้แสดงวิธีการตั้งค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="70f4b-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="70f4b-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="70f4b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="70f4b-106">ไปที่ การจัดการและการบัญชีโครงการ > การตั้งค่า > ราคา > ราคาต้นทุน (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="70f4b-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="70f4b-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="70f4b-107">Click New.</span></span>
3. <span data-ttu-id="70f4b-108">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="70f4b-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="70f4b-109">ในฟิลด์ราคาต้นทุน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="70f4b-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="70f4b-110">คุณสามารถตั้งค่าราคาต้นทุนมาตรฐานสำหรับประเภทโครงการ หรือคุณสามารถตั้งค่าราคาต้นทุนตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ หรือข้อมูลใดๆ ดังกล่าวรวมกัน</span><span class="sxs-lookup"><span data-stu-id="70f4b-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="70f4b-111">ราคาต้นทุนที่จะนำไปใช้เป็นราคาต้นทุนที่มีรายละเอียดในระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70f4b-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="70f4b-112">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="70f4b-112">Click Save.</span></span>
6. <span data-ttu-id="70f4b-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70f4b-113">Close the page.</span></span>
7. <span data-ttu-id="70f4b-114">ไปที่ การจัดการและการบัญชีโครงการ > ตั้งค่า > ราคา > ราคาขาย (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="70f4b-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="70f4b-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="70f4b-115">Click New.</span></span>
9. <span data-ttu-id="70f4b-116">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="70f4b-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="70f4b-117">ในฟิลด์ มีผลบังคับใช้สำหรับ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="70f4b-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="70f4b-118">ในฟิลด์การกำหนดราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="70f4b-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="70f4b-119">คุณสามารถตั้งค่าราคาขายมาตรฐานสำหรับรายการบันทึกชั่วโมงหรือสำหรับประเภทโครงการ </span><span class="sxs-lookup"><span data-stu-id="70f4b-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="70f4b-120">นอกจากนี้คุณยังสามารถตั้งค่าราคาขายตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ธุรกรรม หรือข้อมูลใดๆ ดังกล่าวรวมกัน</span><span class="sxs-lookup"><span data-stu-id="70f4b-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="70f4b-121">ราคาขายจริงซึ่งจะใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันชั่วโมง คือราคาขายที่มีระดับรายละเอียดสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70f4b-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="70f4b-122">ตัวอย่างเช่น ถ้ามีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะผู้ปฏิบัติงาน ระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="70f4b-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="70f4b-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="70f4b-123">Click Save.</span></span>
13. <span data-ttu-id="70f4b-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70f4b-124">Close the page.</span></span>
14. <span data-ttu-id="70f4b-125">ไปที่ การจัดการและการบัญชีโครงการ > การตั้งค่า > ราคา > ราคาต้นทุน (ค่าใช้จ่าย)</span><span class="sxs-lookup"><span data-stu-id="70f4b-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="70f4b-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="70f4b-126">Click New.</span></span>
16. <span data-ttu-id="70f4b-127">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="70f4b-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="70f4b-128">ในฟิลด์ราคาต้นทุน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="70f4b-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="70f4b-129">สามารถกรอกข้อมูลได้หลายฟิลด์ แต่นี่คือจำนวนขั้นต่ำที่จำเป็นสำหรับการบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="70f4b-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="70f4b-130">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="70f4b-130">Click Save.</span></span>
19. <span data-ttu-id="70f4b-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="70f4b-131">Close the page.</span></span>
20. <span data-ttu-id="70f4b-132">ไปที่ การจัดการและการบัญชีโครงการ > การตั้งค่า > ราคา > ราคาขาย (ค่าใช้จ่าย)</span><span class="sxs-lookup"><span data-stu-id="70f4b-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="70f4b-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="70f4b-133">Click New.</span></span>
22. <span data-ttu-id="70f4b-134">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="70f4b-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="70f4b-135">ในฟิลด์ มีผลบังคับใช้สำหรับ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="70f4b-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="70f4b-136">ในฟิลด์การกำหนดราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="70f4b-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="70f4b-137">ราคาขายจริงซึ่งจะใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันค่าใช้จ่าย คือราคาขายที่มีระดับรายละเอียดสูงสุด</span><span class="sxs-lookup"><span data-stu-id="70f4b-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="70f4b-138">ตัวอย่างเช่น ถ้ามีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะผู้ปฏิบัติงาน ระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="70f4b-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="70f4b-139">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="70f4b-139">Click Save.</span></span>

