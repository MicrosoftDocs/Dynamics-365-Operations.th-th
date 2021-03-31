---
title: ภาพรวมของงานบริการ
description: ใช้ภารกิจการให้บริการในการอธิบายภารกิจที่ต้องดำเนินการให้เสร็จสมบูรณ์ในระหว่างใบสั่งบริการ ทั้งช่างเทคนิคและลูกค้าสามารถเห็นข้อมูลนี้ได้
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dfeddcf754ccaf1f5fb5d3f20ca771145c5f2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223325"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="4a21b-104">ภาพรวมของงานบริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a21b-105">ใช้ภารกิจการให้บริการในการอธิบายภารกิจที่ต้องดำเนินการให้เสร็จสมบูรณ์ในระหว่างใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="4a21b-106">ทั้งช่างเทคนิคและลูกค้าสามารถเห็นข้อมูลนี้ได้</span><span class="sxs-lookup"><span data-stu-id="4a21b-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="4a21b-107">คุณสร้างภารกิจการให้บริการในหน้า **ภารกิจการให้บริการ** และคุณเชื่อมโยงภารกิจการให้บริการซึ่งมีข้อตกลงการให้บริการเฉพาะหรือใบสั่งบริการ โดยสร้างความสัมพันธ์ของภารกิจการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="4a21b-108">ทุกครั้งที่คุณสร้างความสัมพันธ์ของภารกิจการให้บริการ คุณสามารถสร้างรายการต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="4a21b-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="4a21b-109">หมายเหตุภายในของภารกิจ เช่น รายละเอียดคำร้องทางเทคนิคของภารกิจที่ช่างเทคนิคจำเป็นต้องทราบ</span><span class="sxs-lookup"><span data-stu-id="4a21b-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="4a21b-110">หมายเหตุภายนอกที่ลูกค้าสามารถดูได้</span><span class="sxs-lookup"><span data-stu-id="4a21b-110">External notes that the customer can see.</span></span> <span data-ttu-id="4a21b-111">รายการเหล่านี้อาจให้คำอธิบายทางเทคนิคที่น้อยกว่าสำหรับภารกิจที่กำลังจะเสร็จสิ้น ตามข้อตกลงระหว่างลูกค้าและบริษัทที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="4a21b-112">เมื่อคุณตั้งค่าความสัมพันธ์ของภารกิจการให้บริการระหว่างภารกิจการให้บริการและใบสั่งบริการหรือหรือข้อตกลงการให้บริการแล้ว คุณจะสามารถกำหนดภารกิจการให้บริการนี้ได้ เมื่อคุณสร้างรายการใบสั่งบริการหรือรายการข้อตกลงการให้บริการสำหรับใบสั่งบริการหรือข้อตกลงการให้บริการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4a21b-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="4a21b-113">เมื่อคุณสร้างใบสั่งบริการจากข้อตกลงการให้บริการ คุณจะสามารถใช้ภารกิจการให้บริการที่ถูกกำหนดให้กับแต่ละรายการข้อตกลงการให้บริการ เพื่อจัดกลุ่มรายการใบสั่งบริการเป็นใบสั่งบริการได้</span><span class="sxs-lookup"><span data-stu-id="4a21b-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="4a21b-114">สร้างภารกิจการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-114">Create a service task</span></span>

1. <span data-ttu-id="4a21b-115">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **ภารกิจการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="4a21b-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="4a21b-116">สร้างบรรทัดใหม่ </span><span class="sxs-lookup"><span data-stu-id="4a21b-116">Create a new line.</span></span>
3. <span data-ttu-id="4a21b-117">ป้อน ID การบริการและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4a21b-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="4a21b-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="4a21b-118">Example</span></span>

<span data-ttu-id="4a21b-119">ช่างเทคนิคต้องดำเนินการงานสองงานเกี่ยวกับกระปุกเกียร์ (ออบเจ็กต์ที่ให้บริการ GB-1234) ที่ไซต์ลูกค้าให้เสร็จเรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="4a21b-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="4a21b-120">มีการสร้างข้อตกลงการให้บริการสำหรับลูกค้า และธุรกรรมต่างๆ ถูกเชื่อมโยงกับงาน</span><span class="sxs-lookup"><span data-stu-id="4a21b-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="4a21b-121">ข้อตกลงการให้บริการและรายการข้อตกลงการให้บริการสำหรับงานทั้งสองคือดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4a21b-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="4a21b-122">ข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-122">Service agreement</span></span>

| <span data-ttu-id="4a21b-123">Project</span><span class="sxs-lookup"><span data-stu-id="4a21b-123">Project</span></span> | <span data-ttu-id="4a21b-124">ข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-124">Service agreement</span></span> | <span data-ttu-id="4a21b-125">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4a21b-125">Description</span></span>                                  | <span data-ttu-id="4a21b-126">กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="4a21b-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="4a21b-127">9012</span><span class="sxs-lookup"><span data-stu-id="4a21b-127">9012</span></span>    | <span data-ttu-id="4a21b-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="4a21b-128">000008\_001</span></span>       | <span data-ttu-id="4a21b-129">การตรวจสอบและการเปลี่ยนตามปกติ – GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="4a21b-130">ค่าจ้างพิเศษ</span><span class="sxs-lookup"><span data-stu-id="4a21b-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="4a21b-131">รายการข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-131">Service agreement lines</span></span>

| <span data-ttu-id="4a21b-132">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4a21b-132">Description</span></span>             | <span data-ttu-id="4a21b-133">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="4a21b-133">Transaction type</span></span> | <span data-ttu-id="4a21b-134">วัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-134">Service object</span></span> | <span data-ttu-id="4a21b-135">งานบริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="4a21b-136">การตรวจสอบและการทำความสะอาด</span><span class="sxs-lookup"><span data-stu-id="4a21b-136">Inspection and cleaning</span></span> | <span data-ttu-id="4a21b-137">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4a21b-137">Hour</span></span>             | <span data-ttu-id="4a21b-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-138">GB-1234</span></span>        | <span data-ttu-id="4a21b-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-139">I/C - GB1234</span></span> |
| <span data-ttu-id="4a21b-140">ค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="4a21b-140">Travel</span></span>                  | <span data-ttu-id="4a21b-141">Expense</span><span class="sxs-lookup"><span data-stu-id="4a21b-141">Expense</span></span>          | <span data-ttu-id="4a21b-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-142">GB-1234</span></span>        | <span data-ttu-id="4a21b-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-143">I/C - GB1234</span></span> |
| <span data-ttu-id="4a21b-144">วัสดุ</span><span class="sxs-lookup"><span data-stu-id="4a21b-144">Materials</span></span>               | <span data-ttu-id="4a21b-145">รายการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-145">Item</span></span>             | <span data-ttu-id="4a21b-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-146">GB-1234</span></span>        | <span data-ttu-id="4a21b-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-147">I/C - GB1234</span></span> |
| <span data-ttu-id="4a21b-148">การเปลี่ยนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="4a21b-148">Routine replacement</span></span>     | <span data-ttu-id="4a21b-149">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4a21b-149">Hour</span></span>             | <span data-ttu-id="4a21b-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-150">GB-1234</span></span>        | <span data-ttu-id="4a21b-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-151">RR - GB1234</span></span>  |
| <span data-ttu-id="4a21b-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="4a21b-152">GR-1</span></span>                    | <span data-ttu-id="4a21b-153">รายการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-153">Item</span></span>             | <span data-ttu-id="4a21b-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-154">GB-1234</span></span>        | <span data-ttu-id="4a21b-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-155">RR - GB1234</span></span>  |
| <span data-ttu-id="4a21b-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="4a21b-156">GR-5</span></span>                    | <span data-ttu-id="4a21b-157">รายการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-157">Item</span></span>             | <span data-ttu-id="4a21b-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-158">GB-1234</span></span>        | <span data-ttu-id="4a21b-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-159">RR - GB1234</span></span>  |

<span data-ttu-id="4a21b-160">บรรทัดข้อตกลงการให้บริการสำหรับงานทั้งสองงานจะต้องมีภารกิจการให้บริการแนบอยู่ด้วยสองภารกิจ </span><span class="sxs-lookup"><span data-stu-id="4a21b-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="4a21b-161">ภารกิจการให้บริการจะกำหนดธุรกรรมของแต่ละงาน </span><span class="sxs-lookup"><span data-stu-id="4a21b-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="4a21b-162">ในกรณีแรก ภารกิจการให้บริการ I/C - GB1234 ระบุรายการข้อตกลงการให้บริการทั้งหมดที่เกี่ยวข้องในการตรวจสอบและการทำความสะอาดของออบเจ็กต์ GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="4a21b-163">ในกรณีที่สอง ภารกิจการให้บริการ RR - GB1234 ระบุรายการข้อตกลงการให้บริการทั้งหมดที่เกี่ยวข้องในการดำเนินงานการเปลี่ยนตามปกติให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4a21b-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="4a21b-164">ความสัมพันธ์ของภารกิจการให้บริการที่เชื่อมโยงภารกิจการให้บริการต่างๆ กับข้อตกลงเฉพาะมีดังนี้</span><span class="sxs-lookup"><span data-stu-id="4a21b-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="4a21b-165">ภารกิจการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-165">Service tasks</span></span>

| <span data-ttu-id="4a21b-166">ภารกิจการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-166">Service task</span></span> | <span data-ttu-id="4a21b-167">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4a21b-167">Description</span></span>                             | <span data-ttu-id="4a21b-168">หมายเหตุภายใน</span><span class="sxs-lookup"><span data-stu-id="4a21b-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="4a21b-169">หมายเหตุภายนอก</span><span class="sxs-lookup"><span data-stu-id="4a21b-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="4a21b-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-170">I/C - GB1234</span></span> | <span data-ttu-id="4a21b-171">การตรวจสอบกระปุกเกียร์ GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="4a21b-172">การตรวจสอบด้วยสายตาและการตรวจสอบทางเทคนิค และการทำความสะอาดกระปุกเกียร์ GB-1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="4a21b-173">การตรวจสอบกระปุกเกียร์ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="4a21b-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="4a21b-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4a21b-174">RR - GB1234</span></span>  | <span data-ttu-id="4a21b-175">การเปลี่ยนอะไหล่ GB-1234 ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="4a21b-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="4a21b-176">บริการเปลี่ยนส่วนประกอบ GR-1 และ GR-5 ตามปกติ (สำหรับกระปุกเกียร์ที่ผลิตก่อน 2002 และเปลี่ยนส่วนประกอบ GR-2)</span><span class="sxs-lookup"><span data-stu-id="4a21b-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="4a21b-177">การเปลี่ยนอะไหล่ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="4a21b-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="4a21b-178">จัดกลุ่มใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="4a21b-178">Group service orders</span></span>

<span data-ttu-id="4a21b-179">เมื่อคุณสร้างใบสั่งบริการโดยอัตโนมัติ คุณจะสามารถใช้ภารกิจการให้บริการเป็นเงื่อนไขการจัดกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="4a21b-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="4a21b-180">ถ้าต้องการจัดกลุ่มใบสั่งบริการตามภารกิจการให้บริการ ให้กำหนดในข้อตกลงการให้บริการว่า ใบสั่งบริการที่ขึ้นกับข้อตกลงการให้บริการควรถูกจัดกลุ่มตาม ID ภารกิจการให้บริการ ตามเงื่อนไขการจัดกลุ่มเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4a21b-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="4a21b-181">**การจัดกลุ่มตามภารกิจการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="4a21b-181">**Group by service task**</span></span>

1. <span data-ttu-id="4a21b-182">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="4a21b-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="4a21b-183">บนแท็บ **ตั้งค่า** เลือก **ตามภารกิจการให้บริการ** ในฟิลด์ **รวมใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="4a21b-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]