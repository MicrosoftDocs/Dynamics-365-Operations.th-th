---
title: โมดูลบัตรของขวัญ
description: หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261593"
---
# <a name="gift-card-module"></a><span data-ttu-id="3eb14-103">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="3eb14-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3eb14-104">หัวข้อนี้ครอบคลุมถึงโมดูลบัตรของขวัญและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3eb14-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3eb14-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="3eb14-105">Overview</span></span>

<span data-ttu-id="3eb14-106">บัตรของขวัญเป็นแบบฟอร์มการชำระเงินทั่วไป และโมดูลของบัตรของขวัญสามารถใช้ในโมดูลการชำระเงินเพื่อรับบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="3eb14-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="3eb14-107">โมดูลบัตรของขวัญสนับสนุนบัตรของขวัญ Dynamics 365, SVS, และ Givex </span><span class="sxs-lookup"><span data-stu-id="3eb14-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="3eb14-108">บัตรของขวัญ SVS และ Givex จะถูกแลกรางวัลผ่านผู้ให้บริการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="3eb14-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="3eb14-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสนับสนุนสำหรับบัตรของขวัญภายนอก เช่น SVS และGivex โปรดดูที่ [การสนับสนุนสำหรับบัตรของขวัญภายนอก](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="3eb14-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

## <a name="module-properties"></a><span data-ttu-id="3eb14-110">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="3eb14-110">Module properties</span></span>

- <span data-ttu-id="3eb14-111">**แสดงฟิลด์เพิ่มเติม** - คุณสมบัตินี้กำหนดว่าควรแสดงฟิลด์ใดสำหรับบัตรของขวัญนอกเหนือจากหมายเลขบัตรของขวัญ ซึ่งจะแสดงตามค่าเริ่มต้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="3eb14-111">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="3eb14-112">ตัวอย่างเช่น บัตรของขวัญบางชิ้นสนับสนุนการแสดงหมายเลขรหัสประจำตัว (PIN) และการสนับสนุนอื่นๆ ที่แสดง PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="3eb14-112">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="3eb14-113">อีกทางหนึ่งคือ คุณสมบัตินี้อาจถูกตั้งค่าเป็น "ไม่มี" ซึ่งจะแสดงหมายเลขบัตรของขวัญเท่านั้นและไม่มีฟิลด์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3eb14-113">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="3eb14-114">ค่าที่สนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="3eb14-114">Supported values:</span></span>
-   <span data-ttu-id="3eb14-115">PIN</span><span class="sxs-lookup"><span data-stu-id="3eb14-115">PIN</span></span>
-   <span data-ttu-id="3eb14-116">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="3eb14-116">Expiration date</span></span>
-   <span data-ttu-id="3eb14-117">รหัส PIN และวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="3eb14-117">PIN and expiration date</span></span> 
-   <span data-ttu-id="3eb14-118">None</span><span class="sxs-lookup"><span data-stu-id="3eb14-118">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="3eb14-119">การตั้งค่าไซต์สำหรับโมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="3eb14-119">Site settings for gift card modules</span></span>

<span data-ttu-id="3eb14-120">ในโปรแกรมสร้างไซต์ Commerce ภายใต้ **การตั้งค่าไซต์ \> ส่วนขยาย** จะมีการตั้งค่าโมดูลสำหรับบัตรของขวัญที่เรียกว่า **ชนิดบัตรของขวัญที่สนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="3eb14-120">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="3eb14-121">การตั้งค่านี้สนับสนุนค่าสามค่า:</span><span class="sxs-lookup"><span data-stu-id="3eb14-121">This setting supports three values:</span></span>
- <span data-ttu-id="3eb14-122">**บัตรของขวัญ Dynamics 365** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eb14-122">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="3eb14-123">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eb14-123">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="3eb14-124">**บัตรของขวัญ SVS และ Givex** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ SVS และ Givex เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eb14-124">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="3eb14-125">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อและผู้ใช้ที่ไม่ระบุชื่อในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="3eb14-125">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="3eb14-126">**บัตรของขวัญ Dynamics 365, SVS และ Givex** - เมื่อมีการใช้การตั้งค่านี้ โมดูลบัตรของขวัญจะอนุญาตให้มีการแลกรางวัลบัตรของขวัญของ Dynamics 365, SVS และ Givex</span><span class="sxs-lookup"><span data-stu-id="3eb14-126">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="3eb14-127">การตั้งค่านี้ได้รับการสนับสนุนสำหรับผู้ใช้ที่ลงชื่อในไซต์อีคอมเมิร์ซเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eb14-127">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="3eb14-128">เพิ่มโมดูลบัตรของขวัญไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="3eb14-128">Add a gift card module to a page</span></span>

<span data-ttu-id="3eb14-129">สำหรับคำแนะนำเกี่ยวกับวิธีการเพิ่มโมดูลบัตรของขวัญลงในหน้าเช็คเอาท์และตั้งค่าคุณสมบัติที่จำเป็น ให้ดูที่ [โมดูลเช็คเอาท์](add-checkout-module.md)</span><span class="sxs-lookup"><span data-stu-id="3eb14-129">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3eb14-130">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3eb14-130">Additional resources</span></span>

[<span data-ttu-id="3eb14-131">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3eb14-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3eb14-132">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="3eb14-132">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3eb14-133">การรองรับบัตรของขวัญภายนอก</span><span class="sxs-lookup"><span data-stu-id="3eb14-133">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
