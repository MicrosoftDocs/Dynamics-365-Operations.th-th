---
title: "กำหนดส่วนลดเฉพาะช่องทาง"
description: "ผู้ค้าปลีกมักจะกำหนดส่วนลดที่แตกต่างกันในช่องทางต่างๆ หัวข้อนี้ทบทวนแนวคิดที่คุณจำเป็นต้องทราบเพื่อสร้างส่วนลดสำหรับช่องทางเฉพาะ"
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0300ed4a10f6979fb673447323f7fdf61041529f
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="ff806-104">กำหนดส่วนลดเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ff806-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff806-105">ผู้ค้าปลีกมักจะกำหนดส่วนลดที่แตกต่างกันในช่องทางต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ff806-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="ff806-106">หัวข้อนี้ทบทวนแนวคิดที่คุณจำเป็นต้องทราบเพื่อสร้างส่วนลดสำหรับช่องทางเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ff806-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span> 

<a name="channel-specific-discounts"></a><span data-ttu-id="ff806-107">ส่วนลดเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ff806-107">Channel-specific discounts</span></span>
--------------------------

<span data-ttu-id="ff806-108">ผู้ค้าปลีกมักจะเสนอส่วนลดที่แตกต่างกันในช่องทางต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ff806-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="ff806-109">นี่อาจสามารถทำได้เพื่อกำหนดเงื่อนไขของตลาดท้องถิ่น หรือ เพื่อจัดการกับผู้ค้าปลีกคู่แข่ง</span><span class="sxs-lookup"><span data-stu-id="ff806-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="ff806-110">Microsoft Dynamics 365 for Retail ใช้กลุ่มราคาเพื่อกำหนดส่วนลดเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ff806-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="ff806-111">กลุ่มราคาสามารถถูกกำหนดให้กับอย่างน้อยหนึ่งเอนทิตีต่อไปนี้: ช่องทาง แค็ตตาล็อก สังกัด และโปรแกรมตอบแทนลูกค้าสมาชิก</span><span class="sxs-lookup"><span data-stu-id="ff806-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="ff806-112">บทความนี้กล่าวถึงช่องทาง แต่แนวคิดเดียวกันกับการนำไปใช้ในส่วนลดในแค็ตตาล็อก ส่วนลดสังกัด และส่วนลดสมาชิก</span><span class="sxs-lookup"><span data-stu-id="ff806-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="ff806-113">กลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ff806-113">Price groups</span></span>

<span data-ttu-id="ff806-114">[![กลุ่มราคา](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="ff806-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="ff806-115">แผนภาพด้านบนแสดงความสัมพันธ์ระหว่างเอนทิตี้ที่อาจอยู่ในธุรกรรม (ช่องทาง แค็ตตาล็อก สังกัด ลูกค้า บัตรสมาชิก) และส่วนลดชนิดต่าง ๆ ที่สามารถถูกจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="ff806-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="ff806-116">ธุรกรรมทั้งหมดเกิดขึ้นในช่องทาง ดังนั้นช่องทางจึงถูกรับประกันว่าต้องแสดงอยู่ในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ff806-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="ff806-117">เอนทิตี้ที่เหลือไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ff806-117">The remaining entities are optional.</span></span> <span data-ttu-id="ff806-118">บนแต่ละหน้าข้อมูลหลัก จะมีลิงค์ไปที่หน้ากลุ่มราคาที่เกี่ยวข้องที่คุณสามารถดูและเพิ่มกลุ่มราคาตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ff806-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="ff806-119">กลุ่มราคาจะถูกใช้เพื่อกำหนดความสัมพันธ์เอนทิตี้สี่ชนิดกับส่วนลด การปรับปรุงราคา และข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="ff806-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="ff806-120">เราขอแนะนำว่า คุณวางแผนกลยุทธ์สำหรับวิธีคุณจะตั้งชื่อกลุ่มราคาของคุณเพื่อจัดกลุ่มเหล่านั้นให้เป็นระเบียบ</span><span class="sxs-lookup"><span data-stu-id="ff806-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="ff806-121">ตัวเลือกหนึ่งจะมีการใช้ตัวอักษรหรือหมายเลขนำหน้าหรือคำต่อท้าย เพื่อแยกความแตกต่างระหว่างชนิดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ff806-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="ff806-122">ตัวอย่างเช่น 1-xxxxx สำหรับกลุ่มราคาของช่องทางและ 2-xxxxx สำหรับกลุ่มราคาของแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="ff806-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="ff806-123">มีอยู่สี่หน้าการสอบถามที่โฟกัสแต่ละเอนทิตี้การขายปลีกที่สามารถมีส่วนลดที่เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="ff806-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

-   <span data-ttu-id="ff806-124">**กลุ่มราคาของช่องทางการขายปลีก** - หน้านี้แสดงรายการของช่องทางและส่วนลดซึ่งเชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ff806-124">**Retail channel price groups** - This page shows a list of channels and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="ff806-125">**กลุ่มราคาของแค็ตตาล็อก**- หน้านี้แสดงรายการของแค็ตตาล็อกและส่วนลดซึ่งเชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ff806-125">**Catalog price groups** - This page shows a list of catalogs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="ff806-126">**กลุ่มราคาสำหรับสมาชิก**- หน้านี้แสดงรายการโปรแกรมตอบแทนลูกค้าสมาชิกและส่วนลดซึ่งเชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ff806-126">**Loyalty price groups** - This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="ff806-127">**กลุ่มราคาของสังกัด**- หน้านี้แสดงรายการของสังกัดและส่วนลดซึ่งเชื่อมโยงกันสำหรับแต่ละกลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="ff806-127">**Affiliation price groups** - This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="ff806-128">ตัวอย่างการตั้งค่าส่วนลดช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ff806-128">Example channel discount set up</span></span>
<span data-ttu-id="ff806-129">ตัวอย่างต่อไปนี้แสดงงานที่เกี่ยวข้องในการตั้งค่าส่วนลดช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ff806-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1.  <span data-ttu-id="ff806-130">ตัวอย่างนี้ คุณมีช่องทางเรียกว่า **Houston** และคุณกำลังจะสร้างส่วนลดใหม่ที่เรียกว่า **Back-to-School**</span><span class="sxs-lookup"><span data-stu-id="ff806-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School.**</span></span>
2.  <span data-ttu-id="ff806-131">เนื่องจากกลยุทธ์การกำหนดราคาและส่วนลดรวมความเป็นไปได้ของส่วนลดช่องทาง คุณสร้างกลุ่มราคาของช่องทางเฉพาะเสมอเมื่อคุณสร้างช่องทางนั้น</span><span class="sxs-lookup"><span data-stu-id="ff806-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3.  <span data-ttu-id="ff806-132">คุณมีกลุ่มราคา **Houston-PG** และกำหนดให้กับช่องทาง **Houston**</span><span class="sxs-lookup"><span data-stu-id="ff806-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4.  <span data-ttu-id="ff806-133">หลังจากที่คุณสร้างส่วนลด **Back-to-School** ใหม่ คุณจำเป็นต้องคลิก **กลุ่มราคา** ในด้านบนของหน้า **ส่วนลด**</span><span class="sxs-lookup"><span data-stu-id="ff806-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="ff806-134">หน้า **กลุ่มราคาส่วนลด** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="ff806-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="ff806-135">ต่อจากนั้น คลิก **New** และเลือกกลุ่มราคา **Houston-PG**</span><span class="sxs-lookup"><span data-stu-id="ff806-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5.  <span data-ttu-id="ff806-136">ขณะนี้ คุณสามารถเปิดใช้งานส่วนลด และผลักไปยังช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ff806-136">Now you can enable the discount and push it to the channel.</span></span>



<a name="additional-resources"></a><span data-ttu-id="ff806-137">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ff806-137">Additional resources</span></span>
--------

[<span data-ttu-id="ff806-138">การปรับปรุงราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="ff806-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)




