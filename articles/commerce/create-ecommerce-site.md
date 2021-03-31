---
title: สร้างไซต์อีคอมเมิร์ซ
description: หัวข้อนี้จะอธิบายถึงขั้นตอนและข้อมูลที่จำเป็นในการสร้างไซต์อีคอมเมิร์ซใหม่ในโปรแกรมสร้างไซต์ Dynamics 365 Commerce
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 465154ef7209547481c8598d5eaefb434359b1fd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208001"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="f09d1-103">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f09d1-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f09d1-104">หัวข้อนี้จะอธิบายถึงขั้นตอนและข้อมูลที่จำเป็นในการสร้างไซต์อีคอมเมิร์ซใหม่ในโปรแกรมสร้างไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f09d1-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="f09d1-105">เมื่อคุณอนุญาตให้ใช้ความสามารถของ Dynamics 365 Commerce โปรแกรมสร้างไซต์จะถูกเตรียมใช้งานด้วยไซต์เริ่มต้นที่คุณสามารถใช้เป็นข้อมูลพื้นฐานสำหรับไซต์ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="f09d1-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="f09d1-106">อย่างไรก็ตามถ้าคุณต้องการเริ่มตั้งแต่ต้นหรือถ้าคุณต้องการสร้างไซต์ที่สอง คุณจะต้องสร้างไซต์ใหม่ในสภาพแวดล้อมการเขียนแก้ของไซต์</span><span class="sxs-lookup"><span data-stu-id="f09d1-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="f09d1-107">ตั้งค่าไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f09d1-107">Set up your site</span></span>

<span data-ttu-id="f09d1-108">ในการตั้งค่าไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f09d1-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="f09d1-109">เปิดสภาพแวดล้อมของโปรแกรมสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="f09d1-109">Open the site builder environment.</span></span> <span data-ttu-id="f09d1-110">คุณสามารถค้นหาลิงค์ไปยังโปรแกรมสร้างไซต์ใน Microsoft Lifecycle Services (LCS) ในหน้าคุณลักษณะของสภาพแวดล้อมสำหรับ Commerce</span><span class="sxs-lookup"><span data-stu-id="f09d1-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="f09d1-111">บนโฮมเพจสำหรับสภาพแวดล้อมการสร้างไซต์ ให้เลือก **ไซต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f09d1-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="f09d1-112">ในกล่องโต้ตอบ **ไซต์ใหม่** ให้ป้อนข้อมูลดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f09d1-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="f09d1-113">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="f09d1-113">Field</span></span>                               | <span data-ttu-id="f09d1-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f09d1-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="f09d1-115">ชื่อไซต์</span><span class="sxs-lookup"><span data-stu-id="f09d1-115">Site name</span></span>                           | <span data-ttu-id="f09d1-116">ป้อนชื่อที่ใช้แสดงที่ควรใช้สำหรับไซต์ของคุณในสภาพแวดล้อมการสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="f09d1-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="f09d1-117">ชื่อนี้จะมองเห็นได้เฉพาะในสภาพแวดล้อมการสร้างไซต์เท่านั้นและจะไม่แสดงให้ลูกค้าเห็น</span><span class="sxs-lookup"><span data-stu-id="f09d1-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="f09d1-118">กลุ่มรักษาความปลอดภัยของผู้ดูแลไซต์</span><span class="sxs-lookup"><span data-stu-id="f09d1-118">Site administrator's security group</span></span> | <span data-ttu-id="f09d1-119">ระบุกลุ่มรักษาความปลอดภัย Microsoft Azure Active Directory (Azure AD) ที่จัดการผู้ใช้ที่มีบทบาทผู้ดูแลไซต์ในไซต์นี้</span><span class="sxs-lookup"><span data-stu-id="f09d1-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="f09d1-120">ช่องทางเริ่มต้น (หมายเลขหน่วยปฏิบัติงาน)</span><span class="sxs-lookup"><span data-stu-id="f09d1-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="f09d1-121">เลือกร้านค้าออนไลน์ที่ไซต์นี้จะทำหน้าที่เป็นเว็บหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="f09d1-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="f09d1-122">ถ้าคุณต้องการให้ไซต์อีคอมเมิร์ซของคุณสนับสนุนร้านค้าออนไลน์หลายร้าน คุณต้องเชื่อมโยงร้านค้ากับไซต์ของคุณใน **การตั้งค่าไซต์** หลังจากที่ตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="f09d1-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="f09d1-123">ภาษาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f09d1-123">Default language</span></span>                            | <span data-ttu-id="f09d1-124">ระบุภาษาเริ่มต้นสำหรับร้านค้าออนไลน์และตลาดนี้</span><span class="sxs-lookup"><span data-stu-id="f09d1-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="f09d1-125">ร้านค้าออนไลน์สามารถรองรับได้หลายภาษา</span><span class="sxs-lookup"><span data-stu-id="f09d1-125">An online store can support multiple languages.</span></span> <span data-ttu-id="f09d1-126">ถ้าคุณต้องการสนับสนุนหลายภาษาสำหรับร้านค้าออนไลน์นี้หรือร้านค้าออนไลน์อื่นคุณสามารถตั้งค่าคอนฟิกการสนับสนุนใน **การตั้งค่าไซต์** หลังจากที่มีการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="f09d1-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="f09d1-127">โดเมน</span><span class="sxs-lookup"><span data-stu-id="f09d1-127">Domain</span></span>                              | <span data-ttu-id="f09d1-128">เลือกชื่อโดเมนจะทำหน้าที่เป็นโดเมนสำหรับร้านค้าออนไลน์นี้</span><span class="sxs-lookup"><span data-stu-id="f09d1-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="f09d1-129">ถ้าคุณไม่ได้ตั้งค่าคอนฟิกโดเมนใดๆ ใน LCS คุณสามารถปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="f09d1-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="f09d1-130">หลังจากที่ตั้งค่าคอนฟิกโดเมนของคุณใน LCS แล้ว คุณต้องเพิ่มลงในร้านค้าออนไลน์ของคุณใน **การตั้งค่าไซต์**</span><span class="sxs-lookup"><span data-stu-id="f09d1-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="f09d1-131">พาธ</span><span class="sxs-lookup"><span data-stu-id="f09d1-131">Path</span></span>                              | <span data-ttu-id="f09d1-132">เมื่อไซต์ของคุณสนับสนุนภาษามากกว่าหนึ่งภาษาสำหรับชื่อโดเมนที่ระบุให้ ใช้ฟิลด์พาธเพื่อสร้าง URL ของไซต์ที่ไม่ซ้ำกันสำหรับชุดข้อมูลโดเมนและภาษานั้นๆ</span><span class="sxs-lookup"><span data-stu-id="f09d1-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="f09d1-133">ถ้าภาษาที่คุณระบุไว้ในฟิลด์ **ภาษาเริ่มต้น** เป็นภาษาเดียวที่คุณจะสนับสนุนสำหรับโดเมนนี้ หรือจะยังคงเป็นภาษาเริ่มต้นต่อไปหลังจากที่คุณได้ตั้งภาษาท้องถิ่นของคุณให้เป็นภาษาเพิ่มเติมแล้ว เราขอแนะนำให้คุณปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f09d1-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="f09d1-134">หลังจากที่สร้างไซต์แล้ว คุณสามารถตรวจสอบว่ามีการเชื่อมโยงกับร้านค้าออนไลน์ของคุณ โดยเลือกแท็บ **ผลิตภัณฑ์** คุณควรเห็นการจัดประเภทของผลิตภัณฑ์ที่ถูกปันส่วนให้กับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="f09d1-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="f09d1-135">นอกจากนี้คุณยังสามารถใช้ฟิลด์เมนูแบบหล่นลงที่ด้านบนซ้ายของหน้า เพื่อเข้าถึงผลิตภัณฑ์ที่จัดสรรตามประเภท</span><span class="sxs-lookup"><span data-stu-id="f09d1-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f09d1-136">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f09d1-136">Additional resources</span></span>

[<span data-ttu-id="f09d1-137">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="f09d1-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f09d1-138">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="f09d1-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f09d1-139">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="f09d1-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f09d1-140">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="f09d1-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f09d1-141">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="f09d1-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f09d1-142">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="f09d1-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="f09d1-143">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f09d1-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f09d1-144">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="f09d1-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="f09d1-145">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="f09d1-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f09d1-146">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f09d1-146">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]