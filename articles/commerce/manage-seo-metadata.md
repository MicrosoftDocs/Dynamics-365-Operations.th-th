---
title: จัดการข้อมูลเมตา SEO
description: หัวข้อนี้จะอธิบายถึงวิธีการจัดการข้อมูลเมตาของโปรแกรมค้นหาการเพิ่มประสิทธิภาพ (SEO) ใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: b69d9d2769023967e2b94fef1b8fcf6b5b3357c5
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698360"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="2238e-103">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="2238e-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2238e-104">หัวข้อนี้จะอธิบายถึงวิธีการจัดการข้อมูลเมตาของโปรแกรมค้นหาการเพิ่มประสิทธิภาพ (SEO) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2238e-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2238e-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="2238e-105">Overview</span></span>

<span data-ttu-id="2238e-106">ข้อมูลเมตาของ SEO สำหรับไซต์สามารถถูกจัดการโดยใช้แผนผังไซต์และข้อมูลเมตาของหน้า</span><span class="sxs-lookup"><span data-stu-id="2238e-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="2238e-107">แผนผังไซต์</span><span class="sxs-lookup"><span data-stu-id="2238e-107">Site maps</span></span>

<span data-ttu-id="2238e-108">แผนผังไซต์เป็นรายการที่สามารถอ่านได้โดยเครื่องในรูปแบบ XML ของหน้าบนเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2238e-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="2238e-109">ซึ่งมีวัตถุประสงค์ที่จะใช้โดยโปรแกรมค้นหาเพื่อให้ผลการค้นหาที่ดีขึ้นจากไซต์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="2238e-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="2238e-110">แผนผังไซต์สามารถถูกรับด้วยตนเองโดยใช้เครื่องมือค้นหาหรือเผยแพร่ในไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="2238e-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="2238e-111">Dynamics 365 Commerce สนับสนุนการสร้างแผนผังไซต์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2238e-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="2238e-112">แผนผังไซต์จะถูกอัพเดตโดยอัตโนมัติเมื่อเผยแพร่และเลิกเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="2238e-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="2238e-113">เปิดการสร้างแผนผังไซต์</span><span class="sxs-lookup"><span data-stu-id="2238e-113">Turn on site map generation</span></span>

1. <span data-ttu-id="2238e-114">ลงชื่อเข้าใช้เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="2238e-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="2238e-115">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="2238e-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2238e-116">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **การจัดการไซต์**</span><span class="sxs-lookup"><span data-stu-id="2238e-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="2238e-117">ตรวจสอบให้แน่ใจว่าตัวเลือก **เปิดใช้งานแผนผังไซต์** ถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="2238e-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="2238e-118">Page metadata</span><span class="sxs-lookup"><span data-stu-id="2238e-118">Page metadata</span></span>

<span data-ttu-id="2238e-119">Dynamics 365 Commerce อนุญาตให้คุณจัดการข้อมูลเมตา SEO สำหรับแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="2238e-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="2238e-120">คุณสามารถดูและปรับเปลี่ยนข้อมูลนี้ได้ในส่วน **คุณสมบัติ SEO** ของคอนเทนเนอร์เพจ</span><span class="sxs-lookup"><span data-stu-id="2238e-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="2238e-121">คุณสมบัติข้อมูลเมตา SEO ต่อไปนี้ได้รับการสนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="2238e-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="2238e-122">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="2238e-122">Title</span></span>
- <span data-ttu-id="2238e-123">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2238e-123">Description</span></span>
- <span data-ttu-id="2238e-124">คำสำคัญ SEO</span><span class="sxs-lookup"><span data-stu-id="2238e-124">SEO keywords</span></span>
- <span data-ttu-id="2238e-125">ป้ายชื่อ ARIA</span><span class="sxs-lookup"><span data-stu-id="2238e-125">Aria labels</span></span>
- <span data-ttu-id="2238e-126">noindex</span><span class="sxs-lookup"><span data-stu-id="2238e-126">noindex</span></span>
- <span data-ttu-id="2238e-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="2238e-127">nofollow</span></span>
- <span data-ttu-id="2238e-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="2238e-128">noarchive</span></span>
- <span data-ttu-id="2238e-129">nocache</span><span class="sxs-lookup"><span data-stu-id="2238e-129">nocache</span></span>
- <span data-ttu-id="2238e-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="2238e-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="2238e-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="2238e-131">nosnippet</span></span>
- <span data-ttu-id="2238e-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="2238e-132">noImageIndex</span></span>
- <span data-ttu-id="2238e-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="2238e-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="2238e-134">ปรับเปลี่ยนข้อมูลเมตาของหน้า</span><span class="sxs-lookup"><span data-stu-id="2238e-134">Modify page metadata</span></span>

<span data-ttu-id="2238e-135">ในการปรับเปลี่ยนข้อมูลเมตาของหน้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2238e-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="2238e-136">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="2238e-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2238e-137">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **หน้า**</span><span class="sxs-lookup"><span data-stu-id="2238e-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="2238e-138">เลือกหน้าหลักเพื่อเปิดในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="2238e-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2238e-139">ในบานหน้าต่างการดำเนินการ เลือก **เช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="2238e-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="2238e-140">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ขยาย **เมตาแท็กเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="2238e-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="2238e-141">เมื่อต้องการเพิ่มเมตาแท็กใหม่ให้เลือก **เพิ่ม** แล้วป้อนแท็กในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2238e-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="2238e-142">ถ้าต้องการลบเมตาแท็กที่มีอยู่ ให้เลือกสัญลักษณ์ถังขยะที่อยู่ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="2238e-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="2238e-143">เลือก **บันทึก** แล้วจากนั้น เลือก **เช็คอิน**</span><span class="sxs-lookup"><span data-stu-id="2238e-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="2238e-144">ในฟิลด์ **ข้อคิดเห็น** ป้อน **อัพเดตเมตาแท็ก** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2238e-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="2238e-145">เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="2238e-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="2238e-146">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="2238e-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="2238e-147">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2238e-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2238e-148">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2238e-148">Additional resources</span></span>

[<span data-ttu-id="2238e-149">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2238e-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="2238e-150">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="2238e-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2238e-151">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="2238e-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2238e-152">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="2238e-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2238e-153">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2238e-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2238e-154">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2238e-154">Enrich a category landing page</span></span>](enrich-category-page.md)

