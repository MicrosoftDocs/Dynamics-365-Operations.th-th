---
title: ปรับเปลี่ยนหน้าไซต์ที่มีอยู่
description: หัวข้อนี้จะอธิบายวิธีการปรับเปลี่ยนหน้าไซต์ที่มีอยู่ใน Microsoft Dynamics 365 Commerce
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 47a7d17b97631ba469a9b68f5f6cf492ebccde6f
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097317"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="115c8-103">ปรับเปลี่ยนหน้าไซต์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="115c8-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="115c8-104">หัวข้อนี้จะอธิบายวิธีการปรับเปลี่ยนหน้าไซต์ที่มีอยู่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="115c8-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="115c8-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="115c8-105">Overview</span></span>

<span data-ttu-id="115c8-106">เมื่อคุณต้องปรับเปลี่ยนหน้า ขั้นตอนแรกคือการเปิดขึ้นในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="115c8-107">ไปที่ไซต์ที่มีหน้าของคุณ จากนั้นในรายการของหน้าให้ค้นหาหน้าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="115c8-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="115c8-108">ถ้าคุณไม่พบหน้า คุณสามารถใช้ฟังก์ชันการค้นหาที่สมบูรณ์ของเครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="115c8-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="115c8-109">พิมพ์ชื่อหน้าที่ถูกต้องหรือพิมพ์ตัวอักษรสองสามตัวแรกและเครื่องหมายดอกจัน (\*)</span><span class="sxs-lookup"><span data-stu-id="115c8-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="115c8-110">รายการที่ถูกกรองของหน้าจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="115c8-110">A filtered list of pages appears.</span></span> <span data-ttu-id="115c8-111">คุณสามารถใช้รายการนี้เพื่อค้นหาหน้าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="115c8-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="115c8-112">หลังจากที่คุณพบหน้าที่ถูกต้องแล้ว ให้เลือกชื่อหน้าเพื่อเปิดหน้าในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="115c8-113">ถ้าหน้าของคุณสามารถมองเห็นได้ในตัวตรวจสอบหน้า คุณสามารถเลือก **แก้ไข** และตรวจสอบหน้า ก่อนที่คุณจะเปิดในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="115c8-114">ด้วยวิธีนี้คุณสามารถตรวจสอบหลายหน้าในเวลาเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="115c8-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="115c8-115">หลังจากที่หน้าเปิดอยู่ในโปรแกรมแก้ไขหน้า คุณต้องตรวจสอบให้แน่ใจว่าได้เช็คเอาท์ไปยังคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="115c8-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="115c8-116">แถบคำสั่งในเครื่องมือการสร้างเป็นแบบไดนามิก มีความไวของบริบท และความไวของสถานะ</span><span class="sxs-lookup"><span data-stu-id="115c8-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="115c8-117">ดังนั้น จะแสดงเฉพาะการดำเนินการที่คุณสามารถดำเนินการบนหน้าในขณะนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="115c8-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="115c8-118">ตัวอย่างเช่น ถ้าหน้าไม่ได้เช็คเอาท์ไปยังคุณ จะไม่มีปุ่ม **บันทึก** และ **แก้ไขให้เสร็จสิ้น** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="115c8-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="115c8-119">สถานะของหน้าจะปรากฏขึ้นทางด้านขวาของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="115c8-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="115c8-120">ถ้าหน้ายังไม่ได้เช็คเอาท์ไปยังคุณ ให้เลือก **แก้ไข** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="115c8-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="115c8-121">แถบคำสั่งจะเปลี่ยนไปเพื่อให้สะท้อนถึงสถานะใหม่ของหน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="115c8-122">นอกจากนี้คุณยังได้รับการแจ้งเตือนที่ระบุว่าหน้าถูกเช็คเอาท์ไปยังคุณ</span><span class="sxs-lookup"><span data-stu-id="115c8-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="115c8-123">ขั้นตอนต่อไปคือทำการเปลี่ยนแปลงจริงของคุณ</span><span class="sxs-lookup"><span data-stu-id="115c8-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="115c8-124">บ่อยครั้งคุณจะใช้แผนภูมิเค้าร่างของหน้าทางด้านซ้ายเพื่อค้นหาและเลือกโมดูลที่คุณต้องการเปลี่ยนแปลง แล้วทำการเปลี่ยนแปลงในบานหน้าต่างคุณสมบัติทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="115c8-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="115c8-125">อย่างไรก็ตาม การเปลี่ยนแปลงในบางครั้งอาจเกี่ยวข้องกับการเพิ่มหรือลบแบบจำลองหรือส่วนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="115c8-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="115c8-126">เมื่อต้องการเพิ่มส่วนหรือโมดูล ให้ใช้แผนภูมิเค้าร่างของหน้าเพื่อค้นหาช่องที่คุณต้องการเพิ่มโมดูลหรือส่วนต่างๆ แล้วเลือกปุ่มจุดไข่ปลา (**...**) สำหรับช่องเสียบดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="115c8-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="115c8-127">เมนูจะปรากฏขึ้นซึ่งรวมคำสั่งสำหรับการเพิ่มโมดูลหรือส่วน</span><span class="sxs-lookup"><span data-stu-id="115c8-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="115c8-128">เมื่อต้องการลบโมดูลหรือส่วน ให้ค้นหาและเลือกตัวเลือกในแผนภูมิเค้าร่างของหน้า เลือกปุ่มจุดไข่ปลา แล้วเลือกคำสั่งเพื่อลบโมดูลหรือส่วน</span><span class="sxs-lookup"><span data-stu-id="115c8-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="115c8-129">นอกจากนี้คุณยังสามารถดูและแก้ไขคุณสมบัติสำหรับโมดูลใดๆ ที่สามารถมองเห็นได้ในการแสดงตัวอย่างตัวสร้างหน้าการแสดงผลด้วยภาพโดยการเลือกโดยตรง</span><span class="sxs-lookup"><span data-stu-id="115c8-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="115c8-130">หลังจากที่คุณทำการเปลี่ยนแปลงและการแสดงตัวอย่างผลกระทบของคุณเสร็จแล้ว คุณควรตรวจสอบในหน้าด้วยการเลือก **แก้ไขให้เสร็จสิ้น** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="115c8-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="115c8-131">เมื่อต้องการเผยแพร่การเปลี่ยนแปลงในทันที ให้เลือก **เผยแพร่** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="115c8-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="115c8-132">เวอร์ชันที่มีการเช็คอินล่าสุดของหน้าที่คุณแก้ไขได้รับการเผยแพร่และจะพร้อมใช้งานสำหรับผู้ใช้ภายนอกที่ดูไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="115c8-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="115c8-133">ตัวอย่าง: เปลี่ยนวิดีโอบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="115c8-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="115c8-134">ตัวอย่างต่อไปนี้แสดงวิธีการปรับเปลี่ยนโฮมเพจโดยการเปลี่ยนวิดีโอที่ปรากฏขึ้นในโมดูลของโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="115c8-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="115c8-135">ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="115c8-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="115c8-136">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **หน้า**</span><span class="sxs-lookup"><span data-stu-id="115c8-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="115c8-137">ค้นหาและเลือกหน้าหลัก เพื่อเปิดในโปรแกรมแก้ไขหน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="115c8-138">บนแถบคำสั่ง ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="115c8-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="115c8-139">ในเค้าร่างหน้าให้เลือกช่อง **หลัก**</span><span class="sxs-lookup"><span data-stu-id="115c8-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="115c8-140">ภายใต้ช่อง **หลัก** ให้ขยายโมดูลคอนเทนเนอร์ของเหลวทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="115c8-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="115c8-141">ค้นหาและเลือกโมดูลของโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="115c8-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="115c8-142">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกคุณสมบัติ **วิดีโอ**</span><span class="sxs-lookup"><span data-stu-id="115c8-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="115c8-143">ตัวเลือกสินทรัพย์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="115c8-143">The asset picker appears.</span></span>
1. <span data-ttu-id="115c8-144">ในตัวเลือกสินทรัพย์ ให้เลือกสินทรัพย์วิดีโอที่มีอยู่ หรือเลือก **อัพโหลดสินทรัพย์ใหม่** เพื่ออัพโหลดสินทรัพย์วิดีโอใหม่</span><span class="sxs-lookup"><span data-stu-id="115c8-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="115c8-145">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="115c8-145">Select **OK**.</span></span>
1. <span data-ttu-id="115c8-146">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="115c8-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="115c8-147">ในฟิลด์ **ข้อคิดเห็น** ป้อน **เปลี่ยนวิดีโอ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="115c8-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="115c8-148">เลือก **แสดงตัวอย่าง** เพื่อเเสดงตัวอย่างหน้าที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="115c8-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="115c8-149">เมื่อเสร็จสิ้นแล้ว ให้ปิดแท็บการแสดงตัวอย่า งเพื่อกลับไปที่เครื่องมือการสร้าง</span><span class="sxs-lookup"><span data-stu-id="115c8-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="115c8-150">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="115c8-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="115c8-151">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="115c8-151">Additional resources</span></span>

[<span data-ttu-id="115c8-152">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="115c8-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="115c8-153">เลือกเค้าโครงหน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="115c8-154">จัดการข้อมูลเมตา SEO</span><span class="sxs-lookup"><span data-stu-id="115c8-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="115c8-155">บันทึก แสดงตัวอย่าง และเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="115c8-156">ทำให้หน้าผลิตภัณฑ์สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="115c8-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="115c8-157">ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="115c8-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="115c8-158">ตรวจสอบการเข้าถึงเนื้อหาของหน้า</span><span class="sxs-lookup"><span data-stu-id="115c8-158">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="115c8-159">สร้างหน้าอีคอมเมิร์ซแบบไดนามิกตามพารามิเตอร์บน URL</span><span class="sxs-lookup"><span data-stu-id="115c8-159">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
