---
title: ตั้งค่าคอนฟิกต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่าย
description: หัวข้อนี้อธิบายวิธีการตั้งค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่ายสำหรับโครงการ
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867737"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="dac8f-103">ตั้งค่าคอนฟิกต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="dac8f-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dac8f-104">หัวข้อนี้อธิบายวิธีการตั้งค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="dac8f-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="dac8f-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="dac8f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="dac8f-106">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาต้นทุน (ชั่วโมง)**</span><span class="sxs-lookup"><span data-stu-id="dac8f-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="dac8f-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="dac8f-107">Select **New**.</span></span>
3. <span data-ttu-id="dac8f-108">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="dac8f-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="dac8f-109">ในฟิลด์ **ราคาต้นทุน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="dac8f-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="dac8f-110">คุณสามารถตั้งค่าราคาต้นทุนมาตรฐานสำหรับประเภทโครงการ หรือคุณสามารถตั้งค่าราคาต้นทุนตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ หรือข้อมูลใดๆ ดังกล่าวรวมกัน</span><span class="sxs-lookup"><span data-stu-id="dac8f-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="dac8f-111">ราคาต้นทุนที่จะนำไปใช้เป็นราคาต้นทุนที่มีรายละเอียดในระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="dac8f-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="dac8f-112">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac8f-112">Select **Save**.</span></span>
6. <span data-ttu-id="dac8f-113">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาขาย (ชั่วโมง)**</span><span class="sxs-lookup"><span data-stu-id="dac8f-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="dac8f-114">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="dac8f-114">Select **New**.</span></span>
8. <span data-ttu-id="dac8f-115">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="dac8f-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="dac8f-116">ในฟิลด์ **มีผลบังคับใช้สำหรับ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="dac8f-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="dac8f-117">ในฟิลด์ **การกำหนดราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="dac8f-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="dac8f-118">คุณสามารถตั้งค่าราคาขายมาตรฐานสำหรับรายการบันทึกชั่วโมงหรือสำหรับประเภทโครงการ </span><span class="sxs-lookup"><span data-stu-id="dac8f-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="dac8f-119">นอกจากนี้คุณยังสามารถตั้งค่าราคาขายตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ธุรกรรม หรือข้อมูลใดๆ ดังกล่าวรวมกัน</span><span class="sxs-lookup"><span data-stu-id="dac8f-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="dac8f-120">ราคาขายจริงซึ่งจะใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันชั่วโมง คือราคาขายที่มีระดับรายละเอียดสูงสุด</span><span class="sxs-lookup"><span data-stu-id="dac8f-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="dac8f-121">ตัวอย่างเช่น ถ้ามีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะผู้ปฏิบัติงาน ระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="dac8f-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="dac8f-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac8f-122">Select **Save**.</span></span>
12. <span data-ttu-id="dac8f-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dac8f-123">Close the page.</span></span>
13. <span data-ttu-id="dac8f-124">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาต้นทุน (ค่าใช้จ่าย)**</span><span class="sxs-lookup"><span data-stu-id="dac8f-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="dac8f-125">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="dac8f-125">Select **New**.</span></span>
15. <span data-ttu-id="dac8f-126">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="dac8f-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="dac8f-127">ในฟิลด์ **ราคาต้นทุน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="dac8f-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="dac8f-128">สามารถกรอกข้อมูลได้หลายฟิลด์ แต่นี่คือจำนวนขั้นต่ำที่จำเป็นสำหรับการบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="dac8f-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="dac8f-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac8f-129">Select **Save**.</span></span>
18. <span data-ttu-id="dac8f-130">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาขาย (ค่าใช้จ่าย)**</span><span class="sxs-lookup"><span data-stu-id="dac8f-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="dac8f-131">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="dac8f-131">Select **New**.</span></span>
20. <span data-ttu-id="dac8f-132">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="dac8f-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="dac8f-133">ในฟิลด์ **มีผลบังคับใช้สำหรับ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="dac8f-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="dac8f-134">ในฟิลด์ **การกำหนดราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="dac8f-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="dac8f-135">ราคาขายจริงซึ่งจะใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันค่าใช้จ่าย คือราคาขายที่มีระดับรายละเอียดสูงสุด</span><span class="sxs-lookup"><span data-stu-id="dac8f-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="dac8f-136">ตัวอย่างเช่น ถ้ามีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะผู้ปฏิบัติงาน ระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="dac8f-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="dac8f-137">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac8f-137">Select **Save**.</span></span>

