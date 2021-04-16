---
title: ตั้งค่าการแม็ปสำหรับคอลัมน์สถานะของใบสั่งขาย
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอลัมน์สถานะของใบสั่งขายสำหรับการรวมแบบสองทิศทาง
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750725"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="3f0b7-103">ตั้งค่าการแม็ปสำหรับคอลัมน์สถานะของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3f0b7-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f0b7-104">คอลัมน์ที่บ่งชี้สถานะของใบสั่งขายมีค่าการแจงนับที่แตกต่างกันใน Microsoft Dynamics 365 Supply Chain Management และ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="3f0b7-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="3f0b7-105">ต้องมีการตั้งค่าเพิ่มเติมเพื่อแม็ปคอลัมน์เหล่านี้ในการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="3f0b7-106">คอลัมน์ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3f0b7-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="3f0b7-107">ใน Supply Chain Management คอลัมน์สองคอลัมน์จะสะท้อนถึงสถานะของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3f0b7-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="3f0b7-108">คอลัมน์ที่คุณต้องแม็ปคือ **สถานะ** และ **สถานะเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="3f0b7-109">การแจง **สถานะ** ระบุสถานะโดยรวมของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="3f0b7-110">สถานะนี้จะแสดงอยู่บนส่วนหน้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-110">This status is shown on the order header.</span></span>

<span data-ttu-id="3f0b7-111">การแจงนับ **สถานะ** มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3f0b7-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="3f0b7-112">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-112">Open Order</span></span>
- <span data-ttu-id="3f0b7-113">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-113">Delivered</span></span>
- <span data-ttu-id="3f0b7-114">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-114">Invoiced</span></span>
- <span data-ttu-id="3f0b7-115">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-115">Cancelled</span></span>

<span data-ttu-id="3f0b7-116">การแจง **สถานะของเอกสาร** ระบุเอกสารล่าสุดที่สร้างขึ้นสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="3f0b7-117">ตัวอย่างเช่น ถ้ายืนยันใบสั่งแล้ว เอกสารนี้เป็นการยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3f0b7-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="3f0b7-118">ถ้าใบสั่งขายมีการออกใบแจ้งหนี้แล้วบางส่วน บรรทัดที่เหลือจะถูกยืนยัน สถานะเอกสารยังคงมีการ **ออกใบแจ้งหนี้** เนื่องจากมีการสร้างใบแจ้งหนี้ในภายหลังในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="3f0b7-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="3f0b7-119">การแจงนับ **สถานะเอกสาร** มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3f0b7-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="3f0b7-120">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3f0b7-120">Confirmation</span></span>
- <span data-ttu-id="3f0b7-121">รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3f0b7-121">Picking List</span></span>
- <span data-ttu-id="3f0b7-122">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-122">Packing Slip</span></span>
- <span data-ttu-id="3f0b7-123">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="3f0b7-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="3f0b7-124">คอลัมน์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="3f0b7-124">columns in Sales</span></span>

<span data-ttu-id="3f0b7-125">ในการขาย มีสองคอลัมน์ที่บ่งชี้สถานะของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="3f0b7-126">คอลัมน์ที่คุณต้องแม็ปคือ **สถานะ** และ **สถานะการประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="3f0b7-127">การแจง **สถานะ** ระบุสถานะโดยรวมของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="3f0b7-128">ซึ่งมีค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3f0b7-128">It has the following values:</span></span>

- <span data-ttu-id="3f0b7-129">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="3f0b7-129">Active</span></span>
- <span data-ttu-id="3f0b7-130">ส่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-130">Submitted</span></span>
- <span data-ttu-id="3f0b7-131">เติมเต็มแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-131">Fulfilled</span></span>
- <span data-ttu-id="3f0b7-132">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-132">Invoiced</span></span>
- <span data-ttu-id="3f0b7-133">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-133">Cancelled</span></span>

<span data-ttu-id="3f0b7-134">การแจงนับ **สถานะการประมวลผล** ถูกนำมาใช้เพื่อให้สามารถแม็ปสถานะได้อย่างถูกต้องกับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3f0b7-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="3f0b7-135">ตารางต่อไปนี้แสดงการแม็ป **สถานะการประมวลผล** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3f0b7-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="3f0b7-136">สถานะการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="3f0b7-136">Processing Status</span></span>   | <span data-ttu-id="3f0b7-137">สถานะใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3f0b7-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="3f0b7-138">สถานะเอกสารใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3f0b7-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="3f0b7-139">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="3f0b7-139">Active</span></span>              | <span data-ttu-id="3f0b7-140">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-140">Open Order</span></span>                        | <span data-ttu-id="3f0b7-141">None</span><span class="sxs-lookup"><span data-stu-id="3f0b7-141">None</span></span>                                       |
| <span data-ttu-id="3f0b7-142">ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="3f0b7-142">Confirmed</span></span>           | <span data-ttu-id="3f0b7-143">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-143">Open Order</span></span>                        | <span data-ttu-id="3f0b7-144">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3f0b7-144">Confirmation</span></span>                               |
| <span data-ttu-id="3f0b7-145">เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-145">Picked</span></span>              | <span data-ttu-id="3f0b7-146">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-146">Open Order</span></span>                        | <span data-ttu-id="3f0b7-147">รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="3f0b7-147">Picking List</span></span>                               |
| <span data-ttu-id="3f0b7-148">จัดส่งสินค้าแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3f0b7-148">Partially Delivered</span></span> | <span data-ttu-id="3f0b7-149">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-149">Open Order</span></span>                        | <span data-ttu-id="3f0b7-150">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-150">Packing Slip</span></span>                               |
| <span data-ttu-id="3f0b7-151">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-151">Delivered</span></span>           | <span data-ttu-id="3f0b7-152">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-152">Delivered</span></span>                         | <span data-ttu-id="3f0b7-153">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-153">Packing Slip</span></span>                               |
| <span data-ttu-id="3f0b7-154">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3f0b7-154">Partially Invoiced</span></span>  | <span data-ttu-id="3f0b7-155">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-155">Delivered</span></span>                         | <span data-ttu-id="3f0b7-156">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="3f0b7-156">Invoice</span></span>                                    |
| <span data-ttu-id="3f0b7-157">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-157">Invoiced</span></span>            | <span data-ttu-id="3f0b7-158">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-158">Invoiced</span></span>                          | <span data-ttu-id="3f0b7-159">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="3f0b7-159">Invoice</span></span>                                    |
| <span data-ttu-id="3f0b7-160">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-160">Cancelled</span></span>           | <span data-ttu-id="3f0b7-161">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-161">Cancelled</span></span>                         | <span data-ttu-id="3f0b7-162">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="3f0b7-162">Not applicable</span></span>                             |

<span data-ttu-id="3f0b7-163">ตารางต่อไปนี้แสดงการแม็ป **สถานะการประมวลผล** ระหว่างการขายและ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3f0b7-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="3f0b7-164">สถานะการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="3f0b7-164">Processing Status</span></span>   | <span data-ttu-id="3f0b7-165">สถานะในการขาย</span><span class="sxs-lookup"><span data-stu-id="3f0b7-165">Status in Sales</span></span> | <span data-ttu-id="3f0b7-166">สถานะใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3f0b7-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="3f0b7-167">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="3f0b7-167">Active</span></span>              | <span data-ttu-id="3f0b7-168">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="3f0b7-168">Active</span></span>          | <span data-ttu-id="3f0b7-169">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-169">Open Order</span></span>                        |
| <span data-ttu-id="3f0b7-170">ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="3f0b7-170">Confirmed</span></span>           | <span data-ttu-id="3f0b7-171">ส่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-171">Submitted</span></span>       | <span data-ttu-id="3f0b7-172">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-172">Open Order</span></span>                        |
| <span data-ttu-id="3f0b7-173">เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-173">Picked</span></span>              | <span data-ttu-id="3f0b7-174">ส่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-174">Submitted</span></span>       | <span data-ttu-id="3f0b7-175">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-175">Open Order</span></span>                        |
| <span data-ttu-id="3f0b7-176">จัดส่งสินค้าแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3f0b7-176">Partially Delivered</span></span> | <span data-ttu-id="3f0b7-177">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="3f0b7-177">Active</span></span>          | <span data-ttu-id="3f0b7-178">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-178">Open Order</span></span>                        |
| <span data-ttu-id="3f0b7-179">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3f0b7-179">Partially Invoiced</span></span>  | <span data-ttu-id="3f0b7-180">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="3f0b7-180">Active</span></span>          | <span data-ttu-id="3f0b7-181">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-181">Open Order</span></span>                        |
| <span data-ttu-id="3f0b7-182">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="3f0b7-182">Partially Invoiced</span></span>  | <span data-ttu-id="3f0b7-183">เติมเต็มแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-183">Fulfilled</span></span>       | <span data-ttu-id="3f0b7-184">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-184">Delivered</span></span>                         |
| <span data-ttu-id="3f0b7-185">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-185">Invoiced</span></span>            | <span data-ttu-id="3f0b7-186">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-186">Invoiced</span></span>        | <span data-ttu-id="3f0b7-187">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-187">Invoiced</span></span>                          |
| <span data-ttu-id="3f0b7-188">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-188">Cancelled</span></span>           | <span data-ttu-id="3f0b7-189">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="3f0b7-189">Cancelled</span></span>       | <span data-ttu-id="3f0b7-190">ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="3f0b7-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="3f0b7-191">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3f0b7-191">Setup</span></span>

<span data-ttu-id="3f0b7-192">เมื่อต้องการตั้งค่าการแม็ปสำหรับคอลัมน์สถานะของใบสั่งขาย คุณต้องเปิดใช้งานแอตทริบิวต์ **IsSOPIntegrationEnabled** **isIntegrationUser**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="3f0b7-193">เมื่อต้องการเปิดใช้งานแอตทริบิวต์ **IsSOPIntegrationEnabled** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3f0b7-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="3f0b7-194">ในเบราเซอร์ ไปที่ `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`</span><span class="sxs-lookup"><span data-stu-id="3f0b7-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="3f0b7-195">แทนที่ **\<test-name\>** ด้วยลิงก์ของบริษัทของคุณไปยังการขาย</span><span class="sxs-lookup"><span data-stu-id="3f0b7-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="3f0b7-196">บนหน้าที่เปิดอยู่ ให้ค้นหา **organizationid** และจดบันทึกค่า</span><span class="sxs-lookup"><span data-stu-id="3f0b7-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![การค้นหา organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="3f0b7-198">ในการขาย ให้เปิดคอนโซลของเบราว์เซอร์แล้วรันสคริปต์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3f0b7-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="3f0b7-199">ใช้ค่า **organizationid** จากขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="3f0b7-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![รหัส JavaScript ในคอนโซลของเบราว์เซอร์](media/sales-map-script.png)

4. <span data-ttu-id="3f0b7-201">ตรวจสอบว่ามีการตั้งค่า **IsSOPIntegrationEnabled** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="3f0b7-202">ใช้ URL จากขั้นตอนที่ 1 เพื่อตรวจสอบค่า</span><span class="sxs-lookup"><span data-stu-id="3f0b7-202">Use the URL from step 1 to check the value.</span></span>

    ![ตั้งค่า IsSOPIntegrationEnabled เป็นจริง](media/sales-map-integration-enabled.png)

<span data-ttu-id="3f0b7-204">เมื่อต้องการเปิดใช้งานแอตทริบิวต์ **isIntegrationUser** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3f0b7-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="3f0b7-205">ในการขาย ให้ไปที่ **การตั้งค่า \> การกำหนดเอง \> การกำหนดเองของระบบ** เลือก **ตารางผู้ใช้** แล้วเปิด **ฟอร์ม \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![การเปิดแบบฟอร์มผู้ใช้](media/sales-map-user.png)

2. <span data-ttu-id="3f0b7-207">ในฟิลด์ Explorer ให้ค้นหา **โหมดผู้ใช้การรวม** และคลิกสองครั้งเพื่อเพิ่มในแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="3f0b7-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="3f0b7-208">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3f0b7-208">Save your change.</span></span>

    ![กำลังเพิ่มคอลัมน์โหมดผู้ใช้ในการรวมกับแบบฟอร์ม](media/sales-map-field-explorer.png)

3. <span data-ttu-id="3f0b7-210">ในการขาย ให้ไปที่ **การตั้งค่า \> ความปลอดภัย \> ผู้ใช้** และเปลี่ยนมุมมองจาก **ผู้ใช้ที่เปิดใช้งาน** เป็น **ผู้ใช้แอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![การเปลี่ยนมุมมองจากผู้ใช้ที่เปิดใช้งานเป็นผู้ใช้แอปพลิเคชัน](media/sales-map-enabled-users.png)

4. <span data-ttu-id="3f0b7-212">เลือกรายการสองรายการสำหรับ **DualWrite IntegrationUser**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![รายการของผู้ใช้แอปพลิเคชัน](media/sales-map-user-mode.png)

5. <span data-ttu-id="3f0b7-214">เปลี่ยนค่าของคอลัมน์ **โหมดผู้ใช้การรวม** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3f0b7-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![การเปลี่ยนค่าของคอลัมน์โหมดผู้ใช้การรวม](media/sales-map-user-mode-yes.png)

<span data-ttu-id="3f0b7-216">ขณะนี้มีการแม็ปใบสั่งขายของคุณ</span><span class="sxs-lookup"><span data-stu-id="3f0b7-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]