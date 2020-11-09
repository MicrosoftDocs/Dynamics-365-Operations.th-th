---
title: โมดูลบัตรของขวัญ
description: หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: b7d28e041b8adc828a2447ab09a0c1d28cc2aec0
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022016"
---
# <a name="gift-card-module"></a><span data-ttu-id="7303f-103">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="7303f-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7303f-104">หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7303f-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7303f-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="7303f-105">Overview</span></span>

<span data-ttu-id="7303f-106">โมดูลบัตรของขวัญสามารถใช้ในโมดูลเช็คเอาท์เพื่อรับบัตรของขวัญ ซึ่งเป็นรูปแบบการชำระเงินทั่วไปที่ใช้สำหรับธุรกรรมอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="7303f-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="7303f-107">โมดูลบัตรของขวัญสนับสนุนบัตรของขวัญ Dynamics 365, SVS, และ Givex </span><span class="sxs-lookup"><span data-stu-id="7303f-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="7303f-108">บัตรของขวัญ SVS และ Givex จะถูกแลกรางวัลผ่านผู้ให้บริการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="7303f-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="7303f-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสนับสนุนสำหรับบัตรของขวัญภายนอก เช่น SVS และ Givex โปรดดูที่ [การสนับสนุนบัตรของขวัญภายนอก](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="7303f-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7303f-110">การสนับสนุนสำหรับการแลกบัตรของขวัญ SVS และ Givex ในระหว่างขั้นตอนการชำระเงิน จะพร้อมใช้งานใน Dynamics 365 Commerce รุ่น 10.0.11</span><span class="sxs-lookup"><span data-stu-id="7303f-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="7303f-111">มีโมดูลบัตรของขวัญสองรายการที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="7303f-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="7303f-112">**บัตรของขวัญ** - สำหรับโมดูลนี้สามารถใช้ในหน้าเช็คเอาท์เพื่อแลกบัตรของขวัญเป็นวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7303f-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="7303f-113">**การตรวจสอบยอดคงเหลือในบัตรของขวัญ** โมดูลนี้สามารถใช้ในหน้าใดก็ได้เพื่อตรวจสอบยอดคงเหลือในบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="7303f-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="7303f-114">โมดูลนี้พร้อมใช้งานใน Commerce รีลีส 10.0.14 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="7303f-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="7303f-115">สนับสนุนสำหรับโมดูลการตรวจสอบยอดคงเหลือในบัตรของขวัญ มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.14</span><span class="sxs-lookup"><span data-stu-id="7303f-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="7303f-116">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลบัตรของขวัญบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="7303f-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![ตัวอย่างของโมดูลบัตรของขวัญ](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="7303f-118">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="7303f-118">Module properties</span></span>

- <span data-ttu-id="7303f-119">**แสดงฟิลด์เพิ่มเติม** - คุณสมบัตินี้กำหนดว่าควรแสดงฟิลด์ใดสำหรับบัตรของขวัญนอกเหนือจากหมายเลขบัตรของขวัญ ซึ่งจะแสดงตามค่าเริ่มต้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="7303f-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="7303f-120">ตัวอย่างเช่น บัตรของขวัญบางชิ้นสนับสนุนการแสดงหมายเลขรหัสประจำตัว (PIN) และการสนับสนุนอื่นๆ ที่แสดง PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="7303f-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="7303f-121">อีกทางหนึ่งคือ คุณสมบัตินี้อาจถูกตั้งค่าเป็น "ไม่มี" ซึ่งจะแสดงหมายเลขบัตรของขวัญเท่านั้นและไม่มีฟิลด์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7303f-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="7303f-122">ค่าที่สนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="7303f-122">Supported values:</span></span>
-   <span data-ttu-id="7303f-123">PIN</span><span class="sxs-lookup"><span data-stu-id="7303f-123">PIN</span></span>
-   <span data-ttu-id="7303f-124">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="7303f-124">Expiration date</span></span>
-   <span data-ttu-id="7303f-125">รหัส PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="7303f-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="7303f-126">None</span><span class="sxs-lookup"><span data-stu-id="7303f-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="7303f-127">การตั้งค่าไซต์สำหรับโมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="7303f-127">Site settings for gift card modules</span></span>

<span data-ttu-id="7303f-128">ในโปรแกรมสร้างไซต์ Commerce ภายใต้ **การตั้งค่าไซต์ \> ส่วนขยาย** จะมีการตั้งค่าโมดูลสำหรับบัตรของขวัญที่เรียกว่า **ชนิดบัตรของขวัญที่สนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="7303f-128">In Commerce site builder under **Site Settings \> Extensions** , there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="7303f-129">การตั้งค่านี้สนับสนุนค่าสามค่า:</span><span class="sxs-lookup"><span data-stu-id="7303f-129">This setting supports three values:</span></span>
- <span data-ttu-id="7303f-130">**บัตรของขวัญ Dynamics 365** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7303f-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="7303f-131">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7303f-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="7303f-132">**บัตรของขวัญ SVS และ Givex** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ SVS และ Givex เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7303f-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="7303f-133">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อและผู้ใช้ที่ไม่ระบุชื่อในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="7303f-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="7303f-134">**บัตรของขวัญ Dynamics 365, SVS และ Givex** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365, SVS และ Givex</span><span class="sxs-lookup"><span data-stu-id="7303f-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="7303f-135">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7303f-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7303f-136">การตั้งค่าเหล่านี้มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.11 และจำเป็นต้องใช้เฉพาะเมื่อคุณต้องการการสนับสนุนสำหรับบัตรของขวัญ SVS หรือ Givex เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7303f-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="7303f-137">ถ้าคุณกำลังอัพปเดตจากเวอร์ชันที่เก่ากว่าของ Dynamics 365 Commerce คุณต้องอัปเดตไฟล์ appsettings.json ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="7303f-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="7303f-138">สำหรับคำแนะนำเกี่ยวกับการอัปเดตไฟล์ appsettings.json ให้ดูที่ [อัปเดต SDK และไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)</span><span class="sxs-lookup"><span data-stu-id="7303f-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="7303f-139">เพิ่มโมดูลบัตรของขวัญไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="7303f-139">Add a gift card module to a page</span></span>

<span data-ttu-id="7303f-140">สำหรับคำแนะนำเกี่ยวกับวิธีการเพิ่มโมดูลบัตรของขวัญลงในหน้าเช็คเอาท์และตั้งค่าคุณสมบัติที่จำเป็น ให้ดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="7303f-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7303f-141">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7303f-141">Additional resources</span></span>

[<span data-ttu-id="7303f-142">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="7303f-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7303f-143">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="7303f-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7303f-144">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="7303f-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7303f-145">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7303f-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7303f-146">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7303f-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7303f-147">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7303f-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="7303f-148">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7303f-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7303f-149">การรองรับบัตรของขวัญภายนอก</span><span class="sxs-lookup"><span data-stu-id="7303f-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="7303f-150">การอัปเดต SDK และไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="7303f-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
