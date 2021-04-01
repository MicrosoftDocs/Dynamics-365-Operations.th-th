---
title: ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์
description: หัวข้อนี้จะครอบคลุมการตกแต่งของหน้าประเภทใน Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fbcf6ec60723b726e022b4e17bbde4c903e5cb57
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238799"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="e7c73-103">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e7c73-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e7c73-104">หัวข้อนี้จะครอบคลุมการตกแต่งของหน้าประเภทใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e7c73-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7c73-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e7c73-105">Overview</span></span>

<span data-ttu-id="e7c73-106">Commerce จะให้หน้าเริ่มต้นที่จะใช้เมื่อมีการแสดงข้อมูลของประเภท</span><span class="sxs-lookup"><span data-stu-id="e7c73-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="e7c73-107">หน้าประเภทเริ่มต้น มีองค์ประกอบที่ต้องการเช่น ตัวปรับปรุง การจัดประเภทการวางสินค้า ตัวเลือกการเรียงลำดับข้อมูล สรุปทางเลือก และการควบคุมการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="e7c73-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="e7c73-108">อย่างไรก็ตาม แทนที่จะใช้หน้าประเภทแบบเริ่มต้นคุณอาจต้องการใช้หน้าเริ่มต้นที่ "สมบูรณ์" ของประเภท ซึ่งมีเนื้อหาเพิ่มเติมและองค์ประกอบเฉพาะมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="e7c73-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="e7c73-109">การตกแต่งโดยทั่วไปอาจเกี่ยวข้องกับการเพิ่มเนื้อหาการตลาดเฉพาะประเภทเข้าในหน้าประเภท</span><span class="sxs-lookup"><span data-stu-id="e7c73-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="e7c73-110">เนื้อหานี้อาจรวมถึงการจัดวางผลิตภัณฑ์ข้ามประเภท เพื่อวัตถุประสงค์ในการขายสินค้า รายการที่เลือกโดยบรรณาธิการ รูปภาพ วิดีโอ และข้อความอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e7c73-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="e7c73-111">คุณสามารถปรับเปลี่ยนหน้าประเภทเริ่มต้นหรือกำหนดหน้าประเภทอื่นสำหรับประเภทที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="e7c73-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![หน้าเริ่มต้นของประเภทที่สมบูรณ์แล้ว](./media/CategoryLandingPages.png)

<span data-ttu-id="e7c73-113">ในโปรแกรมสร้างไซต์ Commerce หน้า **ผลิตภัณฑ์** จะรวมรายการของประเภทต่างๆ จากช่องทางที่กำหนดให้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="e7c73-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="e7c73-114">ถ้ามีสถานะ **สมบูรณ์** สำหรับหน้าประเภทดังกล่าว หมายความว่าหน้าประเภทนั้นสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="e7c73-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="e7c73-115">มิฉะนั้น จะมีการใช้หน้าประเภทเริ่มต้นและเนื้อหาสำหรับประเภทนั้น</span><span class="sxs-lookup"><span data-stu-id="e7c73-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="e7c73-116">คุณสามารถดูตัวอย่างทั้งหน้าของประเภทที่สมบูรณ์และไม่สมบูรณ์สำหรับประเภท โดยการเลือกชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="e7c73-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="e7c73-117">เมื่อต้องการทำให้หน้าประเภทสมบูรณ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e7c73-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="e7c73-118">บนหน้า **ผลิตภัณฑ์** ให้เลือกชื่อของประเภทที่คุณต้องการทำให้หน้าประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e7c73-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="e7c73-119">หน้าประเภทเริ่มต้นสำหรับประเภทที่เลือก เปิดอยู่ในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="e7c73-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="e7c73-120">เลือก **ทำให้หน้าประเภทสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="e7c73-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="e7c73-121">เลือกแม่แบบสำหรับหน้าประเภทที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e7c73-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="e7c73-122">ถ้าคุณกำลังทำการเปลี่ยนแปลงแค่เล็กน้อย คุณสามารถเลือกหน้าประเภทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e7c73-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="e7c73-123">อีกทางหนึ่งคือคุณสามารถเลือกแม่แบบของหน้าประเภทเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="e7c73-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="e7c73-124">เมื่อคุณเลือกแม่แบบ โปรแกรมแก้ไขหน้าเปิดและจะใช้แม่แบบที่เลือกเพื่อสร้างหน้าประเภทใหม่สำหรับประเภทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e7c73-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="e7c73-125">หน้าถูกเช็คเอาท์ไปยังคุณ และขณะนี้คุณสามารถทำการเปลี่ยนแปลงของคุณได้</span><span class="sxs-lookup"><span data-stu-id="e7c73-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="e7c73-126">โมดูลที่ใช้ข้อมูลจำเพาะของประเภทใช้ข้อมูลจากประเภทที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="e7c73-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="e7c73-127">การตั้งค่าของแม่แบบที่คุณเลือกจะกำหนดว่าคุณสามารถทำการเปลี่ยนแปลงที่คุณสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="e7c73-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7c73-128">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e7c73-128">Additional resources</span></span>

[<span data-ttu-id="e7c73-129">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="e7c73-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e7c73-130">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="e7c73-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e7c73-131">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="e7c73-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e7c73-132">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="e7c73-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e7c73-133">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="e7c73-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e7c73-134">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e7c73-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e7c73-135">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="e7c73-135">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="e7c73-136">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL</span><span class="sxs-lookup"><span data-stu-id="e7c73-136">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]