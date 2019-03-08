---
title: การตั้งค่าผู้ขนส่ง
description: 'กระบวนการนี้แสดงวิธีการตั้งค่าการขนส่ง และกำหนดรายละเอียด เช่น การบริการ,โหมดการจัดส่ง,ค่าขนส่ง,วิธีการชำระเงิน,ข้อจำกัดขนส่ง, และอัตราการจัดส่ง '
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
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "314497"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="fac68-103">การตั้งค่าผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="fac68-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fac68-104">กระบวนการนี้แสดงวิธีการตั้งค่าการขนส่ง และกำหนดรายละเอียด เช่น การบริการ,โหมดการจัดส่ง,ค่าขนส่ง,วิธีการชำระเงิน,ข้อจำกัดขนส่ง, และอัตราการจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="fac68-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="fac68-105">ผู้ประสานงานขนส่งสามารถกำหนดผู้ขนส่งสินค้าทั้งโหลดขาเข้าหรือขาออก</span><span class="sxs-lookup"><span data-stu-id="fac68-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="fac68-106">สร้างผู้ขนส่งสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="fac68-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="fac68-107">ไปที่การจัดการการขนส่ง > การตั้งค่า > ผู้ขนส่ง > ผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="fac68-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="fac68-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fac68-108">Click New.</span></span>
3. <span data-ttu-id="fac68-109">ในฟิลด์ผู้ขนส่งสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fac68-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="fac68-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="fac68-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fac68-111">ในฟิลด์โหมด ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fac68-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fac68-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="fac68-114">กรอกข้อมูลทั่วไปสำหรับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="fac68-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="fac68-115">สลับการขยายส่วนภาพรวม</span><span class="sxs-lookup"><span data-stu-id="fac68-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="fac68-116">เลือกหรือไม่เลือกกล่องกาเครื่องหมายของผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="fac68-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="fac68-117">ในฟิลด์ผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="fac68-118">เลือกบัญชีผู้จัดจำหน่ายเพื่อมอบหมายให้กับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="fac68-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="fac68-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fac68-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="fac68-121">ในฟิลด์ชนิดการชำระเงินการขนส่ง ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="fac68-122">เลือกชนิดการชำระเงินขนส่งด้วยตัวเอง หรือเลือก EDI เพื่ออัพเดตการชำระเงิน โดยใช้การแลกเปลี่ยนข้อมูลทางอิเล็กทรอนิกส์ (EDI)</span><span class="sxs-lookup"><span data-stu-id="fac68-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="fac68-123">เลือกหรือไม่เลือกกล่องกาเครื่องหมายการจัดอันดับของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="fac68-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="fac68-124">สร้างบริการที่จำเป็นสำหรับการขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="fac68-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="fac68-125">สลับการขยายส่วนการบริการ</span><span class="sxs-lookup"><span data-stu-id="fac68-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="fac68-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fac68-126">Click New.</span></span>
3. <span data-ttu-id="fac68-127">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fac68-128">ในฟิลด์ผู้บริการขนส่ง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fac68-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="fac68-129">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fac68-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="fac68-130">ในฟิลด์วิธีการขนส่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fac68-131">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="fac68-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="fac68-133">ตั้งค่าอยู่สำหรับผู้ขนส่ง (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="fac68-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="fac68-134">สลับการขยายส่วนที่อยู่</span><span class="sxs-lookup"><span data-stu-id="fac68-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="fac68-135">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fac68-135">Click New.</span></span>
3. <span data-ttu-id="fac68-136">ในฟิลด์ชื่อหรือคำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fac68-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="fac68-137">ในฟิลด์ประเทศ/ภูมิภาค ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fac68-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="fac68-139">ในฟิลด์รหัสไปรษณีย์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fac68-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="fac68-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="fac68-142">ในฟิลด์ถนน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fac68-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="fac68-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fac68-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="fac68-144">ตั้งค่าโพรไฟล์การจัดอันดับสำหรับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="fac68-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="fac68-145">สลับการขยายส่วนของการจัดอันดับโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="fac68-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="fac68-146">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fac68-146">Click New.</span></span>
3. <span data-ttu-id="fac68-147">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fac68-148">ในฟิลด์การจัดอันดับโพรไฟล์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fac68-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="fac68-149">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fac68-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="fac68-150">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fac68-151">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="fac68-152">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="fac68-153">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fac68-154">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="fac68-155">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="fac68-156">ในฟิลด์กลไกจัดการอัตรา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="fac68-157">เลือกกลไกจัดการอัตราที่สอดคล้องกับสัญญากับผู้ขนส่งที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="fac68-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="fac68-158">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="fac68-159">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="fac68-160">ในฟิลด์ต้นแบบอัตรา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="fac68-161">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fac68-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="fac68-162">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="fac68-163">ในฟิลด์กลไกจัดการเวลาในการส่งต่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fac68-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="fac68-164">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fac68-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="fac68-165">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fac68-165">Click Save.</span></span>

