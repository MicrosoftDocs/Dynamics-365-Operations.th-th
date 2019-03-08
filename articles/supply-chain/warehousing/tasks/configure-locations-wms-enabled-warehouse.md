---
title: ตั้งค่าคอนฟิกของสถานที่ในคลังสินค้า WMS ที่เปิดใช้งาน
description: 'คำแนะนำนี้แสดงวิธีการตั้งค่าคอนฟิกการตั้งค่าสถานที่สำหรับการเปิดใช้งานคลังสินค้า WMS ใหม่ (คลังสินค้าที่ใช้กระบวนการจัดการคลังสินค้าขั้นสูง) '
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2be3c7cb33225041872e8b747ba28063f897dae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "337336"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="10d6d-103">ตั้งค่าคอนฟิกของสถานที่ในคลังสินค้า WMS ที่เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="10d6d-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10d6d-104">คำแนะนำนี้แสดงวิธีการตั้งค่าคอนฟิกการตั้งค่าสถานที่สำหรับการเปิดใช้งานคลังสินค้า WMS ใหม่ (คลังสินค้าที่ใช้กระบวนการจัดการคลังสินค้าขั้นสูง) </span><span class="sxs-lookup"><span data-stu-id="10d6d-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="10d6d-105">โดยทั่วไป กระบวนการนี้จะทำโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="10d6d-106">คุณสามารถรับชมคำแนะนำนี้ในข้อมูลสาธิตของบริษัท USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="10d6d-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="10d6d-107">เงื่อนไขเบื้องต้นคือ คุณมีอย่างน้อยหนึ่งไซต์ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="10d6d-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="10d6d-108">สร้างคลังสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="10d6d-108">Create a new warehouse</span></span>
1. <span data-ttu-id="10d6d-109">ไปที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="10d6d-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-110">Click New.</span></span>
3. <span data-ttu-id="10d6d-111">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="10d6d-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="10d6d-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="10d6d-113">ในฟิลด์ไซต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="10d6d-114">ขยายหรือยุบส่วนคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="10d6d-115">ตั้งค่าการใช้กระบวนการจัดการคลังสินค้าที่ตัวเลือก YES</span><span class="sxs-lookup"><span data-stu-id="10d6d-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="10d6d-116">การตั้งค่านี้ช่วยให้คุณสามารถดำเนินกระบวนการคลังสินค้าขั้นสูง โดยใช้งานในคลังสินค้าและอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="10d6d-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="10d6d-118">กำหนดรูปแบบสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-118">Define a location format</span></span>
1. <span data-ttu-id="10d6d-119">ไปที่รูปแบบสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-119">Go to Location formats.</span></span>
    * <span data-ttu-id="10d6d-120">รูปแบบสถานที่มีการตั้งชื่อระบบที่ใช้ในการสร้างชื่อเฉพาะและสอดคล้องกัน สำหรับพิกัดตำแหน่งของช่องเก็บต่างๆที่ใช้ภายในคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="10d6d-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="10d6d-121">อาจมีประโยชน์ที่จะใช้ตัวแบ่งเป็นส่วนหนึ่งของรูปแบบสถานที่ เพื่อให้การระบุส่วนประกอบของที่ตั้งเช่นหมายเลขที่เก็บง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="10d6d-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="10d6d-122">ในตัวอย่างนี้เราจะสร้างชื่อด้วย 4 องค์ประกอบ </span><span class="sxs-lookup"><span data-stu-id="10d6d-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="10d6d-123">ตัวอย่างเช่น องค์ประกอบเหล่านี้อาจเป็น ที่เก็บ ชั้นเก็บสินค้า ชั้น และช่องเก็บ</span><span class="sxs-lookup"><span data-stu-id="10d6d-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="10d6d-124">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-124">Click New.</span></span>
3. <span data-ttu-id="10d6d-125">ในฟิลด์รูปแบบสถานที่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="10d6d-126">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="10d6d-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="10d6d-127">ในฟิลด์คำอธิบายเซ็กเมนต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="10d6d-128">มีการอธิบายสิ่งที่ส่วนแรกของชื่อตั้งที่แสดงถึง </span><span class="sxs-lookup"><span data-stu-id="10d6d-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="10d6d-129">อาจจะเป็น ตัวอย่างเช่น ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="10d6d-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="10d6d-130">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="10d6d-131">จำนวนของอักขระที่ส่วนของชื่อสถานที่เก็บนี้ต้องมีจะถูกกำหนด </span><span class="sxs-lookup"><span data-stu-id="10d6d-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="10d6d-132">โปรดทราบว่า ผลรวมของส่วนประกอบทั้งหมดในชื่อ รวมถึงตัวแบ่ง ต้องไม่เกิน 10 อักขระ</span><span class="sxs-lookup"><span data-stu-id="10d6d-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="10d6d-133">ในฟิลด์ตัวแบ่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="10d6d-134">อักขระหรือสัญลักษณ์ที่ใช้ระหว่างส่วนประกอบที่หนึ่งและสองของชื่อจะถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="10d6d-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="10d6d-135">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-135">Click New.</span></span>
9. <span data-ttu-id="10d6d-136">ในฟิลด์คำอธิบายเซ็กเมนต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="10d6d-137">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="10d6d-138">ในฟิลด์ตัวแบ่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="10d6d-139">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-139">Click New.</span></span>
13. <span data-ttu-id="10d6d-140">ในฟิลด์คำอธิบายเซ็กเมนต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="10d6d-141">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="10d6d-142">ในฟิลด์ตัวแบ่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="10d6d-143">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-143">Click New.</span></span>
17. <span data-ttu-id="10d6d-144">ในฟิลด์คำอธิบายเซ็กเมนต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="10d6d-145">ในฟิลด์ความยาว ให้ใส่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="10d6d-146">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="10d6d-146">Click Save.</span></span>
20. <span data-ttu-id="10d6d-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="10d6d-148">กำหนดชนิดสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-148">Define location types</span></span>
1. <span data-ttu-id="10d6d-149">ไปที่ชนิดสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-149">Go to Location types.</span></span>
    * <span data-ttu-id="10d6d-150">ชนิดของสถานที่สามารถใช้เป็นตัวเลือกการกรองข้อมูลเพื่อควบคุมกระบวนการจัดการคลังสินค้าต่างๆ </span><span class="sxs-lookup"><span data-stu-id="10d6d-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="10d6d-151">อย่างน้อยที่สุด คุณต้องสร้างขั้นตอนและชนิดสถานที่การจัดส่งขั้นสุดท้ายเพื่อที่จะกำหนดกระบวนการจัดการคลังสินค้าขาออก</span><span class="sxs-lookup"><span data-stu-id="10d6d-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="10d6d-152">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-152">Click New.</span></span>
3. <span data-ttu-id="10d6d-153">ในฟิลด์ชนิดสถานที่ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="10d6d-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="10d6d-154">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="10d6d-155">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="10d6d-156">กำหนดโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-156">Define location profile</span></span>
1. <span data-ttu-id="10d6d-157">ไปที่โพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="10d6d-158">การกำหนดโพรไฟล์สถานที่นั้นมีความสำคัญมาก </span><span class="sxs-lookup"><span data-stu-id="10d6d-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="10d6d-159">สามารถควบคุมกำลังการผลิตของสถานที่ที่เป็นกลุ่มได้ที่นี่ เช่นเดียวกับนโยบายที่เกี่ยวข้องกับสิ่งที่สินค้าคงคลังได้รับจัดเก็บและวิธีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="10d6d-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="10d6d-160">ชนิดของสถานที่สามารถใช้เป็นตัวเลือกการกรองข้อมูลเพื่อควบคุมกระบวนการจัดการคลังสินค้าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="10d6d-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="10d6d-161">อย่างน้อยที่สุด คุณต้องสร้างโพรไฟล์ตำแหน่งผู้ใช้เพื่อเปิดใช้งานกระบวนการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="10d6d-162">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-162">Click New.</span></span>
3. <span data-ttu-id="10d6d-163">ในฟิลด์รหัสโพรไฟล์สถานที่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="10d6d-164">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="10d6d-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="10d6d-165">ในฟิลด์รูปแบบสถานที่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10d6d-166">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="10d6d-167">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="10d6d-168">ในฟิลด์ชนิดสถานที่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="10d6d-169">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="10d6d-170">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="10d6d-171">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายของการอนุญาตสถานะสินค้าคงคลังแบบผสม</span><span class="sxs-lookup"><span data-stu-id="10d6d-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="10d6d-172">เปิดใช้งานตัวเลือกนี้ ถ้าคุณต้องการอนุญาตให้มีค่าสถานะของสินค้าคงคลังแบบผสมในสถานที่ที่จะถูกจัดกลุ่มตามโพรไฟล์ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="10d6d-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="10d6d-173">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายของการแทนที่กฎสำหรับจำนวนวันของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="10d6d-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="10d6d-174">เปิดใช้งานตัวเลือกนี้เพื่อแทนที่กฎสำหรับจำนวนวันของวันหมดอายุของชุดงานสินค้าคงคลังที่อาจแตกต่างกัน เพื่ออนุญาตให้มีการผสมของชุดงานสินค้าคงคลังที่ไม่ปฏิบัติตามกฎนี้</span><span class="sxs-lookup"><span data-stu-id="10d6d-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="10d6d-175">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายของการอนุญาตการตรวจนับตามรอบ</span><span class="sxs-lookup"><span data-stu-id="10d6d-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="10d6d-176">เปิดใช้งานตัวเลือกนี้ เพื่ออนุญาตให้มีการดำเนินการการตรวจนับตามรอบในทุกสถานที่ที่จะถูกจัดกลุ่มตามโพรไฟล์ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="10d6d-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="10d6d-177">ขยายหรือยุบส่วนมิติ</span><span class="sxs-lookup"><span data-stu-id="10d6d-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="10d6d-178">แท็บมิติช่วยให้คุณสามารถกำหนดพารามิเตอร์และวิธีการเปิดใช้งานการคำนวณที่แม่นยำของกำลังการผลิตที่อยู่ภายในแต่ละที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="10d6d-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="10d6d-179">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="10d6d-180">เปิดใช้งานพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="10d6d-181">ไปที่พารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="10d6d-182">เพื่อให้สามาถดำเนินงานคลังสินค้าได้ ต้องมีการตั้งค่าพารามิเตอร์สำหรับโพรไฟล์ที่ตั้งผู้ใช้ชนิดสถานที่การแบ่งระยะ และชนิดสถานที่จัดส่งขั้นสุดท้าย ทันทีที่กระบวนการขาออกสิ้นสุดที่ชนิดสถานที่จัดส่งขั้นสุดท้ายตามที่คุณกำหนด ธุรกรรมขาออกที่เกี่ยวข้องจะถูกอัพเดตเป็น เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="10d6d-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="10d6d-183">ขยายหรือยุบส่วนโปรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="10d6d-184">ในฟิลด์สถานที่ผู้ใช้ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="10d6d-185">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="10d6d-186">ขยายหรือยุบส่วนชนิดสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="10d6d-187">ในฟิลด์ชนิดสถานที่การแบ่งระยะ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="10d6d-188">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="10d6d-189">ในฟิลด์ชนิดสถานที่จัดส่งสุดท้าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="10d6d-190">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="10d6d-191">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="10d6d-192">กำหนดกลุ่มโซนคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="10d6d-193">ไปที่กลุ่มโซนคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="10d6d-194">โซนคลังสินค้าสามารถใช้เป็นตัวกรองสำหรับตัวเลือกในการควบคุมกระบวนการจัดการคลังสินค้าต่างๆ </span><span class="sxs-lookup"><span data-stu-id="10d6d-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="10d6d-195">คุณต้องสร้างกลุ่มโซนก่อนที่คุณจะสามารถกำหนดโซน</span><span class="sxs-lookup"><span data-stu-id="10d6d-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="10d6d-196">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-196">Click New.</span></span>
3. <span data-ttu-id="10d6d-197">ในฟิลด์รหัสกลุ่มโซน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="10d6d-198">ในฟิลด์ชื่อกลุ่มโซน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="10d6d-199">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="10d6d-200">กำหนดโซนคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="10d6d-201">ไปที่โซน</span><span class="sxs-lookup"><span data-stu-id="10d6d-201">Go to Zones.</span></span>
2. <span data-ttu-id="10d6d-202">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-202">Click New.</span></span>
3. <span data-ttu-id="10d6d-203">ในฟิลด์รหัสโซน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="10d6d-204">ในฟิลด์ชื่อโซน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="10d6d-205">ในฟิลด์รหัสกลุ่มโซน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10d6d-206">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="10d6d-207">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="10d6d-208">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="10d6d-209">สร้างสถานโดยใช้วิซาร์ดการตั้งค่าสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="10d6d-210">ไปที่วิซาร์ดการตั้งค่าสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="10d6d-211">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="10d6d-212">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="10d6d-213">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="10d6d-214">ในฟิลด์รหัสโซน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10d6d-215">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="10d6d-216">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="10d6d-217">ในฟิลด์รหัสโพรไฟล์สถานที่ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="10d6d-218">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="10d6d-219">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="10d6d-220">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="10d6d-221">ในฟิลด์หมายเลขจาก ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="10d6d-222">ฟิลด์หมายเลขเริ่มต้นและหมายเลขสิ้นสุดกำหนดจำนวนสถานที่จะถูกสร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="10d6d-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="10d6d-223">ตัวอย่างเช่น ถ้าคุณตั้งค่าหมายเลขเริ่มต้นเป็น 1 และหมายเลขสิ้นสุดเป็น 3 สำหรับสี่รายการในรูปแบบที่ตั้ง ที่ตั้ง 81 ที่ตั้งจะถูกสร้าง (3x3x3x3)</span><span class="sxs-lookup"><span data-stu-id="10d6d-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="10d6d-224">ในฟิลด์หมายเลขถึง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="10d6d-225">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="10d6d-226">ในฟิลด์หมายเลขจาก ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="10d6d-227">ในฟิลด์หมายเลขถึง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="10d6d-228">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="10d6d-229">ในฟิลด์หมายเลขจาก ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="10d6d-230">ในฟิลด์หมายเลขถึง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="10d6d-231">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10d6d-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="10d6d-232">ในฟิลด์หมายเลขจาก ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="10d6d-233">ในฟิลด์หมายเลขถึง ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="10d6d-234">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="10d6d-235">สร้างสถานที่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="10d6d-235">Create locations manually</span></span>
1. <span data-ttu-id="10d6d-236">ไปที่สถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-236">Go to Locations.</span></span>
    * <span data-ttu-id="10d6d-237">การสร้างสถานที่ภายในคลังสินค้าสามารถทำได้อย่างง่ายด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="10d6d-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="10d6d-238">ชื่อสถานที่เก็บและรหัสโพรไฟล์สถานที่เป็นค่าบังคับ</span><span class="sxs-lookup"><span data-stu-id="10d6d-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="10d6d-239">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-239">Click New.</span></span>
3. <span data-ttu-id="10d6d-240">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="10d6d-241">ในฟิลด์ตำแหน่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="10d6d-242">โปรดทราบว่า คุณกำลังสร้างตำแหน่งใหม่ที่นี่ ดังนั้นคุณต้องป้อนชื่อเฉพาะใหม่ แทนที่การเลือกชื่อที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="10d6d-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="10d6d-243">ในฟิลด์รหัสโพรไฟล์สถานที่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="10d6d-244">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="10d6d-245">กำหนดประเภทของขนาดแพ็ค</span><span class="sxs-lookup"><span data-stu-id="10d6d-245">Define Pack size categories</span></span>
1. <span data-ttu-id="10d6d-246">ไปที่ประเภทของขนาดแพ็ค</span><span class="sxs-lookup"><span data-stu-id="10d6d-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="10d6d-247">ประเภทของขนาดแพ็คสามารถใช้เพื่อจัดกลุ่มสินค้าที่มีขนาดใกล้เคียงกัน </span><span class="sxs-lookup"><span data-stu-id="10d6d-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="10d6d-248">ในตัวอย่างนี้ จะใช้ประเภทของขนาดแพ็คเพื่อควบคุมกำลังการผลิตที่สถานที่เบิกสินค้าภายในโซนเฉพาะของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="10d6d-249">โปรดทราบว่า รหัสประเภทของขนาดแพ็คต้องถูกกำหนดให้กับเอนทิตี้ผลิตภัณฑ์ที่นำออกใช้เพื่อให้สามารถใช้เป็นส่วนหนึ่งของการประมวลผลการเก็บสต็อก</span><span class="sxs-lookup"><span data-stu-id="10d6d-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="10d6d-250">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-250">Click New.</span></span>
3. <span data-ttu-id="10d6d-251">ในฟิลด์รหัสประเภทขนาดของแพ็ค ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="10d6d-252">ในฟิลด์ชื่อประเภทขนาดของแพ็ค ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="10d6d-253">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="10d6d-254">กำหนดขีดจำกัดการเก็บสต็อกในสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-254">Define location stocking limits</span></span>
1. <span data-ttu-id="10d6d-255">ไปที่ขีดจำกัดการเก็บสต็อกในสถานที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="10d6d-256">ขีดจำกัดของสถานที่เก็บสินค้าคงคลังช่วยให้มั่นใจได้ว่างานที่ไม่ได้ถูกขอให้สร้าง สินค้าคงคลังถูกจัดเก็บอยู่ในสถานที่ที่ไม่ได้มีกำลังการผลิตอยู่จริงเพื่อให้แน่ใจว่าสถานทีที่สามารถจัดเก็บสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="10d6d-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="10d6d-257">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-257">Click New.</span></span>
3. <span data-ttu-id="10d6d-258">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="10d6d-259">ในฟิลด์รหัสโพรไฟล์สถานที่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="10d6d-260">ในฟิลด์รหัสประเภทขนาดของแพ็ค ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="10d6d-261">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="10d6d-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="10d6d-262">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="10d6d-262">Click Save.</span></span>
8. <span data-ttu-id="10d6d-263">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="10d6d-264">กำหนดสถานที่คงที่เบิกสินค้าถาวร</span><span class="sxs-lookup"><span data-stu-id="10d6d-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="10d6d-265">ไปที่สถานที่คงที่</span><span class="sxs-lookup"><span data-stu-id="10d6d-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="10d6d-266">คุณสามารถกำหนดสถานที่ที่จะใช้สำหรับแต่ละผลิตภัณฑ์หรือต่อผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="10d6d-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="10d6d-267">มีความเป็นไปได้ในการสร้างสถานที่คงที่หลายรายการสำหรับผลิตภัณฑ์เดียวกันภายในคลังสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="10d6d-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="10d6d-268">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10d6d-268">Click New.</span></span>
3. <span data-ttu-id="10d6d-269">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="10d6d-270">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10d6d-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="10d6d-271">ในฟิลด์ตำแหน่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="10d6d-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10d6d-272">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10d6d-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="10d6d-273">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10d6d-273">Close the page.</span></span>

