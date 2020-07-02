---
title: ตัวอย่างและตรรกะของรายงานอายุหนี้ของสินค้าคงคลัง
description: หัวข้อนี้จะแสดงตัวอย่างบางรายการที่แสดงวิธีการแปลผลลัพธ์ของรายงานอายุหนี้ของสินค้าคงคลัง
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484541"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="4ae31-103">ตัวอย่างและตรรกะของรายงานอายุหนี้ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ae31-104">หัวข้อนี้จะแสดงตัวอย่างบางรายการที่แสดงวิธีการแปลผลลัพธ์ของรายงาน **อายุหนี้ของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="4ae31-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="4ae31-105">รายงานนี้จัดประเภทปริมาณคงคลังคงเหลือและมูลค่าสินค้าคงคลังสำหรับสินค้าหรือกลุ่มสินค้าที่เลือกไว้เป็นกลุ่มรอบระยะเวลาต่างๆ</span><span class="sxs-lookup"><span data-stu-id="4ae31-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="4ae31-106">นอกจากนี้ หัวข้อนี้จะแสดงตรรกะภายในของรายงาน</span><span class="sxs-lookup"><span data-stu-id="4ae31-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="4ae31-107">ตัวอย่างในหัวข้อนี้แสดงผลลัพธ์ที่แสดงอยู่ในรายงาน **อายุหนี้ของสินค้าคงคลัง** มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="4ae31-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="4ae31-108">อย่างไรก็ตาม โดยทั่วไป เราขอแนะนำให้คุณใช้รุ่น [การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง](inventory-aging-report-storage.md) ของรายงานนี้ โดยเฉพาะเมื่อคุณมีสินค้าและคลังสินค้าจำนวนมากที่ต้องมีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="4ae31-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="4ae31-109">การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลังจะบันทึกรายงานแต่ละฉบับที่คุณสร้าง แสดงผลลัพธ์เป็นหน้าแบบโต้ตอบและแผนภูมิ และช่วยให้คุณสามารถส่งออกรายงานที่บันทึกไว้ใดๆ</span><span class="sxs-lookup"><span data-stu-id="4ae31-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="4ae31-110">ข้อมูลตัวอย่างที่ใช้ในตัวอย่างเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4ae31-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="4ae31-111">ตัวอย่างของหัวข้อนี้จะขึ้นอยู่กับข้อมูลธุรกรรมสินค้าคงคลังตัวอย่างที่อธิบายไว้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="4ae31-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="4ae31-112">การตั้งค่ามิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="4ae31-112">Storage dimension setup</span></span>

<span data-ttu-id="4ae31-113">ระบบตัวอย่างมีการตั้งค่าต่อไปนี้ของมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="4ae31-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="4ae31-114">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4ae31-114">Name</span></span>      | <span data-ttu-id="4ae31-115">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="4ae31-115">Active</span></span> | <span data-ttu-id="4ae31-116">สินค้าคงคลังที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="4ae31-116">Physical inventory</span></span> | <span data-ttu-id="4ae31-117">สินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="4ae31-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="4ae31-118">ไซต์</span><span class="sxs-lookup"><span data-stu-id="4ae31-118">Site</span></span>      | <span data-ttu-id="4ae31-119">ใช่</span><span class="sxs-lookup"><span data-stu-id="4ae31-119">Yes</span></span>    | <span data-ttu-id="4ae31-120">ใช่</span><span class="sxs-lookup"><span data-stu-id="4ae31-120">Yes</span></span>                | <span data-ttu-id="4ae31-121">ใช่</span><span class="sxs-lookup"><span data-stu-id="4ae31-121">Yes</span></span>                 |
| <span data-ttu-id="4ae31-122">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-122">Warehouse</span></span> | <span data-ttu-id="4ae31-123">ใช่</span><span class="sxs-lookup"><span data-stu-id="4ae31-123">Yes</span></span>    | <span data-ttu-id="4ae31-124">ใช่</span><span class="sxs-lookup"><span data-stu-id="4ae31-124">Yes</span></span>                | <span data-ttu-id="4ae31-125">จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="4ae31-126">แบบจำลองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-126">Inventory model</span></span>

<span data-ttu-id="4ae31-127">สำหรับระบบตัวอย่าง แบบจำลองสินค้าคงคลังสำหรับผลิตภัณฑ์ที่นำออกใช้คือ *FIFO* และการตั้งค่า **ราคาต้นทุน** สำหรับแบบจำลองสินค้าคงคลังคือ *รวมค่าทางกายภาพ*</span><span class="sxs-lookup"><span data-stu-id="4ae31-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="4ae31-128">ธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-128">Inventory transactions</span></span>

<span data-ttu-id="4ae31-129">ระบบตัวอย่างมีรายการความเคลื่อนไหวของสินค้าคงคลังต่อไปนี้สำหรับผลิตภัณฑ์ที่นำออกใช้ที่มีหมายเลขสินค้า *1000*</span><span class="sxs-lookup"><span data-stu-id="4ae31-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="4ae31-130">อ้างอิง</span><span class="sxs-lookup"><span data-stu-id="4ae31-130">Reference</span></span>      | <span data-ttu-id="4ae31-131">ไซต์</span><span class="sxs-lookup"><span data-stu-id="4ae31-131">Site</span></span> | <span data-ttu-id="4ae31-132">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-132">Warehouse</span></span> | <span data-ttu-id="4ae31-133">การรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-133">Receipt</span></span>   | <span data-ttu-id="4ae31-134">ออก</span><span class="sxs-lookup"><span data-stu-id="4ae31-134">Issue</span></span> | <span data-ttu-id="4ae31-135">วันที่ตามจริง</span><span class="sxs-lookup"><span data-stu-id="4ae31-135">Physical date</span></span> | <span data-ttu-id="4ae31-136">วันที่ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="4ae31-136">Financial date</span></span> | <span data-ttu-id="4ae31-137">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-137">Quantity</span></span> | <span data-ttu-id="4ae31-138">จำนวนเงินต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4ae31-138">Cost amount</span></span> | <span data-ttu-id="4ae31-139">ยอดต้นทุนจริง</span><span class="sxs-lookup"><span data-stu-id="4ae31-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="4ae31-140">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4ae31-140">Purchase order</span></span> | <span data-ttu-id="4ae31-141">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-141">1</span></span>    | <span data-ttu-id="4ae31-142">11</span><span class="sxs-lookup"><span data-stu-id="4ae31-142">11</span></span>        | <span data-ttu-id="4ae31-143">ซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ae31-143">Purchased</span></span> |       | <span data-ttu-id="4ae31-144">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="4ae31-144">March 15</span></span>      | <span data-ttu-id="4ae31-145">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="4ae31-145">March 15</span></span>       | <span data-ttu-id="4ae31-146">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-146">10</span></span>       | <span data-ttu-id="4ae31-147">1,000</span><span class="sxs-lookup"><span data-stu-id="4ae31-147">1,000</span></span>       | <span data-ttu-id="4ae31-148">1,000</span><span class="sxs-lookup"><span data-stu-id="4ae31-148">1,000</span></span>                |
| <span data-ttu-id="4ae31-149">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4ae31-149">Purchase order</span></span> | <span data-ttu-id="4ae31-150">2</span><span class="sxs-lookup"><span data-stu-id="4ae31-150">2</span></span>    | <span data-ttu-id="4ae31-151">21</span><span class="sxs-lookup"><span data-stu-id="4ae31-151">21</span></span>        | <span data-ttu-id="4ae31-152">ซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ae31-152">Purchased</span></span> |       | <span data-ttu-id="4ae31-153">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="4ae31-153">March 15</span></span>      | <span data-ttu-id="4ae31-154">15 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="4ae31-154">March 15</span></span>       | <span data-ttu-id="4ae31-155">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-155">10</span></span>       | <span data-ttu-id="4ae31-156">2,000</span><span class="sxs-lookup"><span data-stu-id="4ae31-156">2,000</span></span>       | <span data-ttu-id="4ae31-157">2,000</span><span class="sxs-lookup"><span data-stu-id="4ae31-157">2,000</span></span>                |
| <span data-ttu-id="4ae31-158">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4ae31-158">Purchase order</span></span> | <span data-ttu-id="4ae31-159">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-159">1</span></span>    | <span data-ttu-id="4ae31-160">11</span><span class="sxs-lookup"><span data-stu-id="4ae31-160">11</span></span>        | <span data-ttu-id="4ae31-161">ได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ae31-161">Received</span></span>  |       | <span data-ttu-id="4ae31-162">15 เมษายน</span><span class="sxs-lookup"><span data-stu-id="4ae31-162">April 15</span></span>      |                | <span data-ttu-id="4ae31-163">5</span><span class="sxs-lookup"><span data-stu-id="4ae31-163">5</span></span>        |             | <span data-ttu-id="4ae31-164">375</span><span class="sxs-lookup"><span data-stu-id="4ae31-164">375</span></span>                  |
| <span data-ttu-id="4ae31-165">ใบสั่งโอน</span><span class="sxs-lookup"><span data-stu-id="4ae31-165">Transfer order</span></span> | <span data-ttu-id="4ae31-166">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-166">1</span></span>    | <span data-ttu-id="4ae31-167">11</span><span class="sxs-lookup"><span data-stu-id="4ae31-167">11</span></span>        |           | <span data-ttu-id="4ae31-168">ขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ae31-168">Sold</span></span>  | <span data-ttu-id="4ae31-169">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="4ae31-169">May 2</span></span>         | <span data-ttu-id="4ae31-170">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="4ae31-170">May 2</span></span>          | <span data-ttu-id="4ae31-171">-5</span><span class="sxs-lookup"><span data-stu-id="4ae31-171">-5</span></span>       | <span data-ttu-id="4ae31-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-172">-458.33</span></span>     | <span data-ttu-id="4ae31-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-173">-458.33</span></span>              |
| <span data-ttu-id="4ae31-174">ใบสั่งโอน</span><span class="sxs-lookup"><span data-stu-id="4ae31-174">Transfer order</span></span> | <span data-ttu-id="4ae31-175">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-175">1</span></span>    | <span data-ttu-id="4ae31-176">12</span><span class="sxs-lookup"><span data-stu-id="4ae31-176">12</span></span>        | <span data-ttu-id="4ae31-177">ซื้อแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ae31-177">Purchased</span></span> |       | <span data-ttu-id="4ae31-178">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="4ae31-178">May 2</span></span>         | <span data-ttu-id="4ae31-179">พฤษภาคม 2</span><span class="sxs-lookup"><span data-stu-id="4ae31-179">May 2</span></span>          | <span data-ttu-id="4ae31-180">5</span><span class="sxs-lookup"><span data-stu-id="4ae31-180">5</span></span>        | <span data-ttu-id="4ae31-181">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-181">458.33</span></span>      | <span data-ttu-id="4ae31-182">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-182">458.33</span></span>               |
| <span data-ttu-id="4ae31-183">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="4ae31-183">Sales order</span></span>    | <span data-ttu-id="4ae31-184">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-184">1</span></span>    | <span data-ttu-id="4ae31-185">12</span><span class="sxs-lookup"><span data-stu-id="4ae31-185">12</span></span>        |           | <span data-ttu-id="4ae31-186">ขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ae31-186">Sold</span></span>  | <span data-ttu-id="4ae31-187">พฤษภาคม 3</span><span class="sxs-lookup"><span data-stu-id="4ae31-187">May 3</span></span>         | <span data-ttu-id="4ae31-188">พฤษภาคม 3</span><span class="sxs-lookup"><span data-stu-id="4ae31-188">May 3</span></span>          | <span data-ttu-id="4ae31-189">-1</span><span class="sxs-lookup"><span data-stu-id="4ae31-189">-1</span></span>       | <span data-ttu-id="4ae31-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-190">-91.67</span></span>      | <span data-ttu-id="4ae31-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="4ae31-192">วิธีการคำนวณปริมาณและยอดเงินในบักเก็ตรอบระยะเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="4ae31-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="4ae31-193">โดยใช้ข้อมูลตัวอย่างที่อธิบายไว้ในส่วนก่อนหน้านี้ คุณสามารถรันรายงาน **อายุหนี้ของสินค้าคงคลัง** ที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ae31-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="4ae31-194">**ณ วันที่:** *9 พฤษภาคม 2020*</span><span class="sxs-lookup"><span data-stu-id="4ae31-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="4ae31-195">**ไซต์:** *มุมมอง*</span><span class="sxs-lookup"><span data-stu-id="4ae31-195">**Site:** *View*</span></span>
- <span data-ttu-id="4ae31-196">**คลังสินค้า:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="4ae31-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="4ae31-197">**หมายเลขสินค้า:** *รวม*</span><span class="sxs-lookup"><span data-stu-id="4ae31-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="4ae31-198">**รอบระยะเวลาอายุหนี้:** ตั้งค่าฟิลด์นี้เพื่อสร้างกลุ่มรายเดือน</span><span class="sxs-lookup"><span data-stu-id="4ae31-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="4ae31-199">ในกรณีนี้ เนื้อหาของรายงานที่สร้างขึ้นจะมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ae31-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="4ae31-200">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-201">ไซต์</span><span class="sxs-lookup"><span data-stu-id="4ae31-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-202">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4ae31-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-203">มูลค่าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4ae31-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-204">ปริมาณมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-205">มูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-206">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="4ae31-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="4ae31-210">P1:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-211">P1:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="4ae31-212">P2:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-213">P2:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="4ae31-214">P3:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-215">P3:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="4ae31-216">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-216">1000</span></span></td>
    <td><span data-ttu-id="4ae31-217">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-217">1</span></span></td>
    <td><span data-ttu-id="4ae31-218">14</span><span class="sxs-lookup"><span data-stu-id="4ae31-218">14</span></span></td>
    <td><span data-ttu-id="4ae31-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-219">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae31-220">14</span><span class="sxs-lookup"><span data-stu-id="4ae31-220">14</span></span></td>
    <td><span data-ttu-id="4ae31-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-221">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae31-222">91.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-223">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-223">5.00</span></span></td>
    <td><span data-ttu-id="4ae31-224">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-224">458.33</span></span></td>
    <td><span data-ttu-id="4ae31-225">9.00 น.</span><span class="sxs-lookup"><span data-stu-id="4ae31-225">9.00</span></span></td>
    <td><span data-ttu-id="4ae31-226">825.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae31-227">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-227">1000</span></span></td>
    <td><span data-ttu-id="4ae31-228">2</span><span class="sxs-lookup"><span data-stu-id="4ae31-228">2</span></span></td>
    <td><span data-ttu-id="4ae31-229">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-229">10</span></span></td>
    <td><span data-ttu-id="4ae31-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-230">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae31-231">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-231">10</span></span></td>
    <td><span data-ttu-id="4ae31-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-232">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae31-233">200.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-234">10.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-234">10.00</span></span></td>
    <td><span data-ttu-id="4ae31-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="4ae31-236"><strong>ยอดรวม 1000</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae31-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="4ae31-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="4ae31-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="4ae31-243">หมายเหตุรายละเอียดต่อไปนี้ในรายงานตัวอย่างนี้:</span><span class="sxs-lookup"><span data-stu-id="4ae31-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="4ae31-244">**ปริมาณมูลค่าสินค้าคงคลัง** **มูลค่าสินค้าคงคลัง** และมูลค่า **ต้นทุนต่อหน่วยเฉลี่ย** ที่แสดงอยู่ในรายงาน เป็นค่าสำหรับมิติสินค้าคงคลังทางการเงิน (**ไซต์** ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="4ae31-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="4ae31-245">ตัวอย่างเช่น สำหรับไซต์ 1 รายงานจะแสดงข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ae31-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="4ae31-246">ค่า **ปริมาณมูลค่าสินค้าคงคลัง** คือ *14* (= 10 + 5 – 5 + 5 – 1)</span><span class="sxs-lookup"><span data-stu-id="4ae31-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="4ae31-247">ค่า **มูลค่าสินค้าคงคลัง** คือ *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67)</span><span class="sxs-lookup"><span data-stu-id="4ae31-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="4ae31-248">ค่า **ต้นทุนต่อหน่วยเฉลี่ย** คือ *91.67*</span><span class="sxs-lookup"><span data-stu-id="4ae31-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="4ae31-249">ค่า **มูลค่าคงเหลือ** และค่า **จำนวน** ในบักเก็ตรอบระยะเวลาแต่ละรายการ จะถูกคำนวณโดยใช้ค่า **ต้นทุนต่อหน่วยเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="4ae31-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="4ae31-250">รายงานจะกำหนดปริมาณคงคลังคงเหลือสำหรับบักเก็ตรอบระยะเวลาแต่ละรายการ โดยสรุปปริมาณสินค้าคงคลังที่ได้รับรวมสำหรับบักเก็ตรอบระยะเวลาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="4ae31-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="4ae31-251">จากนั้น จะใช้หลักการแบบเข้าก่อนออกก่อน (FIFO) เพื่อหักลบปริมาณที่นำออกใช้ทั้งหมด โดยไม่คำนึงถึงแบบจำลองสินค้าคงคลังที่สินค้าใช้</span><span class="sxs-lookup"><span data-stu-id="4ae31-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="4ae31-252">ถ้าคุณรันรายงานเดียวกันอีกครั้ง แต่ครั้งนี้คุณตั้งค่าทั้งฟิลด์ **ไซต์** และฟิลด์ **คลังสินค้า** เพื่อ *ดู* รายงานใหม่จะมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ae31-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="4ae31-253">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-254">ไซต์</span><span class="sxs-lookup"><span data-stu-id="4ae31-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-255">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-256">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4ae31-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-257">มูลค่าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4ae31-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-258">ปริมาณมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-259">มูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-260">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="4ae31-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="4ae31-264">P1:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-265">P1:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="4ae31-266">P2:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-267">P2:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="4ae31-268">P3:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-269">P3:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="4ae31-270">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-270">1000</span></span></td>
    <td><span data-ttu-id="4ae31-271">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-271">1</span></span></td>
    <td><span data-ttu-id="4ae31-272">11</span><span class="sxs-lookup"><span data-stu-id="4ae31-272">11</span></span></td>
    <td><span data-ttu-id="4ae31-273">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-273">10</span></span></td>
    <td><span data-ttu-id="4ae31-274">916.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-274">916.67</span></span></td>
    <td><span data-ttu-id="4ae31-275">14</span><span class="sxs-lookup"><span data-stu-id="4ae31-275">14</span></span></td>
    <td><span data-ttu-id="4ae31-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-276">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae31-277">91.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-278">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-278">5.00</span></span></td>
    <td><span data-ttu-id="4ae31-279">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-279">458.33</span></span></td>
    <td><span data-ttu-id="4ae31-280">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-280">5.00</span></span></td>
    <td><span data-ttu-id="4ae31-281">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae31-282">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-282">1000</span></span></td>
    <td><span data-ttu-id="4ae31-283">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-283">1</span></span></td>
    <td><span data-ttu-id="4ae31-284">12</span><span class="sxs-lookup"><span data-stu-id="4ae31-284">12</span></span></td>
    <td><span data-ttu-id="4ae31-285">4</span><span class="sxs-lookup"><span data-stu-id="4ae31-285">4</span></span></td>
    <td><span data-ttu-id="4ae31-286">366.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-286">366.67</span></span></td>
    <td><span data-ttu-id="4ae31-287">14</span><span class="sxs-lookup"><span data-stu-id="4ae31-287">14</span></span></td>
    <td><span data-ttu-id="4ae31-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae31-288">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae31-289">91.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-289">91.67</span></span></td>
    <td><span data-ttu-id="4ae31-290">4.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-290">4.00</span></span></td>
    <td><span data-ttu-id="4ae31-291">366.67</span><span class="sxs-lookup"><span data-stu-id="4ae31-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae31-292">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-292">1000</span></span></td>
    <td><span data-ttu-id="4ae31-293">2</span><span class="sxs-lookup"><span data-stu-id="4ae31-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae31-294">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-294">10</span></span></td>
    <td><span data-ttu-id="4ae31-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-295">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae31-296">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-296">10</span></span></td>
    <td><span data-ttu-id="4ae31-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-297">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae31-298">200.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-299">10.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-299">10.00</span></span></td>
    <td><span data-ttu-id="4ae31-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="4ae31-301"><strong>ยอดรวม 1000</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="4ae31-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="4ae31-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="4ae31-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="4ae31-310">เวลานี้ ไซต์ 1 ถูกแบ่งออกเป็นสองแถว หนึ่งแถวสำหรับคลังสินค้า 11 และหนึ่งแถวสำหรับคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="4ae31-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="4ae31-311">อย่างไรก็ตาม ค่า **ปริมาณมูลค่าสินค้าคงคลัง** **มูลค่าสินค้าคงคลัง** และ **ต้นทุนต่อหน่วยเฉลี่ย** เป็นค่าเดียวกัน เนื่องจาก **คลังสินค้า** ไม่ใช่มิติสินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="4ae31-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="4ae31-312">นอกจากนี้ โปรดสังเกตว่าการกระจายปริมาณของไซต์ 1 แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="4ae31-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="4ae31-313">ในรายงานแรกที่คุณรัน ระบบจะละเว้นใบสั่งโอนย้ายที่เกิดขึ้นในไซต์เดียวกันและมีการหักลบปริมาณของใบแจ้งหนี้การขายจากบักเก็ตรอบระยะเวลา **3/31/2020-3/1/2020** ในไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="4ae31-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="4ae31-314">อย่างไรก็ตาม ในรายงานใหม่ ระบบจะหักปริมาณของใบแจ้งหนี้การขายจากบักเก็ตรอบระยะเวลา **5/8/2020-5/1/2020** ในคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="4ae31-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="4ae31-315">ผลกระทบของการปิดบัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-315">Effects of inventory closing</span></span>

<span data-ttu-id="4ae31-316">ถ้าคุณรันการปิดบัญชีสินค้าคงคลังสำหรับเดือนพฤษภาคม และจากนั้น รันรายงานก่อนหน้านี้อีกครั้ง แต่คุณตั้งค่าฟิลด์ **ณ วันที่** เป็น *31 พฤษภาคม 2020* คุณจะพบผลลัพธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ae31-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="4ae31-317">มีการปรับปรุงค่า **มูลค่าสินค้าคงคลัง** และค่า **ต้นทุนต่อหน่วยโดยเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="4ae31-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="4ae31-318">ค่า **มูลค่าคงเหลือ** และค่า **จำนวน** ทั้งหมดในบักเก็ตรอบระยะเวลาทุกรายการจะถูกปรับปรุงโดยสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4ae31-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="4ae31-319">รายงานใหม่จะมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ae31-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="4ae31-320">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-321">ไซต์</span><span class="sxs-lookup"><span data-stu-id="4ae31-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-322">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ae31-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-323">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4ae31-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-324">มูลค่าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="4ae31-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-325">ปริมาณมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-326">มูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ae31-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae31-327">ต้นทุนเฉลี่ยต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="4ae31-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae31-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="4ae31-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="4ae31-331">P1:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-332">P1:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="4ae31-333">P2:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-334">P2:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="4ae31-335">P3:ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="4ae31-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="4ae31-336">P3:จำนวน</span><span class="sxs-lookup"><span data-stu-id="4ae31-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="4ae31-337">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-337">1000</span></span></td>
    <td><span data-ttu-id="4ae31-338">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-338">1</span></span></td>
    <td><span data-ttu-id="4ae31-339">11</span><span class="sxs-lookup"><span data-stu-id="4ae31-339">11</span></span></td>
    <td><span data-ttu-id="4ae31-340">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-340">10</span></span></td>
    <td><span data-ttu-id="4ae31-341">910.70</span><span class="sxs-lookup"><span data-stu-id="4ae31-341">910.70</span></span></td>
    <td><span data-ttu-id="4ae31-342">14</span><span class="sxs-lookup"><span data-stu-id="4ae31-342">14</span></span></td>
    <td><span data-ttu-id="4ae31-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-343">1,275.00</span></span></td>
    <td><span data-ttu-id="4ae31-344">91.07</span><span class="sxs-lookup"><span data-stu-id="4ae31-344">91.07</span></span></td>
    <td><span data-ttu-id="4ae31-345">0.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae31-346">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-346">5.00</span></span></td>
    <td><span data-ttu-id="4ae31-347">455.36</span><span class="sxs-lookup"><span data-stu-id="4ae31-347">455.36</span></span></td>
    <td><span data-ttu-id="4ae31-348">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-348">5.00</span></span></td>
    <td><span data-ttu-id="4ae31-349">455.36</span><span class="sxs-lookup"><span data-stu-id="4ae31-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae31-350">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-350">1000</span></span></td>
    <td><span data-ttu-id="4ae31-351">1</span><span class="sxs-lookup"><span data-stu-id="4ae31-351">1</span></span></td>
    <td><span data-ttu-id="4ae31-352">12</span><span class="sxs-lookup"><span data-stu-id="4ae31-352">12</span></span></td>
    <td><span data-ttu-id="4ae31-353">4</span><span class="sxs-lookup"><span data-stu-id="4ae31-353">4</span></span></td>
    <td><span data-ttu-id="4ae31-354">364.29</span><span class="sxs-lookup"><span data-stu-id="4ae31-354">364.29</span></span></td>
    <td><span data-ttu-id="4ae31-355">14</span><span class="sxs-lookup"><span data-stu-id="4ae31-355">14</span></span></td>
    <td><span data-ttu-id="4ae31-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-356">1,275.00</span></span></td>
    <td><span data-ttu-id="4ae31-357">91.07</span><span class="sxs-lookup"><span data-stu-id="4ae31-357">91.07</span></span></td>
    <td><span data-ttu-id="4ae31-358">4.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-358">4.00</span></span></td>
    <td><span data-ttu-id="4ae31-359">364.29</span><span class="sxs-lookup"><span data-stu-id="4ae31-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae31-360">1000</span><span class="sxs-lookup"><span data-stu-id="4ae31-360">1000</span></span></td>
    <td><span data-ttu-id="4ae31-361">2</span><span class="sxs-lookup"><span data-stu-id="4ae31-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae31-362">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-362">10</span></span></td>
    <td><span data-ttu-id="4ae31-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-363">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae31-364">10</span><span class="sxs-lookup"><span data-stu-id="4ae31-364">10</span></span></td>
    <td><span data-ttu-id="4ae31-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-365">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae31-366">200.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-367">10.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-367">10.00</span></span></td>
    <td><span data-ttu-id="4ae31-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae31-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="4ae31-369"><strong>ยอดรวม 1000</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae31-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="4ae31-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="4ae31-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="4ae31-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="4ae31-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="4ae31-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
