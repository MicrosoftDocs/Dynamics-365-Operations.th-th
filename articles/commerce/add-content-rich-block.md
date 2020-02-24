---
title: โมดูลบล็อคข้อความ
description: หัวข้อนี้ครอบคลุมถึงโมดูลคโมดูลบล็อกข้อความ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025608"
---
# <a name="text-block-module"></a><span data-ttu-id="01618-103">โมดูลบล็อคข้อความ</span><span class="sxs-lookup"><span data-stu-id="01618-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="01618-104">หัวข้อนี้ครอบคลุมถึงโมดูลคโมดูลบล็อกข้อความ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="01618-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="01618-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="01618-105">Overview</span></span>

<span data-ttu-id="01618-106">โมดูลบล็อคข้อความเป็นโมดูลที่ใช้ในการเพิ่มเนื้อหาแบบข้อความ</span><span class="sxs-lookup"><span data-stu-id="01618-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="01618-107">เนื้อหานี้อาจเป็นการให้ข้อมูล หรือการส่งเสริมการขาย</span><span class="sxs-lookup"><span data-stu-id="01618-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="01618-108">โมดูลบล็อคข้อความจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS) และสามารถวางบนหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="01618-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="01618-109">โดยมีโมดูลที่ทำงานแยกต่างหากที่ไม่ขึ้นอยู่กับบริบทเพจ หรือโมดูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="01618-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="01618-110">ตัวอย่างของโมดูลบล็อกข้อความในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="01618-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="01618-111">โมดูลบล็อกข้อความสามารถใช้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="01618-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="01618-112">เพื่อแสดงคุณลักษณะผลิตภัณฑ์บนเพจรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01618-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="01618-113">สำหรับใช้เพื่อให้ข้อมูลบนเพจใดๆ</span><span class="sxs-lookup"><span data-stu-id="01618-113">For informational purposes on any page.</span></span> <span data-ttu-id="01618-114">ตัวอย่างเช่น ผู้ใช้สามารถอธิบายประโยชน์ของโปรแกรมตอบแทนลูกค้าสมาชิกได้ อธิบายนโยบายการจัดส่งและการส่งคืนสินค้า คำถามที่ถามบ่อย หรือระบุเนื้อหา "เกี่ยวกับเรา"</span><span class="sxs-lookup"><span data-stu-id="01618-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="01618-115">เมื่อต้องการเพิ่มข้อความแบบกำหนดเองบนเพจรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="01618-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="01618-116">(ตัวอย่างเช่น "จัดส่งฟรีสำหรับใบสั่งที่มากกว่า $50")</span><span class="sxs-lookup"><span data-stu-id="01618-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="01618-117">สำหรับข้อยกเว้นความรับผิดและรายละเอียดการติดต่อบนเพจรายละเอียดของผลิตภัณฑ์ เพจรถเข็น เพจเช็คเอาท์ และเพจอื่นๆ (ตัวอย่างเช่น "การจัดส่งสินค้าและการส่งคืนอยู่ในนโยบายจัดเก็บ")</span><span class="sxs-lookup"><span data-stu-id="01618-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="01618-118">คุณสมบัติโมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="01618-118">Text block module properties</span></span>

| <span data-ttu-id="01618-119">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="01618-119">Property name</span></span>     | <span data-ttu-id="01618-120">Value</span><span class="sxs-lookup"><span data-stu-id="01618-120">Value</span></span>                                            | <span data-ttu-id="01618-121">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="01618-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="01618-122">ข้อความตกแต่ง</span><span class="sxs-lookup"><span data-stu-id="01618-122">Rich text</span></span>         | <span data-ttu-id="01618-123">ข้อความตกแต่ง</span><span class="sxs-lookup"><span data-stu-id="01618-123">Rich text</span></span>                                        | <span data-ttu-id="01618-124">ข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="01618-124">Paragraph text.</span></span> <span data-ttu-id="01618-125">ความสามารถในการทำงานของข้อความที่สมบูรณ์แบบพื้นฐานบางอย่างจะได้รับการสนับสนุน เช่น ข้อความตัวเอน ขีดเส้นใต้ และแบบตัวหนา</span><span class="sxs-lookup"><span data-stu-id="01618-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="01618-126">ชื่อคลาส แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="01618-126">Custom class name</span></span> | <span data-ttu-id="01618-127">ชื่อคลาส Cascading Sheet Sheet (CSS)</span><span class="sxs-lookup"><span data-stu-id="01618-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="01618-128">ชื่อของคลาส CSS ที่กำหนดเองที่นักพัฒนาจัดเตรียมให้กับโมดูลนี้</span><span class="sxs-lookup"><span data-stu-id="01618-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="01618-129">ชื่อคลาสควรกำหนดในชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="01618-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="01618-130">ขนาดแบบอักษร</span><span class="sxs-lookup"><span data-stu-id="01618-130">Font size</span></span>         | <span data-ttu-id="01618-131">**เล็ก** **กลาง** **ใหญ่** **ใหญ่พิเศษ**</span><span class="sxs-lookup"><span data-stu-id="01618-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="01618-132">ขนาดแบบอักษรของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="01618-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="01618-133">เพิ่มโมดูลบล็อคข้อความไปที่เพจใหม่</span><span class="sxs-lookup"><span data-stu-id="01618-133">Add a text block module to a page</span></span>

<span data-ttu-id="01618-134">การเพิ่มโมดูลบล็อกข้อความไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="01618-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="01618-135">สร้างแม่แบบเพจซึ่งชื่อ **แม่แบบเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="01618-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="01618-136">ในช่อง **Body** ให้เพิ่มโมดูล **หน้าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="01618-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="01618-137">แก้ไขแม่แบบให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="01618-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="01618-138">ใช้แม่แบบเนื้อหาที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="01618-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="01618-139">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="01618-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="01618-140">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลคอนเทนเนอร์ ตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="01618-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="01618-141">เพิ่มโมดูลบล็อคข้อความไปยังโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="01618-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="01618-142">ในบานหน้าต่างคุณสมบัติของโมดูลบล็อคข้อความให้เพิ่มข้อความในฟิลด์ **Rich Text**</span><span class="sxs-lookup"><span data-stu-id="01618-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="01618-143">แก้ไขหน้าให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="01618-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01618-144">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="01618-144">Additional resources</span></span>

[<span data-ttu-id="01618-145">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="01618-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="01618-146">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="01618-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="01618-147">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="01618-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="01618-148">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="01618-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="01618-149">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="01618-149">Video player module</span></span>](add-video-player.md)

