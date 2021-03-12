---
title: บัตรของขวัญดิจิทัลอีคอมเมิร์ซ
description: หัวข้อนี้จะอธิบายวิธีการใช้งานบัตรของขวัญดิจิทัลในการใช้งานอีคอมเมิร์ซของ Microsoft Dynamics 365 Commerce นอกจากนี้ ยังแสดงภาพรวมของขั้นตอนการตั้งค่าคอนฟิกที่สําคัญด้วย
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982677"
---
# <a name="e-commerce-digital-gift-cards"></a><span data-ttu-id="a05a5-104">บัตรของขวัญดิจิทัลอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="a05a5-104">E-commerce digital gift cards</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a05a5-105">หัวข้อนี้จะอธิบายวิธีการใช้งานบัตรของขวัญดิจิทัลในการใช้งานอีคอมเมิร์ซของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-105">This topic describes how digital gift cards work in the e-commerce implementation of Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="a05a5-106">นอกจากนี้ ยังแสดงภาพรวมของขั้นตอนการตั้งค่าคอนฟิกที่สําคัญด้วย</span><span class="sxs-lookup"><span data-stu-id="a05a5-106">It also provides an overview of important configuration steps.</span></span>

<span data-ttu-id="a05a5-107">ใน Dynamics 365 Commerce การซื้อบัตรของขวัญดิจิทัลจะเป็นไปตามโฟลว์เดียวกันกับการซื้อผลิตภัณฑ์อื่นๆ ในระบบ</span><span class="sxs-lookup"><span data-stu-id="a05a5-107">In Dynamics 365 Commerce, the purchase of digital gift cards follows the same flow as the purchase of other products in the system.</span></span> <span data-ttu-id="a05a5-108">ไม่ต้องตั้งค่าคอนฟิกโมดูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a05a5-108">No additional modules have to be configured.</span></span> <span data-ttu-id="a05a5-109">ถ้ามีการเพิ่มบัตรของขวัญหลายใบลงในรถเข็น รายการบัตรของขวัญจะถูกไม่รวมอยู่ในรายการขายเดียว</span><span class="sxs-lookup"><span data-stu-id="a05a5-109">If multiple gift cards are added to the cart, the gift card items aren't aggregated on a single sales line.</span></span> <span data-ttu-id="a05a5-110">ต้องระบุลักษณะการทำงานนี้ เนื่องจากมีการออกใบแจ้งหนี้รายการขายแต่ละรายการโดยใช้หมายเลขบัตรของขวัญแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="a05a5-110">This behavior is required because each sales line is invoiced by using a separate gift card number.</span></span>

<span data-ttu-id="a05a5-111">การซื้อบัตรของขวัญดิจิทัลได้รับการสนับสนุนในรุ่น Dynamics 365 Commerce 10.0.16 และรุ่นหลังจากนั้น</span><span class="sxs-lookup"><span data-stu-id="a05a5-111">The purchase of digital gift cards is supported in the Dynamics 365 Commerce 10.0.16 release and later.</span></span>

<span data-ttu-id="a05a5-112">ภาพต่อไปนี้จะแสดงตัวอย่างของหน้ารายละเอียดผลิตภัณฑ์ (PDP) สำหรับบัตรของขวัญดิจิทัลบนไซต์ Fabrikam อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="a05a5-112">The following illustration shows an example of the product details page (PDP) for a digital gift card on the Fabrikam e-commerce site.</span></span>

![ตัวอย่างของบัตรของขวัญดิจิทัล PDP บนไซต์ Fabrikam e-commerce](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a><span data-ttu-id="a05a5-114">เปิดคุณลักษณะบัตรของขวัญดิจิทัลในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-114">Turn on the digital gift card feature in Commerce headquarters</span></span>

<span data-ttu-id="a05a5-115">เพื่อให้โฟลว์การซื้อสำหรับบัตรของขวัญดิจิทัลใช้งานได้ใน Dynamics 365 Commerce ต้องเปิดคุณลักษณะ **การซื้อบัตรของขวัญบนคุณลักษณะอีคอมเมิร์ซ** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-115">For the purchase flow for digital gift cards to work in Dynamics 365 Commerce, the **Purchasing gift card on e-Commerce feature** feature must be turned on in Commerce headquarters.</span></span> <span data-ttu-id="a05a5-116">คุณสามารถค้นหาคุณลักษณะในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ในศูนย์ควบคุม Commerce ดังแสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a05a5-116">You can find the feature in the **Feature management** workspace in Commerce headquarters, as shown in the following illustration.</span></span>

![พื้นที่ทำงานการจัดการคุณลักษณะในศูนย์ควบคุม Commerce](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a><span data-ttu-id="a05a5-118">ตั้งค่าคอนฟิกบัตรของขวัญดิจิทัลในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-118">Configure a digital gift card in Commerce headquarters</span></span>

<span data-ttu-id="a05a5-119">ควรตั้งค่าคอนฟิกผลิตภัณฑ์บัตรของขวัญดิจิทัลในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-119">Digital gift card products should be configured in Commerce headquarters.</span></span> <span data-ttu-id="a05a5-120">กระบวนการคล้ายกับกระบวนการสำหรับผลิตภัณฑ์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a05a5-120">The process resembles the process for other products.</span></span> <span data-ttu-id="a05a5-121">อย่างไรก็ตาม ขั้นตอนสําคัญต่อไปนี้เฉพาะเจาะจงสำหรับการตั้งค่าคอนฟิกของบัตรของขวัญสำหรับการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a05a5-121">However, the following important steps are specific to the configuration of gift cards for purchase.</span></span> <span data-ttu-id="a05a5-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างและตั้งค่าคอนฟิกผลิตภัณฑ์ โปรดดูที่ [สร้างผลิตภัณฑ์ใหม่ใน Commerce](create-new-product-commerce.md)</span><span class="sxs-lookup"><span data-stu-id="a05a5-122">For more information about how to create and configure products, see [Create a new product in Commerce](create-new-product-commerce.md).</span></span>

- <span data-ttu-id="a05a5-123">เมื่อคุณตั้งค่าคอนฟิกผลิตภัณฑ์บัตรของขวัญดิจิทัลในกล่องโต้ตอบ **ผลิตภัณฑ์ใหม่** ให้ตั้งค่าฟิลด์ **ชนิดผลิตภัณฑ์** เป็น **บริการ**</span><span class="sxs-lookup"><span data-stu-id="a05a5-123">When you configure digital gift card products in the **New product** dialog box, set the **Product type** field to **Service**.</span></span> <span data-ttu-id="a05a5-124">(เมื่อต้องการเปิดกล่องโต้ตอบ ให้ไปที่ **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ผลิตภัณฑ์ตามประเภท** และเลือก **ใหม่**) ผลิตภัณฑ์ของชนิด **บริการ** ไม่ได้รับการตรวจสอบสำหรับสินค้าคงคลังที่มีอยู่ก่อนมีการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="a05a5-124">(To open the dialog box, go to **Retail and commerce \> Products and categories \> Products by category**, and select **New**.) Products of the **Service** type aren't checked for available inventory before an order is placed.</span></span> <span data-ttu-id="a05a5-125">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างผลิตภัณฑ์ใหม่](create-new-product-commerce.md#create-a-new-product)</span><span class="sxs-lookup"><span data-stu-id="a05a5-125">For more information, see [Create a new product](create-new-product-commerce.md#create-a-new-product).</span></span>
- <span data-ttu-id="a05a5-126">ในหน้า **พารามิเตอร์ Commerce** บนแท็บ **การลงรายการบัญชี** ฟิลด์ **ผลิตภัณฑ์บัตรของขวัญ** ต้องถูกตั้งเป็น **บัตรของขวัญดิจิทัล** ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a05a5-126">On the **Commerce parameters** page, on the **Posting** tab, the **Gift card product** field must be set to **Digital Gift Card**, as shown in the following illustration.</span></span> <span data-ttu-id="a05a5-127">หากผลิตภัณฑ์เป็นบัตรของขวัญภายนอก โปรดดู [การสนับสนุนสำหรับบัตรของขวัญภายนอก](./dev-itpro/gift-card.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a05a5-127">If the product is an external gift card, see [Support for external gift cards](./dev-itpro/gift-card.md) for more information.</span></span>

    ![ฟิลด์ผลิตภัณฑ์บัตรของขวัญในศูนย์ควบคุม Commerce](./media/PostGiftcard.png)

- <span data-ttu-id="a05a5-129">ถ้าบัตรของขวัญต้องสนับสนุนยอดเงินที่กําหนดไว้ล่วงหน้าจํานวนมาก (ตัวอย่างเช่น $25, $50 และ $100) ควรใช้มิติ **ขนาด** เพื่อตั้งค่ายอดเงินที่กําหนดไว้ล่วงหน้าดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="a05a5-129">If a gift card must support multiple predefined amounts (for example, $25, $50, and $100), the **Size** dimension should be used to set up those predefined amounts.</span></span> <span data-ttu-id="a05a5-130">ยอดเงินที่กําหนดไว้ล่วงหน้าแต่ละยอดจะเป็นตัวแปร</span><span class="sxs-lookup"><span data-stu-id="a05a5-130">Each predefined amount will be a variant.</span></span> <span data-ttu-id="a05a5-131">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มิติของผลิตภัณฑ์](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)</span><span class="sxs-lookup"><span data-stu-id="a05a5-131">For more information, see [Product dimensions](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).</span></span>
- <span data-ttu-id="a05a5-132">ถ้าลูกค้าต้องสามารถระบุจํานวนเงินที่กำหนดเองในบัตรของขวัญได้ อันดับแรกให้ตั้งค่าตัวแปรที่อนุญาตให้ใช้จํานวนเงินที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a05a5-132">If customers must be able to specify a custom amount for a gift card, first set up a variant that allows for a custom amount.</span></span> <span data-ttu-id="a05a5-133">จากนั้น ให้เปิดผลิตภัณฑ์จากหน้า **ผลิตภัณฑ์ที่เผยแพร่ในประเภท** และจากนั้น บน FastTab **การค้า** ให้ตั้งค่าฟิลด์ **ป้อนราคา** เป็น **ต้องป้อนราคาใหม่** ตามที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a05a5-133">Next, open the product from the **Released products in category** page, and then, on the **Commerce** FastTab, set the **Key in price** field to **Must key in new price**, as shown in the following illustration.</span></span> <span data-ttu-id="a05a5-134">การตั้งค่านี้ช่วยให้มั่นใจว่าลูกค้าจะสามารถป้อนราคา เมื่อพวกเขาเลือกดูผลิตภัณฑ์ใน PDP</span><span class="sxs-lookup"><span data-stu-id="a05a5-134">This setting ensures that customers can enter a price when they browse the product on a PDP.</span></span>

    ![ฟิลด์ป้อนราคาในศูนย์ควบคุม Commerce](./media/KeyInPrice.png)

- <span data-ttu-id="a05a5-136">ต้องตั้งค่าโหมดการจัดส่งสำหรับบัตรของขวัญดิจิทัลเป็น **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a05a5-136">The mode of delivery for a digital gift card must be set to **Electronic**.</span></span> <span data-ttu-id="a05a5-137">บนหน้า **โหมดการจัดส่ง** (**การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> โหมดการจัดส่ง**) ให้เลือกโหมด **อิเล็กทรอนิกส์** ของการจัดส่งในบานหน้าต่างรายการ แล้วจากนั้น เพิ่มผลิตภัณฑ์บัตรของขวัญดิจิทัลลงในกริดบน FastTab **ผลิตภัณฑ์** ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a05a5-137">On the **Modes of delivery** page (**Retail and commerce \> Channel setup \> Modes of delivery**), select the **Electronic** mode of delivery in the list pane, and then add the digital gift card product to the grid on the **Products** FastTab, as shown in the following illustration.</span></span> <span data-ttu-id="a05a5-138">สำหรับข้อมูลเพิ่มเติม โปรดดู [การตั้งค่าโหมดการจัดส่ง](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)</span><span class="sxs-lookup"><span data-stu-id="a05a5-138">For more information, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

    ![ผลิตภัณฑ์บัตรของขวัญดิจิทัลในหน้าโหมดการจัดส่งในศูนย์ควบคุม Commerce](./media/ElectronicMode.PNG)

- <span data-ttu-id="a05a5-140">ตรวจสอบให้แน่ใจว่าโพรไฟล์ฟังก์ชันออนไลน์ได้ถูกสร้างและเชื่อมโยงกับร้านค้าออนไลน์ของคุณในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-140">Make sure that an online functionality profile has been created and associated with your online store in Commerce headquarters.</span></span> <span data-ttu-id="a05a5-141">ในโพรไฟล์ฟังก์ชัน ให้ตั้งค่าตัวเลือก **รวมผลิตภัณฑ์** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a05a5-141">In the functionality profile, set the **Aggregate products** option to **Yes**.</span></span> <span data-ttu-id="a05a5-142">การตั้งค่านี้ช่วยให้มั่นใจว่าสินค้าทั้งหมด ยกเว้นบัตรของขวัญ จะถูกรวมไว้</span><span class="sxs-lookup"><span data-stu-id="a05a5-142">This setting ensures that all items except gift cards are aggregated.</span></span> <span data-ttu-id="a05a5-143">สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างโพรไฟล์ฟังก์ชันออนไลน์](online-functionality-profile.md)</span><span class="sxs-lookup"><span data-stu-id="a05a5-143">For more information, see [Create an online functionality profile](online-functionality-profile.md).</span></span>
- <span data-ttu-id="a05a5-144">เพื่อให้แน่ใจว่าลูกค้าจะได้รับอีเมลหลังจากออกใบแจ้งหนี้บัตรของขวัญแล้ว ให้สร้างชนิดการแจ้งเตือนทางอีเมลใหม่ในหน้า **โพรไฟล์การแจ้งเตือนทางอีเมล** และตั้งค่าฟิลด์ **ชนิดการแจ้งเตือนทางอีเมล** เป็น **ออกบัตรของขวัญ**</span><span class="sxs-lookup"><span data-stu-id="a05a5-144">To ensure that customers receive an email after a gift card is invoiced, create a new email notification type on the **Email notification profiles** page, and set the **Email notification type** field to **Issue gift card**.</span></span> <span data-ttu-id="a05a5-145">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล](email-notification-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="a05a5-145">For more information, see [Set up an email notification profile](email-notification-profiles.md).</span></span>

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a><span data-ttu-id="a05a5-146">เพิ่มรูปภาพผลิตภัณฑ์ลงในไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-146">Add product images to the Commerce site builder Media library</span></span>

<span data-ttu-id="a05a5-147">คุณต้องเพิ่มรูปภาพผลิตภัณฑ์สำหรับผลิตภัณฑ์บัตรของขวัญดิจิทัลลงในไลบรารีสื่อของโปรแกรมสร้างไซต์ของ Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-147">You must add product images for digital gift card products to the Commerce site builder Media library.</span></span> <span data-ttu-id="a05a5-148">ตรวจสอบให้แน่ใจว่าชื่อไฟล์ของไฟล์รูปภาพบัตรของขวัญเป็นไปตามแบบแผนการตั้งชื่อของไซต์ของคุณสำหรับรูปภาพผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a05a5-148">Make sure that the file names of the gift card image files follow your site's naming conventions for product images.</span></span> <span data-ttu-id="a05a5-149">สำหรับข้อมูลเพิ่มเติม ให้ดู [อัปโหลดรูปภาพ](dam-upload-images.md)</span><span class="sxs-lookup"><span data-stu-id="a05a5-149">For more information, see [Upload images](dam-upload-images.md).</span></span>

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a><span data-ttu-id="a05a5-150">ตั้งค่าคอนฟิกยอดเงินที่กําหนดเองสำหรับบัตรของขวัญดิจิทัลในโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-150">Configure a custom amount for a digital gift card in Commerce site builder</span></span>

<span data-ttu-id="a05a5-151">หากบัตรของขวัญดิจิทัลได้รับการตั้งค่าคอนฟิกให้อนุญาตให้ใช้ยอดเงินที่กําหนดเอง ต้องเปิดใช้งานพฤติกรรมนี้ใน [โมดูลกล่องการซื้อ](add-buy-box.md) ที่ใช้ใน PDPs ของไซต์ของคุณด้วย</span><span class="sxs-lookup"><span data-stu-id="a05a5-151">If a digital gift card is configured to allow for a custom amount, this behavior must also be enabled in the [buy box module](add-buy-box.md) that is used on your site's PDPs.</span></span> <span data-ttu-id="a05a5-152">โมดูลกล่องการซื้อสนับสนุนการตั้งค่าคอนฟิกโมดูลเพื่อให้สามารถกําหนดยอดเงินที่กําหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="a05a5-152">The buy box module supports module configuration to allow for custom amounts.</span></span> <span data-ttu-id="a05a5-153">นอกจากนี้ คุณยังสามารถกําหนดจํานวนเงินต่ำสุดและสูงสุดที่ได้รับอนุญาตสำหรับยอดเงินที่กําหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a05a5-153">You can also define the minimum and maximum amounts that are allowed for custom amounts.</span></span>

<span data-ttu-id="a05a5-154">เพื่อตั้งค่าคอนฟิกยอดเงินที่กําหนดเองสำหรับบัตรของขวัญดิจิทัลในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a05a5-154">To configure a custom amount for a digital gift card in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a05a5-155">ไปที่โมดูลกล่องการซื้อที่ใช้ใน PDPs ของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a05a5-155">Go to the buy box module that is used on your site's PDPs.</span></span> <span data-ttu-id="a05a5-156">โมดูลกล่องการซื้อนี้อาจถูกดําเนินการในส่วน ในเทมเพลต หรือบนหน้า</span><span class="sxs-lookup"><span data-stu-id="a05a5-156">This buy box module might be implemented in a fragment, in a template, or on a page.</span></span>
1. <span data-ttu-id="a05a5-157">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a05a5-157">Select **Edit**.</span></span>
1. <span data-ttu-id="a05a5-158">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกกล่องกาเครื่องหมาย **อนุญาตราคาที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="a05a5-158">In the properties pane on the right, select the **Allow custom price** check box.</span></span>
1. <span data-ttu-id="a05a5-159">ไม่จำเป็น: เมื่อต้องการกําหนดยอดเงินต่ำสุดและสูงสุดสำหรับยอดเงินที่กําหนดเอง ให้ป้อนจํานวนเงินภายใต้ **ราคาต่ำสุด** และ **ราคาสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="a05a5-159">Optional: To define minimum and maximum amounts for custom amounts, enter amounts under **Minimum price** and **Maximum price**.</span></span>
1. <span data-ttu-id="a05a5-160">เลือก **เสร็จสิ้นการแก้ไข** และจากนั้น เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="a05a5-160">Select **Finish editing**, and then select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a05a5-161">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a05a5-161">Additional resources</span></span>

[<span data-ttu-id="a05a5-162">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a05a5-162">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a05a5-163">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="a05a5-163">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a05a5-164">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="a05a5-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a05a5-165">สร้างผลิตภัณฑ์ใหม่ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="a05a5-165">Create a new product in Commerce</span></span>](create-new-product-commerce.md)

[<span data-ttu-id="a05a5-166">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="a05a5-166">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="a05a5-167">มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a05a5-167">Product dimensions</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[<span data-ttu-id="a05a5-168">ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="a05a5-168">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="a05a5-169">สร้างโพรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="a05a5-169">Create an online functionality profile</span></span>](online-functionality-profile.md)

[<span data-ttu-id="a05a5-170">การรองรับบัตรของขวัญภายนอก</span><span class="sxs-lookup"><span data-stu-id="a05a5-170">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
