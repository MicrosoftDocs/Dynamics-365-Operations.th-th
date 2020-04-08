---
title: ภาพรวมของคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับคำแนะนำผลิตภัณฑ์ คำแนะนำผลิตภัณฑ์ให้ลูกค้าค้นหาผลิตภัณฑ์ที่ต้องการและแม้กระทั่งผลิตภัณฑ์ที่ไม่ได้ตั้งใจจะซื้อได้ง่ายและรวดเร็ว
author: Moonma
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e61136ed296d673e14600762c6f6199093530546
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154237"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="cae77-104">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cae77-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cae77-105">Microsoft Dynamics 365 Commerce สามารถใช้แสดงคำแนะนำเกี่ยวกับผลิตภัณฑ์บนเว็บไซต์อีคอมเมิร์ซ และอุปกรณ์การขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="cae77-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="cae77-106">คำแนะนำผลิตภัณฑ์คือสินค้าที่ลูกค้าอาจสนใจ</span><span class="sxs-lookup"><span data-stu-id="cae77-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="cae77-107">คำแนะนำเหล่านี้จะขึ้นอยู่กับแนวโน้มของการซื้อของลูกค้ารายอื่นๆ ในร้านค้าออนไลน์และร้านจริง</span><span class="sxs-lookup"><span data-stu-id="cae77-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="cae77-108">คำแนะนำผลิตภัณฑ์อนุญาตให้ลูกค้าค้นหาผลิตภัณฑ์ที่พวกเขาต้องการได้อย่างง่ายดายและรวดเร็ว ในขณะเดียวกันก็มีประสบการณ์การใช้งานที่ดี</span><span class="sxs-lookup"><span data-stu-id="cae77-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="cae77-109">นอกจากนี้ยังสามารถใช้การขายสินค้าชนิดอื่นและการขายสินค้าต่อเนื่อง เพื่อช่วยลูกค้าในการค้นหาผลิตภัณฑ์เพิ่มเติมที่พวกเขาไม่ได้ตั้งใจจะซื้อในตอนแรกได้</span><span class="sxs-lookup"><span data-stu-id="cae77-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="cae77-110">เมื่อมีการใช้ข้อแนะนำในการปรับปรุงการค้นหาผลิตภัณฑ์ จะมีการสร้างโอกาสทางการขายในการแปลงเพิ่มเติม ช่วยเพิ่มรายได้จากการขาย และยังช่วยเพิ่มความพึงพอใจของและการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="cae77-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="cae77-111">ในอีคอมเมิร์ซ คำแนะนำผลิตภัณฑ์มีการขับเคลื่อนโดยเทคโนโลยี Machine Learning ของ Microsoft Recommendations ในขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="cae77-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="cae77-112">บริการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="cae77-112">Recommendation service</span></span>

<span data-ttu-id="cae77-113">บริการคำแนะนำผลิตภัณฑ์ใช้เทคโนโลยีปัญญาประดิษฐ์และ machine learning (AI-ML) ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cae77-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="cae77-114">ข้อมูลในรูปแบบที่บริการคำแนะนำต้องการ จะถูกแยกจากฐานข้อมูลด้านการดำเนินการของ Commerce และถูกส่งไปยัง Azure data lake storage (ADLS) หรือร้านค้าเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="cae77-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure data lake storage (ADLS) or Entity store.</span></span>
- <span data-ttu-id="cae77-115">บริการคำแนะนำจะใช้ข้อมูลที่จัดเก็บในการฝึกอบรมแบบจำลองคำแนะนำสำหรับรายการ **คนชอบสิ่งนี้เช่นกัน** **ซื้อร่วมกันบ่อย** **ใหม่** **ขายดี** และ **ยอดนิยม**</span><span class="sxs-lookup"><span data-stu-id="cae77-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="cae77-116">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="cae77-116">Scenarios</span></span>

<span data-ttu-id="cae77-117">คำแนะนำผลิตภัณฑ์ถูกเปิดใช้งานสำหรับสถานการณ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cae77-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="cae77-118">**บนหน้าร้านค้าใดๆ สำหรับการเรียกดูหรือหน้าเริ่มต้นในอีคอมเมิร์ซ:** ถ้าลูกค้าหรือร้านค้าเข้าถึงหน้าร้านค้า โปรแกรมแนะนำสามารถแนะนำผลิตภัณฑ์ในรายการ **สินค้าใหม่** **ขายดี** และ **ที่กำลังนิยม**</span><span class="sxs-lookup"><span data-stu-id="cae77-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="cae77-119">**บนหน้ารายละเอียดของผลิตภัณฑ์:** ถ้าลูกค้าหรือร้านค้าเข้าร่วมหน้า **รายละเอียดผลิตภัณฑ์** โปรแกรมแนะนำจะแนะนำสินค้าเพิ่มเติมที่มีแนวโน้มจะซื้อด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="cae77-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="cae77-120">รายการเหล่านี้จะปรากฏในรายชื่อ **คนอื่นชอบสิ่งนี้ด้วยเช่นกัน**</span><span class="sxs-lookup"><span data-stu-id="cae77-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="cae77-121">**บนหน้าธุรกรรมหรือหน้าเช็คเอาท์:** โปรแกรมแนะนำจะแนะนำสินค้าตามรายการสินค้าทั้งหมดในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="cae77-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="cae77-122">สินค้าเหล่านี้จะปรากฏในรายการ **สินค้าที่มีการซื้อร่วมกันบ่อยๆ**</span><span class="sxs-lookup"><span data-stu-id="cae77-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="cae77-123">**คำแนะนำส่วนบุคคล:** ผู้จัดซื้อสามารถให้ลูกค้าที่ลงชื่อเข้าใช้ **รายการที่เลือกไว้สำหรับคุณ** ส่วนบุคคล นอกเหนือจากฟังก์ชันใหม่ที่อนุญาตให้ใช้รายการสถานการณ์จำลองที่มีอยู่ เพื่อสร้างความเป็นส่วนบุคคลสำหรับลูกค้ารายนั้น</span><span class="sxs-lookup"><span data-stu-id="cae77-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="cae77-124">เมื่อต้องการเรียนรู้เพิ่มเติม ดูที่ [เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="cae77-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="cae77-125">ชนิดของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cae77-125">Types of product recommendations</span></span>

<span data-ttu-id="cae77-126">ตารางต่อไปนี้อธิบายคำแนะนำเกี่ยวกับผลิตภัณฑ์แบบอัตโนมัติชนิดต่างๆ ที่พร้อมใช้งานสำหรับผู้ขายปลีกเพื่อใช้ในโซลูชัน Dynamics 365 Commerce ของพวกเขาผ่าน [โมดูลการเก็บรวบรวมผลิตภัณฑ์](product-collection-module-overview.md)</span><span class="sxs-lookup"><span data-stu-id="cae77-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="cae77-127">นอกจากนี้ ผู้ขายปลีกยังสามารถแสดงผลลัพธ์ที่เป็นแบบส่วนบุคคลสำหรับผู้ใช้ที่ลงชื่อเข้าใช้ หากผู้สร้างไซต์เลือกตัวเลือกนั้น</span><span class="sxs-lookup"><span data-stu-id="cae77-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="cae77-128">โมดูลการรวบรวมผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cae77-128">Product collection module</span></span>  | <span data-ttu-id="cae77-129">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cae77-129">Type</span></span> | <span data-ttu-id="cae77-130">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cae77-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="cae77-131">สร้าง </span><span class="sxs-lookup"><span data-stu-id="cae77-131">New</span></span>                        | <span data-ttu-id="cae77-132">อัลกอริทึม</span><span class="sxs-lookup"><span data-stu-id="cae77-132">Algorithmic</span></span> | <span data-ttu-id="cae77-133">โมดูลนี้แสดงรายการของผลิตภัณฑ์ใหม่ล่าสุดที่มีการจัดประเภทเป็นช่องทางและแค็ตตาล็อกล่าสุด</span><span class="sxs-lookup"><span data-stu-id="cae77-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="cae77-134">ขายดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="cae77-134">Best selling</span></span>               | <span data-ttu-id="cae77-135">อัลกอริทึม</span><span class="sxs-lookup"><span data-stu-id="cae77-135">Algorithmic</span></span> | <span data-ttu-id="cae77-136">โมดูลนี้แสดงรายการของผลิตภัณฑ์ที่ถูกจัดอันดับตามจำนวนยอดขายสูงสุด</span><span class="sxs-lookup"><span data-stu-id="cae77-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="cae77-137">กำลังนิยม</span><span class="sxs-lookup"><span data-stu-id="cae77-137">Trending</span></span>                   | <span data-ttu-id="cae77-138">อัลกอริทึม</span><span class="sxs-lookup"><span data-stu-id="cae77-138">Algorithmic</span></span> | <span data-ttu-id="cae77-139">โมดูลนี้แสดงรายการของผลิตภัณฑ์ที่มีประสิทธิภาพสูงสุดสำหรับรอบระยะเวลาที่กำหนด ซึ่งจัดอันดับตามจำนวนยอดขายสูงสุด</span><span class="sxs-lookup"><span data-stu-id="cae77-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="cae77-140">สิ่งที่มักซื้อพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="cae77-140">Frequently bought together</span></span> | <span data-ttu-id="cae77-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="cae77-141">AI-ML</span></span> | <span data-ttu-id="cae77-142">โมดูลนี้จะแนะนำรายการของผลิตภัณฑ์ที่ถูกซื้อโดยทั่วไปพร้อมกับเนื้อหาของรถเข็นปัจจุบันของผู้บริโภค</span><span class="sxs-lookup"><span data-stu-id="cae77-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="cae77-143">ผู้คนชอบเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="cae77-143">People also like</span></span>           | <span data-ttu-id="cae77-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="cae77-144">AI-ML</span></span> | <span data-ttu-id="cae77-145">โมดูลนี้แนะนำผลิตภัณฑ์สำหรับผลิตภัณฑ์เมล็ดพันธุ์ที่กำหนดตามรูปแบบการซื้อของผู้บริโภค</span><span class="sxs-lookup"><span data-stu-id="cae77-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="cae77-146">เลือกมาสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="cae77-146">Picks for you</span></span>              | <span data-ttu-id="cae77-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="cae77-147">AI-ML</span></span> | <span data-ttu-id="cae77-148">โมดูลนี้จะแนะนำรายการผลิตภัณฑ์ที่เป็นแบบส่วนบุคคลตามรูปแบบการซื้อของผู้ใช้ที่ลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="cae77-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="cae77-149">สำหรับผู้ใช้ที่เป็นแขก รายการนี้จะถูกยุบ</span><span class="sxs-lookup"><span data-stu-id="cae77-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="cae77-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cae77-150">Additional resources</span></span>

[<span data-ttu-id="cae77-151">เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cae77-151">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="cae77-152">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cae77-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="cae77-153">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="cae77-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="cae77-154">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="cae77-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="cae77-155">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="cae77-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="cae77-156">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cae77-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="cae77-157">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="cae77-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="cae77-158">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="cae77-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="cae77-159">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="cae77-159">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="cae77-160">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cae77-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
