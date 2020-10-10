---
title: โมดูลตัวเลือกการจัดส่ง
description: หัวข้อนี้กล่าวถึงโมดูลตัวเลือกการจัดส่งและอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39e597b88afcca69623b1a23acc95e4da3873082
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818310"
---
# <a name="delivery-options-module"></a><span data-ttu-id="053fe-103">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="053fe-104">หัวข้อนี้กล่าวถึงโมดูลตัวเลือกการจัดส่งและอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="053fe-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="053fe-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="053fe-105">Overview</span></span>

<span data-ttu-id="053fe-106">โมดูลการเลือกการจัดส่งให้ลูกค้าเลือกวิธีการจัดส่ง เช่น การจัดส่งหรือการรับสินค้าสำหรับคำสั่งซื้อออนไลน์ของตน</span><span class="sxs-lookup"><span data-stu-id="053fe-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="053fe-107">ต้องระบุที่อยู่จัดส่งเพื่อกำหนดวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="053fe-108">ถ้ามีการเปลี่ยนแปลงที่อยู่จัดส่ง คุณต้องดึงข้อมูลตัวเลือกการจัดส่งอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="053fe-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="053fe-109">ถ้าใบสั่งมีเฉพาะสินค้าที่จะเบิกสินค้าในร้านค้า โมดูลนี้จะถูกซ่อนไว้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="053fe-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="053fe-110">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกวิธีการจัดส่ง โปรดดูที่ [การตั้งค่าช่องทางออนไลน์](channel-setup-online.md) และ [ตั้งค่าวิธีการจัดส่ง](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)</span><span class="sxs-lookup"><span data-stu-id="053fe-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="053fe-111">วิธีการจัดส่งแต่ละวิธีอาจมีค่าใช้จ่ายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="053fe-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="053fe-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกค่าธรรมเนียมสำหรับร้านค้าออนไลน์ โปรดดูที่ [ค่าธรรมเนียมอัตโนมัติขั้นสูงช่องทาง Omni](omni-auto-charges.md)</span><span class="sxs-lookup"><span data-stu-id="053fe-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="053fe-113">ใน Commerce รุ่น 10.0.13 โมดูลตัวเลือกการจัดส่งได้รับการอัพเดตเพื่อสนับสนุนคุณลักษณะ **ค่าธรรมเนียมในส่วนหัวที่ไม่มีการแบ่งตามสัดส่วน** และ **การจัดส่งเป็นค่าธรรมเนียมต่อรายการ**</span><span class="sxs-lookup"><span data-stu-id="053fe-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="053fe-114">ถ้ามีการปิดการแบ่งตามสัดส่วน ความคาดหวังคือลำดับงานอีคอมเมิร์ซจะไม่อนุญาตให้ใช้วิธีการจัดส่งแบบผสมสำหรับสินค้าในรถเข็น (นั่นคือมีการเลือกสินค้าบางรายการสำหรับการจัดส่ง แต่จะมีการเลือกสินค้าอื่นๆ สำหรับการรับสินค้า)</span><span class="sxs-lookup"><span data-stu-id="053fe-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="053fe-115">คุณลักษณะ **ค่าธรรมเนียมในส่วนหัวที่ไม่มีการแบ่งตามสัดส่วน** ต้องมีการเปิดค่าสถานะ **เปิดใช้งานการจัดการโหมดการจัดส่งที่สอดคล้องกันในช่องทาง** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="053fe-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="053fe-116">หากเปิดค่าสถานะ ค่าธรรมเนียมการจัดส่งจะมีการใช้กับระดับส่วนหัวหรือระดับรายการ ขึ้นอยู่กับการตั้งค่าคอนฟิกในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="053fe-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="053fe-117">ธีม Fabrikam สนับสนุนโหมดการจัดส่งแบบผสมที่มีการเลือกการจัดส่งสำหรับสินค้าบางรายการ แต่มีการเลือกการรับสินค้าสำหรับสินค้าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="053fe-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="053fe-118">ในโหมดนี้ ค่าธรรมเนียมการจัดส่งจะแบ่งสัดส่วนสำหรับสินค้าทั้งหมดที่เลือกไว้สำหรับวิธีการจัดส่งของการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="053fe-119">สำหรับวิธีการจัดส่งแบบผสมที่จะใช้ คุณต้องตั้งค่าคอนฟิกคุณลักษณะ **ค่าธรรมเนียมในส่วนหัวที่มีการแบ่งตามสัดส่วน** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="053fe-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="053fe-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าคอนฟิกนี้ โปรดให้ดู [แบ่งค่าธรรมเนียมในส่วนหัวตามสัดส่วนให้ตรงกับรายการขาย](pro-rate-charges-matching-lines.md)</span><span class="sxs-lookup"><span data-stu-id="053fe-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="053fe-121">ถ้ามีการเรียกเก็บค่าธรรมเนียมการจัดส่งกับสินค้าในรายการ จะมีการแสดงในรายการของรถเข็นสำหรับสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="053fe-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="053fe-122">ฟังก์ชันนี้จำเป็นต้องมีการเปิดใช้คุณสมบัติ **แสดงค่าธรมเนียมการจัดส่งสินค้าในรายการ** สำหรับทั้งโมดูลรถเข็นและโมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="053fe-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="053fe-123">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [โมดูลรถเข็น](add-cart-module.md) และ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="053fe-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="053fe-124">ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกการจัดส่งบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="053fe-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![ตัวอย่างของโมดูลตัวเลือกการจัดส่งบนหน้าเช็คเอาท์](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="053fe-126">คุณสมบัติของโมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-126">Delivery options module properties</span></span>

| <span data-ttu-id="053fe-127">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="053fe-127">Property</span></span> | <span data-ttu-id="053fe-128">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="053fe-128">Values</span></span> | <span data-ttu-id="053fe-129">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="053fe-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="053fe-130">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="053fe-130">Heading</span></span> | <span data-ttu-id="053fe-131">ข้อความหัวเรื่องและแท็กหัวเรื่อง (**H1**, **H2**, **H3**, **H4**, **H5** หรือ **H6**)</span><span class="sxs-lookup"><span data-stu-id="053fe-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="053fe-132">หัวเรื่องที่เป็นตัวเลือกสำหรับโมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="053fe-133">ชื่อคลาส CSS แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="053fe-133">Custom CSS class name</span></span> | <span data-ttu-id="053fe-134">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="053fe-134">Text</span></span> | <span data-ttu-id="053fe-135">ชื่อคลาสแผ่นงานที่จัดรูปแบบเป็นลำดับ (CSS) แบบกำหนดเองจะใช้แสดงโมดูลนี้ หากเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="053fe-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="053fe-136">ตัวเลือกโหมดการจัดส่งตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="053fe-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="053fe-137">**ไม่ต้องกรอง** หรือ **โหมดที่ไม่ใช่การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="053fe-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="053fe-138">ค่าที่ระบุว่าโมดูลตัวเลือกการจัดส่งควรกรองโหมดที่ไม่ใช่การจัดส่งทั้งหมดออกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="053fe-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="053fe-139">เพิ่มโมดูลตัวเลือกการจัดส่งไปยังหน้าเช็คเอาท์ และตั้งค่าคุณสมบัติที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="053fe-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="053fe-140">คุณสามารถเพิ่มโมดูลตัวเลือกการจัดส่งได้เฉพาะในโมดูลเช็คเอาท์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="053fe-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="053fe-141">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกโมดูลตัวเลือกการจัดส่งและเพิ่มลงในหน้าเช็คเอาท์ โปรดดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="053fe-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="053fe-142">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="053fe-142">Additional resources</span></span>

[<span data-ttu-id="053fe-143">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="053fe-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="053fe-144">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="053fe-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="053fe-145">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="053fe-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="053fe-146">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="053fe-147">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="053fe-148">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="053fe-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="053fe-149">การตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="053fe-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="053fe-150">ค่าธรรมเนียมอัตโนมัติขั้นสูงของช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="053fe-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="053fe-151">แบ่งค่าธรรมเนียมในส่วนหัวตามสัดส่วนให้ตรงกับรายการขาย</span><span class="sxs-lookup"><span data-stu-id="053fe-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="053fe-152">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="053fe-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
