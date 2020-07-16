---
title: ภาพรวมของรถเข็นและหน้าเช็คเอาท์
description: หัวข้อนี้แสดงภาพรวมของหน้ารถเข็นและการเช็คเอาท์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c879b90cf49dcab9cf069e4f3613602bd6673aa9
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527583"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="e9fbf-103">ภาพรวมของรถเข็นและหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="e9fbf-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9fbf-104">หัวข้อนี้แสดงภาพรวมของหน้ารถเข็นและการเช็คเอาท์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e9fbf-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e9fbf-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e9fbf-105">Overview</span></span>

<span data-ttu-id="e9fbf-106">หน้ารถเข็นของเว็บไซต์อีคอมเมิร์ซแสดงสินค้าทั้งหมดที่ลูกค้าเพิ่มไว้ในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="e9fbf-107">หน้ารถเข็นสร้างขึ้นโดยใช้โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="e9fbf-108">โมดูลรถเข็นเป็นคอนเทนเนอร์ที่เป็นโฮสต์สำหรับโมดูลทั้งหมดที่จำเป็นต้องใช้ในการแสดงรายการในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="e9fbf-109">โมดูลรถเข็นยังสามารถใช้โมดูลอื่นๆ เพื่อแสดงสรุปใบสั่งและรหัสโปรโมชันใดๆ ที่ใช้กับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9fbf-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="e9fbf-110">หน้าเช็คเอาท์ของเว็บไซต์อีคอมเมิร์ซแสดงถึงขั้นตอนทีละขั้นตอนที่ลูกค้าปฏิบัติตามเพื่อป้อนข้อมูลทั้งหมดที่จำเป็นต้องใช้ในการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="e9fbf-111">โมดูลการเช็คเอาท์อาจรวมถึงโมดูลที่จัดการที่อยู่การจัดส่ง วิธีการจัดส่ง ข้อมูลการเรียกเก็บเงิน สรุปใบสั่ง และข้อมูลอื่นๆ ที่เกี่ยวข้องกับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9fbf-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="e9fbf-112">หน้ารถเข็น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-112">Cart page</span></span>

<span data-ttu-id="e9fbf-113">หน้ารถเข็นทำหน้าที่เป็นถุงช้อปปิ้งและรวมสินค้าทั้งหมดที่มีการเพิ่มลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="e9fbf-114">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้ารถเข็นที่สร้างขึ้นโดยใช้ชุดเริ่มต้นออนไลน์ และชุดรูปแบบ "Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="e9fbf-114">The following illustration show an example of a cart page that was built by using the online starter kit and the "Fabrikam" theme.</span></span>

![ตัวอย่างของหน้ารถเข็น](./media/cart2.PNG)

<span data-ttu-id="e9fbf-116">เนื้อหาหลักของหน้ารถเข็นแสดงสินค้าทั้งหมดที่ลูกค้าเพิ่มไว้ในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="e9fbf-117">ส่วนลดที่ใช้ได้ทั้งหมดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="e9fbf-118">ส่วนลดเหล่านี้รวมส่วนลดที่ซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-118">These discounts include complex discounts.</span></span> <span data-ttu-id="e9fbf-119">ตัวอย่างเช่น "ซื้อ 3 รายการ รับส่วนลด 10%" หรือ "ซื้อขวดและกระเป๋าเป้สะพายเพื่อรับส่วนลด 10%</span><span class="sxs-lookup"><span data-stu-id="e9fbf-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="e9fbf-120">โมดูลสรุปใบสั่งแสดงยอดเงินที่ครบกำหนดหลังจากส่วนลด การจัดส่ง ภาษี และอื่นๆ ถูกใช้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="e9fbf-121">นอกจากนี้ยังมีรหัสโปรโมชันที่ช่วยให้ลูกค้าสามารถใช้หรือลบรหัสโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="e9fbf-122">ลูกค้าสามารถซื้อสินค้าโดยไม่ระบุชื่อหรือเป็นผู้ใช้ที่ลงชื่อเข้าใช้ก็ได้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="e9fbf-123">ถ้าลูกค้าล็อกอิน สินค้าในรถเข็นจะถูกรักษาไว้ระหว่างรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="e9fbf-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="e9fbf-124">ด้วยวิธีนี้ ลูกค้าสามารถซื้อสินค้าจากอุปกรณ์ต่างๆ ได้ต่อไป</span><span class="sxs-lookup"><span data-stu-id="e9fbf-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="e9fbf-125">จากรถเข็น ลูกค้าสามารถดำเนินการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="e9fbf-126">ลูกค้าสามารถเริ่มต้นการชำระเงินในฐานะผู้ใช้ที่เป็นแขกหรือเป็นผู้ใช้ที่ลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="e9fbf-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างหน้ารถเข็น ให้ดูที่ [เพิ่มโมดูลรถเข็นไปยังหน้า](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="e9fbf-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="e9fbf-128">หน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="e9fbf-128">Checkout page</span></span>

<span data-ttu-id="e9fbf-129">หน้าเช็คเอาท์เป็นที่ที่ลูกค้าป้อนข้อมูลที่จำเป็นสำหรับการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="e9fbf-130">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้าเช็คเอาท์ที่สร้างขึ้นโดยใช้ชุดเริ่มต้นออนไลน์</span><span class="sxs-lookup"><span data-stu-id="e9fbf-130">The following illustration show an example of a checkout page that was built by using the online starter kit.</span></span>

![ตัวอย่างของหน้าเช็คเอาท์](./media/Checkout.PNG)

<span data-ttu-id="e9fbf-132">เนื้อหาหลักของหน้าเช็คเอาท์คือจุดที่มีการรวบรวมข้อมูลใบสั่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e9fbf-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="e9fbf-133">ข้อมูลนี้รวมถึงที่อยู่ในการจัดส่ง ตัวเลือกการจัดส่ง และข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="e9fbf-134">การเช็คเอาท์มีขั้นตอนทีละขั้นตอน เนื่องจากต้องมีการป้อนข้อมูลในใบสั่งเฉพาะที่จะประมวลผล</span><span class="sxs-lookup"><span data-stu-id="e9fbf-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="e9fbf-135">ตัวอย่างเช่น ต้องป้อนที่อยู่จัดส่งก่อนที่จะสามารถคำนวณต้นทุนการจัดส่งและการชำระเงินได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="e9fbf-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="e9fbf-136">ที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="e9fbf-136">Shipping address</span></span>

<span data-ttu-id="e9fbf-137">ต้องระบุที่อยู่จัดส่งถ้าต้องจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="e9fbf-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="e9fbf-138">คุณสามารถตั้งค่าคอนฟิกรูปแบบของที่อยู่การจัดส่งสำหรับแต่ละสถานที่ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e9fbf-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e9fbf-139">ตัวอย่างเช่น ถ้าสินค้าจะถูกจัดส่งไปยังประเทศสหรัฐอเมริกา ที่อยู่การจัดส่งต้องมีที่อยู่ ถนน รัฐและรหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="e9fbf-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="e9fbf-140">การตรวจสอบความถูกต้องของการป้อนข้อมูลพื้นฐานบางอย่างจะทำสำหรับฟิลด์ที่อยู่ที่จัดส่ง เช่น การตรวจสอบความถูกต้องของอักขระตัวอักษร ตัวเลขสูงสุด และหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e9fbf-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="e9fbf-141">ถึงแม้ว่าจะไม่มีการตรวจสอบความถูกต้องของที่อยู่ของตัวเอง การตรวจสอบนี้สามารถทำได้โดยใช้บริการของบุคคลที่สามที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="e9fbf-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="e9fbf-142">ที่อยู่การจัดส่งจะใช้กับสินค้าทั้งหมดในรถเข็นที่มีการเลือกตัวเลือก "จัดส่ง"</span><span class="sxs-lookup"><span data-stu-id="e9fbf-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="e9fbf-143">ถ้าคุณใช้ขั้นตอนการชำระเงินที่ระบุไว้ในชุดเริ่มต้นออนไลน์ สินค้าในรถเข็นแต่ละรายการจะไม่สามารถจัดส่งไปยังที่อยู่อื่นได้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-143">If you use the checkout flow that is provided in the online starter kit, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="e9fbf-144">ถ้าคุณต้องการความสามารถนี้ สามารถดำเนินการได้โดยการเลือกกำหนดโมดูลการเชคเอาท์</span><span class="sxs-lookup"><span data-stu-id="e9fbf-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="e9fbf-145">หลังจากที่มีการระบุที่อยู่จัดส่ง จะมีการแสดงวิธีการจัดส่งที่พร้อมใช้งานจากร้านค้าออนไลน์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e9fbf-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="e9fbf-146">วิธีการจัดส่งและที่อยู่ที่สนับสนุนสามารถตั้งค่าคอนฟิกในการค้า</span><span class="sxs-lookup"><span data-stu-id="e9fbf-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="e9fbf-147">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-147">Payment</span></span>

<span data-ttu-id="e9fbf-148">ขั้นตอนต่อไปในการเชคเอาท์คือการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="e9fbf-149">ในอีคอมเมิร์ซ สามารถใช้วิธีการชำระเงินหลายวิธีเพื่อสั่งซื้อ เช่น บัตรเครดิต บัตรของขวัญ และคะแนนสะสมสำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e9fbf-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="e9fbf-150">นอกจากนี้ยังสามารถใช้วิธีการชำระเงินเหล่านี้ร่วมกันได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="e9fbf-151">อาจจำเป็นต้องใช้ข้อมูลเพิ่มเติม ขึ้นอยู่กับวิธีการชำระเงินที่ใช้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="e9fbf-152">ตัวอย่างเช่น การชำระเงินด้วยบัตรเครดิตต้องมีที่อยู่ในการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="e9fbf-153">การชำระเงินด้วยบัตรเครดิตจะถูกประมวลผลโดยใช้การเชื่อมต่อการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="e9fbf-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="e9fbf-154">คะแนนสะสมสำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e9fbf-154">Loyalty points</span></span>

<span data-ttu-id="e9fbf-155">ในระหว่างขั้นตอนการเช็คเอาท์ ลูกค้าที่เป็นสมาชิกของโปรแกรมตอบแทนลูกค้าสมาชิกและผู้ที่มีคะแนนสะสมสำหรับสมาชิกที่ค้างรับสามารถแลกคะแนนสะสมสำหรับการสั่งซื้อได้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="e9fbf-156">โมดูลคะแนนสะสมสำหรับสมาชิกจะแสดงขึ้นเฉพาะเมื่อลูกค้าเป็นสมาชิกอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e9fbf-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="e9fbf-157">สำหรับผู้ใช้ที่ไม่ใช่สมาชิกและผู้ใช้ที่เป็นแขก โมดูลนี้จะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="e9fbf-158">บัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-158">Gift cards</span></span>

<span data-ttu-id="e9fbf-159">ชุดเริ่มต้นออนไลน์ของเราอนุญาตให้มีการแลกบัตรของขวัญภายในสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-159">The online starter kit lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="e9fbf-160">เมื่อต้องการใช้บัตรของขวัญภายใน ลูกค้าต้องเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="e9fbf-161">สำหรับการรักษาความปลอดภัยเพิ่มเติม เราขอแนะนำให้คุณเลือกกำหนดลำดับโดยใช้หมายเลขรหัสประจำตัว (PIN) สำหรับบัตรของขวัญภายใน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="e9fbf-162">ผู้ใช้ที่ลงชื่อเข้าใช้แล้วและผู้ใช้ที่เป็นแขก</span><span class="sxs-lookup"><span data-stu-id="e9fbf-162">Signed-in and guest users</span></span>

<span data-ttu-id="e9fbf-163">ลูกค้าสามารถดำเนินการชำระเงินให้เสร็จในฐานะผู้ใช้ที่เป็นแขกหรือเป็นผู้ใช้ที่ลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="e9fbf-164">ถ้าลูกค้าลงชื่อเข้าใช้ ข้อมูลบัญชี เช่น ที่อยู่การจัดส่งที่บันทึกไว้และรายละเอียดบัตรเครดิตที่บันทึกไว้จะถูกดึงข้อมูลมาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="e9fbf-165">สรุปใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="e9fbf-165">Order summary</span></span>

<span data-ttu-id="e9fbf-166">การเชคเอาท์จะแสดงสรุปรายการสินค้าในรถเข็นเพื่อให้ลูกค้าสามารถตรวจสอบความถูกต้องของใบสั่งก่อนที่เขาหรือเธอจะสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="e9fbf-167">ไม่สามารถแก้ไขสินค้าในรายการในระหว่างขั้นตอนการเช็คเอาท์ได้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="e9fbf-168">อย่างไรก็ตาม การเชื่อมโยงไปยังรถเข็นให้ไว้ในกรณีที่ผู้ใช้ต้องการกลับไปแก้ไขสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="e9fbf-169">หลังจากที่ลูกค้าให้ข้อมูลการจัดส่งและที่อยู่การเรียกเก็บเงิน สรุปใบสั่งจะสะท้อนยอดเงินที่ครบกำหนดหลังจากคะแนนสะสมสำหรับสมาชิกบัตรของขวัญและการชำระเงินอื่นๆ ถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="e9fbf-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="e9fbf-170">การยืนยันการสั่งซื้อและอีเมล</span><span class="sxs-lookup"><span data-stu-id="e9fbf-170">Order confirmation and email</span></span>

<span data-ttu-id="e9fbf-171">เมื่อลูกค้าวางใบสั่งจะมีการระบุหมายเลขการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="e9fbf-172">ถึงตอนนี้ การชำระเงินได้รับการอนุมัติแล้วแต่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="e9fbf-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="e9fbf-173">การชำระเงินจะมีการเรียกเก็บเฉพาะเมื่อมีการสั่งซื้อเรียบร้อยเท่านั้น (นั่นคือเมื่อมีการจัดส่งหรือได้รับสินค้าแล้ว)</span><span class="sxs-lookup"><span data-stu-id="e9fbf-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="e9fbf-174">หลังจากสร้างใบสั่งแล้ว จะมีการส่งอีเมล์ยืนยันใบสั่งไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9fbf-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="e9fbf-175">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างหน้าเช็คเอาท์ ให้ดูที่ [เพิ่มโมดูลเช็คเอาท์ไปยังหน้า](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="e9fbf-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9fbf-176">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e9fbf-176">Additional resources</span></span>

[<span data-ttu-id="e9fbf-177">ภาพรวมโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="e9fbf-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="e9fbf-178">ภาพรวมของหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e9fbf-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="e9fbf-179">ภาพรวมของหน้าการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e9fbf-179">Account management pages overview</span></span>](quick-tour-account-management.md)
