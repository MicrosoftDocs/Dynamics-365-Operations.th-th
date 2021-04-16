---
title: ตั้งค่าต้นแบบอัตรา
description: 'ขั้นตอนนี้แสดงวิธีการตั้งค่าต้นแบบอัตรา '
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809001"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="c548e-103">ตั้งค่าต้นแบบอัตรา</span><span class="sxs-lookup"><span data-stu-id="c548e-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c548e-104">ขั้นตอนนี้แสดงวิธีการตั้งค่าต้นแบบอัตรา </span><span class="sxs-lookup"><span data-stu-id="c548e-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="c548e-105">ผู้จัดการลอจิสติคส์มักจะตั้งค่าต้นแบบอัตราโดยขึ้นอยู่กับสัญญาที่เซ็นกับผู้ขนส่ง </span><span class="sxs-lookup"><span data-stu-id="c548e-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="c548e-106">ในสถานการณ์นี้คุณจะตั้งค่าต้นแบบอัตราสำหรับผู้ขนส่งทางอากาศ</span><span class="sxs-lookup"><span data-stu-id="c548e-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="c548e-107">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c548e-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="c548e-108">ตั้งค่าต้นแบบการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="c548e-108">Set up break master</span></span>

1. <span data-ttu-id="c548e-109">ไปที่ **การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ต้นแบบการแบ่ง**</span><span class="sxs-lookup"><span data-stu-id="c548e-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="c548e-110">ตัวแบ่งหลักจะใช้เพื่อกำหนดโครงสร้างการกำหนดราคาและจุดสั่งหยุด</span><span class="sxs-lookup"><span data-stu-id="c548e-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="c548e-111">โครงสร้างราคาใช้ในการจัดระดับของการกำหนดราคาที่ยึดตามมิติทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="c548e-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="c548e-112">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c548e-112">Select **New**.</span></span>
1. <span data-ttu-id="c548e-113">ในฟิลด์ **ต้นแบบการแบ่ง** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="c548e-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="c548e-114">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c548e-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="c548e-115">ในฟิลด์ **ชนิดข้อมูล** เลือกชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c548e-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="c548e-116">ในฟิลด์ **เปรียบเทียบ** ให้ป้อนชนิดของการเปรียบเทียบที่ร้องขอ (โดยใช้ตัวดำเนินการ)</span><span class="sxs-lookup"><span data-stu-id="c548e-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="c548e-117">ในฟิลด์ **หน่วยการแบ่ง** ป้อนหน่วยการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="c548e-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="c548e-118">ในส่วน **รายละเอียด** ให้สร้างการแบ่งมากเท่าที่จำเป็นสำหรับโครงสร้างการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="c548e-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="c548e-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c548e-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="c548e-120">ตั้งค่าต้นแบบอัตรา</span><span class="sxs-lookup"><span data-stu-id="c548e-120">Set up rate master</span></span>

1. <span data-ttu-id="c548e-121">ไปที่ **การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ต้นแบบอัตรา**</span><span class="sxs-lookup"><span data-stu-id="c548e-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="c548e-122">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c548e-122">Select **New**.</span></span>
1. <span data-ttu-id="c548e-123">ในฟิลด์ **ต้นแบบอัตรา** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c548e-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="c548e-124">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c548e-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="c548e-125">ในฟิลด์ **รหัสข้อมูลเมต้าการจัดอันดับ** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c548e-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="c548e-126">การจัดอันดับของรหัสข้อมูลเมตาจะกำหนดข้อมูลที่จำเป็นสำหรับต้นแบบอัตรา เป็นซึ่งกำหนดข้อมูลเมตาที่คาดไว้โดยกลไกกลไกจัดการการจัดการขนส่งโดยใช้ต้นแบบอัตรานี้</span><span class="sxs-lookup"><span data-stu-id="c548e-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="c548e-127">สำหรับตัวอย่างนี้ ให้เลือกตัวเลือก P2P</span><span class="sxs-lookup"><span data-stu-id="c548e-127">For this example, select the P2P option.</span></span> <span data-ttu-id="c548e-128">ซึ่งมีการกำหนดไว้แล้วในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="c548e-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="c548e-129">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c548e-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="c548e-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c548e-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="c548e-131">ตั้งค่าฐานอัตรา</span><span class="sxs-lookup"><span data-stu-id="c548e-131">Set up rate base</span></span>

1. <span data-ttu-id="c548e-132">เลือก **ฐานอัตรา**</span><span class="sxs-lookup"><span data-stu-id="c548e-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="c548e-133">ฐานอัตรากำหนดอัตราของผู้ขนส่ง และสามารถใช้เพื่อตั้งค่าโครงสร้างภาษีนั้น โดยการร่างโครงสร้างอัตราจุดสั่งหยุดที่ถูกกำหนดไว้ในต้นแบบการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="c548e-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="c548e-134">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c548e-134">Select **New**.</span></span>
3. <span data-ttu-id="c548e-135">ในฟิลด์ **ฐานอัตรา** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c548e-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="c548e-136">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c548e-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c548e-137">ในฟิลด์ **ต้นแบบการแบ่ง** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c548e-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c548e-138">ตัวแบ่งหลักจะใช้เพื่อกำหนดโครงสร้างการกำหนดราคาและจุดสั่งหยุด</span><span class="sxs-lookup"><span data-stu-id="c548e-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="c548e-139">โครงสร้างราคาใช้ในการจัดระดับของการกำหนดราคาที่ยึดตามมิติทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="c548e-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="c548e-140">สำหรับตัวอย่างนี้ ให้ใช้น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="c548e-140">For this example, use weight.</span></span> <span data-ttu-id="c548e-141">ซึ่งมีการกำหนดไว้แล้วในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="c548e-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="c548e-142">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เน้น</span><span class="sxs-lookup"><span data-stu-id="c548e-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="c548e-143">ขยายส่วน **รายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="c548e-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="c548e-144">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c548e-144">Select **New**.</span></span>
10. <span data-ttu-id="c548e-145">ในฟิลด์ **จากรหัสไปรษณีย์ที่ส่ง** ให้พิมพ์ "30301"</span><span class="sxs-lookup"><span data-stu-id="c548e-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="c548e-146">ในฟิลด์ **รหัสไปรษณีย์ที่ส่งถึง** ให้พิมพ์ "30318"</span><span class="sxs-lookup"><span data-stu-id="c548e-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="c548e-147">ในฟิลด์ **ภูมิภาคของประเทศที่ส่ง** ให้พิมพ์ "USA"</span><span class="sxs-lookup"><span data-stu-id="c548e-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="c548e-148">ในฟิลด์ **<1.00 Lbs** ให้พิมพ์ "100"</span><span class="sxs-lookup"><span data-stu-id="c548e-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="c548e-149">แทรกอัตราต่อปอนด์ ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 1 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="c548e-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="c548e-150">ในฟิลด์ **<5.00 Lbs** ให้พิมพ์ "300"</span><span class="sxs-lookup"><span data-stu-id="c548e-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="c548e-151">แทรกอัตราต่อปอนด์ ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 5 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="c548e-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="c548e-152">ในฟิลด์ **<20.00 Lbs** ให้พิมพ์ "500"</span><span class="sxs-lookup"><span data-stu-id="c548e-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="c548e-153">แทรกอัตราต่อปอนด์ ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 20 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="c548e-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="c548e-154">ในฟิลด์ **<100.00 Lbs** ให้พิมพ์ "1000"</span><span class="sxs-lookup"><span data-stu-id="c548e-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="c548e-155">แทรกอัตราต่อปอนด์ ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 100 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="c548e-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="c548e-156">ในฟิลด์ **<1,000.00 Lbs** ให้พิมพ์ "3000"</span><span class="sxs-lookup"><span data-stu-id="c548e-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="c548e-157">แทรกอัตราต่อปอนด์ ถ้าน้ำหนักรวมของน้ำหนักบรรทุกน้อยกว่า 1000 ปอนด์</span><span class="sxs-lookup"><span data-stu-id="c548e-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="c548e-158">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c548e-158">Select **Save**.</span></span>
19. <span data-ttu-id="c548e-159">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c548e-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="c548e-160">กำหนดฐานอัตรา</span><span class="sxs-lookup"><span data-stu-id="c548e-160">Assign rate base</span></span>

1. <span data-ttu-id="c548e-161">ขยายส่วน **การกำหนดฐานอัตรา**</span><span class="sxs-lookup"><span data-stu-id="c548e-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="c548e-162">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c548e-162">Select **New**.</span></span>
    * <span data-ttu-id="c548e-163">คุณสามารถมีการกำหนดฐานอัตราต่างๆ สำหรับแต่ละต้นแบบอัตรา </span><span class="sxs-lookup"><span data-stu-id="c548e-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="c548e-164">ซึ่งทำให้คุณสามารถสร้างจุดราคาที่แตกต่างกันสำหรับแต่ละบริษัทขนส่งโดยขึ้นอยู่กับปลายทาง บริการหรือฐานอัตราที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c548e-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="c548e-165">ในขั้นตอนนี้คุณเพียงแค่สร้างการกำหนดฐานอัตราเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c548e-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="c548e-166">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c548e-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c548e-167">ในฟิลด์ **ฐานอัตรา** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c548e-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c548e-168">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เน้น</span><span class="sxs-lookup"><span data-stu-id="c548e-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="c548e-169">ในฟิลด์ **บริการ** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c548e-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c548e-170">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c548e-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c548e-171">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เน้น</span><span class="sxs-lookup"><span data-stu-id="c548e-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="c548e-172">ในฟิลด์ **รหัสไปรษณีย์ที่เบิกสินค้า** ให้พิมพ์ "98052"</span><span class="sxs-lookup"><span data-stu-id="c548e-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="c548e-173">ระบุว่าการกำหนดฐานอัตรานี้ควรมีผลบังคับใช้จากรหัสไปรษณีย์ใด</span><span class="sxs-lookup"><span data-stu-id="c548e-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="c548e-174">ในฟิลด์ **ภูมิภาคของประเทศที่เบิกสินค้า** ให้พิมพ์ "USA"</span><span class="sxs-lookup"><span data-stu-id="c548e-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="c548e-175">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c548e-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]