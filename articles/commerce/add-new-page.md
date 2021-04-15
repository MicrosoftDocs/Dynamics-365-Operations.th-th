---
title: เพิ่มหน้าไซต์ใหม่
description: หัวข้อนี้อธิบายวิธีการเพิ่มหน้าไซต์ใหม่ใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797562"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="8549d-103">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="8549d-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8549d-104">หัวข้อนี้อธิบายวิธีการเพิ่มหน้าไซต์ใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8549d-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8549d-105">หลังจากที่คุณได้สร้างแม่แบบและส่วนสำหรับไซต์ของคุณแล้ว ขั้นตอนต่อไป คือ การเริ่มต้นสร้างเพจ</span><span class="sxs-lookup"><span data-stu-id="8549d-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="8549d-106">เมื่อต้องการเริ่มต้น คุณต้องเลือกแม่แบบ หรือโครงร่าง ชื่อเพจ และ URL ของเพจ</span><span class="sxs-lookup"><span data-stu-id="8549d-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="8549d-107">แม่แบบหรือโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="8549d-107">Template or layout</span></span>

<span data-ttu-id="8549d-108">คุณสามารถใช้แม่แบบหรือโครงร่างสำหรับเพจใหม่ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8549d-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="8549d-109">สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมแม่แบบและโครงร่าง](templates-layouts-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8549d-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="8549d-110">ชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="8549d-110">Page name</span></span>

<span data-ttu-id="8549d-111">ชื่อเพจต้องไม่ซ้ำกันในเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="8549d-111">The page name must be unique to your page.</span></span> <span data-ttu-id="8549d-112">ควรมีคำอธิบาย เพื่อให้คุณสามารถค้นหาได้ง่าย และบุคคลอื่นๆ รู้ว่าเพจจัดทำขึ้นสำหรับอะไร</span><span class="sxs-lookup"><span data-stu-id="8549d-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="8549d-113">เลือกชื่อเพจอย่างระมัดระวัง เนื่องจากจะไม่สามารถเปลี่ยนแปลงได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="8549d-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="8549d-114">URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="8549d-114">Page URL</span></span>

<span data-ttu-id="8549d-115">คุณสามารถเลือกที่จะป้อน URL สำหรับเพจใหม่ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8549d-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="8549d-116">เมื่อคุณสร้างเพจ คุณสามารถป้อนสตริงที่จะใช้ในการสร้าง URL ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8549d-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="8549d-117">สตริงนี้เรียกว่า URL ที่สัมพันธ์กันหรือ URL Slug</span><span class="sxs-lookup"><span data-stu-id="8549d-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="8549d-118">หลังจากนั้นจะมีการสร้าง URL ที่สมบูรณ์ตาม URL Slug และเพจใหม่จะถูกกำหนดให้กับ URL นั้น</span><span class="sxs-lookup"><span data-stu-id="8549d-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="8549d-119">คุณสามารถเปลี่ยน URL slug ได้ในภายหลัง ก่อนที่คุณจะเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="8549d-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="8549d-120">สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้าง URL ของเพจ](create-page-URL.md)</span><span class="sxs-lookup"><span data-stu-id="8549d-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8549d-121">Dynamics 365 Commerce แยก URL และเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="8549d-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="8549d-122">กล่าวอีกอย่างหนึ่ง คือ สามารถสร้างเพจที่ไม่ได้เชื่อมโยงกับ URL ได้ และสามารถสร้าง URL ที่ไม่ได้เชื่อมโยงกับเพจได้</span><span class="sxs-lookup"><span data-stu-id="8549d-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="8549d-123">ดังนั้น จึงสามารถทำการสลับเนื้อหาสำหรับ URL และไม่จำเป็นต้องมีการหยุดทำงาน และการเปลี่ยนเส้นทางง่ายต่อการจัดการ</span><span class="sxs-lookup"><span data-stu-id="8549d-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="8549d-124">เพิ่มเพจใหม่</span><span class="sxs-lookup"><span data-stu-id="8549d-124">Add a new page</span></span>

<span data-ttu-id="8549d-125">เมื่อต้องการเพิ่มเพจของไซต์ใหม่ให้กับไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8549d-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="8549d-126">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="8549d-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8549d-127">เลือก **เพจใหม่**</span><span class="sxs-lookup"><span data-stu-id="8549d-127">Select **New Page**.</span></span>
1. <span data-ttu-id="8549d-128">ในกล่องโต้ตอบ **เพจใหม่** เลือกแม่แบบ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8549d-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="8549d-129">ในฟิลด์ **ชื่อเพจ** ให้ป้อนชื่อเพจ (ตัวอย่างเช่น **เพจใหม่ของฉัน**)</span><span class="sxs-lookup"><span data-stu-id="8549d-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="8549d-130">ในฟิลด์ **URL** ป้อนสตริง (URL slug) เพื่อทำให้ URL สมบูรณ์ (ตัวอย่างเช่น **mynewpage**)</span><span class="sxs-lookup"><span data-stu-id="8549d-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="8549d-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8549d-131">Select **OK**.</span></span> <span data-ttu-id="8549d-132">โปรแกรมแก้ไขเพจปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8549d-132">The page editor appears.</span></span> <span data-ttu-id="8549d-133">โปรดสังเกตว่ามีการเพิ่มส่วนหัวและส่วนท้ายให้กับเพจโดยอัตโนมัติ ตามแม่แบบที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="8549d-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="8549d-134">ในโครงร่างเพจ ให้เลือกช่อง **หลัก** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="8549d-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8549d-135">เลือก **คอนเทนเนอร์** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8549d-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="8549d-136">เลือก **คอนเทนเนอร์แบบลื่นไหล** เลือกปุ่มจุดไข่ปลา (...) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="8549d-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8549d-137">เลือก **บล็อกเนื้อหา** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8549d-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="8549d-138">เลือก **บล็อกเนื้อหา** เลือกปุ่มจุดไข่ปลา (...) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="8549d-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8549d-139">เลือก **สินค้าบล็อกเนื้อหา** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8549d-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="8549d-140">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **ย่อหน้า** แล้วในฟิลด์ ให้ป้อน **ข้อความการทดสอบของฉัน**</span><span class="sxs-lookup"><span data-stu-id="8549d-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="8549d-141">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="8549d-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8549d-142">ในฟิลด์ **ข้อคิดเห็น** ป้อน **เพิ่มหน้าใหม่** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8549d-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="8549d-143">เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="8549d-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="8549d-144">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="8549d-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="8549d-145">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="8549d-145">Select **Publish**.</span></span>
1. <span data-ttu-id="8549d-146">ในพาธการนำทาง (การแสดงเส้นทาง) ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="8549d-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8549d-147">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **URL**</span><span class="sxs-lookup"><span data-stu-id="8549d-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="8549d-148">ค้นหาและเลือก URL ของคุณ (**mynewpage**) ในรายการ</span><span class="sxs-lookup"><span data-stu-id="8549d-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="8549d-149">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="8549d-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8549d-150">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8549d-150">Additional resources</span></span>

[<span data-ttu-id="8549d-151">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="8549d-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="8549d-152">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="8549d-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="8549d-153">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="8549d-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="8549d-154">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="8549d-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="8549d-155">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8549d-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="8549d-156">เพิ่มข้อมูลหน้าเริ่มต้นของประเภท</span><span class="sxs-lookup"><span data-stu-id="8549d-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="8549d-157">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="8549d-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="8549d-158">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL</span><span class="sxs-lookup"><span data-stu-id="8549d-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
