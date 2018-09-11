--- 
title: "สร้างการจัดวางพื้นที่คลังสินค้าใหม่"
description: "กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลเกี่ยวกับสถานที่เก็บในคลังสินค้า "
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 7db15eb5d80291641f0d0398d236b5e883cafcaf
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="a2e38-103">สร้างการจัดวางพื้นที่คลังสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="a2e38-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2e38-104">กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลเกี่ยวกับสถานที่เก็บในคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="a2e38-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="a2e38-105">ใช้ได้เฉพาะกับคลังสินค้าที่สร้างขึ้นโดยใช้ "คลังสินค้าพื้นฐาน" ในโมดูลการบริหารสินค้าคงคลัง ไม่ใช่คลังสินค้าที่สร้างขึ้นในโมดูลการบริหารคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="a2e38-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือในข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a2e38-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="a2e38-107">ตั้งค่าความจุสถานที่ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a2e38-107">Set the default location capacity</span></span>
1. <span data-ttu-id="a2e38-108">ไปที่การจัดการสินค้าคงคลัง > การตั้งค่า > สินค้าคงคลังและพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="a2e38-109">คลิกแท็บตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="a2e38-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="a2e38-110">ในฟิลด์ความกว้างพื้นฐาน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a2e38-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="a2e38-111">ในฟิลด์ความลึกพื้นฐาน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a2e38-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="a2e38-112">ในฟิลด์ความสูงพื้นฐาน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a2e38-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="a2e38-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="a2e38-113">Click Save.</span></span>
7. <span data-ttu-id="a2e38-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="a2e38-115">กำหนดรูปแบบของชื่อสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="a2e38-115">Define the location name format</span></span>
1. <span data-ttu-id="a2e38-116">ไปที่ การบริหารสินค้าคงคลัง > การตั้งค่า > การแบ่งสินค้าคงคลัง > คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="a2e38-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a2e38-117">Click New.</span></span>
3. <span data-ttu-id="a2e38-118">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a2e38-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="a2e38-119">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="a2e38-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a2e38-120">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2e38-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a2e38-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a2e38-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a2e38-122">สลับการขยายของส่วนชื่อสถานที่</span><span class="sxs-lookup"><span data-stu-id="a2e38-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="a2e38-123">ตัวเลือกในส่วนนี้กำหนดรูปแบบเริ่มต้นสำหรับชื่อสถานที่เก็บ </span><span class="sxs-lookup"><span data-stu-id="a2e38-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="a2e38-124">ในตัวอย่างของเรา จะรวมถึงหมายเลขที่เก็บ หมายเลขชั้นเก็บสินค้า และหมายเลขชั้นวาง</span><span class="sxs-lookup"><span data-stu-id="a2e38-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="a2e38-125">ตั้งค่าตัวเลือก รวมที่เก็บสินค้า ให้เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="a2e38-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="a2e38-126">ตั้งค่าตัวเลือก รวมชั้นเก็บสินค้า ให้เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="a2e38-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="a2e38-127">ในฟิลด์รูปแบบสำหรับชั้นเก็บสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a2e38-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="a2e38-128">ตัวอย่างเช่น: -##</span><span class="sxs-lookup"><span data-stu-id="a2e38-128">For example: -##</span></span>  
11. <span data-ttu-id="a2e38-129">ตั้งค่าตัวเลือก รวมชั้นวางสินค้า ให้เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="a2e38-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="a2e38-130">ในฟิลด์รูปแบบสำหรับชั้นวางสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a2e38-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="a2e38-131">ตัวอย่างเช่น: -##</span><span class="sxs-lookup"><span data-stu-id="a2e38-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="a2e38-132">กำหนดที่ตั้งของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-132">Define warehouse locations</span></span>
1. <span data-ttu-id="a2e38-133">ในบานหน้าต่างการดำเนินการ คลิกคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="a2e38-134">คลิกวิซาร์ดที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="a2e38-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="a2e38-135">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-135">Click Next.</span></span>
4. <span data-ttu-id="a2e38-136">ยกเลิกการเลือกตัวเลือก ท่าสินค้าขาออก</span><span class="sxs-lookup"><span data-stu-id="a2e38-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="a2e38-137">ยกเลิกการเลือกตัวเลือก สถานที่เก็บสินค้าจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="a2e38-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="a2e38-138">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-138">Click Next.</span></span>
7. <span data-ttu-id="a2e38-139">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-139">Click Next.</span></span>
8. <span data-ttu-id="a2e38-140">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-140">Click Next.</span></span>
9. <span data-ttu-id="a2e38-141">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-141">Click Next.</span></span>
10. <span data-ttu-id="a2e38-142">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-142">Click Next.</span></span>
11. <span data-ttu-id="a2e38-143">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-143">Click Next.</span></span>
12. <span data-ttu-id="a2e38-144">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-144">Click Next.</span></span>
    * <span data-ttu-id="a2e38-145">โปรดทราบว่า มิติทางกายภาพที่แสดงบนหน้านี้เป็นมิติที่คุณตั้งค่าตอนเริ่มต้นของกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="a2e38-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="a2e38-146">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a2e38-146">Click Next.</span></span>
14. <span data-ttu-id="a2e38-147">คลิก Finish</span><span class="sxs-lookup"><span data-stu-id="a2e38-147">Click Finish.</span></span>
15. <span data-ttu-id="a2e38-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-148">Close the page.</span></span>
16. <span data-ttu-id="a2e38-149">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="a2e38-149">Refresh the page.</span></span>


