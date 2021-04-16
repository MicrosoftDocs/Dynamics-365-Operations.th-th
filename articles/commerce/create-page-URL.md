---
title: สร้าง URL ของหน้า
description: หัวข้อนี้ครอบคลุมแนวคิดและขั้นตอนพื้นฐานสำหรับการสร้าง URL ของหน้าบนไซต์ของคุณ
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795702"
---
# <a name="create-a-page-url"></a><span data-ttu-id="d20ea-103">สร้าง URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="d20ea-103">Create a page URL</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d20ea-104">หัวข้อนี้ครอบคลุมแนวคิดและขั้นตอนพื้นฐานสำหรับการสร้าง URL ของหน้าบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d20ea-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

<span data-ttu-id="d20ea-105">URL แบบเต็มหรือสัมบูรณ์ซึ่งชี้ไปยังหน้าบนไซต์ของคุณจะประกอบด้วยส่วนที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="d20ea-105">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="d20ea-106">ตัวอย่างเช่น URL `https://www.contoso.com/en-us/contactus` มีส่วนต่างๆ ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d20ea-106">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="d20ea-107">`https://www.contoso.com` – โพรโทคอล HTTP และโดเมนของไซต์</span><span class="sxs-lookup"><span data-stu-id="d20ea-107">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="d20ea-108">`/en-us` – พาธภาษาของไซต์</span><span class="sxs-lookup"><span data-stu-id="d20ea-108">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="d20ea-109">`/contactus` – URL แบบสัมพัทธ์สำหรับหน้า **ติดต่อเรา**</span><span class="sxs-lookup"><span data-stu-id="d20ea-109">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="d20ea-110">URL ที่สัมพันธ์กันเรียกอีกอย่างหนึ่งว่า URL *slug*</span><span class="sxs-lookup"><span data-stu-id="d20ea-110">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="d20ea-111">คุณสร้างโดเมนของไซต์และพาธภาษาที่เลือกกำหนดได้เมื่อคุณตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="d20ea-111">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="d20ea-112">คุณสามารถเพิ่มโดเมนและพาธภาษาให้กับไซต์ของคุณผ่านหน้าร้านค้าออนไลน์ในการตั้งค่าของไซต์</span><span class="sxs-lookup"><span data-stu-id="d20ea-112">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="d20ea-113">slug URL สำหรับหน้ามีอยู่เป็นเอนทิตีแบบสแตนด์อโลนในสภาพแวดล้อมการเขียนแก้ของไซต์</span><span class="sxs-lookup"><span data-stu-id="d20ea-113">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="d20ea-114">URL ของหน้ามีสองส่วน ได้แก่ ชื่อที่แสดงถึง slug URL และตัวชี้ไปยังหน้าบนไซต์ของคุณหรือไซต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="d20ea-114">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="d20ea-115">นอกจากนี้คุณยังสามารถตั้งค่าคอนฟิก URL ของหน้าเพื่อทำหน้าที่เป็นตัวเปลี่ยนเส้นทางไปยังหน้าอื่นบนไซต์ของคุณหรือไซต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="d20ea-115">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="d20ea-116">สร้าง URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="d20ea-116">Create a page URL</span></span>

<span data-ttu-id="d20ea-117">การสร้าง Url ของหน้ามีอยู่สองวิธีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="d20ea-117">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="d20ea-118">โดยอัตโนมัติ เมื่อคุณสร้างหน้าขึ้น</span><span class="sxs-lookup"><span data-stu-id="d20ea-118">Automatically, when you create a page</span></span>
- <span data-ttu-id="d20ea-119">ด้วยตนเอง จากหน้า **URLs**</span><span class="sxs-lookup"><span data-stu-id="d20ea-119">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="d20ea-120">สร้าง URL ของหน้าเมื่อคุณสร้างหน้า</span><span class="sxs-lookup"><span data-stu-id="d20ea-120">Create a page URL when you create a page</span></span>

<span data-ttu-id="d20ea-121">ถ้าคุณระบุชื่อในฟิลด์ **URL** เมื่อคุณสร้างหน้าใหม่ URL ของหน้าซึ่งชี้ไปที่หน้านั้นจะถูกสร้างขึ้นโดยอัตโนมัติบนหน้า **URLs**</span><span class="sxs-lookup"><span data-stu-id="d20ea-121">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="d20ea-122">หลังจากที่คุณเผยแพร่ URL และหน้าที่ชี้ไป ผู้ใช้งานไซต์ (ลูกค้าของคุณ) สามารถเข้าถึงหน้าที่สัมพันธ์กับ URL ได้</span><span class="sxs-lookup"><span data-stu-id="d20ea-122">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="d20ea-123">ถ้าคุณเผยแพร่ URL โดยไม่เผยแพร่หน้าที่ชี้ไป ผู้ใช้งานไซต์จะได้รับข้อผิดพลาด 404 เมื่อพยายามเข้าถึงหน้า</span><span class="sxs-lookup"><span data-stu-id="d20ea-123">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="d20ea-124">ถ้าคุณเผยแพร่หน้าโดยไม่เผยแพร่ URL ที่ชี้ไป จะไม่สามารถเข้าถึงหน้าได้โดยใช้ URL</span><span class="sxs-lookup"><span data-stu-id="d20ea-124">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="d20ea-125">สร้าง URL ของหน้าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d20ea-125">Manually create a page URL</span></span>

<span data-ttu-id="d20ea-126">เมื่อคุณสร้างหน้าใหม่คุณไม่จำเป็นต้องระบุ URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="d20ea-126">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="d20ea-127">ถ้าคุณปล่อยฟิลด์ URL ว่างไว้ จะมีการสร้างหน้านี้ในสถานะที่ไม่มีการยกเลิกการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="d20ea-127">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="d20ea-128">ในกรณีนี้ลูกค้าจะไม่สามารถเข้าถึงหน้าได้แม้ว่าจะมีการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d20ea-128">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="d20ea-129">เมื่อต้องการให้หน้าเข้าถึงได้ คุณต้องสร้าง URL และเชื่อมโยงไปยังหน้าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d20ea-129">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="d20ea-130">เมื่อต้องการสร้าง URL ของหน้าสำหรับหน้าด้วยตนเอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d20ea-130">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="d20ea-131">ในหน้า **URLs** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d20ea-131">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="d20ea-132">เลือกหน้าไซต์ที่จะเชื่อมโยงกับ URL</span><span class="sxs-lookup"><span data-stu-id="d20ea-132">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="d20ea-133">ป้อนชื่อ URL slug และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d20ea-133">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="d20ea-134">ณ จุดนี้ URL จะอยู่ในสถานะร่าง</span><span class="sxs-lookup"><span data-stu-id="d20ea-134">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="d20ea-135">ต้องเผยแพร่ก่อนที่ผู้ใช้ไซต์จะสามารถเข้าถึงหน้าที่เชื่อมโยงได้</span><span class="sxs-lookup"><span data-stu-id="d20ea-135">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="d20ea-136">อัพเดต URL ของหน้า</span><span class="sxs-lookup"><span data-stu-id="d20ea-136">Update a page URL</span></span>

<span data-ttu-id="d20ea-137">เมื่อต้องการอัพเดตหน้าเป้าหมายของ URL ของหน้า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d20ea-137">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="d20ea-138">บนหน้า **URLs** ให้เลือก URL ที่จะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="d20ea-138">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="d20ea-139">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกปุ่มจุดไข่ปลา (**...**) ที่อยู่ถัดจากฟิลด์หน้าเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="d20ea-139">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="d20ea-140">ในกล่องโต้ตอบ เลือกหน้าอื่นๆ จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d20ea-140">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="d20ea-141">บันทึกและเผยแพร่ URL</span><span class="sxs-lookup"><span data-stu-id="d20ea-141">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="d20ea-142">เปลี่ยนเส้นทางหน้า URL</span><span class="sxs-lookup"><span data-stu-id="d20ea-142">Redirect a page URL</span></span>

<span data-ttu-id="d20ea-143">บางครั้งคุณอาจต้องการให้ลูกค้าดูหน้าที่แตกต่างกันเมื่อพวกเขาร้องขอ URL ที่ระบุเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d20ea-143">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="d20ea-144">ในกรณีเหล่านี้ วิธีการที่ดีที่สุดและง่ายที่สุดบ่อยครั้งคือการเปลี่ยนหน้าที่ URL ของหน้าชี้ไป</span><span class="sxs-lookup"><span data-stu-id="d20ea-144">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="d20ea-145">อย่างไรก็ตามคุณอาจมีเหตุผลที่ถูกต้องตามกฎหมายสำหรับการใช้ HTTP 301 หรือ 3023 เปลี่ยนเส้นทางไปยังการร้องขอการเปลี่ยนเส้นทาง URL ไปยัง URL อื่น</span><span class="sxs-lookup"><span data-stu-id="d20ea-145">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="d20ea-146">เมื่อต้องการเปลี่ยนเส้นทาง URL ไปยัง URL อื่นให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d20ea-146">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="d20ea-147">บนหน้า **URLs** ให้เลือก URL ที่จะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="d20ea-147">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="d20ea-148">จากนั้น ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **เปลี่ยนเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="d20ea-148">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="d20ea-149">เลือกปลายทางสำหรับการเปลี่ยนเส้นทางของคุณ</span><span class="sxs-lookup"><span data-stu-id="d20ea-149">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="d20ea-150">ถ้าต้องการชี้ไปยังหน้าอื่นบนไซต์ของคุณ ให้เลือก **URL ภายใน** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก URL ที่จะเปลี่ยนเส้นทางไป</span><span class="sxs-lookup"><span data-stu-id="d20ea-150">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="d20ea-151">ถ้าต้องการชี้ไปยังหน้าบนไซต์ภายนอก ให้เลือก **URL ภายนอก** แล้วป้อน URL สมบูรณ์สำหรับหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="d20ea-151">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="d20ea-152">ตรวจสอบให้แน่ใจว่าได้รวมโพรโทคอลแล้ว</span><span class="sxs-lookup"><span data-stu-id="d20ea-152">Be sure to include the protocol.</span></span> <span data-ttu-id="d20ea-153">ตัวอย่างเช่น ป้อน `https://domain.com/new/page`</span><span class="sxs-lookup"><span data-stu-id="d20ea-153">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="d20ea-154">ถ้า URL เปลี่ยนเส้นทางไปยัง URL ภายในเรียบร้อยแล้ว คุณต้องเลือก **ล้างการเลือก** ก่อนที่คุณจะสามารถป้อน url ภายนอก</span><span class="sxs-lookup"><span data-stu-id="d20ea-154">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="d20ea-155">เลือกชนิดของการเปลี่ยนเส้นทาง:</span><span class="sxs-lookup"><span data-stu-id="d20ea-155">Select a redirect type:</span></span>

    - <span data-ttu-id="d20ea-156">**เปลี่ยนเส้นทางถาวร(301)** – เลือกตัวเลือกนี้เมื่อคุณทราบว่าเนื้อหาของคุณกำลังเคลื่อนที่อย่างถาวรและไม่ได้แปลงกลับเป็น URL ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d20ea-156">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="d20ea-157">โปรแกรมค้นหาจะกำหนดค่าการเพิ่มประสิทธิภาพของโปรแกรมค้นหา (SEO) ของการเปลี่ยนเส้นทาง URL ไปยัง URL ที่กำลังถูกเปลี่ยนเส้นทางและอัพเดตเรกคอร์ดเพื่อแสดง URL ใหม่</span><span class="sxs-lookup"><span data-stu-id="d20ea-157">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="d20ea-158">**เปลี่ยนเส้นทางชั่วคราว (302)** – เลือกตัวเลือกนี้เพื่อเปลี่ยนเส้นทางการจราจรโดยไม่ต้องอัพเดตรายการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d20ea-158">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="d20ea-159">โดยทั่วไปวิธีการนี้จะใช้เมื่อเนื้อหาจะถูกแปลงกลับเป็น URL ก่อนหน้านี้โดยเร็ว</span><span class="sxs-lookup"><span data-stu-id="d20ea-159">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="d20ea-160">เมื่อคุณพร้อมที่จะดำเนินการเปลี่ยนเส้นทาง ให้บันทึกและเผยแพร่ URL</span><span class="sxs-lookup"><span data-stu-id="d20ea-160">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d20ea-161">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d20ea-161">Additional resources</span></span>

[<span data-ttu-id="d20ea-162">เลือกกำหนดการนำทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="d20ea-162">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="d20ea-163">เพิ่มหน้าไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d20ea-163">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d20ea-164">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="d20ea-164">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="d20ea-165">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d20ea-165">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
