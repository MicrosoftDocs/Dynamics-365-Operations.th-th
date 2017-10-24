--- 
title: "กำหนดกฎความครอบคลุมสำหรับสินค้า"
description: "ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14f56c30753da9458d66a46da8935305619fd0b8
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="b054c-103">กำหนดกฎความครอบคลุมสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b054c-103">Define coverage rules for items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b054c-104">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="b054c-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b054c-105">กระบวนการนี้แสดงวิธีการสร้างกฎความครอบคลุมและแทนที่การตั้งค่าความครอบคลุมสำหรับสินค้าเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="b054c-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="b054c-106">และยังแสดงวิธีการระบุการตั้งค่าสินค้าคงคลังเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b054c-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="b054c-107">การสร้างกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="b054c-107">Create a coverage group</span></span>
1. <span data-ttu-id="b054c-108">ไปที่กลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="b054c-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="b054c-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b054c-109">Click New.</span></span>
3. <span data-ttu-id="b054c-110">ในฟิลด์กลุ่มความครอบคลุม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b054c-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="b054c-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="b054c-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b054c-112">ในฟิลด์ปฏิทิน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b054c-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="b054c-113">เลือกปฏิทินที่การวางแผนหลักใช้ในการสร้างคำแนะนำในการเพิ่มเติมสินค้าสำหรับสินค้าในกลุ่มนี้</span><span class="sxs-lookup"><span data-stu-id="b054c-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="b054c-114">ในฟิลด์ความครอบคลุม ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b054c-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="b054c-115">เลือกข้อกำหนดสำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="b054c-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="b054c-116">ในกรอบเวลาความครอบคลุม(วัน) ให้ป้อน 90</span><span class="sxs-lookup"><span data-stu-id="b054c-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="b054c-117">สำหรับสินค้าในกลุ่มนี้ การวางแผนหลักจะสร้างคำแนะนำเพิ่มเติมสินค้าล่วงหน้าสูงสุด 90 วัน</span><span class="sxs-lookup"><span data-stu-id="b054c-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="b054c-118">ในฟิลด์จำนวนวันค่าลบ ให้ป้อน 1</span><span class="sxs-lookup"><span data-stu-id="b054c-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="b054c-119">ในฟิลด์จำนวนวันค่าบวก ให้ป้อน 1</span><span class="sxs-lookup"><span data-stu-id="b054c-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="b054c-120">ขยายหรือยุบส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b054c-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="b054c-121">ในฟิลด์ค่าเผื่อในการรับที่เพิ่มไปยังวันที่ของความต้องการ ให้ป้อน 1</span><span class="sxs-lookup"><span data-stu-id="b054c-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="b054c-122">ตัวอย่างเช่น ถ้าตั้งค่าค่าเผื่อในการรับเป็นหนึ่งวัน และรายการใบสั่งซื้อได้กำหนดการรับสินค้าไว้ในวันที่ 15 พฤษภาคม การวางแผนหลักจะคำนวณวันที่รับสินค้าที่มีการปรับปรุง เป็นวันที่ 16 พฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="b054c-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="b054c-123">ในฟิลด์เวลาเผื่อสำหรับการตัดสินค้าจากคลังที่ถูกหักออกจากวันที่ของความต้องการ ให้ป้อน 1</span><span class="sxs-lookup"><span data-stu-id="b054c-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="b054c-124">ตัวอย่างเช่น ถ้าตั้งค่าค่าเผื่อความปลอดภัยเป็นหนึ่งวัน และรายการใบสั่งขายได้กำหนดการจัดส่งไว้ในวันที่ 15 พฤษภาคม การวางแผนหลักจะคำนวณวันที่จัดส่งที่มีการปรับปรุง เป็นวันที่ 14 พฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="b054c-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="b054c-125">ในฟิลด์ค่าเผื่อในการสั่งใหม่ที่เพิ่มไปยังระยะเวลารอสินค้า ให้ป้อน 1</span><span class="sxs-lookup"><span data-stu-id="b054c-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="b054c-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b054c-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="b054c-127">สร้างผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="b054c-127">Create a new product</span></span>
1. <span data-ttu-id="b054c-128">ไปที่ผลิตภัณฑ์ที่จะนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="b054c-128">Go to Released products.</span></span>
2. <span data-ttu-id="b054c-129">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b054c-129">Click New.</span></span>
3. <span data-ttu-id="b054c-130">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b054c-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="b054c-131">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b054c-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="b054c-132">ในฟิลด์แบบจำลองสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b054c-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b054c-133">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b054c-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b054c-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b054c-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b054c-135">ในฟิลด์กลุ่มสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b054c-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b054c-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b054c-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b054c-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b054c-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b054c-138">ในฟิลด์กลุ่มมิติการจัดเก็บ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b054c-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b054c-139">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b054c-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="b054c-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b054c-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b054c-141">ในฟิลด์กลุ่มมิติการติดตาม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b054c-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b054c-142">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b054c-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="b054c-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b054c-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b054c-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b054c-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="b054c-145">ตั้งค่าการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b054c-145">Setup default order settings</span></span>
1. <span data-ttu-id="b054c-146">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="b054c-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="b054c-147">คลิกการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b054c-147">Click Default order settings.</span></span>
3. <span data-ttu-id="b054c-148">ในฟิลด์ไซต์การซื้อ ให้พิมพ์ไซต์ที่ใช้เป็นค่าเริ่มต้นเมื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b054c-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="b054c-149">ในฟิลด์ไซต์สินค้าคงคลัง ให้พิมพ์ไซต์ที่จัดเก็บสินค้า</span><span class="sxs-lookup"><span data-stu-id="b054c-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="b054c-150">ขยายหรือยุบส่วนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b054c-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="b054c-151">ตั้งค่าตัวคูณเป็น 10</span><span class="sxs-lookup"><span data-stu-id="b054c-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="b054c-152">ตั้งค่าปริมาณต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="b054c-152">Set Min.</span></span> <span data-ttu-id="b054c-153">ในใบสั่งเป็น '10'</span><span class="sxs-lookup"><span data-stu-id="b054c-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="b054c-154">ตั้งค่าปริมาณสูงสุด</span><span class="sxs-lookup"><span data-stu-id="b054c-154">Set Max.</span></span> <span data-ttu-id="b054c-155">ในใบสั่งเป็น '100'</span><span class="sxs-lookup"><span data-stu-id="b054c-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="b054c-156">ตั้งค่าปริมาณมาตรฐานในใบสั่งเป็น 10</span><span class="sxs-lookup"><span data-stu-id="b054c-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="b054c-157">ในฟิลด์ระยะเวลารอคอยสินค้าจากการซื้อ ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b054c-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="b054c-158">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายวันทำงาน</span><span class="sxs-lookup"><span data-stu-id="b054c-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="b054c-159">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b054c-159">Click Save.</span></span>
13. <span data-ttu-id="b054c-160">ในฟิลด์ชนิดใบสั่งเริ่มต้น ให้เลือก 'ใบสั่งซื้อ'</span><span class="sxs-lookup"><span data-stu-id="b054c-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="b054c-161">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b054c-161">Click Save.</span></span>
15. <span data-ttu-id="b054c-162">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b054c-162">Close the page.</span></span>
    * <span data-ttu-id="b054c-163">ปิดหน้าการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b054c-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="b054c-164">เพิ่มสินค้าไปยังกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="b054c-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="b054c-165">ขยายหรือยุบส่วนแผน</span><span class="sxs-lookup"><span data-stu-id="b054c-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="b054c-166">ในฟิลด์กลุ่มความครอบคลุม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b054c-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b054c-167">ในรายการ ให้ค้นหากลุ่มความครอบคลุมที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b054c-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="b054c-168">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b054c-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="b054c-169">สร้างกฎความครอบคลุมสินค้า</span><span class="sxs-lookup"><span data-stu-id="b054c-169">Create item coverage rules</span></span>
1. <span data-ttu-id="b054c-170">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="b054c-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="b054c-171">คลิกความครอบคลุมสินค้า</span><span class="sxs-lookup"><span data-stu-id="b054c-171">Click Item coverage.</span></span>
3. <span data-ttu-id="b054c-172">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b054c-172">Click New.</span></span>
4. <span data-ttu-id="b054c-173">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b054c-173">Click the General tab.</span></span>
5. <span data-ttu-id="b054c-174">เช็คกล่องบนหัวข้อของแทนที่การตั้งค่ากลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="b054c-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="b054c-175">ในฟิลด์กรอบเวลาความครอบคลุม (วัน) ให้ป้อน 60</span><span class="sxs-lookup"><span data-stu-id="b054c-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="b054c-176">แม้ว่าสินค้าที่อยู่ภายใต้ข้อกำหนดกลุ่มที่วางแผนไว้ 90 วันล่วงหน้า สินค้านี้จะถูกวางแผนไว้ 60 วันล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="b054c-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="b054c-177">ในฟิลด์จำนวนวันค่าลบ ให้ป้อน 2</span><span class="sxs-lookup"><span data-stu-id="b054c-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="b054c-178">ในฟิลด์จำนวนวันค่าบวก ให้ป้อน 2</span><span class="sxs-lookup"><span data-stu-id="b054c-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="b054c-179">คลิกที่แท็บเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="b054c-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="b054c-180">เช็คกล่องในส่วนหัวของการซื้อ</span><span class="sxs-lookup"><span data-stu-id="b054c-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="b054c-181">ในฟิลด์เวลาการซื้อ ให้ป้อน 5</span><span class="sxs-lookup"><span data-stu-id="b054c-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="b054c-182">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b054c-182">Click Save.</span></span>


