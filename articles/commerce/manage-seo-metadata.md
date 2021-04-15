---
title: จัดการข้อมูลเมตา SEO
description: หัวข้อนี้จะอธิบายถึงวิธีการจัดการข้อมูลเมตาของโปรแกรมค้นหาการเพิ่มประสิทธิภาพ (SEO) ใน Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794222"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="ad5f7-103">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="ad5f7-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad5f7-104">หัวข้อนี้จะอธิบายถึงวิธีการจัดการข้อมูลเมตาของโปรแกรมค้นหาการเพิ่มประสิทธิภาพ (SEO) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ad5f7-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ad5f7-105">ข้อมูลเมตาของ SEO สำหรับไซต์สามารถถูกจัดการโดยใช้แผนผังไซต์และข้อมูลเมตาของหน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="ad5f7-106">แผนผังไซต์</span><span class="sxs-lookup"><span data-stu-id="ad5f7-106">Site maps</span></span>

<span data-ttu-id="ad5f7-107">แผนผังไซต์เป็นรายการที่สามารถอ่านได้โดยเครื่องในรูปแบบ XML ของหน้าบนเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ad5f7-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="ad5f7-108">ซึ่งมีวัตถุประสงค์ที่จะใช้โดยโปรแกรมค้นหาเพื่อให้ผลการค้นหาที่ดีขึ้นจากไซต์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="ad5f7-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="ad5f7-109">แผนผังไซต์สามารถถูกรับด้วยตนเองโดยใช้เครื่องมือค้นหาหรือเผยแพร่ในไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="ad5f7-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="ad5f7-110">Dynamics 365 Commerce สนับสนุนการสร้างแผนผังไซต์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ad5f7-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="ad5f7-111">แผนผังไซต์จะถูกอัพเดตโดยอัตโนมัติเมื่อเผยแพร่และเลิกเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="ad5f7-112">เปิดการสร้างแผนผังไซต์</span><span class="sxs-lookup"><span data-stu-id="ad5f7-112">Turn on site map generation</span></span>

1. <span data-ttu-id="ad5f7-113">ลงชื่อเข้าใช้เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="ad5f7-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="ad5f7-114">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="ad5f7-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ad5f7-115">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **การจัดการไซต์**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="ad5f7-116">ตรวจสอบให้แน่ใจว่าตัวเลือก **เปิดใช้งานแผนผังไซต์** ถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="ad5f7-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="ad5f7-117">Page metadata</span><span class="sxs-lookup"><span data-stu-id="ad5f7-117">Page metadata</span></span>

<span data-ttu-id="ad5f7-118">Dynamics 365 Commerce อนุญาตให้คุณจัดการข้อมูลเมตา SEO สำหรับแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="ad5f7-119">คุณสามารถดูและปรับเปลี่ยนข้อมูลนี้ได้ในส่วน **คุณสมบัติ SEO** ของคอนเทนเนอร์เพจ</span><span class="sxs-lookup"><span data-stu-id="ad5f7-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="ad5f7-120">คุณสมบัติข้อมูลเมตา SEO ต่อไปนี้ได้รับการสนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="ad5f7-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="ad5f7-121">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="ad5f7-121">Title</span></span>
- <span data-ttu-id="ad5f7-122">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ad5f7-122">Description</span></span>
- <span data-ttu-id="ad5f7-123">คำสำคัญ SEO</span><span class="sxs-lookup"><span data-stu-id="ad5f7-123">SEO keywords</span></span>
- <span data-ttu-id="ad5f7-124">ป้ายชื่อ ARIA</span><span class="sxs-lookup"><span data-stu-id="ad5f7-124">Aria labels</span></span>
- <span data-ttu-id="ad5f7-125">noindex</span><span class="sxs-lookup"><span data-stu-id="ad5f7-125">noindex</span></span>
- <span data-ttu-id="ad5f7-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="ad5f7-126">nofollow</span></span>
- <span data-ttu-id="ad5f7-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="ad5f7-127">noarchive</span></span>
- <span data-ttu-id="ad5f7-128">nocache</span><span class="sxs-lookup"><span data-stu-id="ad5f7-128">nocache</span></span>
- <span data-ttu-id="ad5f7-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="ad5f7-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="ad5f7-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="ad5f7-130">nosnippet</span></span>
- <span data-ttu-id="ad5f7-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="ad5f7-131">noImageIndex</span></span>
- <span data-ttu-id="ad5f7-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="ad5f7-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="ad5f7-133">ปรับเปลี่ยนข้อมูลเมตาของหน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-133">Modify page metadata</span></span>

<span data-ttu-id="ad5f7-134">ในการปรับเปลี่ยนข้อมูลเมตาของหน้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ad5f7-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="ad5f7-135">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="ad5f7-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ad5f7-136">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **หน้า**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="ad5f7-137">เลือกหน้าหลักเพื่อเปิดในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="ad5f7-138">บนแถบคำสั่ง ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="ad5f7-139">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ขยาย **เมตาแท็กเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="ad5f7-140">เมื่อต้องการเพิ่มเมตาแท็กใหม่ให้เลือก **เพิ่ม** แล้วป้อนแท็กในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="ad5f7-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="ad5f7-141">ถ้าต้องการลบเมตาแท็กที่มีอยู่ ให้เลือกสัญลักษณ์ถังขยะที่อยู่ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="ad5f7-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="ad5f7-142">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="ad5f7-143">ในฟิลด์ **ข้อคิดเห็น** ป้อน **อัพเดตเมตาแท็ก** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="ad5f7-144">เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="ad5f7-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="ad5f7-145">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="ad5f7-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="ad5f7-146">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad5f7-147">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ad5f7-147">Additional resources</span></span>

[<span data-ttu-id="ad5f7-148">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="ad5f7-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="ad5f7-149">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ad5f7-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ad5f7-150">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="ad5f7-151">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="ad5f7-152">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ad5f7-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="ad5f7-153">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ad5f7-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="ad5f7-154">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="ad5f7-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="ad5f7-155">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL</span><span class="sxs-lookup"><span data-stu-id="ad5f7-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
