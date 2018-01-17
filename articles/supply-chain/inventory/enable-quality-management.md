---
title: "ภาพรวมการจัดการคุณภาพ"
description: "หัวข้อนี้อธิบายวิธีที่คุณสามารถใช้การจัดการคุณภาพใน Microsoft Dynamics 365 for Finance and Operations เพื่อช่วยปรับปรุงคุณภาพผลิตภัณฑ์ภายในห่วงโซ่อุปทานของคุณ"
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 517ec53695ccf46f57bc1f379036d635c4fea24f
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="quality-management-overview"></a><span data-ttu-id="fc233-103">ภาพรวมการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-103">Quality management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fc233-104">หัวข้อนี้อธิบายวิธีที่คุณสามารถใช้การจัดการคุณภาพใน Microsoft Dynamics 365 for Finance and Operations เพื่อช่วยปรับปรุงคุณภาพผลิตภัณฑ์ภายในห่วงโซ่อุปทานของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc233-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="fc233-105">การจัดการคุณภาพสามารถช่วยให้คุณจัดการระยะเวลาเมื่อคุณจัดการผลิตภัณฑ์ที่ไม่สอดคล้องกันโดยไม่คำนึงถึงจุดกำเนิด</span><span class="sxs-lookup"><span data-stu-id="fc233-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="fc233-106">เนื่องจากชนิดของการวินิจฉัยเชื่อมโยงกับการแก้ไขรายงาน Microsoft Dynamics 365 for Finance and Operations สามารถจัดกำหนดการงานเพื่อแก้ไขปัญหาและป้องกันการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="fc233-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="fc233-107">นอกเหนือจากฟังก์ชันสำหรับการจัดการไม่สอดคล้องกัน การจัดการคุณภาพรวมถึงฟังก์ชันสำหรับการติดตามปัญหาตามชนิดของปัญหา (แม้กระทั่งปัญหาภายใน), และสำหรับ การระบุโซลูชันระยะสั้นหรือระยะยาว</span><span class="sxs-lookup"><span data-stu-id="fc233-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="fc233-108">สถิติเกี่ยวกับตัวบ่งชี้ประสิทธิภาพหลัก (KPIs) ให้เข้าใจเกี่ยวกับประวัติของปัญหาความไม่สอดคล้องก่อนหน้านี้และโซลูชันที่ใช้เพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="fc233-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="fc233-109">คุณสามารถใช้ข้อมูลในอดีตเพื่อตรวจทานประสิทธิภาพของตัวชี้วัดคุณภาพก่อนหน้านี้และกำหนดตัวชี้วัดคุณภาพที่เหมาะสมเพื่อใช้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="fc233-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="fc233-110">เมื่อคุณตั้งค่าการเชื่อมโยงคุณภาพ Finance and Operations สามารถสร้างใบสั่งตรวจสอบคุณภาพสำหรับกระบวนการทางธุรกิจ เหตุการณ์ และเงื่อนไขต่างๆ</span><span class="sxs-lookup"><span data-stu-id="fc233-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="fc233-111">การเชื่อมโยงคุณภาพสามารถครอบคลุมสินค้าเฉพาะ กลุ่มสินค้าเฉพาะ หรือสินค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc233-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="fc233-112">ตัวอย่างของการใช้การจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-112">Examples of the use of quality management</span></span>
<span data-ttu-id="fc233-113">การจัดการคุณภาพเป็นแบบยืดหยุ่นและสามารถนำมาใช้ในวิธีการต่าง ๆ เพื่อให้ตรงกับความต้องการของระดับเฉพาะของการดำเนินงานห่วงโซ่อุปทาน</span><span class="sxs-lookup"><span data-stu-id="fc233-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="fc233-114">ตัวอย่างต่อไปนี้จะแสดงให้เห็นการใช้ที่เป็นไปได้ของลักษณะการทำงาน:</span><span class="sxs-lookup"><span data-stu-id="fc233-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="fc233-115">เริ่มต้นกระบวนการควบคุมคุณภาพโดยอัตโนมัติ ตามเกณฑ์ที่กำหนดไว้ล่วงหน้า (เมื่อมีการลงทะเบียนคลังสินค้าของใบสั่งซื้อจากผู้จัดจำหน่ายเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="fc233-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="fc233-116">บล็อคสินค้าคงคลังในระหว่างการตรวจสอบเพื่อป้องกันไม่ให้สินค้าคงคลังที่ไม่ได้รับการอนุมัติจากการถูกใช้ (การบล็อคทั้งหมดของปริมาณใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="fc233-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="fc233-117">ใช้การสุ่มตัวอย่างสินค้าเป็นส่วนหนึ่งของการเชื่อมโยงคุณภาพเพื่อกำหนดจำนวนของสินค้าคงคลังที่มีอยู่จริงปัจจุบันที่จะต้องตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="fc233-118">การสุ่มตัวอย่างอาจขึ้นอยู่กับปริมาณคงที่หรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="fc233-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="fc233-119">สร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับสินค้าเป็นบางส่วน</span><span class="sxs-lookup"><span data-stu-id="fc233-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="fc233-120">เมื่อต้องการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่รับจริงตามใบสั่ง คุณจะต้องเลือกกล่องกาเครื่องหมาย **ต่อปริมาณที่อัพเดต** บนแบบฟอร์ม **การสุ่มตัวอย่างสินค้า**</span><span class="sxs-lookup"><span data-stu-id="fc233-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="fc233-121">สร้างชนิดของการทดสอบที่มีค่าต่ำสุด สูงสุด และค่าเป้าหมายของการทดสอบ และทำการทดสอบเชิงคุณภาพเทียบกับเชิงปริมาณที่มีผลลัพธ์การตรวจสอบความถูกต้องที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="fc233-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="fc233-122">ระบุถึงระดับคุณภาพที่ยอมรับได้ (AQL) เพื่อควบคุมการยอมรับตัวชี้วัดคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="fc233-123">ระบุทรัพยากรที่ต้องมีการดำเนินการตรวจสอบ เช่นพื้นที่ทดสอบและเครื่องมือทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="fc233-124">การทำงานกับการเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-124">Working with quality associations</span></span>
<span data-ttu-id="fc233-125">กระบวนการทางธุรกิจที่ใช้การเชื่อมโยงคุณภาพอาจเกี่ยวข้องกับเอกสารต้นทางต่าง ๆ เช่นใบสั่งซื้อ ใบสั่งขาย หรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="fc233-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="fc233-126">แต่ละเรกคอร์ดความสัมพันธ์ของคุณภาพกำหนดชุดของการทดสอบ AQL และแผนการสุ่มตัวอย่างที่ใช้กับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fc233-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="fc233-127">คุณต้องกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="fc233-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="fc233-128">ตัวอย่างเช่น คุณสามารถตั้งค่าการเชื่อมโยงคุณภาพที่สร้างใบสั่งตรวจสอบคุณภาพเมื่อมีการอัพเดตใบรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc233-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="fc233-129">ขึ้นอยู่กับการตั้งค่าของแผนปฏิบัติการ ทริกเกอร์ดำเนินการด้วยตัวเองสามารถถูกบล็อคในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ หรือกระบวนการถัดไป เช่นการออกอินวอยซ์ใบสั้งซื้อ สามารถถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="fc233-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="fc233-130">**หมายเหตุ:** ในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ ปริมาณสินค้าคงคลังจะถูกถูกบล็อคจากการออกใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fc233-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="fc233-131">ขึ้นอยู่กับการตั้งค่า **การบล็อคทั้งหมด** บนหน้า **การสุ่มตัวอย่างสินค้า** ปริมาณเป็นปริมาณในใบสั่งตรวจสอบคุณภาพ หรือปริมาณในรายการเอกสารต้นทาง</span><span class="sxs-lookup"><span data-stu-id="fc233-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="fc233-132">สำหรับกระบวนการทางธุรกิจที่ระบุ เรกคอร์ดความสัมพันธ์ของคุณภาพจะระบุเหตุการณ์และเงื่อนไขที่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="fc233-133">เงื่อนไขอาจเป็นเฉพาะสำหรับไซต์หรือนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="fc233-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="fc233-134">สามารถสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับการทดสอบแบบทำลายเฉพาะเมื่อสินค้าคงคลังคงเหลือที่มีอยู่สำหรับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="fc233-135">ตัวอย่างต่อไปนี้อธิบายวิธีกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรในแต่ละกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="fc233-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="fc233-136">สำหรับแต่ละตัวอย่าง ตารางต่อไปนี้สรุปเหตุการณ์และเงื่อนไขที่กำหนดโดยเรกคอร์ดความสัมพันธ์ของคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="fc233-137">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="fc233-137">Reference type</span></span></th>
<th><span data-ttu-id="fc233-138">ชนิดเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-138">Event type</span></span></th>
<th><span data-ttu-id="fc233-139">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="fc233-139">Execution</span></span></th>
<th><span data-ttu-id="fc233-140">การบล็อคเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-140">Event blocking</span></span></th>
<th><span data-ttu-id="fc233-141">การอ้างอิงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="fc233-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="fc233-142">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-142">Inventory</span></span></td>
<td><span data-ttu-id="fc233-143">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fc233-143">Not applicable</span></span></td>
<td><span data-ttu-id="fc233-144">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fc233-144">Not applicable</span></span></td>
<td><span data-ttu-id="fc233-145">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-145">None</span></span></td>
<td><span data-ttu-id="fc233-146">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc233-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="fc233-147">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="fc233-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="fc233-148">กระบวนการเบิกสินค้าถูกจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="fc233-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="fc233-149">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-149">Before</span></span></td>
<td><span data-ttu-id="fc233-150">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="fc233-151">รหัส กลุ่ม หรือทั้งหมด เฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fc233-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-152">กระบวนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-153">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc233-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-154">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc233-155">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc233-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-156">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-156">Before</span></span></td>
<td><span data-ttu-id="fc233-157">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-158">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc233-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-159">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="fc233-160">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc233-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="fc233-161">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="fc233-162">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-162">Before</span></span></td>
<td><span data-ttu-id="fc233-163">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-164">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-165">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-166">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc233-167">หลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-167">After</span></span></td>
<td><span data-ttu-id="fc233-168">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-169">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-170">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc233-171">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="fc233-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-172">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fc233-172">Not applicable</span></span></td>
<td><span data-ttu-id="fc233-173">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-174">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-175">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="fc233-176">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-177">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-177">Before</span></span></td>
<td><span data-ttu-id="fc233-178">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-179">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-180">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc233-181">หลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-181">After</span></span></td>
<td><span data-ttu-id="fc233-182">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-183">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="fc233-184">การผลิต</span><span class="sxs-lookup"><span data-stu-id="fc233-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-185">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="fc233-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-186">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fc233-186">Not applicable</span></span></td>
<td><span data-ttu-id="fc233-187">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="fc233-188">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc233-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-189">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-190">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="fc233-191">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-192">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-192">Before</span></span></td>
<td><span data-ttu-id="fc233-193">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-194">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-195">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc233-196">หลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-196">After</span></span></td>
<td><span data-ttu-id="fc233-197">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-198">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="fc233-199">การตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-200">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="fc233-201">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-201">Before</span></span></td>
<td><span data-ttu-id="fc233-202">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-203">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-204">หลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-204">After</span></span></td>
<td><span data-ttu-id="fc233-205">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-206">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-206">End</span></span></td>
<td><span data-ttu-id="fc233-207">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-207">Before</span></span></td>
<td><span data-ttu-id="fc233-208">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc233-209">ขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="fc233-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-210">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="fc233-211">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-211">Before</span></span></td>
<td><span data-ttu-id="fc233-212">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-213">รหัส กลุ่ม หรือทั้งหมดเฉพาะ และระบุทรัพยากร กลุ่ม หรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc233-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-214">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-215">หลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-215">After</span></span></td>
<td><span data-ttu-id="fc233-216">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fc233-217">การผลิตสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="fc233-217">Co-product production</span></span></td>
<td><span data-ttu-id="fc233-218">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="fc233-218">Registration</span></span></td>
<td><span data-ttu-id="fc233-219">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fc233-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-220">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="fc233-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="fc233-221">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc233-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fc233-222">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fc233-222">Report as finished</span></span></td>
<td><span data-ttu-id="fc233-223">ก่อน</span><span class="sxs-lookup"><span data-stu-id="fc233-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-224">หลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fc233-225">ตารางต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างใบสั่งตรวจสอบคุณภาพสามารถสำหรับชนิดเฉพาะของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="fc233-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="fc233-226">ชนิดของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="fc233-226">Type of process</span></span></th>
<th><span data-ttu-id="fc233-227">เมื่อใบสั่งตรวจสอบคุณภาพสามารถถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fc233-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="fc233-228">เมื่อใบสั่งตรวจสอบคุณภาพสามารถสร้างหากการทดสอบแบบทำลายจำเป็น</span><span class="sxs-lookup"><span data-stu-id="fc233-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="fc233-229">ข้อมูลเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="fc233-229">Condition information</span></span></th>
<th><span data-ttu-id="fc233-230">ข้อมูลการสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="fc233-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="fc233-231">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc233-231">Purchase order</span></span></td>
<td><span data-ttu-id="fc233-232">ก่อนหรือหลังรายการรับสินค้าหรือใบรับสินค้าสำหรับวัสดุที่ได้รับจะมีการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="fc233-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="fc233-233">หลังจากใบรับสินค้าสำหรับวัสดุที่ได้รับมีการลงรายการบัญชี เนื่องจากวัสดุต้องพร้อมใช้งานสำหรับการทดสอบแบบทำลาย</span><span class="sxs-lookup"><span data-stu-id="fc233-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="fc233-234">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="fc233-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="fc233-235">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-236">ใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-236">Quarantine order</span></span></td>
<td><span data-ttu-id="fc233-237">ก่อน หรือหลัง ใบสั่งตรวจสอบสินค้ามีการรายงานเสร็จสิ้นแล้วหรือสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc233-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="fc233-238">ใบสั่งตรวจสอบคุณภาพที่ต้องการการทดสอบแบบทำลายไม่สามารถที่จะสร้าง</span><span class="sxs-lookup"><span data-stu-id="fc233-238">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="fc233-239">สมมติว่า ฟังก์ชันใบสั่งตรวจสอบสินค้าจัดการการโอนการครอบครองวัสดุที่ถูกทำลาย</span><span class="sxs-lookup"><span data-stu-id="fc233-239">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="fc233-240">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="fc233-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="fc233-241">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งตรวจสอบสินค้าสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-242">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="fc233-242">Sales order</span></span></td>
<td><span data-ttu-id="fc233-243">ก่อนการจัดกำหนดการกระบวนการเบิกสินค้าหรืออัพเดตบันทึกสำหรับสินค้าที่กำลังจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc233-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="fc233-244">ในขั้นตอนใดๆ</span><span class="sxs-lookup"><span data-stu-id="fc233-244">At any step</span></span></td>
<td><span data-ttu-id="fc233-245">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือลูกค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="fc233-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="fc233-246">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-247">ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="fc233-247">Production order</span></span></td>
<td><span data-ttu-id="fc233-248">ก่อนหรือหลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="fc233-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="fc233-249">หลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="fc233-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="fc233-250">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="fc233-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="fc233-251">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-252">ใบสั่งผลิตที่มีขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="fc233-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="fc233-253">ก่อนหรือหลังจากรายงานการเสร็จสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="fc233-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="fc233-254">หลังจากการรายงานการผลิตเสร็จสิ้นแล้วสำหรับการดำเนินงานสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="fc233-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="fc233-255">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือทรัพยากรการดำเนินงาน หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="fc233-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="fc233-256">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับขั้นตอนของกระบวนการผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fc233-257">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="fc233-257">Inventory</span></span></td>
<td><span data-ttu-id="fc233-258">ใบสั่งตรวจสอบคุณภาพไม่สามารถถูกสร้างขึ้นโดยอัตโนมัติสำหรับธุรกรรมในสมุดรายวันสินค้าคงคลังหรือธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="fc233-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="fc233-259">ใบสั่งตรวจสอบคุณภาพต้องสร้างด้วยตนเองสำหรับปริมาณสินค้าคงคลังของสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-259">A quality order must be created manually for an item's inventory quantity.</span></span> <span data-ttu-id="fc233-260">จำเป็นต้องมีปริมาณสินค้าคงคลังคงเหลือที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="fc233-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="fc233-261">หน้าการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc233-262">หน้า</span><span class="sxs-lookup"><span data-stu-id="fc233-262">Page</span></span></th>
<th><span data-ttu-id="fc233-263">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="fc233-263">Description</span></span></th>
<th><span data-ttu-id="fc233-264">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fc233-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc233-265">การเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-265">Quality associations</span></span></td>
<td><span data-ttu-id="fc233-266">ดูส่วนก่อนหน้าของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="fc233-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="fc233-267">ความสัมพันธ์ของคุณภาพกำหนดข้อมูลต่อไปนี้ทั้งหมดสำหรับใบสั่งตรวจสอบคุณภาพที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="fc233-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="fc233-268">เหตุการณ์ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="fc233-268">The transaction event</span></span></li>
<li><span data-ttu-id="fc233-269">ชุดของการทดสอบที่ต้องดำเนินการบนสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="fc233-270">AQL</span><span class="sxs-lookup"><span data-stu-id="fc233-270">The AQL</span></span></li>
<li><span data-ttu-id="fc233-271">แผนการสุ่มตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fc233-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="fc233-272">คุณต้องกำหนดคำความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจที่จำเป็นต้องมีการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fc233-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="fc233-273">ตัวอย่างเช่น สามารถสร้างใบสั่งตรวจสอบคุณภาพในกระบวนการทางธุรกิจสำหรับใบสั่งซื้อ ใบสั่งตรวจสอบสินค้า ใบสั่งขาย และใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="fc233-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc233-274">การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-274">Tests</span></span></td>
<td><span data-ttu-id="fc233-275">ใช้หน้านี้ในการกำหนดและดูการทดสอบแต่ละรายการที่กำหนดว่าผลิตภัณฑ์ของคุณตรงตามข้อมูลจำเพาะเกี่ยวกับคุณภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fc233-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="fc233-276">คุณสามารถกำหนดรายการทดสอบแต่ละรายการกับกลุ่มการทดสอบอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="fc233-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="fc233-277">ในกรณีนี้ คุณระบุข้อมูลเฉพาะตัวของการทดสอบ เช่นค่าการประเมินที่ยอมรับได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="fc233-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="fc233-278">ค่าการประเมินค่าจะใช้สำหรับการทดสอบเชิงปริมาณ และตัวแปรทดสอบที่จะใช้สำหรับการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="fc233-279">การทดสอบเชิงปริมาณมีชนิดการทดสอบของ <strong>จำนวนเต็ม</strong> หรือ <strong>เศษส่วน</strong> และยังมีการกำหนดหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="fc233-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="fc233-280">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="fc233-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="fc233-281">การทดสอบเชิงคุณภาพจะมีชนิดของ <strong>ตัวเลือก</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc233-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="fc233-282">การทดสอบเชิงคุณภาพต้องการข้อมูลเพิ่มเติมเกี่ยวกับตัวแปรการทดสอบที่วัดและตัวเลือกที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fc233-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="fc233-283">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงตามผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="fc233-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="fc233-284">บริษัทผู้ผลิตดำเนินการทดสอบวัสดุที่ซื้อสองแบบ: การทดสอบเชิงปริมาณเกี่ยวกับคุณภาพวัสดุและการทดสอบเชิงคุณภาพเกี่ยวกับความเสียหายของบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fc233-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="fc233-285">บริษัทกำหนดข้อมูลเพิ่มเติมเกี่ยวกับการทดสอบเชิงคุณภาพเพื่อระบุตัวแปรการทดสอบ (บรรจุภัณฑ์ที่เสียหาย) และผลลัพธ์ที่ได้</span><span class="sxs-lookup"><span data-stu-id="fc233-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="fc233-286">บริษัทใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดการทดสอบทั้งสองให้กับกลุ่มการทดสอบและเพื่อระบุข้อมูลเฉพาะตัวของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="fc233-287">กลุ่มทดสอบจะถูกกำหนดให้ใบสั่งตรวจสอบคุณภาพ เพื่อให้บริษัทสามารถรายงานผลการทดสอบสำหรับการทดสอบทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="fc233-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc233-288">กลุ่มทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-288">Test groups</span></span></td>
<td><span data-ttu-id="fc233-289">ใช้หน้านี้เพื่อตั้งค่า แก้ไข และดูกลุ่มทดสอบและการทดสอบแต่ละรายการที่กำหนดให้กับกลุ่มทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="fc233-290">บานหน้าต่างด้านบนจะแสดงกลุ่มทดสอบ และบานหน้าต่างด้านล่างแสดงการทดสอบที่กำหนดให้กับกลุ่มการทดสอบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fc233-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="fc233-291">คุณกำหนดนโยบายต่าง ๆ ให้กับกลุ่มการทดสอบ เช่นแผนการสุ่มตัวอย่าง AQL และความต้องการสำหรับการทดสอบแบบทำลาย</span><span class="sxs-lookup"><span data-stu-id="fc233-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="fc233-292">เมื่อคุณกำหนดการทดสอบแต่ละรายการกับกลุ่มการทดสอบ คุณต้องกำหนดข้อมูลเพิ่มเติม เช่นลำดับ เอกสาร และวันที่ที่มีผลใช้</span><span class="sxs-lookup"><span data-stu-id="fc233-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="fc233-293">สำหรับการทดสอบเชิงปริมาณ ข้อมูลที่คุณกำหนดจะประกอบด้วยค่าการประเมินที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="fc233-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="fc233-294">สำหรับการทดสอบเชิงคุณภาพ ข้อมูลนี้รวมถึงตัวแปรทดสอบและผลลัพธ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fc233-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="fc233-295">กลุ่มการทดสอบที่กำหนดให้กับใบสั่งตรวจสอบคุณภาพกำหนดชุดค่าเริ่มต้นของการทดสอบที่ต้องดำเนินการกับสินค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fc233-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="fc233-296">อย่างไรก็ตาม คุณสามารถเพิ่ม ลบ หรือเปลี่ยนการทดสอบบนใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="fc233-297">ผลการทดสอบจะรายงานสำหรับการทดสอบแต่ละรายการบนใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="fc233-298">บริษัทผู้ผลิตกำหนดกลุ่มการทดสอบสำหรับความผันแปรต่าง ๆ ของคำแนะนำเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="fc233-299">กลุ่มการทดสอบต่าง ๆ สะท้อนถึงผลต่างในแผนการสุ่มตัวอย่าง ชุดของการทดสอบที่ต้องดำเนินการพร้อมกัน AQL และปัจจัยอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="fc233-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="fc233-300">สำหรับการทดสอบเชิงปริมาณ ยังมความแตกต่างของค่าการประเมินที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="fc233-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="fc233-301">เพื่อบังคับใช้คำแนะนำด้านคุณภาพ บริษัทกำหนดกลุ่มการทดสอบสำหรับแต่ละกฎสำหรับการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติในหน้า <strong>ความสัมพันธ์ของคุณภาพ</strong> และยังกำหนดกลุ่มการทดสอบสำหรับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="fc233-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc233-302">กลุ่มคุณภาพสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-302">Item quality groups</span></span></td>
<td><span data-ttu-id="fc233-303">ตั้งค่า แก้ไข และดูสินค้าที่กำหนดให้กับกลุ่มคุณภาพหนึ่งหรือหลายกลุ่ม ซึ่งมีการกำหนดให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="fc233-304">กลุ่มคุณภาพแสดงข้อกำหนดในการทดสอบทั่วไปสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="fc233-305">หลังจากที่คุณกำหนดความต้องการทดสอบบนหน้า <strong>กลุ่มทดสอบ</strong> คุณสามารถกำหนดกฎสำหรับการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="fc233-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="fc233-306">เพื่อทำให้กระบวนการ คุณไม่กำหนดกฎสำหรับสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="fc233-306">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="fc233-307">คุณกำหนดกฎสำหรับกลุ่มคุณภาพโดยการใช้หน้า <strong>ความสัมพันธ์ของคุณภาพ</strong> แทน</span><span class="sxs-lookup"><span data-stu-id="fc233-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="fc233-308">คุณยังสามารถใช้หน้า <strong>กลุ่มคุณภาพสินค้า</strong> สำหรับกลุ่มคุณภาพที่เลือกเพื่อกำหนดสินค้าที่เกี่ยวข้องกับกลุ่มนั้นได้</span><span class="sxs-lookup"><span data-stu-id="fc233-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="fc233-309">คุณยังสามารถใช้หน้า <strong>กลุ่มคุณภาพสินค้า</strong> สำหรับกลุ่มคุณภาพที่เลือกเพื่อกำหนดสินค้าที่เกี่ยวข้องกับกลุ่มนั้นได้</span><span class="sxs-lookup"><span data-stu-id="fc233-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="fc233-310">บริษัทผู้ผลิตจัดซื้อวัตถุดิบหลายอย่างที่มีการทดสอบสำหรับสินค้าสำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="fc233-311">บริษัทกำหนดกลุ่มคุณภาพและกำหนดหมายเลขสินค้าที่เกี่ยวข้องกับวัตถุดิบสำหรับกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="fc233-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="fc233-312">ภายหลัง บริษัทสั่งซื้อวัตถุดิบชนิดใหม่ที่มีความต้องการทดสอบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="fc233-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="fc233-313">แทนที่จะติดตั้งข้อกำหนดในการทดสอบใหม่สำหรับวัสดุใหม่ บริษัทเพิ่มหมายเลขสินค้าสำหรับวัสดุใหม่ให้กับกลุ่มคุณภาพที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="fc233-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="fc233-314">บริษัทผู้ผลิตเดียวกันนี้ยังผลิตสินค้าที่มี มีข้อกำหนดในการทดสอบเดียวกันและจัดส่งสินค้าที่มีข้อกำหนดแบบเดียวกันในการทดสอบก่อนจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc233-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="fc233-315">บริษัทกำหนดกลุ่มคุณภาพเพิ่มเติมสองกลุ่มและกำหนดหมายเลขสินค้าที่เกี่ยวข้องให้กับกลุ่มคุณภาพแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="fc233-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc233-316">ตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-316">Test variables</span></span></td>
<td><span data-ttu-id="fc233-317">ใช้หน้านี้เพื่อกำหนดหรือดูตัวแปรที่เชื่อมโยงกับการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="fc233-318">สำหรับแต่ละตัวแปร คุณกำหนดผลที่ได้ที่ระบุไว้แสดงถึงตัวเลือกที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="fc233-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="fc233-319">คุณกำหนดทดสอบบนหน้า <strong>ทดสอบ</strong></span><span class="sxs-lookup"><span data-stu-id="fc233-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="fc233-320">สำหรับการทดสอบเชิงคุณภาพ คุณต้องตั้งค่าชนิดของการทดสอบเป็น <strong>ตัวเลือก</strong></span><span class="sxs-lookup"><span data-stu-id="fc233-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="fc233-321">ใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดตัวแปรการทดสอบในการทดสอบแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="fc233-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="fc233-322">บริษัทผู้ผลิตซึ่งผลิตคุกกี้ใช้การทดสอบตรวจสอบสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="fc233-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="fc233-323">การทดสอบตรวจสอบนี้มีหลายตัวแปร</span><span class="sxs-lookup"><span data-stu-id="fc233-323">This inspection test has several variables.</span></span> <span data-ttu-id="fc233-324">ตัวแปรเป็นรส และผลลัพธ์ที่เป็นไปได้สำหรับตัวแปรนี้คืออร่อยและไม่อร่อย</span><span class="sxs-lookup"><span data-stu-id="fc233-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="fc233-325">ตัวแปรที่สองคือสี และผลลัพธ์ที่เป็นไปได้คือเข้มเกินไป อ่อนเกินไป และพอดี</span><span class="sxs-lookup"><span data-stu-id="fc233-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc233-326">ผลที่ได้ของตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="fc233-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="fc233-327">ใช้หน้านี้เพื่อตั้งค่า แก้ไข และดูผลการทดสอบที่เป็นไปได้ของตัวแปรทดสอบที่เกี่ยวข้องกับการทดสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="fc233-328">สำหรับแต่ละผลลัพธ์ คุณกำหนดสถานะ <strong>ผ่าน</strong> หรือ <strong>ล้มเหลว</strong></span><span class="sxs-lookup"><span data-stu-id="fc233-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="fc233-329">คุณต้องกำหนดตัวแปรและผลของตัวแปรนั้นสำหรับการทดสอบแต่ละเชิงคุณภาพที่กำหนดในหน้า <strong>ทดสอบ</strong></span><span class="sxs-lookup"><span data-stu-id="fc233-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="fc233-330">(สำหรับการทดสอบเชิงคุณภาพ ชนิดการทดสอบถูกตั้งค่าเป็น <strong>ตัวเลือก</strong> ในหน้า<strong>ทดสอบ</strong> ใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดตัวแปรทดสอบและผลลัพธ์เริ่มต้นไปยังการทดสอบเชิงคุณภาพแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="fc233-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="fc233-331">บริษัทผู้ผลิตซึ่งผลิตคุกกี้ใช้การทดสอบตรวจสอบสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="fc233-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="fc233-332">การทดสอบตรวจสอบนี้มีหลายตัวแปร</span><span class="sxs-lookup"><span data-stu-id="fc233-332">This inspection test has of several variables.</span></span> <span data-ttu-id="fc233-333">ตัวแปรเป็นรส และผลลัพธ์ที่เป็นไปได้สำหรับตัวแปรนี้คืออร่อยและไม่อร่อย</span><span class="sxs-lookup"><span data-stu-id="fc233-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="fc233-334">ตัวแปรที่สองคือสี และผลลัพธ์ที่เป็นไปได้คือเข้มเกินไป อ่อนเกินไป และพอดี</span><span class="sxs-lookup"><span data-stu-id="fc233-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="fc233-335">สถานะของ <strong>ผ่าน</strong> หรือ <strong>ล้มเหลว</strong> ถูกกำหนดไปยังแต่ละผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="fc233-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="fc233-336">ในระหว่างการทดสอบตรวจสอบตัวแปรแต่ละตัว ผู้ตรวจสอบจะรายงานผลการทดสอบโดยการเลือกจากผลที่ได้อันใดอันหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fc233-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="fc233-337">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="fc233-337">See also</span></span>
--------

[<span data-ttu-id="fc233-338">กระบวนการการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="fc233-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="fc233-339">การเปิดใช้งานการจัดการไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="fc233-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

