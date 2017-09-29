--- 
title: "ตั้งค่าดัชนีเชื้อเพลิงของผู้ขนส่ง"
description: "คำแนะนำนี้แสดงวิธีการสร้างดัชนีเชื้อเพลิงในภูมิภาค, ดัชนีเชื้อเพลิงและดัชนีเชื้อเพลิงของผู้ขนส่ง "
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 81f3244ff42cf13cd93ac10656c47f8a9204ef99
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="36feb-103">ตั้งค่าดัชนีเชื้อเพลิงของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="36feb-103">Set up a carrier fuel index</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36feb-104">คำแนะนำนี้แสดงวิธีการสร้างดัชนีเชื้อเพลิงในภูมิภาค, ดัชนีเชื้อเพลิงและดัชนีเชื้อเพลิงของผู้ขนส่ง </span><span class="sxs-lookup"><span data-stu-id="36feb-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="36feb-105">ดัชนีเชื้อเพลิงในภูมิภาคระบุว่าภูมิภาคใดควรใช้ดัชนีเชื้อเพลิงแบบใด และดัชนีเชื้อเพลิงระบุราคาในรอบระยะเวลานั้นๆ</span><span class="sxs-lookup"><span data-stu-id="36feb-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="36feb-106">เพื่อสะท้อนการเปลี่ยนแปลงในราคาของเชื้อเพลิงตลอดช่วงเวลา คุณสามารถเชื่อมโยงหลายๆดัชนีเชื้อเพลิงกับผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="36feb-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="36feb-107">งานเหล่านี้โดยทั่วไปถูกทำโดยผู้ประสานงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="36feb-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="36feb-108">คุณสามารถใช้ขั้นตอนนี้ในข้อมูลสาธิตของบริษัทUSMF หรือโดยใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="36feb-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="36feb-109">สร้างดัชนีเชื้อเพลิงของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="36feb-109">Create a fuel index region</span></span>
1. <span data-ttu-id="36feb-110">ไปที่จัดการการขนส่ง > การตั้งค่า > ดัชนีเชื้อเพลิง > ดัชนีเชื้อเพลิงของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="36feb-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="36feb-111">ก่อนอื่น คุณต้องสร้างภูมิภาคที่แตกต่างกัน สถานที่ที่ดำเนินธุรกิจ และคำนวณค่าเชื้อเพลิงเพิ่มเติมต่างๆ</span><span class="sxs-lookup"><span data-stu-id="36feb-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="36feb-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="36feb-112">Click New.</span></span>
3. <span data-ttu-id="36feb-113">ในฟิลด์ภูมิภาค ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="36feb-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="36feb-114">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="36feb-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="36feb-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="36feb-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="36feb-116">สร้างดัชนีเชื้อเพลิง</span><span class="sxs-lookup"><span data-stu-id="36feb-116">Create a fuel index</span></span>
1. <span data-ttu-id="36feb-117">ไปที่จัดการการขนส่ง > การตั้งค่า > ดัชนีเชื้อเพลิง > ดัชนีเชื้อเพลิง</span><span class="sxs-lookup"><span data-stu-id="36feb-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="36feb-118">สำหรับภูมิภาคที่คุณได้ตั้งค่า คุณต้องป้อนราคาเชื้อเพลิงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="36feb-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="36feb-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="36feb-119">Click New.</span></span>
3. <span data-ttu-id="36feb-120">ในฟิลด์ภูมิภาค ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="36feb-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="36feb-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="36feb-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="36feb-122">ในฟิลด์ราคาต่อแกลลอน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="36feb-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="36feb-123">ในฟิลด์วันและเวลาเริ่มต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="36feb-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="36feb-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="36feb-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="36feb-125">สร้างดัชนีเชื้อเพลิงของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="36feb-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="36feb-126">ไปที่จัดการการขนส่ง > การตั้งค่า > ดัชนีเชื้อเพลิง > ดัชนีเชื้อเพลิงของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="36feb-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="36feb-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="36feb-127">Click New.</span></span>
3. <span data-ttu-id="36feb-128">ในฟิลด์ดัชนีเชื้อเพลิงของผู้ขนส่ง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="36feb-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="36feb-129">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="36feb-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="36feb-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="36feb-130">Click New.</span></span>
6. <span data-ttu-id="36feb-131">ในฟิลด์วันและเวลาเริ่มต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="36feb-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="36feb-132">ในฟิลด์PPGต้นทาง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="36feb-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="36feb-133">ในตัวอย่างนี้ คุณสามารถตั้งค่า ppg ในฟิลด์เป็น 1.95</span><span class="sxs-lookup"><span data-stu-id="36feb-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="36feb-134">ในฟิลด์PPGปลายทาง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="36feb-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="36feb-135">ในตัวอย่างนี้ คุณสามารถตั้งค่า ppg ในฟิลด์เป็น 2</span><span class="sxs-lookup"><span data-stu-id="36feb-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="36feb-136">ในฟิลด์เปอร์เซ็นทร์ ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="36feb-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="36feb-137">ในตัวอย่างนี้ คุณสามารถตั้งค่า ppg ในฟิลด์เป็น 3%</span><span class="sxs-lookup"><span data-stu-id="36feb-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="36feb-138">ในฟิลด์สกุลเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="36feb-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="36feb-139">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="36feb-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="36feb-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="36feb-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="36feb-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="36feb-141">Click Save.</span></span>


