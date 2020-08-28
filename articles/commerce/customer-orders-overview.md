---
title: ใบสั่งของลูกค้าใน Modern POS (MPOS)
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับใบสั่งของลูกค้าใน Modern POS (MPOS) ใบสั่งของลูกค้ามีชื่อเรียกอีกอย่างหนึ่งว่าใบสั่งพิเศษ หัวข้อนี้มีคำอธิบายเกี่ยวกับพารามิเตอร์ที่เกี่ยวข้องและขั้นตอนของธุรกรรม
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 87d1217204e0c5cb22f567793b043bf399ca5685
ms.sourcegitcommit: b07434f2bd6db67d8dd712f096329acc902751ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699380"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="811e3-105">ใบสั่งของลูกค้าใน Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="811e3-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="811e3-106">หัวข้อนี้แสดงข้อมูลเกี่ยวกับใบสั่งของลูกค้าใน Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="811e3-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="811e3-107">ใบสั่งของลูกค้ามีชื่อเรียกอีกอย่างหนึ่งว่าใบสั่งพิเศษ</span><span class="sxs-lookup"><span data-stu-id="811e3-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="811e3-108">หัวข้อนี้มีคำอธิบายเกี่ยวกับพารามิเตอร์ที่เกี่ยวข้องและขั้นตอนของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="811e3-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="811e3-109">ในโลกการค้าแบบช่องทาง Omni ผู้ค้าปลีกหลายรายมีตัวเลือกในใบสั่งซื้อของลูกค้าหรือคำสั่งพิเศษเพื่อตอบสนองความต้องการของผลิตภัณฑ์และข้อกำหนดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="811e3-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="811e3-110">ต่อไปนี้เป็นสถานการณ์ทั่วไปบางส่วน:</span><span class="sxs-lookup"><span data-stu-id="811e3-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="811e3-111">ลูกค้าต้องการให้จัดส่งผลิตภัณฑ์ไปยังที่อยู่ที่ระบุในวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="811e3-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="811e3-112">ลูกค้าต้องการรับผลิตภัณฑ์จากร้านค้าหรือสถานที่ที่ไม่ใช่ร้านค้าหรือสถานที่ที่ลูกค้าสั่งซื้อผลิตภัณฑ์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="811e3-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="811e3-113">ลูกค้าต้องการให้ใครสักคนไปรับผลิตภัณฑ์ที่ลูกค้าซื้อ</span><span class="sxs-lookup"><span data-stu-id="811e3-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="811e3-114">นอกจากนี้ผู้ค้าปลีกยังใช้ใบสั่งของลูกค้าในการลดการขายที่สูญเสียที่อาจเกิดขึ้นเนื่องจากความขัดข้องของสินค้าคงคลังได้ เนื่องจากสามารถจัดส่งสินค้าหรือเบิกสินค้าได้ในเวลาหรือสถานที่ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="811e3-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="811e3-115">ตั้งค่าใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-115">Set up customer orders</span></span>

<span data-ttu-id="811e3-116">นี่คือพารามิเตอร์ส่วนหนึ่งที่สามารถตั้งค่าในหน้า **พารามิเตอร์การค้า** เพื่อกำหนดวิธีดำเนินการตามใบสั่งซื้อของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="811e3-117">**เปอร์เซ็นต์เงินฝากเริ่มต้น** – ระบุยอดเงินที่ลูกค้าต้องชำระเป็นเงินฝากก่อนที่จะได้รับการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="811e3-118">ยอดเงินฝากเริ่มต้นจะถูกคำนวณเป็นเปอร์เซ็นต์ของมูลค่าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="811e3-119">การเชื่อมโยงของร้านค้าอาจสามารถแทนยอดเงินได้โดยใช้ **การแทนที่การฝากเงิน** โดยขึ้นอยู่กับสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="811e3-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="811e3-120">**เปอร์เซ็นต์ของค่าธรรมเนียมการยกเลิก** – ถ้าจะใช้ค่าธรรมเนียมเมื่อมีการยกเลิกใบสั่งของลูกค้า ให้ระบุยอดเงินของค่าธรรมเนียมนั้น</span><span class="sxs-lookup"><span data-stu-id="811e3-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="811e3-121">**รหัสค่าธรรมเนียมการยกเลิก** – ถ้าจะใช้ค่าธรรมเนียมเมื่อมีการยกเลิกใบสั่งของลูกค้า ค่าธรรมเนียมนั้นจะปรากฏภายใต้รหัสค่าธรรมเนียมในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="811e3-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="811e3-122">ใช้พารามิเตอร์นี้เมื่อต้องการกำหนดรหัสค่าธรรมเนียมการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="811e3-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="811e3-123">**รหัสค่าธรรมเนียมการจัดส่ง** – ผู้ค้าปลีกสามารถเรียกเก็บค่าธรรมเนียมเพิ่มเติมสำหรับการจัดส่งสินค้าให้แก่ลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="811e3-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="811e3-124">ยอดเงินของค่าธรรมเนียมการจัดส่งนั้นจะปรากฏภายใต้รหัสค่าธรรมเนียมในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="811e3-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="811e3-125">ใช้พารามิเตอร์นี้เมื่อต้องการแม็ปรหัสค่าธรรมเนียมการจัดส่งไปยังค่าธรรมเนียมการจัดส่งในใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="811e3-126">**ขอคืนเงินค่าธรรมเนียมการจัดส่ง** – ระบุว่าค่าธรรมเนียมการจัดส่งที่เกี่ยวข้องกับใบสั่งของลูกค้าสามารถเรียกคืนได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="811e3-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="811e3-127">**ยอดเงินสูงสุดที่ไม่มีการอนุมัติ** – ถ้าค่าธรรมเนียมการจัดส่งสามารถเรียกคืนได้ ให้ระบุยอดเงินสูงสุดของการขอคืนเงินค่าธรรมเนียมการจัดส่งระหว่างใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="811e3-128">ถ้าเกินยอดเงินนี้ จำเป็นต้องมีการแทนที่ของผู้จัดการเพื่อดำเนินการคืนเงินต่อ</span><span class="sxs-lookup"><span data-stu-id="811e3-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="811e3-129">เพื่อให้เหมาะสมกับสถานการณ์จำลองต่อไปนี้ การขอคืนเงินของค่าธรรมเนียมการจัดส่งสามารถเกินยอดเงินที่จ่ายดั้งเดิมได้:</span><span class="sxs-lookup"><span data-stu-id="811e3-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="811e3-130">จะมีการคิดค่าธรรมเนียมที่ระดับส่วนหัวของใบสั่งขาย และเมื่อมีการส่งคืนรายการผลิตภัณฑ์บางจำนวน การคืนเงินค่าจัดส่งสูงสุดสำหรับผลิตภัณฑ์และจำนวนที่ได้รับการอนุมัติ ไม่สามารถกำหนดแนวทางที่เหมาะกับลูกค้าทั้งหมดได้ </span><span class="sxs-lookup"><span data-stu-id="811e3-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="811e3-131">ค่าธรรมเนียมการจัดส่งสินค้าจะเกิดขึ้นสำหรับทุก ๆ อินสแตนซ์ของการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="811e3-132">ถ้าลูกค้าส่งคืนผลิตภัณฑ์หลายครั้ง และนโยบายของผู้ขายปลีกระบุว่า ผู้ขายปลีกจะเป็นผู้ชำระต้นทุนของค่าธรรมเนียมการจัดส่งคืนสินค้า ค่าธรรมเนียมการจัดส่งคืนสินค้าจะมากกว่าค่าธรรมเนียมการจัดส่งจริง</span><span class="sxs-lookup"><span data-stu-id="811e3-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    
- <span data-ttu-id="811e3-133">**ลักษณะการทำงานการคำนวณภาษี** - **คำนวณใหม่** เป็นการตั้งค่าเริ่มต้นและแบบดั้งเดิมสำหรับวิธีการคำนวณภาษีใหม่ เมื่อมีการนำเข้าใบสั่งไปยังส่วนสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="811e3-133">**Tax calculation behavior** - **Recalculate** is the default and traditional setting for how taxes are recalculated when the order is imported into the back office.</span></span> <span data-ttu-id="811e3-134">**ไม่ต้องคำนวณใหม่** จะปิดใช้งานการคำนวณภาษีใหม่จนกว่าหรือยกเว้นจะมีการแก้ไขใบสั่งในส่วนสนับสนุน เมื่อมีการทริกเกอร์การคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="811e3-134">**Don't recalculate** disables tax recalculation until or unless the order is edited in the back office, when recalculation is triggered.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="811e3-135">ขั้นตอนธุรกรรมสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-135">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="811e3-136">สร้างใบสั่งซื้อลูกค้าใน Modern POS</span><span class="sxs-lookup"><span data-stu-id="811e3-136">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="811e3-137">เพิ่มลูกค้าให้กับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="811e3-137">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="811e3-138">เพิ่มผลิตภัณฑ์ลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="811e3-138">Add products to the cart.</span></span>
3. <span data-ttu-id="811e3-139">คลิก **สร้างใบสั่งของลูกค้า** และจากนั้นเลือกชนิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-139">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="811e3-140">ชนิดใบสั่งอาจเป็น **ใบสั่งของลูกค้า** หรือ **ใบเสนอราคา** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-140">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="811e3-141">คลิก **จัดส่งที่เลือก** หรือ **จัดส่งทั้งหมด** เพื่อจัดส่งผลิตภัณฑ์ไปยังที่อยู่ในบัญชีลูกค้า ระบุวันที่จัดส่งที่ร้องขอ และระบุค่าธรรมเนียมการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-141">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="811e3-142">คลิก **เบิกสินค้าที่เลือก** หรือ **เบิกสินค้าทั้งหมด** เพื่อเลือกผลิตภัณฑ์ที่จะเบิกสินค้าจากร้านค้าปัจจุบันหรือร้านค้าอื่นในวันที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="811e3-142">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="811e3-143">รวบรวมยอดเงินฝาก ถ้าจำเป็นต้องใช้เงินฝาก</span><span class="sxs-lookup"><span data-stu-id="811e3-143">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="811e3-144">แก้ไขใบสั่งของลูกค้าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="811e3-144">Edit an existing customer order</span></span>

1. <span data-ttu-id="811e3-145">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="811e3-145">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="811e3-146">ค้นหา และเลือกใบสั่งที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="811e3-146">Find and select the order to edit.</span></span> <span data-ttu-id="811e3-147">ที่ด้านล่างของหน้า คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="811e3-147">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="811e3-148">เบิกสินค้าใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-148">Pick up an order</span></span>

1. <span data-ttu-id="811e3-149">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="811e3-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="811e3-150">เลือกใบสั่งที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-150">Select the order to pick up.</span></span> <span data-ttu-id="811e3-151">ที่ด้านล่างของหน้า คลิก **การเบิกสินค้าและการบรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="811e3-151">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="811e3-152">คลิก **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="811e3-152">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="811e3-153">ยกเลิกใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="811e3-153">Cancel an order</span></span>

1. <span data-ttu-id="811e3-154">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="811e3-154">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="811e3-155">เลือกใบสั่งที่จะยกเลิก</span><span class="sxs-lookup"><span data-stu-id="811e3-155">Select the order to cancel.</span></span> <span data-ttu-id="811e3-156">ที่ด้านล่างของหน้า คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="811e3-156">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="811e3-157">การสร้างใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-157">Create a return order</span></span>

1. <span data-ttu-id="811e3-158">บนโฮมเพจ คลิก **ค้นหาใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="811e3-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="811e3-159">เลือกใบสั่งที่จะส่งคืนสินค้า เลือกใบแจ้งหนี้สำหรับใบสั่ง จากนั้นบรรทัดผลิตภัณฑ์สำหรับสินค้าที่จะส่งคืน</span><span class="sxs-lookup"><span data-stu-id="811e3-159">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="811e3-160">ที่ด้านล่างของหน้า คลิก **ใบสั่งส่งคืนสินค้า**</span><span class="sxs-lookup"><span data-stu-id="811e3-160">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="811e3-161">ขั้นตอนธุรกรรมแบบอะซิงโครนัสสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="811e3-161">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="811e3-162">สามารถสร้างใบสั่งของลูกค้าจากไคลเอ็นต์การขายหน้าร้าน (POS) ในโหมดซิงโครนัสหรือโหมดอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="811e3-162">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="811e3-163">เปิดใช้งานใบสั่งขออของลูกค้าเพื่อให้สร้างขึ้นในโหมดอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="811e3-163">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="811e3-164">คลิก **การขายปลีกและการค้า** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **โปรไฟล์ POS** &gt; **โปรไฟล์ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="811e3-164">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="811e3-165">บนแท็บด่วน **ทั่วไป** ตั้งค่าตัวเลือก **สร้างใบสั่งของลูกค้าในโหมดอะซิงโครนัส** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="811e3-165">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="811e3-166">เมื่อตัวเลือก **สร้างใบสั่งของลูกค้าในโหมดอะซิงโครนัส** ถูกตั้งเป็น **ใช่** ใบสั่งของลูกค้าจะถูกสร้างในโหมดอะซิงโครนัสเสมอ ถึงแม้ว่า Retail Transaction Service (RTS) จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="811e3-166">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="811e3-167">ถ้าคุณตั้งค่าตัวเลือกนี้เป็น **ไม่ใช่**ใบสั่งของลูกค้ามักถูกสร้างในโหมดซิงโครนัสโดยใช้ RTS</span><span class="sxs-lookup"><span data-stu-id="811e3-167">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="811e3-168">เมื่อใบสั่งซื้อลูกค้าถูกสร้างขึ้นในโหมดอะซิงโครนัส พวกเขาจะถูกดึงและแทรกลงใน Commerce โดยงานแบบ Pull (P)</span><span class="sxs-lookup"><span data-stu-id="811e3-168">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="811e3-169">ใบสั่งขายที่สอดคล้องกันจะถูกสร้างขึ้นเมื่อ **ซิงโครไนซ์ใบสั่งซื้อ** ถูกเรียกใช้ด้วยตนเองหรือผ่านกระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="811e3-169">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="811e3-170">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="811e3-170">Additional resources</span></span>

[<span data-ttu-id="811e3-171">ใบสั่งของลูกค้าแบบไฮบริด</span><span class="sxs-lookup"><span data-stu-id="811e3-171">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
