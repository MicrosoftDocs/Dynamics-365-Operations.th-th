---
title: เปิดใช้งานและใช้การใช้ร่วมกันข้ามช่องทาง
description: หัวข้อนี้อธิบายวิธีการเปิดใช้งานและใช้คุณลักษณะการใช้ร่วมกันข้ามช่องทางของตัวสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 987dca54e47b909014862e310aa424019d8c4677
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207834"
---
# <a name="enable-and-use-cross-channel-sharing"></a><span data-ttu-id="593bc-103">เปิดใช้งานและใช้การใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-103">Enable and use cross-channel sharing</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="593bc-104">หัวข้อนี้อธิบายวิธีการเปิดใช้งานและใช้คุณลักษณะการใช้ร่วมกันข้ามช่องทางของตัวสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="593bc-104">This topic describes how to enable and use the cross-channel sharing feature of Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="593bc-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="593bc-105">Overview</span></span>

<span data-ttu-id="593bc-106">การใช้ร่วมกันข้ามช่องทางช่วยให้ร้านค้าปลีกของร้านค้านำมาใช้ใหม่และแบ่งปันเนื้อหาระหว่างหลายช่องทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="593bc-106">Cross-channel sharing lets retailers reuse and share content among multiple channels of a site.</span></span> <span data-ttu-id="593bc-107">ความสามารถนี้มีประโยชน์เมื่อช่องทางไซต์มีภาษาพื้นฐานที่เข้ากันได้ หรือเมื่อมีรายการเนื้อหาจำนวนมากเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="593bc-107">This capability is useful when the site channels have a compatible base language, or when they have numerous content items in common.</span></span>

<span data-ttu-id="593bc-108">การใช้ร่วมกันข้ามช่องทางทำงานโดยการเปิดใช้งานช่องทางเริ่มต้น ซึ่งจะค้นหาเนื้อหาที่มีอยู่เมื่อไม่พบเนื้อหารุ่นเฉพาะช่องทางของเนื้อหาที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="593bc-108">Cross-channel sharing works by enabling a default channel that will be searched for available content when a channel-specific version of the requested content isn't found.</span></span> <span data-ttu-id="593bc-109">เนื้อหาที่มีไว้สำหรับการใช้ร่วมกันระหว่างช่องทางจะถูกสร้างขึ้นในช่องทางเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="593bc-109">Content that is intended to be shared among channels is created in the default channel.</span></span> <span data-ttu-id="593bc-110">เนื้อหาดังกล่าวอาจเป็นภาษาท้องถิ่นสำหรับตำแหน่งที่ตั้งใดๆ ที่ใช้บนช่องทางไซต์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="593bc-110">That content can be localized for any locale that is used on any site channel.</span></span>

## <a name="when-to-use-cross-channel-sharing"></a><span data-ttu-id="593bc-111">เมื่อใช้การใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-111">When to use cross-channel sharing</span></span>

<span data-ttu-id="593bc-112">การใช้ร่วมกันข้ามช่องทางมีประโยชน์เมื่อมีหลายช่องทางในไซต์เดียวสามารถใช้เนื้อหาร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="593bc-112">Cross-channel sharing is useful when multiple channels on a single site can share content.</span></span> <span data-ttu-id="593bc-113">ตัวอย่างเช่น ผู้ค้าปลีกที่มีหลายแบรนด์และหน้าร้านซึ่งจัดกลุ่มภายใต้ไซต์เดียวกันสามารถใช้เนื้อหาบางอย่างร่วมกันระหว่างบางหน้าร้านหรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="593bc-113">For example, a retailer that has multiple brands and storefronts that are grouped under a single site can share some content among some or all of the storefronts.</span></span> <span data-ttu-id="593bc-114">เนื้อหาที่ใช้ร่วมกันนี้อาจรวมถึงหน้าสำหรับเงื่อนไขและข้อกำหนด เงื่อนไขการชำระเงิน วิธีการจัดส่ง และคำถามที่ถามบ่อย (FAQ)</span><span class="sxs-lookup"><span data-stu-id="593bc-114">This shared content can include pages for terms and conditions, payment terms, shipment methods, and frequently asked questions (FAQ).</span></span>

<span data-ttu-id="593bc-115">การใช้ร่วมกันข้ามช่องทางยังรองรับส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="593bc-115">Cross-channel sharing also supports fragments.</span></span> <span data-ttu-id="593bc-116">ดังนั้น หน้าเนื้อหาที่มีส่วนเฉพาะช่องทางสามารถสร้างเป็นเนื้อหาข้ามช่องทางได้</span><span class="sxs-lookup"><span data-stu-id="593bc-116">Therefore, a content page that contains channel-specific fragments can be created as cross-channel content.</span></span> <span data-ttu-id="593bc-117">ในกรณีนี้ ถึงแม้ว่าเนื้อหาส่วนใหญ่จะมีการใช้ร่วมกันระหว่างช่องทาง ส่วนเฉพาะช่องทางในหน้าข้ามช่องทางจะแสดงเฉพาะเมื่อมีการร้องขอจากช่องทางร้านที่สอดคล้องกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="593bc-117">In this case, although most of the content will be shared among channels, channel-specific fragments on a cross-channel page will be rendered only when they are requested from the corresponding storefront channel.</span></span>

<span data-ttu-id="593bc-118">ไซต์ที่มีหนึ่งช่องทาง หรือไซต์ที่มีหลายช่องทางที่ไม่สามารถใช้เนื้อหาร่วมกันได้ จะไม่ได้รับประโยชน์จากการใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-118">Sites that have only one channel, or sites that have multiple channels that can't share content, won't benefit from cross-channel sharing.</span></span>

## <a name="enable-cross-channel-sharing"></a><span data-ttu-id="593bc-119">เปิดใช้งานการใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-119">Enable cross-channel sharing</span></span>

<span data-ttu-id="593bc-120">การใช้ร่วมกันข้ามช่องทางเปิดใช้งานในระดับไซต์</span><span class="sxs-lookup"><span data-stu-id="593bc-120">Cross-channel sharing is enabled at the site level.</span></span> <span data-ttu-id="593bc-121">การดำเนินงานนี้เป็นแบบทางเดียว</span><span class="sxs-lookup"><span data-stu-id="593bc-121">This operation is one-way.</span></span> <span data-ttu-id="593bc-122">กล่าวอีกอย่างหนึ่ง หลังจากเปิดใช้งานการใช้ร่วมกันข้ามช่องทางแล้ว จะไม่สามารถปิดใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="593bc-122">In other words, after cross-channel sharing is enabled, it can't be disabled.</span></span>

<span data-ttu-id="593bc-123">เมื่อต้องการเปิดใช้งานการใช้ร่วมกันข้ามช่องทางในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="593bc-123">To enable cross-channel sharing in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="593bc-124">ไปที่ **การตั้งค่าไซต์ \> คุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="593bc-124">Go to **Site settings \> Features**.</span></span>
1. <span data-ttu-id="593bc-125">ตั้งค่าตัวเลือกสำหรับคุณลักษณะ **ข้ามช่องทาง** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="593bc-125">Set the option for the **Cross Channel** feature to **On**.</span></span>

    ![ตัวเลือกข้ามช่องทางตั้งค่าเป็น เปิด ในโปรแกรมสร้างไซต์ Commerce](./media/enabling-cross-channel-sharing.png)

<span data-ttu-id="593bc-127">หลังจากที่คุณเปิดใช้งานการใช้ร่วมกันข้ามช่องทาง ข้อมูลข้ามช่องทางจะปรากฏในส่วน **ช่องทาง** ที่ **การตั้งค่าไซต์ \> คุณลักษณะ** ในตัวอย่างในภาพประกอบต่อไปนี้จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="593bc-127">After you enable cross-channel sharing, cross-channel information will appear in the **Channels** section at **Site settings \> Features**, as the example in the following illustration shows.</span></span>

![ข้อมูลช่องทางที่มองเห็นได้หลังจากเปิดใช้งานการใช้ร่วมกันข้ามช่องทาง](./media/channels-cross-channel.png)

<span data-ttu-id="593bc-129">นอกจากนี้ หลังจากที่คุณเปิดใช้งานการใช้ร่วมกันข้ามช่องทาง ฟิลด์ **ช่องทาง** ในด้านขวาบนของโปรแกรมสร้างไซต์ Commerce จะรวมตัวเลือก **ร้านค้าออนไลน์ข้ามช่องทาง** ซึ่งคุณสามารถใช้เพื่อจัดการเนื้อหาข้ามช่องทาง ดังแสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="593bc-129">Additionally, after you enable cross-channel sharing, the **Channel** field in the upper right of Commerce site builder will include a **Cross Channel Online Store** option that you can use to manage cross-channel content, as shown in the following illustration.</span></span>

![ตัวเลือกร้านค้าออนไลน์ข้ามช่องทางในฟิลด์ ช่องทาง หลังจากที่เปิดใช้งานการใช้ร่วมกันข้ามช่องทาง](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a><span data-ttu-id="593bc-131">ส้รางและใช้เนื้อหาข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-131">Create and use cross-channel content</span></span>

<span data-ttu-id="593bc-132">คุณสามารถสร้างและใช้เนื้อหาข้ามช่องทางได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="593bc-132">You can create and use cross-channel content in multiple ways.</span></span> <span data-ttu-id="593bc-133">ตัวอย่างเช่น คุณสามารถสร้างส่วนข้ามช่องทางต่างๆ สร้างหน้าข้ามช่องทางที่ใช้เนื้อหาแบบข้ามช่องทางและเฉพาะช่องทาง และแทนที่ส่วนข้ามช่องทางต่างๆ ที่มีรุ่นของส่วนช่องทางเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="593bc-133">For example, you can create cross-channel fragments, create cross-channel pages that use cross-channel and channel-specific content, and override cross-channel fragments with channel-specific versions of fragments.</span></span>

### <a name="create-a-cross-channel-fragment"></a><span data-ttu-id="593bc-134">การสร้างส่วนของข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-134">Create a cross-channel fragment</span></span>

<span data-ttu-id="593bc-135">เมื่อต้องการสร้างส่วนข้ามช่องทางในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="593bc-135">To create a cross-channel fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="593bc-136">ไปที่ **ส่วนย่อย** จากนั้น ให้เลือก **สร้าง** เพื่อสร้างส่วนย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="593bc-136">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="593bc-137">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือกโมดูล **แบนเนอร์โปรโมชั่น** และจากนั้น ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อ (ตัวอย่างเช่น **แบนเนอร์ข้ามช่องทาง**)</span><span class="sxs-lookup"><span data-stu-id="593bc-137">In the **New fragment** dialog box, select the **Promo banner** module, and then, under **Fragment name**, enter a name (for example, **Cross-channel banner**).</span></span> <span data-ttu-id="593bc-138">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-138">Then select **OK**.</span></span>
1. <span data-ttu-id="593bc-139">ในบานหน้าต่างคุณสมบัติของโมดูล **แบนเนอร์โปรโมชัน** ให้เลือก **เพิ่มข้อความ** แล้วเลือก **ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="593bc-139">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="593bc-140">ในกล่องโต้ตอบ **ข้อความ** ภายใต้ **ข้อความ** ให้ป้อน **ข้ามช่องทาง** และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-140">In the **Message** dialog box, under **Text**, enter **Cross-channel**, and the select **OK**.</span></span> 
1. <span data-ttu-id="593bc-141">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="593bc-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="593bc-142">ส่วนข้ามช่องทางนี้สามารถใช้ในหน้าข้ามช่องทางหรือช่องทางเฉพาะที่สร้างบนช่องทางไซต์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="593bc-142">This cross-channel fragment can be used on cross-channel or channel-specific pages that are created on any site channel.</span></span>

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a><span data-ttu-id="593bc-143">สร้างหน้าข้ามช่องทางที่ใช้เนื้อหาข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-143">Create a cross-channel page that uses cross-channel content</span></span>

<span data-ttu-id="593bc-144">หน้าแบบข้ามช่องทางสามารถใช้บนช่องทางใดก็ได้ของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="593bc-144">Cross-channel pages can be used on any channel of your site.</span></span> <span data-ttu-id="593bc-145">ดังนั้น คุณจึงสามารถสร้างหน้าเนื้อหาที่ใช้ร่วมกันหนึ่งครั้ง และทำการอัปเดตที่ตามมาในที่เดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="593bc-145">Therefore, you can create a shared content page one time and make any subsequent updates in a single place.</span></span> <span data-ttu-id="593bc-146">ตัวอย่างเช่น หน้า **ข้อตกลงและเงื่อนไข** ข้ามช่องทางที่มี URL `/toc` สามารถใช้ร่วมกันระหว่างช่องทางทั้งหมดของไซต์ได้</span><span class="sxs-lookup"><span data-stu-id="593bc-146">For example, a cross-channel **Terms and conditions** page that has the URL `/toc` can be shared among all the channels of a site.</span></span> <span data-ttu-id="593bc-147">ถ้า URL พื้นฐานสำหรับช่องทางไซต์คือ `www.fabrikam.com/brand1` และ `www.fabrikam.com/brand2` ช่องทางข้ามช่องทางเดียวกัน หน้า **ข้อกำหนดและเงื่อนไข** ที่ใช้ร่วมกันจะพร้อมใช้งานจากทั้งสอง URL ของช่องทางไซต์ `www.fabrikam.com/brand1/toc` และ `www.fabrikam.com/brand2/toc` ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="593bc-147">If the base URLs for the site channels are `www.fabrikam.com/brand1` and `www.fabrikam.com/brand2`, the same cross-channel, shared **Terms and conditions** page will be available from both site channel URLs, at `www.fabrikam.com/brand1/toc` and `www.fabrikam.com/brand2/toc`, respectively.</span></span> <span data-ttu-id="593bc-148">ถ้าหน้า **ข้อตกลงและเงื่อนไข** ต้องมีการอัปเดตในภายหลัง คุณต้องอัปเดตเฉพาะหน้าเดียวที่ใช้ร่วมกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="593bc-148">If the **Terms and conditions** page must be updated later, you have to update only the single, shared page.</span></span>

<span data-ttu-id="593bc-149">เมื่อต้องการสร้างหน้าข้ามช่องทางในโปรแกรมสร้างไซต์ Commerce ซึ่งใช้เนื้อหาข้ามช่องทาง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="593bc-149">To create a cross-channel page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="593bc-150">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="593bc-150">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="593bc-151">ในกล่องโต้ตอบ **เลือกแม่แบบ** ให้เลือกแม่แบบ เช่น **การตลาด**</span><span class="sxs-lookup"><span data-stu-id="593bc-151">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="593bc-152">ภายใต้ **ชื่อเพจ** ให้ป้อนชื่อของเพจ (ตัวอย่างเช่น **หน้า ข้ามช่องทาง**)</span><span class="sxs-lookup"><span data-stu-id="593bc-152">Under **Page name**, enter a name for the page (for example, **Cross-channel page**).</span></span>
1. <span data-ttu-id="593bc-153">ภายใต้ **URL ของหน้า** ให้ป้อน URL ของหน้า (ตัวอย่างเช่น **examplepage**) แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-153">Under **Page URL**, enter a page URL (for example, **examplepage**), and then select **OK**.</span></span>
1. <span data-ttu-id="593bc-154">ในช่อง **หลัก** ของหน้าใหม่ เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="593bc-154">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="593bc-155">ในกล่องโต้ตอบ **เพิ่มส่วนย่อย** ให้เลือกส่วนข้ามช่องทางที่คุณสร้างไว้ก่อนหน้านี้ที่มีแบบเบอร์โปรโมชั่น แล้วจากนั้่น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-155">In the **Add fragment** dialog box, select the cross-channel fragment that you created earlier that has a promo banner, and then select **OK**.</span></span>
1. <span data-ttu-id="593bc-156">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="593bc-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="593bc-157">คุณควรเห็นแบนเนอร์โปรโมชันที่ระบุว่า "ข้ามช่องทาง"</span><span class="sxs-lookup"><span data-stu-id="593bc-157">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="593bc-158">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="593bc-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a><span data-ttu-id="593bc-159">สร้างหน้าเฉพาะช่องทางที่ใช้เนื้อหาข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-159">Create a channel-specific page that uses cross-channel content</span></span>

<span data-ttu-id="593bc-160">การใช้เนื้อหาข้ามช่องทางบนหน้าเฉพาะช่องทาง คุณสามารถสร้างส่วนเนื้อหาที่ใช้ร่วมกันหนึ่งครั้งแล้วใช้ในหน้าเฉพาะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-160">By using cross-channel content on channel-specific pages, you can create a shared content fragment one time and then use it on channel-specific pages.</span></span> <span data-ttu-id="593bc-161">"การจัดหาเดียว" นี้มีประโยชน์สำหรับเนื้อหาที่ใช้ร่วมกัน เช่น ข้อตกลงและเงื่อนไข เงื่อนไขการชำระเงิน หรือข้อมูลการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="593bc-161">This "single sourcing" is useful for shared content such as terms and conditions, payment terms, or contact information.</span></span>

<span data-ttu-id="593bc-162">เมื่อต้องการสร้างหน้าเฉพาะช่องทางในโปรแกรมสร้างไซต์ Commerce ซึ่งใช้เนื้อหาข้ามช่องทาง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="593bc-162">To create a channel-specific page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="593bc-163">จากภายในช่องทางใดช่องทางหนึ่ง เช่น **ร้านค้าออนไลน์แบบขยายของ Fabrikam** ให้ไปที่ **หน้า** แล้วเลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="593bc-163">From within a specific channel, such as **Fabrikam extended online store**, go to **Pages**, and then select **New** to create a new page.</span></span>
1. <span data-ttu-id="593bc-164">ในกล่องโต้ตอบ **เลือกแม่แบบ** ให้เลือกแม่แบบ เช่น **การตลาด**</span><span class="sxs-lookup"><span data-stu-id="593bc-164">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="593bc-165">ภายใต้ **ชื่อเพจ** ให้ป้อนชื่อของเพจ (ตัวอย่างเช่น **หน้า เฉพาะช่องทาง**)</span><span class="sxs-lookup"><span data-stu-id="593bc-165">Under **Page name**, enter a name for the page (for example, **Channel-specific page**).</span></span>
1. <span data-ttu-id="593bc-166">ภายใต้ **URL ของหน้า** ให้ป้อน URL ของหน้า (ตัวอย่างเช่น **channelspecificpage**) แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-166">Under **Page URL**, enter a page URL (for example, **channelspecificpage**), and then select **OK**.</span></span>
1. <span data-ttu-id="593bc-167">ในช่อง **หลัก** ของหน้าใหม่ เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="593bc-167">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="593bc-168">ในกล่องโต้ตอบ **เพิ่มส่วนย่อย** ภายใต้ **ช่องทาง** ให้เลือก **ร้านค้าออนไลน์ข้ามช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="593bc-168">In the **Add fragment** dialog box, under **Channel**, select **Cross Channel Online Store**.</span></span> <span data-ttu-id="593bc-169">ส่วนของข้ามช่องทางที่คุณสร้างไว้ก่อนหน้านี้ควรปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="593bc-169">The cross-channel fragment that you created earlier should appear in the list.</span></span> <span data-ttu-id="593bc-170">เลือก แล้วจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-170">Select it, and then select **OK**.</span></span>
1. <span data-ttu-id="593bc-171">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="593bc-171">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="593bc-172">คุณควรเห็นแบนเนอร์โปรโมชันที่ระบุว่า "ข้ามช่องทาง"</span><span class="sxs-lookup"><span data-stu-id="593bc-172">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="593bc-173">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="593bc-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a><span data-ttu-id="593bc-174">สร้างรุ่นเฉพาะช่องทางของหน้าข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-174">Create a channel-specific version of a cross-channel page</span></span>

<span data-ttu-id="593bc-175">การใช้ร่วมกันข้ามช่องทางสนับสนุนการแทนที่เนื้อหาข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-175">Cross-channel sharing supports overrides of cross-channel content.</span></span> <span data-ttu-id="593bc-176">ตัวอย่างเช่น ทั้งหมดยกเว้นช่องทางไซต์หนึ่งของคุณใช้เนื้อหาส่วนเดียวกันร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="593bc-176">For example, all but one of your site channels share the same piece of content.</span></span> <span data-ttu-id="593bc-177">หนึ่งช่องทางไซต์ต้องการเนื้อหาแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="593bc-177">That one site channel requires different content.</span></span> <span data-ttu-id="593bc-178">เมื่อต้องการใช้งานเนื้อหาที่แตกต่างกันนี้ คุณจะแทนที่เนื้อหาข้ามช่องทางที่มีเนื้อหาเฉพาะช่องทางโดยการสร้างรุ่นเฉพาะข่องทางชองหน้าข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-178">To implement the different content for it, you override the cross-channel content with channel-specific content by creating a channel-specific version of the cross-channel page.</span></span>

<span data-ttu-id="593bc-179">เมื่อต้องการสร้างรุ่นเฉพาะช่องทางของหน้าข้ามช่องทางในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="593bc-179">To create a channel-specific version of a cross-channel page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="593bc-180">ในฟิลด์ **ช่องทาง** ที่ด้านขวาบน ให้เลือก **ร้านค้าออนไลน์ข้ามช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="593bc-180">In the **Channel** field in the upper right, select **Cross Channel Online Store**.</span></span>
1. <span data-ttu-id="593bc-181">เปิดหน้าข้ามช่องทางที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="593bc-181">Open the cross-channel page that you created earlier.</span></span>
1. <span data-ttu-id="593bc-182">ในฟิลด์ **ช่องทาง** ที่ด้านขวาบน ให้เลือกช่องทางที่ควรมีเนื้อหาเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="593bc-182">In the **Channel** field in the upper right, select the channel that should have specific content.</span></span> <span data-ttu-id="593bc-183">โปรแกรมแก้ไขหน้าแสดงข้อความที่แจ้งให้คุณสร้างตัวแปรหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="593bc-183">The page editor shows a message that prompts you to create a new page variant.</span></span>
1. <span data-ttu-id="593bc-184">เลือก **สร้างตัวแปรของหน้า**</span><span class="sxs-lookup"><span data-stu-id="593bc-184">Select **Create page variant**.</span></span>
1. <span data-ttu-id="593bc-185">ในช่อง **หลัก** ของตัวแปรหน้า เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="593bc-185">In the **Main** slot of the page variant, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="593bc-186">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **แบนเนอร์โปรโมชั่น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-186">In the **Add Module** dialog box, select the **Promo banner** module, and then select **OK**.</span></span>
1. <span data-ttu-id="593bc-187">ในบานหน้าต่างคุณสมบัติของโมดูล **แบนเนอร์โปรโมชัน** ให้เลือก **เพิ่มข้อความ** แล้วเลือก **ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="593bc-187">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="593bc-188">ในกล่องโต้ตอบ **ข้อความ** ภายใต้ **ข้อความ** ให้ป้อน **เฉพาะช่องทาง** และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="593bc-188">In the **Message** dialog box, under **Text**, enter **Channel-specific**, and the select **OK**.</span></span>
1. <span data-ttu-id="593bc-189">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="593bc-189">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="593bc-190">คุณควรเห็นแบนเนอร์โปรโมชันที่ระบุว่า "เฉพาะช่องทาง"</span><span class="sxs-lookup"><span data-stu-id="593bc-190">You should see the promo banner that says, "Channel-specific."</span></span>
1. <span data-ttu-id="593bc-191">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="593bc-191">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="593bc-192">ตอนนี้ ถ้าคุณใช้ URL พื้นฐานของช่องทาง และไปที่ URL ของหน้าข้ามช่องทางบนไซต์นั้น คุณจะเห็นเนื้อหาเฉพาะช่องทางแทนเนื้อหาข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="593bc-192">Now, if you use the base URL of the channel and go to the URL of the cross-channel page on that site, you will see the channel-specific content instead of the cross-channel content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="593bc-193">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="593bc-193">Additional resources</span></span>

[<span data-ttu-id="593bc-194">วิธีการเพิ่มเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="593bc-194">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="593bc-195">อภิธานศัพท์ของรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="593bc-195">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="593bc-196">สถานะและระยะเวลาใช้งานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="593bc-196">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="593bc-197">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="593bc-197">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]