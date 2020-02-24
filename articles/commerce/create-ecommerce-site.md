---
title: สร้างไซต์อีคอมเมิร์ซ
description: หัวข้อนี้จะอธิบายถึงขั้นตอนและข้อมูลที่จำเป็นในการสร้างไซต์ e-Commerce ใหม่ในโปรแกรมสร้างไซต์ Dynamics 365 Commerce
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002024"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="8af69-103">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8af69-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8af69-104">หัวข้อนี้จะอธิบายถึงขั้นตอนและข้อมูลที่จำเป็นในการสร้างไซต์ e-Commerce ใหม่ในโปรแกรมสร้างไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8af69-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="8af69-105">ก่อนที่คุณจะสามารถเริ่มต้นการพัฒนาไซต์ e-Commerce ของคุณ คุณจะต้องสร้างไซต์ใหม่ในโปรแกรมสร้างไซต์ก่อน</span><span class="sxs-lookup"><span data-stu-id="8af69-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="8af69-106">เมื่อต้องการเริ่มต้นการพัฒนาไซต์อีคอมเมิร์ซของคุณ คุณจะต้องสร้างไซต์ใหม่ในสภาพแวดล้อมการสร้างไซต์ใหม่ก่อน</span><span class="sxs-lookup"><span data-stu-id="8af69-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="8af69-107">ก่อนที่คุณจะสามารถสร้างไซต์ใหม่ได้ ต้องสร้างร้านค้าออนไลน์ใน Commerce อย่างน้อยหนึ่งร้าน</span><span class="sxs-lookup"><span data-stu-id="8af69-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="8af69-108">ตั้งค่าไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8af69-108">Set up your site</span></span>

<span data-ttu-id="8af69-109">ในการตั้งค่าไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8af69-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="8af69-110">เปิดสภาพแวดล้อมของโปรแกรมสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="8af69-110">Open the site builder environment.</span></span> <span data-ttu-id="8af69-111">คุณสามารถค้นหาลิงค์ไปยังโปรแกรมสร้างไซต์ใน Microsoft Lifecycle Services (LCS) ในหน้าคุณลักษณะของสภาพแวดล้อมสำหรับ Commerce</span><span class="sxs-lookup"><span data-stu-id="8af69-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="8af69-112">บนโฮมเพจสำหรับสภาพแวดล้อมการสร้างไซต์ ให้เลือก **ไซต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8af69-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="8af69-113">ในกล่องโต้ตอบ **ไซต์ใหม่** ให้ป้อนข้อมูลดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8af69-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="8af69-114">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="8af69-114">Field</span></span>                               | <span data-ttu-id="8af69-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8af69-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="8af69-116">ชื่อไซต์</span><span class="sxs-lookup"><span data-stu-id="8af69-116">Site name</span></span>                           | <span data-ttu-id="8af69-117">ป้อนชื่อที่ใช้แสดงที่ควรใช้สำหรับไซต์ของคุณในสภาพแวดล้อมการสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="8af69-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="8af69-118">ชื่อนี้จะมองเห็นได้เฉพาะในสภาพแวดล้อมการสร้างไซต์เท่านั้นและจะไม่แสดงให้ลูกค้าเห็น</span><span class="sxs-lookup"><span data-stu-id="8af69-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="8af69-119">กลุ่มรักษาความปลอดภัยของผู้ดูแลไซต์</span><span class="sxs-lookup"><span data-stu-id="8af69-119">Site administrator's security group</span></span> | <span data-ttu-id="8af69-120">ระบุกลุ่มรักษาความปลอดภัย Microsoft Azure Active Directory (Azure AD) ที่จัดการผู้ใช้ที่มีบทบาทผู้ดูแลไซต์ในไซต์นี้</span><span class="sxs-lookup"><span data-stu-id="8af69-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="8af69-121">ช่องทางเริ่มต้น (หมายเลขหน่วยปฏิบัติงาน)</span><span class="sxs-lookup"><span data-stu-id="8af69-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="8af69-122">เลือกร้านค้าออนไลน์ที่ไซต์นี้จะทำหน้าที่เป็นเว็บหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="8af69-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="8af69-123">ถ้าคุณต้องการให้ไซต์อีคอมเมิร์ซของคุณสนับสนุนร้านค้าออนไลน์หลายร้าน คุณต้องเชื่อมโยงร้านค้ากับไซต์ของคุณใน **การตั้งค่าไซต์** หลังจากที่ตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="8af69-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="8af69-124">ภาษาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8af69-124">Default language</span></span>                            | <span data-ttu-id="8af69-125">ระบุภาษาเริ่มต้นสำหรับร้านค้าออนไลน์และตลาดนี้</span><span class="sxs-lookup"><span data-stu-id="8af69-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="8af69-126">ร้านค้าออนไลน์สามารถรองรับได้หลายภาษา</span><span class="sxs-lookup"><span data-stu-id="8af69-126">An online store can support multiple languages.</span></span> <span data-ttu-id="8af69-127">ถ้าคุณต้องการสนับสนุนหลายภาษาสำหรับร้านค้าออนไลน์นี้หรือร้านค้าออนไลน์อื่นคุณสามารถตั้งค่าคอนฟิกการสนับสนุนใน **การตั้งค่าไซต์** หลังจากที่มีการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="8af69-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="8af69-128">โดเมน</span><span class="sxs-lookup"><span data-stu-id="8af69-128">Domain</span></span>                              | <span data-ttu-id="8af69-129">เลือกชื่อโดเมนจะทำหน้าที่เป็นโดเมนสำหรับร้านค้าออนไลน์นี้</span><span class="sxs-lookup"><span data-stu-id="8af69-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="8af69-130">ถ้าคุณไม่ได้ตั้งค่าคอนฟิกโดเมนใดๆ ใน LCS คุณสามารถปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="8af69-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="8af69-131">หลังจากที่ตั้งค่าคอนฟิกโดเมนของคุณใน LCS แล้ว คุณต้องเพิ่มลงในร้านค้าออนไลน์ของคุณใน **การตั้งค่าไซต์**</span><span class="sxs-lookup"><span data-stu-id="8af69-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="8af69-132">พาธ</span><span class="sxs-lookup"><span data-stu-id="8af69-132">Path</span></span>                              | <span data-ttu-id="8af69-133">เมื่อไซต์ของคุณสนับสนุนภาษามากกว่าหนึ่งภาษาสำหรับชื่อโดเมนที่ระบุให้ ใช้ฟิลด์พาธเพื่อสร้าง URL ของไซต์ที่ไม่ซ้ำกันสำหรับชุดข้อมูลโดเมนและภาษานั้นๆ</span><span class="sxs-lookup"><span data-stu-id="8af69-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="8af69-134">ถ้าภาษาที่คุณระบุไว้ในฟิลด์ **ภาษาเริ่มต้น** เป็นภาษาเดียวที่คุณจะสนับสนุนสำหรับโดเมนนี้ หรือจะยังคงเป็นภาษาเริ่มต้นต่อไปหลังจากที่คุณได้ตั้งภาษาท้องถิ่นของคุณให้เป็นภาษาเพิ่มเติมแล้ว เราขอแนะนำให้คุณปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="8af69-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="8af69-135">หลังจากที่สร้างไซต์แล้ว คุณสามารถตรวจสอบว่ามีการเชื่อมโยงกับร้านค้าออนไลน์ของคุณ โดยเลือกแท็บ **ผลิตภัณฑ์** คุณควรเห็นการจัดประเภทของผลิตภัณฑ์ที่ถูกปันส่วนให้กับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="8af69-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="8af69-136">นอกจากนี้คุณยังสามารถใช้ฟิลด์เมนูแบบหล่นลงที่ด้านบนซ้ายของหน้า เพื่อเข้าถึงผลิตภัณฑ์ที่จัดสรรตามประเภท</span><span class="sxs-lookup"><span data-stu-id="8af69-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8af69-137">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8af69-137">Additional resources</span></span>

[<span data-ttu-id="8af69-138">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="8af69-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8af69-139">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="8af69-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8af69-140">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8af69-140">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8af69-141">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="8af69-141">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8af69-142">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8af69-142">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8af69-143">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="8af69-143">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8af69-144">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8af69-144">Enable location-based store detection</span></span>](enable-store-detection.md)
