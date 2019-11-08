---
title: ภาพรวมการจัดการคุณภาพ
description: หัวข้อนี้อธิบายวิธีที่คุณสามารถใช้การจัดการคุณภาพใน Dynamics 365 Supply Chain Management เพื่อช่วยพัฒนาคุณภาพผลิตภัณฑ์ภายในห่วงโซ่อุปทานของคุณ
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba38f9c43fed81768155a27dda88a4bfb4a7828e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653567"
---
# <a name="quality-management-overview"></a><span data-ttu-id="b23bc-103">ภาพรวมการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b23bc-104">หัวข้อนี้อธิบายวิธีที่คุณสามารถใช้การจัดการคุณภาพใน Dynamics 365 Supply Chain Management เพื่อช่วยพัฒนาคุณภาพผลิตภัณฑ์ภายในห่วงโซ่อุปทานของคุณ</span><span class="sxs-lookup"><span data-stu-id="b23bc-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="b23bc-105">การจัดการคุณภาพสามารถช่วยให้คุณจัดการระยะเวลาเมื่อคุณจัดการผลิตภัณฑ์ที่ไม่สอดคล้องกันโดยไม่คำนึงถึงจุดกำเนิด</span><span class="sxs-lookup"><span data-stu-id="b23bc-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="b23bc-106">เนื่องจากชนิดของการวินิจฉัยเชื่อมโยงกับการแก้ไขรายงาน Supply Chain Management สามารถจัดกำหนดการงานเพื่อแก้ไขปัญหาและป้องกันการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="b23bc-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="b23bc-107">นอกเหนือจากฟังก์ชันสำหรับการจัดการไม่สอดคล้องกัน การจัดการคุณภาพรวมถึงฟังก์ชันสำหรับการติดตามปัญหาตามชนิดของปัญหา (แม้กระทั่งปัญหาภายใน), และสำหรับ การระบุโซลูชันระยะสั้นหรือระยะยาว</span><span class="sxs-lookup"><span data-stu-id="b23bc-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="b23bc-108">สถิติเกี่ยวกับตัวบ่งชี้ประสิทธิภาพหลัก (KPIs) ให้เข้าใจเกี่ยวกับประวัติของปัญหาความไม่สอดคล้องก่อนหน้านี้และโซลูชันที่ใช้เพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b23bc-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="b23bc-109">คุณสามารถใช้ข้อมูลในอดีตเพื่อตรวจทานประสิทธิภาพของตัวชี้วัดคุณภาพก่อนหน้านี้และกำหนดตัวชี้วัดคุณภาพที่เหมาะสมเพื่อใช้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="b23bc-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="b23bc-110">เมื่อคุณตั้งค่าการเชื่อมโยงคุณภาพ Supply Chain Management สามารถสร้างใบสั่งตรวจสอบคุณภาพสำหรับกระบวนการทางธุรกิจ เหตุการณ์ และเงื่อนไขต่างๆ</span><span class="sxs-lookup"><span data-stu-id="b23bc-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="b23bc-111">การเชื่อมโยงคุณภาพสามารถครอบคลุมสินค้าเฉพาะ กลุ่มสินค้าเฉพาะ หรือสินค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b23bc-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="b23bc-112">ตัวอย่างของการใช้การจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-112">Examples of the use of quality management</span></span>
<span data-ttu-id="b23bc-113">การจัดการคุณภาพเป็นแบบยืดหยุ่นและสามารถนำมาใช้ในวิธีการต่าง ๆ เพื่อให้ตรงกับความต้องการของระดับเฉพาะของการดำเนินงานห่วงโซ่อุปทาน</span><span class="sxs-lookup"><span data-stu-id="b23bc-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="b23bc-114">ตัวอย่างต่อไปนี้จะแสดงให้เห็นการใช้ที่เป็นไปได้ของลักษณะการทำงาน:</span><span class="sxs-lookup"><span data-stu-id="b23bc-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="b23bc-115">เริ่มต้นกระบวนการควบคุมคุณภาพโดยอัตโนมัติ ตามเกณฑ์ที่กำหนดไว้ล่วงหน้า (เมื่อมีการลงทะเบียนคลังสินค้าของใบสั่งซื้อจากผู้จัดจำหน่ายเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="b23bc-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="b23bc-116">บล็อคสินค้าคงคลังในระหว่างการตรวจสอบเพื่อป้องกันไม่ให้สินค้าคงคลังที่ไม่ได้รับการอนุมัติจากการถูกใช้ (การบล็อคทั้งหมดของปริมาณใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="b23bc-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="b23bc-117">ใช้การสุ่มตัวอย่างสินค้าเป็นส่วนหนึ่งของการเชื่อมโยงคุณภาพเพื่อกำหนดจำนวนของสินค้าคงคลังที่มีอยู่จริงปัจจุบันที่จะต้องตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="b23bc-118">การสุ่มตัวอย่างอาจขึ้นอยู่กับปริมาณคงที่หรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="b23bc-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="b23bc-119">สร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับสินค้าเป็นบางส่วน</span><span class="sxs-lookup"><span data-stu-id="b23bc-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="b23bc-120">เมื่อต้องการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่รับจริงตามใบสั่ง คุณจะต้องเลือกกล่องกาเครื่องหมาย **ต่อปริมาณที่อัพเดต** บนแบบฟอร์ม **การสุ่มตัวอย่างสินค้า**</span><span class="sxs-lookup"><span data-stu-id="b23bc-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="b23bc-121">สร้างชนิดของการทดสอบที่มีค่าต่ำสุด สูงสุด และค่าเป้าหมายของการทดสอบ และทำการทดสอบเชิงคุณภาพเทียบกับเชิงปริมาณที่มีผลลัพธ์การตรวจสอบความถูกต้องที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="b23bc-122">ระบุถึงระดับคุณภาพที่ยอมรับได้ (AQL) เพื่อควบคุมการยอมรับตัวชี้วัดคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="b23bc-123">ระบุทรัพยากรที่ต้องมีการดำเนินการตรวจสอบ เช่นพื้นที่ทดสอบและเครื่องมือทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="b23bc-124">การทำงานกับการเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-124">Working with quality associations</span></span>
<span data-ttu-id="b23bc-125">กระบวนการทางธุรกิจที่ใช้การเชื่อมโยงคุณภาพอาจเกี่ยวข้องกับเอกสารต้นทางต่าง ๆ เช่นใบสั่งซื้อ ใบสั่งขาย หรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b23bc-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="b23bc-126">แต่ละเรกคอร์ดความสัมพันธ์ของคุณภาพกำหนดชุดของการทดสอบ AQL และแผนการสุ่มตัวอย่างที่ใช้กับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b23bc-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="b23bc-127">คุณต้องกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b23bc-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="b23bc-128">ตัวอย่างเช่น คุณสามารถตั้งค่าการเชื่อมโยงคุณภาพที่สร้างใบสั่งตรวจสอบคุณภาพเมื่อมีการอัพเดตใบรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b23bc-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="b23bc-129">ขึ้นอยู่กับการตั้งค่าของแผนปฏิบัติการ ทริกเกอร์ดำเนินการด้วยตัวเองสามารถถูกบล็อคในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ หรือกระบวนการถัดไป เช่นการออกอินวอยซ์ใบสั้งซื้อ สามารถถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="b23bc-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="b23bc-130">**หมายเหตุ:** ในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ ปริมาณสินค้าคงคลังจะถูกถูกบล็อคจากการออกใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b23bc-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="b23bc-131">ขึ้นอยู่กับการตั้งค่า **การบล็อคทั้งหมด** บนหน้า **การสุ่มตัวอย่างสินค้า** ปริมาณเป็นปริมาณในใบสั่งตรวจสอบคุณภาพ หรือปริมาณในรายการเอกสารต้นทาง</span><span class="sxs-lookup"><span data-stu-id="b23bc-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="b23bc-132">สำหรับกระบวนการทางธุรกิจที่ระบุ เรกคอร์ดความสัมพันธ์ของคุณภาพจะระบุเหตุการณ์และเงื่อนไขที่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="b23bc-133">เงื่อนไขอาจเป็นเฉพาะสำหรับไซต์หรือนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="b23bc-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="b23bc-134">สามารถสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับการทดสอบแบบทำลายเฉพาะเมื่อสินค้าคงคลังคงเหลือที่มีอยู่สำหรับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="b23bc-135">ตัวอย่างต่อไปนี้อธิบายวิธีกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรในแต่ละกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b23bc-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="b23bc-136">สำหรับแต่ละตัวอย่าง ตารางต่อไปนี้สรุปเหตุการณ์และเงื่อนไขที่กำหนดโดยเรกคอร์ดความสัมพันธ์ของคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b23bc-137">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="b23bc-137">Reference type</span></span></th>
<th><span data-ttu-id="b23bc-138">ชนิดเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-138">Event type</span></span></th>
<th><span data-ttu-id="b23bc-139">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b23bc-139">Execution</span></span></th>
<th><span data-ttu-id="b23bc-140">การบล็อคเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-140">Event blocking</span></span></th>
<th><span data-ttu-id="b23bc-141">การอ้างอิงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="b23bc-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b23bc-142">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-142">Inventory</span></span></td>
<td><span data-ttu-id="b23bc-143">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-143">Not applicable</span></span></td>
<td><span data-ttu-id="b23bc-144">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-144">Not applicable</span></span></td>
<td><span data-ttu-id="b23bc-145">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-145">None</span></span></td>
<td><span data-ttu-id="b23bc-146">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b23bc-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="b23bc-147">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="b23bc-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="b23bc-148">กระบวนการเบิกสินค้าถูกจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="b23bc-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="b23bc-149">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-149">Before</span></span></td>
<td><span data-ttu-id="b23bc-150">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="b23bc-151">รหัส กลุ่ม หรือทั้งหมด เฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b23bc-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-152">กระบวนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-153">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b23bc-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-154">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b23bc-155">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b23bc-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-156">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-156">Before</span></span></td>
<td><span data-ttu-id="b23bc-157">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-158">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b23bc-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-159">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="b23bc-160">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="b23bc-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="b23bc-161">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="b23bc-162">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-162">Before</span></span></td>
<td><span data-ttu-id="b23bc-163">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-164">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-165">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-166">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b23bc-167">หลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-167">After</span></span></td>
<td><span data-ttu-id="b23bc-168">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-169">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-170">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b23bc-171">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="b23bc-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-172">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-172">Not applicable</span></span></td>
<td><span data-ttu-id="b23bc-173">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-174">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-175">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b23bc-176">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-177">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-177">Before</span></span></td>
<td><span data-ttu-id="b23bc-178">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-179">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-180">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b23bc-181">หลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-181">After</span></span></td>
<td><span data-ttu-id="b23bc-182">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-183">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="b23bc-184">การผลิต</span><span class="sxs-lookup"><span data-stu-id="b23bc-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-185">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="b23bc-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-186">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-186">Not applicable</span></span></td>
<td><span data-ttu-id="b23bc-187">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="b23bc-188">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b23bc-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-189">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-190">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b23bc-191">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-192">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-192">Before</span></span></td>
<td><span data-ttu-id="b23bc-193">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-194">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-195">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b23bc-196">หลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-196">After</span></span></td>
<td><span data-ttu-id="b23bc-197">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-198">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b23bc-199">การตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-200">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b23bc-201">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-201">Before</span></span></td>
<td><span data-ttu-id="b23bc-202">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-203">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-204">หลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-204">After</span></span></td>
<td><span data-ttu-id="b23bc-205">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-206">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-206">End</span></span></td>
<td><span data-ttu-id="b23bc-207">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-207">Before</span></span></td>
<td><span data-ttu-id="b23bc-208">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b23bc-209">ขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="b23bc-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-210">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b23bc-211">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-211">Before</span></span></td>
<td><span data-ttu-id="b23bc-212">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-213">รหัส กลุ่ม หรือทั้งหมดเฉพาะ และระบุทรัพยากร กลุ่ม หรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b23bc-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-214">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-215">หลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-215">After</span></span></td>
<td><span data-ttu-id="b23bc-216">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b23bc-217">การผลิตสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="b23bc-217">Co-product production</span></span></td>
<td><span data-ttu-id="b23bc-218">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="b23bc-218">Registration</span></span></td>
<td><span data-ttu-id="b23bc-219">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-220">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="b23bc-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b23bc-221">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b23bc-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b23bc-222">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-222">Report as finished</span></span></td>
<td><span data-ttu-id="b23bc-223">ก่อน</span><span class="sxs-lookup"><span data-stu-id="b23bc-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-224">หลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b23bc-225">ตารางต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างใบสั่งตรวจสอบคุณภาพสามารถสำหรับชนิดเฉพาะของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="b23bc-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="b23bc-226">ชนิดของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="b23bc-226">Type of process</span></span></th>
<th><span data-ttu-id="b23bc-227">เมื่อใบสั่งตรวจสอบคุณภาพสามารถถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b23bc-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="b23bc-228">เมื่อใบสั่งตรวจสอบคุณภาพสามารถสร้างหากการทดสอบแบบทำลายจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b23bc-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="b23bc-229">ข้อมูลเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b23bc-229">Condition information</span></span></th>
<th><span data-ttu-id="b23bc-230">ข้อมูลการสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b23bc-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b23bc-231">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b23bc-231">Purchase order</span></span></td>
<td><span data-ttu-id="b23bc-232">ก่อนหรือหลังรายการรับสินค้าหรือใบรับสินค้าสำหรับวัสดุที่ได้รับจะมีการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b23bc-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="b23bc-233">หลังจากใบรับสินค้าสำหรับวัสดุที่ได้รับมีการลงรายการบัญชี เนื่องจากวัสดุต้องพร้อมใช้งานสำหรับการทดสอบแบบทำลาย</span><span class="sxs-lookup"><span data-stu-id="b23bc-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="b23bc-234">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b23bc-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b23bc-235">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-236">ใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-236">Quarantine order</span></span></td>
<td><span data-ttu-id="b23bc-237">ก่อน หรือหลัง ใบสั่งตรวจสอบสินค้ามีการรายงานเสร็จสิ้นแล้วหรือสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b23bc-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="b23bc-238">ใบสั่งคุณภาพที่ต้องการการทดสอบแบบหักล้างไม่&#39;สามารถถูกสร้างได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="b23bc-239">ถือ&#39;ว่าฟังก์ชันใบสั่งการกักกันจัดการการจัดการของวัสดุที่ถูกทำลาย</span><span class="sxs-lookup"><span data-stu-id="b23bc-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="b23bc-240">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b23bc-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b23bc-241">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งตรวจสอบสินค้าสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-242">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="b23bc-242">Sales order</span></span></td>
<td><span data-ttu-id="b23bc-243">ก่อนการจัดกำหนดการกระบวนการเบิกสินค้าหรืออัพเดตบันทึกสำหรับสินค้าที่กำลังจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b23bc-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="b23bc-244">ในขั้นตอนใดๆ</span><span class="sxs-lookup"><span data-stu-id="b23bc-244">At any step</span></span></td>
<td><span data-ttu-id="b23bc-245">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือลูกค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b23bc-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b23bc-246">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-247">ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b23bc-247">Production order</span></span></td>
<td><span data-ttu-id="b23bc-248">ก่อนหรือหลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b23bc-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b23bc-249">หลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b23bc-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b23bc-250">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b23bc-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b23bc-251">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-252">ใบสั่งผลิตที่มีขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="b23bc-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="b23bc-253">ก่อนหรือหลังจากรายงานการเสร็จสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b23bc-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="b23bc-254">หลังจากการรายงานการผลิตเสร็จสิ้นแล้วสำหรับการดำเนินงานสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="b23bc-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="b23bc-255">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือทรัพยากรการดำเนินงาน หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b23bc-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b23bc-256">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับขั้นตอนของกระบวนการผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-257">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b23bc-257">Inventory</span></span></td>
<td><span data-ttu-id="b23bc-258">ใบสั่งตรวจสอบคุณภาพไม่สามารถถูกสร้างขึ้นโดยอัตโนมัติสำหรับธุรกรรมในสมุดรายวันสินค้าคงคลังหรือธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="b23bc-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b23bc-259">ใบสั่งคุณภาพต้องถูกสร้างด้วยตนเองสำหรับปริมาณสินค้าคงคลังของ&#39;สินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="b23bc-260">จำเป็นต้องมีปริมาณสินค้าคงคลังคงเหลือที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="b23bc-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="b23bc-261">ตัวอย่างการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b23bc-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="b23bc-262">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="b23bc-262">Purchasing</span></span>

<span data-ttu-id="b23bc-263">ในการซื้อ หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น **ใบรับสินค้า** และฟิลด์ **การดำเนินการ** เป็น **ภายหลัง** บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b23bc-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="b23bc-264">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ใช่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกการรับสินค้าต่อใบสั่งซื้อ ตามปริมาณที่รับและการตั้งค่าในสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b23bc-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="b23bc-265">ทุกครั้งที่มีการรับปริมาณต่อใบสั่งซื้อ จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่รับมาใหม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="b23bc-266">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ไม่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับสินค้ารายการแรกต่อใบสั่งซื้อ ตามปริมาณที่รับ</span><span class="sxs-lookup"><span data-stu-id="b23bc-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="b23bc-267">นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="b23bc-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="b23bc-268">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับต่อใบสั่งซื้อหลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b23bc-269">ข้อกำหนดเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-269">Quality specification</span></span></th>
<th><span data-ttu-id="b23bc-270">ต่อปริมาณที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="b23bc-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="b23bc-271">ต่อมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="b23bc-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="b23bc-272">ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b23bc-273">เปอร์เซ็นต์: 10%</span><span class="sxs-lookup"><span data-stu-id="b23bc-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="b23bc-274">ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="b23bc-275">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-275">Batch number: No</span></span></p>
<p><span data-ttu-id="b23bc-276">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="b23bc-277">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="b23bc-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="b23bc-278">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="b23bc-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b23bc-279">ใบสั่งตรวจสอบคุณภาพ #1 สำหรับ 3 (10% ของ 30)</span><span class="sxs-lookup"><span data-stu-id="b23bc-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-280">รายงานเมื่อเสร็จสิ้นสำหรับ 70</span><span class="sxs-lookup"><span data-stu-id="b23bc-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="b23bc-281">ใบสั่งตรวจสอบคุณภาพ #2 สำหรับ 7 (10% ของปริมาณในใบสั่งที่เหลืออยู่ซึ่งเท่ากับ 70 ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="b23bc-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-282">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="b23bc-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b23bc-283">ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-283">No</span></span></td>
<td>
<p><span data-ttu-id="b23bc-284">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-284">Batch number: No</span></span></p>
<p><span data-ttu-id="b23bc-285">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="b23bc-286">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="b23bc-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="b23bc-287">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="b23bc-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b23bc-288">มีการสร้างใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 (สำหรับปริมาณที่รายงานการเสร็จงานครั้งแรกซึ่งมีค่าคงที่เป็น 1)</span><span class="sxs-lookup"><span data-stu-id="b23bc-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="b23bc-289">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพเพิ่มเติมกับปริมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="b23bc-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-290">รายงานเมื่อเสร็จสิ้นสำหรับ 10</span><span class="sxs-lookup"><span data-stu-id="b23bc-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="b23bc-291">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-292">รายงานเมื่อเสร็จสิ้นสำหรับ 60</span><span class="sxs-lookup"><span data-stu-id="b23bc-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="b23bc-293">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-294">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="b23bc-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b23bc-295">ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="b23bc-296">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b23bc-297">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b23bc-298">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="b23bc-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b23bc-299">รายงานเมื่อเสร็จสิ้นสำหรับ 3</span><span class="sxs-lookup"><span data-stu-id="b23bc-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="b23bc-300">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 ของชุดงาน #b1 หมายเลขลำดับ #s1</span><span class="sxs-lookup"><span data-stu-id="b23bc-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="b23bc-301">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 สำหรับชุดงาน #b2 หมายเลขลำดับ #s2</span><span class="sxs-lookup"><span data-stu-id="b23bc-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="b23bc-302">ใบสั่งตรวจสอบคุณภาพ #3 ต่อ 1 สำหรับชุดงาน #b3 หมายเลขลำดับ #s3</span><span class="sxs-lookup"><span data-stu-id="b23bc-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-303">รายงานเมื่อเสร็จสิ้นสำหรับ 2</span><span class="sxs-lookup"><span data-stu-id="b23bc-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="b23bc-304">ใบสั่งตรวจสอบคุณภาพ #4 ต่อ 1 สำหรับชุดงาน #b4 หมายเลขลำดับ #s4</span><span class="sxs-lookup"><span data-stu-id="b23bc-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="b23bc-305">ใบสั่งตรวจสอบคุณภาพ #5 ต่อ 1 สำหรับชุดงาน #b5 หมายเลขลำดับ #s5</span><span class="sxs-lookup"><span data-stu-id="b23bc-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="b23bc-306"><strong>หมายเหตุ:</strong> : ชุดงานสามารถนำมาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-307">ปริมาณคงที่: 2</span><span class="sxs-lookup"><span data-stu-id="b23bc-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="b23bc-308">ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-308">No</span></span></td>
<td>
<p><span data-ttu-id="b23bc-309">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b23bc-310">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b23bc-311">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="b23bc-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b23bc-312">รายงานเมื่อเสร็จสิ้นสำหรับ 4</span><span class="sxs-lookup"><span data-stu-id="b23bc-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="b23bc-313">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 ของชุดงาน #b1 หมายเลขลำดับ #s1</span><span class="sxs-lookup"><span data-stu-id="b23bc-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="b23bc-314">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 สำหรับชุดงาน #b2 หมายเลขลำดับ #s2</span><span class="sxs-lookup"><span data-stu-id="b23bc-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="b23bc-315">ใบสั่งตรวจสอบคุณภาพ #3 ต่อ 1 สำหรับชุดงาน #b3 หมายเลขลำดับ #s3</span><span class="sxs-lookup"><span data-stu-id="b23bc-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="b23bc-316">ใบสั่งตรวจสอบคุณภาพ #4 ต่อ 1 สำหรับชุดงาน #b4 หมายเลขลำดับ #s4</span><span class="sxs-lookup"><span data-stu-id="b23bc-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="b23bc-317">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพเพิ่มเติมกับปริมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="b23bc-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-318">รายงานเมื่อเสร็จสิ้นสำหรับ 6</span><span class="sxs-lookup"><span data-stu-id="b23bc-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="b23bc-319">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="b23bc-320">การผลิต</span><span class="sxs-lookup"><span data-stu-id="b23bc-320">Production</span></span>

<span data-ttu-id="b23bc-321">ในการผลิต หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น **รายงานเป็นเสร็จสิ้น** และฟิลด์ **การดำเนินการ** เป็น **ภายหลัง** บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b23bc-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="b23bc-322">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ใช่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกปริมาณที่เสร็จสิ้นและการตั้งค่าในสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b23bc-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="b23bc-323">ทุกครั้งที่มีการรายงานปริมาณเป็นเสร็จสิ้นต่อใบสั่งผลิต จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่เพิ่งเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="b23bc-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="b23bc-324">ตรรกะการสร้างนี้สอดคล้องกับการซื้อ</span><span class="sxs-lookup"><span data-stu-id="b23bc-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="b23bc-325">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ไม่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพในครั้งแรกที่มีการรายงานปริมาณเป็นเสร็จสิ้น ตามปริมาณที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="b23bc-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="b23bc-326">นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตามของสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b23bc-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="b23bc-327">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับปริมาณที่เสร็จสิ้นในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="b23bc-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b23bc-328">ข้อกำหนดเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-328">Quality specification</span></span></th>
<th><span data-ttu-id="b23bc-329">ต่อปริมาณที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="b23bc-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="b23bc-330">ต่อมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="b23bc-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="b23bc-331">ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b23bc-332">เปอร์เซ็นต์: 10%</span><span class="sxs-lookup"><span data-stu-id="b23bc-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="b23bc-333">ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="b23bc-334">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-334">Batch number: No</span></span></p>
<p><span data-ttu-id="b23bc-335">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="b23bc-336">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="b23bc-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="b23bc-337">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="b23bc-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b23bc-338">ใบสั่งตรวจสอบคุณภาพ #1 สำหรับ 3 (10% ของ 30)</span><span class="sxs-lookup"><span data-stu-id="b23bc-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-339">รายงานเมื่อเสร็จสิ้นสำหรับ 70</span><span class="sxs-lookup"><span data-stu-id="b23bc-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="b23bc-340">ใบสั่งตรวจสอบคุณภาพ #2 สำหรับ 7 (10% ของปริมาณในใบสั่งที่เหลืออยู่ซึ่งเท่ากับ 70 ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="b23bc-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-341">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="b23bc-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b23bc-342">ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-342">No</span></span></td>
<td>
<p><span data-ttu-id="b23bc-343">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-343">Batch number: No</span></span></p>
<p><span data-ttu-id="b23bc-344">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="b23bc-345">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="b23bc-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="b23bc-346">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="b23bc-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b23bc-347">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 (สำหรับปริมาณที่รายงานการเสร็จงานครั้งแรกซึ่งมีค่าคงที่เป็น 1)</span><span class="sxs-lookup"><span data-stu-id="b23bc-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="b23bc-348">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 (สำหรับปริมาณที่คงเหลือ ซึ่งยังมีค่าคงที่เป็น 1)</span><span class="sxs-lookup"><span data-stu-id="b23bc-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-349">รายงานเมื่อเสร็จสิ้นสำหรับ 10</span><span class="sxs-lookup"><span data-stu-id="b23bc-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="b23bc-350">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-351">รายงานเมื่อเสร็จสิ้นสำหรับ 60</span><span class="sxs-lookup"><span data-stu-id="b23bc-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="b23bc-352">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-353">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="b23bc-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b23bc-354">ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="b23bc-355">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b23bc-356">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b23bc-357">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="b23bc-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b23bc-358">รายงานเป็นเสร็จสิ้นสำหรับ3: 1 สำหรับ #b1, #s1; 1 สำหรับ #b2, #s2; และ 1 สำหรับ #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="b23bc-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="b23bc-359">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 ของชุดงาน #b1 หมายเลขลำดับ #s1</span><span class="sxs-lookup"><span data-stu-id="b23bc-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="b23bc-360">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 สำหรับชุดงาน #b2 หมายเลขลำดับ #s2</span><span class="sxs-lookup"><span data-stu-id="b23bc-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="b23bc-361">ใบสั่งตรวจสอบคุณภาพ #3 ต่อ 1 สำหรับชุดงาน #b3 หมายเลขลำดับ #s3</span><span class="sxs-lookup"><span data-stu-id="b23bc-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-362">รายงานเป็นเสร็จสิ้นสำหรับ 2: 1 สำหรับ #b4, #s4; และ 1 สำหรับ #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="b23bc-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="b23bc-363">ใบสั่งตรวจสอบคุณภาพ #4 ต่อ 1 สำหรับชุดงาน #b4 หมายเลขลำดับ #s4</span><span class="sxs-lookup"><span data-stu-id="b23bc-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="b23bc-364">ใบสั่งตรวจสอบคุณภาพ #5 ต่อ 1 สำหรับชุดงาน #b5 หมายเลขลำดับ #s5</span><span class="sxs-lookup"><span data-stu-id="b23bc-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="b23bc-365"><strong>หมายเหตุ:</strong> : ชุดงานสามารถนำมาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="b23bc-366">ปริมาณคงที่: 2</span><span class="sxs-lookup"><span data-stu-id="b23bc-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="b23bc-367">ไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-367">No</span></span></td>
<td>
<p><span data-ttu-id="b23bc-368">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b23bc-369">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="b23bc-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b23bc-370">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="b23bc-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b23bc-371">รายงานเป็นเสร็จสิ้นสำหรับ 4: 1 สำหรับ #b1, #s1; 1 สำหรับ #b2, #s2; 1 สำหรับ #b3, #s3; และ 1 สำหรับ #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="b23bc-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="b23bc-372">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 ของชุดงาน #b1 หมายเลขลำดับ #s1</span><span class="sxs-lookup"><span data-stu-id="b23bc-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="b23bc-373">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 สำหรับชุดงาน #b2 หมายเลขลำดับ #s2</span><span class="sxs-lookup"><span data-stu-id="b23bc-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="b23bc-374">ใบสั่งตรวจสอบคุณภาพ #3 ต่อ 1 สำหรับชุดงาน #b3 หมายเลขลำดับ #s3</span><span class="sxs-lookup"><span data-stu-id="b23bc-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="b23bc-375">ใบสั่งตรวจสอบคุณภาพ #4 ต่อ 1 สำหรับชุดงาน #b4 หมายเลขลำดับ #s4</span><span class="sxs-lookup"><span data-stu-id="b23bc-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="b23bc-376">ใบสั่งตรวจสอบคุณภาพ #5 สำหรับ 2 โดยไม่มีการอ้างอิงถึงชุดงานและหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b23bc-377">รายงานเป็นเสร็จสิ้นสำหรับ 6: 1 สำหรับ #b5, #s5; 1 สำหรับ #b6, #s6; 1 สำหรับ #b7, #s7; 1 สำหรับ #b8, #s8; 1 สำหรับ #b9, #s9; และ 1สำหรับ #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="b23bc-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="b23bc-378">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="b23bc-379">หน้าการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b23bc-380">หน้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-380">Page</span></span></th>
<th><span data-ttu-id="b23bc-381">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b23bc-381">Description</span></span></th>
<th><span data-ttu-id="b23bc-382">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b23bc-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b23bc-383">การเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-383">Quality associations</span></span></td>
<td><span data-ttu-id="b23bc-384">ดูส่วนก่อนหน้าของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="b23bc-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="b23bc-385">ความสัมพันธ์ของคุณภาพกำหนดข้อมูลต่อไปนี้ทั้งหมดสำหรับใบสั่งตรวจสอบคุณภาพที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="b23bc-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="b23bc-386">เหตุการณ์ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b23bc-386">The transaction event</span></span></li>
<li><span data-ttu-id="b23bc-387">ชุดของการทดสอบที่ต้องดำเนินการบนสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="b23bc-388">AQL</span><span class="sxs-lookup"><span data-stu-id="b23bc-388">The AQL</span></span></li>
<li><span data-ttu-id="b23bc-389">แผนการสุ่มตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b23bc-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="b23bc-390">คุณต้องกำหนดคำความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจที่จำเป็นต้องมีการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b23bc-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="b23bc-391">ตัวอย่างเช่น สามารถสร้างใบสั่งตรวจสอบคุณภาพในกระบวนการทางธุรกิจสำหรับใบสั่งซื้อ ใบสั่งตรวจสอบสินค้า ใบสั่งขาย และใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b23bc-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b23bc-392">การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-392">Tests</span></span></td>
<td><span data-ttu-id="b23bc-393">ใช้หน้านี้ในการกำหนดและดูการทดสอบแต่ละรายการที่กำหนดว่าผลิตภัณฑ์ของคุณตรงตามข้อมูลจำเพาะเกี่ยวกับคุณภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b23bc-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="b23bc-394">คุณสามารถกำหนดรายการทดสอบแต่ละรายการกับกลุ่มการทดสอบอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="b23bc-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="b23bc-395">ในกรณีนี้ คุณระบุข้อมูลเฉพาะตัวของการทดสอบ เช่นค่าการประเมินที่ยอมรับได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b23bc-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="b23bc-396">ค่าการประเมินค่าจะใช้สำหรับการทดสอบเชิงปริมาณ และตัวแปรทดสอบที่จะใช้สำหรับการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="b23bc-397">การทดสอบเชิงปริมาณมีชนิดการทดสอบของ <strong>จำนวนเต็ม</strong> หรือ <strong>เศษส่วน</strong> และยังมีการกำหนดหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="b23bc-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="b23bc-398">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b23bc-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="b23bc-399">การทดสอบเชิงคุณภาพจะมีชนิดของ <strong>ตัวเลือก</strong>.</span><span class="sxs-lookup"><span data-stu-id="b23bc-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="b23bc-400">การทดสอบเชิงคุณภาพต้องการข้อมูลเพิ่มเติมเกี่ยวกับตัวแปรการทดสอบที่วัดและตัวเลือกที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b23bc-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="b23bc-401">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงตามผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="b23bc-402">บริษัทผู้ผลิตดำเนินการทดสอบวัสดุที่ซื้อสองแบบ: การทดสอบเชิงปริมาณเกี่ยวกับคุณภาพวัสดุและการทดสอบเชิงคุณภาพเกี่ยวกับความเสียหายของบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="b23bc-403">บริษัทกำหนดข้อมูลเพิ่มเติมเกี่ยวกับการทดสอบเชิงคุณภาพเพื่อระบุตัวแปรการทดสอบ (บรรจุภัณฑ์ที่เสียหาย) และผลลัพธ์ที่ได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="b23bc-404">บริษัทใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดการทดสอบทั้งสองให้กับกลุ่มการทดสอบและเพื่อระบุข้อมูลเฉพาะตัวของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="b23bc-405">กลุ่มทดสอบจะถูกกำหนดให้ใบสั่งตรวจสอบคุณภาพ เพื่อให้บริษัทสามารถรายงานผลการทดสอบสำหรับการทดสอบทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="b23bc-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b23bc-406">กลุ่มทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-406">Test groups</span></span></td>
<td><span data-ttu-id="b23bc-407">ใช้หน้านี้เพื่อตั้งค่า แก้ไข และดูกลุ่มทดสอบและการทดสอบแต่ละรายการที่กำหนดให้กับกลุ่มทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="b23bc-408">บานหน้าต่างด้านบนจะแสดงกลุ่มทดสอบ และบานหน้าต่างด้านล่างแสดงการทดสอบที่กำหนดให้กับกลุ่มการทดสอบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b23bc-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="b23bc-409">คุณกำหนดนโยบายต่าง ๆ ให้กับกลุ่มการทดสอบ เช่นแผนการสุ่มตัวอย่าง AQL และความต้องการสำหรับการทดสอบแบบทำลาย</span><span class="sxs-lookup"><span data-stu-id="b23bc-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="b23bc-410">เมื่อคุณกำหนดการทดสอบแต่ละรายการกับกลุ่มการทดสอบ คุณต้องกำหนดข้อมูลเพิ่มเติม เช่นลำดับ เอกสาร และวันที่ที่มีผลใช้</span><span class="sxs-lookup"><span data-stu-id="b23bc-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="b23bc-411">สำหรับการทดสอบเชิงปริมาณ ข้อมูลที่คุณกำหนดจะประกอบด้วยค่าการประเมินที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="b23bc-412">สำหรับการทดสอบเชิงคุณภาพ ข้อมูลนี้รวมถึงตัวแปรทดสอบและผลลัพธ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b23bc-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="b23bc-413">กลุ่มการทดสอบที่กำหนดให้กับใบสั่งตรวจสอบคุณภาพกำหนดชุดค่าเริ่มต้นของการทดสอบที่ต้องดำเนินการกับสินค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b23bc-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="b23bc-414">อย่างไรก็ตาม คุณสามารถเพิ่ม ลบ หรือเปลี่ยนการทดสอบบนใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="b23bc-415">ผลการทดสอบจะรายงานสำหรับการทดสอบแต่ละรายการบนใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="b23bc-416">บริษัทผู้ผลิตกำหนดกลุ่มการทดสอบสำหรับความผันแปรต่าง ๆ ของคำแนะนำเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="b23bc-417">กลุ่มการทดสอบต่าง ๆ สะท้อนถึงผลต่างในแผนการสุ่มตัวอย่าง ชุดของการทดสอบที่ต้องดำเนินการพร้อมกัน AQL และปัจจัยอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="b23bc-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="b23bc-418">สำหรับการทดสอบเชิงปริมาณ ยังมความแตกต่างของค่าการประเมินที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="b23bc-419">เพื่อบังคับใช้คำแนะนำด้านคุณภาพ บริษัทกำหนดกลุ่มการทดสอบสำหรับแต่ละกฎสำหรับการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติในหน้า <strong>ความสัมพันธ์ของคุณภาพ</strong> และยังกำหนดกลุ่มการทดสอบสำหรับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b23bc-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b23bc-420">กลุ่มคุณภาพสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-420">Item quality groups</span></span></td>
<td><span data-ttu-id="b23bc-421">ตั้งค่า แก้ไข และดูสินค้าที่กำหนดให้กับกลุ่มคุณภาพหนึ่งหรือหลายกลุ่ม ซึ่งมีการกำหนดให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="b23bc-422">กลุ่มคุณภาพแสดงข้อกำหนดในการทดสอบทั่วไปสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="b23bc-423">หลังจากที่คุณกำหนดความต้องการทดสอบบนหน้า <strong>กลุ่มทดสอบ</strong> คุณสามารถกำหนดกฎสำหรับการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="b23bc-424">เพื่อทำให้กระบวนการง่ายขึ้น คุณไม่ต้อง&#39;กำหนดกฎสำหรับสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="b23bc-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="b23bc-425">คุณกำหนดกฎสำหรับกลุ่มคุณภาพโดยการใช้หน้า <strong>ความสัมพันธ์ของคุณภาพ</strong> แทน</span><span class="sxs-lookup"><span data-stu-id="b23bc-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="b23bc-426">คุณยังสามารถใช้หน้า <strong>กลุ่มคุณภาพสินค้า</strong> สำหรับกลุ่มคุณภาพที่เลือกเพื่อกำหนดสินค้าที่เกี่ยวข้องกับกลุ่มนั้นได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="b23bc-427">คุณยังสามารถใช้หน้า <strong>กลุ่มคุณภาพสินค้า</strong> สำหรับกลุ่มคุณภาพที่เลือกเพื่อกำหนดสินค้าที่เกี่ยวข้องกับกลุ่มนั้นได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="b23bc-428">บริษัทผู้ผลิตจัดซื้อวัตถุดิบหลายอย่างที่มีการทดสอบสำหรับสินค้าสำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="b23bc-429">บริษัทกำหนดกลุ่มคุณภาพและกำหนดหมายเลขสินค้าที่เกี่ยวข้องกับวัตถุดิบสำหรับกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="b23bc-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="b23bc-430">ภายหลัง บริษัทสั่งซื้อวัตถุดิบชนิดใหม่ที่มีความต้องการทดสอบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b23bc-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="b23bc-431">แทนที่จะติดตั้งข้อกำหนดในการทดสอบใหม่สำหรับวัสดุใหม่ บริษัทเพิ่มหมายเลขสินค้าสำหรับวัสดุใหม่ให้กับกลุ่มคุณภาพที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b23bc-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="b23bc-432">บริษัทผู้ผลิตเดียวกันนี้ยังผลิตสินค้าที่มี มีข้อกำหนดในการทดสอบเดียวกันและจัดส่งสินค้าที่มีข้อกำหนดแบบเดียวกันในการทดสอบก่อนจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="b23bc-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="b23bc-433">บริษัทกำหนดกลุ่มคุณภาพเพิ่มเติมสองกลุ่มและกำหนดหมายเลขสินค้าที่เกี่ยวข้องให้กับกลุ่มคุณภาพแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="b23bc-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b23bc-434">ตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-434">Test variables</span></span></td>
<td><span data-ttu-id="b23bc-435">ใช้หน้านี้เพื่อกำหนดหรือดูตัวแปรที่เชื่อมโยงกับการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="b23bc-436">สำหรับแต่ละตัวแปร คุณกำหนดผลที่ได้ที่ระบุไว้แสดงถึงตัวเลือกที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="b23bc-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="b23bc-437">คุณกำหนดทดสอบบนหน้า <strong>ทดสอบ</strong></span><span class="sxs-lookup"><span data-stu-id="b23bc-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b23bc-438">สำหรับการทดสอบเชิงคุณภาพ คุณต้องตั้งค่าชนิดของการทดสอบเป็น <strong>ตัวเลือก</strong></span><span class="sxs-lookup"><span data-stu-id="b23bc-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="b23bc-439">ใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดตัวแปรการทดสอบในการทดสอบแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="b23bc-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="b23bc-440">บริษัทผู้ผลิตซึ่งผลิตคุกกี้ใช้การทดสอบตรวจสอบสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="b23bc-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b23bc-441">การทดสอบตรวจสอบนี้มีหลายตัวแปร</span><span class="sxs-lookup"><span data-stu-id="b23bc-441">This inspection test has several variables.</span></span> <span data-ttu-id="b23bc-442">ตัวแปรเป็นรส และผลลัพธ์ที่เป็นไปได้สำหรับตัวแปรนี้คืออร่อยและไม่อร่อย</span><span class="sxs-lookup"><span data-stu-id="b23bc-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b23bc-443">ตัวแปรที่สองคือสี และผลลัพธ์ที่เป็นไปได้คือเข้มเกินไป อ่อนเกินไป และพอดี</span><span class="sxs-lookup"><span data-stu-id="b23bc-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b23bc-444">ผลที่ได้ของตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="b23bc-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="b23bc-445">ใช้หน้านี้เพื่อตั้งค่า แก้ไข และดูผลการทดสอบที่เป็นไปได้ของตัวแปรทดสอบที่เกี่ยวข้องกับการทดสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="b23bc-446">สำหรับแต่ละผลลัพธ์ คุณกำหนดสถานะ <strong>ผ่าน</strong> หรือ <strong>ล้มเหลว</strong></span><span class="sxs-lookup"><span data-stu-id="b23bc-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="b23bc-447">คุณต้องกำหนดตัวแปรและผลของตัวแปรนั้นสำหรับการทดสอบแต่ละเชิงคุณภาพที่กำหนดในหน้า <strong>ทดสอบ</strong></span><span class="sxs-lookup"><span data-stu-id="b23bc-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b23bc-448">(สำหรับการทดสอบเชิงคุณภาพ ชนิดการทดสอบถูกตั้งค่าเป็น <strong>ตัวเลือก</strong> ในหน้า<strong>ทดสอบ</strong> ใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดตัวแปรทดสอบและผลลัพธ์เริ่มต้นไปยังการทดสอบเชิงคุณภาพแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="b23bc-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="b23bc-449">บริษัทผู้ผลิตซึ่งผลิตคุกกี้ใช้การทดสอบตรวจสอบสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="b23bc-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b23bc-450">การทดสอบตรวจสอบนี้มีหลายตัวแปร</span><span class="sxs-lookup"><span data-stu-id="b23bc-450">This inspection test has of several variables.</span></span> <span data-ttu-id="b23bc-451">ตัวแปรเป็นรส และผลลัพธ์ที่เป็นไปได้สำหรับตัวแปรนี้คืออร่อยและไม่อร่อย</span><span class="sxs-lookup"><span data-stu-id="b23bc-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b23bc-452">ตัวแปรที่สองคือสี และผลลัพธ์ที่เป็นไปได้คือเข้มเกินไป อ่อนเกินไป และพอดี</span><span class="sxs-lookup"><span data-stu-id="b23bc-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="b23bc-453">สถานะของ <strong>ผ่าน</strong> หรือ <strong>ล้มเหลว</strong> ถูกกำหนดไปยังแต่ละผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b23bc-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="b23bc-454">ในระหว่างการทดสอบตรวจสอบตัวแปรแต่ละตัว ผู้ตรวจสอบจะรายงานผลการทดสอบโดยการเลือกจากผลที่ได้อันใดอันหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b23bc-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="b23bc-455">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b23bc-455">Additional resources</span></span>
--------

[<span data-ttu-id="b23bc-456">กระบวนการการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b23bc-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="b23bc-457">การเปิดใช้งานการจัดการไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b23bc-457">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
