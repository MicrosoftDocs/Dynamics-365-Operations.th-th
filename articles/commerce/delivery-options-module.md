---
title: โมดูลตัวเลือกการจัดส่ง
description: หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกการจัดส่งและอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 8342afefa6eeda3a53decb39caddb62d1e4e1963
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270872"
---
# <a name="delivery-options-module"></a><span data-ttu-id="53805-103">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="53805-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53805-104">หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกการจัดส่งและอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="53805-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="53805-105">โมดูลการเลือกการจัดส่งให้ลูกค้าเลือกวิธีการจัดส่ง เช่น การจัดส่งหรือการรับสินค้าสำหรับคำสั่งซื้อออนไลน์ของตน</span><span class="sxs-lookup"><span data-stu-id="53805-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="53805-106">ต้องระบุที่อยู่จัดส่งเพื่อกำหนดวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="53805-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="53805-107">ถ้ามีการเปลี่ยนแปลงที่อยู่จัดส่ง คุณต้องดึงข้อมูลตัวเลือกการจัดส่งอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="53805-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="53805-108">ถ้าใบสั่งมีเฉพาะสินค้าที่จะเบิกสินค้าในร้านค้า โมดูลนี้จะถูกซ่อนไว้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="53805-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="53805-109">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกวิธีการจัดส่ง โปรดดูที่ [การตั้งค่าช่องทางออนไลน์](channel-setup-online.md) และ [ตั้งค่าวิธีการจัดส่ง](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)</span><span class="sxs-lookup"><span data-stu-id="53805-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="53805-110">วิธีการจัดส่งแต่ละวิธีอาจมีค่าใช้จ่ายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="53805-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="53805-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกค่าธรรมเนียมสำหรับร้านค้าออนไลน์ โปรดดูที่ [ค่าธรรมเนียมอัตโนมัติขั้นสูงช่องทาง Omni](omni-auto-charges.md)</span><span class="sxs-lookup"><span data-stu-id="53805-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="53805-112">ใน Commerce รุ่น 10.0.13 โมดูลตัวเลือกการจัดส่งได้รับการอัพเดตเพื่อสนับสนุนคุณลักษณะ **ค่าธรรมเนียมในส่วนหัวที่ไม่มีการแบ่งตามสัดส่วน** และ **การจัดส่งเป็นค่าธรรมเนียมต่อรายการ**</span><span class="sxs-lookup"><span data-stu-id="53805-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="53805-113">ถ้ามีการปิดการแบ่งตามสัดส่วน ความคาดหวังคือลำดับงานอีคอมเมิร์ซจะไม่อนุญาตให้ใช้วิธีการจัดส่งแบบผสมสำหรับสินค้าในรถเข็น (นั่นคือมีการเลือกสินค้าบางรายการสำหรับการจัดส่ง แต่จะมีการเลือกสินค้าอื่นๆ สำหรับการรับสินค้า)</span><span class="sxs-lookup"><span data-stu-id="53805-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="53805-114">คุณลักษณะ **ค่าธรรมเนียมในส่วนหัวที่ไม่มีการแบ่งตามสัดส่วน** ต้องมีการเปิดค่าสถานะ **เปิดใช้งานการจัดการโหมดการจัดส่งที่สอดคล้องกันในช่องทาง** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="53805-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="53805-115">หากเปิดค่าสถานะคุณลักษณะนั้น จะมีการใช้ค่าธรรมเนียมการจัดส่งกับระดับส่วนหัวหรือระดับรายการ โดยขึ้นอยู่กับการตั้งค่าคอนฟิกในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="53805-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="53805-116">ธีม Fabrikam สนับสนุนโหมดการจัดส่งแบบผสมที่มีการเลือกการจัดส่งสำหรับสินค้าบางรายการ แต่มีการเลือกการรับสินค้าสำหรับสินค้าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="53805-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="53805-117">ในโหมดนี้ ค่าธรรมเนียมการจัดส่งจะแบ่งสัดส่วนสำหรับสินค้าทั้งหมดที่เลือกไว้สำหรับวิธีการจัดส่งของการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="53805-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="53805-118">สำหรับวิธีการจัดส่งแบบผสมที่จะใช้ คุณต้องตั้งค่าคอนฟิกคุณลักษณะ **ค่าธรรมเนียมในส่วนหัวที่มีการแบ่งตามสัดส่วน** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="53805-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="53805-119">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าคอนฟิกนี้ โปรดให้ดู [แบ่งค่าธรรมเนียมในส่วนหัวตามสัดส่วนให้ตรงกับรายการขาย](pro-rate-charges-matching-lines.md)</span><span class="sxs-lookup"><span data-stu-id="53805-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="53805-120">ถ้ามีการเรียกเก็บค่าธรรมเนียมการจัดส่งกับสินค้าในรายการ จะมีการแสดงในรายการของรถเข็นสำหรับสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="53805-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="53805-121">ฟังก์ชันนี้จำเป็นต้องมีการเปิดใช้คุณสมบัติ **แสดงค่าธรมเนียมการจัดส่งสินค้าในรายการ** สำหรับทั้งโมดูลรถเข็นและโมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="53805-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="53805-122">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [โมดูลรถเข็น](add-cart-module.md) และ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="53805-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="53805-123">ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกการจัดส่งบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="53805-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![ตัวอย่างของโมดูลตัวเลือกการจัดส่งบนหน้าเช็คเอาท์](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="53805-125">คุณสมบัติของโมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="53805-125">Delivery options module properties</span></span>

| <span data-ttu-id="53805-126">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="53805-126">Property</span></span> | <span data-ttu-id="53805-127">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="53805-127">Values</span></span> | <span data-ttu-id="53805-128">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="53805-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="53805-129">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="53805-129">Heading</span></span> | <span data-ttu-id="53805-130">ข้อความหัวเรื่องและแท็กหัวเรื่อง (**H1**, **H2**, **H3**, **H4**, **H5** หรือ **H6**)</span><span class="sxs-lookup"><span data-stu-id="53805-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="53805-131">หัวเรื่องที่เป็นตัวเลือกสำหรับโมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="53805-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="53805-132">ชื่อคลาส CSS แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="53805-132">Custom CSS class name</span></span> | <span data-ttu-id="53805-133">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="53805-133">Text</span></span> | <span data-ttu-id="53805-134">ชื่อคลาสแผ่นงานที่จัดรูปแบบเป็นลำดับ (CSS) แบบกำหนดเองจะใช้แสดงโมดูลนี้ หากเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="53805-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="53805-135">ตัวเลือกโหมดการจัดส่งตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="53805-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="53805-136">**ไม่ต้องกรอง** หรือ **โหมดที่ไม่ใช่การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="53805-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="53805-137">ค่าที่ระบุว่าโมดูลตัวเลือกการจัดส่งควรกรองโหมดที่ไม่ใช่การจัดส่งทั้งหมดออกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="53805-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="53805-138">เลือกตัวเลือกการจัดส่งโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="53805-138">Auto select a delivery option</span></span> | <span data-ttu-id="53805-139">**ไม่กรอง** **ตัวเลือกเลือกการจัดส่งอัตโนมัติและแสดงสรุป** หรือ **ตัวเลือกเลือกการจัดส่งอัตโนมัติและไม่แสดงสรุป**</span><span class="sxs-lookup"><span data-stu-id="53805-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="53805-140">คุณสมบัตินี้จะใช้ตัวเลือกการจัดส่งที่พร้อมใช้งานรายการแรกในการตรวจสอบโดยอัตโนมัติ โดยไม่ให้ผู้ใช้เลือกตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="53805-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="53805-141">ควรใช้ตัวเลือกนี้เฉพาะเมื่อมีตัวเลือกการจัดส่งที่พร้อมใช้งานเพียงตัวเลือกเดียว</span><span class="sxs-lookup"><span data-stu-id="53805-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="53805-142">มีการรองรับคุณสมบัตินี้ ณ การนำออกใช้ Commerce รุ่น 10.0.19</span><span class="sxs-lookup"><span data-stu-id="53805-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="53805-143">เพิ่มโมดูลตัวเลือกการจัดส่งไปยังหน้าเช็คเอาท์ และตั้งค่าคุณสมบัติที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="53805-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="53805-144">คุณสามารถเพิ่มโมดูลตัวเลือกการจัดส่งได้เฉพาะในโมดูลเช็คเอาท์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="53805-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="53805-145">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกโมดูลตัวเลือกการจัดส่งและเพิ่มลงในหน้าเช็คเอาท์ โปรดดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="53805-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53805-146">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="53805-146">Additional resources</span></span>

[<span data-ttu-id="53805-147">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="53805-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="53805-148">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="53805-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="53805-149">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="53805-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="53805-150">โมดูลที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="53805-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="53805-151">โมดูลข้อมูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="53805-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="53805-152">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="53805-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="53805-153">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="53805-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="53805-154">การตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="53805-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="53805-155">ค่าธรรมเนียมอัตโนมัติขั้นสูงของช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="53805-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="53805-156">แบ่งค่าธรรมเนียมในส่วนหัวตามสัดส่วนให้ตรงกับรายการขาย</span><span class="sxs-lookup"><span data-stu-id="53805-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="53805-157">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="53805-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
