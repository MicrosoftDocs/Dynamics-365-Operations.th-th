---
title: โมดูลเช็คเอาท์
description: หัวข้อนี้จะอธิบายถึงวิธีการเพิ่มโมดูลการชำระเงินให้กับหน้าและตั้งค่าคุณสมบัติที่จำเป็น
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1d913fdc9ab9a3dbf7d5534fba38add7f942652a
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686753"
---
# <a name="checkout-module"></a><span data-ttu-id="4a96c-103">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-103">Checkout module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4a96c-104">หัวข้อนี้จะอธิบายถึงวิธีการเพิ่มโมดูลการชำระเงินให้กับหน้าและตั้งค่าคุณสมบัติที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="4a96c-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="4a96c-105">Overview</span></span>

<span data-ttu-id="4a96c-106">โมดูลการชำระเงินเป็นคอนเทนเนอร์พิเศษที่เป็นโฮสต์สำหรับโมดูลทั้งหมดที่จำเป็นในการสร้างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-106">A checkout module is a special container that hosts all modules that are required to create an order.</span></span> <span data-ttu-id="4a96c-107">โดยจะแสดงขั้นตอนแต่ละขั้นตอนของลูกค้าที่ใช้ในการป้อนข้อมูลที่เกี่ยวข้องทั้งหมดเพื่อทำการซื้อ</span><span class="sxs-lookup"><span data-stu-id="4a96c-107">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span> <span data-ttu-id="4a96c-108">โดยจะรวบรวมข้อมูลที่อยู่ที่จัดส่ง วิธีการจัดส่ง และข้อมูลการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="4a96c-108">It captures the shipping address, shipping method, and billing information.</span></span> <span data-ttu-id="4a96c-109">นอกจากนี้ยังมีสรุปใบสั่งและข้อมูลอื่น ๆ ที่เกี่ยวข้องกับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4a96c-109">It also provides an order summary and other information that is related to a customer order.</span></span>

<span data-ttu-id="4a96c-110">โมดูลการชำระเงินแสดงข้อมูลตามรหัสรถเข็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-110">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="4a96c-111">รหัสรถเข็นนี้ถูกบันทึกเป็นคุกกี้ของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="4a96c-111">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="4a96c-112">ต้องระบุรหัสรถเข็นเพื่อแสดงข้อมูลในโมดูลการเช็คเอาท์เช่นสินค้าในใบสั่งยอดเงินรวมและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="4a96c-112">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span> 

<span data-ttu-id="4a96c-113">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลเช็คเอาท์ Fabrikam บนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-113">The following image shows an example of a Fabrikam checkout module on a checkout page.</span></span>

![ตัวอย่างของโมดูลเช็คเอาท์](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a><span data-ttu-id="4a96c-115">คุณสมบัติของโมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-115">Checkout module properties</span></span>

<span data-ttu-id="4a96c-116">โมดูลการชำระเงินแสดงสรุปใบสั่ง และแสดงให้เห็นถึงฟังก์ชันสำหรับการวางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-116">A checkout module shows an order summary and provides the functionality for placing an order.</span></span> <span data-ttu-id="4a96c-117">เมื่อต้องการรวบรวมข้อมูลลูกค้าทั้งหมดที่จำเป็นต้องใช้ก่อนที่จะสามารถวางใบสั่งได้ ต้องเพิ่มโมดูลเพิ่มเติมที่โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4a96c-117">To gather all the customer information that is required before an order can be placed, additional modules must be added to the checkout module.</span></span> <span data-ttu-id="4a96c-118">ดังนั้น ร้านค้าปลีกมีความยืดหยุ่นในการเพิ่มโมดูลที่กำหนดเองไปยังขั้นตอนการเช็คเอาท์ หรือเพื่อแยกโมดูลตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="4a96c-118">Therefore, retailers have the flexibility to add custom modules to the checkout flow, or to exclude modules, based on their requirements.</span></span>

| <span data-ttu-id="4a96c-119">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="4a96c-119">Property name</span></span> | <span data-ttu-id="4a96c-120">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="4a96c-120">Values</span></span> | <span data-ttu-id="4a96c-121">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4a96c-121">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4a96c-122">หัวเรื่องการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4a96c-122">Checkout heading</span></span> | <span data-ttu-id="4a96c-123">ข้อความหัวเรื่องและแท็กหัวเรื่อง (**H1**, **H2**, **H3**, **H4**, **H5** หรือ **H6**)</span><span class="sxs-lookup"><span data-stu-id="4a96c-123">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4a96c-124">หัวเรื่องสำหรับโมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-124">A heading for the checkout module.</span></span> |
| <span data-ttu-id="4a96c-125">หัวเรื่องสรุปใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-125">Order summary heading</span></span> | <span data-ttu-id="4a96c-126">ข้อความหัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="4a96c-126">Heading text</span></span> | <span data-ttu-id="4a96c-127">หัวเรื่องสำหรับส่วนสรุปข้อมูลใบสั่งของโมดูล</span><span class="sxs-lookup"><span data-stu-id="4a96c-127">A heading for the order summary section of the module.</span></span> |
| <span data-ttu-id="4a96c-128">หัวเรื่องสินค้าในรายการของรถเข็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-128">Cart line items heading</span></span> | <span data-ttu-id="4a96c-129">ข้อความหัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="4a96c-129">Heading text</span></span> | <span data-ttu-id="4a96c-130">หัวเรื่องสำหรับสินค้าในรายการของรถเข็นที่แสดงอยู่ในโมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-130">A heading for cart line items that are shown in the checkout module.</span></span> |
| <span data-ttu-id="4a96c-131">แสดงค่าธรรมเนียมการจัดส่งของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="4a96c-131">Show shipping charges on line item</span></span> | <span data-ttu-id="4a96c-132">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4a96c-132">**True** or **False**</span></span> | <span data-ttu-id="4a96c-133">ถ้ามีการตั้งค่าคุณสมบัตินี้เป็น **จริง** ค่าธรรมเนียมการจัดส่งที่ใช้กับสินค้าในรายการจะแสดงในรายการของรถเข็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-133">If this property is set to **True**, the shipping charges that are applicable for line items will be shown on cart lines.</span></span> <span data-ttu-id="4a96c-134">หากไม่ได้เปิด **ค่าธรรมเนียมในส่วนหัวที่ไม่มีการแบ่งตามสัดส่วน** ในศูนย์ควบคุม Commerce ค่าธรรมเนียมการจัดส่งจะนำไปใช้ในระดับส่วนหัวไม่ใช่ระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="4a96c-134">If the **Header charge with no proration** feature is turned on in Commerce headquarters, the shipping charge will be applied at the header level, not the line level.</span></span> <span data-ttu-id="4a96c-135">คุณลักษณะนี้มีการเพิ่มใน Commerce รุ่น10.0.13</span><span class="sxs-lookup"><span data-stu-id="4a96c-135">This feature was added in Commerce version 10.0.13.</span></span> |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="4a96c-136">โมดูลที่สามารถใช้ในโมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-136">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="4a96c-137">**ที่อยู่จัดส่ง** –โมดูลนี้จะช่วยให้ลูกค้าเพิ่มหรือเลือกที่อยู่จัดส่งสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-137">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="4a96c-138">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลที่อยู่จัดส่ง](ship-address-module.md)</span><span class="sxs-lookup"><span data-stu-id="4a96c-138">For more information about this module, see [Shipping address module](ship-address-module.md).</span></span>

    <span data-ttu-id="4a96c-139">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลที่อยู่การจัดส่งบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-139">The following image shows an example of a shipping address module on a checkout page.</span></span>

    ![ตัวอย่างของโมดูลที่อยู่จัดส่ง](./media/ecommerce-shippingaddress.PNG)

- <span data-ttu-id="4a96c-141">**ตัวเลือกการจัดส่ง** – โมดูลนี้จะช่วยให้ลูกค้าสามารถเลือกวิธีการจัดส่งสำหรับใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="4a96c-141">**Delivery options** – This module lets a customer select a mode of delivery for an order.</span></span> <span data-ttu-id="4a96c-142">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลตัวเลือกการจัดส่ง](delivery-options-module.md)</span><span class="sxs-lookup"><span data-stu-id="4a96c-142">For more information about this module, see [Delivery options module](delivery-options-module.md).</span></span>

    <span data-ttu-id="4a96c-143">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกการจัดส่งบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-143">The following image shows an example of a delivery options module on a checkout page.</span></span>
 
    ![ตัวอย่างของโมดูลตัวเลือกการจัดส่ง](./media/ecommerce-deliveryoptions.PNG)

- <span data-ttu-id="4a96c-145">**คอนเทนเนอร์ส่วนการเช็คเอาท์** –โมดูลนี้เป็นคอนเทนเนอร์ที่คุณสามารถใส่หลายโมดูลภายใน เพื่อสร้างส่วนภายในขั้นตอนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4a96c-145">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="4a96c-146">ตัวอย่าง เช่น คุณสามารถกำหนดโมดูลที่เกี่ยวข้องกับการชำระเงินทั้งหมด ภายในคอนเทนเนอร์นี้เพื่อให้ปรากฏเป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-146">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="4a96c-147">โมดูลนี้มีผลเฉพาะกับโครงร่างของลำดับงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4a96c-147">This module affects only the layout of the flow.</span></span>

- <span data-ttu-id="4a96c-148">**บัตรของขวัญ** –โมดูลนี้จะช่วยให้ลูกค้าชำระเงินสำหรับใบสั่ง โดยใช้บัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="4a96c-148">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="4a96c-149">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลบัตรของขวัญ](add-giftcard.md)</span><span class="sxs-lookup"><span data-stu-id="4a96c-149">For more information about this module, see [Gift card module](add-giftcard.md).</span></span>

- <span data-ttu-id="4a96c-150">**คะแนนสะสมสำหรับสมาชิก** –โมดูลนี้จะช่วยให้ลูกค้าชำระเงินสำหรับใบสั่งโดยใช้คะแนนสะสมสำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="4a96c-150">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="4a96c-151">โดยจะให้ข้อมูลสรุปของคะแนนที่พร้อมใช้งานและคะแนนที่กำลังจะหมดอายุ และให้ลูกค้าสามารถเลือกจำนวนคะแนนเพื่อใช้แลกรางวัล</span><span class="sxs-lookup"><span data-stu-id="4a96c-151">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="4a96c-152">ถ้าลูกค้าไม่ได้ล็อกอินหรือไม่ใช่สมาชิกสมาชิก หรือถ้ายอดเงินรวมในรถเข็นเป็น 0 (ศูนย์) โมดูลนี้จะถูกซ่อนไว้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4a96c-152">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>

- <span data-ttu-id="4a96c-153">**การชำระเงิน** – โมดูลนี้จะช่วยให้ลูกค้าชำระเงินสำหรับใบสั่ง โดยใช้บัตรเครดิตหรือบัตรเดบิต</span><span class="sxs-lookup"><span data-stu-id="4a96c-153">**Payment** – This module lets a customer pay for an order by using a credit or debit card.</span></span> <span data-ttu-id="4a96c-154">ลูกค้ายังสามารถระบุที่อยู่สำหรับการเรียกเก็บเงินสำหรับตัวเลือกการชำระเงินที่จะเลือกได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="4a96c-154">Customers can also provide a billing address for the payment option that they select.</span></span> <span data-ttu-id="4a96c-155">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมดูลนี้ โปรดดูที่ [โมดูลการชำระเงิน](payment-module.md)</span><span class="sxs-lookup"><span data-stu-id="4a96c-155">For more information about this module, see [Payment module](payment-module.md).</span></span>

    <span data-ttu-id="4a96c-156">รูปภาพต่อไปนี้แสดงตัวอย่างโมดูลบัตรของขวัญ คะแนนสะสมสำหรับสมาชิก และการชำระเงินบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-156">The following image shows an example of gift card, loyalty points, and payment modules on a checkout page.</span></span>

    ![ตัวอย่างโมดูลบัตรของขวัญ คะแนนสะสมสำหรับสมาชิก และการชำระเงินบนหน้าเช็คเอาท์](./media/ecommerce-payments.PNG)

- <span data-ttu-id="4a96c-158">**ข้อมูลการติดต่อ** –โมดูลนี้จะช่วยให้ลูกค้าสามารถเพิ่มหรือเปลี่ยนแปลงข้อมูลการติดต่อ (ที่อยู่อีเมล์) สำหรับใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="4a96c-158">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>

- <span data-ttu-id="4a96c-159">**บล็อกข้อความ** – โมดูลนี้มีการส่งข้อความใด ๆ ที่ขับเคลื่อนโดยระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="4a96c-159">**Text block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="4a96c-160">ตัวอย่างเช่น อาจประกอบด้วยข้อความที่ระบุว่า "สำหรับปัญหาต่างๆ เกี่ยวกับใบสั่งของคุณ โปรดติดต่อ 1-800-Fabrikam"</span><span class="sxs-lookup"><span data-stu-id="4a96c-160">For example, it might contain a message that states, "For issues with your order, contact 1-800-Fabrikam."</span></span> 

- <span data-ttu-id="4a96c-161">**ข้อกำหนดและเงื่อนไขการเช็คเอาท์** – โมดูลนี้แสดงข้อความซึ่งประกอบด้วยข้อกำหนดและเงื่อนไขและกล่องกาเครื่องหมายสำหรับข้อมูลที่ลูกค้าป้อน</span><span class="sxs-lookup"><span data-stu-id="4a96c-161">**Checkout terms and conditions** – This module shows rich text that contains the terms and conditions and a check box for the customer input.</span></span> <span data-ttu-id="4a96c-162">กล่องกาเครื่องหมายนี้ไม่จำเป็นต้องระบุและสามารถตั้งค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="4a96c-162">The check box is optional and configurable.</span></span> <span data-ttu-id="4a96c-163">โมดูลจะบันทึกข้อมูลที่ป้อนไว้และสามารถใช้เมื่อมีการตรวจสอบก่อนที่จะทริกเกอร์การสั่งซื้อ แต่ไม่ได้รวมอยู่ในข้อมูลสรุปใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-163">The input is captured by the module and can be used as a check before order placement is triggered, but it isn't included in the order summary information.</span></span> <span data-ttu-id="4a96c-164">คุณสามารถเพิ่มโมดูลนี้ลงในคอนเทนเนอร์เช็คเอาท์ คอนเทนเนอร์ส่วนเช็คเอาท์ หรือช่องข้อกำหนดและเงื่อนไขได้ตามความต้องการของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4a96c-164">This module can be added to the checkout container, checkout section container, or terms and conditions slot, according to business needs.</span></span> <span data-ttu-id="4a96c-165">ถ้ามีการเพิ่มลงในคอนเทนเนอร์เช็คเอาท์หรือช่องคอนเทนเนอร์ส่วนเช็คเอาท์ โมดูลจะปรากฏขึ้นเป็นขั้นตอนในกระบวนการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-165">If it's added to the checkout container or checkout section container slot, it will appear as a step in the checkout process.</span></span> <span data-ttu-id="4a96c-166">หากมีการเพิ่มในช่องข้อกำหนดและเงื่อนไข โมดูลจะปรากฏขึ้นใกล้กับปุ่มการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4a96c-166">If it's added to the terms and conditions slot, it will appear near the order placement button.</span></span>

    <span data-ttu-id="4a96c-167">รูปภาพต่อไปนี้แสดงตัวอย่างของข้อกำหนดและเงื่อนไขบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4a96c-167">The following image shows an example of terms and conditions on a checkout page.</span></span>

    ![ตัวอย่างของข้อกำหนดและเงื่อนไขบนหน้าเช็คเอาท์](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="4a96c-169">การโต้ตอบ Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="4a96c-169">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="4a96c-170">ข้อมูลส่วนใหญ่ของการชำระเงิน เช่น ที่อยู่ในการจัดส่ง และวิธีการจัดส่งสินค้า จะถูกจัดเก็บไว้ในรถเข็นและดำเนินการโดยเป็นส่วนหนึ่งของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-170">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="4a96c-171">ข้อยกเว้นเดียวคือข้อมูลบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="4a96c-171">The only exception is the credit card information.</span></span> <span data-ttu-id="4a96c-172">ข้อมูลนี้จะถูกประมวลผลโดยตรงโดยใช้ตัวเชื่อมต่อการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="4a96c-172">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="4a96c-173">การชำระเงินได้รับอนุมัติแล้ว แต่ยังไม่มีการคิดค่าธรรมเนียมจนกว่าจะมีการดำเนินการตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-173">The payment is authorized, but it isn't charged until the order is fulfilled.</span></span>

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a><span data-ttu-id="4a96c-174">เพิ่มโมดูลเช็คเอาท์ไปยังหน้า และตั้งค่าคุณสมบัติที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-174">Add a checkout module to a page and set the required properties</span></span>

<span data-ttu-id="4a96c-175">การเพิ่มโมดูลกเช็คเอาท์ไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4a96c-175">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4a96c-176">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="4a96c-176">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="4a96c-177">ในกล่องโต้ตอบ **ส่วนย่อยของหน้าใหม่** ให้เลือกโมดูล **เช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="4a96c-177">In the **New page fragment** dialog box, select the **Checkout** module.</span></span>
1. <span data-ttu-id="4a96c-178">ภายใต้ **ชื่อส่วนย่อยของหน้า** ให้ป้อนชื่อสำหรับ **ส่วนย่อยการเช็คเอาท์** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4a96c-178">Under **Page fragment name**, enter the name **Checkout fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="4a96c-179">เลือกช่อง **โมดูลการเช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="4a96c-179">Select the **Checkout module** slot.</span></span>
1. <span data-ttu-id="4a96c-180">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกสัญลักษณ์ดินสอ ป้อนข้อความหัวข้อในฟิลด์ แล้วเลือกสัญลักษณ์เครื่องหมายถูก</span><span class="sxs-lookup"><span data-stu-id="4a96c-180">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="4a96c-181">ในช่อง **เช็คเอาท์ข้อมูล** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4a96c-181">In the **Checkout Information** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4a96c-182">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **ที่อยู่ในการจัดส่ง** **ตัวเลือกการจัดส่ง** **คอนเทนเนอร์ส่วนเช็คเอาท์** และ **ข้อมูลการติดต่อ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4a96c-182">In the **Add Module** dialog box, select the **Shipping address**, **Delivery options**, **Checkout section container**, and **Contact information** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="4a96c-183">ในโมดูล **คอนเทนเนอร์ส่วนเช็คเอาท์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="4a96c-183">In the **Checkout section container** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4a96c-184">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **บัตรของขวัญ** **สมาชิก** และ **การชำระเงิน** จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4a96c-184">In the **Add Module** dialog box, select the **Gift card**, **Loyalty**, and **Payment** modules, and then select **OK**.</span></span> <span data-ttu-id="4a96c-185">ด้วยวิธีนี้ คุณควรตรวจสอบให้แน่ใจว่าวิธีการชำระเงินทั้งหมดจะปรากฏรวมกันในส่วน</span><span class="sxs-lookup"><span data-stu-id="4a96c-185">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="4a96c-186">ในช่อง **ข้อกำหนดและเงื่อนไข** ให้เพิ่มโมดูล **ข้อกำหนดและเงื่อนไขการเช็คเอาท์** หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-186">In the **Terms and conditions** slot, add a **Checkout terms and conditions** module if it's required.</span></span> <span data-ttu-id="4a96c-187">ในแผงคุณสมบัติของโมดูล ให้ตั้งค่าคอนฟิกข้อความของข้อกำหนดและเงื่อนไขตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="4a96c-187">In the module's properties pane, configure the terms and condition text as appropriate.</span></span>
1. <span data-ttu-id="4a96c-188">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="4a96c-188">Select **Save**, and then select **Preview** to preview the fragment.</span></span> <span data-ttu-id="4a96c-189">บางโมดูลที่ไม่มีบริบทรถเข็น อาจไม่แสดงในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="4a96c-189">Some modules that don't have a cart context might not be rendered in the preview.</span></span>
1. <span data-ttu-id="4a96c-190">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อเช็คอินส่วนย่อย และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="4a96c-190">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4a96c-191">สร้างเท็มเพลตที่ใช้ส่วนการชำระเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="4a96c-191">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="4a96c-192">สร้างส่วนการชำระเงินที่ใช้เท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="4a96c-192">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a96c-193">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4a96c-193">Additional resources</span></span>

[<span data-ttu-id="4a96c-194">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-194">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4a96c-195">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="4a96c-195">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4a96c-196">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4a96c-196">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4a96c-197">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-197">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4a96c-198">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-198">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4a96c-199">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4a96c-199">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4a96c-200">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="4a96c-200">Gift card module</span></span>](add-giftcard.md)
