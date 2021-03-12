---
title: ย้ายไปที่ผนัง - ย้ายไปยังร้านค้า
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับฟังก์ชันย้ายไปที่ผนัง - ย้ายไปยังร้านค้า ฟังก์ชันนี้ช่วยให้คุณสามารถจัดการกับสถานการณ์ที่คุณต้องรวมผลิตภัณฑ์กับพื้นที่การแบ่งระยะการจัดเตรียม โดยยึดตามเงื่อนไขที่ตั้งค่าคอนฟิกได้ ซึ่งจะช่วยลดเวลาในการเบิกสินค้า เนื่องจากจะอนุญาตการเบิกสินค้าไปยังป้ายทะเบียนเป้าหมายเดียว และสามารถใช้ตำแหน่งการสำรองได้มากกว่าการเบิกสินค้าคลัสเตอร์
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3f2ae63758fcb6247c5e56433645d9252576c755
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996286"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="7f83e-105">ย้ายไปที่ผนัง - ย้ายไปยังร้านค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f83e-106">ฟังก์ชัน *ย้ายไปที่ผนัง - ย้ายไปยังร้านค้า* ช่วยให้คุณสามารถจัดการกับสถานการณ์ที่คุณต้องรวมผลิตภัณฑ์กับพื้นที่การแบ่งระยะการจัดเตรียม โดยยึดตามเงื่อนไขที่ตั้งค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="7f83e-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="7f83e-107">เนื่องจากฟังก์ชันนี้อนุญาตให้มีการเบิกสินค้าไปยังป้ายทะเบียนเป้าหมายเดียวและสามารถใช้ตำแหน่งการสำรองได้มากกว่าการเบิกสินค้าคลัสเตอร์ บริษัทที่จัดส่งสินค้าไปยังร้านค้าหรือจัดการสินค้าขนาดเล็ก จะได้รับประโยชน์จากเวลาการเบิกสินค้าที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="7f83e-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="7f83e-108">ลำดับงานสำหรับฟังก์ชันนี้บังคับให้ผลิตภัณฑ์ที่มีการเบิกสินค้าไปยังสถานที่การเรียงลำดับสำหรับการกระจายออกเป็นคอนเทนเนอร์ชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="7f83e-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="7f83e-109">โดยทั่วไป สถานที่การเรียงลำดับแต่ละแห่งประกอบด้วยตำแหน่งการเรียงลำดับหลายตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="7f83e-110">ตำแหน่งการเรียงลำดับแต่ละตำแหน่งจะถูกมอบหมายตามเงื่อนไขที่กำหนดโดยกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7f83e-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="7f83e-111">เงื่อนไขโดยทั่วไปคือปลายทาง การจัดส่ง หรือการโหลดขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="7f83e-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="7f83e-112">หลังจากที่ผลิตภัณฑ์มาถึงแล้ว จะมีการกระจายสินค้าไปยังตำแหน่งการเรียงลำดับแต่ละตำแหน่ง โดยยึดตามปริมาณที่สัมพันธ์กับใบสั่ง ปลายทาง การจัดส่ง หรือการโหลด</span><span class="sxs-lookup"><span data-stu-id="7f83e-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="7f83e-113">เมื่อคอนเทนเนอร์เต็มหรือสมบูรณ์ จะมีการย้ายไปยังสถานที่การแบ่งระยะหรือสถานที่จัดส่งสำหรับการจัดการเพิ่มเติม ทั้งนี้ขึ้นอยู่กับกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7f83e-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="7f83e-114">นอกจากนี้ ฟังก์ชันของคลังสินค้านี้ยังมีการอ้างอิงถึงโดยชื่ออื่นๆ เช่น การวางตามไฟ และการงัด</span><span class="sxs-lookup"><span data-stu-id="7f83e-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="7f83e-115">เปิดคุณลักษณะการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="7f83e-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="7f83e-116">ก่อนที่คุณจะสามารถใช้ฟังก์ชัน *ย้ายไปที่ผนัง - ย้ายไปยังร้านค้า* คุณลักษณะ *การเรียงลำดับขาออก* ต้องถูกเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f83e-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="7f83e-117">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="7f83e-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7f83e-118">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7f83e-119">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="7f83e-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7f83e-120">**ชื่อคุณลักษณะ:** *การเรียงลำดับขาออก*</span><span class="sxs-lookup"><span data-stu-id="7f83e-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="7f83e-121">คุณลักษณะ *การเรียงลำดับขาออก* ต้องถูกใช้ร่วมกับ คุณลักษณะ *รหัสขั้นตอนของเวฟทั่วทั้งองค์กร* ถ้ามีการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="7f83e-122">นอกจากนี้ คุณยังต้องเปิดใช้งานคุณลักษณะนี้ ถ้าคุณจะใช้รหัสที่กำหนดไว้ล่วงหน้าซึ่งตั้งค่าไว้ในรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="7f83e-123">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะนี้ในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="7f83e-124">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="7f83e-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7f83e-125">**ชื่อคุณลักษณะ:** *รหัสขั้นตอนของเวฟทั่วทั้งองค์กร*</span><span class="sxs-lookup"><span data-stu-id="7f83e-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="7f83e-126">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="7f83e-126">Setup</span></span>

<span data-ttu-id="7f83e-127">สำหรับการสาธิตนี้ จะมีการใช้ข้อมูล Contoso มาตรฐานและคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="7f83e-128">นอกจากนี้ ยังมีการใช้ส่วนเพิ่มเติมบางอย่างที่บันทึกไว้ในภายหลังด้วย</span><span class="sxs-lookup"><span data-stu-id="7f83e-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="7f83e-129">ชนิดของสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="7f83e-129">Location type</span></span>

1. <span data-ttu-id="7f83e-130">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> ชนิดสถานที่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="7f83e-131">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างชนิดสถานที่สำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="7f83e-132">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-132">Set the following values:</span></span>

    - <span data-ttu-id="7f83e-133">**ชนิดสถานที่:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="7f83e-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="7f83e-134">**คำอธิบาย:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="7f83e-135">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="7f83e-136">พารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="7f83e-137">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="7f83e-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="7f83e-138">บนแท็บ **ทั่วไป** บน FastTab **ชนิดสถานที่** ในฟิลด์ **ชนิดสถานที่การเรียงลำดับ** ป้อน *SORT*</span><span class="sxs-lookup"><span data-stu-id="7f83e-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="7f83e-139">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="7f83e-140">โพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="7f83e-140">Location profile</span></span>

1. <span data-ttu-id="7f83e-141">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="7f83e-142">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างโพรไฟล์สถานที่สำหรับสถานที่การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="7f83e-143">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="7f83e-144">**รหัสโพรไฟล์สถานที่:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-145">**ชื่อ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="7f83e-146">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7f83e-147">**รูปแบบสถานที่:** *PACK*</span><span class="sxs-lookup"><span data-stu-id="7f83e-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="7f83e-148">**ชนิดสถานที่:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="7f83e-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="7f83e-149">**ใช้การติดตามป้ายทะเบียน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="7f83e-150">**อนุญาตสินค้าแบบผสม:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="7f83e-151">**อนุญาตสถานะสินค้าคงคลังแบบผสม:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="7f83e-152">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="7f83e-153">ตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-153">Locations</span></span>

1. <span data-ttu-id="7f83e-154">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> สถานที่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="7f83e-155">ยกเลิกการเลือกกล่องกาเครื่องหมาย **สร้างตัวเลขการตรวจสอบสำหรับสถานที่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="7f83e-156">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="7f83e-157">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="7f83e-158">**สถานที่:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-159">**รหัสโพรไฟล์สถานที่:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="7f83e-160">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="7f83e-161">โพรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="7f83e-161">Packing profiles</span></span>

1. <span data-ttu-id="7f83e-162">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> โพรไฟล์การบรรจุ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="7f83e-163">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="7f83e-164">**รหัสโพรไฟล์การบรรจุ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-165">**คำอธิบาย:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-166">**นโยบายการบรรจุคอนเทนเนอร์:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="7f83e-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="7f83e-167">**โหมดรหัสคอนเทนเนอร์:** *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="7f83e-168">**ชนิดคอนเทนเนอร์** *แท่นวางสินค้า 48X48*</span><span class="sxs-lookup"><span data-stu-id="7f83e-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="7f83e-169">**สร้างคอนเทนเนอร์ที่การปิดคอนเทนเนอร์โดยอัตโนมัติ:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="7f83e-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="7f83e-170">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="7f83e-171">รหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-171">Wave step codes</span></span>

<span data-ttu-id="7f83e-172">ถ้าคุณเปิดใช้งานคุณลักษณะ *รหัสขั้นตอนของแบบเวฟทั่วทั้งองค์กร* ให้ตั้งค่ารหัสต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="7f83e-173">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> รหัสขั้นตอนของเวฟ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="7f83e-174">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="7f83e-175">**รหัสขั้นตอนของเวฟ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-176">**คำอธิบายขั้นตอนของเวฟ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-177">**ชนิดของขั้นตอนเวฟ:** *เท็มเพลตการเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="7f83e-178">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="7f83e-179">เท็มเพลตการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="7f83e-179">Outbound sorting template</span></span>

<span data-ttu-id="7f83e-180">เท็มเพลตการเรียงลำดับจะควบคุมว่ามีการสร้างตำแหน่งการเรียงลำดับหรือไม่ จะใช้เกณฑ์ใด และแอททริบิวต์อื่นๆ ของกระบวนการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="7f83e-181">ไปยัง **การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> เท็มเพลตการเรียงลำดับขาออก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="7f83e-182">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างเท็มเพลตการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="7f83e-183">ในส่วนหัวของเท็มเพลตใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="7f83e-184">**รหัสเท็มเพลตการเรียงลำดับขาออก:** *การเรียงลำดับเวฟ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="7f83e-185">**คำอธิบาย:** *การเรียงลำดับเวฟ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="7f83e-186">**ชนิดของเท็มเพลตเวฟ:** *ตามความต้องการของเวฟ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="7f83e-187">ฟิลด์นี้จะกำหนดกระบวนการที่จะใช้เท็มเพลตการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="7f83e-188">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-188">The following values are available:</span></span>

        - <span data-ttu-id="7f83e-189">**ความต้องการของเวฟ** – มีการใช้เท็มเพลตการเรียงลำดับสำหรับกระบวนการ *ย้ายไปยังผนัง*</span><span class="sxs-lookup"><span data-stu-id="7f83e-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="7f83e-190">ชนิดของเท็มเพลตนี้ใช้เพื่อข้ามสถานีบรรจุและประมวลผลสินค้าคงคลังออกจากเวฟโดยตรง</span><span class="sxs-lookup"><span data-stu-id="7f83e-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="7f83e-191">คุณสามารถใช้ชนิดนี้ได้เฉพาะเมื่อวิธีการประมวลผลเวฟ **การเรียงลำดับ** ถูกรวมอยู่ในเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="7f83e-192">**คอนเทนเนอร์** – มีการใช้เท็มเพลตการเรียงลำดับสำหรับกระบวนการ *การสร้างแท่นวางสินค้าหลังจากการบรรจุ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="7f83e-193">ชนิดเท็มเพลตนี้ถูกใช้ในการประมวลผลคอนเทนเนอร์ที่ถูกปิดที่สถานีบรรจุสินค้า และต้องถูกเรียงลำดับไปยังแท่นวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="7f83e-194">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="7f83e-195">**สถานที่:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="7f83e-196">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7f83e-197">**การยืนยันการเรียงลำดับ:** *การสแกนตำแหน่ง*</span><span class="sxs-lookup"><span data-stu-id="7f83e-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="7f83e-198">ฟิลด์นี้จะกำหนดการตรวจสอบความถูกต้องที่จำเป็นในระหว่างการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="7f83e-199">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-199">The following values are available:</span></span>

        - <span data-ttu-id="7f83e-200">None</span><span class="sxs-lookup"><span data-stu-id="7f83e-200">None</span></span>
        - <span data-ttu-id="7f83e-201">การสแกนป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="7f83e-201">License plate scan</span></span>
        - <span data-ttu-id="7f83e-202">การสแกนตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-202">Position scan</span></span>

    - <span data-ttu-id="7f83e-203">**สร้างงานในการปิดตำแหน่ง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="7f83e-204">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* เมื่อปิดตำแหน่ง จะมีการสร้างงานเพื่อย้ายสินค้าคงคลังไปยังสถานที่จัดส่งขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="7f83e-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="7f83e-205">ถ้ามีการตั้งค่าเป็น *ไม่* จะมีการเบิกสินค้าคงคลังไปยังใบสั่งนี้โดยทันที เมื่อมีการปิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="7f83e-206">**การกำหนดตำแหน่ง:** *ด้วยตนเอง*</span><span class="sxs-lookup"><span data-stu-id="7f83e-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="7f83e-207">ฟิลด์นี้จะกำหนดชนิดของการกำหนดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="7f83e-208">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-208">The following values are available:</span></span>

        - <span data-ttu-id="7f83e-209">**ด้วยตนเอง** – ผู้ใช้จะต้องระบุตำแหน่งที่ควรเรียงลำดับสินค้าคงคลังให้เสมอ</span><span class="sxs-lookup"><span data-stu-id="7f83e-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="7f83e-210">**อัตโนมัติ** – ระบบจะแนะนำสินค้าคงคลังไปยังตำแหน่งโดยอัตโนมัติ เมื่อใดก็ตามที่สามารถทำได้ โดยยึดตามการแบ่งเท็มเพลตการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="7f83e-211">**กำหนดเกณฑ์ตำแหน่งการเรียงลำดับ:** *ใช้ตำแหน่งที่ว่างเปล่าเท่านั้น*</span><span class="sxs-lookup"><span data-stu-id="7f83e-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="7f83e-212">ฟิลด์นี้ควบคุมว่าสินค้าคงคลังที่มีอยู่แล้วในตำแหน่งการเรียงลำดับจะถูกพิจารณาหรือไม่ เมื่อมีการกำหนดตำแหน่งสำหรับความต้องการ</span><span class="sxs-lookup"><span data-stu-id="7f83e-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="7f83e-213">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-213">The following values are available:</span></span>

        - <span data-ttu-id="7f83e-214">**ใช้ตำแหน่งที่ว่างเปล่าเท่านั้น** – ตำแหน่งที่มีสินค้าคงคลังที่เชื่อมโยงกับสินค้าคงคลังอยู่แล้วเท่านั้นที่จะถูกพิจารณา</span><span class="sxs-lookup"><span data-stu-id="7f83e-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="7f83e-215">**สมมติว่าตำแหน่งว่างเปล่า** – สินค้าคงคลังที่มีอยู่แล้วในตำแหน่งจะถูกละเว้นในระหว่างการกำหนด</span><span class="sxs-lookup"><span data-stu-id="7f83e-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="7f83e-216">ตำแหน่งที่พร้อมใช้งานทั้งหมดจะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="7f83e-216">All available positions will be used.</span></span>

    - <span data-ttu-id="7f83e-217">**รหัสขั้นตอนของเวฟ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="7f83e-218">ถ้ามีการเปิดใช้งานคุณลักษณะของ *รหัสขั้นตอนของเวฟทั่วทั้งองค์กร* ต้องมีการตั้งค่ารหัสขั้นตอนของเวฟ *การเรียงลำดับ* ในรหัสขั้นตอนของเวฟด้วย</span><span class="sxs-lookup"><span data-stu-id="7f83e-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="7f83e-219">**ปิดตำแหน่งการเรียงลำดับโดยอัตโนมัติ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="7f83e-220">ถ้าตัวเลือกนี้ถูกตั้งค่าเป็น *ใช่* ตำแหน่งการเรียงลำดับจะถูกปิดโดยอัตโนมัติ เมื่องานทั้งหมดที่มาที่ตำแหน่งเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="7f83e-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="7f83e-221">**จำนวนของตำแหน่งการเรียงลำดับ:** *3*</span><span class="sxs-lookup"><span data-stu-id="7f83e-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="7f83e-222">ฟิลด์นี้จะกำหนดจำนวนสูงสุดของตำแหน่งการเรียงลำดับที่ระบบจะสร้าง</span><span class="sxs-lookup"><span data-stu-id="7f83e-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="7f83e-223">**คำนำหน้าตำแหน่งการเรียงลำดับ:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="7f83e-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="7f83e-224">ฟิลด์นี้จะกำหนดคำนำหน้าที่ระบบกำหนด ก่อนหมายเลขตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="7f83e-225">**บรรจุตำแหน่งการเรียงลำดับโดยอัตโนมัติ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="7f83e-226">ถ้าตัวเลือกนี้ถูกตั้งค่าเป็น *ใช่* สินค้าคงคลังในตำแหน่งการเรียงลำดับจะถูกบรรจุลงในคอนเทนเนอร์ เมื่อตำแหน่งถูกปิด</span><span class="sxs-lookup"><span data-stu-id="7f83e-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="7f83e-227">**รหัสโพรไฟล์การบรรจุ:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="7f83e-228">ฟิลด์นี้กำหนดโพรไฟล์การบรรจุที่จะใช้ เมื่อตำแหน่งการเรียงลำดับถูกบรรจุลงในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="7f83e-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="7f83e-229">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการสอบถาม** เพื่อระบุเกณฑ์ที่จะใช้สำหรับเท็มเพลตการเรียงลำดับนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="7f83e-230">ในกล่องโต้ตอบการสอบถาม บนแท็บ **การเรียงลำดับ** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัด แล้วจากนั้น ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="7f83e-231">**ตาราง:** *รายละเอียดการบรรทุก*</span><span class="sxs-lookup"><span data-stu-id="7f83e-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="7f83e-232">**ตารางที่ได้รับ:** *รายละเอียดการบรรทุก*</span><span class="sxs-lookup"><span data-stu-id="7f83e-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="7f83e-233">**ฟิลด์:** *รหัสการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="7f83e-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="7f83e-234">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="7f83e-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="7f83e-235">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-235">Select **OK**.</span></span>
1. <span data-ttu-id="7f83e-236">คุณอาจได้รับข้อความแสดงข้อความต่อไปนี้: "การจัดกลุ่มจะถูกรีเซ็ต ดำเนินการต่อหรือไม่"</span><span class="sxs-lookup"><span data-stu-id="7f83e-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="7f83e-237">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-237">Select **Yes**.</span></span>

    <span data-ttu-id="7f83e-238">ปุ่ม **การแบ่งเท็มเพลตการเรียงลำดับขาออก** ในบานหน้าต่างการดำเนินการ จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="7f83e-239">ในบานหน้าต่างการดำเนินการ ให้เลือก **การแบ่งเท็มเพลตการเรียงลำดับขาออก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="7f83e-240">เลือกกล่องกาเครื่องหมาย **จัดกลุ่มตามฟิลด์** เพื่อจัดกลุ่มตามรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="7f83e-241">การตั้งค่านี้จะสร้างตำแหน่งการเรียงลำดับหนึ่งตำแหน่งต่อการจัดส่งที่เป็นคอนเทนเนอร์ในเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="7f83e-242">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="7f83e-243">วิธีการกระบวนการเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-243">Wave process methods</span></span>

1. <span data-ttu-id="7f83e-244">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="7f83e-245">บนบานหน้าต่างการดำเนินการ เลือก **สร้างวิธีการใหม่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="7f83e-246">วิธีการ **การเรียงลำดับ** จะถูกเพิ่มเข้าในรายการของวิธีการที่พร้อมใช้งาน และมีการเลือกชนิดเท็มเพลตเวฟ *การจัดส่ง* สำหรับรายการนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="7f83e-247">เท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-247">Wave templates</span></span>

<span data-ttu-id="7f83e-248">แก้ไขเท็มเพลตเวฟที่ใช้สำหรับการเรียงลำดับความต้องการของเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="7f83e-249">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="7f83e-250">ในฟิลด์ **ชนิดเท็มเพลตเวฟ** เลือก *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="7f83e-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="7f83e-251">เลือกเท็มเพลต **62 ค่าเริ่มต้นของการจัดส่ง** ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="7f83e-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="7f83e-252">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="7f83e-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="7f83e-253">บน FastTab **ทั่วไป** ให้ทำการเปลี่ยนแปลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="7f83e-254">ตั้งค่าตัวเลือก **ประมวลผลเวฟเมื่อนำออกใช้ไปยังคลังสินค้า** เป็น *ไม่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="7f83e-255">ตั้งค่าตัวเลือก **กำหนดให้เปิดเวฟ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="7f83e-256">บน FastTab **วิธีการ** ให้ตั้งค่าวิธีการ **การเรียงลำดับ**:</span><span class="sxs-lookup"><span data-stu-id="7f83e-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="7f83e-257">ในกริด **วิธีการที่เหลือ** ให้เลือก **การเรียงลำดับ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="7f83e-258">เลือกปุ่มลูกศรขวาเพื่อย้าย **การเรียงลำดับ** ไปยังกริด **วิธีการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="7f83e-259">ในกริด **วิธีการที่เลือก** ให้เลือก **การเรียงลำดับ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="7f83e-260">ตั้งค่าฟิลด์ **รหัสขั้นตอนของเวฟ** เป็น *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="7f83e-261">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="7f83e-262">รายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="7f83e-262">Mobile device menu items</span></span>

1. <span data-ttu-id="7f83e-263">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="7f83e-264">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7f83e-265">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="7f83e-266">**ชื่อรายการเมนู:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-267">**ชื่อเรื่อง:** *เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="7f83e-268">**โหมด:** *ทางอ้อม*</span><span class="sxs-lookup"><span data-stu-id="7f83e-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="7f83e-269">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="7f83e-270">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7f83e-271">**รหัสกิจกรรม:** *การเรียงลำดับขาออก*</span><span class="sxs-lookup"><span data-stu-id="7f83e-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="7f83e-272">**ใช้คู่มือกระบวนการ:** *ใช่* (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="7f83e-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="7f83e-273">**รหัสเท็มเพลตการเรียงลำดับขาออก:** *การเรียงลำดับเวฟ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="7f83e-274">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="7f83e-275">เมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="7f83e-275">Mobile device menu</span></span>

1. <span data-ttu-id="7f83e-276">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="7f83e-277">ในรายการของเมนู ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="7f83e-278">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="7f83e-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="7f83e-279">ในกริด **เมนูและรายการเมนูที่พร้อมใช้งาน** ให้ค้นหาและเลือกรายการเมนู **เรียงลำดับ** ที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="7f83e-280">เลือกปุ่มลูกศรขวาเพื่อย้าย **เรียงลำดับ** ไปยังกริด **โครงสร้างเมนู**</span><span class="sxs-lookup"><span data-stu-id="7f83e-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="7f83e-281">ด้วยวิธีนี้ คุณจะเพิ่มรายการเมนูไปยังเมนู **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="7f83e-282">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="7f83e-283">คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="7f83e-283">Location directives</span></span>

<span data-ttu-id="7f83e-284">คุณต้องสร้างคำสั่งสถานที่เพื่อแนะนำงานที่สร้างขึ้นหลังจากที่การเรียงลำดับเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="7f83e-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="7f83e-285">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="7f83e-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="7f83e-286">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="7f83e-287">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7f83e-288">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="7f83e-289">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="7f83e-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="7f83e-290">**ชื่อ:** *ย้ายไปยัง Baydoor*</span><span class="sxs-lookup"><span data-stu-id="7f83e-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="7f83e-291">บน FastTab **คำสั่งสถานที่** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7f83e-292">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="7f83e-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="7f83e-293">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="7f83e-293">**Site:** *6*</span></span>
    - <span data-ttu-id="7f83e-294">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="7f83e-295">**รหัสคำสั่ง:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="7f83e-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="7f83e-296">**SKU หลายรายการ:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="7f83e-297">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="7f83e-298">บน FastTab **รายการ** ให้เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="7f83e-299">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7f83e-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="7f83e-300">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="7f83e-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="7f83e-301">**ปริมาณเริ่มต้น:** *0*</span><span class="sxs-lookup"><span data-stu-id="7f83e-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="7f83e-302">**ปริมาณสิ้นสุด:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="7f83e-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="7f83e-303">เลือก **บันทึก** เพื่อให้แท็บด่วน **การดำเนินคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="7f83e-304">บน FastTab **การดำเนินการคำสั่งสถานที่** ให้เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="7f83e-305">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7f83e-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="7f83e-306">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="7f83e-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="7f83e-307">**ชื่อ:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="7f83e-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="7f83e-308">เลือก **บันทึก** เพื่อทำให้ปุ่ม **แก้ไขการสอบถาม** บน FastTab **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="7f83e-309">บน FastTab **การดำเนินการของคำสั่งสถานที่** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="7f83e-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="7f83e-310">ในกล่องโต้ตอบการสอบถาม บนแท็บ **ช่วง** ให้ค้นหาแถวที่มีการตั้งค่า **ฟิลด์** เป็น *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="7f83e-311">ตั้งค่าฟิลด์ **เงื่อนไข** สำหรับแถวนี้เป็น *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="7f83e-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="7f83e-312">เลือก **ตกลง** เพื่อยืนยันการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="7f83e-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="7f83e-313">คลาสงาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-313">Work classes</span></span>

1. <span data-ttu-id="7f83e-314">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="7f83e-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="7f83e-315">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7f83e-316">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="7f83e-317">**รหัสคลาสงาน:** *การเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="7f83e-318">**คำอธิบาย:** *การเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="7f83e-319">**ชนิดของใบสั่งงาน:** *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="7f83e-320">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="7f83e-321">เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-321">Work templates</span></span>

1. <span data-ttu-id="7f83e-322">ไปที่ **การจัดการคลังสินค้า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="7f83e-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="7f83e-323">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="7f83e-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="7f83e-324">ในกริด ให้เลือกเท็มเพลตงาน **62 เบิกสินค้าไปบรรจุ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="7f83e-325">ในบานหน้าต่างการดำเนินการ ให้เลือก **ตัวแบ่งส่วนหัวของงาน**</span><span class="sxs-lookup"><span data-stu-id="7f83e-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="7f83e-326">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="7f83e-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="7f83e-327">บนบรรทัดที่มีการตั้งค่าฟิลด์ **ชื่อฟิลด์** เป็น *รหัสการจัดส่ง* ยกเลิกการเลือกกล่องกาเครื่องหมาย **จัดกลุ่มตามฟิลด์นี้**</span><span class="sxs-lookup"><span data-stu-id="7f83e-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="7f83e-328">เลือก **บันทึก** แล้วจากนั้น ปิดกล่องโต้ตอบ **ตัวแบ่งส่วนหัวของงาน**</span><span class="sxs-lookup"><span data-stu-id="7f83e-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="7f83e-329">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *การเบิกสินค้าคงคลังที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="7f83e-330">เลือก **สร้าง** เพื่อสร้างเท็มเพลตของงาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="7f83e-331">ในส่วน **ภาพรวม** ให้ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="7f83e-332">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7f83e-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="7f83e-333">**เท็มเพลตงาน:** *การเบิกสินค้าที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="7f83e-334">**คำอธิบายเท็มเพลตงาน:** *การเบิกสินค้าที่เรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="7f83e-335">เลือก **บันทึก** เพื่อทำให้ส่วน **รายละเอียดเท็มเพลตงาน** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="7f83e-336">ในส่วน **รายละเอียดเท็มเพลตงาน** คุณจะสร้างสองบรรทัด</span><span class="sxs-lookup"><span data-stu-id="7f83e-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="7f83e-337">เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้สำหรับบรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="7f83e-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="7f83e-338">**ชนิดงาน:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="7f83e-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="7f83e-339">**ข้อบังคับ:** เลือก (= *ใช่*)</span><span class="sxs-lookup"><span data-stu-id="7f83e-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="7f83e-340">**รหัสคลาสงาน:** *การเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="7f83e-341">เลือก **สร้าง** อีกครั้ง แล้วจากนั้น ตั้งค่าค่าต่อไปนี้สำหรับบรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="7f83e-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="7f83e-342">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="7f83e-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="7f83e-343">**ข้อบังคับ:** เลือก (= *ใช่*)</span><span class="sxs-lookup"><span data-stu-id="7f83e-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="7f83e-344">**รหัสคลาสงาน:** *การเรียงลำดับ*</span><span class="sxs-lookup"><span data-stu-id="7f83e-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="7f83e-345">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="7f83e-346">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="7f83e-346">Example scenario</span></span>

<span data-ttu-id="7f83e-347">สถานการณ์จำลองนี้จำลองสถานการณ์ที่ซึ่งคลังสินค้าจัดเก็บสินค้าขนาดเล็กในสถานที่และต้องบรรจุไว้ในกล่องก่อนที่จะจัดส่ง และที่ซึ่งฟังก์ชันของสถานีบรรจุไม่ค่อยเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7f83e-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="7f83e-348">ผู้ปฏิบัติงานเบิกสินค้าตามใบสั่งสำหรับลูกค้าหลายรายและที่อยู่ที่แตกต่างกันในเวลาเดียวกันเพื่อเพิ่มความเร็วในการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="7f83e-349">หลังจากเสร็จสิ้นการเบิกสินค้าแล้ว ผู้ปฏิบัติงานจะมาถึงสถานที่การเรียงลำดับซึ่งสินค้าที่เบิกสินค้าสามารถถูกเรียงลำดับไปยังกล่องที่ถูกต้อง โดยยึดตามเงื่อนไขที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7f83e-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="7f83e-350">ในตัวอย่างนี้ รหัสการจัดส่งจะถูกใช้เพื่อกำหนดกล่องที่ถูกต้อง เนื่องจากการจัดส่งแต่ละครั้งมีที่อยู่ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7f83e-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="7f83e-351">หลังจากที่มีการบรรจุสินค้าทั้งหมดจากโหลดและเรียงลำดับตามการจัดส่ง กล่องจะถูกย้ายไปยังพื้นที่การแบ่งระยะและถูกโหลดไปยังรถบรรทุกในที่สุด</span><span class="sxs-lookup"><span data-stu-id="7f83e-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="7f83e-352">ก่อนที่คุณจะเริ่มต้นสถานการณ์จำลอง โปรดตรวจสอบให้แน่ใจว่ามีการตั้งค่าฟังก์ชันของคลังสินค้ามาตรฐานทั้งหมดสำหรับคลังสินค้าของคุณอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7f83e-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="7f83e-353">คลังสินค้า Contoso มาตรฐาน *62* ถูกใช้สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="7f83e-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="7f83e-354">ไม่มีการเปลี่ยนแปลงการตั้งค่าคอนฟิกมาตรฐาน นอกจากจะมีการอธิบายไว้ในการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="7f83e-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="7f83e-355">สร้างความต้องการ</span><span class="sxs-lookup"><span data-stu-id="7f83e-355">Create demand</span></span>

<span data-ttu-id="7f83e-356">ก่อนที่จะสามารถแสดงฟังก์ชันได้ คุณต้องสร้างความต้องการบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="7f83e-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="7f83e-357">สำหรับสถานการณ์นี้ คุณจะสร้างใบสั่งขายสามใบสำหรับลูกค้าที่แตกต่างกันสามราย เพื่อจำลองที่อยู่การจัดส่งที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7f83e-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="7f83e-358">ด้วยวิธีนี้ คุณจะสามารถสร้างการจัดส่งที่แยกต่างหากสามรายการได้</span><span class="sxs-lookup"><span data-stu-id="7f83e-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="7f83e-359">ก่อนที่คุณจะสร้างใบสั่งขายและการจัดส่ง ต้องตรวจสอบให้แน่ใจว่าสถานที่เบิกสินค้ามีสินค้าคงคลังที่เพียงพอสำหรับสินค้าทั้งหมดในใบสั่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7f83e-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="7f83e-360">รีวิวการตั้งค่าคำสั่งสถานที่เพื่อยืนยันสถานที่เบิกสินค้าที่จะใช้สำหรับการเบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7f83e-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="7f83e-361">ถ้าคุณต้องปรับปรุงสินค้าคงคลัง คุณสามารถสร้างการเคลื่อนไหวด้วยตนเอง ใช้การเติมสินค้า หรือใช้โฟลว์อื่นใดๆ</span><span class="sxs-lookup"><span data-stu-id="7f83e-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="7f83e-362">จากนั้น จองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7f83e-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="7f83e-363">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7f83e-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7f83e-364">เลือก **สร้าง** เพื่อสร้างใบสั่งขายสำหรับใบสั่งที่ 1</span><span class="sxs-lookup"><span data-stu-id="7f83e-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="7f83e-365">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7f83e-366">**ลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7f83e-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="7f83e-367">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="7f83e-368">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-368">Select **OK**.</span></span>
1. <span data-ttu-id="7f83e-369">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="7f83e-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="7f83e-370">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-370">Set the following values:</span></span>

    - <span data-ttu-id="7f83e-371">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="7f83e-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="7f83e-372">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="7f83e-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="7f83e-373">เลือก **สร้างรายการ** เพื่อเพิ่มรายการที่สอง และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="7f83e-374">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="7f83e-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="7f83e-375">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="7f83e-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="7f83e-376">ทำซ้ำขั้นตอนต่อไปนี้สำหรับแต่ละรายการขายในใบสั่งเพื่อจองสินค้าคงคลัง:</span><span class="sxs-lookup"><span data-stu-id="7f83e-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="7f83e-377">บน FastTab **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="7f83e-378">บนหน้า **การจอง** เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="7f83e-379">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-379">Select **Save**.</span></span>

1. <span data-ttu-id="7f83e-380">เลือก **สร้าง** เพื่อสร้างใบสั่งขายสำหรับใบสั่งที่ 2</span><span class="sxs-lookup"><span data-stu-id="7f83e-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="7f83e-381">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7f83e-382">**ลูกค้า:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="7f83e-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="7f83e-383">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="7f83e-384">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-384">Select **OK**.</span></span>
1. <span data-ttu-id="7f83e-385">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="7f83e-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="7f83e-386">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-386">Set the following values:</span></span>

    - <span data-ttu-id="7f83e-387">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="7f83e-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="7f83e-388">**ปริมาณ:** *7*</span><span class="sxs-lookup"><span data-stu-id="7f83e-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="7f83e-389">เลือก **สร้างรายการ** เพื่อเพิ่มรายการที่สอง และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="7f83e-390">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="7f83e-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="7f83e-391">**ปริมาณ:** *3*</span><span class="sxs-lookup"><span data-stu-id="7f83e-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="7f83e-392">ทำซ้ำขั้นตอนต่อไปนี้สำหรับแต่ละรายการขายในใบสั่งเพื่อจองสินค้าคงคลัง:</span><span class="sxs-lookup"><span data-stu-id="7f83e-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="7f83e-393">บน FastTab **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="7f83e-394">บนหน้า **การจอง** เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="7f83e-395">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-395">Select **Save**.</span></span>

1. <span data-ttu-id="7f83e-396">เลือก **สร้าง** เพื่อสร้างใบสั่งขายสำหรับใบสั่งที่ 3</span><span class="sxs-lookup"><span data-stu-id="7f83e-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="7f83e-397">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7f83e-398">**ลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="7f83e-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="7f83e-399">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="7f83e-400">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-400">Select **OK**.</span></span>
1. <span data-ttu-id="7f83e-401">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="7f83e-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="7f83e-402">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-402">Set the following values:</span></span>

    - <span data-ttu-id="7f83e-403">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="7f83e-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="7f83e-404">**ปริมาณ:** *8*</span><span class="sxs-lookup"><span data-stu-id="7f83e-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="7f83e-405">ทำตามขั้นตอนต่อไปนี้เพื่อจองสินค้าคงคลังสำหรับรายการขาย:</span><span class="sxs-lookup"><span data-stu-id="7f83e-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="7f83e-406">บน FastTab **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="7f83e-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="7f83e-407">บนหน้า **การจอง** เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="7f83e-408">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-408">Select **Save**.</span></span>

<span data-ttu-id="7f83e-409">ดำเนินการกระบวนงานต่อไปนี้ให้เสร็จสมบูรณ์เพื่อนำใบสั่งขายแต่ละใบออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="7f83e-410">การจัดส่งที่แตกต่างกันสามรายการจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-410">Three different shipments will be created.</span></span> <span data-ttu-id="7f83e-411">จากนั้น คุณจะเพิ่มการจัดส่งทั้งหมดสามรายการไปยังเวฟใหม่</span><span class="sxs-lookup"><span data-stu-id="7f83e-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="7f83e-412">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7f83e-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7f83e-413">ในกริด ให้เลือกใบสั่งขายแรกที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="7f83e-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="7f83e-414">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="7f83e-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="7f83e-415">คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการจัดส่งที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="7f83e-416">ทำซ้ำขั้นตอนก่อนหน้านี้เพื่อนำใบสั่งขายที่ 2 และ 3 ออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="7f83e-417">โปรดสังเกตว่าข้อความที่ให้ข้อมูลที่คุณได้รับบ่งชี้ว่ามีการเพิ่มการจัดส่งไปยังเวฟที่สร้างขึ้น เมื่อคุณนำใบสั่งขายที่ 1 ออกใช้</span><span class="sxs-lookup"><span data-stu-id="7f83e-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="7f83e-418">ไปที่ **การจัดการคลังสินค้า \> เวฟขาออก \> เวฟการจัดส่ง \> เวฟทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7f83e-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="7f83e-419">เลือกรหัสเวฟที่สร้างจากการนำออกใช้ของใบสั่งขายเพื่อเปิดหน้า **เวฟ**</span><span class="sxs-lookup"><span data-stu-id="7f83e-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="7f83e-420">หน้านี้แสดงรายละเอียดเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-420">This page shows the wave details.</span></span> <span data-ttu-id="7f83e-421">FastTab **รายการเวฟ** แสดงการจัดส่งที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="7f83e-422">ขณะนี้คุณต้องสร้างงานเพื่อดึงสินค้าจากสถานที่เบิกสินค้าไปยังสถานที่การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="7f83e-423">ในบานหน้าต่างการดำเนินการ เลือก **ประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="7f83e-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="7f83e-424">ในระหว่างการประมวลผลเวฟ วิธีการเรียงลำดับจะใช้เท็มเพลตการเรียงลำดับเพื่อกำหนดสินค้าคงคลังเพื่อเรียงลำดับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="7f83e-425">เมื่อการประมวลผลเวฟเสร็จสมบูรณ์ คุณจะได้รับข้อความที่ให้ข้อมูลซึ่งบ่งชี้ว่ามีการลงรายการบัญชีเวฟและมีการสร้างงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="7f83e-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="7f83e-426">บนบานหน้าต่างการดำเนินการ บนแท็บ **เวฟ** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน** เพื่อดูงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="7f83e-427">จดบันทึกรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="7f83e-428">ไปที่ **การจัดการคลังสินค้า \> การบรรจุและการบรรจุลงตู้บรรจุสินค้า \> การกำหนดตำแหน่งการเรียงลำดับขาออก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="7f83e-429">ในคอลัมน์ด้านซ้าย คุณสามารถดูตำแหน่งการเรียงลำดับขาออกที่สร้างขึ้นสำหรับการจัดส่งสินค้าแต่ละครั้งได้</span><span class="sxs-lookup"><span data-stu-id="7f83e-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="7f83e-430">บน FastTab **เงื่อนไขตำแหน่งการเรียงลำดับ** คุณสามารถดูรหัสการจัดส่งสำหรับตำแหน่งดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="7f83e-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="7f83e-431">มีการสร้างรหัสงานหนึ่งรหัสเพื่อดึงสินค้าคงคลังจากสถานที่เบิกสินค้าไปยังสถานที่การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="7f83e-432">เมื่อต้องการทำงานให้เสร็จสมบูรณ์ คุณจะต้องมีรหัสงานที่สร้างขึ้นในระหว่างการประมวลผลเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="7f83e-433">การเบิกสินค้าตามใบสั่งขายไปยังสถานที่การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="7f83e-434">ลงชื่อเข้าใช้แอปสำหรับอุปกรณ์เคลื่อนที่ในฐานะผู้ปฏิบัติงานในคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="7f83e-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="7f83e-435">บนเมนูหลัก ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="7f83e-436">บนเมนู **ขาออก** ให้เลือก **การเบิกสินค้าขาย**</span><span class="sxs-lookup"><span data-stu-id="7f83e-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="7f83e-437">เลือกฟิลด์ **รหัส** แล้วจากนั้น ป้อนรหัสงานจากการประมวลผลเวฟ</span><span class="sxs-lookup"><span data-stu-id="7f83e-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="7f83e-438">ยืนยันรายการของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f83e-438">Confirm your entry.</span></span>

    <span data-ttu-id="7f83e-439">ถัดไป คุณจะได้รับพร้อมท์ให้ป้อนป้ายทะเบียนเป้าหมาย (LP)</span><span class="sxs-lookup"><span data-stu-id="7f83e-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="7f83e-440">โปรดสังเกตว่าบรรทัดที่ 1จากใบสั่งขายที่ 1 เป็นสิ่งที่ต้องมีการเบิกสินค้าและเพิ่มไปยังป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="7f83e-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="7f83e-441">หมายเลขสินค้า ปริมาณ คำอธิบายสินค้า และสถานที่เบิกสินค้า จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="7f83e-442">ในฟิลด์ **LP เป้าหมาย** ให้ป้อนหมายเลขป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="7f83e-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="7f83e-443">คุณจะเลือกบรรทัดทั้งหมดที่สร้างขึ้นจากเวฟที่มีการประมวลผลไปยังป้ายทะเบียนเป้าหมายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="7f83e-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="7f83e-444">ยืนยันรายการของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f83e-444">Confirm your entry.</span></span>

    <span data-ttu-id="7f83e-445">ขณะนี้แอปสำหรับอุปกรณ์เคลื่อนที่จะแสดงชุดของหน้า **การเบิกสินค้า** ที่ชี้ไปยังสถานที่เบิกสินค้าและไปยังสินค้าและปริมาณที่ต้องมีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="7f83e-446">หลังจากที่มีการเพิ่มสินค้าที่เบิกเข้าในป้ายทะเบียน คุณจะยืนยันงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="7f83e-447">หน้าสุดท้ายจะเป็นงานที่จะใช้ในการนำสินค้าที่เบิกเข้าไปไว้ในสถานที่การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="7f83e-448">ยืนยันงานการเบิกสินค้าครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="7f83e-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="7f83e-449">งานการเบิกสินค้าครั้งถัดไปจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-449">The next pick work is shown.</span></span> <span data-ttu-id="7f83e-450">ยืนยันการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-450">Confirm the pick.</span></span>
1. <span data-ttu-id="7f83e-451">ดำเนินการต่อเพื่อยืนยันงานการเบิกสินค้าที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="7f83e-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="7f83e-452">ขั้นตอนสุดท้ายคือการทำงานการส่งสินค้าให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="7f83e-452">The last step is to complete the put work.</span></span> <span data-ttu-id="7f83e-453">ยืนยันการสำรองสินค้าไปยังสถานที่การเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="7f83e-454">คุณได้รับข้อความ "งานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="7f83e-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="7f83e-455">ออกจาก **การเบิกสินค้าขาย** บนแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="7f83e-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="7f83e-456">การเรียงลำดับ/การย้ายไปที่ผนัง</span><span class="sxs-lookup"><span data-stu-id="7f83e-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="7f83e-457">หลังจากที่มีการย้ายสินค้าคงคลังทั้งหมดไปยังสถานที่การเรียงลำดับ ต้องมีการเรียงลำดับไปยังตำแหน่งการเรียงลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7f83e-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="7f83e-458">ลงชื่อเข้าใช้แอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="7f83e-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="7f83e-459">บนเมนูหลัก ให้เลือก **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="7f83e-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="7f83e-460">บนเมนู **ขาออก** ให้เลือก **เรียงลำดับ** เพื่อเริ่มต้นการเรียงลำดับสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="7f83e-461">ในฟิลด์ **LP/CON** ป้อนป้ายทะเบียนเป้าหมายของงานใบสั่งขายที่มีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="7f83e-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="7f83e-462">ยืนยันรายการของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f83e-462">Confirm your entry.</span></span>
1. <span data-ttu-id="7f83e-463">ป้อนหมายเลขสินค้าเพื่อเรียงลำดับก่อน</span><span class="sxs-lookup"><span data-stu-id="7f83e-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="7f83e-464">ระบบจะกำหนดตำแหน่งการเรียงลำดับแรกที่ควรแสดง</span><span class="sxs-lookup"><span data-stu-id="7f83e-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="7f83e-465">ยืนยันตำแหน่งการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="7f83e-466">คุณได้รับพร้อมท์ให้กำหนดป้ายทะเบียนให้กับตำแหน่งการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="7f83e-467">เลือกฟิลด์ **LP** ป้อนหมายเลขป้ายทะเบียน แล้วจากนั้น ยืนยันรายการของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f83e-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="7f83e-468">เนื่องจากตำแหน่งการเรียงลำดับเกี่ยวข้องกับรหัสการจัดส่ง คุณจะเรียงลำดับสินค้าที่มีการเบิกสินค้าไว้ในป้ายทะเบียนที่เฉพาะเจาะจงสำหรับการจัดส่งสินค้าขาออกและใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7f83e-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="7f83e-469">หน้าถัดไปจะแสดงรหัสสินค้า ปริมาณ รหัสตำแหน่งการเรียงลำดับ และรหัสรหัสป้ายทะเบียน "เริ่มต้น" (การเบิกสินค้า) และ "สิ้นสุด" (การเรียงลำดับ)</span><span class="sxs-lookup"><span data-stu-id="7f83e-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="7f83e-470">ข้อมูลในหน้านี้จะแนะนำให้คุณเรียงลำดับสินค้าและปริมาณที่ระบุจากป้ายทะเบียนการเบิกสินค้าลงในป้ายทะเบียนการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="7f83e-471">ยืนยันตำแหน่งการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="7f83e-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="7f83e-472">เรียงลำดับสินค้าในตำแหน่งการเรียงลำดับแรก</span><span class="sxs-lookup"><span data-stu-id="7f83e-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="7f83e-473">เมื่อคุณดำเนินการเสร็จสิ้น ระบบจะนำคุณไปยังตำแหน่งการเรียงลำดับถัดไป</span><span class="sxs-lookup"><span data-stu-id="7f83e-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="7f83e-474">ทำกระบวนการนี้ซ้ำสำหรับบรรทัดที่มีการเบิกสินค้าทั้งหมดในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="7f83e-475">นอกจากนี้ คุณควรใช้กระบวนการนี้ เมื่อมีบรรทัดการเบิกสินค้าหลายบรรทัดที่มีหมายเลขสินค้าเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="7f83e-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="7f83e-476">เมื่อคุณทำกระบวนการนี้ซ้ำสำหรับสินค้าทั้งหมด ระบบจะประเมินเงื่อนไขจากสินค้าที่สแกนถัดไป (รายการงาน) และกำหนดว่าควรวางไว้ในตำแหน่งการเรียงลำดับใด</span><span class="sxs-lookup"><span data-stu-id="7f83e-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="7f83e-477">คุณจะถูกนำทางโดยอัตโนมัติเพื่อย้ายสินค้าไปยังตำแหน่งการเรียงลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7f83e-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="7f83e-478">ทั้งนี้ขึ้นอยู่กับการตั้งค่าการยืนยัน คุณจะถูกนำทางเพื่อยืนยันการดำเนินการนี้โดยป้อนหมายเลขตำแหน่งหรือรหัสป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="7f83e-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f83e-479">ถ้ามีการเปิดใช้งานการเรียงลำดับอัตโนมัติ การแทนที่ด้วยตนเองจะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="7f83e-480">เมื่อคุณดำเนินการเสร็จสิ้น ใน Microsoft Dynamics 365 Supply Chain Management ให้เปิดหน้า **การกำหนดตำแหน่งการเรียงลำดับขาออก** เพื่อรีวิวสถานะของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="7f83e-481">ถ้ามีการปิดตำแหน่งโดยอัตโนมัติ ให้เลือก **แสดงรายการที่ปิด** เพื่อแสดงตำแหน่งที่ปิด</span><span class="sxs-lookup"><span data-stu-id="7f83e-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="7f83e-482">โปรดสังเกตว่าธุรกรรมตำแหน่งการเรียงลำดับจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="7f83e-483">สินค้าและปริมาณที่มีการประมวลผลโดยใช้ตำแหน่งจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="7f83e-484">เมื่อคุณตั้งค่าเท็มเพลตการเรียงลำดับขาออก คุณตั้งค่าตัวเลือก **ปิดตำแหน่งการจัดเรียงลำดับโดยอัตโนมัติ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="7f83e-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="7f83e-485">ดังนั้น ตำแหน่งจะถูกปิดโดยอัตโนมัติ หลังจากที่สินค้าคงคลังที่คาดไว้ท้ายสุดถูกย้ายไปยังตำแหน่งนั้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="7f83e-486">ตำแหน่งการเรียงลำดับจะอยู่ในสถานะ **ปิด** และมีการสร้างงานเพื่อย้ายสินค้าคงคลังที่เรียงลำดับไปยังสถานที่ *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="7f83e-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="7f83e-487">ทำงานการเบิกสินค้าคงคลังที่เรียงลำดับให้เสร็จสมบูรณ์ เพื่อย้ายสินค้าคงคลังไปยังสถานที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="7f83e-488">เมื่อสินค้าคงคลังพร้อมแล้ว ให้ยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="7f83e-489">สำหรับงานการเบิกสินค้าคงคลังที่เรียงลำดับที่จะถูกประมวลผลอย่างถูกต้อง รายการเมนูของอุปกรณ์เคลื่อนที่ที่มีรหัสคลาสงานที่มีการตั้งค่าฟิลด์ **ชนิดของใบสั่งงาน** เป็น *การเบิกสินค้าคงคลังที่เรียงลำดับ* ควรถูกใช้สำหรับกระบวนการเคลื่อนย้ายและการโหลด</span><span class="sxs-lookup"><span data-stu-id="7f83e-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="7f83e-490">ปิดตำแหน่งด้วยตนเอง (ไม่จำเป็นต้องระบุ)</span><span class="sxs-lookup"><span data-stu-id="7f83e-490">Manually close a position (optional)</span></span>

<span data-ttu-id="7f83e-491">ถ้าควรปิดตำแหน่งการเรียงลำดับด้วยตนเอง จะต้องมีการตั้งค่าตัวเลือก **ปิดตำแหน่งการเรียงลำดับอัตโนมัติ** สำหรับเท็มเพลตการเรียงลำดับขาออกเป็น *ไม่* และต้องทำการปิดก่อนที่จะสามารถย้ายสินค้าคงคลังไปยังพื้นที่ประตูได้</span><span class="sxs-lookup"><span data-stu-id="7f83e-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="7f83e-492">ตำแหน่งสามารถปิดได้หลายวิธีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="7f83e-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="7f83e-493">ผ่านแอปคลังสินค้า:</span><span class="sxs-lookup"><span data-stu-id="7f83e-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="7f83e-494">ผู้ใช้สามารถสแกนหนึ่งในสินค้าที่มีอยู่แล้วในตำแหน่ง แล้วจากนั้น เลือก **ปิด** เพื่อปิดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="7f83e-495">ถ้าผู้ใช้สแกนคอนเทนเนอร์ที่มีคอนเทนเนอร์ที่เรียงลำดับอยู่แล้ว ข้อความแสดงข้อผิดพลาดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7f83e-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="7f83e-496">อย่างไรก็ตาม ผู้ใช้ยังคงสามารถดำเนินการต่อเพื่อปิดตำแหน่งได้</span><span class="sxs-lookup"><span data-stu-id="7f83e-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="7f83e-497">จากหน้า **การกำหนดตำแหน่งการเรียงลำดับขาออก** ของ Microsoft Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="7f83e-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="7f83e-498">ผู้ใช้สามารถเลือกเรกคอร์ดตำแหน่งการเรียงลำดับขาออก แล้วจากนั้น เลือก **ปิดตำแหน่ง** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7f83e-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="7f83e-499">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="7f83e-499">Tips</span></span>

- <span data-ttu-id="7f83e-500">ไม่สามารถย้ายสินค้าระหว่างตำแหน่งต่างๆ ได้ หลังจากที่กำหนดให้กับตำแหน่งหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7f83e-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="7f83e-501">ระบบจะตรวจสอบจำนวนสินค้าแต่ละรายการที่ควรไปยังตำแหน่งที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="7f83e-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="7f83e-502">คุณสามารถตั้งค่าคอนฟิกเท็มเพลตการเรียงลำดับเพื่อสร้างคอนเทนเนอร์โดยอัตโนมัติ เมื่อมีการปิดตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="7f83e-503">วิธีการนี้จะสร้างโครงสร้างรหัสคอนเทนเนอร์มาตรฐานซึ่งยึดตามโพรไฟล์การจัดส่งที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="7f83e-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f83e-504">หลังจากที่สร้างงานการเคลื่อนย้ายจากสถานที่การเรียงลำดับแล้ว คุณต้องไม่ยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="7f83e-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="7f83e-505">มิฉะนั้น ตำแหน่งและคอนเทนเนอร์ในนั้นจะถูกลบออกจากระบบ และไม่พร้อมใช้งานสำหรับการประมวลผลต่อไป</span><span class="sxs-lookup"><span data-stu-id="7f83e-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="7f83e-506">สินค้าคงคลังจะถูกลบออกด้วย</span><span class="sxs-lookup"><span data-stu-id="7f83e-506">The inventory will also be removed.</span></span>
