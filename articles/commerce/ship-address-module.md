---
title: โมดูลที่อยู่จัดส่ง
description: หัวข้อนี้กล่าวถึงโมดูลที่อยู่จัดส่งและอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/07/2020
ms.locfileid: "4416290"
---
# <a name="shipping-address-module"></a><span data-ttu-id="99927-103">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="99927-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99927-104">หัวข้อนี้อธิบายโมดูลที่อยู่จัดส่งและอธิบายวิธีการกำหนดค่าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="99927-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="99927-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="99927-105">Overview</span></span>

<span data-ttu-id="99927-106">โมดูลที่อยู่จัดส่งนี้จะช่วยให้ลูกค้าเพิ่มหรือเลือกที่อยู่จัดส่งสำหรับใบสั่งในระหว่างขั้นตอนการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="99927-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="99927-107">ถ้าลูกค้าเคยลงชื่อเข้าใช้ไว้ ที่อยู่ที่บันทึกไว้ก่อนหน้านี้สำหรับลูกค้ารายนั้นจะแสดงขึ้นและลูกค้าสามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="99927-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="99927-108">ลูกค้ายังสามารถเพิ่มที่อยู่ใหม่ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="99927-108">The customer can also add a new address.</span></span> <span data-ttu-id="99927-109">โมดูลที่อยู่จัดส่งจะใช้สำหรับสินค้าทั้งหมดในใบสั่งที่ต้องมีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="99927-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="99927-110">คุณสามารถกำหนดรูปแบบที่อยู่ที่จัดส่งในศูนย์ควบคุม Commerce สำหรับแต่ละประเทศหรือภูมิภาคและโมดูลที่อยู่ที่จัดส่งจะบังคับใช้กฎเฉพาะประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="99927-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="99927-111">เมื่อลูกค้าป้อนที่อยู่ที่จัดส่งในระหว่างขั้นตอนการเช็คเอาท์ จะมีตัวเลือกในการบันทึกที่อยู่เป็นที่อยู่หลัก</span><span class="sxs-lookup"><span data-stu-id="99927-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="99927-112">ตัวเลือกนี้จะแสดงขึ้นเฉพาะเมื่อลูกค้าลงชื่อเข้าใช้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="99927-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="99927-113">ถึงแม้ว่าโมดูลที่อยู่จัดส่งนี้จะไม่มีการตรวจสอบความถูกต้องของที่อยู่ แต่ฟังก์ชันนี้สามารถดำเนินการผ่านการเลือกกำหนด</span><span class="sxs-lookup"><span data-stu-id="99927-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="99927-114">ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลที่อยู่จัดส่งใหม่บนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="99927-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![ตัวอย่างของโมดูลที่อยู่จัดส่งบนหน้าเช็คเอาท์](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="99927-116">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="99927-116">Module properties</span></span>

| <span data-ttu-id="99927-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="99927-117">Property name</span></span> | <span data-ttu-id="99927-118">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="99927-118">Values</span></span> | <span data-ttu-id="99927-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="99927-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="99927-120">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="99927-120">Heading</span></span> | <span data-ttu-id="99927-121">ข้อความหัวเรื่องและแท็กหัวเรื่อง (**H1**, **H2**, **H3**, **H4**, **H5** หรือ **H6**)</span><span class="sxs-lookup"><span data-stu-id="99927-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="99927-122">หัวเรื่องที่เป็นตัวเลือกสำหรับโมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="99927-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="99927-123">แสดงชนิดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="99927-123">Show address type</span></span> | <span data-ttu-id="99927-124">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="99927-124">**True** or **False**</span></span> | <span data-ttu-id="99927-125">ถ้ามีการตั้งค่าคุณสมบัติที่เป็นตัวเลือกนี้เป็น **จริง** ชนิดที่อยู่ เช่น **บ้าน** หรือ **ธุรกิจ** จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="99927-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="99927-126">ถ้าไม่มีการระบุชนิดของที่อยู่ ที่อยู่จะถูกบันทึกเป็น **ชนิด**=**อื่นๆ** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="99927-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="99927-127">เพิ่มโมดูลที่อยู่จัดส่งไปยังหน้าเช็คเอาท์ และตั้งค่าคุณสมบัติที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="99927-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="99927-128">คุณสามารถเพิ่มโมดูลที่อยู่จัดส่งได้เฉพาะในโมดูลเช็คเอาท์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="99927-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="99927-129">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกโมดูลที่อยู่จัดส่งและเพิ่มลงในหน้าเช็คเอาท์ โปรดดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="99927-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99927-130">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="99927-130">Additional resources</span></span>

[<span data-ttu-id="99927-131">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="99927-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="99927-132">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="99927-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="99927-133">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="99927-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="99927-134">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="99927-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="99927-135">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="99927-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="99927-136">โมดูลข้อมูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="99927-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="99927-137">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="99927-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="99927-138">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="99927-138">Gift card module</span></span>](add-giftcard.md)
