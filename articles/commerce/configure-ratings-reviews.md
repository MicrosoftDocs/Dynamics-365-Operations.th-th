---
title: ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าไซต์อีคอมเมิร์ซเพื่อแสดงการให้คะแนนและบทวิจารณ์ของลูกค้าใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416031"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="74fa4-103">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="74fa4-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74fa4-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าไซต์อีคอมเมิร์ซเพื่อแสดงการให้คะแนนและบทวิจารณ์ของลูกค้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="74fa4-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74fa4-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="74fa4-105">Overview</span></span>

<span data-ttu-id="74fa4-106">การให้คะแนนและบทวิจารณ์บนเว็บไซต์อีคอมเมิร์ซช่วยให้ลูกค้าเรียนรู้เกี่ยวกับผลิตภัณฑ์ก่อนที่พวกเขาทำการตัดสินใจซื้อ โดยแสดงให้พวกเขาเห็นว่าลูกค้าคนอื่นคิดอะไรเกี่ยวกับผลิตภัณฑ์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="74fa4-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="74fa4-107">สำหรับเว็บไซต์อีคอมเมิร์ซ การให้คะแนนและบทวิจารณ์ยังเป็นกลไกสำหรับการรวบรวมความคิดเห็นของลูกค้าเกี่ยวกับผลิตภัณฑ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="74fa4-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="74fa4-108">ตั้งค่าไซต์เพื่อการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="74fa4-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="74fa4-109">การตั้งค่าค่าสำหรับการให้คะแนนและบทวิจารณ์ เช่น รหัสผู้เช่า ความยาวของข้อความบทวิจารณ์ และความยาวของชื่อบทวิจารณ์ จะตั้งค่าในระดับไซต์</span><span class="sxs-lookup"><span data-stu-id="74fa4-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="74fa4-110">เมื่อต้องการตั้งค่าไซต์เพื่อแสดงการให้คะแนนและบทวิจารณ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="74fa4-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="74fa4-111">ไปที่ **หน้าหลัก \> ไซต์**</span><span class="sxs-lookup"><span data-stu-id="74fa4-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="74fa4-112">เลือกชื่อไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="74fa4-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="74fa4-113">ไปที่ **การตั้งค่าไซต์\> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="74fa4-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="74fa4-114">ในฟิลด์ **ความยาวสูงสุดของข้อความบทวิจารณ์** ให้ป้อนจำนวนสูงสุดของอักขระที่ข้อความบทวิจารณ์จะมีได้ (ตัวอย่างเช่น **1000**)</span><span class="sxs-lookup"><span data-stu-id="74fa4-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="74fa4-115">ในฟิลด์ **ความยาวสูงสุดของชื่อบทวิจารณ์** ให้ป้อนจำนวนสูงสุดของอักขระที่ชื่อบทวิจารณ์จะมีได้ (ตัวอย่างเช่น **55**)</span><span class="sxs-lookup"><span data-stu-id="74fa4-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="74fa4-116">เลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="74fa4-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="74fa4-117">ภาพประกอบต่อไปนี้แสดงว่าการตั้งค่าเป็นอย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="74fa4-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![การตั้งค่าไซต์เพื่อแสดงการให้คะแนนและบทวิจารณ์](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="74fa4-119">เชื่อมโยงการให้คะแนนผลิตภัณฑ์ไปยังส่วนบทวิจารณ์ของ PDP</span><span class="sxs-lookup"><span data-stu-id="74fa4-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="74fa4-120">การให้คะแนนผลิตภัณฑ์จะแสดงอยู่ด้านล่างของชื่อผลิตภัณฑ์ที่ด้านบนของ PDP</span><span class="sxs-lookup"><span data-stu-id="74fa4-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="74fa4-121">การให้คะแนนผลิตภัณฑ์สามารถตั้งค่าได้เพื่อให้เชื่อมโยงไปยังส่วน **บทวิจารณ์** ของ PDP เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="74fa4-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="74fa4-122">เมื่อต้องการเชื่อมโยงการให้คะแนนผลิตภัณฑ์ไปยังส่วน **บทวิจารณ์** ของ PDP ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="74fa4-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="74fa4-123">เปิดเท็มเพลต PDP</span><span class="sxs-lookup"><span data-stu-id="74fa4-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="74fa4-124">ไปที่ **การตั้งค่าโมดูลคอนเทนเนอร์กล่องการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="74fa4-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="74fa4-125">ภายใต้ **กล่องการซื้อ** ให้เลือก **การให้คะแนนผลิตภัณฑ์** จากนั้นเลือกกล่องการเครื่องหมาย **เชื่อมโยงการคลิกกับโมดูลบทวิจารณ์แบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="74fa4-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="74fa4-126">ภาพประกอบต่อไปนี้แสดงว่าการตั้งค่าเป็นอย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="74fa4-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![เชื่อมโยงการให้คะแนนผลิตภัณฑ์ไปยังส่วนบทวิจารณ์ของ PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="74fa4-128">ตั้งค่าลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย</span><span class="sxs-lookup"><span data-stu-id="74fa4-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="74fa4-129">เมื่อต้องการตั้งค่าลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="74fa4-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="74fa4-130">ไปที่ **หน้าหลัก \> ไซต์**</span><span class="sxs-lookup"><span data-stu-id="74fa4-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="74fa4-131">เลือกชื่อไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="74fa4-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="74fa4-132">ไปที่ **การตั้งค่าไซต์\> ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="74fa4-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="74fa4-133">บนแท็บ **เส้นทาง** ภายใต้ **ความเป็นส่วนตัวและนโยบาย RNR** ให้เลือก **เพิ่มลิงก์**</span><span class="sxs-lookup"><span data-stu-id="74fa4-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="74fa4-134">ถ้าลิงก์ลิงก์หนึ่งถูกป้อนไว้แล้ว และคุณต้องการแทนที่ ให้เลือกลิงก์นั้น</span><span class="sxs-lookup"><span data-stu-id="74fa4-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="74fa4-135">ในกล่องโต้ตอบ **เพิ่มลิงก์** ให้เลือกลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="74fa4-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="74fa4-136">เลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="74fa4-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="74fa4-137">ภาพประกอบต่อไปนี้แสดงว่าการตั้งค่าเป็นอย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="74fa4-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![การตั้งค่าลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="74fa4-139">ตั้งค่าคอนฟิกโมดูลการจัดอันดับและบทวิจารณ์บนหน้ารายละเอียดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="74fa4-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="74fa4-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าคอนฟิกโมดูลการจัดอันดับและบทวิจารณ์บนหน้ารายละเอียดของผลิตภัณฑ์ โปรดดูที่ [โมดูลการจัดอันดับและบทวิจารณ์](ratings-reviews-modules.md)</span><span class="sxs-lookup"><span data-stu-id="74fa4-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74fa4-141">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="74fa4-141">Additional resources</span></span>

[<span data-ttu-id="74fa4-142">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="74fa4-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="74fa4-143">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="74fa4-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="74fa4-144">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="74fa4-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="74fa4-145">ตั้งค่าคอนฟิกโมดูลการจัดอันดับและบทวิจารณ์บนหน้ารายละเอียดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="74fa4-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="74fa4-146">ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="74fa4-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
