---
title: โมดูลการให้คะแนนและบทวิจารณ์
description: หัวข้อนี้ครอบคลุมโมดูลการจัดอันดับและบทวิจารณ์ที่ใช้ในหน้ารายละเอียดของผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: dee9a6a7e2a5278f069958ce00689b1beb9b1bd7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792158"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="55600-103">โมดูลการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="55600-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="55600-104">หัวข้อนี้ครอบคลุมโมดูลการจัดอันดับและบทวิจารณ์ที่ใช้ในหน้ารายละเอียดของผลิตภัณฑ์ (PDPs) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="55600-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="55600-105">การจัดอันดับและบทวิจารณ์บนเว็บไซต์อีคอมเมิร์ซช่วยให้ลูกค้าเรียนรู้เกี่ยวกับผลิตภัณฑ์ก่อนที่พวกเขาทำการตัดสินใจซื้อ และยังเป็นกลไกสำหรับการรวบรวมข้อคิดเห็นของลูกค้าเกี่ยวกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="55600-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="55600-106">การให้คะแนนแสดงอยู่บนหน้ารายการผลิตภัณฑ์ หน้ารายการประเภท หน้าผลการค้นหา และหน้าไซต์อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="55600-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="55600-107">กราฟแสดงค่าสถิติความถี่ของการให้คะแนนและบทวิจารณ์ผลิตภัณฑ์จะแสดงอยู่บน PDPs</span><span class="sxs-lookup"><span data-stu-id="55600-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="55600-108">ปุ่ม **เขียนบทวิจารณ์** ช่วยให้ลูกค้าส่งการให้คะแนนและบทวิจารณ์สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="55600-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="55600-109">คุณลักษณะ PDP เหล่านี้จะถูกควบคุมโดยโมดูลการจัดอันดับและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="55600-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="55600-110">โมดูลการให้คะแนนและบทวิจารณ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="55600-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="55600-111">สามโมดูลจะแสดงนสรุปการให้คะแนนและบทวิจารณ์บน PDP:</span><span class="sxs-lookup"><span data-stu-id="55600-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="55600-112">โมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="55600-112">Write review module</span></span>
- <span data-ttu-id="55600-113">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="55600-113">Product reviews list module</span></span>
- <span data-ttu-id="55600-114">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="55600-114">Ratings histogram module</span></span>
 
<span data-ttu-id="55600-115">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าโมดูลการให้คะแนนและบทวิจารณ์มีลักษณะอย่างไรบน PDP</span><span class="sxs-lookup"><span data-stu-id="55600-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![โมดูลการให้คะแนนและบทวิจารณ์บน PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="55600-117">สำหรับข้อมูลเกี่ยวกับวิธีการทำเท็มเพลตและเค้าโครง PDP ให้เหมาะสม เพื่อให้คุณสามารถใช้การตั้งค่าสำหรับโมดูลการให้คะแนนและบทวิจารณ์ร่วมกันระหว่างหลาย PDP บนไซต์อีคอมเมิร์ซของคุณ โปรดดูที่ [ภาพรวมเท็มเพลตและเค้าโครง](templates-layouts-overview.md)</span><span class="sxs-lookup"><span data-stu-id="55600-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="55600-118">ภาพประกอบต่อไปนี้แสดงว่ากล่องโต้ตอบ **เพิ่มโมดูล** แสดงโมดูลการให้คะแนนและบทวิจารณ์อย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="55600-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="55600-119">![กล่องโต้ตอบของการเพิ่มโมดูล](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="55600-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="55600-120">โมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="55600-120">Write review module</span></span>

<span data-ttu-id="55600-121">โมดูลการเขียนบทวิจารณ์จะมีปุ่ม **เขียนบทวิจารณ์** ที่ช่วยให้ผู้ใช้ลงชื่อเข้าใช้ กำหนดการให้คะแนน และเขียนบทวิจารณ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="55600-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="55600-122">โมดูลนี้ยังช่วยให้ผู้ใช้แก้ไขการให้คะแนนหรือบทวิจารณ์ที่พวกเขาได้ส่งก่อนหน้านี้ได้</span><span class="sxs-lookup"><span data-stu-id="55600-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="55600-123">โดยทั่วไปแล้ว โมดูลจะปรากฏขึ้นด้านบนของโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนและโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="55600-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="55600-124">ภาพประกอบต่อไปนี้แสดงกล่องตอบโต้ **เขียนบทวิจารณ์** ที่ปรากฏขึ้นเมื่อลูกค้าเลือก **เขียนบทวิจารณ์**</span><span class="sxs-lookup"><span data-stu-id="55600-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="55600-125">ลูกค้าสามารถใช้กล่องโต้ตอบนี้เพื่อส่งการให้คะแนนและบทวิจารณ์ได้</span><span class="sxs-lookup"><span data-stu-id="55600-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="55600-126">![กล่องโต้ตอบการเขียนบทวิจารณ์](media/rnr-eCommerce-write-review-module.png) ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลการเขียนบทวิจารณ์ที่จำเป็นต้องตั้งค่าคอนฟิกในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="55600-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="55600-127">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="55600-127">Property name</span></span> | <span data-ttu-id="55600-128">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="55600-128">Value</span></span>        | <span data-ttu-id="55600-129">คำอธิบายคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="55600-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="55600-130">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="55600-130">Name</span></span>          | <span data-ttu-id="55600-131">การเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="55600-131">Write review</span></span> | <span data-ttu-id="55600-132">ชื่อของโมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="55600-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="55600-133">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="55600-133">Ratings histogram module</span></span>

<span data-ttu-id="55600-134">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนแสดงกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="55600-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="55600-135">โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นระหว่างโมดูลการเขียนบทวิจารณ์และโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="55600-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="55600-136">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนไม่ต้องมีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="55600-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="55600-137">คุณเพียงแค่ต้องเพิ่มโมดูลในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="55600-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="55600-138">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าเท็มเพลต PDP ใน Dynamics 365 Commerce จะมีลักษณะอย่างไรโมดูลต่าง ๆ การให้คะแนนและบทวิจารณ์มีการตั้งค่าสำหรับแสดงบน PDP</span><span class="sxs-lookup"><span data-stu-id="55600-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="55600-139">![เท็มเพลต PDP เมื่อการให้คะแนนและบทวิจารณ์มีการตั้งค่าสำหรับการแสดงผลบน PDP](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="55600-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="55600-140">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="55600-140">Product reviews list module</span></span>

<span data-ttu-id="55600-141">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์แสดงรายการของบทวิจารณ์ผลิตภัณฑ์พร้อมด้วยตัวเลือกการเรียงลำดับ การกรองข้อมูล และการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="55600-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="55600-142">โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นหลังจากโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนบน PDP</span><span class="sxs-lookup"><span data-stu-id="55600-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="55600-143">ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ที่จำเป็นต้องตั้งค่าในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="55600-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="55600-144">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="55600-144">Property name</span></span>              | <span data-ttu-id="55600-145">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="55600-145">Value</span></span> | <span data-ttu-id="55600-146">คำอธิบายคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="55600-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="55600-147">บทวิจารณ์ที่แสดงในแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="55600-147">Reviews shown on each page</span></span> | <span data-ttu-id="55600-148">10</span><span class="sxs-lookup"><span data-stu-id="55600-148">10</span></span>    | <span data-ttu-id="55600-149">จำนวนบทวิจารณ์ที่ควรจะแสดงออกมาในแต่ละครั้งบน PDP</span><span class="sxs-lookup"><span data-stu-id="55600-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="55600-150">ปุ่ม **ถัดไป** และ **ก่อนหน้า** จะมีอยู่ เพื่อให้ผู้ใช้สามารถย้ายไปยังหน้าต่าง ๆ ของบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="55600-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="55600-151">กราฟแสดงค่าสถิติความถี่ของการให้คะแนน - มุมมองสรุป</span><span class="sxs-lookup"><span data-stu-id="55600-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="55600-152">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์มีช่องที่คุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนได้</span><span class="sxs-lookup"><span data-stu-id="55600-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="55600-153">ภาพประกอบต่อไปนี้แสดงว่าคุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ใน Dynamics 365 Commerce ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="55600-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![การเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="55600-155">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="55600-155">Additional resources</span></span>

[<span data-ttu-id="55600-156">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="55600-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="55600-157">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="55600-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="55600-158">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="55600-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="55600-159">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="55600-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="55600-160">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="55600-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="55600-161">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="55600-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="55600-162">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="55600-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]