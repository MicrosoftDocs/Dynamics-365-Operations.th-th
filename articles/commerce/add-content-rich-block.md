---
title: โมดูลบล็อกเนื้อหา
description: หัวข้อนี้ครอบคลุมถึงโมดูลคโมดูลบล็อกเนื้อหา และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785432"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="1d75e-103">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1d75e-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1d75e-104">หัวข้อนี้ครอบคลุมถึงโมดูลคโมดูลบล็อกเนื้อหา และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1d75e-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1d75e-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="1d75e-105">Overview</span></span>

<span data-ttu-id="1d75e-106">โมดูลบล็อกเนื้อหาเป็นคอนเทนเนอร์พิเศษที่สามารถจัดเก็บสินค้าที่มีความอุดมสมบูรณ์ของเนื้อหาอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="1d75e-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="1d75e-107">โมดูลบล็อกเนื้อหาใช้สำหรับเนื้อหาแบบข้อความบนเพจ</span><span class="sxs-lookup"><span data-stu-id="1d75e-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="1d75e-108">เนื้อหานี้อาจเป็นการให้ข้อมูลหรือการส่งเสริมการขาย</span><span class="sxs-lookup"><span data-stu-id="1d75e-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="1d75e-109">โมดูลบล็อกเนื้อหาจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS) และสามารถวางบนเพจใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="1d75e-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="1d75e-110">โดยมีโมดูลที่ทำงานแยกต่างหากที่ไม่ขึ้นอยู่กับบริบทเพจ หรือโมดูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1d75e-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="1d75e-111">ตัวอย่างของโมดูลบล็อกเนื้อหาในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="1d75e-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="1d75e-112">โมดูลบล็อกเนื้อหาสามารถใช้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1d75e-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="1d75e-113">เพื่อแสดงคุณลักษณะผลิตภัณฑ์บนเพจรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1d75e-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="1d75e-114">สำหรับใช้เพื่อให้ข้อมูลบนเพจใดๆ</span><span class="sxs-lookup"><span data-stu-id="1d75e-114">For informational purposes on any page.</span></span> <span data-ttu-id="1d75e-115">ตัวอย่างเช่น ผู้ใช้สามารถอธิบายประโยชน์ของโปรแกรมตอบแทนลูกค้าสมาชิกได้ อธิบายนโยบายการจัดส่งและการส่งคืนสินค้า คำถามที่ถามบ่อย หรือระบุเนื้อหา "เกี่ยวกับเรา"</span><span class="sxs-lookup"><span data-stu-id="1d75e-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="1d75e-116">เมื่อต้องการเพิ่มข้อความแบบกำหนดเองบนเพจรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1d75e-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="1d75e-117">(ตัวอย่างเช่น "จัดส่งฟรีสำหรับใบสั่งที่มากกว่า $50")</span><span class="sxs-lookup"><span data-stu-id="1d75e-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="1d75e-118">สำหรับข้อยกเว้นความรับผิดและรายละเอียดการติดต่อบนเพจรายละเอียดของผลิตภัณฑ์ เพจรถเข็น เพจเช็คเอาท์ และเพจอื่นๆ (ตัวอย่างเช่น "การจัดส่งสินค้าและการส่งคืนอยู่ในนโยบายจัดเก็บ")</span><span class="sxs-lookup"><span data-stu-id="1d75e-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="1d75e-119">คุณสมบัติโมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1d75e-119">Content rich block module properties</span></span>

| <span data-ttu-id="1d75e-120">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="1d75e-120">Property name</span></span>     | <span data-ttu-id="1d75e-121">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="1d75e-121">Value</span></span>                                 | <span data-ttu-id="1d75e-122">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="1d75e-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="1d75e-123">จำนวนคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="1d75e-123">Number of columns</span></span> | <span data-ttu-id="1d75e-124">ตัวเลขตั้งแต่ **1** ถึง **4**</span><span class="sxs-lookup"><span data-stu-id="1d75e-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="1d75e-125">จำนวนคอลัมน์ในบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1d75e-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="1d75e-126">สามารถมีได้ถึงสี่คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="1d75e-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="1d75e-127">ความกว้าง</span><span class="sxs-lookup"><span data-stu-id="1d75e-127">Width</span></span>             | <span data-ttu-id="1d75e-128">**เต็มคอนเทนเนอร์** หรือ **เต็มหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="1d75e-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="1d75e-129">ถ้ามีการตั้งค่าให้ **เต็มคอนเทนเนอร์** สินค้าที่อยู่ภายในคอนเทนเนอร์จะถูกจำกัดโดยความกว้างของคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="1d75e-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="1d75e-130">ถ้ามีการตั้งค่าให้ **เต็มหน้าจอ** สินค้าจะไม่ถูกจำกัดไว้ที่ความกว้างของคอนเทนเนอร์ แต่สามารถไปที่โหมดเต็มหน้าจอได้</span><span class="sxs-lookup"><span data-stu-id="1d75e-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="1d75e-131">คุณสามารถเปลี่ยนค่าเพื่อให้บรรลุโครงร่างที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="1d75e-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="1d75e-132">คุณสมบัติโมดูลสินค้าบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1d75e-132">Content rich block item module properties</span></span>

| <span data-ttu-id="1d75e-133">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="1d75e-133">Property name</span></span> | <span data-ttu-id="1d75e-134">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="1d75e-134">Value</span></span>          | <span data-ttu-id="1d75e-135">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1d75e-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="1d75e-136">ย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="1d75e-136">Paragraph</span></span>     | <span data-ttu-id="1d75e-137">ข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="1d75e-137">Paragraph text</span></span> | <span data-ttu-id="1d75e-138">ข้อความที่มาพร้อมกับสินค้าบล็อกเนื้อหาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="1d75e-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="1d75e-139">ความสามารถในการทำงานของข้อความที่สมบูรณ์แบบพื้นฐานบางอย่างจะได้รับการสนับสนุน เช่น ข้อความตัวเอน ขีดเส้นใต้ และแบบตัวหนา</span><span class="sxs-lookup"><span data-stu-id="1d75e-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="1d75e-140">เพิ่มโมดูลบล็อกเนื้อหาไปที่เพจ</span><span class="sxs-lookup"><span data-stu-id="1d75e-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="1d75e-141">การเพิ่มโมดูลบล็อกเนื้อหาไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1d75e-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1d75e-142">สร้างแม่แบบเพจซึ่งชื่อ **แม่แบบเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="1d75e-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="1d75e-143">ในช่อง **หลัก** ของเพจเริ่มต้น ให้เพิ่มโมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1d75e-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="1d75e-144">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="1d75e-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="1d75e-145">ใช้แม่แบบเนื้อหาที่คุณเพิ่งสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="1d75e-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="1d75e-146">ในช่อง **หลัก** ของเพจใหม่ ให้เพิ่มโมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1d75e-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="1d75e-147">ในคุณสมบัติของโมดูลบล็อกเนื้อหา ให้กำหนดจำนวนคอลัมน์เป็น **2**</span><span class="sxs-lookup"><span data-stu-id="1d75e-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="1d75e-148">ในโมดูลบล็อกเนื้อหา ให้เลือก **เพิ่มโมดูล** แล้วเพิ่มสินค้าบล็อกเนื้อหา (ตัวอย่างเช่น **สินค้า1**)</span><span class="sxs-lookup"><span data-stu-id="1d75e-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="1d75e-149">ในสินค้าบล็อกเนื้อหาใหม่ ให้เพิ่มข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="1d75e-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="1d75e-150">ในโมดูลบล็อกเนื้อหา ให้เลือก **เพิ่มโมดูล** แล้วเพิ่มสินค้าบล็อกเนื้อหา (ตัวอย่างเช่น **สินค้า2**)</span><span class="sxs-lookup"><span data-stu-id="1d75e-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="1d75e-151">ในสินค้าบล็อกเนื้อหาใหม่ ให้เพิ่มข้อความย่อหน้า</span><span class="sxs-lookup"><span data-stu-id="1d75e-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="1d75e-152">บันทึกเพจ และแสดงตัวอย่างการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1d75e-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="1d75e-153">คุณควรเห็นบล็อกข้อความสองบล็อกในมุมมองสองคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="1d75e-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="1d75e-154">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="1d75e-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="1d75e-155">ถ้าคุณเพิ่มสินค้าของบล็อคเนื้อหาที่สาม สินค้าจะซ้อนอยู่ด้านล่างสองรายการที่คุณเพิ่มไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="1d75e-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="1d75e-156">ด้วยการเปลี่ยนจำนวนของคอลัมน์ และสินค้าในคอนเทนเนอร์ คุณสามารถบรรลุโครงร่างต่างๆ สำหรับเนื้อหาแบบข้อความได้</span><span class="sxs-lookup"><span data-stu-id="1d75e-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d75e-157">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1d75e-157">Additional resources</span></span>

[<span data-ttu-id="1d75e-158">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1d75e-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1d75e-159">โมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="1d75e-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="1d75e-160">โมดูลแบบวงล้อ</span><span class="sxs-lookup"><span data-stu-id="1d75e-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1d75e-161">โมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="1d75e-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="1d75e-162">โมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="1d75e-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="1d75e-163">โมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="1d75e-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="1d75e-164">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="1d75e-164">Video player module</span></span>](add-video-player.md)

