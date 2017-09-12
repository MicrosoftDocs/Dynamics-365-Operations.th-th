---
title: "ตั้งค่าโพรไฟล์ภาพรวมของการมาถึงของสินค้า"
description: "งานนี้มุ่งเน้นการตั้งค่าโพรไฟล์ภาพรวมการมาถึง "
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 9d4377f4ebf777258de13a2d2cd0a3a095f98fdd
ms.contentlocale: th-th
ms.lasthandoff: 09/12/2017

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="fddb7-103">ตั้งค่าโพรไฟล์ภาพรวมของการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="fddb7-103">Set up an item arrival overview profile</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fddb7-104">งานนี้มุ่งเน้นการตั้งค่าโพรไฟล์ภาพรวมการมาถึง </span><span class="sxs-lookup"><span data-stu-id="fddb7-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="fddb7-105">โพรไฟล์ภาพรวมการมาถึงคือ ชุดของกฎที่จะใช้เมื่อผู้ใช้มีการเปิดหน้าภาพรวมของการมาถึง</span><span class="sxs-lookup"><span data-stu-id="fddb7-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="fddb7-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="fddb7-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="fddb7-107">โดยทั่วไปจะดำเนินการโดยเจ้าหน้าที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fddb7-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="fddb7-108">ไปยังการจัดการสินค้าคงคลัง > การตั้งค่า > การกระจาย > โพรไฟล์ภาพรวมการมาถึง</span><span class="sxs-lookup"><span data-stu-id="fddb7-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="fddb7-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fddb7-109">Click New.</span></span>
    * <span data-ttu-id="fddb7-110">เนื่องจากคุณจะทำงานในคลังสินค้าเดียวกันตลอดเวลาในการถ่ายสินค้าจากการขนส่งเต็มรถบรรทุก คุณควรสร้างโพรไฟล์ภาพรวมการมาถึงของสินค้าเพื่อให้กระบวนการในการลงทะเบียนสินค้าที่ได้รับนั้นง่ายมากยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="fddb7-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="fddb7-111">ในฟิลด์ชื่อโพรไฟล์ภาพรวมการมาถึง ให้พิมพ์ชื่อสำหรับโพรไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="fddb7-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="fddb7-112">ในฟิลด์แสดงรายการ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fddb7-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="fddb7-113">เลือกรายการที่จะแสดงสำหรับการรับสินค้า:   ทั้งหมด – แสดงรายการทั้งหมด โดยไม่คำนึงถึงสถานะ</span><span class="sxs-lookup"><span data-stu-id="fddb7-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="fddb7-114">อยู่ระหว่างการดำเนินการ – แสดงรายการสำหรับการรับสินค้าที่ดำเนินการเสร็จสมบูรณ์แล้ว หรือเสร็จสมบูรณ์เพียงบางส่วน</span><span class="sxs-lookup"><span data-stu-id="fddb7-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="fddb7-115">ซึ่งหมายความว่า สำหรับแต่ละรายการ ทั้งการรับสินค้าปริมาณเต็มจำนวนหรือการได้รับบางส่วน ก็ให้มีการลงทะเบียนในสมุดรายวันการมาถึง</span><span class="sxs-lookup"><span data-stu-id="fddb7-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="fddb7-116">ไม่เสร็จสมบูรณ์ – แสดงรายการสำหรับการรับสินค้าที่ยังไม่มาถึงเลย หรือได้รับเพียงบางส่วน</span><span class="sxs-lookup"><span data-stu-id="fddb7-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="fddb7-117">ยังไม่มีการลงทะเบียนปริมาณไว้หรือมีการลงทะเบียนแล้วบางส่วนในสมุดรายวันการมาถึง</span><span class="sxs-lookup"><span data-stu-id="fddb7-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="fddb7-118">ขยายหรือยุบส่วนตัวเลือกการมาถึง</span><span class="sxs-lookup"><span data-stu-id="fddb7-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="fddb7-119">ในฟิลด์จำนวนวันข้างหน้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fddb7-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="fddb7-120">ขั้นตอนนี้เป็นการตั้งค่าตัวกรองเพื่อแสดงรายการสินค้าที่คาดว่าจะได้รับภายในอีกสองสามวัน (ขึ้นอยู่กับตัวเลขที่คุณกำหนด)</span><span class="sxs-lookup"><span data-stu-id="fddb7-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="fddb7-121">ในฟิลด์จำนวนวันย้อนหลัง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fddb7-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="fddb7-122">ขั้นตอนนี้เป็นการกำหนดตัวกรองเพื่อแสดงรายการสินค้าที่คาดว่าจะได้รับวันก่อนหน้าวันนี้</span><span class="sxs-lookup"><span data-stu-id="fddb7-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="fddb7-123">ในฟิลด์คลังสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fddb7-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="fddb7-124">ใช้ตัวกรองคลังสินค้าหนึ่งหรือหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="fddb7-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="fddb7-125">ในฟิลด์วิธีการจัดส่ง ให้เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fddb7-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="fddb7-126">ขั้นตอนนี้เป็นการกำหนดตัวกรองเพื่อแสดงเฉพาะรายการสินค้าที่ได้รับ ด้วยวิธีการจัดส่งนี้</span><span class="sxs-lookup"><span data-stu-id="fddb7-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="fddb7-127">ในฟิลด์ชื่อ เลือก WHS</span><span class="sxs-lookup"><span data-stu-id="fddb7-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="fddb7-128">ในฟิลด์คลังสินค้า เลือกคลังสินค้า 24</span><span class="sxs-lookup"><span data-stu-id="fddb7-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="fddb7-129">นี่เป็นคลังสินค้าเริ่มต้นที่จะใช้สำหรับการรับรายการสินค้าที่ลงทะเบียนไว้ซึ่งใช้โพรไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="fddb7-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="fddb7-130">ในฟิลด์สถานที่ เลือก Baydoor</span><span class="sxs-lookup"><span data-stu-id="fddb7-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="fddb7-131">นี่เป็นสถานที่เริ่มต้นที่จะใช้สำหรับการรับรายการสินค้าที่ลงทะเบียนไว้ซึ่งใช้โพรไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="fddb7-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="fddb7-132">ขยายหรือยุบส่วนรายละเอียดการสอบถามการมาถึง</span><span class="sxs-lookup"><span data-stu-id="fddb7-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="fddb7-133">ในฟิลด์ข้อจำกัดเกี่ยวกับไซต์ เลือกไซต์ 2</span><span class="sxs-lookup"><span data-stu-id="fddb7-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="fddb7-134">ขั้นตอนนี้เป็นการตั้งค่าตัวกรองเพื่อแสดงเฉพาะรายการสินค้าที่ได้รับ ของไซต์งานนี้</span><span class="sxs-lookup"><span data-stu-id="fddb7-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="fddb7-135">ตั้งค่าตัวเลือกใบสั่งซื้อเป็นใช่</span><span class="sxs-lookup"><span data-stu-id="fddb7-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="fddb7-136">เลือกรายการสินค้าจากใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fddb7-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="fddb7-137">ตั้งค่าตัวเลือกใบสั่งโอนเป็นใช่</span><span class="sxs-lookup"><span data-stu-id="fddb7-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="fddb7-138">เลือกรายการสินค้าจากใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="fddb7-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="fddb7-139">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fddb7-139">Click Save.</span></span>
18. <span data-ttu-id="fddb7-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fddb7-140">Close the page.</span></span>

