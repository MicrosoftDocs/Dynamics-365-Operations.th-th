---
title: โมดูลแบนเนอร์โปรโมชั่น
description: หัวข้อนี้ครอบคลุมถึงโมดูลแบนเนอร์โปรโมชั่น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025631"
---
# <a name="promo-banner-module"></a><span data-ttu-id="5a60f-103">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="5a60f-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5a60f-104">หัวข้อนี้ครอบคลุมถึงโมดูลแบนเนอร์โปรโมชั่น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5a60f-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5a60f-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="5a60f-105">Overview</span></span>

<span data-ttu-id="5a60f-106">โมดูลแบนเนอร์โปรโมชั่นใช้เพื่อแสดงข้อความที่ให้ข้อมูลแบบอินไลน์บนหน้า</span><span class="sxs-lookup"><span data-stu-id="5a60f-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="5a60f-107">ผู้ใช้สามารถใช้เพื่อแสดงโปรโมชันทั้งไซต์ที่ปรากฏในหน้าทั้งหมดของไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="5a60f-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="5a60f-108">โมดูลแบนเนอร์โปรโมชั่นสนับสนุนข้อความตัวอักษรและลิงค์</span><span class="sxs-lookup"><span data-stu-id="5a60f-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="5a60f-109">ถ้ามีการเพิ่มข้อความหลายรายการในโมดูลแบนเนอร์โปรโมชั่น โมดูลจะกลายเป็นแบนเนอร์แบบวงล้อที่ให้ลูกค้าวนผ่านข้อความทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5a60f-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="5a60f-110">โมดูลแบนเนอร์โปรโมชั่นจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS) และสามารถวางบนหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="5a60f-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="5a60f-111">ตัวอย่างการใช้งานของแบนเนอร์โปรโมชั่นในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="5a60f-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="5a60f-112">แบนเนอร์โปรโมชั่นสามารถใช้ในส่วนหัวของไซต์ เพื่อแสดงข้อความหรือข้อความทั่วทั้งไซต์ เช่นเดียวกับในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5a60f-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="5a60f-113">"ยอดขายประจำปีสิ้นสุดในเวลา10วัน"</span><span class="sxs-lookup"><span data-stu-id="5a60f-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="5a60f-114">"ประหยัดอย่างมากกับโปรโมชัน Back to School</span><span class="sxs-lookup"><span data-stu-id="5a60f-114">"Save big with back to school sale.</span></span> <span data-ttu-id="5a60f-115">ซื้อตอนนี้ "</span><span class="sxs-lookup"><span data-stu-id="5a60f-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="5a60f-116">คุณสมบัติโมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="5a60f-116">Promo banner module properties</span></span>

| <span data-ttu-id="5a60f-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="5a60f-117">Property name</span></span>             | <span data-ttu-id="5a60f-118">Value</span><span class="sxs-lookup"><span data-stu-id="5a60f-118">Value</span></span>                              | <span data-ttu-id="5a60f-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5a60f-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="5a60f-120">ข้อความแบนเนอร์</span><span class="sxs-lookup"><span data-stu-id="5a60f-120">Banner messages</span></span>           | <span data-ttu-id="5a60f-121">ข้อความและลิงก์</span><span class="sxs-lookup"><span data-stu-id="5a60f-121">Text and links</span></span>                     | <span data-ttu-id="5a60f-122">แถวของข้อความและลิงก์</span><span class="sxs-lookup"><span data-stu-id="5a60f-122">An array of text and links.</span></span> |
| <span data-ttu-id="5a60f-123">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5a60f-123">Autoplay</span></span>                  | <span data-ttu-id="5a60f-124">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="5a60f-124">**True** or **False**</span></span>              | <span data-ttu-id="5a60f-125">ค่าที่ระบุว่าข้อความจะถูกวนโดยอัตโนมัติหรือไม่ ถ้ามีการตั้งค่าคอนฟิกข้อความจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="5a60f-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="5a60f-126">ช่วงเวลาของการเปลี่ยนภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="5a60f-126">Slide transition interval</span></span> | <span data-ttu-id="5a60f-127">จำนวนมิลลิวินาที (ms)</span><span class="sxs-lookup"><span data-stu-id="5a60f-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="5a60f-128">ช่วงเวลาที่ใช้ในการวนผ่านข้อความ</span><span class="sxs-lookup"><span data-stu-id="5a60f-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="5a60f-129">อนุญาตให้ปิด</span><span class="sxs-lookup"><span data-stu-id="5a60f-129">Allow dismiss</span></span>             | <span data-ttu-id="5a60f-130">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="5a60f-130">**True** or **False**</span></span>              | <span data-ttu-id="5a60f-131">หากค่าถูกตั้งเป็น **จริง** ลูกค้าสามารถยกเลิกการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="5a60f-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="5a60f-132">แสดงตัวเลื่อนวงล้อ</span><span class="sxs-lookup"><span data-stu-id="5a60f-132">Show carousel flipper</span></span>     | <span data-ttu-id="5a60f-133">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="5a60f-133">**True** or **False**</span></span>              | <span data-ttu-id="5a60f-134">ค่าที่ระบุว่าควรจะแสดงตัวหมุนวงล้อหรือไม่ เพื่อให้ลูกค้าสามารถหมุนรายการแบนเนอร์หลายรายการด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="5a60f-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="5a60f-135">การปรับแนวข้อความ</span><span class="sxs-lookup"><span data-stu-id="5a60f-135">Text alignment</span></span>            | <span data-ttu-id="5a60f-136">**ขวา** **ซ้าย** หรือ **กึ่งกลาง**</span><span class="sxs-lookup"><span data-stu-id="5a60f-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="5a60f-137">การจัดแนวข้อความในโมดูลแบนเนอร์โปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="5a60f-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="5a60f-138">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="5a60f-138">Link</span></span>                      | <span data-ttu-id="5a60f-139">URL</span><span class="sxs-lookup"><span data-stu-id="5a60f-139">A URL</span></span>                              | <span data-ttu-id="5a60f-140">URL สำหรับลิงก์ทางเลือก</span><span class="sxs-lookup"><span data-stu-id="5a60f-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="5a60f-141">เพิ่มโมดูลแบนเนอร์โปรโมชั่นไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="5a60f-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="5a60f-142">การเพิ่มโมดูลแบนเนอร์โปรโมชั่นไปยังหน้า และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5a60f-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5a60f-143">สร้างแม่แบบของหน้าซึ่งชื่อ **แม่แบบแบนเนอร์โปรโมชั่น**</span><span class="sxs-lookup"><span data-stu-id="5a60f-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="5a60f-144">ภายใต้ **โครงร่างเพจ** ให้เพิ่ม **Default page** ไปยังช่อง **เนื้อความ**</span><span class="sxs-lookup"><span data-stu-id="5a60f-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="5a60f-145">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a60f-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="5a60f-146">ใช้แม่แบบที่คุณเพิ่งสร้างขึ้นเพื่อสร้างหน้าที่ชื่อ **หน้าแบนเนอร์โปรโมชั่น**</span><span class="sxs-lookup"><span data-stu-id="5a60f-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="5a60f-147">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="5a60f-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="5a60f-148">ในบานหน้าต่างด้านขวา ให้ตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="5a60f-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="5a60f-149">ภายใต้ **โครงร่างเพจ** ให้เพิ่มโมดูลแบนเนอร์โปรโมชั่นไปยังโมดูลตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="5a60f-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="5a60f-150">ในการตั้งค่าสำหรับโมดูลแบนเนอร์ ให้เพิ่มข้อความแบนเนอร์หนึ่งข้อขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="5a60f-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="5a60f-151">แต่ละข้อความสามารถมีข้อความพร้อมกับลิงก์ได้</span><span class="sxs-lookup"><span data-stu-id="5a60f-151">Each message can have text together with a link.</span></span> <span data-ttu-id="5a60f-152">คุณสามารถแก้ไขคุณสมบัติอื่น ๆ ได้ เพื่อเลือกกำหนดโมดูลต่อไป</span><span class="sxs-lookup"><span data-stu-id="5a60f-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="5a60f-153">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="5a60f-153">Save and preview the page.</span></span> <span data-ttu-id="5a60f-154">ที่ด้านบนของหน้า คุณควรเห็นการแจ้งเตือนที่แสดงข้อความที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5a60f-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="5a60f-155">แก้ไขหน้าให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a60f-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="5a60f-156">โดยทั่วไปป้ายโฆษณาแบบโปรโมชั่นจะใช้ในช่องส่วนหัวของหน้า หรือช่องหัวข้อย่อย</span><span class="sxs-lookup"><span data-stu-id="5a60f-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5a60f-157">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5a60f-157">Additional resources</span></span>

[<span data-ttu-id="5a60f-158">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5a60f-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5a60f-159">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="5a60f-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="5a60f-160">โมดูลบล็อคข้อความ</span><span class="sxs-lookup"><span data-stu-id="5a60f-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="5a60f-161">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="5a60f-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="5a60f-162">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="5a60f-162">Video player module</span></span>](add-video-player.md)
