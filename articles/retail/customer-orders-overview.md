---
title: "ใบสั่งของลูกค้าใน Retail Modern POS (MPOS)"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับใบสั่งของลูกค้าใน Modern POS ของการขายปลีก (MPOS) ใบสั่งของลูกค้ามีชื่อเรียกอีกอย่างหนึ่งว่าใบสั่งพิเศษ หัวข้อนี้มีคำอธิบายเกี่ยวกับพารามิเตอร์ที่เกี่ยวข้องและขั้นตอนของธุรกรรม"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b54f39cc7896871d77f9371e6197bf6dbaac51de
ms.contentlocale: th-th
ms.lasthandoff: 01/04/2019

---

# <a name="customer-orders-in-retail-modern-pos-mpos"></a><span data-ttu-id="0dd5e-105">ใบสั่งของลูกค้าใน Retail Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="0dd5e-105">Customer orders in Retail Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0dd5e-106">หัวข้อนี้แสดงข้อมูลเกี่ยวกับใบสั่งของลูกค้าใน Modern POS ของการขายปลีก (MPOS)</span><span class="sxs-lookup"><span data-stu-id="0dd5e-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="0dd5e-107">ใบสั่งของลูกค้ามีชื่อเรียกอีกอย่างหนึ่งว่าใบสั่งพิเศษ</span><span class="sxs-lookup"><span data-stu-id="0dd5e-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="0dd5e-108">หัวข้อนี้มีคำอธิบายเกี่ยวกับพารามิเตอร์ที่เกี่ยวข้องและขั้นตอนของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0dd5e-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="0dd5e-109">ในโลกการขายปลีกช่องทาง Omni ผู้ค้าปลีกหลายรายมีตัวเลือกสำหรับใบสั่งของลูกค้า หรือใบสั่งพิเศษ เพื่อให้ตรงกับผลิตภัณฑ์ที่หลากหลายและความต้องการในการเติมเต็ม</span><span class="sxs-lookup"><span data-stu-id="0dd5e-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="0dd5e-110">ต่อไปนี้เป็นสถานการณ์ทั่วไปบางส่วน:</span><span class="sxs-lookup"><span data-stu-id="0dd5e-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="0dd5e-111">ลูกค้าต้องการให้จัดส่งผลิตภัณฑ์ไปยังที่อยู่ที่ระบุในวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0dd5e-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="0dd5e-112">ลูกค้าต้องการรับผลิตภัณฑ์จากร้านค้าหรือสถานที่ที่ไม่ใช่ร้านค้าหรือสถานที่ที่ลูกค้าสั่งซื้อผลิตภัณฑ์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="0dd5e-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="0dd5e-113">ลูกค้าต้องการให้ใครสักคนไปรับผลิตภัณฑ์ที่ลูกค้าซื้อ</span><span class="sxs-lookup"><span data-stu-id="0dd5e-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="0dd5e-114">นอกจากนี้ผู้ค้าปลีกยังใช้ใบสั่งของลูกค้าในการลดการขายที่สูญเสียที่อาจเกิดขึ้นเนื่องจากความขัดข้องของสินค้าคงคลังได้ เนื่องจากสามารถจัดส่งสินค้าหรือเบิกสินค้าได้ในเวลาหรือสถานที่ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="0dd5e-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="0dd5e-115">ตั้งค่าใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0dd5e-115">Set up customer orders</span></span>

<span data-ttu-id="0dd5e-116">นี่เป็นบางส่วนของพารามิเตอร์ที่สามารถตั้งค่าได้ในหน้า **พารามิเตอร์การขายปลีก** เพื่อกำหนดวิธีการปฏิบัติตามใบสั่งของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="0dd5e-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="0dd5e-117">**เปอร์เซ็นต์เงินฝากเริ่มต้น** – ระบุยอดเงินที่ลูกค้าต้องชำระเป็นเงินฝากก่อนที่จะได้รับการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="0dd5e-118">ยอดเงินฝากเริ่มต้นจะถูกคำนวณเป็นเปอร์เซ็นต์ของมูลค่าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="0dd5e-119">การเชื่อมโยงของร้านค้าอาจสามารถแทนยอดเงินได้โดยใช้ **การแทนที่การฝากเงิน** โดยขึ้นอยู่กับสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="0dd5e-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="0dd5e-120">**เปอร์เซ็นต์ของค่าธรรมเนียมการยกเลิก** – ถ้าจะใช้ค่าธรรมเนียมเมื่อมีการยกเลิกใบสั่งของลูกค้า ให้ระบุยอดเงินของค่าธรรมเนียมนั้น</span><span class="sxs-lookup"><span data-stu-id="0dd5e-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="0dd5e-121">**รหัสค่าธรรมเนียมการยกเลิก** – ถ้าจะใช้ค่าธรรมเนียมเมื่อมีการยกเลิกใบสั่งของลูกค้า ค่าธรรมเนียมนั้นจะปรากฏภายใต้รหัสค่าธรรมเนียมในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0dd5e-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="0dd5e-122">ใช้พารามิเตอร์นี้เมื่อต้องการกำหนดรหัสค่าธรรมเนียมการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="0dd5e-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="0dd5e-123">**รหัสค่าธรรมเนียมการจัดส่ง** – ผู้ค้าปลีกสามารถเรียกเก็บค่าธรรมเนียมเพิ่มเติมสำหรับการจัดส่งสินค้าให้แก่ลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="0dd5e-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="0dd5e-124">ยอดเงินของค่าธรรมเนียมการจัดส่งนั้นจะปรากฏภายใต้รหัสค่าธรรมเนียมในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0dd5e-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="0dd5e-125">ใช้พารามิเตอร์นี้เมื่อต้องการแม็ปรหัสค่าธรรมเนียมการจัดส่งไปยังค่าธรรมเนียมการจัดส่งในใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0dd5e-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="0dd5e-126">**ขอคืนเงินค่าธรรมเนียมการจัดส่ง** – ระบุว่าค่าธรรมเนียมการจัดส่งที่เกี่ยวข้องกับใบสั่งของลูกค้าสามารถเรียกคืนได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0dd5e-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="0dd5e-127">**ยอดเงินสูงสุดที่ไม่มีการอนุมัติ** – ถ้าค่าธรรมเนียมการจัดส่งสามารถเรียกคืนได้ ให้ระบุยอดเงินสูงสุดของการขอคืนเงินค่าธรรมเนียมการจัดส่งระหว่างใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="0dd5e-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="0dd5e-128">ถ้าเกินยอดเงินนี้ จำเป็นต้องมีการแทนที่ของผู้จัดการเพื่อดำเนินการคืนเงินต่อ</span><span class="sxs-lookup"><span data-stu-id="0dd5e-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="0dd5e-129">เพื่อให้เหมาะสมกับสถานการณ์จำลองต่อไปนี้ การขอคืนเงินของค่าธรรมเนียมการจัดส่งสามารถเกินยอดเงินที่จ่ายดั้งเดิมได้:</span><span class="sxs-lookup"><span data-stu-id="0dd5e-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="0dd5e-130">ค่าธรรมเนียมจะถูกนำไปใช้ในระดับของส่วนหัวใบสั่งขาย และเมื่อปริมาณบางส่วนของบรรทัดผลิตภัณฑ์ถูกส่งคืน จะไม่สามารถกำหนดการขอคืนเงินสูงสุดของค่าธรรมเนียมการจัดส่งสินค้าที่ได้รับอนุญาตสำหรับผลิตภัณฑ์และปริมาณในลักษณะที่เหมาะสมสำหรับลูกค้าขายปลีกทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="0dd5e-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    - <span data-ttu-id="0dd5e-131">ค่าธรรมเนียมการจัดส่งสินค้าจะเกิดขึ้นสำหรับทุก ๆ อินสแตนซ์ของการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="0dd5e-132">ถ้าลูกค้าส่งคืนผลิตภัณฑ์หลายครั้ง และนโยบายของผู้ขายปลีกระบุว่า ผู้ขายปลีกจะเป็นผู้ชำระต้นทุนของค่าธรรมเนียมการจัดส่งคืนสินค้า ค่าธรรมเนียมการจัดส่งคืนสินค้าจะมากกว่าค่าธรรมเนียมการจัดส่งจริง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="0dd5e-133">ขั้นตอนธุรกรรมสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0dd5e-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="0dd5e-134">สร้างใบสั่งของลูกค้าใน Modern POS ของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="0dd5e-134">Create a customer order in Retail Modern POS</span></span>

1. <span data-ttu-id="0dd5e-135">เพิ่มลูกค้าให้กับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0dd5e-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="0dd5e-136">เพิ่มผลิตภัณฑ์ลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="0dd5e-136">Add products to the cart.</span></span>
3. <span data-ttu-id="0dd5e-137">คลิก **สร้างใบสั่งของลูกค้า** และจากนั้นเลือกชนิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="0dd5e-138">ชนิดใบสั่งอาจเป็น **ใบสั่งของลูกค้า** หรือ **ใบเสนอราคา** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="0dd5e-139">คลิก **จัดส่งที่เลือก** หรือ **จัดส่งทั้งหมด** เพื่อจัดส่งผลิตภัณฑ์ไปยังที่อยู่ในบัญชีลูกค้า ระบุวันที่จัดส่งที่ร้องขอ และระบุค่าธรรมเนียมการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="0dd5e-140">คลิก **เบิกสินค้าที่เลือก** หรือ **เบิกสินค้าทั้งหมด** เพื่อเลือกผลิตภัณฑ์ที่จะเบิกสินค้าจากร้านค้าปัจจุบันหรือร้านค้าอื่นในวันที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0dd5e-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="0dd5e-141">รวบรวมยอดเงินฝาก ถ้าจำเป็นต้องใช้เงินฝาก</span><span class="sxs-lookup"><span data-stu-id="0dd5e-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="0dd5e-142">แก้ไขใบสั่งของลูกค้าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0dd5e-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="0dd5e-143">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="0dd5e-144">ค้นหา และเลือกใบสั่งที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="0dd5e-144">Find and select the order to edit.</span></span> <span data-ttu-id="0dd5e-145">ที่ด้านล่างของหน้า คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="0dd5e-146">เบิกสินค้าใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-146">Pick up an order</span></span>

1. <span data-ttu-id="0dd5e-147">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="0dd5e-148">เลือกใบสั่งที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="0dd5e-148">Select the order to pick up.</span></span> <span data-ttu-id="0dd5e-149">ที่ด้านล่างของหน้า คลิก **การเบิกสินค้าและการบรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="0dd5e-150">คลิก **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="0dd5e-151">ยกเลิกใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="0dd5e-151">Cancel an order</span></span>

1. <span data-ttu-id="0dd5e-152">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="0dd5e-153">เลือกใบสั่งที่จะยกเลิก</span><span class="sxs-lookup"><span data-stu-id="0dd5e-153">Select the order to cancel.</span></span> <span data-ttu-id="0dd5e-154">ที่ด้านล่างของหน้า คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="0dd5e-155">การสร้างใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="0dd5e-155">Create a return order</span></span>

1. <span data-ttu-id="0dd5e-156">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="0dd5e-157">เลือกใบสั่งที่จะส่งคืนสินค้า เลือกใบแจ้งหนี้สำหรับใบสั่ง จากนั้นบรรทัดผลิตภัณฑ์สำหรับสินค้าที่จะส่งคืน</span><span class="sxs-lookup"><span data-stu-id="0dd5e-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="0dd5e-158">ที่ด้านล่างของหน้า คลิก **ใบสั่งส่งคืนสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="0dd5e-159">ขั้นตอนธุรกรรมแบบอะซิงโครนัสสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0dd5e-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="0dd5e-160">สามารถสร้างใบสั่งของลูกค้าจากไคลเอ็นต์การขายหน้าร้าน (POS) ในโหมดซิงโครนัสหรือโหมดอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="0dd5e-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="0dd5e-161">เปิดใช้งานใบสั่งขออของลูกค้าเพื่อให้สร้างขึ้นในโหมดอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="0dd5e-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="0dd5e-162">คลิก **การขายปลีก** &gt; **การตั้งค่าช่องสัทาง** &gt; **การตั้งค่า POS** &gt; **โปรไฟล์ POS** &gt; **โพรไฟล์ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="0dd5e-163">บนแท็บด่วน **ทั่วไป** ตั้งค่าตัวเลือก **สร้างใบสั่งของลูกค้าในโหมดอะซิงโครนัส** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0dd5e-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="0dd5e-164">เมื่อตัวเลือก **สร้างใบสั่งของลูกค้าในโหมดอะซิงโครนัส** ถูกตั้งค่าเป็น **ใช่** ใบสั่งของลูกค้ามักถูกสร้างในโหมดอะซิงโครนัส แม้ว่า Retail Transaction Service (RTS) จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0dd5e-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="0dd5e-165">ถ้าคุณตั้งค่าตัวเลือกนี้เป็น **ไม่ใช่**ใบสั่งของลูกค้ามักถูกสร้างในโหมดซิงโครนัสโดยใช้ RTS</span><span class="sxs-lookup"><span data-stu-id="0dd5e-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="0dd5e-166">เมื่อใบสั่งของลูกค้าถูกสร้างขึ้นในโหมดอะซิงโครนัส จะถูกดึงและแทรกลงใน Retail โดยงาน Pull (P)</span><span class="sxs-lookup"><span data-stu-id="0dd5e-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="0dd5e-167">มีการสร้างใบสั่งขายที่สอดคล้องกันใน Retail เมื่อมีการเรียกใช้ **ซิงโครไนส์ใบสั่ง** ด้วยตนเองหรือโดยใช้กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0dd5e-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0dd5e-168">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0dd5e-168">Additional resources</span></span>

[<span data-ttu-id="0dd5e-169">ใบสั่งของลูกค้าแบบไฮบริด</span><span class="sxs-lookup"><span data-stu-id="0dd5e-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)

