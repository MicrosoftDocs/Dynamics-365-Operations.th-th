---
title: ภาพรวมของหน้ารายละเอียดผลิตภัณฑ์
description: หัวข้อนี้แสดงภาพรวมของหน้ารายละเอียดผลิตภัณฑ์ (PDPs) ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697876"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="c2a6d-103">ภาพรวมของหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c2a6d-104">หัวข้อนี้แสดงภาพรวมของหน้ารายละเอียดผลิตภัณฑ์ (PDPs) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c2a6d-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c2a6d-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="c2a6d-105">Overview</span></span>

<span data-ttu-id="c2a6d-106">PDP แสดงข้อมูลรายละเอียดเกี่ยวกับผลิตภัณฑ์ และให้ลูกค้าของเราเลือกตัวเลือกผลิตภัณฑ์ เช่น ขนาดลักษณะและสี</span><span class="sxs-lookup"><span data-stu-id="c2a6d-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="c2a6d-107">PDP ควรแสดงข้อมูลผลิตภัณฑ์ทั้งหมดที่ลูกค้าต้องการ เพื่อตัดสินใจซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="c2a6d-108">ในแผนภาพต่อไปนี้แสดงตัวอย่างของ PDP</span><span class="sxs-lookup"><span data-stu-id="c2a6d-108">The following illustration shows an example of a PDP.</span></span>

![ตัวอย่างของหน้ารายละเอียดผลิตภัณฑ์](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="c2a6d-110">โมดูลส่วนหัวและส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="c2a6d-110">Header and footer modules</span></span>

<span data-ttu-id="c2a6d-111">ด้านบนสุดของ PDP มีส่วนหัวที่แสดงประเภทผลิตภัณฑ์ทั้งหมด และหน้าอื่นๆที่ผู้ค้าปลีกต้องการให้ลูกค้าเรียกดู</span><span class="sxs-lookup"><span data-stu-id="c2a6d-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="c2a6d-112">ด้านล่างของหน้า มีส่วนท้ายที่มีลิงก์ลัดไปยังหัวข้อต่าง ๆ ที่อาจทำให้ลูกค้าสนใจ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="c2a6d-113">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-113">Buy box module</span></span>

<span data-ttu-id="c2a6d-114">โมดูลที่สำคัญที่สุดบน PDP คือโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="c2a6d-115">ดังนั้น จึงเป็นรายการแรกในส่วนหลักของหน้า</span><span class="sxs-lookup"><span data-stu-id="c2a6d-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="c2a6d-116">โมดูลกล่องการซื้อเป็นโมดูลคอนเทนเนอร์และโฮสต์หลายโมดูลที่มีข้อมูลที่สำคัญที่สุดเกี่ยวกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="c2a6d-117">ข้อมูลนี้รวมถึง ชื่อผลิตภัณฑ์ รูปภาพผลิตภัณฑ์ คำอธิบายราคา และการจัดอันดับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="c2a6d-118">โมดูลกล่องการซื้อช่วยให้ลูกค้าเลือกตัวเลือกผลิตภัณฑ์ (ตัวอย่างเช่น ขนาด ลักษณะ และสี) และเพิ่มผลิตภัณฑ์ลงในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="c2a6d-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="c2a6d-119">นอกจากนี้ยังช่วยให้ลูกค้าซื้อผลิตภัณฑ์ออนไลน์และรับสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="c2a6d-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="c2a6d-120">โมดูลการซื้อออนไลน์และการรับสินค้าในร้านค้า จะใช้การรวมกับแอพลิเคชันโปรแกรมมิ่งอินเทอร์เฟส (APIs) ของ Bing Maps เพื่อค้นหาสถานที่เก็บหรือร้านค้าใกล้เคียงที่ลูกค้าระบุ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="c2a6d-121">โมดูลกล่องการซื้อต้องใช้รหัสผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="c2a6d-122">รหัสนี้ได้รับมาจากบริบทของหน้า</span><span class="sxs-lookup"><span data-stu-id="c2a6d-122">This ID is derived from the page context.</span></span> <span data-ttu-id="c2a6d-123">ถ้ามีการเพิ่มโมดูลกล่องการซื้อในหน้าที่จัดเก็บไว้ในหน้าซึ่งบริบทของหน้าไม่มีหมายเลขผลิตภัณฑ์ จะแสดงข้อมูลอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c2a6d-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="c2a6d-124">โมดูลข้อมูลจำเพาะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-124">Product specifications module</span></span>

<span data-ttu-id="c2a6d-125">โมดูลข้อมูลจำเพาะของผลิตภัณฑ์ สามารถใช้เพื่อแสดงรายละเอียดเพิ่มเติมเกี่ยวกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="c2a6d-126">รายละเอียดเหล่านี้นำมาจากคุณลักษณะของผลิตภัณฑ์ใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="c2a6d-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="c2a6d-127">โมดูลเฉพาะของผลิตภัณฑ์จะแสดงทุกแอททริบิวต์ที่มีการตั้งค่าคุณสมบัติ **ที่มองเห็นได้** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="c2a6d-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="c2a6d-128">ต้องใช้รหัสผลิตภัณฑ์เพื่อดึงข้อมูลแอททริบิวต์ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="c2a6d-129">โมดูลคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-129">Recommendations module</span></span>

<span data-ttu-id="c2a6d-130">โมดูลคำแนะนำเป็นโมดูลที่สำคัญบนโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="c2a6d-131">ในขณะที่ลูกค้าเลือกดูผลิตภัณฑ์แควรมีตัวเลือกผลิตภัณฑ์เพิ่มเติมแสดงให้เห็น เพื่อให้สามารถค้นหาผลิตภัณฑ์ที่ถูกต้องและทำการซื้อได้</span><span class="sxs-lookup"><span data-stu-id="c2a6d-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="c2a6d-132">คำแนะนำช่วยลูกค้าในการค้นหาเนื้อหาที่เกี่ยวข้องและดำเนินการการซื้อต่อไป</span><span class="sxs-lookup"><span data-stu-id="c2a6d-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="c2a6d-133">ชนิดของรายการคำแนะนำต่าง ๆ มีดังนี้</span><span class="sxs-lookup"><span data-stu-id="c2a6d-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="c2a6d-134">**ผู้คนยังชื่นชอบ** การแสดงรายการตาม Machine Learning</span><span class="sxs-lookup"><span data-stu-id="c2a6d-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="c2a6d-135">ใช้ประวัติธุรกรรมของลูกค้ารายอื่นเพื่อให้คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="c2a6d-136">รายการนี้จะถูกสร้างขึ้นโดยบริการคำแนะนำและลักษณะการทำงานรายการ "ลูกค้าที่ซื้อนี้ยังซื้อ ..."</span><span class="sxs-lookup"><span data-stu-id="c2a6d-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="c2a6d-137">ต้องระบุรหัสผลิตภัณฑ์เพื่อสร้างรายการนี้</span><span class="sxs-lookup"><span data-stu-id="c2a6d-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="c2a6d-138">สามารถตั้งค่าคอนฟิกรายการที่ **เกี่ยวข้อง** สำหรับผลิตภัณฑ์ใน Retail</span><span class="sxs-lookup"><span data-stu-id="c2a6d-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="c2a6d-139">ตัวอย่างเช่น สำหรับกระเป๋าเดินทางหนังสีน้ำตาล ต้องมีกระเป๋าถือที่เป็นหนังหรือมีการออกแบบเพื่อวัตถุประสงค์ในการเดินทาง ที่สามารถตั้งค่าคอนฟิกสำหรับรายการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c2a6d-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="c2a6d-140">ชนิดอื่นๆของรายการที่เกี่ยวข้อง เช่น **อุปกรณ์เสริม** และ **อื่น ๆ** ที่ยังสามารถตั้งค่าคอนฟิกใน Retail ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="c2a6d-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="c2a6d-141">ต้องระบุรหัสผลิตภัณฑ์เพื่อสร้างรายการนี้</span><span class="sxs-lookup"><span data-stu-id="c2a6d-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="c2a6d-142">ดังนั้น ถ้ามีการเพิ่มเข้าในหน้าหลักโดยที่บริบทของหน้าไม่มีรหัสผลิตภัณฑ์รายการจะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="c2a6d-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="c2a6d-143">การสร้างรายการแนะนำโดยอัลกอริทึม เช่น **ยอดนิยม** **ขายดี** **ใหม่** สามารถใช้ใน PDPs</span><span class="sxs-lookup"><span data-stu-id="c2a6d-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="c2a6d-144">ถึงแม้ว่ารายการเหล่านี้อาจไม่เกี่ยวข้องโดยตรงกับผลิตภัณฑ์บน PDP แต่ก็เป็นอีกวิธีหนึ่งที่จะช่วยให้ลูกค้าสามารถค้นหาผลิตภัณฑ์ที่อาจสนใจได้</span><span class="sxs-lookup"><span data-stu-id="c2a6d-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="c2a6d-145">ชนิดของรายการเหล่านี้ไม่จำเป็นต้องใช้หมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="c2a6d-146">เป็นรายการทั่วไปที่สร้างขึ้นตามรูปแบบการช้อปปิ้งทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="c2a6d-147">รายการที่บรรณาธิการแนะนำเป็นรายการที่มีการสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c2a6d-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="c2a6d-148">ตัวอย่างเช่น ผู้ค้าปลีกอาจตัดสินใจเลือกจัดการของผลิตภัณฑ์ที่ต้องการแสดงด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c2a6d-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="c2a6d-149">โมดูลการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-149">Ratings and reviews module</span></span>

<span data-ttu-id="c2a6d-150">โมดูลการให้คะแนนและบทวิจารณ์ แสดงให้เห็นถึงการให้คะแนนและบทวิจารณ์ที่ให้ไว้โดยลูกค้ารายอื่น</span><span class="sxs-lookup"><span data-stu-id="c2a6d-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="c2a6d-151">นอกจากนี้ยังช่วยให้ลูกค้าสามารถเขียนบทวิจารณ์ของตนเองได้บนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="c2a6d-152">นอกจากนี้ยังมีฮิสโตแกรมที่แสดงแนวโน้มการจัดอันดับสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="c2a6d-153">สำหรับรายละเอียดเพิ่มเติม ดู [ภาพรวมการให้คะแนนและบทวิจารณ์](ratings-reviews-overview.md)</span><span class="sxs-lookup"><span data-stu-id="c2a6d-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="c2a6d-154">โมดูลการตลาด</span><span class="sxs-lookup"><span data-stu-id="c2a6d-154">Marketing modules</span></span>

<span data-ttu-id="c2a6d-155">ถ้าเนื้อหาทางการตลาดจำเพาะสำหรับผลิตภัณฑ์หนึ่ง ๆ คุณสามารถเพิ่มโมดูลทางการตลาดใด ๆ เข้ากับ PDP</span><span class="sxs-lookup"><span data-stu-id="c2a6d-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="c2a6d-156">คุณสามารถเพิ่มโมดูลทางการตลาดให้กับ PDP โดยการ "การเพิ่มความสมบูรณ์" ให้กับหน้า</span><span class="sxs-lookup"><span data-stu-id="c2a6d-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="c2a6d-157">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c2a6d-157">Additional resources</span></span>

[<span data-ttu-id="c2a6d-158">ภาพรวมของโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="c2a6d-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="c2a6d-159">ภาพรวมของหน้าเริ่มต้นของประเภทและหน้าผลการค้นหาค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c2a6d-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="c2a6d-160">ภาพรวมของหน้ารถเข็นและการเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="c2a6d-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="c2a6d-161">ภาพรวมของหน้าการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c2a6d-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
