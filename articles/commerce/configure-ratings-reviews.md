---
title: ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าไซต์อีคอมเมิร์ซเพื่อแสดงการให้คะแนนและบทวิจารณ์ของลูกค้าใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770492"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="0b032-103">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0b032-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าไซต์อีคอมเมิร์ซเพื่อแสดงการให้คะแนนและบทวิจารณ์ของลูกค้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0b032-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0b032-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="0b032-105">Overview</span></span>

<span data-ttu-id="0b032-106">การให้คะแนนและบทวิจารณ์บนเว็บไซต์อีคอมเมิร์ซช่วยให้ลูกค้าเรียนรู้เกี่ยวกับผลิตภัณฑ์ก่อนที่พวกเขาจะมีการตัดสินใจซื้อ โดยแสดงให้ลูกค้าเห็นว่าลูกค้าคนอื่นคิดอะไรเกี่ยวกับผลิตภัณฑ์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="0b032-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="0b032-107">สำหรับเว็บไซต์อีคอมเมิร์ซ การให้คะแนนและบทวิจารณ์ยังเป็นกลไกสำหรับการรวบรวมความคิดเห็นของลูกค้าเกี่ยวกับผลิตภัณฑ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="0b032-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="0b032-108">การให้คะแนนแสดงอยู่บนหน้ารายการผลิตภัณฑ์ หน้ารายการประเภท หน้าผลการค้นหา และหน้าไซต์อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="0b032-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="0b032-109">กราฟแสดงค่าสถิติความถี่ของการให้คะแนนและบทวิจารณ์ผลิตภัณฑ์จะแสดงอยู่บนหน้ารายละเอียดผลิตภัณฑ์ (PDP)</span><span class="sxs-lookup"><span data-stu-id="0b032-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="0b032-110">ปุ่ม **เขียนบทวิจารณ์** ช่วยให้ลูกค้าส่งการให้คะแนนและบทวิจารณ์สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0b032-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="0b032-111">โมดูลการให้คะแนนและบทวิจารณ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="0b032-112">สามโมดูลจะแสดงนสรุปการให้คะแนนและบทวิจารณ์บน PDP:</span><span class="sxs-lookup"><span data-stu-id="0b032-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="0b032-113">โมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-113">Write review module</span></span>
- <span data-ttu-id="0b032-114">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0b032-114">Product reviews list module</span></span>
- <span data-ttu-id="0b032-115">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="0b032-115">Ratings histogram module</span></span>
 
<span data-ttu-id="0b032-116">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าโมดูลการให้คะแนนและบทวิจารณ์มีลักษณะอย่างไรบน PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![โมดูลการให้คะแนนและบทวิจารณ์บน PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="0b032-118">สำหรับข้อมูลเกี่ยวกับวิธีการทำเท็มเพลตและเค้าโครง PDP ให้เหมาะสม เพื่อให้คุณสามารถใช้การตั้งค่าสำหรับโมดูลการให้คะแนนและบทวิจารณ์ร่วมกันระหว่างหลาย PDP บนไซต์อีคอมเมิร์ซของคุณ โปรดดูที่ [ภาพรวมเท็มเพลตและเค้าโครง](templates-layouts-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0b032-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="0b032-119">ภาพประกอบต่อไปนี้แสดงว่ากล่องโต้ตอบ **เพิ่มโมดูล** แสดงโมดูลการให้คะแนนและบทวิจารณ์อย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0b032-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![กล่องโต้ตอบของการเพิ่มโมดูล](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="0b032-121">โมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-121">Write review module</span></span>

<span data-ttu-id="0b032-122">โมดูลการเขียนบทวิจารณ์จะมีปุ่ม **เขียนบทวิจารณ์** ที่ช่วยให้ผู้ใช้ลงชื่อเข้าใช้ กำหนดการให้คะแนน และเขียนบทวิจารณ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0b032-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="0b032-123">โมดูลนี้ยังช่วยให้ผู้ใช้แก้ไขการให้คะแนนหรือบทวิจารณ์ที่พวกเขาได้ส่งก่อนหน้านี้ได้</span><span class="sxs-lookup"><span data-stu-id="0b032-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="0b032-124">โดยทั่วไปแล้ว โมดูลจะปรากฏขึ้นด้านบนของโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนและโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="0b032-125">ภาพประกอบต่อไปนี้แสดงกล่องตอบโต้ **เขียนบทวิจารณ์** ที่ปรากฏขึ้นเมื่อลูกค้าเลือก **เขียนบทวิจารณ์**</span><span class="sxs-lookup"><span data-stu-id="0b032-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="0b032-126">ลูกค้าสามารถใช้กล่องโต้ตอบนี้เพื่อส่งการให้คะแนนและบทวิจารณ์ได้</span><span class="sxs-lookup"><span data-stu-id="0b032-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![กล่องโต้ตอบการเขียนบทวิจารณ์](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="0b032-128">ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลการเขียนบทวิจารณ์ที่จำเป็นต้องตั้งค่าในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="0b032-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0b032-129">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0b032-129">Property name</span></span> | <span data-ttu-id="0b032-130">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="0b032-130">Value</span></span>        | <span data-ttu-id="0b032-131">คำอธิบายคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0b032-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="0b032-132">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="0b032-132">Name</span></span>          | <span data-ttu-id="0b032-133">การเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-133">Write review</span></span> | <span data-ttu-id="0b032-134">ชื่อของโมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="0b032-135">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="0b032-135">Ratings histogram module</span></span>

<span data-ttu-id="0b032-136">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนแสดงกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="0b032-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="0b032-137">โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นระหว่างโมดูลการเขียนบทวิจารณ์และโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="0b032-138">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนไม่ต้องมีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="0b032-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="0b032-139">คุณเพียงแค่ต้องเพิ่มโมดูลในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="0b032-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="0b032-140">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าเท็มเพลต PDP ใน Dynamics 365 Commerce จะมีลักษณะอย่างไรโมดูลต่าง ๆ การให้คะแนนและบทวิจารณ์มีการตั้งค่าสำหรับแสดงบน PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![เท็มเพลต PDP เมื่อการให้คะแนนและบทวิจารณ์มีการตั้งค่าสำหรับการแสดงผลบน PDP](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="0b032-142">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0b032-142">Product reviews list module</span></span>

<span data-ttu-id="0b032-143">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์แสดงรายการของบทวิจารณ์ผลิตภัณฑ์พร้อมด้วยตัวเลือกการเรียงลำดับ การกรองข้อมูล และการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="0b032-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="0b032-144">โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นหลังจากโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนบน PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="0b032-145">ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ที่จำเป็นต้องตั้งค่าในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="0b032-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0b032-146">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0b032-146">Property name</span></span>              | <span data-ttu-id="0b032-147">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="0b032-147">Value</span></span> | <span data-ttu-id="0b032-148">คำอธิบายคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0b032-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="0b032-149">บทวิจารณ์ที่แสดงในแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="0b032-149">Reviews shown on each page</span></span> | <span data-ttu-id="0b032-150">10</span><span class="sxs-lookup"><span data-stu-id="0b032-150">10</span></span>    | <span data-ttu-id="0b032-151">จำนวนบทวิจารณ์ที่ควรจะแสดงออกมาในแต่ละครั้งบน PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="0b032-152">ปุ่ม **ถัดไป** และ **ก่อนหน้า** จะมีอยู่ เพื่อให้ผู้ใช้สามารถย้ายไปยังหน้าต่าง ๆ ของบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="0b032-153">กราฟแสดงค่าสถิติความถี่ของการให้คะแนน - มุมมองสรุป</span><span class="sxs-lookup"><span data-stu-id="0b032-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="0b032-154">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์มีช่องที่คุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนได้</span><span class="sxs-lookup"><span data-stu-id="0b032-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="0b032-155">ภาพประกอบต่อไปนี้แสดงว่าคุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ใน Dynamics 365 Commerce ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="0b032-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![การเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="0b032-157">ตั้งค่าไซต์เพื่อการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="0b032-158">การตั้งค่าค่าสำหรับการให้คะแนนและบทวิจารณ์ เช่น รหัสผู้เช่า ความยาวของข้อความบทวิจารณ์ และความยาวของชื่อบทวิจารณ์ จะตั้งค่าในระดับไซต์</span><span class="sxs-lookup"><span data-stu-id="0b032-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="0b032-159">เมื่อต้องการตั้งค่าไซต์เพื่อแสดงการให้คะแนนและบทวิจารณ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0b032-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="0b032-160">ไปที่ **หน้าหลัก \> ไซต์**</span><span class="sxs-lookup"><span data-stu-id="0b032-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0b032-161">เลือกชื่อไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="0b032-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="0b032-162">ไปที่ **การจัดการไซต์ \> ความสามารถในการเพิ่มฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="0b032-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="0b032-163">ในฟิลด์ **ความยาวสูงสุดของข้อความบทวิจารณ์** ให้ป้อนจำนวนสูงสุดของอักขระที่ข้อความบทวิจารณ์จะมีได้ (ตัวอย่างเช่น **1000**)</span><span class="sxs-lookup"><span data-stu-id="0b032-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="0b032-164">ในฟิลด์ **ความยาวสูงสุดของชื่อบทวิจารณ์** ให้ป้อนจำนวนสูงสุดของอักขระที่ชื่อบทวิจารณ์จะมีได้ (ตัวอย่างเช่น **55**)</span><span class="sxs-lookup"><span data-stu-id="0b032-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="0b032-165">เลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="0b032-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0b032-166">ภาพประกอบต่อไปนี้แสดงว่าการตั้งค่าเป็นอย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0b032-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![การตั้งค่าไซต์เพื่อแสดงการให้คะแนนและบทวิจารณ์](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="0b032-168">เชื่อมโยงการให้คะแนนผลิตภัณฑ์ไปยังส่วนบทวิจารณ์ของ PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="0b032-169">การให้คะแนนผลิตภัณฑ์จะแสดงอยู่ด้านล่างของชื่อผลิตภัณฑ์ที่ด้านบนของ PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="0b032-170">การให้คะแนนผลิตภัณฑ์สามารถตั้งค่าได้เพื่อให้เชื่อมโยงไปยังส่วน **บทวิจารณ์** ของ PDP เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0b032-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="0b032-171">เมื่อต้องการเชื่อมโยงการให้คะแนนผลิตภัณฑ์ไปยังส่วน **บทวิจารณ์** ของ PDP ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0b032-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="0b032-172">เปิดเท็มเพลต PDP</span><span class="sxs-lookup"><span data-stu-id="0b032-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="0b032-173">ไปที่ **การตั้งค่าโมดูลคอนเทนเนอร์กล่องการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="0b032-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="0b032-174">ภายใต้ **กล่องการซื้อ** ให้เลือก **การให้คะแนนผลิตภัณฑ์** จากนั้นเลือกกล่องการเครื่องหมาย **เชื่อมโยงการคลิกกับโมดูลบทวิจารณ์แบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="0b032-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="0b032-175">ภาพประกอบต่อไปนี้แสดงว่าการตั้งค่าเป็นอย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0b032-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![เชื่อมโยงการให้คะแนนผลิตภัณฑ์ไปยังส่วนบทวิจารณ์ของ PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="0b032-177">ตั้งค่าลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย</span><span class="sxs-lookup"><span data-stu-id="0b032-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="0b032-178">เมื่อต้องการตั้งค่าลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0b032-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="0b032-179">ไปที่ **หน้าหลัก \> ไซต์**</span><span class="sxs-lookup"><span data-stu-id="0b032-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0b032-180">เลือกชื่อไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="0b032-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="0b032-181">ไปที่ **การจัดการไซต์ \> ความสามารถในการเพิ่มฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="0b032-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="0b032-182">บนแท็บ **เส้นทาง** ภายใต้ **ความเป็นส่วนตัวและนโยบาย RNR** ให้เลือก **เพิ่มลิงก์**</span><span class="sxs-lookup"><span data-stu-id="0b032-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="0b032-183">ถ้าลิงก์ลิงก์หนึ่งถูกป้อนไว้แล้ว และคุณต้องการแทนที่ ให้เลือกลิงก์นั้น</span><span class="sxs-lookup"><span data-stu-id="0b032-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="0b032-184">ในกล่องโต้ตอบ **เพิ่มลิงก์** ให้เลือกลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0b032-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="0b032-185">เลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="0b032-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0b032-186">ภาพประกอบต่อไปนี้แสดงว่าการตั้งค่าเป็นอย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0b032-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![การตั้งค่าลิงก์สำหรับหน้าความเป็นส่วนตัวและนโยบาย](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="0b032-188">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0b032-188">Additional resources</span></span>

[<span data-ttu-id="0b032-189">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="0b032-190">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="0b032-191">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="0b032-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="0b032-192">ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="0b032-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
