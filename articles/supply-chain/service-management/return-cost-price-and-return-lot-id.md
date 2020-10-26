---
title: ราคาทุนของสินค้ารับคืนและรหัสล็อตการส่งคืน
description: คุณอาจต้องการต้นทุนของผลิตภัณฑ์ที่ส่งคืนให้เท่ากับต้นทุนของผลิตภัณฑ์ ในเวลาเมื่อคุณขายผลิตภัณฑ์ให้กับลูกค้า คุณสามารถทำได้โดยใช้ **รหัสล็อตการส่งคืน**
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d5ac48dd390e2f57a7312e3c54af53dd49fd4f7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975595"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="4f08c-104">ราคาทุนของสินค้ารับคืนและรหัสล็อตการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4f08c-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="4f08c-105">ต้นทุนของผลิตภัณฑ์ที่ถูกส่งคืนไปยังสินค้าคงคลังจะถูกคำนวณ โดยใช้ต้นทุนปัจจุบันของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4f08c-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="4f08c-106">อย่างไรก็ตาม คุณอาจต้องการต้นทุนของผลิตภัณฑ์ที่ส่งคืนให้เท่ากับต้นทุนของผลิตภัณฑ์ ที่เวลาเมื่อคุณขายผลิตภัณฑ์ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="4f08c-107">คุณสามารถทำได้โดยใช้ฟิลด์ **รหัสล็อตการส่งคืน** บน FastTab **รายละเอียดรายการ** ในแบบฟอร์ม **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="4f08c-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="4f08c-108">ตัวอย่างเช่น พิจารณาสถานการณ์จำลองต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f08c-108">For example, consider the following scenario.</span></span> <span data-ttu-id="4f08c-109">คุณออกใบแจ้งหนี้ให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-109">You invoice a customer.</span></span> <span data-ttu-id="4f08c-110">จากนั้น ลูกค้าส่งคืนผลิตภัณฑ์จัดส่งถึงคุณ</span><span class="sxs-lookup"><span data-stu-id="4f08c-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="4f08c-111">คุณส่งคืนผลิตภัณฑ์ไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4f08c-111">You return the products to stock.</span></span> <span data-ttu-id="4f08c-112">ในกรณีนี้ เมื่อคุณบันทึกเครดิตลูกค้าสำหรับผลิตภัณฑ์ที่ส่งคืน ต้นทุนของผลิตภัณฑ์ดังกล่าวจะถูกคำนวณ โดยใช้ต้นทุนปัจจุบันของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4f08c-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="4f08c-113">อย่างไรก็ตาม ถ้าคุณใช้ฟิลด์ **รหัสล็อตการส่งคืน** ต้นทุนของผลิตภัณฑ์ที่ส่งคืนจะถูกคำนวณโดยใช้ต้นทุนในใบแจ้งหนี้ของการขายต้นฉบับให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="4f08c-114">เมื่อต้องการใช้ต้นทุนอื่นนอกเหนือจากต้นทุนปัจจุบันสำหรับการส่งคืนสินค้าจากลูกค้า ใช้หนึ่งในวิธีต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f08c-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="4f08c-115">วิธีที่ 1: ป้อนราคาต้นทุนการส่งคืนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="4f08c-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="4f08c-116">โดยค่าเริ่มต้น เมื่อคุณเพิ่มสินค้าไปยังใบสั่งส่งคืน มีการส่งคืนสินค้าไปยังสินค้าคงคลังที่ราคาต้นทุนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4f08c-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="4f08c-117">เมื่อต้องการระบุราคาต้นทุนการส่งคืนต่างๆ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4f08c-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="4f08c-118">คลิก **การขายและการตลาด** \> **ทั่วไป** \> **ใบสั่งส่งคืนสินค้า** \> **ใบสั่งส่งคืนสินค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4f08c-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="4f08c-119">บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **สร้าง** คลิก **ใบสั่งส่งคืนสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4f08c-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="4f08c-120">ในฟอร์ม **สร้างใบสั่งส่งคืนสินค้า** เลือกบัญชีลูกค้า และจากนั้น คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f08c-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="4f08c-121">ในฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2** เลือกสินค้า และจากนั้น ป้อนปริมาณค่าลบในฟิลด์ **ปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="4f08c-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="4f08c-122">คลิก FastTab **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="4f08c-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="4f08c-123">บนแท็บ **ทั่วไป** ป้อนค่าในฟิลด์ **ราคาทุนของสินค้ารับคืน**</span><span class="sxs-lookup"><span data-stu-id="4f08c-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="4f08c-124">ค่านี้จะใช้เมื่อมีการส่งคืนสินค้าไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4f08c-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="4f08c-125">ถ้าคุณไม่ได้ป้อนค่า ราคาต้นทุนปัจจุบันจะถูกใช้เมื่อมีการส่งคืนสินค้าไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4f08c-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="4f08c-126">วิธีที่ 2: สร้างราคาต้นทุนที่ขึ้นอยู่กับรายการใบแจ้งหนี้ของลูกค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4f08c-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="4f08c-127">นี่เป็นวิธีการที่ต้องการที่จะใช้ในการสร้างรายการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="4f08c-128">ในการใช้ต้นทุนผลิตภัณฑ์ในเวลาที่คุณขายผลิตภัณฑ์ให้กับลูกค้า สร้างใบสั่งส่งคืนสินค้า และระบุรายการขายเพื่อส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="4f08c-129">คลิก **การขายและการตลาด** \> **ทั่วไป** \> **ใบสั่งส่งคืนสินค้า** \> **ใบสั่งส่งคืนสินค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4f08c-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="4f08c-130">บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **สร้าง** คลิก **ใบสั่งส่งคืนสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4f08c-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="4f08c-131">ในฟอร์ม **สร้างใบสั่งส่งคืนสินค้า** เลือกบัญชีลูกค้า และจากนั้น คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f08c-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="4f08c-132">ในฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2** ใน **บานหน้าต่างการดำเนินการ** คลิก **ค้นหาใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="4f08c-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="4f08c-133">ในฟอร์ม **ค้นหาใบสั่งขาย** เลือกรายการใบแจ้งหนี้ที่จะส่งคืน แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f08c-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="4f08c-134">บน FastTab **รายละเอียดรายการ** บนแท็บ **ทั่วไป** ฟิลด์ **รหัสล็อตการส่งคืน** แสดงค่าจากรายการขายเดิม</span><span class="sxs-lookup"><span data-stu-id="4f08c-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="4f08c-135">นอกจากนี้ ฟิลด์ **ราคาต้นทุนการส่งคืน** จะแสดงมูลค่าต้นทุนจากรายการขายดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="4f08c-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="4f08c-136">ตัวอย่างการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4f08c-136">Cost calculation example</span></span>

<span data-ttu-id="4f08c-137">เมื่อคุณใช้ฟิลด์ **รหัสล็อตการส่งคืน** บนรายการใบสั่งส่งคืนสินค้าเพื่อระบุราคาต้นทุนในการส่งคืนสินค้า ต้นทุนในรายการใบสั่งส่งคืนสินค้าจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="4f08c-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="4f08c-138">ถ้าคุณเรียกใช้ฟังก์ชันปิดหรือคำนวณซ้ำในสินค้าคงคลัง ต้นทุนจะมีการปรับปรุงในรายการขายเดิม</span><span class="sxs-lookup"><span data-stu-id="4f08c-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="4f08c-139">ต้นทุนในรายการใบสั่งส่งคืนสินค้ามีการปรับปรุงโดยอัตโนมัติ เพื่อสะท้อนถึงต้นทุนเดียวกันสำหรับแต่ละชิ้น</span><span class="sxs-lookup"><span data-stu-id="4f08c-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="4f08c-140">สร้าง และนำออกใช้ผลิตภัณฑ์ที่มีการตั้งชื่อว่า การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="4f08c-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="4f08c-141">ในฟอร์ม **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** ระบุข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f08c-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="4f08c-142">ใน FastTab **จัดการต้นทุน** ในฟิลด์ **กลุ่มสินค้า** เลือกกลุ่ม **ส่วน**</span><span class="sxs-lookup"><span data-stu-id="4f08c-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="4f08c-143">บน FastTab **ทั่วไป** ในฟิลด์ **กลุ่มแบบจำลองสินค้า** เลือก **DEF**</span><span class="sxs-lookup"><span data-stu-id="4f08c-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="4f08c-144">บน FastTab **ซื้อ** ในฟิลด์ **ราคา** พิมพ์ 10.00 เป็นราคาต้นทุนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="4f08c-145">ใน **บานหน้าต่างการดำเนินการ** คลิก **กลุ่มมิติ**</span><span class="sxs-lookup"><span data-stu-id="4f08c-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="4f08c-146">ในฟิลด์ **กลุ่มมิติการจัดเก็บ** เลือก **ไซต์และคลังสินค้าเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="4f08c-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="4f08c-147">ในฟิลด์ **กลุ่มมิติการติดตาม** เลือก **ไม่มีมิติการติดตามที่เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="4f08c-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="4f08c-148">สร้างใบสั่งซื้อสำหรับสินค้าทดสอบจำนวน 10 ชิ้นที่ 6.00 ต่อชิ้น และจากนั้น ลงรายการบัญชีใบแจ้งหนี้สำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4f08c-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="4f08c-149">สร้างใบสั่งซื้อที่สองจำนวน 10 ชิ้นของสินค้าทดสอบที่ 8.00 ต่อชิ้น และจากนั้น ลงรายการบัญชีใบแจ้งหนี้สำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4f08c-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="4f08c-150">ลงรายการบัญชีใบแจ้งหนี้สำหรับใบสั่งขาย เพื่อขายสินค้าทดสอบห้าชิ้น</span><span class="sxs-lookup"><span data-stu-id="4f08c-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="4f08c-151">ในกรณีนี้ จะมีการคิดต้นทุนรายการใบสั่งขายที่ 35.00 (5 ชิ้น \* 7.00 ต้นทุนเฉลี่ยต่อชิ้น)</span><span class="sxs-lookup"><span data-stu-id="4f08c-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="4f08c-152">สร้างใบสั่งส่งคืนสินค้าสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-152">Create a return order for the customer.</span></span> <span data-ttu-id="4f08c-153">ในฟอร์ม **ค้นหาใบสั่งขาย** เลือกรายการใบแจ้งหนี้ แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f08c-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="4f08c-154">ในฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2** ตรวจสอบว่าใบสั่งส่งคืนถูกสร้างเพื่อส่งคืนสินค้าทดสอบ</span><span class="sxs-lookup"><span data-stu-id="4f08c-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="4f08c-155">มีการตั้งค่าปริมาณในใบสั่งส่งคืนสินค้าเป็น -5.00</span><span class="sxs-lookup"><span data-stu-id="4f08c-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="4f08c-156">ฟิลด์ **รหัสล็อตการส่งคืน** แสดงรหัสล็อต</span><span class="sxs-lookup"><span data-stu-id="4f08c-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="4f08c-157">รหัสล็อตนี้จะนำมาจากใบสั่งขายต้นฉบับของสินค้าที่ถูกขายให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="4f08c-158">ฟิลด์ **ราคาต้นทุนการส่งคืน** จะแสดงราคาต้นทุนจากรายการขายดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="4f08c-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="4f08c-159">ลงทะเบียนการรับของสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4f08c-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="4f08c-160">ลงรายการบัญชีบันทึกการจัดส่งสำหรับสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4f08c-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="4f08c-161">ลงรายการบัญชีใบแจ้งหนี้สำหรับใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="4f08c-161">Post an invoice for the return order.</span></span> <span data-ttu-id="4f08c-162">ในหน้ารายการ **ใบสั่งขายทั้งหมด** เลือกใบสั่งขายสำหรับ **ใบสั่งส่งคืน** ที่เป็นชนิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4f08c-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="4f08c-163">เปิดแบบฟอร์ม **ธุรกรรมสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="4f08c-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="4f08c-164">ตรวจสอบว่า การส่งคืนคิดต้นทุนที่ 7.00 ต่อชิ้น โดยใช้ค่าในฟิลด์ **ราคาต้นทุนการส่งคืน** สำหรับยอดรวมเป็น 35.00 ในฟิลด์ **ยอดต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="4f08c-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="4f08c-165">คุณสามารถเปิดฟอร์ม **ธุรกรรมสินค้าคงคลัง** จากฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2**</span><span class="sxs-lookup"><span data-stu-id="4f08c-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="4f08c-166">ในกริด **รายการ** คลิก **สินค้าคงคลัง** \> **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="4f08c-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="4f08c-167">ในการบริหารสินค้าคงคลังและคลังสินค้า ใช้แบบฟอร์ม **การปิดและการปรับปรุง** เพื่อเรียกใช้กระบวนงาน **3. ปิด**</span><span class="sxs-lookup"><span data-stu-id="4f08c-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="4f08c-168">การดำเนินการนี้ปรับเปลี่ยนต้นทุนในรายการขายต้นฉบับที่มีการคิดต้นทุนที่ -35.00 (5 ชิ้น \* 7.00) เป็น -30.00 (5 ชิ้น \* 6.00)</span><span class="sxs-lookup"><span data-stu-id="4f08c-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="4f08c-169">ทั้งนี้เนื่องจากกลุ่มแบบจำลองสินค้าคงคลังใช้เข้าก่อนออกก่อน (FIFO) และ 6.00 ต่อชิ้น เป็นต้นทุน FIFO จากใบสั่งซื้อแรก</span><span class="sxs-lookup"><span data-stu-id="4f08c-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="4f08c-170">นอกจากนี้ การดำเนินการจะปรับปรุงต้นทุนบนรายการขายส่งคืน เพื่อจับคู่ต้นทุนต่อชิ้นในรายการขายเดิม</span><span class="sxs-lookup"><span data-stu-id="4f08c-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="4f08c-171">ดังนั้น ต้นทุนของรายการส่งคืนจะถูกปรับจาก 35.00 เป็น 30.00</span><span class="sxs-lookup"><span data-stu-id="4f08c-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




