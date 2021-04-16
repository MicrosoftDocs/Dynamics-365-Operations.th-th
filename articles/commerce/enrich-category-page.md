---
title: ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์
description: หัวข้อนี้จะครอบคลุมการตกแต่งของหน้าประเภทใน Dynamics 365 Commerce
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799022"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="a24a6-103">เพิ่มข้อมูลหน้าเริ่มต้นของประเภท</span><span class="sxs-lookup"><span data-stu-id="a24a6-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a24a6-104">หัวข้อนี้จะครอบคลุมการตกแต่งของหน้าประเภทใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a24a6-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a24a6-105">Commerce จะให้หน้าเริ่มต้นที่จะใช้เมื่อมีการแสดงข้อมูลของประเภท</span><span class="sxs-lookup"><span data-stu-id="a24a6-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="a24a6-106">หน้าประเภทเริ่มต้น มีองค์ประกอบที่ต้องการเช่น ตัวปรับปรุง การจัดประเภทการวางสินค้า ตัวเลือกการเรียงลำดับข้อมูล สรุปทางเลือก และการควบคุมการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="a24a6-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="a24a6-107">อย่างไรก็ตาม แทนที่จะใช้หน้าประเภทแบบเริ่มต้นคุณอาจต้องการใช้หน้าเริ่มต้นที่ "สมบูรณ์" ของประเภท ซึ่งมีเนื้อหาเพิ่มเติมและองค์ประกอบเฉพาะมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="a24a6-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="a24a6-108">การตกแต่งโดยทั่วไปอาจเกี่ยวข้องกับการเพิ่มเนื้อหาการตลาดเฉพาะประเภทเข้าในหน้าประเภท</span><span class="sxs-lookup"><span data-stu-id="a24a6-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="a24a6-109">เนื้อหานี้อาจรวมถึงการจัดวางผลิตภัณฑ์ข้ามประเภท เพื่อวัตถุประสงค์ในการขายสินค้า รายการที่เลือกโดยบรรณาธิการ รูปภาพ วิดีโอ และข้อความอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a24a6-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="a24a6-110">คุณสามารถปรับเปลี่ยนหน้าประเภทเริ่มต้นหรือกำหนดหน้าประเภทอื่นสำหรับประเภทที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="a24a6-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![หน้าเริ่มต้นของประเภทที่สมบูรณ์แล้ว](./media/CategoryLandingPages.png)

<span data-ttu-id="a24a6-112">ในโปรแกรมสร้างไซต์ Commerce หน้า **ผลิตภัณฑ์** จะรวมรายการของประเภทต่างๆ จากช่องทางที่กำหนดให้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="a24a6-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="a24a6-113">ถ้ามีสถานะ **สมบูรณ์** สำหรับหน้าประเภทดังกล่าว หมายความว่าหน้าประเภทนั้นสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="a24a6-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="a24a6-114">มิฉะนั้น จะมีการใช้หน้าประเภทเริ่มต้นและเนื้อหาสำหรับประเภทนั้น</span><span class="sxs-lookup"><span data-stu-id="a24a6-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="a24a6-115">คุณสามารถดูตัวอย่างทั้งหน้าของประเภทที่สมบูรณ์และไม่สมบูรณ์สำหรับประเภท โดยการเลือกชื่อประเภท</span><span class="sxs-lookup"><span data-stu-id="a24a6-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="a24a6-116">เมื่อต้องการทำให้หน้าประเภทสมบูรณ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a24a6-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="a24a6-117">บนหน้า **ผลิตภัณฑ์** ให้เลือกชื่อของประเภทที่คุณต้องการทำให้หน้าประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a24a6-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="a24a6-118">หน้าประเภทเริ่มต้นสำหรับประเภทที่เลือก เปิดอยู่ในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="a24a6-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="a24a6-119">เลือก **ทำให้หน้าประเภทสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="a24a6-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="a24a6-120">เลือกแม่แบบสำหรับหน้าประเภทที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a24a6-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="a24a6-121">ถ้าคุณกำลังทำการเปลี่ยนแปลงแค่เล็กน้อย คุณสามารถเลือกหน้าประเภทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a24a6-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="a24a6-122">อีกทางหนึ่งคือคุณสามารถเลือกแม่แบบของหน้าประเภทเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="a24a6-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="a24a6-123">เมื่อคุณเลือกแม่แบบ โปรแกรมแก้ไขหน้าเปิดและจะใช้แม่แบบที่เลือกเพื่อสร้างหน้าประเภทใหม่สำหรับประเภทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a24a6-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="a24a6-124">หน้าถูกเช็คเอาท์ไปยังคุณ และขณะนี้คุณสามารถทำการเปลี่ยนแปลงของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a24a6-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="a24a6-125">โมดูลที่ใช้ข้อมูลจำเพาะของประเภทใช้ข้อมูลจากประเภทที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="a24a6-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="a24a6-126">การตั้งค่าของแม่แบบที่คุณเลือกจะกำหนดว่าคุณสามารถทำการเปลี่ยนแปลงที่คุณสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="a24a6-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a24a6-127">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a24a6-127">Additional resources</span></span>

[<span data-ttu-id="a24a6-128">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a24a6-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="a24a6-129">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="a24a6-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="a24a6-130">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="a24a6-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="a24a6-131">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="a24a6-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="a24a6-132">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="a24a6-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="a24a6-133">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a24a6-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="a24a6-134">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="a24a6-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="a24a6-135">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL</span><span class="sxs-lookup"><span data-stu-id="a24a6-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
