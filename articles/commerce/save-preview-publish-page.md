---
title: บันทึก แสดงตัวอย่าง และเผยแพร่หน้า
description: หัวข้อนี้จะอธิบายวิธีการบันทึกแสดงตัวอย่างและเผยแพร่หน้าใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 8c1b82b1b8423c63d442ee581ed0cc8789ee63fd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697899"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="78e5b-103">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="78e5b-104">หัวข้อนี้จะอธิบายวิธีการบันทึกแสดงตัวอย่างและเผยแพร่หน้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="78e5b-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="78e5b-105">บันทึกหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-105">Save a page</span></span>

<span data-ttu-id="78e5b-106">เมื่อต้องการบันทึกหน้า คุณต้องทำการเช็คเอาท์ไปยังตัวคุณเองและเปิดในตัวแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="78e5b-107">คุณควรบันทึกหน้าทันทีหลังจากที่คุณแก้ไขแล้ว เพื่อช่วยรับประกันว่ามีการจัดเก็บการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="78e5b-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="78e5b-108">เมื่อคุณบันทึกหน้า การเปลี่ยนแปลงจะมองเห็นได้เฉพาะกับคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="78e5b-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="78e5b-109">การดำเนินการบันทึกมีไว้สำหรับจัดเก็บการเปลี่ยนแปลงในขณะที่หน้ายังไม่พร้อมที่จะเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="78e5b-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="78e5b-110">เมื่อคุณปรับเปลี่ยนหน้าเสร็จแล้ว เราขอแนะนำให้คุณเช็คอินไว้ เพื่อให้ผู้อื่นสามารถมองเห็นการเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="78e5b-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="78e5b-111">นอกจากนี้ ยังสามารถตรวจสอบความถูกต้องของหน้าดังกล่าวได้ โดยผู้ใช้รายอื่นที่ต้องแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="78e5b-112">แสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-112">Preview a page</span></span>

<span data-ttu-id="78e5b-113">เครื่องมือการสร้างมีลักษณะการทำงานการแสดงตัวอย่างสองชนิด: a "สิ่งที่คุณเห็นคือสิ่งที่คุณได้รับ" (WYSIWYG) แสดงตัวอย่างบานหน้าต่างในตัวแก้ไขหน้า และหน้าต่างแสดงตัวอย่างที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="78e5b-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="78e5b-114">ขณะที่คุณกำลังใช้ตัวแก้ไขหน้า "สิ่งที่คุณเห็นคือสิ่งที่คุณได้รับ" (WYSIWYG) แสดงตัวอย่างที่ปรากฏขึ้นในบานหน้าต่างศูนย์</span><span class="sxs-lookup"><span data-stu-id="78e5b-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="78e5b-115">การแสดงตัวอย่างนี้จะได้รับการอัพเดตโดยอัตโนมัติเมื่อใดก็ตามที่คุณบันทึกหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="78e5b-116">นอกจากนี้คุณยังสามารถอัพเดตด้วยตนเองได้ด้วยการเลือก **รีเฟรช** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="78e5b-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="78e5b-117">การแสดงตัวอย่าง WYSIWYG แสดงหน้าเช่นเดียวกับที่ผู้ใช้ของไซต์จะเห็น แต่ตัวช่วยการสร้างจะแสดงอยู่ด้านบนของหน้านี้</span><span class="sxs-lookup"><span data-stu-id="78e5b-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="78e5b-118">เมื่อคุณปรับเปลี่ยนหน้าเสร็จแล้วคุณอาจต้องการดูตัวอย่างเพื่อดูว่าลูกค้าจะเห็นอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="78e5b-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="78e5b-119">เมื่อต้องการแสดงตัวอย่างหน้า ให้เลือก **แสดงตัวอย่าง** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="78e5b-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="78e5b-120">การแสดงตัวอย่างจะปรากฏในหน้าต่างเบราว์เซอร์แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="78e5b-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="78e5b-121">หน้าในหน้าต่างแสดงตัวอย่างจะแสดงขึ้นเช่นเดียวกับที่ผู้ใช้ของไซต์จะเห็น</span><span class="sxs-lookup"><span data-stu-id="78e5b-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="78e5b-122">คุณสามารถปรับขนาดหน้าต่างเพื่อให้แน่ใจว่ามีการแสดงโมดูลที่ตอบสนองอย่างถูกต้องในพอร์ตมุมมองทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="78e5b-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="78e5b-123">การตรวจสอบความถูกต้องและสิทธิ์ที่ถูกต้องที่ต้องใช้เพื่อดูตัวอย่างเนื้อหาที่ไม่ได้เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="78e5b-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="78e5b-124">ดังนั้น ถ้าคุณแบ่งปัน URL ของตัวอย่างกับบุคคลบุคคลนั้นต้องมีสิทธิ์ที่ถูกต้องในการเข้าถึงเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="78e5b-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="78e5b-125">เผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-125">Publish a page</span></span>

<span data-ttu-id="78e5b-126">เมื่อหน้าของคุณพร้อมแล้ว ขั้นตอนต่อไปคือเผยแพร่เพื่อให้ผู้ใช้ภายนอกสามารถดูเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="78e5b-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="78e5b-127">ก่อนที่คุณจะสามารถเผยแพร่หน้า คุณต้องเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="78e5b-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="78e5b-128">คุณสามารถเผยแพร่และยกเลิกการเผยแพร่ หน้าจากตัวตรวจสอบหน้าหรือตัวแก้ไขหน้าได้</span><span class="sxs-lookup"><span data-stu-id="78e5b-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="78e5b-129">ตัวตรวจสอบหน้าจะแสดงรายการของหน้า และอนุญาตให้มีการดำเนินงานจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="78e5b-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="78e5b-130">ตัวแก้ไขหน้าสามารถใช้ในการเผยแพร่หรือยกเลิกการเผยแพร่ เฉพาะหน้าเดียวที่เปิดอยู่ในนั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="78e5b-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="78e5b-131">เมื่อต้องการเผยแพร่หน้าตั้งแต่หนึ่งหน้าขึ้นไปจากตัวตรวจสอบหน้า ให้เลือกหน้าที่ตรวจสอบให้แน่ใจว่ามีการเช็คอินแล้วจึงเลือก **เผยแพร่** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="78e5b-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="78e5b-132">มีการเผยแพร่หน้า และคุณได้รับการแจ้งเตือนเกี่ยวกับการดำเนินงานในเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="78e5b-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="78e5b-133">เมื่อต้องการเผยแพร่หน้าเดียวจากตัวแก้ไขหน้ากระบวนงานจะเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="78e5b-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="78e5b-134">ในขณะที่หน้าเปิดอยู่ในโปรแกรมแก้ไขหน้า โปรดตรวจสอบให้แน่ใจว่าได้มีการเช็คอินแล้วและเลือก **เผยแพร่** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="78e5b-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="78e5b-135">มีการเผยแพร่หน้า และคุณได้รับการแจ้งเตือนเกี่ยวกับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="78e5b-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="78e5b-136">เมื่อคุณเผยแพร่หน้าจะมีการเผยแพร่เฉพาะเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="78e5b-137">คุณและผู้ใช้คนอื่น ๆ สามารถไปที่หน้าและดูได้เฉพาะหลังจากเชื่อมโยงด้วย URL</span><span class="sxs-lookup"><span data-stu-id="78e5b-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="78e5b-138">ต้องเผยแพร่ URL แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="78e5b-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78e5b-139">ก่อนที่คุณจะสามารถเผยแพร่ หน้า รูปภาพ หรือส่วนต่าง ๆ ที่หน้าอ้างอิงต้องได้รับการเผยแพร่อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="78e5b-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="78e5b-140">บันทึก แสดงตัวอย่าง และเผยแพร่หน้าหลัก</span><span class="sxs-lookup"><span data-stu-id="78e5b-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="78e5b-141">เมื่อต้องการบันทึกแสดงตัวอย่างและเผยแพร่หน้าหลักให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="78e5b-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="78e5b-142">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="78e5b-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="78e5b-143">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **หน้า**</span><span class="sxs-lookup"><span data-stu-id="78e5b-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="78e5b-144">ค้นหาและเลือกหน้าหลัก เพื่อเปิดในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="78e5b-145">เลือก **เช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="78e5b-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="78e5b-146">ปรับเปลี่ยนหน้าตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="78e5b-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="78e5b-147">เลือก **บันทึก** แล้วจากนั้น เลือก **เช็คอิน**</span><span class="sxs-lookup"><span data-stu-id="78e5b-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="78e5b-148">ในฟิลด์ **ข้อคิดเห็น** ให้ป้อนหมายเหตุเกี่ยวกับการเปลี่ยนแปลงที่คุณทำไว้แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="78e5b-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="78e5b-149">เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="78e5b-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="78e5b-150">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="78e5b-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="78e5b-151">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="78e5b-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="78e5b-152">เผยแพร่ URL</span><span class="sxs-lookup"><span data-stu-id="78e5b-152">Publish a URL</span></span>

<span data-ttu-id="78e5b-153">หากต้องการเผยแพร่ URL ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="78e5b-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="78e5b-154">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="78e5b-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="78e5b-155">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **URL**</span><span class="sxs-lookup"><span data-stu-id="78e5b-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="78e5b-156">ค้นหา และเลือก URL เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="78e5b-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="78e5b-157">บนแถบคำสั่ง ให้เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="78e5b-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78e5b-158">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="78e5b-158">Additional resources</span></span>

[<span data-ttu-id="78e5b-159">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="78e5b-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="78e5b-160">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="78e5b-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="78e5b-161">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="78e5b-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="78e5b-162">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="78e5b-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="78e5b-163">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="78e5b-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="78e5b-164">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="78e5b-164">Enrich a category landing page</span></span>](enrich-category-page.md)

