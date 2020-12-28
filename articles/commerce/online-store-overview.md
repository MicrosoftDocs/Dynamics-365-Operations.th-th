---
title: ภาพรวมไซต์อีคอมเมิร์ซ
description: หัวข้อนี้แสดงภาพรวมของการสนับสนุนสำหรับไซต์อีคอมเมิร์ซใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a5ced6311f32405e544e66d18c912ce40deb177f
ms.sourcegitcommit: 33a746e41cd6f7b6b056b19b550a84f6a1b905d4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/12/2020
ms.locfileid: "4512928"
---
# <a name="e-commerce-site-overview"></a><span data-ttu-id="e1534-103">ภาพรวมไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e1534-103">E-commerce site overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1534-104">หัวข้อนี้แสดงภาพรวมของการสนับสนุนสำหรับไซต์อีคอมเมิร์ซใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-104">This topic provides an overview of the support for e-commerce sites in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="e1534-105">โดยรวมข้อมูลเกี่ยวกับวิธีการเริ่มต้นและจัดการร้านค้าออนไลน์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-105">It includes information about how e-commerce online stores are initialized and managed in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e1534-106">นอกจากนี้ ยังมีการเชื่อมโยงไปยังข้อมูลเพิ่มเติมเกี่ยวกับร้านค้าออนไลน์และเกี่ยวกับวิธีการตั้งค่าและกำหนดไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e1534-106">It also provides links to more information about online stores, and about how to set up and configure an e-commerce site.</span></span> <span data-ttu-id="e1534-107">ถึงแม้ว่าหัวข้อนี้จะครอบคลุมพื้นฐานต่าง ๆ มากมาย แต่จะไม่ครอบคลุมทุกอย่างที่จำเป็นสำหรับการตั้งค่าไซต์อีคอมเมิร์ซการผลิต</span><span class="sxs-lookup"><span data-stu-id="e1534-107">Although this topic covers many of the basics, it doesn't cover everything that is required to set up a production e-commerce site.</span></span> <span data-ttu-id="e1534-108">คุณสามารถดูหัวข้อขั้นสูงเพิ่มเติมได้ในคู่มือ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-108">More advanced topics can be found in the Dynamics 365 Commerce documentation.</span></span>

## <a name="online-store-channel"></a><span data-ttu-id="e1534-109">ช่องทางร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="e1534-109">Online store channel</span></span>

<span data-ttu-id="e1534-110">ก่อนที่คุณจะสามารถสร้างไซต์ของคุณใน Dynamics 365 Commerce ต้องสร้างช่องทางร้านค้าออนไลน์อย่างน้อยหนึ่งร้าน</span><span class="sxs-lookup"><span data-stu-id="e1534-110">Before you can build your site in Dynamics 365 Commerce, at least one online store channel must be set up.</span></span> <span data-ttu-id="e1534-111">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าช่องทางออนไลน์](channel-setup-online.md)</span><span class="sxs-lookup"><span data-stu-id="e1534-111">For more information, see [Set up an online channel](channel-setup-online.md).</span></span> 

<span data-ttu-id="e1534-112">ใน Dynamics 365 Commerce คุณใช้ช่องทางร้านค้าออนไลน์เพื่อสร้างผลิตภัณฑ์ การกำหนดราคา ภาษา วิธีการชำระเงิน โหมดการจัดส่ง ศูนย์เติมสินค้า และด้านอื่นๆ ของประสบการณ์ออนไลน์ที่ควรจะพร้อมใช้งานสำหรับลูกค้าของคุณ.</span><span class="sxs-lookup"><span data-stu-id="e1534-112">In Dynamics 365 Commerce, you use an online store channel to establish the products, pricing, languages, payment methods, delivery modes, fulfillment centers, and other aspects of the online experience that should be available to your customers.</span></span>

<span data-ttu-id="e1534-113">มีเพียงช่องทางร้านค้าออนไลน์เดียวเท่านั้นที่จะได้รับการตั้งค่า ก่อนที่คุณจะสามารถเริ่มต้นใช้งาน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-113">Only one online store channel has to be set up before you can get started with Dynamics 365 Commerce.</span></span> <span data-ttu-id="e1534-114">อย่างไรก็ตาม ไซต์อีคอมเมิร์ซเดียวสามารถให้ประสบการณ์การใช้งานแบบออนไลน์สำหรับร้านค้าออนไลน์หลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="e1534-114">However, a single e-commerce site can provide the online experience for multiple online stores.</span></span> <span data-ttu-id="e1534-115">ตัวอย่างเช่น ถ้าร้านค้าออนไลน์หลายแห่งมีการตั้งค่าเพื่อสนับสนุนภูมิภาคทางภูมิศาสตร์ที่แตกต่างกัน หน้าอีคอมเมิร์ซชุดเดียวสามารถใช้เพื่อให้ประสบการณ์ที่ไม่ซ้ำกันที่กำหนดโดยแต่ละร้านค้า</span><span class="sxs-lookup"><span data-stu-id="e1534-115">For example, if multiple online stores are set up to support different geographical regions, a single set of e-commerce pages can be used to provide the unique experiences that are defined by each store.</span></span> <span data-ttu-id="e1534-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกไซต์เพื่อสนับสนุนร้านค้าออนไลน์หลายแห่ง ให้ดู [เชื่อมโยงไซต์แบบออนไลน์กับช่องทาง](associate-site-online-store.md)</span><span class="sxs-lookup"><span data-stu-id="e1534-116">For more information about how to configure a site to support multiple online stores, see [Associate an online site with a channel](associate-site-online-store.md).</span></span>

<span data-ttu-id="e1534-117">หลังจากตั้งค่าร้านค้าออนไลน์แล้ว จะสามารถเชื่อมโยงกับไซต์ Dynamics 365 Commerce ที่จะทำหน้าที่เป็นหน้าร้านออนไลน์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="e1534-117">After an online store is set up, it can be associated with the Dynamics 365 Commerce site that will serve as your online storefront.</span></span> <span data-ttu-id="e1534-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับร้านค้าออนไลน์และวิธีการตั้งค่า ให้ดูที่ [การตั้งค่าร้านค้าออนไลน์](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores)</span><span class="sxs-lookup"><span data-stu-id="e1534-118">For more information about online stores and how to set them up, see [Set up online stores](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).</span></span>

## <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="e1534-119">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="e1534-119">Deploy a new e-commerce tenant</span></span>

<span data-ttu-id="e1534-120">ระหว่างการเริ่มต้นไซต์อีคอมเมิร์ซ คุณจะได้รับพร้อมท์ให้ป้อนชื่อโดเมน</span><span class="sxs-lookup"><span data-stu-id="e1534-120">During initialization of an e-commerce site, you're prompted for a domain name.</span></span> <span data-ttu-id="e1534-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโดเมนใน Commerce โปรดดู [การตั้งค่าคอนฟิกชื่อโดเมนของคุณ](configure-your-domain-name.md) และ [โดเมนใน Dynamics 365 Commerce](domains-commerce.md)</span><span class="sxs-lookup"><span data-stu-id="e1534-121">For more information about domains in Commerce, see [Configure your domain name](configure-your-domain-name.md) and [Domains in Dynamics 365 Commerce](domains-commerce.md).</span></span> <span data-ttu-id="e1534-122">เมื่อต้องการจัดวางผู้เช่าอีคอมเมิร์ซใหม่โดยใช้ [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) ให้ทำตามขั้นตอนใน [การจัดวางผู้เช่าอีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="e1534-122">To deploy a new e-commerce tenant by using [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), follow the steps in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="e1534-123">หลังจากที่ผู้เช่าอีคอมเมิร์ซของคุณถูกตั้งค่าใน LCS จะมีการระบุลิงค์ไปยังตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-123">After your e-commerce tenant is set up in LCS, a link to Commerce site builder will be provided.</span></span> <span data-ttu-id="e1534-124">จากนั้นคุณสามารถใช้ตัวสร้างไซต์ Commerce เพื่อเริ่มต้นและตั้งค่าคอนฟิกไซต์อีคอมเมิร์ซของคุณได้</span><span class="sxs-lookup"><span data-stu-id="e1534-124">You can then use Commerce site builder to initialize and configure your e-commerce sites.</span></span>

## <a name="initialize-your-e-commerce-site"></a><span data-ttu-id="e1534-125">เริ่มต้นไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="e1534-125">Initialize your e-commerce site</span></span>

<span data-ttu-id="e1534-126">เมื่อคุณเริ่มต้นตัวสร้างไซต์ Commerce จาก LCS หน้า **ไซต์** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="e1534-126">When you start Commerce site builder from LCS, the **Sites** page appears.</span></span> <span data-ttu-id="e1534-127">หน้านี้มีไซต์ที่ตั้งค่าคอนฟิกไว้ล่วงหน้าสองไซต์ **ค่าเริ่มต้น** และ **fabrikam** ดังที่แสดงในตัวอย่างในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e1534-127">This page includes two preconfigured sites, **default** and **fabrikam**, as shown in the example in the following illustration.</span></span>

![หน้าไซต์ในตัวสร้างไซต์ Commerce](media/e-commerce-site-01.png)

<span data-ttu-id="e1534-129">เมื่อคุณเลือกไซต์ใดไซต์หนึ่งต่อไปนี้ คุณจะได้รับพร้อมท์ให้เลือกชื่อโดเมนช่องทางร้านค้าออนไลน์เริ่มต้น ภาษาที่สนับสนุนสำหรับช่องทางที่เลือก และเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="e1534-129">When you select one of these sites, you're prompted to select a domain name, a default online store channel, a supported language for the selected channel, and a path.</span></span> <span data-ttu-id="e1534-130">ถ้ามีการใช้ช่องทางนีเพียงช่องเดียว คุณก็สามารถปล่อยให้เส้นทางว่างเปล่าได้</span><span class="sxs-lookup"><span data-stu-id="e1534-130">If only one channel is used, you can leave the path blank.</span></span> <span data-ttu-id="e1534-131">สามารถตั้งค่าคอนฟิกช่องทางหรือภาษาของร้านค้าออนไลน์เพิ่มเติมในภายหลังในโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-131">More online store channels or languages can be configured later in Commerce site builder.</span></span> <span data-ttu-id="e1534-132">แต่ละช่องทางหรือภาษาเพิ่มเติมจะต้องมีพาธที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="e1534-132">Each additional channel or language will require a unique path.</span></span> <span data-ttu-id="e1534-133">ตัวอย่างเช่น คุณมีช่องทางออนไลน์สองช่องที่เชื่อมโยงกับไซต์เดียวและชื่อโดเมนของไซต์คือ `www.fabrikam.com`</span><span class="sxs-lookup"><span data-stu-id="e1534-133">For example, you have two online channels that are associated with a single site, and the domain name for the site is `www.fabrikam.com`.</span></span> <span data-ttu-id="e1534-134">ในกรณีนี้ พาธสำหรับหนึ่งช่องทางอาจเป็นค่าเริ่มต้นที่ไม่มีพาธ (`https://www.fabrikam.com`) และช่องทางที่สองสามารถตั้งค่าเป็นพาธใหม่ เช่น **site2** ซึ่งจะมี URL `https://www.fabrikam.com/site2`</span><span class="sxs-lookup"><span data-stu-id="e1534-134">In this case, the path for one channel can be the default value that has no path (`https://www.fabrikam.com`), and the second channel can be set to a new path, such as **site2**, that will have the URL `https://www.fabrikam.com/site2`.</span></span> <span data-ttu-id="e1534-135">ภาพประกอบต่อไปนี้แสดงตัวอย่างของกล่องโต้ตอบการเริ่มต้นของไซต์ในตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-135">The following illustration shows an example of a site initialization dialog box in Commerce site builder.</span></span>

![กล่องโต้ตอบการเริ่มต้นไซต์ในตัวสร้างไซต์ Commerce](media/e-commerce-site-02.png)

<span data-ttu-id="e1534-137">หน้า **ไซต์** ยังรวมถึงปุ่ม **ไซต์ใหม่** ด้วย</span><span class="sxs-lookup"><span data-stu-id="e1534-137">The **Sites** page also includes a **New site** button.</span></span> <span data-ttu-id="e1534-138">กล่องโต้ตอบที่ปรากฏขึ้นเมื่อคุณเลือกปุ่มนี้คล้ายกับกล่องโต้ตอบการเริ่มต้นของไซต์แต่ใช้เพื่อสร้างไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="e1534-138">The dialog box that appears when you select this button resembles the site initialization dialog box, but it's used to create a new site.</span></span> <span data-ttu-id="e1534-139">ไซต์ใหม่จะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="e1534-139">New sites are blank.</span></span> <span data-ttu-id="e1534-140">โดยไม่รวมแม่แบบเริ่มต้นหน้า และรูปภาพเดียวกันที่มีให้กับไซต์ **เริ่มต้น** และ **fabrikam**</span><span class="sxs-lookup"><span data-stu-id="e1534-140">They don't include the same default templates, fragments, pages, and images that are provided with the **default** and **fabrikam** sites.</span></span> <span data-ttu-id="e1534-141">อย่างไรก็ตาม คุณสามารถเปิดตั๋วสนับสนุนเพื่อร้องขอให้มีการเพิ่มสำเนาของเนื้อหาเริ่มต้นลงในไซต์เปล่าใหม่</span><span class="sxs-lookup"><span data-stu-id="e1534-141">However, as you require, you can open a support ticket to request that a copy of the default content be added to a new blank site.</span></span> <span data-ttu-id="e1534-142">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="e1534-142">For more information, see [Create an e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="e1534-143">หลังจากที่มีการเริ่มต้นไซต์ใหม่แล้ว หน้า **แรก** โปรแกรมสร้างไซต์ Commerceจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="e1534-143">After a new site is initialized, the Commerce site builder **Home** page appears.</span></span> <span data-ttu-id="e1534-144">หน้านี้มีลิงค์ไปยังการดำเนินการทั่วไปและเนื้อหาคำแนะนำ ดังที่แสดงในตัวอย่างในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e1534-144">This page includes links to common actions and guidance content, as shown in the example in the following illustration.</span></span>

![ลิงค์บนหน้าแรกในตัวสร้างไซต์ Commerce](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a><span data-ttu-id="e1534-146">แก้ไขช่องทางออนไลน์ของร้านค้าหรือเพิ่มช่องทางออนไลน์ของร้านค้าลงในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e1534-146">Modify online store channels or add online store channels to an e-commerce site</span></span>

<span data-ttu-id="e1534-147">หลังจากที่สร้างไซต์อีคอมเมิร์ซแล้ว คุณสามารถเปลี่ยนช่องทางที่เชื่อมโยงโดยปฏิบัติตามขั้นตอนต่าง ๆ ใน [การเชื่อมโยงไซต์อีคอมเมิร์ซกับช่องทางออนไลน์](associate-site-online-store.md)</span><span class="sxs-lookup"><span data-stu-id="e1534-147">After an e-commerce site is created, you can change the channel that it's associated with by following the steps in [Associate an e-commerce site with an online channel](associate-site-online-store.md).</span></span> <span data-ttu-id="e1534-148">ตัวอย่างในภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถเปลี่ยนหมายเลขหน่วยปฏิบัติงานของช่องทาง (OUN) บนหน้า **ช่องทาง** (**การตั้งค่าไซต์ \> ช่องทาง**)</span><span class="sxs-lookup"><span data-stu-id="e1534-148">The example in the following illustration shows how a channel operating unit number (OUN) can be changed on the **Channels** page (**Site settings \> Channels**).</span></span> <span data-ttu-id="e1534-149">หลังจากที่คุณทำการเปลี่ยนแปลงเสร็จเรียบร้อยแล้ว ให้ตรวจสอบให้แน่ใจว่าได้เลือก **บันทึกและเผยแพร่** แล้ว</span><span class="sxs-lookup"><span data-stu-id="e1534-149">After you've finished making a change, be sure to select **Save and publish**.</span></span> <span data-ttu-id="e1534-150">วิธีนี้ช่วยให้คุณมั่นใจได้ว่าการเปลี่ยนแปลงจะเผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="e1534-150">In this way, you ensure that the change is published.</span></span>

![หน้าช่องทางในตัวสร้างไซต์ Commerce](media/e-commerce-site-04.png)

<span data-ttu-id="e1534-152">คุณสามารถเพิ่มช่องทางใหม่ได้โดยการเลือก **เพิ่มช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="e1534-152">You can add new channels by selecting **Add a channel**.</span></span> <span data-ttu-id="e1534-153">เมื่อต้องการเพิ่มภาษาใหม่ลงในช่องทาง ให้เลือกช่องทาง แล้วเลือก **เพิ่มตำแหน่งที่ตั้ง** ในกล่องโต้ตอบช่องทางที่จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="e1534-153">To add new languages to a channel, select the channel, and then select **Add a locale** in the channel dialog box that appears.</span></span> <span data-ttu-id="e1534-154">ก่อนที่จะปรากฏในกล่องโต้ตอบ จะต้องตั้งค่าคอนฟิกที่ตั้งค่าคอนฟิกไว้ล่วงหน้าสำหรับช่องทางร้านค้าออนไลน์ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="e1534-154">Before locales can appear in the dialog box, they must be preconfigured for the online store channel in Commerce headquarters.</span></span>

![กล่องโต้ตอบช่องทางในตัวสร้างไซต์ Commerce](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a><span data-ttu-id="e1534-156">ตั้งค่าผู้เช่า B2C ของ Azure</span><span class="sxs-lookup"><span data-stu-id="e1534-156">Set up an Azure B2C tenant</span></span>

<span data-ttu-id="e1534-157">Dynamics 365 Commerce ใช้ข้อมูลธุรกิจ-ผู้บริโภค Azure Active Directory (Azure AD) (B2C) เพื่อสนับสนุนข้อมูลประจำตัวของผู้ใช้และขั้นตอนการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e1534-157">Dynamics 365 Commerce uses Azure Active Directory (Azure AD) business-to-consumer (B2C) to support user credential and authentication flows.</span></span> <span data-ttu-id="e1534-158">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าผู้เช่าของ Azure B2C ให้ดู [การตั้งค่าผู้เช่า B2C ใน Commerce](set-up-b2c-tenant.md) [ตั้งค่าหน้าแบบกำหนดเองสำหรับการลงชื่อเข้าใช้ของผู้ใช้](custom-pages-user-logins.md) และ [ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce](configure-multi-b2c-tenants.md)</span><span class="sxs-lookup"><span data-stu-id="e1534-158">For information about how to set up your Azure B2C tenant, see [Set up a B2C tenant in Commerce](set-up-b2c-tenant.md), [Set up custom pages for user sign-ins](custom-pages-user-logins.md), and [Configure multiple B2C tenants in a Commerce environment](configure-multi-b2c-tenants.md).</span></span>

## <a name="overview-of-the-default-site-pages"></a><span data-ttu-id="e1534-159">ภาพรวมของหน้าไซต์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1534-159">Overview of the default site pages</span></span>

<span data-ttu-id="e1534-160">ไซต์ **ค่าเริ่มต้น** และ **fabrikam** รวมถึงแม่แบบ ส่วน และหน้าที่กำหนดไว้ล่วงหน้าเพื่อช่วยคุณในการเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e1534-160">The **default** and **fabrikam** sites include preconfigured templates, fragments, and pages to help you get started.</span></span> <span data-ttu-id="e1534-161">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1534-161">For more information, see the following topics:</span></span>

- [<span data-ttu-id="e1534-162">ภาพรวมของโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="e1534-162">Home page overview</span></span>](quick-tour-home-page.md)
- [<span data-ttu-id="e1534-163">ภาพรวมของหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1534-163">Product details page overview</span></span>](quick-tour-pdp.md)
- [<span data-ttu-id="e1534-164">ภาพรวมของรถเข็นและหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="e1534-164">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)
- [<span data-ttu-id="e1534-165">ภาพรวมของหน้าการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1534-165">Account management pages overview</span></span>](quick-tour-account-management.md)

## <a name="manage-site-settings"></a><span data-ttu-id="e1534-166">จัดการการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="e1534-166">Manage site settings</span></span>

<span data-ttu-id="e1534-167">สำหรับข้อมูลเกี่ยวกับจัดการการตั้งค่าไซต์ของคุณ ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1534-167">For information about how to manage your site settings, see the following topics:</span></span>

- [<span data-ttu-id="e1534-168">จัดการผู้ใช้และบทบาทอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e1534-168">Manage e-commerce users and roles</span></span>](manage-ecommerce-users-roles.md)
- [<span data-ttu-id="e1534-169">ข้อควรพิจารณาเกี่ยวกับการเพิ่มประสิทธิภาพโปรแกรมค้นหา (SEO) สำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e1534-169">Search engine optimization (SEO) considerations for your site</span></span>](/search-engine-optimization-considerations.md)
- [<span data-ttu-id="e1534-170">จัดการนโยบายความปลอดภัยของเนื้อหา (CSP)</span><span class="sxs-lookup"><span data-stu-id="e1534-170">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
- [<span data-ttu-id="e1534-171">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="e1534-171">Select a site theme</span></span>](select-site-theme.md)

## <a name="manage-site-content"></a><span data-ttu-id="e1534-172">จัดการเนื้อหาไซต์</span><span class="sxs-lookup"><span data-stu-id="e1534-172">Manage site content</span></span>

<span data-ttu-id="e1534-173">สำหรับข้อมูลเกี่ยวกับจัดการเนื้อหาไซต์ของคุณ ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1534-173">For information about how to manage site content, see the following topics:</span></span>

- [<span data-ttu-id="e1534-174">อภิธานศัพท์ของรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="e1534-174">Page model glossary</span></span>](page-elements-overview.md)
- [<span data-ttu-id="e1534-175">สถานะและระยะเวลาใช้งานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="e1534-175">Document states and lifecycle</span></span>](document-states-overview.md)
- [<span data-ttu-id="e1534-176">แม่แบบและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="e1534-176">Templates and layout</span></span>](templates-layouts-overview.md)
- [<span data-ttu-id="e1534-177">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="e1534-177">Work with fragments</span></span>](work-with-fragments.md)
- [<span data-ttu-id="e1534-178">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="e1534-178">Work with modules</span></span>](work-with-modules.md)
- [<span data-ttu-id="e1534-179">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="e1534-179">Digital asset management overview</span></span>](dam-overview.md)
- [<span data-ttu-id="e1534-180">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="e1534-180">Module library overview</span></span>](starter-kit-overview.md)

## <a name="additional-resources"></a><span data-ttu-id="e1534-181">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e1534-181">Additional resources</span></span>

[<span data-ttu-id="e1534-182">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e1534-182">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e1534-183">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="e1534-183">Deploy a new e-commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e1534-184">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="e1534-184">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e1534-185">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="e1534-185">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e1534-186">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="e1534-186">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e1534-187">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="e1534-187">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="e1534-188">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="e1534-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
