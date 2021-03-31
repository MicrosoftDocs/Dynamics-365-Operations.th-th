---
title: โมดูลบล็อคข้อความ
description: หัวข้อนี้ครอบคลุมถึงโมดูลบล็อกข้อความและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3926f23e4e762a49ef94ef0c8f3291e7e9a4a6a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206402"
---
# <a name="text-block-module"></a><span data-ttu-id="77cf2-103">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="77cf2-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77cf2-104">หัวข้อนี้ครอบคลุมถึงโมดูลบล็อกข้อความและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="77cf2-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="77cf2-105">โมดูลบล็อคข้อความเป็นโมดูลที่ใช้ในการเพิ่มเนื้อหาแบบข้อความ</span><span class="sxs-lookup"><span data-stu-id="77cf2-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="77cf2-106">เนื้อหานี้อาจเป็นการให้ข้อมูล หรือการส่งเสริมการขาย</span><span class="sxs-lookup"><span data-stu-id="77cf2-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="77cf2-107">โมดูลบล็อคข้อความจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS) และสามารถวางบนหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="77cf2-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="77cf2-108">โดยมีโมดูลที่ทำงานแยกต่างหากที่ไม่ขึ้นอยู่กับบริบทเพจ หรือโมดูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="77cf2-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="77cf2-109">ตัวอย่างของโมดูลบล็อกข้อความในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="77cf2-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="77cf2-110">โมดูลบล็อกข้อความสามารถใช้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="77cf2-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="77cf2-111">เพื่อแสดงคุณลักษณะผลิตภัณฑ์บนเพจรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="77cf2-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="77cf2-112">สำหรับใช้เพื่อให้ข้อมูลบนเพจใดๆ</span><span class="sxs-lookup"><span data-stu-id="77cf2-112">For informational purposes on any page.</span></span> <span data-ttu-id="77cf2-113">ตัวอย่างเช่น ผู้ใช้สามารถอธิบายประโยชน์ของโปรแกรมตอบแทนลูกค้าสมาชิกได้ อธิบายนโยบายการจัดส่งและการส่งคืนสินค้า คำถามที่ถามบ่อย หรือระบุเนื้อหา "เกี่ยวกับเรา"</span><span class="sxs-lookup"><span data-stu-id="77cf2-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="77cf2-114">เมื่อต้องการเพิ่มข้อความแบบกำหนดเองบนเพจรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="77cf2-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="77cf2-115">(ตัวอย่างเช่น "จัดส่งฟรีสำหรับใบสั่งที่มากกว่า $50")</span><span class="sxs-lookup"><span data-stu-id="77cf2-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="77cf2-116">สำหรับข้อยกเว้นความรับผิดและรายละเอียดการติดต่อบนเพจรายละเอียดของผลิตภัณฑ์ เพจรถเข็น เพจเช็คเอาท์ และเพจอื่นๆ (ตัวอย่างเช่น "การจัดส่งสินค้าและการส่งคืนอยู่ในนโยบายจัดเก็บ")</span><span class="sxs-lookup"><span data-stu-id="77cf2-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="77cf2-117">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลบล็อกข้อความที่ใช้ในโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="77cf2-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![ตัวอย่างของโมดูลบล็อกข้อความ](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="77cf2-119">คุณสมบัติโมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="77cf2-119">Text block module properties</span></span>

| <span data-ttu-id="77cf2-120">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="77cf2-120">Property name</span></span>     | <span data-ttu-id="77cf2-121">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="77cf2-121">Value</span></span>                                            | <span data-ttu-id="77cf2-122">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="77cf2-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="77cf2-123">ข้อความตกแต่ง</span><span class="sxs-lookup"><span data-stu-id="77cf2-123">Rich text</span></span>         | <span data-ttu-id="77cf2-124">ข้อความตกแต่ง</span><span class="sxs-lookup"><span data-stu-id="77cf2-124">Rich text</span></span>                                        | <span data-ttu-id="77cf2-125">ข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="77cf2-125">Paragraph text.</span></span> <span data-ttu-id="77cf2-126">ความสามารถในการทำงานของข้อความที่สมบูรณ์แบบพื้นฐานบางอย่างจะได้รับการสนับสนุน เช่น ข้อความตัวเอน ขีดเส้นใต้ และแบบตัวหนา</span><span class="sxs-lookup"><span data-stu-id="77cf2-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="77cf2-127">ชื่อคลาส แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="77cf2-127">Custom class name</span></span> | <span data-ttu-id="77cf2-128">ชื่อคลาส Cascading Sheet Sheet (CSS)</span><span class="sxs-lookup"><span data-stu-id="77cf2-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="77cf2-129">ชื่อของคลาส CSS ที่กำหนดเองที่นักพัฒนาจัดเตรียมให้กับโมดูลนี้</span><span class="sxs-lookup"><span data-stu-id="77cf2-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="77cf2-130">ชื่อคลาสควรกำหนดในชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="77cf2-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="77cf2-131">ขนาดแบบอักษร</span><span class="sxs-lookup"><span data-stu-id="77cf2-131">Font size</span></span>         | <span data-ttu-id="77cf2-132">**เล็ก** **กลาง** **ใหญ่** **ใหญ่พิเศษ**</span><span class="sxs-lookup"><span data-stu-id="77cf2-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="77cf2-133">ขนาดแบบอักษรของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="77cf2-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="77cf2-134">เพิ่มโมดูลบล็อคข้อความไปที่เพจใหม่</span><span class="sxs-lookup"><span data-stu-id="77cf2-134">Add a text block module to a page</span></span>

<span data-ttu-id="77cf2-135">การเพิ่มโมดูลบล็อกข้อความไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="77cf2-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="77cf2-136">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="77cf2-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="77cf2-137">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="77cf2-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="77cf2-138">ในช่อง **เนื้อหา** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="77cf2-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="77cf2-139">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หน้าเริ่มต้น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="77cf2-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="77cf2-140">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="77cf2-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="77cf2-141">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="77cf2-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="77cf2-142">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือก **เท็มเพลตเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="77cf2-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="77cf2-143">ใต้ **ชื่อของหน้า** ให้ป้อน **หน้าเนื้อหา** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="77cf2-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="77cf2-144">ในช่อง **หลัก** ของหน้าใหม่ เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="77cf2-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="77cf2-145">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="77cf2-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="77cf2-146">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลคอนเทนเนอร์ ตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="77cf2-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="77cf2-147">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="77cf2-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="77cf2-148">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **บล็อกข้อความ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="77cf2-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="77cf2-149">ในบานหน้าต่างคุณสมบัติของโมดูลบล็อคข้อความให้เพิ่มข้อความในฟิลด์ **Rich Text**</span><span class="sxs-lookup"><span data-stu-id="77cf2-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="77cf2-150">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="77cf2-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="77cf2-151">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="77cf2-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77cf2-152">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="77cf2-152">Additional resources</span></span>

[<span data-ttu-id="77cf2-153">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="77cf2-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="77cf2-154">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="77cf2-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="77cf2-155">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="77cf2-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="77cf2-156">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="77cf2-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="77cf2-157">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="77cf2-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]