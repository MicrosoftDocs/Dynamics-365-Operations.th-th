---
title: โมดูลที่อยู่จัดส่ง
description: หัวข้อนี้กล่าวถึงโมดูลที่อยู่จัดส่งและอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 02/11/2021
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
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795440"
---
# <a name="shipping-address-module"></a><span data-ttu-id="abeb6-103">โมดูลที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="abeb6-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="abeb6-104">หัวข้อนี้อธิบายโมดูลที่อยู่จัดส่งและอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="abeb6-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="abeb6-105">โมดูลที่อยู่จัดส่งนี้จะช่วยให้ลูกค้าเพิ่มหรือเลือกที่อยู่จัดส่งสำหรับใบสั่งในระหว่างขั้นตอนการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="abeb6-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="abeb6-106">ถ้าลูกค้าเคยลงชื่อเข้าใช้ไว้ ที่อยู่ที่บันทึกไว้ก่อนหน้านี้สำหรับลูกค้ารายนั้นจะแสดงขึ้นและลูกค้าสามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="abeb6-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="abeb6-107">ลูกค้ายังสามารถเพิ่มที่อยู่ใหม่ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="abeb6-107">The customer can also add a new address.</span></span> <span data-ttu-id="abeb6-108">โมดูลที่อยู่จัดส่งจะใช้สำหรับสินค้าทั้งหมดในใบสั่งที่ต้องมีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="abeb6-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="abeb6-109">คุณสามารถกำหนดรูปแบบที่อยู่ที่จัดส่งในศูนย์ควบคุม Commerce สำหรับแต่ละประเทศหรือภูมิภาคและโมดูลที่อยู่ที่จัดส่งจะบังคับใช้กฎเฉพาะประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="abeb6-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="abeb6-110">เมื่อลูกค้าป้อนที่อยู่ที่จัดส่งในระหว่างขั้นตอนการเช็คเอาท์ จะมีตัวเลือกในการบันทึกที่อยู่เป็นที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="abeb6-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="abeb6-111">ตัวเลือกนี้จะแสดงขึ้นเฉพาะเมื่อลูกค้าลงชื่อเข้าใช้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="abeb6-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="abeb6-112">ถึงแม้ว่าโมดูลที่อยู่จัดส่งนี้จะไม่มีการตรวจสอบความถูกต้องของที่อยู่ แต่ฟังก์ชันนี้สามารถดำเนินการผ่านการเลือกกำหนด</span><span class="sxs-lookup"><span data-stu-id="abeb6-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="abeb6-113">ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลที่อยู่จัดส่งใหม่บนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="abeb6-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![ตัวอย่างของโมดูลที่อยู่จัดส่งบนหน้าเช็คเอาท์](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="abeb6-115">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="abeb6-115">Module properties</span></span>

| <span data-ttu-id="abeb6-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="abeb6-116">Property name</span></span> | <span data-ttu-id="abeb6-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="abeb6-117">Values</span></span> | <span data-ttu-id="abeb6-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="abeb6-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="abeb6-119">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="abeb6-119">Heading</span></span> | <span data-ttu-id="abeb6-120">ข้อความหัวเรื่องและแท็กหัวเรื่อง (**H1**, **H2**, **H3**, **H4**, **H5** หรือ **H6**)</span><span class="sxs-lookup"><span data-stu-id="abeb6-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="abeb6-121">หัวเรื่องที่เป็นตัวเลือกสำหรับโมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="abeb6-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="abeb6-122">แสดงชนิดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="abeb6-122">Show address type</span></span> | <span data-ttu-id="abeb6-123">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="abeb6-123">**True** or **False**</span></span> | <span data-ttu-id="abeb6-124">ถ้ามีการตั้งค่าคุณสมบัติที่เป็นตัวเลือกนี้เป็น **จริง** ชนิดที่อยู่ เช่น **บ้าน** หรือ **ธุรกิจ** จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="abeb6-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="abeb6-125">ถ้าไม่มีการระบุชนิดของที่อยู่ ที่อยู่จะถูกบันทึกเป็น **ชนิด**=**อื่นๆ** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="abeb6-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="abeb6-126">เปิดใช้งานการแนะนำอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="abeb6-126">Enable auto suggestion</span></span>| <span data-ttu-id="abeb6-127">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="abeb6-127">**True** or **False**</span></span> | <span data-ttu-id="abeb6-128">หากการตั้งค่าคุณสมบัติที่เลือกได้นี้เป็น **จริง** จะมีการเสนอคำแนะนำที่อยู่อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="abeb6-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="abeb6-129">คำแนะนำเหล่านี้ขับเคลื่อนโดย Bing Maps</span><span class="sxs-lookup"><span data-stu-id="abeb6-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="abeb6-130">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีตั้งค่าการรวม Bing Maps ของไซต์ของคุณ โปรดดูที่ [โมดูลตัวเลือกร้านค้า](store-selector.md)</span><span class="sxs-lookup"><span data-stu-id="abeb6-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="abeb6-131">คุณลักษณะนี้พร้อมใช้งานตั้งแต่ Commerce รุ่น 10.0.15</span><span class="sxs-lookup"><span data-stu-id="abeb6-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="abeb6-132">ตัวเลือกการแนะนำอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="abeb6-132">Auto suggest options</span></span>| <span data-ttu-id="abeb6-133">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="abeb6-133">A number</span></span>| <span data-ttu-id="abeb6-134">หากมีการเปิดใช้งานการแนะนำที่อยู่อัตโนมัติ คุณสามารถระบุตัวเลือกเพิ่มเติมได้ เช่น จํานวนคำแนะนำสูงสุดที่ควรให้</span><span class="sxs-lookup"><span data-stu-id="abeb6-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="abeb6-135">เพิ่มโมดูลที่อยู่จัดส่งไปยังหน้าเช็คเอาท์ และตั้งค่าคุณสมบัติที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="abeb6-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="abeb6-136">คุณสามารถเพิ่มโมดูลที่อยู่จัดส่งได้เฉพาะในโมดูลเช็คเอาท์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="abeb6-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="abeb6-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกโมดูลที่อยู่จัดส่งและเพิ่มลงในหน้าเช็คเอาท์ โปรดดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="abeb6-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abeb6-138">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="abeb6-138">Additional resources</span></span>

[<span data-ttu-id="abeb6-139">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="abeb6-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="abeb6-140">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="abeb6-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="abeb6-141">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="abeb6-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="abeb6-142">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="abeb6-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="abeb6-143">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="abeb6-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="abeb6-144">โมดูลข้อมูลการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="abeb6-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="abeb6-145">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="abeb6-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="abeb6-146">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="abeb6-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="abeb6-147">โมดูลตัวเลือกการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="abeb6-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]