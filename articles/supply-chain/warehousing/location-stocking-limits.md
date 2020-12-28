---
title: ขีดจำกัดการเก็บสต็อกในสถานที่
description: หัวข้อนี้จะอธิบายถึงฟังก์ชันสำหรับขีดจำกัดการเก็บสต็อกของสถานที่เก็บ
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 208662f38b06b1f230bdde5247946a9fefd57cea
ms.sourcegitcommit: d2dea9ce480f35d0c0b10615c18862695e107d55
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/23/2020
ms.locfileid: "4607290"
---
# <a name="location-stocking-limits"></a><span data-ttu-id="f7994-103">ขีดจำกัดการเก็บสต็อกในสถานที่</span><span class="sxs-lookup"><span data-stu-id="f7994-103">Location stocking limits</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7994-104">คุณสามารถใช้หน้า **ขีดจำกัดของสถานที่เก็บ** (**การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> ขีดจำกัดของสถานที่เก็บ**) เพื่อควบคุมความจุของจำนวนงานในศูนย์การผลิตที่ที่ตั้งคลังสินค้าได้โดยไม่ต้องใช้กระบวนการขั้นสูงเพิ่มเติมสำหรับการคำนวณปริมาตรของผลิตภัณฑ์ทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="f7994-104">You can use the **Location stocking limits** page (**Warehouse management \> Setup \> Warehouse \> Location stocking limits**) to control the load capacity at warehouse locations without having to use the more advanced processes for volumetric calculations of physical products.</span></span>

<span data-ttu-id="f7994-105">จุดประสงค์ของขีดจำกัดของสถานที่เก็บจะประเมินปริมาณสูงสุดที่สถานที่สามารถมีได้</span><span class="sxs-lookup"><span data-stu-id="f7994-105">The purpose of location stocking limits is to evaluate the maximum quantity that a location can contain.</span></span> <span data-ttu-id="f7994-106">คุณสามารถตั้งค่าลักษณะการทำงานได้ในระดับสามระดับ ซึ่งแต่ละอย่างจะมีแท็บของตนเองบนหน้า **ขีดจำกัดของสถานที่เก็บข้อมูล**:</span><span class="sxs-lookup"><span data-stu-id="f7994-106">You can set up the feature on any of three levels, each of which has its own tab on the **Location stocking limits** page:</span></span>

- <span data-ttu-id="f7994-107">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f7994-107">Products</span></span>
- <span data-ttu-id="f7994-108">ผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="f7994-108">Product variants</span></span>
- <span data-ttu-id="f7994-109">ชนิดตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7994-109">Container types</span></span>

<span data-ttu-id="f7994-110">สำหรับแต่ละระดับ คุณสามารถกำหนดค่าฟิลด์ที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="f7994-110">For each level, you can define different field values.</span></span> <span data-ttu-id="f7994-111">โดยระบบจะประเมินกำลังการผลิตของสถานที่เก็บที่ระบุตามค่า **ปริมาณ** และ **ต่อหน่วย** สำหรับแต่ละแถว</span><span class="sxs-lookup"><span data-stu-id="f7994-111">The system will then evaluate the capacity of a specific location, based on the **Quantity** and **Unit** values for each row.</span></span> <span data-ttu-id="f7994-112">การทำเช่นนี้จะเป็นการเลือกเรกคอร์ดการจับคู่ที่มีรายละเอียดมากที่สุดก่อน</span><span class="sxs-lookup"><span data-stu-id="f7994-112">It will select the most detailed matching record first.</span></span> <span data-ttu-id="f7994-113">ตัวอย่างเช่น แถวที่มีค่าในฟิลด์ **รหัสโพรไฟล์สถานที่** จะถูกประเมินก่อนแถวที่มีค่าเฉพาะในฟิลด์ **คลังสินค้า** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f7994-113">For example, a row that has a value in the **Location profile ID** field will be evaluated before a row that has a value only in the **Warehouse** field.</span></span> <span data-ttu-id="f7994-114">ความจุที่เหลือจะถูกประเมินตามค่า **ปริมาณ** เรกคอร์ดขีดจำกัดการเก็บสต็อกในสถานที่ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="f7994-114">The remaining capacity will also be evaluated, based on the **Quantity** value for the location stocking limit record that is used.</span></span>

<span data-ttu-id="f7994-115">ในส่วน **ผลิตภัณฑ์** ของหน้า คุณสามารถกำหนดค่าของฟิลด์ต่อไปนี้สำหรับการค้นหาการจำกัดการกำหนดสถานที่เก็บ:</span><span class="sxs-lookup"><span data-stu-id="f7994-115">In the **Products** section of the page, you can define the following field values for the search for location stocking limits:</span></span>

- <span data-ttu-id="f7994-116">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7994-116">Warehouse</span></span>
- <span data-ttu-id="f7994-117">รหัสโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="f7994-117">Location profile ID</span></span>
- <span data-ttu-id="f7994-118">ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f7994-118">Location</span></span>
- <span data-ttu-id="f7994-119">รหัสประเภทของขนาดแพ็ค</span><span class="sxs-lookup"><span data-stu-id="f7994-119">Pack size category ID</span></span>
- <span data-ttu-id="f7994-120">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7994-120">Item number</span></span>
- <span data-ttu-id="f7994-121">หน่วย</span><span class="sxs-lookup"><span data-stu-id="f7994-121">Unit</span></span>

> [!NOTE]
> <span data-ttu-id="f7994-122">คุณไม่จำเป็นต้องกำหนดค่า **ต่อหน่วย** สำหรับเรกคอร์ดขีดจำกัดการเก็บสต็อกในสถานที่แต่ละเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="f7994-122">You don't have to define a **Unit** value for each location stocking limit record.</span></span> <span data-ttu-id="f7994-123">การคำนวณความจุสถานที่จะขึ้นอยู่กับปริมาณของหน่วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f7994-123">The location capacity calculations will be based on the inventory unit quantities.</span></span> <span data-ttu-id="f7994-124">ถ้าไม่มีการแปลงหน่วยที่กำหนดไว้สำหรับค่าที่ใช้อยู่ จะมีการข้ามเรกคอร์ดที่กำหนดให้กับขีดจำกัดการเก็บสต็อกในสถานที่ เนื่องจากมีการกำหนดค่า **หมายเลขสินค้า** อื่นไว้</span><span class="sxs-lookup"><span data-stu-id="f7994-124">If no unit conversion is defined for a value that is used, the location stocking limit record will be skipped, as if another **Item number** value is defined for it.</span></span>

## <a name="example--purchase-order-receiving"></a><span data-ttu-id="f7994-125">ตัวอย่าง – การรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f7994-125">Example – Purchase order receiving</span></span>

<span data-ttu-id="f7994-126">ตัวอย่างนี้ขึ้นอยู่กับชุดข้อมูลสาธิต *USMF* ที่มีการตั้งค่าต่อไปนี้บนแท็บ **ผลิตภัณฑ์ย่อย** ของหน้า **ขีดจำกัดการเก็บสต็อกในสถานที่**</span><span class="sxs-lookup"><span data-stu-id="f7994-126">This example is based on a clean *USMF* demo data set, where the following values are set on the **Product variants** tab of the **Location stocking limits** page.</span></span>

| <span data-ttu-id="f7994-127">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7994-127">Warehouse</span></span> | <span data-ttu-id="f7994-128">รหัสโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="f7994-128">Location profile ID</span></span> | <span data-ttu-id="f7994-129">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7994-129">Item number</span></span> | <span data-ttu-id="f7994-130">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f7994-130">Size</span></span> | <span data-ttu-id="f7994-131">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="f7994-131">Quantity</span></span> | <span data-ttu-id="f7994-132">หน่วย</span><span class="sxs-lookup"><span data-stu-id="f7994-132">Unit</span></span> |
|-----------|---------------------|-------------|------|----------|------|
| <span data-ttu-id="f7994-133">24</span><span class="sxs-lookup"><span data-stu-id="f7994-133">24</span></span>        | <span data-ttu-id="f7994-134">ชั้น</span><span class="sxs-lookup"><span data-stu-id="f7994-134">FLOOR</span></span>               | <span data-ttu-id="f7994-135">D0013</span><span class="sxs-lookup"><span data-stu-id="f7994-135">D0013</span></span>       | <span data-ttu-id="f7994-136">จ.</span><span class="sxs-lookup"><span data-stu-id="f7994-136">M</span></span>    | <span data-ttu-id="f7994-137">300</span><span class="sxs-lookup"><span data-stu-id="f7994-137">300</span></span>      | <span data-ttu-id="f7994-138">Ea</span><span class="sxs-lookup"><span data-stu-id="f7994-138">Ea</span></span>   |
| <span data-ttu-id="f7994-139">24</span><span class="sxs-lookup"><span data-stu-id="f7994-139">24</span></span>        | <span data-ttu-id="f7994-140">ชั้น</span><span class="sxs-lookup"><span data-stu-id="f7994-140">FLOOR</span></span>               | <span data-ttu-id="f7994-141">D0013</span><span class="sxs-lookup"><span data-stu-id="f7994-141">D0013</span></span>       | <span data-ttu-id="f7994-142">L</span><span class="sxs-lookup"><span data-stu-id="f7994-142">L</span></span>    | <span data-ttu-id="f7994-143">240</span><span class="sxs-lookup"><span data-stu-id="f7994-143">240</span></span>      | <span data-ttu-id="f7994-144">Ea</span><span class="sxs-lookup"><span data-stu-id="f7994-144">Ea</span></span>   |
| <span data-ttu-id="f7994-145">24</span><span class="sxs-lookup"><span data-stu-id="f7994-145">24</span></span>        | <span data-ttu-id="f7994-146">ชั้น</span><span class="sxs-lookup"><span data-stu-id="f7994-146">FLOOR</span></span>               | <span data-ttu-id="f7994-147">D0013</span><span class="sxs-lookup"><span data-stu-id="f7994-147">D0013</span></span>       | <span data-ttu-id="f7994-148">ส.</span><span class="sxs-lookup"><span data-stu-id="f7994-148">S</span></span>    | <span data-ttu-id="f7994-149">360</span><span class="sxs-lookup"><span data-stu-id="f7994-149">360</span></span>      | <span data-ttu-id="f7994-150">Ea</span><span class="sxs-lookup"><span data-stu-id="f7994-150">Ea</span></span>   |

<span data-ttu-id="f7994-151">มีการตั้งค่าผลิตภัณฑ์ย่อยของหน่วยวัดต่าง ๆ สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f7994-151">Different unit of measure product variants are set up for the products.</span></span> <span data-ttu-id="f7994-152">ผลิตภัณฑ์ย่อยเหล่านี้จะสอดคล้องกับขีดจำกัดการเก็บสต็อกในสถานที่สำหรับแท่นวางสินค้าสามแท่น (PL):</span><span class="sxs-lookup"><span data-stu-id="f7994-152">These variants are aligned with the location stocking limits for three pallets (PL):</span></span>

- <span data-ttu-id="f7994-153">**ขนาด M:** 1 PL = แต่ละ 100 (Ea)</span><span class="sxs-lookup"><span data-stu-id="f7994-153">**Size M:** 1 PL = 100 each (Ea)</span></span>
- <span data-ttu-id="f7994-154">**ขนาด L:** 1 PL = 80 Ea</span><span class="sxs-lookup"><span data-stu-id="f7994-154">**Size L:** 1 PL = 80 Ea</span></span>
- <span data-ttu-id="f7994-155">**ขนาด S:** 1 PL = 120 Ea</span><span class="sxs-lookup"><span data-stu-id="f7994-155">**Size S:** 1 PL = 120 Ea</span></span>

<span data-ttu-id="f7994-156">แต่ละสถานที่ที่มีการตั้งค่า **รหัสโพรไฟล์ของสถานที่เก็บ** เป็น *ชั้น* อาจมีการดำเนินการ *3* *PL* ของหมายเลขสินค้า *D0013*</span><span class="sxs-lookup"><span data-stu-id="f7994-156">Therefore, each location where the **Location profile ID** value is set to *FLOOR* can carry *3* *PL* of item number *D0013*.</span></span>

### <a name="prepare-for-the-example"></a><span data-ttu-id="f7994-157">จัดเตรียมสำหรับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f7994-157">Prepare for the example</span></span>

<span data-ttu-id="f7994-158">ในตัวอย่างนี้ คุณจะรันขั้นตอนการรับใบสั่งซื้อสำหรับสองบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f7994-158">In this example, you will run a purchase order receiving flow for two lines.</span></span> <span data-ttu-id="f7994-159">อย่างไรก็ตาม คุณต้องอัพเดตข้อมูลการสาธิตอย่างใดอย่างหนึ่งต่อไปนี้เพื่อให้แน่ใจว่าที่ตั้งจะอนุญาตให้มีการจัดเก็บสินค้าผสมที่สถานที่เก็บสินค้าที่ว่างเปล่า ใช้ *fl-002* ถึง *fl-004* เท่านั้น และไม่มีงานที่เปิดขาเข้า</span><span class="sxs-lookup"><span data-stu-id="f7994-159">However, you must first update the demo data in the following way to ensure that the locations allow mixed items to be carried, only the empty locations *FL-002* through *FL-004* are used, and there is no open inbound work.</span></span>

1. <span data-ttu-id="f7994-160">สำหรับที่ตั้ง *FL-001* ให้เปลี่ยนค่าของฟิลด์ **โพรไฟล์สถานที่** จาก *ชั้น* ไปยัง *ชั้น-05*</span><span class="sxs-lookup"><span data-stu-id="f7994-160">For location *FL-001*, change the value of the **Location profile** field from *FLOOR* to *FLOOR-05*.</span></span>
1. <span data-ttu-id="f7994-161">สำหรับโพรไฟล์สถานที่ *ชั้น* ให้ตั้งค่าตัวเลือก **อนุญาตให้ผสมสินค้า** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="f7994-161">For the *FLOOR* location profile, set the **Allow mixed items** option to *Yes*.</span></span>
1. <span data-ttu-id="f7994-162">สร้างใบสั่งซื้อที่มีสองรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f7994-162">Create a purchase order that has the following two lines.</span></span>

    | <span data-ttu-id="f7994-163">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7994-163">Warehouse</span></span> | <span data-ttu-id="f7994-164">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="f7994-164">Item number</span></span> | <span data-ttu-id="f7994-165">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f7994-165">Size</span></span> | <span data-ttu-id="f7994-166">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="f7994-166">Quantity</span></span> | <span data-ttu-id="f7994-167">หน่วย</span><span class="sxs-lookup"><span data-stu-id="f7994-167">Unit</span></span> |
    |-----------|-------------|------|----------|------|
    | <span data-ttu-id="f7994-168">24</span><span class="sxs-lookup"><span data-stu-id="f7994-168">24</span></span>        | <span data-ttu-id="f7994-169">D0013</span><span class="sxs-lookup"><span data-stu-id="f7994-169">D0013</span></span>       | <span data-ttu-id="f7994-170">ส.</span><span class="sxs-lookup"><span data-stu-id="f7994-170">S</span></span>    | <span data-ttu-id="f7994-171">4</span><span class="sxs-lookup"><span data-stu-id="f7994-171">4</span></span>        | <span data-ttu-id="f7994-172">PL</span><span class="sxs-lookup"><span data-stu-id="f7994-172">PL</span></span>   |
    | <span data-ttu-id="f7994-173">24</span><span class="sxs-lookup"><span data-stu-id="f7994-173">24</span></span>        | <span data-ttu-id="f7994-174">D0013</span><span class="sxs-lookup"><span data-stu-id="f7994-174">D0013</span></span>       | <span data-ttu-id="f7994-175">L</span><span class="sxs-lookup"><span data-stu-id="f7994-175">L</span></span>    | <span data-ttu-id="f7994-176">4</span><span class="sxs-lookup"><span data-stu-id="f7994-176">4</span></span>        | <span data-ttu-id="f7994-177">PL</span><span class="sxs-lookup"><span data-stu-id="f7994-177">PL</span></span>   |

### <a name="process-the-example"></a><span data-ttu-id="f7994-178">ประมวลผลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f7994-178">Process the example</span></span>

<span data-ttu-id="f7994-179">อย่างแรกคุณจะได้รับปริมาณของ *4* ของหน่วย *PL* ในขนาด *S* และตรวจสอบที่ตั้งของรายการที่วางสำหรับงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f7994-179">You will first receive a quantity of *4* of unit *PL* in size *S*, and review the put line locations for the work that is created.</span></span> <span data-ttu-id="f7994-180">คุณจะได้รับปริมาณของ *4* ของหน่วย *PL* ในขนาด *L* และตรวจสอบที่ตั้งของรายการที่วางสำหรับงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f7994-180">You will then receive a quantity of *4* of unit *PL* in size *L*, and review the put line locations for the work that is created.</span></span>

1. <span data-ttu-id="f7994-181">ในแอปคลังสินค้า ให้ลงชื่อเข้าใช้โดยใช้ *24* เป็นรหัสผู้ใช้ และ *1* เป็นรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="f7994-181">In the warehouse app, sign in by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="f7994-182">เลือก **ขาเข้า** \> **รับการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="f7994-182">Select **Inbound** \> **Purchase Receive**.</span></span>
1. <span data-ttu-id="f7994-183">รับ *4* *PL* หมายเลขสินค้า *D0013* ในขนาด *S*</span><span class="sxs-lookup"><span data-stu-id="f7994-183">Receive *4* *PL* of item number *D0013* in size *S*.</span></span>
1. <span data-ttu-id="f7994-184">ตรวจทานงานการสำรองที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f7994-184">Review the putaway work that was created.</span></span> <span data-ttu-id="f7994-185">คุณควรเห็นผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f7994-185">You should see the following result:</span></span>

    - <span data-ttu-id="f7994-186">3 PL -\> FL-002</span><span class="sxs-lookup"><span data-stu-id="f7994-186">3 PL -\> FL-002</span></span>
    - <span data-ttu-id="f7994-187">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="f7994-187">1 PL -\> FL-003</span></span>

1. <span data-ttu-id="f7994-188">รับ *4* *PL* หมายเลขสินค้า *D0013* ในขนาด *L*</span><span class="sxs-lookup"><span data-stu-id="f7994-188">Receive *4* *PL* of item number *D0013* in size *L*.</span></span>
1. <span data-ttu-id="f7994-189">ตรวจทานงานการสำรองที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f7994-189">Review the putaway work that was created.</span></span> <span data-ttu-id="f7994-190">คุณควรเห็นผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f7994-190">You should see the following result:</span></span>

    - <span data-ttu-id="f7994-191">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="f7994-191">1 PL -\> FL-003</span></span>
    - <span data-ttu-id="f7994-192">3 PL -\> FL-004</span><span class="sxs-lookup"><span data-stu-id="f7994-192">3 PL -\> FL-004</span></span>

<span data-ttu-id="f7994-193">ขึ้นอยู่กับผลลัพธ์ คุณอาจสรุปได้ว่าระบบล้มเหลวในการปันส่วนที่ตั้งการสำรองที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f7994-193">Based on the results, you might conclude that the system failed to allocate the correct putaway locations.</span></span> <span data-ttu-id="f7994-194">มิฉะนั้น เหตุใดระบบจึงเพิ่มเพียง *1* *PL* ของขนาด *L* ไปยังสถานที่ *FL-003* ในขั้นตอนสุดท้ายไม่ใช่ *2* *PL*</span><span class="sxs-lookup"><span data-stu-id="f7994-194">Otherwise, why did the system add only *1* *PL* of size *L* to location *FL-003* in the last step, not *2* *PL*?</span></span> <span data-ttu-id="f7994-195">นั่นคือ เพราะเหตุใดจึงไม่มีทั้งหมด *3* *PL* สำหรับการสำรองไปสถานที่นั้น</span><span class="sxs-lookup"><span data-stu-id="f7994-195">That is, why isn't there is a total of *3* *PL* for putaway to that location?</span></span>

<span data-ttu-id="f7994-196">เมื่อต้องการอธิบายความล้มเหลวที่ชัดเจนนี้ คุณต้องเข้าใจเงื่อนไขการเลือกสำหรับขีดจำกัดการเก็บสต็อกในสถานที่</span><span class="sxs-lookup"><span data-stu-id="f7994-196">To explain this apparent failure, you must understand the selection criteria for the location stocking limits.</span></span> <span data-ttu-id="f7994-197">รบบเลือกเรกคอร์ดการจับคู่ที่มีรายละเอียดมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="f7994-197">The system selects the most detailed matching record.</span></span> <span data-ttu-id="f7994-198">ในตัวอย่างนี้ เรกคอร์ดการจับคู่ที่มีรายละเอียดมากที่สุดคือบรรทัดที่มีค่า **ขนาด** เป็น *L* ค่า **ปริมาณ** คือ *240* และค่า **ต่อหน่วย** คือ *Ea*</span><span class="sxs-lookup"><span data-stu-id="f7994-198">In this example, the most detailed matching record is the line where the **Size** value is *L*, the **Quantity** value is *240*, and the **Unit** value is *Ea*.</span></span> <span data-ttu-id="f7994-199">เนื่องจากคุณมีงานที่เปิดค้างไว้ตั้งแต่การรับสินค้าก่อนหน้านี้ของปริมาณ *120* *Ea* ขนาด *S* ความจุที่เหลือจะคำนวณเป็น *240* – *120* = *120* *Ea*</span><span class="sxs-lookup"><span data-stu-id="f7994-199">Because you already have open work from the previous receipt of a quantity of *120* *Ea* of size *S*, the remaining capacity is calculated as *240* – *120* = *120* *Ea*.</span></span> <span data-ttu-id="f7994-200">ดังนั้น ความจุที่เหลือสามารถดำเนินการเพียง *1* *PL* ของ *80* *Ea*</span><span class="sxs-lookup"><span data-stu-id="f7994-200">Therefore, the remaining capacity can carry only *1* *PL* of *80* *Ea*.</span></span>

> [!NOTE]
> <span data-ttu-id="f7994-201">คุณไม่สามารถใช้ขีดจำกัดการเก็บสต็อกในสถานที่ในการควบคุม ตัวอย่างเช่น การเติมสินค้าที่มีปริมาณที่แตกต่างกันในสถานที่เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f7994-201">You can't use location stocking limits to control, for example, the replenishment of items that have different quantities in the same location.</span></span> <span data-ttu-id="f7994-202">ในกรณีนี้ ให้ใช้ *แม่แบบการเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f7994-202">In this case, use a *replenishment template*.</span></span>
