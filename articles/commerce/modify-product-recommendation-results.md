---
title: จัดการผลลัพธ์ของคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML
description: หัวข้อนี้จะอธิบายถึงวิธีการปรับแต่งผลลัพธ์ของคำแนะนำผลิตภัณฑ์โดยใช้การเรียนรู้เครื่องมือปัญญาประดิษฐ์ (AI-ML) กับธุรกิจของคุณ
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770081"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="0065d-103">จัดการผลลัพธ์ของคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML</span><span class="sxs-lookup"><span data-stu-id="0065d-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0065d-104">หัวข้อนี้จะอธิบายถึงวิธีการปรับแต่งผลลัพธ์ของคำแนะนำผลิตภัณฑ์โดยใช้การเรียนรู้เครื่องมือปัญญาประดิษฐ์ (AI-ML) กับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="0065d-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="0065d-105">หลังจากเปิดใช้งานคำแนะนำผลิตภัณฑ์แล้ว การตั้งค่าเริ่มต้นจะมีผลบังคับใช้ พารามิเตอร์เหล่านี้จะทำงานสำหรับความต้องการหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="0065d-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="0065d-106">วิธีการที่ดีที่สุดคือการวางแผนในการใช้เวลาในการประเมินว่าผลลัพธ์มีความเหมาะสมกับการเคลื่อนไหวทางการขายของผลิตภัณฑ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0065d-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="0065d-107">เราขอแนะนำให้ประเมินผลลัพธ์เป็นเวลาสองสามวันก่อนที่จะเปลี่ยนพารามิเตอร์ตามต้องการก่อนการทดสอบอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0065d-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="0065d-108">การทำความเข้าใจเกี่ยวกับพารามิเตอร์รายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="0065d-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="0065d-109">ก่อนที่จะเปลี่ยนพารามิเตอร์ ให้เรียนรู้ว่าจะส่งผลกระทบต่อผลลัพธ์อย่างไรตามด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="0065d-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="0065d-110">รายการผลิตภัณฑ์ยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="0065d-110">Trending product list</span></span>

<span data-ttu-id="0065d-111">รายการผลิตภัณฑ์ **ยอดนิยม** ที่มีความนิยมมีสองพารามิเตอร์ที่สามารถเปลี่ยนแปลงได้ ![พารามิเตอร์เริ่มต้นของรายการยอดนิยมที่เป็นตัวอย่าง](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="0065d-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="0065d-112">**รวมผลิตภัณฑ์ใหม่จาก X วันล่าสุด** - ผลิตภัณฑ์ที่มีการเพิ่มภายในจำนวนวันที่ระบุไว้ก่อนที่จะสามารถใช้วันที่ปัจจุบันเพื่อเลือกผู้สมัครผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0065d-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="0065d-113">ค่าเริ่มต้นในรูปภาพแสดงให้เห็นว่าผลิตภัณฑ์ที่มีอายุ 180 วันสามารถใช้ได้ในรายการผลิตภัณฑ์ยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="0065d-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="0065d-114">**รวมการขายใหม่จาก X วันล่าสุด** - ธุรกรรมการขายที่เกิดขึ้นในจำนวนวันที่ระบุไว้ก่อนที่จะสามารถใช้วันที่ปัจจุบันสามารถใช้เพื่อสั่งซื้อสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="0065d-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="0065d-115">ค่าเริ่มต้นข้างต้นจะแนะนำว่าการสั่งซื้อทั้งหมดของผลิตภัณฑ์ใน 30 วันที่ผ่านมาจะใช้ในการกำหนดตำแหน่งของผลิตภัณฑ์ในรายการผลิตภัณฑ์ยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="0065d-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="0065d-116">รายการผลิตภัณฑ์ที่ขายดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="0065d-116">Best selling product list</span></span>

<span data-ttu-id="0065d-117">ทั้งนี้ขึ้นอยู่กับธุรกิจของคุณ การขายที่ดีที่สุดอาจนำผลลัพธ์ที่แตกต่างจากรายการยอดนิยม ถึงแม้ว่าทั้งสองจะใช้ข้อมูลธุรกรรมเพื่อสั่งผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0065d-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="0065d-118">เนื่องจากการขายที่ดีที่สุดไม่มีการตัดออกตามวันที่จัดประเภท การขายที่ดีที่สุดยังคงเน้นความนิยมมากที่สุด ผลิตภัณฑ์ที่เก่ากว่าอาจตกลงจากรายการยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="0065d-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="0065d-119">รายการผลิตภัณฑ์ **ที่ขายดีที่สุด** มีพารามิเตอร์เดียวที่สามารถเปลี่ยนแปลงได้:</span><span class="sxs-lookup"><span data-stu-id="0065d-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![ตัวอย่างพารามิเตอร์เริ่มต้นสำหรับรายการขายที่ดีที่สุด](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="0065d-121">**รวมการขายใหม่จาก X วันล่าสุด** - ธุรกรรมการขายที่เกิดขึ้นในจำนวนวันที่ระบุไว้ก่อนที่จะสามารถใช้วันที่ปัจจุบันสามารถใช้เพื่อสั่งซื้อสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="0065d-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="0065d-122">ค่าเริ่มต้นข้างต้นจะแนะนำว่าการสั่งซื้อทั้งหมดของผลิตภัณฑ์ใน 30 วันที่ผ่านมาจะใช้ในการกำหนดตำแหน่งของผลิตภัณฑ์ในรายการผลิตภัณฑ์ที่ขายดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="0065d-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="0065d-123">เพิ่มหรือลบผลิตภัณฑ์ออกจากรายการคำแนะนำด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0065d-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="0065d-124">สำหรับสินค้าใหม่ ยอดนิยม หรือขายดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="0065d-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="0065d-125">ไปที่ **การขายปลีก** > **คำแนะนำของผลิตภัณฑ์** > **พารามิเตอร์คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="0065d-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="0065d-126">ในรายการพารามิเตอร์ที่ใช้ร่วมกันของการขายปลีก เลือก **รายการแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="0065d-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="0065d-127">เลือกรายการที่จะเพิ่มหรือลบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0065d-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="0065d-128">ในการเพิ่มผลิตภัณฑ์ไปยังตาราง ให้เลือก **เพิ่มบรรทัด**</span><span class="sxs-lookup"><span data-stu-id="0065d-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="0065d-129">ภายใต้คอลัมน์ผลิตภัณฑ์ ให้ค้นหาผลิตภัณฑ์ตาม **ชื่อ** หรือ **หมายเลขผลิตภัณฑ์** 
![ตัวอย่างของการค้นหาผลิตภัณฑ์ในรายการผลิตภัณฑ์ใหม่](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="0065d-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="0065d-130">ภายใต้คอลัมน์ชนิดบรรทัด ให้เลือกตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0065d-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="0065d-131">**รวม** – บังคับผลิตภัณฑ์ให้กับด้านหน้าของรายการ</span><span class="sxs-lookup"><span data-stu-id="0065d-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="0065d-132">**ไม่รวม** – ลบผลิตภัณฑ์ออกจากที่ปรากฏในรายการ ![ตัวอย่างของการรวมหรือไม่รวมผลิตภัณฑ์จากรายการผลิตภัณฑ์ใหม่](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="0065d-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="0065d-133">การเปลี่ยน **ลำดับการแสดง** จะเปลี่ยนลำดับของผลิตภัณฑ์ที่มีการทำเครื่องหมาย **รวม** จะปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="0065d-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="0065d-134">ถ้าผลิตภัณฑ์สองตัวมีค่าของ **ลำดับการแสดงผล** เดียวกัน ใบสั่งสุดท้ายของผลลัพธ์สองอย่างอาจแตกต่างจากฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="0065d-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="0065d-135">เมื่อต้องการลบผลิตภัณฑ์ออกจากตาราง: ให้เลือกบรรทัดที่จะลบออก และเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="0065d-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="0065d-136">สำหรับรายการที่คนชอบหรือซื้อที่รวมกันบ่อยๆ</span><span class="sxs-lookup"><span data-stu-id="0065d-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="0065d-137">ในบริบทของรายการ **ซื้อด้วยกันบ่อยครั้ง** หรือ **ผู้คนยังชอบสิ่งนี้ด้วย** การเรียนรู้ของเครื่องใช้ในการวิเคราะห์รูปแบบการซื้อของผู้บริโภคเพื่อแนะนำผลิตภัณฑ์ที่เกี่ยวข้องโดยทั่วไปที่ซื้อร่วมกันสำหรับผลิตภัณฑ์เมล็ดพันธุ์ที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="0065d-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="0065d-138">**ผลิตภัณฑ์เมล็ดพันธุ์** คือผลิตภัณฑ์ที่คุณต้องการสร้างผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0065d-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="0065d-139">ในบริบทของการปรับปรุงรายการแนะนำด้วยตนเอง คุณกำลังเพิ่มหรือลบผลลัพธ์สำหรับผลิตภัณฑ์นี้</span><span class="sxs-lookup"><span data-stu-id="0065d-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="0065d-140">ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มหรือลบผลลัพธ์สำหรับผลิตภัณฑ์เมล็ดพันธุ์ด้วยตนเอง:</span><span class="sxs-lookup"><span data-stu-id="0065d-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="0065d-141">เลือก **ผลิตภัณฑ์เมล็ดพันธุ์**</span><span class="sxs-lookup"><span data-stu-id="0065d-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="0065d-142">ภายใต้คอลัมน์ **ผลิตภัณฑ์** ให้ค้นหาผลิตภัณฑ์ตาม **ชื่อ** หรือ **หมายเลขผลิตภัณฑ์**
![ตัวอย่างของการค้นหาผลิตภัณฑ์ในรายการที่ซื้อร่วมกันบ่อย](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="0065d-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="0065d-143">ภายใต้คอลัมน์ **ชนิดบรรทัด** ให้เลือกตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0065d-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="0065d-144">**รวม** – บังคับผลิตภัณฑ์ให้กับด้านหน้าของรายการ</span><span class="sxs-lookup"><span data-stu-id="0065d-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="0065d-145">**ไม่รวม** – ลบผลิตภัณฑ์ออกจากการปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="0065d-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="0065d-146">![ตัวอย่างของการรวมหรือไม่รวมผลิตภัณฑ์ในรายการซื้อที่รวมกันบ่อยๆ](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="0065d-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="0065d-147">เมื่อต้องการลบผลิตภัณฑ์ออกจากตาราง: ให้เลือกบรรทัดที่จะลบออก และเลือก ลบ</span><span class="sxs-lookup"><span data-stu-id="0065d-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="0065d-148">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0065d-148">Additional resources</span></span>

[<span data-ttu-id="0065d-149">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0065d-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="0065d-150">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0065d-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="0065d-151">เพิ่มรายการคำแนะนำผลิตภัณฑ์ลงในหน้า</span><span class="sxs-lookup"><span data-stu-id="0065d-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
