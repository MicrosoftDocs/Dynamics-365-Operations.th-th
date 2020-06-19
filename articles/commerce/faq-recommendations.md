---
title: FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับกระบวนการและเครื่องมือ ที่คุณสามารถใช้ในการแก้ไขปัญหาที่เกี่ยวข้องกับคำแนะนำผลิตภัณฑ์หรือผลลัพธ์ของผลิตภัณฑ์
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e27e4c4d8bdf614d6f55f44daeac3bc152219004
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404313"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="84215-103">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="84215-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="84215-104">หัวข้อนี้จะให้ข้อมูลเกี่ยวกับกระบวนการและเครื่องมือ ที่คุณสามารถใช้ในการแก้ไขปัญหาที่เกี่ยวข้องกับ [คำแนะนำผลิตภัณฑ์](product-recommendations.md) หรือผลลัพธ์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="84215-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="84215-105">แนวทางปฏิบัติ</span><span class="sxs-lookup"><span data-stu-id="84215-105">Best practices</span></span>
<span data-ttu-id="84215-106">มีความสำคัญมากที่จะใช้แนวคิดของผลิตภัณฑ์หลักและผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="84215-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="84215-107">การจัดกลุ่มตัวแปรที่เหมาะสมให้กับผลิตภัณฑ์หลัก จะช่วยให้รายการอัลกอริทึมและบริการสร้างแบบจำลองที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="84215-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="84215-108">นอกจากนี้ บริการสามารถใช้งานได้เพียงหนึ่งอินสแตนซ์ของผลิตภัณฑ์ แทนที่จะใส่ตัวแปรที่เกี่ยวข้องอย่างใกล้ชิดทั้งหมดในรายการ</span><span class="sxs-lookup"><span data-stu-id="84215-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="84215-109">เมื่อมีการกำหนดตัวแปรที่เกี่ยวข้องอย่างใกล้ชิดทั้งหมดในรายการ ผลลัพธ์ที่ไม่ถูกต้องหรือซ้ำกันอาจเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="84215-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="84215-110">เพราะเหตุใดผลิตภัณฑ์จึงขาดหายไปจากรายการแนะนำของฉัน</span><span class="sxs-lookup"><span data-stu-id="84215-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="84215-111">โดยทั่วไปถ้าสินค้าขาดหายไปจากรายการคำแนะนำ ผลิตภัณฑ์อาจมีปัญหาเกี่ยวกับการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="84215-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="84215-112">ตัวอย่างเช่น อาจเป็นวันที่เริ่มต้นของผลิตภัณฑ์หรือวันที่สิ้นสุดที่ไม่ถูกต้อง ขนาดอาจเป็นกำหนดค่าไม่ถูกต้อง หรือผลิตภัณฑ์อาจไม่ได้อยู่ในการจัดประเภทช่องทางที่ถูกต้อง เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="84215-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="84215-113">ถ้าสินค้าขาดหายไปจากรายการคำแนะนำที่ขึ้นอยู่กับการเรียนรู้เครื่องมือปัญญาประดิษฐ์ (AI-ML) สินค้าอาจไม่สอดคล้องกับเงื่อนไขของรายการคำแนะนำ หรืออาจมีธุรกรรมการซื้อที่ไม่เพียงพอสำหรับรายการคำแนะนำที่จะแสดง</span><span class="sxs-lookup"><span data-stu-id="84215-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="84215-114">เราขอแนะนำให้คุณตรวจสอบขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="84215-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="84215-115">**ตรวจสอบให้แน่ใจว่ามีการเปิดใช้งานคำแนะนำผลิตภัณฑ์ใน HQ แล้ว**</span><span class="sxs-lookup"><span data-stu-id="84215-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="84215-116">สำหรับข้อมูลเกี่ยวกับวิธีการเปิดใช้งานบริการนี้เพิ่มเติม ให้ดู [การเปิดใช้งานการแนะนำผลิตภัณฑ์](enable-product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="84215-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="84215-117">**ตรวจสอบให้แน่ใจว่าได้ตั้งค่าคุณสมบัติของผลิตภัณฑ์หลักแล้ว**</span><span class="sxs-lookup"><span data-stu-id="84215-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="84215-118">ตัวอย่างเช่น ต้องตั้งค่าการจัดประเภทผลิตภัณฑ์เพื่อ **รวม**</span><span class="sxs-lookup"><span data-stu-id="84215-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="84215-119">**สำหรับผลิตภัณฑ์ที่จัดประเภทใหม่ อาจใช้เวลานานถึง 3 ชั่วโมงก่อนที่ผลิตภัณฑ์จะเริ่มต้นปรากฏในรายการใหม่**</span><span class="sxs-lookup"><span data-stu-id="84215-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="84215-120">**ถ้าผลิตภัณฑ์ยังคงไม่ปรากฏใน ยอดนิยม ขายดี คนอื่นชอบสิ่งนี้ด้วยเช่นกัน หรือถูกซื้อบ่อย ผลิตภัณฑ์ดังกล่าวอาจมีการทำธุรกรรมที่ไม่เพียงพอ**</span><span class="sxs-lookup"><span data-stu-id="84215-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="84215-121">ในกรณีนี้ คุณสามารถรอให้ธุรกรรมเกิดขึ้นเพิ่มเติม อัพเดตพารามิเตอร์รายการคำแนะนำเริ่มต้น หรือใช้การขัดจังหวะด้วยตนเอง เพื่อแก้ไขผลลัพธ์ของรายการผลิตภัณฑ์ที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="84215-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="84215-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์คำแนะนำให้ดูที่ [การจัดการผลลัพธ์ของคำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="84215-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="84215-123">**ตรวจสอบให้แน่ใจว่าผลิตภัณฑ์ตรงตามเงื่อนไขการแนะนำของรายการ**</span><span class="sxs-lookup"><span data-stu-id="84215-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="84215-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์คำแนะนำให้ดูที่ [การจัดการผลลัพธ์ของคำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="84215-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="84215-125">ฉันจะป้องกันไม่ให้มีการส่งคืนผลลัพธ์ของคำแนะนำที่ไม่ดีได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="84215-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="84215-126">รายการคำแนะนำจำเป็นต้องมีธุรกรรมจำนวนมาก เพื่อที่จะสร้างผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="84215-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="84215-127">ดังนั้นจึงเป็นเรื่องสำคัญที่ผู้ใช้ให้ข้อมูลธุรกรรมในอดีตเต็มรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="84215-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="84215-128">นอกจากนี้ ผลิตภัณฑ์ที่ไม่มีธุรกรรมหรือมีธุรกรรมน้อย โดยทั่วไปจะไม่มี **คนอื่นชอบสิ่งนี้ด้วยเช่นกัน** หรือ **สิ่งที่มักซื้อพร้อมกัน**  และจะไม่ปรากฏในรายการแนะนำ **ยอดนิยม** หรือ **ขายดี**</span><span class="sxs-lookup"><span data-stu-id="84215-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="84215-129">สถานการณ์นี้มักจะเกิดขึ้นสำหรับผลิตภัณฑ์ใหม่มาก หรือสำหรับผลิตภัณฑ์เก่าที่มีการซื้อน้อย</span><span class="sxs-lookup"><span data-stu-id="84215-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="84215-130">สินค้าใหม่ยอดนิยมจะสามารถผ่านปัญหานี้ได้</span><span class="sxs-lookup"><span data-stu-id="84215-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="84215-131">เราขอแนะนำให้คุณทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="84215-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="84215-132">**ตรวจสอบให้แน่ใจว่าผลิตภัณฑ์ตรงตามเงื่อนไขการแนะนำของรายการนั้น**</span><span class="sxs-lookup"><span data-stu-id="84215-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="84215-133">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์คำแนะนำให้ดูที่ แก้ไขผลลัพธ์ของคำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ใช้ AI-ML</span><span class="sxs-lookup"><span data-stu-id="84215-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="84215-134">**ถ้าผลิตภัณฑ์เป็นสินค้าใหม่ ให้พิจารณาแก้ไขรายการคำแนะนำจนกว่าผลิตภัณฑ์จะมีธุรกรรมเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="84215-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="84215-135">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขรายการคำแนะนำ ให้ดูที่ [การจัดการผลลัพธ์ของคำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="84215-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="84215-136">**ตรวจสอบให้แน่ใจว่าผลิตภัณฑ์ตรงตามเงื่อนไขการแนะนำของรายการนั้น**</span><span class="sxs-lookup"><span data-stu-id="84215-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="84215-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์คำแนะนำให้ดูที่ [การจัดการผลลัพธ์ของคำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="84215-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="84215-138">**ถ้าผลิตภัณฑ์เป็นสินค้าใหม่ ให้พิจารณาแก้ไขรายการคำแนะนำจนกว่าผลิตภัณฑ์จะมีธุรกรรมเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="84215-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="84215-139">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขรายการคำแนะนำ ให้ดูที่ [การจัดการผลลัพธ์ของคำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="84215-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="84215-140">ฉันสามารถลบผลิตภัณฑ์แต่ยังคงเห็นผลิตภัณฑ์นั้นในร้านค้าได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="84215-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="84215-141">คุณสามารถปรับปรุงรายการที่สร้างขึ้นโดยอัลกอริทึม ถ้ามีความจำเป็นทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="84215-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="84215-142">อย่างไรก็ตาม ถ้าผลิตภัณฑ์ถูกลบออกจากรายการคำแนะนำ ผลิตภัณฑ์จะยังคงสามารถมองเห็นได้ในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="84215-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="84215-143">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขคำแนะนำผลิตภัณฑ์ ให้ดูที่ [การจัดการผลลัพธ์ของคำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="84215-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="84215-144">ถ้าคุณต้องบล็อคสินค้าจากการค้นพบในร้านค้าคุณต้องเปลี่ยนค่า **การจัดประเภทสินค้า** เป็น **ไม่รวม**</span><span class="sxs-lookup"><span data-stu-id="84215-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="84215-145">ฉันจะเพิ่มรายการลงในหน้าอีคอมเมิร์ซได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="84215-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="84215-146">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเพิ่มหน้าคำแนะนำผลิตภัณฑ์ให้กับเว็บไซต์อีคอมเมิร์ซของคุณให้ดูที่ [การเพิ่มรายการแนะนำผลิตภัณฑ์ลงในหน้า](add-reco-list-to-page.md)</span><span class="sxs-lookup"><span data-stu-id="84215-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="84215-147">ฉันจะเปิดใช้งานคำแนะนำบน POS ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="84215-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="84215-148">หลังจากเปิดใช้งานคำแนะนำผลิตภัณฑ์แล้วคุณจะต้องเพิ่มแผงคำแนะนำลงในหน้าจอควบคุม POS</span><span class="sxs-lookup"><span data-stu-id="84215-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="84215-149">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="84215-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84215-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="84215-150">Additional resources</span></span>

[<span data-ttu-id="84215-151">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="84215-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="84215-152">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="84215-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="84215-153">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="84215-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="84215-154">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="84215-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="84215-155">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="84215-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="84215-156">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="84215-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="84215-157">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="84215-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="84215-158">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="84215-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="84215-159">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="84215-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="84215-160">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="84215-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
