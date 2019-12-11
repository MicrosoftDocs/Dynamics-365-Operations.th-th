---
title: โมดูลการจัดวางเนื้อหา
description: หัวข้อนี้ครอบคลุมถึงโมดูลการจัดวางเนื้อหาและโมดูลสินค้าการจัดวางเนื้อหา และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785311"
---
# <a name="content-placement-module"></a><span data-ttu-id="2b240-103">โมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2b240-104">หัวข้อนี้ครอบคลุมถึงโมดูลการจัดวางเนื้อหาและโมดูลสินค้าการจัดวางเนื้อหา และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2b240-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b240-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="2b240-105">Overview</span></span>

<span data-ttu-id="2b240-106">โมดูลการจัดวางเนื้อหาเป็นคอนเทนเนอร์พิเศษที่สามารถใส่โมดูลอื่นๆ ในเค้าโครงเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="2b240-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="2b240-107">โมดูลการจัดวางเนื้อหาสนับสนุนชนิดของโมดูลต่อไปนี้เป็นโมดูลรอง: สินค้าการจัดวางเนื้อหา สินค้าต้อนรับของบัญชี สินค้าในใบสั่งของบัญชี สินค้าที่ต้องการของบัญชี และสินค้าในโพรไฟล์ของบัญชี</span><span class="sxs-lookup"><span data-stu-id="2b240-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="2b240-108">โมดูลการจัดวางเนื้อหาที่สืบทอดข้อมูลมาจากโมดูลรองที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="2b240-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="2b240-109">ดังนั้น โมดูลการจัดวางเนื้อหาสามารถใช้ในลักษณะต่างๆ ได้ ทั้งนี้ขึ้นอยู่กับโมดูลที่เพิ่มเข้ามา</span><span class="sxs-lookup"><span data-stu-id="2b240-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="2b240-110">โมดูลรายการการจัดวางเนื้อหาใช้ทั้งรูปภาพและข้อความที่จะแสดงโปรโมชัน นโยบาย และคุณลักษณะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b240-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="2b240-111">ตัวอย่างเช่น โมดูลสินค้าการจัดวางเนื้อหาสามารถใช้บนโฮมเพจ เพื่อแสดงนโยบายร้านค้า หรือข้อมูลการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="2b240-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="2b240-112">โมดูลสินค้าการจัดวางเนื้อหาจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS) และสามารถวางบนเพจใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="2b240-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="2b240-113">อย่างไรก็ตาม คุณสามารถใช้ได้เฉพาะภายในโมดูลการจัดวางเนื้อหาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2b240-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="2b240-114">ตัวอย่างของโมดูลการจัดวางเนื้อหาในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="2b240-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="2b240-115">โมดูลการจัดวางเนื้อหาที่มีโมดูลรายการการจัดวางเนื้อหาสามารถใช้บนโฮมเพจ หรือเพจการตลาด เพื่อแสดงคุณลักษณะของผลิตภัณฑ์ โปรโมชั่น นโยบายร้านค้า ข้อมูลการจัดส่ง และข้อมูลอื่นๆ ผ่านทั้งรูปภาพและข้อความ</span><span class="sxs-lookup"><span data-stu-id="2b240-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="2b240-116">โมดูลการจัดวางเนื้อหาที่มีโมดูลสินค้าการจัดวางเนื้อหาสามารถใช้บนเพจรายละเอียดของผลิตภัณฑ์ เพื่อแสดงคุณลักษณะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b240-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="2b240-117">โมดูลการจัดวางเนื้อหาที่มีโมดูลสินค้าต้อนรับบัญชี หรือโมดูลสินค้าใบสั่งของของบัญชี สามารถใช้บนเพจการจัดการบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="2b240-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="2b240-118">คุณสมบัติของโมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-118">Content placement module properties</span></span>

| <span data-ttu-id="2b240-119">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="2b240-119">Property name</span></span> | <span data-ttu-id="2b240-120">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2b240-120">Value</span></span> | <span data-ttu-id="2b240-121">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2b240-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="2b240-122">ความกว้าง</span><span class="sxs-lookup"><span data-stu-id="2b240-122">Width</span></span>         | <span data-ttu-id="2b240-123">**พอดีกับคอนเทนเนอร์** หรือ **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="2b240-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="2b240-124">ถ้ามีการตั้งค่าให้ **พอดีกับคอนเทนเนอร์** สินค้าที่อยู่ภายในโมดูลการจัดวางเนื้อหาจะถูกจำกัดความกว้างของโมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="2b240-125">ถ้ามีการตั้งค่าให้ **เต็มหน้าจอ** สินค้าจะไม่ถูกจำกัดไว้ที่ความกว้างของโมดูลการจัดวางเนื้อหา แต่สามารถไปที่โหมดเต็มหน้าจอได้</span><span class="sxs-lookup"><span data-stu-id="2b240-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="2b240-126">คุณสมบัติของโมดูลสินค้าการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-126">Content placement item module properties</span></span>

| <span data-ttu-id="2b240-127">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="2b240-127">Property name</span></span> | <span data-ttu-id="2b240-128">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2b240-128">Value</span></span> | <span data-ttu-id="2b240-129">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2b240-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="2b240-130">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="2b240-130">Heading</span></span>       | <span data-ttu-id="2b240-131">ข้อความหัวข้อ และแท็กหัวข้อ (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span><span class="sxs-lookup"><span data-stu-id="2b240-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="2b240-132">โมดูลสินค้าการจัดวางเนื้อหาทั้งหมดสามารถมีหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="2b240-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="2b240-133">คุณสมบัติ **หัวข้อ** สนับสนุนแท็กหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="2b240-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="2b240-134">โดยค่าเริ่มต้น แท็กหัวข้อ **H2** จะถูกใช้ แต่สามารถเปลี่ยนแท็กหัวข้อให้ตรงกับความต้องการสำหรับการเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="2b240-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="2b240-135">ย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="2b240-135">Paragraph</span></span>     | <span data-ttu-id="2b240-136">ข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="2b240-136">Paragraph text</span></span> | <span data-ttu-id="2b240-137">โมดูลสินค้าการจัดวางเนื้อหาสนับสนุนข้อความย่อหน้าในรูปแบบข้อความที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="2b240-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="2b240-138">ความสามารถในการทำงานของข้อความที่สมบูรณ์แบบพื้นฐานบางอย่างจะได้รับการสนับสนุน เช่น ข้อความตัวเอน ขีดเส้นใต้ และแบบตัวหนา และไฮเปอร์ลิงค์</span><span class="sxs-lookup"><span data-stu-id="2b240-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="2b240-139">ความสามารถบางอย่างเหล่านี้อาจถูกแทนที่ด้วยชุดรูปแบบของเพจที่ใช้กับโมดูล</span><span class="sxs-lookup"><span data-stu-id="2b240-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="2b240-140">รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="2b240-140">Image</span></span>         | <span data-ttu-id="2b240-141">ไฟล์รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="2b240-141">Image file</span></span> | <span data-ttu-id="2b240-142">รูปภาพอาจสัมพันธ์กับข้อความ</span><span class="sxs-lookup"><span data-stu-id="2b240-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="2b240-143">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="2b240-143">Link</span></span>          | <span data-ttu-id="2b240-144">URL ของลิงค์และข้อความลิงค์</span><span class="sxs-lookup"><span data-stu-id="2b240-144">Link URL and link text</span></span> | <span data-ttu-id="2b240-145">สามารถเพิ่มลิงค์ไปที่ข้อความเพื่อเปลี่ยนเส้นทางผู้ใช้ไปยังเพจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2b240-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="2b240-146">ขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="2b240-146">Tile size</span></span>     | <span data-ttu-id="2b240-147">ตัวเลขตั้งแต่ **1** ถึง **12**</span><span class="sxs-lookup"><span data-stu-id="2b240-147">A number from **1** through **12**</span></span> | <span data-ttu-id="2b240-148">สำหรับแต่ละสินค้าการจัดวางเนื้อหา คุณสมบัตินี้จะกำหนดจำนวนช่องที่สินค้าควรกรอกข้อมูลในโมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="2b240-149">ขนาดสูงสุดของโมดูลการจัดวางเนื้อหา คือ 12 ช่อง</span><span class="sxs-lookup"><span data-stu-id="2b240-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="2b240-150">ถ้าขนาดของไทล์รวมสำหรับสินค้า *n* แรกในโมดูลการจัดวางเนื้อหาเกินกว่า 12 ช่อง สินค้าจะถูกห่อไปยังแถวถัดไป</span><span class="sxs-lookup"><span data-stu-id="2b240-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="2b240-151">เพิ่มโมดูลการจัดวางเนื้อหาที่มีโมดูลสินค้าการจัดวางเนื้อหาไปที่เพจ</span><span class="sxs-lookup"><span data-stu-id="2b240-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="2b240-152">เมื่อต้องการเพิ่มโมดูลการจัดวางเนื้อหาที่มีโมดูลสินค้าการจัดวางเนื้อหาไปที่เพจใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b240-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2b240-153">สร้างแม่แบบที่ชื่อ **แม่แบบการจัดวางเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="2b240-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="2b240-154">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="2b240-155">ในโมดูลการจัดวางเนื้อหา เพิ่มโมดูลสินค้าการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="2b240-156">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2b240-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="2b240-157">ใช้แม่แบบการจัดวางเนื้อหาที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจการจัดวางเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="2b240-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="2b240-158">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="2b240-159">ในโมดูลการจัดวางเนื้อหา เพิ่มโมดูลสินค้าการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="2b240-160">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลสินค้าการจัดวางเนื้อหา ให้เลือกรูปภาพ เพิ่มหัวข้อ เพิ่มย่อหน้า เพิ่มลิงค์ แล้วตั้งค่า URL ลิงค์ และตั้งค่าขนาดไทล์เป็น **6**</span><span class="sxs-lookup"><span data-stu-id="2b240-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="2b240-161">ทำซ้ำขั้นตอนที่ 7 และ 8 เพื่อเพิ่มโมดูลสินค้าการจัดวางเนื้อหาอื่น ที่มีขนาดไทล์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="2b240-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="2b240-162">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="2b240-162">Save and preview the page.</span></span> <span data-ttu-id="2b240-163">คุณควรเห็นสินค้าการจัดวางเนื้อหาสองรายการที่แสดงอยู่เคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="2b240-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="2b240-164">คุณสามารถปรับปรุงคุณสมบัติ **ขนาดไทล์** ของแต่ละโมดูลการจัดวางเนื้อหา หรือเพิ่มโมดูลเพิ่มเติม เพื่อให้บรรลุโครงร่างที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="2b240-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="2b240-165">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2b240-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b240-166">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b240-166">Additional resources</span></span>

[<span data-ttu-id="2b240-167">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2b240-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2b240-168">โมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="2b240-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="2b240-169">โมดูลแบบวงล้อ</span><span class="sxs-lookup"><span data-stu-id="2b240-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2b240-170">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2b240-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2b240-171">โมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="2b240-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="2b240-172">โมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="2b240-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="2b240-173">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="2b240-173">Video player module</span></span>](add-video-player.md)
