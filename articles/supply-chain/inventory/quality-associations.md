---
title: การเชื่อมโยงคุณภาพ
description: หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถใช้การเชื่อมโยงคุณภาพใน Microsoft Dynamics 365 Supply Chain Management เพื่อสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับกระบวนการผลิตการขาย การซื้อ และกระบวนการผลิตของคุณโดยอัตโนมัติ
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956846"
---
# <a name="quality-associations"></a><span data-ttu-id="88e44-103">การเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88e44-104">หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถใช้การเชื่อมโยงคุณภาพใน Microsoft Dynamics 365 Supply Chain Management เพื่อสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับกระบวนการผลิตการขาย การซื้อ และกระบวนการผลิตของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="88e44-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="88e44-105">ความสัมพันธ์ของคุณภาพกำหนดข้อมูลต่อไปนี้ทั้งหมดสำหรับใบสั่งตรวจสอบคุณภาพที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="88e44-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="88e44-106">เหตุการณ์ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="88e44-106">The transaction event</span></span>
- <span data-ttu-id="88e44-107">ชุดของการทดสอบที่ต้องดำเนินการบนสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="88e44-108">ระดับคุณภาพที่ยอมรับได้ (AQL)</span><span class="sxs-lookup"><span data-stu-id="88e44-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="88e44-109">แผนการสุ่มตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="88e44-109">The sampling plan</span></span>

<span data-ttu-id="88e44-110">คุณต้องกำหนดคำความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจที่จำเป็นต้องมีการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="88e44-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="88e44-111">ตัวอย่างเช่น สามารถสร้างใบสั่งตรวจสอบคุณภาพในกระบวนการทางธุรกิจสำหรับใบสั่งซื้อ ใบสั่งตรวจสอบสินค้า ใบสั่งขาย และใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="88e44-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="88e44-112">การทำงานกับการเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-112">Working with quality associations</span></span>

<span data-ttu-id="88e44-113">กระบวนการทางธุรกิจที่ใช้การเชื่อมโยงคุณภาพอาจเกี่ยวข้องกับเอกสารต้นทางต่าง ๆ เช่นใบสั่งซื้อ ใบสั่งขาย หรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="88e44-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="88e44-114">แต่ละเรกคอร์ดความสัมพันธ์ของคุณภาพกำหนดชุดของการทดสอบ AQL และแผนการสุ่มตัวอย่างที่ใช้กับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="88e44-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="88e44-115">คุณต้องกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="88e44-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="88e44-116">ตัวอย่างเช่น คุณสามารถตั้งค่าการเชื่อมโยงคุณภาพที่สร้างใบสั่งตรวจสอบคุณภาพเมื่อมีการอัพเดตใบรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="88e44-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="88e44-117">ทั้งนี้ขึ้นอยู่กับการตั้งค่าของแผนปฏิบัติการ คุณสามารถบล็อคกระบวนการทริกเกอร์ได้เองในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="88e44-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="88e44-118">หรือกระบวนการต่อมา เช่น การออกใบแจ้งหนี้ใบสั่งซื้อ สามารถบล็อคได้</span><span class="sxs-lookup"><span data-stu-id="88e44-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="88e44-119">ในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ ปริมาณสินค้าคงคลังจะถูกถูกบล็อคจากการออกใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="88e44-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="88e44-120">ขึ้นอยู่กับการตั้งค่าฟิลด์ **การบล็อคทั้งหมด** บนหน้า **การสุ่มตัวอย่างสินค้า** ปริมาณเป็นปริมาณในใบสั่งตรวจสอบคุณภาพ หรือปริมาณในรายการเอกสารต้นทาง</span><span class="sxs-lookup"><span data-stu-id="88e44-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="88e44-121">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การสุ่มตัวอย่างสินค้าการจัดการคุณภาพ](quality-item-sampling.md)</span><span class="sxs-lookup"><span data-stu-id="88e44-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="88e44-122">สำหรับกระบวนการทางธุรกิจที่ระบุ เรกคอร์ดความสัมพันธ์ของคุณภาพจะระบุเหตุการณ์และเงื่อนไขที่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="88e44-123">เงื่อนไขอาจเป็นเฉพาะสำหรับไซต์หรือนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="88e44-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="88e44-124">สามารถสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับการทดสอบแบบทำลายเฉพาะเมื่อสินค้าคงคลังคงเหลือที่มีอยู่สำหรับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="88e44-125">เมื่อต้องการใช้งานการเชื่อมโยงคุณภาพ ให้ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> การเชื่อมโยงคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="88e44-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="88e44-126">ตัวอย่างต่อไปนี้อธิบายวิธีกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรในแต่ละกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="88e44-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="88e44-127">สำหรับแต่ละตัวอย่าง ตารางต่อไปนี้สรุปเหตุการณ์และเงื่อนไขที่กำหนดโดยเรกคอร์ดความสัมพันธ์ของคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88e44-128">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="88e44-128">Reference type</span></span></th>
<th><span data-ttu-id="88e44-129">ชนิดเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-129">Event type</span></span></th>
<th><span data-ttu-id="88e44-130">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88e44-130">Execution</span></span></th>
<th><span data-ttu-id="88e44-131">การบล็อคเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-131">Event blocking</span></span></th>
<th><span data-ttu-id="88e44-132">การอ้างอิงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="88e44-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88e44-133">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="88e44-133">Inventory</span></span></td>
<td><span data-ttu-id="88e44-134">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="88e44-134">Not applicable</span></span></td>
<td><span data-ttu-id="88e44-135">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="88e44-135">Not applicable</span></span></td>
<td><span data-ttu-id="88e44-136">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-136">None</span></span></td>
<td><span data-ttu-id="88e44-137">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="88e44-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="88e44-138">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="88e44-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="88e44-139">กระบวนการเบิกสินค้าถูกจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="88e44-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="88e44-140">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-140">Before</span></span></td>
<td><span data-ttu-id="88e44-141">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="88e44-142">รหัส กลุ่ม หรือทั้งหมด เฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="88e44-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-143">กระบวนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-144">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88e44-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-145">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="88e44-146">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88e44-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-147">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-147">Before</span></span></td>
<td><span data-ttu-id="88e44-148">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-149">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88e44-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-150">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="88e44-151">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="88e44-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="88e44-152">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="88e44-153">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-153">Before</span></span></td>
<td><span data-ttu-id="88e44-154">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-155">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-156">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-157">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="88e44-158">หลัง</span><span class="sxs-lookup"><span data-stu-id="88e44-158">After</span></span></td>
<td><span data-ttu-id="88e44-159">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-160">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-161">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="88e44-162">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="88e44-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-163">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="88e44-163">Not applicable</span></span></td>
<td><span data-ttu-id="88e44-164">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-165">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-166">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="88e44-167">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-168">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-168">Before</span></span></td>
<td><span data-ttu-id="88e44-169">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-170">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-171">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="88e44-172">หลัง</span><span class="sxs-lookup"><span data-stu-id="88e44-172">After</span></span></td>
<td><span data-ttu-id="88e44-173">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-174">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="88e44-175">การผลิต</span><span class="sxs-lookup"><span data-stu-id="88e44-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-176">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="88e44-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-177">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="88e44-177">Not applicable</span></span></td>
<td><span data-ttu-id="88e44-178">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="88e44-179">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="88e44-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-180">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-181">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="88e44-182">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-183">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-183">Before</span></span></td>
<td><span data-ttu-id="88e44-184">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-185">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-186">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="88e44-187">หลัง</span><span class="sxs-lookup"><span data-stu-id="88e44-187">After</span></span></td>
<td><span data-ttu-id="88e44-188">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="88e44-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-189">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="88e44-190">การตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-191">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="88e44-192">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-192">Before</span></span></td>
<td><span data-ttu-id="88e44-193">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-194">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-195">หลัง</span><span class="sxs-lookup"><span data-stu-id="88e44-195">After</span></span></td>
<td><span data-ttu-id="88e44-196">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-197">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-197">End</span></span></td>
<td><span data-ttu-id="88e44-198">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-198">Before</span></span></td>
<td><span data-ttu-id="88e44-199">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="88e44-200">ขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="88e44-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-201">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="88e44-202">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-202">Before</span></span></td>
<td><span data-ttu-id="88e44-203">None</span><span class="sxs-lookup"><span data-stu-id="88e44-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-204">รหัส กลุ่ม หรือทั้งหมดเฉพาะ และระบุทรัพยากร กลุ่ม หรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="88e44-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-205">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-206">หลังจาก</span><span class="sxs-lookup"><span data-stu-id="88e44-206">After</span></span></td>
<td><span data-ttu-id="88e44-207">None</span><span class="sxs-lookup"><span data-stu-id="88e44-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="88e44-208">การผลิตสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="88e44-208">Co-product production</span></span></td>
<td><span data-ttu-id="88e44-209">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="88e44-209">Registration</span></span></td>
<td><span data-ttu-id="88e44-210">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="88e44-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-211">None</span><span class="sxs-lookup"><span data-stu-id="88e44-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="88e44-212">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="88e44-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="88e44-213">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88e44-213">Report as finished</span></span></td>
<td><span data-ttu-id="88e44-214">ก่อน</span><span class="sxs-lookup"><span data-stu-id="88e44-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-215">หลังจาก</span><span class="sxs-lookup"><span data-stu-id="88e44-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="88e44-216">คุณลักษณะ *การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า* เพิ่มความสามารถสำหรับการประมวลผลใบสั่งตรวจสอบคุณภาพสำหรับการผลิตที่มีการตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *รายงานการเสร็จงาน* และมีการตั้งค่าฟิลด์ **การดำเนินการ** เป็น *ภายหลัง* และสำหรับการซื้อที่มีการตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *การลงทะเบียน*</span><span class="sxs-lookup"><span data-stu-id="88e44-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="88e44-217">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](quality-management-for-warehouses-processes.md)</span><span class="sxs-lookup"><span data-stu-id="88e44-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="88e44-218">ตารางต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างใบสั่งตรวจสอบคุณภาพสามารถสำหรับชนิดเฉพาะของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="88e44-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="88e44-219">ชนิดของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="88e44-219">Type of process</span></span></th>
<th><span data-ttu-id="88e44-220">เมื่อใบสั่งตรวจสอบคุณภาพสามารถถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="88e44-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="88e44-221">เมื่อใบสั่งตรวจสอบคุณภาพสามารถสร้างหากการทดสอบแบบทำลายจำเป็น</span><span class="sxs-lookup"><span data-stu-id="88e44-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="88e44-222">ข้อมูลเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="88e44-222">Condition information</span></span></th>
<th><span data-ttu-id="88e44-223">ข้อมูลการสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="88e44-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88e44-224">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="88e44-224">Purchase order</span></span></td>
<td><span data-ttu-id="88e44-225">ก่อนหรือหลังรายการรับสินค้าหรือใบรับสินค้าสำหรับวัสดุที่ได้รับจะมีการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="88e44-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="88e44-226">หลังจากใบรับสินค้าสำหรับวัสดุที่ได้รับมีการลงรายการบัญชี เนื่องจากวัสดุต้องพร้อมใช้งานสำหรับการทดสอบแบบทำลาย</span><span class="sxs-lookup"><span data-stu-id="88e44-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="88e44-227">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="88e44-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="88e44-228">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="88e44-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-229">ใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-229">Quarantine order</span></span></td>
<td><span data-ttu-id="88e44-230">ก่อน หรือหลัง ใบสั่งตรวจสอบสินค้ามีการรายงานเสร็จสิ้นแล้วหรือสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="88e44-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="88e44-231">ใบสั่งตรวจสอบคุณภาพที่ต้องการการทดสอบแบบทำลายไม่สามารถที่จะสร้าง</span><span class="sxs-lookup"><span data-stu-id="88e44-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="88e44-232">สมมติว่า ฟังก์ชันใบสั่งตรวจสอบสินค้าจัดการการโอนการครอบครองวัสดุที่ถูกทำลาย</span><span class="sxs-lookup"><span data-stu-id="88e44-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="88e44-233">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="88e44-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="88e44-234">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งตรวจสอบสินค้าสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="88e44-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-235">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="88e44-235">Sales order</span></span></td>
<td><span data-ttu-id="88e44-236">ก่อนการจัดกำหนดการกระบวนการเบิกสินค้าหรืออัพเดตบันทึกสำหรับสินค้าที่กำลังจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="88e44-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="88e44-237">ในขั้นตอนใดๆ</span><span class="sxs-lookup"><span data-stu-id="88e44-237">At any step</span></span></td>
<td><span data-ttu-id="88e44-238">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือลูกค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="88e44-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="88e44-239">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="88e44-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-240">ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="88e44-240">Production order</span></span></td>
<td><span data-ttu-id="88e44-241">ก่อนหรือหลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="88e44-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="88e44-242">หลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="88e44-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="88e44-243">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="88e44-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="88e44-244">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="88e44-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-245">ใบสั่งผลิตที่มีขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="88e44-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="88e44-246">ก่อนหรือหลังจากรายงานการเสร็จสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="88e44-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="88e44-247">หลังจากการรายงานการผลิตเสร็จสิ้นแล้วสำหรับการดำเนินงานสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="88e44-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="88e44-248">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือทรัพยากรการดำเนินงาน หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="88e44-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="88e44-249">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับขั้นตอนของกระบวนการผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="88e44-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88e44-250">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="88e44-250">Inventory</span></span></td>
<td><span data-ttu-id="88e44-251">ใบสั่งตรวจสอบคุณภาพไม่สามารถถูกสร้างขึ้นโดยอัตโนมัติสำหรับธุรกรรมในสมุดรายวันสินค้าคงคลังหรือธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="88e44-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="88e44-252">ใบสั่งคุณภาพต้องถูกสร้างด้วยตนเองสำหรับปริมาณสินค้าคงคลังของสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="88e44-253">จำเป็นต้องมีปริมาณสินค้าคงคลังคงเหลือที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="88e44-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="88e44-254">ตัวอย่างของการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="88e44-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="88e44-255">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="88e44-255">Purchasing</span></span>

<span data-ttu-id="88e44-256">ในการซื้อ หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *ใบรับสินค้า* และฟิลด์ **การดำเนินการ** เป็น *ภายหลัง* บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88e44-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="88e44-257">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ใช่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกการรับสินค้าต่อใบสั่งซื้อ ตามปริมาณที่รับและการตั้งค่าในสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="88e44-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="88e44-258">ทุกครั้งที่มีการรับปริมาณต่อใบสั่งซื้อ จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่รับมาใหม่</span><span class="sxs-lookup"><span data-stu-id="88e44-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="88e44-259">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ไม่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับสินค้ารายการแรกต่อใบสั่งซื้อ ตามปริมาณที่รับ</span><span class="sxs-lookup"><span data-stu-id="88e44-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="88e44-260">นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="88e44-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="88e44-261">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับต่อใบสั่งซื้อหลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="88e44-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="88e44-262">การใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="88e44-262">Production</span></span>

<span data-ttu-id="88e44-263">ในการผลิต หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น *รายงานเป็นเสร็จสิ้น* และฟิลด์ **การดำเนินการ** เป็น *ภายหลัง* บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88e44-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="88e44-264">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ใช่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกปริมาณที่เสร็จสิ้นและการตั้งค่าในสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="88e44-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="88e44-265">ทุกครั้งที่มีการรายงานปริมาณเป็นเสร็จสิ้นต่อใบสั่งผลิต จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่เพิ่งเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="88e44-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="88e44-266">ตรรกะการสร้างนี้สอดคล้องกับการซื้อ</span><span class="sxs-lookup"><span data-stu-id="88e44-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="88e44-267">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น *ไม่* จะมีการสร้างใบสั่งตรวจสอบคุณภาพในครั้งแรกที่มีการรายงานปริมาณเป็นเสร็จสิ้น ตามปริมาณที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="88e44-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="88e44-268">นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตามของสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="88e44-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="88e44-269">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับปริมาณที่เสร็จสิ้นในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="88e44-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88e44-270">ข้อกำหนดเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-270">Quality specification</span></span></th>
<th><span data-ttu-id="88e44-271">ต่อปริมาณที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="88e44-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="88e44-272">ต่อมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="88e44-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="88e44-273">ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="88e44-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88e44-274">เปอร์เซ็นต์: 10%</span><span class="sxs-lookup"><span data-stu-id="88e44-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="88e44-275">ใช่</span><span class="sxs-lookup"><span data-stu-id="88e44-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="88e44-276">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="88e44-276">Batch number: No</span></span></p>
<p><span data-ttu-id="88e44-277">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="88e44-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="88e44-278">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="88e44-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="88e44-279">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="88e44-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="88e44-280">ใบสั่งตรวจสอบคุณภาพ 1 สำหรับ 3 (10% ของ 30)</span><span class="sxs-lookup"><span data-stu-id="88e44-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="88e44-281">รายงานเมื่อเสร็จสิ้นสำหรับ 70</span><span class="sxs-lookup"><span data-stu-id="88e44-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="88e44-282">ใบสั่งตรวจสอบคุณภาพ 2 สำหรับ 7 (10% ของปริมาณในใบสั่งที่เหลืออยู่ซึ่งเท่ากับ 70 ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="88e44-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="88e44-283">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="88e44-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="88e44-284">ไม่</span><span class="sxs-lookup"><span data-stu-id="88e44-284">No</span></span></td>
<td>
<p><span data-ttu-id="88e44-285">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="88e44-285">Batch number: No</span></span></p>
<p><span data-ttu-id="88e44-286">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="88e44-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="88e44-287">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="88e44-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="88e44-288">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="88e44-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="88e44-289">ใบสั่งตรวจสอบคุณภาพ 1 ต่อ 1 (สำหรับปริมาณที่รายงานการเสร็จงานครั้งแรกซึ่งมีค่าคงที่เป็น 1)</span><span class="sxs-lookup"><span data-stu-id="88e44-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="88e44-290">ใบสั่งตรวจสอบคุณภาพ 2 ต่อ 1 (สำหรับปริมาณที่คงเหลือ ซึ่งยังมีค่าคงที่เป็น 1)</span><span class="sxs-lookup"><span data-stu-id="88e44-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="88e44-291">รายงานเมื่อเสร็จสิ้นสำหรับ 10</span><span class="sxs-lookup"><span data-stu-id="88e44-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="88e44-292">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="88e44-293">รายงานเมื่อเสร็จสิ้นสำหรับ 60</span><span class="sxs-lookup"><span data-stu-id="88e44-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="88e44-294">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="88e44-295">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="88e44-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="88e44-296">ใช่</span><span class="sxs-lookup"><span data-stu-id="88e44-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="88e44-297">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="88e44-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="88e44-298">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="88e44-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="88e44-299">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="88e44-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="88e44-300">รายงานการเสร็จงานของ 3: 1 สำหรับหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1 1 สำหรับหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2 และ 1 สำหรับหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3</span><span class="sxs-lookup"><span data-stu-id="88e44-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="88e44-301">ใบสั่งตรวจสอบคุณภาพ 1 ต่อ 1 ของหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1</span><span class="sxs-lookup"><span data-stu-id="88e44-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="88e44-302">ใบสั่งตรวจสอบคุณภาพ 2 ต่อ 1 ของหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2</span><span class="sxs-lookup"><span data-stu-id="88e44-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="88e44-303">ใบสั่งตรวจสอบคุณภาพ 3 ต่อ 1 ของหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3</span><span class="sxs-lookup"><span data-stu-id="88e44-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="88e44-304">รายงานการเสร็จงานของ 2: 1 สำหรับหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4 1 สำหรับหมายเลขชุดงาน b5 หมายเลขลำดับประจำสินค้า s5</span><span class="sxs-lookup"><span data-stu-id="88e44-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="88e44-305">ใบสั่งตรวจสอบคุณภาพ 4 ต่อ 1 ของหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4</span><span class="sxs-lookup"><span data-stu-id="88e44-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="88e44-306">ใบสั่งตรวจสอบคุณภาพ 5 ต่อ 1 ของหมายเลขชุดงาน b5 หมายเลขลำดับประจำสินค้า s5</span><span class="sxs-lookup"><span data-stu-id="88e44-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="88e44-307"><strong>หมายเหตุ:</strong> : ชุดงานสามารถนำมาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="88e44-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="88e44-308">ปริมาณคงที่: 2</span><span class="sxs-lookup"><span data-stu-id="88e44-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="88e44-309">ไม่</span><span class="sxs-lookup"><span data-stu-id="88e44-309">No</span></span></td>
<td>
<p><span data-ttu-id="88e44-310">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="88e44-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="88e44-311">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="88e44-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="88e44-312">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="88e44-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="88e44-313">รายงานการเสร็จงานของ 3: 1 สำหรับหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1 1 สำหรับหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2 และ 1 สำหรับหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3 และ 1 สำหรับหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4</span><span class="sxs-lookup"><span data-stu-id="88e44-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="88e44-314">ใบสั่งตรวจสอบคุณภาพ 1 ต่อ 1 ของหมายเลขชุดงาน b1 หมายเลขลำดับประจำสินค้า s1</span><span class="sxs-lookup"><span data-stu-id="88e44-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="88e44-315">ใบสั่งตรวจสอบคุณภาพ 2 ต่อ 1 ของหมายเลขชุดงาน b2 หมายเลขลำดับประจำสินค้า s2</span><span class="sxs-lookup"><span data-stu-id="88e44-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="88e44-316">ใบสั่งตรวจสอบคุณภาพ 3 ต่อ 1 ของหมายเลขชุดงาน b3 หมายเลขลำดับประจำสินค้า s3</span><span class="sxs-lookup"><span data-stu-id="88e44-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="88e44-317">ใบสั่งตรวจสอบคุณภาพ 4 ต่อ 1 ของหมายเลขชุดงาน b4 หมายเลขลำดับประจำสินค้า s4</span><span class="sxs-lookup"><span data-stu-id="88e44-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="88e44-318">ใบสั่งตรวจสอบคุณภาพ 5 สำหรับ 2 โดยไม่มีการอ้างอิงถึงหมายเลขชุดงานและหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="88e44-319">รายงานการเสร็จงานของ 6: 1 สำหรับหมายเลขชุดงาน b5 หมายเลขลำดับประจำสินค้า s5 1 สำหรับหมายเลขชุดงาน b6 หมายเลขลำดับประจำสินค้า s6 และ 1 สำหรับหมายเลขชุดงาน b7 หมายเลขลำดับประจำสินค้า s7 1 สำหรับหมายเลขชุดงาน b8 หมายเลขลำดับประจำสินค้า s8 สำหรับหมายเลขชุดงาน b9 หมายเลขลำดับประจำสินค้า s9 และ 1 สำหรับหมายเลขชุดงาน b10 หมายเลขลำดับประจำสินค้า s10</span><span class="sxs-lookup"><span data-stu-id="88e44-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="88e44-320">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="88e44-321">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="88e44-321">Additional resources</span></span>

- [<span data-ttu-id="88e44-322">กระบวนการการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="88e44-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="88e44-323">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="88e44-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="88e44-324">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="88e44-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
