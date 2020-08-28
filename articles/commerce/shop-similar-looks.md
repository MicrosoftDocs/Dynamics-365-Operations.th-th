---
title: เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"
description: หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ "เลือกซื้อสินค้าที่คล้ายกัน" ใน Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2e57965a1073982a7b6c34b79dbf6e5b90d7ee30
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666319"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="36069-103">เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="36069-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="36069-104">หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ "เลือกซื้อสินค้าที่คล้ายกัน" ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="36069-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="36069-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="36069-105">Overview</span></span>

<span data-ttu-id="36069-106">คุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" ใน Dynamics 365 Commerce ใช้ความสามารถของปัญญาประดิษฐ์และการเรียนรู้ของเครื่อง (AI-ML) เพื่อให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่คล้ายกันแก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="36069-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="36069-107">ด้วยการทำให้คำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" สามารถใช้ได้สำหรับช่องทางการขายปลีกทั้งหมดใน Commerce ร้านค้าปลีกสามารถเพิ่มความพึงพอใจของลูกค้าโดยการช่วยให้ลูกค้าพบสิ่งที่ต้องการได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="36069-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="36069-108">ฟังก์ชันคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" ใช้ภาพผลิตภัณฑ์ของผลิตภัณฑ์ย่อยเบื้องต้นในการค้นหาและเสนอแนะผลิตภัณฑ์ที่คล้ายกันแบบเป็นภาพในแคตตาล็อกผลิตภัณฑ์ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="36069-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="36069-109">คำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" มีให้ใช้งานในทั้งการขายหน้าร้าน (POS) และอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="36069-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="36069-110">สถานการณ์จำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="36069-110">Example scenarios</span></span>

- <span data-ttu-id="36069-111">ลูกค้าดูเสื้อกันหนาวที่มีแถบสีดำและได้รับการแนะนำเสื้อกันหนาวที่คล้ายกันเป็นสีแดง</span><span class="sxs-lookup"><span data-stu-id="36069-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="36069-112">ลูกค้าเลือกผลิตภัณฑ์ที่แนะนำแทนที่จะเป็นผลิตภัณฑ์ที่ดูไว้แต่เดิมและได้รับคำแนะนำสำหรับผลิตภัณฑ์ที่คล้ายกันที่เป็นสีแดง</span><span class="sxs-lookup"><span data-stu-id="36069-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="36069-113">ลูกค้าใช้คำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" เพื่อค้นหาต่างหูที่เข้าคู่กันกับแหวนที่ลูกค้าสนใจจะซื้อ</span><span class="sxs-lookup"><span data-stu-id="36069-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="36069-114">เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="36069-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="36069-115">คำแนะนำผลิตภัณฑ์รองรับเฉพาะสำหรับผู้ใช้ Commerce ที่โอนย้ายที่เก็บข้อมูลของตนไปโดยใช้ Azure Data Lake Gen2 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="36069-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="36069-116">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="36069-116">Prerequisites</span></span>

<span data-ttu-id="36069-117">ก่อนที่ร้านค้าปลีกสามารถเริ่มแสดงคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" ให้แก่ลูกค้า มีขั้นตอนที่เป็นข้อกำหนดเบื้องต้นสองประการดังนี้</span><span class="sxs-lookup"><span data-stu-id="36069-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="36069-118">[เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md) ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="36069-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="36069-119">ยืนยันว่าเซิร์ฟเวอร์สื่อสนับสนุนการเรียก HTTPS</span><span class="sxs-lookup"><span data-stu-id="36069-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="36069-120">สำหรับโปรแกรมคำแนะนำในการเข้าถึงภาพผลิตภัณฑ์ ร้านค้าปลีกต้องสร้าง URL ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36069-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="36069-121">เมื่อต้องการสร้าง URL ของผลิตภัณฑ์ในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="36069-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="36069-122">ไปที่ **รูปภาพผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="36069-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="36069-123">ในบานหน้าต่างการดำเนินการ ให้เลือก **กำหนดเท็มเพลตสื่อ**</span><span class="sxs-lookup"><span data-stu-id="36069-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="36069-124">ในบานหน้าต่างคุณสมบัติ **กำหนดเท็มเพลตสื่อ** ภายใต้ **URL ของสื่อ** ให้เลือก **สร้าง URL**</span><span class="sxs-lookup"><span data-stu-id="36069-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="36069-125">เมื่อคุณเปิดใช้งานคุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" กระบวนการสร้างรายการแนะนำผลิตภัณฑ์จะเริ่มต้นขึ้น</span><span class="sxs-lookup"><span data-stu-id="36069-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="36069-126">อาจต้องใช้เวลาสูงสุดหนึ่งวัน ก่อนที่รายการเหล่านั้นจะพร้อมใช้งานและสามารถมองเห็นได้ทางออนไลน์และที่เทอร์มินัล POS</span><span class="sxs-lookup"><span data-stu-id="36069-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="36069-127">เมื่อต้องการเปิดใช้งานคุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" ในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="36069-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="36069-128">ไปที่ **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="36069-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="36069-129">ในรายการของคุณลักษณะที่พร้อมใช้งาน ให้ค้นหาและเลือก **เลือกซื้อสินค้าที่คล้ายกัน**</span><span class="sxs-lookup"><span data-stu-id="36069-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="36069-130">ในบานหน้าต่างด้านขวา ให้เลือก **เปิดใช้งาน** เพื่อเปิดใช้บริการ</span><span class="sxs-lookup"><span data-stu-id="36069-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="36069-131">ภาพประกอบต่อไปนี้แสดงคุณลักษณะ **เลือกซื้อสินค้าที่คล้ายกัน** บนหน้า **การจัดการคุณลักษณะ** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="36069-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![คุณลักษณะเลือกซื้อสินค้าที่คล้ายกันบนหน้าการจัดการคุณลักษณะในศูนย์ควบคุม Commerce](./media/enableshopsimilarlooks.png)

<span data-ttu-id="36069-133">หลังจากที่งานก่อนหน้านี้เสร็จสมบูรณ์ แล้วเทอร์มินัล POS จะถูกปรับปรุงโดยอัตโนมัติด้วยแผง **เลือกซื้อสินค้าที่คล้ายกัน**</span><span class="sxs-lookup"><span data-stu-id="36069-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="36069-134">ด้วยการเลือก **ดูเพิ่มเติม** ผู้ใช้เทอร์มินัล POS จะถูกนำไปยังหน้า "เลือกซื้อสินค้าที่คล้ายกัน" เฉพาะซึ่งสามารถกรองข้อมูลเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="36069-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="36069-135">ถ้าคุณปิดคุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" จะไม่ส่งผลต่อคำแนะนำผลิตภัณฑ์ชนิดอื่น</span><span class="sxs-lookup"><span data-stu-id="36069-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="36069-136">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ ดู [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="36069-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="36069-137">เพิ่มปุ่มเลือกซื้อสินค้าที่คล้ายกันในหน้ารายละเอียดผลิตภัณฑ์โดยใช้ตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="36069-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="36069-138">หลังจากที่คุณเปิดใช้งานคุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน" ในศูนย์ควบคุม Commerce ตัวเลือกในตัวสร้างไซต์ Commerce จะให้ร้านค้าปลีกสามารถเพิ่มปุ่ม **เลือกซื้อสินค้าที่คล้ายกัน** ในกล่องสั่งซื้อบนหน้ารายละเอียดของผลิตภัณฑ์ (PDP)</span><span class="sxs-lookup"><span data-stu-id="36069-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="36069-139">ลูกค้าที่เลือกปุ่มนี้จะถูกนำไปที่หน้า "เลือกซื้อสินค้าที่คล้ายกัน" เฉพาะซึ่งแสดงภาพผลิตภัณฑ์ที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="36069-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="36069-140">ลูกค้าสามารถใช้ตัวเลือกเพื่อกรองข้อมูลผลิตภัณฑ์เพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="36069-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="36069-141">หากต้องการเพิ่มปุ่ม **เลือกซื้อสินค้าที่คล้ายกัน** ใน PDP โดยใช้ตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="36069-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="36069-142">เปิดหน้าตัวสร้างไซต์ที่มีอยู่ซึ่งมีโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="36069-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="36069-143">ในหน้าต่างการนำทางทางด้านซ้าย เลือกโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="36069-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="36069-144">ในบานหน้าต่างนำทางขวา ให้เลือกกล่องกาเครื่องหมาย **เปิดใช้งานลิงก์เลือกซื้อสินค้าที่คล้ายกัน**</span><span class="sxs-lookup"><span data-stu-id="36069-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="36069-145">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="36069-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="36069-146">หลังจากเผยแพร่หน้าแล้ว PDP จะมีปุ่ม **เลือกซื้อสินค้าที่คล้ายกัน**</span><span class="sxs-lookup"><span data-stu-id="36069-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="36069-147">ภาพประกอบต่อไปนี้แสดงกล่องกาเครื่องหมาย **เปิดใช้งานลิงก์เลือกซื้อสินค้าที่คล้ายกัน** และปุ่ม **เลือกซื้อสินค้าที่คล้ายกัน** บน PDP ตัวอย่างในตัวสร้างในไซต์</span><span class="sxs-lookup"><span data-stu-id="36069-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![กล่องกาเครื่องหมายเปิดใช้งานลิงก์เลือกซื้อสินค้าที่คล้ายกันและปุ่มเลือกซื้อสินค้าที่คล้ายกันบน PDP ตัวอย่างในตัวสร้างในไซต์](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="36069-149">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="36069-149">Additional resources</span></span>

[<span data-ttu-id="36069-150">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36069-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="36069-151">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="36069-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="36069-152">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36069-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="36069-153">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="36069-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="36069-154">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="36069-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="36069-155">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="36069-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="36069-156">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="36069-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="36069-157">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="36069-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="36069-158">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="36069-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="36069-159">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="36069-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
