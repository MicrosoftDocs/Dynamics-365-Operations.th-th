---
title: ตั้งค่าการบรรจุด้วยตนเอง (กุมภาพันธ์ 2016 และ พฤษภาคม 2016)
description: 'กระบวนการบรรจุสินค้าอนุญาตให้คุณตรวจสอบความถูกต้องและบรรจุผลิตภัณฑ์ลงในตู้บรรจุสินค้า '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e1e99b479752a027c60a878c57bd35d4219981
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438867"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="35907-103">ตั้งค่าการบรรจุด้วยตนเอง (กุมภาพันธ์ 2016 และ พฤษภาคม 2016)</span><span class="sxs-lookup"><span data-stu-id="35907-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35907-104">กระบวนการบรรจุสินค้าอนุญาตให้คุณตรวจสอบความถูกต้องและบรรจุผลิตภัณฑ์ลงในตู้บรรจุสินค้า </span><span class="sxs-lookup"><span data-stu-id="35907-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="35907-105">ในกระบวนการนี้ ผู้ปฏิบัติงานสำหรับคลังสินค้าบรรจุผลิตภัณฑ์จากสถานที่จัดเก็บ และย้ายไปยังสถานีบรรจุที่พวกเขาตรวจสอบปริมาณและชนิดของสินค้า และมอบหมายให้กับตู้บรรจุสินค้าที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="35907-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="35907-106">เมื่อตู้บรรจุสินค้าถูกบรรจุจนเต็ม พวกเขาสามารถปิดและย้ายไปยังท่าสินค้าขาออกได้ และผลิตภัณฑ์พร้อมในการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="35907-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="35907-107">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="35907-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="35907-108">กระบวนงานนี้ใช้สำหรับรุ่นกุมภาพันธ์ 2016 และพฤษภาคม 2016 ของ Dynamics 365 for Operations เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="35907-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="35907-109">ตั้งค่าโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="35907-109">Set up location profiles</span></span>
1. <span data-ttu-id="35907-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > คลังสินค้า > โพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="35907-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="35907-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="35907-111">Click New.</span></span>
    * <span data-ttu-id="35907-112">โฟรไฟล์สถานที่ถูกใช้สำหรับสถานีการบรรจุ และประกอบด้วยข้อมูลและกฎสำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="35907-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="35907-113">ในฟิลด์รหัสโพรไฟล์สถานที่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="35907-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="35907-114">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="35907-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="35907-115">ในฟิลด์รูปแบบสถานที่ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35907-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="35907-116">ในฟิลด์ชนิดของสถานที่ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="35907-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="35907-117">เลือก ใช่ ในฟิลด์อนุญาตสินค้าผสม</span><span class="sxs-lookup"><span data-stu-id="35907-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="35907-118">เลือก ใช่ ในฟิลด์อนุญาตสถานะสินค้าคงคลังแบบผสม</span><span class="sxs-lookup"><span data-stu-id="35907-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="35907-119">เลือก ใช่ ในฟิลด์การแทนที่กฎสำหรับจำนวนวันของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="35907-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="35907-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="35907-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="35907-121">ตั้งค่าพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="35907-122">ไปที่การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="35907-123">คลิกแท็บการบรรจุ</span><span class="sxs-lookup"><span data-stu-id="35907-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="35907-124">ในฟิลด์รหัสโพรไฟล์สำหรับสถานที่เบิกสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35907-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="35907-125">เลือกโฟรไฟล์สถานที่ที่คุณต้องการใช้สำหรับการบรรจุ</span><span class="sxs-lookup"><span data-stu-id="35907-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="35907-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="35907-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="35907-127">ตั้งค่าชนิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-127">Set up container types</span></span>
1. <span data-ttu-id="35907-128">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > ชนิดของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="35907-129">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="35907-129">Click New.</span></span>
    * <span data-ttu-id="35907-130">คุณสามารถกำหนดชนิดของตู้บรรจุสินค้าที่จะใช้ คุณสามารถระบุมิติทางกายภาพของตู้บรรจุสินค้า </span><span class="sxs-lookup"><span data-stu-id="35907-130">You can define the types of containers to use.</span></span> <span data-ttu-id="35907-131">รวมถึงน้ำหนักหีบห่อ น้ำหนักสูงสุด ปริมาณสูงสุด ความยาว ความกว้าง และน้ำหนัก </span><span class="sxs-lookup"><span data-stu-id="35907-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="35907-132">แอททริบิวต์ถูกกำหนดค่าฟิลด์ที่อนุญาตให้คุณเพิ่มมิติเพิ่มเติมได้ในชนิดของตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="35907-133">ในฟิลด์รหัสชนิดของตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35907-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="35907-134">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="35907-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="35907-135">ในฟิลด์น้ำหนักหีบห่อ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="35907-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="35907-136">ในฟิลด์น้ำหนักสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="35907-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="35907-137">ในฟิลด์จำนวน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="35907-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="35907-138">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="35907-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="35907-139">ในฟิลด์ความกว้าง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="35907-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="35907-140">ในฟิลด์ความสูง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="35907-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="35907-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="35907-141">Click Save.</span></span>
12. <span data-ttu-id="35907-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="35907-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="35907-143">ตั้งค่าโพรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="35907-143">Set up packing profiles</span></span>
1. <span data-ttu-id="35907-144">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การบรรจุ > โพรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="35907-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="35907-145">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="35907-145">Click New.</span></span>
3. <span data-ttu-id="35907-146">ในฟิลด์รหัสโพรไฟล์การบรรจุ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="35907-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="35907-147">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="35907-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="35907-148">ในฟิลด์รหัสโพรไฟล์การปิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35907-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="35907-149">รหัสโพรไฟล์การปิดตู้บรรจุสินค้าไม่จำเป็นต้องระบุ และให้เป็นโพรไฟล์ตู้บรรจุสินค้าที่ปิดเริ่มต้นสำหรับโพรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="35907-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="35907-150">ในฟิลด์โหมดรหัสตู้บรรจุสินค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="35907-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="35907-151">ตัวเลือกนี้กำหนดว่ารหัสตู้บรรจุสินค้าจะถูกสร้างขึ้นโดยอัตโนมัติเมื่อมีการสร้างตู้บรรจุสินค้า หรือเมื่อรหัสตู้บรรจุสินค้าถูกสร้างขึ้นโดยตนเอง</span><span class="sxs-lookup"><span data-stu-id="35907-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="35907-152">ในฟิลด์ชนิดตู้บรรจุสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="35907-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="35907-153">ชนิดของตู้บรรจุสินค้าจะถูกใช้โดยค่าเริ่มต้น เมื่อตู้บรรจุสินค้าใหม่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="35907-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="35907-154">เลือกกล่องกาเครื่องหมายการสร้างตู้บรรจุสินค้าอัตโนมัติเมื่อปิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="35907-155">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="35907-155">Click Save.</span></span>
10. <span data-ttu-id="35907-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="35907-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="35907-157">ตั้งค่าโพรไฟล์การปิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="35907-158">ไปที่การจัดการคลังสินค้า > การตั้งค่า > ตู้บรรจุสินค้า > โพรไฟล์การปิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="35907-159">โพรไฟล์การปิดตู้บรรจุสินค้ากำหนดสิ่งที่จะเกิดขึ้น เมื่อตู้บรรจุสินค้าถูกปิด </span><span class="sxs-lookup"><span data-stu-id="35907-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="35907-160">คุณสามารถตั้งค่าโพรไฟล์ตู้บรรจุสินค้าที่ปิดหลายโพรไฟล์ได้</span><span class="sxs-lookup"><span data-stu-id="35907-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="35907-161">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="35907-161">Click New.</span></span>
3. <span data-ttu-id="35907-162">ในฟิลด์รหัสโพรไฟล์การปิดตู้บรรจุสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35907-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="35907-163">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="35907-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="35907-164">ในฟิลด์ รายการเมื่อ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="35907-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="35907-165">ระบุว่าการแสดงรายการจะเกิดขึ้นเมื่อมีการปิดตู้บรรจุสินค้า หรือเมื่อมีการยืนยันการจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="35907-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="35907-166">หมายเหตุว่าการแสดงรายการต้องการการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="35907-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="35907-167">การแสดงรายการต้องถูกนำมาใช้ในกลไกจัดการการขนส่งเพื่อให้ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="35907-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="35907-168">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35907-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="35907-169">ในฟิลด์สถานที่เริ่มต้นสำหรับการจัดส่งขั้นสุดท้าย ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35907-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="35907-170">นี่จะเป็นสถานที่ให้กับผลิตภัณฑ์ที่จะถูกย้ายหลังจากการปิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="35907-171">สถานที่นี้ต้องมีโพรไฟล์สถานที่ที่กำหนดในพารามิเตอร์คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="35907-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="35907-172">ในฟิลด์หน่วยน้ำหนัก ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="35907-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="35907-173">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="35907-173">Click Save.</span></span>

