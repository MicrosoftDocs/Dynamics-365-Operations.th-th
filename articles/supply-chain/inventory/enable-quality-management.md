---
title: ภาพรวมการจัดการคุณภาพ
description: หัวข้อนี้อธิบายวิธีที่คุณสามารถใช้การจัดการคุณภาพใน Dynamics 365 Supply Chain Management เพื่อช่วยพัฒนาคุณภาพผลิตภัณฑ์ภายในห่วงโซ่อุปทานของคุณ
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65858838b0fbb245a9330fab4e3b65b36a9eb944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219376"
---
# <a name="quality-management-overview"></a><span data-ttu-id="84269-103">ภาพรวมการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84269-104">หัวข้อนี้อธิบายวิธีที่คุณสามารถใช้การจัดการคุณภาพใน Dynamics 365 Supply Chain Management เพื่อช่วยพัฒนาคุณภาพผลิตภัณฑ์ภายในห่วงโซ่อุปทานของคุณ</span><span class="sxs-lookup"><span data-stu-id="84269-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="84269-105">การจัดการคุณภาพสามารถช่วยให้คุณจัดการระยะเวลาเมื่อคุณจัดการผลิตภัณฑ์ที่ไม่สอดคล้องกันโดยไม่คำนึงถึงจุดกำเนิด</span><span class="sxs-lookup"><span data-stu-id="84269-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="84269-106">เนื่องจากชนิดของการวินิจฉัยเชื่อมโยงกับการแก้ไขรายงาน Supply Chain Management สามารถจัดกำหนดการงานเพื่อแก้ไขปัญหาและป้องกันการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="84269-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="84269-107">นอกเหนือจากฟังก์ชันสำหรับการจัดการไม่สอดคล้องกัน การจัดการคุณภาพรวมถึงฟังก์ชันสำหรับการติดตามปัญหาตามชนิดของปัญหา (แม้กระทั่งปัญหาภายใน), และสำหรับ การระบุโซลูชันระยะสั้นหรือระยะยาว</span><span class="sxs-lookup"><span data-stu-id="84269-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="84269-108">สถิติเกี่ยวกับตัวบ่งชี้ประสิทธิภาพหลัก (KPIs) ให้เข้าใจเกี่ยวกับประวัติของปัญหาความไม่สอดคล้องก่อนหน้านี้และโซลูชันที่ใช้เพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="84269-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="84269-109">คุณสามารถใช้ข้อมูลในอดีตเพื่อตรวจทานประสิทธิภาพของตัวชี้วัดคุณภาพก่อนหน้านี้และกำหนดตัวชี้วัดคุณภาพที่เหมาะสมเพื่อใช้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="84269-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="84269-110">เมื่อคุณตั้งค่าการเชื่อมโยงคุณภาพ Supply Chain Management สามารถสร้างใบสั่งตรวจสอบคุณภาพสำหรับกระบวนการทางธุรกิจ เหตุการณ์ และเงื่อนไขต่างๆ</span><span class="sxs-lookup"><span data-stu-id="84269-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="84269-111">การเชื่อมโยงคุณภาพสามารถครอบคลุมสินค้าเฉพาะ กลุ่มสินค้าเฉพาะ หรือสินค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84269-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="84269-112">ตัวอย่างของการใช้การจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-112">Examples of the use of quality management</span></span>
<span data-ttu-id="84269-113">การจัดการคุณภาพเป็นแบบยืดหยุ่นและสามารถนำมาใช้ในวิธีการต่าง ๆ เพื่อให้ตรงกับความต้องการของระดับเฉพาะของการดำเนินงานห่วงโซ่อุปทาน</span><span class="sxs-lookup"><span data-stu-id="84269-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="84269-114">ตัวอย่างต่อไปนี้จะแสดงให้เห็นการใช้ที่เป็นไปได้ของลักษณะการทำงาน:</span><span class="sxs-lookup"><span data-stu-id="84269-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="84269-115">เริ่มต้นกระบวนการควบคุมคุณภาพโดยอัตโนมัติ ตามเกณฑ์ที่กำหนดไว้ล่วงหน้า (เมื่อมีการลงทะเบียนคลังสินค้าของใบสั่งซื้อจากผู้จัดจำหน่ายเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="84269-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="84269-116">บล็อคสินค้าคงคลังในระหว่างการตรวจสอบเพื่อป้องกันไม่ให้สินค้าคงคลังที่ไม่ได้รับการอนุมัติจากการถูกใช้ (การบล็อคทั้งหมดของปริมาณใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="84269-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="84269-117">ใช้การสุ่มตัวอย่างสินค้าเป็นส่วนหนึ่งของการเชื่อมโยงคุณภาพเพื่อกำหนดจำนวนของสินค้าคงคลังที่มีอยู่จริงปัจจุบันที่จะต้องตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="84269-118">การสุ่มตัวอย่างอาจขึ้นอยู่กับปริมาณคงที่ เปอร์เซ็นต์ หรือป้ายทะเบียนแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="84269-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="84269-119">คุณลักษณะ _การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า_ ขยายความสามารถของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="84269-120">ถ้าคุณกำลังใช้คุณลักษณะนี้ ให้ดูที่ [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](quality-management-for-warehouses-processes.md) สำหรับตัวอย่างของวิธีการที่การจัดการคุณภาพทำงาน เมื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="84269-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="84269-121">สร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับสินค้าเป็นบางส่วน</span><span class="sxs-lookup"><span data-stu-id="84269-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="84269-122">เมื่อต้องการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่รับจริงตามใบสั่ง คุณจะต้องเลือกกล่องกาเครื่องหมาย **ต่อปริมาณที่อัพเดต** บนแบบฟอร์ม **การสุ่มตัวอย่างสินค้า**</span><span class="sxs-lookup"><span data-stu-id="84269-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="84269-123">สร้างชนิดของการทดสอบที่มีค่าต่ำสุด สูงสุด และค่าเป้าหมายของการทดสอบ และทำการทดสอบเชิงคุณภาพเทียบกับเชิงปริมาณที่มีผลลัพธ์การตรวจสอบความถูกต้องที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="84269-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="84269-124">ระบุถึงระดับคุณภาพที่ยอมรับได้ (AQL) เพื่อควบคุมการยอมรับตัวชี้วัดคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="84269-125">ระบุทรัพยากรที่ต้องมีการดำเนินการตรวจสอบ เช่นพื้นที่ทดสอบและเครื่องมือทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="84269-126">การทำงานกับการเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-126">Working with quality associations</span></span>
<span data-ttu-id="84269-127">กระบวนการทางธุรกิจที่ใช้การเชื่อมโยงคุณภาพอาจเกี่ยวข้องกับเอกสารต้นทางต่าง ๆ เช่นใบสั่งซื้อ ใบสั่งขาย หรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="84269-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="84269-128">แต่ละเรกคอร์ดความสัมพันธ์ของคุณภาพกำหนดชุดของการทดสอบ AQL และแผนการสุ่มตัวอย่างที่ใช้กับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="84269-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="84269-129">คุณต้องกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="84269-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="84269-130">ตัวอย่างเช่น คุณสามารถตั้งค่าการเชื่อมโยงคุณภาพที่สร้างใบสั่งตรวจสอบคุณภาพเมื่อมีการอัพเดตใบรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="84269-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="84269-131">ขึ้นอยู่กับการตั้งค่าของแผนปฏิบัติการ ทริกเกอร์ดำเนินการด้วยตัวเองสามารถถูกบล็อคในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ หรือกระบวนการถัดไป เช่นการออกอินวอยซ์ใบสั้งซื้อ สามารถถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="84269-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="84269-132">**หมายเหตุ:** ในขณะที่มีใบสั่งตรวจสอบคุณภาพที่เปิดอยู่ ปริมาณสินค้าคงคลังจะถูกถูกบล็อคจากการออกใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="84269-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="84269-133">ขึ้นอยู่กับการตั้งค่า **การบล็อคทั้งหมด** บนหน้า **การสุ่มตัวอย่างสินค้า** ปริมาณเป็นปริมาณในใบสั่งตรวจสอบคุณภาพ หรือปริมาณในรายการเอกสารต้นทาง</span><span class="sxs-lookup"><span data-stu-id="84269-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="84269-134">สำหรับกระบวนการทางธุรกิจที่ระบุ เรกคอร์ดความสัมพันธ์ของคุณภาพจะระบุเหตุการณ์และเงื่อนไขที่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="84269-135">เงื่อนไขอาจเป็นเฉพาะสำหรับไซต์หรือนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="84269-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="84269-136">สามารถสร้างใบสั่งตรวจสอบคุณภาพที่เกี่ยวข้องกับการทดสอบแบบทำลายเฉพาะเมื่อสินค้าคงคลังคงเหลือที่มีอยู่สำหรับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="84269-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="84269-137">ตัวอย่างต่อไปนี้อธิบายวิธีกำหนดเรกคอร์ดความสัมพันธ์ของคุณภาพสำหรับความผันแปรในแต่ละกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="84269-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="84269-138">สำหรับแต่ละตัวอย่าง ตารางต่อไปนี้สรุปเหตุการณ์และเงื่อนไขที่กำหนดโดยเรกคอร์ดความสัมพันธ์ของคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="84269-139">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="84269-139">Reference type</span></span></th>
<th><span data-ttu-id="84269-140">ชนิดเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="84269-140">Event type</span></span></th>
<th><span data-ttu-id="84269-141">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="84269-141">Execution</span></span></th>
<th><span data-ttu-id="84269-142">การบล็อคเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="84269-142">Event blocking</span></span></th>
<th><span data-ttu-id="84269-143">การอ้างอิงเอกสาร</span><span class="sxs-lookup"><span data-stu-id="84269-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="84269-144">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="84269-144">Inventory</span></span></td>
<td><span data-ttu-id="84269-145">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="84269-145">Not applicable</span></span></td>
<td><span data-ttu-id="84269-146">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="84269-146">Not applicable</span></span></td>
<td><span data-ttu-id="84269-147">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-147">None</span></span></td>
<td><span data-ttu-id="84269-148">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84269-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="84269-149">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="84269-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="84269-150">กระบวนการเบิกสินค้าถูกจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="84269-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="84269-151">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-151">Before</span></span></td>
<td><span data-ttu-id="84269-152">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="84269-153">รหัส กลุ่ม หรือทั้งหมด เฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="84269-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-154">กระบวนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-155">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="84269-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-156">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="84269-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="84269-157">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="84269-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-158">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-158">Before</span></span></td>
<td><span data-ttu-id="84269-159">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-160">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="84269-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-161">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="84269-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="84269-162">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="84269-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="84269-163">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="84269-164">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-164">Before</span></span></td>
<td><span data-ttu-id="84269-165">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-166">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-167">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-168">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="84269-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="84269-169">หลัง</span><span class="sxs-lookup"><span data-stu-id="84269-169">After</span></span></td>
<td><span data-ttu-id="84269-170">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-171">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-172">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="84269-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="84269-173">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="84269-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-174">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="84269-174">Not applicable</span></span></td>
<td><span data-ttu-id="84269-175">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-176">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-177">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="84269-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="84269-178">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-179">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-179">Before</span></span></td>
<td><span data-ttu-id="84269-180">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-181">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-182">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="84269-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="84269-183">หลัง</span><span class="sxs-lookup"><span data-stu-id="84269-183">After</span></span></td>
<td><span data-ttu-id="84269-184">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-185">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="84269-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="84269-186">การผลิต</span><span class="sxs-lookup"><span data-stu-id="84269-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-187">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="84269-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-188">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="84269-188">Not applicable</span></span></td>
<td><span data-ttu-id="84269-189">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="84269-190">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84269-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-191">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-192">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="84269-193">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-194">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-194">Before</span></span></td>
<td><span data-ttu-id="84269-195">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-196">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-197">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="84269-198">หลัง</span><span class="sxs-lookup"><span data-stu-id="84269-198">After</span></span></td>
<td><span data-ttu-id="84269-199">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-200">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="84269-201">การตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-202">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="84269-203">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-203">Before</span></span></td>
<td><span data-ttu-id="84269-204">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-205">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-206">หลัง</span><span class="sxs-lookup"><span data-stu-id="84269-206">After</span></span></td>
<td><span data-ttu-id="84269-207">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-208">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-208">End</span></span></td>
<td><span data-ttu-id="84269-209">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-209">Before</span></span></td>
<td><span data-ttu-id="84269-210">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="84269-211">ขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="84269-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-212">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="84269-213">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-213">Before</span></span></td>
<td><span data-ttu-id="84269-214">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-215">รหัส กลุ่ม หรือทั้งหมดเฉพาะ และระบุทรัพยากร กลุ่ม หรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84269-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-216">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-217">หลัง</span><span class="sxs-lookup"><span data-stu-id="84269-217">After</span></span></td>
<td><span data-ttu-id="84269-218">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="84269-219">การผลิตสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="84269-219">Co-product production</span></span></td>
<td><span data-ttu-id="84269-220">การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="84269-220">Registration</span></span></td>
<td><span data-ttu-id="84269-221">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="84269-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-222">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="84269-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="84269-223">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84269-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="84269-224">รายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84269-224">Report as finished</span></span></td>
<td><span data-ttu-id="84269-225">ก่อน</span><span class="sxs-lookup"><span data-stu-id="84269-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-226">หลัง</span><span class="sxs-lookup"><span data-stu-id="84269-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="84269-227">ตารางต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างใบสั่งตรวจสอบคุณภาพสามารถสำหรับชนิดเฉพาะของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="84269-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="84269-228">ชนิดของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="84269-228">Type of process</span></span></th>
<th><span data-ttu-id="84269-229">เมื่อใบสั่งตรวจสอบคุณภาพสามารถถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="84269-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="84269-230">เมื่อใบสั่งตรวจสอบคุณภาพสามารถสร้างหากการทดสอบแบบทำลายจำเป็น</span><span class="sxs-lookup"><span data-stu-id="84269-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="84269-231">ข้อมูลเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="84269-231">Condition information</span></span></th>
<th><span data-ttu-id="84269-232">ข้อมูลการสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="84269-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="84269-233">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="84269-233">Purchase order</span></span></td>
<td><span data-ttu-id="84269-234">ก่อนหรือหลังรายการรับสินค้าหรือใบรับสินค้าสำหรับวัสดุที่ได้รับจะมีการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="84269-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="84269-235">หลังจากใบรับสินค้าสำหรับวัสดุที่ได้รับมีการลงรายการบัญชี เนื่องจากวัสดุต้องพร้อมใช้งานสำหรับการทดสอบแบบทำลาย</span><span class="sxs-lookup"><span data-stu-id="84269-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="84269-236">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="84269-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="84269-237">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-238">ใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-238">Quarantine order</span></span></td>
<td><span data-ttu-id="84269-239">ก่อน หรือหลัง ใบสั่งตรวจสอบสินค้ามีการรายงานเสร็จสิ้นแล้วหรือสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84269-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="84269-240">ใบสั่งคุณภาพที่ต้องการการทดสอบแบบหักล้างไม่&#39;สามารถถูกสร้างได้</span><span class="sxs-lookup"><span data-stu-id="84269-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="84269-241">ถือ&#39;ว่าฟังก์ชันใบสั่งการกักกันจัดการการจัดการของวัสดุที่ถูกทำลาย</span><span class="sxs-lookup"><span data-stu-id="84269-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="84269-242">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพอาจสะท้อนถึงไซต์ สินค้า หรือผู้จัดจำหน่าย หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="84269-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="84269-243">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งตรวจสอบสินค้าสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-244">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="84269-244">Sales order</span></span></td>
<td><span data-ttu-id="84269-245">ก่อนการจัดกำหนดการกระบวนการเบิกสินค้าหรืออัพเดตบันทึกสำหรับสินค้าที่กำลังจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="84269-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="84269-246">ในขั้นตอนใดๆ</span><span class="sxs-lookup"><span data-stu-id="84269-246">At any step</span></span></td>
<td><span data-ttu-id="84269-247">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือลูกค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="84269-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="84269-248">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งซื้อสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-249">ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="84269-249">Production order</span></span></td>
<td><span data-ttu-id="84269-250">ก่อนหรือหลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="84269-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="84269-251">หลังปริมาณที่เสร็จสิ้นสำหรับใบสั่งผลิตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="84269-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="84269-252">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="84269-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="84269-253">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับใบสั่งผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-254">ใบสั่งผลิตที่มีขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="84269-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="84269-255">ก่อนหรือหลังจากรายงานการเสร็จสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="84269-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="84269-256">หลังจากการรายงานการผลิตเสร็จสิ้นแล้วสำหรับการดำเนินงานสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="84269-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="84269-257">ความต้องการสำหรับใบสั่งตรวจสอบคุณภาพสามารถสะท้อนถึงไซต์ สินค้า หรือทรัพยากรการดำเนินงาน หรือชุดของเงื่อนไขเหล่านี้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="84269-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="84269-258">ใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นด้วยตนเองซึ่งอ้างอิงกับขั้นตอนของกระบวนการผลิตสามารถใช้ข้อมูลในเรกคอร์ดความสัมพันธ์ของคุณภาพ เช่นแผนการสุ่มตัวอย่างของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="84269-259">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="84269-259">Inventory</span></span></td>
<td><span data-ttu-id="84269-260">ใบสั่งตรวจสอบคุณภาพไม่สามารถถูกสร้างขึ้นโดยอัตโนมัติสำหรับธุรกรรมในสมุดรายวันสินค้าคงคลังหรือธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="84269-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="84269-261">ใบสั่งคุณภาพต้องถูกสร้างด้วยตนเองสำหรับปริมาณสินค้าคงคลังของ&#39;สินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="84269-262">จำเป็นต้องมีปริมาณสินค้าคงคลังคงเหลือที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="84269-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="84269-263">ตัวอย่างการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="84269-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="84269-264">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="84269-264">Purchasing</span></span>

<span data-ttu-id="84269-265">ในการซื้อ หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น **ใบรับสินค้า** และฟิลด์ **การดำเนินการ** เป็น **ภายหลัง** บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="84269-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="84269-266">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ใช่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกการรับสินค้าต่อใบสั่งซื้อ ตามปริมาณที่รับและการตั้งค่าในสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="84269-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="84269-267">ทุกครั้งที่มีการรับปริมาณต่อใบสั่งซื้อ จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่รับมาใหม่</span><span class="sxs-lookup"><span data-stu-id="84269-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="84269-268">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ไม่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับสินค้ารายการแรกต่อใบสั่งซื้อ ตามปริมาณที่รับ</span><span class="sxs-lookup"><span data-stu-id="84269-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="84269-269">นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="84269-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="84269-270">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับการรับต่อใบสั่งซื้อหลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="84269-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="84269-271">การใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="84269-271">Production</span></span>

<span data-ttu-id="84269-272">ในการผลิต หากคุณตั้งค่าฟิลด์ **ชนิดเหตุการณ์** เป็น **รายงานเป็นเสร็จสิ้น** และฟิลด์ **การดำเนินการ** เป็น **ภายหลัง** บนเพจ **การเชื่อมโยงคุณภาพ** คุณจะได้ผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="84269-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="84269-273">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ใช่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับทุกปริมาณที่เสร็จสิ้นและการตั้งค่าในสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="84269-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="84269-274">ทุกครั้งที่มีการรายงานปริมาณเป็นเสร็จสิ้นต่อใบสั่งผลิต จะมีการสร้างใบสั่งตรวจสอบคุณภาพตามปริมาณที่เพิ่งเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="84269-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="84269-275">ตรรกะการสร้างนี้สอดคล้องกับการซื้อ</span><span class="sxs-lookup"><span data-stu-id="84269-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="84269-276">หากตัวเลือก **ต่อปริมาณที่อัพเดต** ถูกตั้งค่าเป็น **ไม่** จะมีการสร้างใบสั่งตรวจสอบคุณภาพในครั้งแรกที่มีการรายงานปริมาณเป็นเสร็จสิ้น ตามปริมาณที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="84269-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="84269-277">นอกจากนี้ จะมีการสร้างใบสั่งตรวจสอบคุณภาพอย่างน้อยหนึ่งรายการตามปริมาณคงเหลือ ขึ้นอยู่กับมิติการติดตามของสินค้าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="84269-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="84269-278">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับปริมาณที่เสร็จสิ้นในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="84269-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="84269-279">ข้อกำหนดเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-279">Quality specification</span></span></th>
<th><span data-ttu-id="84269-280">ต่อปริมาณที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="84269-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="84269-281">ต่อมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="84269-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="84269-282">ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="84269-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="84269-283">เปอร์เซ็นต์: 10%</span><span class="sxs-lookup"><span data-stu-id="84269-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="84269-284">ใช่</span><span class="sxs-lookup"><span data-stu-id="84269-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="84269-285">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="84269-285">Batch number: No</span></span></p>
<p><span data-ttu-id="84269-286">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="84269-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="84269-287">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="84269-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="84269-288">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="84269-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="84269-289">ใบสั่งตรวจสอบคุณภาพ #1 สำหรับ 3 (10% ของ 30)</span><span class="sxs-lookup"><span data-stu-id="84269-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="84269-290">รายงานเมื่อเสร็จสิ้นสำหรับ 70</span><span class="sxs-lookup"><span data-stu-id="84269-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="84269-291">ใบสั่งตรวจสอบคุณภาพ #2 สำหรับ 7 (10% ของปริมาณในใบสั่งที่เหลืออยู่ซึ่งเท่ากับ 70 ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="84269-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="84269-292">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="84269-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="84269-293">ไม่</span><span class="sxs-lookup"><span data-stu-id="84269-293">No</span></span></td>
<td>
<p><span data-ttu-id="84269-294">หมายเลขชุดงาน: ไม่</span><span class="sxs-lookup"><span data-stu-id="84269-294">Batch number: No</span></span></p>
<p><span data-ttu-id="84269-295">รหัสหมายเลขลำดับประจำสินค้า: ไม่</span><span class="sxs-lookup"><span data-stu-id="84269-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="84269-296">ปริมาณการสั่ง: 100</span><span class="sxs-lookup"><span data-stu-id="84269-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="84269-297">รายงานเมื่อเสร็จสิ้นสำหรับ 30</span><span class="sxs-lookup"><span data-stu-id="84269-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="84269-298">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 (สำหรับปริมาณที่รายงานการเสร็จงานครั้งแรกซึ่งมีค่าคงที่เป็น 1)</span><span class="sxs-lookup"><span data-stu-id="84269-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="84269-299">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 (สำหรับปริมาณที่คงเหลือ ซึ่งยังมีค่าคงที่เป็น 1)</span><span class="sxs-lookup"><span data-stu-id="84269-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="84269-300">รายงานเมื่อเสร็จสิ้นสำหรับ 10</span><span class="sxs-lookup"><span data-stu-id="84269-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="84269-301">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="84269-302">รายงานเมื่อเสร็จสิ้นสำหรับ 60</span><span class="sxs-lookup"><span data-stu-id="84269-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="84269-303">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="84269-304">ปริมาณคงที่: 1</span><span class="sxs-lookup"><span data-stu-id="84269-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="84269-305">ใช่</span><span class="sxs-lookup"><span data-stu-id="84269-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="84269-306">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="84269-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="84269-307">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="84269-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="84269-308">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="84269-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="84269-309">รายงานเป็นเสร็จสิ้นสำหรับ3: 1 สำหรับ #b1, #s1; 1 สำหรับ #b2, #s2; และ 1 สำหรับ #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="84269-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="84269-310">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 ของชุดงาน #b1 หมายเลขลำดับ #s1</span><span class="sxs-lookup"><span data-stu-id="84269-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="84269-311">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 สำหรับชุดงาน #b2 หมายเลขลำดับ #s2</span><span class="sxs-lookup"><span data-stu-id="84269-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="84269-312">ใบสั่งตรวจสอบคุณภาพ #3 ต่อ 1 สำหรับชุดงาน #b3 หมายเลขลำดับ #s3</span><span class="sxs-lookup"><span data-stu-id="84269-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="84269-313">รายงานเป็นเสร็จสิ้นสำหรับ 2: 1 สำหรับ #b4, #s4; และ 1 สำหรับ #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="84269-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="84269-314">ใบสั่งตรวจสอบคุณภาพ #4 ต่อ 1 สำหรับชุดงาน #b4 หมายเลขลำดับ #s4</span><span class="sxs-lookup"><span data-stu-id="84269-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="84269-315">ใบสั่งตรวจสอบคุณภาพ #5 ต่อ 1 สำหรับชุดงาน #b5 หมายเลขลำดับ #s5</span><span class="sxs-lookup"><span data-stu-id="84269-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="84269-316"><strong>หมายเหตุ:</strong> : ชุดงานสามารถนำมาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="84269-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="84269-317">ปริมาณคงที่: 2</span><span class="sxs-lookup"><span data-stu-id="84269-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="84269-318">ไม่</span><span class="sxs-lookup"><span data-stu-id="84269-318">No</span></span></td>
<td>
<p><span data-ttu-id="84269-319">หมายเลขชุดงาน: ใช่</span><span class="sxs-lookup"><span data-stu-id="84269-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="84269-320">หมายเลขลำดับประจำสินค้า: ใช่</span><span class="sxs-lookup"><span data-stu-id="84269-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="84269-321">ปริมาณการสั่ง: 10</span><span class="sxs-lookup"><span data-stu-id="84269-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="84269-322">รายงานเป็นเสร็จสิ้นสำหรับ 4: 1 สำหรับ #b1, #s1; 1 สำหรับ #b2, #s2; 1 สำหรับ #b3, #s3; และ 1 สำหรับ #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="84269-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="84269-323">ใบสั่งตรวจสอบคุณภาพ #1 ต่อ 1 ของชุดงาน #b1 หมายเลขลำดับ #s1</span><span class="sxs-lookup"><span data-stu-id="84269-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="84269-324">ใบสั่งตรวจสอบคุณภาพ #2 ต่อ 1 สำหรับชุดงาน #b2 หมายเลขลำดับ #s2</span><span class="sxs-lookup"><span data-stu-id="84269-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="84269-325">ใบสั่งตรวจสอบคุณภาพ #3 ต่อ 1 สำหรับชุดงาน #b3 หมายเลขลำดับ #s3</span><span class="sxs-lookup"><span data-stu-id="84269-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="84269-326">ใบสั่งตรวจสอบคุณภาพ #4 ต่อ 1 สำหรับชุดงาน #b4 หมายเลขลำดับ #s4</span><span class="sxs-lookup"><span data-stu-id="84269-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="84269-327">ใบสั่งตรวจสอบคุณภาพ #5 สำหรับ 2 โดยไม่มีการอ้างอิงถึงชุดงานและหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="84269-328">รายงานเป็นเสร็จสิ้นสำหรับ 6: 1 สำหรับ #b5, #s5; 1 สำหรับ #b6, #s6; 1 สำหรับ #b7, #s7; 1 สำหรับ #b8, #s8; 1 สำหรับ #b9, #s9; และ 1สำหรับ #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="84269-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="84269-329">ไม่มีการสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="84269-330">คุณลักษณะ *การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า* เพิ่มความสามารถสำหรับการประมวลผลใบสั่งตรวจสอบคุณภาพสำหรับการผลิตที่มีการตั้งค่า **ชนิดเหตุการณ์** เป็น *รายงานการเสร็จงาน* และมีการตั้งค่า **การดำเนินการ** เป็น *ภายหลัง* และสำหรับการซื้อที่มีการตั้งค่า **ชนิดเหตุการณ์** เป็น *การลงทะเบียน*</span><span class="sxs-lookup"><span data-stu-id="84269-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="84269-331">สำหรับรายละเอียด ให้ดูที่ [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](quality-management-for-warehouses-processes.md)</span><span class="sxs-lookup"><span data-stu-id="84269-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="84269-332">หน้าการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84269-333">หน้า</span><span class="sxs-lookup"><span data-stu-id="84269-333">Page</span></span></th>
<th><span data-ttu-id="84269-334">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="84269-334">Description</span></span></th>
<th><span data-ttu-id="84269-335">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="84269-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84269-336">การเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-336">Quality associations</span></span></td>
<td><span data-ttu-id="84269-337">ดูส่วนก่อนหน้าของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="84269-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="84269-338">ความสัมพันธ์ของคุณภาพกำหนดข้อมูลต่อไปนี้ทั้งหมดสำหรับใบสั่งตรวจสอบคุณภาพที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="84269-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="84269-339">เหตุการณ์ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="84269-339">The transaction event</span></span></li>
<li><span data-ttu-id="84269-340">ชุดของการทดสอบที่ต้องดำเนินการบนสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="84269-341">AQL</span><span class="sxs-lookup"><span data-stu-id="84269-341">The AQL</span></span></li>
<li><span data-ttu-id="84269-342">แผนการสุ่มตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="84269-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="84269-343">คุณต้องกำหนดคำความสัมพันธ์ของคุณภาพสำหรับความผันแปรต่าง ๆ ในกระบวนการทางธุรกิจที่จำเป็นต้องมีการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="84269-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="84269-344">ตัวอย่างเช่น สามารถสร้างใบสั่งตรวจสอบคุณภาพในกระบวนการทางธุรกิจสำหรับใบสั่งซื้อ ใบสั่งตรวจสอบสินค้า ใบสั่งขาย และใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="84269-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84269-345">การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-345">Tests</span></span></td>
<td><span data-ttu-id="84269-346">ใช้หน้านี้ในการกำหนดและดูการทดสอบแต่ละรายการที่กำหนดว่าผลิตภัณฑ์ของคุณตรงตามข้อมูลจำเพาะเกี่ยวกับคุณภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="84269-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="84269-347">คุณสามารถกำหนดรายการทดสอบแต่ละรายการกับกลุ่มการทดสอบอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="84269-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="84269-348">ในกรณีนี้ คุณระบุข้อมูลเฉพาะตัวของการทดสอบ เช่นค่าการประเมินที่ยอมรับได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="84269-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="84269-349">ค่าการประเมินค่าจะใช้สำหรับการทดสอบเชิงปริมาณ และตัวแปรทดสอบที่จะใช้สำหรับการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="84269-350">การทดสอบเชิงปริมาณมีชนิดการทดสอบของ <strong>จำนวนเต็ม</strong> หรือ <strong>เศษส่วน</strong> และยังมีการกำหนดหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="84269-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="84269-351">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="84269-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="84269-352">การทดสอบเชิงคุณภาพจะมีชนิดของ <strong>ตัวเลือก</strong>.</span><span class="sxs-lookup"><span data-stu-id="84269-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="84269-353">การทดสอบเชิงคุณภาพต้องการข้อมูลเพิ่มเติมเกี่ยวกับตัวแปรการทดสอบที่วัดและตัวเลือกที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84269-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="84269-354">ข้อมูลจำเพาะเกี่ยวกับคุณภาพและผลการทดสอบแสดงตามผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="84269-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="84269-355">บริษัทผู้ผลิตดำเนินการทดสอบวัสดุที่ซื้อสองแบบ: การทดสอบเชิงปริมาณเกี่ยวกับคุณภาพวัสดุและการทดสอบเชิงคุณภาพเกี่ยวกับความเสียหายของบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="84269-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="84269-356">บริษัทกำหนดข้อมูลเพิ่มเติมเกี่ยวกับการทดสอบเชิงคุณภาพเพื่อระบุตัวแปรการทดสอบ (บรรจุภัณฑ์ที่เสียหาย) และผลลัพธ์ที่ได้</span><span class="sxs-lookup"><span data-stu-id="84269-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="84269-357">บริษัทใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดการทดสอบทั้งสองให้กับกลุ่มการทดสอบและเพื่อระบุข้อมูลเฉพาะตัวของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="84269-358">กลุ่มทดสอบจะถูกกำหนดให้ใบสั่งตรวจสอบคุณภาพ เพื่อให้บริษัทสามารถรายงานผลการทดสอบสำหรับการทดสอบทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="84269-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84269-359">กลุ่มทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-359">Test groups</span></span></td>
<td><span data-ttu-id="84269-360">ใช้หน้านี้เพื่อตั้งค่า แก้ไข และดูกลุ่มทดสอบและการทดสอบแต่ละรายการที่กำหนดให้กับกลุ่มทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="84269-361">บานหน้าต่างด้านบนจะแสดงกลุ่มทดสอบ และบานหน้าต่างด้านล่างแสดงการทดสอบที่กำหนดให้กับกลุ่มการทดสอบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="84269-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="84269-362">คุณกำหนดนโยบายต่าง ๆ ให้กับกลุ่มการทดสอบ เช่นแผนการสุ่มตัวอย่าง AQL และความต้องการสำหรับการทดสอบแบบทำลาย</span><span class="sxs-lookup"><span data-stu-id="84269-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="84269-363">เมื่อคุณกำหนดการทดสอบแต่ละรายการกับกลุ่มการทดสอบ คุณต้องกำหนดข้อมูลเพิ่มเติม เช่นลำดับ เอกสาร และวันที่ที่มีผลใช้</span><span class="sxs-lookup"><span data-stu-id="84269-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="84269-364">สำหรับการทดสอบเชิงปริมาณ ข้อมูลที่คุณกำหนดจะประกอบด้วยค่าการประเมินที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="84269-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="84269-365">สำหรับการทดสอบเชิงคุณภาพ ข้อมูลนี้รวมถึงตัวแปรทดสอบและผลลัพธ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="84269-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="84269-366">กลุ่มการทดสอบที่กำหนดให้กับใบสั่งตรวจสอบคุณภาพกำหนดชุดค่าเริ่มต้นของการทดสอบที่ต้องดำเนินการกับสินค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84269-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="84269-367">อย่างไรก็ตาม คุณสามารถเพิ่ม ลบ หรือเปลี่ยนการทดสอบบนใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="84269-368">ผลการทดสอบจะรายงานสำหรับการทดสอบแต่ละรายการบนใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="84269-369">บริษัทผู้ผลิตกำหนดกลุ่มการทดสอบสำหรับความผันแปรต่าง ๆ ของคำแนะนำเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="84269-370">กลุ่มการทดสอบต่าง ๆ สะท้อนถึงผลต่างในแผนการสุ่มตัวอย่าง ชุดของการทดสอบที่ต้องดำเนินการพร้อมกัน AQL และปัจจัยอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="84269-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="84269-371">สำหรับการทดสอบเชิงปริมาณ ยังมความแตกต่างของค่าการประเมินที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="84269-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="84269-372">เพื่อบังคับใช้คำแนะนำด้านคุณภาพ บริษัทกำหนดกลุ่มการทดสอบสำหรับแต่ละกฎสำหรับการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติในหน้า <strong>ความสัมพันธ์ของคุณภาพ</strong> และยังกำหนดกลุ่มการทดสอบสำหรับใบสั่งตรวจสอบคุณภาพที่ถูกสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="84269-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84269-373">กลุ่มคุณภาพสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-373">Item quality groups</span></span></td>
<td><span data-ttu-id="84269-374">ตั้งค่า แก้ไข และดูสินค้าที่กำหนดให้กับกลุ่มคุณภาพหนึ่งหรือหลายกลุ่ม ซึ่งมีการกำหนดให้กับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="84269-375">กลุ่มคุณภาพแสดงข้อกำหนดในการทดสอบทั่วไปสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="84269-376">หลังจากที่คุณกำหนดความต้องการทดสอบบนหน้า <strong>กลุ่มทดสอบ</strong> คุณสามารถกำหนดกฎสำหรับการสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="84269-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="84269-377">เพื่อทำให้กระบวนการง่ายขึ้น คุณไม่ต้อง&#39;กำหนดกฎสำหรับสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="84269-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="84269-378">คุณกำหนดกฎสำหรับกลุ่มคุณภาพโดยการใช้หน้า <strong>ความสัมพันธ์ของคุณภาพ</strong> แทน</span><span class="sxs-lookup"><span data-stu-id="84269-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="84269-379">คุณยังสามารถใช้หน้า <strong>กลุ่มคุณภาพสินค้า</strong> สำหรับกลุ่มคุณภาพที่เลือกเพื่อกำหนดสินค้าที่เกี่ยวข้องกับกลุ่มนั้นได้</span><span class="sxs-lookup"><span data-stu-id="84269-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="84269-380">คุณยังสามารถใช้หน้า <strong>กลุ่มคุณภาพสินค้า</strong> สำหรับกลุ่มคุณภาพที่เลือกเพื่อกำหนดสินค้าที่เกี่ยวข้องกับกลุ่มนั้นได้</span><span class="sxs-lookup"><span data-stu-id="84269-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="84269-381">บริษัทผู้ผลิตจัดซื้อวัตถุดิบหลายอย่างที่มีการทดสอบสำหรับสินค้าสำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="84269-382">บริษัทกำหนดกลุ่มคุณภาพและกำหนดหมายเลขสินค้าที่เกี่ยวข้องกับวัตถุดิบสำหรับกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="84269-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="84269-383">ภายหลัง บริษัทสั่งซื้อวัตถุดิบชนิดใหม่ที่มีความต้องการทดสอบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="84269-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="84269-384">แทนที่จะติดตั้งข้อกำหนดในการทดสอบใหม่สำหรับวัสดุใหม่ บริษัทเพิ่มหมายเลขสินค้าสำหรับวัสดุใหม่ให้กับกลุ่มคุณภาพที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="84269-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="84269-385">บริษัทผู้ผลิตเดียวกันนี้ยังผลิตสินค้าที่มี มีข้อกำหนดในการทดสอบเดียวกันและจัดส่งสินค้าที่มีข้อกำหนดแบบเดียวกันในการทดสอบก่อนจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="84269-386">บริษัทกำหนดกลุ่มคุณภาพเพิ่มเติมสองกลุ่มและกำหนดหมายเลขสินค้าที่เกี่ยวข้องให้กับกลุ่มคุณภาพแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="84269-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84269-387">ตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-387">Test variables</span></span></td>
<td><span data-ttu-id="84269-388">ใช้หน้านี้เพื่อกำหนดหรือดูตัวแปรที่เชื่อมโยงกับการทดสอบเชิงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="84269-389">สำหรับแต่ละตัวแปร คุณกำหนดผลที่ได้ที่ระบุไว้แสดงถึงตัวเลือกที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="84269-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="84269-390">คุณกำหนดทดสอบบนหน้า <strong>ทดสอบ</strong></span><span class="sxs-lookup"><span data-stu-id="84269-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="84269-391">สำหรับการทดสอบเชิงคุณภาพ คุณต้องตั้งค่าชนิดของการทดสอบเป็น <strong>ตัวเลือก</strong></span><span class="sxs-lookup"><span data-stu-id="84269-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="84269-392">ใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดตัวแปรการทดสอบในการทดสอบแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="84269-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="84269-393">บริษัทผู้ผลิตซึ่งผลิตคุกกี้ใช้การทดสอบตรวจสอบสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="84269-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="84269-394">การทดสอบตรวจสอบนี้มีหลายตัวแปร</span><span class="sxs-lookup"><span data-stu-id="84269-394">This inspection test has several variables.</span></span> <span data-ttu-id="84269-395">ตัวแปรเป็นรส และผลลัพธ์ที่เป็นไปได้สำหรับตัวแปรนี้คืออร่อยและไม่อร่อย</span><span class="sxs-lookup"><span data-stu-id="84269-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="84269-396">ตัวแปรที่สองคือสี และผลลัพธ์ที่เป็นไปได้คือเข้มเกินไป อ่อนเกินไป และพอดี</span><span class="sxs-lookup"><span data-stu-id="84269-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84269-397">ผลที่ได้ของตัวแปรทดสอบ</span><span class="sxs-lookup"><span data-stu-id="84269-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="84269-398">ใช้หน้านี้เพื่อตั้งค่า แก้ไข และดูผลการทดสอบที่เป็นไปได้ของตัวแปรทดสอบที่เกี่ยวข้องกับการทดสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="84269-399">สำหรับแต่ละผลลัพธ์ คุณกำหนดสถานะ <strong>ผ่าน</strong> หรือ <strong>ล้มเหลว</strong></span><span class="sxs-lookup"><span data-stu-id="84269-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="84269-400">คุณต้องกำหนดตัวแปรและผลของตัวแปรนั้นสำหรับการทดสอบแต่ละเชิงคุณภาพที่กำหนดในหน้า <strong>ทดสอบ</strong></span><span class="sxs-lookup"><span data-stu-id="84269-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="84269-401">(สำหรับการทดสอบเชิงคุณภาพ ชนิดการทดสอบถูกตั้งค่าเป็น <strong>ตัวเลือก</strong> ในหน้า<strong>ทดสอบ</strong>) ใช้หน้า <strong>กลุ่มทดสอบ</strong> เพื่อกำหนดตัวแปรทดสอบและผลลัพธ์เริ่มต้นไปยังการทดสอบเชิงคุณภาพแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="84269-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="84269-402">บริษัทผู้ผลิตซึ่งผลิตคุกกี้ใช้การทดสอบตรวจสอบสำหรับผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="84269-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="84269-403">การทดสอบตรวจสอบนี้มีหลายตัวแปร</span><span class="sxs-lookup"><span data-stu-id="84269-403">This inspection test has of several variables.</span></span> <span data-ttu-id="84269-404">ตัวแปรเป็นรส และผลลัพธ์ที่เป็นไปได้สำหรับตัวแปรนี้คืออร่อยและไม่อร่อย</span><span class="sxs-lookup"><span data-stu-id="84269-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="84269-405">ตัวแปรที่สองคือสี และผลลัพธ์ที่เป็นไปได้คือเข้มเกินไป อ่อนเกินไป และพอดี</span><span class="sxs-lookup"><span data-stu-id="84269-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="84269-406">สถานะของ <strong>ผ่าน</strong> หรือ <strong>ล้มเหลว</strong> ถูกกำหนดไปยังแต่ละผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="84269-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="84269-407">ในระหว่างการทดสอบตรวจสอบตัวแปรแต่ละตัว ผู้ตรวจสอบจะรายงานผลการทดสอบโดยการเลือกจากผลที่ได้อันใดอันหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84269-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="84269-408">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="84269-408">Additional resources</span></span>
--------

[<span data-ttu-id="84269-409">กระบวนการการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="84269-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="84269-410">การจัดการความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="84269-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="84269-411">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="84269-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]