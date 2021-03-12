---
title: รายการต้นทุน
description: บทความนี้แสดงข้อมูลเกี่ยวกับรายการต้นทุนและเวลาที่สร้าง รายการต้นทุนเป็นเรกคอร์ดที่ลงทะเบียนปริมาณและต้นทุนของกิจกรรมที่กำหนด
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12ff771cf44595420ca721605daabaa6b071a4ff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967838"
---
# <a name="cost-entries"></a><span data-ttu-id="f2d0f-104">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f2d0f-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2d0f-105">บทความนี้แสดงข้อมูลเกี่ยวกับรายการต้นทุนและเวลาที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="f2d0f-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="f2d0f-106">รายการต้นทุนเป็นเรกคอร์ดที่ลงทะเบียนปริมาณและต้นทุนของกิจกรรมที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="f2d0f-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="f2d0f-107">รายการต้นทุนคือการรวมธุรกรรมสินค้าคงคลังที่ถูกบันทึกไว้ในมิติสินค้าคงคลังทางการเงินที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="f2d0f-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="f2d0f-108">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="f2d0f-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="f2d0f-109">ตัวอย่างที่ 1: ไม่มีรายการที่ต้นทุนที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f2d0f-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="f2d0f-110">เหตุการณ์สมุดรายวันการโอนย้ายถูกลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f2d0f-110">A transfer journal event is registered.</span></span> <span data-ttu-id="f2d0f-111">เหตุการณ์การโอนย้ายสินค้า A หนึ่งชิ้นจากสถานที่เก็บ A ไป B. มิติสถานที่เก็บสินค้าคงคลังไม่ได้เป็นส่วนหนึ่งของต้นทุนวัตถุ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="f2d0f-112">ดังนั้น เหตุการณ์สร้างธุรกรรมสินค้าคงคลังสองรายการและไม่มีรายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f2d0f-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="f2d0f-113">ตัวอย่างที่ 2: รายการต้นทุนถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f2d0f-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="f2d0f-114">เหตุการณ์สมุดรายวันการโอนย้ายถูกลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f2d0f-114">A transfer journal event is registered.</span></span> <span data-ttu-id="f2d0f-115">เหตุการณ์การโอนย้ายสินค้า A หนึ่งชิ้นจากไซต์ 1 ไป 2</span><span class="sxs-lookup"><span data-stu-id="f2d0f-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="f2d0f-116">มิติสินค้าคงคลังของไซต์เป็นส่วนหนึ่งของต้นทุนวัตถุ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="f2d0f-117">ดังนั้น เหตุการณ์สร้างธุรกรรมสินค้าคงคลังสองรายการและรายการต้นทุนสองรายการ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="f2d0f-118">ตัวอย่างที่ 3: รายการต้นทุนหนึ่งรายการถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f2d0f-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="f2d0f-119">เหตุการณ์การรับผลิตภัณฑ์มีการลงทะเบียนสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="f2d0f-120">เหตุการณ์การลงทะเบียนการเบิกสินค้า A 100 ชิ้นที่ต้นทุนหน่วย 10.00 ดอลลาร์สหรัฐฯ (USD)</span><span class="sxs-lookup"><span data-stu-id="f2d0f-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="f2d0f-121">เนื่องจากการใช้สินค้า A สร้างจากลำดับหมายเลขประจำเฉพาะเพื่อติดตามวัตถุประสงค์ของการบริหารสินค้าคงคลัง หมายเลขประจำเฉพาะจะถูกสร้างขึ้นสำหรับแต่ละสินค้าที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="f2d0f-122">ดังนั้น เหตุการณ์สร้างธุรกรรมสินค้าคงคลัง 100 รายการและมีรายการต้นทุนหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="f2d0f-123">หน้ารายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f2d0f-123">Cost entries page</span></span>
<span data-ttu-id="f2d0f-124">หน้าใหม่ของ **ต้นทุนรายการ** ช่วยให้คุณสามารถดูและควบคุมการลงทะเบียนของปริมาณและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f2d0f-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="f2d0f-125">หน้านี้จะหมายถึง **ธุรกรรมของสินค้าคงคลัง** และ **การชำระเงินของสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="f2d0f-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="f2d0f-126">เรกคอร์ดที่มีการลงทะเบียนสำหรับเหตุการณ์ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="f2d0f-127">ดังนั้น คุณสามารถค้นหาข้อมูลได้อย่างรวดเร็วและควบคุมต้นทุนสะสมของเหตุการณ์เฉพาะหรือเหตุการณ์ทั้งหมดที่เกี่ยวข้องกับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="f2d0f-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="f2d0f-128">ดังตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f2d0f-128">Here is an example:</span></span>

-   <span data-ttu-id="f2d0f-129">เหตุการณ์ใบรับสินค้า A. ถูกลงทะเบียนสำหรับผลิตภัณฑ์ A. หนึ่งร้อยชิ้นถูกรับที่ต้นทุนต่อหน่วย 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="f2d0f-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="f2d0f-130">สองสามวันหลังจากมีการลงทะเบียนใบแจ้งหนี้เหตุการณ์ ต้นทุนที่เพิ่มขึ้นเป็น USD 11.00</span><span class="sxs-lookup"><span data-stu-id="f2d0f-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="f2d0f-131">ดังนั้นยอดเงินรวมคือ 1,100 USD</span><span class="sxs-lookup"><span data-stu-id="f2d0f-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="f2d0f-132">มีสร้างใบสำคัญที่สองไปยังบัญชีสำหรับผลต่างของ 100 USD</span><span class="sxs-lookup"><span data-stu-id="f2d0f-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="f2d0f-133">สองสามวันต่อมา ค่าธรรมเนียมเบ็ดเตล็ด USD 15.00 จะครอบคลุมต้นทุนการขนส่งในการลงทะเบียนในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="f2d0f-134">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-134">Voucher</span></span> | <span data-ttu-id="f2d0f-135">วันที่</span><span class="sxs-lookup"><span data-stu-id="f2d0f-135">Date</span></span>       | <span data-ttu-id="f2d0f-136">ข้อมูลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="f2d0f-136">Reference</span></span>      | <span data-ttu-id="f2d0f-137">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="f2d0f-137">Number</span></span> | <span data-ttu-id="f2d0f-138">รหัสล็อต</span><span class="sxs-lookup"><span data-stu-id="f2d0f-138">Lot ID</span></span>  | <span data-ttu-id="f2d0f-139">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-139">Quantity</span></span> | <span data-ttu-id="f2d0f-140">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f2d0f-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="f2d0f-141">00001</span><span class="sxs-lookup"><span data-stu-id="f2d0f-141">00001</span></span>   | <span data-ttu-id="f2d0f-142">1 มกราคม 2015</span><span class="sxs-lookup"><span data-stu-id="f2d0f-142">01-01-2015</span></span> | <span data-ttu-id="f2d0f-143">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-143">Purchase order</span></span> | <span data-ttu-id="f2d0f-144">100001</span><span class="sxs-lookup"><span data-stu-id="f2d0f-144">100001</span></span> | <span data-ttu-id="f2d0f-145">0000101</span><span class="sxs-lookup"><span data-stu-id="f2d0f-145">0000101</span></span> | <span data-ttu-id="f2d0f-146">100.00</span><span class="sxs-lookup"><span data-stu-id="f2d0f-146">100.00</span></span>   | <span data-ttu-id="f2d0f-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="f2d0f-147">1000.00</span></span> |
| <span data-ttu-id="f2d0f-148">00002</span><span class="sxs-lookup"><span data-stu-id="f2d0f-148">00002</span></span>   | <span data-ttu-id="f2d0f-149">20 มกราคม 2015</span><span class="sxs-lookup"><span data-stu-id="f2d0f-149">20-01-2015</span></span> | <span data-ttu-id="f2d0f-150">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f2d0f-150">Purchase order</span></span> | <span data-ttu-id="f2d0f-151">100001</span><span class="sxs-lookup"><span data-stu-id="f2d0f-151">100001</span></span> | <span data-ttu-id="f2d0f-152">0000101</span><span class="sxs-lookup"><span data-stu-id="f2d0f-152">0000101</span></span> |          | <span data-ttu-id="f2d0f-153">100.00</span><span class="sxs-lookup"><span data-stu-id="f2d0f-153">100.00</span></span>  |
| <span data-ttu-id="f2d0f-154">00003</span><span class="sxs-lookup"><span data-stu-id="f2d0f-154">00003</span></span>   | <span data-ttu-id="f2d0f-155">31 มกราคม 2015</span><span class="sxs-lookup"><span data-stu-id="f2d0f-155">31-01-2015</span></span> | <span data-ttu-id="f2d0f-156">การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="f2d0f-156">Adjustment</span></span>     | <span data-ttu-id="f2d0f-157">100001</span><span class="sxs-lookup"><span data-stu-id="f2d0f-157">100001</span></span> | <span data-ttu-id="f2d0f-158">0000101</span><span class="sxs-lookup"><span data-stu-id="f2d0f-158">0000101</span></span> |          | <span data-ttu-id="f2d0f-159">15.00 น.</span><span class="sxs-lookup"><span data-stu-id="f2d0f-159">15.00</span></span>   |

<span data-ttu-id="f2d0f-160">หน้า **ต้นทุนรายการ** สามารถเปิดใช้งานการกรองข้อมูลตามรหัสเอกสารและวันเอกสาร</span><span class="sxs-lookup"><span data-stu-id="f2d0f-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="f2d0f-161">รายการต้นทุนจะพร้อมใช้งานเฉพาะสำหรับ [ออบเจ็กต์ต้นทุน](cost-object.md) หรือผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="f2d0f-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f2d0f-162">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f2d0f-162">Additional resources</span></span>
--------

[<span data-ttu-id="f2d0f-163">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f2d0f-163">Cost objects</span></span>](cost-object.md)



