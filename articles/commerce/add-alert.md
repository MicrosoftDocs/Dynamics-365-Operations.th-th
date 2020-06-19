---
title: โมดูลแบนเนอร์โปรโมชั่น
description: หัวข้อนี้ครอบคลุมถึงโมดูลแบนเนอร์โปรโมชั่น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: dae824cdbaaf56f85f125c5f36aaa56171bbd6bc
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411376"
---
# <a name="promo-banner-module"></a><span data-ttu-id="bb364-103">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="bb364-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb364-104">หัวข้อนี้ครอบคลุมถึงโมดูลแบนเนอร์โปรโมชั่น และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb364-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bb364-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="bb364-105">Overview</span></span>

<span data-ttu-id="bb364-106">โมดูลแบนเนอร์โปรโมชั่นใช้เพื่อแสดงข้อความที่ให้ข้อมูลแบบอินไลน์บนหน้า</span><span class="sxs-lookup"><span data-stu-id="bb364-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="bb364-107">ผู้ใช้สามารถใช้เพื่อแสดงโปรโมชันทั้งไซต์ที่ปรากฏในหน้าทั้งหมดของไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="bb364-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="bb364-108">โมดูลแบนเนอร์โปรโมชั่นสนับสนุนข้อความตัวอักษรและลิงค์</span><span class="sxs-lookup"><span data-stu-id="bb364-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="bb364-109">ถ้ามีการเพิ่มข้อความหลายรายการในโมดูลแบนเนอร์โปรโมชั่น โมดูลจะกลายเป็นแบนเนอร์แบบวงล้อที่ให้ลูกค้าวนผ่านข้อความทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bb364-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="bb364-110">โมดูลแบนเนอร์โปรโมชั่นจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS) และสามารถวางบนหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="bb364-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="bb364-111">ตัวอย่างการใช้งานของแบนเนอร์โปรโมชั่นในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="bb364-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="bb364-112">แบนเนอร์โปรโมชั่นสามารถใช้ในส่วนหัวของไซต์ เพื่อแสดงข้อความหรือข้อความทั่วทั้งไซต์ เช่นเดียวกับในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bb364-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="bb364-113">"ยอดขายประจำปีสิ้นสุดในเวลา10วัน"</span><span class="sxs-lookup"><span data-stu-id="bb364-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="bb364-114">"ประหยัดอย่างมากกับโปรโมชัน Back to School</span><span class="sxs-lookup"><span data-stu-id="bb364-114">"Save big with back to school sale.</span></span> <span data-ttu-id="bb364-115">ซื้อตอนนี้ "</span><span class="sxs-lookup"><span data-stu-id="bb364-115">Shop Now."</span></span>

<span data-ttu-id="bb364-116">"ช้อปลดราคาในช่วง Thanksgiving"</span><span class="sxs-lookup"><span data-stu-id="bb364-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="bb364-117">รูปภาพต่อไปนี้แสดงตัวอย่างของแบนเนอร์โปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="bb364-117">The following image shows an example of a promo banner.</span></span>

![ตัวอย่างของโมดูลแบนเนอร์โปรโมชัน](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="bb364-119">คุณสมบัติโมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="bb364-119">Promo banner module properties</span></span>

| <span data-ttu-id="bb364-120">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="bb364-120">Property name</span></span>             | <span data-ttu-id="bb364-121">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="bb364-121">Value</span></span>                              | <span data-ttu-id="bb364-122">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb364-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="bb364-123">ข้อความแบนเนอร์</span><span class="sxs-lookup"><span data-stu-id="bb364-123">Banner messages</span></span>           | <span data-ttu-id="bb364-124">ข้อความและลิงก์</span><span class="sxs-lookup"><span data-stu-id="bb364-124">Text and links</span></span>                     | <span data-ttu-id="bb364-125">แถวของข้อความและลิงก์</span><span class="sxs-lookup"><span data-stu-id="bb364-125">An array of text and links.</span></span> |
| <span data-ttu-id="bb364-126">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bb364-126">Autoplay</span></span>                  | <span data-ttu-id="bb364-127">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="bb364-127">**True** or **False**</span></span>              | <span data-ttu-id="bb364-128">ค่าที่ระบุว่าข้อความจะถูกวนโดยอัตโนมัติหรือไม่ ถ้ามีการตั้งค่าคอนฟิกข้อความจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="bb364-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="bb364-129">ช่วงเวลาของการเปลี่ยนภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="bb364-129">Slide transition interval</span></span> | <span data-ttu-id="bb364-130">จำนวนมิลลิวินาที (ms)</span><span class="sxs-lookup"><span data-stu-id="bb364-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="bb364-131">ช่วงเวลาที่ใช้ในการวนผ่านข้อความ</span><span class="sxs-lookup"><span data-stu-id="bb364-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="bb364-132">อนุญาตให้ปิด</span><span class="sxs-lookup"><span data-stu-id="bb364-132">Allow dismiss</span></span>             | <span data-ttu-id="bb364-133">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="bb364-133">**True** or **False**</span></span>              | <span data-ttu-id="bb364-134">หากค่าถูกตั้งเป็น **จริง** ลูกค้าสามารถยกเลิกการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="bb364-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="bb364-135">แสดงตัวเลื่อนวงล้อ</span><span class="sxs-lookup"><span data-stu-id="bb364-135">Show carousel flipper</span></span>     | <span data-ttu-id="bb364-136">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="bb364-136">**True** or **False**</span></span>              | <span data-ttu-id="bb364-137">ค่าที่ระบุว่าควรจะแสดงตัวหมุนวงล้อหรือไม่ เพื่อให้ลูกค้าสามารถหมุนรายการแบนเนอร์หลายรายการด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="bb364-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="bb364-138">การปรับแนวข้อความ</span><span class="sxs-lookup"><span data-stu-id="bb364-138">Text alignment</span></span>            | <span data-ttu-id="bb364-139">**ขวา** **ซ้าย** หรือ **กึ่งกลาง**</span><span class="sxs-lookup"><span data-stu-id="bb364-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="bb364-140">การจัดแนวข้อความในโมดูลแบนเนอร์โปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="bb364-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="bb364-141">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="bb364-141">Link</span></span>                      | <span data-ttu-id="bb364-142">URL</span><span class="sxs-lookup"><span data-stu-id="bb364-142">A URL</span></span>                              | <span data-ttu-id="bb364-143">URL สำหรับลิงก์ทางเลือก</span><span class="sxs-lookup"><span data-stu-id="bb364-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="bb364-144">เพิ่มโมดูลแบนเนอร์โปรโมชั่นไปยังเพจ</span><span class="sxs-lookup"><span data-stu-id="bb364-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="bb364-145">การเพิ่มโมดูลแบนเนอร์โปรโมชั่นไปยังหน้า และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bb364-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="bb364-146">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="bb364-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="bb364-147">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตแบนเนอร์โปรโมชั่น** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bb364-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="bb364-148">ภายใต้ **โครงร่างเพจ** ให้เพิ่ม **Default page** ไปยังช่อง **เนื้อความ**</span><span class="sxs-lookup"><span data-stu-id="bb364-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="bb364-149">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="bb364-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="bb364-150">ใช้แม่แบบที่คุณเพิ่งสร้างขึ้นเพื่อสร้างหน้าที่ชื่อ **หน้าแบนเนอร์โปรโมชั่น**</span><span class="sxs-lookup"><span data-stu-id="bb364-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="bb364-151">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="bb364-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="bb364-152">ในบานหน้าต่างด้านขวา ให้ตั้งค่า **ความกว้าง** เป็น **เต็มคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="bb364-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="bb364-153">ภายใต้ **โครงร่างเพจ** ให้เพิ่มโมดูลแบนเนอร์โปรโมชั่นไปยังโมดูลตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="bb364-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="bb364-154">ในการตั้งค่าสำหรับโมดูลแบนเนอร์ ให้เพิ่มข้อความแบนเนอร์หนึ่งข้อขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="bb364-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="bb364-155">แต่ละข้อความสามารถมีข้อความพร้อมกับลิงก์ได้</span><span class="sxs-lookup"><span data-stu-id="bb364-155">Each message can have text together with a link.</span></span> <span data-ttu-id="bb364-156">คุณสามารถแก้ไขคุณสมบัติอื่น ๆ ได้ เพื่อเลือกกำหนดโมดูลต่อไป</span><span class="sxs-lookup"><span data-stu-id="bb364-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="bb364-157">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="bb364-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="bb364-158">ที่ด้านบนของหน้า คุณควรเห็นการแจ้งเตือนที่แสดงข้อความที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="bb364-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="bb364-159">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="bb364-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="bb364-160">โดยทั่วไปป้ายโฆษณาแบบโปรโมชั่นจะใช้ในช่องส่วนหัวของหน้า หรือช่องหัวข้อย่อย</span><span class="sxs-lookup"><span data-stu-id="bb364-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="bb364-161">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bb364-161">Additional resources</span></span>

[<span data-ttu-id="bb364-162">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bb364-162">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bb364-163">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="bb364-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="bb364-164">โมดูลบล็อคข้อความ</span><span class="sxs-lookup"><span data-stu-id="bb364-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="bb364-165">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="bb364-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="bb364-166">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="bb364-166">Video player module</span></span>](add-video-player.md)
