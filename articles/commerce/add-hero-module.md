---
title: โมดูลบล็อกเนื้อหา
description: หัวข้อนี้ครอบคลุมถึงโมดูลบล็อกเนื้อหาและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0a3fd442f20fd40cdf8b845d353ae5d61ce51e29
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797658"
---
# <a name="content-block-module"></a><span data-ttu-id="90996-103">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="90996-103">Content block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90996-104">หัวข้อนี้ครอบคลุมถึงโมดูลบล็อกเนื้อหาและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="90996-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="90996-105">โมดูลบล็อกเนื้อหาใช้ในการทำตลาดผลิตภัณฑ์ หรือโปรโมชันผ่านการรวมกันของรูปภาพและข้อความ</span><span class="sxs-lookup"><span data-stu-id="90996-105">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="90996-106">ตัวอย่างเช่น ผู้ค้าปลีกสามารถเพิ่มโมดูลบล็อกเนื้อหาไปยังโฮมเพจของไซต์อีคอมเมิร์ซเพื่อส่งเสริมผลิตภัณฑ์ใหม่ และดึงดูดความสนใจของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="90996-106">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="90996-107">โมดูลบล็อกเนื้อหาถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="90996-107">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="90996-108">โมดูลที่ทำงานแยกต่างหากคือโมดูลที่ไม่ขึ้นอยู่กับบริบทเพจ หรือโมดูลอื่นๆ บนเพจ</span><span class="sxs-lookup"><span data-stu-id="90996-108">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="90996-109">โมดูลบล็อกเนื้อหาสามารถวางบนเพจเว็บไซต์ใดๆ ที่ผู้ค้าปลีกต้องการทำตลาด หรือส่งเสริมบางสิ่งบางอย่าง (เช่น ผลิตภัณฑ์ การขาย หรือคุณลักษณะ)</span><span class="sxs-lookup"><span data-stu-id="90996-109">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="90996-110">ตัวอย่างของโมดูลบล็อกเนื้อหาในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="90996-110">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="90996-111">คุณสามารถใช้โมดูลบล็อกเนื้อหาบนโฮมเพจของไซต์อีคอมเมิร์ซ เพื่อเน้นโปรโมชั่นและผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="90996-111">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="90996-112">โมดูลบล็อกเนื้อหาสามารถใช้ในเพจรายละเอียดของผลิตภัณฑ์ เพื่อแสดงข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="90996-112">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="90996-113">หลายโมดูลบล็อกเนื้อหาสามารถใส่ไว้ภายในโมดูลวงล้อเพื่อเน้นผลิตภัณฑ์ หรือโปรโมชั่นต่างๆ</span><span class="sxs-lookup"><span data-stu-id="90996-113">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="90996-114">โมดูลและชุดรูปแบบบล็อคเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="90996-114">Content block modules and themes</span></span>

<span data-ttu-id="90996-115">โมดูลบล็อกเนื้อหาสนับสนุนโครงร่างและลักษณะต่างๆตามชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="90996-115">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="90996-116">ตัวอย่างเช่น ชุดรูปแบบ Fabrikam สนับสนุนการเปลี่ยนแปลงโครงร่างสามแบบของโมดูลบล็อกเนื้อหา: ฮีโร คุณลักษณะ และไทล์</span><span class="sxs-lookup"><span data-stu-id="90996-116">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="90996-117">โครงร่างของฮีโรจะแสดงภาพบนพื้นหลังโดยมีข้อความซ้อนทับ</span><span class="sxs-lookup"><span data-stu-id="90996-117">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="90996-118">โครงร่างลักษณะการทำงานแสดงรูปและข้อความแบบเคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="90996-118">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="90996-119">รูปแบบการจัดรูปแบบไทล์จะช่วยให้แสดงบล็อกเนื้อหาได้หลายรายการในไทล์</span><span class="sxs-lookup"><span data-stu-id="90996-119">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="90996-120">นอกจากนี้ ชุดรูปแบบอาจเปิดเผยคุณสมบัติต่าง ๆ สำหรับแต่ละโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="90996-120">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="90996-121">นักพัฒนาชุดรูปแบบสามารถสร้างโครงร่างเพิ่มเติมโดยใช้ลักษณะการทำงานของโมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="90996-121">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="90996-122">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลที่บล็อคเนื้อหาที่มีโครงร่างแบบฮีโร</span><span class="sxs-lookup"><span data-stu-id="90996-122">The following image shows an example of a content block module with a hero layout.</span></span>

![ตัวอย่างของโมดูลฮีโร่](./media/Hero.PNG)

<span data-ttu-id="90996-124">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลที่บล็อคเนื้อหาที่มีโครงร่างแบบคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="90996-124">The following image shows an example of a content block module with a feature layout.</span></span>

![ตัวอย่างของโมดูลของลักษณะการทำงาน](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="90996-126">คุณสมบัติโมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="90996-126">Content block module properties</span></span>

| <span data-ttu-id="90996-127">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="90996-127">Property name</span></span>  | <span data-ttu-id="90996-128">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="90996-128">Values</span></span> | <span data-ttu-id="90996-129">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="90996-129">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="90996-130">รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="90996-130">Image</span></span>          | <span data-ttu-id="90996-131">ไฟล์รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="90996-131">Image file</span></span> | <span data-ttu-id="90996-132">สามารถใช้รูปภาพเพื่อแสดงผลิตภัณฑ์ หรือโปรโมชันได้</span><span class="sxs-lookup"><span data-stu-id="90996-132">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="90996-133">สามารถอัพโหลดรูปภาพไปที่แกลเลอรีรูปภาพ หรือสามารถใช้รูปภาพที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="90996-133">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="90996-134">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="90996-134">Heading</span></span>        | <span data-ttu-id="90996-135">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="90996-135">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="90996-136">ทุกโมดูลฮีโรสามารถมีหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="90996-136">Every hero module can have a heading.</span></span> <span data-ttu-id="90996-137">โดยค่าเริ่มต้น แท็กหัวเรื่อง **H2** จะใช้สำหรับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="90996-137">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="90996-138">อย่างไรก็ตาม คุณสามารถเปลี่ยนแท็กเพื่อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="90996-138">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="90996-139">ย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="90996-139">Paragraph</span></span>      | <span data-ttu-id="90996-140">ข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="90996-140">Paragraph text</span></span> | <span data-ttu-id="90996-141">โมดูลฮีโรสนับสนุนข้อความย่อหน้าในรูปแบบข้อความที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="90996-141">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="90996-142">ความสามารถในการทำงานของข้อความที่สมบูรณ์แบบพื้นฐานบางอย่างจะได้รับการสนับสนุน เช่น ข้อความตัวเอน ขีดเส้นใต้ และแบบตัวหนา และไฮเปอร์ลิงค์</span><span class="sxs-lookup"><span data-stu-id="90996-142">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="90996-143">ความสามารถบางอย่างเหล่านี้อาจถูกแทนที่ด้วยชุดรูปแบบของเพจที่ใช้กับโมดูล</span><span class="sxs-lookup"><span data-stu-id="90996-143">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="90996-144">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="90996-144">Link</span></span>           | <span data-ttu-id="90996-145">ลิงค์ข้อความ ลิงค์ URL ป้ายชื่อ Accessible Rich Internet Applications (ARIA) และ **เปิดลิงค์ในแท็บใหม่**</span><span class="sxs-lookup"><span data-stu-id="90996-145">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="90996-146">โมดูลฮีโรสนับสนุนลิงค์ "การกระตุ้นให้ดำเนินการ" หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="90996-146">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="90996-147">ถ้ามีการเพิ่มลิงค์ ลิงค์ข้อความ URL และป้ายชื่อ ARIA จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="90996-147">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="90996-148">ป้ายชื่อ ARIA ควรเป็นคำอธิบายเพื่อให้ตรงตามข้อกำหนดของความสามารถในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="90996-148">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="90996-149">สามารถตั้งค่าคอนฟิกลิงค์ เพื่อให้เปิดบนแท็บใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="90996-149">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="90996-150">คุณสมบัติโมดูลของบล็อคเนื้อหา ที่เปิดเผยโดยชุดรูปแบบ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="90996-150">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="90996-151">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="90996-151">Property name</span></span>  | <span data-ttu-id="90996-152">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="90996-152">Values</span></span> | <span data-ttu-id="90996-153">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="90996-153">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="90996-154">การจัดวางข้อความ</span><span class="sxs-lookup"><span data-stu-id="90996-154">Text placement</span></span> | <span data-ttu-id="90996-155">**ซ้าย** **ขวา** **กึ่งกลาง**</span><span class="sxs-lookup"><span data-stu-id="90996-155">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="90996-156">คุณสมบัตินี้กำหนดตำแหน่งของข้อความที่สัมพันธ์กับรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="90996-156">This property defines the position of the text on the image.</span></span> <span data-ttu-id="90996-157">ใช้กับโครงร่างแบบฮีโรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="90996-157">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="90996-158">ชุดรูปแบบของข้อความ</span><span class="sxs-lookup"><span data-stu-id="90996-158">Text theme</span></span>     | <span data-ttu-id="90996-159">**สีอ่อน** หรือ **สีเข้ม**</span><span class="sxs-lookup"><span data-stu-id="90996-159">**Light** or **Dark**</span></span> | <span data-ttu-id="90996-160">คุณสามารถกำหนดโครงร่างสีสำหรับข้อความได้ ตามรูปภาพพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="90996-160">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="90996-161">ตัวอย่างเช่น ถ้ารูปภาพมีพื้นหลังสีเข้ม ชุดรูปแบบสีอ่อนสามารถใช้เพื่อให้สามารถมองเห็นข้อความได้ชัดขึ้น และเพื่อให้ตรงกับอัตราส่วนความคมชัดของสีสำหรับวัตถุประสงค์ในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="90996-161">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="90996-162">ใช้กับโครงร่างแบบฮีโรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="90996-162">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="90996-163">การจัดวางรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="90996-163">Image placement</span></span>       | <span data-ttu-id="90996-164">**ซ้าย** **ขวา**</span><span class="sxs-lookup"><span data-stu-id="90996-164">**Left**,  **Right**</span></span> | <span data-ttu-id="90996-165">คุณสมบัตินี้จะระบุว่ารูปภาพควรอยู่ทางด้านซ้ายหรือด้านขวาของข้อความ</span><span class="sxs-lookup"><span data-stu-id="90996-165">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="90996-166">ใช้กับโครงร่างแบบคุณลักษณะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="90996-166">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="90996-167">เพิ่มโมดูลบล็อกเนื้อหาไปที่เพจใหม่</span><span class="sxs-lookup"><span data-stu-id="90996-167">Add a content block module to a new page</span></span>

<span data-ttu-id="90996-168">การเพิ่มโมดูลฮีโรไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="90996-168">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="90996-169">ไปที่ **เท็มเพลต** และสร้างเท็มเพลตเพจที่ชื่อ **เท็มเพลตบล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="90996-169">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="90996-170">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="90996-170">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="90996-171">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="90996-171">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="90996-172">ใช้เท็มเพลตฮีโรที่คุณเพิ่งสร้างขึ้น เพื่อสร้างหน้าที่ชื่อ **หน้าบล็อกเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="90996-172">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="90996-173">ในช่อง **หลัก** ของเพจเริ่มต้น เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="90996-173">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="90996-174">ในกล่องโต้ตอบ **เพิ่มโมดูล** ใต้ **เลือกโมดูล** เลือกโมดูลฮีโร จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="90996-174">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="90996-175">ในแผนภูมิเค้าร่างทางด้านซ้าย เลือกโมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="90996-175">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="90996-176">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **เพิ่มรูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="90996-176">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="90996-177">เลือกรูปภาพที่มีอยู่ หรืออัพโหลดรูปภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="90996-177">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="90996-178">เลือก **หัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="90996-178">Select **Heading**.</span></span>
1. <span data-ttu-id="90996-179">ในกล่องโต้ตอบ **ส่วนหัว** ให้เพิ่มข้อความหัวข้อ เลือกระดับหัวข้อ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="90996-179">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="90996-180">ภายใต้ **Rich Text** ให้เพิ่มข้อความตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="90996-180">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="90996-181">เลือก **เพิ่มลิงก์**</span><span class="sxs-lookup"><span data-stu-id="90996-181">Select **Add Link**.</span></span>
1. <span data-ttu-id="90996-182">ในกล่องโต้ตอบ **ลิงก์** เพิ่มข้อความลิงก์ URL ลิงก์ และป้ายชื่อ ARIA สำหรับลิงค์ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="90996-182">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="90996-183">เลือกโครงร่าง **ฮีโร**</span><span class="sxs-lookup"><span data-stu-id="90996-183">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="90996-184">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="90996-184">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="90996-185">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="90996-185">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="90996-186">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="90996-186">Additional resources</span></span>

[<span data-ttu-id="90996-187">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="90996-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="90996-188">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="90996-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="90996-189">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="90996-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="90996-190">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="90996-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="90996-191">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="90996-191">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]