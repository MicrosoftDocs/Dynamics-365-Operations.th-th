---
title: นโยบายงานของคลังสินค้า
description: นโยบายงานคลังสินค้าควบคุมวิธีการสร้างงานคลังสินค้าโดยกระบวนการคลังสินค้าในการผลิต โดยยึดตามชนิดของใบสั่งงาน สถานที่เก็บสินค้าคงคลัง และผลิตภัณฑ์
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0710eac8daba7f51f6b5d1522476b812a130960d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567043"
---
# <a name="warehouse-work-policies"></a><span data-ttu-id="4ecb5-103">นโยบายงานของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ecb5-103">Warehouse work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ecb5-104">นโยบายงานคลังสินค้าใน Microsoft Dynamics 365 for Finance and Operations ควบคุมว่า มีการสร้างงานคลังสินค้าโดยกระบวนการคลังสินค้าในการผลิต ตามชนิดของใบสั่งงาน สถานที่สินค้าคงคลัง และผลิตภัณฑ์ หรือไม่</span><span class="sxs-lookup"><span data-stu-id="4ecb5-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="4ecb5-105">นโยบายงานนี้ควบคุมว่ามีการสร้างงานของคลังสินค้าสำหรับกระบวนการคลังสินค้าในการผลิตหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4ecb5-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="4ecb5-106">คุณสามารถตั้งค่านโยบายงานได้โดยใช้ชุดข้อมูลของ **ชนิดใบสั่งงาน** **สถานที่เก็บสินค้าคงคลัง**และ **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="4ecb5-107">ตัวอย่างเช่น ผลิตภัณฑ์ L0101 ถูกรายงานเมื่อเสร็จสมบูรณ์ไปยังที่ตั้งเอาท์พุท 001</span><span class="sxs-lookup"><span data-stu-id="4ecb5-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="4ecb5-108">สินค้าที่สำเร็จแล้วจะถูกใช้ในใบสั่งผลิตอื่นในที่ตั้งเอาท์พุท 001 ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="4ecb5-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="4ecb5-109">ในกรณีนี้ คุณสามารถตั้งค่านโยบายงานเพื่อป้องกันไม่ให้มีการสร้างการสำรองสินค้าที่สำเร็จแล้วเมื่อคุณรายงานผลิตภัณฑ์ L0101 เมื่อเสร็จสมบูรณ์ไปยังที่ตั้งเอาท์พุท 001</span><span class="sxs-lookup"><span data-stu-id="4ecb5-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="4ecb5-110">นโยบายงานคือเอนทิตี้แต่ละรายการที่สามารถอธิบายได้โดยใช้ข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ecb5-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="4ecb5-111">**ชื่อนโยบายงาน**(ตัวระบุเฉพาะของนโยบายงาน)</span><span class="sxs-lookup"><span data-stu-id="4ecb5-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="4ecb5-112">**ชนิดใบสั่งงาน**และ**วิธีการสร้างงาน**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="4ecb5-113">**สถานที่เก็บสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-113">**Inventory locations**</span></span>
-   <span data-ttu-id="4ecb5-114">**ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="4ecb5-115">ชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-115">Work order types</span></span>
<span data-ttu-id="4ecb5-116">คุณสามารถเลือกชนิดใบสั่งงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ecb5-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="4ecb5-117">การสำรองสินค้าที่สำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ecb5-117">Finished goods put away</span></span>
-   <span data-ttu-id="4ecb5-118">การสำรองผลิตภัณฑ์ร่วมและสินค้าพลอยได้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="4ecb5-119">การเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="4ecb5-119">Raw material picking</span></span>

<span data-ttu-id="4ecb5-120">ฟิลด์ **วิธีการสร้างงาน** มีค่า **ไม่เคย**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="4ecb5-121">ค่านี้บ่งชี้ว่านโยบายงานจะป้องกันไม่ให้มีการสร้างงานของคลังสินค้าสำหรับชนิดลำดับงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="4ecb5-122">สถานที่เก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ecb5-122">Inventory locations</span></span>
<span data-ttu-id="4ecb5-123">คุณสามารถเลือกที่ตั้งที่นโยบายงานใช้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="4ecb5-124">ถ้าไม่มีที่ตั้งที่เชื่อมโยงกับนโยบายงาน นโยบายงานจะไม่ใช้กับกระบวนการใดๆ</span><span class="sxs-lookup"><span data-stu-id="4ecb5-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="4ecb5-125">ในหน้า **ที่ตั้ง** คุณยังสามารถเลือกหรือยกเลิกการเลือกนโยบายงานสำหรับที่ตั้งเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="4ecb5-126">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4ecb5-126">Products</span></span>
<span data-ttu-id="4ecb5-127">คุณสามารถเลือกผลิตภัณฑ์ที่นโยบายงานใช้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="4ecb5-128">คุณสามารถใช้นโยบายงานกับผลิตภัณฑ์ทั้งหมดหรือผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="4ecb5-129">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="4ecb5-129">Example</span></span>
<span data-ttu-id="4ecb5-130">ในตัวอย่างต่อไปนี้ มีใบสั่งผลิตสองรายการ คือ PRD-001 และ PRD-00*2*</span><span class="sxs-lookup"><span data-stu-id="4ecb5-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="4ecb5-131">ใบสั่งผลิต PRD-001 มีการดำเนินการที่มีชื่อว่า **ส่วนประกอบ**โดยที่ผลิตภัณฑ์ SC1 ถูกรายงานเมื่อเสร็จสมบูรณ์ไปยังที่ตั้ง O1</span><span class="sxs-lookup"><span data-stu-id="4ecb5-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="4ecb5-132">ใบสั่งผลิต PRD-002 มีการดำเนินการที่มีชื่อว่า **การทาสี** และใช้ผลิตภัณฑ์ SC1 จากที่ตั้ง O1</span><span class="sxs-lookup"><span data-stu-id="4ecb5-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="4ecb5-133">นอกจากนี้ใบสั่งผลิต PRD-002 ก็ใช้วัตถุดิบ RM1 จากที่ตั้ง O1 เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="4ecb5-134">RM1 ถูกจัดเก็บในที่ตั้งคลังสินค้า BULK-001 และจะถูกเบิกสินค้าไปยังที่ตั้ง O1 โดยงานของคลังสินค้าสำหรับการเบิกสินค้าวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="4ecb5-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="4ecb5-135">มีการสร้างงานการเบิกสินค้าเมื่อการผลิต PRD-002 ถูกนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="4ecb5-136">[![นโยบายงานของคลังสินค้า](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="4ecb5-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="4ecb5-137">เมื่อคุณวางแผนที่จะตั้งค่าคอนฟิกนโยบายงานของคลังสินค้าสำหรับสถานการณ์จำลองนี้ คุณควรพิจารณาข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ecb5-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="4ecb5-138">งานของคลังสินค้าสำหรับการสำรองสินค้าที่สำเร็จแล้วไม่จำเป็นเมื่อคุณรายงานผลิตภัณฑ์ SC1 เมื่อเสร็จสมบูรณ์จากใบสั่งผลิต PRD-001 ไปยังที่ตั้ง O1</span><span class="sxs-lookup"><span data-stu-id="4ecb5-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="4ecb5-139">ทั้งนี้เนื่องจากการดำเนินงาน **การทาสี** สำหรับใบสั่งผลิต PRD-002 ใช้ SC1 ที่ที่ตั้งเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="4ecb5-140">งานของคลังสินค้าสำหรับการเบิกสินค้าวัตถุดิบจำเป็นในการย้ายวัตถุดิบ RM1 จากที่ตั้งคลังสินค้า BULK-001 ไปยังที่ตั้ง O1</span><span class="sxs-lookup"><span data-stu-id="4ecb5-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="4ecb5-141">นี่คือตัวอย่างของนโยบายงานที่คุณสามารถตั้งค่าได้ตามข้อควรพิจารณาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="4ecb5-142"><strong>ชื่อนโยบายงาน</strong></span><span class="sxs-lookup"><span data-stu-id="4ecb5-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="4ecb5-143"><strong>ชนิดใบสั่งงาน</strong></span><span class="sxs-lookup"><span data-stu-id="4ecb5-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="4ecb5-144">ไม่มีการสำรองสินค้า 01     \`</span><span class="sxs-lookup"><span data-stu-id="4ecb5-144">No put away 01     \`</span></span>          |     <span data-ttu-id="4ecb5-145">- การสำรองสินค้าที่สำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ecb5-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="4ecb5-146"><strong>สถานที่</strong></span><span class="sxs-lookup"><span data-stu-id="4ecb5-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="4ecb5-147">- O1</span><span class="sxs-lookup"><span data-stu-id="4ecb5-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="4ecb5-148"><strong>ผลิตภัณฑ์</strong></span><span class="sxs-lookup"><span data-stu-id="4ecb5-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="4ecb5-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="4ecb5-149">- SC1</span></span>                 |

<span data-ttu-id="4ecb5-150">กระบวนงานต่อไปนี้ให้คำแนะนำทีละขั้นตอนเกี่ยวกับวิธีการตั้งค่านโยบายงานของคลังสินค้าสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="4ecb5-151">นอกจากนี้ยังมีการอธิบายการตั้งค่าตัวอย่างที่แสดงวิธีการรายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์ไปยังที่ตั้งที่ไม่มีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="4ecb5-152">ตั้งค่านโยบายงานของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ecb5-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="4ecb5-153">กระบวนการคลังสินค้าไม่รวมงานคลังสินค้าเสมอไป</span><span class="sxs-lookup"><span data-stu-id="4ecb5-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="4ecb5-154">โดยการกำหนดนโยบายงาน คุณสามารถป้องกันการสร้างงานสำหรับการเบิกวัตถุดิบและการสำรองสินค้าสำเร็จรูป สำหรับชุดของผลิตภัณฑ์ที่ตำแหน่งเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="4ecb5-155">บริษัทข้อมูลสาธิต USMF ถูกนำมาใช้ในการสร้างกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="4ecb5-156">ขั้นตอน (21)</span><span class="sxs-lookup"><span data-stu-id="4ecb5-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="4ecb5-157">1</span><span class="sxs-lookup"><span data-stu-id="4ecb5-157">1.</span></span>  | <span data-ttu-id="4ecb5-158">ไปที่การจัดการคลังสินค้า &gt; การตั้งค่า &gt; งาน &gt; นโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="4ecb5-159">2</span><span class="sxs-lookup"><span data-stu-id="4ecb5-159">2.</span></span>  | <span data-ttu-id="4ecb5-160">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ecb5-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="4ecb5-161">3</span><span class="sxs-lookup"><span data-stu-id="4ecb5-161">3.</span></span>  | <span data-ttu-id="4ecb5-162">ในฟิลด์ชื่อนโยบายงาน ให้พิมพ์ 'ไม่มีงานการย้ายเก็บ'</span><span class="sxs-lookup"><span data-stu-id="4ecb5-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="4ecb5-163">4</span><span class="sxs-lookup"><span data-stu-id="4ecb5-163">4.</span></span>  | <span data-ttu-id="4ecb5-164">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="4ecb5-165">5.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-165">5.</span></span>  | <span data-ttu-id="4ecb5-166">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4ecb5-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4ecb5-167">6.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-167">6.</span></span>  | <span data-ttu-id="4ecb5-168">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4ecb5-169">7.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-169">7.</span></span>  | <span data-ttu-id="4ecb5-170">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การสำรองสินค้าที่สำเร็จแล้ว'</span><span class="sxs-lookup"><span data-stu-id="4ecb5-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="4ecb5-171">8.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-171">8.</span></span>  | <span data-ttu-id="4ecb5-172">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4ecb5-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4ecb5-173">9.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-173">9.</span></span>  | <span data-ttu-id="4ecb5-174">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4ecb5-175">10.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-175">10.</span></span> | <span data-ttu-id="4ecb5-176">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การสำรองผลิตภัณฑ์ร่วมและสินค้าพลอยได้'</span><span class="sxs-lookup"><span data-stu-id="4ecb5-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="4ecb5-177">11.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-177">11.</span></span> | <span data-ttu-id="4ecb5-178">ขยายส่วนสถานที่เก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4ecb5-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="4ecb5-179">12.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-179">12.</span></span> | <span data-ttu-id="4ecb5-180">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4ecb5-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4ecb5-181">13.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-181">13.</span></span> | <span data-ttu-id="4ecb5-182">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4ecb5-183">14.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-183">14.</span></span> | <span data-ttu-id="4ecb5-184">ในรายการคลังสินค้า ป้อน '51'</span><span class="sxs-lookup"><span data-stu-id="4ecb5-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="4ecb5-185">15.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-185">15.</span></span> | <span data-ttu-id="4ecb5-186">ในฟิลด์สถานที่ ให้ป้อนหรือเลือก '001'</span><span class="sxs-lookup"><span data-stu-id="4ecb5-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="4ecb5-187">16.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-187">16.</span></span> | <span data-ttu-id="4ecb5-188">ขยายส่วนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4ecb5-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="4ecb5-189">17.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-189">17.</span></span> | <span data-ttu-id="4ecb5-190">ในฟิลด์การเลือกผลิตภัณฑ์ ให้ป้อน 'เลือกแล้ว'</span><span class="sxs-lookup"><span data-stu-id="4ecb5-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="4ecb5-191">18.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-191">18.</span></span> | <span data-ttu-id="4ecb5-192">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4ecb5-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="4ecb5-193">19.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-193">19.</span></span> | <span data-ttu-id="4ecb5-194">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="4ecb5-195">20.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-195">20.</span></span> | <span data-ttu-id="4ecb5-196">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือก 'L0101'</span><span class="sxs-lookup"><span data-stu-id="4ecb5-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="4ecb5-197">21.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-197">21.</span></span> | <span data-ttu-id="4ecb5-198">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4ecb5-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="4ecb5-199">รายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์ไปยังที่ตั้งที่ไม่มีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="4ecb5-200">กระบวนงานนี้แสดงตัวอย่างการรายงานเป็น เสร็จแล้ว ไปยังสถานที่ที่เป็นป้ายทะเบียนที่มีการควบคุม</span><span class="sxs-lookup"><span data-stu-id="4ecb5-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="4ecb5-201">นโยบายงานที่ใช้งานได้เป็นข้อกำหนดเบื้องต้นสำหรับงานนี้</span><span class="sxs-lookup"><span data-stu-id="4ecb5-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="4ecb5-202">กระบวนงานก่อนหน้าแสดงการตั้งค่าของนโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="4ecb5-203">ขั้นตอน (25)</span><span class="sxs-lookup"><span data-stu-id="4ecb5-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="4ecb5-204"><strong>งานย่อย: ตั้งค่าที่ตั้งเอาท์พุท</strong></span><span class="sxs-lookup"><span data-stu-id="4ecb5-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="4ecb5-205">ไปที่จัดการองค์กร &gt; ทรัพยากร &gt; กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4ecb5-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="4ecb5-206">ในรายการ เลือกกลุ่มทรัพยากร &#39;5102&#39;</span><span class="sxs-lookup"><span data-stu-id="4ecb5-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="4ecb5-207">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="4ecb5-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="4ecb5-208">ในฟิลด์คลังสินค้าเอาท์พุท ป้อน &#39;51&#39;</span><span class="sxs-lookup"><span data-stu-id="4ecb5-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="4ecb5-209">ในฟิลด์สถานที่เอาท์พุท ป้อน &#39;001&#39;</span><span class="sxs-lookup"><span data-stu-id="4ecb5-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="4ecb5-210">สถานที่ 001 ไม่ใช่สถานที่ควบคุมแผ่นป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="4ecb5-211">คุณสามารถตั้งค่าสถานที่เอาท์พุทที่ควบคุมป้ายที่ไม่ใช่ป้ายทะเบียน เฉพาะเมื่อนโยบายงานมีอยู่สำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="4ecb5-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="4ecb5-212"><strong>งานย่อย: สร้างใบสั่งผลิตและรายงานเป็น เสร็จแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="4ecb5-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="4ecb5-213">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ecb5-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="4ecb5-214">ไปที่การควบคุมการผลิต &gt; ใบสั่งผลิต &gt; ใบสั่งผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4ecb5-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="4ecb5-215">คลิกใบสั่งผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="4ecb5-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="4ecb5-216">ในฟิลด์หมายเลขสินค้า ป้อน &#39;L0101&#39;</span><span class="sxs-lookup"><span data-stu-id="4ecb5-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="4ecb5-217">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ecb5-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="4ecb5-218">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="4ecb5-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="4ecb5-219">คลิกประเมิน </span><span class="sxs-lookup"><span data-stu-id="4ecb5-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="4ecb5-220">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="4ecb5-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="4ecb5-221">คลิกที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4ecb5-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="4ecb5-222">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4ecb5-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="4ecb5-223">ในฟิลด์การใช้ BOM อัตโนมัติ เลือก &#39;ไม่เคย&#39;</span><span class="sxs-lookup"><span data-stu-id="4ecb5-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="4ecb5-224">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ecb5-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="4ecb5-225">คลิก รายงาน เมื่อเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="4ecb5-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="4ecb5-226">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4ecb5-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="4ecb5-227">เลือก ใช่ ในฟิลด์ยอมรับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="4ecb5-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="4ecb5-228">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="4ecb5-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="4ecb5-229">ในบานหน้าต่างการดำเนินการ คลิกคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ecb5-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="4ecb5-230">คลิกรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="4ecb5-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="4ecb5-231">เมื่อใบสั่งผลิตถูกรายงานเป็น เสร็จแล้ว จึงไม่มีการสร้างงานสำหรับการสำรอง </span><span class="sxs-lookup"><span data-stu-id="4ecb5-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="4ecb5-232">นี่เกิดขึ้นเนื่องจากนโยบายงานถูกกำหนดให้ป้องกันงานจากการถูกสร้าง เมื่อผลิตภัณฑ์ L0101 ถูกรายงานเป็น เสร็จแล้ว ไปยังสถานที่ 001</span><span class="sxs-lookup"><span data-stu-id="4ecb5-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>



