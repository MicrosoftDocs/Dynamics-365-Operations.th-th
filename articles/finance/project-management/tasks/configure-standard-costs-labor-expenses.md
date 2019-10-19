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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185416"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="3d02c-103">ตั้งค่าคอนฟิกต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3d02c-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d02c-104">หัวข้อนี้อธิบายวิธีการตั้งค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="3d02c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="3d02c-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="3d02c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="3d02c-106">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาต้นทุน (ชั่วโมง)**</span><span class="sxs-lookup"><span data-stu-id="3d02c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="3d02c-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3d02c-107">Select **New**.</span></span>
3. <span data-ttu-id="3d02c-108">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3d02c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="3d02c-109">ในฟิลด์ **ราคาต้นทุน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="3d02c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="3d02c-110">คุณสามารถตั้งค่าราคาต้นทุนมาตรฐานสำหรับประเภทโครงการ หรือคุณสามารถตั้งค่าราคาต้นทุนตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ หรือข้อมูลใดๆ ดังกล่าวรวมกัน</span><span class="sxs-lookup"><span data-stu-id="3d02c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="3d02c-111">ราคาต้นทุนที่จะนำไปใช้เป็นราคาต้นทุนที่มีรายละเอียดในระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="3d02c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="3d02c-112">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3d02c-112">Select **Save**.</span></span>
6. <span data-ttu-id="3d02c-113">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาขาย (ชั่วโมง)**</span><span class="sxs-lookup"><span data-stu-id="3d02c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="3d02c-114">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3d02c-114">Select **New**.</span></span>
8. <span data-ttu-id="3d02c-115">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3d02c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="3d02c-116">ในฟิลด์ **มีผลบังคับใช้สำหรับ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3d02c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="3d02c-117">ในฟิลด์ **การกำหนดราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3d02c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="3d02c-118">คุณสามารถตั้งค่าราคาขายมาตรฐานสำหรับรายการบันทึกชั่วโมงหรือสำหรับประเภทโครงการ </span><span class="sxs-lookup"><span data-stu-id="3d02c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="3d02c-119">นอกจากนี้คุณยังสามารถตั้งค่าราคาขายตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ธุรกรรม หรือข้อมูลใดๆ ดังกล่าวรวมกัน</span><span class="sxs-lookup"><span data-stu-id="3d02c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="3d02c-120">ราคาขายจริงซึ่งจะใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันชั่วโมง คือราคาขายที่มีระดับรายละเอียดสูงสุด</span><span class="sxs-lookup"><span data-stu-id="3d02c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="3d02c-121">ตัวอย่างเช่น ถ้ามีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะผู้ปฏิบัติงาน ระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3d02c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="3d02c-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3d02c-122">Select **Save**.</span></span>
12. <span data-ttu-id="3d02c-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3d02c-123">Close the page.</span></span>
13. <span data-ttu-id="3d02c-124">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาต้นทุน (ค่าใช้จ่าย)**</span><span class="sxs-lookup"><span data-stu-id="3d02c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="3d02c-125">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3d02c-125">Select **New**.</span></span>
15. <span data-ttu-id="3d02c-126">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3d02c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="3d02c-127">ในฟิลด์ **ราคาต้นทุน** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="3d02c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="3d02c-128">สามารถกรอกข้อมูลได้หลายฟิลด์ แต่นี่คือจำนวนขั้นต่ำที่จำเป็นสำหรับการบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="3d02c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="3d02c-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3d02c-129">Select **Save**.</span></span>
18. <span data-ttu-id="3d02c-130">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาขาย (ค่าใช้จ่าย)**</span><span class="sxs-lookup"><span data-stu-id="3d02c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="3d02c-131">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3d02c-131">Select **New**.</span></span>
20. <span data-ttu-id="3d02c-132">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3d02c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="3d02c-133">ในฟิลด์ **มีผลบังคับใช้สำหรับ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3d02c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="3d02c-134">ในฟิลด์ **การกำหนดราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3d02c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="3d02c-135">ราคาขายจริงซึ่งจะใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันค่าใช้จ่าย คือราคาขายที่มีระดับรายละเอียดสูงสุด</span><span class="sxs-lookup"><span data-stu-id="3d02c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="3d02c-136">ตัวอย่างเช่น ถ้ามีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะผู้ปฏิบัติงาน ระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3d02c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="3d02c-137">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3d02c-137">Select **Save**.</span></span>

