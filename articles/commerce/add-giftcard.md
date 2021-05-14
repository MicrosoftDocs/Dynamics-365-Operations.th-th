---
title: โมดูลบัตรของขวัญ
description: หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962774"
---
# <a name="gift-card-module"></a><span data-ttu-id="fdbd2-103">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fdbd2-104">หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fdbd2-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fdbd2-105">โมดูลบัตรของขวัญสามารถใช้ในโมดูลเช็คเอาท์เพื่อรับบัตรของขวัญ ซึ่งเป็นรูปแบบการชำระเงินทั่วไปที่ใช้สำหรับธุรกรรมอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="fdbd2-106">โมดูลบัตรของขวัญสนับสนุนบัตรของขวัญ Dynamics 365, SVS, และ Givex </span><span class="sxs-lookup"><span data-stu-id="fdbd2-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="fdbd2-107">บัตรของขวัญ SVS และ Givex จะถูกแลกรางวัลผ่านผู้ให้บริการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="fdbd2-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="fdbd2-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสนับสนุนสำหรับบัตรของขวัญภายนอก เช่น SVS และ Givex โปรดดูที่ [การสนับสนุนบัตรของขวัญภายนอก](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="fdbd2-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fdbd2-109">การสนับสนุนสำหรับการแลกบัตรของขวัญ SVS และ Givex ในระหว่างขั้นตอนการชำระเงิน จะพร้อมใช้งานใน Dynamics 365 Commerce รุ่น 10.0.11</span><span class="sxs-lookup"><span data-stu-id="fdbd2-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="fdbd2-110">มีโมดูลบัตรของขวัญสองรายการที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="fdbd2-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="fdbd2-111">**บัตรของขวัญ** – สำหรับโมดูลนี้สามารถใช้ในหน้าเช็คเอาท์เพื่อแลกบัตรของขวัญเป็นวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="fdbd2-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="fdbd2-112">**การตรวจสอบยอดคงเหลือในบัตรของขวัญ** – โมดูลนี้สามารถใช้ในหน้าใดก็ได้เพื่อตรวจสอบยอดคงเหลือในบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="fdbd2-113">โมดูลนี้พร้อมใช้งานใน Commerce รีลีส 10.0.14 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="fdbd2-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="fdbd2-114">สนับสนุนสำหรับโมดูลการตรวจสอบยอดคงเหลือในบัตรของขวัญ มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.14</span><span class="sxs-lookup"><span data-stu-id="fdbd2-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="fdbd2-115">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลบัตรของขวัญบนหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="fdbd2-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![ตัวอย่างของโมดูลบัตรของขวัญ](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="fdbd2-117">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="fdbd2-117">Module properties</span></span>

- <span data-ttu-id="fdbd2-118">**แสดงฟิลด์เพิ่มเติม** – คุณสมบัตินี้กำหนดว่าควรแสดงฟิลด์ใดสำหรับบัตรของขวัญนอกเหนือจากหมายเลขบัตรของขวัญ ซึ่งจะแสดงตามค่าเริ่มต้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="fdbd2-119">ตัวอย่างเช่น บัตรของขวัญบางชิ้นสนับสนุนการแสดงหมายเลขรหัสประจำตัว (PIN) และการสนับสนุนอื่นๆ ที่แสดง PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="fdbd2-120">อีกทางหนึ่งคือ คุณสมบัตินี้อาจถูกตั้งค่าเป็น "ไม่มี" ซึ่งจะแสดงหมายเลขบัตรของขวัญเท่านั้นและไม่มีฟิลด์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fdbd2-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="fdbd2-121">ค่าที่สนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="fdbd2-121">Supported values:</span></span>
-   <span data-ttu-id="fdbd2-122">PIN</span><span class="sxs-lookup"><span data-stu-id="fdbd2-122">PIN</span></span>
-   <span data-ttu-id="fdbd2-123">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-123">Expiration date</span></span>
-   <span data-ttu-id="fdbd2-124">รหัส PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="fdbd2-125">None</span><span class="sxs-lookup"><span data-stu-id="fdbd2-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="fdbd2-126">การตั้งค่าไซต์สำหรับโมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-126">Site settings for gift card modules</span></span>

<span data-ttu-id="fdbd2-127">ในโปรแกรมสร้างไซต์ Commerce ภายใต้ **การตั้งค่าไซต์ \> ส่วนขยาย** จะมีการตั้งค่าโมดูลสำหรับบัตรของขวัญที่เรียกว่า **ชนิดบัตรของขวัญที่สนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="fdbd2-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="fdbd2-128">การตั้งค่านี้สนับสนุนค่าสามค่า:</span><span class="sxs-lookup"><span data-stu-id="fdbd2-128">This setting supports three values:</span></span>
- <span data-ttu-id="fdbd2-129">**บัตรของขวัญ Dynamics 365** – เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="fdbd2-130">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="fdbd2-131">**บัตรของขวัญ SVS และ Givex** – เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ SVS และ Givex เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="fdbd2-132">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อและผู้ใช้ที่ไม่ระบุชื่อในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="fdbd2-133">**บัตรของขวัญ Dynamics 365, SVS และ Givex** – เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365, SVS และ Givex</span><span class="sxs-lookup"><span data-stu-id="fdbd2-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="fdbd2-134">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fdbd2-135">การตั้งค่าเหล่านี้มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.11 และจำเป็นต้องใช้เฉพาะเมื่อคุณต้องการการสนับสนุนสำหรับบัตรของขวัญ SVS หรือ Givex เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="fdbd2-136">ถ้าคุณกำลังอัพปเดตจากเวอร์ชันที่เก่ากว่าของ Dynamics 365 Commerce คุณต้องอัปเดตไฟล์ appsettings.json ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="fdbd2-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="fdbd2-137">สำหรับคำแนะนำเกี่ยวกับการอัปเดตไฟล์ appsettings.json ให้ดูที่ [อัปเดต SDK และไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)</span><span class="sxs-lookup"><span data-stu-id="fdbd2-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="fdbd2-138">ขยายบัตรของขวัญภายในเพื่อใช้งานในร้านค้า e-commerce</span><span class="sxs-lookup"><span data-stu-id="fdbd2-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="fdbd2-139">ตามค่าเริ่มต้น บัตรของขวัญภายในจะไม่เหมาะที่จะใช้ในร้านค้า e-commerce</span><span class="sxs-lookup"><span data-stu-id="fdbd2-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="fdbd2-140">ดังนั้น ก่อนที่คุณจะอนุญาตให้ใช้บัตรของขวัญภายในเพื่อการจ่ายเงิน คุณควรตั้งค่าคอนฟิกบัตรของขวัญด้วยส่วนขยายที่ช่วยให้บัตรของขวัญปลอดภัยยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="fdbd2-141">ต่อไปนี้เป็นพื้นที่บัตรของขวัญที่คุณควรขยายก่อนที่คุณจะอนุญาตให้ใช้บัตรของขวัญภายในในการผลิต:</span><span class="sxs-lookup"><span data-stu-id="fdbd2-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="fdbd2-142">**หมายเลขบัตรของขวัญ** – ใช้ลำดับหมายเลขเพื่อสร้างหมายเลขบัตรของขวัญบัตรของขวัญภายใน</span><span class="sxs-lookup"><span data-stu-id="fdbd2-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="fdbd2-143">เนื่องจากลำดับหมายเลขสามารถคาดเดาได้อย่างง่ายดาย คุณจึงควรขยายการสร้างหมายเลขบัตรของขวัญเพื่อสุ่ม สตริงที่ปลอดภัยตามการเข้ารหัสลับจะใช้กับหมายเลขบัตรของขวัญที่ออกให้</span><span class="sxs-lookup"><span data-stu-id="fdbd2-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="fdbd2-144">**GetBalance** – API ของ **GetBalance** ใช้ค้นหายอดดุลของบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="fdbd2-145">ตามค่าเริ่มต้น API สาธารณะนี้</span><span class="sxs-lookup"><span data-stu-id="fdbd2-145">By default, this API public.</span></span> <span data-ttu-id="fdbd2-146">ถ้าไม่ต้องระบุ PIN เพื่อค้นหายอดดุลบัตรของขวัญ เสี่ยงต่อการถูกโจมตีจากบังคับ อาจใช้ API **GetBalance** เพื่อลองค้นหาหมายเลขบัตรของขวัญที่มียอดดุล</span><span class="sxs-lookup"><span data-stu-id="fdbd2-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="fdbd2-147">ด้วยการดําเนินการทั้งข้อต้องระบุ PIN ของบัตรของขวัญภายใน และ API throttling คุณสามารถช่วยป้องกันความเสี่ยงได้</span><span class="sxs-lookup"><span data-stu-id="fdbd2-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="fdbd2-148">**PIN** – ตามค่าเริ่มต้น บัตรของขวัญภายในจะไม่สนับสนุน PIN</span><span class="sxs-lookup"><span data-stu-id="fdbd2-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="fdbd2-149">คุณควรขยายบัตรของขวัญภายใน เพื่อให้ต้องใช้ PIN ค้นหายอดดุล</span><span class="sxs-lookup"><span data-stu-id="fdbd2-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="fdbd2-150">ฟังก์ชันนี้ยังสามารถใช้เพื่อล็อคบัตรของขวัญหลังจากความพยายามที่ไม่ถูกต้องที่ต่อเนื่องกัน ในการป้อน PIN</span><span class="sxs-lookup"><span data-stu-id="fdbd2-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="fdbd2-151">เปิดใช้งานการเช็คเอาท์ด้วยบัตรของขวัญ เพื่อการชำระเงินของผู้เยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="fdbd2-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="fdbd2-152">ตามค่าเริ่มต้น การชำระเงินด้วยบัตรของขวัญจะไม่เปิดใช้งาน เมื่อเช็คเอาท์เป็นผู้เยื่ยมชม (ไม่ระบุชื่อ)</span><span class="sxs-lookup"><span data-stu-id="fdbd2-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="fdbd2-153">ในการเปิดใช้งาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="fdbd2-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="fdbd2-154">ในศูนย์ควบคุม Commerce ไปที่ **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> POS \> การดำเนินงาน POS**</span><span class="sxs-lookup"><span data-stu-id="fdbd2-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="fdbd2-155">เลือกและระงับ (หรือคลิกขวา) ส่วนหัวของกริด แล้วเลือก **แทรกคอลัมน์**</span><span class="sxs-lookup"><span data-stu-id="fdbd2-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="fdbd2-156">ในกล่องโต้ตอบ **แทรกคอลัมน์** ให้เลือกกล่องกาเครื่องหมาย **AllowAnonymousAccess**</span><span class="sxs-lookup"><span data-stu-id="fdbd2-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="fdbd2-157">เลือก **ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="fdbd2-157">Select **Update**.</span></span>
1. <span data-ttu-id="fdbd2-158">หากต้องการดําเนินงาน **520** (ยอดคงเหลือในบัตรของขวัญ) และ **214** ให้ตั้งค่า **AllowAnonymousAccess** เป็น **1**</span><span class="sxs-lookup"><span data-stu-id="fdbd2-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="fdbd2-159">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fdbd2-159">Select **Save**.</span></span>
1. <span data-ttu-id="fdbd2-160">รันงานของตัวกำหนดตารางทำงาน **1090** เพื่อซิงค์การเปลี่ยนแปลงไปยังฐานข้อมูลช่องทาง</span><span class="sxs-lookup"><span data-stu-id="fdbd2-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="fdbd2-161">เพิ่มโมดูลบัตรของขวัญไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="fdbd2-161">Add a gift card module to a page</span></span>

<span data-ttu-id="fdbd2-162">สำหรับคำแนะนำเกี่ยวกับวิธีการเพิ่มโมดูลบัตรของขวัญลงในหน้าเช็คเอาท์และตั้งค่าคุณสมบัติที่จำเป็น ให้ดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="fdbd2-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdbd2-163">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fdbd2-163">Additional resources</span></span>

[<span data-ttu-id="fdbd2-164">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fdbd2-165">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="fdbd2-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fdbd2-166">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="fdbd2-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fdbd2-167">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="fdbd2-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fdbd2-168">โมดูลที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fdbd2-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fdbd2-169">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fdbd2-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fdbd2-170">โมดูลข้อมูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="fdbd2-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="fdbd2-171">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="fdbd2-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fdbd2-172">การรองรับบัตรของขวัญภายนอก</span><span class="sxs-lookup"><span data-stu-id="fdbd2-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="fdbd2-173">การอัปเดต SDK และไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="fdbd2-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
