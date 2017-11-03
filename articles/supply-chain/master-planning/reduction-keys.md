---
title: "คีย์การลด"
description: "บทความนี้แสดงตัวอย่างที่แสดงวิธีการตั้งค่าเงื่อนไขสำคัญของการลด โดยมีข้อมูลเกี่ยวกับการตั้งค่าเงื่อนไขสำคัญของการลดต่างๆ และผลลัพธ์แต่ละครั้ง คุณสามารถใช้เงื่อนไขสำคัญของการลดเพื่อกำหนดวิธีการลดความต้องการการคาดการณ์"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 506ca3aac7ad271ca7472f3b74627e94d97a74ee
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="524cc-105">คีย์การลด</span><span class="sxs-lookup"><span data-stu-id="524cc-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="524cc-106">บทความนี้แสดงตัวอย่างที่แสดงวิธีการตั้งค่าเงื่อนไขสำคัญของการลด</span><span class="sxs-lookup"><span data-stu-id="524cc-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="524cc-107">โดยมีข้อมูลเกี่ยวกับการตั้งค่าเงื่อนไขสำคัญของการลดต่างๆ และผลลัพธ์แต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="524cc-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="524cc-108">คุณสามารถใช้เงื่อนไขสำคัญของการลดเพื่อกำหนดวิธีการลดความต้องการการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="524cc-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="524cc-109">ตัวอย่างที่ 1: เปอร์เซ็นต์ - คีย์การลดคาดการณ์หลักการลด</span><span class="sxs-lookup"><span data-stu-id="524cc-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="524cc-110">ตัวอย่างนี้แสดงว่าคีย์การลดช่วยลดข้อกำหนดของการคาดการณ์ความต้องการตามเปอร์เซ็นต์และรอบระยะเวลาที่กำหนดโดยคีย์การลด</span><span class="sxs-lookup"><span data-stu-id="524cc-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="524cc-111">ในหน้า **คีย์การลด** ตั้งค่าบรรทัดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="524cc-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="524cc-112">เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="524cc-112">Change</span></span> | <span data-ttu-id="524cc-113">หน่วย</span><span class="sxs-lookup"><span data-stu-id="524cc-113">Unit</span></span>  | <span data-ttu-id="524cc-114">เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="524cc-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="524cc-115">1</span><span class="sxs-lookup"><span data-stu-id="524cc-115">1</span></span>      | <span data-ttu-id="524cc-116">เดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-116">Month</span></span> | <span data-ttu-id="524cc-117">100</span><span class="sxs-lookup"><span data-stu-id="524cc-117">100</span></span>     |
    | <span data-ttu-id="524cc-118">2</span><span class="sxs-lookup"><span data-stu-id="524cc-118">2</span></span>      | <span data-ttu-id="524cc-119">เดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-119">Month</span></span> | <span data-ttu-id="524cc-120">75</span><span class="sxs-lookup"><span data-stu-id="524cc-120">75</span></span>      |
    | <span data-ttu-id="524cc-121">3</span><span class="sxs-lookup"><span data-stu-id="524cc-121">3</span></span>      | <span data-ttu-id="524cc-122">เดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-122">Month</span></span> | <span data-ttu-id="524cc-123">50</span><span class="sxs-lookup"><span data-stu-id="524cc-123">50</span></span>      |
    | <span data-ttu-id="524cc-124">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="524cc-124">4</span></span>      | <span data-ttu-id="524cc-125">เดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-125">Month</span></span> | <span data-ttu-id="524cc-126">25</span><span class="sxs-lookup"><span data-stu-id="524cc-126">25</span></span>      |

2.  <span data-ttu-id="524cc-127">เชื่อมโยงคีย์การลดกับกลุ่มความครอบคลุมของสินค้า</span><span class="sxs-lookup"><span data-stu-id="524cc-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="524cc-128">บนหน้า **แผนหลัก** ในฟิลด์ **หลักการลด** เลือก **เปอร์เซ็นต์ - คีย์การลด**</span><span class="sxs-lookup"><span data-stu-id="524cc-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="524cc-129">สร้างการคาดการณ์ความต้องการของ 1,000 ชิ้นต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="524cc-130">ถ้าคุณรันการจัดกำหนดการการคาดการณ์ในวันที่ 1 มกราคม ข้อกำหนดการคาดการณ์ความต้องการจะถูกใช้ตามเปอร์เซ็นต์ที่คุณตั้งค่าในหน้า **คีย์การลด**</span><span class="sxs-lookup"><span data-stu-id="524cc-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="524cc-131">ปริมาณข้อกำหนดต่อไปนี้จะถูกโอนย้ายไปยังแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="524cc-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="524cc-132">เดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-132">Month</span></span>                | <span data-ttu-id="524cc-133">จำนวนชิ้นที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="524cc-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="524cc-134">มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-134">January</span></span>              | <span data-ttu-id="524cc-135">0</span><span class="sxs-lookup"><span data-stu-id="524cc-135">0</span></span>                         |
| <span data-ttu-id="524cc-136">กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="524cc-136">February</span></span>             | <span data-ttu-id="524cc-137">250</span><span class="sxs-lookup"><span data-stu-id="524cc-137">250</span></span>                       |
| <span data-ttu-id="524cc-138">มีนาคม</span><span class="sxs-lookup"><span data-stu-id="524cc-138">March</span></span>                | <span data-ttu-id="524cc-139">500</span><span class="sxs-lookup"><span data-stu-id="524cc-139">500</span></span>                       |
| <span data-ttu-id="524cc-140">เมษายน</span><span class="sxs-lookup"><span data-stu-id="524cc-140">April</span></span>                | <span data-ttu-id="524cc-141">750</span><span class="sxs-lookup"><span data-stu-id="524cc-141">750</span></span>                       |
| <span data-ttu-id="524cc-142">พฤษภาคม - ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="524cc-142">May through December</span></span> | <span data-ttu-id="524cc-143">1,000</span><span class="sxs-lookup"><span data-stu-id="524cc-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="524cc-144">ตัวอย่างที่ 2: ธุรกรรม คีย์การลดคาดการณ์หลักการลด</span><span class="sxs-lookup"><span data-stu-id="524cc-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="524cc-145">ตัวอย่างนี้แสดงว่าใบสั่งจริงที่เกิดขึ้นระหว่างรอบระยะเวลาที่ถูกกำหนดโดยคีย์การลดช่วยลดข้อกำหนดการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="524cc-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="524cc-146">บนหน้า **แผนหลัก** ในฟิลด์ **หลักการลด** เลือก **ธุรกรรม - คีย์การลด**</span><span class="sxs-lookup"><span data-stu-id="524cc-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="524cc-147">ใบสั่งขายต่อไปนี้มีอยู่ในวันที่ 1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="524cc-148">เดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-148">Month</span></span>    | <span data-ttu-id="524cc-149">จำนวนชิ้นที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="524cc-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="524cc-150">มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-150">January</span></span>  | <span data-ttu-id="524cc-151">956</span><span class="sxs-lookup"><span data-stu-id="524cc-151">956</span></span>                      |
| <span data-ttu-id="524cc-152">กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="524cc-152">February</span></span> | <span data-ttu-id="524cc-153">1,176</span><span class="sxs-lookup"><span data-stu-id="524cc-153">1,176</span></span>                    |
| <span data-ttu-id="524cc-154">มีนาคม</span><span class="sxs-lookup"><span data-stu-id="524cc-154">March</span></span>    | <span data-ttu-id="524cc-155">451</span><span class="sxs-lookup"><span data-stu-id="524cc-155">451</span></span>                      |
| <span data-ttu-id="524cc-156">เมษายน</span><span class="sxs-lookup"><span data-stu-id="524cc-156">April</span></span>    | <span data-ttu-id="524cc-157">119</span><span class="sxs-lookup"><span data-stu-id="524cc-157">119</span></span>                      |

<span data-ttu-id="524cc-158">ถ้าคุณใช้การคาดการณ์ความต้องการเดียวกันที่ 1,000 ชิ้นต่อเดือน ปริมาณความต้องการต่อไปนี้จะถูกโอนย้ายไปยังแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="524cc-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="524cc-159">เดือน</span><span class="sxs-lookup"><span data-stu-id="524cc-159">Month</span></span>                | <span data-ttu-id="524cc-160">จำนวนชิ้นที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="524cc-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="524cc-161">มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-161">January</span></span>              | <span data-ttu-id="524cc-162">44</span><span class="sxs-lookup"><span data-stu-id="524cc-162">44</span></span>                        |
| <span data-ttu-id="524cc-163">กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="524cc-163">February</span></span>             | <span data-ttu-id="524cc-164">0</span><span class="sxs-lookup"><span data-stu-id="524cc-164">0</span></span>                         |
| <span data-ttu-id="524cc-165">มีนาคม</span><span class="sxs-lookup"><span data-stu-id="524cc-165">March</span></span>                | <span data-ttu-id="524cc-166">549</span><span class="sxs-lookup"><span data-stu-id="524cc-166">549</span></span>                       |
| <span data-ttu-id="524cc-167">เมษายน</span><span class="sxs-lookup"><span data-stu-id="524cc-167">April</span></span>                | <span data-ttu-id="524cc-168">881</span><span class="sxs-lookup"><span data-stu-id="524cc-168">881</span></span>                       |
| <span data-ttu-id="524cc-169">พฤษภาคม - ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="524cc-169">May through December</span></span> | <span data-ttu-id="524cc-170">1,000</span><span class="sxs-lookup"><span data-stu-id="524cc-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="524cc-171">ตัวอย่างที่ 3: ธุรกรรม รอบระยะเวลาแบบไดนามิกคาดการณ์หลักการลด</span><span class="sxs-lookup"><span data-stu-id="524cc-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="524cc-172">ในกรณีส่วนใหญ่ ระบบจะตั้งค่าเพื่อให้ธุรกรรมลดความต้องการการคาดการณ์ภายในรอบระยะเวลาการคาดการณ์ที่กำหนด: สัปดาห์ เดือน เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="524cc-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="524cc-173">รอบระยะเวลาเหล่านี้จะถูกกำหนดอยู่ในคีย์การลด</span><span class="sxs-lookup"><span data-stu-id="524cc-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="524cc-174">อย่างไรก็ตาม เวลาระหว่างสองรายการการคาดการณ์ความต้องการสามารถ *บ่งบอก* รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="524cc-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="524cc-175">สร้างการคาดการณ์ความต้องการสำหรับวันต่อไปนี้และปริมาณการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="524cc-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="524cc-176">วันที่</span><span class="sxs-lookup"><span data-stu-id="524cc-176">Date</span></span>       | <span data-ttu-id="524cc-177">การคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="524cc-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="524cc-178">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-178">January 1</span></span>  | <span data-ttu-id="524cc-179">1,000</span><span class="sxs-lookup"><span data-stu-id="524cc-179">1,000</span></span>           |
    | <span data-ttu-id="524cc-180">5 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-180">January 5</span></span>  | <span data-ttu-id="524cc-181">500</span><span class="sxs-lookup"><span data-stu-id="524cc-181">500</span></span>             |
    | <span data-ttu-id="524cc-182">12 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-182">January 12</span></span> | <span data-ttu-id="524cc-183">1,000</span><span class="sxs-lookup"><span data-stu-id="524cc-183">1,000</span></span>           |

    <span data-ttu-id="524cc-184">ในการคาดการณ์นี้ ไม่มีรอบระยะเวลาที่ชัดเจนระหว่างวันคาดการณ์: ระหว่างวันที่หนึ่ง และวันที่สอง มีช่วงสี่วัน และระหว่างวันที่สอง และวันที่สาม มีช่วงเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="524cc-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="524cc-185">ระยะเวลาต่างๆเหล่านี้คือรอบระยะเวลาแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="524cc-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="524cc-186">สร้างรายการใบสั่งขายดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="524cc-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="524cc-187">วันที่</span><span class="sxs-lookup"><span data-stu-id="524cc-187">Date</span></span>                             | <span data-ttu-id="524cc-188">ปริมาณในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="524cc-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="524cc-189">15 ธันวาคมในปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="524cc-189">December 15 in the previous year</span></span> | <span data-ttu-id="524cc-190">500</span><span class="sxs-lookup"><span data-stu-id="524cc-190">500</span></span>                  |
    | <span data-ttu-id="524cc-191">3 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-191">January 3</span></span>                        | <span data-ttu-id="524cc-192">100</span><span class="sxs-lookup"><span data-stu-id="524cc-192">100</span></span>                  |
    | <span data-ttu-id="524cc-193">10 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-193">January 10</span></span>                       | <span data-ttu-id="524cc-194">200</span><span class="sxs-lookup"><span data-stu-id="524cc-194">200</span></span>                  |

<span data-ttu-id="524cc-195">การคาดการณ์จะถูกลดลงดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="524cc-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="524cc-196">ใบสั่งขายแรกไม่อยู่ภายในรอบระยะเวลา ดังนั้นจึงไม่สามารถลดการคาดการณ์ใด ๆ</span><span class="sxs-lookup"><span data-stu-id="524cc-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="524cc-197">ใบสั่งขายที่สองอยู่ระหว่าง 1 มกราคมและ 5 มกราคม ดังนั้นจึงจะลดการคาดการณ์สำหรับวันที่ 1 มกราคม ไป 100</span><span class="sxs-lookup"><span data-stu-id="524cc-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="524cc-198">ใบสั่งขายที่สามอยู่ระหว่าง 5 มกราคมและ 12 มกราคม ดังนั้นจึงจะลดการคาดการณ์สำหรับวันที่ 5 มกราคม ไป 200</span><span class="sxs-lookup"><span data-stu-id="524cc-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="524cc-199">ใบสั่งที่ได้วางแผนไว้ต่อไปนี้จะถูกสร้างเพื่อตอบสนองการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="524cc-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="524cc-200">วันที่การคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="524cc-200">Demand forecast date</span></span> | <span data-ttu-id="524cc-201">ลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="524cc-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="524cc-202">1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-202">January 1</span></span>            | <span data-ttu-id="524cc-203">900</span><span class="sxs-lookup"><span data-stu-id="524cc-203">900</span></span>              |
| <span data-ttu-id="524cc-204">5 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-204">January 5</span></span>            | <span data-ttu-id="524cc-205">300</span><span class="sxs-lookup"><span data-stu-id="524cc-205">300</span></span>              |
| <span data-ttu-id="524cc-206">12 มกราคม</span><span class="sxs-lookup"><span data-stu-id="524cc-206">January 12</span></span>           | <span data-ttu-id="524cc-207">1,000</span><span class="sxs-lookup"><span data-stu-id="524cc-207">1,000</span></span>            |

<span data-ttu-id="524cc-208">นี่คือสรุปของการลด **ธุรกรรม - รอบระยะเวลาแบบไดนามิก** :</span><span class="sxs-lookup"><span data-stu-id="524cc-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="524cc-209">ความต้องการการคาดการณ์จะลดลงตามธุรกรรมใบสั่งจริงที่เกิดขึ้นในระหว่างรอบระยะเวลาแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="524cc-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="524cc-210">รอบระยะเวลาแบบไดนามิกครอบคลุมวันการคาดการณ์ปัจจุบัน และสิ้นสุดที่จุดเริ่มต้นของการคาดการณ์ถัดไป</span><span class="sxs-lookup"><span data-stu-id="524cc-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="524cc-211">วิธีการนี้ไม่ใช้หรือต้องมีคีย์การลด</span><span class="sxs-lookup"><span data-stu-id="524cc-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="524cc-212">เมื่อใช้ตัวเลือกนี้ ลักษณะการทำงานต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="524cc-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="524cc-213">ถ้าการคาดการณ์ถูกลดลงโดยสมบูรณ์ ข้อกำหนดการคาดการณ์สำหรับการคาดการณ์ปัจจุบันจะกลายเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="524cc-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="524cc-214">ถ้าไม่มีการคาดการณ์ในอนาคต ข้อกำหนดการคาดการณ์จากการคาดการณ์ครั้งสุดท้ายที่ป้อนจะลดลง</span><span class="sxs-lookup"><span data-stu-id="524cc-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="524cc-215">กรอบเวลาจะรวมอยู่ในการคำนวณการลดการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="524cc-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="524cc-216">จำนวนวันค่าบวกจะรวมอยู่ในการคำนวณการลดการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="524cc-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="524cc-217">ถ้าธุรกรรมใบสั่งจริงเกินกว่าข้อกำหนดความคาดการณ์ ธุรกรรมที่เหลือจะไม่ถูกส่งต่อถึงรอบระยะเวลาการคาดการณ์ถัดไป</span><span class="sxs-lookup"><span data-stu-id="524cc-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="524cc-218">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="524cc-218">See also</span></span>
--------

[<span data-ttu-id="524cc-219">แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="524cc-219">Master plans</span></span>](master-plans.md)




