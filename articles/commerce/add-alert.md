---
title: โมดูลการแจ้งเตือน
description: หัวข้อนี้ครอบคลุมถึงโมดูลการแจ้งเตือน และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785363"
---
# <a name="alert-module"></a><span data-ttu-id="e61b5-103">โมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e61b5-104">หัวข้อนี้ครอบคลุมถึงโมดูลการแจ้งเตือน และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e61b5-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e61b5-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="e61b5-105">Overview</span></span>

<span data-ttu-id="e61b5-106">โมดูลการแจ้งเตือนใช้เพื่อแสดงข้อความที่ให้ข้อมูลแบบอินไลน์บนหน้า</span><span class="sxs-lookup"><span data-stu-id="e61b5-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="e61b5-107">โมดูลการแจ้งเตือนสนับสนุนข้อความตัวอักษรและลิงค์</span><span class="sxs-lookup"><span data-stu-id="e61b5-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="e61b5-108">ผู้ใช้สามารถใช้เพื่อแสดงโปรโมชันทั้งไซต์ที่ปรากฏในหน้าทั้งหมดของไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e61b5-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="e61b5-109">โมดูลการแจ้งเตือนจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS) และสามารถวางบนหน้าใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="e61b5-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="e61b5-110">ตัวอย่างของโมดูลการแจ้งเตือนในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e61b5-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="e61b5-111">โมดูลการแจ้งเตือนสามารถใช้ในส่วนหัวของไซต์ เพื่อบ่งชี้ว่ามีการส่งเสริมการตลาดหรือข้อความทั่วทั้งไซต์</span><span class="sxs-lookup"><span data-stu-id="e61b5-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="e61b5-112">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="e61b5-112">Here are some examples:</span></span>

<span data-ttu-id="e61b5-113">"ยอดขายประจำปีสิ้นสุดในเวลา10วัน"</span><span class="sxs-lookup"><span data-stu-id="e61b5-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="e61b5-114">"ประหยัดอย่างมากกับโปรโมชัน Back to School</span><span class="sxs-lookup"><span data-stu-id="e61b5-114">"Save big with back to school sale.</span></span> <span data-ttu-id="e61b5-115">ซื้อตอนนี้ "</span><span class="sxs-lookup"><span data-stu-id="e61b5-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="e61b5-116">คุณสมบัติของโมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-116">Alert module properties</span></span>

| <span data-ttu-id="e61b5-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="e61b5-117">Property name</span></span>  | <span data-ttu-id="e61b5-118">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="e61b5-118">Value</span></span>                              | <span data-ttu-id="e61b5-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e61b5-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="e61b5-120">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="e61b5-120">Text</span></span>           | <span data-ttu-id="e61b5-121">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="e61b5-121">Text</span></span>                               | <span data-ttu-id="e61b5-122">ข้อความตัวอักษรที่ปรากฏขึ้นในโมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="e61b5-123">การปรับแนวข้อความ</span><span class="sxs-lookup"><span data-stu-id="e61b5-123">Text alignment</span></span> | <span data-ttu-id="e61b5-124">**ขวา** **ซ้าย** หรือ **กึ่งกลาง**</span><span class="sxs-lookup"><span data-stu-id="e61b5-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="e61b5-125">ค่าที่กำหนดวิธีการจัดตำแหน่งข้อความไว้ในโมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="e61b5-126">ยกเลิกการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-126">Dismiss alert</span></span>  | <span data-ttu-id="e61b5-127">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="e61b5-127">**True** or **False**</span></span>              | <span data-ttu-id="e61b5-128">หากค่าถูกตั้งเป็น **จริง** ลูกค้าสามารถยกเลิกการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="e61b5-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="e61b5-129">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="e61b5-129">Link</span></span>           | <span data-ttu-id="e61b5-130">URL</span><span class="sxs-lookup"><span data-stu-id="e61b5-130">URL</span></span>                                | <span data-ttu-id="e61b5-131">URL สำหรับลิงก์ทางเลือก</span><span class="sxs-lookup"><span data-stu-id="e61b5-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="e61b5-132">เพิ่มโมดูลการแจ้งเตือนไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="e61b5-132">Add an alert module to a page</span></span> 

<span data-ttu-id="e61b5-133">การเพิ่มโมดูลการแจ้งเตือนไปยังหน้า และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e61b5-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e61b5-134">สร้างเท็มเพลตของหน้าซึ่งชื่อ **เท็มเพลตการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="e61b5-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="e61b5-135">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="e61b5-136">เช็คอินแม่แบบ และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="e61b5-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="e61b5-137">ใช้เท็มเพลตการแจ้งเตือนที่คุณเพิ่งสร้างขึ้นเพื่อสร้างหน้าที่ชื่อ **หน้าการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="e61b5-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="e61b5-138">ในช่อง **หลัก** ของหน้าใหม่ ให้เพิ่มโมดูลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="e61b5-139">ในการตั้งค่าสำหรับโมดูลการแจ้งเตือน ให้ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="e61b5-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="e61b5-140">คุณสามารถแก้ไขคุณสมบัติอื่นๆได้ถ้าคุณต้องการเลือกกำหนดโมดูลการแจ้งเตือนต่อไป</span><span class="sxs-lookup"><span data-stu-id="e61b5-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="e61b5-141">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="e61b5-141">Save and preview the page.</span></span> <span data-ttu-id="e61b5-142">ที่ด้านบนของหน้า คุณควรเห็นการแจ้งเตือนที่มีข้อความที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e61b5-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="e61b5-143">เช็คอินหน้า และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="e61b5-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e61b5-144">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e61b5-144">Additional resources</span></span>

[<span data-ttu-id="e61b5-145">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e61b5-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e61b5-146">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="e61b5-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e61b5-147">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="e61b5-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e61b5-148">โมดูลการจัดวางเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="e61b5-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e61b5-149">โมดูลคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e61b5-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e61b5-150">โมดูลฮีโร</span><span class="sxs-lookup"><span data-stu-id="e61b5-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="e61b5-151">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="e61b5-151">Video player module</span></span>](add-video-player.md)
