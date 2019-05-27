---
title: ตั้งค่าดัชนีเชื้อเพลิงของผู้ขนส่ง
description: 'คำแนะนำนี้แสดงวิธีการสร้างดัชนีเชื้อเพลิงในภูมิภาค, ดัชนีเชื้อเพลิงและดัชนีเชื้อเพลิงของผู้ขนส่ง '
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552103"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="02b1d-103">ตั้งค่าดัชนีเชื้อเพลิงของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="02b1d-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02b1d-104">คำแนะนำนี้แสดงวิธีการสร้างดัชนีเชื้อเพลิงในภูมิภาค, ดัชนีเชื้อเพลิงและดัชนีเชื้อเพลิงของผู้ขนส่ง </span><span class="sxs-lookup"><span data-stu-id="02b1d-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="02b1d-105">ดัชนีเชื้อเพลิงในภูมิภาคระบุว่าภูมิภาคใดควรใช้ดัชนีเชื้อเพลิงแบบใด และดัชนีเชื้อเพลิงระบุราคาในรอบระยะเวลานั้นๆ</span><span class="sxs-lookup"><span data-stu-id="02b1d-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="02b1d-106">เพื่อสะท้อนการเปลี่ยนแปลงในราคาของเชื้อเพลิงตลอดช่วงเวลา คุณสามารถเชื่อมโยงหลายๆดัชนีเชื้อเพลิงกับผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="02b1d-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="02b1d-107">งานเหล่านี้โดยทั่วไปถูกทำโดยผู้ประสานงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="02b1d-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="02b1d-108">คุณสามารถใช้ขั้นตอนนี้ในข้อมูลสาธิตของบริษัทUSMF หรือโดยใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="02b1d-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="02b1d-109">สร้างดัชนีเชื้อเพลิงของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="02b1d-109">Create a fuel index region</span></span>
1. <span data-ttu-id="02b1d-110">ไปที่จัดการการขนส่ง > การตั้งค่า > ดัชนีเชื้อเพลิง > ดัชนีเชื้อเพลิงของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="02b1d-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="02b1d-111">ก่อนอื่น คุณต้องสร้างภูมิภาคที่แตกต่างกัน สถานที่ที่ดำเนินธุรกิจ และคำนวณค่าเชื้อเพลิงเพิ่มเติมต่างๆ</span><span class="sxs-lookup"><span data-stu-id="02b1d-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="02b1d-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="02b1d-112">Click New.</span></span>
3. <span data-ttu-id="02b1d-113">ในฟิลด์ภูมิภาค ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="02b1d-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="02b1d-114">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="02b1d-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="02b1d-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="02b1d-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="02b1d-116">สร้างดัชนีเชื้อเพลิง</span><span class="sxs-lookup"><span data-stu-id="02b1d-116">Create a fuel index</span></span>
1. <span data-ttu-id="02b1d-117">ไปที่จัดการการขนส่ง > การตั้งค่า > ดัชนีเชื้อเพลิง > ดัชนีเชื้อเพลิง</span><span class="sxs-lookup"><span data-stu-id="02b1d-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="02b1d-118">สำหรับภูมิภาคที่คุณได้ตั้งค่า คุณต้องป้อนราคาเชื้อเพลิงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="02b1d-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="02b1d-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="02b1d-119">Click New.</span></span>
3. <span data-ttu-id="02b1d-120">ในฟิลด์ภูมิภาค ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="02b1d-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="02b1d-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02b1d-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="02b1d-122">ในฟิลด์ราคาต่อแกลลอน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="02b1d-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="02b1d-123">ในฟิลด์วันและเวลาเริ่มต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="02b1d-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="02b1d-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="02b1d-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="02b1d-125">สร้างดัชนีเชื้อเพลิงของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="02b1d-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="02b1d-126">ไปที่จัดการการขนส่ง > การตั้งค่า > ดัชนีเชื้อเพลิง > ดัชนีเชื้อเพลิงของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="02b1d-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="02b1d-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="02b1d-127">Click New.</span></span>
3. <span data-ttu-id="02b1d-128">ในฟิลด์ดัชนีเชื้อเพลิงของผู้ขนส่ง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="02b1d-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="02b1d-129">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="02b1d-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="02b1d-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="02b1d-130">Click New.</span></span>
6. <span data-ttu-id="02b1d-131">ในฟิลด์วันและเวลาเริ่มต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="02b1d-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="02b1d-132">ในฟิลด์PPGต้นทาง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="02b1d-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="02b1d-133">ในตัวอย่างนี้ คุณสามารถตั้งค่า ppg ในฟิลด์เป็น 1.95</span><span class="sxs-lookup"><span data-stu-id="02b1d-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="02b1d-134">ในฟิลด์PPGปลายทาง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="02b1d-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="02b1d-135">ในตัวอย่างนี้ คุณสามารถตั้งค่า ppg ในฟิลด์เป็น 2</span><span class="sxs-lookup"><span data-stu-id="02b1d-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="02b1d-136">ในฟิลด์เปอร์เซ็นทร์ ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="02b1d-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="02b1d-137">ในตัวอย่างนี้ คุณสามารถตั้งค่า ppg ในฟิลด์เป็น 3%</span><span class="sxs-lookup"><span data-stu-id="02b1d-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="02b1d-138">ในฟิลด์สกุลเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="02b1d-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="02b1d-139">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="02b1d-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="02b1d-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02b1d-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="02b1d-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="02b1d-141">Click Save.</span></span>

