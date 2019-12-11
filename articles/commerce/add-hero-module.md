---
title: โมดูลฮีโร
description: หัวข้อนี้ครอบคลุมถึงโมดูลฮีโร และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785409"
---
# <a name="hero-module"></a><span data-ttu-id="6a076-103">โมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="6a076-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6a076-104">หัวข้อนี้ครอบคลุมถึงโมดูลฮีโร และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6a076-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a076-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="6a076-105">Overview</span></span>

<span data-ttu-id="6a076-106">โมดูลฮีโรใช้ในการทำตลาดผลิตภัณฑ์ หรือโปรโมชันผ่านการรวมกันของรูปภาพและข้อความ</span><span class="sxs-lookup"><span data-stu-id="6a076-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="6a076-107">ตัวอย่างเช่น ผู้ค้าปลีกสามารถเพิ่มโมดูลฮีโรไปยังโฮมเพจของไซต์อีคอมเมิร์ซเพื่อส่งเสริมผลิตภัณฑ์ใหม่ และดึงดูดความสนใจของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6a076-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="6a076-108">โมดูลของฮีโรถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="6a076-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="6a076-109">โมดูลที่ทำงานแยกต่างหากคือโมดูลที่ไม่ขึ้นอยู่กับบริบทเพจ หรือโมดูลอื่นๆ บนเพจ</span><span class="sxs-lookup"><span data-stu-id="6a076-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="6a076-110">โมดูลฮีโรสามารถวางบนเพจเว็บไซต์ใดๆ ที่ผู้ค้าปลีกต้องการทำตลาด หรือส่งเสริมบางสิ่งบางอย่าง (เช่น ผลิตภัณฑ์ การขาย หรือคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="6a076-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="6a076-111">ตัวอย่างของโมดูลฮีโรในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="6a076-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="6a076-112">คุณสามารถใช้โมดูลฮีโรบนโฮมเพจของไซต์อีคอมเมิร์ซ เพื่อเน้นโปรโมชั่นและผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="6a076-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="6a076-113">โมดูลฮีโรสามารถใช้ในเพจรายละเอียดของผลิตภัณฑ์ เพื่อแสดงข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6a076-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="6a076-114">หลายโมดูลฮีโรสามารถใส่ไว้ภายในโมดูลวงล้อเพื่อเน้นผลิตภัณฑ์ หรือโปรโมชั่นต่างๆ</span><span class="sxs-lookup"><span data-stu-id="6a076-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="6a076-115">คุณสมบัติของโมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="6a076-115">Hero module properties</span></span>

| <span data-ttu-id="6a076-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="6a076-116">Property name</span></span>  | <span data-ttu-id="6a076-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="6a076-117">Values</span></span> | <span data-ttu-id="6a076-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6a076-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="6a076-119">รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="6a076-119">Image</span></span>          | <span data-ttu-id="6a076-120">ไฟล์รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="6a076-120">Image file</span></span> | <span data-ttu-id="6a076-121">สามารถใช้รูปภาพเพื่อแสดงผลิตภัณฑ์ หรือโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="6a076-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="6a076-122">สามารถอัพโหลดรูปภาพไปที่แกลเลอรีรูปภาพ หรือสามารถใช้รูปภาพที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="6a076-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="6a076-123">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="6a076-123">Heading</span></span>        | <span data-ttu-id="6a076-124">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="6a076-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="6a076-125">ทุกโมดูลฮีโรสามารถมีหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="6a076-125">Every hero module can have a heading.</span></span> <span data-ttu-id="6a076-126">โดยค่าเริ่มต้น แท็กหัวเรื่อง **H2** จะใช้สำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="6a076-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="6a076-127">อย่างไรก็ตาม คุณสามารถเปลี่ยนแท็กเพื่อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="6a076-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="6a076-128">ย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="6a076-128">Paragraph</span></span>      | <span data-ttu-id="6a076-129">ข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="6a076-129">Paragraph text</span></span> | <span data-ttu-id="6a076-130">โมดูลฮีโรสนับสนุนข้อความย่อหน้าในรูปแบบข้อความที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="6a076-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="6a076-131">ความสามารถในการทำงานของข้อความที่สมบูรณ์แบบพื้นฐานบางอย่างจะได้รับการสนับสนุน เช่น ข้อความตัวเอน ขีดเส้นใต้ และแบบตัวหนา และไฮเปอร์ลิงค์</span><span class="sxs-lookup"><span data-stu-id="6a076-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="6a076-132">ความสามารถบางอย่างเหล่านี้อาจถูกแทนที่ด้วยชุดรูปแบบของเพจที่ใช้กับโมดูล</span><span class="sxs-lookup"><span data-stu-id="6a076-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="6a076-133">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="6a076-133">Link</span></span>           | <span data-ttu-id="6a076-134">ลิงค์ข้อความ ลิงค์ URL ป้ายชื่อ Accessible Rich Internet Applications (ARIA) และ **เปิดลิงค์ในแท็บใหม่**</span><span class="sxs-lookup"><span data-stu-id="6a076-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="6a076-135">โมดูลฮีโรสนับสนุนลิงค์ "การกระตุ้นให้ดำเนินการ" หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="6a076-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="6a076-136">ถ้ามีการเพิ่มลิงค์ ลิงค์ข้อความ URL และป้ายชื่อ ARIA จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="6a076-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="6a076-137">ป้ายชื่อ ARIA ควรเป็นคำอธิบายเพื่อให้ตรงตามข้อกำหนดของความสามารถในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="6a076-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="6a076-138">สามารถตั้งค่าคอนฟิกลิงค์ เพื่อให้เปิดบนแท็บใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="6a076-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="6a076-139">การจัดวางข้อความ</span><span class="sxs-lookup"><span data-stu-id="6a076-139">Text placement</span></span> | <span data-ttu-id="6a076-140">**ด้านบนซ้าย** **ด้านบนขวา** **ด้านบนตรงกลาง** **ด้านล่างซ้าย** **ด้านล่างขวา** **ด้านล่างตรงกลาง** **ศูนย์กลางซ้าย** **ศูนย์กลางขวา** หรือ **กึ่งกลางศูนย์กลาง**</span><span class="sxs-lookup"><span data-stu-id="6a076-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="6a076-141">คุณสมบัตินี้กำหนดตำแหน่งของรูปภาพที่สัมพันธ์กับข้อความ</span><span class="sxs-lookup"><span data-stu-id="6a076-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="6a076-142">ตัวอย่างเช่น ถ้า **ด้านขวา** ถูกเลือก รูปภาพจะปรากฏทางด้านขวาของข้อความ</span><span class="sxs-lookup"><span data-stu-id="6a076-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="6a076-143">ชุดรูปแบบของข้อความ</span><span class="sxs-lookup"><span data-stu-id="6a076-143">Text theme</span></span>     | <span data-ttu-id="6a076-144">**สีอ่อน** หรือ **สีเข้ม**</span><span class="sxs-lookup"><span data-stu-id="6a076-144">**Light** or **Dark**</span></span> | <span data-ttu-id="6a076-145">คุณสามารถกำหนดโครงร่างสีสำหรับข้อความได้ ตามรูปภาพพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="6a076-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="6a076-146">ตัวอย่างเช่น ถ้ารูปภาพมีพื้นหลังสีเข้ม ชุดรูปแบบสีอ่อนสามารถใช้เพื่อให้สามารถมองเห็นข้อความได้ชัดขึ้น และเพื่อให้ตรงกับอัตราส่วนความคมชัดของสีสำหรับวัตถุประสงค์ในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="6a076-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="6a076-147">ไล่ระดับสี</span><span class="sxs-lookup"><span data-stu-id="6a076-147">Gradient</span></span>       | <span data-ttu-id="6a076-148">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="6a076-148">**True** or **False**</span></span> | <span data-ttu-id="6a076-149">คุณสามารถใช้การไล่ระดับสีกับรูปภาพ เพื่อให้ตรงกับอัตราส่วนความคมชัดของสีสำหรับวัตถุประสงค์ในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="6a076-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="6a076-150">เพิ่มโมดูลฮีโรไปยังเพจใหม่</span><span class="sxs-lookup"><span data-stu-id="6a076-150">Add a hero module to a new page</span></span>

<span data-ttu-id="6a076-151">การเพิ่มโมดูลฮีโรไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6a076-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6a076-152">ไปที่ **แม่แบบ** และสร้างแม่แบบเพจที่ชื่อ **แม่แบบฮีโร**</span><span class="sxs-lookup"><span data-stu-id="6a076-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="6a076-153">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="6a076-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="6a076-154">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="6a076-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="6a076-155">ใช้แม่แบบฮีโรที่คุณเพิ่งสร้างขึ้นเพื่อสร้างเพจที่ชื่อ **เพจฮีโร**</span><span class="sxs-lookup"><span data-stu-id="6a076-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="6a076-156">ในช่อง **หลัก** ของเพจเริ่มต้น เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="6a076-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6a076-157">ในกล่องโต้ตอบ **เพิ่มโมดูล** ใต้ **เลือกโมดูล** เลือกโมดูลฮีโร จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6a076-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="6a076-158">ในแผนภูมิเค้าร่างทางด้านซ้าย เลือกโมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="6a076-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="6a076-159">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **เพิ่มรูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="6a076-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="6a076-160">เลือกรูปภาพที่มีอยู่ หรืออัพโหลดรูปภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="6a076-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="6a076-161">เลือก **หัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="6a076-161">Select **Heading**.</span></span>
1. <span data-ttu-id="6a076-162">ในกล่องโต้ตอบ **ส่วนหัว** ให้เพิ่มข้อความหัวข้อ เลือกระดับหัวข้อ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6a076-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="6a076-163">ภายใต้ **Rich Text** ให้เพิ่มข้อความตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="6a076-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="6a076-164">เลือก **เพิ่มลิงค์การดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="6a076-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="6a076-165">ในกล่องโต้ตอบ **ลิงค์การดำเนินการ** เพิ่มข้อความลิงค์ URL ลิงค์ และป้ายชื่อ ARIA สำหรับลิงค์ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6a076-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="6a076-166">บันทึกเพจ และแสดงตัวอย่างการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="6a076-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="6a076-167">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="6a076-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a076-168">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6a076-168">Additional resources</span></span>

[<span data-ttu-id="6a076-169">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6a076-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6a076-170">โมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="6a076-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="6a076-171">โมดูลแบบวงล้อ</span><span class="sxs-lookup"><span data-stu-id="6a076-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="6a076-172">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="6a076-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6a076-173">โมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="6a076-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="6a076-174">โมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="6a076-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="6a076-175">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="6a076-175">Video player module</span></span>](add-video-player.md)
