---
title: โดเมนใน Dynamics 365 Commerce
description: หัวข้อนี้จะอธิบายวิธีการจัดการโดเมนใน Microsoft Dynamics 365 Commerce
author: BrShoo
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 0a494a36d1d8fa55521c416efd4262d860e1a708
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022847"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="52d37-103">โดเมนใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="52d37-104">หัวข้อนี้จะอธิบายวิธีการจัดการโดเมนใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="52d37-105">โดเมนคือที่อยู่เว็บที่ใช้เพื่อนำทางไปยังไซต์ Dynamics 365 Commerce ในเว็บเบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="52d37-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="52d37-106">คุณควบคุมการจัดการโดเมนของคุณด้วยผู้ให้บริการเซิร์ฟเวอร์ชื่อโดเมน (DNS) ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="52d37-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="52d37-107">โดเมนมีการอ้างอิงในตัวสร้างไซต์ Dynamics 365 Commerce เพื่อประสานงานว่าจะเข้าถึงไซต์อย่างไรเมื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="52d37-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="52d37-108">หัวข้อนี้จะเสนอว่าโดเมนมีการจัดการและการอ้างอิงตลอดระยะเวลาของการพัฒนาและการเปิดใช้งานไซต์ Commerce site อย่างไร</span><span class="sxs-lookup"><span data-stu-id="52d37-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="52d37-109">การเตรียมใช้งานและชื่อโฮสต์ที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="52d37-109">Provisioning and supported host names</span></span>

<span data-ttu-id="52d37-110">เมื่อเตรียมใช้งานสภาพแวดล้อมอีคอมเมิร์ซใน [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) กล่อง **ชื่อโฮสต์ที่ได้รับการสนับสนุน** บนหน้าจอการเตรียมใช้งานอีคอมเมิร์ซถูกใช้เพื่อป้อนโดเมนที่จะเชื่อมโยงกับสภาพแวดล้อม Commerce ที่ปรับใช้</span><span class="sxs-lookup"><span data-stu-id="52d37-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="52d37-111">โดเมนเหล่านี้จะเป็นชื่อของเซิร์ฟเวอร์ชื่อโดเมน (DNS) ที่เชื่อมต่อกับลูกค้าที่ซึ่งจะเป็นโฮสต์ของเว็บไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="52d37-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="52d37-112">การป้อนโดเมนในลำขั้นนี้ไม่ได้เริ่มต้นการแปลงการรับส่งข้อมูลสำหรับโดเมน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="52d37-113">การรับส่งข้อมูลสำหรับโดเมนจะถูกส่งไปยังปลายทาง Commerce เมื่อมีการอัปเดตเรกคอร์ด DNS CNAME เพื่อใช้ปลายทาง Commerce กับโดเมนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="52d37-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="52d37-114">คุณสามารถป้อนหลายโดเมนลงในกล่อง **ชื่อโฮสต์ที่ได้รับการสนับสนุน** โดยการแยกด้วยเซมิโคลอน</span><span class="sxs-lookup"><span data-stu-id="52d37-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="52d37-115">ภาพประกอบต่อไปนี้แสดงหน้าจอการเตรียมใช้งานอีคอมเมิร์ซของ LCS ที่มีการเน้นกล่อง **ชื่อโฮสต์ที่ได้รับการสนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="52d37-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![หน้าจอการเตรียมใช้งานอีคอมเมิร์ซของ LCS ที่มีการเน้นกล่อง **ชื่อโฮสต์ที่ได้รับการสนับสนุน**](./media/Domains_ProvisioningeCommerceScreen_publish.png)

<span data-ttu-id="52d37-117">คุณสามารถสร้างคำขอบริการเพื่อเพิ่มโดเมนเพิ่มเติมลงในสภาพแวดล้อมได้ถ้ามีการเตรียมใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="52d37-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="52d37-118">เมื่อต้องการสร้างคำขอบริการใน LCS ภายในสภาพแวดล้อมของคุณ ให้ไปที่ **การสนับสนุน \>ปัญหาที่รับการสนับสนุน** และเลือก **ส่งเหตุการณ์**</span><span class="sxs-lookup"><span data-stu-id="52d37-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="52d37-119">URL ที่สร้างโดย Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-119">Commerce-generated URLs</span></span>

<span data-ttu-id="52d37-120">เมื่อเตรียมใช้งานสภาพแวดล้อมอีคอมเมิร์ซของ Dynamics 365 Commerce Commerce จะสร้าง URL ซึ่งจะเป็นที่อยู่ในการทำงานสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="52d37-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="52d37-121">มีการอ้างอิง URL นี้ในลิงก์ไซต์อีคอมเมิร์ซที่แสดงอยู่ใน LCS หลังจากที่มีการเตรียมใช้งานสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="52d37-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="52d37-122">URL ที่สร้างโดย Commerce อยู่ในรูปแบบ `https://<e-commerce tenant name>.commerce.dynamics.com` โดยชื่อผู้เช่าอีคอมเมิร์ซเป็นชื่อที่ป้อนใน LCS สำหรับสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="52d37-123">คุณสามารถใช้ชื่อโฮสต์ของไซต์การทำงานจริงในสภาพแวดล้อม Sandbox ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="52d37-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="52d37-124">ตัวเลือกนี้เหมาะอย่างยิ่งเมื่อคุณจะคัดลอกไซต์จากสภาพแวดล้อม Sandbox ไปยังการทำงานจริง</span><span class="sxs-lookup"><span data-stu-id="52d37-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="52d37-125">การตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-125">Site setup</span></span>

<span data-ttu-id="52d37-126">หลังจากที่คุณได้เตรียมใช้งานสภาพแวดล้อมของอีคอมเมิร์ซแล้ว คุณต้องตั้งค่าไซต์ของคุณในตัวสร้างไซต์ Commerce เพื่อเชื่อมโยงไซต์ของคุณกับ URL ที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="52d37-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="52d37-127">เมื่อคุณตั้งค่าไซต์ในตัวสร้างไซต์เป็นครั้งแรก กล่องโต้ตอบ **ตั้งค่าไซต์ของคุณ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="52d37-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="52d37-128">ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **ตั้งค่าไซต์ของคุณ** สำหรับไซต์ที่ชื่อว่า "default" เมื่อคุณเข้าถึงไซต์เป็นครั้งแรกในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![กล่องโต้ตอบ **ตั้งค่าไซต์ของคุณ**](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="52d37-130">กล่อง **เลือกโดเมน** ช่วยให้คุณสามารถเชื่อมโยงหนึ่งในชื่อโฮสต์ที่ได้รับการสนับสนุนที่มีให้กับไซต์ของคุณใน LCS กับไซต์ของคุณในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="52d37-131">กล่อง **พาธ** อาจปล่อยว่างไว้หรืออาจเพิ่มสตริงของพาธเพิ่มเติมที่จะแสดงให้เห็นใน URL ที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="52d37-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="52d37-132">การปล่อยกล่อง **พาธ** ว่างไว้เชื่อมโยง URL ฐานที่สร้างโดย Commerce กับไซต์ที่มีการตั้งค่าในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="52d37-133">พาธต้องไม่ซ้ำกันสำหรับไซต์/โดเมนแต่ละคู่</span><span class="sxs-lookup"><span data-stu-id="52d37-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="52d37-134">ภายในไซต์และโดเมนที่เลือก จะมีเพียงไซต์เดียวในสภาพแวดล้อมเท่านั้นที่สามารถใช้พาธที่ว่างเปล่าหรือเชื่อมโยงกับสตริงการพาธที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="52d37-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="52d37-135">สตริงที่เพิ่มเข้าไปในฟิลด์ **พาธ** ในระหว่างการตั้งค่าไซต์จะกลายเป็นพาธย่อยของ URL ฐานที่สร้างโดย Commerce ซึ่งใช้ในการเข้าถึงไซต์ในเว็บเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="52d37-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="52d37-136">พาธนี้เรียกอีกอย่างว่า **พาธการจับคู่** เมื่อเพิ่มช่องทางในส่วนการตั้งค่าคอนฟิก **การตั้งค่าไซต์ \> ช่องทาง** ของตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="52d37-137">ตัวอย่างเช่น ถ้าคุณมีไซต์ในตัวสร้างไซต์ที่ชื่อ"fabrikam" ในผู้เช่าอีคอมเมิร์ซที่ชื่อ "xyz" และถ้าคุณตั้งค่าไซต์ที่มีพาธที่ว่างเปล่า คุณจะเข้าถึงเนื้อหาของไซต์ที่เผยแพร่ในเว็บเบราว์เซอร์โดยไปที่ URL ฐานที่สร้างโดย Commerce โดยตรง:</span><span class="sxs-lookup"><span data-stu-id="52d37-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="52d37-138">หรือถ้าคุณได้เพิ่มพาธของ "fabrikam" ในระหว่างการตั้งค่าไซต์เดียวกันนี้ คุณจะเข้าถึงเนื้อหาของไซต์ที่เผยแพร่ในเว็บเบราว์เซอร์โดยใช้ URL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="52d37-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="52d37-139">หน้าและ URL</span><span class="sxs-lookup"><span data-stu-id="52d37-139">Pages and URLs</span></span>

<span data-ttu-id="52d37-140">หลังจากที่มีการตั้งค่าไซต์ของคุณโดยใช้พาธ, URL ทั้งหมดที่เชื่อมโยงกับหน้าในตัวสร้างไซต์จะสร้างบน URL ที่ทำงาน (URL ที่สร้างโดย Commerce หรือ URL ที่สร้างโดย Commerce พร้อมกับพาธ) สำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="52d37-141">การสร้าง URL ใหม่ในตัวสร้างไซต์ (**URLS/> + ใหม่**) โดยการเลือกหน้าจากรายการในกล่องโต้ตอบ **URL ใหม่** และการป้อนพาธ URL สำหรับหน้านั้นจะเชื่อมโยง URL นั้นกับหน้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="52d37-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="52d37-142">ค่าพาธของ URL จะผนวกเข้ากับ URL ที่ทำงานของไซต์เพื่อเข้าถึงหน้า และมีการติดป้ายชื่อ `./<URL path>` ในรายชื่อ URL ของหน้า **URL** ในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="52d37-143">ภาพประกอบต่อไปนี้จะแสดงกล่องโต้ตอบ **URL ใหม่** ในตัวสร้างไซต์โดยมีการเน้นพาธ URL</span><span class="sxs-lookup"><span data-stu-id="52d37-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![กล่องโต้ตอบ **URL ใหม่** ในตัวสร้างไซต์](./media/Domains_PageSetup2a.png)

<span data-ttu-id="52d37-145">ภาพประกอบต่อไปนี้จะแสดงหน้า **URL** ในตัวสร้างไซต์ที่มีตัวอย่างการเน้น URL ในรายการ</span><span class="sxs-lookup"><span data-stu-id="52d37-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![รันตัวเลือกขั้นตอนของผู้ใช้ในขั้นตอนของนโยบาย](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="52d37-147">โดเมนในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-147">Domains in site builder</span></span>

<span data-ttu-id="52d37-148">ค่าของชื่อโฮสต์ที่ได้รับการสนับสนุนจะพสามารถใช้ในการเชื่อมโยงกับโดเมนเมื่อตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="52d37-149">เมื่อเลือกค่าชื่อโฮสต์ที่ได้รับการสนับสนุนเป็นโดเมน คุณจะเห็นโดเมนที่เลือกที่อ้างอิงในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="52d37-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="52d37-150">โดเมนนี้เป็นเพียงการอ้างอิงภายในสภาพแวดล้อม Commerce เท่านั้น การรับส่งข้อมูลจริงสำหรับโดเมนนั้นจะยังไม่ได้ส่งต่อไปยัง Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="52d37-151">เมื่อทำงานกับไซต์ในตัวสร้างไซต์ ถ้าคุณมีสองไซต์ที่ตั้งค่าด้วยโดเมนที่แตกต่างกันสองโดเมน คุณสามารถผนวกแอททริบิวต์ **?domain=** กับ URL ที่ทำงานของคุณเพื่อเข้าถึงเนื้อหาไซต์ที่เผยแพร่ในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="52d37-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="52d37-152">ตัวอย่างเช่น มีการเตรียมใช้งานสภาพแวดล้อม "xyz" และมีการสร้างไซต์สองแห่งและเชื่อมโยงในตัวสร้างไซต์: ไซต์หนึ่งมีโดเมน `www.fabrikam.com`และอีกไซต์มีโดเมน `www.constoso.com`</span><span class="sxs-lookup"><span data-stu-id="52d37-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="52d37-153">มีการตั้งค่าไซต์แต่ละไซต์โดยใช้พาธที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="52d37-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="52d37-154">จากนั้นคุณจะสามารถเข้าถึงไซต์ทั้งคู่เหล่านี้ได้ในเว็บเบราว์เซอร์ดังต่อไปนี้โดยใช้แอททริบิวต์ **?domain=**:</span><span class="sxs-lookup"><span data-stu-id="52d37-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="52d37-155">เมื่อสตริงการสอบถามโดเมนไม่ได้กำหนดไว้ในสภาพแวดล้อมที่มีโดเมนหลายโดเมน Commerce จะใช้โดเมนแรกที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="52d37-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="52d37-156">ตัวอย่างเช่น ถ้ามีการเตรียมใช้งานพาธ "fabrikam" ไว้เป็นอันดับแรกในระหว่างการตั้งค่าไซต์ สามารถใช้ URL `https://xyz.commerce.dynamics.com` เพื่อเข้าถึงไซต์เนื้อหาของไซต์ที่เผยแพร่แล้วสำหรับ `www.fabrikam.com` ได้</span><span class="sxs-lookup"><span data-stu-id="52d37-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="52d37-157">การส่งต่อการรับส่งข้อมูลในการทำงานจริง</span><span class="sxs-lookup"><span data-stu-id="52d37-157">Traffic forwarding in production</span></span>

<span data-ttu-id="52d37-158">คุณสามารถจำลองหลายโดเมนโดยใช้พารามิเตอร์สตริงการสอบถามโดเมนบนปลายทาง commerce.dynamics.com ของตัวเองได้</span><span class="sxs-lookup"><span data-stu-id="52d37-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="52d37-159">แต่เมื่อคุณต้องการใช้งานในการทำงานจริง คุณต้องส่งต่อการรับส่งข้อมูลสำหรับโดเมนที่กำหนดเองของคุณไปยังปลายทาง `<e-commerce tenant name>.commerce.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="52d37-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="52d37-160">ปลายทาง `<e-commerce tenant name>.commerce.dynamics.com` ไม่สนับสนุน Secure Sockets Layers (SSL) สำหรับโดเมนที่กำหนดเอง ดังนั้นคุณต้องตั้งค่าโดเมนที่กำหนดเองโดยใช้บริการประตูด้านหน้าหรือเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="52d37-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="52d37-161">หากต้องการตั้งค่าโดเมนแบบกำหนดเองโดยใช้บริการประตูหน้าหรือ CDN คุณมีสองตัวเลือกดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="52d37-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="52d37-162">ตั้งค่าบริการประตูหน้า เช่น Azure Front Door เพื่อจัดการกับการรับส่งข้อมูลฟร้อนเอนด์และเชื่อมต่อกับสภาพแวดล้อม Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="52d37-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="52d37-163">ซึ่งช่วยให้สามารถควบคุมการจัดการโดเมนและใบรับรองและนโยบายความปลอดภัยแบบละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="52d37-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="52d37-164">ใช้อินสแตนซ์ Azure Front Door ที่ให้มากับ Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="52d37-165">การดำเนินการนี้จำเป็นต้องมีการดำเนินร่วมกับทีม Dynamics 365 Commerce สำหรับการตรวจสอบโดเมนและการขอรับใบรับรอง SSL สำหรับโดเมนการทำงานจริงของคุณ</span><span class="sxs-lookup"><span data-stu-id="52d37-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="52d37-166">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าบริการ CDN โดยตรง ให้ดูที่ [การเพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)](add-cdn-support.md)</span><span class="sxs-lookup"><span data-stu-id="52d37-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="52d37-167">เมื่อต้องการใช้อินสแตนซ์ Azure Front Door ที่ให้มากับ Commerce คุณต้องสร้างคำขอรับบริการสำหรับความช่วยเหลือในการตั้งค่า CDN จากทีมเตรียมความพร้อมของ Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="52d37-168">คุณจะต้องระบุชื่อบริษัทของคุณ โดเมนการทำงานจริง รหัสสภาพแวดล้อม และชื่อผู้เช่าอีคอมเมิร์ซสำหรับการทำงานจริง</span><span class="sxs-lookup"><span data-stu-id="52d37-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="52d37-169">คุณจะต้องยืนยันว่าเป็นโดเมนที่มีอยู่ (ใช้สำหรับไซต์ที่ใช้งานอยู่ในปัจจุบัน) หรือเป็นโดเมนใหม่</span><span class="sxs-lookup"><span data-stu-id="52d37-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="52d37-170">สำหรับโดเมนใหม่ การตรวจสอบโดเมนและใบรับรอง SSL สามารถทำได้ในขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="52d37-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="52d37-171">สำหรับโดเมนที่ให้บริการเว็บไซต์ที่มีอยู่ มีกระบวนการหลายขั้นตอนที่จำเป็นในการสร้างการตรวจสอบความถูกต้องของโดเมนและใบรับรอง SSL</span><span class="sxs-lookup"><span data-stu-id="52d37-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="52d37-172">กระบวนการนี้มีข้อตกลงระดับการให้บริการ (SLA) แบบ 7 วันทำการสำหรับโดเมนที่จะใช้งาน เนื่องจากมีขั้นตอนตามลำดับหลายขั้น</span><span class="sxs-lookup"><span data-stu-id="52d37-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="52d37-173">เมื่อต้องการสร้างคำขอบริการใน LCS ภายในสภาพแวดล้อมของคุณ ให้ไปที่ **การสนับสนุน \>ปัญหาที่รับการสนับสนุน** และเลือก **ส่งเหตุการณ์**</span><span class="sxs-lookup"><span data-stu-id="52d37-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="52d37-174">โดเมนแบบกำหนดเองที่มี SSL สนับสนุนเฉพาะในสภาพแวดล้อมการทำงานจริงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="52d37-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="52d37-175">สำหรับสภาพแวดล้อมที่ไม่ใช่สำหรับการทำงานจริง เช่น Sandbox และการทดสอบการยอมรับของผู้ใช้ (UAT) ให้ใช้ URL ที่สร้างโดย Commerce เพื่อเข้าถึงเนื้อหาที่เผยแพร่ในเว็บเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="52d37-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="52d37-176">กระบวนการใบรับรอง SSL</span><span class="sxs-lookup"><span data-stu-id="52d37-176">SSL certificate process</span></span>

<span data-ttu-id="52d37-177">เมื่อส่งคำขอรับบริการแล้ว ทีม Commerce จะประสานงานขั้นตอนต่อไปนี้ให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="52d37-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="52d37-178">สำหรับโดเมนใหม่:</span><span class="sxs-lookup"><span data-stu-id="52d37-178">For new domains:</span></span>
- <span data-ttu-id="52d37-179">ทีม Commerce จะตั้งค่าอินสแตนซ์ Azure Front Door (โฮสต์ Commerce)</span><span class="sxs-lookup"><span data-stu-id="52d37-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="52d37-180">ทีม Commerce จะกำหนดเรกคอร์ด CNAME เพื่อชี้ไปที่โดเมนที่กำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="52d37-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="52d37-181">หลังจากที่มีการอัปเดตเรกคอร์ด CNAME อินสแตน Azure Front Door ที่โฮสต์บน Commerce จะสามารถตรวจสอบความเป็นเจ้าของโดเมนและรับใบรับรอง SSL ได้</span><span class="sxs-lookup"><span data-stu-id="52d37-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="52d37-182">สำหรับโดเมนที่มีอยู่/ที่ใช้งานอยู่:</span><span class="sxs-lookup"><span data-stu-id="52d37-182">For existing/active domains:</span></span>
- <span data-ttu-id="52d37-183">ทีม Commerce จะแนะนำให้คุณเพิ่มเรกคอร์ด CNAME `afdverify.<custom-domain>` เพื่อระบุผู้ให้บริการ DNS โดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="52d37-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="52d37-184">เมื่อเสร็จสมบูรณ์ ทีม Commerce จะเพิ่มโดเมนลงในอินสแตนซ์ Azure Front Door และระบุเรกคอร์ด TXT DNS เพิ่มเติมที่จะเพิ่มลงใน DNS สำหรับโดเมน</span><span class="sxs-lookup"><span data-stu-id="52d37-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="52d37-185">หลังจากที่เรกคอร์ด TXT เสร็จสมบูรณ์แล้ว ทีม Commerce จะทำการอัปเดต Azure Front Door สำหรับโดเมนที่จะตั้งค่าใบรับรอง SSL</span><span class="sxs-lookup"><span data-stu-id="52d37-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="52d37-186">โดเมน Apex</span><span class="sxs-lookup"><span data-stu-id="52d37-186">Apex domains</span></span>

<span data-ttu-id="52d37-187">อินสแตนซ์ Azure Front Door ที่ให้มากับ Commerce ไม่สนับสนุนโดเมน apex (โดเมนรากที่ไม่มีโดเมนย่อย)</span><span class="sxs-lookup"><span data-stu-id="52d37-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="52d37-188">โดเมน Apex ต้องมีที่อยู่ IP เพื่อแก้ไข และมีอินสแตนซ์ Commerce Azure Front Door ที่มีปลายทางเสมือนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="52d37-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="52d37-189">เมื่อต้องการใช้โดเมนแบบ apex คุณมีสองตัวเลือกดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="52d37-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="52d37-190">**ตัวเลือก 1** - ใช้ตัวให้บริการ DNS ของคุณเพื่อเปลี่ยนเส้นทางโดเมน apex กับโดเมน "www"</span><span class="sxs-lookup"><span data-stu-id="52d37-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="52d37-191">ตัวอย่างเช่น fabrikam.com เปลี่ยนเส้นทางไปยัง `www.fabrikam.com` โดยที่ `www.fabrikam.com` เป็นเรกคอร์ด CNAME ซึ่งชี้ไปยังอินสแตนซ์ Azure Front Door ที่โฮสต์บน Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="52d37-192">**ตัวเลือก 2** - ตั้งค่าอินสแตนซ์ CDN/ประตูหน้าด้วยตัวคุณเองเพื่อโฮสต์โดเมน apex</span><span class="sxs-lookup"><span data-stu-id="52d37-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="52d37-193">หากคุณใช้ Azure Front Door คุณต้องตั้งค่า Azure DNS ในการสมัครใช้งานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="52d37-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="52d37-194">โดเมน apex ที่โฮสต์บน Azure DNS สามารถชี้ไปที่ Azure Front Door ของคุณเป็นเรกคอร์ดนามแฝง</span><span class="sxs-lookup"><span data-stu-id="52d37-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="52d37-195">นี่เป็นวิธีแก้ปัญหาชั่วคราวเท่านั้น เพราะโดเมน apex ต้องชี้ไปที่ที่อยู่ IP เสมอ</span><span class="sxs-lookup"><span data-stu-id="52d37-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="52d37-196">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="52d37-196">Additional resources</span></span>

  [<span data-ttu-id="52d37-197">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="52d37-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="52d37-198">ตั้งค่าช่องทางร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="52d37-198">Set up an online store channel</span></span>](./channel-setup-online.md)

  [<span data-ttu-id="52d37-199">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="52d37-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="52d37-200">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="52d37-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="52d37-201">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="52d37-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="52d37-202">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="52d37-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="52d37-203">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="52d37-204">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="52d37-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="52d37-205">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="52d37-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="52d37-206">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="52d37-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="52d37-207">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="52d37-207">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]