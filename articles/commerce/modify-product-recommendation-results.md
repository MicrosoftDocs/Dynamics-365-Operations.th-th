---
title: ปรับปรุงผลลัพธ์ของคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML
description: หัวข้อนี้จะอธิบายถึงวิธีการปรับแต่งผลลัพธ์ของคำแนะนำผลิตภัณฑ์โดยใช้การเรียนรู้เครื่องมือปัญญาประดิษฐ์ (AI-ML) กับธุรกิจของคุณ
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4631ef03e1d73b70d80e774d1efa4909e619bbc0
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127939"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="35535-103">ปรับปรุงผลลัพธ์ของคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML</span><span class="sxs-lookup"><span data-stu-id="35535-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="35535-104">หัวข้อนี้จะอธิบายถึงวิธีการปรับปรุงผลลัพธ์ของคำแนะนำผลิตภัณฑ์โดยใช้การเรียนรู้เครื่องมือปัญญาประดิษฐ์ (AI-ML) กับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="35535-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="35535-105">หลังจากเปิดใช้งานคำแนะนำผลิตภัณฑ์แล้ว การตั้งค่าเริ่มต้นจะมีผลบังคับใช้ พารามิเตอร์เหล่านี้จะทำงานสำหรับความต้องการหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="35535-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="35535-106">วิธีการที่ดีที่สุดคือการวางแผนในการใช้เวลาในการประเมินว่าผลลัพธ์มีความเหมาะสมกับการเคลื่อนไหวทางการขายของผลิตภัณฑ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="35535-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="35535-107">เราขอแนะนำให้ประเมินผลลัพธ์เป็นเวลาสองสามวันก่อนที่จะเปลี่ยนพารามิเตอร์ตามต้องการก่อนการทดสอบอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="35535-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="35535-108">การทำความเข้าใจเกี่ยวกับพารามิเตอร์รายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="35535-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="35535-109">ก่อนที่จะเปลี่ยนพารามิเตอร์ ให้เรียนรู้ว่าจะส่งผลกระทบต่อผลลัพธ์อย่างไรตามด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="35535-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="35535-110">รายการผลิตภัณฑ์ "ยอดนิยม"</span><span class="sxs-lookup"><span data-stu-id="35535-110">"Trending" product list</span></span>

<span data-ttu-id="35535-111">รายการผลิตภัณฑ์ "ยอดนิยม" มีพารามิเตอร์สองอย่างที่สามารถเปลี่ยนแปลงได้:</span><span class="sxs-lookup"><span data-stu-id="35535-111">The "Trending" product list has two parameters that can be changed:</span></span>

![ตัวอย่างพารามิเตอร์เริ่มต้นสำหรับรายการ "ของยอดนิยม"](./media/exampletrendingparameters.png)

1. <span data-ttu-id="35535-113">**รวมผลิตภัณฑ์ใหม่จาก X วันล่าสุด** - ผลิตภัณฑ์ที่มีการเพิ่มภายในจำนวนวันที่ระบุไว้ก่อนที่จะสามารถใช้วันที่ปัจจุบันเพื่อเลือกผู้สมัครผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="35535-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="35535-114">ค่าเริ่มต้นในรูปภาพแสดงให้เห็นว่าผลิตภัณฑ์ที่มีอายุ 180 วันสามารถใช้ได้ในรายการผลิตภัณฑ์ยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="35535-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="35535-115">**รวมการขายใหม่จาก X วันล่าสุด** - ธุรกรรมการขายที่เกิดขึ้นในจำนวนวันที่ระบุไว้ก่อนที่จะสามารถใช้วันที่ปัจจุบันสามารถใช้เพื่อสั่งซื้อสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="35535-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="35535-116">ค่าเริ่มต้นข้างต้นจะแนะนำว่าการสั่งซื้อทั้งหมดของผลิตภัณฑ์ใน 30 วันที่ผ่านมาจะใช้ในการกำหนดตำแหน่งของผลิตภัณฑ์ในรายการผลิตภัณฑ์ยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="35535-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="35535-117">รายการผลิตภัณฑ์ "ที่ขายดีที่สุด"</span><span class="sxs-lookup"><span data-stu-id="35535-117">"Best selling" product list</span></span>

<span data-ttu-id="35535-118">ทั้งนี้ขึ้นอยู่กับธุรกิจของคุณรายการ "สินค้าขายที่ดีที่สุด" อาจนำผลลัพธ์ที่แตกต่างจากสินค้ายอดนิยม ถึงแม้ว่าทั้งสองจะใช้ข้อมูลธุรกรรมเพื่อสั่งผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="35535-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="35535-119">เนื่องจากการขายที่ดีที่สุดไม่มีการตัดออกตามวันที่จัดประเภท การขายที่ดีที่สุดยังคงเน้นความนิยมมากที่สุด ผลิตภัณฑ์ที่เก่ากว่าอาจตกลงจากรายการยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="35535-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="35535-120">รายการผลิตภัณฑ์ "ที่ขายดีที่สุด" มีพารามิเตอร์เดียวที่สามารถเปลี่ยนแปลงได้:</span><span class="sxs-lookup"><span data-stu-id="35535-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![ตัวอย่างพารามิเตอร์เริ่มต้นสำหรับรายการขายที่ดีที่สุด](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="35535-122">**รวมการขายใหม่จาก X วันล่าสุด** - ธุรกรรมการขายที่เกิดขึ้นในจำนวนวันที่ระบุไว้ก่อนที่จะสามารถใช้วันที่ปัจจุบันสามารถใช้เพื่อสั่งซื้อสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="35535-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="35535-123">ค่าเริ่มต้นข้างต้นจะแนะนำว่าการสั่งซื้อทั้งหมดของผลิตภัณฑ์ใน 30 วันที่ผ่านมาจะใช้ในการกำหนดตำแหน่งของผลิตภัณฑ์ในรายการผลิตภัณฑ์ที่ขายดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="35535-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="35535-124">เพิ่มหรือลบผลิตภัณฑ์ออกจากรายการคำแนะนำด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="35535-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="35535-125">สำหรับรายการ "สินค้าใหม่" "สินค้ายอดนิยม" หรือ "สินค้าที่ขายดีที่สุด"</span><span class="sxs-lookup"><span data-stu-id="35535-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="35535-126">ไปที่ **การขายปลีกและการค้า** > **คำแนะนำของผลิตภัณฑ์** > **พารามิเตอร์คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="35535-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="35535-127">ในรายการพารามิเตอร์ที่ใช้ร่วมกัน โปรดเลือก **รายการแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="35535-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="35535-128">เลือกรายการที่จะเพิ่มหรือลบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="35535-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="35535-129">ในการเพิ่มผลิตภัณฑ์ไปยังตาราง ให้เลือก **เพิ่มบรรทัด**</span><span class="sxs-lookup"><span data-stu-id="35535-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="35535-130">ภายใต้คอลัมน์ผลิตภัณฑ์ให้ค้นหาผลิตภัณฑ์ตาม **ชื่อ** หรือ **หมายเลขผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="35535-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![ตัวอย่างของการค้นหาสำหรับผลิตภัณฑ์ในรายการผลิตภัณฑ์ใหม่](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="35535-132">ภายใต้คอลัมน์ชนิดบรรทัด ให้เลือกตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="35535-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="35535-133">**รวม** – บังคับผลิตภัณฑ์ให้กับด้านหน้าของรายการ</span><span class="sxs-lookup"><span data-stu-id="35535-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="35535-134">**ไม่รวม** – ลบผลิตภัณฑ์ออกจากการปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="35535-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![ตัวอย่างของการรวมหรือไม่รวมผลิตภัณฑ์จากรายการผลิตภัณฑ์ใหม่](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="35535-136">การเปลี่ยน **ลำดับการแสดง** จะเปลี่ยนลำดับของผลิตภัณฑ์ที่มีการทำเครื่องหมาย **รวม** จะปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="35535-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="35535-137">ถ้าผลิตภัณฑ์สองตัวมีค่าของ **ลำดับการแสดงผล** เดียวกัน ใบสั่งสุดท้ายของผลลัพธ์สองอย่างอาจแตกต่างจากฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="35535-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="35535-138">เมื่อต้องการลบผลิตภัณฑ์ออกจากตาราง: ให้เลือกบรรทัดที่จะลบออก และเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="35535-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="35535-139">สำหรับรายการ ""ของที่เป็นที่ชื่นชอบด้วย"" หรือ "ของซื้อที่รวมกันบ่อยๆ"</span><span class="sxs-lookup"><span data-stu-id="35535-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="35535-140">ในบริบทของรายการ "ของซื้อด้วยกันบ่อยครั้ง" หรือ "ของที่เป็นที่ชื่นชอบด้วย" Machine Learning ถูกใช้ในการวิเคราะห์รูปแบบการซื้อของผู้ใช้เพื่อแนะนำผลิตภัณฑ์ที่เกี่ยวข้องโดยทั่วไปที่ซื้อร่วมกันสำหรับผลิตภัณฑ์เริ่มต้นที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="35535-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="35535-141">*ผลิตภัณฑ์เมล็ดพันธุ์* คือผลิตภัณฑ์ที่คุณต้องการสร้างผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="35535-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="35535-142">ในบริบทของการปรับปรุงรายการแนะนำด้วยตนเอง คุณกำลังเพิ่มหรือลบผลลัพธ์สำหรับผลิตภัณฑ์นี้</span><span class="sxs-lookup"><span data-stu-id="35535-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="35535-143">ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มหรือลบผลลัพธ์สำหรับผลิตภัณฑ์เมล็ดพันธุ์ด้วยตนเอง:</span><span class="sxs-lookup"><span data-stu-id="35535-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="35535-144">เลือก **ผลิตภัณฑ์เมล็ดพันธุ์**</span><span class="sxs-lookup"><span data-stu-id="35535-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="35535-145">ภายใต้คอลัมน์ **ผลิตภัณฑ์** ให้ค้นหาผลิตภัณฑ์ตาม **ชื่อ** หรือ **หมายเลขผลิตภัณฑ์**
![ตัวอย่างของการค้นหาผลิตภัณฑ์ในรายการที่ซื้อร่วมกันบ่อย](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="35535-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="35535-146">ภายใต้คอลัมน์ **ชนิดบรรทัด** ให้เลือกตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="35535-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="35535-147">**รวม** – บังคับผลิตภัณฑ์ให้กับด้านหน้าของรายการ</span><span class="sxs-lookup"><span data-stu-id="35535-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="35535-148">**ไม่รวม** – ลบผลิตภัณฑ์ออกจากการปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="35535-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="35535-149">![ตัวอย่างของการรวมหรือไม่รวมผลิตภัณฑ์ในรายการซื้อที่รวมกันบ่อยๆ](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="35535-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="35535-150">เมื่อต้องการลบผลิตภัณฑ์ออกจากตาราง: ให้เลือกบรรทัดที่จะลบออก และเลือก ลบ</span><span class="sxs-lookup"><span data-stu-id="35535-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="35535-151">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="35535-151">Additional resources</span></span>

[<span data-ttu-id="35535-152">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="35535-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="35535-153">เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="35535-153">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="35535-154">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="35535-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="35535-155">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="35535-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="35535-156">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="35535-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="35535-157">เพิ่มรายการคำแนะนำลงในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="35535-157">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="35535-158">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="35535-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="35535-159">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="35535-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="35535-160">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="35535-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="35535-161">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="35535-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="35535-162">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="35535-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
