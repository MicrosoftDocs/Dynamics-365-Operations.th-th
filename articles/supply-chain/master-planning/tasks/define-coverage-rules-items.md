---
title: กำหนดกฎความครอบคลุมสำหรับสินค้า
description: ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF
author: ShylaThompson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ecd56c84b232fd7855bf2fb01eaebe3f3bd4440
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150297"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="a102e-103">กำหนดกฎความครอบคลุมสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="a102e-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a102e-104">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="a102e-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a102e-105">กระบวนการนี้แสดงวิธีการสร้างกฎความครอบคลุมและแทนที่การตั้งค่าความครอบคลุมสำหรับสินค้าเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="a102e-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="a102e-106">และยังแสดงวิธีการระบุการตั้งค่าสินค้าคงคลังเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a102e-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="a102e-107">การสร้างกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="a102e-107">Create a coverage group</span></span>
1. <span data-ttu-id="a102e-108">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การวางแผนหลัก > การตั้งค่า > กลุ่มความครอบคลุม**</span><span class="sxs-lookup"><span data-stu-id="a102e-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="a102e-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a102e-109">Click **New**.</span></span>
3. <span data-ttu-id="a102e-110">ในฟิลด์ **กลุ่มความครอบคลุม** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a102e-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="a102e-111">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a102e-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a102e-112">ในฟิลด์ **ปฏิทิน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a102e-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="a102e-113">เลือกปฏิทินที่การวางแผนหลักใช้ในการสร้างคำแนะนำในการเพิ่มเติมสินค้าสำหรับสินค้าในกลุ่มนี้</span><span class="sxs-lookup"><span data-stu-id="a102e-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="a102e-114">ในฟิลด์ **รหัสความครอบคลุม** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="a102e-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="a102e-115">เลือก 'ข้อกำหนด' สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="a102e-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="a102e-116">ใน **ฟิลด์กรอบเวลาความครอบคลุม (วัน)** ให้ป้อน '90'</span><span class="sxs-lookup"><span data-stu-id="a102e-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="a102e-117">สำหรับสินค้าในกลุ่มนี้ การวางแผนหลักจะสร้างคำแนะนำเพิ่มเติมสินค้าล่วงหน้าสูงสุด 90 วัน</span><span class="sxs-lookup"><span data-stu-id="a102e-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="a102e-118">ในฟิลด์ **จำนวนวันค่าลบ** ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="a102e-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="a102e-119">ในฟิลด์ **จำนวนวันค่าบวก** ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="a102e-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="a102e-120">ขยายหรือยุบส่วน **อื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="a102e-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="a102e-121">ภายใต้ส่วน **ค่าเผื่อความปลอดภัยเป็นวัน** ในฟิลด์ **ค่าเผื่อในการรับที่เพิ่มไปยังวันที่ของความต้องการ** ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="a102e-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="a102e-122">ตัวอย่างเช่น ถ้าตั้งค่าค่าเผื่อในการรับเป็นหนึ่งวัน และรายการใบสั่งซื้อได้กำหนดการรับสินค้าไว้ในวันที่ 15 พฤษภาคม การวางแผนหลักจะคำนวณวันที่รับสินค้าที่มีการปรับปรุง เป็นวันที่ 16 พฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="a102e-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="a102e-123">ในฟิลด์ **ออกกำไรที่หักออกจากวันที่ของความต้องการ** ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="a102e-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="a102e-124">ตัวอย่างเช่น ถ้าตั้งค่าค่าเผื่อความปลอดภัยเป็นหนึ่งวัน และรายการใบสั่งขายได้กำหนดการจัดส่งไว้ในวันที่ 15 พฤษภาคม การวางแผนหลักจะคำนวณวันที่จัดส่งที่มีการปรับปรุง เป็นวันที่ 14 พฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="a102e-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="a102e-125">ในฟิลด์ **จัดลำดับกำไรที่เพิ่มไปยังระยะเวลารอสินค้าใหม่** ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="a102e-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="a102e-126">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a102e-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="a102e-127">สร้างผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="a102e-127">Create a new product</span></span>
1. <span data-ttu-id="a102e-128">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a102e-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="a102e-129">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a102e-129">Click **New**.</span></span>
3. <span data-ttu-id="a102e-130">ในฟิลด์ **หมายเลขผลิตภัณฑ์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a102e-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="a102e-131">ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a102e-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="a102e-132">ในฟิลด์ **กลุ่มแบบจำลองสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a102e-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a102e-133">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a102e-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a102e-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a102e-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a102e-135">ในฟิลด์ **กลุ่มสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a102e-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a102e-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a102e-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a102e-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a102e-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a102e-138">ในฟิลด์ **กลุ่มมิติการจัดเก็บ** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a102e-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a102e-139">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a102e-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="a102e-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a102e-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a102e-141">ในฟิลด์ **กลุ่มมิติการติดตาม** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a102e-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="a102e-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a102e-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="a102e-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a102e-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="a102e-144">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a102e-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="a102e-145">ตั้งค่าการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a102e-145">Setup default order settings</span></span>
1. <span data-ttu-id="a102e-146">ใน **บานหน้าต่างการดำเนินการ** คลิก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="a102e-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="a102e-147">ภายใต้ **การตั้งค่าใบสั่ง** คลิก **การตั้งค่าใบสั่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="a102e-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="a102e-148">ภายใต้ **ใบสั่งซื้อ** ในฟิลด์ **ไซต์เริ่มต้น** ให้พิมพ์ไซต์ที่ใช้เป็นค่าเริ่มต้นเมื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="a102e-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="a102e-149">ในฟิลด์ **คลังสินค้าเริ่มต้น** ให้พิมพ์ไซต์ที่ซึ่งมีการจัดเก็บสินค้า</span><span class="sxs-lookup"><span data-stu-id="a102e-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="a102e-150">ขยายหรือยุบส่วน **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="a102e-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="a102e-151">ในฟิลด์ **หลายรายการ** ให้พิมพ์ '10'</span><span class="sxs-lookup"><span data-stu-id="a102e-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="a102e-152">ในฟิลด์ **ปริมาณต่ำสุดในใบสั่ง** ให้พิมพ์ '10'</span><span class="sxs-lookup"><span data-stu-id="a102e-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="a102e-153">ในฟิลด์ **ปริมาณสูงสุดในใบสั่ง** ให้พิมพ์ '100'</span><span class="sxs-lookup"><span data-stu-id="a102e-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="a102e-154">ใน **ปริมาณในใบสั่งมาตรฐาน** พิมพ์ '10'</span><span class="sxs-lookup"><span data-stu-id="a102e-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="a102e-155">ในฟิลด์ **ระยะเวลารอคอยสินค้าจากการซื้อ** ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="a102e-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="a102e-156">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **วันทำงาน**</span><span class="sxs-lookup"><span data-stu-id="a102e-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="a102e-157">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a102e-157">Click **Save**.</span></span>
13. <span data-ttu-id="a102e-158">ในฟิลด์ **ชนิดใบสั่งเริ่มต้น** ให้เลือก 'ใบสั่งซื้อ'</span><span class="sxs-lookup"><span data-stu-id="a102e-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="a102e-159">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a102e-159">Click **Save**.</span></span>
15. <span data-ttu-id="a102e-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a102e-160">Close the page.</span></span> <span data-ttu-id="a102e-161">ปิดหน้าการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a102e-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="a102e-162">เพิ่มสินค้าไปยังกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="a102e-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="a102e-163">ขยายหรือยุบส่วน **แผน**</span><span class="sxs-lookup"><span data-stu-id="a102e-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="a102e-164">ในฟิลด์ **กลุ่มความครอบคลุม** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a102e-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a102e-165">ในรายการ ให้ค้นหา **กลุ่มความครอบคลุม** ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a102e-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="a102e-166">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a102e-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="a102e-167">สร้างกฎความครอบคลุมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a102e-167">Create item coverage rules</span></span>
1. <span data-ttu-id="a102e-168">ใน **บานหน้าต่างการดำเนินการ** คลิก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="a102e-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="a102e-169">ภายใต้ **ความครอบคลุม** คลิก **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a102e-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="a102e-170">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a102e-170">Click **New**.</span></span>
4. <span data-ttu-id="a102e-171">คลิกแท็บ **ทั่วไป** </span><span class="sxs-lookup"><span data-stu-id="a102e-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="a102e-172">ตรวจสอบกล่องบนส่วนหัวของการตั้งค่า **แทนที่กลุ่มความครอบคลุม**</span><span class="sxs-lookup"><span data-stu-id="a102e-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="a102e-173">ในฟิลด์ **กรอบเวลาความครอบคลุม (วัน)** ให้ป้อน '60'</span><span class="sxs-lookup"><span data-stu-id="a102e-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="a102e-174">แม้ว่าสินค้าที่อยู่ภายใต้ข้อกำหนดกลุ่มที่วางแผนไว้ 90 วันล่วงหน้า สินค้านี้จะถูกวางแผนไว้ 60 วันล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a102e-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="a102e-175">ในฟิลด์ **จำนวนวันค่าลบ** ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="a102e-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="a102e-176">ในฟิลด์ **จำนวนวันค่าบวก** ให้ป้อน '2'</span><span class="sxs-lookup"><span data-stu-id="a102e-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="a102e-177">คลิกที่แท็บ **เวลารอคอยสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a102e-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="a102e-178">ตรวจสอบกล่องในส่วนหัวของ **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="a102e-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="a102e-179">ในฟิลด์ **เวลาที่ซื้อ** ให้ป้อน '5'</span><span class="sxs-lookup"><span data-stu-id="a102e-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="a102e-180">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a102e-180">Click **Save**.</span></span>

