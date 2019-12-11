---
title: โมดูลคุณลักษณะ
description: หัวข้อนี้ครอบคลุมถึงโมดูลคุณลักษณะ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785317"
---
# <a name="feature-module"></a><span data-ttu-id="3016b-103">โมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="3016b-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3016b-104">หัวข้อนี้ครอบคลุมถึงโมดูลคุณลักษณะ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3016b-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3016b-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="3016b-105">Overview</span></span>

<span data-ttu-id="3016b-106">โมดูลคุณลักษณะใช้ในการทำตลาดผลิตภัณฑ์ หรือโปรโมชันผ่านการรวมกันของรูปภาพและข้อความ</span><span class="sxs-lookup"><span data-stu-id="3016b-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="3016b-107">ตัวอย่างเช่น ผู้ค้าปลีกสามารถเพิ่มโมดูลคุณลักษณะให้กับเพจรายละเอียดผลิตภัณฑ์ เพื่อเน้นคุณลักษณะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3016b-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="3016b-108">โมดูลคุณลักษณะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="3016b-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="3016b-109">โมดูลที่ทำงานแยกต่างหากคือโมดูลที่ไม่ขึ้นอยู่กับบริบทเพจ หรือโมดูลอื่นๆ บนเพจ</span><span class="sxs-lookup"><span data-stu-id="3016b-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="3016b-110">โมดูลคุณลักษณะสามารถวางบนเพจเว็บไซต์ใดๆ ที่ผู้ค้าปลีกต้องการทำตลาด หรือส่งเสริมบางสิ่งบางอย่าง (เช่น ผลิตภัณฑ์ การขาย หรือคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="3016b-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="3016b-111">ตัวอย่างของโมดูลคุณลักษณะในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="3016b-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="3016b-112">โมดูลขคุณลักษณะสามารถใช้ได้ในเพจต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3016b-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="3016b-113">บนเพจรายละเอียดผลิตภัณฑ์ เพื่อแสดงคุณลักษณะผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3016b-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="3016b-114">โฮมเพจ เพื่อส่งเสริมผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3016b-114">The home page, to promote products</span></span>
- <span data-ttu-id="3016b-115">เพจประเภท เพื่อเน้นประเภทของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3016b-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="3016b-116">คุณสมบัติของโมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="3016b-116">Feature module properties</span></span>

| <span data-ttu-id="3016b-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3016b-117">Property name</span></span>     | <span data-ttu-id="3016b-118">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="3016b-118">Values</span></span> | <span data-ttu-id="3016b-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3016b-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="3016b-120">รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="3016b-120">Image</span></span>             | <span data-ttu-id="3016b-121">ไฟล์รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="3016b-121">Image file</span></span> | <span data-ttu-id="3016b-122">สามารถใช้รูปภาพเพื่อทำตลาดผลิตภัณฑ์ หรือโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="3016b-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="3016b-123">สามารถอัพโหลดรูปภาพไปที่แกลเลอรีรูปภาพ หรือสามารถใช้รูปภาพที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="3016b-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="3016b-124">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="3016b-124">Heading</span></span>           | <span data-ttu-id="3016b-125">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="3016b-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="3016b-126">ทุกโมดูลคุณลักษณะสามารถมีหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="3016b-126">Every feature module can have a heading.</span></span> <span data-ttu-id="3016b-127">โดยค่าเริ่มต้น แท็กหัวเรื่อง **H2** จะใช้สำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="3016b-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="3016b-128">อย่างไรก็ตาม คุณสามารถเปลี่ยนแท็กเพื่อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="3016b-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="3016b-129">ย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="3016b-129">Paragraph</span></span>         | <span data-ttu-id="3016b-130">ข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="3016b-130">Paragraph text</span></span> | <span data-ttu-id="3016b-131">โมดูลคุณลักษณะสนับสนุนข้อความย่อหน้าในรูปแบบข้อความที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="3016b-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="3016b-132">ความสามารถในการทำงานของข้อความที่สมบูรณ์แบบพื้นฐานบางอย่างจะได้รับการสนับสนุน เช่น ข้อความตัวเอน ขีดเส้นใต้ และแบบตัวหนา และไฮเปอร์ลิงค์</span><span class="sxs-lookup"><span data-stu-id="3016b-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="3016b-133">ความสามารถบางอย่างเหล่านี้อาจถูกแทนที่ด้วยชุดรูปแบบของเพจที่ใช้กับโมดูล</span><span class="sxs-lookup"><span data-stu-id="3016b-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="3016b-134">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="3016b-134">Link</span></span>              | <span data-ttu-id="3016b-135">ลิงค์ข้อความ ลิงค์ URL ป้ายชื่อ Accessible Rich Internet Applications (ARIA) และ **เปิดลิงค์ในแท็บใหม่**</span><span class="sxs-lookup"><span data-stu-id="3016b-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="3016b-136">โมดูลคุณลักษณะสนับสนุนลิงค์ "การกระตุ้นให้ดำเนินการ" หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="3016b-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="3016b-137">ถ้ามีการเพิ่มลิงค์ ลิงค์ข้อความ URL และป้ายชื่อ ARIA จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3016b-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="3016b-138">ป้ายชื่อ ARIA ควรเป็นคำอธิบายเพื่อให้ตรงตามข้อกำหนดของความสามารถในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="3016b-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="3016b-139">สามารถตั้งค่าคอนฟิกลิงค์ เพื่อให้เปิดบนแท็บใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="3016b-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="3016b-140">การจัดวางรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="3016b-140">Image placement</span></span>   | <span data-ttu-id="3016b-141">**ขวา** **ซ้าย** **ด้านบน** หรือ **ด้านล่าง**</span><span class="sxs-lookup"><span data-stu-id="3016b-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="3016b-142">คุณสมบัตินี้กำหนดตำแหน่งของรูปภาพที่สัมพันธ์กับข้อความ</span><span class="sxs-lookup"><span data-stu-id="3016b-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="3016b-143">ตัวอย่างเช่น ถ้า **ด้านขวา** ถูกเลือก รูปภาพจะปรากฏทางด้านขวาของข้อความ</span><span class="sxs-lookup"><span data-stu-id="3016b-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="3016b-144">ขนาดคอลัมน์รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="3016b-144">Image column size</span></span> | <span data-ttu-id="3016b-145">ค่าตั้งแต่ **1** ถึง **12**</span><span class="sxs-lookup"><span data-stu-id="3016b-145">A value from **1** through **12**</span></span> | <span data-ttu-id="3016b-146">คุณสมบัตินี้กำหนดขนาดของรูปภาพที่สัมพันธ์กับข้อความ</span><span class="sxs-lookup"><span data-stu-id="3016b-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="3016b-147">ขนาดจะแสดงเป็นจำนวนของคอลัมน์บนเพจ</span><span class="sxs-lookup"><span data-stu-id="3016b-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="3016b-148">มี 12 คอลัมน์บนเพจ</span><span class="sxs-lookup"><span data-stu-id="3016b-148">There are 12 columns on a page.</span></span> <span data-ttu-id="3016b-149">โดยค่าเริ่มต้น รูปภาพและข้อความมีขนาดเท่ากัน (หกคอลัมน์สำหรับแต่ละตัว)</span><span class="sxs-lookup"><span data-stu-id="3016b-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="3016b-150">อย่างไรก็ตาม คุณสามารถปรับขนาดได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="3016b-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="3016b-151">เพิ่มโมดูลคุณลักษณะไปยังเพจใหม่</span><span class="sxs-lookup"><span data-stu-id="3016b-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="3016b-152">การเพิ่มโมดูลคุณลักษณะไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3016b-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3016b-153">ไปที่ **แม่แบบ** และสร้างแม่แบบเพจที่ชื่อ **แม่แบบคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="3016b-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="3016b-154">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="3016b-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="3016b-155">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="3016b-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="3016b-156">ใช้แม่แบบคุณลักษณะที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="3016b-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="3016b-157">ในช่อง **หลัก** ของเพจเริ่มต้น เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="3016b-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3016b-158">ในกล่องโต้ตอบ **เพิ่มโมดูล** ใต้ **เลือกโมดูล** เลือกโมดูลคุณลักษณะ จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3016b-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="3016b-159">ในแผนภูมิเค้าร่างทางด้านซ้าย เลือกโมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="3016b-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="3016b-160">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **เพิ่มรูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="3016b-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="3016b-161">เลือกรูปภาพที่มีอยู่ หรืออัพโหลดรูปภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="3016b-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="3016b-162">เลือก **หัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="3016b-162">Select **Heading**.</span></span>
1. <span data-ttu-id="3016b-163">ในกล่องโต้ตอบ **ส่วนหัว** ให้เพิ่มข้อความหัวข้อ เลือกระดับหัวข้อ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3016b-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="3016b-164">ภายใต้ **Rich Text** ให้เพิ่มข้อความตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="3016b-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="3016b-165">เลือก **เพิ่มลิงค์การดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="3016b-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="3016b-166">ในกล่องโต้ตอบ **ลิงค์การดำเนินการ** เพิ่มข้อความลิงค์ URL ลิงค์ และป้ายชื่อ ARIA สำหรับลิงค์ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3016b-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="3016b-167">บันทึกเพจ และแสดงตัวอย่างการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="3016b-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="3016b-168">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="3016b-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3016b-169">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3016b-169">Additional resources</span></span>

[<span data-ttu-id="3016b-170">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3016b-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3016b-171">โมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="3016b-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="3016b-172">โมดูลแบบวงล้อ</span><span class="sxs-lookup"><span data-stu-id="3016b-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="3016b-173">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="3016b-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3016b-174">โมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="3016b-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="3016b-175">โมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="3016b-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="3016b-176">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="3016b-176">Video player module</span></span>](add-video-player.md)
