---
title: สร้างไซต์อีคอมเมิร์ซ
description: หัวข้อนี้จะอธิบายถึงภารกิจงานที่เกี่ยวข้องกับการสร้างไซต์อีคอมเมิร์ซใหม่ใน Dynamics 365 Commerce
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945846"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="e8276-103">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e8276-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e8276-104">หัวข้อนี้จะอธิบายถึงภารกิจงานที่เกี่ยวข้องกับการสร้างไซต์อีคอมเมิร์ซใหม่ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e8276-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e8276-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e8276-105">Overview</span></span>

<span data-ttu-id="e8276-106">เมื่อต้องการเริ่มต้นการพัฒนาไซต์อีคอมเมิร์ซของคุณ คุณจะต้องสร้างไซต์ใหม่ในสภาพแวดล้อมการสร้างไซต์ใหม่ก่อน</span><span class="sxs-lookup"><span data-stu-id="e8276-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="e8276-107">ก่อนที่คุณจะสามารถสร้างไซต์ใหม่ได้ ต้องสร้างร้านค้าออนไลน์ Dynamics 365 Retail อย่างน้อยหนึ่งร้าน</span><span class="sxs-lookup"><span data-stu-id="e8276-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="e8276-108">ตั้งค่าไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e8276-108">Set up your site</span></span>

<span data-ttu-id="e8276-109">ในการตั้งค่าไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e8276-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="e8276-110">ใน Microsoft Lifecycle Services (LCS) ให้เลือกลิงก์สำหรับสภาพแวดล้อมการสร้างของไซต์</span><span class="sxs-lookup"><span data-stu-id="e8276-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="e8276-111">บนโฮมเพจสำหรับสภาพแวดล้อมการสร้างไซต์ ให้เลือก **ไซต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e8276-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="e8276-112">ในกล่องโต้ตอบ **ไซต์ใหม่** ให้ป้อนข้อมูลดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e8276-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="e8276-113">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="e8276-113">Field</span></span>                               | <span data-ttu-id="e8276-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e8276-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="e8276-115">ชื่อไซต์</span><span class="sxs-lookup"><span data-stu-id="e8276-115">Site name</span></span>                           | <span data-ttu-id="e8276-116">ป้อนชื่อที่ใช้แสดงที่ควรใช้สำหรับไซต์ของคุณในสภาพแวดล้อมการสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="e8276-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="e8276-117">ชื่อนี้จะมองเห็นได้เฉพาะในสภาพแวดล้อมการสร้างไซต์เท่านั้นและจะไม่แสดงให้ลูกค้าเห็น</span><span class="sxs-lookup"><span data-stu-id="e8276-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="e8276-118">กลุ่มรักษาความปลอดภัยของผู้ดูแลไซต์</span><span class="sxs-lookup"><span data-stu-id="e8276-118">Site administrator's security group</span></span> | <span data-ttu-id="e8276-119">ระบุกลุ่มรักษาความปลอดภัย Microsoft Azure Active Directory (Azure AD) ที่จัดการผู้ใช้ที่มีบทบาทผู้ดูแลไซต์ในไซต์นี้</span><span class="sxs-lookup"><span data-stu-id="e8276-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="e8276-120">ช่องทางเริ่มต้น (หมายเลขหน่วยปฏิบัติงาน)</span><span class="sxs-lookup"><span data-stu-id="e8276-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="e8276-121">เลือกร้านค้าออนไลน์ที่ไซต์นี้จะทำหน้าที่เป็นเว็บหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="e8276-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="e8276-122">ถ้าคุณต้องการให้ไซต์อีคอมเมิร์ซของคุณสนับสนุนร้านค้าออนไลน์หลายร้าน คุณต้องเชื่อมโยงร้านค้ากับไซต์ของคุณใน **การตั้งค่าไซต์** หลังจากที่ตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="e8276-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="e8276-123">ภาษาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e8276-123">Default language</span></span>                            | <span data-ttu-id="e8276-124">ระบุภาษาเริ่มต้นสำหรับร้านค้าออนไลน์และตลาดนี้</span><span class="sxs-lookup"><span data-stu-id="e8276-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="e8276-125">ร้านค้าออนไลน์สามารถรองรับได้หลายภาษา</span><span class="sxs-lookup"><span data-stu-id="e8276-125">An online store can support multiple languages.</span></span> <span data-ttu-id="e8276-126">ถ้าคุณต้องการสนับสนุนหลายภาษาสำหรับร้านค้าออนไลน์นี้หรือร้านค้าออนไลน์อื่นคุณสามารถตั้งค่าคอนฟิกการสนับสนุนใน **การตั้งค่าไซต์** หลังจากที่มีการตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="e8276-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="e8276-127">โดเมน</span><span class="sxs-lookup"><span data-stu-id="e8276-127">Domain</span></span>                              | <span data-ttu-id="e8276-128">เลือกชื่อโดเมนจะทำหน้าที่เป็นโดเมนสำหรับร้านค้าออนไลน์นี้</span><span class="sxs-lookup"><span data-stu-id="e8276-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="e8276-129">ถ้าคุณไม่ได้ตั้งค่าคอนฟิกโดเมนใดๆ ใน LCS คุณสามารถปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="e8276-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="e8276-130">หลังจากที่ตั้งค่าคอนฟิกโดเมนของคุณใน LCS แล้ว คุณต้องเพิ่มลงในร้านค้าออนไลน์ของคุณใน **การตั้งค่าไซต์**</span><span class="sxs-lookup"><span data-stu-id="e8276-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="e8276-131">พาธ</span><span class="sxs-lookup"><span data-stu-id="e8276-131">Path</span></span>                              | <span data-ttu-id="e8276-132">เมื่อไซต์ของคุณสนับสนุนภาษามากกว่าหนึ่งภาษาสำหรับชื่อโดเมนที่ระบุให้ ใช้ฟิลด์พาธเพื่อสร้าง URL ของไซต์ที่ไม่ซ้ำกันสำหรับชุดข้อมูลโดเมนและภาษานั้นๆ</span><span class="sxs-lookup"><span data-stu-id="e8276-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="e8276-133">ถ้าภาษาที่คุณระบุไว้ในฟิลด์ **ภาษาเริ่มต้น** เป็นภาษาเดียวที่คุณจะสนับสนุนสำหรับโดเมนนี้ หรือจะยังคงเป็นภาษาเริ่มต้นต่อไปหลังจากที่คุณได้ตั้งภาษาท้องถิ่นของคุณให้เป็นภาษาเพิ่มเติมแล้ว เราขอแนะนำให้คุณปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="e8276-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="e8276-134">หลังจากที่สร้างไซต์แล้ว คุณสามารถตรวจสอบว่ามีการเชื่อมโยงกับร้านค้าออนไลน์ของคุณ โดยเลือกแท็บ **ผลิตภัณฑ์** คุณควรเห็นการจัดประเภทของผลิตภัณฑ์ที่ถูกปันส่วนให้กับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="e8276-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="e8276-135">นอกจากนี้คุณยังสามารถใช้ฟิลด์เมนูแบบหล่นลงที่ด้านบนซ้ายของหน้า เพื่อเข้าถึงผลิตภัณฑ์ที่จัดสรรตามประเภท</span><span class="sxs-lookup"><span data-stu-id="e8276-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8276-136">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e8276-136">Additional resources</span></span>

[<span data-ttu-id="e8276-137">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="e8276-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e8276-138">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="e8276-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e8276-139">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="e8276-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e8276-140">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="e8276-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e8276-141">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="e8276-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e8276-142">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="e8276-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e8276-143">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="e8276-143">Enable location-based store detection</span></span>](enable-store-detection.md)
