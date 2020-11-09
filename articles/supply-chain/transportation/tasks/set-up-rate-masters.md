---
title: ตั้งค่าต้นแบบอัตรา
description: 'ขั้นตอนนี้แสดงวิธีการตั้งค่าต้นแบบอัตรา '
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRouteWorkbench, TMSRateMaster, TMSRateBaseType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72d71aa15f8cec532980f412ff1cb48e142c4cb1
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016481"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="820f4-103">ตั้งค่าต้นแบบอัตรา</span><span class="sxs-lookup"><span data-stu-id="820f4-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="820f4-104">ขั้นตอนนี้แสดงวิธีการตั้งค่าต้นแบบอัตรา </span><span class="sxs-lookup"><span data-stu-id="820f4-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="820f4-105">ผู้จัดการลอจิสติคส์มักจะตั้งค่าต้นแบบอัตราโดยขึ้นอยู่กับสัญญาที่เซ็นกับผู้ขนส่ง </span><span class="sxs-lookup"><span data-stu-id="820f4-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="820f4-106">ในสถานการณ์นี้คุณจะตั้งค่าต้นแบบอัตราสำหรับผู้ขนส่งทางอากาศ</span><span class="sxs-lookup"><span data-stu-id="820f4-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="820f4-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="820f4-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="820f4-108">ตั้งค่าต้นแบบอัตรา</span><span class="sxs-lookup"><span data-stu-id="820f4-108">Set up rate master</span></span>
1. <span data-ttu-id="820f4-109">ไปที่จัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ต้นแบบอัตรา</span><span class="sxs-lookup"><span data-stu-id="820f4-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="820f4-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="820f4-110">Click New.</span></span>
3. <span data-ttu-id="820f4-111">ในฟิลด์ต้นแบบอัตรา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="820f4-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="820f4-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="820f4-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="820f4-113">ในฟิลด์ ID ข้อมูลเมต้าการจัดอันดับ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="820f4-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="820f4-114">การจัดอันดับของรหัสข้อมูลเมตาจะกำหนดข้อมูลที่จำเป็นสำหรับต้นแบบอัตรา เป็นซึ่งกำหนดข้อมูลเมตาที่คาดไว้โดยกลไก TMS โดยใช้ต้นแบบอัตรานี้</span><span class="sxs-lookup"><span data-stu-id="820f4-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="820f4-115">สำหรับตัวอย่างนี้ ให้เลือกตัวเลือก P2P</span><span class="sxs-lookup"><span data-stu-id="820f4-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="820f4-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="820f4-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="820f4-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="820f4-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="820f4-118">ตั้งค่าฐานอัตรา</span><span class="sxs-lookup"><span data-stu-id="820f4-118">Set up rate base</span></span>
1. <span data-ttu-id="820f4-119">คลิกฐานอัตรา</span><span class="sxs-lookup"><span data-stu-id="820f4-119">Click Rate base.</span></span>
    * <span data-ttu-id="820f4-120">ฐานอัตรากำหนดอัตราของผู้ขนส่ง และสามารถใช้เพื่อตั้งค่าโครงสร้างภาษีนั้น โดยการร่างโครงสร้างอัตราจุดสั่งหยุดที่ถูกกำหนดไว้ในต้นแบบการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="820f4-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="820f4-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="820f4-121">Click New.</span></span>
3. <span data-ttu-id="820f4-122">ในฟิลด์ฐานอัตรา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="820f4-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="820f4-123">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="820f4-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="820f4-124">ในฟิลด์ต้นแบบการแบ่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="820f4-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="820f4-125">ตัวแบ่งหลักจะใช้เพื่อกำหนดโครงสร้างการกำหนดราคาและจุดสั่งหยุด</span><span class="sxs-lookup"><span data-stu-id="820f4-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="820f4-126">โครงสร้างราคาใช้ในการจัดระดับของการกำหนดราคาที่ยึดตามมิติทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="820f4-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="820f4-127">สำหรับตัวอย่างนี้ ให้ใช้น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="820f4-127">For this example, use weight</span></span>
7. <span data-ttu-id="820f4-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="820f4-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="820f4-129">สลับการขยายส่วนของรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="820f4-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="820f4-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="820f4-130">Click New.</span></span>
10. <span data-ttu-id="820f4-131">ในฟิลด์จากรหัสไปรษณีย์ที่ส่ง ให้พิมพ์ '30301'</span><span class="sxs-lookup"><span data-stu-id="820f4-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="820f4-132">ในฟิลด์รหัสไปรษณีย์ที่ส่งถึง ให้พิมพ์ '30318'</span><span class="sxs-lookup"><span data-stu-id="820f4-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="820f4-133">ในฟิลด์ภูมิภาคของประเทศที่ส่ง ให้พิมพ์ 'USA'</span><span class="sxs-lookup"><span data-stu-id="820f4-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="820f4-134">ในฟิลด์ <1.00 Lbs ให้พิมพ์ '100'</span><span class="sxs-lookup"><span data-stu-id="820f4-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="820f4-135">ระบุอัตราต่อปอนด์ หากน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 1 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="820f4-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="820f4-136">ในฟิลด์ <5.00 Lbs ให้พิมพ์ '300'</span><span class="sxs-lookup"><span data-stu-id="820f4-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="820f4-137">แทรกอัตราต่อ lbs ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 5 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="820f4-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="820f4-138">ในฟิลด์ <20.00 Lbs ให้พิมพ์ '500'</span><span class="sxs-lookup"><span data-stu-id="820f4-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="820f4-139">แทรกอัตราต่อ lbs ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 20 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="820f4-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="820f4-140">ในฟิลด์ <100.00 Lbs ให้พิมพ์ '1000'</span><span class="sxs-lookup"><span data-stu-id="820f4-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="820f4-141">แทรกอัตราต่อlbsถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 100 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="820f4-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="820f4-142">ในฟิลด์ <1,000.00 Lbs ให้พิมพ์ '3000'</span><span class="sxs-lookup"><span data-stu-id="820f4-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="820f4-143">แทรกอัตราต่อ lbs ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 1000 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="820f4-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="820f4-144">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="820f4-144">Click Save.</span></span>
19. <span data-ttu-id="820f4-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="820f4-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="820f4-146">กำหนดฐานอัตรา</span><span class="sxs-lookup"><span data-stu-id="820f4-146">Assign rate base</span></span>
1. <span data-ttu-id="820f4-147">สลับการขยายส่วนของภาคการกำหนดฐานอัตรา </span><span class="sxs-lookup"><span data-stu-id="820f4-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="820f4-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="820f4-148">Click New.</span></span>
    * <span data-ttu-id="820f4-149">คุณสามารถมีการกำหนดฐานอัตราต่างๆ สำหรับแต่ละต้นแบบอัตรา </span><span class="sxs-lookup"><span data-stu-id="820f4-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="820f4-150">ซึ่งทำให้คุณสามารถสร้างจุดราคาที่แตกต่างกันสำหรับแต่ละบริษัทขนส่งโดยขึ้นอยู่กับปลายทาง บริการหรือฐานอัตราที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="820f4-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="820f4-151">ในขั้นตอนนี้คุณเพียงแค่สร้างการกำหนดฐานอัตราเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="820f4-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="820f4-152">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="820f4-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="820f4-153">ในฟิลด์ฐานอัตรา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="820f4-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="820f4-154">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="820f4-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="820f4-155">ในฟิลด์การบริการ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="820f4-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="820f4-156">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="820f4-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="820f4-157">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="820f4-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="820f4-158">ในฟิลด์รหัสไปรษณีย์ที่เบิกสินค้า ให้พิมพ์ '98052'</span><span class="sxs-lookup"><span data-stu-id="820f4-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="820f4-159">ระบุว่าการกำหนดฐานอัตรานี้ควรมีผลบังคับใช้จากรหัสไปรษณีย์ใด</span><span class="sxs-lookup"><span data-stu-id="820f4-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="820f4-160">ในฟิลด์ภูมิภาคของประเทศที่เบิกสินค้า ให้พิมพ์ 'USA'</span><span class="sxs-lookup"><span data-stu-id="820f4-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="820f4-161">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="820f4-161">Click Save.</span></span>

