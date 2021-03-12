---
title: กำหนดส่วนลดเฉพาะช่องทาง
description: ผู้ค้าปลีกมักจะกำหนดส่วนลดที่แตกต่างกันในช่องทางต่างๆ หัวข้อนี้ทบทวนแนวคิดที่คุณจำเป็นต้องทราบเพื่อสร้างส่วนลดสำหรับช่องทางเฉพาะ
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 990c0d0b4b89420094dc86552b3e07717e5c7056
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991401"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="ee719-104">กำหนดส่วนลดเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ee719-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ee719-105">หัวข้อนี้ทบทวนแนวคิดที่คุณจำเป็นต้องทราบเพื่อสร้างส่วนลดสำหรับช่องทางเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ee719-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="ee719-106">ส่วนลดเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ee719-106">Channel-specific discounts</span></span>

<span data-ttu-id="ee719-107">ผู้ค้าปลีกมักจะเสนอส่วนลดที่แตกต่างกันในช่องทางต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ee719-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="ee719-108">สิ่งนี้อาจทำเพื่อจัดการกับสภาพตลาดท้องถิ่นหรือเพื่อจัดการกับผู้ค้าปลีกที่กำลังแข่งขันกันอยู่</span><span class="sxs-lookup"><span data-stu-id="ee719-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="ee719-109">การค้าใช้กลุ่มราคาเพื่อกำหนดส่วนลดเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ee719-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="ee719-110">กลุ่มราคาสามารถถูกกำหนดให้กับอย่างน้อยหนึ่งเอนทิตีต่อไปนี้: ช่องทาง แค็ตตาล็อก สังกัด และโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="ee719-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="ee719-111">บทความนี้กล่าวถึงช่องทาง แต่แนวคิดเดียวกันกับการนำไปใช้ในส่วนลดในแค็ตตาล็อก ส่วนลดสังกัด และส่วนลดสมาชิก</span><span class="sxs-lookup"><span data-stu-id="ee719-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="ee719-112">กลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ee719-112">Price groups</span></span>

<span data-ttu-id="ee719-113">[![กลุ่มราคา](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="ee719-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="ee719-114">แผนภาพด้านบนแสดงความสัมพันธ์ระหว่างเอนทิตี้ที่อาจอยู่ในธุรกรรม (ช่องทาง แค็ตตาล็อก สังกัด ลูกค้า บัตรสมาชิก) และส่วนลดชนิดต่าง ๆ ที่สามารถถูกจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="ee719-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="ee719-115">ธุรกรรมทั้งหมดเกิดขึ้นในช่องทาง ดังนั้นช่องทางจึงถูกรับประกันว่าต้องแสดงอยู่ในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ee719-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="ee719-116">เอนทิตี้ที่เหลือไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ee719-116">The remaining entities are optional.</span></span> <span data-ttu-id="ee719-117">บนแต่ละหน้าข้อมูลหลัก จะมีลิงค์ไปที่หน้ากลุ่มราคาที่เกี่ยวข้องที่คุณสามารถดูและเพิ่มกลุ่มราคาตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ee719-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="ee719-118">กลุ่มราคาจะถูกใช้เพื่อกำหนดความสัมพันธ์เอนทิตี้สี่ชนิดกับส่วนลด การปรับปรุงราคา และข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="ee719-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="ee719-119">เราขอแนะนำว่า คุณวางแผนกลยุทธ์สำหรับวิธีคุณจะตั้งชื่อกลุ่มราคาของคุณเพื่อจัดกลุ่มเหล่านั้นให้เป็นระเบียบ</span><span class="sxs-lookup"><span data-stu-id="ee719-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="ee719-120">ตัวเลือกหนึ่งจะมีการใช้ตัวอักษรหรือหมายเลขนำหน้าหรือคำต่อท้าย เพื่อแยกความแตกต่างระหว่างชนิดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ee719-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="ee719-121">ตัวอย่างเช่น 1-xxxxx สำหรับกลุ่มราคาของช่องทางและ 2-xxxxx สำหรับกลุ่มราคาของแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="ee719-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="ee719-122">มีหน้าการสอบถามสี่หน้าที่มุ่งเน้นไปที่แต่ละเอนทิตีการค้าที่สามารถมีส่วนลดที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="ee719-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="ee719-123">**ช่องทาง กลุ่มราคาช่องทาง** – หน้านี้แสดงรายการช่องทางและส่วนลดที่เชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ee719-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="ee719-124">**กลุ่มราคาของแค็ตตาล็อก** – หน้านี้แสดงรายการของแค็ตตาล็อกและส่วนลดซึ่งเชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ee719-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="ee719-125">**กลุ่มราคาสำหรับสมาชิก** – หน้านี้แสดงรายการของโปรแกรมตอบแทนลูกค้าสมาชิกและส่วนลดซึ่งเชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ee719-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="ee719-126">**กลุ่มราคาของสังกัด** – หน้านี้แสดงรายการของสังกัดและส่วนลดซึ่งเชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ee719-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="ee719-127">ตัวอย่างการตั้งค่าส่วนลดช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ee719-127">Example channel discount set up</span></span>

<span data-ttu-id="ee719-128">ตัวอย่างต่อไปนี้แสดงงานที่เกี่ยวข้องในการตั้งค่าส่วนลดช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ee719-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="ee719-129">สำหรับตัวอย่างนี้ คุณมีช่องทางที่เรียกว่า **Houston** และคุณกำลังจะสร้างส่วนลดใหม่ที่เรียกว่า **Back-to-School**</span><span class="sxs-lookup"><span data-stu-id="ee719-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="ee719-130">เนื่องจากกลยุทธ์การกำหนดราคาและส่วนลดรวมความเป็นไปได้ของส่วนลดช่องทาง คุณสร้างกลุ่มราคาของช่องทางเฉพาะเสมอเมื่อคุณสร้างช่องทางนั้น</span><span class="sxs-lookup"><span data-stu-id="ee719-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="ee719-131">คุณมีกลุ่มราคา **Houston-PG** และกำหนดให้กับช่องทาง **Houston**</span><span class="sxs-lookup"><span data-stu-id="ee719-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="ee719-132">หลังจากที่คุณสร้างส่วนลด **Back-to-School** ใหม่ คุณจำเป็นต้องคลิก **กลุ่มราคา** ในด้านบนของหน้า **ส่วนลด**</span><span class="sxs-lookup"><span data-stu-id="ee719-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="ee719-133">หน้า **กลุ่มราคาส่วนลด** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="ee719-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="ee719-134">ต่อจากนั้น คลิก **New** และเลือกกลุ่มราคา **Houston-PG**</span><span class="sxs-lookup"><span data-stu-id="ee719-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="ee719-135">ขณะนี้ คุณสามารถเปิดใช้งานส่วนลด และผลักไปยังช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ee719-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee719-136">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ee719-136">Additional resources</span></span>

[<span data-ttu-id="ee719-137">การปรับปรุงราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="ee719-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
