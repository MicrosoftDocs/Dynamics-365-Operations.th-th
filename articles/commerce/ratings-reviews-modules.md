---
title: โมดูลการให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะครอบคลุมโมดูลการจัดอันดับและบทวิจารณ์ที่ใช้ในหน้ารายละเอียดของผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: ee2a2a781537b592fb5f80ce424a7331c4e21d41
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071899"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="a48b9-103">โมดูลการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a48b9-104">หัวข้อนี้จะครอบคลุมโมดูลการจัดอันดับและบทวิจารณ์ที่ใช้ในหน้ารายละเอียดของผลิตภัณฑ์ (PDPs) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a48b9-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a48b9-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="a48b9-105">Overview</span></span>

<span data-ttu-id="a48b9-106">การจัดอันดับและบทวิจารณ์บนเว็บไซต์อีคอมเมิร์ซช่วยให้ลูกค้าเรียนรู้เกี่ยวกับผลิตภัณฑ์ก่อนที่พวกเขาทำการตัดสินใจซื้อ และยังเป็นกลไกสำหรับการรวบรวมข้อคิดเห็นของลูกค้าเกี่ยวกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="a48b9-107">การให้คะแนนแสดงอยู่บนหน้ารายการผลิตภัณฑ์ หน้ารายการประเภท หน้าผลการค้นหา และหน้าไซต์อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="a48b9-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="a48b9-108">กราฟแสดงค่าสถิติความถี่ของการให้คะแนนและบทวิจารณ์ผลิตภัณฑ์จะแสดงอยู่บน PDPs</span><span class="sxs-lookup"><span data-stu-id="a48b9-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="a48b9-109">ปุ่ม **เขียนบทวิจารณ์** ช่วยให้ลูกค้าส่งการให้คะแนนและบทวิจารณ์สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="a48b9-110">คุณลักษณะ PDP เหล่านี้จะถูกควบคุมโดยโมดูลการจัดอันดับและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="a48b9-111">โมดูลการให้คะแนนและบทวิจารณ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="a48b9-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="a48b9-112">สามโมดูลจะแสดงนสรุปการให้คะแนนและบทวิจารณ์บน PDP:</span><span class="sxs-lookup"><span data-stu-id="a48b9-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="a48b9-113">โมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-113">Write review module</span></span>
- <span data-ttu-id="a48b9-114">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-114">Product reviews list module</span></span>
- <span data-ttu-id="a48b9-115">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="a48b9-115">Ratings histogram module</span></span>
 
<span data-ttu-id="a48b9-116">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าโมดูลการให้คะแนนและบทวิจารณ์มีลักษณะอย่างไรบน PDP</span><span class="sxs-lookup"><span data-stu-id="a48b9-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![โมดูลการให้คะแนนและบทวิจารณ์บน PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="a48b9-118">สำหรับข้อมูลเกี่ยวกับวิธีการทำเท็มเพลตและเค้าโครง PDP ให้เหมาะสม เพื่อให้คุณสามารถใช้การตั้งค่าสำหรับโมดูลการให้คะแนนและบทวิจารณ์ร่วมกันระหว่างหลาย PDP บนไซต์อีคอมเมิร์ซของคุณ โปรดดูที่ [ภาพรวมเท็มเพลตและเค้าโครง](templates-layouts-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a48b9-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="a48b9-119">ภาพประกอบต่อไปนี้แสดงว่ากล่องโต้ตอบ **เพิ่มโมดูล** แสดงโมดูลการให้คะแนนและบทวิจารณ์อย่างไรใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a48b9-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="a48b9-120">![กล่องโต้ตอบของการเพิ่มโมดูล](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="a48b9-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="a48b9-121">โมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-121">Write review module</span></span>

<span data-ttu-id="a48b9-122">โมดูลการเขียนบทวิจารณ์จะมีปุ่ม **เขียนบทวิจารณ์** ที่ช่วยให้ผู้ใช้ลงชื่อเข้าใช้ กำหนดการให้คะแนน และเขียนบทวิจารณ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="a48b9-123">โมดูลนี้ยังช่วยให้ผู้ใช้แก้ไขการให้คะแนนหรือบทวิจารณ์ที่พวกเขาได้ส่งก่อนหน้านี้ได้</span><span class="sxs-lookup"><span data-stu-id="a48b9-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="a48b9-124">โดยทั่วไปแล้ว โมดูลจะปรากฏขึ้นด้านบนของโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนและโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="a48b9-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="a48b9-125">ภาพประกอบต่อไปนี้แสดงกล่องตอบโต้ **เขียนบทวิจารณ์** ที่ปรากฏขึ้นเมื่อลูกค้าเลือก **เขียนบทวิจารณ์**</span><span class="sxs-lookup"><span data-stu-id="a48b9-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="a48b9-126">ลูกค้าสามารถใช้กล่องโต้ตอบนี้เพื่อส่งการให้คะแนนและบทวิจารณ์ได้</span><span class="sxs-lookup"><span data-stu-id="a48b9-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="a48b9-127">![กล่องโต้ตอบการเขียนบทวิจารณ์](media/rnr-eCommerce-write-review-module.png) ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลการเขียนบทวิจารณ์ที่จำเป็นต้องตั้งค่าคอนฟิกในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="a48b9-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="a48b9-128">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="a48b9-128">Property name</span></span> | <span data-ttu-id="a48b9-129">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="a48b9-129">Value</span></span>        | <span data-ttu-id="a48b9-130">คำอธิบายคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="a48b9-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="a48b9-131">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="a48b9-131">Name</span></span>          | <span data-ttu-id="a48b9-132">การเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-132">Write review</span></span> | <span data-ttu-id="a48b9-133">ชื่อของโมดูลการเขียนบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="a48b9-134">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="a48b9-134">Ratings histogram module</span></span>

<span data-ttu-id="a48b9-135">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนแสดงกราฟแสดงค่าสถิติความถี่ของการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="a48b9-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="a48b9-136">โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นระหว่างโมดูลการเขียนบทวิจารณ์และโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP</span><span class="sxs-lookup"><span data-stu-id="a48b9-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="a48b9-137">โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนไม่ต้องมีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="a48b9-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="a48b9-138">คุณเพียงแค่ต้องเพิ่มโมดูลในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a48b9-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="a48b9-139">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าเท็มเพลต PDP ใน Dynamics 365 Commerce จะมีลักษณะอย่างไรโมดูลต่าง ๆ การให้คะแนนและบทวิจารณ์มีการตั้งค่าสำหรับแสดงบน PDP</span><span class="sxs-lookup"><span data-stu-id="a48b9-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="a48b9-140">![เท็มเพลต PDP เมื่อการให้คะแนนและบทวิจารณ์มีการตั้งค่าสำหรับการแสดงผลบน PDP](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="a48b9-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="a48b9-141">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-141">Product reviews list module</span></span>

<span data-ttu-id="a48b9-142">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์แสดงรายการของบทวิจารณ์ผลิตภัณฑ์พร้อมด้วยตัวเลือกการเรียงลำดับ การกรองข้อมูล และการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="a48b9-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="a48b9-143">โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นหลังจากโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนบน PDP</span><span class="sxs-lookup"><span data-stu-id="a48b9-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="a48b9-144">ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ที่จำเป็นต้องตั้งค่าในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="a48b9-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="a48b9-145">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="a48b9-145">Property name</span></span>              | <span data-ttu-id="a48b9-146">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="a48b9-146">Value</span></span> | <span data-ttu-id="a48b9-147">คำอธิบายคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="a48b9-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="a48b9-148">บทวิจารณ์ที่แสดงในแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="a48b9-148">Reviews shown on each page</span></span> | <span data-ttu-id="a48b9-149">10</span><span class="sxs-lookup"><span data-stu-id="a48b9-149">10</span></span>    | <span data-ttu-id="a48b9-150">จำนวนบทวิจารณ์ที่ควรจะแสดงออกมาในแต่ละครั้งบน PDP</span><span class="sxs-lookup"><span data-stu-id="a48b9-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="a48b9-151">ปุ่ม **ถัดไป** และ **ก่อนหน้า** จะมีอยู่ เพื่อให้ผู้ใช้สามารถย้ายไปยังหน้าต่าง ๆ ของบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="a48b9-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="a48b9-152">กราฟแสดงค่าสถิติความถี่ของการให้คะแนน - มุมมองสรุป</span><span class="sxs-lookup"><span data-stu-id="a48b9-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="a48b9-153">โมดูลรายการบทวิจารณ์ผลิตภัณฑ์มีช่องที่คุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนได้</span><span class="sxs-lookup"><span data-stu-id="a48b9-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="a48b9-154">ภาพประกอบต่อไปนี้แสดงว่าคุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ใน Dynamics 365 Commerce ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="a48b9-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![การเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="a48b9-156">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a48b9-156">Additional resources</span></span>

[<span data-ttu-id="a48b9-157">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a48b9-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a48b9-158">โมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="a48b9-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a48b9-159">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="a48b9-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a48b9-160">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="a48b9-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a48b9-161">โมดูลใบยืนยันคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="a48b9-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a48b9-162">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="a48b9-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a48b9-163">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="a48b9-163">Footer module</span></span>](author-footer-module.md)
