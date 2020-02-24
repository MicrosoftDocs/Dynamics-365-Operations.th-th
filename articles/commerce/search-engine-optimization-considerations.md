---
title: ข้อควรพิจารณาเกี่ยวกับการเพิ่มประสิทธิภาพโปรแกรมค้นหา (SEO) สำหรับไซต์ของคุณ
description: หัวข้อนี้จะครอบคลุมการเพิ่มประสิทธิภาพของกลไกจัดการค้นหา (SEO) สำหรับไซต์ของคุณจากการพัฒนาไปยังการผลิต
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c7afed8e4620d5fe49ead47eb6c17d97d7492ad
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002824"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="d4598-103">ข้อควรพิจารณาเกี่ยวกับการเพิ่มประสิทธิภาพโปรแกรมค้นหา (SEO) สำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d4598-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d4598-104">หัวข้อนี้จะครอบคลุมการเพิ่มประสิทธิภาพของกลไกจัดการค้นหา (SEO) สำหรับไซต์ของคุณจากการพัฒนาไปยังการผลิต</span><span class="sxs-lookup"><span data-stu-id="d4598-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="d4598-105">ไซต์ที่อยู่ระหว่างการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="d4598-105">A site that is under development</span></span>

<span data-ttu-id="d4598-106">ในขณะที่ไซต์อยู่ระหว่างการพัฒนาหน้าไซต์ทั้งหมดควรมีแท็กเมตา **NOINDEX** และ **NOFOLLOW**  ซึ่งจะทำให้โปรแกรมการค้นหาไม่จัดทำดัชนีและจัดเก็บเวอร์ชันการพัฒนาของไซต์ของคุณในแคช</span><span class="sxs-lookup"><span data-stu-id="d4598-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="d4598-107">เมื่อต้องการทำการตั้งค่าคอนฟิกนี้คุณต้องเพิ่มโมดูลแท็กเมตา เริ่มต้นลงในเท็มเพลตของหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="d4598-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="d4598-108">คุณสมบัติของแท็กเมตา เริ่มต้นจะพร้อมใช้งานในส่วนของคุณสมบัติ SEO ในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="d4598-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="d4598-109">คุณสามารถใช้คุณสมบัติเหล่านี้ในการจัดการแท็กเมตา</span><span class="sxs-lookup"><span data-stu-id="d4598-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="d4598-110">การเปิดใช้งานแบบทดสอบของไซต์</span><span class="sxs-lookup"><span data-stu-id="d4598-110">Soft launch of a site</span></span>

<span data-ttu-id="d4598-111">ในระหว่าง "การเปิดใช้งานแบบทดสอบ" เว็บไซต์จะเปิดโดยจำกัดผู้เข้าชมหรือตลาดก่อนที่การเปิดใช้งานแบบเต็มจะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="d4598-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="d4598-112">ถ้าคุณทำการเปิดใช้งานแบบทดสอบของเว็บไซต์ของคุณ คุณควรพิจารณาการไม่ย้ายเมตาแท็ก **NOINDEX**</span><span class="sxs-lookup"><span data-stu-id="d4598-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="d4598-113">ด้วยวิธีนี้ คุณจะช่วยรับประกันได้ว่าการเปิดใช้งานแบบทดสอบจะยังคงจำกัดกลุ่มเป้าหมายที่จำกัดที่คุณต้องการเข้าถึงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d4598-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="d4598-114">ไซต์ที่อยู่ในการผลิต</span><span class="sxs-lookup"><span data-stu-id="d4598-114">A site that is in production</span></span>

<span data-ttu-id="d4598-115">เมื่อไซต์อยู่ในการผลิต คุณควรตรวจสอบให้แน่ใจว่าได้ติดแท็กหน้าไซต์ทั้งหมดไว้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d4598-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="d4598-116">Microsoft Dynamics 365 Commerce ใช้ข้อมูลที่ป้อนไว้สำหรับหน้าเพื่อแสดงข้อมูล SEO ทั้งหมดในหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="d4598-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="d4598-117">โมดูลต่อไปนี้จะให้ฟังก์ชันนี้: ข้อมูลสรุปของหน้าประเภท ข้อมูลสรุปของหน้ารายการ และข้อมูลสรุปของหน้าผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d4598-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="d4598-118">เมื่อต้องการเพิ่มประสิทธิภาพโปรแกรมค้นหา การแสดงผลโปรแกรมการแสดงผลจะใช้ทั้งข้อมูลจากคุณสมบัติ SEO ที่มีการตั้งค่าคอนฟิกไว้ใน Dynamics 365 Commerce และข้อมูลเฉพาะโมดูล</span><span class="sxs-lookup"><span data-stu-id="d4598-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="d4598-119">สำหรับไซต์ที่อยู่ในการผลิต คุณควรตรวจสอบให้แน่ใจว่าไฟล์ robots.txt ช่วยให้สามารถจัดทำดัชนีของไซต์ทั้งหมดของคุณได้ และมีลิงค์ไปยังเอกสารแผนผังเว็บไซต์ที่เผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="d4598-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="d4598-120">คุณควรเปิดใช้งานฟังก์ชันการสร้างแม็ปของไซต์ที่ **ตั้งค่าไซต์ \> เปิดใช้งานแผนผังไซต์**</span><span class="sxs-lookup"><span data-stu-id="d4598-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="d4598-121">การตั้งค่า SEO หน้าสำหรับการแสดงตัวอย่างภายใน ผู้เข้าชมที่จำกัด และผู้ชมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d4598-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="d4598-122">เนื่องจาก Dynamics 365 Commerce สนับสนุนการแสดงตัวอย่างที่ได้รับรองความถูกต้องของ "สิ่งที่คุณเห็นคือสิ่งที่คุณได้รับ" (WYSIWYG) ซึ่งผู้เขียนสามารถจัดเตรียมเนื้อหาของหน้าของตนเองได้ โดยไม่ต้องกังวลว่าข้อมูลจะสามารถมองเห็นได้โดยผู้เยี่ยมชมไซต์</span><span class="sxs-lookup"><span data-stu-id="d4598-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="d4598-123">ถ้าต้องการเผยแพร่หน้า แต่ต้องมีการจำกัดปริมาณการใช้งาน จะต้องมีแท็กเมตา **NOINDEX** ซึ่งจะทำให้โปรแกรมการค้นหาไม่จัดทำดัชนีหน้า</span><span class="sxs-lookup"><span data-stu-id="d4598-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="d4598-124">เมื่อหน้าพร้อมสำหรับผู้ใช้ทุกคน ข้อมูลเมตาทั้งหมดของ SEO พื้นฐานควรมีอยู่ เพื่อให้ประสิทธิภาพการทำงานของการจัดดัชนีหน้าของโปรแกรมค้นหาสูงสุด</span><span class="sxs-lookup"><span data-stu-id="d4598-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="d4598-125">นอกจากนี้แท็กเมตา **NOLIMIT** ควรถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="d4598-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4598-126">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d4598-126">Additional resources</span></span>

[<span data-ttu-id="d4598-127">จัดการผู้ใช้และบทบาทอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="d4598-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="d4598-128">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="d4598-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="d4598-129">จัดการนโยบายความปลอดภัยของเนื้อหา (CSP)</span><span class="sxs-lookup"><span data-stu-id="d4598-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
