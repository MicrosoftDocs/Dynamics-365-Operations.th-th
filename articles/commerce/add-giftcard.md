---
title: โมดูลบัตรของขวัญ
description: หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761092"
---
# <a name="gift-card-module"></a><span data-ttu-id="771ae-103">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="771ae-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="771ae-104">หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="771ae-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="771ae-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="771ae-105">Overview</span></span>

<span data-ttu-id="771ae-106">โมดูลบัตรของขวัญสามารถใช้ในโมดูลเช็คเอาท์เพื่อรับบัตรของขวัญ ซึ่งเป็นรูปแบบการชำระเงินทั่วไปที่ใช้สำหรับธุรกรรมอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="771ae-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="771ae-107">โมดูลบัตรของขวัญสนับสนุนบัตรของขวัญ Dynamics 365, SVS, และ Givex </span><span class="sxs-lookup"><span data-stu-id="771ae-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="771ae-108">บัตรของขวัญ SVS และ Givex จะถูกแลกรางวัลผ่านผู้ให้บริการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="771ae-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="771ae-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสนับสนุนสำหรับบัตรของขวัญภายนอก เช่น SVS และ Givex โปรดดูที่ [การสนับสนุนบัตรของขวัญภายนอก](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="771ae-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="771ae-110">มีโมดูลบัตรของขวัญสองรายการที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="771ae-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="771ae-111">**บัตรของขวัญ** - สำหรับโมดูลนี้สามารถใช้ในหน้าเช็คเอาท์เพื่อแลกบัตรของขวัญเป็นวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="771ae-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="771ae-112">**การตรวจสอบยอดคงเหลือในบัตรของขวัญ** โมดูลนี้สามารถใช้ในหน้าใดก็ได้เพื่อตรวจสอบยอดคงเหลือในบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="771ae-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="771ae-113">โมดูลนี้พร้อมใช้งานใน Commerce รีลีส 10.0.14 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="771ae-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="771ae-114">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลบัตรของขวัญบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="771ae-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![ตัวอย่างของโมดูลบัตรของขวัญ](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="771ae-116">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="771ae-116">Module properties</span></span>

- <span data-ttu-id="771ae-117">**แสดงฟิลด์เพิ่มเติม** - คุณสมบัตินี้กำหนดว่าควรแสดงฟิลด์ใดสำหรับบัตรของขวัญนอกเหนือจากหมายเลขบัตรของขวัญ ซึ่งจะแสดงตามค่าเริ่มต้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="771ae-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="771ae-118">ตัวอย่างเช่น บัตรของขวัญบางชิ้นสนับสนุนการแสดงหมายเลขรหัสประจำตัว (PIN) และการสนับสนุนอื่นๆ ที่แสดง PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="771ae-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="771ae-119">อีกทางหนึ่งคือ คุณสมบัตินี้อาจถูกตั้งค่าเป็น "ไม่มี" ซึ่งจะแสดงหมายเลขบัตรของขวัญเท่านั้นและไม่มีฟิลด์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="771ae-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="771ae-120">ค่าที่สนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="771ae-120">Supported values:</span></span>
-   <span data-ttu-id="771ae-121">PIN</span><span class="sxs-lookup"><span data-stu-id="771ae-121">PIN</span></span>
-   <span data-ttu-id="771ae-122">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="771ae-122">Expiration date</span></span>
-   <span data-ttu-id="771ae-123">รหัส PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="771ae-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="771ae-124">None</span><span class="sxs-lookup"><span data-stu-id="771ae-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="771ae-125">การตั้งค่าไซต์สำหรับโมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="771ae-125">Site settings for gift card modules</span></span>

<span data-ttu-id="771ae-126">ในโปรแกรมสร้างไซต์ Commerce ภายใต้ **การตั้งค่าไซต์ \> ส่วนขยาย** จะมีการตั้งค่าโมดูลสำหรับบัตรของขวัญที่เรียกว่า **ชนิดบัตรของขวัญที่สนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="771ae-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="771ae-127">การตั้งค่านี้สนับสนุนค่าสามค่า:</span><span class="sxs-lookup"><span data-stu-id="771ae-127">This setting supports three values:</span></span>
- <span data-ttu-id="771ae-128">**บัตรของขวัญ Dynamics 365** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="771ae-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="771ae-129">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="771ae-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="771ae-130">**บัตรของขวัญ SVS และ Givex** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ SVS และ Givex เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="771ae-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="771ae-131">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อและผู้ใช้ที่ไม่ระบุชื่อในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="771ae-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="771ae-132">**บัตรของขวัญ Dynamics 365, SVS และ Givex** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365, SVS และ Givex</span><span class="sxs-lookup"><span data-stu-id="771ae-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="771ae-133">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="771ae-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="771ae-134">เพิ่มโมดูลบัตรของขวัญไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="771ae-134">Add a gift card module to a page</span></span>

<span data-ttu-id="771ae-135">สำหรับคำแนะนำเกี่ยวกับวิธีการเพิ่มโมดูลบัตรของขวัญลงในหน้าเช็คเอาท์และตั้งค่าคุณสมบัติที่จำเป็น ให้ดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="771ae-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="771ae-136">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="771ae-136">Additional resources</span></span>

[<span data-ttu-id="771ae-137">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="771ae-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="771ae-138">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="771ae-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="771ae-139">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="771ae-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="771ae-140">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="771ae-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="771ae-141">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="771ae-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="771ae-142">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="771ae-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="771ae-143">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="771ae-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="771ae-144">การรองรับบัตรของขวัญภายนอก</span><span class="sxs-lookup"><span data-stu-id="771ae-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
