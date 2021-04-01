---
title: เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน"
description: หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" ใน Microsoft Dynamics 365 Commerce
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234400"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="337bf-103">เปิดใช้งานคำแนะนำ "คำอธิบายเลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="337bf-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="337bf-104">หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="337bf-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="337bf-105">คุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" ใน Dynamics 365 Commerce ใช้ปัญญาประดิษฐ์และการเรียนรู้ของเครื่อง (AI-ML) เพื่อให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่คำอธิบายคล้ายกันกับสิ่งที่ลูกค้ากำลังมองหา</span><span class="sxs-lookup"><span data-stu-id="337bf-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="337bf-106">ด้วยการทำให้คำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" สามารถใช้ได้สำหรับช่องทางการขายปลีกทั้งหมดใน Commerce ร้านค้าปลีกสามารถรช่วยให้ลูกค้าพบสิ่งที่ต้องการได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="337bf-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="337bf-107">ฟังก์ชันคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" ใช้ชื่อผลิตภัณฑ์ของคำอธิบายผลิตภัณฑ์ย่อยเบื้องต้นในการค้นหาและเสนอแนะผลิตภัณฑ์ที่คล้ายกันในแคตตาล็อกผลิตภัณฑ์ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="337bf-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="337bf-108">คำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" มีให้ใช้งานในทั้งการขายหน้าร้าน (POS) และอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="337bf-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="337bf-109">สถานการณ์จำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="337bf-109">Example scenarios</span></span>

<span data-ttu-id="337bf-110">ตัวอย่างต่อไปนี้แสดงชนิดของข้อแนะอธิบายที่ฟังก์ชัน "ซื้อสินค้าที่คำอธิบายคล้ายกัน" สามารถมีได้</span><span class="sxs-lookup"><span data-stu-id="337bf-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="337bf-111">ลูกค้ารายหนึ่งกำลังดูแว่นตาทรง Horn-rimmed สไตล์เรโทรและได้รับชุดข้อแนะนาใหม่ให้กับแว่นตาอื่นๆ ที่มีการออกแบบที่คล้ายกัน และเป็นบริบทของอุตสาหกรรมค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="337bf-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="337bf-112">ลูกค้ารายหนึ่งใช้ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" เพื่อพบสินค้าประเภทหนึ่ง ๆ ซึ่งคล้ายกับหนึ่งเริ่มต้นที่ซื้อมาก่อนหน้านี้จากผู้ค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="337bf-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="337bf-113">ตั้งค่าคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="337bf-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="337bf-114">คำแนะนำผลิตภัณฑ์รองรับเฉพาะสำหรับผู้ใช้ Commerce ที่โอนย้ายที่เก็บข้อมูลของตนไปโดยใช้ Azure Data Lake Storage Gen2 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="337bf-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="337bf-115">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="337bf-115">Prerequisites</span></span>

<span data-ttu-id="337bf-116">ก่อนที่สามารถแสดงคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน"ให้แก่ลูกค้าได้ คุณต้องปฏิบัติตามข้อแนะเบื้องต้นต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="337bf-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="337bf-117">[เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md) ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="337bf-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="337bf-118">ยืนยันว่าเซิร์ฟเวอร์สื่อสนับสนุนการเรียก HTTPS</span><span class="sxs-lookup"><span data-stu-id="337bf-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="337bf-119">เปิดใช้งานคุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="337bf-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="337bf-120">เมื่อต้องการเปิดใช้งานคุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" ในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="337bf-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="337bf-121">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ในรายการคุณลักษณะที่พร้อมใช้งาน ให้ค้นหาและเลือก **เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน**</span><span class="sxs-lookup"><span data-stu-id="337bf-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="337bf-122">ในบานหน้าต่างด้านขวา เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="337bf-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="337bf-123">เมื่อคุณเปิดคุณลักษณะเช่นนี้ ระบบจะเริ่มต้นสร้างรายการแนะนำเกี่ยวกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="337bf-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="337bf-124">อาจต้องใช้เวลาสูงสุดหนึ่งวัน ก่อนที่รายการเหล่านั้นจะพร้อมใช้งานและสามารถมองเห็นได้ทางออนไลน์และที่เทอร์มินัล POS</span><span class="sxs-lookup"><span data-stu-id="337bf-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="337bf-125">ถ้าคุณปิดคุณลักษณะ การแนะนำผลิตภัณฑ์ชนิดอื่นๆ จะไม่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="337bf-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="337bf-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ ดู [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="337bf-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="337bf-127">เพิ่มปุ่มอธิบายที่คล้ายกันของร้านค้าลงในหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="337bf-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="337bf-128">หลังจากที่คุณเปิดใช้งานคุณลักษณะคำแนะนำ "เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน" ในศูนย์ควบคุม Commerce คุณสามารถเพิ่มปุ่ม **เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน** ในกล่องสั่งซื้อบนหน้ารายละเอียดของผลิตภัณฑ์ (PDP)</span><span class="sxs-lookup"><span data-stu-id="337bf-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="337bf-129">ลูกค้าที่เลือกปุ่มนี้จะถูกนำไปที่หน้า **เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน** เฉพาะซึ่งแสดงภาพผลิตภัณฑ์ที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="337bf-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="337bf-130">ลูกค้าสามารถใช้ตัวเลือกเพื่อกรองข้อมูลผลิตภัณฑ์เพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="337bf-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="337bf-131">หากต้องการเพิ่มปุ่ม **เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน** ใน PDP โดยใช้ตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="337bf-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="337bf-132">เปิดหน้าตัวสร้างไซต์ที่มีอยู่ซึ่งมีโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="337bf-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="337bf-133">ในหน้าต่างการนำทางทางด้านซ้าย เลือกโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="337bf-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="337bf-134">ในบานหน้าต่างด้านขวา ให้เลือกกล่องกาเครื่องหมาย **เปิดใช้งานลิงก์เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน**</span><span class="sxs-lookup"><span data-stu-id="337bf-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="337bf-135">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="337bf-135">Select **Save**.</span></span>
1. <span data-ttu-id="337bf-136">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="337bf-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="337bf-137">หลังจากเผยแพร่หน้าแล้ว PDP จะมีปุ่ม **เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน**</span><span class="sxs-lookup"><span data-stu-id="337bf-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="337bf-138">ภาพประกอบต่อไปนี้แสดงกล่องกาเครื่องหมาย **เปิดใช้งานลิงก์เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน** และปุ่ม **เลือกซื้อสินค้าที่คำอธิบายคล้ายกัน** บน PDP ตัวอย่างในตัวสร้างในไซต์</span><span class="sxs-lookup"><span data-stu-id="337bf-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![กล่องกาเครื่องหมายเปิดใช้งานลิงก์เลือกซื้อสินค้าที่คำอธิบายคล้ายกันและปุ่มเลือกซื้อสินค้าที่คำอธิบายคล้ายกันบน PDP ตัวอย่างในตัวสร้างในไซต์](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="337bf-140">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="337bf-140">Additional resources</span></span>

[<span data-ttu-id="337bf-141">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="337bf-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="337bf-142">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="337bf-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="337bf-143">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="337bf-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="337bf-144">เปิดใช้งานคำแนะนำ "ร้านค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="337bf-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="337bf-145">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="337bf-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="337bf-146">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="337bf-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="337bf-147">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="337bf-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]