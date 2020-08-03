---
title: ตัวอย่างและตรรกะของรายงานอายุหนี้ของสินค้าคงคลัง
description: หัวข้อนี้จะแสดงตัวอย่างบางรายการที่แสดงวิธีการแปลผลลัพธ์ของรายงานอายุหนี้ของสินค้าคงคลัง
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: cb7b7a055c26b53ee3acc3b872acf04fcf089eca
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597251"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="e51c3-103">ตัวอย่างและตรรกะของรายงานอายุหนี้ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e51c3-104">หัวข้อนี้จะแสดงตัวอย่างบางรายการที่แสดงวิธีการแปลผลลัพธ์ของรายงาน **อายุหนี้ของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="e51c3-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="e51c3-105">รายงานนี้จัดประเภทปริมาณคงคลังคงเหลือและมูลค่าสินค้าคงคลังสำหรับสินค้าหรือกลุ่มสินค้าที่เลือกไว้เป็นกลุ่มรอบระยะเวลาต่างๆ</span><span class="sxs-lookup"><span data-stu-id="e51c3-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="e51c3-106">นอกจากนี้ หัวข้อนี้จะแสดงตรรกะภายในของรายงาน</span><span class="sxs-lookup"><span data-stu-id="e51c3-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="e51c3-107">ตัวอย่างในหัวข้อนี้แสดงผลลัพธ์ที่แสดงอยู่ในรายงาน **อายุหนี้ของสินค้าคงคลัง** มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="e51c3-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="e51c3-108">อย่างไรก็ตาม โดยทั่วไป เราขอแนะนำให้คุณใช้รุ่น [การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง](inventory-aging-report-storage.md) ของรายงานนี้ โดยเฉพาะเมื่อคุณมีสินค้าและคลังสินค้าจำนวนมากที่ต้องมีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="e51c3-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="e51c3-109">การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลังจะบันทึกรายงานแต่ละฉบับที่คุณสร้าง แสดงผลลัพธ์เป็นหน้าแบบโต้ตอบและแผนภูมิ และช่วยให้คุณสามารถส่งออกรายงานที่บันทึกไว้ใดๆ</span><span class="sxs-lookup"><span data-stu-id="e51c3-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="e51c3-110">ข้อมูลตัวอย่างที่ใช้ในตัวอย่างเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e51c3-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="e51c3-111">ตัวอย่างของหัวข้อนี้จะขึ้นอยู่กับข้อมูลธุรกรรมสินค้าคงคลังตัวอย่างที่อธิบายไว้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="e51c3-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="e51c3-112">การตั้งค่ามิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="e51c3-112">Storage dimension setup</span></span>

<span data-ttu-id="e51c3-113">ระบบตัวอย่างมีการตั้งค่าต่อไปนี้ของมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="e51c3-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="e51c3-114">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="e51c3-114">Name</span></span>      | <span data-ttu-id="e51c3-115">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="e51c3-115">Active</span></span> | <span data-ttu-id="e51c3-116">สินค้าคงคลังที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="e51c3-116">Physical inventory</span></span> | <span data-ttu-id="e51c3-117">สินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e51c3-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="e51c3-118">ไซต์</span><span class="sxs-lookup"><span data-stu-id="e51c3-118">Site</span></span>      | <span data-ttu-id="e51c3-119">ใช่</span><span class="sxs-lookup"><span data-stu-id="e51c3-119">Yes</span></span>    | <span data-ttu-id="e51c3-120">ใช่</span><span class="sxs-lookup"><span data-stu-id="e51c3-120">Yes</span></span>                | <span data-ttu-id="e51c3-121">ใช่</span><span class="sxs-lookup"><span data-stu-id="e51c3-121">Yes</span></span>                 |
| <span data-ttu-id="e51c3-122">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-122">Warehouse</span></span> | <span data-ttu-id="e51c3-123">ใช่</span><span class="sxs-lookup"><span data-stu-id="e51c3-123">Yes</span></span>    | <span data-ttu-id="e51c3-124">ใช่</span><span class="sxs-lookup"><span data-stu-id="e51c3-124">Yes</span></span>                | <span data-ttu-id="e51c3-125">จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="e51c3-126">แบบจำลองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-126">Inventory model</span></span>

<span data-ttu-id="e51c3-127">สำหรับระบบตัวอย่าง แบบจำลองสินค้าคงคลังสำหรับผลิตภัณฑ์ที่นำออกใช้คือ *FIFO* และการตั้งค่า **ราคาต้นทุน** สำหรับแบบจำลองสินค้าคงคลังคือ *รวมค่าทางกายภาพ*</span><span class="sxs-lookup"><span data-stu-id="e51c3-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="e51c3-128">ธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-128">Inventory transactions</span></span>

<span data-ttu-id="e51c3-129">ระบบตัวอย่างมีรายการความเคลื่อนไหวของสินค้าคงคลังต่อไปนี้สำหรับผลิตภัณฑ์ที่นำออกใช้ที่มีหมายเลขสินค้า *1000*</span><span class="sxs-lookup"><span data-stu-id="e51c3-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="e51c3-130">อ้างอิง</span><span class="sxs-lookup"><span data-stu-id="e51c3-130">Reference</span></span>      | <span data-ttu-id="e51c3-131">ไซต์</span><span class="sxs-lookup"><span data-stu-id="e51c3-131">Site</span></span> | <span data-ttu-id="e51c3-132">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-132">Warehouse</span></span> | <span data-ttu-id="e51c3-133">การรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-133">Receipt</span></span>   | <span data-ttu-id="e51c3-134">ออก</span><span class="sxs-lookup"><span data-stu-id="e51c3-134">Issue</span></span> | <span data-ttu-id="e51c3-135">วันที่ตามจริง</span><span class="sxs-lookup"><span data-stu-id="e51c3-135">Physical date</span></span> | <span data-ttu-id="e51c3-136">วันที่ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e51c3-136">Financial date</span></span> | <span data-ttu-id="e51c3-137">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-137">Quantity</span></span> | <span data-ttu-id="e51c3-138">จำนวนเงินต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e51c3-138">Cost amount</span></span> | <span data-ttu-id="e51c3-139">ยอดต้นทุนจริง</span><span class="sxs-lookup"><span data-stu-id="e51c3-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="e51c3-140">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e51c3-140">Purchase order</span></span> | <span data-ttu-id="e51c3-141">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-141">1</span></span>    | <span data-ttu-id="e51c3-142">11</span><span class="sxs-lookup"><span data-stu-id="e51c3-142">11</span></span>        | <span data-ttu-id="e51c3-143">ซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="e51c3-143">Purchased</span></span> |       | <span data-ttu-id="e51c3-144">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="e51c3-144">March 15</span></span>      | <span data-ttu-id="e51c3-145">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="e51c3-145">March 15</span></span>       | <span data-ttu-id="e51c3-146">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-146">10</span></span>       | <span data-ttu-id="e51c3-147">1,000</span><span class="sxs-lookup"><span data-stu-id="e51c3-147">1,000</span></span>       | <span data-ttu-id="e51c3-148">1,000</span><span class="sxs-lookup"><span data-stu-id="e51c3-148">1,000</span></span>                |
| <span data-ttu-id="e51c3-149">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e51c3-149">Purchase order</span></span> | <span data-ttu-id="e51c3-150">2</span><span class="sxs-lookup"><span data-stu-id="e51c3-150">2</span></span>    | <span data-ttu-id="e51c3-151">21</span><span class="sxs-lookup"><span data-stu-id="e51c3-151">21</span></span>        | <span data-ttu-id="e51c3-152">ซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="e51c3-152">Purchased</span></span> |       | <span data-ttu-id="e51c3-153">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="e51c3-153">March 15</span></span>      | <span data-ttu-id="e51c3-154">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="e51c3-154">March 15</span></span>       | <span data-ttu-id="e51c3-155">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-155">10</span></span>       | <span data-ttu-id="e51c3-156">2,000</span><span class="sxs-lookup"><span data-stu-id="e51c3-156">2,000</span></span>       | <span data-ttu-id="e51c3-157">2,000</span><span class="sxs-lookup"><span data-stu-id="e51c3-157">2,000</span></span>                |
| <span data-ttu-id="e51c3-158">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e51c3-158">Purchase order</span></span> | <span data-ttu-id="e51c3-159">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-159">1</span></span>    | <span data-ttu-id="e51c3-160">11</span><span class="sxs-lookup"><span data-stu-id="e51c3-160">11</span></span>        | <span data-ttu-id="e51c3-161">ได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="e51c3-161">Received</span></span>  |       | <span data-ttu-id="e51c3-162">15 เมษายน</span><span class="sxs-lookup"><span data-stu-id="e51c3-162">April 15</span></span>      |                | <span data-ttu-id="e51c3-163">5</span><span class="sxs-lookup"><span data-stu-id="e51c3-163">5</span></span>        |             | <span data-ttu-id="e51c3-164">375</span><span class="sxs-lookup"><span data-stu-id="e51c3-164">375</span></span>                  |
| <span data-ttu-id="e51c3-165">ใบสั่งโอน</span><span class="sxs-lookup"><span data-stu-id="e51c3-165">Transfer order</span></span> | <span data-ttu-id="e51c3-166">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-166">1</span></span>    | <span data-ttu-id="e51c3-167">11</span><span class="sxs-lookup"><span data-stu-id="e51c3-167">11</span></span>        |           | <span data-ttu-id="e51c3-168">ขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="e51c3-168">Sold</span></span>  | <span data-ttu-id="e51c3-169">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="e51c3-169">May 2</span></span>         | <span data-ttu-id="e51c3-170">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="e51c3-170">May 2</span></span>          | <span data-ttu-id="e51c3-171">-5</span><span class="sxs-lookup"><span data-stu-id="e51c3-171">-5</span></span>       | <span data-ttu-id="e51c3-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-172">-458.33</span></span>     | <span data-ttu-id="e51c3-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-173">-458.33</span></span>              |
| <span data-ttu-id="e51c3-174">ใบสั่งโอน</span><span class="sxs-lookup"><span data-stu-id="e51c3-174">Transfer order</span></span> | <span data-ttu-id="e51c3-175">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-175">1</span></span>    | <span data-ttu-id="e51c3-176">12</span><span class="sxs-lookup"><span data-stu-id="e51c3-176">12</span></span>        | <span data-ttu-id="e51c3-177">ซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="e51c3-177">Purchased</span></span> |       | <span data-ttu-id="e51c3-178">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="e51c3-178">May 2</span></span>         | <span data-ttu-id="e51c3-179">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="e51c3-179">May 2</span></span>          | <span data-ttu-id="e51c3-180">5</span><span class="sxs-lookup"><span data-stu-id="e51c3-180">5</span></span>        | <span data-ttu-id="e51c3-181">458.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-181">458.33</span></span>      | <span data-ttu-id="e51c3-182">458.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-182">458.33</span></span>               |
| <span data-ttu-id="e51c3-183">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="e51c3-183">Sales order</span></span>    | <span data-ttu-id="e51c3-184">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-184">1</span></span>    | <span data-ttu-id="e51c3-185">12</span><span class="sxs-lookup"><span data-stu-id="e51c3-185">12</span></span>        |           | <span data-ttu-id="e51c3-186">ขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="e51c3-186">Sold</span></span>  | <span data-ttu-id="e51c3-187">พฤษภาคม 3</span><span class="sxs-lookup"><span data-stu-id="e51c3-187">May 3</span></span>         | <span data-ttu-id="e51c3-188">พฤษภาคม 3</span><span class="sxs-lookup"><span data-stu-id="e51c3-188">May 3</span></span>          | <span data-ttu-id="e51c3-189">-1</span><span class="sxs-lookup"><span data-stu-id="e51c3-189">-1</span></span>       | <span data-ttu-id="e51c3-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-190">-91.67</span></span>      | <span data-ttu-id="e51c3-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="e51c3-192">วิธีการคำนวณปริมาณและยอดเงินในบักเก็ตรอบระยะเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="e51c3-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="e51c3-193">โดยใช้ข้อมูลตัวอย่างที่อธิบายไว้ในส่วนก่อนหน้านี้ คุณสามารถรันรายงาน **อายุหนี้ของสินค้าคงคลัง** ที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e51c3-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="e51c3-194">**ณ วันที่:** *9 พฤษภาคม 2020*</span><span class="sxs-lookup"><span data-stu-id="e51c3-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="e51c3-195">**ไซต์:** *มุมมอง*</span><span class="sxs-lookup"><span data-stu-id="e51c3-195">**Site:** *View*</span></span>
- <span data-ttu-id="e51c3-196">**คลังสินค้า:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="e51c3-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="e51c3-197">**หมายเลขสินค้า:** *รวม*</span><span class="sxs-lookup"><span data-stu-id="e51c3-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="e51c3-198">**รอบระยะเวลาอายุหนี้:** ตั้งค่าฟิลด์นี้เพื่อสร้างกลุ่มรายเดือน</span><span class="sxs-lookup"><span data-stu-id="e51c3-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="e51c3-199">ในกรณีนี้ เนื้อหาของรายงานที่สร้างขึ้นจะมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e51c3-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="e51c3-200">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-201">ไซต์</span><span class="sxs-lookup"><span data-stu-id="e51c3-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-202">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="e51c3-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-203">มูลค่าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="e51c3-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-204">ปริมาณมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-205">มูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-206">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="e51c3-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="e51c3-210">P1:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-211">P1:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="e51c3-212">P2:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-213">P2:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="e51c3-214">P3:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-215">P3:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="e51c3-216">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-216">1000</span></span></td>
    <td><span data-ttu-id="e51c3-217">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-217">1</span></span></td>
    <td><span data-ttu-id="e51c3-218">14</span><span class="sxs-lookup"><span data-stu-id="e51c3-218">14</span></span></td>
    <td><span data-ttu-id="e51c3-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-219">1,283.33</span></span></td>
    <td><span data-ttu-id="e51c3-220">14</span><span class="sxs-lookup"><span data-stu-id="e51c3-220">14</span></span></td>
    <td><span data-ttu-id="e51c3-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-221">1,283.33</span></span></td>
    <td><span data-ttu-id="e51c3-222">91.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-223">5.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-223">5.00</span></span></td>
    <td><span data-ttu-id="e51c3-224">458.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-224">458.33</span></span></td>
    <td><span data-ttu-id="e51c3-225">9.00 น.</span><span class="sxs-lookup"><span data-stu-id="e51c3-225">9.00</span></span></td>
    <td><span data-ttu-id="e51c3-226">825.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="e51c3-227">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-227">1000</span></span></td>
    <td><span data-ttu-id="e51c3-228">2</span><span class="sxs-lookup"><span data-stu-id="e51c3-228">2</span></span></td>
    <td><span data-ttu-id="e51c3-229">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-229">10</span></span></td>
    <td><span data-ttu-id="e51c3-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-230">2,000.00</span></span></td>
    <td><span data-ttu-id="e51c3-231">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-231">10</span></span></td>
    <td><span data-ttu-id="e51c3-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-232">2,000.00</span></span></td>
    <td><span data-ttu-id="e51c3-233">200.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-234">10.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-234">10.00</span></span></td>
    <td><span data-ttu-id="e51c3-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="e51c3-236"><strong>ยอดรวม 1000</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="e51c3-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="e51c3-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="e51c3-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="e51c3-243">หมายเหตุรายละเอียดต่อไปนี้ในรายงานตัวอย่างนี้:</span><span class="sxs-lookup"><span data-stu-id="e51c3-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="e51c3-244">**ปริมาณมูลค่าสินค้าคงคลัง** **มูลค่าสินค้าคงคลัง** และมูลค่า **ต้นทุนต่อหน่วยเฉลี่ย** ที่แสดงอยู่ในรายงาน เป็นค่าสำหรับมิติสินค้าคงคลังทางการเงิน (**ไซต์** ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="e51c3-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="e51c3-245">ตัวอย่างเช่น สำหรับไซต์ 1 รายงานจะแสดงข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e51c3-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="e51c3-246">ค่า **ปริมาณมูลค่าสินค้าคงคลัง** คือ *14* (= 10 + 5 – 5 + 5 – 1)</span><span class="sxs-lookup"><span data-stu-id="e51c3-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="e51c3-247">ค่า **มูลค่าสินค้าคงคลัง** คือ *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67)</span><span class="sxs-lookup"><span data-stu-id="e51c3-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="e51c3-248">ค่า **ต้นทุนต่อหน่วยเฉลี่ย** คือ *91.67*</span><span class="sxs-lookup"><span data-stu-id="e51c3-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="e51c3-249">ค่า **มูลค่าคงเหลือ** และค่า **จำนวน** ในบักเก็ตรอบระยะเวลาแต่ละรายการ จะถูกคำนวณโดยใช้ค่า **ต้นทุนต่อหน่วยเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="e51c3-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="e51c3-250">รายงานจะกำหนดปริมาณคงคลังคงเหลือสำหรับบักเก็ตรอบระยะเวลาแต่ละรายการ โดยสรุปปริมาณสินค้าคงคลังที่ได้รับรวมสำหรับบักเก็ตรอบระยะเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="e51c3-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="e51c3-251">จากนั้น จะใช้หลักการแบบเข้าก่อนออกก่อน (FIFO) เพื่อหักลบปริมาณที่นำออกใช้ทั้งหมด โดยไม่คำนึงถึงแบบจำลองสินค้าคงคลังที่สินค้าใช้</span><span class="sxs-lookup"><span data-stu-id="e51c3-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="e51c3-252">ถ้าคุณรันรายงานเดียวกันอีกครั้ง แต่ครั้งนี้คุณตั้งค่าทั้งฟิลด์ **ไซต์** และฟิลด์ **คลังสินค้า** เพื่อ *ดู* รายงานใหม่จะมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e51c3-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="e51c3-253">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-254">ไซต์</span><span class="sxs-lookup"><span data-stu-id="e51c3-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-255">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-256">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="e51c3-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-257">มูลค่าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="e51c3-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-258">ปริมาณมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-259">มูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-260">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="e51c3-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="e51c3-264">P1:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-265">P1:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="e51c3-266">P2:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-267">P2:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="e51c3-268">P3:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-269">P3:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="e51c3-270">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-270">1000</span></span></td>
    <td><span data-ttu-id="e51c3-271">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-271">1</span></span></td>
    <td><span data-ttu-id="e51c3-272">11</span><span class="sxs-lookup"><span data-stu-id="e51c3-272">11</span></span></td>
    <td><span data-ttu-id="e51c3-273">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-273">10</span></span></td>
    <td><span data-ttu-id="e51c3-274">916.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-274">916.67</span></span></td>
    <td><span data-ttu-id="e51c3-275">14</span><span class="sxs-lookup"><span data-stu-id="e51c3-275">14</span></span></td>
    <td><span data-ttu-id="e51c3-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-276">1,283.33</span></span></td>
    <td><span data-ttu-id="e51c3-277">91.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-278">5.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-278">5.00</span></span></td>
    <td><span data-ttu-id="e51c3-279">458.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-279">458.33</span></span></td>
    <td><span data-ttu-id="e51c3-280">5.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-280">5.00</span></span></td>
    <td><span data-ttu-id="e51c3-281">458.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="e51c3-282">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-282">1000</span></span></td>
    <td><span data-ttu-id="e51c3-283">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-283">1</span></span></td>
    <td><span data-ttu-id="e51c3-284">12</span><span class="sxs-lookup"><span data-stu-id="e51c3-284">12</span></span></td>
    <td><span data-ttu-id="e51c3-285">4</span><span class="sxs-lookup"><span data-stu-id="e51c3-285">4</span></span></td>
    <td><span data-ttu-id="e51c3-286">366.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-286">366.67</span></span></td>
    <td><span data-ttu-id="e51c3-287">14</span><span class="sxs-lookup"><span data-stu-id="e51c3-287">14</span></span></td>
    <td><span data-ttu-id="e51c3-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e51c3-288">1,283.33</span></span></td>
    <td><span data-ttu-id="e51c3-289">91.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-289">91.67</span></span></td>
    <td><span data-ttu-id="e51c3-290">4.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-290">4.00</span></span></td>
    <td><span data-ttu-id="e51c3-291">366.67</span><span class="sxs-lookup"><span data-stu-id="e51c3-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="e51c3-292">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-292">1000</span></span></td>
    <td><span data-ttu-id="e51c3-293">2</span><span class="sxs-lookup"><span data-stu-id="e51c3-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="e51c3-294">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-294">10</span></span></td>
    <td><span data-ttu-id="e51c3-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-295">2,000.00</span></span></td>
    <td><span data-ttu-id="e51c3-296">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-296">10</span></span></td>
    <td><span data-ttu-id="e51c3-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-297">2,000.00</span></span></td>
    <td><span data-ttu-id="e51c3-298">200.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-299">10.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-299">10.00</span></span></td>
    <td><span data-ttu-id="e51c3-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="e51c3-301"><strong>ยอดรวม 1000</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="e51c3-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="e51c3-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="e51c3-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="e51c3-310">เวลานี้ ไซต์ 1 ถูกแบ่งออกเป็นสองแถว หนึ่งแถวสำหรับคลังสินค้า 11 และหนึ่งแถวสำหรับคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="e51c3-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="e51c3-311">อย่างไรก็ตาม ค่า **ปริมาณมูลค่าสินค้าคงคลัง** **มูลค่าสินค้าคงคลัง** และ **ต้นทุนต่อหน่วยเฉลี่ย** เป็นค่าเดียวกัน เนื่องจาก **คลังสินค้า** ไม่ใช่มิติสินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e51c3-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="e51c3-312">นอกจากนี้ โปรดสังเกตว่าการกระจายปริมาณของไซต์ 1 แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e51c3-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="e51c3-313">ในรายงานแรกที่คุณรัน ระบบจะละเว้นใบสั่งโอนย้ายที่เกิดขึ้นในไซต์เดียวกันและมีการหักลบปริมาณของใบแจ้งหนี้การขายจากบักเก็ตรอบระยะเวลา **3/31/2020-3/1/2020** ในไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="e51c3-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="e51c3-314">อย่างไรก็ตาม ในรายงานใหม่ ระบบจะหักปริมาณของใบแจ้งหนี้การขายจากบักเก็ตรอบระยะเวลา **5/8/2020-5/1/2020** ในคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="e51c3-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="e51c3-315">ผลกระทบของการปิดบัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-315">Effects of inventory closing</span></span>

<span data-ttu-id="e51c3-316">ถ้าคุณรันการปิดบัญชีสินค้าคงคลังสำหรับเดือนพฤษภาคม และจากนั้น รันรายงานก่อนหน้านี้อีกครั้ง แต่คุณตั้งค่าฟิลด์ **ณ วันที่** เป็น *31 พฤษภาคม 2020* คุณจะพบผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e51c3-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="e51c3-317">มีการปรับปรุงค่า **มูลค่าสินค้าคงคลัง** และค่า **ต้นทุนต่อหน่วยโดยเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="e51c3-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="e51c3-318">ค่า **มูลค่าคงเหลือ** และค่า **จำนวน** ทั้งหมดในบักเก็ตรอบระยะเวลาทุกรายการจะถูกปรับปรุงโดยสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="e51c3-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="e51c3-319">รายงานใหม่จะมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e51c3-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="e51c3-320">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-321">ไซต์</span><span class="sxs-lookup"><span data-stu-id="e51c3-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-322">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="e51c3-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-323">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="e51c3-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-324">มูลค่าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="e51c3-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-325">ปริมาณมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-326">มูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e51c3-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e51c3-327">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="e51c3-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e51c3-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="e51c3-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="e51c3-331">P1:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-332">P1:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="e51c3-333">P2:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-334">P2:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="e51c3-335">P3:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="e51c3-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="e51c3-336">P3:จำนวน</span><span class="sxs-lookup"><span data-stu-id="e51c3-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="e51c3-337">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-337">1000</span></span></td>
    <td><span data-ttu-id="e51c3-338">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-338">1</span></span></td>
    <td><span data-ttu-id="e51c3-339">11</span><span class="sxs-lookup"><span data-stu-id="e51c3-339">11</span></span></td>
    <td><span data-ttu-id="e51c3-340">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-340">10</span></span></td>
    <td><span data-ttu-id="e51c3-341">910.70</span><span class="sxs-lookup"><span data-stu-id="e51c3-341">910.70</span></span></td>
    <td><span data-ttu-id="e51c3-342">14</span><span class="sxs-lookup"><span data-stu-id="e51c3-342">14</span></span></td>
    <td><span data-ttu-id="e51c3-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-343">1,275.00</span></span></td>
    <td><span data-ttu-id="e51c3-344">91.07</span><span class="sxs-lookup"><span data-stu-id="e51c3-344">91.07</span></span></td>
    <td><span data-ttu-id="e51c3-345">0.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="e51c3-346">5.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-346">5.00</span></span></td>
    <td><span data-ttu-id="e51c3-347">455.36</span><span class="sxs-lookup"><span data-stu-id="e51c3-347">455.36</span></span></td>
    <td><span data-ttu-id="e51c3-348">5.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-348">5.00</span></span></td>
    <td><span data-ttu-id="e51c3-349">455.36</span><span class="sxs-lookup"><span data-stu-id="e51c3-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="e51c3-350">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-350">1000</span></span></td>
    <td><span data-ttu-id="e51c3-351">1</span><span class="sxs-lookup"><span data-stu-id="e51c3-351">1</span></span></td>
    <td><span data-ttu-id="e51c3-352">12</span><span class="sxs-lookup"><span data-stu-id="e51c3-352">12</span></span></td>
    <td><span data-ttu-id="e51c3-353">4</span><span class="sxs-lookup"><span data-stu-id="e51c3-353">4</span></span></td>
    <td><span data-ttu-id="e51c3-354">364.29</span><span class="sxs-lookup"><span data-stu-id="e51c3-354">364.29</span></span></td>
    <td><span data-ttu-id="e51c3-355">14</span><span class="sxs-lookup"><span data-stu-id="e51c3-355">14</span></span></td>
    <td><span data-ttu-id="e51c3-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-356">1,275.00</span></span></td>
    <td><span data-ttu-id="e51c3-357">91.07</span><span class="sxs-lookup"><span data-stu-id="e51c3-357">91.07</span></span></td>
    <td><span data-ttu-id="e51c3-358">4.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-358">4.00</span></span></td>
    <td><span data-ttu-id="e51c3-359">364.29</span><span class="sxs-lookup"><span data-stu-id="e51c3-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="e51c3-360">1000</span><span class="sxs-lookup"><span data-stu-id="e51c3-360">1000</span></span></td>
    <td><span data-ttu-id="e51c3-361">2</span><span class="sxs-lookup"><span data-stu-id="e51c3-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="e51c3-362">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-362">10</span></span></td>
    <td><span data-ttu-id="e51c3-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-363">2,000.00</span></span></td>
    <td><span data-ttu-id="e51c3-364">10</span><span class="sxs-lookup"><span data-stu-id="e51c3-364">10</span></span></td>
    <td><span data-ttu-id="e51c3-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-365">2,000.00</span></span></td>
    <td><span data-ttu-id="e51c3-366">200.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-367">10.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-367">10.00</span></span></td>
    <td><span data-ttu-id="e51c3-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e51c3-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="e51c3-369"><strong>ยอดรวม 1000</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e51c3-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="e51c3-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="e51c3-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="e51c3-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="e51c3-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="e51c3-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
