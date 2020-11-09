---
title: ตั้งค่าการแม็ปสำหรับฟิลด์สถานะของใบสั่งขาย
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าฟิลด์สถานะของใบสั่งขายสำหรับการรวมแบบสองทิศทาง
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997685"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="128da-103">ตั้งค่าการแม็ปสำหรับฟิลด์สถานะของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="128da-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="128da-104">ฟิลด์ที่บ่งชี้สถานะของใบสั่งขายมีค่าการแจงนับที่แตกต่างกันใน Microsoft Dynamics 365 Supply Chain Management และ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="128da-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="128da-105">ต้องมีการตั้งค่าเพิ่มเติมเพื่อแม็ปฟิลด์เหล่านี้ในการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="128da-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="128da-106">ฟิลด์ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="128da-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="128da-107">ใน Supply Chain Management ฟิลด์สองฟิลด์จะสะท้อนถึงสถานะของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="128da-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="128da-108">ฟิลด์ที่คุณต้องแม็ปคือ **สถานะ** และ **สถานะเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="128da-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="128da-109">การแจง **สถานะ** ระบุสถานะโดยรวมของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="128da-110">สถานะนี้จะแสดงอยู่บนส่วนหน้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-110">This status is shown on the order header.</span></span>

<span data-ttu-id="128da-111">การแจงนับ **สถานะ** มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="128da-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="128da-112">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-112">Open Order</span></span>
- <span data-ttu-id="128da-113">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-113">Delivered</span></span>
- <span data-ttu-id="128da-114">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-114">Invoiced</span></span>
- <span data-ttu-id="128da-115">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-115">Cancelled</span></span>

<span data-ttu-id="128da-116">การแจง **สถานะของเอกสาร** ระบุเอกสารล่าสุดที่สร้างขึ้นสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="128da-117">ตัวอย่างเช่น ถ้ายืนยันใบสั่งแล้ว เอกสารนี้เป็นการยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="128da-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="128da-118">ถ้าใบสั่งขายมีการออกใบแจ้งหนี้แล้วบางส่วน บรรทัดที่เหลือจะถูกยืนยัน สถานะเอกสารยังคงมีการ **ออกใบแจ้งหนี้** เนื่องจากมีการสร้างใบแจ้งหนี้ในภายหลังในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="128da-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice** , because the invoice is generated later in the process.</span></span>

<span data-ttu-id="128da-119">การแจงนับ **สถานะเอกสาร** มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="128da-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="128da-120">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="128da-120">Confirmation</span></span>
- <span data-ttu-id="128da-121">รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="128da-121">Picking List</span></span>
- <span data-ttu-id="128da-122">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="128da-122">Packing Slip</span></span>
- <span data-ttu-id="128da-123">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="128da-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="128da-124">ฟิลด์ในการขาย</span><span class="sxs-lookup"><span data-stu-id="128da-124">Fields in Sales</span></span>

<span data-ttu-id="128da-125">ในการขาย มีสองฟิลด์ที่บ่งชี้สถานะของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="128da-126">ฟิลด์ที่คุณต้องแม็ปคือ **สถานะ** และ **สถานะการประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="128da-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="128da-127">การแจง **สถานะ** ระบุสถานะโดยรวมของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="128da-128">ซึ่งมีค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="128da-128">It has the following values:</span></span>

- <span data-ttu-id="128da-129">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="128da-129">Active</span></span>
- <span data-ttu-id="128da-130">ส่ง</span><span class="sxs-lookup"><span data-stu-id="128da-130">Submitted</span></span>
- <span data-ttu-id="128da-131">เติมเต็มแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-131">Fulfilled</span></span>
- <span data-ttu-id="128da-132">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-132">Invoiced</span></span>
- <span data-ttu-id="128da-133">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-133">Cancelled</span></span>

<span data-ttu-id="128da-134">การแจงนับ **สถานะการประมวลผล** ถูกนำมาใช้เพื่อให้สามารถแม็ปสถานะได้อย่างถูกต้องกับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="128da-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="128da-135">ตารางต่อไปนี้แสดงการแม็ป **สถานะการประมวลผล** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="128da-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="128da-136">สถานะการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="128da-136">Processing Status</span></span>   | <span data-ttu-id="128da-137">สถานะใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="128da-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="128da-138">สถานะเอกสารใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="128da-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="128da-139">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="128da-139">Active</span></span>              | <span data-ttu-id="128da-140">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-140">Open Order</span></span>                        | <span data-ttu-id="128da-141">None</span><span class="sxs-lookup"><span data-stu-id="128da-141">None</span></span>                                       |
| <span data-ttu-id="128da-142">ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="128da-142">Confirmed</span></span>           | <span data-ttu-id="128da-143">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-143">Open Order</span></span>                        | <span data-ttu-id="128da-144">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="128da-144">Confirmation</span></span>                               |
| <span data-ttu-id="128da-145">เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-145">Picked</span></span>              | <span data-ttu-id="128da-146">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-146">Open Order</span></span>                        | <span data-ttu-id="128da-147">รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="128da-147">Picking List</span></span>                               |
| <span data-ttu-id="128da-148">จัดส่งสินค้าแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="128da-148">Partially Delivered</span></span> | <span data-ttu-id="128da-149">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-149">Open Order</span></span>                        | <span data-ttu-id="128da-150">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="128da-150">Packing Slip</span></span>                               |
| <span data-ttu-id="128da-151">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-151">Delivered</span></span>           | <span data-ttu-id="128da-152">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-152">Delivered</span></span>                         | <span data-ttu-id="128da-153">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="128da-153">Packing Slip</span></span>                               |
| <span data-ttu-id="128da-154">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="128da-154">Partially Invoiced</span></span>  | <span data-ttu-id="128da-155">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-155">Delivered</span></span>                         | <span data-ttu-id="128da-156">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="128da-156">Invoice</span></span>                                    |
| <span data-ttu-id="128da-157">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-157">Invoiced</span></span>            | <span data-ttu-id="128da-158">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-158">Invoiced</span></span>                          | <span data-ttu-id="128da-159">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="128da-159">Invoice</span></span>                                    |
| <span data-ttu-id="128da-160">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-160">Cancelled</span></span>           | <span data-ttu-id="128da-161">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-161">Cancelled</span></span>                         | <span data-ttu-id="128da-162">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="128da-162">Not applicable</span></span>                             |

<span data-ttu-id="128da-163">ตารางต่อไปนี้แสดงการแม็ป **สถานะการประมวลผล** ระหว่างการขายและ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="128da-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="128da-164">สถานะการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="128da-164">Processing Status</span></span>   | <span data-ttu-id="128da-165">สถานะในการขาย</span><span class="sxs-lookup"><span data-stu-id="128da-165">Status in Sales</span></span> | <span data-ttu-id="128da-166">สถานะใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="128da-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="128da-167">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="128da-167">Active</span></span>              | <span data-ttu-id="128da-168">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="128da-168">Active</span></span>          | <span data-ttu-id="128da-169">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-169">Open Order</span></span>                        |
| <span data-ttu-id="128da-170">ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="128da-170">Confirmed</span></span>           | <span data-ttu-id="128da-171">ส่ง</span><span class="sxs-lookup"><span data-stu-id="128da-171">Submitted</span></span>       | <span data-ttu-id="128da-172">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-172">Open Order</span></span>                        |
| <span data-ttu-id="128da-173">เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-173">Picked</span></span>              | <span data-ttu-id="128da-174">ส่ง</span><span class="sxs-lookup"><span data-stu-id="128da-174">Submitted</span></span>       | <span data-ttu-id="128da-175">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-175">Open Order</span></span>                        |
| <span data-ttu-id="128da-176">จัดส่งสินค้าแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="128da-176">Partially Delivered</span></span> | <span data-ttu-id="128da-177">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="128da-177">Active</span></span>          | <span data-ttu-id="128da-178">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-178">Open Order</span></span>                        |
| <span data-ttu-id="128da-179">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="128da-179">Partially Invoiced</span></span>  | <span data-ttu-id="128da-180">ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="128da-180">Active</span></span>          | <span data-ttu-id="128da-181">เปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="128da-181">Open Order</span></span>                        |
| <span data-ttu-id="128da-182">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="128da-182">Partially Invoiced</span></span>  | <span data-ttu-id="128da-183">เติมเต็มแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-183">Fulfilled</span></span>       | <span data-ttu-id="128da-184">จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-184">Delivered</span></span>                         |
| <span data-ttu-id="128da-185">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-185">Invoiced</span></span>            | <span data-ttu-id="128da-186">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-186">Invoiced</span></span>        | <span data-ttu-id="128da-187">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-187">Invoiced</span></span>                          |
| <span data-ttu-id="128da-188">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-188">Cancelled</span></span>           | <span data-ttu-id="128da-189">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-189">Cancelled</span></span>       | <span data-ttu-id="128da-190">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="128da-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="128da-191">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="128da-191">Setup</span></span>

<span data-ttu-id="128da-192">เมื่อต้องการตั้งค่าการแม็ปสำหรับฟิลด์สถานะของใบสั่งขาย คุณต้องเปิดใช้งานแอตทริบิวต์ **IsSOPIntegrationEnabled** **isIntegrationUser**</span><span class="sxs-lookup"><span data-stu-id="128da-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="128da-193">เมื่อต้องการเปิดใช้งานแอตทริบิวต์ **IsSOPIntegrationEnabled** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="128da-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="128da-194">ในเบราเซอร์ ไปที่ `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`</span><span class="sxs-lookup"><span data-stu-id="128da-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="128da-195">แทนที่ **\<test-name\>** ด้วยลิงก์ของบริษัทของคุณไปยังการขาย</span><span class="sxs-lookup"><span data-stu-id="128da-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="128da-196">บนหน้าที่เปิดอยู่ ให้ค้นหา **organizationid** และจดบันทึกค่า</span><span class="sxs-lookup"><span data-stu-id="128da-196">On the page that is opened, find **organizationid** , and make a note of the value.</span></span>

    ![การค้นหา organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="128da-198">ในการขาย ให้เปิดคอนโซลของเบราว์เซอร์แล้วรันสคริปต์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="128da-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="128da-199">ใช้ค่า **organizationid** จากขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="128da-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![รหัส JavaScript ในคอนโซลของเบราว์เซอร์](media/sales-map-script.png)

4. <span data-ttu-id="128da-201">ตรวจสอบว่ามีการตั้งค่า **IsSOPIntegrationEnabled** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="128da-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="128da-202">ใช้ URL จากขั้นตอนที่ 1 เพื่อตรวจสอบค่า</span><span class="sxs-lookup"><span data-stu-id="128da-202">Use the URL from step 1 to check the value.</span></span>

    ![ตั้งค่า IsSOPIntegrationEnabled เป็นจริง](media/sales-map-integration-enabled.png)

<span data-ttu-id="128da-204">เมื่อต้องการเปิดใช้งานแอตทริบิวต์ **isIntegrationUser** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="128da-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="128da-205">ในการขาย ให้ไปที่ **การตั้งค่า \> การกำหนดเอง \> การกำหนดเองของระบบ** เลือก **เอนทิตีผู้ใช้** แล้วเปิด **ฟอร์ม \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="128da-205">In Sales, go to **Setting \> Customization \> Customize the System** , select **User entity** , and then open **Form \> User**.</span></span>

    ![การเปิดแบบฟอร์มผู้ใช้](media/sales-map-user.png)

2. <span data-ttu-id="128da-207">ในฟิลด์ Explorer ให้ค้นหา **โหมดผู้ใช้การรวม** และคลิกสองครั้งเพื่อเพิ่มในแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="128da-207">In Field Explorer, find **Integration user mode** , and double-click it to add it to the form.</span></span> <span data-ttu-id="128da-208">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="128da-208">Save your change.</span></span>

    ![กำลังเพิ่มฟิลด์โหมดผู้ใช้ในการรวมกับแบบฟอร์ม](media/sales-map-field-explorer.png)

3. <span data-ttu-id="128da-210">ในการขาย ให้ไปที่ **การตั้งค่า \> ความปลอดภัย \> ผู้ใช้** และเปลี่ยนมุมมองจาก **ผู้ใช้ที่เปิดใช้งาน** เป็น **ผู้ใช้แอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="128da-210">In Sales, go to **Setting \> Security \> Users** , and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![การเปลี่ยนมุมมองจากผู้ใช้ที่เปิดใช้งานเป็นผู้ใช้แอปพลิเคชัน](media/sales-map-enabled-users.png)

4. <span data-ttu-id="128da-212">เลือกรายการสองรายการสำหรับ **DualWrite IntegrationUser**</span><span class="sxs-lookup"><span data-stu-id="128da-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![รายการของผู้ใช้แอปพลิเคชัน](media/sales-map-user-mode.png)

5. <span data-ttu-id="128da-214">เปลี่ยนค่าของฟิลด์ **โหมดผู้ใช้การรวม** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="128da-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![การเปลี่ยนค่าของฟิลด์โหมดผู้ใช้การรวม](media/sales-map-user-mode-yes.png)

<span data-ttu-id="128da-216">ขณะนี้มีการแม็ปใบสั่งขายของคุณ</span><span class="sxs-lookup"><span data-stu-id="128da-216">Your sales orders are now mapped.</span></span>
